---
title: "Error Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a175d453-fa55-4f49-9ede-a26d83177919
caps.latest.revision: 8
caps.handback.revision: 8
manager: sonalm
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - zh-cn
  - zh-tw
---
# Error Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f5fafb6469e9e044910d3d57714f0bde" id="tgt1" class="tgtSentence">Contains details about data access errors that pertain to a single operation involving the provider.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="0db235f1047666c67c722de3017294ad" id="tgt2" class="tgtSentence">Any operation involving ADO objects can generate one or more provider errors.</caps:sentence>
            <caps:sentence sentenceid="4a07c2df8d8171c37beb2609955d87af" id="tgt3" class="tgtSentence"> As each error occurs, one or more <legacyBold>Error</legacyBold> objects are placed in the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="cbfef042ca08be00214b0b47e98192ea" id="tgt4" class="tgtSentence"> When another ADO operation generates an error, the <legacyBold>Errors</legacyBold> collection is cleared, and the new set of <legacyBold>Error</legacyBold> objects is placed in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="ded2638ab56cdc8d21a8dd7570607028" id="tgt5" class="tgtSentence">Each <legacyBold>Error</legacyBold> object represents a specific provider error, not an ADO error.</caps:sentence>
              <caps:sentence sentenceid="459e85cd84a5d6aeaa5d6bb1ce23934d" id="tgt6" class="tgtSentence"> ADO errors are exposed to the run-time exception-handling mechanism.</caps:sentence>
              <caps:sentence sentenceid="c38fd968c34546eed430fd2248fd6c80" id="tgt7" class="tgtSentence"> For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an <legacyBold>On Error</legacyBold> event and appear in the <legacyBold>Error</legacyBold> object.</caps:sentence>
              <caps:sentence sentenceid="0d9cf156864b4ff1d647ff095e8cf0f2" id="tgt8" class="tgtSentence"> For a complete list of ADO errors, see the <legacyLink xlink:href="9469ba3a-5e4f-4a10-bbb8-a51a6c9660ea">ErrorValueEnum</legacyLink> topic.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="2c8973386649c35887d0c2e88c4dac42" id="tgt9" class="tgtSentence">You can read an <legacyBold>Error</legacyBold> object's properties to obtain specific details about each error, including the following:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="6bdc707eede0bd0921e2a4730c5fc90b" id="tgt10" class="tgtSentence">The <legacyLink xlink:href="4b5d6790-6c29-42aa-bf78-d9cfb8ad7965">Description</legacyLink> property, which contains the text of the error.</caps:sentence>
                <caps:sentence sentenceid="73020ad75e8fc55a59e4deb3d75f570d" id="tgt11" class="tgtSentence"> This is the default property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5eafcb7ed9a56bf08df4fb6b1c29cf94" id="tgt12" class="tgtSentence">The <legacyLink xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number</legacyLink> property, which contains the <legacyBold>Long</legacyBold> integer value of the error constant.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0636750b2a3ceb80d0a0d9cedb9ea588" id="tgt13" class="tgtSentence">The <legacyLink xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source</legacyLink> property, which identifies the object that raised the error.</caps:sentence>
                <caps:sentence sentenceid="e37e3a6900bf12be251175315a4fda0d" id="tgt14" class="tgtSentence"> This is particularly useful when you have several <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection following a request to a data source.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4721241662fd01be95852f5c8b888fb3" id="tgt15" class="tgtSentence">The <legacyLink xlink:href="f9e25967-54b0-444d-af2a-0d2c75365d3e">SQLState</legacyLink> and <legacyLink xlink:href="b9b47e57-18a4-4186-aef5-5bd18d7b1d74">NativeError</legacyLink> properties, which provide information from SQL data sources.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ac69230e0a36a1870986e3b1bc57f9be" id="tgt16" class="tgtSentence">When a provider error occurs, it is placed in the <legacyBold>Errors</legacyBold> collection of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="d539cbd840a5c65e86ae22a207164fcb" id="tgt17" class="tgtSentence"> ADO supports the return of multiple errors by a single ADO operation to allow for error information specific to the provider.</caps:sentence>
            <caps:sentence sentenceid="e7888700069bfd3005ac5e17b4da3643" id="tgt18" class="tgtSentence"> To obtain this rich error information in an error handler, use the appropriate error-trapping features of the language or environment you are working with, then use nested loops to enumerate the properties of each <legacyBold>Error</legacyBold> object in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="666a80f310a6db0a87a495fa1e2505ea" id="tgt19" class="tgtSentence">
                <legacyBold>Microsoft Visual Basic and VBScript Users</legacyBold>   If there is no valid <legacyBold>Connection</legacyBold> object, you will need to retrieve error information from the <legacyBold>Error</legacyBold> object.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="5f225164b5bc892414298a79670ee9bb" id="tgt20" class="tgtSentence">Just as providers do, ADO clears the <legacyBold>OLE Error Info</legacyBold> object before making a call that could potentially generate a new provider error.</caps:sentence>
            <caps:sentence sentenceid="18b7f86fc5a7bb73e5fd671240c44b7a" id="tgt21" class="tgtSentence"> However, the <legacyBold>Errors</legacyBold> collection on the <legacyBold>Connection</legacyBold> object is cleared and populated only when the provider generates a new error, or when the <legacyLink xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear</legacyLink> method is called.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6f4b4844080ffcd57d47f3cfb89416e5" id="tgt22" class="tgtSentence">Some properties and methods return warnings that appear as <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection but do not halt a program's execution.</caps:sentence>
            <caps:sentence sentenceid="04ffca219e1b72701c8bcd9890ff7bcb" id="tgt23" class="tgtSentence"> Before you call the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> methods on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object; the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method on a <legacyBold>Connection</legacyBold> object; or set the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property on a <legacyBold>Recordset</legacyBold> object, call the <legacyBold>Clear</legacyBold> method on the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="62838da27d9c2b07a00f569aa949f4f8" id="tgt24" class="tgtSentence"> That way, you can read the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property of the <legacyBold>Errors</legacyBold> collection to test for returned warnings.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8aefda42a9a3aa31a88cbc4e8787210b" id="tgt25" class="tgtSentence">The <legacyBold>Error</legacyBold> object is not safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt26" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="cd69e4b7-82bf-4ffc-bc53-c535ba20161f">
                  <caps:sentence sentenceid="1e7656acdf13e86bc2ac0da92b25a23b" id="tgt27" class="tgtSentence">Error Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="5c728458-d85c-497c-afcf-2cfa36c3342a">Visual Basic Example</link>
        <link xlink:href="5321fc0f-cd0c-4e2a-a5bc-0008fba86b59">Visual C++ Example</link>
        <link xlink:href="7fd0eebc-99f4-490e-9b62-0b62b1884d6b">Visual J++ Example</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains details about data access errors that pertain to a single operation involving the provider.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Any operation involving ADO objects can generate one or more provider errors.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> As each error occurs, one or more <legacyBold>Error</legacyBold> objects are placed in the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> When another ADO operation generates an error, the <legacyBold>Errors</legacyBold> collection is cleared, and the new set of <legacyBold>Error</legacyBold> objects is placed in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src5" class="srcSentence">Each <legacyBold>Error</legacyBold> object represents a specific provider error, not an ADO error.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> ADO errors are exposed to the run-time exception-handling mechanism.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence"> For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an <legacyBold>On Error</legacyBold> event and appear in the <legacyBold>Error</legacyBold> object.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> For a complete list of ADO errors, see the <legacyLink xlink:href="9469ba3a-5e4f-4a10-bbb8-a51a6c9660ea">ErrorValueEnum</legacyLink> topic.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src9" class="srcSentence">You can read an <legacyBold>Error</legacyBold> object's properties to obtain specific details about each error, including the following:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">The <legacyLink xlink:href="4b5d6790-6c29-42aa-bf78-d9cfb8ad7965">Description</legacyLink> property, which contains the text of the error.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> This is the default property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">The <legacyLink xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number</legacyLink> property, which contains the <legacyBold>Long</legacyBold> integer value of the error constant.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">The <legacyLink xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source</legacyLink> property, which identifies the object that raised the error.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> This is particularly useful when you have several <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection following a request to a data source.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">The <legacyLink xlink:href="f9e25967-54b0-444d-af2a-0d2c75365d3e">SQLState</legacyLink> and <legacyLink xlink:href="b9b47e57-18a4-4186-aef5-5bd18d7b1d74">NativeError</legacyLink> properties, which provide information from SQL data sources.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src16" class="srcSentence">When a provider error occurs, it is placed in the <legacyBold>Errors</legacyBold> collection of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> ADO supports the return of multiple errors by a single ADO operation to allow for error information specific to the provider.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> To obtain this rich error information in an error handler, use the appropriate error-trapping features of the language or environment you are working with, then use nested loops to enumerate the properties of each <legacyBold>Error</legacyBold> object in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src19" class="srcSentence">
                <legacyBold>Microsoft Visual Basic and VBScript Users</legacyBold>   If there is no valid <legacyBold>Connection</legacyBold> object, you will need to retrieve error information from the <legacyBold>Error</legacyBold> object.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src20" class="srcSentence">Just as providers do, ADO clears the <legacyBold>OLE Error Info</legacyBold> object before making a call that could potentially generate a new provider error.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> However, the <legacyBold>Errors</legacyBold> collection on the <legacyBold>Connection</legacyBold> object is cleared and populated only when the provider generates a new error, or when the <legacyLink xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear</legacyLink> method is called.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">Some properties and methods return warnings that appear as <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection but do not halt a program's execution.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> Before you call the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> methods on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object; the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method on a <legacyBold>Connection</legacyBold> object; or set the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property on a <legacyBold>Recordset</legacyBold> object, call the <legacyBold>Clear</legacyBold> method on the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> That way, you can read the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property of the <legacyBold>Errors</legacyBold> collection to test for returned warnings.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">The <legacyBold>Error</legacyBold> object is not safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src26" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="cd69e4b7-82bf-4ffc-bc53-c535ba20161f">
                  <caps:sentence id="src27" class="srcSentence">Error Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="5c728458-d85c-497c-afcf-2cfa36c3342a">Visual Basic Example</link>
        <link xlink:href="5321fc0f-cd0c-4e2a-a5bc-0008fba86b59">Visual C++ Example</link>
        <link xlink:href="7fd0eebc-99f4-490e-9b62-0b62b1884d6b">Visual J++ Example</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
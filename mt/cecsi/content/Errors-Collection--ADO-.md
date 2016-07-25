---
title: "Errors Collection (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 290819e1-7b39-4e1e-a93b-801257138b00
caps.latest.revision: 9
caps.handback.revision: 9
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
# Errors Collection (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7d4685f8c7921d69799bff64f7c566f3" id="tgt1" class="tgtSentence">Contains all the <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> objects created in response to a single provider-related failure.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="0db235f1047666c67c722de3017294ad" id="tgt2" class="tgtSentence">Any operation involving ADO objects can generate one or more provider errors.</caps:sentence>
            <caps:sentence sentenceid="a46df822358d022b5b7cdca807725e87" id="tgt3" class="tgtSentence"> As each error occurs, one or more <legacyBold>Error</legacyBold> objects can be placed in the <legacyBold>Errors</legacyBold> collection of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="f73f20c26ba6248dada7dfe22c793de8" id="tgt4" class="tgtSentence"> When another ADO operation generates an error, the <legacyBold>Errors</legacyBold> collection is cleared, and the new set of <legacyBold>Error</legacyBold> objects can be placed in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ded2638ab56cdc8d21a8dd7570607028" id="tgt5" class="tgtSentence">Each <legacyBold>Error</legacyBold> object represents a specific provider error, not an ADO error.</caps:sentence>
            <caps:sentence sentenceid="459e85cd84a5d6aeaa5d6bb1ce23934d" id="tgt6" class="tgtSentence"> ADO errors are exposed to the run-time exception-handling mechanism.</caps:sentence>
            <caps:sentence sentenceid="4c35e8aed16e34acad841ba5bc63b02e" id="tgt7" class="tgtSentence"> For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an <legacyLink xlink:href="b01cbc62-fbd7-4068-b16c-8b0f80a05887">onError</legacyLink> event and appear in the <legacyBold>Err</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2497bf8e6c18f3ed7289f4863493ad1f" id="tgt8" class="tgtSentence">ADO operations that don't generate an error have no effect on the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="1d973c5e1e6dec50ab103909aeef652b" id="tgt9" class="tgtSentence"> Use the <legacyLink xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear</legacyLink> method to manually clear the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4b9ca9b4fe0652ed4b95f99281db22e5" id="tgt10" class="tgtSentence">The set of <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection describes all errors that occurred in response to a single statement.</caps:sentence>
            <caps:sentence sentenceid="5d42a0b70487d731cf8bffa9995fe55b" id="tgt11" class="tgtSentence"> Enumerating the specific errors in the <legacyBold>Errors</legacyBold> collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6f4b4844080ffcd57d47f3cfb89416e5" id="tgt12" class="tgtSentence">Some properties and methods return warnings that appear as <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection but do not halt a program's execution.</caps:sentence>
            <caps:sentence sentenceid="e4eb2c634eeb114d20e7a90cceaced84" id="tgt13" class="tgtSentence"> Before you call the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> methods on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method on a <legacyBold>Connection</legacyBold> object, or set the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property on a <legacyBold>Recordset</legacyBold> object, call the <legacyBold>Clear</legacyBold> method on the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="3453887de7e0bcd85ca7e406dd769b2a" id="tgt14" class="tgtSentence"> That way you can read the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property of the <legacyBold>Errors</legacyBold> collection to test for returned warnings.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="46ac366c9c413f7de5400657f02e3f2b" id="tgt15" class="tgtSentence">See the <legacyBold>Error</legacyBold> object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt16" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="6849bbe1eaef2266f2e2cec753f5dbbd" id="tgt17" class="tgtSentence">
                  <legacyLink xlink:href="606f2b92-3821-4d11-a207-4c22f6f35619">Errors Collection Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error Object</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all the <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> objects created in response to a single provider-related failure.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Any operation involving ADO objects can generate one or more provider errors.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> As each error occurs, one or more <legacyBold>Error</legacyBold> objects can be placed in the <legacyBold>Errors</legacyBold> collection of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> When another ADO operation generates an error, the <legacyBold>Errors</legacyBold> collection is cleared, and the new set of <legacyBold>Error</legacyBold> objects can be placed in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">Each <legacyBold>Error</legacyBold> object represents a specific provider error, not an ADO error.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> ADO errors are exposed to the run-time exception-handling mechanism.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an <legacyLink xlink:href="b01cbc62-fbd7-4068-b16c-8b0f80a05887">onError</legacyLink> event and appear in the <legacyBold>Err</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">ADO operations that don't generate an error have no effect on the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Use the <legacyLink xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear</legacyLink> method to manually clear the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">The set of <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection describes all errors that occurred in response to a single statement.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Enumerating the specific errors in the <legacyBold>Errors</legacyBold> collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">Some properties and methods return warnings that appear as <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection but do not halt a program's execution.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Before you call the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> methods on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method on a <legacyBold>Connection</legacyBold> object, or set the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property on a <legacyBold>Recordset</legacyBold> object, call the <legacyBold>Clear</legacyBold> method on the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> That way you can read the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property of the <legacyBold>Errors</legacyBold> collection to test for returned warnings.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src15" class="srcSentence">See the <legacyBold>Error</legacyBold> object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src16" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">
                  <legacyLink xlink:href="606f2b92-3821-4d11-a207-4c22f6f35619">Errors Collection Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error Object</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
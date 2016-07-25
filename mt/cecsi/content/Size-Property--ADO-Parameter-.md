---
title: "Size Property (ADO Parameter)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2
caps.latest.revision: 6
caps.handback.revision: 6
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
# Size Property (ADO Parameter)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="320d88fe8205d4c36889320b8e4dab05" id="tgt1" class="tgtSentence">Indicates the maximum size, in bytes or characters, of a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bd097796fb5db2a604b449ea0efd5259" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that indicates the maximum size in bytes or characters of a value in a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="01c7b21cb1a075cfda1a28dac9fbee5a" id="tgt4" class="tgtSentence">Use the <legacyBold>Size</legacyBold> property to determine the maximum size for values written to or read from the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property of a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="486485a77a718d0f8de7da09a230831a" id="tgt5" class="tgtSentence">If you specify a variable-length data type for a <legacyBold>Parameter</legacyBold> object (for example, any <legacyBold>String</legacyBold> type, such as <legacyBold>adVarChar</legacyBold>), you must set the object's <legacyBold>Size</legacyBold> property before appending it to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection; otherwise, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="43cc81928c71a75af51cf99810e580c3" id="tgt6" class="tgtSentence">If you have already appended the <legacyBold>Parameter</legacyBold> object to the <legacyBold>Parameters</legacyBold> collection of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object and you change its type to a variable-length data type, you must set the <legacyBold>Parameter</legacyBold> object's <legacyBold>Size</legacyBold> property before executing the <legacyBold>Command</legacyBold> object; otherwise, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="766ec81b4fecc716a37887b56f11a00c" id="tgt7" class="tgtSentence">If you use the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method to obtain parameter information from the provider and it returns one or more variable-length data type <legacyBold>Parameter</legacyBold> objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution.</caps:sentence>
            <caps:sentence sentenceid="7803b726d60bca4ee00eaf720c52cfc3" id="tgt8" class="tgtSentence"> To prevent an error, you should explicitly set the <legacyBold>Size</legacyBold> property for these parameters before executing the command.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3b2d23db9706a7e8e1da899d83c37c2c" id="tgt9" class="tgtSentence">The <legacyBold>Size</legacyBold> property is read/write.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dade4531-0bcc-4a52-8f86-b110ba2a3f9d">Visual Basic Example</link>
        <link xlink:href="0d9917c4-9ef0-4d7a-b4ce-4f1fa6ce1817">Visual C++ Example</link>
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++ Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
        <link xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size Property (ADO Stream)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the maximum size, in bytes or characters, of a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that indicates the maximum size in bytes or characters of a value in a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Size</legacyBold> property to determine the maximum size for values written to or read from the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property of a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">If you specify a variable-length data type for a <legacyBold>Parameter</legacyBold> object (for example, any <legacyBold>String</legacyBold> type, such as <legacyBold>adVarChar</legacyBold>), you must set the object's <legacyBold>Size</legacyBold> property before appending it to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection; otherwise, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">If you have already appended the <legacyBold>Parameter</legacyBold> object to the <legacyBold>Parameters</legacyBold> collection of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object and you change its type to a variable-length data type, you must set the <legacyBold>Parameter</legacyBold> object's <legacyBold>Size</legacyBold> property before executing the <legacyBold>Command</legacyBold> object; otherwise, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If you use the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method to obtain parameter information from the provider and it returns one or more variable-length data type <legacyBold>Parameter</legacyBold> objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> To prevent an error, you should explicitly set the <legacyBold>Size</legacyBold> property for these parameters before executing the command.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <legacyBold>Size</legacyBold> property is read/write.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dade4531-0bcc-4a52-8f86-b110ba2a3f9d">Visual Basic Example</link>
        <link xlink:href="0d9917c4-9ef0-4d7a-b4ce-4f1fa6ce1817">Visual C++ Example</link>
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++ Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
        <link xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size Property (ADO Stream)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
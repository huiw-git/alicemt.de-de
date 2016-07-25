---
title: "Description Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 4b5d6790-6c29-42aa-bf78-d9cfb8ad7965
caps.latest.revision: 10
caps.handback.revision: 10
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
# Description Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d451b57c61554dc839e01577b4c70108" id="tgt1" class="tgtSentence">Describes an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="eb839034971c25612a0af6e4c01818c9" id="tgt3" class="tgtSentence">Returns a <languageKeyword>String</languageKeyword> value that contains a description of the error.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="fbeb1f7b9ea35ba7df30739c0a75eb66" id="tgt4" class="tgtSentence">Use the <legacyBold>Description</legacyBold> property to obtain a short description of the error.</caps:sentence>
            <caps:sentence sentenceid="4f5b39f5d077914621d6f4e599470cd5" id="tgt5" class="tgtSentence"> Display this property to alert the user to an error that you cannot or do not want to handle.</caps:sentence>
            <caps:sentence sentenceid="c40b978787a87d22aa3f7e380b183ebb" id="tgt6" class="tgtSentence"> The string will come from either ADO or a provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="20f9ff1d9347b486ad3644808f26570b" id="tgt7" class="tgtSentence">Providers are responsible for passing specific error text to ADO.</caps:sentence>
            <caps:sentence sentenceid="9ded84668b7b3ba0048f8bb99b527b19" id="tgt8" class="tgtSentence"> ADO adds an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object to the <legacyBold>Errors</legacyBold> collection for each provider error or warning it receives.</caps:sentence>
            <caps:sentence sentenceid="9105d2cbfd3e59af900dd5fa70f4c4cd" id="tgt9" class="tgtSentence"> Enumerate the <legacyBold>Errors</legacyBold> collection to trace the errors that the provider passes.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5c728458-d85c-497c-afcf-2cfa36c3342a">Visual Basic Example</link>
        <link xlink:href="5321fc0f-cd0c-4e2a-a5bc-0008fba86b59">Visual C++ Example</link>
        <link xlink:href="7fd0eebc-99f4-490e-9b62-0b62b1884d6b">Visual J++ Example</link>
        <link xlink:href="2b9ef441-993c-44d4-8f87-fac0979dac1d">HelpContext, HelpFile Properties</link>
        <link xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number Property</link>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Describes an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>String</languageKeyword> value that contains a description of the error.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Description</legacyBold> property to obtain a short description of the error.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Display this property to alert the user to an error that you cannot or do not want to handle.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The string will come from either ADO or a provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">Providers are responsible for passing specific error text to ADO.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> ADO adds an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object to the <legacyBold>Errors</legacyBold> collection for each provider error or warning it receives.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Enumerate the <legacyBold>Errors</legacyBold> collection to trace the errors that the provider passes.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5c728458-d85c-497c-afcf-2cfa36c3342a">Visual Basic Example</link>
        <link xlink:href="5321fc0f-cd0c-4e2a-a5bc-0008fba86b59">Visual C++ Example</link>
        <link xlink:href="7fd0eebc-99f4-490e-9b62-0b62b1884d6b">Visual J++ Example</link>
        <link xlink:href="2b9ef441-993c-44d4-8f87-fac0979dac1d">HelpContext, HelpFile Properties</link>
        <link xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number Property</link>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
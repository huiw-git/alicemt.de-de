---
title: "EOS Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 57e08c5f-f3ed-4ecd-8c66-50b83b1031d1
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
# EOS Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="92fdf9a53d80299ac2691ec0a00d7bbb" id="tgt1" class="tgtSentence">Indicates whether the current position is at the end of the <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">stream</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f5378dc069d81152a749076929e7fa0e" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Boolean</languageKeyword> value that indicates whether the current position is at the end of the stream.</caps:sentence>
            <caps:sentence sentenceid="6a30576dfe15ee32e2e56f8c0147cfe8" id="tgt4" class="tgtSentence">
              <legacyBold>EOS</legacyBold> returns <legacyBold>True</legacyBold> if there are no more bytes in the stream; it returns <legacyBold>False</legacyBold> if there are more bytes following the current position.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="659c4afb17b23048a372432452a36b23" id="tgt5" class="tgtSentence">To set the end of stream position, use the <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="81e5751c84d574654c20df654a4bfec1" id="tgt6" class="tgtSentence"> To determine the current position, use the <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="77ce3042-9ebc-44ba-a4ff-0f1b1fd4a9c4">Visual Basic Example</link>
        <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates whether the current position is at the end of the <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">stream</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Boolean</languageKeyword> value that indicates whether the current position is at the end of the stream.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence">
              <legacyBold>EOS</legacyBold> returns <legacyBold>True</legacyBold> if there are no more bytes in the stream; it returns <legacyBold>False</legacyBold> if there are more bytes following the current position.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">To set the end of stream position, use the <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink> method.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> To determine the current position, use the <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="77ce3042-9ebc-44ba-a4ff-0f1b1fd4a9c4">Visual Basic Example</link>
        <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
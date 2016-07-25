---
title: "Type Property (ADO Stream)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f6a17e8c-7a28-48d0-bded-76b9e0cf7639
caps.latest.revision: 11
caps.handback.revision: 11
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
# Type Property (ADO Stream)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bacdde05f8bef2d66556a570b108e124" id="tgt1" class="tgtSentence">Indicates the type of data contained in the <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> (binary or text).</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d40a4c4654c3a47675de33cbe0c32b58" id="tgt3" class="tgtSentence">Sets or returns a <legacyLink xlink:href="220fe51d-4889-4020-a099-2ec9c7485503">StreamTypeEnum</legacyLink> value that specifies the type of data contained in the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="cc5a833b94d3271ecbdaab4cd58e9e0b" id="tgt4" class="tgtSentence"> The default value is <legacyBold>adTypeText</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="301688762f21f2c427ad35efba9abc25" id="tgt5" class="tgtSentence"> However, if binary data is initially written to a new, empty <legacyBold>Stream</legacyBold>, the <legacyBold>Type</legacyBold> will be changed to <legacyBold>adTypeBinary</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d7413af873fce7330e913782dfb37ae2" id="tgt6" class="tgtSentence">The <legacyBold>Type</legacyBold> property is read/write only when the current position is at the beginning of the <legacyBold>Stream </legacyBold>(<legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> is 0), and read-only at any other position.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="824765ed59f7b268764d8d13c66e1140" id="tgt7" class="tgtSentence">The <legacyBold>Type</legacyBold> property determines which methods should be used for reading and writing the <legacyBold>Stream</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="3f8ee48db66f73e33052e078a8c45470" id="tgt8" class="tgtSentence"> For text <legacyBold>Streams</legacyBold>, use <legacyLink xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">ReadText</legacyLink> and <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="9499a3764b0b906c7549b36e82e47bfa" id="tgt9" class="tgtSentence"> For binary <legacyBold>Streams</legacyBold>, use <legacyLink xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">Read</legacyLink> and <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="790e46a2-13d2-451e-a8be-130bd9a206a4">RecordType Property</link>
        <link xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the type of data contained in the <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> (binary or text).</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyLink xlink:href="220fe51d-4889-4020-a099-2ec9c7485503">StreamTypeEnum</legacyLink> value that specifies the type of data contained in the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>adTypeText</legacyBold>.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> However, if binary data is initially written to a new, empty <legacyBold>Stream</legacyBold>, the <legacyBold>Type</legacyBold> will be changed to <legacyBold>adTypeBinary</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">The <legacyBold>Type</legacyBold> property is read/write only when the current position is at the beginning of the <legacyBold>Stream </legacyBold>(<legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> is 0), and read-only at any other position.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <legacyBold>Type</legacyBold> property determines which methods should be used for reading and writing the <legacyBold>Stream</legacyBold>.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> For text <legacyBold>Streams</legacyBold>, use <legacyLink xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">ReadText</legacyLink> and <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> For binary <legacyBold>Streams</legacyBold>, use <legacyLink xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">Read</legacyLink> and <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="790e46a2-13d2-451e-a8be-130bd9a206a4">RecordType Property</link>
        <link xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
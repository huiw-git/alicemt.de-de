---
title: "SetEOS Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 707c18ca-6a56-4970-bbd6-ae1fb86a0b8a
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
# SetEOS Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="269857b16ce62889b25b604290b3b204" id="tgt1" class="tgtSentence">Sets the position that is the end of the stream.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
Stream.SetEOS</legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="5559e654a8ae2cbb80ad9a95f8327b1c" id="tgt2" class="tgtSentence">
              <legacyBold>SetEOS</legacyBold> updates the value of the <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink> property, by making the current <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> the end of the stream.</caps:sentence>
            <caps:sentence sentenceid="55edaeb79cd1050a4487e9801118040c" id="tgt3" class="tgtSentence"> Any bytes or characters following the current position are truncated.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="094d3fcc48de5996c92f14a592636658" id="tgt4" class="tgtSentence">Because <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink>, <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink>, and <legacyLink xlink:href="b4aa5714-916b-48b8-8b09-cc2708379602">CopyTo</legacyLink> do not truncate any extra values in existing <legacyBold>Stream</legacyBold> objects, you can truncate these bytes or characters by setting the new end-of-stream position with <legacyBold>SetEOS</legacyBold>.</caps:sentence>
          </para>
          <alert class="caution">
            <para>
              <caps:sentence sentenceid="7cf26c201182cd10b2341f414bee70b2" id="tgt5" class="tgtSentence">If you set <legacyBold>EOS</legacyBold> to a position before the actual end of the stream, you will lose all data after the new <legacyBold>EOS</legacyBold> position.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt6" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Sets the position that is the end of the stream.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
Stream.SetEOS</legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">
              <legacyBold>SetEOS</legacyBold> updates the value of the <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink> property, by making the current <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> the end of the stream.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Any bytes or characters following the current position are truncated.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">Because <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink>, <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink>, and <legacyLink xlink:href="b4aa5714-916b-48b8-8b09-cc2708379602">CopyTo</legacyLink> do not truncate any extra values in existing <legacyBold>Stream</legacyBold> objects, you can truncate these bytes or characters by setting the new end-of-stream position with <legacyBold>SetEOS</legacyBold>.</caps:sentence>
          </para>
          <alert class="caution">
            <para>
              <caps:sentence id="src5" class="srcSentence">If you set <legacyBold>EOS</legacyBold> to a position before the actual end of the stream, you will lose all data after the new <legacyBold>EOS</legacyBold> position.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
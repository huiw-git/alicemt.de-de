---
title: "Ordinal Property (ADO MD Cell)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a6001168-b954-47f0-ba0d-c05c4cc40c58
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
# Ordinal Property (ADO MD Cell)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9f444fcda0c5bc3c19b829c8d2104ddb" id="tgt1" class="tgtSentence">Uniquely identifies a <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">cell</legacyLink> by its position within a cellset.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4836b9c7f8adc96baae280626f9885f1" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> integer and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="5951dab69161388a99e033097ae3cac0" id="tgt4" class="tgtSentence">The cell's ordinal value uniquely identifies the cell within a cellset.</caps:sentence>
            <caps:sentence sentenceid="be4bebc9c9b47b25e7bb959ac74082d0" id="tgt5" class="tgtSentence"> Conceptually, cells are numbered in a cellset as if the cellset were a <legacyItalic>p</legacyItalic>-dimensional array, where <legacyItalic>p</legacyItalic> is the number of <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">axes</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="792e3be1fc5e443d26295078dd1613bb" id="tgt6" class="tgtSentence"> Cells are numbered starting from zero in row-major order.</caps:sentence>
            <caps:sentence sentenceid="df67c0bacf1bbaf45e6e3b5d04626748" id="tgt7" class="tgtSentence"> Here is the formula for calculating the ordinal number of a cell:</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f2cafe5a0532cc13a2779ed3b6a6b1c8" id="tgt8" class="tgtSentence">The cell's ordinal value can be used with the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property of the <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object to quickly retrieve the <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b4647211-2566-4657-ae7b-3dd761457d7b">VBScript Example</link>
        <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object</link>
        <link xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item Property (Cellset)</link>
        <link xlink:href="6efe8b5d-a2d5-43a9-a5ea-f9244f8d4ec9">Ordinal Property (Position)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Uniquely identifies a <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">cell</legacyLink> by its position within a cellset.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> integer and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The cell's ordinal value uniquely identifies the cell within a cellset.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Conceptually, cells are numbered in a cellset as if the cellset were a <legacyItalic>p</legacyItalic>-dimensional array, where <legacyItalic>p</legacyItalic> is the number of <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">axes</legacyLink>.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Cells are numbered starting from zero in row-major order.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Here is the formula for calculating the ordinal number of a cell:</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The cell's ordinal value can be used with the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property of the <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object to quickly retrieve the <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b4647211-2566-4657-ae7b-3dd761457d7b">VBScript Example</link>
        <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object</link>
        <link xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item Property (Cellset)</link>
        <link xlink:href="6efe8b5d-a2d5-43a9-a5ea-f9244f8d4ec9">Ordinal Property (Position)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
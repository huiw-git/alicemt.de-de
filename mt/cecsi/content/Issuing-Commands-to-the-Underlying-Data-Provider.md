---
title: "Issuing Commands to the Underlying Data Provider"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6001863-7733-4c32-817f-081e48587fa1
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
# Issuing Commands to the Underlying Data Provider
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bd97259e98d330df388b69e855ef7ea7" id="tgt1" class="tgtSentence">Any command that does not begin with SHAPE is passed through to the data provider.</caps:sentence>
          <caps:sentence sentenceid="9a78222690bf22be475abf6c31ad4dba" id="tgt2" class="tgtSentence"> This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</caps:sentence>
          <caps:sentence sentenceid="451a039257f46fa354baa2d3a2ce5bae" id="tgt3" class="tgtSentence"> These commands do <legacyItalic>not</legacyItalic> have to produce a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="54bd7390df4db0ab088c70d574b2f32a" id="tgt4" class="tgtSentence"> For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8269ae9e1906b843c4543373d8cc790a" id="tgt5" class="tgtSentence">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Any command that does not begin with SHAPE is passed through to the data provider.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> These commands do <legacyItalic>not</legacyItalic> have to produce a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
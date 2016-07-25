---
title: "Persisting Filtered and Hierarchical Recordsets"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d01aeb4d-4e43-450b-b3f2-0c27eaaf9f86
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
# Persisting Filtered and Hierarchical Recordsets
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="25d25b89353f151478d11ff6325efcf7" id="tgt1" class="tgtSentence">If the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property is in effect for the <legacyBold>Recordset</legacyBold>, only the rows accessible under the filter are saved.</caps:sentence>
          <caps:sentence sentenceid="13f40f777be81833c77c64c8f32e24d7" id="tgt2" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> is hierarchical, the current child <legacyBold>Recordset</legacyBold> and its children are saved, including the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="ad4ead59b7cf14196357145ce0eedb56" id="tgt3" class="tgtSentence"> If the <legacyBold>Save</legacyBold> method of a child <legacyBold>Recordset</legacyBold> is called, the child and all its children are saved, but the parent is not.</caps:sentence>
          <caps:sentence sentenceid="ca2675ea265c83caad125e598f8b9fbb" id="tgt4" class="tgtSentence"> For more information about hierarchical <legacyBold>Recordsets</legacyBold>, see <link xlink:href="62bd7dc9-45b5-4ca9-8b52-457325e0ce9e">Data Shaping</link>.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="5b13fe7db2d3977e8ac91e5bf50bd322" id="tgt5" class="tgtSentence">Some limitations apply when saving hierarchical <legacyBold>Recordsets</legacyBold> (data shapes) in XML format.</caps:sentence>
            <caps:sentence sentenceid="368c24e61ffd5eb9891524c2657f695d" id="tgt6" class="tgtSentence"> For more information, see <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">If the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property is in effect for the <legacyBold>Recordset</legacyBold>, only the rows accessible under the filter are saved.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> is hierarchical, the current child <legacyBold>Recordset</legacyBold> and its children are saved, including the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> If the <legacyBold>Save</legacyBold> method of a child <legacyBold>Recordset</legacyBold> is called, the child and all its children are saved, but the parent is not.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For more information about hierarchical <legacyBold>Recordsets</legacyBold>, see <link xlink:href="62bd7dc9-45b5-4ca9-8b52-457325e0ce9e">Data Shaping</link>.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src5" class="srcSentence">Some limitations apply when saving hierarchical <legacyBold>Recordsets</legacyBold> (data shapes) in XML format.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For more information, see <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
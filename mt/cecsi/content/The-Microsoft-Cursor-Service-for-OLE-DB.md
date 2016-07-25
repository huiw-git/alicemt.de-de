---
title: "The Microsoft Cursor Service for OLE DB"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ac3bd9b-2d45-4cc8-88ec-bd8a218cfb49
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
# The Microsoft Cursor Service for OLE DB
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="324bda5ed9c81c81ecbab474cfc8c42b" id="tgt1" class="tgtSentence">When you select a client-side cursor, or set the <legacyBold>CursorLocation</legacyBold> property to <legacyBold>adUseClient</legacyBold>, you are invoking the Microsoft Cursor Service for OLE DB.</caps:sentence>
          <caps:sentence sentenceid="a3f487c63c45133981f81077488a4ccf" id="tgt2" class="tgtSentence"> You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO.</caps:sentence>
          <caps:sentence sentenceid="9b26cfcfcdb37bbdfd762ec653442f1a" id="tgt3" class="tgtSentence"> This service supplements the cursor-support functions of data providers.</caps:sentence>
          <caps:sentence sentenceid="3e037b5d8144d0feb9f8746d94458cca" id="tgt4" class="tgtSentence"> As a result, you can perceive relatively uniform functionality from all data providers.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b7327aa6fceef1685012372f5e39b8c1" id="tgt5" class="tgtSentence">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods.</caps:sentence>
          <caps:sentence sentenceid="43000a4bab12e638558361ba2a77c4ac" id="tgt6" class="tgtSentence"> For example, the <legacyBold>Optimize</legacyBold> dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the <legacyBold>Find</legacyBold> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="dc07c463e9d3bf2990402a4ff15c9a54" id="tgt7" class="tgtSentence">The Cursor Service enables support for batch updating in all cases.</caps:sentence>
          <caps:sentence sentenceid="71b34842bd0a14fd1d55e63fe0edc98a" id="tgt8" class="tgtSentence"> It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">When you select a client-side cursor, or set the <legacyBold>CursorLocation</legacyBold> property to <legacyBold>adUseClient</legacyBold>, you are invoking the Microsoft Cursor Service for OLE DB.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This service supplements the cursor-support functions of data providers.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> As a result, you can perceive relatively uniform functionality from all data providers.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> For example, the <legacyBold>Optimize</legacyBold> dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the <legacyBold>Find</legacyBold> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">The Cursor Service enables support for batch updating in all cases.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
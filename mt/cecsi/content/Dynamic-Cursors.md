---
title: "Dynamic Cursors"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 00460f30-8cf7-494e-82df-41012f40ae51
caps.latest.revision: 5
caps.handback.revision: 5
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
# Dynamic Cursors
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ce135a5cda19fbf58e15d1e0736e65b1" id="tgt1" class="tgtSentence">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor.</caps:sentence>
          <caps:sentence sentenceid="bbc302856523d25442558423a04307b8" id="tgt2" class="tgtSentence"> All insert, update, and delete statements made by all users are visible through the cursor.</caps:sentence>
          <caps:sentence sentenceid="521bc54133d7e5e47d441fbef92dea79" id="tgt3" class="tgtSentence"> The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened.</caps:sentence>
          <caps:sentence sentenceid="c329ae6a38284a0a2f1d59920ff0c203" id="tgt4" class="tgtSentence"> Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e68b886ad08e527591e47dfeb747d016" id="tgt5" class="tgtSentence">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other.</caps:sentence>
          <caps:sentence sentenceid="512f3c5b542675fa41421efd91c73557" id="tgt6" class="tgtSentence"> If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1112cb394d57a85ecb88b2ddc82e2df6" id="tgt7" class="tgtSentence">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users.</caps:sentence>
          <caps:sentence sentenceid="76feeb183241c1d2585384256d62cb4a" id="tgt8" class="tgtSentence"> Use the <legacyBold>adOpenDynamic</legacyBold> <legacyBold>CursorTypeEnum</legacyBold> to indicate that you want to use a dynamic cursor in ADO.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</link>
        <link xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</link>
        <link xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> All insert, update, and delete statements made by all users are visible through the cursor.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Use the <legacyBold>adOpenDynamic</legacyBold> <legacyBold>CursorTypeEnum</legacyBold> to indicate that you want to use a dynamic cursor in ADO.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</link>
        <link xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</link>
        <link xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
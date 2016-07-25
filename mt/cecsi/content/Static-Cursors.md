---
title: "Static Cursors"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cce93ace-c4ed-4c6c-940c-28a50ff2fd12
caps.latest.revision: 4
caps.handback.revision: 4
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
# Static Cursors
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="76c964dbfa7712c2847bba6c2f6974d5" id="tgt1" class="tgtSentence">The static cursor always displays the result set as it was when the cursor was first opened.</caps:sentence>
          <caps:sentence sentenceid="9d17377e86b7e6618fdd65c8c0947ff8" id="tgt2" class="tgtSentence"> Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling.</caps:sentence>
          <caps:sentence sentenceid="c5e37154777d9d07332990417f0951f8" id="tgt3" class="tgtSentence"> The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened.</caps:sentence>
          <caps:sentence sentenceid="5539b2de01be3bb0860cfbb2886efcea" id="tgt4" class="tgtSentence"> Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="dfb6b37d22aad9e19a73e1c59a0e8b7a" id="tgt5" class="tgtSentence">Static cursors never detect other updates, deletes, and inserts.</caps:sentence>
          <caps:sentence sentenceid="7b16728f7a5c0d2252eb32231d1e2992" id="tgt6" class="tgtSentence"> For example, suppose a static cursor fetches a row, and another application then updates that row.</caps:sentence>
          <caps:sentence sentenceid="e75df90b3795f26be830047fcb45c89e" id="tgt7" class="tgtSentence"> If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application.</caps:sentence>
          <caps:sentence sentenceid="c82afb69187dd23a6d72d8c1176ed332" id="tgt8" class="tgtSentence"> All types of scrolling are supported, but providers may or may not support bookmarks.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="44561e77d79770b8b9b7e4c76589c537" id="tgt9" class="tgtSentence">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice.</caps:sentence>
          <caps:sentence sentenceid="c3d0dc7bedba7407e50c273d930f0b55" id="tgt10" class="tgtSentence"> Use the <legacyBold>adOpenStatic</legacyBold> <legacyBold>CursorTypeEnum</legacyBold> to indicate that you want to use a static cursor in ADO.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</link>
        <link xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</link>
        <link xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The static cursor always displays the result set as it was when the cursor was first opened.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">Static cursors never detect other updates, deletes, and inserts.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> For example, suppose a static cursor fetches a row, and another application then updates that row.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> All types of scrolling are supported, but providers may or may not support bookmarks.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> Use the <legacyBold>adOpenStatic</legacyBold> <legacyBold>CursorTypeEnum</legacyBold> to indicate that you want to use a static cursor in ADO.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</link>
        <link xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</link>
        <link xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
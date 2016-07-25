---
title: "Forward-Only Cursors"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b1e062f-3294-4a6f-8241-a17045c4df18
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
# Forward-Only Cursors
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4ac9198a46b44e5688bf49f709954e01" id="tgt1" class="tgtSentence">The typical default cursor type, called a forward-only (or non-scrollable) cursor, can move only forward through the result set.</caps:sentence>
          <caps:sentence sentenceid="cccfed57c42144a15994f094b3fc7f1e" id="tgt2" class="tgtSentence"> A forward-only cursor does not support scrolling (the ability to move forward and backward in the result set); it only supports fetching rows from the start to the end of the result set.</caps:sentence>
          <caps:sentence sentenceid="bca04ea0b6be1b05dec3b4c681df64ea" id="tgt3" class="tgtSentence"> With some forward-only cursors (such as with the SQL Server cursor library), all insert, update, and delete statements made by the current user (or committed by other users) that affect rows in the result set are visible as the rows are fetched.</caps:sentence>
          <caps:sentence sentenceid="96650978398bac4a90060c3b0f6581a2" id="tgt4" class="tgtSentence"> Because the cursor cannot be scrolled backward, however, changes made to rows in the database after the row was fetched are not visible through the cursor.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="80a3b659602d3ec6c549687df84f0594" id="tgt5" class="tgtSentence">After the data for the current row is processed, the forward-only cursor releases the resources that were used to hold that data.</caps:sentence>
          <caps:sentence sentenceid="de046090d1a05f88adcae915174351a1" id="tgt6" class="tgtSentence"> Forward-only cursors are dynamic by default, meaning that all changes are detected as the current row is processed.</caps:sentence>
          <caps:sentence sentenceid="0cd6197fcf4fd29a45326e32c93a9655" id="tgt7" class="tgtSentence"> This provides faster cursor opening and enables the result set to display updates made to the underlying tables.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1a4d3a6b111a1ee608349524414d3aae" id="tgt8" class="tgtSentence">While forward-only cursors do not support backward scrolling, your application can return to the beginning of the result set by closing and reopening the cursor.</caps:sentence>
          <caps:sentence sentenceid="edc5edbde4ba2ed3935545d8147786d0" id="tgt9" class="tgtSentence"> This is an effective way to work with small amounts of data.</caps:sentence>
          <caps:sentence sentenceid="a91a69862cdf740a4044e3988a3bc9c2" id="tgt10" class="tgtSentence"> As an alternative, your application could read the result set once, cache the data locally, and then browse the local data cache.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0857b926bce05ddcbbe109019ab7f810" id="tgt11" class="tgtSentence">If your application does not require scrolling through the result set, the forward-only cursor is the best way to retrieve data quickly with the least amount of overhead.</caps:sentence>
          <caps:sentence sentenceid="840c74bb8c51e141ef521422d7d50d20" id="tgt12" class="tgtSentence"> Use the <legacyBold>adOpenForwardOnly</legacyBold> <legacyBold>CursorTypeEnum</legacyBold> to indicate that you want to use a forward-only cursor in ADO.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</link>
        <link xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</link>
        <link xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The typical default cursor type, called a forward-only (or non-scrollable) cursor, can move only forward through the result set.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A forward-only cursor does not support scrolling (the ability to move forward and backward in the result set); it only supports fetching rows from the start to the end of the result set.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> With some forward-only cursors (such as with the SQL Server cursor library), all insert, update, and delete statements made by the current user (or committed by other users) that affect rows in the result set are visible as the rows are fetched.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Because the cursor cannot be scrolled backward, however, changes made to rows in the database after the row was fetched are not visible through the cursor.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">After the data for the current row is processed, the forward-only cursor releases the resources that were used to hold that data.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Forward-only cursors are dynamic by default, meaning that all changes are detected as the current row is processed.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> This provides faster cursor opening and enables the result set to display updates made to the underlying tables.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">While forward-only cursors do not support backward scrolling, your application can return to the beginning of the result set by closing and reopening the cursor.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> This is an effective way to work with small amounts of data.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> As an alternative, your application could read the result set once, cache the data locally, and then browse the local data cache.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">If your application does not require scrolling through the result set, the forward-only cursor is the best way to retrieve data quickly with the least amount of overhead.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Use the <legacyBold>adOpenForwardOnly</legacyBold> <legacyBold>CursorTypeEnum</legacyBold> to indicate that you want to use a forward-only cursor in ADO.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</link>
        <link xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</link>
        <link xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
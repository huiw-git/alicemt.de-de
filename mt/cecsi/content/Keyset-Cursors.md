---
title: "Keyset Cursors"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 14b51b17-6fd9-4146-af45-ca4b0fe6d48a
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
# Keyset Cursors
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="06f319d242804c71b01ac001ab687aeb" id="tgt1" class="tgtSentence">The keyset cursor provides functionality between a static and a dynamic cursor in its ability to detect changes.</caps:sentence>
          <caps:sentence sentenceid="ca47b973c537ee0b3af2800d1d3f589c" id="tgt2" class="tgtSentence"> Like a static cursor, it does not always detect changes to the membership and order of the result set.</caps:sentence>
          <caps:sentence sentenceid="481cea91c3e73cec9dd06f0918984c86" id="tgt3" class="tgtSentence"> Like a dynamic cursor, it does detect changes to the values of rows in the result set.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7d89bcdbfbfb364a148bf1f149469100" id="tgt4" class="tgtSentence">Keyset-driven cursors are controlled by a set of unique identifiers (keys) known as the keyset.</caps:sentence>
          <caps:sentence sentenceid="4ced5bf3fd8de15e0ccb52c78ea9c036" id="tgt5" class="tgtSentence"> The keys are built from a set of columns that uniquely identify the rows in the result set.</caps:sentence>
          <caps:sentence sentenceid="f732ccb290ea235e0faa453ebe4a17f6" id="tgt6" class="tgtSentence"> The keyset is the set of key values from all the rows returned by the query statement.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="07f19bb3f0059206374366058a32bc57" id="tgt7" class="tgtSentence">With keyset-driven cursors, a key is built and saved for each row in the cursor and stored either on the client workstation or on the server.</caps:sentence>
          <caps:sentence sentenceid="7d3af6db46250e9ed1eb40d83487c175" id="tgt8" class="tgtSentence"> When you access each row, the stored key is used to fetch the current data values from the data source.</caps:sentence>
          <caps:sentence sentenceid="7f0fe912fdf5775ef30bbc85d3e73080" id="tgt9" class="tgtSentence"> In a keyset-driven cursor, result set membership is frozen when the keyset is fully populated.</caps:sentence>
          <caps:sentence sentenceid="5eea5847826e2ae62469b81be26cb71e" id="tgt10" class="tgtSentence"> Thereafter, additions or updates that affect membership are not a part of the result set until it is reopened.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a809c8d157abbc33604777b023c403ca" id="tgt11" class="tgtSentence">Changes to data values (made either by the keyset owner or other processes) are visible as the user scrolls through the result set.</caps:sentence>
          <caps:sentence sentenceid="53cf341879e3b74f374b934d50c699ed" id="tgt12" class="tgtSentence"> Inserts made outside the cursor (by other processes) are visible only if the cursor is closed and reopened.</caps:sentence>
          <caps:sentence sentenceid="924ebd8d986d7defbf086dd513ffb2dd" id="tgt13" class="tgtSentence"> Inserts made from inside the cursor are visible at the end of the result set.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="27366558a10dc65b436444e39e3136e9" id="tgt14" class="tgtSentence">When a keyset-driven cursor attempts to retrieve a row that has been deleted, the row appears as a "hole" in the result set.</caps:sentence>
          <caps:sentence sentenceid="3076d23fb97ba2f0dbcda6b3330196be" id="tgt15" class="tgtSentence"> The key for the row exists in the keyset, but the row no longer exists in the result set.</caps:sentence>
          <caps:sentence sentenceid="73aad073be4b33118f2562bb2421f47e" id="tgt16" class="tgtSentence"> If the key values in a row are updated, the row is considered to have been deleted and then inserted, so such rows also appear as holes in the result set.</caps:sentence>
          <caps:sentence sentenceid="5d2974f3b6cc7a972b45f12c080e8a3f" id="tgt17" class="tgtSentence"> While a keyset-driven cursor can always detect rows deleted by other processes, it can optionally remove the keys for rows it deletes itself.</caps:sentence>
          <caps:sentence sentenceid="55daa74b3d486bddd25298d8e0e6f572" id="tgt18" class="tgtSentence"> Keyset-driven cursors that do this cannot detect their own deletes because the evidence has been removed.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="88265a1e3cd7a4f765847b95889c66fd" id="tgt19" class="tgtSentence">An update to a key column operates like a delete of the old key followed by an insert of the new key.</caps:sentence>
          <caps:sentence sentenceid="f0e8d5886f9a61e184a75452d29497a9" id="tgt20" class="tgtSentence"> The new key value is not visible if the update was not made through the cursor.</caps:sentence>
          <caps:sentence sentenceid="301904ba176002134c7e9ab32e261c51" id="tgt21" class="tgtSentence"> If the update was made through the cursor, the new key value is visible at the end of the result set.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="feaa31252b5597f4ffd6b5684c14cf21" id="tgt22" class="tgtSentence">There is a variation on keyset-driven cursors called keyset-driven standard cursors.</caps:sentence>
          <caps:sentence sentenceid="755ebe8eebdc22d814de9fb8968d0aff" id="tgt23" class="tgtSentence"> In a keyset-driven standard cursor, the membership of rows in the result set and the order of the rows are fixed at cursor open time, but changes to values that are made by the cursor owner and committed changes made by other processes are visible.</caps:sentence>
          <caps:sentence sentenceid="d787c10ddea9bc6d6d13c4afe3d36ab3" id="tgt24" class="tgtSentence"> If a change disqualifies a row for membership or affects the order of a row, the row does not disappear or move unless the cursor is closed and reopened.</caps:sentence>
          <caps:sentence sentenceid="c2c7fe1455e33853aa118773f20f7d91" id="tgt25" class="tgtSentence"> Inserted data does not appear, but changes to existing data do appear as the rows are fetched.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2f9e15ef068d7035d48b64e45b24e528" id="tgt26" class="tgtSentence">The keyset-driven cursor is difficult to use correctly because the sensitivity to data changes depends on many differing circumstances, as described above.</caps:sentence>
          <caps:sentence sentenceid="f0dee9d28335d33840e7848a4b2760c7" id="tgt27" class="tgtSentence"> However, if your application is not concerned with concurrent updates, can programmatically handle bad keys, and must directly access certain keyed rows, the keyset-driven cursor might work for you.</caps:sentence>
          <caps:sentence sentenceid="d6d7eb7dc9c1fa68065dbb900c89e0ee" id="tgt28" class="tgtSentence"> Use the <legacyBold>adOpenKeyset</legacyBold> <legacyBold>CursorTypeEnum</legacyBold> to indicate that you want to use a keyset cursor in ADO.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</link>
        <link xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</link>
        <link xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The keyset cursor provides functionality between a static and a dynamic cursor in its ability to detect changes.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Like a static cursor, it does not always detect changes to the membership and order of the result set.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Like a dynamic cursor, it does detect changes to the values of rows in the result set.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">Keyset-driven cursors are controlled by a set of unique identifiers (keys) known as the keyset.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> The keys are built from a set of columns that uniquely identify the rows in the result set.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The keyset is the set of key values from all the rows returned by the query statement.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">With keyset-driven cursors, a key is built and saved for each row in the cursor and stored either on the client workstation or on the server.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> When you access each row, the stored key is used to fetch the current data values from the data source.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> In a keyset-driven cursor, result set membership is frozen when the keyset is fully populated.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> Thereafter, additions or updates that affect membership are not a part of the result set until it is reopened.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">Changes to data values (made either by the keyset owner or other processes) are visible as the user scrolls through the result set.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Inserts made outside the cursor (by other processes) are visible only if the cursor is closed and reopened.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> Inserts made from inside the cursor are visible at the end of the result set.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">When a keyset-driven cursor attempts to retrieve a row that has been deleted, the row appears as a "hole" in the result set.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> The key for the row exists in the keyset, but the row no longer exists in the result set.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> If the key values in a row are updated, the row is considered to have been deleted and then inserted, so such rows also appear as holes in the result set.</caps:sentence>
          <caps:sentence id="src17" class="srcSentence"> While a keyset-driven cursor can always detect rows deleted by other processes, it can optionally remove the keys for rows it deletes itself.</caps:sentence>
          <caps:sentence id="src18" class="srcSentence"> Keyset-driven cursors that do this cannot detect their own deletes because the evidence has been removed.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src19" class="srcSentence">An update to a key column operates like a delete of the old key followed by an insert of the new key.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> The new key value is not visible if the update was not made through the cursor.</caps:sentence>
          <caps:sentence id="src21" class="srcSentence"> If the update was made through the cursor, the new key value is visible at the end of the result set.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src22" class="srcSentence">There is a variation on keyset-driven cursors called keyset-driven standard cursors.</caps:sentence>
          <caps:sentence id="src23" class="srcSentence"> In a keyset-driven standard cursor, the membership of rows in the result set and the order of the rows are fixed at cursor open time, but changes to values that are made by the cursor owner and committed changes made by other processes are visible.</caps:sentence>
          <caps:sentence id="src24" class="srcSentence"> If a change disqualifies a row for membership or affects the order of a row, the row does not disappear or move unless the cursor is closed and reopened.</caps:sentence>
          <caps:sentence id="src25" class="srcSentence"> Inserted data does not appear, but changes to existing data do appear as the rows are fetched.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src26" class="srcSentence">The keyset-driven cursor is difficult to use correctly because the sensitivity to data changes depends on many differing circumstances, as described above.</caps:sentence>
          <caps:sentence id="src27" class="srcSentence"> However, if your application is not concerned with concurrent updates, can programmatically handle bad keys, and must directly access certain keyed rows, the keyset-driven cursor might work for you.</caps:sentence>
          <caps:sentence id="src28" class="srcSentence"> Use the <legacyBold>adOpenKeyset</legacyBold> <legacyBold>CursorTypeEnum</legacyBold> to indicate that you want to use a keyset cursor in ADO.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</link>
        <link xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</link>
        <link xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
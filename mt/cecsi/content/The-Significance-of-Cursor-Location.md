---
title: "The Significance of Cursor Location"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70ef5b1c-0459-41a1-b796-031f61a29a8a
caps.latest.revision: 8
caps.handback.revision: 8
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
# The Significance of Cursor Location
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="460208b33e95576696d529c1e53a475b" id="tgt1" class="tgtSentence">Every cursor uses temporary resources to hold its data.</caps:sentence>
          <caps:sentence sentenceid="d87ffd2a8f07bad56751b3feb021d45f" id="tgt2" class="tgtSentence"> These resources can be memory, a disk paging file, temporary disk files, or even temporary storage in the database.</caps:sentence>
          <caps:sentence sentenceid="aa314354d5116e0f139cf162041b995a" id="tgt3" class="tgtSentence"> The cursor is called a <legacyItalic>client-side</legacyItalic> cursor when these resources are located on the client computer.</caps:sentence>
          <caps:sentence sentenceid="bdfdbf8096f38261097f203c2d5ba4d2" id="tgt4" class="tgtSentence"> The cursor is called a <legacyItalic>server-side</legacyItalic> cursor when these resources are located on the server.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="44bf6f82b5429eea3b2643271d73b954" id="tgt5" class="tgtSentence">Client-Side Cursors</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c0d2aedfb9b919ff1973002431ee8367" id="tgt6" class="tgtSentence">In ADO, call for a client-side cursor by using the <legacyBold>adUseClient</legacyBold> <legacyBold>CursorLocationEnum.</legacyBold> With a non-keyset client-side cursor, the server sends the entire result set across the network to the client computer.</caps:sentence>
            <caps:sentence sentenceid="59f0eb64ad7a11a78dd00d6a7129a4ad" id="tgt7" class="tgtSentence"> The client computer provides and manages the temporary resources needed by the cursor and result set.</caps:sentence>
            <caps:sentence sentenceid="c639a6451d9b30c8248540c68aebd062" id="tgt8" class="tgtSentence"> The client-side application can browse through the entire result set to determine which rows it requires.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="20c409dcd779b51651d850438c494bf9" id="tgt9" class="tgtSentence">Static and keyset-driven client-side cursors may place a significant load on your workstation if they include too many rows.</caps:sentence>
            <caps:sentence sentenceid="0d5d5742794458297d2dfd45a6185d13" id="tgt10" class="tgtSentence"> While all of the cursor libraries are capable of building cursors with thousands of rows, applications designed to fetch such large rowsets may perform poorly.</caps:sentence>
            <caps:sentence sentenceid="0f0cac5d97b9bdcaaffc353249d86956" id="tgt11" class="tgtSentence"> There are exceptions, of course.</caps:sentence>
            <caps:sentence sentenceid="6d9ce17f44c1c4f1086ab0a3a6705b90" id="tgt12" class="tgtSentence"> For some applications, a large client-side cursor might be perfectly appropriate and performance might not be an issue.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a5ce123545d3d54acb4b25da41b387d4" id="tgt13" class="tgtSentence">One obvious benefit of the client-side cursor is quick response.</caps:sentence>
            <caps:sentence sentenceid="61d69fc60bd03600c3a163c24a5ad352" id="tgt14" class="tgtSentence"> After the result set has been downloaded to the client computer, browsing through the rows is very fast.</caps:sentence>
            <caps:sentence sentenceid="8540df0c6b1558fee7344837e293ac0d" id="tgt15" class="tgtSentence"> Your application is generally more scalable with client-side cursors because the cursor's resource requirements are placed on each separate client and not on the server.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="eb0e23cd56523f85e87d44bce0d1d881" id="tgt16" class="tgtSentence">Server-Side Cursors</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5670004f81603b44afdaa97be6d09544" id="tgt17" class="tgtSentence">In ADO, call for a server-side cursor by using the <legacyBold>adUseServer</legacyBold> <legacyBold>CursorLocationEnum.</legacyBold> With a server-side cursor, the server manages the result set using resources provided by the server computer.</caps:sentence>
            <caps:sentence sentenceid="b5005f4d7878d3119d907877fca74d74" id="tgt18" class="tgtSentence"> The server-side cursor returns only the requested data over the network.</caps:sentence>
            <caps:sentence sentenceid="524cfaabffab14175427d34e6315c7b0" id="tgt19" class="tgtSentence"> This type of cursor can sometimes provide better performance than the client-side cursor, especially in situations where excessive network traffic is a problem.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="eb61d9fa746397c6330f7afb5d91de75" id="tgt20" class="tgtSentence">However, it is important to point out that a server-side cursor is — at least temporarily — consuming precious server resources for every active client.</caps:sentence>
            <caps:sentence sentenceid="1c9c31f25dd61251d4f259c5fee17261" id="tgt21" class="tgtSentence"> You must plan accordingly to ensure that your server hardware is capable of managing all of the server-side cursors requested by active clients.</caps:sentence>
            <caps:sentence sentenceid="ea1ff650d62a1e6b2b58007361b86a36" id="tgt22" class="tgtSentence"> Also, a server-side cursor can be slow because it provides only single row access — there is no batch cursor available.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="43c2df1c8c2b4b26f7ed0649f4b7d904" id="tgt23" class="tgtSentence">Server-side cursors are useful when inserting, updating, or deleting records.</caps:sentence>
            <caps:sentence sentenceid="3909bd3bbe44fca000759db9d10d943e" id="tgt24" class="tgtSentence"> With server-side cursors, you can have multiple active statements on the same connection.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Every cursor uses temporary resources to hold its data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These resources can be memory, a disk paging file, temporary disk files, or even temporary storage in the database.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The cursor is called a <legacyItalic>client-side</legacyItalic> cursor when these resources are located on the client computer.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The cursor is called a <legacyItalic>server-side</legacyItalic> cursor when these resources are located on the server.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Client-Side Cursors</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">In ADO, call for a client-side cursor by using the <legacyBold>adUseClient</legacyBold> <legacyBold>CursorLocationEnum.</legacyBold> With a non-keyset client-side cursor, the server sends the entire result set across the network to the client computer.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The client computer provides and manages the temporary resources needed by the cursor and result set.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The client-side application can browse through the entire result set to determine which rows it requires.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">Static and keyset-driven client-side cursors may place a significant load on your workstation if they include too many rows.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> While all of the cursor libraries are capable of building cursors with thousands of rows, applications designed to fetch such large rowsets may perform poorly.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> There are exceptions, of course.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> For some applications, a large client-side cursor might be perfectly appropriate and performance might not be an issue.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">One obvious benefit of the client-side cursor is quick response.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> After the result set has been downloaded to the client computer, browsing through the rows is very fast.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Your application is generally more scalable with client-side cursors because the cursor's resource requirements are placed on each separate client and not on the server.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Server-Side Cursors</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">In ADO, call for a server-side cursor by using the <legacyBold>adUseServer</legacyBold> <legacyBold>CursorLocationEnum.</legacyBold> With a server-side cursor, the server manages the result set using resources provided by the server computer.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> The server-side cursor returns only the requested data over the network.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> This type of cursor can sometimes provide better performance than the client-side cursor, especially in situations where excessive network traffic is a problem.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">However, it is important to point out that a server-side cursor is — at least temporarily — consuming precious server resources for every active client.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> You must plan accordingly to ensure that your server hardware is capable of managing all of the server-side cursors requested by active clients.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Also, a server-side cursor can be slow because it provides only single row access — there is no batch cursor available.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">Server-side cursors are useful when inserting, updating, or deleting records.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> With server-side cursors, you can have multiple active statements on the same connection.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
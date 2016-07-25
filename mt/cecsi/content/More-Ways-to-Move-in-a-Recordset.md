---
title: "More Ways to Move in a Recordset"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9f8cf1b2-3def-453f-a0ff-4646c5f15262
caps.latest.revision: 10
caps.handback.revision: 10
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
# More Ways to Move in a Recordset
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="94d48d76d904ba612ae2286b870fe7ae" id="tgt1" class="tgtSentence">The following four methods are used to move around, or scroll, in the <legacyBold>Recordset</legacyBold>: <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="2fbef81a89bdcc708284b7c69983c125" id="tgt2" class="tgtSentence"> (Some of these methods are unavailable on forward-only cursors.)</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c2636e6c2aab06f7db7ea9edb79b7727" id="tgt3" class="tgtSentence">         <legacyBold>MoveFirst</legacyBold> changes the current record position to the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="5a86d2f5634e7fd2dffb97be7d74e2e4" id="tgt4" class="tgtSentence">
            <legacyBold>MoveLast</legacyBold> changes the current record position to the last record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="49ecb40b8b7f998eb9da0f42225144ff" id="tgt5" class="tgtSentence"> To use <legacyBold>MoveFirst</legacyBold> or <legacyBold>MoveLast</legacyBold>, the <legacyBold>Recordset</legacyBold> object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1e74387bf9d1094432b08343710c7f25" id="tgt6" class="tgtSentence">         <legacyBold>MoveNext</legacyBold> moves the current record position one place forward.</caps:sentence>
          <caps:sentence sentenceid="566c8555cc692eb9cc789422fca1c8f3" id="tgt7" class="tgtSentence"> If you are on the last record when you call <legacyBold>MoveNext</legacyBold>, <legacyBold>EOF</legacyBold> will be set to <legacyBold>True</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="9a9c7eadc2531411dc910a06b629d803" id="tgt8" class="tgtSentence">
            <legacyBold>MovePrevious</legacyBold> moves the current record position one place backward.</caps:sentence>
          <caps:sentence sentenceid="6d074d5f0fa189ce451fb5ad8aa0ecc7" id="tgt9" class="tgtSentence"> If you are on the first record when you call <legacyBold>MovePrevious</legacyBold>, <legacyBold>BOF</legacyBold> will be set to <legacyBold>True</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="7428b8f89d81dc88dcff3f1c5fc14784" id="tgt10" class="tgtSentence"> It is wise to check the <legacyBold>EOF</legacyBold> and <legacyBold>BOF</legacyBold> properties when using these methods and to move the cursor back to a valid current record position if you move off either end of the <legacyBold>Recordset</legacyBold>, as shown here:</caps:sentence>
        </para>
        <code>. . .
oRs.MoveNext
If oRs.EOF Then oRs.MoveLast
. . . </code>
        <para>
          <caps:sentence sentenceid="a1b61163d00c2079b211101e17de2888" id="tgt11" class="tgtSentence">Or, in the case of the <legacyBold>MovePrevious</legacyBold> method:</caps:sentence>
        </para>
        <code>. . . 
oRs.MovePrevious
If oRs.BOF Then oRs.MoveFirst
. . .</code>
        <para>
          <caps:sentence sentenceid="a83a0d7d8dc4dbda100f709ff5569b48" id="tgt12" class="tgtSentence">In cases where the <legacyBold>Recordset</legacyBold> has been filtered or sorted and the current record's data is changed, the position may also change.</caps:sentence>
          <caps:sentence sentenceid="34495f19d9550b7c8a331f2ad5e70eac" id="tgt13" class="tgtSentence"> In such cases the <legacyBold>MoveNext</legacyBold> method works normally, but be aware that the position is moved one record forward from the new position, not the old position.</caps:sentence>
          <caps:sentence sentenceid="4c2252ae86ba0ea97865aa47dfd31ed9" id="tgt14" class="tgtSentence"> For example, changing the data in the current record, such that the record is moved to the end of the sorted <legacyBold>Recordset</legacyBold>, would mean that calling <legacyBold>MoveNext</legacyBold> results in ADO setting the current record to the position after the last record in the <legacyBold>Recordset</legacyBold> (<legacyBold>EOF</legacyBold> = <legacyBold>True</legacyBold>).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="6d01fae9e3a8326ffbad7a00241836df" id="tgt15" class="tgtSentence">The behavior of the various Move methods of the <legacyBold>Recordset</legacyBold> object depends, to some extent, on the data within the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="1132e1431ab92207f736394b5bc35ab0" id="tgt16" class="tgtSentence"> New records added to the <legacyBold>Recordset</legacyBold> are initially added in a particular order, which is defined by the data source and may be dependent implicitly or explicitly on the data in the new record.</caps:sentence>
          <caps:sentence sentenceid="0feb10a799ab04f845c3a3d5466517c0" id="tgt17" class="tgtSentence"> For example, if a sort or a join is done within the query that populates the <legacyBold>Recordset</legacyBold>, the new record will be inserted in the appropriate place within the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="902570194a87ffaa8ececa2e60aa2b28" id="tgt18" class="tgtSentence"> If ordering is not explicitly specified when creating the <legacyBold>Recordset</legacyBold>, changes in the data source implementation may cause the ordering of the returned rows to change inadvertently.</caps:sentence>
          <caps:sentence sentenceid="0bb6007f9f2099cf64a7b2427d7ee9aa" id="tgt19" class="tgtSentence"> In addition, the sorting, filtering, and editing functions of the <legacyBold>Recordset</legacyBold> can affect the order and possibly which rows in the recordset will be visible.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fb03285ffb38734bac128b7993c3ce65" id="tgt20" class="tgtSentence">Therefore, <legacyBold>MoveNext</legacyBold>, <legacyBold>MovePrevious</legacyBold>, <legacyBold>MoveFirst</legacyBold>, <legacyBold>MoveLast</legacyBold>, and <legacyBold>Move</legacyBold> are all sensitive to other operations performed on the same <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="20bd0f7d9ca4c0fa6fe2a8cfa6335a33" id="tgt21" class="tgtSentence"> ADO will always try to maintain your current position until you explicitly move it, but sometimes, intervening changes make it difficult to understand the effects of a subsequent move.</caps:sentence>
          <caps:sentence sentenceid="26689da1dc681da2d478a6a7991fb053" id="tgt22" class="tgtSentence"> For example, if you call <legacyBold>MoveFirst</legacyBold> to position on the first row of a sorted <legacyBold>Recordset</legacyBold> and you change the sort from ascending order to descending order, you are still on the same row — but now it is the last row in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="c7787f786a6b83a80d72db23908e63b0" id="tgt23" class="tgtSentence">
            <legacyBold>MoveFirst</legacyBold> will take you to a different row (the new first row).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9c1f78b56142311d8fc3341921ed10df" id="tgt24" class="tgtSentence">As another example, if you are positioned on a particular row in the middle of a <legacyBold>Recordset</legacyBold> and you call <legacyBold>Delete</legacyBold> and then call <legacyBold>MoveNext</legacyBold>, you are now on the record immediately following the deleted record.</caps:sentence>
          <caps:sentence sentenceid="62e33e2ebaa413f2404bdd8610f3d448" id="tgt25" class="tgtSentence"> But calling <legacyBold>MovePrevious</legacyBold> makes the record preceding the one you deleted the current record, because the deleted record is no longer counted in the active membership of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="06a380216167e47232882bc151e9c1ef" id="tgt26" class="tgtSentence">It is particularly difficult to define consistent move semantics across all providers for methods that move relative to the current record — <legacyBold>MovePrevious</legacyBold>, <legacyBold>MoveNext</legacyBold>, and <legacyBold>Move</legacyBold> — in the face of changing data in the current record.</caps:sentence>
          <caps:sentence sentenceid="8a56d3923b85b4806767867604be08c6" id="tgt27" class="tgtSentence"> For example, if you are working with a sorted, filtered <legacyBold>Recordset</legacyBold>, and you change the data in the current record so that it would precede all other records, but your changed data also no longer matches the filter, it is not clear where a <legacyBold>MoveNext</legacyBold> operation should take you.</caps:sentence>
          <caps:sentence sentenceid="c2f76810649e0e3de476fad625c3dd2f" id="tgt28" class="tgtSentence"> The safest conclusion is that relative movement within a <legacyBold>Recordset</legacyBold> is riskier than absolute movement (such as using <legacyBold>MoveFirst</legacyBold> or <legacyBold>MoveLast</legacyBold>) when the data is changing while records are being edited, added, or deleted.</caps:sentence>
          <caps:sentence sentenceid="64cd032f33ee178a0ea579e078258568" id="tgt29" class="tgtSentence"> Sorting and filtering should be based on a primary key or ID, because this type of value should not change.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following four methods are used to move around, or scroll, in the <legacyBold>Recordset</legacyBold>: <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> (Some of these methods are unavailable on forward-only cursors.)</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">         <legacyBold>MoveFirst</legacyBold> changes the current record position to the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence">
            <legacyBold>MoveLast</legacyBold> changes the current record position to the last record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> To use <legacyBold>MoveFirst</legacyBold> or <legacyBold>MoveLast</legacyBold>, the <legacyBold>Recordset</legacyBold> object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">         <legacyBold>MoveNext</legacyBold> moves the current record position one place forward.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> If you are on the last record when you call <legacyBold>MoveNext</legacyBold>, <legacyBold>EOF</legacyBold> will be set to <legacyBold>True</legacyBold>.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence">
            <legacyBold>MovePrevious</legacyBold> moves the current record position one place backward.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> If you are on the first record when you call <legacyBold>MovePrevious</legacyBold>, <legacyBold>BOF</legacyBold> will be set to <legacyBold>True</legacyBold>.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> It is wise to check the <legacyBold>EOF</legacyBold> and <legacyBold>BOF</legacyBold> properties when using these methods and to move the cursor back to a valid current record position if you move off either end of the <legacyBold>Recordset</legacyBold>, as shown here:</caps:sentence>
        </para>
        <code>. . .
oRs.MoveNext
If oRs.EOF Then oRs.MoveLast
. . . </code>
        <para>
          <caps:sentence id="src11" class="srcSentence">Or, in the case of the <legacyBold>MovePrevious</legacyBold> method:</caps:sentence>
        </para>
        <code>. . . 
oRs.MovePrevious
If oRs.BOF Then oRs.MoveFirst
. . .</code>
        <para>
          <caps:sentence id="src12" class="srcSentence">In cases where the <legacyBold>Recordset</legacyBold> has been filtered or sorted and the current record's data is changed, the position may also change.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> In such cases the <legacyBold>MoveNext</legacyBold> method works normally, but be aware that the position is moved one record forward from the new position, not the old position.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> For example, changing the data in the current record, such that the record is moved to the end of the sorted <legacyBold>Recordset</legacyBold>, would mean that calling <legacyBold>MoveNext</legacyBold> results in ADO setting the current record to the position after the last record in the <legacyBold>Recordset</legacyBold> (<legacyBold>EOF</legacyBold> = <legacyBold>True</legacyBold>).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src15" class="srcSentence">The behavior of the various Move methods of the <legacyBold>Recordset</legacyBold> object depends, to some extent, on the data within the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> New records added to the <legacyBold>Recordset</legacyBold> are initially added in a particular order, which is defined by the data source and may be dependent implicitly or explicitly on the data in the new record.</caps:sentence>
          <caps:sentence id="src17" class="srcSentence"> For example, if a sort or a join is done within the query that populates the <legacyBold>Recordset</legacyBold>, the new record will be inserted in the appropriate place within the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src18" class="srcSentence"> If ordering is not explicitly specified when creating the <legacyBold>Recordset</legacyBold>, changes in the data source implementation may cause the ordering of the returned rows to change inadvertently.</caps:sentence>
          <caps:sentence id="src19" class="srcSentence"> In addition, the sorting, filtering, and editing functions of the <legacyBold>Recordset</legacyBold> can affect the order and possibly which rows in the recordset will be visible.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src20" class="srcSentence">Therefore, <legacyBold>MoveNext</legacyBold>, <legacyBold>MovePrevious</legacyBold>, <legacyBold>MoveFirst</legacyBold>, <legacyBold>MoveLast</legacyBold>, and <legacyBold>Move</legacyBold> are all sensitive to other operations performed on the same <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src21" class="srcSentence"> ADO will always try to maintain your current position until you explicitly move it, but sometimes, intervening changes make it difficult to understand the effects of a subsequent move.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> For example, if you call <legacyBold>MoveFirst</legacyBold> to position on the first row of a sorted <legacyBold>Recordset</legacyBold> and you change the sort from ascending order to descending order, you are still on the same row — but now it is the last row in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src23" class="srcSentence">
            <legacyBold>MoveFirst</legacyBold> will take you to a different row (the new first row).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src24" class="srcSentence">As another example, if you are positioned on a particular row in the middle of a <legacyBold>Recordset</legacyBold> and you call <legacyBold>Delete</legacyBold> and then call <legacyBold>MoveNext</legacyBold>, you are now on the record immediately following the deleted record.</caps:sentence>
          <caps:sentence id="src25" class="srcSentence"> But calling <legacyBold>MovePrevious</legacyBold> makes the record preceding the one you deleted the current record, because the deleted record is no longer counted in the active membership of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src26" class="srcSentence">It is particularly difficult to define consistent move semantics across all providers for methods that move relative to the current record — <legacyBold>MovePrevious</legacyBold>, <legacyBold>MoveNext</legacyBold>, and <legacyBold>Move</legacyBold> — in the face of changing data in the current record.</caps:sentence>
          <caps:sentence id="src27" class="srcSentence"> For example, if you are working with a sorted, filtered <legacyBold>Recordset</legacyBold>, and you change the data in the current record so that it would precede all other records, but your changed data also no longer matches the filter, it is not clear where a <legacyBold>MoveNext</legacyBold> operation should take you.</caps:sentence>
          <caps:sentence id="src28" class="srcSentence"> The safest conclusion is that relative movement within a <legacyBold>Recordset</legacyBold> is riskier than absolute movement (such as using <legacyBold>MoveFirst</legacyBold> or <legacyBold>MoveLast</legacyBold>) when the data is changing while records are being edited, added, or deleted.</caps:sentence>
          <caps:sentence id="src29" class="srcSentence"> Sorting and filtering should be based on a primary key or ID, because this type of value should not change.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
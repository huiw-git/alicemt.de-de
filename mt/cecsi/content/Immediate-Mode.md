---
title: "Immediate Mode"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 31fc53d0-97de-4315-a87b-3bf5cdd1f432
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
# Immediate Mode
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="765d1b490060313036b9b7ef100963b7" id="tgt1" class="tgtSentence">Immediate mode is in effect when the <legacyBold>LockType</legacyBold> property is set to <legacyBold>adLockOptimistic</legacyBold> or <legacyBold>adLockPessimistic</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="795946fc380e65b0f383fa3da7c944e1" id="tgt2" class="tgtSentence"> In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the <legacyBold>Update</legacyBold> method.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="952a9391dc49fbc73be89e9c10b9dc28" id="tgt3" class="tgtSentence">Calling Update</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b51a087f6325960ab30d650f9d2a9981" id="tgt4" class="tgtSentence">If you move from the record you are adding or editing before calling the <legacyBold>Update</legacyBold> method, ADO will automatically call <legacyBold>Update</legacyBold> to save the changes.</caps:sentence>
            <caps:sentence sentenceid="8a06f51c88f0d68bb477d9ab06772164" id="tgt5" class="tgtSentence"> You must call the <legacyBold>CancelUpdate</legacyBold> method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d34acd3113224bf80ebcfbfdfccc0840" id="tgt6" class="tgtSentence">The current record remains current after you call the <legacyBold>Update</legacyBold> method.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="07e957a04a9b08eadc8537a17615e387" id="tgt7" class="tgtSentence">CancelUpdate</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ac150ed0618d6c3f27b1ed3a869c4296" id="tgt8" class="tgtSentence">Use the <legacyBold>CancelUpdate</legacyBold> method to cancel any changes made to the current row or to discard a newly added row.</caps:sentence>
            <caps:sentence sentenceid="5e7d1a8fd22bf52ded542ec5bd5cd0c5" id="tgt9" class="tgtSentence"> You cannot cancel changes to the current row or a new row after you call the <legacyBold>Update</legacyBold> method, unless the changes are either part of a transaction that you can roll back with the <legacyBold>RollbackTrans</legacyBold> method or part of a batch update.</caps:sentence>
            <caps:sentence sentenceid="83ac5b2168dec1283d5fb59acb258826" id="tgt10" class="tgtSentence"> In the case of a batch update, you can cancel the <legacyBold>Update</legacyBold> with the <legacyBold>CancelUpdate</legacyBold> or <legacyBold>CancelBatch</legacyBold> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1ff11e8607f2140e9632ba70d3b2eb07" id="tgt11" class="tgtSentence">If you are adding a new row when you call the <legacyBold>CancelUpdate</legacyBold> method, the current row becomes the row that was current before the <legacyBold>AddNew</legacyBold> call.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="21a5222793b6c17165c3b68cd021741b" id="tgt12" class="tgtSentence">If you have not changed the current row or added a new row, calling the <legacyBold>CancelUpdate</legacyBold> method generates an error.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Immediate mode is in effect when the <legacyBold>LockType</legacyBold> property is set to <legacyBold>adLockOptimistic</legacyBold> or <legacyBold>adLockPessimistic</legacyBold>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the <legacyBold>Update</legacyBold> method.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Calling Update</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">If you move from the record you are adding or editing before calling the <legacyBold>Update</legacyBold> method, ADO will automatically call <legacyBold>Update</legacyBold> to save the changes.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> You must call the <legacyBold>CancelUpdate</legacyBold> method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">The current record remains current after you call the <legacyBold>Update</legacyBold> method.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">CancelUpdate</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">Use the <legacyBold>CancelUpdate</legacyBold> method to cancel any changes made to the current row or to discard a newly added row.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> You cannot cancel changes to the current row or a new row after you call the <legacyBold>Update</legacyBold> method, unless the changes are either part of a transaction that you can roll back with the <legacyBold>RollbackTrans</legacyBold> method or part of a batch update.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> In the case of a batch update, you can cancel the <legacyBold>Update</legacyBold> with the <legacyBold>CancelUpdate</legacyBold> or <legacyBold>CancelBatch</legacyBold> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If you are adding a new row when you call the <legacyBold>CancelUpdate</legacyBold> method, the current row becomes the row that was current before the <legacyBold>AddNew</legacyBold> call.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">If you have not changed the current row or added a new row, calling the <legacyBold>CancelUpdate</legacyBold> method generates an error.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
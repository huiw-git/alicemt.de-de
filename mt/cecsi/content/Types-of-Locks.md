---
title: "Types of Locks"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 12a978c0-b8a0-4ef0-87f0-a43c13659272
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
# Types of Locks
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="7ea6949dd6117ed20e65d11b751dce53" id="tgt1" class="tgtSentence">adLockBatchOptimistic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cf1e0dbc829efd6eeb51fe2d7b4cf8e2" id="tgt2" class="tgtSentence">Indicates optimistic batch updates.</caps:sentence>
            <caps:sentence sentenceid="ea51151186cd6a67f406c0dc7bfec53d" id="tgt3" class="tgtSentence"> Required for batch update mode.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1ad76647932c753ff0d0b1a11a5f00a1" id="tgt4" class="tgtSentence">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted.</caps:sentence>
            <caps:sentence sentenceid="88d0d29dd8864aab161accb6edad8fae" id="tgt5" class="tgtSentence"> With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic.</caps:sentence>
            <caps:sentence sentenceid="cc9f2a36879186782e22952dae4e8236" id="tgt6" class="tgtSentence"> Using a batch cursor library, you can create a static cursor and then disconnect from the data source.</caps:sentence>
            <caps:sentence sentenceid="313d79fff096b8c361377af5e89d3a35" id="tgt7" class="tgtSentence"> At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="95c61c35a284e29b0938d92a5bdf7803" id="tgt8" class="tgtSentence">adLockOptimistic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="00643c08016ab8c5626d9b42379d6456" id="tgt9" class="tgtSentence">Indicates that the provider uses optimistic locking — locking records only when you call the <legacyBold>Update</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="50df6750a73673d319d159e2f1205e8e" id="tgt10" class="tgtSentence"> This means that there is a chance that another user may change the data between the time you edit the record and when you call <legacyBold>Update</legacyBold>, which creates conflicts.</caps:sentence>
            <caps:sentence sentenceid="0fcda3df1cab39a2acb3ebcebf06b542" id="tgt11" class="tgtSentence"> Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a471c1dd4035ab5600e576bd780cf587" id="tgt12" class="tgtSentence">adLockPessimistic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ef984d9e4cb84701a0e0c1fcad987344" id="tgt13" class="tgtSentence">Indicates pessimistic locking, record by record.</caps:sentence>
            <caps:sentence sentenceid="c6ef0680203dd8b2913ff120bea8ce8e" id="tgt14" class="tgtSentence"> The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing.</caps:sentence>
            <caps:sentence sentenceid="e367763ebef225e258926f8f194d8fc8" id="tgt15" class="tgtSentence"> Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling <legacyBold>Update.</legacyBold> Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="206b3571b04c113b4d0a4193a707efb2" id="tgt16" class="tgtSentence">adLockReadOnly</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d61a3a17aa3c1ead593597ec636998d7" id="tgt17" class="tgtSentence">Indicates read-only records.</caps:sentence>
            <caps:sentence sentenceid="0d71cd8b59f04d3c3d7df01ccdbf1663" id="tgt18" class="tgtSentence"> You cannot alter the data.</caps:sentence>
            <caps:sentence sentenceid="535fc33f2a504d8e30fba009a10f36a8" id="tgt19" class="tgtSentence"> A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="868bc70e440a34508ac6deeea43c6f09" id="tgt20" class="tgtSentence">adLockUnspecified</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="fd796b32044447e407ea03e8c309da3f" id="tgt21" class="tgtSentence">Does not specify a type of lock.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">adLockBatchOptimistic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Indicates optimistic batch updates.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Required for batch update mode.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Using a batch cursor library, you can create a static cursor and then disconnect from the data source.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">adLockOptimistic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">Indicates that the provider uses optimistic locking — locking records only when you call the <legacyBold>Update</legacyBold> method.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> This means that there is a chance that another user may change the data between the time you edit the record and when you call <legacyBold>Update</legacyBold>, which creates conflicts.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">adLockPessimistic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">Indicates pessimistic locking, record by record.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling <legacyBold>Update.</legacyBold> Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">adLockReadOnly</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">Indicates read-only records.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> You cannot alter the data.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">adLockUnspecified</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">Does not specify a type of lock.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
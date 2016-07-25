---
title: "Filtering for Updated Records"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4a798921-d7bb-47c9-a252-550fd9463ec9
caps.latest.revision: 3
caps.handback.revision: 3
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
# Filtering for Updated Records
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b2f2118699860c2dfcd91c812925d2a6" id="tgt1" class="tgtSentence">Before you call UpdateBatch, you can use the Recordset Filter property to view only those records that have been changed since the Recordset was opened or the last call to UpdateBatch.</caps:sentence>
          <caps:sentence sentenceid="4a84ba204d02f7294e52e56d77e7b698" id="tgt2" class="tgtSentence"> To do this, set Filter equal to adFilterPendingRecords to determine how many records will be updated, as shown in the code example in the next section.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt3" class="tgtSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b545fa4d048cc54a0859cfa21c2812f1" id="tgt4" class="tgtSentence">This example extends the previous UpdateBatch example by filtering the Recordset just before it calls the UpdateBatch, showing the user which records will change and allowing her to cancel the update (using the CancelBatch method).</caps:sentence>
          </para>
          <code>'BeginFilterPend
    '...
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText
    
    ' Change value of Phone field for first record in Recordset, saving value
    ' for later restoration.
    intId = objRs1("ShipperId")
    sPhone = objRs1("Phone")
    
    objRs1("Phone") = "(111) 555-1111"
    
    'Add two new records
    For i = 0 To 1
        objRs1.AddNew
        objRs1(1) = "New Shipper #" &amp; CStr((i + 1))
        objRs1(2) = "(nnn) 555-" &amp; i &amp; i &amp; i &amp; i
    Next i
    
    objRs1.Filter = adFilterPendingRecords
    
    MsgBox "There are " &amp; objRs1.RecordCount &amp; " records pending.", _
            , "Filter Pending"
            
    ' Cancel the updates
    objRs1.CancelBatch
'EndFilterPend</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Before you call UpdateBatch, you can use the Recordset Filter property to view only those records that have been changed since the Recordset was opened or the last call to UpdateBatch.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> To do this, set Filter equal to adFilterPendingRecords to determine how many records will be updated, as shown in the code example in the next section.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">This example extends the previous UpdateBatch example by filtering the Recordset just before it calls the UpdateBatch, showing the user which records will change and allowing her to cancel the update (using the CancelBatch method).</caps:sentence>
          </para>
          <code>'BeginFilterPend
    '...
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText
    
    ' Change value of Phone field for first record in Recordset, saving value
    ' for later restoration.
    intId = objRs1("ShipperId")
    sPhone = objRs1("Phone")
    
    objRs1("Phone") = "(111) 555-1111"
    
    'Add two new records
    For i = 0 To 1
        objRs1.AddNew
        objRs1(1) = "New Shipper #" &amp; CStr((i + 1))
        objRs1(2) = "(nnn) 555-" &amp; i &amp; i &amp; i &amp; i
    Next i
    
    objRs1.Filter = adFilterPendingRecords
    
    MsgBox "There are " &amp; objRs1.RecordCount &amp; " records pending.", _
            , "Filter Pending"
            
    ' Cancel the updates
    objRs1.CancelBatch
'EndFilterPend</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
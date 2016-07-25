---
title: "Sending the Updates: UpdateBatch Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 87123797-831f-48e0-94b5-f669f9ca194a
caps.latest.revision: 2
caps.handback.revision: 2
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
# Sending the Updates: UpdateBatch Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="071094aa154ef325b7f1d96d871109ca" id="tgt1" class="tgtSentence">The following code opens a Recordset in batch mode by setting the LockType property to adLockBatchOptimistic and the CursorLocation to adUseClient.</caps:sentence>
          <caps:sentence sentenceid="cbb350f304147ec7fa585cf2eab2d693" id="tgt2" class="tgtSentence"> It adds two new records and changes the value of a field in an existing record, saving the original values, and then calls UpdateBatch to send the changes back to the data source.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt3" class="tgtSentence">Remarks</caps:sentence>
        </title>
        <content>
          <code>'BeginBatchUpdate
    strConn = "Provider=SQLOLEDB;Initial Catalog=Northwind;" &amp; _
              "Data Source=MySQLServer;Integrated Security=SSPI;"
             
    strSQL = "SELECT ShipperId, CompanyName, Phone FROM Shippers"
                 
    Set objRs1 = New ADODB.Recordset
    objRs1.CursorLocation = adUseClient
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
    
    ' Send the updates
    objRs1.UpdateBatch
'EndBatchUpdate</code>
          <para>
            <caps:sentence sentenceid="7a238a3bd885f0fef1cc59e50f64c4a8" id="tgt4" class="tgtSentence">If you are editing the current record or adding a new record when you call the UpdateBatch method, ADO will automatically call the Update method to save any pending changes to the current record before transmitting the batched changes to the provider.</caps:sentence>
          </para>
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
          <caps:sentence id="src1" class="srcSentence">The following code opens a Recordset in batch mode by setting the LockType property to adLockBatchOptimistic and the CursorLocation to adUseClient.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It adds two new records and changes the value of a field in an existing record, saving the original values, and then calls UpdateBatch to send the changes back to the data source.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Remarks</caps:sentence>
        </title>
        <content>
          <code>'BeginBatchUpdate
    strConn = "Provider=SQLOLEDB;Initial Catalog=Northwind;" &amp; _
              "Data Source=MySQLServer;Integrated Security=SSPI;"
             
    strSQL = "SELECT ShipperId, CompanyName, Phone FROM Shippers"
                 
    Set objRs1 = New ADODB.Recordset
    objRs1.CursorLocation = adUseClient
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
    
    ' Send the updates
    objRs1.UpdateBatch
'EndBatchUpdate</code>
          <para>
            <caps:sentence id="src4" class="srcSentence">If you are editing the current record or adding a new record when you call the UpdateBatch method, ADO will automatically call the Update method to save any pending changes to the current record before transmitting the batched changes to the provider.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
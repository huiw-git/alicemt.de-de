---
title: "Detecting and Resolving Conflicts"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b28fdd26-c1a4-40ce-a700-2b0c9d201514
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
# Detecting and Resolving Conflicts
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b32b0413c89e3745e04093d8ac07dd0b" id="tgt1" class="tgtSentence">If you are dealing with your Recordset in immediate mode, there is much less chance for concurrency problems to occur.</caps:sentence>
          <caps:sentence sentenceid="c659933b2a2b664bb2298f46f93a073e" id="tgt2" class="tgtSentence"> On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes that were made by another user editing the same record are saved.</caps:sentence>
          <caps:sentence sentenceid="7ecbe5a8574505badad9d174c39aaf3d" id="tgt3" class="tgtSentence"> In such a case, you will want your application to gracefully handle the conflict.</caps:sentence>
          <caps:sentence sentenceid="ac7bd096516828bfdce4c19a561cb178" id="tgt4" class="tgtSentence"> It may be your wish that the last person to send an update to the server "wins."</caps:sentence>
          <caps:sentence sentenceid="3d4704c6a186e9f52a522b72182e97ca" id="tgt5" class="tgtSentence"> Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="13c72e45cd0275195d833fd0457f32a8" id="tgt6" class="tgtSentence">Whatever the case, ADO provides the UnderlyingValue and OriginalValue properties of the Field object to handle these types of conflicts.</caps:sentence>
          <caps:sentence sentenceid="8c97b369f767e2b1fec5ae6a88fb2561" id="tgt7" class="tgtSentence"> Use these properties in combination with the Resync method and Filter property of the Recordset.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt8" class="tgtSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8c81885c5e8813ec10062ee7c28e35ba" id="tgt9" class="tgtSentence">When ADO encounters a conflict during a batch update, a warning will be added to the Errors collection.</caps:sentence>
            <caps:sentence sentenceid="76273ac22dd624cdd015b1e3f795a349" id="tgt10" class="tgtSentence"> Therefore, you should always check for errors immediately after you call BatchUpdate, and if you find them, begin testing the assumption that you have encountered a conflict.</caps:sentence>
            <caps:sentence sentenceid="c8548c240ab6c8a75e5f54faa90f02b9" id="tgt11" class="tgtSentence"> The first step is to set the Filter property on the Recordset equal to adFilterConflictingRecords.</caps:sentence>
            <caps:sentence sentenceid="0f8f489e1db3f0cdda36a36603c0b3a4" id="tgt12" class="tgtSentence"> This limits the view on your Recordset to only those records that are in conflict.</caps:sentence>
            <caps:sentence sentenceid="98c53bc8edb31628e9d7794281a3d5d9" id="tgt13" class="tgtSentence"> If the RecordCount property is equal to zero after this step, you know the error was raised by something other than a conflict.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a0ce88dd69c889710c08883e94758011" id="tgt14" class="tgtSentence">When you call BatchUpdate, ADO and the provider are generating SQL statements to perform updates on the data source.</caps:sentence>
            <caps:sentence sentenceid="7d149f4efb34e5501076446a1592908a" id="tgt15" class="tgtSentence"> Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="89279c676009fbfeeaaabfecd2fb7a4b" id="tgt16" class="tgtSentence">Next, call the Resync method on the Recordset with the AffectRecords argument set equal to adAffectGroup and the ResyncValues argument set equal to adResyncUnderlyingValues.</caps:sentence>
            <caps:sentence sentenceid="8d02da556b548456a407d5c8f8357ac9" id="tgt17" class="tgtSentence"> The Resync method updates the data in the current Recordset object from the underlying database.</caps:sentence>
            <caps:sentence sentenceid="f728cdee7e9cafe26d0d454ae82e105c" id="tgt18" class="tgtSentence"> By using adAffectGroup, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</caps:sentence>
            <caps:sentence sentenceid="6676c9261ed20a8500027a62fa99a422" id="tgt19" class="tgtSentence"> This could make a significant performance difference if you are dealing with a large Recordset.</caps:sentence>
            <caps:sentence sentenceid="e93fd1eac719b231734771bd73b9cef6" id="tgt20" class="tgtSentence"> By setting the ResyncValues argument to adResyncUnderlyingValues when calling Resync, you ensure that the UnderlyingValue property will contain the (conflicting) value from the database, that the Value property will maintain the value entered by the user, and that the OriginalValue property will hold the original value for the field (the value it had before the last successful UpdateBatch call was made).</caps:sentence>
            <caps:sentence sentenceid="6f09ce3b2229dd7c2adcc3f31f8659bb" id="tgt21" class="tgtSentence"> You can then use these values to resolve the conflict programmatically or require the user to select the value that will be used.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d0e90a3760d7cb3404c6dfe7cf9c501a" id="tgt22" class="tgtSentence">This technique is shown in the following code example.</caps:sentence>
            <caps:sentence sentenceid="5a1e841bb4152540428a2ff5ecfe9ac9" id="tgt23" class="tgtSentence"> The example artificially creates a conflict by using a separate Recordset to change a value in the underlying table before UpdateBatch is called.</caps:sentence>
          </para>
          <code>'BeginConflicts
    strConn = "Provider=SQLOLEDB;Initial Catalog=Northwind;" &amp; _
              "Data Source=MySQLServer;Integrated Security=SSPI;"
             
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2"
                 
    'Open Rs and change a value
    Set objRs1 = New ADODB.Recordset
    Set objRs2 = New ADODB.Recordset
    objRs1.CursorLocation = adUseClient
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText
    objRs1("Phone") = "(111) 555-1111"
    
    'Introduce a conflict at the db...
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText
    objRs2("Phone") = "(999) 555-9999"
    objRs2.Update
    objRs2.Close
    Set objRs2 = Nothing
    
    On Error Resume Next
    objRs1.UpdateBatch
    
    If objRs1.ActiveConnection.Errors.Count &lt;&gt; 0 Then
        Dim intConflicts As Integer
        
        intConflicts = 0
        
        objRs1.Filter = adFilterConflictingRecords
        
        intConflicts = objRs1.RecordCount
        
        'Resync so we can see the UnderlyingValue and offer user a choice.
        'This sample only displays all three values and resets to original.
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues
        
        If intConflicts &gt; 0 Then
            strMsg = "A conflict occurred with updates for " &amp; intConflicts &amp; _
                     " record(s)." &amp; vbCrLf &amp; "The values will be restored" &amp; _
                     " to their original values." &amp; vbCrLf &amp; vbCrLf
                     
            objRs1.MoveFirst
            While Not objRs1.EOF
              strMsg = strMsg &amp; "SHIPPER = " &amp; objRs1("CompanyName") &amp; vbCrLf
              strMsg = strMsg &amp; "Value = " &amp; objRs1("Phone").Value &amp; vbCrLf
              strMsg = strMsg &amp; "UnderlyingValue = " &amp; _
                                 objRs1("Phone").UnderlyingValue &amp; vbCrLf
              strMsg = strMsg &amp; "OriginalValue = " &amp; _
                                 objRs1("Phone").OriginalValue &amp; vbCrLf
              strMsg = strMsg &amp; vbCrLf &amp; "Original value has been restored."
                
              MsgBox strMsg, vbOKOnly, _
                    "Conflict " &amp; objRs1.AbsolutePosition &amp; _
                    " of " &amp; intConflicts
                
              objRs1("Phone").Value = objRs1("Phone").OriginalValue
              objRs1.MoveNext
            Wend
            
            objRs1.UpdateBatch adAffectGroup
        Else
            'Other error occurred. Minimal handling in this example.
             strMsg = "Errors occurred during the update. " &amp; _
                        objRs1.ActiveConnection.Errors(0).Number &amp; " " &amp; _
                        objRs1.ActiveConnection.Errors(0).Description
        End If
        
        On Error GoTo 0
    End If
    
    objRs1.MoveFirst
    objRs1.Close
    Set objRs1 = Nothing
'EndConflicts</code>
          <para>
            <caps:sentence sentenceid="91457bb696200702e6ac438ccecdac65" id="tgt24" class="tgtSentence">You can use the Status property of the current Record or of a specific Field to determine what kind of a conflict has occurred.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2cc5d27b07720e43c402372a7b96833e" id="tgt25" class="tgtSentence">For detailed information about error handling, see <link xlink:href="4909e413-f3b0-4183-8ad3-67b1434df742">Error Handling</link>.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">If you are dealing with your Recordset in immediate mode, there is much less chance for concurrency problems to occur.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes that were made by another user editing the same record are saved.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> In such a case, you will want your application to gracefully handle the conflict.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> It may be your wish that the last person to send an update to the server "wins."</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">Whatever the case, ADO provides the UnderlyingValue and OriginalValue properties of the Field object to handle these types of conflicts.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Use these properties in combination with the Resync method and Filter property of the Recordset.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">When ADO encounters a conflict during a batch update, a warning will be added to the Errors collection.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Therefore, you should always check for errors immediately after you call BatchUpdate, and if you find them, begin testing the assumption that you have encountered a conflict.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The first step is to set the Filter property on the Recordset equal to adFilterConflictingRecords.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> This limits the view on your Recordset to only those records that are in conflict.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> If the RecordCount property is equal to zero after this step, you know the error was raised by something other than a conflict.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">When you call BatchUpdate, ADO and the provider are generating SQL statements to perform updates on the data source.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">Next, call the Resync method on the Recordset with the AffectRecords argument set equal to adAffectGroup and the ResyncValues argument set equal to adResyncUnderlyingValues.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> The Resync method updates the data in the current Recordset object from the underlying database.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> By using adAffectGroup, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> This could make a significant performance difference if you are dealing with a large Recordset.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> By setting the ResyncValues argument to adResyncUnderlyingValues when calling Resync, you ensure that the UnderlyingValue property will contain the (conflicting) value from the database, that the Value property will maintain the value entered by the user, and that the OriginalValue property will hold the original value for the field (the value it had before the last successful UpdateBatch call was made).</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> You can then use these values to resolve the conflict programmatically or require the user to select the value that will be used.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">This technique is shown in the following code example.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> The example artificially creates a conflict by using a separate Recordset to change a value in the underlying table before UpdateBatch is called.</caps:sentence>
          </para>
          <code>'BeginConflicts
    strConn = "Provider=SQLOLEDB;Initial Catalog=Northwind;" &amp; _
              "Data Source=MySQLServer;Integrated Security=SSPI;"
             
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2"
                 
    'Open Rs and change a value
    Set objRs1 = New ADODB.Recordset
    Set objRs2 = New ADODB.Recordset
    objRs1.CursorLocation = adUseClient
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText
    objRs1("Phone") = "(111) 555-1111"
    
    'Introduce a conflict at the db...
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText
    objRs2("Phone") = "(999) 555-9999"
    objRs2.Update
    objRs2.Close
    Set objRs2 = Nothing
    
    On Error Resume Next
    objRs1.UpdateBatch
    
    If objRs1.ActiveConnection.Errors.Count &lt;&gt; 0 Then
        Dim intConflicts As Integer
        
        intConflicts = 0
        
        objRs1.Filter = adFilterConflictingRecords
        
        intConflicts = objRs1.RecordCount
        
        'Resync so we can see the UnderlyingValue and offer user a choice.
        'This sample only displays all three values and resets to original.
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues
        
        If intConflicts &gt; 0 Then
            strMsg = "A conflict occurred with updates for " &amp; intConflicts &amp; _
                     " record(s)." &amp; vbCrLf &amp; "The values will be restored" &amp; _
                     " to their original values." &amp; vbCrLf &amp; vbCrLf
                     
            objRs1.MoveFirst
            While Not objRs1.EOF
              strMsg = strMsg &amp; "SHIPPER = " &amp; objRs1("CompanyName") &amp; vbCrLf
              strMsg = strMsg &amp; "Value = " &amp; objRs1("Phone").Value &amp; vbCrLf
              strMsg = strMsg &amp; "UnderlyingValue = " &amp; _
                                 objRs1("Phone").UnderlyingValue &amp; vbCrLf
              strMsg = strMsg &amp; "OriginalValue = " &amp; _
                                 objRs1("Phone").OriginalValue &amp; vbCrLf
              strMsg = strMsg &amp; vbCrLf &amp; "Original value has been restored."
                
              MsgBox strMsg, vbOKOnly, _
                    "Conflict " &amp; objRs1.AbsolutePosition &amp; _
                    " of " &amp; intConflicts
                
              objRs1("Phone").Value = objRs1("Phone").OriginalValue
              objRs1.MoveNext
            Wend
            
            objRs1.UpdateBatch adAffectGroup
        Else
            'Other error occurred. Minimal handling in this example.
             strMsg = "Errors occurred during the update. " &amp; _
                        objRs1.ActiveConnection.Errors(0).Number &amp; " " &amp; _
                        objRs1.ActiveConnection.Errors(0).Description
        End If
        
        On Error GoTo 0
    End If
    
    objRs1.MoveFirst
    objRs1.Close
    Set objRs1 = Nothing
'EndConflicts</code>
          <para>
            <caps:sentence id="src24" class="srcSentence">You can use the Status property of the current Record or of a specific Field to determine what kind of a conflict has occurred.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">For detailed information about error handling, see <link xlink:href="4909e413-f3b0-4183-8ad3-67b1434df742">Error Handling</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
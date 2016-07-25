---
title: "Editing Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef514f85-c446-4f05-824e-c9313b2ffae1
caps.latest.revision: 15
caps.handback.revision: 15
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
# Editing Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="049222e341a81756f47a6cf296e020a8" id="tgt1" class="tgtSentence">We have explained how use ADO to connect to a data source, execute a command, get the results in a <legacyBold>Recordset</legacyBold> object, and navigate within the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="2d779a28a9e2855d178d8aa16b6a781a" id="tgt2" class="tgtSentence"> This section focuses on the next fundamental ADO operation: editing data.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ff403df4f53190fffd7a469fcaa0a324" id="tgt3" class="tgtSentence">This section continues to use the sample <legacyBold>Recordset</legacyBold> introduced in <legacyLink xlink:href="de1d74af-89b6-4f3f-a8c9-07c3e2b3c9a5">Examining Data</legacyLink>, with one important change.</caps:sentence>
          <caps:sentence sentenceid="87abf12eb972544adb26c69ea571e00e" id="tgt4" class="tgtSentence"> The following code is used to open the <legacyBold>Recordset</legacyBold>:</caps:sentence>
        </para>
        <code>'BeginEditIntro
    Dim strSQL As String
    Dim objRs1 As ADODB.Recordset
    
    strSQL = "SELECT * FROM Shippers"
    
    Set objRs1 = New ADODB.Recordset
    
    objRs1.Open strSQL, GetNewConnection, adOpenStatic, _
                adLockBatchOptimistic, adCmdText
    
    ' Disconnect the Recordset from the Connection object.
    Set objRs1.ActiveConnection = Nothing
'EndEditIntro</code>
        <para>
          <caps:sentence sentenceid="3af3a06effa54b6ac33e9969d3b1402d" id="tgt5" class="tgtSentence">The important change to the code involves setting the <legacyBold>CursorLocation</legacyBold> property of the <legacyBold>Connection</legacyBold> object equal to <legacyBold>adUseClient</legacyBold> in the <legacyItalic>GetNewConnection</legacyItalic> function (shown in the next example), which indicates the use of a client cursor.</caps:sentence>
          <caps:sentence sentenceid="c03fb0af6dc0f5916edcba96e5bd99f5" id="tgt6" class="tgtSentence"> For more information about the differences between client-side and server-side cursors, see <legacyLink xlink:href="c1b7d7e6-1707-4ce2-863f-0c6dea967df6">Understanding Cursors and Locks</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="defe9766d2081c83966a084fc93fe72a" id="tgt7" class="tgtSentence">The <legacyBold>CursorLocation</legacyBold> property's <legacyBold>adUseClient</legacyBold> setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation).</caps:sentence>
          <caps:sentence sentenceid="a665a6a2a639ace82bed7f8bac4ed152" id="tgt8" class="tgtSentence"> This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2cefb22548a82fd9eac547fc6f75fe0a" id="tgt9" class="tgtSentence">You might also have noticed that the <legacyBold>LockType</legacyBold> parameter of the <legacyBold>Open</legacyBold> method changed to <legacyBold>adLockBatchOptimistic</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="c9c8df5cf65f0946e594dcae8acbbdcd" id="tgt10" class="tgtSentence"> This opens the cursor in batch mode.</caps:sentence>
          <caps:sentence sentenceid="15fcad9d15288ff77d41f5171a788b71" id="tgt11" class="tgtSentence"> (The provider caches multiple changes and writes them to the underlying data source only when you call the <legacyBold>UpdateBatch</legacyBold> method.)</caps:sentence>
          <caps:sentence sentenceid="2df864cd50778b3fcff4a73fd6ee6755" id="tgt12" class="tgtSentence"> Changes that were made to the <legacyBold>Recordset</legacyBold> will not be updated in the database until the <legacyBold>UpdateBatch</legacyBold> method is called.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ab3f4f2e561584ff0441e9d4e78727f5" id="tgt13" class="tgtSentence">Finally, the code in this section uses a modified version of the GetNewConnection function.</caps:sentence>
          <caps:sentence sentenceid="e8cce48d5864a08d89a26398b83298a5" id="tgt14" class="tgtSentence"> This version of the function now returns a client-side cursor.</caps:sentence>
          <caps:sentence sentenceid="265e6ad2f0cd5b2dcf056b2ea3ec5b2f" id="tgt15" class="tgtSentence"> The function looks like this:</caps:sentence>
        </para>
        <code>'BeginNewConnection
Public Function GetNewConnection() As ADODB.Connection
    On Error GoTo ErrHandler:
    
    Dim objConn As New ADODB.Connection
    Dim strConnStr As String
    
    strConnStr = "Provider='SQLOLEDB';Initial Catalog='Northwind';" &amp; _
                 "Data Source='MySqlServer';Integrated Security='SSPI';"
             
    objConn.ConnectionString = strConnStr
    objConn.CursorLocation = adUseClient
    objConn.Open
    
    Set GetNewConnection = objConn
    
    Exit Function
    
ErrHandler:
    Set objConn = Nothing
    Set GetNewConnection = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Function
'EndNewConnection</code>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt16" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="17ce1263-5897-452a-9ea5-c7f96b33df65">
                <caps:sentence sentenceid="ed9cc23d6f1356d787cdd2504fb06cbc" id="tgt17" class="tgtSentence">Editing Existing Records</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="dd34669e-6f06-403b-9241-1c85c82aecc2">
                <caps:sentence sentenceid="7063131489741caa1240663367972a51" id="tgt18" class="tgtSentence">Adding Records</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="65090cba-6d46-4775-8d61-f6838e7752a6">
                <caps:sentence sentenceid="92cf7b1b9aa2d694d50b7347699ba0cc" id="tgt19" class="tgtSentence">Determining What is Supported</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="bfed5cfa-7f57-463b-9da2-0c612a079d30">
                <caps:sentence sentenceid="7ce4aad7276ea28d045bbcf6f3e17df7" id="tgt20" class="tgtSentence">Deleting Records Using the Delete Method</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="8b528b23-063d-45ea-8dea-6a90d4060b20">
                <caps:sentence sentenceid="b6f5027a7ff756504e850a92ee59bb59" id="tgt21" class="tgtSentence">Alternatives: Using SQL Statements</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">We have explained how use ADO to connect to a data source, execute a command, get the results in a <legacyBold>Recordset</legacyBold> object, and navigate within the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This section focuses on the next fundamental ADO operation: editing data.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">This section continues to use the sample <legacyBold>Recordset</legacyBold> introduced in <legacyLink xlink:href="de1d74af-89b6-4f3f-a8c9-07c3e2b3c9a5">Examining Data</legacyLink>, with one important change.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The following code is used to open the <legacyBold>Recordset</legacyBold>:</caps:sentence>
        </para>
        <code>'BeginEditIntro
    Dim strSQL As String
    Dim objRs1 As ADODB.Recordset
    
    strSQL = "SELECT * FROM Shippers"
    
    Set objRs1 = New ADODB.Recordset
    
    objRs1.Open strSQL, GetNewConnection, adOpenStatic, _
                adLockBatchOptimistic, adCmdText
    
    ' Disconnect the Recordset from the Connection object.
    Set objRs1.ActiveConnection = Nothing
'EndEditIntro</code>
        <para>
          <caps:sentence id="src5" class="srcSentence">The important change to the code involves setting the <legacyBold>CursorLocation</legacyBold> property of the <legacyBold>Connection</legacyBold> object equal to <legacyBold>adUseClient</legacyBold> in the <legacyItalic>GetNewConnection</legacyItalic> function (shown in the next example), which indicates the use of a client cursor.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> For more information about the differences between client-side and server-side cursors, see <legacyLink xlink:href="c1b7d7e6-1707-4ce2-863f-0c6dea967df6">Understanding Cursors and Locks</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">The <legacyBold>CursorLocation</legacyBold> property's <legacyBold>adUseClient</legacyBold> setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation).</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">You might also have noticed that the <legacyBold>LockType</legacyBold> parameter of the <legacyBold>Open</legacyBold> method changed to <legacyBold>adLockBatchOptimistic</legacyBold>.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> This opens the cursor in batch mode.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> (The provider caches multiple changes and writes them to the underlying data source only when you call the <legacyBold>UpdateBatch</legacyBold> method.)</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Changes that were made to the <legacyBold>Recordset</legacyBold> will not be updated in the database until the <legacyBold>UpdateBatch</legacyBold> method is called.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">Finally, the code in this section uses a modified version of the GetNewConnection function.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> This version of the function now returns a client-side cursor.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> The function looks like this:</caps:sentence>
        </para>
        <code>'BeginNewConnection
Public Function GetNewConnection() As ADODB.Connection
    On Error GoTo ErrHandler:
    
    Dim objConn As New ADODB.Connection
    Dim strConnStr As String
    
    strConnStr = "Provider='SQLOLEDB';Initial Catalog='Northwind';" &amp; _
                 "Data Source='MySqlServer';Integrated Security='SSPI';"
             
    objConn.ConnectionString = strConnStr
    objConn.CursorLocation = adUseClient
    objConn.Open
    
    Set GetNewConnection = objConn
    
    Exit Function
    
ErrHandler:
    Set objConn = Nothing
    Set GetNewConnection = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Function
'EndNewConnection</code>
        <para>
          <caps:sentence id="src16" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="17ce1263-5897-452a-9ea5-c7f96b33df65">
                <caps:sentence id="src17" class="srcSentence">Editing Existing Records</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="dd34669e-6f06-403b-9241-1c85c82aecc2">
                <caps:sentence id="src18" class="srcSentence">Adding Records</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="65090cba-6d46-4775-8d61-f6838e7752a6">
                <caps:sentence id="src19" class="srcSentence">Determining What is Supported</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="bfed5cfa-7f57-463b-9da2-0c612a079d30">
                <caps:sentence id="src20" class="srcSentence">Deleting Records Using the Delete Method</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="8b528b23-063d-45ea-8dea-6a90d4060b20">
                <caps:sentence id="src21" class="srcSentence">Alternatives: Using SQL Statements</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
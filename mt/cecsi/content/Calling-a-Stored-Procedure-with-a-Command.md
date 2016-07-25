---
title: "Calling a Stored Procedure with a Command"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 685f7652-2271-4ede-b552-2eeb8c756b4c
caps.latest.revision: 14
caps.handback.revision: 14
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
# Calling a Stored Procedure with a Command
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2fb0a184f71c5393169f4f9c0ccc136c" id="tgt1" class="tgtSentence">You can use a command to call a stored procedure.</caps:sentence>
          <caps:sentence sentenceid="1bfdc9f2b9e9838ea4a8d93a20924a8e" id="tgt2" class="tgtSentence"> The code sample at the end of this topic refers to a stored procedure in the Northwind sample database, called CustOrdersOrders, which is defined as follows.</caps:sentence>
        </para>
        <code>CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS
SELECT OrderID, OrderDate, RequiredDate, ShippedDate
FROM Orders
WHERE CustomerID = @CustomerID
ORDER BY OrderID</code>
        <para>
          <caps:sentence sentenceid="f0d9a0e96d2bd8006306197bb66b28c8" id="tgt3" class="tgtSentence">See your SQL Server documentation for more information about how to define and call stored procedures.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="411085ce637630ce4986878ba4a4003b" id="tgt4" class="tgtSentence">This stored procedure is similar to the command used in <legacyLink xlink:href="10e7ef4a-78bf-4e91-931e-cbc6c065dd4c">Command Object Parameters</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="7a1d436b123e846902a48bd35edc727b" id="tgt5" class="tgtSentence"> It takes a customer ID parameter and returns information about that customer's orders.</caps:sentence>
          <caps:sentence sentenceid="9ea2c116bf61dd2ae74416cdec57aef5" id="tgt6" class="tgtSentence"> The following code sample uses this stored procedure as the source for an ADO <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="df187cd2e2e513be4031c6fe5cbab388" id="tgt7" class="tgtSentence">Using the stored procedure allows you to access another capability of ADO: the <legacyBold>Parameters</legacyBold> collection <legacyBold>Refresh</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="bce4bbb9f7178039f45b4d84adceb96b" id="tgt8" class="tgtSentence"> By using this method, ADO can automatically fill in all information about the parameters required by the command at run time.</caps:sentence>
          <caps:sentence sentenceid="ac7a944b501de1e82b842c0122bd2fe3" id="tgt9" class="tgtSentence"> There is a performance penalty in using this technique, because ADO must query the data source for the information about the parameters.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="cbdbc6bf9493dc1899d1ab57f795201b" id="tgt10" class="tgtSentence">Other important differences exist between the following code sample and the code in <legacyLink xlink:href="10e7ef4a-78bf-4e91-931e-cbc6c065dd4c">Command Object Parameters</legacyLink>, where the parameters were entered manually.</caps:sentence>
          <caps:sentence sentenceid="7a3c659ba0f23df9933e0f0b546a03c6" id="tgt11" class="tgtSentence"> First, this code does not set the <legacyBold>Prepared</legacyBold> property to <legacyBold>True</legacyBold> because it is a SQL Server stored procedure and is precompiled by definition.</caps:sentence>
          <caps:sentence sentenceid="1581f971179b1c08d10aea6ec51370f6" id="tgt12" class="tgtSentence"> Second, the <legacyBold>CommandType</legacyBold> property of the <legacyBold>Command</legacyBold> object changed to <legacyBold>adCmdStoredProc</legacyBold> in the second example to inform ADO that the command was a stored procedure.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ce09681c4de872c8ca591f93d77d8b40" id="tgt13" class="tgtSentence">Finally, in the second example the parameter must be referred to by index when setting the value, because you might not know the name of the parameter at design time.</caps:sentence>
          <caps:sentence sentenceid="ff12b6f462577bef2d604f51b6475b3f" id="tgt14" class="tgtSentence"> If you do know the name of the parameter, you can set the new <legacyLink xlink:href="42409387-026c-435f-a9b1-bf4167095875">NamedParameters</legacyLink> property of the <legacyBold>Command</legacyBold> object to True and refer to the property's name.</caps:sentence>
          <caps:sentence sentenceid="1bd382943a13c2b553c7b5d3143e0e41" id="tgt15" class="tgtSentence"> You might wonder why the position of the first parameter mentioned in the stored procedure (@CustomerID) is 1 instead of 0 (<codeInline>objCmd(1) = "ALFKI"</codeInline>).</caps:sentence>
          <caps:sentence sentenceid="cf837acf15380ce54456963d8f10a2de" id="tgt16" class="tgtSentence"> This is because parameter 0 contains a return value from the SQL Server stored procedure.</caps:sentence>
        </para>
        <code>'BeginAutoParamCmd
    On Error GoTo ErrHandler:
    
    Dim objConn As New ADODB.Connection
    Dim objCmd As New ADODB.Command
    Dim objParm1 As New ADODB.Parameter
    Dim objRs As New ADODB.Recordset
    
    ' Set CommandText equal to the stored procedure name.
    objCmd.CommandText = "CustOrdersOrders"
    objCmd.CommandType = adCmdStoredProc
            
    ' Connect to the data source.
    Set objConn = GetNewConnection
    objCmd.ActiveConnection = objConn
        
    ' Automatically fill in parameter info from stored procedure.
    objCmd.Parameters.Refresh
    
    ' Set the param value.
    objCmd(1) = "ALFKI"
    
    ' Execute once and display...
    Set objRs = objCmd.Execute
        
    Debug.Print objParm1.Value
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
        
    ' ...then set new param value, re-execute command, and display.
    objCmd(1) = "CACTU"
    Set objRs = objCmd.Execute
        
    Debug.Print objParm1.Value
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
        
    'clean up
    objRs.Close
    objConn.Close
    Set objRs = Nothing
    Set objConn = Nothing
    Set objCmd = Nothing
    Set objParm1 = Nothing
    Exit Sub
    
ErrHandler:
    'clean up
    If objRs.State = adStateOpen Then
        objRs.Close
    End If
    
    If objConn.State = adStateOpen Then
        objConn.Close
    End If
    
    Set objRs = Nothing
    Set objConn = Nothing
    Set objCmd = Nothing
    Set objParm1 = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
'EndAutoParamCmd


'BeginNewConnection
Private Function GetNewConnection() As ADODB.Connection
    Dim oCn As New ADODB.Connection
    Dim sCnStr As String
    
    sCnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" &amp; _
             "Integrated Security='SSPI';Initial Catalog='Northwind';"
    oCn.Open sCnStr
    
    If oCn.State = adStateOpen Then
        Set GetNewConnection = oCn
    End If
    
End Function
'EndNewConnection</code>
      </introduction>
      <relatedTopics>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="1141a6169fedfc83a32c7dc03a5c9ca0" id="tgt17" class="tgtSentence">Knowledge Base article 117500</caps:sentence>
          </linkText>
          <linkUri>http://go.microsoft.com/fwlink/?LinkId=117500</linkUri>
        </externalLink>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">You can use a command to call a stored procedure.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The code sample at the end of this topic refers to a stored procedure in the Northwind sample database, called CustOrdersOrders, which is defined as follows.</caps:sentence>
        </para>
        <code>CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS
SELECT OrderID, OrderDate, RequiredDate, ShippedDate
FROM Orders
WHERE CustomerID = @CustomerID
ORDER BY OrderID</code>
        <para>
          <caps:sentence id="src3" class="srcSentence">See your SQL Server documentation for more information about how to define and call stored procedures.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">This stored procedure is similar to the command used in <legacyLink xlink:href="10e7ef4a-78bf-4e91-931e-cbc6c065dd4c">Command Object Parameters</legacyLink>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> It takes a customer ID parameter and returns information about that customer's orders.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The following code sample uses this stored procedure as the source for an ADO <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">Using the stored procedure allows you to access another capability of ADO: the <legacyBold>Parameters</legacyBold> collection <legacyBold>Refresh</legacyBold> method.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> By using this method, ADO can automatically fill in all information about the parameters required by the command at run time.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> There is a performance penalty in using this technique, because ADO must query the data source for the information about the parameters.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">Other important differences exist between the following code sample and the code in <legacyLink xlink:href="10e7ef4a-78bf-4e91-931e-cbc6c065dd4c">Command Object Parameters</legacyLink>, where the parameters were entered manually.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> First, this code does not set the <legacyBold>Prepared</legacyBold> property to <legacyBold>True</legacyBold> because it is a SQL Server stored procedure and is precompiled by definition.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Second, the <legacyBold>CommandType</legacyBold> property of the <legacyBold>Command</legacyBold> object changed to <legacyBold>adCmdStoredProc</legacyBold> in the second example to inform ADO that the command was a stored procedure.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">Finally, in the second example the parameter must be referred to by index when setting the value, because you might not know the name of the parameter at design time.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> If you do know the name of the parameter, you can set the new <legacyLink xlink:href="42409387-026c-435f-a9b1-bf4167095875">NamedParameters</legacyLink> property of the <legacyBold>Command</legacyBold> object to True and refer to the property's name.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> You might wonder why the position of the first parameter mentioned in the stored procedure (@CustomerID) is 1 instead of 0 (<codeInline>objCmd(1) = "ALFKI"</codeInline>).</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> This is because parameter 0 contains a return value from the SQL Server stored procedure.</caps:sentence>
        </para>
        <code>'BeginAutoParamCmd
    On Error GoTo ErrHandler:
    
    Dim objConn As New ADODB.Connection
    Dim objCmd As New ADODB.Command
    Dim objParm1 As New ADODB.Parameter
    Dim objRs As New ADODB.Recordset
    
    ' Set CommandText equal to the stored procedure name.
    objCmd.CommandText = "CustOrdersOrders"
    objCmd.CommandType = adCmdStoredProc
            
    ' Connect to the data source.
    Set objConn = GetNewConnection
    objCmd.ActiveConnection = objConn
        
    ' Automatically fill in parameter info from stored procedure.
    objCmd.Parameters.Refresh
    
    ' Set the param value.
    objCmd(1) = "ALFKI"
    
    ' Execute once and display...
    Set objRs = objCmd.Execute
        
    Debug.Print objParm1.Value
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
        
    ' ...then set new param value, re-execute command, and display.
    objCmd(1) = "CACTU"
    Set objRs = objCmd.Execute
        
    Debug.Print objParm1.Value
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
        
    'clean up
    objRs.Close
    objConn.Close
    Set objRs = Nothing
    Set objConn = Nothing
    Set objCmd = Nothing
    Set objParm1 = Nothing
    Exit Sub
    
ErrHandler:
    'clean up
    If objRs.State = adStateOpen Then
        objRs.Close
    End If
    
    If objConn.State = adStateOpen Then
        objConn.Close
    End If
    
    Set objRs = Nothing
    Set objConn = Nothing
    Set objCmd = Nothing
    Set objParm1 = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
'EndAutoParamCmd


'BeginNewConnection
Private Function GetNewConnection() As ADODB.Connection
    Dim oCn As New ADODB.Connection
    Dim sCnStr As String
    
    sCnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" &amp; _
             "Integrated Security='SSPI';Initial Catalog='Northwind';"
    oCn.Open sCnStr
    
    If oCn.State = adStateOpen Then
        Set GetNewConnection = oCn
    End If
    
End Function
'EndNewConnection</code>
      </introduction>
      <relatedTopics>
        <externalLink>
          <linkText>
            <caps:sentence id="src17" class="srcSentence">Knowledge Base article 117500</caps:sentence>
          </linkText>
          <linkUri>http://go.microsoft.com/fwlink/?LinkId=117500</linkUri>
        </externalLink>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
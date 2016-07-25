---
title: "Creating and Executing a Simple Command"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b81af6f-b9ae-4f7c-b59b-b5bdd775036f
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
# Creating and Executing a Simple Command
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c51b60a69a26855e78ff4e2e8cb3b501" id="tgt1" class="tgtSentence">A simple command is one that is not parameterized and requires no persistence.</caps:sentence>
          <caps:sentence sentenceid="9aba80e862013f2a2999e1d6e52d4b64" id="tgt2" class="tgtSentence"> There are three ways to create and execute a simple command.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="fda93d78a7003dbd72e28435e0583fda" id="tgt3" class="tgtSentence">Using a <legacyBold>Command</legacyBold> object</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="94e94e2bbee6a3fbc3ce7a7cac683832" id="tgt4" class="tgtSentence">Using a <legacyBold>Connection</legacyBold> object</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="2684066cf1e64aca2aa3c3c19b28858a" id="tgt5" class="tgtSentence">Using a <legacyBold>Recordset</legacyBold> object</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="5f28415b8036061bd6831b6d226ed1ae" id="tgt6" class="tgtSentence">Using a Command object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6a0f442d41340c433a0b6634cb85c689" id="tgt7" class="tgtSentence">To create a simple command using a <legacyBold>Command</legacyBold> object, you must assign the instruction to the <legacyBold>CommandText</legacyBold> property of a <legacyBold>Command</legacyBold> object and set the appropriate value for the <legacyBold>CommandType</legacyBold> property.</caps:sentence>
            <caps:sentence sentenceid="9d2280d5c9fa01bc579c4251f3ba923f" id="tgt8" class="tgtSentence"> Executing the command requires that an open connection is assigned to the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object, followed by a call to the <legacyBold>Execute</legacyBold> method on the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d0d5f2100c0973471a0d5c12c46c5fb0" id="tgt9" class="tgtSentence">The following code snippet shows the basic method of using the <legacyBold>Command</legacyBold> object to execute a command against a data source.</caps:sentence>
            <caps:sentence sentenceid="ac8f7a4dcaefeca5a9b2e4003ea04c11" id="tgt10" class="tgtSentence"> This example uses a row-returning command, and returns the results of the command execution as a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <code>    'BeginBasicCmd
    On Error GoTo ErrHandler:
    
    Dim objConn As New ADODB.Connection
    Dim objCmd As New ADODB.Command
    Dim objRs As New ADODB.Recordset
    
    objCmd.CommandText = "SELECT OrderID, OrderDate, " &amp; _
                         "RequiredDate, ShippedDate " &amp; _
                         "FROM Orders " &amp; _
                         "WHERE CustomerID = 'ALFKI' " &amp; _
                         "ORDER BY OrderID"
    objCmd.CommandType = adCmdText
    
    ' Connect to the data source.
    Set objConn = GetNewConnection
    objCmd.ActiveConnection = objConn
    
    ' Execute once and display...
    Set objRs = objCmd.Execute
    
    Debug.Print "ALFKI"
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
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
'EndBasicCmd


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
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4b7725914e8f0bd9057259e1b37dc06e" id="tgt11" class="tgtSentence">Using a Recordset object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="48eb1403e47f221dba3936c11dd47e0f" id="tgt12" class="tgtSentence">You can also create a command as a text string and pas it to the <legacyBold>Open</legacyBold> method on a <legacyBold>Recordset</legacyBold> object, together with the command type (adCmdText), for execution.</caps:sentence>
            <caps:sentence sentenceid="8fe7aa26357df0e66fc9d8e89db69e3e" id="tgt13" class="tgtSentence"> The following code snippet demonstrate this.</caps:sentence>
          </para>
          <code>    
    Const DS = "MySqlServer"
    Const DB = "Northwind"
    Const DP = "SQLOLEDB"
    
    Dim objRs As New ADODB.Recordset
    Dim CommandText As String
    Dim ConnctionString As String
    
    CommandText = "SELECT OrderID, OrderDate, " &amp; _
                         "RequiredDate, ShippedDate " &amp; _
                         "FROM Orders " &amp; _
                         "WHERE CustomerID = 'ALFKI' " &amp; _
                         "ORDER BY OrderID"
    ConnectionString = "Provider=" &amp; DP &amp; _
                       ";Data Source=" &amp; DS &amp; _
                       ";Initial Catalog=" &amp; DB &amp; _
                       ";Integrated Security=SSPI;"
    
    ' Connect to data source and execute the SQL command.
    objRs.Open <codeFeaturedElement xmlns="">CommandText</codeFeaturedElement>, ConnectionString, _
                adOpenStatic, adLockReadOnly, <codeFeaturedElement xmlns="">adCmdText</codeFeaturedElement>
    
    Debug.Print "ALFKI"
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
    
    'Clean up.
    objRs.Close
    Set objRs = Nothing</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="79a20ad8a9df3906b4d19d2d8a7d2550" id="tgt14" class="tgtSentence">Using a Connection object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ded162a5483e92bd07558110695681c6" id="tgt15" class="tgtSentence">You can also execute a command on an open Connection object.</caps:sentence>
            <caps:sentence sentenceid="6b26e45733f28311f05aea1c1bab843f" id="tgt16" class="tgtSentence"> The previous code example now becomes this:</caps:sentence>
          </para>
          <code>    Const DS = "MySqlServer"
    Const DB = "Northwind"
    Const DP = "SQLOLEDB"
    
    
    Dim objConn As New ADODB.Connection
    Dim objRs As New ADODB.Recordset
    
    CommandText = "SELECT OrderID, OrderDate, " &amp; _
                         "RequiredDate, ShippedDate " &amp; _
                         "FROM Orders " &amp; _
                         "WHERE CustomerID = 'ALFKI' " &amp; _
                         "ORDER BY OrderID"
                         
    ConnectionString = "Provider=" &amp; DP &amp; _
                       ";Data Source=" &amp; DS &amp; _
                       ";Initial Catalog=" &amp; DB &amp; _
                       ";Integrated Security=SSPI;"
    
    ' Connect to the data source.
    objConn.Open ConnectionString
    
    ' Execute command through the connection and display...
    Set objRs = objConn.Execute(<codeFeaturedElement xmlns="">CommandText</codeFeaturedElement>)
    
    Debug.Print "ALFKI"
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
    
    'Clean up.
    objRs.Close
    objConn.Close
    Set objRs = Nothing
    Set objConn = Nothing</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">A simple command is one that is not parameterized and requires no persistence.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> There are three ways to create and execute a simple command.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Using a <legacyBold>Command</legacyBold> object</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Using a <legacyBold>Connection</legacyBold> object</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Using a <legacyBold>Recordset</legacyBold> object</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Using a Command object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">To create a simple command using a <legacyBold>Command</legacyBold> object, you must assign the instruction to the <legacyBold>CommandText</legacyBold> property of a <legacyBold>Command</legacyBold> object and set the appropriate value for the <legacyBold>CommandType</legacyBold> property.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Executing the command requires that an open connection is assigned to the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object, followed by a call to the <legacyBold>Execute</legacyBold> method on the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The following code snippet shows the basic method of using the <legacyBold>Command</legacyBold> object to execute a command against a data source.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> This example uses a row-returning command, and returns the results of the command execution as a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <code>    'BeginBasicCmd
    On Error GoTo ErrHandler:
    
    Dim objConn As New ADODB.Connection
    Dim objCmd As New ADODB.Command
    Dim objRs As New ADODB.Recordset
    
    objCmd.CommandText = "SELECT OrderID, OrderDate, " &amp; _
                         "RequiredDate, ShippedDate " &amp; _
                         "FROM Orders " &amp; _
                         "WHERE CustomerID = 'ALFKI' " &amp; _
                         "ORDER BY OrderID"
    objCmd.CommandType = adCmdText
    
    ' Connect to the data source.
    Set objConn = GetNewConnection
    objCmd.ActiveConnection = objConn
    
    ' Execute once and display...
    Set objRs = objCmd.Execute
    
    Debug.Print "ALFKI"
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
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
'EndBasicCmd


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
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Using a Recordset object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">You can also create a command as a text string and pas it to the <legacyBold>Open</legacyBold> method on a <legacyBold>Recordset</legacyBold> object, together with the command type (adCmdText), for execution.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> The following code snippet demonstrate this.</caps:sentence>
          </para>
          <code>    
    Const DS = "MySqlServer"
    Const DB = "Northwind"
    Const DP = "SQLOLEDB"
    
    Dim objRs As New ADODB.Recordset
    Dim CommandText As String
    Dim ConnctionString As String
    
    CommandText = "SELECT OrderID, OrderDate, " &amp; _
                         "RequiredDate, ShippedDate " &amp; _
                         "FROM Orders " &amp; _
                         "WHERE CustomerID = 'ALFKI' " &amp; _
                         "ORDER BY OrderID"
    ConnectionString = "Provider=" &amp; DP &amp; _
                       ";Data Source=" &amp; DS &amp; _
                       ";Initial Catalog=" &amp; DB &amp; _
                       ";Integrated Security=SSPI;"
    
    ' Connect to data source and execute the SQL command.
    objRs.Open <codeFeaturedElement xmlns="">CommandText</codeFeaturedElement>, ConnectionString, _
                adOpenStatic, adLockReadOnly, <codeFeaturedElement xmlns="">adCmdText</codeFeaturedElement>
    
    Debug.Print "ALFKI"
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
    
    'Clean up.
    objRs.Close
    Set objRs = Nothing</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Using a Connection object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">You can also execute a command on an open Connection object.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> The previous code example now becomes this:</caps:sentence>
          </para>
          <code>    Const DS = "MySqlServer"
    Const DB = "Northwind"
    Const DP = "SQLOLEDB"
    
    
    Dim objConn As New ADODB.Connection
    Dim objRs As New ADODB.Recordset
    
    CommandText = "SELECT OrderID, OrderDate, " &amp; _
                         "RequiredDate, ShippedDate " &amp; _
                         "FROM Orders " &amp; _
                         "WHERE CustomerID = 'ALFKI' " &amp; _
                         "ORDER BY OrderID"
                         
    ConnectionString = "Provider=" &amp; DP &amp; _
                       ";Data Source=" &amp; DS &amp; _
                       ";Initial Catalog=" &amp; DB &amp; _
                       ";Integrated Security=SSPI;"
    
    ' Connect to the data source.
    objConn.Open ConnectionString
    
    ' Execute command through the connection and display...
    Set objRs = objConn.Execute(<codeFeaturedElement xmlns="">CommandText</codeFeaturedElement>)
    
    Debug.Print "ALFKI"
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
    
    'Clean up.
    objRs.Close
    objConn.Close
    Set objRs = Nothing
    Set objConn = Nothing</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
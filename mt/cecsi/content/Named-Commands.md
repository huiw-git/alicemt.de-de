---
title: "Named Commands"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5a0ec8f9-5ba3-4f9f-b80d-2073aa049586
caps.latest.revision: 13
caps.handback.revision: 13
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
# Named Commands
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b5527adee24016911030959c3a13ba05" id="tgt1" class="tgtSentence">
            <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Creating and Executing a Simple Command</legacyLink> shows one way to execute a command.</caps:sentence>
          <caps:sentence sentenceid="661c1ad026914abd4e368015e459b5f6" id="tgt2" class="tgtSentence"> There is another way: you can make it a named command, and then call this named command directly on the <legacyBold>Connection</legacyBold> object (assigned to the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object).</caps:sentence>
          <caps:sentence sentenceid="a64b5338386ab0649b0508062055c34d" id="tgt3" class="tgtSentence"> Naming a command means assigning a name to the <legacyBold>Name</legacyBold> property of a <legacyBold>Command</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="2c802c1c3cc7a4e8d0693decfaa19694" id="tgt4" class="tgtSentence"> For example,</caps:sentence>
        </para>
        <code>objCmd.Name = "GetCustomers"
objCmd.ActiveConnection = objConn
objConn.GetCustomers objRs</code>
        <para>
          <caps:sentence sentenceid="627f9948d008b3c3ef32fce651245e52" id="tgt5" class="tgtSentence">The named command acts as if it were a "custom method" on the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="60f4392466fb2b7a9021499d574243b4" id="tgt6" class="tgtSentence"> The result of the command is returned as an out parameter of this "custom method".</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fffd2170a9236866cf35846d6ac4f25f" id="tgt7" class="tgtSentence">The following example illustrates this feature.</caps:sentence>
        </para>
        <code>'BeginNamedCmd
    On Error GoTo ErrHandler:
    
    Dim objConn As New ADODB.Connection
    Dim objCmd As New ADODB.Command
    Dim objRs As New ADODB.Recordset
    
    ' Connect to the data source.
    Set objConn = GetNewConnection
    
    objCmd.CommandText = "SELECT CustomerID, CompanyName FROM Customers"
    objCmd.CommandType = adCmdText
    
    'Name the command.
    objCmd.Name = "GetCustomers"
    
    objCmd.ActiveConnection = objConn
    
    ' Execute using Command.Name from the Connection.
    objConn.GetCustomers objRs
    
    ' Display.
    Do While Not objRs.EOF
        Debug.Print objRs(0) &amp; vbTab &amp; objRs(1)
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
'EndNamedCmd</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Creating and Executing a Simple Command</legacyLink> shows one way to execute a command.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> There is another way: you can make it a named command, and then call this named command directly on the <legacyBold>Connection</legacyBold> object (assigned to the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object).</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Naming a command means assigning a name to the <legacyBold>Name</legacyBold> property of a <legacyBold>Command</legacyBold> object.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example,</caps:sentence>
        </para>
        <code>objCmd.Name = "GetCustomers"
objCmd.ActiveConnection = objConn
objConn.GetCustomers objRs</code>
        <para>
          <caps:sentence id="src5" class="srcSentence">The named command acts as if it were a "custom method" on the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The result of the command is returned as an out parameter of this "custom method".</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">The following example illustrates this feature.</caps:sentence>
        </para>
        <code>'BeginNamedCmd
    On Error GoTo ErrHandler:
    
    Dim objConn As New ADODB.Connection
    Dim objCmd As New ADODB.Command
    Dim objRs As New ADODB.Recordset
    
    ' Connect to the data source.
    Set objConn = GetNewConnection
    
    objCmd.CommandText = "SELECT CustomerID, CompanyName FROM Customers"
    objCmd.CommandType = adCmdText
    
    'Name the command.
    objCmd.Name = "GetCustomers"
    
    objCmd.ActiveConnection = objConn
    
    ' Execute using Command.Name from the Connection.
    objConn.GetCustomers objRs
    
    ' Display.
    Do While Not objRs.EOF
        Debug.Print objRs(0) &amp; vbTab &amp; objRs(1)
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
'EndNamedCmd</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
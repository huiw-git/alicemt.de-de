---
title: "ActiveCommand Property Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 23b06499-62df-4f46-88eb-6da392f9b456
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
# ActiveCommand Property Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a046721d7b384dc7dacb163e6aca52bd" id="tgt1" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="fb4088d5-5968-42d6-aeaa-3955046bb4da">ActiveCommand</legacyLink> property.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9571b9a1367985211abeea17bb3ede91" id="tgt2" class="tgtSentence">A subroutine is given a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object whose <legacyBold>ActiveCommand</legacyBold> property is used to display the command text and parameter that created the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <code>'BeginActiveCommandVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string

Public Sub Main()
    On Error GoTo ErrorHandler

        'recordset and connection variables
    Dim cmd As ADODB.Command
    Dim rst As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
        'record variables
    Dim strPrompt As String
    Dim strName As String
    
    Set Cnxn = New ADODB.Connection
    Set cmd = New ADODB.Command
    
    strPrompt = "Enter an author's name (e.g., Ringer): "
    strName = Trim(InputBox(strPrompt, "ActiveCommandX Example"))
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
        
        'create SQL command string
    cmd.CommandText = "SELECT * FROM Authors WHERE au_lname = ?"
    cmd.Parameters.Append cmd.CreateParameter("LastName", adChar, adParamInput, 20, strName)
    
    Cnxn.Open strCnxn
    cmd.ActiveConnection = Cnxn
    
        'create the recordset by executing command string
    Set rst = cmd.Execute(, , adCmdText)
        'see the results
    Call ActiveCommandXprint(rst)
  
    ' clean up
    Cnxn.Close
    Set rst = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rst Is Nothing Then
        If rst.State = adStateOpen Then rst.Close
    End If
    Set rst = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndActiveCommandVB</code>
        <para>
          <caps:sentence sentenceid="34541e71739d77d0e70eac4e60e822e4" id="tgt3" class="tgtSentence">The <legacyBold>ActiveCommandXprint</legacyBold> routine is given only a <legacyBold>Recordset</legacyBold> object, yet it must print the command text and parameter that created the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="34777f5d415643d221b386150a65ee44" id="tgt4" class="tgtSentence"> This can be done because the <legacyBold>Recordset</legacyBold> object's <legacyBold>ActiveCommand</legacyBold> property yields the associated <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3ca0e130c828cf87f6236ff0a9378a18" id="tgt5" class="tgtSentence">The <legacyBold>Command</legacyBold> object's <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property yields the parameterized command that created the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="43577eb156aec39693742292c3012a9b" id="tgt6" class="tgtSentence"> The <legacyBold>Command</legacyBold> object's <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection yields the value that was substituted for the command's parameter placeholder ("<legacyBold>?</legacyBold>").</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="87922231dc3fbda1582d6b0a5da8fc71" id="tgt7" class="tgtSentence">Finally, an error message or the author's name and ID are printed.</caps:sentence>
        </para>
        <code>'BeginActiveCommandPrintVB
Public Sub ActiveCommandXprint(rstp As ADODB.Recordset)

    Dim strName As String
    
    strName = rstp.ActiveCommand.Parameters.Item("LastName").Value
    
    Debug.Print "Command text = '"; rstp.ActiveCommand.CommandText; "'"
    Debug.Print "Parameter = '"; strName; "'"
    
    If rstp.BOF = True Then
       Debug.Print "Name = '"; strName; "', not found."
    Else
       Debug.Print "Name = '"; rstp!au_fname; " "; rstp!au_lname; _
             "', author ID = '"; rstp!au_id; "'"
    End If

    rstp.Close
    Set rstp = Nothing
End Sub
'EndActiveCommandPrintVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="fb4088d5-5968-42d6-aeaa-3955046bb4da">ActiveCommand Property</link>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example demonstrates the <legacyLink xlink:href="fb4088d5-5968-42d6-aeaa-3955046bb4da">ActiveCommand</legacyLink> property.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">A subroutine is given a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object whose <legacyBold>ActiveCommand</legacyBold> property is used to display the command text and parameter that created the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <code>'BeginActiveCommandVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string

Public Sub Main()
    On Error GoTo ErrorHandler

        'recordset and connection variables
    Dim cmd As ADODB.Command
    Dim rst As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
        'record variables
    Dim strPrompt As String
    Dim strName As String
    
    Set Cnxn = New ADODB.Connection
    Set cmd = New ADODB.Command
    
    strPrompt = "Enter an author's name (e.g., Ringer): "
    strName = Trim(InputBox(strPrompt, "ActiveCommandX Example"))
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
        
        'create SQL command string
    cmd.CommandText = "SELECT * FROM Authors WHERE au_lname = ?"
    cmd.Parameters.Append cmd.CreateParameter("LastName", adChar, adParamInput, 20, strName)
    
    Cnxn.Open strCnxn
    cmd.ActiveConnection = Cnxn
    
        'create the recordset by executing command string
    Set rst = cmd.Execute(, , adCmdText)
        'see the results
    Call ActiveCommandXprint(rst)
  
    ' clean up
    Cnxn.Close
    Set rst = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rst Is Nothing Then
        If rst.State = adStateOpen Then rst.Close
    End If
    Set rst = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndActiveCommandVB</code>
        <para>
          <caps:sentence id="src3" class="srcSentence">The <legacyBold>ActiveCommandXprint</legacyBold> routine is given only a <legacyBold>Recordset</legacyBold> object, yet it must print the command text and parameter that created the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> This can be done because the <legacyBold>Recordset</legacyBold> object's <legacyBold>ActiveCommand</legacyBold> property yields the associated <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The <legacyBold>Command</legacyBold> object's <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property yields the parameterized command that created the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The <legacyBold>Command</legacyBold> object's <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection yields the value that was substituted for the command's parameter placeholder ("<legacyBold>?</legacyBold>").</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">Finally, an error message or the author's name and ID are printed.</caps:sentence>
        </para>
        <code>'BeginActiveCommandPrintVB
Public Sub ActiveCommandXprint(rstp As ADODB.Recordset)

    Dim strName As String
    
    strName = rstp.ActiveCommand.Parameters.Item("LastName").Value
    
    Debug.Print "Command text = '"; rstp.ActiveCommand.CommandText; "'"
    Debug.Print "Parameter = '"; strName; "'"
    
    If rstp.BOF = True Then
       Debug.Print "Name = '"; strName; "', not found."
    Else
       Debug.Print "Name = '"; rstp!au_fname; " "; rstp!au_lname; _
             "', author ID = '"; rstp!au_id; "'"
    End If

    rstp.Close
    Set rstp = Nothing
End Sub
'EndActiveCommandPrintVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="fb4088d5-5968-42d6-aeaa-3955046bb4da">ActiveCommand Property</link>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
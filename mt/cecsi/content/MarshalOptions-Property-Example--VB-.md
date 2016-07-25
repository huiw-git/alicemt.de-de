---
title: "MarshalOptions Property Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ae576b2c-65aa-4838-872a-85e618806dc8
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
# MarshalOptions Property Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="99eacb1a3760e9710fb5e478ffdc3960" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">MarshalOptions</legacyLink> property to specify what rows are sent back to the server — All Rows or only Modified Rows.</caps:sentence>
        </para>
        <code>'BeginMarshalOptionsVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string

Public Sub Main()
    On Error GoTo ErrorHandler

    Dim rstEmployees As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
    Dim strSQLEmployees As String
    
    Dim strOldFirst As String
    Dim strOldLast As String
    Dim strMessage As String
    Dim strMarshalAll As String
    Dim strMarshalModified As String
    
    ' Open connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Set Cnxn = New ADODB.Connection
    Cnxn.Open strCnxn
    
    ' open recordset with names from Employees table
    ' and set some properties through object refs
    Set rstEmployees = New ADODB.Recordset
    rstEmployees.CursorType = adOpenKeyset
    rstEmployees.LockType = adLockOptimistic
    rstEmployees.CursorLocation = adUseClient
    
    strSQLEmployees = "SELECT fname, lname FROM Employee ORDER BY lname"
    
    rstEmployees.Open strSQLEmployees, Cnxn, , , adCmdText
     ' empty properties have been set above
    
     ' Store original data
    strOldFirst = rstEmployees!fname
    strOldLast = rstEmployees!lname
    
    ' Change data in edit buffer
    rstEmployees!fname = "Linda"
    rstEmployees!lname = "Kobara"
    
    ' Show contents of buffer and get user input
    strMessage = "Edit in progress:" &amp; vbCr &amp; _
        " Original data = " &amp; strOldFirst &amp; " " &amp; _
        strOldLast &amp; vbCr &amp; " Data in buffer = " &amp; _
        rstEmployees!fname &amp; " " &amp; rstEmployees!lname &amp; vbCr &amp; vbCr &amp; _
        "Use Update to replace the original data with " &amp; _
        "the buffered data in the Recordset?"
    strMarshalAll = "Would you like to send all the rows " &amp; _
        "in the recordset back to the server?"
    strMarshalModified = "Would you like to send only " &amp; _
        "modified rows back to the server?"
    
    If MsgBox(strMessage, vbYesNo) = vbYes Then
        If MsgBox(strMarshalAll, vbYesNo) = vbYes Then
            rstEmployees.MarshalOptions = adMarshalAll
            rstEmployees.Update
        ElseIf MsgBox(strMarshalModified, vbYesNo) = vbYes Then
            rstEmployees.MarshalOptions = adMarshalModifiedOnly
            rstEmployees.Update
        End If
    End If
    
    ' sShow the resulting data
    MsgBox "Data in recordset = " &amp; rstEmployees!fname &amp; " " &amp; _
        rstEmployees!lname
    
    ' restore original data because this is a demonstration
    If Not (strOldFirst = rstEmployees!fname And _
            strOldLast = rstEmployees!lname) Then
        rstEmployees!fname = strOldFirst
        rstEmployees!lname = strOldLast
        rstEmployees.Update
    End If

    ' clean up
    rstEmployees.Close
    Cnxn.Close
    Set rstEmployees = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rstEmployees Is Nothing Then
        If rstEmployees.State = adStateOpen Then rstEmployees.Close
    End If
    Set rstEmployees = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndMarshalOptionsVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">MarshalOptions Property</link>
        <link xlink:href="4013075d-dbea-4bbc-a6f4-c345a55c5633">MarshalOptionsEnum</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">MarshalOptions</legacyLink> property to specify what rows are sent back to the server — All Rows or only Modified Rows.</caps:sentence>
        </para>
        <code>'BeginMarshalOptionsVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string

Public Sub Main()
    On Error GoTo ErrorHandler

    Dim rstEmployees As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
    Dim strSQLEmployees As String
    
    Dim strOldFirst As String
    Dim strOldLast As String
    Dim strMessage As String
    Dim strMarshalAll As String
    Dim strMarshalModified As String
    
    ' Open connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Set Cnxn = New ADODB.Connection
    Cnxn.Open strCnxn
    
    ' open recordset with names from Employees table
    ' and set some properties through object refs
    Set rstEmployees = New ADODB.Recordset
    rstEmployees.CursorType = adOpenKeyset
    rstEmployees.LockType = adLockOptimistic
    rstEmployees.CursorLocation = adUseClient
    
    strSQLEmployees = "SELECT fname, lname FROM Employee ORDER BY lname"
    
    rstEmployees.Open strSQLEmployees, Cnxn, , , adCmdText
     ' empty properties have been set above
    
     ' Store original data
    strOldFirst = rstEmployees!fname
    strOldLast = rstEmployees!lname
    
    ' Change data in edit buffer
    rstEmployees!fname = "Linda"
    rstEmployees!lname = "Kobara"
    
    ' Show contents of buffer and get user input
    strMessage = "Edit in progress:" &amp; vbCr &amp; _
        " Original data = " &amp; strOldFirst &amp; " " &amp; _
        strOldLast &amp; vbCr &amp; " Data in buffer = " &amp; _
        rstEmployees!fname &amp; " " &amp; rstEmployees!lname &amp; vbCr &amp; vbCr &amp; _
        "Use Update to replace the original data with " &amp; _
        "the buffered data in the Recordset?"
    strMarshalAll = "Would you like to send all the rows " &amp; _
        "in the recordset back to the server?"
    strMarshalModified = "Would you like to send only " &amp; _
        "modified rows back to the server?"
    
    If MsgBox(strMessage, vbYesNo) = vbYes Then
        If MsgBox(strMarshalAll, vbYesNo) = vbYes Then
            rstEmployees.MarshalOptions = adMarshalAll
            rstEmployees.Update
        ElseIf MsgBox(strMarshalModified, vbYesNo) = vbYes Then
            rstEmployees.MarshalOptions = adMarshalModifiedOnly
            rstEmployees.Update
        End If
    End If
    
    ' sShow the resulting data
    MsgBox "Data in recordset = " &amp; rstEmployees!fname &amp; " " &amp; _
        rstEmployees!lname
    
    ' restore original data because this is a demonstration
    If Not (strOldFirst = rstEmployees!fname And _
            strOldLast = rstEmployees!lname) Then
        rstEmployees!fname = strOldFirst
        rstEmployees!lname = strOldLast
        rstEmployees.Update
    End If

    ' clean up
    rstEmployees.Close
    Cnxn.Close
    Set rstEmployees = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rstEmployees Is Nothing Then
        If rstEmployees.State = adStateOpen Then rstEmployees.Close
    End If
    Set rstEmployees = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndMarshalOptionsVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">MarshalOptions Property</link>
        <link xlink:href="4013075d-dbea-4bbc-a6f4-c345a55c5633">MarshalOptionsEnum</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
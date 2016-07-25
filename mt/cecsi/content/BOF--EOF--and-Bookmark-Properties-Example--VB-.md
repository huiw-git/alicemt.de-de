---
title: "BOF, EOF, and Bookmark Properties Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b6573c6e-fee8-4267-a722-fadaec6eafe6
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
# BOF, EOF, and Bookmark Properties Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2a0293054bea293e0e55d6f92ada324d" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> and <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> properties to display a message if a user tries to move past the first or last record of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="0035840dcb01b1d7a9689f05a0257064" id="tgt2" class="tgtSentence"> It uses the <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink> property to let the user flag a record in a <legacyBold>Recordset</legacyBold> and return to it later.</caps:sentence>
        </para>
        <code>'BeginBOFVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string
    
Public Sub Main()
    On Error GoTo ErrorHandler

    'recordset and connection variables
    Dim Cnxn As ADODB.Connection
    Dim rstPublishers As ADODB.Recordset
    Dim strCnxn As String
    Dim strSQLPubs As String
     'record variables
    Dim strMessage As String
    Dim intCommand As Integer
    Dim varBookmark As Variant
     
     ' open connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
       
     ' Open recordset and use client cursor
     ' to enable AbsolutePosition property
    Set rstPublishers = New ADODB.Recordset
    strSQLPubs = "SELECT pub_id, pub_name FROM publishers ORDER BY pub_name"
    rstPublishers.Open strSQLPubs, strCnxn, adUseClient, adOpenStatic, adCmdText
    
    rstPublishers.MoveFirst
    Do Until rstPublishers.EOF
        ' Display information about current record
        ' and get user input
        strMessage = "Publisher: " &amp; rstPublishers!pub_name &amp; _
            vbCr &amp; "(record " &amp; rstPublishers.AbsolutePosition &amp; _
            " of " &amp; rstPublishers.RecordCount &amp; ")" &amp; vbCr &amp; vbCr &amp; _
            "Enter command:" &amp; vbCr &amp; _
            "[1 - next / 2 - previous /" &amp; vbCr &amp; _
            "3 - set bookmark / 4 - go to bookmark]"
        intCommand = Val(InputBox(strMessage))

        ' Check user input
        Select Case intCommand
            Case 1
                ' Move forward trapping for EOF
                rstPublishers.MoveNext
                If rstPublishers.EOF Then
                    MsgBox "Moving past the last record." &amp; _
                        vbCr &amp; "Try again."
                    rstPublishers.MoveLast
                End If
            Case 2
                ' Move backward trapping for BOF
                rstPublishers.MovePrevious
                If rstPublishers.BOF Then
                    MsgBox "Moving past the first record." &amp; _
                        vbCr &amp; "Try again."
                    rstPublishers.MoveFirst
                End If
            Case 3
                ' Store the bookmark of the current record
                varBookmark = rstPublishers.Bookmark
            Case 4
                ' Go to the record indicated by the stored bookmark
                If IsEmpty(varBookmark) Then
                    MsgBox "No Bookmark set!"
                Else
                    rstPublishers.Bookmark = varBookmark
                End If
            Case Else
                Exit Do
        End Select
    Loop

    ' clean up
    rstPublishers.Close
    Cnxn.Close
    Set rstPublishers = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rstPublishers Is Nothing Then
        If rstPublishers.State = adStateOpen Then rstPublishers.Close
    End If
    Set rstPublishers = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndBOFVB</code>
        <para>
          <caps:sentence sentenceid="4059b0e84d8fb66b669f28518f1d1bbd" id="tgt3" class="tgtSentence">This example uses the <legacyBold>Bookmark</legacyBold> and <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> properties to create a limited view of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="12a0a429e45a1b68f2be4a940ee55002" id="tgt4" class="tgtSentence"> Only records referenced by the array of bookmarks are accessible.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "BOF"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF, EOF Properties</link>
        <link xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> and <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> properties to display a message if a user tries to move past the first or last record of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It uses the <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink> property to let the user flag a record in a <legacyBold>Recordset</legacyBold> and return to it later.</caps:sentence>
        </para>
        <code>'BeginBOFVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string
    
Public Sub Main()
    On Error GoTo ErrorHandler

    'recordset and connection variables
    Dim Cnxn As ADODB.Connection
    Dim rstPublishers As ADODB.Recordset
    Dim strCnxn As String
    Dim strSQLPubs As String
     'record variables
    Dim strMessage As String
    Dim intCommand As Integer
    Dim varBookmark As Variant
     
     ' open connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
       
     ' Open recordset and use client cursor
     ' to enable AbsolutePosition property
    Set rstPublishers = New ADODB.Recordset
    strSQLPubs = "SELECT pub_id, pub_name FROM publishers ORDER BY pub_name"
    rstPublishers.Open strSQLPubs, strCnxn, adUseClient, adOpenStatic, adCmdText
    
    rstPublishers.MoveFirst
    Do Until rstPublishers.EOF
        ' Display information about current record
        ' and get user input
        strMessage = "Publisher: " &amp; rstPublishers!pub_name &amp; _
            vbCr &amp; "(record " &amp; rstPublishers.AbsolutePosition &amp; _
            " of " &amp; rstPublishers.RecordCount &amp; ")" &amp; vbCr &amp; vbCr &amp; _
            "Enter command:" &amp; vbCr &amp; _
            "[1 - next / 2 - previous /" &amp; vbCr &amp; _
            "3 - set bookmark / 4 - go to bookmark]"
        intCommand = Val(InputBox(strMessage))

        ' Check user input
        Select Case intCommand
            Case 1
                ' Move forward trapping for EOF
                rstPublishers.MoveNext
                If rstPublishers.EOF Then
                    MsgBox "Moving past the last record." &amp; _
                        vbCr &amp; "Try again."
                    rstPublishers.MoveLast
                End If
            Case 2
                ' Move backward trapping for BOF
                rstPublishers.MovePrevious
                If rstPublishers.BOF Then
                    MsgBox "Moving past the first record." &amp; _
                        vbCr &amp; "Try again."
                    rstPublishers.MoveFirst
                End If
            Case 3
                ' Store the bookmark of the current record
                varBookmark = rstPublishers.Bookmark
            Case 4
                ' Go to the record indicated by the stored bookmark
                If IsEmpty(varBookmark) Then
                    MsgBox "No Bookmark set!"
                Else
                    rstPublishers.Bookmark = varBookmark
                End If
            Case Else
                Exit Do
        End Select
    Loop

    ' clean up
    rstPublishers.Close
    Cnxn.Close
    Set rstPublishers = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rstPublishers Is Nothing Then
        If rstPublishers.State = adStateOpen Then rstPublishers.Close
    End If
    Set rstPublishers = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndBOFVB</code>
        <para>
          <caps:sentence id="src3" class="srcSentence">This example uses the <legacyBold>Bookmark</legacyBold> and <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> properties to create a limited view of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Only records referenced by the array of bookmarks are accessible.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "BOF"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF, EOF Properties</link>
        <link xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
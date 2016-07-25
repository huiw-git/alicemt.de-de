---
title: "CompareBookmarks Method Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f156aa48-bfc2-40d1-962b-7b08855776c6
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
# CompareBookmarks Method Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3f8f464c0b78c3dc4a393dccc3fbfe16" id="tgt1" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="d0b64286-2cc4-4a22-8f1d-9aefeebbcbc6">CompareBookmarks</legacyLink> method.</caps:sentence>
          <caps:sentence sentenceid="6917b470520f9e2ac02dc11d1b7ed2b2" id="tgt2" class="tgtSentence"> The relative value of bookmarks is seldom needed unless a particular bookmark is somehow special.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="67816fde461b405bfea56039e9af33ae" id="tgt3" class="tgtSentence">Designate a random row of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> derived from the <legacyBold><legacyItalic>Authors</legacyItalic></legacyBold> table as the target of a search.</caps:sentence>
          <caps:sentence sentenceid="27021e4281a2f689b0322ad602fff171" id="tgt4" class="tgtSentence"> Then display the position of each row relative to that target.</caps:sentence>
        </para>
        <code>'BeginCompareBookmarksVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string
    
Public Sub Main()
    On Error GoTo ErrorHandler
    
     ' recordset and connection variables
    Dim rstAuthors As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strSQLAuthors As String
    Dim strCnxn As String
    
     ' comparison variables
    Dim count As Integer
    Dim target As Variant
    Dim result As Long
    Dim strAnswer As String
    Dim strTitle As String
    strTitle = "CompareBookmarks Example"
    
    ' Open a connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn

     ' Open recordset as a static cursor type recordset
    Set rstAuthors = New ADODB.Recordset
    strSQLAuthors = "SELECT * FROM Authors"
    rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText
    
    count = rstAuthors.RecordCount
    Debug.Print "Rows in the Recordset = "; count
    
     ' Exit if an empty recordset
    If count = 0 Then Exit Sub
    
     ' Get position between 0 and count -1
    Randomize
    count = (Int(count * Rnd))
    Debug.Print "Randomly chosen row position = "; count
     ' Move row to random position
    rstAuthors.Move count, adBookmarkFirst
     ' Remember the mystery row
    target = rstAuthors.Bookmark
    
    count = 0
    rstAuthors.MoveFirst
         ' Loop through recordset
    Do Until rstAuthors.EOF
       result = rstAuthors.CompareBookmarks(rstAuthors.Bookmark, target)
       
       If result = adCompareNotEqual Then
          Debug.Print "Row "; count; ": Bookmarks are not equal."
       ElseIf result = adCompareNotComparable Then
          Debug.Print "Row "; count; ": Bookmarks are not comparable."
       Else
          Select Case result
             Case adCompareLessThan
                strAnswer = "less than"
             Case adCompareEqual
                strAnswer = "equal to"
             Case adCompareGreaterThan
                strAnswer = "greater than"
             Case Else
                strAnswer = "in error comparing to"
          End Select
            'show the results row-by-row
          Debug.Print "Row position " &amp; count &amp; " is " &amp; strAnswer &amp; " the target."
       End If
       
       count = count + 1
       rstAuthors.MoveNext
    Loop
    
    ' clean up
    rstAuthors.Close
    Cnxn.Close
    Set rstAuthors = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rstAuthors Is Nothing Then
        If rstAuthors.State = adStateOpen Then rstAuthors.Close
    End If
    Set rstAuthors = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
    
End Sub
'EndCompareBookmarksVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d0b64286-2cc4-4a22-8f1d-9aefeebbcbc6">CompareBookmarks Method</link>
        <link xlink:href="bc8f710d-0621-4673-8d8e-0361e44abed0">CompareEnum</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example demonstrates the <legacyLink xlink:href="d0b64286-2cc4-4a22-8f1d-9aefeebbcbc6">CompareBookmarks</legacyLink> method.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The relative value of bookmarks is seldom needed unless a particular bookmark is somehow special.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Designate a random row of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> derived from the <legacyBold><legacyItalic>Authors</legacyItalic></legacyBold> table as the target of a search.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Then display the position of each row relative to that target.</caps:sentence>
        </para>
        <code>'BeginCompareBookmarksVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string
    
Public Sub Main()
    On Error GoTo ErrorHandler
    
     ' recordset and connection variables
    Dim rstAuthors As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strSQLAuthors As String
    Dim strCnxn As String
    
     ' comparison variables
    Dim count As Integer
    Dim target As Variant
    Dim result As Long
    Dim strAnswer As String
    Dim strTitle As String
    strTitle = "CompareBookmarks Example"
    
    ' Open a connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn

     ' Open recordset as a static cursor type recordset
    Set rstAuthors = New ADODB.Recordset
    strSQLAuthors = "SELECT * FROM Authors"
    rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText
    
    count = rstAuthors.RecordCount
    Debug.Print "Rows in the Recordset = "; count
    
     ' Exit if an empty recordset
    If count = 0 Then Exit Sub
    
     ' Get position between 0 and count -1
    Randomize
    count = (Int(count * Rnd))
    Debug.Print "Randomly chosen row position = "; count
     ' Move row to random position
    rstAuthors.Move count, adBookmarkFirst
     ' Remember the mystery row
    target = rstAuthors.Bookmark
    
    count = 0
    rstAuthors.MoveFirst
         ' Loop through recordset
    Do Until rstAuthors.EOF
       result = rstAuthors.CompareBookmarks(rstAuthors.Bookmark, target)
       
       If result = adCompareNotEqual Then
          Debug.Print "Row "; count; ": Bookmarks are not equal."
       ElseIf result = adCompareNotComparable Then
          Debug.Print "Row "; count; ": Bookmarks are not comparable."
       Else
          Select Case result
             Case adCompareLessThan
                strAnswer = "less than"
             Case adCompareEqual
                strAnswer = "equal to"
             Case adCompareGreaterThan
                strAnswer = "greater than"
             Case Else
                strAnswer = "in error comparing to"
          End Select
            'show the results row-by-row
          Debug.Print "Row position " &amp; count &amp; " is " &amp; strAnswer &amp; " the target."
       End If
       
       count = count + 1
       rstAuthors.MoveNext
    Loop
    
    ' clean up
    rstAuthors.Close
    Cnxn.Close
    Set rstAuthors = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rstAuthors Is Nothing Then
        If rstAuthors.State = adStateOpen Then rstAuthors.Close
    End If
    Set rstAuthors = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
    
End Sub
'EndCompareBookmarksVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d0b64286-2cc4-4a22-8f1d-9aefeebbcbc6">CompareBookmarks Method</link>
        <link xlink:href="bc8f710d-0621-4673-8d8e-0361e44abed0">CompareEnum</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
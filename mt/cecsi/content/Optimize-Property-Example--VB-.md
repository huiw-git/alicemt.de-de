---
title: "Optimize Property Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 652194af-cfa4-4aa0-a6d6-fa409bbc3f98
caps.latest.revision: 10
caps.handback.revision: 10
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
# Optimize Property Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b84724720567e68f2e83efe19855d85d" id="tgt1" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object's dynamic <legacyBold>Optimize</legacyBold> property.</caps:sentence>
          <caps:sentence sentenceid="57e70469741ff0c6d527dec4f2c877ef" id="tgt2" class="tgtSentence"> The <legacyBold><legacyItalic>zip</legacyItalic></legacyBold> field of the <legacyBold><legacyItalic>Authors</legacyItalic></legacyBold> table in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database is not indexed.</caps:sentence>
          <caps:sentence sentenceid="fa431903ce66a217bba16e9d773d0bfc" id="tgt3" class="tgtSentence"> Setting the <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> property to <languageKeyword>True</languageKeyword> on the <legacyBold><legacyItalic>zip</legacyItalic></legacyBold> field authorizes ADO to build an index that improves the performance of the <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find</legacyLink> method.</caps:sentence>
        </para>
        <code>'BeginOptimizeVB
Public Sub Main()
    On Error GoTo ErrorHandler

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string.

    ' Declare the recordset and connection variables.
    Dim Cnxn As ADODB.Connection
    Dim rstAuthors As ADODB.Recordset
    Dim strCnxn As String
    Dim strSQLAuthors As String
    
     ' Open connection.
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Set Cnxn = New ADODB.Connection
    Cnxn.Open strCnxn
     
     ' open recordset client-side to enable index creation.
    Set rstAuthors = New ADODB.Recordset
    rstAuthors.CursorLocation = adUseClient
    strSQLAuthors = "SELECT * FROM Authors"
    rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText
     ' Create the index.
    rstAuthors!zip.Properties("Optimize") = True
     ' Find Akiko Yokomoto
    rstAuthors.Find "zip = '94595'"
     
     ' Show results.
    Debug.Print rstAuthors!au_fname &amp; " " &amp; rstAuthors!au_lname &amp; " " &amp; _
             rstAuthors!address &amp; " " &amp; rstAuthors!city &amp; " " &amp; rstAuthors!State
    rstAuthors!zip.Properties("Optimize") = False  'Delete the index.
    
    ' Clean up.
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
'EndOptimizeVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize Property — Dynamic (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example demonstrates the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object's dynamic <legacyBold>Optimize</legacyBold> property.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyBold><legacyItalic>zip</legacyItalic></legacyBold> field of the <legacyBold><legacyItalic>Authors</legacyItalic></legacyBold> table in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database is not indexed.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Setting the <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> property to <languageKeyword>True</languageKeyword> on the <legacyBold><legacyItalic>zip</legacyItalic></legacyBold> field authorizes ADO to build an index that improves the performance of the <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find</legacyLink> method.</caps:sentence>
        </para>
        <code>'BeginOptimizeVB
Public Sub Main()
    On Error GoTo ErrorHandler

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string.

    ' Declare the recordset and connection variables.
    Dim Cnxn As ADODB.Connection
    Dim rstAuthors As ADODB.Recordset
    Dim strCnxn As String
    Dim strSQLAuthors As String
    
     ' Open connection.
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Set Cnxn = New ADODB.Connection
    Cnxn.Open strCnxn
     
     ' open recordset client-side to enable index creation.
    Set rstAuthors = New ADODB.Recordset
    rstAuthors.CursorLocation = adUseClient
    strSQLAuthors = "SELECT * FROM Authors"
    rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText
     ' Create the index.
    rstAuthors!zip.Properties("Optimize") = True
     ' Find Akiko Yokomoto
    rstAuthors.Find "zip = '94595'"
     
     ' Show results.
    Debug.Print rstAuthors!au_fname &amp; " " &amp; rstAuthors!au_lname &amp; " " &amp; _
             rstAuthors!address &amp; " " &amp; rstAuthors!city &amp; " " &amp; rstAuthors!State
    rstAuthors!zip.Properties("Optimize") = False  'Delete the index.
    
    ' Clean up.
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
'EndOptimizeVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize Property — Dynamic (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
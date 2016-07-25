---
title: "OpenSchema Method Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 455a02f0-8143-4562-8648-8fb45ffd334c
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
# OpenSchema Method Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1bfe9c80a25f4ed480e73b46a7f39130" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method to display the name and type of each table in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database.</caps:sentence>
        </para>
        <code>'BeginOpenSchemaVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string

Public Sub Main()
    On Error GoTo ErrorHandler

    Dim Cnxn As ADODB.Connection
    Dim rstSchema As ADODB.Recordset
    Dim strCnxn As String
       
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
       
    Set rstSchema = Cnxn.OpenSchema(adSchemaTables)
    
    Do Until rstSchema.EOF
        Debug.Print "Table name: " &amp; _
            rstSchema!TABLE_NAME &amp; vbCr &amp; _
            "Table type: " &amp; rstSchema!TABLE_TYPE &amp; vbCr
        rstSchema.MoveNext
    Loop
   
    ' clean up
    rstSchema.Close
    Cnxn.Close
    Set rstSchema = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rstSchema Is Nothing Then
        If rstSchema.State = adStateOpen Then rstSchema.Close
    End If
    Set rstSchema = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndOpenSchemaVB</code>
        <para>
          <caps:sentence sentenceid="9501d653d5bf60349ec92f0402faa8e5" id="tgt2" class="tgtSentence">This example specifies a TABLE_TYPE query constraint in the <legacyBold>OpenSchema</legacyBold> method <legacyBold><legacyItalic>Criteria</legacyItalic></legacyBold> argument.</caps:sentence>
          <caps:sentence sentenceid="9843ec8b68a61c25875d46167f6fe24f" id="tgt3" class="tgtSentence"> As a result, only schema information for the Views specified in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database are returned.</caps:sentence>
          <caps:sentence sentenceid="1107f56f49e68dd0ce976cd32cca1057" id="tgt4" class="tgtSentence"> The example then displays the name(s) and type(s) of each table(s).</caps:sentence>
        </para>
        <code>Attribute VB_Name = "OpenSchema"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method to display the name and type of each table in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database.</caps:sentence>
        </para>
        <code>'BeginOpenSchemaVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string

Public Sub Main()
    On Error GoTo ErrorHandler

    Dim Cnxn As ADODB.Connection
    Dim rstSchema As ADODB.Recordset
    Dim strCnxn As String
       
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
       
    Set rstSchema = Cnxn.OpenSchema(adSchemaTables)
    
    Do Until rstSchema.EOF
        Debug.Print "Table name: " &amp; _
            rstSchema!TABLE_NAME &amp; vbCr &amp; _
            "Table type: " &amp; rstSchema!TABLE_TYPE &amp; vbCr
        rstSchema.MoveNext
    Loop
   
    ' clean up
    rstSchema.Close
    Cnxn.Close
    Set rstSchema = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rstSchema Is Nothing Then
        If rstSchema.State = adStateOpen Then rstSchema.Close
    End If
    Set rstSchema = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndOpenSchemaVB</code>
        <para>
          <caps:sentence id="src2" class="srcSentence">This example specifies a TABLE_TYPE query constraint in the <legacyBold>OpenSchema</legacyBold> method <legacyBold><legacyItalic>Criteria</legacyItalic></legacyBold> argument.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> As a result, only schema information for the Views specified in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database are returned.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The example then displays the name(s) and type(s) of each table(s).</caps:sentence>
        </para>
        <code>Attribute VB_Name = "OpenSchema"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
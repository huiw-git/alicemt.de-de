---
title: "Filter and RecordCount Properties Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e8bc63c7-8967-438a-9a49-512478a87a15
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
# Filter and RecordCount Properties Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="75cd86b37824f4b54facd40cea452e76" id="tgt1" class="tgtSentence">This example open a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> on the Publishers table in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database.</caps:sentence>
          <caps:sentence sentenceid="4413442e2179143450f9c53f8fd9060e" id="tgt2" class="tgtSentence"> It then uses the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property to limit the number of visible records to those publishers in a particular country/region.</caps:sentence>
          <caps:sentence sentenceid="5a9f6401cc590256f7e1eb6d6f2022c3" id="tgt3" class="tgtSentence"> The <legacyBold>RecordCount</legacyBold> property is used to show the difference between the filtered and unfiltered recordsets.</caps:sentence>
        </para>
        <code>'BeginFilterVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string

Public Sub Main()
    On Error GoTo ErrorHandler

    ' recordset variables
    Dim rstPublishers As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
    Dim SQLPublishers As String
    
     ' criteria variables
    Dim intPublisherCount As Integer
    Dim strCountry As String
    Dim strMessage As String
    
     ' open connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
    
    ' open recordset with data from Publishers table
    Set rstPublishers = New ADODB.Recordset
    SQLPublishers = "publishers"
    rstPublishers.Open SQLPublishers, strCnxn, adOpenStatic, , adCmdTable
    
    intPublisherCount = rstPublishers.RecordCount
    
    ' get user input
    strCountry = Trim(InputBox("Enter a country to filter on (e.g. USA):"))
    
    If strCountry &lt;&gt; "" Then
        ' open a filtered Recordset object
        rstPublishers.Filter = "Country ='" &amp; strCountry &amp; "'"
    
        If rstPublishers.RecordCount = 0 Then
            MsgBox "No publishers from that country."
        Else
           ' print number of records for the original recordset
           ' and the filtered recordset
            strMessage = "Orders in original recordset: " &amp; _
                vbCr &amp; intPublisherCount &amp; vbCr &amp; _
                "Orders in filtered recordset (Country = '" &amp; _
                strCountry &amp; "'): " &amp; vbCr &amp; _
                rstPublishers.RecordCount
            MsgBox strMessage
        End If
    End If
   
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
'EndFilterVB</code>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="8ede1ff293ba89b0a9317ebbf343e172" id="tgt4" class="tgtSentence">When you know the data you want to select, it's usually more efficient to open a <legacyBold>Recordset</legacyBold> with an SQL statement.</caps:sentence>
            <caps:sentence sentenceid="288de295b7214cb848854b35e5cc98be" id="tgt5" class="tgtSentence"> This example shows how you can create just one <legacyBold>Recordset</legacyBold> and obtain records from a particular country.</caps:sentence>
          </para>
        </alert>
        <code>Attribute VB_Name = "Filter"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link>
        <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example open a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> on the Publishers table in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It then uses the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property to limit the number of visible records to those publishers in a particular country/region.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The <legacyBold>RecordCount</legacyBold> property is used to show the difference between the filtered and unfiltered recordsets.</caps:sentence>
        </para>
        <code>'BeginFilterVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string

Public Sub Main()
    On Error GoTo ErrorHandler

    ' recordset variables
    Dim rstPublishers As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
    Dim SQLPublishers As String
    
     ' criteria variables
    Dim intPublisherCount As Integer
    Dim strCountry As String
    Dim strMessage As String
    
     ' open connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
    
    ' open recordset with data from Publishers table
    Set rstPublishers = New ADODB.Recordset
    SQLPublishers = "publishers"
    rstPublishers.Open SQLPublishers, strCnxn, adOpenStatic, , adCmdTable
    
    intPublisherCount = rstPublishers.RecordCount
    
    ' get user input
    strCountry = Trim(InputBox("Enter a country to filter on (e.g. USA):"))
    
    If strCountry &lt;&gt; "" Then
        ' open a filtered Recordset object
        rstPublishers.Filter = "Country ='" &amp; strCountry &amp; "'"
    
        If rstPublishers.RecordCount = 0 Then
            MsgBox "No publishers from that country."
        Else
           ' print number of records for the original recordset
           ' and the filtered recordset
            strMessage = "Orders in original recordset: " &amp; _
                vbCr &amp; intPublisherCount &amp; vbCr &amp; _
                "Orders in filtered recordset (Country = '" &amp; _
                strCountry &amp; "'): " &amp; vbCr &amp; _
                rstPublishers.RecordCount
            MsgBox strMessage
        End If
    End If
   
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
'EndFilterVB</code>
        <alert class="note">
          <para>
            <caps:sentence id="src4" class="srcSentence">When you know the data you want to select, it's usually more efficient to open a <legacyBold>Recordset</legacyBold> with an SQL statement.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This example shows how you can create just one <legacyBold>Recordset</legacyBold> and obtain records from a particular country.</caps:sentence>
          </para>
        </alert>
        <code>Attribute VB_Name = "Filter"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link>
        <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
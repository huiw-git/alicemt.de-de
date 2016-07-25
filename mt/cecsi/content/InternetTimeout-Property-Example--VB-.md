---
title: "InternetTimeout Property Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b35d2f4a-449c-4170-aab6-9ff88c890043
caps.latest.revision: 12
caps.handback.revision: 12
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
# InternetTimeout Property Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt1" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt2" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt3" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt4" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="ddbb4b831556b3526f6482a8e9ed7388" id="tgt5" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="4d1c8892-4bbc-4e71-bf4b-ba52c0ea9549">InternetTimeout</legacyLink> property, which exists on the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl</legacyLink> and <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace</legacyLink> objects.</caps:sentence>
          <caps:sentence sentenceid="0148fc27c35022d70d97e3771873fd7f" id="tgt6" class="tgtSentence"> This example uses the <legacyBold>DataControl</legacyBold> object and sets the timeout to 20 seconds.</caps:sentence>
        </para>
        <code>'BeginInternetTimeoutVB


Public Sub Main()
    On Error GoTo ErrorHandler

    Dim dc As RDS.DataControl
    Dim rst As ADODB.Recordset
    Set dc = New RDS.DataControl
    
    dc.Server = "http://MyServer"
    dc.ExecuteOptions = 1
    dc.FetchOptions = 1
    dc.Connect = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    dc.SQL = "SELECT * FROM Authors"
     ' Wait at least 20 seconds
    dc.InternetTimeout = 200
    
    dc.Refresh
     ' Use another Recordset as a convenience
    Set rst = dc.Recordset
    Do While Not rst.EOF
       Debug.Print rst!au_fname &amp; " " &amp; rst!au_lname
       rst.MoveNext
    Loop

    If rst.State = adStateOpen Then rst.Close
    Set rst = Nothing
    Set dc = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rst Is Nothing Then
        If rst.State = adStateOpen Then rst.Close
    End If
    Set rst = Nothing
    Set dc = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
    
End Sub
'EndInternetTimeoutVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
        <link xlink:href="4d1c8892-4bbc-4e71-bf4b-ba52c0ea9549">InternetTimeout Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src5" class="srcSentence">This example demonstrates the <legacyLink xlink:href="4d1c8892-4bbc-4e71-bf4b-ba52c0ea9549">InternetTimeout</legacyLink> property, which exists on the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl</legacyLink> and <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace</legacyLink> objects.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> This example uses the <legacyBold>DataControl</legacyBold> object and sets the timeout to 20 seconds.</caps:sentence>
        </para>
        <code>'BeginInternetTimeoutVB


Public Sub Main()
    On Error GoTo ErrorHandler

    Dim dc As RDS.DataControl
    Dim rst As ADODB.Recordset
    Set dc = New RDS.DataControl
    
    dc.Server = "http://MyServer"
    dc.ExecuteOptions = 1
    dc.FetchOptions = 1
    dc.Connect = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    dc.SQL = "SELECT * FROM Authors"
     ' Wait at least 20 seconds
    dc.InternetTimeout = 200
    
    dc.Refresh
     ' Use another Recordset as a convenience
    Set rst = dc.Recordset
    Do While Not rst.EOF
       Debug.Print rst!au_fname &amp; " " &amp; rst!au_lname
       rst.MoveNext
    Loop

    If rst.State = adStateOpen Then rst.Close
    Set rst = Nothing
    Set dc = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not rst Is Nothing Then
        If rst.State = adStateOpen Then rst.Close
    End If
    Set rst = Nothing
    Set dc = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
    
End Sub
'EndInternetTimeoutVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
        <link xlink:href="4d1c8892-4bbc-4e71-bf4b-ba52c0ea9549">InternetTimeout Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
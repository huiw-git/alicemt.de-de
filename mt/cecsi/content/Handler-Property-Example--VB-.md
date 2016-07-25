---
title: "Handler Property Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9664f9a6-65fc-4e7f-be3d-3e4b501b558a
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
# Handler Property Example (VB)
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
          <caps:sentence sentenceid="84155cea93af7819ca070810f8828cd5" id="tgt5" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS DataControl</legacyLink> object <legacyLink xlink:href="fdc34362-6d47-4727-b171-8d033159408e">Handler</legacyLink> property.</caps:sentence>
          <caps:sentence sentenceid="ef5e58ca6b30e10c81fef60de9635312" id="tgt6" class="tgtSentence"> (See <legacyLink xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</legacyLink> for more details.)</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4ee62f553bb9b1afa990499b9ab62e1f" id="tgt7" class="tgtSentence">Assume that the following sections in the parameter file, Msdfmap.ini, are located on the server:</caps:sentence>
        </para>
        <code>[connect AuthorDataBase]
Access=ReadWrite
Connect="DSN=Pubs"
[sql AuthorById]
SQL="SELECT * FROM Authors WHERE au_id = ?"</code>
        <para>
          <caps:sentence sentenceid="d2a93af734d290a1c07711c8710713d9" id="tgt8" class="tgtSentence">Your code looks like the following.</caps:sentence>
          <caps:sentence sentenceid="420bd895ee974b596d828f2e28f57963" id="tgt9" class="tgtSentence"> The command assigned to the <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> property will match the <legacyBold><legacyItalic>AuthorById</legacyItalic></legacyBold> identifier and will retrieve a row for author Michael O'Leary.</caps:sentence>
          <caps:sentence sentenceid="f46729c284c152d5b35972b3882608f4" id="tgt10" class="tgtSentence"> The <legacyBold>DataControl</legacyBold> object <legacyBold>Recordset</legacyBold> property is assigned to a disconnected <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object purely as a coding convenience.</caps:sentence>
        </para>
        <code>'BeginHandlerVB
Public Sub Main()
    On Error GoTo ErrorHandler
    
    Dim dc As New DataControl
    Dim rst As ADODB.Recordset
    
    dc.Handler = "MSDFMAP.Handler"
    dc.ExecuteOptions = 1
    dc.FetchOptions = 1
    dc.Server = "http://MyServer"
    dc.Connect = "Data Source=AuthorDataBase"
    dc.SQL = "AuthorById('267-41-2394')"
    dc.Refresh                  'Retrieve the record
    Set rst = dc.Recordset      'Use another Recordset as a convenience
    Debug.Print "Author is '" &amp; rst!au_fname &amp; " " &amp; rst!au_lname &amp; "'"

    ' clean up
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
'EndHandlerVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="fdc34362-6d47-4727-b171-8d033159408e">Handler Property (RDS)</link>
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
          <caps:sentence id="src5" class="srcSentence">This example demonstrates the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS DataControl</legacyLink> object <legacyLink xlink:href="fdc34362-6d47-4727-b171-8d033159408e">Handler</legacyLink> property.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> (See <legacyLink xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</legacyLink> for more details.)</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">Assume that the following sections in the parameter file, Msdfmap.ini, are located on the server:</caps:sentence>
        </para>
        <code>[connect AuthorDataBase]
Access=ReadWrite
Connect="DSN=Pubs"
[sql AuthorById]
SQL="SELECT * FROM Authors WHERE au_id = ?"</code>
        <para>
          <caps:sentence id="src8" class="srcSentence">Your code looks like the following.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> The command assigned to the <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> property will match the <legacyBold><legacyItalic>AuthorById</legacyItalic></legacyBold> identifier and will retrieve a row for author Michael O'Leary.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> The <legacyBold>DataControl</legacyBold> object <legacyBold>Recordset</legacyBold> property is assigned to a disconnected <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object purely as a coding convenience.</caps:sentence>
        </para>
        <code>'BeginHandlerVB
Public Sub Main()
    On Error GoTo ErrorHandler
    
    Dim dc As New DataControl
    Dim rst As ADODB.Recordset
    
    dc.Handler = "MSDFMAP.Handler"
    dc.ExecuteOptions = 1
    dc.FetchOptions = 1
    dc.Server = "http://MyServer"
    dc.Connect = "Data Source=AuthorDataBase"
    dc.SQL = "AuthorById('267-41-2394')"
    dc.Refresh                  'Retrieve the record
    Set rst = dc.Recordset      'Use another Recordset as a convenience
    Debug.Print "Author is '" &amp; rst!au_fname &amp; " " &amp; rst!au_lname &amp; "'"

    ' clean up
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
'EndHandlerVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="fdc34362-6d47-4727-b171-8d033159408e">Handler Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ConvertToString Method Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: edd0a01c-1a1b-4b91-9966-2529e244abae
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
# ConvertToString Method Example (VBScript)
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
          <caps:sentence sentenceid="f055f148ee45cfb67d279e9de40d841c" id="tgt5" class="tgtSentence">The following example shows how to convert a <legacyBold>Recordset</legacyBold> into a MIME-encoded string using the <legacyBold>RDSServer.DataFactory</legacyBold> <legacyBold>ConvertToString</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="19abb2c81eb9cdcec4f0e7028186bc69" id="tgt6" class="tgtSentence"> It then shows how the string can be converted back into a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="081b6240d891e397b51b85fe424d0ed6" id="tgt7" class="tgtSentence"> Cut and paste the following code to Notepad or another text editor and save it as <legacyBold>ConvertToString.htm</legacyBold>.</caps:sentence>
        </para>
        <code>&lt;!-- BeginConvertToStringVBS --&gt;
&lt;HTML&gt;
&lt;HEAD&gt;&lt;TITLE&gt;ConvertToString Example&lt;/TITLE&gt;&lt;HEAD&gt;
&lt;BODY&gt;

&lt;SCRIPT LANGUAGE=VBSCRIPT&gt;
Sub ConvertToStringX()
    Dim objRs, objDF, strServer, vString
    Const adcExecSync = 1
    Const adcFetchUpFront = 1

    ' Replace value below with your server name to use without ASP.
    strServer = "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;

    Set objDF = RDS1.CreateObject("RDSServer.DataFactory", strServer)
    Set objRs = objDF.Query(txtConnect.Value,txtQueryRecordset.Value)

    ' convert Recordset to MIME encoded string
    vString = objDF.ConvertToString(objRs)

    ' display MIME string for demo purposes
    txtRS.value = vString

    ' convert MIME string back to useable ADO Recordset 
    ' using RDS.DataControl
    RDC1.SQL = vString

    RDC1.ExecuteOptions = adcExecSync
    RDC1.FetchOptions = adcFetchUpFront
    RDC1.Refresh

    MsgBox "RecordCount = " &amp; RDC1.Recordset.RecordCount
End Sub 
&lt;/SCRIPT&gt;

Connect String: 
 &lt;INPUT TYPE=Text NAME=txtConnect SIZE=50 
    VALUE="Provider=sqloledb;Initial Catalog=pubs;Integrated Security='SSPI';"&gt; 
 &lt;BR&gt;

Query: 
 &lt;INPUT TYPE=Text NAME=txtQueryRecordset SIZE=50 
    VALUE="select * from authors"&gt; 
 &lt;BR&gt;

 &lt;INPUT TYPE=Button VALUE="ConvertToString" OnClick="ConvertToStringX()"&gt;
 &lt;BR&gt;

MIME Encoded RS: &lt;BR&gt;
 &lt;TEXTAREA NAME=txtRS ROWS=15 COLS=50 WRAP=virtual&gt;&lt;/TEXTAREA&gt;

&lt;!-- RDS.DataSpace  ID RDS1 --&gt;
 &lt;OBJECT ID="RDS1" WIDTH=1 HEIGHT=1
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"&gt;
 &lt;/OBJECT&gt;

&lt;!-- RDS.DataControl ID RDC1 --&gt;
 &lt;OBJECT ID="RDC1" WIDTH=1 HEIGHT=1 
     CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"&gt;
 &lt;/OBJECT&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndConvertToStringVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe">ConvertToString Method (RDS)</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
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
          <caps:sentence id="src5" class="srcSentence">The following example shows how to convert a <legacyBold>Recordset</legacyBold> into a MIME-encoded string using the <legacyBold>RDSServer.DataFactory</legacyBold> <legacyBold>ConvertToString</legacyBold> method.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> It then shows how the string can be converted back into a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Cut and paste the following code to Notepad or another text editor and save it as <legacyBold>ConvertToString.htm</legacyBold>.</caps:sentence>
        </para>
        <code>&lt;!-- BeginConvertToStringVBS --&gt;
&lt;HTML&gt;
&lt;HEAD&gt;&lt;TITLE&gt;ConvertToString Example&lt;/TITLE&gt;&lt;HEAD&gt;
&lt;BODY&gt;

&lt;SCRIPT LANGUAGE=VBSCRIPT&gt;
Sub ConvertToStringX()
    Dim objRs, objDF, strServer, vString
    Const adcExecSync = 1
    Const adcFetchUpFront = 1

    ' Replace value below with your server name to use without ASP.
    strServer = "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;

    Set objDF = RDS1.CreateObject("RDSServer.DataFactory", strServer)
    Set objRs = objDF.Query(txtConnect.Value,txtQueryRecordset.Value)

    ' convert Recordset to MIME encoded string
    vString = objDF.ConvertToString(objRs)

    ' display MIME string for demo purposes
    txtRS.value = vString

    ' convert MIME string back to useable ADO Recordset 
    ' using RDS.DataControl
    RDC1.SQL = vString

    RDC1.ExecuteOptions = adcExecSync
    RDC1.FetchOptions = adcFetchUpFront
    RDC1.Refresh

    MsgBox "RecordCount = " &amp; RDC1.Recordset.RecordCount
End Sub 
&lt;/SCRIPT&gt;

Connect String: 
 &lt;INPUT TYPE=Text NAME=txtConnect SIZE=50 
    VALUE="Provider=sqloledb;Initial Catalog=pubs;Integrated Security='SSPI';"&gt; 
 &lt;BR&gt;

Query: 
 &lt;INPUT TYPE=Text NAME=txtQueryRecordset SIZE=50 
    VALUE="select * from authors"&gt; 
 &lt;BR&gt;

 &lt;INPUT TYPE=Button VALUE="ConvertToString" OnClick="ConvertToStringX()"&gt;
 &lt;BR&gt;

MIME Encoded RS: &lt;BR&gt;
 &lt;TEXTAREA NAME=txtRS ROWS=15 COLS=50 WRAP=virtual&gt;&lt;/TEXTAREA&gt;

&lt;!-- RDS.DataSpace  ID RDS1 --&gt;
 &lt;OBJECT ID="RDS1" WIDTH=1 HEIGHT=1
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"&gt;
 &lt;/OBJECT&gt;

&lt;!-- RDS.DataControl ID RDC1 --&gt;
 &lt;OBJECT ID="RDC1" WIDTH=1 HEIGHT=1 
     CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"&gt;
 &lt;/OBJECT&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndConvertToStringVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe">ConvertToString Method (RDS)</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
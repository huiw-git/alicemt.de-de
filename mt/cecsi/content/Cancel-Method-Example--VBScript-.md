---
title: "Cancel Method Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4ade106d-063d-486e-bc4d-a1a6b6e0bea9
caps.latest.revision: 13
caps.handback.revision: 13
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
# Cancel Method Example (VBScript)
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
          <caps:sentence sentenceid="ce88479495d877074423ed5306abbd29" id="tgt5" class="tgtSentence">The following example shows how to read the <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel</legacyLink> method at run time.</caps:sentence>
          <caps:sentence sentenceid="0b72872943edc40f613ec4578458dcb2" id="tgt6" class="tgtSentence"> Cut and paste the following code to Notepad or another text editor and save it as CancelVBS.asp.</caps:sentence>
          <caps:sentence sentenceid="2ec2928247650e1340e8f032c91c1be4" id="tgt7" class="tgtSentence"> You can view the result in any client browser.</caps:sentence>
        </para>
        <code>&lt;!-- BeginCancelVBS --&gt;
&lt;Script Language="VBScript"&gt;
&lt;!--
Sub cmdCancelAsync_OnClick
   ' Terminates currently running AsyncExecute,
   ' ReadyState property set to adcReadyStateLoaded,
   ' Recordset set to Nothing
  ADC.Cancel
End Sub

Sub cmdRefreshTable_OnClick
   ADC.Refresh
End Sub
--&gt;
&lt;/Script&gt;

&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="ADC"&gt;
.
   &lt;PARAM NAME="SQL" VALUE="Select FirstName, LastName from Employees"&gt;
   &lt;PARAM NAME="CONNECT" VALUE="Provider='sqloledb';Integrated Security='SSPI';Initial Catalog='Northwind'"&gt;
   &lt;PARAM NAME="Server" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
.
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#ADC&gt;
&lt;TBODY&gt;
  &lt;TR&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;

&lt;FORM&gt;
&lt;INPUT type="button" value="Refresh" id=cmdRefreshTable name=cmdRefreshTable&gt;
&lt;INPUT type="button" value="Cancel" id=cmdCancelAsync name=cmdCancelAsync&gt;
&lt;/FORM&gt;
&lt;!-- EndCancelVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel Method</link>
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
          <caps:sentence id="src5" class="srcSentence">The following example shows how to read the <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel</legacyLink> method at run time.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Cut and paste the following code to Notepad or another text editor and save it as CancelVBS.asp.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> You can view the result in any client browser.</caps:sentence>
        </para>
        <code>&lt;!-- BeginCancelVBS --&gt;
&lt;Script Language="VBScript"&gt;
&lt;!--
Sub cmdCancelAsync_OnClick
   ' Terminates currently running AsyncExecute,
   ' ReadyState property set to adcReadyStateLoaded,
   ' Recordset set to Nothing
  ADC.Cancel
End Sub

Sub cmdRefreshTable_OnClick
   ADC.Refresh
End Sub
--&gt;
&lt;/Script&gt;

&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="ADC"&gt;
.
   &lt;PARAM NAME="SQL" VALUE="Select FirstName, LastName from Employees"&gt;
   &lt;PARAM NAME="CONNECT" VALUE="Provider='sqloledb';Integrated Security='SSPI';Initial Catalog='Northwind'"&gt;
   &lt;PARAM NAME="Server" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
.
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#ADC&gt;
&lt;TBODY&gt;
  &lt;TR&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;

&lt;FORM&gt;
&lt;INPUT type="button" value="Refresh" id=cmdRefreshTable name=cmdRefreshTable&gt;
&lt;INPUT type="button" value="Cancel" id=cmdCancelAsync name=cmdCancelAsync&gt;
&lt;/FORM&gt;
&lt;!-- EndCancelVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
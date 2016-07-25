---
title: "ReadyState Property Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e3e18da4-0511-4ece-a35d-699978bc28c6
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
# ReadyState Property Example (VBScript)
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
          <caps:sentence sentenceid="b67af18a8f334dc9ebb0d0fc8a581444" id="tgt5" class="tgtSentence">The following example shows how to read the <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState</legacyLink> property of the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object at run time in VBScript code.</caps:sentence>
          <caps:sentence sentenceid="f2e2a5bcb1d7a67f86edb1a00d2ce0ac" id="tgt6" class="tgtSentence">
            <legacyBold>ReadyState</legacyBold> is a read-only property.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5727c3a8423b0f81c2f61aab478812f0" id="tgt7" class="tgtSentence">To test this example, cut and paste this code between the &lt;Body&gt; and &lt;/Body&gt; tags in a normal HTML document and name it <legacyBold>RDSReadySt.asp</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="8d4a266da99215a41601c920149d3e4f" id="tgt8" class="tgtSentence"> Use <legacyBold>Find</legacyBold> to locate the file Adovbs.inc and place it in the directory you plan to use.</caps:sentence>
          <caps:sentence sentenceid="266295192f1fe18632e24dd9222d8bdc" id="tgt9" class="tgtSentence"> ASP script will identify your server.</caps:sentence>
        </para>
        <code>&lt;!-- BeginReadyStateVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;!--#include file="adovbs.inc"--&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;RDS.DataControl ReadyState Property&lt;/title&gt;
&lt;style&gt;
&lt;!--
body {
   font-family: 'Verdana','Arial','Helvetica',sans-serif;
   BACKGROUND-COLOR:white;
   COLOR:black;
    }
.thead {
   background-color: #008080; 
   font-family: 'Verdana','Arial','Helvetica',sans-serif; 
   font-size: x-small;
   color: white;
   }
.thead2 {
   background-color: #800000; 
   font-family: 'Verdana','Arial','Helvetica',sans-serif; 
   font-size: x-small;
   color: white;
   }
.tbody { 
   text-align: center;
   background-color: #f7efde;
   font-family: 'Verdana','Arial','Helvetica',sans-serif; 
   font-size: x-small;
    }
--&gt;
&lt;/style&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;H1&gt;RDS.DataControl ReadyState Property&lt;/H1&gt;
&lt;H2&gt;RDS API Code Examples &lt;/H2&gt;
&lt;HR&gt;
&lt;!-- RDS.DataControl with parameters set at design time --&gt;
&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID=RDS&gt;
   &lt;PARAM NAME="SQL" VALUE="Select * from Orders"&gt;
   &lt;PARAM NAME="SERVER" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
   &lt;PARAM NAME="CONNECT" VALUE="Provider=SQLOLEDB;Integrated Security=SSPI;Initial Catalog=Northwind"&gt;
   &lt;PARAM NAME="ExecuteOptions" VALUE="2"&gt; 
   &lt;PARAM NAME="FetchOptions" VALUE="3"&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;TBODY&gt;
  &lt;TR&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="OrderID"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;

&lt;Script Language="VBScript"&gt;

   Sub Window_OnLoad

      Select Case RDS.ReadyState
         case 2   'adcReadyStateLoaded
          MsgBox "Executing Query"
         case 3   'adcReadyStateInteractive
          MsgBox "Fetching records in background"
         case 4   'adcReadyStateComplete
          MsgBox "All records fetched"
      End Select

   End Sub
&lt;/Script&gt;

&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndReadyStateVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState Property (RDS)</link>
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
          <caps:sentence id="src5" class="srcSentence">The following example shows how to read the <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState</legacyLink> property of the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object at run time in VBScript code.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence">
            <legacyBold>ReadyState</legacyBold> is a read-only property.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">To test this example, cut and paste this code between the &lt;Body&gt; and &lt;/Body&gt; tags in a normal HTML document and name it <legacyBold>RDSReadySt.asp</legacyBold>.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Use <legacyBold>Find</legacyBold> to locate the file Adovbs.inc and place it in the directory you plan to use.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> ASP script will identify your server.</caps:sentence>
        </para>
        <code>&lt;!-- BeginReadyStateVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;!--#include file="adovbs.inc"--&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;RDS.DataControl ReadyState Property&lt;/title&gt;
&lt;style&gt;
&lt;!--
body {
   font-family: 'Verdana','Arial','Helvetica',sans-serif;
   BACKGROUND-COLOR:white;
   COLOR:black;
    }
.thead {
   background-color: #008080; 
   font-family: 'Verdana','Arial','Helvetica',sans-serif; 
   font-size: x-small;
   color: white;
   }
.thead2 {
   background-color: #800000; 
   font-family: 'Verdana','Arial','Helvetica',sans-serif; 
   font-size: x-small;
   color: white;
   }
.tbody { 
   text-align: center;
   background-color: #f7efde;
   font-family: 'Verdana','Arial','Helvetica',sans-serif; 
   font-size: x-small;
    }
--&gt;
&lt;/style&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;H1&gt;RDS.DataControl ReadyState Property&lt;/H1&gt;
&lt;H2&gt;RDS API Code Examples &lt;/H2&gt;
&lt;HR&gt;
&lt;!-- RDS.DataControl with parameters set at design time --&gt;
&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID=RDS&gt;
   &lt;PARAM NAME="SQL" VALUE="Select * from Orders"&gt;
   &lt;PARAM NAME="SERVER" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
   &lt;PARAM NAME="CONNECT" VALUE="Provider=SQLOLEDB;Integrated Security=SSPI;Initial Catalog=Northwind"&gt;
   &lt;PARAM NAME="ExecuteOptions" VALUE="2"&gt; 
   &lt;PARAM NAME="FetchOptions" VALUE="3"&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;TBODY&gt;
  &lt;TR&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="OrderID"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;

&lt;Script Language="VBScript"&gt;

   Sub Window_OnLoad

      Select Case RDS.ReadyState
         case 2   'adcReadyStateLoaded
          MsgBox "Executing Query"
         case 3   'adcReadyStateInteractive
          MsgBox "Fetching records in background"
         case 4   'adcReadyStateComplete
          MsgBox "All records fetched"
      End Select

   End Sub
&lt;/Script&gt;

&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndReadyStateVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
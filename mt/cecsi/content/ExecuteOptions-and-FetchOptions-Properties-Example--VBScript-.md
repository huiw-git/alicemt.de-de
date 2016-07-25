---
title: "ExecuteOptions and FetchOptions Properties Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 753a4a3d-0fba-40b8-86e7-50b34182ca69
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
# ExecuteOptions and FetchOptions Properties Example (VBScript)
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
          <caps:sentence sentenceid="b19d3a0e6d6472096d559fc6bef65a17" id="tgt5" class="tgtSentence">The following code shows how to set the <legacyLink xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions</legacyLink> and <legacyLink xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions</legacyLink> properties at design time.</caps:sentence>
          <caps:sentence sentenceid="af45f4e5360ce429a951f78ea5abcf17" id="tgt6" class="tgtSentence"> If left unset, <legacyBold>ExecuteOptions</legacyBold> defaults to <legacyBold>adcExecSync</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="4554059d7a5cd72c518a911abd71f928" id="tgt7" class="tgtSentence"> This setting indicates that when the <legacyBold>RDS.Refresh</legacyBold> method is called, it will be executed on the current calling thread—that is, synchronously.</caps:sentence>
          <caps:sentence sentenceid="15b5a292c249801e2057609a02a604d7" id="tgt8" class="tgtSentence"> Cut and paste the following code to Notepad or another text editor and save it as <legacyBold>ExecuteOptionsDesignVBS.asp</legacyBold>.</caps:sentence>
        </para>
        <code>&lt;!-- BeginExecuteOptionsDesignVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;Design-time ExecuteOptions and FetchOptions Properties Example&lt;/title&gt;
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
&lt;h2&gt;Design-time &lt;br&gt; ExecuteOptions and FetchOptions Properties Example&lt;/h2&gt;

&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID=RDS height=1 width=1&gt;
&lt;PARAM NAME="SQL" VALUE="SELECT FirstName, LastName FROM Employees ORDER BY LastName"&gt;
&lt;PARAM NAME="Connect" VALUE="Provider='sqloledb';Data Source=&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;;Integrated Security='SSPI';Initial Catalog='Northwind'"&gt;
&lt;PARAM NAME="Server" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
&lt;PARAM NAME="ExecuteOptions" VALUE="1"&gt;
&lt;PARAM NAME="FetchOptions" VALUE="3"&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;TBODY&gt;
   &lt;TR class="thead2"&gt;
      &lt;TH&gt;First Name&lt;/TH&gt;
      &lt;TH&gt;Last Name&lt;/TH&gt;
   &lt;/TR&gt;
   &lt;TR class="tbody"&gt;
     &lt;TD&gt;&lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
     &lt;TD&gt;&lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;

&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndExecuteOptionsDesignVBS --&gt;</code>
        <para>
          <caps:sentence sentenceid="8bcdfcf213e26572eac63293f9d336f5" id="tgt9" class="tgtSentence">The following example shows how to set the <legacyBold>ExecuteOptions</legacyBold> and <legacyBold>FetchOptions</legacyBold> properties at run time in VBScript code.</caps:sentence>
          <caps:sentence sentenceid="0d7a16568ea98b87b6754c0ce055896c" id="tgt10" class="tgtSentence"> See the <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh</legacyLink> method for a working example of these properties.</caps:sentence>
          <caps:sentence sentenceid="e183e59ea1d46afeee790feef9236b5b" id="tgt11" class="tgtSentence"> Cut and paste the following code to Notepad or another text editor and save it as <legacyBold>ExecuteOptionsRuntimeVBS.asp</legacyBold>.</caps:sentence>
        </para>
        <code>&lt;!-- BeginExecuteOptionsRuntimeVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;Run-time ExecuteOptions and FetchOptions Properties Example&lt;/title&gt;
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
&lt;h2&gt;Run-time &lt;br&gt; ExecuteOptions and FetchOptions Properties Example&lt;/h2&gt;
&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID=RDS height=1 width=1&gt;
&lt;PARAM NAME="SQL" VALUE="SELECT FirstName, LastName FROM Employees ORDER BY LastName"&gt;
&lt;PARAM NAME="Connect" VALUE="Provider='sqloledb';Data Source=&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;;Integrated Security='SSPI';Initial Catalog='Northwind'"&gt;
&lt;PARAM NAME="Server" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;TBODY&gt;
   &lt;TR class="thead2"&gt;
      &lt;TH&gt;First Name&lt;/TH&gt;
      &lt;TH&gt;Last Name&lt;/TH&gt;
   &lt;/TR&gt;
   &lt;TR class="tbody"&gt;
     &lt;TD&gt;&lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
     &lt;TD&gt;&lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;
&lt;Script Language="VBScript"&gt;
Const adcExecSync = 1
Const adcFetchAsynch = 3

Sub ExecuteHow
  ' set RDS properties at run-time
  RDS1.ExecuteOptions = adcExecSync
  RDS1.FetchOptions = adcFetchAsynch
  RDS.Refresh
End Sub
&lt;/Script&gt;
&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndExecuteOptionsRuntimeVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions Property (RDS)</link>
        <link xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions Property (RDS)</link>
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
          <caps:sentence id="src5" class="srcSentence">The following code shows how to set the <legacyLink xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions</legacyLink> and <legacyLink xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions</legacyLink> properties at design time.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> If left unset, <legacyBold>ExecuteOptions</legacyBold> defaults to <legacyBold>adcExecSync</legacyBold>.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> This setting indicates that when the <legacyBold>RDS.Refresh</legacyBold> method is called, it will be executed on the current calling thread—that is, synchronously.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Cut and paste the following code to Notepad or another text editor and save it as <legacyBold>ExecuteOptionsDesignVBS.asp</legacyBold>.</caps:sentence>
        </para>
        <code>&lt;!-- BeginExecuteOptionsDesignVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;Design-time ExecuteOptions and FetchOptions Properties Example&lt;/title&gt;
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
&lt;h2&gt;Design-time &lt;br&gt; ExecuteOptions and FetchOptions Properties Example&lt;/h2&gt;

&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID=RDS height=1 width=1&gt;
&lt;PARAM NAME="SQL" VALUE="SELECT FirstName, LastName FROM Employees ORDER BY LastName"&gt;
&lt;PARAM NAME="Connect" VALUE="Provider='sqloledb';Data Source=&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;;Integrated Security='SSPI';Initial Catalog='Northwind'"&gt;
&lt;PARAM NAME="Server" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
&lt;PARAM NAME="ExecuteOptions" VALUE="1"&gt;
&lt;PARAM NAME="FetchOptions" VALUE="3"&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;TBODY&gt;
   &lt;TR class="thead2"&gt;
      &lt;TH&gt;First Name&lt;/TH&gt;
      &lt;TH&gt;Last Name&lt;/TH&gt;
   &lt;/TR&gt;
   &lt;TR class="tbody"&gt;
     &lt;TD&gt;&lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
     &lt;TD&gt;&lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;

&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndExecuteOptionsDesignVBS --&gt;</code>
        <para>
          <caps:sentence id="src9" class="srcSentence">The following example shows how to set the <legacyBold>ExecuteOptions</legacyBold> and <legacyBold>FetchOptions</legacyBold> properties at run time in VBScript code.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> See the <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh</legacyLink> method for a working example of these properties.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> Cut and paste the following code to Notepad or another text editor and save it as <legacyBold>ExecuteOptionsRuntimeVBS.asp</legacyBold>.</caps:sentence>
        </para>
        <code>&lt;!-- BeginExecuteOptionsRuntimeVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;Run-time ExecuteOptions and FetchOptions Properties Example&lt;/title&gt;
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
&lt;h2&gt;Run-time &lt;br&gt; ExecuteOptions and FetchOptions Properties Example&lt;/h2&gt;
&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID=RDS height=1 width=1&gt;
&lt;PARAM NAME="SQL" VALUE="SELECT FirstName, LastName FROM Employees ORDER BY LastName"&gt;
&lt;PARAM NAME="Connect" VALUE="Provider='sqloledb';Data Source=&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;;Integrated Security='SSPI';Initial Catalog='Northwind'"&gt;
&lt;PARAM NAME="Server" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;TBODY&gt;
   &lt;TR class="thead2"&gt;
      &lt;TH&gt;First Name&lt;/TH&gt;
      &lt;TH&gt;Last Name&lt;/TH&gt;
   &lt;/TR&gt;
   &lt;TR class="tbody"&gt;
     &lt;TD&gt;&lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
     &lt;TD&gt;&lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;
&lt;Script Language="VBScript"&gt;
Const adcExecSync = 1
Const adcFetchAsynch = 3

Sub ExecuteHow
  ' set RDS properties at run-time
  RDS1.ExecuteOptions = adcExecSync
  RDS1.FetchOptions = adcFetchAsynch
  RDS.Refresh
End Sub
&lt;/Script&gt;
&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndExecuteOptionsRuntimeVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions Property (RDS)</link>
        <link xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "SQL Property Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 32c33bcf-3320-4836-9e2e-99c8978ce581
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
# SQL Property Example (VBScript)
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
          <caps:sentence sentenceid="4648ca9db545ef8519ecc928b612a5a1" id="tgt5" class="tgtSentence">The following code shows how to set the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> SQL parameter at design time and bind it to a data-aware control using the database called <legacyItalic>Pubs</legacyItalic>, which ships with Microsoft SQL Server.</caps:sentence>
          <caps:sentence sentenceid="5e9283eb94a32a5cd99a981eac818f7d" id="tgt6" class="tgtSentence"> To test the example, copy the following code into a normal ASP document named <legacyBold>SQLDesignVBS.asp</legacyBold> on your Web server.</caps:sentence>
        </para>
        <code>&lt;!-- BeginSQLDesignVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;SQL Property Example (VBScript)&lt;/title&gt;
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
&lt;h1&gt;SQL Property Example (VBScript)&lt;/h1&gt;

&lt;!-- RDS.DataControl --&gt;
&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID=RDC HEIGHT=1 WIDTH=1&gt;
   &lt;PARAM NAME="SQL" VALUE="Select FirstName, LastName from Employees"&gt;
   &lt;PARAM NAME="SERVER" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
   &lt;PARAM NAME="CONNECT" VALUE="Provider='sqloledb';Initial Catalog='Northwind';Integrated Security='SSPI';"&gt;
&lt;/OBJECT&gt;

&lt;!-- Data Table --&gt;

&lt;TABLE DATASRC=#RDC BORDER=1&gt;
   &lt;TR&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TABLE&gt;

&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndSQLDesignVBS --&gt;</code>
        <para>
          <caps:sentence sentenceid="8c7991f2c9949777b3d58bc396471682" id="tgt7" class="tgtSentence">The following example shows how to set the necessary parameters of <legacyBold>RDS.DataControl</legacyBold> at run time.</caps:sentence>
          <caps:sentence sentenceid="f82aad88b0c693f3f4c37c2d66c61501" id="tgt8" class="tgtSentence"> To test this example, cut and paste the following code into a normal ASP document and name it <legacyBold>SQLRuntimeVBS.asp</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="266295192f1fe18632e24dd9222d8bdc" id="tgt9" class="tgtSentence"> ASP script will identify your server.</caps:sentence>
        </para>
        <code>&lt;!-- BeginSQLRuntimeVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;SQL Property Example (VBScript)&lt;/title&gt;
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
&lt;h1&gt;SQL Property Example (VBScript)&lt;/h1&gt;

&lt;H2&gt;RDS API Code Examples &lt;/H2&gt;
&lt;H3&gt;Remote Data Service SQL Property Set at Run Time&lt;/H3&gt;

&lt;!-- RDS.DataControl with no parameters set at design time --&gt;
&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"
   ID=RDC HEIGHT=1 WIDTH=1&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDC&gt;
   &lt;TR&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="Title"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="Type"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="Email"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TABLE&gt;

&lt;HR&gt;
&lt;Input Size=70 Name="txtServer" Value= "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
&lt;BR&gt;
&lt;Input Size=70 Name="txtConnect" Value="Provider='sqloledb';Integrated Security='SSPI';Initial Catalog='Northwind';"&gt;
&lt;BR&gt;
&lt;Input Size=70 Name="txtSQL" VALUE="Select * from Employees"&gt;
&lt;HR&gt;
&lt;INPUT TYPE=BUTTON NAME="Run" VALUE="Run"&gt;&lt;BR&gt;

&lt;Script Language="VBScript"&gt;
&lt;!--
' Set parameters of RDS.DataControl at Run Time.
Sub Run_OnClick
   RDC.Server = txtServer.Value
   RDC.SQL = txtSQL.Value
   RDC.Connect = txtConnect.Value
   RDC.Refresh
End Sub
--&gt;
&lt;/Script&gt;
   
&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndSQLRuntimeVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL Property (RDS)</link>
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
          <caps:sentence id="src5" class="srcSentence">The following code shows how to set the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> SQL parameter at design time and bind it to a data-aware control using the database called <legacyItalic>Pubs</legacyItalic>, which ships with Microsoft SQL Server.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> To test the example, copy the following code into a normal ASP document named <legacyBold>SQLDesignVBS.asp</legacyBold> on your Web server.</caps:sentence>
        </para>
        <code>&lt;!-- BeginSQLDesignVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;SQL Property Example (VBScript)&lt;/title&gt;
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
&lt;h1&gt;SQL Property Example (VBScript)&lt;/h1&gt;

&lt;!-- RDS.DataControl --&gt;
&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID=RDC HEIGHT=1 WIDTH=1&gt;
   &lt;PARAM NAME="SQL" VALUE="Select FirstName, LastName from Employees"&gt;
   &lt;PARAM NAME="SERVER" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
   &lt;PARAM NAME="CONNECT" VALUE="Provider='sqloledb';Initial Catalog='Northwind';Integrated Security='SSPI';"&gt;
&lt;/OBJECT&gt;

&lt;!-- Data Table --&gt;

&lt;TABLE DATASRC=#RDC BORDER=1&gt;
   &lt;TR&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TABLE&gt;

&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndSQLDesignVBS --&gt;</code>
        <para>
          <caps:sentence id="src7" class="srcSentence">The following example shows how to set the necessary parameters of <legacyBold>RDS.DataControl</legacyBold> at run time.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> To test this example, cut and paste the following code into a normal ASP document and name it <legacyBold>SQLRuntimeVBS.asp</legacyBold>.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> ASP script will identify your server.</caps:sentence>
        </para>
        <code>&lt;!-- BeginSQLRuntimeVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;SQL Property Example (VBScript)&lt;/title&gt;
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
&lt;h1&gt;SQL Property Example (VBScript)&lt;/h1&gt;

&lt;H2&gt;RDS API Code Examples &lt;/H2&gt;
&lt;H3&gt;Remote Data Service SQL Property Set at Run Time&lt;/H3&gt;

&lt;!-- RDS.DataControl with no parameters set at design time --&gt;
&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"
   ID=RDC HEIGHT=1 WIDTH=1&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDC&gt;
   &lt;TR&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="Title"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="Type"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
      &lt;TD&gt; &lt;SPAN DATAFLD="Email"&gt;&lt;/SPAN&gt; &lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TABLE&gt;

&lt;HR&gt;
&lt;Input Size=70 Name="txtServer" Value= "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
&lt;BR&gt;
&lt;Input Size=70 Name="txtConnect" Value="Provider='sqloledb';Integrated Security='SSPI';Initial Catalog='Northwind';"&gt;
&lt;BR&gt;
&lt;Input Size=70 Name="txtSQL" VALUE="Select * from Employees"&gt;
&lt;HR&gt;
&lt;INPUT TYPE=BUTTON NAME="Run" VALUE="Run"&gt;&lt;BR&gt;

&lt;Script Language="VBScript"&gt;
&lt;!--
' Set parameters of RDS.DataControl at Run Time.
Sub Run_OnClick
   RDC.Server = txtServer.Value
   RDC.SQL = txtSQL.Value
   RDC.Connect = txtConnect.Value
   RDC.Refresh
End Sub
--&gt;
&lt;/Script&gt;
   
&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndSQLRuntimeVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
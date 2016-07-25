---
title: "DataSpace Object and CreateObject Method Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 12b0e160-5e5c-441f-bed7-ac0bd061e003
caps.latest.revision: 14
caps.handback.revision: 14
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
# DataSpace Object and CreateObject Method Example (VBScript)
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
          <caps:sentence sentenceid="0282c766fa0b44c094801462c19c87dd" id="tgt5" class="tgtSentence">The following example shows how to use the <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method of the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> with the default business object, <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="11989d5b138795960d3cf051a913fb48" id="tgt6" class="tgtSentence"> To test this example, cut and paste this code between the &lt;Body&gt; and &lt;/Body&gt; tags in a normal HTML document and name it <legacyBold>DataSpaceVBS.asp</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="266295192f1fe18632e24dd9222d8bdc" id="tgt7" class="tgtSentence"> ASP script will identify your server.</caps:sentence>
        </para>
        <code>&lt;!-- BeginDataSpaceVBS --&gt;
&lt;html&gt;
&lt;head&gt;
&lt;!--use the following META tag instead of adovbs.inc--&gt;
&lt;!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;DataSpace Object and CreateObject Method Example (VBScript)&lt;/title&gt;
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
&lt;h1&gt;DataSpace Object and CreateObject Method Example (VBScript)&lt;/h1&gt;

&lt;H2&gt;RDS API Code Examples&lt;/H2&gt;
&lt;HR&gt;
&lt;H3&gt;Using Query Method of RDSServer.DataFactory&lt;/H3&gt;

&lt;!-- RDS.DataSpace  ID rdsDS--&gt;
&lt;OBJECT ID="rdsDS" WIDTH=1 HEIGHT=1
CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"&gt;
&lt;/OBJECT&gt;

&lt;!-- RDS.DataControl with parameters set at run time --&gt;
&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"
   ID=RDS WIDTH=1 HEIGHT=1&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;TBODY&gt;
  &lt;TR&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;

&lt;HR&gt;
&lt;INPUT TYPE=BUTTON NAME="Run" VALUE="Run"&gt;

&lt;H4&gt;Click Run -
The &lt;i&gt;CreateObject&lt;/i&gt; Method of the RDS.DataSpace Object Creates an instance of the RDSServer.DataFactory.
The &lt;i&gt;Query&lt;/i&gt; Method of the RDSServer.DataFactory is used to bring back a Recordset.&lt;/H4&gt;

&lt;Script Language="VBScript"&gt;

    Dim rdsDF
    Dim strServer
    Dim strCnxn
    Dim strSQL

    strServer = "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"
    strCnxn = "Provider='sqloledb';Data Source=" &amp; _
            "&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;" &amp; ";" &amp; _
            "Integrated Security='SSPI';Initial Catalog='Northwind';"
    strSQL = "Select FirstName, LastName from Employees"

    Sub Run_OnClick()
              
       Dim rs      
        ' Create Data Factory
       Set rdsDF = rdsDS.CreateObject("RDSServer.DataFactory", strServer)
        'Get Recordset  
       Set rs = rdsDF.Query(strCnxn, strSQL)   
       ' Use  RDS.DataControl to bind Recordset to data-aware Table above
       RDS.SourceRecordset = rs

    End Sub
&lt;/Script&gt;

&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndDataSpaceVBS --&gt;</code>
        <para>
          <caps:sentence sentenceid="992869098ae31887d4bd528306ccaa93" id="tgt8" class="tgtSentence">The following example shows how to use the <legacyBold>CreateObject</legacyBold> method to create an instance of a custom business object, VbBusObj.VbBusObjCls.</caps:sentence>
          <caps:sentence sentenceid="3ac5858230d78ecad321b992bfd63c94" id="tgt9" class="tgtSentence"> It also uses the Active Server Pages scripting to identify the Web server name.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b3e67d8e1da3cd821073c62a8f864dd8" id="tgt10" class="tgtSentence">To see the complete example, open the sample applications selector.</caps:sentence>
          <caps:sentence sentenceid="59659e47dd7940b169a44da2b83f1bc5" id="tgt11" class="tgtSentence"> In the <legacyBold>Client Tier</legacyBold> column, select <legacyBold>VBScript in Internet Explorer</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="d87fd43d68c991e1c5887a3dec835464" id="tgt12" class="tgtSentence"> In the <legacyBold>Middle Tier</legacyBold> column, select <legacyBold>Custom Visual Basic Business Object</legacyBold>.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="a955ec3a31d8205c3ae07b07b7fefc6d" id="tgt13" class="tgtSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <system>Trusted_Connection=yes</system> or <system>Integrated Security = SSPI</system> instead of user ID and password information in the connection string.</caps:sentence>
          </para>
        </alert>
        <code>Sub Window_OnLoad()
   strServer = "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"
   Set BO = ADS1.CreateObject("VbBusObj.VbBusObjCls", strServer)
   txtConnect.Value = "dsn=Pubs;uid=MyUserID;pwd=MyPassword;"
   txtGetRecordset.Value = "Select * From authors for Browse"
End Sub</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject Method (RDS)</link>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
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
          <caps:sentence id="src5" class="srcSentence">The following example shows how to use the <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method of the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> with the default business object, <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> To test this example, cut and paste this code between the &lt;Body&gt; and &lt;/Body&gt; tags in a normal HTML document and name it <legacyBold>DataSpaceVBS.asp</legacyBold>.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> ASP script will identify your server.</caps:sentence>
        </para>
        <code>&lt;!-- BeginDataSpaceVBS --&gt;
&lt;html&gt;
&lt;head&gt;
&lt;!--use the following META tag instead of adovbs.inc--&gt;
&lt;!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --&gt;
    &lt;meta name="VI60_DefaultClientScript"  content=VBScript&gt;
    &lt;meta name="GENERATOR" content="Microsoft Visual Studio 6.0"&gt;
    &lt;title&gt;DataSpace Object and CreateObject Method Example (VBScript)&lt;/title&gt;
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
&lt;h1&gt;DataSpace Object and CreateObject Method Example (VBScript)&lt;/h1&gt;

&lt;H2&gt;RDS API Code Examples&lt;/H2&gt;
&lt;HR&gt;
&lt;H3&gt;Using Query Method of RDSServer.DataFactory&lt;/H3&gt;

&lt;!-- RDS.DataSpace  ID rdsDS--&gt;
&lt;OBJECT ID="rdsDS" WIDTH=1 HEIGHT=1
CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"&gt;
&lt;/OBJECT&gt;

&lt;!-- RDS.DataControl with parameters set at run time --&gt;
&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"
   ID=RDS WIDTH=1 HEIGHT=1&gt;
&lt;/OBJECT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;TBODY&gt;
  &lt;TR&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="FirstName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
    &lt;TD&gt;&lt;SPAN DATAFLD="LastName"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;

&lt;HR&gt;
&lt;INPUT TYPE=BUTTON NAME="Run" VALUE="Run"&gt;

&lt;H4&gt;Click Run -
The &lt;i&gt;CreateObject&lt;/i&gt; Method of the RDS.DataSpace Object Creates an instance of the RDSServer.DataFactory.
The &lt;i&gt;Query&lt;/i&gt; Method of the RDSServer.DataFactory is used to bring back a Recordset.&lt;/H4&gt;

&lt;Script Language="VBScript"&gt;

    Dim rdsDF
    Dim strServer
    Dim strCnxn
    Dim strSQL

    strServer = "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"
    strCnxn = "Provider='sqloledb';Data Source=" &amp; _
            "&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;" &amp; ";" &amp; _
            "Integrated Security='SSPI';Initial Catalog='Northwind';"
    strSQL = "Select FirstName, LastName from Employees"

    Sub Run_OnClick()
              
       Dim rs      
        ' Create Data Factory
       Set rdsDF = rdsDS.CreateObject("RDSServer.DataFactory", strServer)
        'Get Recordset  
       Set rs = rdsDF.Query(strCnxn, strSQL)   
       ' Use  RDS.DataControl to bind Recordset to data-aware Table above
       RDS.SourceRecordset = rs

    End Sub
&lt;/Script&gt;

&lt;/body&gt;
&lt;/html&gt;
&lt;!-- EndDataSpaceVBS --&gt;</code>
        <para>
          <caps:sentence id="src8" class="srcSentence">The following example shows how to use the <legacyBold>CreateObject</legacyBold> method to create an instance of a custom business object, VbBusObj.VbBusObjCls.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> It also uses the Active Server Pages scripting to identify the Web server name.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">To see the complete example, open the sample applications selector.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> In the <legacyBold>Client Tier</legacyBold> column, select <legacyBold>VBScript in Internet Explorer</legacyBold>.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> In the <legacyBold>Middle Tier</legacyBold> column, select <legacyBold>Custom Visual Basic Business Object</legacyBold>.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src13" class="srcSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <system>Trusted_Connection=yes</system> or <system>Integrated Security = SSPI</system> instead of user ID and password information in the connection string.</caps:sentence>
          </para>
        </alert>
        <code>Sub Window_OnLoad()
   strServer = "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"
   Set BO = ADS1.CreateObject("VbBusObj.VbBusObjCls", strServer)
   txtConnect.Value = "dsn=Pubs;uid=MyUserID;pwd=MyPassword;"
   txtGetRecordset.Value = "Select * From authors for Browse"
End Sub</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject Method (RDS)</link>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
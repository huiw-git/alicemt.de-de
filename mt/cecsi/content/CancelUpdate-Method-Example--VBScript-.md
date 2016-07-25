---
title: "CancelUpdate Method Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c23912f0-1288-4727-8fb4-f643b8811cf7
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
# CancelUpdate Method Example (VBScript)
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
          <caps:sentence sentenceid="e2e43b0bc9d0e8c0c8071e9b18dfdaf4" id="tgt5" class="tgtSentence">To test this example, cut and paste this code between the &lt;Body&gt; and &lt;/Body&gt; tags in a normal HTML document and name it <legacyBold>CancelUpdateVBS.asp</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="fbe7b655b9664fe1a7fe45b366a16244" id="tgt6" class="tgtSentence"> ASP script will identify your internet server.</caps:sentence>
          <caps:sentence sentenceid="9f59133092e790d59883919dc2ab8199" id="tgt7" class="tgtSentence"> You will need to edit the name of the server to reflect your own setup.</caps:sentence>
          <caps:sentence sentenceid="73688fbdcf49d903cdd4a313e5509eae" id="tgt8" class="tgtSentence"> Simply change the value in the connect string from MyServer to the name of your SQL Server installation.</caps:sentence>
        </para>
        <code>&lt;!-- BeginCancelUpdateVBS --&gt;
&lt;%@Language=VBScript%&gt;

&lt;%'Option Explicit%&gt;
&lt;% 'use the following META tag instead of adovbs.inc%&gt;
&lt;!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;META NAME="GENERATOR" Content="Microsoft Visual Studio 6.0"&gt;
&lt;TITLE&gt;&lt;/TITLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;CENTER&gt;
&lt;H1&gt;Remote Data Service&lt;/H1&gt;
&lt;H2&gt;SubmitChanges and CancelUpdate Methods&lt;/H2&gt;

&lt;%  ' to integrate/test this code replace the Server property value and 
    ' the Data Source value in the Connect property with appropriate values%&gt;

&lt;HR&gt;
&lt;OBJECT ID=RDS classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" HEIGHT=1 WIDTH=1&gt;&lt;/OBJECT&gt;
&lt;SCRIPT Language="VBScript"&gt;

     'set RDS properties for control just created

    RDS.Server = "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"
    RDS.SQL = "Select * from Employees"
    RDS.Connect = "Provider='sqloledb';Integrated Security='SSPI';Initial Catalog='Northwind';"
    RDS.Refresh
&lt;/SCRIPT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;THEAD&gt;
&lt;TR ID="ColHeaders"&gt;
   &lt;TH&gt;ID&lt;/TH&gt;
   &lt;TH&gt;FName&lt;/TH&gt;
   &lt;TH&gt;LName&lt;/TH&gt;
   &lt;TH&gt;Title&lt;/TH&gt;
   &lt;TH&gt;Hire Date&lt;/TH&gt;
   &lt;TH&gt;Birth Date&lt;/TH&gt;
   &lt;TH&gt;Extension&lt;/TH&gt;
   &lt;TH&gt;Home Phone&lt;/TH&gt;
&lt;/TR&gt;
&lt;/THEAD&gt;
&lt;TBODY&gt;
&lt;TR&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="EmployeeID" size=4&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="FirstName" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="LastName" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="Title" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="HireDate" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="BirthDate" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="Extension" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="HomePhone" size=8&gt; &lt;/TD&gt;
&lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;
&lt;HR&gt;
&lt;INPUT TYPE=button NAME="SubmitChange" VALUE="Submit Changes"&gt;
&lt;INPUT TYPE=button NAME="CancelChange" VALUE="Cancel Update"&gt;
&lt;BR&gt;
&lt;H4&gt;Alter a current entry on the grid. Move off that Row. &lt;BR&gt;
Submit the Changes to your DBMS or cancel the updates. &lt;/H4&gt;
&lt;/CENTER&gt;
&lt;SCRIPT Language="VBScript"&gt;

Sub SubmitChange_OnClick
    
    msgbox "Changes will be made"
    RDS.SubmitChanges   
    RDS.Refresh

End Sub

Sub CancelChange_OnClick

    msgbox "Changes will be cancelled"
    RDS.CancelUpdate
    RDS.Refresh

End Sub
--&gt;
&lt;/SCRIPT&gt;


&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndCancelUpdateVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
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
          <caps:sentence id="src5" class="srcSentence">To test this example, cut and paste this code between the &lt;Body&gt; and &lt;/Body&gt; tags in a normal HTML document and name it <legacyBold>CancelUpdateVBS.asp</legacyBold>.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> ASP script will identify your internet server.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> You will need to edit the name of the server to reflect your own setup.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Simply change the value in the connect string from MyServer to the name of your SQL Server installation.</caps:sentence>
        </para>
        <code>&lt;!-- BeginCancelUpdateVBS --&gt;
&lt;%@Language=VBScript%&gt;

&lt;%'Option Explicit%&gt;
&lt;% 'use the following META tag instead of adovbs.inc%&gt;
&lt;!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;META NAME="GENERATOR" Content="Microsoft Visual Studio 6.0"&gt;
&lt;TITLE&gt;&lt;/TITLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;CENTER&gt;
&lt;H1&gt;Remote Data Service&lt;/H1&gt;
&lt;H2&gt;SubmitChanges and CancelUpdate Methods&lt;/H2&gt;

&lt;%  ' to integrate/test this code replace the Server property value and 
    ' the Data Source value in the Connect property with appropriate values%&gt;

&lt;HR&gt;
&lt;OBJECT ID=RDS classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" HEIGHT=1 WIDTH=1&gt;&lt;/OBJECT&gt;
&lt;SCRIPT Language="VBScript"&gt;

     'set RDS properties for control just created

    RDS.Server = "http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"
    RDS.SQL = "Select * from Employees"
    RDS.Connect = "Provider='sqloledb';Integrated Security='SSPI';Initial Catalog='Northwind';"
    RDS.Refresh
&lt;/SCRIPT&gt;

&lt;TABLE DATASRC=#RDS&gt;
&lt;THEAD&gt;
&lt;TR ID="ColHeaders"&gt;
   &lt;TH&gt;ID&lt;/TH&gt;
   &lt;TH&gt;FName&lt;/TH&gt;
   &lt;TH&gt;LName&lt;/TH&gt;
   &lt;TH&gt;Title&lt;/TH&gt;
   &lt;TH&gt;Hire Date&lt;/TH&gt;
   &lt;TH&gt;Birth Date&lt;/TH&gt;
   &lt;TH&gt;Extension&lt;/TH&gt;
   &lt;TH&gt;Home Phone&lt;/TH&gt;
&lt;/TR&gt;
&lt;/THEAD&gt;
&lt;TBODY&gt;
&lt;TR&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="EmployeeID" size=4&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="FirstName" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="LastName" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="Title" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="HireDate" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="BirthDate" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="Extension" size=10&gt; &lt;/TD&gt;
   &lt;TD&gt; &lt;INPUT DATAFLD="HomePhone" size=8&gt; &lt;/TD&gt;
&lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;
&lt;HR&gt;
&lt;INPUT TYPE=button NAME="SubmitChange" VALUE="Submit Changes"&gt;
&lt;INPUT TYPE=button NAME="CancelChange" VALUE="Cancel Update"&gt;
&lt;BR&gt;
&lt;H4&gt;Alter a current entry on the grid. Move off that Row. &lt;BR&gt;
Submit the Changes to your DBMS or cancel the updates. &lt;/H4&gt;
&lt;/CENTER&gt;
&lt;SCRIPT Language="VBScript"&gt;

Sub SubmitChange_OnClick
    
    msgbox "Changes will be made"
    RDS.SubmitChanges   
    RDS.Refresh

End Sub

Sub CancelChange_OnClick

    msgbox "Changes will be cancelled"
    RDS.CancelUpdate
    RDS.Refresh

End Sub
--&gt;
&lt;/SCRIPT&gt;


&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndCancelUpdateVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
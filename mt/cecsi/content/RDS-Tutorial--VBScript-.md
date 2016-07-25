---
title: "RDS Tutorial (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e2a48c4d-88b1-43ff-a202-9cdec54997d2
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
# RDS Tutorial (VBScript)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="633bb91186097992976bd6eb0965b8cd" id="tgt1" class="tgtSentence">This is the RDS Tutorial, written in Microsoft Visual Basic Scripting Edition.</caps:sentence>
          <caps:sentence sentenceid="fd56b1be98949f935d1a5de2e5237c13" id="tgt2" class="tgtSentence"> For a description of the purpose of this tutorial, see the <legacyLink xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</legacyLink>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="3076039ffbe667dc4fef68967b6c9a2c" id="tgt7" class="tgtSentence">In this tutorial, <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> and <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> are created at design time — that is, they are defined with object tags, like this: <codeInline>&lt;OBJECT&gt;...&lt;/OBJECT&gt;</codeInline>.</caps:sentence>
          <caps:sentence sentenceid="f925251a174daa396ba4aa4055c97121" id="tgt8" class="tgtSentence"> Alternatively, they could be created at run time with the <link xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject Method (RDS)</link> method.</caps:sentence>
          <caps:sentence sentenceid="32e3f534bc49306e95ba8a1b7727352f" id="tgt9" class="tgtSentence"> For example, the <unmanagedCodeEntityReference>RDS.DataControl</unmanagedCodeEntityReference> object could be created like this:</caps:sentence>
        </para>
        <code>Set DC = <codeFeaturedElement xmlns="">Server.CreateObject</codeFeaturedElement>("RDS.DataControl")
   &lt;!-- RDS.DataControl --&gt;
   &lt;OBJECT 
      ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"&gt;
   &lt;/OBJECT&gt;

   &lt;!-- RDS.DataSpace --&gt;
   &lt;OBJECT 
      ID="DS1" WIDTH=1 HEIGHT=1
      CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"&gt;
   &lt;/OBJECT&gt;
   
   &lt;SCRIPT LANGUAGE="VBScript"&gt;

   Sub RDSTutorial()
   Dim DF1 </code>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4e1f002b8d5486c7c5b2c09e79adb478" id="tgt10" class="tgtSentence">Step 1 — Specify a server program</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="652dc5b902dcd3a2c3e2f6200eafeca7" id="tgt11" class="tgtSentence">VBScript can discover the name of the IIS Web server it is running on by accessing the VBScript <legacyBold>Request.ServerVariables</legacyBold> method available to Active Server Pages:</caps:sentence>
          </para>
          <code>"http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"</code>
          <para>
            <caps:sentence sentenceid="da1a5f8667fcfbbb3c46aca97ba986d6" id="tgt12" class="tgtSentence">However, for this tutorial, use the imaginary server, "yourServer".</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="a731bf42666040b2f4a75a8d7a6e9ec7" id="tgt13" class="tgtSentence">Pay attention to the data type of <legacyBold>ByRef</legacyBold> arguments.</caps:sentence>
              <caps:sentence sentenceid="fd1792864c225b595e99df24ada97a0b" id="tgt14" class="tgtSentence"> VBScript does not let you specify the variable type, so you must always pass a <languageKeyword>Variant</languageKeyword>.</caps:sentence>
              <caps:sentence sentenceid="627bd273d2e1a78c0dafbc6dbc17cc19" id="tgt15" class="tgtSentence"> When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the <legacyBold>RDS.DataSpace</legacyBold> object <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method.</caps:sentence>
              <caps:sentence sentenceid="8a7e69384525deb2bd7cd3cc6e8d1d83" id="tgt16" class="tgtSentence"> When using DCOM or an in-process server, you must match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</caps:sentence>
            </para>
          </alert>
          <code>Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "http://yourServer")</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1e9d33b36c6b8f57fcb57c227576beb7" id="tgt17" class="tgtSentence">Step 2a — Invoke the server program with RDS.DataControl</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="3ec11434eeff400953bf4d0bde951bbd" id="tgt18" class="tgtSentence">This example is merely a comment demonstrating that the default behavior of the <legacyBold>RDS.DataControl </legacyBold>is to perform the specified query.</caps:sentence>
          </para>
          <code>&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"&gt;
   &lt;PARAM NAME="SQL" VALUE="SELECT * FROM Authors"&gt;
   &lt;PARAM NAME="Connect" VALUE="DSN=Pubs;"&gt;
   &lt;PARAM NAME="Server" VALUE="http://yourServer/"&gt;
&lt;/OBJECT&gt;
...
&lt;SCRIPT LANGUAGE="VBScript"&gt;

Sub RDSTutorial2A()
   Dim RS
   DC1.Refresh
   Set RS = DC1.Recordset
...</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d61a24269e0dc0c092d007f86a18f162" id="tgt19" class="tgtSentence">Step 2b — Invoke the server program with RDSServer.DataFactory</caps:sentence>
        </title>
        <content></content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f3a869c8958b706135d0ab058efbcafb" id="tgt20" class="tgtSentence">Step 3 — Server obtains a Recordset</caps:sentence>
        </title>
        <content></content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="cc15c9724d77efe25586806e2612dea1" id="tgt21" class="tgtSentence">Step 4 — Server returns the Recordset</caps:sentence>
        </title>
        <content>
          <code>Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors")</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="7570af9af653d6403ff3db526bb85d46" id="tgt22" class="tgtSentence">Step 5 — DataControl is made usable by visual controls</caps:sentence>
        </title>
        <content>
          <code>' Assign the returned recordset to the DataControl.

DC1.SourceRecordset = RS</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a15233a7c321513d58ab647c11c84de6" id="tgt23" class="tgtSentence">Step 6a — Changes are sent to the server with RDS.DataControl</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="30ef2a1ce73494cb2311493c353e1b26" id="tgt24" class="tgtSentence">This example is merely a comment demonstrating how the <legacyBold>RDS.DataControl</legacyBold> performs updates.</caps:sentence>
          </para>
          <code>&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"&gt;
   &lt;PARAM NAME="SQL" VALUE="SELECT * FROM Authors"&gt;
   &lt;PARAM NAME="Connect" VALUE="DSN=Pubs;"&gt;
   &lt;PARAM NAME="Server" VALUE="http://yourServer/"&gt;
&lt;/OBJECT&gt;
...
&lt;SCRIPT LANGUAGE="VBScript"&gt;

Sub RDSTutorial6A()
Dim RS
DC1.Refresh
...
Set RS = DC1.Recordset
' Edit the Recordset object...
' The SERVER and CONNECT properties are already set from Step 2A.
Set DC1.SourceRecordset = RS
...
DC1.SubmitChanges</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="bbde3101c5c846cf27d431a4a1f39fc0" id="tgt25" class="tgtSentence">Step 6b — Changes are sent to the server with RDSServer.DataFactory</caps:sentence>
        </title>
        <content>
          <code>DF.SubmitChanges "DSN=Pubs", RS

End Sub
&lt;/SCRIPT&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;</code>
          <para>
            <caps:sentence sentenceid="933e817b96a7a9248336f20d9e222414" id="tgt26" class="tgtSentence">         <legacyBold>This is the end of the tutorial.</legacyBold>       </caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This is the RDS Tutorial, written in Microsoft Visual Basic Scripting Edition.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For a description of the purpose of this tutorial, see the <legacyLink xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</legacyLink>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src7" class="srcSentence">In this tutorial, <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> and <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> are created at design time — that is, they are defined with object tags, like this: <codeInline>&lt;OBJECT&gt;...&lt;/OBJECT&gt;</codeInline>.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Alternatively, they could be created at run time with the <link xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject Method (RDS)</link> method.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> For example, the <unmanagedCodeEntityReference>RDS.DataControl</unmanagedCodeEntityReference> object could be created like this:</caps:sentence>
        </para>
        <code>Set DC = <codeFeaturedElement xmlns="">Server.CreateObject</codeFeaturedElement>("RDS.DataControl")
   &lt;!-- RDS.DataControl --&gt;
   &lt;OBJECT 
      ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"&gt;
   &lt;/OBJECT&gt;

   &lt;!-- RDS.DataSpace --&gt;
   &lt;OBJECT 
      ID="DS1" WIDTH=1 HEIGHT=1
      CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"&gt;
   &lt;/OBJECT&gt;
   
   &lt;SCRIPT LANGUAGE="VBScript"&gt;

   Sub RDSTutorial()
   Dim DF1 </code>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Step 1 — Specify a server program</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">VBScript can discover the name of the IIS Web server it is running on by accessing the VBScript <legacyBold>Request.ServerVariables</legacyBold> method available to Active Server Pages:</caps:sentence>
          </para>
          <code>"http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"</code>
          <para>
            <caps:sentence id="src12" class="srcSentence">However, for this tutorial, use the imaginary server, "yourServer".</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence">Pay attention to the data type of <legacyBold>ByRef</legacyBold> arguments.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> VBScript does not let you specify the variable type, so you must always pass a <languageKeyword>Variant</languageKeyword>.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the <legacyBold>RDS.DataSpace</legacyBold> object <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method.</caps:sentence>
              <caps:sentence id="src16" class="srcSentence"> When using DCOM or an in-process server, you must match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</caps:sentence>
            </para>
          </alert>
          <code>Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "http://yourServer")</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src17" class="srcSentence">Step 2a — Invoke the server program with RDS.DataControl</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src18" class="srcSentence">This example is merely a comment demonstrating that the default behavior of the <legacyBold>RDS.DataControl </legacyBold>is to perform the specified query.</caps:sentence>
          </para>
          <code>&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"&gt;
   &lt;PARAM NAME="SQL" VALUE="SELECT * FROM Authors"&gt;
   &lt;PARAM NAME="Connect" VALUE="DSN=Pubs;"&gt;
   &lt;PARAM NAME="Server" VALUE="http://yourServer/"&gt;
&lt;/OBJECT&gt;
...
&lt;SCRIPT LANGUAGE="VBScript"&gt;

Sub RDSTutorial2A()
   Dim RS
   DC1.Refresh
   Set RS = DC1.Recordset
...</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src19" class="srcSentence">Step 2b — Invoke the server program with RDSServer.DataFactory</caps:sentence>
        </title>
        <content></content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Step 3 — Server obtains a Recordset</caps:sentence>
        </title>
        <content></content>
      </section>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Step 4 — Server returns the Recordset</caps:sentence>
        </title>
        <content>
          <code>Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors")</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Step 5 — DataControl is made usable by visual controls</caps:sentence>
        </title>
        <content>
          <code>' Assign the returned recordset to the DataControl.

DC1.SourceRecordset = RS</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">Step 6a — Changes are sent to the server with RDS.DataControl</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src24" class="srcSentence">This example is merely a comment demonstrating how the <legacyBold>RDS.DataControl</legacyBold> performs updates.</caps:sentence>
          </para>
          <code>&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"&gt;
   &lt;PARAM NAME="SQL" VALUE="SELECT * FROM Authors"&gt;
   &lt;PARAM NAME="Connect" VALUE="DSN=Pubs;"&gt;
   &lt;PARAM NAME="Server" VALUE="http://yourServer/"&gt;
&lt;/OBJECT&gt;
...
&lt;SCRIPT LANGUAGE="VBScript"&gt;

Sub RDSTutorial6A()
Dim RS
DC1.Refresh
...
Set RS = DC1.Recordset
' Edit the Recordset object...
' The SERVER and CONNECT properties are already set from Step 2A.
Set DC1.SourceRecordset = RS
...
DC1.SubmitChanges</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src25" class="srcSentence">Step 6b — Changes are sent to the server with RDSServer.DataFactory</caps:sentence>
        </title>
        <content>
          <code>DF.SubmitChanges "DSN=Pubs", RS

End Sub
&lt;/SCRIPT&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;</code>
          <para>
            <caps:sentence id="src26" class="srcSentence">         <legacyBold>This is the end of the tutorial.</legacyBold>       </caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
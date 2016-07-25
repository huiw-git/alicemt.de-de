---
title: "VBScript ADO Programming"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6aaaf6d0-1376-4473-bea6-b81f2645a9ac
caps.latest.revision: 9
caps.handback.revision: 9
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
# VBScript ADO Programming
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="659f3fca12bb99ab0a089b2b83aab445" id="tgt1" class="tgtSentence">Creating an ADO Project</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a7b51d6319760705922d33632930b08a" id="tgt2" class="tgtSentence">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project.</caps:sentence>
            <caps:sentence sentenceid="0b472fcf19715e6dab7a9a65b4654629" id="tgt3" class="tgtSentence"> Consequently, no associated features such as command line completion are supported.</caps:sentence>
            <caps:sentence sentenceid="b6be211f976012192c93337415038a41" id="tgt4" class="tgtSentence"> Also, by default, ADO enumerated constants are not defined in VBScript.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="47d3921cbc2020d1897cfc9da6149567" id="tgt5" class="tgtSentence">However, ADO provides you with two include files containing the following definitions to be used with VBScript:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="20de9ade5fc748bbe8bfe298fc9c1eea" id="tgt6" class="tgtSentence">For server-side scripting use Adovbs.inc, which is installed in the c:\Program Files\Common Files\System\ado\ folder by default.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fa4629dc24b64ab13e1780fa098bc38a" id="tgt7" class="tgtSentence">For client-side scripting use Adcvbs.inc, which is installed in the c:\Program Files\Common Files\System\msdac\ folder by default.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="8b087a47b74a04ae798b89a923ec38c5" id="tgt8" class="tgtSentence">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your Web site and referencing it from your ASP page like this:</caps:sentence>
          </para>
          <code>&lt;!--#include File="adovbs.inc"--&gt;</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f4db934d0876a93b9244bf25b4a3e64f" id="tgt9" class="tgtSentence">Creating ADO Objects in VBScript</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="82bed9f80cbb106fe1bec1e6789c6f66" id="tgt10" class="tgtSentence">You cannot use the <legacyBold>Dim</legacyBold> statement to assign objects to a specific type in VBScript.</caps:sentence>
            <caps:sentence sentenceid="956c90dfedd6f64fff86ef3c980a9398" id="tgt11" class="tgtSentence"> Also, VBScript does not support the <legacyBold>New</legacyBold> syntax used with the <legacyBold>Dim</legacyBold> statement in Visual Basic for Applications.</caps:sentence>
            <caps:sentence sentenceid="1dd4ad663f9cf7fc8e97c571484770fa" id="tgt12" class="tgtSentence"> You must instead use the <legacyBold>CreateObject</legacyBold> function call:</caps:sentence>
          </para>
          <code>Dim Rs1
Set Rs1 = Server.CreateObject( "ADODB.Recordset" )</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="168709963cf2b3dd558d4d6e5295827d" id="tgt13" class="tgtSentence">VBScript Examples</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f7f660c8daf47dd6e5b309e9d9c048e3" id="tgt14" class="tgtSentence">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</caps:sentence>
          </para>
          <code>&lt;%  @LANGUAGE="VBSCRIPT" %&gt;
&lt;%  Option Explicit %&gt;
&lt;!--#include File="adovbs.inc"--&gt;
&lt;HTML&gt;
    &lt;BODY BGCOLOR="White" topmargin="10" leftmargin="10"&gt;

    &lt;!-- Your ASP Code goes here --&gt;
&lt;%
Dim Source
Dim Connect
Dim Rs1
    
Source = "SELECT * FROM Authors"
Connect = "Provider=sqloledb;Data Source=srv;" &amp; _
    "Initial Catalog=Pubs;Integrated Security=SSPI;"

Set Rs1 = Server.CreateObject( "ADODB.Recordset" )
Rs1.Open Source, Connect, adOpenForwardOnly
Response.Write("Success!")
%&gt;
    &lt;/BODY&gt;
&lt;/HTML&gt;</code>
          <para>
            <caps:sentence sentenceid="280d48f67f41b2c33ed66a4b2aa04bd0" id="tgt15" class="tgtSentence">More specific VBScript examples are included with the ADO documentation.</caps:sentence>
            <caps:sentence sentenceid="6a4136a815298b98899c1a1b55866675" id="tgt16" class="tgtSentence"> For more information, see <legacyLink xlink:href="78bb9a95-7ac4-44b6-818b-d1787f952ed7">ADO Code Examples in Microsoft Visual Basic Scripting Edition</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="af6e5ae708cdc8144f40b7acd9b21d28" id="tgt17" class="tgtSentence">Differences Between VBScript and Visual Basic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e8eb8235648410bc3112155d7c624b98" id="tgt18" class="tgtSentence">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used.</caps:sentence>
            <caps:sentence sentenceid="a56922c2938e1c2a61279ce5d2654503" id="tgt19" class="tgtSentence"> However, some significant differences exist:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="123ed04d2c6050cf056124a3cebcfe3f" id="tgt20" class="tgtSentence">VBScript supports only the Variant data type, which can hold different types of data.</caps:sentence>
                <caps:sentence sentenceid="56b00abf599358e6b5a1695a40e6ac82" id="tgt21" class="tgtSentence"> You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript.</caps:sentence>
                <caps:sentence sentenceid="7ca9d20339a0c2103e77994edae12376" id="tgt22" class="tgtSentence"> It recognizes the type required by ADO, and converts the value in the Variant accordingly.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="14a4f3bf43ad6d4197ff3762a7eaa53d" id="tgt23" class="tgtSentence">You cannot use <legacyBold>on error goto &lt;label&gt;</legacyBold> within VBScript.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3a28bc6c66f8dd1914298f6b0e8a5cbc" id="tgt24" class="tgtSentence">VBScript supports some of the built-in Visual Basic functions such as <legacyBold>Msgbox</legacyBold>, <legacyBold>Date</legacyBold>, and <legacyBold>IsNumeric</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="48f1156c14cd86e86948d39b3c3cd1b6" id="tgt25" class="tgtSentence"> However, because VBScript is a subset of Visual Basic, not all built-in functions are supported.</caps:sentence>
                <caps:sentence sentenceid="cc7295b81c5c36c7aa05ab2ecfe0b165" id="tgt26" class="tgtSentence"> For example, VBScript does not support the <legacyBold>Format</legacyBold> function and the file I/O functions.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Creating an ADO Project</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Consequently, no associated features such as command line completion are supported.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Also, by default, ADO enumerated constants are not defined in VBScript.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">However, ADO provides you with two include files containing the following definitions to be used with VBScript:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">For server-side scripting use Adovbs.inc, which is installed in the c:\Program Files\Common Files\System\ado\ folder by default.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">For client-side scripting use Adcvbs.inc, which is installed in the c:\Program Files\Common Files\System\msdac\ folder by default.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src8" class="srcSentence">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your Web site and referencing it from your ASP page like this:</caps:sentence>
          </para>
          <code>&lt;!--#include File="adovbs.inc"--&gt;</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Creating ADO Objects in VBScript</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">You cannot use the <legacyBold>Dim</legacyBold> statement to assign objects to a specific type in VBScript.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Also, VBScript does not support the <legacyBold>New</legacyBold> syntax used with the <legacyBold>Dim</legacyBold> statement in Visual Basic for Applications.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> You must instead use the <legacyBold>CreateObject</legacyBold> function call:</caps:sentence>
          </para>
          <code>Dim Rs1
Set Rs1 = Server.CreateObject( "ADODB.Recordset" )</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">VBScript Examples</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</caps:sentence>
          </para>
          <code>&lt;%  @LANGUAGE="VBSCRIPT" %&gt;
&lt;%  Option Explicit %&gt;
&lt;!--#include File="adovbs.inc"--&gt;
&lt;HTML&gt;
    &lt;BODY BGCOLOR="White" topmargin="10" leftmargin="10"&gt;

    &lt;!-- Your ASP Code goes here --&gt;
&lt;%
Dim Source
Dim Connect
Dim Rs1
    
Source = "SELECT * FROM Authors"
Connect = "Provider=sqloledb;Data Source=srv;" &amp; _
    "Initial Catalog=Pubs;Integrated Security=SSPI;"

Set Rs1 = Server.CreateObject( "ADODB.Recordset" )
Rs1.Open Source, Connect, adOpenForwardOnly
Response.Write("Success!")
%&gt;
    &lt;/BODY&gt;
&lt;/HTML&gt;</code>
          <para>
            <caps:sentence id="src15" class="srcSentence">More specific VBScript examples are included with the ADO documentation.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> For more information, see <legacyLink xlink:href="78bb9a95-7ac4-44b6-818b-d1787f952ed7">ADO Code Examples in Microsoft Visual Basic Scripting Edition</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src17" class="srcSentence">Differences Between VBScript and Visual Basic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src18" class="srcSentence">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> However, some significant differences exist:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">VBScript supports only the Variant data type, which can hold different types of data.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> It recognizes the type required by ADO, and converts the value in the Variant accordingly.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">You cannot use <legacyBold>on error goto &lt;label&gt;</legacyBold> within VBScript.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src24" class="srcSentence">VBScript supports some of the built-in Visual Basic functions such as <legacyBold>Msgbox</legacyBold>, <legacyBold>Date</legacyBold>, and <legacyBold>IsNumeric</legacyBold>.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> However, because VBScript is a subset of Visual Basic, not all built-in functions are supported.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> For example, VBScript does not support the <legacyBold>Format</legacyBold> function and the file I/O functions.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
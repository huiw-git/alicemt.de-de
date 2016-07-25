---
title: "JScript ADO Programming"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - JScript
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 62273658-0fe7-4aac-b4d8-f725e6baf043
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
# JScript ADO Programming
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
            <caps:sentence sentenceid="0dd1ff9c3cf47cf7a58253a7ff599d99" id="tgt2" class="tgtSentence">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project.</caps:sentence>
            <caps:sentence sentenceid="0b472fcf19715e6dab7a9a65b4654629" id="tgt3" class="tgtSentence"> Consequently, no associated features such as command line completion are supported.</caps:sentence>
            <caps:sentence sentenceid="0f300593ce462beda636645450ddf050" id="tgt4" class="tgtSentence"> Also, by default, ADO enumerated constants are not defined in JScript.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1512d043887d29aefa5817743fa3fd32" id="tgt5" class="tgtSentence">However, ADO provides you with two include files containing the following definitions to be used with JScript:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="b1dda635ec25e313b7af80980be35e71" id="tgt6" class="tgtSentence">For server-side scripting use Adojavas.inc, which is installed in the ADO library folders.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ba1251a1d13fca6107050b7601ec33dd" id="tgt7" class="tgtSentence">For client-side scripting use Adcjavas.inc, which is installed in the ADO library folders.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="c5c3df42f3100335ddcc7b783909b3c9" id="tgt8" class="tgtSentence">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your Web site and references it from your ASP page like this:</caps:sentence>
          </para>
          <code>&lt;!--#include File="adojavas.inc"--&gt;</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5ae9b63b7bc9c8f19aebec3a9e6cde69" id="tgt9" class="tgtSentence">Creating ADO Objects in JScript</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e49fe3cf343b45d524f39c98169443db" id="tgt10" class="tgtSentence">You must instead use the <legacyBold>CreateObject</legacyBold> function call:</caps:sentence>
          </para>
          <code>var Rs1;
Rs1 = Server.CreateObject("ADODB.Recordset");</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5d2af74bc7808d2e6741c6100e16521c" id="tgt11" class="tgtSentence">JScript Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1efc19497796690d80330f40d8c7777c" id="tgt12" class="tgtSentence">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a <legacyBold>Recordset</legacyBold> object:</caps:sentence>
          </para>
          <code>&lt;%  @LANGUAGE="JScript" %&gt;
&lt;!--#include File="adojavas.inc"--&gt;
&lt;HTML&gt;
&lt;BODY BGCOLOR="White" topmargin="10" leftmargin="10"&gt;
&lt;%
var Source = "SELECT * FROM Authors";
var Connect =  "Provider=sqloledb;Data Source=srv;" +
    "Initial Catalog=Pubs;Integrated Security=SSPI;"
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" );
Rs1.Open(Source,Connect,adOpenForwardOnly);
Response.Write("Success!");
%&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;</code>
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
            <caps:sentence id="src2" class="srcSentence">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Consequently, no associated features such as command line completion are supported.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Also, by default, ADO enumerated constants are not defined in JScript.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">However, ADO provides you with two include files containing the following definitions to be used with JScript:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">For server-side scripting use Adojavas.inc, which is installed in the ADO library folders.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">For client-side scripting use Adcjavas.inc, which is installed in the ADO library folders.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src8" class="srcSentence">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your Web site and references it from your ASP page like this:</caps:sentence>
          </para>
          <code>&lt;!--#include File="adojavas.inc"--&gt;</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Creating ADO Objects in JScript</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">You must instead use the <legacyBold>CreateObject</legacyBold> function call:</caps:sentence>
          </para>
          <code>var Rs1;
Rs1 = Server.CreateObject("ADODB.Recordset");</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">JScript Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a <legacyBold>Recordset</legacyBold> object:</caps:sentence>
          </para>
          <code>&lt;%  @LANGUAGE="JScript" %&gt;
&lt;!--#include File="adojavas.inc"--&gt;
&lt;HTML&gt;
&lt;BODY BGCOLOR="White" topmargin="10" leftmargin="10"&gt;
&lt;%
var Source = "SELECT * FROM Authors";
var Connect =  "Provider=sqloledb;Data Source=srv;" +
    "Initial Catalog=Pubs;Integrated Security=SSPI;"
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" );
Rs1.Open(Source,Connect,adOpenForwardOnly);
Response.Write("Success!");
%&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
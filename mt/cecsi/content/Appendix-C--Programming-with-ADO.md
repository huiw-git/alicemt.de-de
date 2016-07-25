---
title: "Appendix C: Programming with ADO"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40af6e70-2a37-480f-aadc-92095d450af7
caps.latest.revision: 11
caps.handback.revision: 11
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
# Appendix C: Programming with ADO
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7b28617d913263b92d714cd6a18371a2" id="tgt1" class="tgtSentence">ADO is a COM automation interface component that can be used with many programming languages, including Microsoft Visual Basic, VBScript, JScript, Visual C++, and Visual J++.</caps:sentence>
          <caps:sentence sentenceid="2d80372526dedd0196ddd30d79741ed0" id="tgt2" class="tgtSentence"> A version of ADO is installed with each of these tools and other applications, such as Microsoft Office and Microsoft SQL Server.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="354a62f272bfe0039b47d8b7841a4d14" id="tgt3" class="tgtSentence">The library for ADO is msado15.dll and the program ID (ProgID) prefix is "ADODB."</caps:sentence>
          <caps:sentence sentenceid="16d620a426932590814ac316cc1e19f3" id="tgt4" class="tgtSentence"> For example, to explicitly refer to an ADO <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, use <codeInline>ADODB.Recordset</codeInline>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4886e26d8d53f13d189adbd7baacc690" id="tgt5" class="tgtSentence">For more information about programming with ADO in various development environments, see the following topics:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="9dfb6784-037d-4f9d-bb7f-b506b4498573">
                <caps:sentence sentenceid="63f8a677b3d261e69f7bdb3305484b2e" id="tgt6" class="tgtSentence">Using ADO with Microsoft Visual Basic</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="587cb1ba2fa6d22892c431e14ec305ab" id="tgt7" class="tgtSentence">
                <legacyLink xlink:href="76fc4d00-0c9f-422b-af5c-af6ed8fb29d8">Using ADO with Scripting Languages</legacyLink> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="bc4dda4afcaee778b3426933d2850079" id="tgt8" class="tgtSentence">
                <legacyLink xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">Using ADO with Microsoft Visual C++</legacyLink> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="15542c35-3bf7-4d5f-a3b2-3a5cff286987">
                <caps:sentence sentenceid="5ac9f309f120e22707e45fd6040f741f" id="tgt9" class="tgtSentence">Using ADO with Microsoft Visual J++</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="1582e411-55ac-40f0-bd3d-9a10654e4b67">ADO Samples</link>
        <link xlink:href="5dd48483-858a-48c2-98ce-f2359abe1f59">Configuring RDS</link>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
        <link xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">What's New in ADO</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO is a COM automation interface component that can be used with many programming languages, including Microsoft Visual Basic, VBScript, JScript, Visual C++, and Visual J++.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A version of ADO is installed with each of these tools and other applications, such as Microsoft Office and Microsoft SQL Server.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">The library for ADO is msado15.dll and the program ID (ProgID) prefix is "ADODB."</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example, to explicitly refer to an ADO <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, use <codeInline>ADODB.Recordset</codeInline>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">For more information about programming with ADO in various development environments, see the following topics:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="9dfb6784-037d-4f9d-bb7f-b506b4498573">
                <caps:sentence id="src6" class="srcSentence">Using ADO with Microsoft Visual Basic</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">
                <legacyLink xlink:href="76fc4d00-0c9f-422b-af5c-af6ed8fb29d8">Using ADO with Scripting Languages</legacyLink> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">
                <legacyLink xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">Using ADO with Microsoft Visual C++</legacyLink> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="15542c35-3bf7-4d5f-a3b2-3a5cff286987">
                <caps:sentence id="src9" class="srcSentence">Using ADO with Microsoft Visual J++</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="1582e411-55ac-40f0-bd3d-9a10654e4b67">ADO Samples</link>
        <link xlink:href="5dd48483-858a-48c2-98ce-f2359abe1f59">Configuring RDS</link>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
        <link xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">What's New in ADO</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
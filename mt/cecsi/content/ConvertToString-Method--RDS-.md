---
title: "ConvertToString Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe
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
# ConvertToString Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d536f3906df2f2227e9bba8de0bea5da" id="tgt1" class="tgtSentence">Converts a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to a MIME string that represents the recordset data.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>DataFactory</parameterReference>.<legacyBold>ConvertToString</legacyBold>(<parameterReference>Recordset</parameterReference>)</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="41531125f69098131facc32b1b8f2d1d" id="tgt6" class="tgtSentence"> <legacyItalic>DataFactory</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="35dd05598ab8303c73bc9037d548f6b2" id="tgt7" class="tgtSentence">An object variable that represents an <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f12c824c1f08397ff9ad9725419e444a" id="tgt8" class="tgtSentence"> <legacyItalic>Recordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="19fb7fa3b3a1eb1bd47c6441687333f8" id="tgt9" class="tgtSentence">An object variable that represents a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d858da988c732d4ad9ac1128b0673f98" id="tgt10" class="tgtSentence">With .asp files, use <legacyBold>ConvertToString</legacyBold> to embed the <legacyBold>Recordset</legacyBold> in an HTML page generated on the server to transport it to a client computer.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="348da97f7b924eb0112f692f12bd6df5" id="tgt11" class="tgtSentence">
              <legacyBold>ConvertToString</legacyBold> first loads the <legacyBold>Recordset</legacyBold> into the Cursor Service tables, and then generates a stream in MIME format.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ded2711ec0f10e7b4e28415f0d522f9b" id="tgt12" class="tgtSentence">On the client, Remote Data Service can convert the MIME string back into a fully functioning <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="c4cdc00c19bcf7595ef37a42de14edbe" id="tgt13" class="tgtSentence"> It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row.</caps:sentence>
            <caps:sentence sentenceid="1f20f8f26904fe582075a5f78f395609" id="tgt14" class="tgtSentence"> You shouldn't use it for streaming BLOB data and large result sets over HTTP.</caps:sentence>
            <caps:sentence sentenceid="dd96466c9822a702ac4ec00b07ef3696" id="tgt15" class="tgtSentence"> No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="3e92a1c46a772e03e0a41c878ca97db0" id="tgt16" class="tgtSentence">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K.</caps:sentence>
              <caps:sentence sentenceid="986077b1614d7005b549f9a31a58c04a" id="tgt17" class="tgtSentence"> If this limit is exceeded, an error is returned.</caps:sentence>
              <caps:sentence sentenceid="97f070bd895bb2eeff21325e0ddccc7c" id="tgt18" class="tgtSentence"> Keep the query scope relatively small when using MIME embedding via .asp files.</caps:sentence>
              <caps:sentence sentenceid="67eda541fd428d9dc80bf37bf9a2c923" id="tgt19" class="tgtSentence"> To fix this, download the latest version of VBScript from the Microsoft Windows Script Technologies Web site.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt20" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="31731e4f-3c0c-451e-8cbc-c9df28fabf6c">Visual Basic Example</link>
        <link xlink:href="edd0a01c-1a1b-4b91-9966-2529e244abae">VBScript Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Converts a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to a MIME string that represents the recordset data.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>DataFactory</parameterReference>.<legacyBold>ConvertToString</legacyBold>(<parameterReference>Recordset</parameterReference>)</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>DataFactory</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An object variable that represents an <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>Recordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">An object variable that represents a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">With .asp files, use <legacyBold>ConvertToString</legacyBold> to embed the <legacyBold>Recordset</legacyBold> in an HTML page generated on the server to transport it to a client computer.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">
              <legacyBold>ConvertToString</legacyBold> first loads the <legacyBold>Recordset</legacyBold> into the Cursor Service tables, and then generates a stream in MIME format.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">On the client, Remote Data Service can convert the MIME string back into a fully functioning <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> You shouldn't use it for streaming BLOB data and large result sets over HTTP.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src16" class="srcSentence">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> If this limit is exceeded, an error is returned.</caps:sentence>
              <caps:sentence id="src18" class="srcSentence"> Keep the query scope relatively small when using MIME embedding via .asp files.</caps:sentence>
              <caps:sentence id="src19" class="srcSentence"> To fix this, download the latest version of VBScript from the Microsoft Windows Script Technologies Web site.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="31731e4f-3c0c-451e-8cbc-c9df28fabf6c">Visual Basic Example</link>
        <link xlink:href="edd0a01c-1a1b-4b91-9966-2529e244abae">VBScript Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
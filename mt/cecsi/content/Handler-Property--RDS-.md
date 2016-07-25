---
title: "Handler Property (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: fdc34362-6d47-4727-b171-8d033159408e
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
# Handler Property (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d1947fe698b687dd2803a66c2d29efb2" id="tgt1" class="tgtSentence">Indicates the name of a server-side customization program (handler) that extends the functionality of the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>, and any parameters used by the <legacyItalic>handler</legacyItalic>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b400748c808c6bb7ebf1f0aa4c6277a9" id="tgt2" class="tgtSentence">
            <embeddedLabel>Applies To:</embeddedLabel> <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link></caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>DataControl</parameterReference>.<legacyBold>Handler = </legacyBold><parameterReference>String</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="5410803de64b24c3bce2e6be4e78df92" id="tgt7" class="tgtSentence">DataControl</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0f504ae70ec16a59af2497e524453cfb" id="tgt8" class="tgtSentence">An object variable that represents an <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt9" class="tgtSentence">String</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="48e969fe73f004d33e249f74bdf2fa89" id="tgt10" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that contains the name of the handler and any parameters, all separated by commas (for example, <codeInline>"handlerName,parm1,parm2,...,parm</codeInline><legacyItalic>N</legacyItalic><codeInline>"</codeInline>).</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ebac71877adce296ea273a059839aad9" id="tgt11" class="tgtSentence">This property supports <legacyLink xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">customization</legacyLink>, a functionality that requires setting the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0c73236182d0c539d9fb19b1e06deee3" id="tgt12" class="tgtSentence">The name of the handler and its parameters, if any, are separated by commas (",").</caps:sentence>
            <caps:sentence sentenceid="1b284b41d7b65d340f9f2dd527864eee" id="tgt13" class="tgtSentence"> Unpredictable behavior will result if a semicolon (";") appears anywhere within <legacyItalic>String</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="358adaf763d01ce853415fba19291a36" id="tgt14" class="tgtSentence"> You can write your own handler, provided it supports the <legacyBold>IDataFactoryHandler</legacyBold> interface.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2a312627fa9ce7b39bf8f1cba9fd3c67" id="tgt15" class="tgtSentence">The name of the default handler is <legacyBold>MSDFMAP.Handler</legacyBold>, and its default parameter is a customization file named <legacyBold>MSDFMAP.INI</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="3b629fcef915bf79a1fbc10d181439e9" id="tgt16" class="tgtSentence"> Use this property to invoke alternate customization files created by your server administrator.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ceff804d476b80945bfc694cbae5c4d2" id="tgt17" class="tgtSentence">The alternative to setting the <legacyBold>Handler </legacyBold>property is to specify a handler and parameters in the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property; that is, "<legacyBold>Handler=</legacyBold><legacyItalic>handlerName,parameter1,parameter2,...;</legacyItalic>".</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt18" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="9664f9a6-65fc-4e7f-be3d-3e4b501b558a">Visual Basic Example</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the name of a server-side customization program (handler) that extends the functionality of the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>, and any parameters used by the <legacyItalic>handler</legacyItalic>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">
            <embeddedLabel>Applies To:</embeddedLabel> <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link></caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>DataControl</parameterReference>.<legacyBold>Handler = </legacyBold><parameterReference>String</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src7" class="srcSentence">DataControl</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">An object variable that represents an <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src9" class="srcSentence">String</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">A <languageKeyword>String</languageKeyword> value that contains the name of the handler and any parameters, all separated by commas (for example, <codeInline>"handlerName,parm1,parm2,...,parm</codeInline><legacyItalic>N</legacyItalic><codeInline>"</codeInline>).</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">This property supports <legacyLink xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">customization</legacyLink>, a functionality that requires setting the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">The name of the handler and its parameters, if any, are separated by commas (",").</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Unpredictable behavior will result if a semicolon (";") appears anywhere within <legacyItalic>String</legacyItalic>.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> You can write your own handler, provided it supports the <legacyBold>IDataFactoryHandler</legacyBold> interface.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">The name of the default handler is <legacyBold>MSDFMAP.Handler</legacyBold>, and its default parameter is a customization file named <legacyBold>MSDFMAP.INI</legacyBold>.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Use this property to invoke alternate customization files created by your server administrator.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">The alternative to setting the <legacyBold>Handler </legacyBold>property is to specify a handler and parameters in the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property; that is, "<legacyBold>Handler=</legacyBold><legacyItalic>handlerName,parameter1,parameter2,...;</legacyItalic>".</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src18" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="9664f9a6-65fc-4e7f-be3d-3e4b501b558a">Visual Basic Example</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "URL Property (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8c56b233-1be8-442c-8d0e-a4c96465bc99
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
# URL Property (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="514a720ff0a038e3fbdd4a415bb8bd88" id="tgt1" class="tgtSentence">Indicates a string that contains a relative or absolute URL.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="bb387bedaa83b091abaa6acb06635bea" id="tgt2" class="tgtSentence">You can set the <legacyBold>URL</legacyBold> property at design time in the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl</legacyLink> object's OBJECT tag, or at run time in scripting code.</caps:sentence>
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
Design time: <legacyBold>&lt;PARAM NAME="URL" VALUE="</legacyBold><parameterReference>Server</parameterReference><legacyBold>"&gt;</legacyBold>
Run time: <parameterReference>DataControl</parameterReference>.<legacyBold>URL</legacyBold>=<legacyBold>"</legacyBold><parameterReference>Server</parameterReference><legacyBold>"</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="cf1e8c14e54505f60aa10ceb8d5d8ab3" id="tgt7" class="tgtSentence">Server</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ad50d0e26db9d12b8f919428393e76c2" id="tgt8" class="tgtSentence">A <legacyBold>String</legacyBold> value that contains a valid URL.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="5410803de64b24c3bce2e6be4e78df92" id="tgt9" class="tgtSentence">DataControl</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="83838e08d1fb9ccfecaf30421d4e584f" id="tgt10" class="tgtSentence">An object variable that represents a <legacyBold>DataControl</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="6294a6123160c74a089c20250ea05bde" id="tgt11" class="tgtSentence">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="df6bbd3f821d6b7e7cbe3f4ae14c073f" id="tgt12" class="tgtSentence"> Therefore, the user can obtain a <legacyBold>Recordset</legacyBold> without having to invoke the server-side <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory</legacyLink> object, or program a custom business object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c85f6bab9efce8061b50cf536ae29c9e" id="tgt13" class="tgtSentence">If the <legacyBold>URL</legacyBold> property has been set, <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges</legacyLink> will submit changes to the location specified by the URL.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="6ae5ac50-c88c-4262-b7ab-f2b3de382a0b">VBScript Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates a string that contains a relative or absolute URL.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">You can set the <legacyBold>URL</legacyBold> property at design time in the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl</legacyLink> object's OBJECT tag, or at run time in scripting code.</caps:sentence>
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
Design time: <legacyBold>&lt;PARAM NAME="URL" VALUE="</legacyBold><parameterReference>Server</parameterReference><legacyBold>"&gt;</legacyBold>
Run time: <parameterReference>DataControl</parameterReference>.<legacyBold>URL</legacyBold>=<legacyBold>"</legacyBold><parameterReference>Server</parameterReference><legacyBold>"</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src7" class="srcSentence">Server</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">A <legacyBold>String</legacyBold> value that contains a valid URL.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src9" class="srcSentence">DataControl</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">An object variable that represents a <legacyBold>DataControl</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Therefore, the user can obtain a <legacyBold>Recordset</legacyBold> without having to invoke the server-side <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory</legacyLink> object, or program a custom business object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">If the <legacyBold>URL</legacyBold> property has been set, <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges</legacyLink> will submit changes to the location specified by the URL.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="6ae5ac50-c88c-4262-b7ab-f2b3de382a0b">VBScript Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
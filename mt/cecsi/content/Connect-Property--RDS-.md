---
title: "Connect Property (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: dbad5e77-b213-4eb8-aecf-d60f203fdb59
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
# Connect Property (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8e451d7388e496b57de8c5267d3b5a5b" id="tgt1" class="tgtSentence">Indicates the database name from which the query and update operations are run.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="afef9bbc399a4d77f23639561d6a6469" id="tgt2" class="tgtSentence">You can set the <legacyBold>Connect</legacyBold> property at design time in the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</caps:sentence>
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
Design time: <legacyBold>&lt;PARAM NAME="Connect" VALUE="</legacyBold><parameterReference>ConnectionString</parameterReference><legacyBold>"&gt;</legacyBold>
Run time: <parameterReference>DataControl</parameterReference>.<legacyBold>Connect</legacyBold> = <legacyBold>"</legacyBold><parameterReference>ConnectionString</parameterReference><legacyBold>"</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d78656013dfd2e3c848a339806ae4610" id="tgt7" class="tgtSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="50412dd1faa516a61c1a268f2a981302" id="tgt8" class="tgtSentence">A valid connection string.</caps:sentence>
                <caps:sentence sentenceid="799dc91686f1e0683526ad9684864d1a" id="tgt9" class="tgtSentence"> For more general information about connection strings, see the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property or your provider documentation.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="013b19deee3040527abcfc89f542a3a5" id="tgt10" class="tgtSentence">Specifying MS Remote as the provider for the <legacyBold>RDS.DataControl</legacyBold> would create a four-tier scenario.</caps:sentence>
                  <caps:sentence sentenceid="c775aa768720d03f003bd3d641d29448" id="tgt11" class="tgtSentence"> Scenarios greater than three tiers have not been tested and should not be needed.</caps:sentence>
                </para>
              </alert>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="033f425d12dfef3857c30172a3b63457" id="tgt12" class="tgtSentence"> <legacyItalic>DataControl</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="828490da16877cdbdeeca7991f4d5603" id="tgt13" class="tgtSentence">An object variable that represents an <legacyBold>RDS.DataControl</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
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
        <link xlink:href="06297993-fe72-4446-aa76-3b8bc25444f6">VBScript Example</link>
        <link xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query Method (RDS)</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the database name from which the query and update operations are run.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">You can set the <legacyBold>Connect</legacyBold> property at design time in the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</caps:sentence>
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
Design time: <legacyBold>&lt;PARAM NAME="Connect" VALUE="</legacyBold><parameterReference>ConnectionString</parameterReference><legacyBold>"&gt;</legacyBold>
Run time: <parameterReference>DataControl</parameterReference>.<legacyBold>Connect</legacyBold> = <legacyBold>"</legacyBold><parameterReference>ConnectionString</parameterReference><legacyBold>"</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">A valid connection string.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> For more general information about connection strings, see the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property or your provider documentation.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src10" class="srcSentence">Specifying MS Remote as the provider for the <legacyBold>RDS.DataControl</legacyBold> would create a four-tier scenario.</caps:sentence>
                  <caps:sentence id="src11" class="srcSentence"> Scenarios greater than three tiers have not been tested and should not be needed.</caps:sentence>
                </para>
              </alert>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>DataControl</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">An object variable that represents an <legacyBold>RDS.DataControl</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
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
        <link xlink:href="06297993-fe72-4446-aa76-3b8bc25444f6">VBScript Example</link>
        <link xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query Method (RDS)</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
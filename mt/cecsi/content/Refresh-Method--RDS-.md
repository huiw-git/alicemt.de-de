---
title: "Refresh Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: c90a8050-0ff4-4c83-9925-261f2f2ccfe9
caps.latest.revision: 15
caps.handback.revision: 15
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
# Refresh Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8c8be8b7759b95498489c29821aa7c6d" id="tgt1" class="tgtSentence">Requeries the data source specified in the <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property and updates the query results.</caps:sentence>
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
          <parameterReference>DataControl.</parameterReference>
          <legacyBold>Refresh</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="5410803de64b24c3bce2e6be4e78df92" id="tgt6" class="tgtSentence">DataControl</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0f504ae70ec16a59af2497e524453cfb" id="tgt7" class="tgtSentence">An object variable that represents an <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1a583dcc02a8dfb36566fe16cb7d12fd" id="tgt8" class="tgtSentence">You must set the <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink>, <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server</legacyLink>, and <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> properties before you use the <legacyBold>Refresh</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="15f0595ea65480d2bf59b50ff72b75e2" id="tgt9" class="tgtSentence"> All data-bound controls on the form associated with an <legacyBold>RDS.DataControl</legacyBold> object will reflect the new set of records.</caps:sentence>
            <caps:sentence sentenceid="67559a5223c338de99e42490a8fc9342" id="tgt10" class="tgtSentence"> Any pre-existing <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object is released, and any unsaved changes are discarded.</caps:sentence>
            <caps:sentence sentenceid="d9c080cc7b54c400a833de54cc3f09bb" id="tgt11" class="tgtSentence"> The <legacyBold>Refresh</legacyBold> method automatically makes the first record the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ee9001788a84c88ea412130f4abc9abc" id="tgt12" class="tgtSentence">It is a good idea to call the <legacyBold>Refresh</legacyBold> method periodically when you work with data.</caps:sentence>
            <caps:sentence sentenceid="69e220a407fbb4b57bfe0cef211594f7" id="tgt13" class="tgtSentence"> If you retrieve data, and then leave it on a client computer for a while, it is likely to become out of date.</caps:sentence>
            <caps:sentence sentenceid="5aee99143cebdeb0bc2bd9fb6c56ac76" id="tgt14" class="tgtSentence"> It is possible that any changes that you make will fail, because someone else might have changed the record and submitted changes before you.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt15" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f5375fa1-4711-4f7e-9ba4-54c427f71325">Visual Basic Example</link>
        <link xlink:href="f2926578-bc60-464b-916e-ddfdb8014253">VBScript Example</link>
        <link xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Requeries the data source specified in the <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property and updates the query results.</caps:sentence>
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
          <parameterReference>DataControl.</parameterReference>
          <legacyBold>Refresh</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src6" class="srcSentence">DataControl</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An object variable that represents an <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">You must set the <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink>, <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server</legacyLink>, and <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> properties before you use the <legacyBold>Refresh</legacyBold> method.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> All data-bound controls on the form associated with an <legacyBold>RDS.DataControl</legacyBold> object will reflect the new set of records.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Any pre-existing <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object is released, and any unsaved changes are discarded.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The <legacyBold>Refresh</legacyBold> method automatically makes the first record the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">It is a good idea to call the <legacyBold>Refresh</legacyBold> method periodically when you work with data.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> If you retrieve data, and then leave it on a client computer for a while, it is likely to become out of date.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> It is possible that any changes that you make will fail, because someone else might have changed the record and submitted changes before you.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f5375fa1-4711-4f7e-9ba4-54c427f71325">Visual Basic Example</link>
        <link xlink:href="f2926578-bc60-464b-916e-ddfdb8014253">VBScript Example</link>
        <link xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
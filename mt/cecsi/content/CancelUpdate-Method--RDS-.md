---
title: "CancelUpdate Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650
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
# CancelUpdate Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8f657b4acdb74c03724281ed55b14174" id="tgt1" class="tgtSentence">Cancels any changes made to the current or new row of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
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
          <legacyBold>CancelUpdate</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="033f425d12dfef3857c30172a3b63457" id="tgt6" class="tgtSentence"> <legacyItalic>DataControl</legacyItalic> </caps:sentence>
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
            <caps:sentence sentenceid="531da96409b88491462377cd62cd0b10" id="tgt8" class="tgtSentence">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes.</caps:sentence>
            <caps:sentence sentenceid="1a141fceb8a74fa99370f50f066ff1e0" id="tgt9" class="tgtSentence"> When you call <legacyBold>CancelUpdate</legacyBold>, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c23912f0-1288-4727-8fb4-f643b8811cf7">VBScript Example</link>
        <link xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</link>
        <link xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel Method</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Cancels any changes made to the current or new row of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
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
          <legacyBold>CancelUpdate</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>DataControl</legacyItalic> </caps:sentence>
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
            <caps:sentence id="src8" class="srcSentence">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> When you call <legacyBold>CancelUpdate</legacyBold>, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c23912f0-1288-4727-8fb4-f643b8811cf7">VBScript Example</link>
        <link xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</link>
        <link xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel Method</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
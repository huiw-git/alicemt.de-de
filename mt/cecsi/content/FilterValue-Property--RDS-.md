---
title: "FilterValue Property (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 28f17186-b842-4cf9-b320-a9bb941c481b
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
# FilterValue Property (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b7c632296f693b8c718d7db3d07b4489" id="tgt1" class="tgtSentence">Indicates the value with which to filter records.</caps:sentence>
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
          <parameterReference>DataControl</parameterReference>.<legacyBold>FilterValue = </legacyBold><parameterReference>String</parameterReference></legacySyntax>
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
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt8" class="tgtSentence">String</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="dbdacaf5ad19c2626fa47b2b9856f849" id="tgt9" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that represents a data value with which to filter records (for example, <codeInline>'Programmer'</codeInline> or <codeInline>125</codeInline>).</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="43dfa00a494e7979698cc4673b7afb65" id="tgt10" class="tgtSentence">The <legacyLink xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn</legacyLink>, <legacyLink xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection</legacyLink>, <unmanagedCodeEntityReference>FilterValue</unmanagedCodeEntityReference>, <legacyLink xlink:href="24eb03ba-ccfd-4353-b6af-03586b2da6fd">FilterCriterion</legacyLink>, and <legacyLink xlink:href="0a5473e8-8ce6-4518-83fb-4920b827e285">FilterColumn</legacyLink> properties provide sorting and filtering functionality on the client-side cache.</caps:sentence>
            <caps:sentence sentenceid="55f7b6d4acb5cae0fd6b10260fefd7da" id="tgt11" class="tgtSentence"> The sorting functionality orders records by values from one column.</caps:sentence>
            <caps:sentence sentenceid="745c176b47f3959f8775f98aaf14bdf8" id="tgt12" class="tgtSentence"> The filtering functionality displays a subset of records based on find criteria, while the full <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is maintained in the cache.</caps:sentence>
            <caps:sentence sentenceid="5b9617c5e2a90a2184d103ace9f3648f" id="tgt13" class="tgtSentence"> The <legacyLink xlink:href="3957197a-f543-4d6b-9e11-67a77c2063b7">Reset</legacyLink> method will execute the criteria and replace the current <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> with an updatable <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dd824c85325adda7fbe7b25299fe10f8" id="tgt14" class="tgtSentence">Null values result in a type mismatch error.</caps:sentence>
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
        <link xlink:href="8a74802f-34d6-4676-bf94-07df5f8bff66">VBScript Example</link>
        <link xlink:href="0a5473e8-8ce6-4518-83fb-4920b827e285">FilterColumn Property (RDS)</link>
        <link xlink:href="24eb03ba-ccfd-4353-b6af-03586b2da6fd">FilterCriterion Property (RDS)</link>
        <link xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn Property (RDS)</link>
        <link xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the value with which to filter records.</caps:sentence>
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
          <parameterReference>DataControl</parameterReference>.<legacyBold>FilterValue = </legacyBold><parameterReference>String</parameterReference></legacySyntax>
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
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src8" class="srcSentence">String</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">A <languageKeyword>String</languageKeyword> value that represents a data value with which to filter records (for example, <codeInline>'Programmer'</codeInline> or <codeInline>125</codeInline>).</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">The <legacyLink xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn</legacyLink>, <legacyLink xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection</legacyLink>, <unmanagedCodeEntityReference>FilterValue</unmanagedCodeEntityReference>, <legacyLink xlink:href="24eb03ba-ccfd-4353-b6af-03586b2da6fd">FilterCriterion</legacyLink>, and <legacyLink xlink:href="0a5473e8-8ce6-4518-83fb-4920b827e285">FilterColumn</legacyLink> properties provide sorting and filtering functionality on the client-side cache.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The sorting functionality orders records by values from one column.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The filtering functionality displays a subset of records based on find criteria, while the full <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is maintained in the cache.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> The <legacyLink xlink:href="3957197a-f543-4d6b-9e11-67a77c2063b7">Reset</legacyLink> method will execute the criteria and replace the current <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> with an updatable <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">Null values result in a type mismatch error.</caps:sentence>
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
        <link xlink:href="8a74802f-34d6-4676-bf94-07df5f8bff66">VBScript Example</link>
        <link xlink:href="0a5473e8-8ce6-4518-83fb-4920b827e285">FilterColumn Property (RDS)</link>
        <link xlink:href="24eb03ba-ccfd-4353-b6af-03586b2da6fd">FilterCriterion Property (RDS)</link>
        <link xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn Property (RDS)</link>
        <link xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Reset Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3957197a-f543-4d6b-9e11-67a77c2063b7
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
# Reset Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="35afc4bf7938a8e7168aed71949be54c" id="tgt1" class="tgtSentence">Executes the sort or filter on a client-side <legacyBold>Recordset </legacyBold>based on the specified sort and filter properties.</caps:sentence>
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
          <parameterReference>DataControl</parameterReference>.<legacyBold>Reset(</legacyBold><parameterReference>value</parameterReference><legacyBold>)</legacyBold></legacySyntax>
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
            <definedTerm>
              <caps:sentence sentenceid="586d4526025012f78b5f65abd7fde628" id="tgt8" class="tgtSentence"> <legacyItalic>value</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt9" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="018e2c965522fb35485a6684153db12a" id="tgt10" class="tgtSentence"> A <languageKeyword>Boolean</languageKeyword> value that is <languageKeyword>True</languageKeyword> (default) if you want to filter on the current "filtered" rowset.</caps:sentence>
                <caps:sentence sentenceid="bea35489fce864eb713a6fa9cc985ef1" id="tgt11" class="tgtSentence">
                  <languageKeyword>False</languageKeyword> indicates that you filter on the original rowset, removing any previous filter options.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b1eca47a2748e2ceddb1407bd9ee11ac" id="tgt12" class="tgtSentence">The <legacyLink xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn</legacyLink>, <legacyLink xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection</legacyLink>, <legacyLink xlink:href="28f17186-b842-4cf9-b320-a9bb941c481b">FilterValue</legacyLink>, <legacyLink xlink:href="24eb03ba-ccfd-4353-b6af-03586b2da6fd">FilterCriterion</legacyLink>, and <legacyLink xlink:href="0a5473e8-8ce6-4518-83fb-4920b827e285">FilterColumn</legacyLink> properties provide sorting and filtering functionality on the client-side cache.</caps:sentence>
            <caps:sentence sentenceid="55f7b6d4acb5cae0fd6b10260fefd7da" id="tgt13" class="tgtSentence"> The sorting functionality orders records by values from one column.</caps:sentence>
            <caps:sentence sentenceid="0a5596a415e806cde080cad7df50b6cb" id="tgt14" class="tgtSentence"> The filtering functionality displays a subset of records based on a find criteria, while the full <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is maintained in the cache.</caps:sentence>
            <caps:sentence sentenceid="2a30dff9025f5a62073a6e0d1656fa3d" id="tgt15" class="tgtSentence"> The <legacyBold>Reset</legacyBold> method will execute the criteria and replace the current <legacyBold>Recordset</legacyBold> with an updatable <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8c85d0ff93cbbf96f58017dffe58ade5" id="tgt16" class="tgtSentence">If there are changes to the original data that have not been submitted, the <legacyBold>Reset</legacyBold> method will fail.</caps:sentence>
            <caps:sentence sentenceid="3932f69577a2450c719833eff06d1e8e" id="tgt17" class="tgtSentence"> First, use the <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges</legacyLink> method to save any changes in a read/write <legacyBold>Recordset</legacyBold>, and then use the <legacyBold>Reset</legacyBold> method to sort or filter the records.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1db8e19be2012adfaf3bc6e48c6482a4" id="tgt18" class="tgtSentence">If you want to perform more than one filter on your rowset, you can use the optional <legacyItalic>Boolean</legacyItalic> argument with the <legacyBold>Reset</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="d0890e0e495e769ecd2ea5beee68840e" id="tgt19" class="tgtSentence"> The following example shows how to do this:</caps:sentence>
          </para>
          <code>ADC.SQL = "Select au_lname from authors"
ADC.Refresh    ' Get the new rowset.

ADC.FilterColumn = "au_lname"
ADC.FilterCriterion = "&lt;"
ADC.FilterValue = "'M'"
ADC.Reset         ' Rowset now has all Last Names &lt; "M".

ADC.FilterCriterion = "&gt;"
ADC.FilterValue = "'F'"
' Passing True is not necessary, because it is the 
' default filter on the current "filtered" rowset.
ADC.Reset(TRUE)     ' Rowset now has all Last 
                    ' Names &lt; "M" and &gt; "F".

ADC.FilterCriterion = "&gt;"
ADC.FilterValue = "'T'"
' Filter on the original rowset, throwing out the
' previous filter options.
ADC.Reset(FALSE)   ' Rowset now has all Last Names &gt; "T".</code>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt20" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="8a74802f-34d6-4676-bf94-07df5f8bff66">VBScript Example</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Executes the sort or filter on a client-side <legacyBold>Recordset </legacyBold>based on the specified sort and filter properties.</caps:sentence>
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
          <parameterReference>DataControl</parameterReference>.<legacyBold>Reset(</legacyBold><parameterReference>value</parameterReference><legacyBold>)</legacyBold></legacySyntax>
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
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>value</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> A <languageKeyword>Boolean</languageKeyword> value that is <languageKeyword>True</languageKeyword> (default) if you want to filter on the current "filtered" rowset.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence">
                  <languageKeyword>False</languageKeyword> indicates that you filter on the original rowset, removing any previous filter options.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">The <legacyLink xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn</legacyLink>, <legacyLink xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection</legacyLink>, <legacyLink xlink:href="28f17186-b842-4cf9-b320-a9bb941c481b">FilterValue</legacyLink>, <legacyLink xlink:href="24eb03ba-ccfd-4353-b6af-03586b2da6fd">FilterCriterion</legacyLink>, and <legacyLink xlink:href="0a5473e8-8ce6-4518-83fb-4920b827e285">FilterColumn</legacyLink> properties provide sorting and filtering functionality on the client-side cache.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> The sorting functionality orders records by values from one column.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The filtering functionality displays a subset of records based on a find criteria, while the full <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is maintained in the cache.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The <legacyBold>Reset</legacyBold> method will execute the criteria and replace the current <legacyBold>Recordset</legacyBold> with an updatable <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">If there are changes to the original data that have not been submitted, the <legacyBold>Reset</legacyBold> method will fail.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> First, use the <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges</legacyLink> method to save any changes in a read/write <legacyBold>Recordset</legacyBold>, and then use the <legacyBold>Reset</legacyBold> method to sort or filter the records.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If you want to perform more than one filter on your rowset, you can use the optional <legacyItalic>Boolean</legacyItalic> argument with the <legacyBold>Reset</legacyBold> method.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> The following example shows how to do this:</caps:sentence>
          </para>
          <code>ADC.SQL = "Select au_lname from authors"
ADC.Refresh    ' Get the new rowset.

ADC.FilterColumn = "au_lname"
ADC.FilterCriterion = "&lt;"
ADC.FilterValue = "'M'"
ADC.Reset         ' Rowset now has all Last Names &lt; "M".

ADC.FilterCriterion = "&gt;"
ADC.FilterValue = "'F'"
' Passing True is not necessary, because it is the 
' default filter on the current "filtered" rowset.
ADC.Reset(TRUE)     ' Rowset now has all Last 
                    ' Names &lt; "M" and &gt; "F".

ADC.FilterCriterion = "&gt;"
ADC.FilterValue = "'T'"
' Filter on the original rowset, throwing out the
' previous filter options.
ADC.Reset(FALSE)   ' Rowset now has all Last Names &gt; "T".</code>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="8a74802f-34d6-4676-bf94-07df5f8bff66">VBScript Example</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
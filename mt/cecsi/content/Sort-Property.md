---
title: "Sort Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3683ffa0-6f93-4906-9533-ef6942f24f39
caps.latest.revision: 10
caps.handback.revision: 10
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
# Sort Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="373b945cae101ad3890e80064237030b" id="tgt1" class="tgtSentence">Indicates one or more field names on which the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is sorted, and whether each field is sorted in ascending or descending order.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7c2771e9ace4c3434076ba4105845b12" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that indicates the field names in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> on which to sort.</caps:sentence>
            <caps:sentence sentenceid="fa1affb27a8b3e4659891b028669c58a" id="tgt4" class="tgtSentence"> Each name is separated by a comma, and is optionally followed by a blank and the keyword, <languageKeyword>ASC</languageKeyword>, which sorts the field in ascending order, or <languageKeyword>DESC</languageKeyword>, which sorts the field in descending order.</caps:sentence>
            <caps:sentence sentenceid="d38e14e58622062acad1659334d1ef9b" id="tgt5" class="tgtSentence"> By default, if no keyword is specified, the field is sorted in ascending order.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="0a62935d2273151632762c03c1bab296" id="tgt6" class="tgtSentence">This property requires the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to be set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="6031fa3fd4d435848bd178b32c5fb7d6" id="tgt7" class="tgtSentence"> A temporary index will be created for each field specified in the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property if an index does not already exist.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0b92dbe7cb91c2b211e69017bddcaa5e" id="tgt8" class="tgtSentence">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c6bb1d26a50047468a1495d8fe99ea4a" id="tgt9" class="tgtSentence">When the value of the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property is anything other than an empty string, the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property order takes precedence over the order specified in an <languageKeyword>ORDER BY</languageKeyword> clause included in the SQL statement used to open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="af672b1a90a87c223957724e4627183f" id="tgt10" class="tgtSentence">The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> does not have to be opened before accessing the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property; it can be set at any time after the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is instantiated.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f3155745544ee3c05a116a9382e11fb4" id="tgt11" class="tgtSentence">Setting the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property to an empty string will reset the rows to their original order and delete temporary indexes.</caps:sentence>
            <caps:sentence sentenceid="f50be024f80b7867ced581d002816f22" id="tgt12" class="tgtSentence"> Existing indexes will not be deleted.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f6af980acd4d38d975dce6f5cb2a3691" id="tgt13" class="tgtSentence">Suppose a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> contains three fields named <legacyItalic>firstName</legacyItalic>, <legacyItalic>middleInitial</legacyItalic>, and <legacyItalic>lastName</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="c30ec00f9cc203285c1d5d5d0cd4c576" id="tgt14" class="tgtSentence"> Set the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property to the string, "<codeInline>lastName DESC, firstName ASC</codeInline>", which will order the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> by last name in descending order, then by first name in ascending order.</caps:sentence>
            <caps:sentence sentenceid="3a43ba2e847c8bd0a870ab39157c5a54" id="tgt15" class="tgtSentence"> The middle initial is ignored.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3084c59530fe8b04b429a86d6bb9a677" id="tgt16" class="tgtSentence">No field can be named "ASC" or "DESC" because those names conflict with the keywords <languageKeyword>ASC</languageKeyword> and <languageKeyword>DESC</languageKeyword>.</caps:sentence>
            <caps:sentence sentenceid="74d7a060b148c86af1bf6366e05a8a72" id="tgt17" class="tgtSentence"> You can create an alias for a field with a conflicting name by using the <languageKeyword>AS</languageKeyword> keyword in the query that returns the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt18" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="fc2fd40b-65d6-4023-90a3-90c9a88ef6cf">Visual Basic Example</link>
        <link xlink:href="58199284-747b-4312-b97f-797ee7bd4435">Visual C++ Example</link>
        <link xlink:href="460d4bbc-6250-475e-843e-899cf3c11742">Visual J++ Example</link>
        <link xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize Property — Dynamic (ADO)</link>
        <link xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn Property (RDS)</link>
        <link xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates one or more field names on which the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is sorted, and whether each field is sorted in ascending or descending order.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that indicates the field names in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> on which to sort.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Each name is separated by a comma, and is optionally followed by a blank and the keyword, <languageKeyword>ASC</languageKeyword>, which sorts the field in ascending order, or <languageKeyword>DESC</languageKeyword>, which sorts the field in descending order.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> By default, if no keyword is specified, the field is sorted in ascending order.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">This property requires the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to be set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> A temporary index will be created for each field specified in the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property if an index does not already exist.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">When the value of the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property is anything other than an empty string, the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property order takes precedence over the order specified in an <languageKeyword>ORDER BY</languageKeyword> clause included in the SQL statement used to open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> does not have to be opened before accessing the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property; it can be set at any time after the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is instantiated.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">Setting the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property to an empty string will reset the rows to their original order and delete temporary indexes.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Existing indexes will not be deleted.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">Suppose a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> contains three fields named <legacyItalic>firstName</legacyItalic>, <legacyItalic>middleInitial</legacyItalic>, and <legacyItalic>lastName</legacyItalic>.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> Set the <unmanagedCodeEntityReference>Sort</unmanagedCodeEntityReference> property to the string, "<codeInline>lastName DESC, firstName ASC</codeInline>", which will order the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> by last name in descending order, then by first name in ascending order.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The middle initial is ignored.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">No field can be named "ASC" or "DESC" because those names conflict with the keywords <languageKeyword>ASC</languageKeyword> and <languageKeyword>DESC</languageKeyword>.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> You can create an alias for a field with a conflicting name by using the <languageKeyword>AS</languageKeyword> keyword in the query that returns the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src18" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="fc2fd40b-65d6-4023-90a3-90c9a88ef6cf">Visual Basic Example</link>
        <link xlink:href="58199284-747b-4312-b97f-797ee7bd4435">Visual C++ Example</link>
        <link xlink:href="460d4bbc-6250-475e-843e-899cf3c11742">Visual J++ Example</link>
        <link xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize Property — Dynamic (ADO)</link>
        <link xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn Property (RDS)</link>
        <link xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
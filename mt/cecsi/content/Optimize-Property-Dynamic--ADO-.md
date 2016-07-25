---
title: "Optimize Property-Dynamic (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a491c4ce-2b04-4c84-be83-3846bde8d16b
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
# Optimize Property-Dynamic (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3450b60ba2507fa3163a216e7247c5bd" id="tgt1" class="tgtSentence">Specifies whether an index should be created on a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">field</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ff96bc031f90da0f6c36eebc038eab6d" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Boolean</languageKeyword> value that indicates whether an index should be created.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b4f345934e8bef49e8f275198199c9b8" id="tgt4" class="tgtSentence">An index can improve the performance of operations that find or sort values in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="f9bcf7a7dd462c5cdc84d18292620bc2" id="tgt5" class="tgtSentence"> The index is internal to ADO; you cannot explicitly access or use it in your application.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0776b5f1618a4f5ae91d17944fe53120" id="tgt6" class="tgtSentence">To create an index on a field, set the <legacyBold>Optimize</legacyBold> property to <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence sentenceid="6c19ce8916b3ec682fd8ca88d5a9642f" id="tgt7" class="tgtSentence"> To delete the index, set this property to <languageKeyword>False</languageKeyword>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5555d204ed35a02c3dca983e365d1b95" id="tgt8" class="tgtSentence">
              <legacyBold>Optimize</legacyBold> is a dynamic property appended to the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="9366282e11c151558bdfaab4a264aa1b" id="tgt9" class="tgtSentence">Usage</caps:sentence>
        </title>
        <content>
          <code>Dim rs As New Recordset
Dim fld As Field
rs.CursorLocation = adUseClient      'Enable index creation
rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
rs.Open
Set fld = rs.Fields(0)
fld.Properties("Optimize") = True    'Create an index
fld.Properties("Optimize") = False   'Delete an index</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="652194af-cfa4-4aa0-a6d6-fa409bbc3f98">Visual Basic Example</link>
        <link xlink:href="cb335455-b027-4f66-868d-d0d8b2175de1">Visual C++ Example</link>
        <link xlink:href="a75d5239-54a9-4eec-b144-a5848cdbf265">Visual J++ Example</link>
        <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link>
        <link xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find Method</link>
        <link xlink:href="3683ffa0-6f93-4906-9533-ef6942f24f39">Sort Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies whether an index should be created on a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">field</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Boolean</languageKeyword> value that indicates whether an index should be created.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">An index can improve the performance of operations that find or sort values in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The index is internal to ADO; you cannot explicitly access or use it in your application.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">To create an index on a field, set the <legacyBold>Optimize</legacyBold> property to <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> To delete the index, set this property to <languageKeyword>False</languageKeyword>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">
              <legacyBold>Optimize</legacyBold> is a dynamic property appended to the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Usage</caps:sentence>
        </title>
        <content>
          <code>Dim rs As New Recordset
Dim fld As Field
rs.CursorLocation = adUseClient      'Enable index creation
rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
rs.Open
Set fld = rs.Fields(0)
fld.Properties("Optimize") = True    'Create an index
fld.Properties("Optimize") = False   'Delete an index</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="652194af-cfa4-4aa0-a6d6-fa409bbc3f98">Visual Basic Example</link>
        <link xlink:href="cb335455-b027-4f66-868d-d0d8b2175de1">Visual C++ Example</link>
        <link xlink:href="a75d5239-54a9-4eec-b144-a5848cdbf265">Visual J++ Example</link>
        <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link>
        <link xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find Method</link>
        <link xlink:href="3683ffa0-6f93-4906-9533-ef6942f24f39">Sort Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
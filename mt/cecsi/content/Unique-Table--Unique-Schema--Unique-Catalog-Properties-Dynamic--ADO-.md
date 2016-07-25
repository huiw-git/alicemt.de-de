---
title: "Unique Table, Unique Schema, Unique Catalog Properties-Dynamic (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d0e775d8-e353-46a1-ad10-ed4cc240dfaa
caps.latest.revision: 11
caps.handback.revision: 11
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
# Unique Table, Unique Schema, Unique Catalog Properties-Dynamic (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2e569ff8ea9401da9efe1e2a4c50339d" id="tgt1" class="tgtSentence">Enables you to closely control modifications to a particular base table in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> that was formed by a JOIN operation on multiple base tables.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="73457e318ef69bbf4255bf8a2fdb228b" id="tgt2" class="tgtSentence">
                <legacyBold>Unique Table</legacyBold> specifies the name of the base table upon which updates, insertions, and deletions are allowed.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3974d09c37d7978e32e01e8884ca794f" id="tgt3" class="tgtSentence">
                <legacyBold>Unique Schema</legacyBold> specifies the <legacyItalic>schema</legacyItalic>, or name of the owner of the table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f1c0c21d503754fcc71a40f52192a43e" id="tgt4" class="tgtSentence">
                <legacyBold>Unique Catalog</legacyBold> specifies the <legacyItalic>catalog</legacyItalic>, or name of the database containing the table.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt5" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0aea3959747a8f884e17d8f53801236c" id="tgt6" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that is the name of a table, schema, or catalog.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="5b5f56adfa549ce64eb78a3f7b1a64d3" id="tgt7" class="tgtSentence">The desired base table is uniquely identified by its catalog, schema, and table names.</caps:sentence>
            <caps:sentence sentenceid="e56eaf22661518a285151f496f4d6ca0" id="tgt8" class="tgtSentence"> When the <legacyBold>Unique Table</legacyBold> property is set, the values of the <legacyBold>Unique Schema</legacyBold> or <legacyBold>Unique Catalog</legacyBold> properties are used to find the base table.</caps:sentence>
            <caps:sentence sentenceid="bba54ea34552c6879532d2d4f8d43211" id="tgt9" class="tgtSentence"> It is intended, but not required, that either or both the <legacyBold>Unique Schema</legacyBold> and <legacyBold>Unique Catalog</legacyBold> properties be set before the <legacyBold>Unique Table</legacyBold> property is set.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="06fc966d6c091dc7a0e9873cddbd8314" id="tgt10" class="tgtSentence">The primary key of the <legacyBold>Unique Table</legacyBold> is treated as the primary key of the entire <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="fe5f420bc8d98c8ef177798e889b5f1e" id="tgt11" class="tgtSentence"> This is the key that is used for any method requiring a primary key.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0b02f7e711e9f6720c980e6377a61546" id="tgt12" class="tgtSentence">While <legacyBold>Unique Table</legacyBold> is set, the <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink> method affects only the named table.</caps:sentence>
            <caps:sentence sentenceid="f18c819886a80c0ef7196b38cf6ed7d7" id="tgt13" class="tgtSentence"> The <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink>, <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>, and <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> methods affect any appropriate underlying base tables of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="718b444d6d8a8e041440305934839be7" id="tgt14" class="tgtSentence">
              <legacyBold>Unique Table</legacyBold> must be specified before doing any custom resynchronizations.</caps:sentence>
            <caps:sentence sentenceid="8001739bdcf15f66751959c3159b4415" id="tgt15" class="tgtSentence"> If <legacyBold>Unique Table</legacyBold> has not been specified, the <legacyLink xlink:href="4e2bb601-0fe8-4d61-b00e-38341d85a6bb">Resync Command</legacyLink> property will have no effect.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ce165c9ce1181bb52fbf10b253b5bc83" id="tgt16" class="tgtSentence">A run-time error results if a unique base table cannot be found.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ca24045a7cbcb40e2fa46f75feee4a4a" id="tgt17" class="tgtSentence">These dynamic properties are all appended to the <legacyBold>Recordset</legacyBold> object <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
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
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Enables you to closely control modifications to a particular base table in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> that was formed by a JOIN operation on multiple base tables.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">
                <legacyBold>Unique Table</legacyBold> specifies the name of the base table upon which updates, insertions, and deletions are allowed.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">
                <legacyBold>Unique Schema</legacyBold> specifies the <legacyItalic>schema</legacyItalic>, or name of the owner of the table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">
                <legacyBold>Unique Catalog</legacyBold> specifies the <legacyItalic>catalog</legacyItalic>, or name of the database containing the table.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that is the name of a table, schema, or catalog.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">The desired base table is uniquely identified by its catalog, schema, and table names.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> When the <legacyBold>Unique Table</legacyBold> property is set, the values of the <legacyBold>Unique Schema</legacyBold> or <legacyBold>Unique Catalog</legacyBold> properties are used to find the base table.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> It is intended, but not required, that either or both the <legacyBold>Unique Schema</legacyBold> and <legacyBold>Unique Catalog</legacyBold> properties be set before the <legacyBold>Unique Table</legacyBold> property is set.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">The primary key of the <legacyBold>Unique Table</legacyBold> is treated as the primary key of the entire <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> This is the key that is used for any method requiring a primary key.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">While <legacyBold>Unique Table</legacyBold> is set, the <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink> method affects only the named table.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> The <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink>, <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>, and <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> methods affect any appropriate underlying base tables of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">
              <legacyBold>Unique Table</legacyBold> must be specified before doing any custom resynchronizations.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> If <legacyBold>Unique Table</legacyBold> has not been specified, the <legacyLink xlink:href="4e2bb601-0fe8-4d61-b00e-38341d85a6bb">Resync Command</legacyLink> property will have no effect.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">A run-time error results if a unique base table cannot be found.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">These dynamic properties are all appended to the <legacyBold>Recordset</legacyBold> object <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
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
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
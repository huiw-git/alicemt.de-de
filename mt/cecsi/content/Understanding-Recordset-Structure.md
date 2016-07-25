---
title: "Understanding Recordset Structure"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3ef36d24-f121-4a5f-84ad-5fc84992e81d
caps.latest.revision: 9
caps.handback.revision: 9
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
# Understanding Recordset Structure
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4bd3c0ff6efd741311d3f559639d3464" id="tgt1" class="tgtSentence">Every <legacyBold>Recordset</legacyBold> has a <legacyBold>Fields</legacyBold> collection consisting of one or more <legacyBold>Field</legacyBold> objects.</caps:sentence>
          <caps:sentence sentenceid="a46251565fe9c939818b3613a1bf2fd9" id="tgt2" class="tgtSentence"> A <legacyBold>Field</legacyBold> object usually represents a table column.</caps:sentence>
          <caps:sentence sentenceid="abdfe6280782a0f78b5effde662daeff" id="tgt3" class="tgtSentence"> The following topics will explain how to navigate through the <legacyBold>Fields</legacyBold> collection and get information about each field.</caps:sentence>
          <caps:sentence sentenceid="de2e0abddbd6e5ff2b2579ce6900a495" id="tgt4" class="tgtSentence"> Then they will discuss what kind of information is available to you via the <legacyBold>Field</legacyBold> object and how to use it.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="1c1cb8fa8d8a8b0bc60002fed0ae5f73" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="574cf36e-e5f5-403b-983c-749ef93c108f">The Fields Collection</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6e8e4a66cb53d3a52b00f520ba4e13be" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="7d1c4ad5-4be3-42ab-b516-e7133ca300bc">The Field Object</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6db676d24ef4ba05082899685cbfc094" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="bdf9a56a-de4a-44de-9111-2f11ab7b16ea">Working with Recordsets</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Every <legacyBold>Recordset</legacyBold> has a <legacyBold>Fields</legacyBold> collection consisting of one or more <legacyBold>Field</legacyBold> objects.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A <legacyBold>Field</legacyBold> object usually represents a table column.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The following topics will explain how to navigate through the <legacyBold>Fields</legacyBold> collection and get information about each field.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Then they will discuss what kind of information is available to you via the <legacyBold>Field</legacyBold> object and how to use it.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="574cf36e-e5f5-403b-983c-749ef93c108f">The Fields Collection</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="7d1c4ad5-4be3-42ab-b516-e7133ca300bc">The Field Object</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="bdf9a56a-de4a-44de-9111-2f11ab7b16ea">Working with Recordsets</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
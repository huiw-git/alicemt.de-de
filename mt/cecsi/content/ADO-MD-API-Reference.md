---
title: "ADO MD API Reference"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ad709f69-113b-4972-9384-c1215641844d
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
# ADO MD API Reference
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f8f756ff28d0bbd37a6850ca6037b7c5" id="tgt1" class="tgtSentence">This section of the ADO MD documentation contains topics for each ADO MD object, collection, method, and property, as well as example code when appropriate.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt2" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="162e3a6dddef823395eaa6b531b2b8c0" id="tgt3" class="tgtSentence">             <legacyLink xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="040d087faf7cfc245bd6c24e95507180" id="tgt4" class="tgtSentence">             <legacyLink xlink:href="2a32e873-3282-4520-a7ed-89493f1da80e">ADO MD Objects</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="70f58cae2aa21f5be395825805a85444" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="01c53429-ccc9-4077-b738-d3c1f43bd76c">ADO MD Collections</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a123d7c1fa50717888e81dcd9e307058" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="11ca7e42-ab6a-47da-ab32-55abab663069">ADO MD Properties</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="19c92324fedd65753d3b19e2cd29d464" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="78bfa2f0-358b-40bb-be2e-16262752d676">ADO MD Methods</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="09f5f31328fa234189e30168476e1354" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="d9e66999-96f3-48ec-93b2-d9442da56d9b">ADO MD Enumerated Constants</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8aefac4c3b2931e39ddd8a2852edc35d" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="72cf9eb3-31f6-441c-aede-5383fdfb81af">ADO MD Code Examples</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="72cf9eb3-31f6-441c-aede-5383fdfb81af">ADO MD Code Examples</link>
        <link xlink:href="01c53429-ccc9-4077-b738-d3c1f43bd76c">ADO MD Collections</link>
        <link xlink:href="d9e66999-96f3-48ec-93b2-d9442da56d9b">ADO MD Enumerated Constants</link>
        <link xlink:href="78bfa2f0-358b-40bb-be2e-16262752d676">ADO MD Methods</link>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="2a32e873-3282-4520-a7ed-89493f1da80e">ADO MD Objects</link>
        <link xlink:href="11ca7e42-ab6a-47da-ab32-55abab663069">ADO MD Properties</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This section of the ADO MD documentation contains topics for each ADO MD object, collection, method, and property, as well as example code when appropriate.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">             <legacyLink xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">             <legacyLink xlink:href="2a32e873-3282-4520-a7ed-89493f1da80e">ADO MD Objects</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="01c53429-ccc9-4077-b738-d3c1f43bd76c">ADO MD Collections</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="11ca7e42-ab6a-47da-ab32-55abab663069">ADO MD Properties</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="78bfa2f0-358b-40bb-be2e-16262752d676">ADO MD Methods</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="d9e66999-96f3-48ec-93b2-d9442da56d9b">ADO MD Enumerated Constants</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="72cf9eb3-31f6-441c-aede-5383fdfb81af">ADO MD Code Examples</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="72cf9eb3-31f6-441c-aede-5383fdfb81af">ADO MD Code Examples</link>
        <link xlink:href="01c53429-ccc9-4077-b738-d3c1f43bd76c">ADO MD Collections</link>
        <link xlink:href="d9e66999-96f3-48ec-93b2-d9442da56d9b">ADO MD Enumerated Constants</link>
        <link xlink:href="78bfa2f0-358b-40bb-be2e-16262752d676">ADO MD Methods</link>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="2a32e873-3282-4520-a7ed-89493f1da80e">ADO MD Objects</link>
        <link xlink:href="11ca7e42-ab6a-47da-ab32-55abab663069">ADO MD Properties</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
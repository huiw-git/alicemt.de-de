---
title: "Getting Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3931e7ec-f66b-4d5d-aad3-c4bf12e8b154
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
# Getting Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a34ba54710e3ad4a3cb1af440bde5486" id="tgt1" class="tgtSentence">
            <legacyLink xlink:href="d6a66928-e68f-4c38-b87a-838c5de50a28">ADO Fundamentals</legacyLink>, and the <legacyLink xlink:href="de4bcd56-dac2-45e6-95ab-9fd7f25878fc">HelloData</legacyLink> example in particular, introduced the four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data.</caps:sentence>
          <caps:sentence sentenceid="ab54b4ef1d90c58a3ca2689493e5cf71" id="tgt2" class="tgtSentence"> This section discusses getting data in more detail.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="17c5d1e1bf20b63e61a6b5d5cdfb9b41" id="tgt3" class="tgtSentence">On a basic level, several ADO objects contribute to the operations of getting data.</caps:sentence>
          <caps:sentence sentenceid="55ab0b70d1f60dd03f0306fb68595b8c" id="tgt4" class="tgtSentence"> First you must connect to a data source using an ADO <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="94a4f4d8835737c77edd3e15c9f8fc3d" id="tgt5" class="tgtSentence"> Then you pass instructions to the data source using an ADO <legacyBold>Command</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="5deafb3c716f17f00dfed23fd68aa4cc" id="tgt6" class="tgtSentence"> Finally, you most often receive data in an ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt7" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="faa639542091ad857518057fc14e2d5f" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="82770486-37bd-4c90-885f-6817a7c77ad7">Connecting to Data Sources</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5e782624ff6a9008d20ed805d42e794c" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="7448d9ee-7f4b-47e3-be54-2df8c9bbac32">Preparing and Executing Commands</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b7bf3cde32ceb3d681d7f3cefa4f7f91" id="tgt10" class="tgtSentence">             <legacyLink xlink:href="791aa26e-7aae-477e-9f05-5cd46e1de095">Receiving Results</legacyLink>           </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">
            <legacyLink xlink:href="d6a66928-e68f-4c38-b87a-838c5de50a28">ADO Fundamentals</legacyLink>, and the <legacyLink xlink:href="de4bcd56-dac2-45e6-95ab-9fd7f25878fc">HelloData</legacyLink> example in particular, introduced the four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This section discusses getting data in more detail.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">On a basic level, several ADO objects contribute to the operations of getting data.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> First you must connect to a data source using an ADO <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Then you pass instructions to the data source using an ADO <legacyBold>Command</legacyBold> object.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Finally, you most often receive data in an ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="82770486-37bd-4c90-885f-6817a7c77ad7">Connecting to Data Sources</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="7448d9ee-7f4b-47e3-be54-2df8c9bbac32">Preparing and Executing Commands</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">             <legacyLink xlink:href="791aa26e-7aae-477e-9f05-5cd46e1de095">Receiving Results</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
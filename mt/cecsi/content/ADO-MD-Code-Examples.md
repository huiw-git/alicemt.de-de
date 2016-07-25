---
title: "ADO MD Code Examples"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 72cf9eb3-31f6-441c-aede-5383fdfb81af
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
# ADO MD Code Examples
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ea2cc1d0e5925aa19d7fa5dae4667e88" id="tgt1" class="tgtSentence">Use the following code examples to learn how to use the ADO MD objects, methods, and properties.</caps:sentence>
          <caps:sentence sentenceid="32c9b7f160f2918469c1be7cafd7ba90" id="tgt2" class="tgtSentence"> These examples are a subset of the sample applications installed with Microsoft SQL Server OLAP Services for SQL Server 7.0.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="900c58ea7c112b5804a82d7f7bf1739d" id="tgt3" class="tgtSentence">These examples use the MSOLAP OLE DB provider, and run against a Microsoft SQL Server OLAP Services local host.</caps:sentence>
          <caps:sentence sentenceid="388157165e3c9237baab369e344f5cd9" id="tgt4" class="tgtSentence"> However, these examples are intended to show fundamental ADO MD programming techniques, and should be easily adapted to other data sources or providers.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="1f32d844b7dc569afa7792cdc10ccf7d" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="bfb52e8c-cb06-47a0-931c-03b8bdb1a05a">ADO MD Code Examples in Visual Basic</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="cfb0c152866f11ad74b6312187171dbf" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="f2fb2d57-6884-42ef-a18c-2673ba9b85c0">ADO MD Code Examples in Visual Basic, Scripting Edition</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="ad709f69-113b-4972-9384-c1215641844d">ADO MD API Reference</link>
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
          <caps:sentence id="src1" class="srcSentence">Use the following code examples to learn how to use the ADO MD objects, methods, and properties.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These examples are a subset of the sample applications installed with Microsoft SQL Server OLAP Services for SQL Server 7.0.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">These examples use the MSOLAP OLE DB provider, and run against a Microsoft SQL Server OLAP Services local host.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> However, these examples are intended to show fundamental ADO MD programming techniques, and should be easily adapted to other data sources or providers.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="bfb52e8c-cb06-47a0-931c-03b8bdb1a05a">ADO MD Code Examples in Visual Basic</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="f2fb2d57-6884-42ef-a18c-2673ba9b85c0">ADO MD Code Examples in Visual Basic, Scripting Edition</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="ad709f69-113b-4972-9384-c1215641844d">ADO MD API Reference</link>
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
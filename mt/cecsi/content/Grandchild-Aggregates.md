---
title: "Grandchild Aggregates"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4162d35f-2ce1-4218-80a5-b6933348837e
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
# Grandchild Aggregates
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="84726074d6282cbf376df733a4872ea7" id="tgt1" class="tgtSentence">The chapter column created in a clause of a shape command may be given a <legacyItalic>chapter-alias name</legacyItalic> (typically with the AS keyword).</caps:sentence>
          <caps:sentence sentenceid="daa5e22d96e4e8661e3b7d2d606d1bae" id="tgt2" class="tgtSentence"> You can identify any column in any chapter of the shaped <legacyBold>Recordset</legacyBold> with a fully qualified name that identifies the child containing the column.</caps:sentence>
          <caps:sentence sentenceid="2ec44b882c56a7b8de9f199956ba322f" id="tgt3" class="tgtSentence"> For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</caps:sentence>
          <caps:sentence sentenceid="d9631790add9087a0a38e8c984f92e52" id="tgt4" class="tgtSentence"> The qualified name can then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The chapter column created in a clause of a shape command may be given a <legacyItalic>chapter-alias name</legacyItalic> (typically with the AS keyword).</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can identify any column in any chapter of the shaped <legacyBold>Recordset</legacyBold> with a fully qualified name that identifies the child containing the column.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The qualified name can then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
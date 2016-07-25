---
title: "Hybrid Commands"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e8ca40e8-459c-40e2-8dd3-3ec6d5ee7b51
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
# Hybrid Commands
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6938e495984f32fdef911fcde30e5721" id="tgt1" class="tgtSentence">Hybrid commands are partially parameterized commands.</caps:sentence>
          <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt2" class="tgtSentence"> For example:</caps:sentence>
        </para>
        <code>SHAPE {select * from plants} 
   APPEND( {select * from customers where country = ?} 
           RELATE PlantCountry TO PARAMETER 0, 
             PlantRegion TO CustomerRegion ) </code>
        <para>
          <caps:sentence sentenceid="87829d2b3c4a579e7a8484d6b4eef7d0" id="tgt3" class="tgtSentence">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Hybrid commands are partially parameterized commands.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For example:</caps:sentence>
        </para>
        <code>SHAPE {select * from plants} 
   APPEND( {select * from customers where country = ?} 
           RELATE PlantCountry TO PARAMETER 0, 
             PlantRegion TO CustomerRegion ) </code>
        <para>
          <caps:sentence id="src3" class="srcSentence">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
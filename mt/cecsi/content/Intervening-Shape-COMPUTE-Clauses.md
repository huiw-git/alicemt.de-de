---
title: "Intervening Shape COMPUTE Clauses"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a576bf81-8f3c-4ba1-817b-87e89a8da684
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
# Intervening Shape COMPUTE Clauses
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e16ccd087525d517a1d24871392a5ec6" id="tgt1" class="tgtSentence">It is valid to embed one or more COMPUTE clauses between the parent and child in a parameterized shape command, as in the following example:</caps:sentence>
        </para>
        <code>SHAPE {select au_lname, state from authors} APPEND 
   ((SHAPE 
      (SHAPE 
         {select * from authors where state = ?} rs 
      COMPUTE rs, ANY(rs.state) state, ANY(rs.au_lname) au_lname 
      BY au_id) rs2 
   COMPUTE rs2, ANY(rs2.state) BY au_lname) 
RELATE state TO PARAMETER 0)</code>
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
          <caps:sentence id="src1" class="srcSentence">It is valid to embed one or more COMPUTE clauses between the parent and child in a parameterized shape command, as in the following example:</caps:sentence>
        </para>
        <code>SHAPE {select au_lname, state from authors} APPEND 
   ((SHAPE 
      (SHAPE 
         {select * from authors where state = ?} rs 
      COMPUTE rs, ANY(rs.state) state, ANY(rs.au_lname) au_lname 
      BY au_id) rs2 
   COMPUTE rs2, ANY(rs2.state) BY au_lname) 
RELATE state TO PARAMETER 0)</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Examining Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de1d74af-89b6-4f3f-a8c9-07c3e2b3c9a5
caps.latest.revision: 13
caps.handback.revision: 13
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
# Examining Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ff2cc40a9f64de35440c89e9905eec58" id="tgt1" class="tgtSentence">The <legacyLink xlink:href="3931e7ec-f66b-4d5d-aad3-c4bf12e8b154">Getting Data</legacyLink> section explained how to retrieve data from a data source as one or more <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
          <caps:sentence sentenceid="da975c2a6eb9127f94eec1f4b80cf288" id="tgt2" class="tgtSentence"> This section will discuss <legacyBold>Recordset</legacyBold> in more detail, including how to navigate through the <legacyBold>Recordset</legacyBold> and view its data.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9054ee8cc6a7de318a648bea4f1e1d3f" id="tgt3" class="tgtSentence">
            <legacyBold>Recordset</legacyBold> supports various <legacyLink xlink:href="4295a6e5-112d-4595-b18a-57728893ac2d">properties and methods</legacyLink> for you to navigate and examine data contained within.</caps:sentence>
          <caps:sentence sentenceid="1f4eb3a637c6edae6481b107867da435" id="tgt4" class="tgtSentence"> These features are provider-dependent.</caps:sentence>
          <caps:sentence sentenceid="e18f895510302cc47efdfea4d23023dc" id="tgt5" class="tgtSentence"> Some providers might not support some properties or methods.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt6" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="e63ff331-8655-4be7-82c6-e6cd6cc9d16d">
                <caps:sentence sentenceid="ef061ed6401bcf9c04cafde6d8901024" id="tgt7" class="tgtSentence">Current Record and Size of Recordset</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="8d88c9aa-8ec8-4969-8fa1-1663fd29bfc4">
                <caps:sentence sentenceid="7a4cdd3e15bd1228a27e401d3db973da" id="tgt8" class="tgtSentence">Navigating Through Data</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="3ef36d24-f121-4a5f-84ad-5fc84992e81d">
                <caps:sentence sentenceid="144d77be5e619b775fd2d6d174eb3838" id="tgt9" class="tgtSentence">Understanding Recordset Structure</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="e770e626-68b1-4ddf-a217-d7b30311e2ee">
                <caps:sentence sentenceid="dc73a95e13b226eecfa33e49e59add62" id="tgt10" class="tgtSentence">Sample Recordset for Examining Data</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="c0dd4a0f-478d-4c5e-b5d5-7535f211d064">Boundaries of a Recordset</link>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyLink xlink:href="3931e7ec-f66b-4d5d-aad3-c4bf12e8b154">Getting Data</legacyLink> section explained how to retrieve data from a data source as one or more <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This section will discuss <legacyBold>Recordset</legacyBold> in more detail, including how to navigate through the <legacyBold>Recordset</legacyBold> and view its data.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">
            <legacyBold>Recordset</legacyBold> supports various <legacyLink xlink:href="4295a6e5-112d-4595-b18a-57728893ac2d">properties and methods</legacyLink> for you to navigate and examine data contained within.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> These features are provider-dependent.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Some providers might not support some properties or methods.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="e63ff331-8655-4be7-82c6-e6cd6cc9d16d">
                <caps:sentence id="src7" class="srcSentence">Current Record and Size of Recordset</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="8d88c9aa-8ec8-4969-8fa1-1663fd29bfc4">
                <caps:sentence id="src8" class="srcSentence">Navigating Through Data</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="3ef36d24-f121-4a5f-84ad-5fc84992e81d">
                <caps:sentence id="src9" class="srcSentence">Understanding Recordset Structure</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="e770e626-68b1-4ddf-a217-d7b30311e2ee">
                <caps:sentence id="src10" class="srcSentence">Sample Recordset for Examining Data</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="c0dd4a0f-478d-4c5e-b5d5-7535f211d064">Boundaries of a Recordset</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
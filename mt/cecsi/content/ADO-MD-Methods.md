---
title: "ADO MD Methods"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 78bfa2f0-358b-40bb-be2e-16262752d676
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
# ADO MD Methods
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerOrientationDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="77b7ec5422d33f847bbfedb6e70e9117" id="tgt1" class="tgtSentence">             <legacyLink xlink:href="a3aa594d-f9d4-4654-8625-ec20153ff5d9">Close</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="452f6a2d6fe327e61831cdd68440a618" id="tgt2" class="tgtSentence">Closes an open cellset.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4df9bbf50b299a11856113d739fa062b" id="tgt3" class="tgtSentence">             <legacyLink xlink:href="36b754b4-6b17-4dd1-a925-bca46938b7c4">GetSchemaObject</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1643c4f5e63f41124b8b7d8ee43fec5e" id="tgt4" class="tgtSentence">Retrieves an ADO MD schema object (dimension, hierarchy, level, or member) by its unique name.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f16d0858273040ba96b746120c96909a" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e4bbcdc29268e494e5f431fb8a32cfbc" id="tgt6" class="tgtSentence">Retrieves the results of a multidimensional query and returns the results to a cellset.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="ad709f69-113b-4972-9384-c1215641844d">ADO MD API Reference</link>
        <link xlink:href="72cf9eb3-31f6-441c-aede-5383fdfb81af">ADO MD Code Examples</link>
        <link xlink:href="01c53429-ccc9-4077-b738-d3c1f43bd76c">ADO MD Collections</link>
        <link xlink:href="d9e66999-96f3-48ec-93b2-d9442da56d9b">ADO MD Enumerated Constants</link>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="2a32e873-3282-4520-a7ed-89493f1da80e">ADO MD Objects</link>
        <link xlink:href="11ca7e42-ab6a-47da-ab32-55abab663069">ADO MD Properties</link>
      </relatedTopics>
    </developerOrientationDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerOrientationDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src1" class="srcSentence">             <legacyLink xlink:href="a3aa594d-f9d4-4654-8625-ec20153ff5d9">Close</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Closes an open cellset.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">             <legacyLink xlink:href="36b754b4-6b17-4dd1-a925-bca46938b7c4">GetSchemaObject</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Retrieves an ADO MD schema object (dimension, hierarchy, level, or member) by its unique name.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Retrieves the results of a multidimensional query and returns the results to a cellset.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="ad709f69-113b-4972-9384-c1215641844d">ADO MD API Reference</link>
        <link xlink:href="72cf9eb3-31f6-441c-aede-5383fdfb81af">ADO MD Code Examples</link>
        <link xlink:href="01c53429-ccc9-4077-b738-d3c1f43bd76c">ADO MD Collections</link>
        <link xlink:href="d9e66999-96f3-48ec-93b2-d9442da56d9b">ADO MD Enumerated Constants</link>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="2a32e873-3282-4520-a7ed-89493f1da80e">ADO MD Objects</link>
        <link xlink:href="11ca7e42-ab6a-47da-ab32-55abab663069">ADO MD Properties</link>
      </relatedTopics>
    </developerOrientationDocument>
  </caps:SxSSource>
</caps:SxS>
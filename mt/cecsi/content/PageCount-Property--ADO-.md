---
title: "PageCount Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b601b56c-0ac4-44ee-bc91-c3d2d104f00a
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
# PageCount Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1cacab1824a95c6170c02c316ab6f561" id="tgt1" class="tgtSentence">Indicates how many pages of data the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object contains.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="25852df05e2f116102a977422d9daa0a" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> value that indicates the number of pages in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="8b1e98f07dff51efd60a37563a63d4bd" id="tgt4" class="tgtSentence">Use the <legacyBold>PageCount</legacyBold> property to determine how many pages of data are in the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="756f3a8d855fa3af20283e68d7acd040" id="tgt5" class="tgtSentence">
              <legacyItalic>Pages</legacyItalic> are groups of records whose size equals the <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize</legacyLink> property setting.</caps:sentence>
            <caps:sentence sentenceid="82689e96cfc90c17526ccb7818e5f342" id="tgt6" class="tgtSentence"> Even if the last page is incomplete because there are fewer records than the <legacyBold>PageSize</legacyBold> value, it counts as an additional page in the <legacyBold>PageCount</legacyBold> value.</caps:sentence>
            <caps:sentence sentenceid="b972c4e8de6f824cb0882810d97b288f" id="tgt7" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> object does not support this property, the value will be -1 to indicate that the <legacyBold>PageCount</legacyBold> is indeterminable.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="203d88c98e14a34b688e18e8b9695343" id="tgt8" class="tgtSentence">See the <legacyBold>PageSize</legacyBold> and <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> properties for more on page functionality.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5aaada64-5115-4adc-8668-827348f32566">Visual Basic Example</link>
        <link xlink:href="38ca4e1b-c109-4fba-b590-bdd6994f770e">Visual C++ Example</link>
        <link xlink:href="05f9f20e-0697-46bf-b004-76d7fc2e5d52">Visual J++ Example</link>
        <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property</link>
        <link xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize Property</link>
        <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates how many pages of data the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object contains.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> value that indicates the number of pages in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>PageCount</legacyBold> property to determine how many pages of data are in the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence">
              <legacyItalic>Pages</legacyItalic> are groups of records whose size equals the <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize</legacyLink> property setting.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Even if the last page is incomplete because there are fewer records than the <legacyBold>PageSize</legacyBold> value, it counts as an additional page in the <legacyBold>PageCount</legacyBold> value.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> object does not support this property, the value will be -1 to indicate that the <legacyBold>PageCount</legacyBold> is indeterminable.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">See the <legacyBold>PageSize</legacyBold> and <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> properties for more on page functionality.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5aaada64-5115-4adc-8668-827348f32566">Visual Basic Example</link>
        <link xlink:href="38ca4e1b-c109-4fba-b590-bdd6994f770e">Visual C++ Example</link>
        <link xlink:href="05f9f20e-0697-46bf-b004-76d7fc2e5d52">Visual J++ Example</link>
        <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property</link>
        <link xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize Property</link>
        <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
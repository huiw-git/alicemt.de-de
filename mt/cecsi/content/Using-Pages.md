---
title: "Using Pages"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 442b08c5-ccc7-4192-a1cc-22f250867782
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
# Using Pages
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8b1e98f07dff51efd60a37563a63d4bd" id="tgt1" class="tgtSentence">Use the <legacyBold>PageCount</legacyBold> property to determine how many pages of data are in the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="8e8097e95a6d5160206864b27c9eba8e" id="tgt2" class="tgtSentence">
            <legacyItalic>Pages</legacyItalic> are groups of records whose size equals the <legacyBold>PageSize</legacyBold> property setting.</caps:sentence>
          <caps:sentence sentenceid="82689e96cfc90c17526ccb7818e5f342" id="tgt3" class="tgtSentence"> Even if the last page is incomplete because there are fewer records than the <legacyBold>PageSize</legacyBold> value, it counts as an additional page in the <legacyBold>PageCount</legacyBold> value.</caps:sentence>
          <caps:sentence sentenceid="1a461b77221b474faaaa77eb161dd7f5" id="tgt4" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> object does not support this property, <legacyBold>PageCount</legacyBold> will be -1 to indicate that the <legacyBold>PageCount</legacyBold> is indeterminable.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ef68b690e4a47410d2a1fe53fce933de" id="tgt5" class="tgtSentence">Use the <legacyBold>PageSize</legacyBold> property to determine how many records make up a logical page of data.</caps:sentence>
          <caps:sentence sentenceid="5407b8fd8b8fa4bfae9910f520cb5258" id="tgt6" class="tgtSentence"> Establishing a page size allows you to use the <legacyBold>AbsolutePage</legacyBold> property to move to the first record of a particular page.</caps:sentence>
          <caps:sentence sentenceid="c6a97d7ed05f6e1da740614167612c12" id="tgt7" class="tgtSentence"> This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="76b8e688de580089bedf04c8283b5ede" id="tgt8" class="tgtSentence">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c0dec25cd9daeca4c9548cdbfbe0a230" id="tgt9" class="tgtSentence">Use the <legacyBold>AbsolutePage</legacyBold> property to identify the page number on which the current record is located.</caps:sentence>
          <caps:sentence sentenceid="a5999b4783287546af146836c9e6addb" id="tgt10" class="tgtSentence"> Again, the provider must support the appropriate functionality for this property to be available.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="913a988c5911e06cc63a2bf7d6d95f91" id="tgt11" class="tgtSentence">         <legacyBold>AbsolutePage</legacyBold> is 1-based and equals 1 when the current record is the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="0b7f0e16bf1ff57965a799973a87e5a8" id="tgt12" class="tgtSentence"> Set this property to move to the first record of a particular page.</caps:sentence>
          <caps:sentence sentenceid="18397dbfd65d35be21e5a49af6afddc8" id="tgt13" class="tgtSentence"> Obtain the total number of pages from the <legacyBold>PageCount</legacyBold> property.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <legacyBold>PageCount</legacyBold> property to determine how many pages of data are in the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence">
            <legacyItalic>Pages</legacyItalic> are groups of records whose size equals the <legacyBold>PageSize</legacyBold> property setting.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Even if the last page is incomplete because there are fewer records than the <legacyBold>PageSize</legacyBold> value, it counts as an additional page in the <legacyBold>PageCount</legacyBold> value.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> object does not support this property, <legacyBold>PageCount</legacyBold> will be -1 to indicate that the <legacyBold>PageCount</legacyBold> is indeterminable.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>PageSize</legacyBold> property to determine how many records make up a logical page of data.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Establishing a page size allows you to use the <legacyBold>AbsolutePage</legacyBold> property to move to the first record of a particular page.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">Use the <legacyBold>AbsolutePage</legacyBold> property to identify the page number on which the current record is located.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> Again, the provider must support the appropriate functionality for this property to be available.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">         <legacyBold>AbsolutePage</legacyBold> is 1-based and equals 1 when the current record is the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Set this property to move to the first record of a particular page.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> Obtain the total number of pages from the <legacyBold>PageCount</legacyBold> property.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
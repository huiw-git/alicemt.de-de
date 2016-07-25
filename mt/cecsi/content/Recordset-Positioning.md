---
title: "Recordset Positioning"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c8f6fbcb-6675-4133-b37e-430de43949c1
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
# Recordset Positioning
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="051850d6eb01dcbdaa1de5035329d305" id="tgt1" class="tgtSentence">Use the <legacyBold>AbsolutePosition</legacyBold> property to move to a record, based on its ordinal position in the <legacyBold>Recordset</legacyBold> object, or to determine the ordinal position of the current record.</caps:sentence>
          <caps:sentence sentenceid="f493d8b74249676ab7220d3ce60d4999" id="tgt2" class="tgtSentence"> The provider must support the appropriate functionality for this property to be available.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="de6b26c5fc8ef794a7a33f78a7250610" id="tgt3" class="tgtSentence">         <legacyBold>AbsolutePosition</legacyBold> is 1-based and equals 1 when the current record is the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="6303216c05a3340df60a2d83726af410" id="tgt4" class="tgtSentence"> As mentioned previously, you can obtain the total number of records in the <legacyBold>Recordset</legacyBold> object from the <legacyBold>RecordCount</legacyBold> property.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4fd3b6c7dc481b79db094faca2f5bc8c" id="tgt5" class="tgtSentence">When you set the <legacyBold>AbsolutePosition</legacyBold> property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified.</caps:sentence>
          <caps:sentence sentenceid="ab6ab90d14f17e9ce748da155bc916a4" id="tgt6" class="tgtSentence"> The <legacyBold>CacheSize</legacyBold> property determines the size of this group.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="d670f6ddbf984d9f58feb714f05e2912" id="tgt7" class="tgtSentence">You should not use the <legacyBold>AbsolutePosition</legacyBold> property as a surrogate record number.</caps:sentence>
            <caps:sentence sentenceid="fc1197fa9878f50b7559697bea304b14" id="tgt8" class="tgtSentence"> The position of a given record changes when you delete a preceding record.</caps:sentence>
            <caps:sentence sentenceid="463566b1b125ff27cf3f06fe0e17c914" id="tgt9" class="tgtSentence"> There also is no assurance that a given record will have the same <legacyBold>AbsolutePosition</legacyBold> if the <legacyBold>Recordset</legacyBold> object is requeried or reopened.</caps:sentence>
            <caps:sentence sentenceid="688d41eb0f7ed7ce4e28012469270e2b" id="tgt10" class="tgtSentence"> Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <legacyBold>AbsolutePosition</legacyBold> property to move to a record, based on its ordinal position in the <legacyBold>Recordset</legacyBold> object, or to determine the ordinal position of the current record.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The provider must support the appropriate functionality for this property to be available.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">         <legacyBold>AbsolutePosition</legacyBold> is 1-based and equals 1 when the current record is the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> As mentioned previously, you can obtain the total number of records in the <legacyBold>Recordset</legacyBold> object from the <legacyBold>RecordCount</legacyBold> property.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">When you set the <legacyBold>AbsolutePosition</legacyBold> property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The <legacyBold>CacheSize</legacyBold> property determines the size of this group.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src7" class="srcSentence">You should not use the <legacyBold>AbsolutePosition</legacyBold> property as a surrogate record number.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The position of a given record changes when you delete a preceding record.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> There also is no assurance that a given record will have the same <legacyBold>AbsolutePosition</legacyBold> if the <legacyBold>Recordset</legacyBold> object is requeried or reopened.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
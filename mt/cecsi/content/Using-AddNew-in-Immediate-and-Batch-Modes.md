---
title: "Using AddNew in Immediate and Batch Modes"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ed314bb9-e188-4658-a68c-a2abc49610be
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
# Using AddNew in Immediate and Batch Modes
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4c8bc67e924a287904f71d49a4e83fdb" id="tgt1" class="tgtSentence">The behavior of the <legacyBold>AddNew</legacyBold> method depends on the updating mode of the <legacyBold>Recordset</legacyBold> object and whether you pass the <legacyItalic>FieldList</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e0be070e8ac9cf2de329b54d97c55175" id="tgt2" class="tgtSentence">In immediate update mode (in which the provider writes changes to the underlying data source once you call the <legacyBold>Update</legacyBold> method), calling the <legacyBold>AddNew</legacyBold> method without arguments sets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditAdd.</legacyBold> The provider caches any field value changes locally.</caps:sentence>
          <caps:sentence sentenceid="5be8f1075c35ba230d6f29d094b909fa" id="tgt3" class="tgtSentence"> Calling the <legacyBold>Update</legacyBold> method posts the new record to the database and resets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditNone.</legacyBold> If you pass the <legacyItalic>FieldList</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments, ADO immediately posts the new record to the database (no <legacyBold>Update</legacyBold> call is necessary); the <legacyBold>EditMode</legacyBold> property value does not change (<legacyBold>adEditNone</legacyBold>).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1765d4435b74d6b72c878a6591140ea2" id="tgt4" class="tgtSentence">In batch update mode, calling the <legacyBold>AddNew</legacyBold> method without arguments sets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditAdd</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="169d1f869b196172745b8f23ccd01141" id="tgt5" class="tgtSentence"> The provider caches any field value changes locally.</caps:sentence>
          <caps:sentence sentenceid="2bd5d757c0355ccc7451d74977705e45" id="tgt6" class="tgtSentence"> Calling the <legacyBold>Update</legacyBold> method adds the new record to the current <legacyBold>Recordset</legacyBold> and resets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditNone</legacyBold>, but the provider does not post the changes to the underlying database until you call the <legacyBold>UpdateBatch</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="40196cadae8c8d8133f05eccb33c1150" id="tgt7" class="tgtSentence"> If you pass the <legacyItalic>FieldList</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments, ADO sends the new record to the provider for storage in a cache; you need to call the <legacyBold>UpdateBatch</legacyBold> method to post the new record to the underlying database.</caps:sentence>
          <caps:sentence sentenceid="a282c56f1865780e546eed247b59f6df" id="tgt8" class="tgtSentence"> For more information about <legacyBold>Update</legacyBold> and <legacyBold>UpdateBatch</legacyBold>, see <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The behavior of the <legacyBold>AddNew</legacyBold> method depends on the updating mode of the <legacyBold>Recordset</legacyBold> object and whether you pass the <legacyItalic>FieldList</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">In immediate update mode (in which the provider writes changes to the underlying data source once you call the <legacyBold>Update</legacyBold> method), calling the <legacyBold>AddNew</legacyBold> method without arguments sets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditAdd.</legacyBold> The provider caches any field value changes locally.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Calling the <legacyBold>Update</legacyBold> method posts the new record to the database and resets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditNone.</legacyBold> If you pass the <legacyItalic>FieldList</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments, ADO immediately posts the new record to the database (no <legacyBold>Update</legacyBold> call is necessary); the <legacyBold>EditMode</legacyBold> property value does not change (<legacyBold>adEditNone</legacyBold>).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">In batch update mode, calling the <legacyBold>AddNew</legacyBold> method without arguments sets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditAdd</legacyBold>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> The provider caches any field value changes locally.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Calling the <legacyBold>Update</legacyBold> method adds the new record to the current <legacyBold>Recordset</legacyBold> and resets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditNone</legacyBold>, but the provider does not post the changes to the underlying database until you call the <legacyBold>UpdateBatch</legacyBold> method.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> If you pass the <legacyItalic>FieldList</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments, ADO sends the new record to the provider for storage in a cache; you need to call the <legacyBold>UpdateBatch</legacyBold> method to post the new record to the underlying database.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> For more information about <legacyBold>Update</legacyBold> and <legacyBold>UpdateBatch</legacyBold>, see <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
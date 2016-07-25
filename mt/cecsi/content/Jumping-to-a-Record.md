---
title: "Jumping to a Record"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6caf6299-2eea-4d34-9b0e-b75aab07b740
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
# Jumping to a Record
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d9be3124831220c75893812a713cb0b6" id="tgt1" class="tgtSentence">The <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink> method allows you to move forward or backward in the <legacyBold>Recordset</legacyBold> a specified number of records by using the following syntax:</caps:sentence>
        </para>
        <code>oRs.Move NumRecords, Start</code>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7378753297b005957904e3d6deddb6b6" id="tgt2" class="tgtSentence">The <legacyBold>Move</legacyBold> method is supported on all <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="de2a928e24b0f1b2e6aa5de05bd9631c" id="tgt3" class="tgtSentence">If the <legacyItalic>NumRecords</legacyItalic> argument is greater than zero, the current record position moves forward (toward the end of the <legacyBold>Recordset</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="7719aaa4e10d7b0da1944cacb9d6b620" id="tgt4" class="tgtSentence"> If <legacyItalic>NumRecords</legacyItalic> is less than zero, the current record position moves backward (toward the beginning of the <legacyBold>Recordset</legacyBold>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="200a9e704b14438d17713c2923f66e67" id="tgt5" class="tgtSentence">If the <legacyBold>Move</legacyBold> call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the <legacyBold>Recordset</legacyBold> (<legacyBold>BOF</legacyBold> is <legacyBold>True</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="4c99003d94608e41b79194d45c6be9df" id="tgt6" class="tgtSentence"> An attempt to move backward when the <legacyBold>BOF</legacyBold> property is already <legacyBold>True</legacyBold> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0a3ef584e313234af3437571e3c78da7" id="tgt7" class="tgtSentence">If the <legacyBold>Move</legacyBold> call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the <legacyBold>Recordset</legacyBold> (<legacyBold>EOF</legacyBold> is <legacyBold>True</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="4697085a8b6f42204605523e9c0413dc" id="tgt8" class="tgtSentence"> An attempt to move forward when the <legacyBold>EOF</legacyBold> property is already <legacyBold>True</legacyBold> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6d4e8f68cd6c3cede4ca0d688df970ef" id="tgt9" class="tgtSentence">Calling the <legacyBold>Move</legacyBold> method from an empty <legacyBold>Recordset</legacyBold> object generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="24d86ad041b78ed51312e19d343f1a63" id="tgt10" class="tgtSentence">If you pass a bookmark in the <legacyItalic>Start</legacyItalic> argument, the move is relative to the record with this bookmark, assuming the <legacyBold>Recordset</legacyBold> object supports bookmarks.</caps:sentence>
            <caps:sentence sentenceid="8516406a779315f49ca577a02e85162b" id="tgt11" class="tgtSentence"> A bookmark is obtained by using the <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink> property.</caps:sentence>
            <caps:sentence sentenceid="b2d25f66d32d22ed9015297a9115fd76" id="tgt12" class="tgtSentence"> If not specified, the move is relative to the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dd1ccbf12f3085e8b938ed0090038c2f" id="tgt13" class="tgtSentence">If you are using the <legacyBold>CacheSize</legacyBold> property to locally cache records from the provider, passing a <legacyItalic>NumRecords</legacyItalic> argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</caps:sentence>
            <caps:sentence sentenceid="008e8e5a365de535e848a80c7c1864e6" id="tgt14" class="tgtSentence"> The <legacyBold>CacheSize</legacyBold> property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink> method allows you to move forward or backward in the <legacyBold>Recordset</legacyBold> a specified number of records by using the following syntax:</caps:sentence>
        </para>
        <code>oRs.Move NumRecords, Start</code>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <legacyBold>Move</legacyBold> method is supported on all <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">If the <legacyItalic>NumRecords</legacyItalic> argument is greater than zero, the current record position moves forward (toward the end of the <legacyBold>Recordset</legacyBold>).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> If <legacyItalic>NumRecords</legacyItalic> is less than zero, the current record position moves backward (toward the beginning of the <legacyBold>Recordset</legacyBold>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">If the <legacyBold>Move</legacyBold> call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the <legacyBold>Recordset</legacyBold> (<legacyBold>BOF</legacyBold> is <legacyBold>True</legacyBold>).</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> An attempt to move backward when the <legacyBold>BOF</legacyBold> property is already <legacyBold>True</legacyBold> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If the <legacyBold>Move</legacyBold> call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the <legacyBold>Recordset</legacyBold> (<legacyBold>EOF</legacyBold> is <legacyBold>True</legacyBold>).</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> An attempt to move forward when the <legacyBold>EOF</legacyBold> property is already <legacyBold>True</legacyBold> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">Calling the <legacyBold>Move</legacyBold> method from an empty <legacyBold>Recordset</legacyBold> object generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">If you pass a bookmark in the <legacyItalic>Start</legacyItalic> argument, the move is relative to the record with this bookmark, assuming the <legacyBold>Recordset</legacyBold> object supports bookmarks.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> A bookmark is obtained by using the <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink> property.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> If not specified, the move is relative to the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">If you are using the <legacyBold>CacheSize</legacyBold> property to locally cache records from the provider, passing a <legacyItalic>NumRecords</legacyItalic> argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The <legacyBold>CacheSize</legacyBold> property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Understanding Cursors and Locks"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c1b7d7e6-1707-4ce2-863f-0c6dea967df6
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
# Understanding Cursors and Locks
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b3141b3c8130cca0b5c935b31c0220b7" id="tgt1" class="tgtSentence">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements.</caps:sentence>
          <caps:sentence sentenceid="8d530e827251cc9a1b1bd8944fde268a" id="tgt2" class="tgtSentence"> A less-than-optimal cursor configuration can make data-access operations painfully slow.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="bac8479ed6ddd0dc6fc44802e5841644" id="tgt3" class="tgtSentence">Many capabilities of the ADO <legacyBold>Recordset</legacyBold> object are determined by the type and location of the cursor, as well as the lock type.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt4" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="631749cc57a77b2b079d787fd3db4def" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="596eb4b6-c22f-4cde-b23f-172dd66c3161">What is a Cursor?</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="623e50d5aad80ccec94ca45102a4e761" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="7cc01544-e814-403b-bbfe-a2750bf921bd">Types of Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4e2e4fbe5ebcf64115e1b2bdabc07637" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="70ef5b1c-0459-41a1-b796-031f61a29a8a">The Significance of Cursor Location</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="052adf75c8d1f98c08780b0daf48a25f" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="1ac3bd9b-2d45-4cc8-88ec-bd8a218cfb49">The Microsoft Cursor Service for OLE DB</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="69112b44a9dae004f96d9c7f75677e08" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="f8989555-28c6-4c17-9bf8-7f44a8a5c407">What is a Lock?</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="fe021f84a4344fc9170d5986c91d2b53" id="tgt10" class="tgtSentence">             <legacyLink xlink:href="ca1c3422-b6a4-4ba6-af55-54f975b698b1">Using CacheSize</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9df5457c0e4c228ecda3add6cbb39bc0" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="459c29cb-4230-42bf-8cc2-f3132ccc7aba">Cursor and Lock Characteristics</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A less-than-optimal cursor configuration can make data-access operations painfully slow.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Many capabilities of the ADO <legacyBold>Recordset</legacyBold> object are determined by the type and location of the cursor, as well as the lock type.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="596eb4b6-c22f-4cde-b23f-172dd66c3161">What is a Cursor?</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="7cc01544-e814-403b-bbfe-a2750bf921bd">Types of Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="70ef5b1c-0459-41a1-b796-031f61a29a8a">The Significance of Cursor Location</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="1ac3bd9b-2d45-4cc8-88ec-bd8a218cfb49">The Microsoft Cursor Service for OLE DB</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="f8989555-28c6-4c17-9bf8-7f44a8a5c407">What is a Lock?</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">             <legacyLink xlink:href="ca1c3422-b6a4-4ba6-af55-54f975b698b1">Using CacheSize</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="459c29cb-4230-42bf-8cc2-f3132ccc7aba">Cursor and Lock Characteristics</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
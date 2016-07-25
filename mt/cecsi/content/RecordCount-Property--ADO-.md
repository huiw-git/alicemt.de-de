---
title: "RecordCount Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 834f0121-394a-44d4-ad7d-999b43a6fe63
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
# RecordCount Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d3b2c7f4a5cc6e0ba60a693d9b572ec1" id="tgt1" class="tgtSentence">Indicates the number of records in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1091ddf65df16d6d553a324bf085d971" id="tgt3" class="tgtSentence">Returns a <legacyBold>Long</legacyBold> value that indicates the number of records in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="6ed5f4998b69b5b6069997c51c2e95f4" id="tgt4" class="tgtSentence">Use the <legacyBold>RecordCount</legacyBold> property to find out how many records are in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="5b5d86c26f14cee362d67ae1755433cb" id="tgt5" class="tgtSentence"> The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support <legacyBold>RecordCount</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="af60bfd661f1112381fd3f8107c42125" id="tgt6" class="tgtSentence"> Reading the <legacyBold>RecordCount</legacyBold> property on a closed <legacyBold>Recordset</legacyBold> causes an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="178ffe8e76d2ddc9c425e443e7eb78a7" id="tgt7" class="tgtSentence">If the <legacyBold>Recordset</legacyBold> object supports approximate positioning or bookmarks — that is, <legacyBold>Supports (adApproxPosition)</legacyBold> or <legacyBold>Supports (adBookmark)</legacyBold>, respectively, return <legacyBold>True</legacyBold>— this value will be the exact number of records in the <legacyBold>Recordset</legacyBold>, regardless of whether it has been fully populated.</caps:sentence>
            <caps:sentence sentenceid="81538f5f88714e59fc7b27681984d8bc" id="tgt8" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate <legacyBold>RecordCount</legacyBold> value.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="44a1c25c62122e99b2064d7a931f3574" id="tgt9" class="tgtSentence">In ADO versions 2.8 and earlier, the SQLOLEDB provider fetches all records when a server-side cursor is used, despite the fact that it returns <legacyBold>True</legacyBold> for both <legacyBold>Supports (adApproxPosition)</legacyBold> and <legacyBold>Supports (adBookmark)</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="3166fa223d6ac024177bd9ff02ff509c" id="tgt10" class="tgtSentence">The cursor type of the <legacyBold>Recordset</legacyBold> object affects whether the number of records can be determined.</caps:sentence>
            <caps:sentence sentenceid="86282d17812ec3127706ce87aa62c1bb" id="tgt11" class="tgtSentence"> The <legacyBold>RecordCount</legacyBold> property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e8bc63c7-8967-438a-9a49-512478a87a15">Visual Basic Example</link>
        <link xlink:href="b71346cb-3b09-4b8c-a600-976171a1c336">Visual C++ Example</link>
        <link xlink:href="16d5d896-9905-4f75-973b-e1e696cd169f">Visual J++ Example</link>
        <link xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition Property</link>
        <link xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the number of records in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyBold>Long</legacyBold> value that indicates the number of records in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>RecordCount</legacyBold> property to find out how many records are in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support <legacyBold>RecordCount</legacyBold>.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Reading the <legacyBold>RecordCount</legacyBold> property on a closed <legacyBold>Recordset</legacyBold> causes an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If the <legacyBold>Recordset</legacyBold> object supports approximate positioning or bookmarks — that is, <legacyBold>Supports (adApproxPosition)</legacyBold> or <legacyBold>Supports (adBookmark)</legacyBold>, respectively, return <legacyBold>True</legacyBold>— this value will be the exact number of records in the <legacyBold>Recordset</legacyBold>, regardless of whether it has been fully populated.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate <legacyBold>RecordCount</legacyBold> value.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src9" class="srcSentence">In ADO versions 2.8 and earlier, the SQLOLEDB provider fetches all records when a server-side cursor is used, despite the fact that it returns <legacyBold>True</legacyBold> for both <legacyBold>Supports (adApproxPosition)</legacyBold> and <legacyBold>Supports (adBookmark)</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src10" class="srcSentence">The cursor type of the <legacyBold>Recordset</legacyBold> object affects whether the number of records can be determined.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The <legacyBold>RecordCount</legacyBold> property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e8bc63c7-8967-438a-9a49-512478a87a15">Visual Basic Example</link>
        <link xlink:href="b71346cb-3b09-4b8c-a600-976171a1c336">Visual C++ Example</link>
        <link xlink:href="16d5d896-9905-4f75-973b-e1e696cd169f">Visual J++ Example</link>
        <link xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition Property</link>
        <link xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
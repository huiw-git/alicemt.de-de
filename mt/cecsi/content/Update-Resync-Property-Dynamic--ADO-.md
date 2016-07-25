---
title: "Update Resync Property-Dynamic (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8a3bb608-66d7-4128-a3ef-84cb0556de0d
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
# Update Resync Property-Dynamic (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2df6f9939cb037371a135ab05bc06960" id="tgt1" class="tgtSentence">Specifies whether the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method is followed by an implicit <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method operation, and if so, the scope of that operation.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6546fd23020938f4e716e63409f0626a" id="tgt3" class="tgtSentence">Sets or returns one or more of the <legacyLink xlink:href="bc9e1a37-e969-47e9-8382-0bbfffa2034f">ADCPROP_UPDATERESYNC_ENUM</legacyLink> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="44c74c5052941244cfa0d3d566b1cbd6" id="tgt4" class="tgtSentence">The values of ADCPROP_UPDATERESYNC_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5066d547863b4ee66c861991910b1116" id="tgt5" class="tgtSentence">The constant <legacyBold>adResyncConflicts</legacyBold> stores the resync values as underlying values, but does not override pending changes.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="320a42976fbaf3e66157e4ade2a09694" id="tgt6" class="tgtSentence">
              <legacyBold>Update Resync</legacyBold> is a dynamic property appended to the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies whether the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method is followed by an implicit <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method operation, and if so, the scope of that operation.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns one or more of the <legacyLink xlink:href="bc9e1a37-e969-47e9-8382-0bbfffa2034f">ADCPROP_UPDATERESYNC_ENUM</legacyLink> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The values of ADCPROP_UPDATERESYNC_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">The constant <legacyBold>adResyncConflicts</legacyBold> stores the resync values as underlying values, but does not override pending changes.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">
              <legacyBold>Update Resync</legacyBold> is a dynamic property appended to the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
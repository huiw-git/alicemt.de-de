---
title: "Updating Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6508e4e9-e33a-4dad-b340-5d632fd78a91
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
# Updating Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ffa463da06e8411a5342716154c2df27" id="tgt1" class="tgtSentence">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a1a715c1c78f30f2218bc46b94045193" id="tgt2" class="tgtSentence">Use the <legacyBold>Update</legacyBold> method to save any changes you have made to the current record of a <legacyBold>Recordset</legacyBold> object since calling the <legacyBold>AddNew</legacyBold> method or since changing any field values in an existing record.</caps:sentence>
          <caps:sentence sentenceid="80b6f8ecc21600414fdaeea6d6bd3498" id="tgt3" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> object must support updates.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ba1402217534318661106f2f0bd83ae4" id="tgt4" class="tgtSentence">If the <legacyBold>Recordset</legacyBold> object supports batch updating, you can cache multiple changes to one or more records locally until you call the <legacyBold>UpdateBatch</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="2f4896cabc48816935578cf0273dd102" id="tgt5" class="tgtSentence"> If you are editing the current record or adding a new record when you call the <legacyBold>UpdateBatch</legacyBold> method, ADO will automatically call the <legacyBold>Update</legacyBold> method to save any pending changes to the current record before transmitting the batched changes to the provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="6224001f4a57560ef9d49a762b7c8c2d" id="tgt6" class="tgtSentence">The current record remains current after you call the <legacyBold>Update</legacyBold> or <legacyBold>UpdateBatch</legacyBold> methods.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt7" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="58daeef1a5c3df60f35664f6b116165a" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="31fc53d0-97de-4315-a87b-3bf5cdd1f432">Immediate Mode</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5ca22a9644100b5c82268b29fab51bcd" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f37d1e0438b674e1460b6906aee3d2e8" id="tgt10" class="tgtSentence">             <legacyLink xlink:href="74ab6706-e2dc-42cb-af77-dbc58a9cf4ce">Transaction Processing</legacyLink>           </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Use the <legacyBold>Update</legacyBold> method to save any changes you have made to the current record of a <legacyBold>Recordset</legacyBold> object since calling the <legacyBold>AddNew</legacyBold> method or since changing any field values in an existing record.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The <legacyBold>Recordset</legacyBold> object must support updates.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">If the <legacyBold>Recordset</legacyBold> object supports batch updating, you can cache multiple changes to one or more records locally until you call the <legacyBold>UpdateBatch</legacyBold> method.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> If you are editing the current record or adding a new record when you call the <legacyBold>UpdateBatch</legacyBold> method, ADO will automatically call the <legacyBold>Update</legacyBold> method to save any pending changes to the current record before transmitting the batched changes to the provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">The current record remains current after you call the <legacyBold>Update</legacyBold> or <legacyBold>UpdateBatch</legacyBold> methods.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="31fc53d0-97de-4315-a87b-3bf5cdd1f432">Immediate Mode</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">             <legacyLink xlink:href="74ab6706-e2dc-42cb-af77-dbc58a9cf4ce">Transaction Processing</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Batch Mode"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0cb548e0-fcb4-4c49-98c8-be287911f826
caps.latest.revision: 14
caps.handback.revision: 14
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
# Batch Mode
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e1c32fe75fb06d7dcffeddbd1d9b0ffe" id="tgt1" class="tgtSentence">Batch mode is in effect when the <legacyBold>LockType</legacyBold> property is set to <legacyBold>adLockBatchOptimistic</legacyBold> and batch updating is supported by the provider.</caps:sentence>
          <caps:sentence sentenceid="f9d6b891498a7d44282581f4d87a745b" id="tgt2" class="tgtSentence"> Certain lock type settings are not available depending on cursor location.</caps:sentence>
          <caps:sentence sentenceid="7078680976cf84d9556589abfc6d989d" id="tgt3" class="tgtSentence"> For instance, a pessimistic lock type is not available when the <legacyBold>CursorLocation</legacyBold> is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="2aa19147ae2100243d84eb1027e20a9a" id="tgt4" class="tgtSentence"> Conversely, a provider cannot support a batch optimistic lock when the cursor location is on the server.</caps:sentence>
          <caps:sentence sentenceid="49229c0081f97b058513479e4d10c42b" id="tgt5" class="tgtSentence"> You should use batch updating with either a keyset or static cursor only.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="be4765ad4c71310bcdb35d4d9e2b5332" id="tgt6" class="tgtSentence">The <legacyBold>UpdateBatch</legacyBold> method is used to send <legacyBold>Recordset</legacyBold> changes held in the copy buffer to the server to update the data source.</caps:sentence>
          <caps:sentence sentenceid="861dc397eaf49ef1391d5fa18f1dfcc0" id="tgt7" class="tgtSentence"> In the following section, we will open a <legacyBold>Recordset</legacyBold> in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to <legacyBold>UpdateBatch</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="70a6f6496064fbbcc6c3110b6b32fd39" id="tgt8" class="tgtSentence">This section contains the following topics:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="87123797-831f-48e0-94b5-f669f9ca194a">Sending the Updates: UpdateBatch Method</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f3ea276c23bc71cab55daa012ed62b12" id="tgt9" class="tgtSentence">
                <link xlink:href="4a798921-d7bb-47c9-a252-550fd9463ec9">Filtering for Updated Records</link> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="31d417ef2a4af19de8ecb801fad0b7be" id="tgt10" class="tgtSentence">
                <link xlink:href="299c37bd-19ff-4261-8571-b9665687e075">Dealing with Failed Updates</link> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="b28fdd26-c1a4-40ce-a700-2b0c9d201514">Detecting and Resolving Conflicts</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="059250e776004e9bef297d20421a8d1b" id="tgt11" class="tgtSentence">
                <link xlink:href="c5134af7-81d6-4de4-9fd1-cfe29973545e">Disconnecting and Reconnecting the Recordset</link> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="67ba8b975cb5290b707d75d35959a948" id="tgt12" class="tgtSentence">
                <link xlink:href="d52e6926-5c22-43dc-9f32-7b32c1a071e2">Updating JOINed Results: Unique Table</link> </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Batch mode is in effect when the <legacyBold>LockType</legacyBold> property is set to <legacyBold>adLockBatchOptimistic</legacyBold> and batch updating is supported by the provider.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Certain lock type settings are not available depending on cursor location.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For instance, a pessimistic lock type is not available when the <legacyBold>CursorLocation</legacyBold> is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Conversely, a provider cannot support a batch optimistic lock when the cursor location is on the server.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> You should use batch updating with either a keyset or static cursor only.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">The <legacyBold>UpdateBatch</legacyBold> method is used to send <legacyBold>Recordset</legacyBold> changes held in the copy buffer to the server to update the data source.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> In the following section, we will open a <legacyBold>Recordset</legacyBold> in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to <legacyBold>UpdateBatch</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">This section contains the following topics:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="87123797-831f-48e0-94b5-f669f9ca194a">Sending the Updates: UpdateBatch Method</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">
                <link xlink:href="4a798921-d7bb-47c9-a252-550fd9463ec9">Filtering for Updated Records</link> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">
                <link xlink:href="299c37bd-19ff-4261-8571-b9665687e075">Dealing with Failed Updates</link> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="b28fdd26-c1a4-40ce-a700-2b0c9d201514">Detecting and Resolving Conflicts</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">
                <link xlink:href="c5134af7-81d6-4de4-9fd1-cfe29973545e">Disconnecting and Reconnecting the Recordset</link> </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">
                <link xlink:href="d52e6926-5c22-43dc-9f32-7b32c1a071e2">Updating JOINed Results: Unique Table</link> </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
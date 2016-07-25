---
title: "Using CacheSize"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ca1c3422-b6a4-4ba6-af55-54f975b698b1
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
# Using CacheSize
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="395939613085b27fce175de970de8ca6" id="tgt1" class="tgtSentence">Use the <legacyBold>CacheSize</legacyBold> property to control how many records to retrieve at one time into local memory from the provider.</caps:sentence>
          <caps:sentence sentenceid="7a545c2b8297bfdae3ddbdca5d181fc3" id="tgt2" class="tgtSentence"> For example, if the <legacyBold>CacheSize</legacyBold> is 10, after first opening the <legacyBold>Recordset</legacyBold> object, the provider retrieves the first 10 records into local memory.</caps:sentence>
          <caps:sentence sentenceid="619943e3035be5ed203a9479a8d55bc1" id="tgt3" class="tgtSentence"> As you move through the <legacyBold>Recordset</legacyBold> object, the provider returns the data from the local memory buffer.</caps:sentence>
          <caps:sentence sentenceid="b1e59c0e38004b82dde9c944b93e0bef" id="tgt4" class="tgtSentence"> As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="51398f23a0b6b849d0ea6d9ac5c00eea" id="tgt5" class="tgtSentence">           <legacyBold>CacheSize</legacyBold> is based on the <legacyBold>Maximum Open Rows</legacyBold> provider-specific property (in the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> object).</caps:sentence>
            <caps:sentence sentenceid="4c9f618b8c71b19955c5feb252dc83f3" id="tgt6" class="tgtSentence"> You cannot set <legacyBold>CacheSize</legacyBold> to a value greater than <legacyBold>Maximum Open Rows.</legacyBold> To modify the number of rows that can be opened by the provider, set <legacyBold>Maximum Open Rows</legacyBold>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="8ae091a33ceb5f6c5a6c5f697d6110b4" id="tgt7" class="tgtSentence">The value of <legacyBold>CacheSize</legacyBold> can be adjusted during the life of the <legacyBold>Recordset</legacyBold> object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</caps:sentence>
          <caps:sentence sentenceid="697406226712d075703b80bec6b8d068" id="tgt8" class="tgtSentence"> Changing the property value alone will not change the current contents of the cache.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9a20ac0482c62efb4b458746ddaaff76" id="tgt9" class="tgtSentence">If there are fewer records to retrieve than <legacyBold>CacheSize</legacyBold> specifies, the provider returns the remaining records and no error occurs.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="dcbf8f176b6e061d7f1554dc09898323" id="tgt10" class="tgtSentence">A <legacyBold>CacheSize</legacyBold> setting of zero is not allowed and returns an error.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ee0dc1d932302dca5ac78dee879473c5" id="tgt11" class="tgtSentence">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data.</caps:sentence>
          <caps:sentence sentenceid="d42260ab0593aed2ba518752f3549769" id="tgt12" class="tgtSentence"> To force an update of all the cached data, use the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e1ae49d4aa6c0c5c08afc22566866607" id="tgt13" class="tgtSentence">If <legacyBold>CacheSize</legacyBold> is set to a value greater than 1, the navigation methods (<legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious</legacyLink>) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</caps:sentence>
          <caps:sentence sentenceid="7e34148e07b01e5baf1ffe90d5e045a3" id="tgt14" class="tgtSentence"> After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</caps:sentence>
          <caps:sentence sentenceid="2fde11698c37bd74312fd46a57281f90" id="tgt15" class="tgtSentence"> However, setting <legacyBold>CacheSize</legacyBold> to 1 eliminates this issue because deleted rows cannot be fetched.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <legacyBold>CacheSize</legacyBold> property to control how many records to retrieve at one time into local memory from the provider.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For example, if the <legacyBold>CacheSize</legacyBold> is 10, after first opening the <legacyBold>Recordset</legacyBold> object, the provider retrieves the first 10 records into local memory.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> As you move through the <legacyBold>Recordset</legacyBold> object, the provider returns the data from the local memory buffer.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src5" class="srcSentence">           <legacyBold>CacheSize</legacyBold> is based on the <legacyBold>Maximum Open Rows</legacyBold> provider-specific property (in the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> object).</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> You cannot set <legacyBold>CacheSize</legacyBold> to a value greater than <legacyBold>Maximum Open Rows.</legacyBold> To modify the number of rows that can be opened by the provider, set <legacyBold>Maximum Open Rows</legacyBold>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src7" class="srcSentence">The value of <legacyBold>CacheSize</legacyBold> can be adjusted during the life of the <legacyBold>Recordset</legacyBold> object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Changing the property value alone will not change the current contents of the cache.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">If there are fewer records to retrieve than <legacyBold>CacheSize</legacyBold> specifies, the provider returns the remaining records and no error occurs.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">A <legacyBold>CacheSize</legacyBold> setting of zero is not allowed and returns an error.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> To force an update of all the cached data, use the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">If <legacyBold>CacheSize</legacyBold> is set to a value greater than 1, the navigation methods (<legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious</legacyLink>) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> However, setting <legacyBold>CacheSize</legacyBold> to 1 eliminates this issue because deleted rows cannot be fetched.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
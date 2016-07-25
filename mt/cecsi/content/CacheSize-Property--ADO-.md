---
title: "CacheSize Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 49dc9a49-af7b-433b-be36-7a14ca984fb7
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
# CacheSize Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="90e9c3547ad46967f7f19762ee08540a" id="tgt1" class="tgtSentence">Indicates the number of records from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object that are cached locally in memory.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6ca6ec54b50c4bbd62a7187bb0061da8" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that must be greater than 0.</caps:sentence>
            <caps:sentence sentenceid="ce13314b7f013f8110d364ae8facae8b" id="tgt4" class="tgtSentence"> Default is 1.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="395939613085b27fce175de970de8ca6" id="tgt5" class="tgtSentence">Use the <legacyBold>CacheSize</legacyBold> property to control how many records to retrieve at one time into local memory from the provider.</caps:sentence>
            <caps:sentence sentenceid="7a545c2b8297bfdae3ddbdca5d181fc3" id="tgt6" class="tgtSentence"> For example, if the <legacyBold>CacheSize</legacyBold> is 10, after first opening the <legacyBold>Recordset</legacyBold> object, the provider retrieves the first 10 records into local memory.</caps:sentence>
            <caps:sentence sentenceid="619943e3035be5ed203a9479a8d55bc1" id="tgt7" class="tgtSentence"> As you move through the <legacyBold>Recordset</legacyBold> object, the provider returns the data from the local memory buffer.</caps:sentence>
            <caps:sentence sentenceid="b1e59c0e38004b82dde9c944b93e0bef" id="tgt8" class="tgtSentence"> As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="7d2da42378b552b8c958baf40160702b" id="tgt9" class="tgtSentence"> <legacyBold>CacheSize</legacyBold> is based on the <legacyBold>Maximum Open Rows</legacyBold> provider-specific property (in the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> object).</caps:sentence>
              <caps:sentence sentenceid="a65fa5c24dad5f513d98d1dd80004b58" id="tgt10" class="tgtSentence"> You cannot set <legacyBold>CacheSize</legacyBold> to a value greater than <legacyBold>Maximum Open Rows</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="bf983dd77dd5f4bb3a3a71256390b4bf" id="tgt11" class="tgtSentence"> To modify the number of rows which can be opened by the provider, set <legacyBold>Maximum Open Rows</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="8ae091a33ceb5f6c5a6c5f697d6110b4" id="tgt12" class="tgtSentence">The value of <legacyBold>CacheSize</legacyBold> can be adjusted during the life of the <legacyBold>Recordset</legacyBold> object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</caps:sentence>
            <caps:sentence sentenceid="697406226712d075703b80bec6b8d068" id="tgt13" class="tgtSentence"> Changing the property value alone will not change the current contents of the cache.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9a20ac0482c62efb4b458746ddaaff76" id="tgt14" class="tgtSentence">If there are fewer records to retrieve than <legacyBold>CacheSize</legacyBold> specifies, the provider returns the remaining records and no error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dcbf8f176b6e061d7f1554dc09898323" id="tgt15" class="tgtSentence">A <legacyBold>CacheSize</legacyBold> setting of zero is not allowed and returns an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2b4bfd6792294b79b22d19fd0613ed20" id="tgt16" class="tgtSentence">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</caps:sentence>
            <caps:sentence sentenceid="d42260ab0593aed2ba518752f3549769" id="tgt17" class="tgtSentence"> To force an update of all the cached data, use the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2e22829166dcb10da16031f1b872dc03" id="tgt18" class="tgtSentence">If <legacyBold>CacheSize</legacyBold> is set to a value greater than one, the navigation methods (<legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious</legacyLink>) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</caps:sentence>
            <caps:sentence sentenceid="7e34148e07b01e5baf1ffe90d5e045a3" id="tgt19" class="tgtSentence"> After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</caps:sentence>
            <caps:sentence sentenceid="ddb7c65a996bf030b650ac6f00bf0776" id="tgt20" class="tgtSentence"> However, setting <legacyBold>CacheSize</legacyBold> to one eliminates this issue since deleted rows cannot be fetched.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt21" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a237ffdb-6e5b-47c6-9901-d5cdbe8625f3">Visual Basic Example</link>
        <link xlink:href="e0e7b7ba-3943-43cb-a2cd-0e4667187973">Visual C++ Example</link>
        <link xlink:href="d6fe482a-6951-438b-be58-e08f64efd1e2">Visual J++ Example</link>
        <link xlink:href="3675f641-b4b1-48ff-ba33-8d9ea064cd04">Jscript Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the number of records from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object that are cached locally in memory.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that must be greater than 0.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Default is 1.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>CacheSize</legacyBold> property to control how many records to retrieve at one time into local memory from the provider.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For example, if the <legacyBold>CacheSize</legacyBold> is 10, after first opening the <legacyBold>Recordset</legacyBold> object, the provider retrieves the first 10 records into local memory.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> As you move through the <legacyBold>Recordset</legacyBold> object, the provider returns the data from the local memory buffer.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src9" class="srcSentence"> <legacyBold>CacheSize</legacyBold> is based on the <legacyBold>Maximum Open Rows</legacyBold> provider-specific property (in the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> object).</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> You cannot set <legacyBold>CacheSize</legacyBold> to a value greater than <legacyBold>Maximum Open Rows</legacyBold>.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> To modify the number of rows which can be opened by the provider, set <legacyBold>Maximum Open Rows</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src12" class="srcSentence">The value of <legacyBold>CacheSize</legacyBold> can be adjusted during the life of the <legacyBold>Recordset</legacyBold> object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Changing the property value alone will not change the current contents of the cache.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">If there are fewer records to retrieve than <legacyBold>CacheSize</legacyBold> specifies, the provider returns the remaining records and no error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">A <legacyBold>CacheSize</legacyBold> setting of zero is not allowed and returns an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> To force an update of all the cached data, use the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If <legacyBold>CacheSize</legacyBold> is set to a value greater than one, the navigation methods (<legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious</legacyLink>) may result in navigation to a deleted record, if deletion occurs after the records were retrieved.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> However, setting <legacyBold>CacheSize</legacyBold> to one eliminates this issue since deleted rows cannot be fetched.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a237ffdb-6e5b-47c6-9901-d5cdbe8625f3">Visual Basic Example</link>
        <link xlink:href="e0e7b7ba-3943-43cb-a2cd-0e4667187973">Visual C++ Example</link>
        <link xlink:href="d6fe482a-6951-438b-be58-e08f64efd1e2">Visual J++ Example</link>
        <link xlink:href="3675f641-b4b1-48ff-ba33-8d9ea064cd04">Jscript Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
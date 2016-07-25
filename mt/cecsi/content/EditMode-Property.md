---
title: "EditMode Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a1b04bb2-8c8b-47f9-8477-bfd0368b6f68
caps.latest.revision: 12
caps.handback.revision: 12
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
# EditMode Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="612102003b35a67262ce2eab71e84bd6" id="tgt1" class="tgtSentence">Indicates the editing status of the current record.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e5943bf3ed257c36c720a0a36cdc99a8" id="tgt3" class="tgtSentence">Returns an <legacyLink xlink:href="45d54b6e-db2c-4553-9fd0-528147d6da2f">EditModeEnum</legacyLink> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="332080f9b83c3db0e4eeb3e5f307f547" id="tgt4" class="tgtSentence">ADO maintains an editing buffer associated with the current record.</caps:sentence>
            <caps:sentence sentenceid="811634a6fecd2644196ca3542b5553ce" id="tgt5" class="tgtSentence"> This property indicates whether changes have been made to this buffer, or whether a new record has been created.</caps:sentence>
            <caps:sentence sentenceid="8eab3b2fe511da8c961b7472e0952862" id="tgt6" class="tgtSentence"> Use the <legacyBold>EditMode</legacyBold> property to determine the editing status of the current record.</caps:sentence>
            <caps:sentence sentenceid="13b1ae23828e37e692e15ed01ad905b6" id="tgt7" class="tgtSentence"> You can test for pending changes if an editing process has been interrupted and determine whether you need to use the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> or <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="16fd08f5467ce8aa7ffad111183844ed" id="tgt8" class="tgtSentence">In <legacyItalic>immediate update mode</legacyItalic> the <legacyBold>EditMode</legacyBold> property is reset to <legacyBold>adEditNone</legacyBold> after a successful call to the <legacyBold>Update</legacyBold> method is called.</caps:sentence>
            <caps:sentence sentenceid="3bc1b148976db4dbe52d1130513bf1df" id="tgt9" class="tgtSentence"> When a call to <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink> does not successfully delete the record or records in the data source (for example, because of referential integrity violations), the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> remains in edit mode (<legacyBold>EditMode</legacyBold> = <legacyBold>adEditInProgress</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="8ee98579c7deef4a70eda080ffb3f16e" id="tgt10" class="tgtSentence"> Therefore, <legacyBold>CancelUpdate</legacyBold> must be called before moving off the current record (for example with <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>, or <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> ).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="574d98f4b15766a748036616faf0d487" id="tgt11" class="tgtSentence">In <legacyItalic>batch update mode</legacyItalic> (in which the provider caches multiple changes and writes them to the underlying data source only when you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method), the value of the <legacyBold>EditMode</legacyBold> property is changed when the first operation is performed and it is not reset by a call to the <legacyBold>Update</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="3b7ad0afe07dec5496ed701d5ed97c4e" id="tgt12" class="tgtSentence"> Subsequent operations do not change the value of the <legacyBold>EditMode</legacyBold> property, even if different operations are performed.</caps:sentence>
            <caps:sentence sentenceid="cc37fe2616ea2d81caa85079a84c7e6b" id="tgt13" class="tgtSentence"> For example, if the first operation is to add a new record, and the second makes changes to an existing record, the property of <legacyBold>EditMode</legacyBold> will still be <legacyBold>adEditAdd</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="0c17a4dba06d30f771d6482a932c1ae0" id="tgt14" class="tgtSentence"> The <legacyBold>EditMode</legacyBold> property is not reset to <legacyBold>adEditNone</legacyBold> until after the call to <legacyBold>UpdateBatch</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="f0a37920b8e52d17f30cd829b567b559" id="tgt15" class="tgtSentence"> To determine what operations have been performed, set the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property to <legacyLink xlink:href="b22e725e-84bd-4286-a070-290c278c3783">adFilterPending</legacyLink> so that only records with pending changes will be visible and examine the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property of each record to determine what changes have been made to the data.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="957cfc884660db3a588c0babb2a538e7" id="tgt16" class="tgtSentence">  <legacyBold>EditMode</legacyBold> can return a valid value only if there is a current record.</caps:sentence>
              <caps:sentence sentenceid="d5c2df27c196e7c909ca60fa62fed05b" id="tgt17" class="tgtSentence">
                <legacyBold>EditMode</legacyBold> will return an error if <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF or EOF</legacyLink> is true, or if the current record has been deleted.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt18" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object (ADO)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2cb4a304-f40a-4897-8b93-82c2d8e93500">Visual Basic Example</link>
        <link xlink:href="b2a80e44-03d8-426e-81b6-dd9dfc30e181">Visual C++ Example</link>
        <link xlink:href="c222016e-415d-485e-86c5-e29feac4297a">Visual J++ Example</link>
        <link xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew Method</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the editing status of the current record.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns an <legacyLink xlink:href="45d54b6e-db2c-4553-9fd0-528147d6da2f">EditModeEnum</legacyLink> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">ADO maintains an editing buffer associated with the current record.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This property indicates whether changes have been made to this buffer, or whether a new record has been created.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Use the <legacyBold>EditMode</legacyBold> property to determine the editing status of the current record.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> You can test for pending changes if an editing process has been interrupted and determine whether you need to use the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> or <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">In <legacyItalic>immediate update mode</legacyItalic> the <legacyBold>EditMode</legacyBold> property is reset to <legacyBold>adEditNone</legacyBold> after a successful call to the <legacyBold>Update</legacyBold> method is called.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> When a call to <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink> does not successfully delete the record or records in the data source (for example, because of referential integrity violations), the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> remains in edit mode (<legacyBold>EditMode</legacyBold> = <legacyBold>adEditInProgress</legacyBold>).</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Therefore, <legacyBold>CancelUpdate</legacyBold> must be called before moving off the current record (for example with <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>, or <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> ).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">In <legacyItalic>batch update mode</legacyItalic> (in which the provider caches multiple changes and writes them to the underlying data source only when you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method), the value of the <legacyBold>EditMode</legacyBold> property is changed when the first operation is performed and it is not reset by a call to the <legacyBold>Update</legacyBold> method.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Subsequent operations do not change the value of the <legacyBold>EditMode</legacyBold> property, even if different operations are performed.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> For example, if the first operation is to add a new record, and the second makes changes to an existing record, the property of <legacyBold>EditMode</legacyBold> will still be <legacyBold>adEditAdd</legacyBold>.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The <legacyBold>EditMode</legacyBold> property is not reset to <legacyBold>adEditNone</legacyBold> until after the call to <legacyBold>UpdateBatch</legacyBold>.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> To determine what operations have been performed, set the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property to <legacyLink xlink:href="b22e725e-84bd-4286-a070-290c278c3783">adFilterPending</legacyLink> so that only records with pending changes will be visible and examine the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property of each record to determine what changes have been made to the data.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src16" class="srcSentence">  <legacyBold>EditMode</legacyBold> can return a valid value only if there is a current record.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence">
                <legacyBold>EditMode</legacyBold> will return an error if <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF or EOF</legacyLink> is true, or if the current record has been deleted.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src18" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object (ADO)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2cb4a304-f40a-4897-8b93-82c2d8e93500">Visual Basic Example</link>
        <link xlink:href="b2a80e44-03d8-426e-81b6-dd9dfc30e181">Visual C++ Example</link>
        <link xlink:href="c222016e-415d-485e-86c5-e29feac4297a">Visual J++ Example</link>
        <link xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew Method</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
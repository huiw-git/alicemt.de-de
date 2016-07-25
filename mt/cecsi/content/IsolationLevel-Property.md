---
title: "IsolationLevel Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ea84e4b2-fbf2-4eef-b9ce-796b22e21800
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
# IsolationLevel Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="94402e6c2c496f3b2aebdf40c5974c8e" id="tgt1" class="tgtSentence">Indicates the level of isolation for a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="eb37d770d688961242513d982b21e97f" id="tgt3" class="tgtSentence">Sets or returns an <legacyLink xlink:href="8e17a7bc-b8a3-4ae2-b6c9-ce088ad31fdf">IsolationLevelEnum</legacyLink> value.</caps:sentence>
            <caps:sentence sentenceid="c1a13e4e5c71718815645bcb3d3c1d4b" id="tgt4" class="tgtSentence"> The default is <legacyBold>adXactReadCommitted</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="758b6249b35978d24c51778935e022b5" id="tgt5" class="tgtSentence">Use the <legacyBold>IsolationLevel</legacyBold> property to set the isolation level of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="f1eb267b0b438ca140725e2f74957737" id="tgt6" class="tgtSentence"> The setting does not take effect until the next time you call the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="5ce542422fcddbd330922c2a3e70c1a0" id="tgt7" class="tgtSentence"> If the level of isolation you request is unavailable, the provider may return the next greater level of isolation without updating the <legacyBold>IsolationLevel</legacyBold> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d79b7fec90fe2a4174dfb49b8605493d" id="tgt8" class="tgtSentence">The <legacyBold>IsolationLevel</legacyBold> property is read/write.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="b75fa0918d862c26375568af3e05d933" id="tgt9" class="tgtSentence">
                <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Connection</legacyBold> object, the <legacyBold>IsolationLevel</legacyBold> property can be set only to <legacyBold>adXactUnspecified</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="191f036aaab3485e93920909a099b091" id="tgt10" class="tgtSentence"> Because users are working with disconnected <legacyBold>Recordset</legacyBold> objects on a client-side cache, there may be multiuser issues.</caps:sentence>
              <caps:sentence sentenceid="834c74e6b057175f5af68c7247ca5e90" id="tgt11" class="tgtSentence"> For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win."</caps:sentence>
              <caps:sentence sentenceid="a2833a9cb85237195168ff35ca659339" id="tgt12" class="tgtSentence"> The second user's update request will fail with an error.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt13" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3382fd41-0aa1-4091-97d3-624403111e07">Visual Basic Example</link>
        <link xlink:href="92ddec5d-e3dc-4e8e-997a-c5417cceab69">Visual C++ Example</link>
        <link xlink:href="7662d89a-c5f9-44db-8c93-606db48cdd96">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the level of isolation for a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns an <legacyLink xlink:href="8e17a7bc-b8a3-4ae2-b6c9-ce088ad31fdf">IsolationLevelEnum</legacyLink> value.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default is <legacyBold>adXactReadCommitted</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>IsolationLevel</legacyBold> property to set the isolation level of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The setting does not take effect until the next time you call the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans</legacyLink> method.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If the level of isolation you request is unavailable, the provider may return the next greater level of isolation without updating the <legacyBold>IsolationLevel</legacyBold> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <legacyBold>IsolationLevel</legacyBold> property is read/write.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src9" class="srcSentence">
                <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Connection</legacyBold> object, the <legacyBold>IsolationLevel</legacyBold> property can be set only to <legacyBold>adXactUnspecified</legacyBold>.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> Because users are working with disconnected <legacyBold>Recordset</legacyBold> objects on a client-side cache, there may be multiuser issues.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win."</caps:sentence>
              <caps:sentence id="src12" class="srcSentence"> The second user's update request will fail with an error.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3382fd41-0aa1-4091-97d3-624403111e07">Visual Basic Example</link>
        <link xlink:href="92ddec5d-e3dc-4e8e-997a-c5417cceab69">Visual C++ Example</link>
        <link xlink:href="7662d89a-c5f9-44db-8c93-606db48cdd96">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "LockType Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 9920c14e-033a-4de1-8149-0ce9737a3246
caps.latest.revision: 11
caps.handback.revision: 11
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
# LockType Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="49a8f320a51a4192ec52cce2223aee72" id="tgt1" class="tgtSentence">Indicates the type of locks placed on records during editing.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a1ed2537ec2a79ff5d826a1e8a6ff113" id="tgt3" class="tgtSentence">Sets or returns a <legacyLink xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</legacyLink> value.</caps:sentence>
            <caps:sentence sentenceid="a26c9e32289b077755bd0b340d0557d8" id="tgt4" class="tgtSentence"> The default value is <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="a59963c1e2e370f57ce1dde4d3155448" id="tgt5" class="tgtSentence">Set the <legacyBold>LockType</legacyBold> property before opening a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to specify what type of locking the provider should use when opening it.</caps:sentence>
            <caps:sentence sentenceid="1d326d701a2acb3a589e54fc01c36f78" id="tgt6" class="tgtSentence"> Read the property to return the type of locking in use on an open <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="61d96a96cfb434f25832681c9de600fe" id="tgt7" class="tgtSentence">Providers may not support all lock types.</caps:sentence>
            <caps:sentence sentenceid="8940e372a25502dc4c78273411641a85" id="tgt8" class="tgtSentence"> If a provider cannot support the requested <legacyBold>LockType</legacyBold> setting, it will substitute another type of locking.</caps:sentence>
            <caps:sentence sentenceid="1f539ebd4569bd5f952fafccaaeb5feb" id="tgt9" class="tgtSentence"> To determine the actual locking functionality available in a <legacyBold>Recordset</legacyBold> object, use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method with <legacyBold>adUpdate</legacyBold> and <legacyBold>adUpdateBatch</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8438dc2501806b830b5e24e0865eb8ea" id="tgt10" class="tgtSentence">The <legacyBold>adLockPessimistic</legacyBold> setting is not supported if the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="e5cc931847e5aab67971523aa02fb639" id="tgt11" class="tgtSentence"> If an unsupported value is set, then no error will result; the closest supported <legacyBold>LockType</legacyBold> will be used instead.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="84ac8b5517df2dcb99d97041f98fdd07" id="tgt12" class="tgtSentence">The <legacyBold>LockType</legacyBold> property is read/write when the <legacyBold>Recordset</legacyBold> is closed and read-only when it is open.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="006c8fe4c164cb09fbd5837ea137877d" id="tgt13" class="tgtSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> object, the <legacyBold>LockType</legacyBold> property can only be set to <legacyBold>adLockBatchOptimistic</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
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
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the type of locks placed on records during editing.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyLink xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</legacyLink> value.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Set the <legacyBold>LockType</legacyBold> property before opening a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to specify what type of locking the provider should use when opening it.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Read the property to return the type of locking in use on an open <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">Providers may not support all lock types.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> If a provider cannot support the requested <legacyBold>LockType</legacyBold> setting, it will substitute another type of locking.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> To determine the actual locking functionality available in a <legacyBold>Recordset</legacyBold> object, use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method with <legacyBold>adUpdate</legacyBold> and <legacyBold>adUpdateBatch</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">The <legacyBold>adLockPessimistic</legacyBold> setting is not supported if the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> If an unsupported value is set, then no error will result; the closest supported <legacyBold>LockType</legacyBold> will be used instead.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">The <legacyBold>LockType</legacyBold> property is read/write when the <legacyBold>Recordset</legacyBold> is closed and read-only when it is open.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> object, the <legacyBold>LockType</legacyBold> property can only be set to <legacyBold>adLockBatchOptimistic</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
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
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
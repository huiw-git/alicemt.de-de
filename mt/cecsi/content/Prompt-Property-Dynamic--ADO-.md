---
title: "Prompt Property-Dynamic (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: c4f001b5-8d16-4d39-a42e-c0e2faaaceaf
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
# Prompt Property-Dynamic (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c28aee0644e7b026feaf244a74e5e07b" id="tgt1" class="tgtSentence">Specifies whether the OLE DB provider should prompt the user for initialization information.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="3a4c5a6ca8951123af563b4af380f428" id="tgt3" class="tgtSentence">Sets and returns a <legacyLink xlink:href="21026e24-62b7-4cc9-8aef-62c1fc6cba75">ConnectPromptEnum</legacyLink> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="a29f22c9e7f5dba20eb5a1002f7eff02" id="tgt4" class="tgtSentence">
              <legacyBold>Prompt</legacyBold> is a dynamic property, which may be appended to the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection by the OLE DB provider.</caps:sentence>
            <caps:sentence sentenceid="7b1db80e1cba1c1f59fc7b292b3d96d8" id="tgt5" class="tgtSentence"> To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c345508531c042008db2213404502420" id="tgt6" class="tgtSentence">Dynamic properties of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object are lost when the <legacyBold>Connection</legacyBold> is closed.</caps:sentence>
            <caps:sentence sentenceid="748b206bc04e2388dffc0dea59396d50" id="tgt7" class="tgtSentence"> The <legacyBold>Prompt</legacyBold> property must be reset before re-opening the <legacyBold>Connection</legacyBold> to use a value other than the default.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="f5386713a0ab06a976325fd6f6934a48" id="tgt8" class="tgtSentence">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box.</caps:sentence>
              <caps:sentence sentenceid="6f81ef14ca2a3a0952fc14c3eec232b4" id="tgt9" class="tgtSentence"> For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on.</caps:sentence>
              <caps:sentence sentenceid="e0b41e01cb2885b80ae0639fe4040bb5" id="tgt10" class="tgtSentence"> In these cases, the application will wait indefinitely for a response and seem to lock up.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="9366282e11c151558bdfaab4a264aa1b" id="tgt11" class="tgtSentence">Usage</caps:sentence>
        </title>
        <content>
          <code>Set cn = New Connection
cn.Provider = "SQLOLEDB"
cn.Properties("Prompt") = adPromptNever    ' do not prompt the user</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies whether the OLE DB provider should prompt the user for initialization information.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets and returns a <legacyLink xlink:href="21026e24-62b7-4cc9-8aef-62c1fc6cba75">ConnectPromptEnum</legacyLink> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">
              <legacyBold>Prompt</legacyBold> is a dynamic property, which may be appended to the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection by the OLE DB provider.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">Dynamic properties of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object are lost when the <legacyBold>Connection</legacyBold> is closed.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The <legacyBold>Prompt</legacyBold> property must be reset before re-opening the <legacyBold>Connection</legacyBold> to use a value other than the default.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src8" class="srcSentence">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> In these cases, the application will wait indefinitely for a response and seem to lock up.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Usage</caps:sentence>
        </title>
        <content>
          <code>Set cn = New Connection
cn.Provider = "SQLOLEDB"
cn.Properties("Prompt") = adPromptNever    ' do not prompt the user</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
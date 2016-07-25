---
title: "Mode Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 808661eb-0d7c-4e6d-8e40-9dc3bef3d77a
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
# Mode Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="cc8d2270daa619ccca0f315ded3b5720" id="tgt1" class="tgtSentence">Indicates the available permissions for modifying data in a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, or <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1415dd25c5640a47f63e67c095354c40" id="tgt3" class="tgtSentence">Sets or returns a <legacyLink xlink:href="3792c294-5161-4538-a908-22a5fc50b85f">ConnectModeEnum</legacyLink> value.</caps:sentence>
            <caps:sentence sentenceid="e3525dd82119830499a435f74f04fb88" id="tgt4" class="tgtSentence"> The default value for a <legacyBold>Connection</legacyBold> is <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="8945f8d39d09f533225f9e5e777b38dc" id="tgt5" class="tgtSentence"> The default value for a <legacyBold>Record</legacyBold> object is <legacyBold>adModeRead</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="87db9dddad4b04cb966c20e88fc7af1d" id="tgt6" class="tgtSentence"> The default value for a <legacyBold>Stream</legacyBold> associated with an underlying source (opened with a URL as the source, or as the default <legacyBold>Stream</legacyBold> of a <legacyBold>Record</legacyBold>) is <legacyBold>adModeRead</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="fddf28d687534431580789533fba1f94" id="tgt7" class="tgtSentence"> The default value for a <legacyBold>Stream</legacyBold> not associated with an underlying source (instantiated in memory) is <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ee74c629e565413bea447c4ca53ce392" id="tgt8" class="tgtSentence">Use the <legacyBold>Mode</legacyBold> property to set or return the access permissions in use by the provider on the current connection.</caps:sentence>
            <caps:sentence sentenceid="ec6b29357b4b2a8ae914ace90e461733" id="tgt9" class="tgtSentence"> You can set the <legacyBold>Mode</legacyBold> property only when the <legacyBold>Connection</legacyBold> object is closed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7a9d8f407b0c426db8691a89f00efc79" id="tgt10" class="tgtSentence">For a <legacyBold>Stream</legacyBold> object, if the access mode is not specified, it is inherited from the source used to open the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="672913a747f94004c858dbd88f8294d8" id="tgt11" class="tgtSentence"> For example, if a <legacyBold>Stream</legacyBold> is opened from a <legacyBold>Record</legacyBold> object, by default it is opened in the same mode as the <legacyBold>Record</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c2c83331fa300fc57deeade8865abaa3" id="tgt12" class="tgtSentence">This property is read/write while the object is closed and read-only while the object is open.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="a1ad9de07ce90c895da5deb92630f3ee" id="tgt13" class="tgtSentence">
                <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Connection</legacyBold> object, the <legacyBold>Mode</legacyBold> property can only be set to <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
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
          <caps:sentence id="src1" class="srcSentence">Indicates the available permissions for modifying data in a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, or <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyLink xlink:href="3792c294-5161-4538-a908-22a5fc50b85f">ConnectModeEnum</legacyLink> value.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value for a <legacyBold>Connection</legacyBold> is <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The default value for a <legacyBold>Record</legacyBold> object is <legacyBold>adModeRead</legacyBold>.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The default value for a <legacyBold>Stream</legacyBold> associated with an underlying source (opened with a URL as the source, or as the default <legacyBold>Stream</legacyBold> of a <legacyBold>Record</legacyBold>) is <legacyBold>adModeRead</legacyBold>.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The default value for a <legacyBold>Stream</legacyBold> not associated with an underlying source (instantiated in memory) is <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">Use the <legacyBold>Mode</legacyBold> property to set or return the access permissions in use by the provider on the current connection.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> You can set the <legacyBold>Mode</legacyBold> property only when the <legacyBold>Connection</legacyBold> object is closed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">For a <legacyBold>Stream</legacyBold> object, if the access mode is not specified, it is inherited from the source used to open the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> For example, if a <legacyBold>Stream</legacyBold> is opened from a <legacyBold>Record</legacyBold> object, by default it is opened in the same mode as the <legacyBold>Record</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">This property is read/write while the object is closed and read-only while the object is open.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence">
                <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Connection</legacyBold> object, the <legacyBold>Mode</legacyBold> property can only be set to <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
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
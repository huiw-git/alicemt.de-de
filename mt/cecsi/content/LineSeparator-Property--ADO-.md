---
title: "LineSeparator Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 0b20fbb8-6b83-48ec-b442-f96c8a4bafbb
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
# LineSeparator Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="21656e49d6f6b923d6c46838f2e8a260" id="tgt1" class="tgtSentence">Indicates the binary character to be used as the line separator in text <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d8f2fdac48a0446d37fbcc9f56faca88" id="tgt3" class="tgtSentence">Sets or returns a <legacyLink xlink:href="0440b793-99c7-49a2-b3e2-ec5b1a7e3e60">LineSeparatorsEnum</legacyLink> value that indicates the line separator character used in the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="f9c9cd2a647f6ad0302555d40b46c098" id="tgt4" class="tgtSentence"> The default value is <legacyBold>adCRLF</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9c615e65d9af90b1e877e0fd0d709209" id="tgt5" class="tgtSentence">
              <unmanagedCodeEntityReference>LineSeparator</unmanagedCodeEntityReference> is used to interpret lines when reading the content of a text <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="8304531af403efe45bc8878febe61055" id="tgt6" class="tgtSentence"> Lines can be skipped with the <legacyLink xlink:href="0abc00fe-ee09-4c8e-b1f2-48ee9c5f3329">SkipLine</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a60c1e0d6a3a3a2a0c2b8a84cda88738" id="tgt7" class="tgtSentence">
              <unmanagedCodeEntityReference>LineSeparator</unmanagedCodeEntityReference> is used only with text <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> objects (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="a59a78d99cf53770ec7f0fc575820095" id="tgt8" class="tgtSentence"> This property is ignored if <unmanagedCodeEntityReference>Type</unmanagedCodeEntityReference> is <legacyBold>adTypeBinary</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the binary character to be used as the line separator in text <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyLink xlink:href="0440b793-99c7-49a2-b3e2-ec5b1a7e3e60">LineSeparatorsEnum</legacyLink> value that indicates the line separator character used in the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>adCRLF</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">
              <unmanagedCodeEntityReference>LineSeparator</unmanagedCodeEntityReference> is used to interpret lines when reading the content of a text <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Lines can be skipped with the <legacyLink xlink:href="0abc00fe-ee09-4c8e-b1f2-48ee9c5f3329">SkipLine</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">
              <unmanagedCodeEntityReference>LineSeparator</unmanagedCodeEntityReference> is used only with text <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> objects (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> This property is ignored if <unmanagedCodeEntityReference>Type</unmanagedCodeEntityReference> is <legacyBold>adTypeBinary</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
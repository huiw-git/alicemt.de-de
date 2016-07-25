---
title: "State Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 06d480ca-9eb6-4570-a45d-a73539bddd32
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
# State Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="262f0bf574464f40e0f1828aa5025d95" id="tgt1" class="tgtSentence">Indicates the current state of the cellset.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4c0fad3425696399b9f267f11040a9f5" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> integer indicating the current condition of the <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object and is read-only.</caps:sentence>
            <caps:sentence sentenceid="09ecad635d6cf76c849c97fd8ea77baf" id="tgt4" class="tgtSentence"> The following values are valid: <legacyBold>adStateClosed</legacyBold> (0) and <legacyBold>adStateOpen</legacyBold> (1).</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="6a0edff8f9cebe4a881bfd678f92444a" id="tgt5" class="tgtSentence">To use the <legacyLink xlink:href="32746558-097b-4749-989e-519aadf7e3f4">ObjectStateEnum</legacyLink> constant names, you must have the ADO type library referenced in your project.</caps:sentence>
            <caps:sentence sentenceid="6620faf0fde07f2193a58a15a74657da" id="tgt6" class="tgtSentence"> See <legacyLink xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</legacyLink> for more information.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a3aa594d-f9d4-4654-8625-ec20153ff5d9">Close Method</link>
        <link xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the current state of the cellset.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> integer indicating the current condition of the <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object and is read-only.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The following values are valid: <legacyBold>adStateClosed</legacyBold> (0) and <legacyBold>adStateOpen</legacyBold> (1).</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">To use the <legacyLink xlink:href="32746558-097b-4749-989e-519aadf7e3f4">ObjectStateEnum</legacyLink> constant names, you must have the ADO type library referenced in your project.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> See <legacyLink xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</legacyLink> for more information.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a3aa594d-f9d4-4654-8625-ec20153ff5d9">Close Method</link>
        <link xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Size Property (ADO Stream)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a487c241-d953-4c31-ae7e-6358d5cf6733
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
# Size Property (ADO Stream)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="91c813cb52f94ff8ba5ee51cfe64baea" id="tgt1" class="tgtSentence">Indicates the size of the stream in number of bytes.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ef8f52364764ffaba6e9bf07bef22fd1" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> value that specifies the size of the stream in number of bytes.</caps:sentence>
            <caps:sentence sentenceid="8aaaac4bf7be0f90c97dde56b1907c44" id="tgt4" class="tgtSentence"> The default value is the size of the stream, or -1 if the size of the stream is not known.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="3a92a0021b4fe0305308d863546c5cbd" id="tgt5" class="tgtSentence">
              <legacyBold>Size</legacyBold> can be used only with open <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d7a8e4c736436046a1b5697baddd0b68" id="tgt6" class="tgtSentence">Any number of bits can be stored in a <legacyBold>Stream</legacyBold> object, limited only by system resources.</caps:sentence>
              <caps:sentence sentenceid="59fc3b0a1a9a9e9309d34a08bac2f333" id="tgt7" class="tgtSentence"> If the <legacyBold>Stream</legacyBold> contains more bits than can be represented by a <legacyBold>Long</legacyBold> value, <legacyBold>Size</legacyBold> is truncated and therefore does not accurately represent the length of the <legacyBold>Stream</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the size of the stream in number of bytes.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> value that specifies the size of the stream in number of bytes.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is the size of the stream, or -1 if the size of the stream is not known.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">
              <legacyBold>Size</legacyBold> can be used only with open <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src6" class="srcSentence">Any number of bits can be stored in a <legacyBold>Stream</legacyBold> object, limited only by system resources.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence"> If the <legacyBold>Stream</legacyBold> contains more bits than can be represented by a <legacyBold>Long</legacyBold> value, <legacyBold>Size</legacyBold> is truncated and therefore does not accurately represent the length of the <legacyBold>Stream</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
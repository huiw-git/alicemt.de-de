---
title: "Position Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d
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
# Position Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b108eb3763d72c3c4bfb053978a25434" id="tgt1" class="tgtSentence">Indicates the current position within a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b59a6f8163d8f8e111f7998b4532e7ce" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that specifies the offset, in number of bytes, of the current position from the beginning of the stream.</caps:sentence>
            <caps:sentence sentenceid="5985e1b8e640bfb1b5ce93762689077d" id="tgt4" class="tgtSentence"> The default is 0, which represents the first byte in the stream.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="52f6e8a2ed6f25df2e17102ec0b7215f" id="tgt5" class="tgtSentence">The current position can be moved to a point after the end of the stream.</caps:sentence>
            <caps:sentence sentenceid="a5e808c3d1459f019538cf977fb9b84d" id="tgt6" class="tgtSentence"> If you specify the current position beyond the end of the stream, the <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> of the <legacyBold>Stream</legacyBold> object will be increased accordingly.</caps:sentence>
            <caps:sentence sentenceid="e43a7c1498fcb2c3bc2ce9245811efac" id="tgt7" class="tgtSentence"> Any new bytes added in this way will be null.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="6b91bb109e96347d798491cf835aa6a4" id="tgt8" class="tgtSentence">  <legacyBold>Position</legacyBold> always measures bytes.</caps:sentence>
              <caps:sentence sentenceid="c878847c74abdec272a0169330df8da3" id="tgt9" class="tgtSentence"> For text streams using multibyte character sets, multiply the position by the character size to determine the character number.</caps:sentence>
              <caps:sentence sentenceid="442f48db7b2147852e04dcca3dc5187b" id="tgt10" class="tgtSentence"> For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="c8f674d84a1a980ca38947dcca859efa" id="tgt11" class="tgtSentence">Negative values cannot be used to change the current position in a <legacyBold>Stream</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="7ace71d9f689d0b80a3b372e37594c3a" id="tgt12" class="tgtSentence"> Only positive numbers can be used for <legacyBold>Position</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="cc1a10a687ea195043f330541f4a8754" id="tgt13" class="tgtSentence">For read-only <legacyBold>Stream</legacyBold> objects, ADO will not return an error if <legacyBold>Position</legacyBold> is set to a value greater than the <legacyBold>Size</legacyBold> of the <legacyBold>Stream</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="3a41d1b4ef3f73613828bae6de31eb71" id="tgt14" class="tgtSentence"> This does not change the size of the <legacyBold>Stream</legacyBold>, or alter the <legacyBold>Stream</legacyBold> contents in any way.</caps:sentence>
              <caps:sentence sentenceid="f8411ed542efe2232ecd3c959edc5631" id="tgt15" class="tgtSentence"> However, doing this should be avoided because it results in a meaningless <legacyBold>Position</legacyBold> value.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt16" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e42507cb-9b46-4ce4-8191-2948eaf14ca2">Charset Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the current position within a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that specifies the offset, in number of bytes, of the current position from the beginning of the stream.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default is 0, which represents the first byte in the stream.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The current position can be moved to a point after the end of the stream.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> If you specify the current position beyond the end of the stream, the <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> of the <legacyBold>Stream</legacyBold> object will be increased accordingly.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Any new bytes added in this way will be null.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src8" class="srcSentence">  <legacyBold>Position</legacyBold> always measures bytes.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> For text streams using multibyte character sets, multiply the position by the character size to determine the character number.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src11" class="srcSentence">Negative values cannot be used to change the current position in a <legacyBold>Stream</legacyBold>.</caps:sentence>
              <caps:sentence id="src12" class="srcSentence"> Only positive numbers can be used for <legacyBold>Position</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence">For read-only <legacyBold>Stream</legacyBold> objects, ADO will not return an error if <legacyBold>Position</legacyBold> is set to a value greater than the <legacyBold>Size</legacyBold> of the <legacyBold>Stream</legacyBold>.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> This does not change the size of the <legacyBold>Stream</legacyBold>, or alter the <legacyBold>Stream</legacyBold> contents in any way.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> However, doing this should be avoided because it results in a meaningless <legacyBold>Position</legacyBold> value.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e42507cb-9b46-4ce4-8191-2948eaf14ca2">Charset Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
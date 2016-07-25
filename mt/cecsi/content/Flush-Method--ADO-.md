---
title: "Flush Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 938522b4-f836-4c80-8d27-a598a000f0ee
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
# Flush Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b7b2dbfc580de306e166bb9ea6740158" id="tgt1" class="tgtSentence">Forces the contents of the <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> remaining in the ADO buffer to the underlying object with which the <legacyBold>Stream</legacyBold> is associated.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.Flush</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="c842a6ce8674f7c9496ce0b2ae3f5093" id="tgt2" class="tgtSentence">This method can be used to send the contents of the stream buffer to the underlying object: for example, the node or file represented by the URL that is the source of the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="732ddb0424e5270935f127185c6d0979" id="tgt3" class="tgtSentence"> This method should be called when you want to ensure that all changes that were made to the contents of a <legacyBold>Stream</legacyBold> have been written.</caps:sentence>
            <caps:sentence sentenceid="7092a351ddb73037ad5812695004428a" id="tgt4" class="tgtSentence"> However, with ADO it is not usually necessary to call <legacyBold>Flush</legacyBold>, as ADO continuously flushes its buffer as much as possible in the background.</caps:sentence>
            <caps:sentence sentenceid="97738c55390e5c0f7fa0d26054f54138" id="tgt5" class="tgtSentence"> Changes to the content of a <legacyBold>Stream</legacyBold> are made automatically, not cached until <legacyBold>Flush</legacyBold> is called.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8be63f44a137f02a77cef9525e2e31ec" id="tgt6" class="tgtSentence">Closing a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method flushes the contents of a <legacyBold>Stream</legacyBold> automatically; there is no need to explicitly call <legacyBold>Flush</legacyBold> immediately before <legacyBold>Close</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Forces the contents of the <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> remaining in the ADO buffer to the underlying object with which the <legacyBold>Stream</legacyBold> is associated.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.Flush</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">This method can be used to send the contents of the stream buffer to the underlying object: for example, the node or file represented by the URL that is the source of the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> This method should be called when you want to ensure that all changes that were made to the contents of a <legacyBold>Stream</legacyBold> have been written.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> However, with ADO it is not usually necessary to call <legacyBold>Flush</legacyBold>, as ADO continuously flushes its buffer as much as possible in the background.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Changes to the content of a <legacyBold>Stream</legacyBold> are made automatically, not cached until <legacyBold>Flush</legacyBold> is called.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">Closing a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method flushes the contents of a <legacyBold>Stream</legacyBold> automatically; there is no need to explicitly call <legacyBold>Flush</legacyBold> immediately before <legacyBold>Close</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
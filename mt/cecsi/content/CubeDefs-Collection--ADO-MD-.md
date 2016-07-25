---
title: "CubeDefs Collection (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: c79a5e36-71fd-44c4-948d-d6a7a89bb3b5
caps.latest.revision: 9
caps.handback.revision: 9
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
# CubeDefs Collection (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="cdd57c90c13ec75dece88a83f8a91754" id="tgt1" class="tgtSentence">Contains the <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> objects that represent a cube from a multidimensional catalog.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ec6b100716e56ae7d46fb5cb4f454062" id="tgt2" class="tgtSentence">
              <legacyBold>CubeDefs</legacyBold> is a standard ADO collection.</caps:sentence>
            <caps:sentence sentenceid="aa7ab60c38131526d7cc907ae21f8cf8" id="tgt3" class="tgtSentence"> With the properties and methods of a collection, you can do the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="119df3e27fc24c7b7e2ba67302fea726" id="tgt4" class="tgtSentence">Obtain the number of objects in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="91b3fcecbf61504098c6ca4a08390a91" id="tgt5" class="tgtSentence">Return an object from the collection with the default <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b855e706ff56cde78c100799a071e811" id="tgt6" class="tgtSentence">Update the objects in the collection from the provider with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt7" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="a25442b8be48f10ec303ae580bc72f3b" id="tgt8" class="tgtSentence">
                  <legacyLink xlink:href="bf2d1108-ba3c-4830-9c49-78e833ff37b1">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="3aae1107-2f81-413c-8eda-ef96c3df1b8a">Visual Basic Example</link>
        <link xlink:href="11f6f896-d69c-44a4-94cd-d54c93140e4a">Catalog Object</link>
        <link xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains the <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> objects that represent a cube from a multidimensional catalog.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">
              <legacyBold>CubeDefs</legacyBold> is a standard ADO collection.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> With the properties and methods of a collection, you can do the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Obtain the number of objects in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Return an object from the collection with the default <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Update the objects in the collection from the provider with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src7" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">
                  <legacyLink xlink:href="bf2d1108-ba3c-4830-9c49-78e833ff37b1">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="3aae1107-2f81-413c-8eda-ef96c3df1b8a">Visual Basic Example</link>
        <link xlink:href="11f6f896-d69c-44a4-94cd-d54c93140e4a">Catalog Object</link>
        <link xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
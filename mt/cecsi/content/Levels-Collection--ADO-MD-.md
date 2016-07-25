---
title: "Levels Collection (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: fed8684a-b428-4ee4-8f8d-928abe4ad9ad
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
# Levels Collection (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d630f599bc300a507a3891fcf3a60d50" id="tgt1" class="tgtSentence">Contains the <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> objects that make up a hierarchy.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d30f82c05d19ee954937037af56aab11" id="tgt2" class="tgtSentence">
              <legacyBold>Levels</legacyBold> is a standard ADO collection.</caps:sentence>
            <caps:sentence sentenceid="a9b20dd574a5a7dca51e334adda499a6" id="tgt3" class="tgtSentence"> By using the properties and methods of a collection, you can do the following:</caps:sentence>
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
                <caps:sentence sentenceid="2ed0ab3174c5202c34fae380b8a5ea5b" id="tgt8" class="tgtSentence">
                  <legacyLink xlink:href="7fba3296-5bd0-4f9e-8f63-9565fe1ee15f">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="3aae1107-2f81-413c-8eda-ef96c3df1b8a">Visual Basic Example</link>
        <link xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy Object</link>
        <link xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains the <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> objects that make up a hierarchy.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">
              <legacyBold>Levels</legacyBold> is a standard ADO collection.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> By using the properties and methods of a collection, you can do the following:</caps:sentence>
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
                  <legacyLink xlink:href="7fba3296-5bd0-4f9e-8f63-9565fe1ee15f">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="3aae1107-2f81-413c-8eda-ef96c3df1b8a">Visual Basic Example</link>
        <link xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy Object</link>
        <link xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
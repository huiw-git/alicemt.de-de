---
title: "Catalog Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 11f6f896-d69c-44a4-94cd-d54c93140e4a
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
# Catalog Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f5f1a70a43bf03c804575f01e70e6740" id="tgt1" class="tgtSentence">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="6b317be400758cebed958a3029ee0c58" id="tgt2" class="tgtSentence">With the collections and properties of a <legacyBold>Catalog</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="d628a2bdcce01dd3d1bfbc44421719b5" id="tgt3" class="tgtSentence">Open the catalog by setting the <legacyLink xlink:href="2509b32c-a995-4364-9152-d8c83129bdd8">ActiveConnection</legacyLink> property to a standard ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object or to a valid connection string.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d947aa9a0f21c874ec080b36167439d3" id="tgt4" class="tgtSentence">Identify the <legacyBold>Catalog</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="55996dbd8ec198706fb1177c2a9ba73a" id="tgt5" class="tgtSentence">Iterate through the cubes in a catalog using the <legacyLink xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt6" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="4ceb8bf0c619b055449113f1f49bcadb" id="tgt7" class="tgtSentence">
                  <legacyLink xlink:href="e9566718-9122-490d-8a8e-da8f605246f2">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="3aae1107-2f81-413c-8eda-ef96c3df1b8a">Visual Basic Example</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">With the collections and properties of a <legacyBold>Catalog</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src3" class="srcSentence">Open the catalog by setting the <legacyLink xlink:href="2509b32c-a995-4364-9152-d8c83129bdd8">ActiveConnection</legacyLink> property to a standard ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object or to a valid connection string.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Identify the <legacyBold>Catalog</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Iterate through the cubes in a catalog using the <legacyLink xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src6" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">
                  <legacyLink xlink:href="e9566718-9122-490d-8a8e-da8f605246f2">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="3aae1107-2f81-413c-8eda-ef96c3df1b8a">Visual Basic Example</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
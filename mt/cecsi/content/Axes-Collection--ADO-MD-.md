---
title: "Axes Collection (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 072fb21a-ec0f-4b02-9022-1cef3ad4bfff
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
# Axes Collection (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="232faa0395599ccb34ca00e5effd6a46" id="tgt1" class="tgtSentence">Contains the <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink> objects that define a cellset.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="da43c518ecd71d8ad3def0fd666bfa79" id="tgt2" class="tgtSentence">A <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object contains an <legacyBold>Axes</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="2bfac5f207f35a690a75cf451f1f6841" id="tgt3" class="tgtSentence"> Once the <legacyBold>Cellset</legacyBold> is opened, this collection will contain at least one <legacyBold>Axis</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="34ade6edcec48b884b2579781dc44bd6" id="tgt4" class="tgtSentence"> See the <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink> object for a more detailed explanation of how to use <legacyBold>Axis</legacyBold> objects.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="238d7fd7652b660e2dd2ad0dc6cadd36" id="tgt5" class="tgtSentence">The filter axis of a <legacyBold>Cellset</legacyBold> is not contained in the <legacyBold>Axes</legacyBold> collection.</caps:sentence>
              <caps:sentence sentenceid="d3b4aa160c7ca69c055f33c4ed778fba" id="tgt6" class="tgtSentence"> See the <legacyLink xlink:href="9c656963-531e-4cd1-b698-d5f42a9b7ba3">FilterAxis</legacyLink> property for more information.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="fcd7df67b097df281801aede8f31f22a" id="tgt7" class="tgtSentence">         <legacyBold>Axes</legacyBold> is a standard ADO collection.</caps:sentence>
            <caps:sentence sentenceid="aa7ab60c38131526d7cc907ae21f8cf8" id="tgt8" class="tgtSentence"> With the properties and methods of a collection, you can do the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="119df3e27fc24c7b7e2ba67302fea726" id="tgt9" class="tgtSentence">Obtain the number of objects in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="91b3fcecbf61504098c6ca4a08390a91" id="tgt10" class="tgtSentence">Return an object from the collection with the default <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b855e706ff56cde78c100799a071e811" id="tgt11" class="tgtSentence">Update the objects in the collection from the provider with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt12" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="fa0fad80a55daee4f3cb58e8e61b0716" id="tgt13" class="tgtSentence">
                  <legacyLink xlink:href="be459530-6f28-458f-ad70-759eae3ae08c">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains the <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink> objects that define a cellset.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object contains an <legacyBold>Axes</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Once the <legacyBold>Cellset</legacyBold> is opened, this collection will contain at least one <legacyBold>Axis</legacyBold>.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> See the <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink> object for a more detailed explanation of how to use <legacyBold>Axis</legacyBold> objects.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src5" class="srcSentence">The filter axis of a <legacyBold>Cellset</legacyBold> is not contained in the <legacyBold>Axes</legacyBold> collection.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> See the <legacyLink xlink:href="9c656963-531e-4cd1-b698-d5f42a9b7ba3">FilterAxis</legacyLink> property for more information.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src7" class="srcSentence">         <legacyBold>Axes</legacyBold> is a standard ADO collection.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> With the properties and methods of a collection, you can do the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Obtain the number of objects in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Return an object from the collection with the default <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Update the objects in the collection from the provider with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src12" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">
                  <legacyLink xlink:href="be459530-6f28-458f-ad70-759eae3ae08c">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
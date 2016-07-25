---
title: "Axis Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada
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
# Axis Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="52b1fb1bed4a5badda321a0ec384426a" id="tgt1" class="tgtSentence">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="c0f6810009485916ca34d350f5b242e0" id="tgt2" class="tgtSentence">An <legacyBold>Axis</legacyBold> object can be contained by an <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes</legacyLink> collection, or returned by the <legacyLink xlink:href="9c656963-531e-4cd1-b698-d5f42a9b7ba3">FilterAxis</legacyLink> property of a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fe7bb9a03f2d6c63cbc13493c84c5adc" id="tgt3" class="tgtSentence">With the collections and properties of an <legacyBold>Axis</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="d68342db03ca9febaa85d19670b70403" id="tgt4" class="tgtSentence">Identify the <legacyBold>Axis</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="67607e98897c2e103e63657e2702c2b0" id="tgt5" class="tgtSentence">Iterate through each position along an <legacyBold>Axis</legacyBold> using the <legacyLink xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b97aea7ba0a3519c67080944642e3d95" id="tgt6" class="tgtSentence">Obtain the number of dimensions on the <legacyBold>Axis</legacyBold> with the <legacyLink xlink:href="87929cbc-9c38-491a-8616-62d45c51e299">DimensionCount</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0f207d0d54e8442ddb1aaa31cd5dd713" id="tgt7" class="tgtSentence">Obtain provider-specific attributes of the <legacyBold>Axis</legacyBold> with the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt8" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f07bd815118f1787bef79cf88dd2a335" id="tgt9" class="tgtSentence">
                  <legacyLink xlink:href="89ec13b9-6324-4a95-92a7-3230d46bd02f">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b4647211-2566-4657-ae7b-3dd761457d7b">VBScript Example</link>
        <link xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes Collection</link>
        <link xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">An <legacyBold>Axis</legacyBold> object can be contained by an <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes</legacyLink> collection, or returned by the <legacyLink xlink:href="9c656963-531e-4cd1-b698-d5f42a9b7ba3">FilterAxis</legacyLink> property of a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">With the collections and properties of an <legacyBold>Axis</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Identify the <legacyBold>Axis</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Iterate through each position along an <legacyBold>Axis</legacyBold> using the <legacyLink xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Obtain the number of dimensions on the <legacyBold>Axis</legacyBold> with the <legacyLink xlink:href="87929cbc-9c38-491a-8616-62d45c51e299">DimensionCount</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Obtain provider-specific attributes of the <legacyBold>Axis</legacyBold> with the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src8" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">
                  <legacyLink xlink:href="89ec13b9-6324-4a95-92a7-3230d46bd02f">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b4647211-2566-4657-ae7b-3dd761457d7b">VBScript Example</link>
        <link xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes Collection</link>
        <link xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Position Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 91eab784-3ce9-41d6-a840-9b0939ca0608
caps.latest.revision: 8
caps.handback.revision: 8
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
# Position Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3b68e7a878976523acbde905d16c3d02" id="tgt1" class="tgtSentence">Represents a set of one or more members of different dimensions that defines a point along an axis.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b09e4dad8ca88da4459ed0cad38c23ab" id="tgt2" class="tgtSentence">With the properties and collections of a <legacyBold>Position</legacyBold> object you can do the following:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="87bccb71ed4559e77baab5b76b69762b" id="tgt3" class="tgtSentence">Use the <legacyBold>Ordinal</legacyBold> property to return the ordinal position of the <legacyBold>Position</legacyBold> along the <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1f00fd54bc787eb1ecb38bfa3e46263" id="tgt4" class="tgtSentence">Use the <legacyLink xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members</legacyLink> collection to return the members that make up the position along the <legacyBold>Axis</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt5" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="c3e824b1-30c7-4afa-9a27-213c407453e8">
                  <caps:sentence sentenceid="22ce6edfcceaf6e5d93b186cec4e2a71" id="tgt6" class="tgtSentence">Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b4647211-2566-4657-ae7b-3dd761457d7b">VBScript Example</link>
        <link xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis Object</link>
        <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object</link>
        <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
        <link xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a set of one or more members of different dimensions that defines a point along an axis.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">With the properties and collections of a <legacyBold>Position</legacyBold> object you can do the following:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src3" class="srcSentence">Use the <legacyBold>Ordinal</legacyBold> property to return the ordinal position of the <legacyBold>Position</legacyBold> along the <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Use the <legacyLink xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members</legacyLink> collection to return the members that make up the position along the <legacyBold>Axis</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src5" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="c3e824b1-30c7-4afa-9a27-213c407453e8">
                  <caps:sentence id="src6" class="srcSentence">Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b4647211-2566-4657-ae7b-3dd761457d7b">VBScript Example</link>
        <link xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis Object</link>
        <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object</link>
        <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
        <link xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
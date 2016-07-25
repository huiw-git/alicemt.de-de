---
title: "FilterAxis Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 9c656963-531e-4cd1-b698-d5f42a9b7ba3
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
# FilterAxis Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="29eb77dce767f63a035f27d9098d4ae0" id="tgt1" class="tgtSentence">Indicates filter information about the current <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">cellset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bebd68720e20d7825d20a61b7bdf9c4d" id="tgt3" class="tgtSentence">Returns an <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink> object, and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e7981414a1ba8353d5a6ed325795b335" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>FilterAxis</unmanagedCodeEntityReference> property to return information about the dimensions that were used to slice the data.</caps:sentence>
            <caps:sentence sentenceid="3620f2072bfb2402c854f73eeb5e778c" id="tgt5" class="tgtSentence"> The <legacyLink xlink:href="87929cbc-9c38-491a-8616-62d45c51e299">DimensionCount</legacyLink> property of the <unmanagedCodeEntityReference>Axis</unmanagedCodeEntityReference> returns the number of slicer dimensions.</caps:sentence>
            <caps:sentence sentenceid="b48aa97e1ff25c879cf1ee32aed638a5" id="tgt6" class="tgtSentence"> This axis usually has just one row.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ccfcddab7db3270d8db5aab1d0df823b" id="tgt7" class="tgtSentence">The <unmanagedCodeEntityReference>Axis</unmanagedCodeEntityReference> returned by <unmanagedCodeEntityReference>FilterAxis</unmanagedCodeEntityReference> is not contained in the <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes</legacyLink> collection for a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis Object</link>
        <link xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension Object</link>
        <link xlink:href="87929cbc-9c38-491a-8616-62d45c51e299">DimensionCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates filter information about the current <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">cellset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns an <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink> object, and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>FilterAxis</unmanagedCodeEntityReference> property to return information about the dimensions that were used to slice the data.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The <legacyLink xlink:href="87929cbc-9c38-491a-8616-62d45c51e299">DimensionCount</legacyLink> property of the <unmanagedCodeEntityReference>Axis</unmanagedCodeEntityReference> returns the number of slicer dimensions.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> This axis usually has just one row.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <unmanagedCodeEntityReference>Axis</unmanagedCodeEntityReference> returned by <unmanagedCodeEntityReference>FilterAxis</unmanagedCodeEntityReference> is not contained in the <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes</legacyLink> collection for a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis Object</link>
        <link xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension Object</link>
        <link xlink:href="87929cbc-9c38-491a-8616-62d45c51e299">DimensionCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
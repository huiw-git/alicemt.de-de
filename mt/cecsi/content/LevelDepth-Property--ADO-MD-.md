---
title: "LevelDepth Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8a1cfe2c-f207-4445-b152-ade090f64608
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
# LevelDepth Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bd0cdd1ef1630ecca60d418e1a1175dc" id="tgt1" class="tgtSentence">Indicates the number of levels between the root of the hierarchy and a <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">member</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d9bea579e731ab4d61667ce884491f1c" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> integer, and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="63852bd5e6af6e878af75a86094b1a60" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>LevelDepth</unmanagedCodeEntityReference> property to determine the distance of the <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink>object from the root level of the hierarchy.</caps:sentence>
            <caps:sentence sentenceid="2935d4fceffedd771049e70de9426bd0" id="tgt5" class="tgtSentence"> The <unmanagedCodeEntityReference>LevelDepth</unmanagedCodeEntityReference><legacyBold> </legacyBold>of a member at the root level is 0.</caps:sentence>
            <caps:sentence sentenceid="e935d9b7f0a419c5c1bb2f408f5f1016" id="tgt6" class="tgtSentence"> This corresponds to the <legacyLink xlink:href="e41f2644-617d-4c09-80a4-feb5cf736186">Depth</legacyLink> property of a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e41f2644-617d-4c09-80a4-feb5cf736186">Depth Property</link>
        <link xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the number of levels between the root of the hierarchy and a <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">member</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> integer, and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>LevelDepth</unmanagedCodeEntityReference> property to determine the distance of the <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink>object from the root level of the hierarchy.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The <unmanagedCodeEntityReference>LevelDepth</unmanagedCodeEntityReference><legacyBold> </legacyBold>of a member at the root level is 0.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> This corresponds to the <legacyLink xlink:href="e41f2644-617d-4c09-80a4-feb5cf736186">Depth</legacyLink> property of a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e41f2644-617d-4c09-80a4-feb5cf736186">Depth Property</link>
        <link xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Children Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 61d36468-1ccd-467a-9cb5-17d0bfacc766
caps.latest.revision: 11
caps.handback.revision: 11
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
# Children Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6f2b105dec74381bb4ef0ab4920c008c" id="tgt1" class="tgtSentence">Returns a <legacyLink xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members</legacyLink> collection for which the current <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> is the parent in the hierarchy.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="787ea0c7d91fc2ed50992bceb84c5b3f" id="tgt3" class="tgtSentence">Returns a <legacyBold>Members</legacyBold> collection and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="387d1ee87b469c78f79909c937c953af" id="tgt4" class="tgtSentence">The <legacyBold>Children</legacyBold> property contains a <legacyBold>Members</legacyBold> collection for which the current <legacyBold>Member</legacyBold> is the hierarchical parent.</caps:sentence>
            <caps:sentence sentenceid="3d508f5f3c3f85ac4bc624581aa2c6da" id="tgt5" class="tgtSentence"> Leaf level <legacyBold>Member</legacyBold> objects have no child members in the <legacyBold>Members</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="2d0b35fd498515771283314bfac4ea36" id="tgt6" class="tgtSentence"> This property is only supported on <legacyBold>Member</legacyBold> objects belonging to a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="d699576f6a65cd6f7247374560951f8d" id="tgt7" class="tgtSentence"> An error occurs when this property is referenced from <legacyBold>Member</legacyBold> objects belonging to a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5463be22-ca50-43ea-9c92-468fc8eda280">ChildCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Returns a <legacyLink xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members</legacyLink> collection for which the current <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> is the parent in the hierarchy.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyBold>Members</legacyBold> collection and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <legacyBold>Children</legacyBold> property contains a <legacyBold>Members</legacyBold> collection for which the current <legacyBold>Member</legacyBold> is the hierarchical parent.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Leaf level <legacyBold>Member</legacyBold> objects have no child members in the <legacyBold>Members</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> This property is only supported on <legacyBold>Member</legacyBold> objects belonging to a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> An error occurs when this property is referenced from <legacyBold>Member</legacyBold> objects belonging to a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5463be22-ca50-43ea-9c92-468fc8eda280">ChildCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
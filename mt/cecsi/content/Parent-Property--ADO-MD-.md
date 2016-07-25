---
title: "Parent Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 32c278c1-d8e1-4bb7-9ecd-2fbfdffee34b
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
# Parent Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b53d99262bf3f609e124345ba3e04b47" id="tgt1" class="tgtSentence">Indicates the member that is the parent of the current <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">member</legacyLink> in a hierarchy.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f6febf85b37bcc90ee02feac15113ca6" id="tgt3" class="tgtSentence">Returns a <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> object and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="cacd5d108c425c7532ad374f8c15f4de" id="tgt4" class="tgtSentence">A member that is at the top level of a hierarchy (the root) has no parent.</caps:sentence>
            <caps:sentence sentenceid="7fa40cbf73b6cd3b240000adaf2c1502" id="tgt5" class="tgtSentence"> This property is supported only on <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects belonging to a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="9c3c28de9e45d33a1f63927fb3a76d73" id="tgt6" class="tgtSentence"> An error occurs when this property is referenced from <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects belonging to a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
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
        <link xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the member that is the parent of the current <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">member</legacyLink> in a hierarchy.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> object and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">A member that is at the top level of a hierarchy (the root) has no parent.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This property is supported only on <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects belonging to a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> An error occurs when this property is referenced from <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects belonging to a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
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
        <link xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "DrilledDown Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: bf39dd36-fc7a-4f6e-86c0-fa71430c0d86
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
# DrilledDown Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a99c477a8566bdf3d84d27c460f53069" id="tgt1" class="tgtSentence">Indicates whether children immediately follow the <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">member</legacyLink> on the axis.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b514e56a34a2d48ab85be4a732d244e7" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Boolean</languageKeyword> value and is read-only.</caps:sentence>
            <caps:sentence sentenceid="aac29f5177a73308f8fcfdf1e03cb73b" id="tgt4" class="tgtSentence">
              <unmanagedCodeEntityReference>DrilledDown</unmanagedCodeEntityReference> returns <languageKeyword>True</languageKeyword> if there are no child members of the current member on the axis.</caps:sentence>
            <caps:sentence sentenceid="2185ad71a420de1edf02dba8715659ee" id="tgt5" class="tgtSentence">
              <unmanagedCodeEntityReference>DrilledDown</unmanagedCodeEntityReference> returns <languageKeyword>False</languageKeyword> if the current member has one or more child members on the axis.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="fca312ab00ac6e2b285c0a3512e39060" id="tgt6" class="tgtSentence">Use the <unmanagedCodeEntityReference>DrilledDown</unmanagedCodeEntityReference> property to determine whether there is at least one child of this member on the axis immediately following this member.</caps:sentence>
            <caps:sentence sentenceid="c25f2ce67a64db983f58f1ffaffa50f3" id="tgt7" class="tgtSentence"> This information is useful when displaying the member.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="906f8e625ce544f40d9b106ab709b533" id="tgt8" class="tgtSentence">This property is only supported on <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects belonging to a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="0f374f75adba40f197f67f8389a24feb" id="tgt9" class="tgtSentence"> An error occurs when this property is referenced from <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects belonging to a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="510842e0-e8dc-4b33-9517-bd1c6df0cf3c">ParentSameAsPrev Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates whether children immediately follow the <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">member</legacyLink> on the axis.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Boolean</languageKeyword> value and is read-only.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence">
              <unmanagedCodeEntityReference>DrilledDown</unmanagedCodeEntityReference> returns <languageKeyword>True</languageKeyword> if there are no child members of the current member on the axis.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence">
              <unmanagedCodeEntityReference>DrilledDown</unmanagedCodeEntityReference> returns <languageKeyword>False</languageKeyword> if the current member has one or more child members on the axis.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Use the <unmanagedCodeEntityReference>DrilledDown</unmanagedCodeEntityReference> property to determine whether there is at least one child of this member on the axis immediately following this member.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> This information is useful when displaying the member.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">This property is only supported on <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects belonging to a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> An error occurs when this property is referenced from <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects belonging to a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="510842e0-e8dc-4b33-9517-bd1c6df0cf3c">ParentSameAsPrev Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
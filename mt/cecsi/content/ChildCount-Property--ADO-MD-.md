---
title: "ChildCount Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 5463be22-ca50-43ea-9c92-468fc8eda280
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
# ChildCount Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="404f1d363e4dbdb20851b6e7cc5b7675" id="tgt1" class="tgtSentence">Indicates the number of members for which the current <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> object is the parent in a hierarchy.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4836b9c7f8adc96baae280626f9885f1" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> integer and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="fc3ec10c2fe800a5b1f3762ba7ec3c24" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>ChildCount</unmanagedCodeEntityReference> property to return an estimate of how many children a <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> has.</caps:sentence>
            <caps:sentence sentenceid="636079680af11665f1088e5957254718" id="tgt5" class="tgtSentence"> The actual children of a <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> can be returned by the <legacyLink xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="139bd96ac946b079c6203c5d81fe5e9c" id="tgt6" class="tgtSentence">For <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects from a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object, the maximum number returned is 65536.</caps:sentence>
            <caps:sentence sentenceid="44816109fffcf7148899bc4967217cec" id="tgt7" class="tgtSentence"> If the actual number of children exceeds 65536, the value returned will still be 65536.</caps:sentence>
            <caps:sentence sentenceid="a220a53aafb631fc9a4629d0b397d7ec" id="tgt8" class="tgtSentence"> Therefore, the application should interpret a <unmanagedCodeEntityReference>ChildCount</unmanagedCodeEntityReference> of 65536 as equal to or greater than 65536 children.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="71974be9ccbaee930539f26718299ca8" id="tgt9" class="tgtSentence">For <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects from a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object, use the ADO collection <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property on the <unmanagedCodeEntityReference>Children</unmanagedCodeEntityReference> collection to determine the exact number of children.</caps:sentence>
            <caps:sentence sentenceid="a3d294edfc8e06f940b8a834303936d9" id="tgt10" class="tgtSentence"> Determining the exact number of children may be slow if the number of children in the collection is large.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt11" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children Property</link>
        <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property</link>
        <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the number of members for which the current <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> object is the parent in a hierarchy.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> integer and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>ChildCount</unmanagedCodeEntityReference> property to return an estimate of how many children a <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> has.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The actual children of a <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> can be returned by the <legacyLink xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">For <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects from a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object, the maximum number returned is 65536.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If the actual number of children exceeds 65536, the value returned will still be 65536.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Therefore, the application should interpret a <unmanagedCodeEntityReference>ChildCount</unmanagedCodeEntityReference> of 65536 as equal to or greater than 65536 children.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">For <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects from a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object, use the ADO collection <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property on the <unmanagedCodeEntityReference>Children</unmanagedCodeEntityReference> collection to determine the exact number of children.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Determining the exact number of children may be slow if the number of children in the collection is large.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children Property</link>
        <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property</link>
        <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
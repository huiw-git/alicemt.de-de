---
title: "Description Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6d626d35-0bf3-4f24-9934-ad9c9c91273a
caps.latest.revision: 10
caps.handback.revision: 10
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
# Description Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="24f675bdefab724450fd86173775ce1d" id="tgt1" class="tgtSentence">Returns a text explanation of the current object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9d294800d28d028bbd37911a03f41432" id="tgt3" class="tgtSentence">Returns a <legacyBold>String </legacyBold>and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="5457beca5c94f7b88ec54d19658d5165" id="tgt4" class="tgtSentence">For <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects, <unmanagedCodeEntityReference>Description</unmanagedCodeEntityReference> applies only to measure and formula members.</caps:sentence>
            <caps:sentence sentenceid="4ae0153c0853235ab041f39040bbf6e1" id="tgt5" class="tgtSentence">
              <unmanagedCodeEntityReference>Description</unmanagedCodeEntityReference> returns an empty string ("") for all other types of members.</caps:sentence>
            <caps:sentence sentenceid="20ebbd855203ef077f6f489e839658f8" id="tgt6" class="tgtSentence"> For more information about the various types of members, see the <legacyLink xlink:href="34698910-64b9-41d8-8531-9de12f2b1e32">Type</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e9570466633e1abb7b3acc8c3fcaf135" id="tgt7" class="tgtSentence">This property is only supported on <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects that belong to a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="9c3c28de9e45d33a1f63927fb3a76d73" id="tgt8" class="tgtSentence"> An error occurs when this property is referenced from <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects belonging to a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Returns a text explanation of the current object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyBold>String </legacyBold>and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">For <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects, <unmanagedCodeEntityReference>Description</unmanagedCodeEntityReference> applies only to measure and formula members.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence">
              <unmanagedCodeEntityReference>Description</unmanagedCodeEntityReference> returns an empty string ("") for all other types of members.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For more information about the various types of members, see the <legacyLink xlink:href="34698910-64b9-41d8-8531-9de12f2b1e32">Type</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">This property is only supported on <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects that belong to a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> An error occurs when this property is referenced from <unmanagedCodeEntityReference>Member</unmanagedCodeEntityReference> objects belonging to a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ADO API Reference"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bfd96a4b-c913-45aa-9e4c-ec86ac364f3a
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
# ADO API Reference
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0a94ccbf78c754ee4cfc1673962c5751" id="tgt1" class="tgtSentence">This section of the ADO documentation contains topics for each ADO object, collection, property, dynamic property, method, event, and enumeration.</caps:sentence>
          <caps:sentence sentenceid="eb4568c91b5a913675005f346f5ec997" id="tgt2" class="tgtSentence"> In addition, it contains a list of ADO syntax indexes to be used with Microsoft Visual C++ and Windows Foundation Classes (WFC).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="735f620a44121e99e68030e0c754d420" id="tgt3" class="tgtSentence">For more information, search for a specific topic in the index or refer to the following topics:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="2ec3c420265b2b64aa39b22b1e4ea785" id="tgt4" class="tgtSentence">             <legacyLink xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="7bb6a5d600f2311f7dfe6c22541e7595" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects and Interfaces</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="2b87197b71facc0a65fdf2af75828a2a" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="331ee1959d0eb9b4564b6a9e565fe669" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e916942c8c2e165cfcf57aad34ab47dc" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="d7b06d72-f792-4328-93a2-5006b9e2c581">ADO Dynamic Properties</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="26f2d56b30eb4e27e90a3b454f355176" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d33d28cdeba8032f0c930beda68a251d" id="tgt10" class="tgtSentence">             <legacyLink xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="70a933f2c921ec9e607b5f7db271c76d" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="c97ed131-1a93-463c-9e61-22f029b0c474">ADO Enumerated Constants</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e96ce897cf559293afe7ae6892a22536" id="tgt12" class="tgtSentence">             <legacyLink xlink:href="fad34f61-c34f-4c0b-8ce5-3b8872abfe4e">ADO Syntax Indexes</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="65123b97aaaf6a3eefce4c1842a601b4" id="tgt13" class="tgtSentence">             <legacyLink xlink:href="eb16724f-6fca-4873-b005-68626a8999b2">ADO Code Examples</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="1582e411-55ac-40f0-bd3d-9a10654e4b67">Appendix D: ADO Samples</link>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="40af6e70-2a37-480f-aadc-92095d450af7">Appendix C: Programming with ADO</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
        <link xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">What's New in ADO</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This section of the ADO documentation contains topics for each ADO object, collection, property, dynamic property, method, event, and enumeration.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> In addition, it contains a list of ADO syntax indexes to be used with Microsoft Visual C++ and Windows Foundation Classes (WFC).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">For more information, search for a specific topic in the index or refer to the following topics:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">             <legacyLink xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects and Interfaces</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="d7b06d72-f792-4328-93a2-5006b9e2c581">ADO Dynamic Properties</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">             <legacyLink xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="c97ed131-1a93-463c-9e61-22f029b0c474">ADO Enumerated Constants</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">             <legacyLink xlink:href="fad34f61-c34f-4c0b-8ce5-3b8872abfe4e">ADO Syntax Indexes</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">             <legacyLink xlink:href="eb16724f-6fca-4873-b005-68626a8999b2">ADO Code Examples</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="1582e411-55ac-40f0-bd3d-9a10654e4b67">Appendix D: ADO Samples</link>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="40af6e70-2a37-480f-aadc-92095d450af7">Appendix C: Programming with ADO</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
        <link xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">What's New in ADO</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
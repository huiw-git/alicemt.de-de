---
title: "Using ADO with Microsoft Visual C++"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 07d25fc0-4958-4e12-b616-36257ead812b
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
# Using ADO with Microsoft Visual C++
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e2bb64274c81102c6e6cc5dfb27841dd" id="tgt1" class="tgtSentence">For information about using ADO with Visual C++, see the following sections:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="672392a82c36ccdeac328f0879d2640b" id="tgt2" class="tgtSentence">             <legacyLink xlink:href="11233b96-e05c-4221-9aed-5f20944b0f1c">Visual C++ ADO Programming</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6a23db82c8d860a2d2dfa3ac14827746" id="tgt3" class="tgtSentence">             <legacyLink xlink:href="2952ece0-7217-4448-bb09-f6b64f43b7e2">Visual C++ Extensions for ADO</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5dc0c61861b0b59000440d033a95f6b7" id="tgt4" class="tgtSentence">             <legacyLink xlink:href="ff759185-df41-4507-8d12-0921894ffbd9">Using Visual C++ Extensions</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="56a08ccc2651d74d74e91dd0488a2969" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="e492d307-24cb-489c-a5b0-99cdc09b07da">Visual C++ Extensions Header</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b74ceba036c45cd43dab5c022e735f84" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">Visual C++ Extensions Example</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="d02b199e-1e52-4cc9-b118-750952ae7f63">ADO for Visual C++ Syntax Index for COM</link>
        <link xlink:href="5930ccd2-5bab-448a-b0bf-773b8a83e87c">ADO for Visual C++ Syntax Index with #import</link>
        <link xlink:href="9dfb6784-037d-4f9d-bb7f-b506b4498573">Using ADO with Microsoft Visual Basic</link>
        <link xlink:href="15542c35-3bf7-4d5f-a3b2-3a5cff286987">Using ADO with Microsoft Visual J++</link>
        <link xlink:href="76fc4d00-0c9f-422b-af5c-af6ed8fb29d8">Using ADO with Scripting Languages</link>
        <link xlink:href="2952ece0-7217-4448-bb09-f6b64f43b7e2">Visual C++ Extensions for ADO</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">For information about using ADO with Visual C++, see the following sections:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">             <legacyLink xlink:href="11233b96-e05c-4221-9aed-5f20944b0f1c">Visual C++ ADO Programming</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">             <legacyLink xlink:href="2952ece0-7217-4448-bb09-f6b64f43b7e2">Visual C++ Extensions for ADO</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">             <legacyLink xlink:href="ff759185-df41-4507-8d12-0921894ffbd9">Using Visual C++ Extensions</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="e492d307-24cb-489c-a5b0-99cdc09b07da">Visual C++ Extensions Header</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">Visual C++ Extensions Example</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="d02b199e-1e52-4cc9-b118-750952ae7f63">ADO for Visual C++ Syntax Index for COM</link>
        <link xlink:href="5930ccd2-5bab-448a-b0bf-773b8a83e87c">ADO for Visual C++ Syntax Index with #import</link>
        <link xlink:href="9dfb6784-037d-4f9d-bb7f-b506b4498573">Using ADO with Microsoft Visual Basic</link>
        <link xlink:href="15542c35-3bf7-4d5f-a3b2-3a5cff286987">Using ADO with Microsoft Visual J++</link>
        <link xlink:href="76fc4d00-0c9f-422b-af5c-af6ed8fb29d8">Using ADO with Scripting Languages</link>
        <link xlink:href="2952ece0-7217-4448-bb09-f6b64f43b7e2">Visual C++ Extensions for ADO</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
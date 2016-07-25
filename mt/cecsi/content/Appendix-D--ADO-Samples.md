---
title: "Appendix D: ADO Samples"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1582e411-55ac-40f0-bd3d-9a10654e4b67
caps.latest.revision: 13
caps.handback.revision: 13
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
# Appendix D: ADO Samples
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c8bbb454a5b2128a3b72ba5e0bd73623" id="tgt1" class="tgtSentence">The Windows SDK contains several sample applications that demonstrate the use of ADO and RDS code.</caps:sentence>
          <caps:sentence sentenceid="b872ee5fd3d7fa7d3cbb95d34c2dc7f8" id="tgt2" class="tgtSentence"> These samples are intended to help you learn how to use ADO and RDS, but are not intended to be deployed on production servers.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="2aead3271afdbccf7b6fda91c910231e" id="tgt3" class="tgtSentence">Companies, names, and data used in samples are fictitious unless otherwise noted.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="da7273ebbce3810553e0560bb36066a4" id="tgt4" class="tgtSentence"> To find the ADO samples, navigate to your Windows SDK root folder, such as C:\Program Files\Microsoft SDKs\Windows\v6.0.</caps:sentence>
          <caps:sentence sentenceid="32168b8a42ff5fbbeb6f1052a643678c" id="tgt5" class="tgtSentence"> Then navigate to the Samples\dataaccess\ADO subfolder.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a83d13f4fa0275a08c3b443e6b137b48" id="tgt6" class="tgtSentence">To get started with the ADO and RDS sample applications, open default.htm from the ADO and RDS samples folders, respectively.</caps:sentence>
          <caps:sentence sentenceid="ec68cf21542691078b81ee60f85dbe05" id="tgt7" class="tgtSentence"> These files describe each available sample application and explain how to configure and run the samples how to browse the sample source code.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="82a0c7564a23d24376d46619bbb0c146" id="tgt8" class="tgtSentence">The ADO documentation also contains code examples in multiple languages, which are included as topics within this online help.</caps:sentence>
          <caps:sentence sentenceid="0696009932bb2a3b9374cf9abb183deb" id="tgt9" class="tgtSentence"> For more information about these examples, see <legacyLink xlink:href="eb16724f-6fca-4873-b005-68626a8999b2">ADO Code Examples</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="eb16724f-6fca-4873-b005-68626a8999b2">ADO Code Examples</link>
        <link xlink:href="1152893e-b617-40f1-88b6-81e82e2234f1">ADO Code Examples in Microsoft Visual Basic</link>
        <link xlink:href="78bb9a95-7ac4-44b6-818b-d1787f952ed7">ADO Code Examples in Microsoft Visual Basic Scripting Edition</link>
        <link xlink:href="af30b764-398f-4918-aaa7-3952226cf544">ADO Code Examples in Microsoft Visual C++</link>
        <link xlink:href="d1c82f1a-cf78-4bd6-9ad4-1eb526e2c474">ADO Code Examples in Microsoft Visual J++</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
        <link xlink:href="5dd48483-858a-48c2-98ce-f2359abe1f59">Configuring RDS</link>
        <link xlink:href="40af6e70-2a37-480f-aadc-92095d450af7">Programming with ADO</link>
        <link xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">What's New in ADO</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Windows SDK contains several sample applications that demonstrate the use of ADO and RDS code.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These samples are intended to help you learn how to use ADO and RDS, but are not intended to be deployed on production servers.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src3" class="srcSentence">Companies, names, and data used in samples are fictitious unless otherwise noted.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src4" class="srcSentence"> To find the ADO samples, navigate to your Windows SDK root folder, such as C:\Program Files\Microsoft SDKs\Windows\v6.0.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Then navigate to the Samples\dataaccess\ADO subfolder.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">To get started with the ADO and RDS sample applications, open default.htm from the ADO and RDS samples folders, respectively.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> These files describe each available sample application and explain how to configure and run the samples how to browse the sample source code.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">The ADO documentation also contains code examples in multiple languages, which are included as topics within this online help.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> For more information about these examples, see <legacyLink xlink:href="eb16724f-6fca-4873-b005-68626a8999b2">ADO Code Examples</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="eb16724f-6fca-4873-b005-68626a8999b2">ADO Code Examples</link>
        <link xlink:href="1152893e-b617-40f1-88b6-81e82e2234f1">ADO Code Examples in Microsoft Visual Basic</link>
        <link xlink:href="78bb9a95-7ac4-44b6-818b-d1787f952ed7">ADO Code Examples in Microsoft Visual Basic Scripting Edition</link>
        <link xlink:href="af30b764-398f-4918-aaa7-3952226cf544">ADO Code Examples in Microsoft Visual C++</link>
        <link xlink:href="d1c82f1a-cf78-4bd6-9ad4-1eb526e2c474">ADO Code Examples in Microsoft Visual J++</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
        <link xlink:href="5dd48483-858a-48c2-98ce-f2359abe1f59">Configuring RDS</link>
        <link xlink:href="40af6e70-2a37-480f-aadc-92095d450af7">Programming with ADO</link>
        <link xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">What's New in ADO</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "RDS Fundamentals"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a676f0a7-7d17-45db-87c1-3fc78627465f
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
# RDS Fundamentals
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt1" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt2" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt3" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt4" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="dc0f3e88c93da8bdcc0559d4938f2d6f" id="tgt5" class="tgtSentence">The following topics introduce RDS.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="d311cc67-7db7-4c43-9590-d465564695e4">
                  <caps:sentence sentenceid="fb4fe4be29375956485b7040023b7c6b" id="tgt6" class="tgtSentence">Solutions for Remote Data Access</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="0bdd236b-edff-4aac-94c3-93e1465ca6c5">
                  <caps:sentence sentenceid="a5dc346b9bf6e6bec6fca47ad013aaa9" id="tgt7" class="tgtSentence">Basic RDS Programming Model</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="3e57af8d-519b-4467-a0bd-af468534cefd">
                  <caps:sentence sentenceid="6b313480d0588f59dd5f91b894908a38" id="tgt8" class="tgtSentence">RDS Programming Model in Detail</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="07ce0ef0-72f1-48f4-823d-1b65d28c0926">
                  <caps:sentence sentenceid="35683e2bdee02394050066d41498063f" id="tgt9" class="tgtSentence">RDS Programming Model with Objects</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="909f9af7-31db-4eec-ad52-650ce74dac2f">
                  <caps:sentence sentenceid="c343ccc7de9ab6fbd29e7a4d75d3357a" id="tgt10" class="tgtSentence">The RDS Object Model Summary</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d311cc67-7db7-4c43-9590-d465564695e4">Solutions for Remote Data Access</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src5" class="srcSentence">The following topics introduce RDS.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="d311cc67-7db7-4c43-9590-d465564695e4">
                  <caps:sentence id="src6" class="srcSentence">Solutions for Remote Data Access</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="0bdd236b-edff-4aac-94c3-93e1465ca6c5">
                  <caps:sentence id="src7" class="srcSentence">Basic RDS Programming Model</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="3e57af8d-519b-4467-a0bd-af468534cefd">
                  <caps:sentence id="src8" class="srcSentence">RDS Programming Model in Detail</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="07ce0ef0-72f1-48f4-823d-1b65d28c0926">
                  <caps:sentence id="src9" class="srcSentence">RDS Programming Model with Objects</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="909f9af7-31db-4eec-ad52-650ce74dac2f">
                  <caps:sentence id="src10" class="srcSentence">The RDS Object Model Summary</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d311cc67-7db7-4c43-9590-d465564695e4">Solutions for Remote Data Access</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
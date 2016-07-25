---
title: "RDS Code Examples in Visual C++"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 380264da-e6bb-418c-b4af-3c22d35644b8
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
# RDS Code Examples in Visual C++
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f5a89f8f0114f57a085dc14cda74b54a" id="tgt1" class="tgtSentence">Use the following code examples to learn how to use RDS properties when writing in Microsoft Visual C++.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <content>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="a3a4362505f29dd00933c3ddd2b474e7" id="tgt6" class="tgtSentence">Paste the entire code example, from beginning to end, into your code editor.</caps:sentence>
              <caps:sentence sentenceid="d0af02b2a7f5e8d60d6ca45d510c2f3c" id="tgt7" class="tgtSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="d046d89c-622b-48bc-9d30-f454c3e13595">
                  <caps:sentence sentenceid="5a077b4f7e4684fb6158a565bf63bf53" id="tgt8" class="tgtSentence">Handler Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="88b6d05c-d4eb-4ab1-bbe2-95d146237f94">
                  <caps:sentence sentenceid="29fa9207b5ff4c862ab4ff8c5bfafcb8" id="tgt9" class="tgtSentence">InternetTimeout Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the following code examples to learn how to use RDS properties when writing in Microsoft Visual C++.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <content>
          <alert class="note">
            <para>
              <caps:sentence id="src6" class="srcSentence">Paste the entire code example, from beginning to end, into your code editor.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="d046d89c-622b-48bc-9d30-f454c3e13595">
                  <caps:sentence id="src8" class="srcSentence">Handler Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="88b6d05c-d4eb-4ab1-bbe2-95d146237f94">
                  <caps:sentence id="src9" class="srcSentence">InternetTimeout Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
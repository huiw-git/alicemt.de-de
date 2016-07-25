---
title: "RDS Code Examples"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 59030e99-de9c-4506-a450-67dfcb6f7c00
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
# RDS Code Examples
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
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
          <caps:sentence sentenceid="34c7e15da23c04fbdeb3b07acfcc2287" id="tgt5" class="tgtSentence">Use the following code examples to learn how to use the RDS objects, methods, properties, and events.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b46d33bee7b3eb18ac259aa51166ad35" id="tgt6" class="tgtSentence">         <legacyBold>Note</legacyBold>   Paste the entire code example into your code editor.</caps:sentence>
          <caps:sentence sentenceid="d0af02b2a7f5e8d60d6ca45d510c2f3c" id="tgt7" class="tgtSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="d3c0ff66bafe061eb1abb80358250090" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="d9cb84a1-4ec2-4d41-8f92-dec2e17cde67">RDS Code Examples in Microsoft Visual Basic</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="53a49852bf5c1a9963448c27c3719991" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="22f23c30-7c21-4fe3-8e76-36cea6448819">RDS Code Examples in Microsoft Visual Basic Scripting Edition</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0b8f4de7e822fb69799a2e621bb88793" id="tgt10" class="tgtSentence">             <legacyLink xlink:href="380264da-e6bb-418c-b4af-3c22d35644b8">RDS Code Examples in Microsoft Visual C++</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="70595327061ba640e7f1a086c1347528" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="693778e0-11ed-4e8d-922b-baab25b6bc17">RDS Code Examples in Microsoft Visual J++</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
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
          <caps:sentence id="src5" class="srcSentence">Use the following code examples to learn how to use the RDS objects, methods, properties, and events.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">         <legacyBold>Note</legacyBold>   Paste the entire code example into your code editor.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="d9cb84a1-4ec2-4d41-8f92-dec2e17cde67">RDS Code Examples in Microsoft Visual Basic</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="22f23c30-7c21-4fe3-8e76-36cea6448819">RDS Code Examples in Microsoft Visual Basic Scripting Edition</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">             <legacyLink xlink:href="380264da-e6bb-418c-b4af-3c22d35644b8">RDS Code Examples in Microsoft Visual C++</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="693778e0-11ed-4e8d-922b-baab25b6bc17">RDS Code Examples in Microsoft Visual J++</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
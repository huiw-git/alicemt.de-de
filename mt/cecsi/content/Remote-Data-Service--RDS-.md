---
title: "Remote Data Service (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 63a5f26b-e7ca-47d9-a004-59eaad6052b4
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
# Remote Data Service (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6cd8ae097806e00ce911977af8ffb665" id="tgt1" class="tgtSentence">Remote Data Service (RDS) is a feature of ADO, with which you can move data from a server to a client application or Web page, manipulate the data on the client, and return updates to the server in a single round trip.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="ebfd69ac032f6a439b9ad503c98bc123" id="tgt6" class="tgtSentence">The RDS Programmer's Guide contains the following chapters:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">
                <caps:sentence sentenceid="42b36bfc7445e8efe81890cccd23786f" id="tgt7" class="tgtSentence">RDS Fundamentals</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">
                <caps:sentence sentenceid="a3f03e6170b5b6467b0b05c9e53d8795" id="tgt8" class="tgtSentence">RDS Tutorial</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">
                <caps:sentence sentenceid="06cefdc014452bd5658cfa219a96a3e0" id="tgt9" class="tgtSentence">RDS Usage and Security</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Remote Data Service (RDS) is a feature of ADO, with which you can move data from a server to a client application or Web page, manipulate the data on the client, and return updates to the server in a single round trip.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src6" class="srcSentence">The RDS Programmer's Guide contains the following chapters:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">
                <caps:sentence id="src7" class="srcSentence">RDS Fundamentals</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">
                <caps:sentence id="src8" class="srcSentence">RDS Tutorial</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">
                <caps:sentence id="src9" class="srcSentence">RDS Usage and Security</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
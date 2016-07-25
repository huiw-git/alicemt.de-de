---
title: "Using Related Technologies with RDS"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a98a7245-06a7-455c-82ef-950807b9f1e7
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
# Using Related Technologies with RDS
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt1" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="bbae8bc48f374b0eaf84bb88394c23c4" id="tgt2" class="tgtSentence">             <legacyLink xlink:href="e8b912c1-da5b-4e85-a000-1e6648a94237">Using RDS with ODBC Connection Pooling</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1e5a7f061c70b7bbd68b0474b71f9251" id="tgt3" class="tgtSentence">             <legacyLink xlink:href="3077d0b6-42d6-4f10-8e5d-42e6204f1109">Running Business Objects in Component Services</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt4" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt5" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt6" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt7" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="42bb25e869f463d6ac889508d875b2bc" id="tgt8" class="tgtSentence">Many other technologies interact with Remote Data Service or are used in its implementation.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="6fc3fe10e7274cf0f39a51c152384d5b" id="tgt9" class="tgtSentence">         <legacyBold>Internet Information Services</legacyBold>   For more information about Microsoft Internet Information Services (IIS), see the Microsoft Internet Information Services Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c79ce539edcb2585a89cf46c29668ffb" id="tgt10" class="tgtSentence">         <legacyBold>Active Server Pages</legacyBold>   For more information about Microsoft Active Server Pages (ASP), see the Microsoft Active Server Pages Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="bfa4462b0c8b1a534b1b07d9d7e1621e" id="tgt11" class="tgtSentence">         <legacyBold>Microsoft Component Services</legacyBold>   For more information about Component Services, see the Microsoft Transaction Server Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="86b3afb8a461d0247cfb0410d0e37023" id="tgt12" class="tgtSentence">         <legacyBold>Microsoft SQL Server</legacyBold>   For more information about Microsoft SQL Server, see the Microsoft SQL Server Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b58e4ad23ada1b14806b9612e5903262" id="tgt13" class="tgtSentence">         <legacyBold>Microsoft Internet Explorer</legacyBold>   For more information about Microsoft Internet Explorer, see the Microsoft Internet ExplorerWeb site and the MSDN Library and Web Workshop Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="535dfa844cb1ba206947c49ad5cf4954" id="tgt14" class="tgtSentence">         <legacyBold>Microsoft Windows NT Server/Windows 2000 Server</legacyBold>   For more information about security in Microsoft Windows NT Server or Windows 2000 Server, see the Microsoft Windows Web site.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">             <legacyLink xlink:href="e8b912c1-da5b-4e85-a000-1e6648a94237">Using RDS with ODBC Connection Pooling</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">             <legacyLink xlink:href="3077d0b6-42d6-4f10-8e5d-42e6204f1109">Running Business Objects in Component Services</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence id="src4" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src8" class="srcSentence">Many other technologies interact with Remote Data Service or are used in its implementation.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">         <legacyBold>Internet Information Services</legacyBold>   For more information about Microsoft Internet Information Services (IIS), see the Microsoft Internet Information Services Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">         <legacyBold>Active Server Pages</legacyBold>   For more information about Microsoft Active Server Pages (ASP), see the Microsoft Active Server Pages Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">         <legacyBold>Microsoft Component Services</legacyBold>   For more information about Component Services, see the Microsoft Transaction Server Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">         <legacyBold>Microsoft SQL Server</legacyBold>   For more information about Microsoft SQL Server, see the Microsoft SQL Server Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">         <legacyBold>Microsoft Internet Explorer</legacyBold>   For more information about Microsoft Internet Explorer, see the Microsoft Internet ExplorerWeb site and the MSDN Library and Web Workshop Web site.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">         <legacyBold>Microsoft Windows NT Server/Windows 2000 Server</legacyBold>   For more information about security in Microsoft Windows NT Server or Windows 2000 Server, see the Microsoft Windows Web site.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
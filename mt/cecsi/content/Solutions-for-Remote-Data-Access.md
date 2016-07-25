---
title: "Solutions for Remote Data Access"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d311cc67-7db7-4c43-9590-d465564695e4
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
# Solutions for Remote Data Access
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="835368bbef90c56633f40624fa3b31f3" id="tgt1" class="tgtSentence">The Issue</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="3a4e69d24837247d425e010e41d319f6" id="tgt2" class="tgtSentence">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system).</caps:sentence>
            <caps:sentence sentenceid="e5d638327d7119110dd57e59b9ebfda1" id="tgt3" class="tgtSentence"> For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt4" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
              <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt5" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
              <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt6" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
              <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt7" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="f7aeafe2bac2093b2d5345b134c98cfd" id="tgt8" class="tgtSentence">However, you may want to access data sources indirectly through an intermediary such as Microsoft® Internet Information Services (IIS).</caps:sentence>
            <caps:sentence sentenceid="9b7a493b0368dceab2eee1fca3f47c3a" id="tgt9" class="tgtSentence"> This arrangement is sometimes called a three-tier system.</caps:sentence>
            <caps:sentence sentenceid="41ac6da246afb64221b7d3a37d1ea935" id="tgt10" class="tgtSentence"> IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</caps:sentence>
            <caps:sentence sentenceid="39570f614ec73de9cde08cc412f039dd" id="tgt11" class="tgtSentence"> The server program gains access to the data source and optionally processes the acquired data.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fe4515d91c8a213f1a534ac655d2f7d5" id="tgt12" class="tgtSentence">For example, your intranet Web page contains an application written in Microsoft® Visual Basic Scripting Edition (VBScript), which connects to IIS.</caps:sentence>
            <caps:sentence sentenceid="b0439a7c0377ac04b3c05ae46ebaeecb" id="tgt13" class="tgtSentence"> IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="49c40f0267a32e205acfc511e6b8a013" id="tgt14" class="tgtSentence">In this example, your application never directly connected to the data source; IIS did.</caps:sentence>
            <caps:sentence sentenceid="2bf6e350d5bbd36948503ed1a10d3661" id="tgt15" class="tgtSentence"> And IIS accessed the data by means of ADO.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="690dc8c1352ee35b73f50fecfd14d398" id="tgt16" class="tgtSentence">The client/server application does not have to be based on the Internet or an intranet (that is, Web-based) — it could consist solely of compiled programs on a local area network.</caps:sentence>
              <caps:sentence sentenceid="c303d2cf0a91824f37c7e80899a40563" id="tgt17" class="tgtSentence"> However, the typical case is a Web-based application.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="64d7956aad01929a01f7dd8de7cb052a" id="tgt18" class="tgtSentence">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="85a074f6bc7c0a63bbc8bbd8a1cf8965" id="tgt19" class="tgtSentence">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system.</caps:sentence>
            <caps:sentence sentenceid="4875f9ff9eeeb8804ae12cd5cd08f04a" id="tgt20" class="tgtSentence"> Remote Data Service (RDS) is this interface.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="fe72ddac3eff931af0d8667d67d86365" id="tgt21" class="tgtSentence">The Solution</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7b806e686968def715e5f9d917dbd5c0" id="tgt22" class="tgtSentence">RDS defines a programming model — the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</caps:sentence>
            <caps:sentence sentenceid="9585d8b82638c771776be64b92481cf8" id="tgt23" class="tgtSentence"> The programming model summarizes the entire functionality of RDS.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0bdd236b-edff-4aac-94c3-93e1465ca6c5">Basic RDS Programming Model</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">The Issue</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src4" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
              <caps:sentence id="src5" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src8" class="srcSentence">However, you may want to access data sources indirectly through an intermediary such as Microsoft® Internet Information Services (IIS).</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> This arrangement is sometimes called a three-tier system.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The server program gains access to the data source and optionally processes the acquired data.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">For example, your intranet Web page contains an application written in Microsoft® Visual Basic Scripting Edition (VBScript), which connects to IIS.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">In this example, your application never directly connected to the data source; IIS did.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> And IIS accessed the data by means of ADO.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src16" class="srcSentence">The client/server application does not have to be based on the Internet or an intranet (that is, Web-based) — it could consist solely of compiled programs on a local area network.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> However, the typical case is a Web-based application.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src18" class="srcSentence">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Remote Data Service (RDS) is this interface.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">The Solution</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src22" class="srcSentence">RDS defines a programming model — the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> The programming model summarizes the entire functionality of RDS.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0bdd236b-edff-4aac-94c3-93e1465ca6c5">Basic RDS Programming Model</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
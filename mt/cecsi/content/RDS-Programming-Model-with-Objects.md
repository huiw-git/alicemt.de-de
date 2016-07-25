---
title: "RDS Programming Model with Objects"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 07ce0ef0-72f1-48f4-823d-1b65d28c0926
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
# RDS Programming Model with Objects
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="89a3585232c1f213b637e73b7afff91a" id="tgt1" class="tgtSentence">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS.</caps:sentence>
          <caps:sentence sentenceid="dd9204a9d15a1b7303e681fcb18f4fd1" id="tgt2" class="tgtSentence"> The programming model specifies the sequence of activities necessary to accomplish this goal.</caps:sentence>
          <caps:sentence sentenceid="347e42dd9a69a49df9c228cecfbc85f9" id="tgt3" class="tgtSentence"> The object model specifies the objects whose methods and properties affect the programming model.</caps:sentence>
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
          <caps:sentence sentenceid="1825fcbda494091d5eea7b139edca554" id="tgt8" class="tgtSentence">RDS provides the means to perform the following sequence of actions:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="64c1efc2a313b5b4021350c09cabaf4e" id="tgt9" class="tgtSentence">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client (<legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink>).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="83f2b4f3d98548dba9b841e8d943777d" id="tgt10" class="tgtSentence">Invoke the server program.</caps:sentence>
              <caps:sentence sentenceid="621ad3472a7d4f4737c4fc7594d8815a" id="tgt11" class="tgtSentence"> Pass parameters to the server program that identifies the data source and the command to issue (proxy or <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink>).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="22dc421d101c5632a3c5054488d92d73" id="tgt12" class="tgtSentence">The server program obtains a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object from the data source, typically by using ADO.</caps:sentence>
              <caps:sentence sentenceid="eb08fbb866d03fa2320481df11f78008" id="tgt13" class="tgtSentence"> Optionally, the <legacyBold>Recordset</legacyBold> object is processed on the server (<legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8da01a026b83151dd4673fc0de836d54" id="tgt14" class="tgtSentence">The server program returns the final <legacyBold>Recordset</legacyBold> object to the client application (proxy).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3be654a0fa72b12c9bb3632d8afc1f07" id="tgt15" class="tgtSentence">On the client, the <legacyBold>Recordset</legacyBold> object is put into a form that can be easily used by visual controls (visual control and <legacyBold>RDS.DataControl</legacyBold>).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9469bc695052b9f87e902a700ee6b80f" id="tgt16" class="tgtSentence">Changes to the <legacyBold>Recordset</legacyBold> object are sent back to the server and used to update the data source (<legacyBold>RDS.DataControl</legacyBold> or <legacyBold>RDSServer.DataFactory</legacyBold>).</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="909f9af7-31db-4eec-ad52-650ce74dac2f">RDS Object Model Summary</link>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The programming model specifies the sequence of activities necessary to accomplish this goal.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The object model specifies the objects whose methods and properties affect the programming model.</caps:sentence>
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
          <caps:sentence id="src8" class="srcSentence">RDS provides the means to perform the following sequence of actions:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client (<legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink>).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Invoke the server program.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> Pass parameters to the server program that identifies the data source and the command to issue (proxy or <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink>).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">The server program obtains a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object from the data source, typically by using ADO.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> Optionally, the <legacyBold>Recordset</legacyBold> object is processed on the server (<legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">The server program returns the final <legacyBold>Recordset</legacyBold> object to the client application (proxy).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">On the client, the <legacyBold>Recordset</legacyBold> object is put into a form that can be easily used by visual controls (visual control and <legacyBold>RDS.DataControl</legacyBold>).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">Changes to the <legacyBold>Recordset</legacyBold> object are sent back to the server and used to update the data source (<legacyBold>RDS.DataControl</legacyBold> or <legacyBold>RDSServer.DataFactory</legacyBold>).</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="909f9af7-31db-4eec-ad52-650ce74dac2f">RDS Object Model Summary</link>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
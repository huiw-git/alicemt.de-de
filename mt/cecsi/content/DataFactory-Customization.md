---
title: "DataFactory Customization"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 86d77985-a0d0-405a-8587-c85a20540a0e
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
# DataFactory Customization
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="21c194ae69ef8fe6afca4df67510df2f" id="tgt1" class="tgtSentence">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system.</caps:sentence>
          <caps:sentence sentenceid="044bb3e023b865ab1420df861ea036f7" id="tgt2" class="tgtSentence"> A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object parameters to perform an update.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="e051abb2f28d2a055e388f5b07004d71" id="tgt7" class="tgtSentence">The parameters are passed to a server program, which performs the data-access operation on the remote data source.</caps:sentence>
          <caps:sentence sentenceid="a54ee89b7b20ebb8c12d64d3eaff039d" id="tgt8" class="tgtSentence"> RDS provides a default server program called the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="b61392126b23ad0dbab931d5d03044f1" id="tgt9" class="tgtSentence"> The <legacyBold>RDSServer.DataFactory</legacyBold> object returns any <legacyBold>Recordset</legacyBold> object produced by a query to the client.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="d6afdf6925bb961082bd62b3e6d4b54d" id="tgt10" class="tgtSentence">However, the <legacyBold>RDSServer.DataFactory</legacyBold> is limited to performing queries and updates.</caps:sentence>
          <caps:sentence sentenceid="f4f1e2a8917f7b583db2d2acfc1157bb" id="tgt11" class="tgtSentence"> It cannot perform any validation or processing on the connection or command strings.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8d55f1daa855e2db76f7b96f0b393cd2" id="tgt12" class="tgtSentence">With ADO, you can specify that the <legacyBold>DataFactory</legacyBold> work in conjunction with another type of server program called a <legacyItalic>handler</legacyItalic>.</caps:sentence>
          <caps:sentence sentenceid="547d21dd4575a21dc5a7f3dad9253154" id="tgt13" class="tgtSentence"> The handler can modify client connection and command strings before they are used to access the data source.</caps:sentence>
          <caps:sentence sentenceid="00b5f89f460c009153d92ab2684c618e" id="tgt14" class="tgtSentence"> In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9f0f95a1029fa87f832fb52178b6c602" id="tgt15" class="tgtSentence">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1c19cb44b916e8449e16b0b1b5fcbc6e" id="tgt16" class="tgtSentence">The following topics provide more information about customizing the <legacyBold>DataFactory</legacyBold> object.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="198506f9efe022c4e30c3d1a854af2a6" id="tgt17" class="tgtSentence">             <legacyLink xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="22a938440496cb07583597ea343363f2" id="tgt18" class="tgtSentence">             <legacyLink xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="854af76fb514a21880e5b9e52917d99d" id="tgt19" class="tgtSentence">             <legacyLink xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c43849cb4e6d9d8c38daa4222113abd8" id="tgt20" class="tgtSentence">             <legacyLink xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6da07e89b0e7a85504167c0ef0f8e2cb" id="tgt21" class="tgtSentence">             <legacyLink xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6aa99aa4bdc1e14789ec05be2005625b" id="tgt22" class="tgtSentence">             <legacyLink xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3820e7957fc9d5683e547bd8e7cbe77f" id="tgt23" class="tgtSentence">             <legacyLink xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</legacyLink>           </caps:sentence>
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
        <para>
          <caps:sentence id="src1" class="srcSentence">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object parameters to perform an update.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src7" class="srcSentence">The parameters are passed to a server program, which performs the data-access operation on the remote data source.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> RDS provides a default server program called the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> The <legacyBold>RDSServer.DataFactory</legacyBold> object returns any <legacyBold>Recordset</legacyBold> object produced by a query to the client.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">However, the <legacyBold>RDSServer.DataFactory</legacyBold> is limited to performing queries and updates.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> It cannot perform any validation or processing on the connection or command strings.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">With ADO, you can specify that the <legacyBold>DataFactory</legacyBold> work in conjunction with another type of server program called a <legacyItalic>handler</legacyItalic>.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> The handler can modify client connection and command strings before they are used to access the data source.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src15" class="srcSentence">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src16" class="srcSentence">The following topics provide more information about customizing the <legacyBold>DataFactory</legacyBold> object.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">             <legacyLink xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">             <legacyLink xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src19" class="srcSentence">             <legacyLink xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src20" class="srcSentence">             <legacyLink xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src21" class="srcSentence">             <legacyLink xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src22" class="srcSentence">             <legacyLink xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src23" class="srcSentence">             <legacyLink xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
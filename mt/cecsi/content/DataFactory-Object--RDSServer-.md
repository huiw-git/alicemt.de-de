---
title: "DataFactory Object (RDSServer)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e75240c2-b749-471e-b6ea-98cae232efbe
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
# DataFactory Object (RDSServer)
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
          <caps:sentence sentenceid="80a02a7516e20364c01c6bda0cca5e41" id="tgt5" class="tgtSentence">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="80721c3ae23b4a5bca613790aa390056" id="tgt6" class="tgtSentence">The <legacyBold>RDSServer.DataFactory</legacyBold> object is designed as a server-side Automation object that receives client requests.</caps:sentence>
          <caps:sentence sentenceid="8966fa2bbed4edf93eb007d69299c281" id="tgt7" class="tgtSentence"> In an Internet implementation, it resides on a Web server and is instantiated by the ADISAPI component.</caps:sentence>
          <caps:sentence sentenceid="a274c868f9ac183a317a9dcfbf887cc4" id="tgt8" class="tgtSentence"> The <legacyBold>RDSServer.DataFactory</legacyBold> object provides read and write access to specified data sources, but does not contain any validation or business rules logic.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="69c164bd87f99fcfd256705852a6e04c" id="tgt9" class="tgtSentence">If you use a method that is available in both the <legacyBold>RDSServer.DataFactory</legacyBold> and <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> objects, Remote Data Service uses the <legacyBold>RDS.DataControl</legacyBold> version by default.</caps:sentence>
          <caps:sentence sentenceid="fb6b20e6617d10c6c7fc52a2faff5f22" id="tgt10" class="tgtSentence"> The default assumes a basic programming scenario, where the <legacyBold>RDSServer.DataFactory</legacyBold> serves as a generic server-side business object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5cea7c8b58f89173f4cc1ec5ca8e726a" id="tgt11" class="tgtSentence">If you want your Web application to handle task-specific server-side processing, you can replace the <legacyBold>RDSServer.DataFactory</legacyBold> with a custom business object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="cf996d8c1c942ad8e2980de290312bec" id="tgt12" class="tgtSentence">You can create server-side business objects that call the <legacyBold>RDSServer.DataFactory</legacyBold> methods, such as <legacyLink xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query</legacyLink> and <legacyLink xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="f20479a76ca1f9e7b9a3f212b310f4e5" id="tgt13" class="tgtSentence"> This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1cbded089aab1a1e22cd875d45e757b6" id="tgt14" class="tgtSentence">The <unmanagedCodeEntityReference>DataFactory</unmanagedCodeEntityReference> object is not safe for scripts that run on the client side.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fbd7a0e7dd7e5d40d223eaa356a16baf" id="tgt15" class="tgtSentence">The class ID for the <legacyBold>RDSServer.DataFactory</legacyBold> object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt16" class="tgtSentence">This section contains the following topic.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="17110c732c9b804d42ce0a300c1a45ad" id="tgt17" class="tgtSentence">
                <legacyLink xlink:href="36a1f49b-91f4-44f4-b6e2-52fc7ed06d7e">DataFactory Object (RDSServer) Properties, Methods, and Events</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="b4e2844a-120a-4513-860b-f1b6e4b5dda4">VBScript Example</link>
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
          <caps:sentence id="src5" class="srcSentence">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">The <legacyBold>RDSServer.DataFactory</legacyBold> object is designed as a server-side Automation object that receives client requests.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> In an Internet implementation, it resides on a Web server and is instantiated by the ADISAPI component.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The <legacyBold>RDSServer.DataFactory</legacyBold> object provides read and write access to specified data sources, but does not contain any validation or business rules logic.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">If you use a method that is available in both the <legacyBold>RDSServer.DataFactory</legacyBold> and <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> objects, Remote Data Service uses the <legacyBold>RDS.DataControl</legacyBold> version by default.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> The default assumes a basic programming scenario, where the <legacyBold>RDSServer.DataFactory</legacyBold> serves as a generic server-side business object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">If you want your Web application to handle task-specific server-side processing, you can replace the <legacyBold>RDSServer.DataFactory</legacyBold> with a custom business object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">You can create server-side business objects that call the <legacyBold>RDSServer.DataFactory</legacyBold> methods, such as <legacyLink xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query</legacyLink> and <legacyLink xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset</legacyLink>.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">The <unmanagedCodeEntityReference>DataFactory</unmanagedCodeEntityReference> object is not safe for scripts that run on the client side.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src15" class="srcSentence">The class ID for the <legacyBold>RDSServer.DataFactory</legacyBold> object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src16" class="srcSentence">This section contains the following topic.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">
                <legacyLink xlink:href="36a1f49b-91f4-44f4-b6e2-52fc7ed06d7e">DataFactory Object (RDSServer) Properties, Methods, and Events</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="b4e2844a-120a-4513-860b-f1b6e4b5dda4">VBScript Example</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Configuring DataFactory for Safe or Unrestricted Modes"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8ff24805-dc7a-42ae-b600-5bad0e3f51b8
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
# Configuring DataFactory for Safe or Unrestricted Modes
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
          <caps:sentence sentenceid="725650f4f66a241a7514bcae04ed54b0" id="tgt5" class="tgtSentence">By default, ADO is installed with a "safe" <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> configuration.</caps:sentence>
          <caps:sentence sentenceid="2ea4da962ba9a30c60b8b2ba08712072" id="tgt6" class="tgtSentence"> Safe mode for RDS Server components means that the following are true:</caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence sentenceid="21cda82de6ff67ac8cc318b8095b68fa" id="tgt7" class="tgtSentence">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="2993133065ddf1ad7cb8120edf93f08e" id="tgt8" class="tgtSentence">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="cb68a818913cf746bc3ef58d2697c62b" id="tgt9" class="tgtSentence">Msdfmap.ini file is installed in the Windows directory.</caps:sentence>
              <caps:sentence sentenceid="7bec6443d3e2288e0a682e75a222e44a" id="tgt10" class="tgtSentence"> You must configure this file according to your needs, before you use RDS in three-tier mode.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="a937831dd0033fa9e4335c7615455a70" id="tgt11" class="tgtSentence">Optionally, you can configure an unrestricted <legacyBold>DataFactory</legacyBold> installation.</caps:sentence>
          <caps:sentence sentenceid="5f54b8bf3727dde466d9f737dc31b504" id="tgt12" class="tgtSentence">
            <legacyBold>DataFactory</legacyBold> can be used directly without the custom handler.</caps:sentence>
          <caps:sentence sentenceid="26dcff099c2a88494a11e25521dc38f0" id="tgt13" class="tgtSentence"> Users can still use a custom handler by modifying the connection strings, but it is not required.</caps:sentence>
          <caps:sentence sentenceid="dc91e92ffa54ee8e8d694b46fb570fde" id="tgt14" class="tgtSentence"> For more information about the implications of using the <legacyBold>RDSServer.DataFactory</legacyBold> object, see <legacyLink xlink:href="82fb1330-d6c6-4c17-ad3e-d417ff822b25">Securing RDS Applications</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="32e43c2f2fe3b17e17ec3e2d6cea8c05" id="tgt15" class="tgtSentence">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration.</caps:sentence>
          <caps:sentence sentenceid="270498bf92c761c2dad7b4a4075fd377" id="tgt16" class="tgtSentence"> To run in safe mode, run handsafe.reg.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="81f214158f27842b91ace50ec4ba4bf8" id="tgt17" class="tgtSentence">After running handsafe.reg, you must stop and restart the World Wide Web Publishing Service on the Web server by typing the following commands in a Command Prompt window: "NET STOP W3SVC" and "NET START W3SVC".</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
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
          <caps:sentence id="src5" class="srcSentence">By default, ADO is installed with a "safe" <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> configuration.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Safe mode for RDS Server components means that the following are true:</caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Msdfmap.ini file is installed in the Windows directory.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> You must configure this file according to your needs, before you use RDS in three-tier mode.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src11" class="srcSentence">Optionally, you can configure an unrestricted <legacyBold>DataFactory</legacyBold> installation.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence">
            <legacyBold>DataFactory</legacyBold> can be used directly without the custom handler.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> Users can still use a custom handler by modifying the connection strings, but it is not required.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> For more information about the implications of using the <legacyBold>RDSServer.DataFactory</legacyBold> object, see <legacyLink xlink:href="82fb1330-d6c6-4c17-ad3e-d417ff822b25">Securing RDS Applications</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src15" class="srcSentence">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> To run in safe mode, run handsafe.reg.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src17" class="srcSentence">After running handsafe.reg, you must stop and restart the World Wide Web Publishing Service on the Web server by typing the following commands in a Command Prompt window: "NET STOP W3SVC" and "NET START W3SVC".</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
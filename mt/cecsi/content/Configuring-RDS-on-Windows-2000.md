---
title: "Configuring RDS on Windows 2000"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef37e858-c05f-4f52-a65f-3ce6037e0d03
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
# Configuring RDS on Windows 2000
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6736138a9af7ade90c175d82d6355b1a" id="tgt1" class="tgtSentence">If you experience difficulties getting RDS to function correctly after you upgrade to Windows 2000, follow these steps to troubleshoot the issue:  </caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence sentenceid="5992490a8f0e69630fe04969e77897cf" id="tgt2" class="tgtSentence">Make sure that the World Wide Web Publishing Service is running first by navigating to http:// server by using Internet Explorer.</caps:sentence>
              <caps:sentence sentenceid="c751dd79fd6ede7d5fbfc28a71caba28" id="tgt3" class="tgtSentence"> If you cannot access the Web server in this manner, open a command prompt and enter the following command, "NET START W3SVC".</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0b594198bee3407378b01710993cd841" id="tgt4" class="tgtSentence">On the Start menu, select Run.</caps:sentence>
              <caps:sentence sentenceid="76591339af8964a4cd27350987892ae4" id="tgt5" class="tgtSentence"> Type msdfmap.ini and then click OK to open the msdfmap.ini file in Notepad.</caps:sentence>
              <caps:sentence sentenceid="f603e40b1e6d7a352b2d51ebee8647be" id="tgt6" class="tgtSentence"> Check the [CONNECT DEFAULT] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="add28d1efc66ab840063b011d2a5fa9e" id="tgt7" class="tgtSentence">Using the RegEdit utility, navigate to "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DataFactory\HandlerInfo" and make sure <legacyBold>HandlerRequired</legacyBold> is set to 0 and <legacyBold>DefaultHandler</legacyBold> is "" (Null string).</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="6e6ae90cd560e5893d8e818814a399a5" id="tgt8" class="tgtSentence">             <legacyBold>Note</legacyBold>   If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="11eac562adb35386ec1ad8c129d76f0e" id="tgt9" class="tgtSentence">Using the RegEdit utility, navigate in the registry to "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCLaunch" and verify that there is a key named <legacyBold>RDSServer.Datafactory</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="d113115ec007b108c26f8ce326235df8" id="tgt10" class="tgtSentence"> If not, create it.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="7c98f51937de4b34357dab1eab93e75c" id="tgt11" class="tgtSentence">Using Internet Services Manager, locate the Default Web site and view the properties of the MSADC virtual root.</caps:sentence>
              <caps:sentence sentenceid="12b1902d32f7008cd159a4929c6f9f51" id="tgt12" class="tgtSentence"> Inspect the Directory Security/IP Address and Domain Name Restrictions.</caps:sentence>
              <caps:sentence sentenceid="d2c6e82c5caca8b74c28743887110c41" id="tgt13" class="tgtSentence"> If the "Access is Denied" is checked then select "Granted".</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="ad6a7a4a49d31083ce81731c0733cf43" id="tgt14" class="tgtSentence">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt15" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt16" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt17" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="6db515175c3ad631fbb2b3b9009da05e" id="tgt18" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system.</caps:sentence>
            <caps:sentence sentenceid="e946a13ba71be45a9aab7dfacab71384" id="tgt19" class="tgtSentence"> Migrate applications that use RDS to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
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
          <caps:sentence id="src1" class="srcSentence">If you experience difficulties getting RDS to function correctly after you upgrade to Windows 2000, follow these steps to troubleshoot the issue:  </caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">Make sure that the World Wide Web Publishing Service is running first by navigating to http:// server by using Internet Explorer.</caps:sentence>
              <caps:sentence id="src3" class="srcSentence"> If you cannot access the Web server in this manner, open a command prompt and enter the following command, "NET START W3SVC".</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">On the Start menu, select Run.</caps:sentence>
              <caps:sentence id="src5" class="srcSentence"> Type msdfmap.ini and then click OK to open the msdfmap.ini file in Notepad.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> Check the [CONNECT DEFAULT] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Using the RegEdit utility, navigate to "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DataFactory\HandlerInfo" and make sure <legacyBold>HandlerRequired</legacyBold> is set to 0 and <legacyBold>DefaultHandler</legacyBold> is "" (Null string).</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyBold>Note</legacyBold>   If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Using the RegEdit utility, navigate in the registry to "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCLaunch" and verify that there is a key named <legacyBold>RDSServer.Datafactory</legacyBold>.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> If not, create it.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Using Internet Services Manager, locate the Default Web site and view the properties of the MSADC virtual root.</caps:sentence>
              <caps:sentence id="src12" class="srcSentence"> Inspect the Directory Security/IP Address and Domain Name Restrictions.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> If the "Access is Denied" is checked then select "Granted".</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src14" class="srcSentence">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src15" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> Migrate applications that use RDS to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
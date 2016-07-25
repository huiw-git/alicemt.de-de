---
title: "Registering a Custom Business Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9032ad8-d14c-42e3-ba13-cb5f00084a79
caps.latest.revision: 17
caps.handback.revision: 17
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
# Registering a Custom Business Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e335e769219d367708d69eacb67b31ee" id="tgt1" class="tgtSentence">To successfully launch a custom business object (.dll or .exe) through the Web server, the business object's ProgID must be entered into the registry as explained in this procedure.</caps:sentence>
          <caps:sentence sentenceid="2b64f8c436f13fecb97209fee04ed15b" id="tgt2" class="tgtSentence"> This RDS feature protects the security of your Web server by running only sanctioned executables.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="0aac3f51dc89f88089da67071545209e" id="tgt7" class="tgtSentence">For MDAC 2.0 and later and Windows DAC, the default business object, <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>, is not registered by default during the MDAC/Windows DAC installation.</caps:sentence>
            <caps:sentence sentenceid="5336b5573ff6ce8895efc31330eb0780" id="tgt8" class="tgtSentence"> However, if <legacyBold>RDSServer.DataFactory</legacyBold> was registered as safe for execution on the computer prior to the installation, the registry entry is maintained for the new installation.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence sentenceid="7d0531c06b1c7f12cfcba85675773a94" id="tgt9" class="tgtSentence">To register a custom business object:</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="cc79da913c8cf8a9908f2026e6eaf435" id="tgt10" class="tgtSentence">Click <ui>Start</ui> and then click <ui>Run</ui>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="2c00765f4c117b4c7103ce2869baf265" id="tgt11" class="tgtSentence">Type <ui>RegEdit</ui> and click <ui>OK</ui>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="d897e4a3f7cec96ea5ccad572163d3d6" id="tgt12" class="tgtSentence">In the Registry Editor, navigate to the <legacyBold>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\W3SVC\Parameters\ADCLaunch </legacyBold>registry key.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="1f05c9c88890a937224f56f2f5f97870" id="tgt13" class="tgtSentence">Select the <ui>ADCLaunch</ui> key, and then from the <ui>Edit</ui><legacyBold> </legacyBold>menu, point to <ui>New</ui> and click <ui>Key</ui>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="320ff8f34ba18c796a32557cd38cb6f8" id="tgt14" class="tgtSentence">Type the ProgID of your custom business object and click <ui>Enter</ui>.</caps:sentence>
                  <caps:sentence sentenceid="abb8ba666d84b682a007a621d9dd4d40" id="tgt15" class="tgtSentence"> Leave the <ui>Value</ui> entry blank.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To successfully launch a custom business object (.dll or .exe) through the Web server, the business object's ProgID must be entered into the registry as explained in this procedure.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This RDS feature protects the security of your Web server by running only sanctioned executables.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <alert class="note">
          <para>
            <caps:sentence id="src7" class="srcSentence">For MDAC 2.0 and later and Windows DAC, the default business object, <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>, is not registered by default during the MDAC/Windows DAC installation.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> However, if <legacyBold>RDSServer.DataFactory</legacyBold> was registered as safe for execution on the computer prior to the installation, the registry entry is maintained for the new installation.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence id="src9" class="srcSentence">To register a custom business object:</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Click <ui>Start</ui> and then click <ui>Run</ui>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Type <ui>RegEdit</ui> and click <ui>OK</ui>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src12" class="srcSentence">In the Registry Editor, navigate to the <legacyBold>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\W3SVC\Parameters\ADCLaunch </legacyBold>registry key.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Select the <ui>ADCLaunch</ui> key, and then from the <ui>Edit</ui><legacyBold> </legacyBold>menu, point to <ui>New</ui> and click <ui>Key</ui>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Type the ProgID of your custom business object and click <ui>Enter</ui>.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> Leave the <ui>Value</ui> entry blank.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
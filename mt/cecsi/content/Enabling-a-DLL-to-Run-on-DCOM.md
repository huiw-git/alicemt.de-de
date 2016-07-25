---
title: "Enabling a DLL to Run on DCOM"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5f1c2205-191c-4fb4-9bd9-84c878ea46ed
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
# Enabling a DLL to Run on DCOM
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
          <caps:sentence sentenceid="6368df6a49de66c43284b8650b4ae4a7" id="tgt5" class="tgtSentence">The following steps outline how to enable a business object .dll to use both DCOM and Microsoft Internet Information Services (HTTP) via Component Services.</caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence sentenceid="1c37d0d93275435d5de96f3dfd9269b4" id="tgt6" class="tgtSentence">Create a new empty package in the Component Services MMC snap-in.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="d008a8fdca05e39e175e243e8a46a3b4" id="tgt7" class="tgtSentence">You will use the Component Services MMC snap-in to create a package and add the DLL into this package.</caps:sentence>
              <caps:sentence sentenceid="0973526461d93faff94a74a0ad32166c" id="tgt8" class="tgtSentence"> This makes the .dll accessible through DCOM, but it removes the accessibility through IIS.</caps:sentence>
              <caps:sentence sentenceid="d7b89b2e533c6b3736f32093f6ee5fec" id="tgt9" class="tgtSentence"> (If you check in the registry for the .dll, the <legacyBold>Inproc </legacyBold>key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the <legacyBold>Inproc </legacyBold>key.)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8f2e5772e2992101f4a18507d899b81a" id="tgt10" class="tgtSentence">Install a business object into the package.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="533bd2f15b304e5ce764f6da2d6c7502" id="tgt11" class="tgtSentence">-or-  </caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="9b7787e6473bfe954c2e47a04560fecf" id="tgt12" class="tgtSentence">Import the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object into the package.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d94f08605935038a515e09f7de3de355" id="tgt13" class="tgtSentence">Set the Activation attribute for the package to <legacyBold>In the creator's process</legacyBold> (Library application).</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="7b5c706ec48942a2f11e4af243b0ea82" id="tgt14" class="tgtSentence">To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in.</caps:sentence>
              <caps:sentence sentenceid="ff657bf702cb331c0263728de3ed837f" id="tgt15" class="tgtSentence"> After you set the attribute to <legacyBold>In the creator's process</legacyBold>, you will notice that an <legacyBold>Inproc</legacyBold> server key in the registry has been added that points to a Component Services surrogate .dll.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="571f33dffe1140c7d46c0f0daa698fac" id="tgt16" class="tgtSentence">For more information about Component Services (or Microsoft Transaction Service, if you are using Windows NT) and how to perform these steps, visit the Microsoft Transaction Server Web site.</caps:sentence>
        </para>
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
          <caps:sentence id="src5" class="srcSentence">The following steps outline how to enable a business object .dll to use both DCOM and Microsoft Internet Information Services (HTTP) via Component Services.</caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Create a new empty package in the Component Services MMC snap-in.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src7" class="srcSentence">You will use the Component Services MMC snap-in to create a package and add the DLL into this package.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> This makes the .dll accessible through DCOM, but it removes the accessibility through IIS.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> (If you check in the registry for the .dll, the <legacyBold>Inproc </legacyBold>key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the <legacyBold>Inproc </legacyBold>key.)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Install a business object into the package.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src11" class="srcSentence">-or-  </caps:sentence>
            </para>
            <para>
              <caps:sentence id="src12" class="srcSentence">Import the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object into the package.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">Set the Activation attribute for the package to <legacyBold>In the creator's process</legacyBold> (Library application).</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src14" class="srcSentence">To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> After you set the attribute to <legacyBold>In the creator's process</legacyBold>, you will notice that an <legacyBold>Inproc</legacyBold> server key in the registry has been added that points to a Component Services surrogate .dll.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src16" class="srcSentence">For more information about Component Services (or Microsoft Transaction Service, if you are using Windows NT) and how to perform these steps, visit the Microsoft Transaction Server Web site.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
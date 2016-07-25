---
title: "Step 1: Specify a Server Program (RDS Tutorial)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d8bb35b1-c02a-4231-8d55-016e56e53b95
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
# Step 1: Specify a Server Program (RDS Tutorial)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b8eeb94dc7315b217e7a26714fddc9fb" id="tgt1" class="tgtSentence">In the most general case, use the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method to specify the default server program, <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>, or your own custom server program (business object).</caps:sentence>
          <caps:sentence sentenceid="d3782474b567e00ad0c7ac547db73103" id="tgt2" class="tgtSentence"> A server program is instantiated on the server, and a reference to the server program, or <legacyItalic>proxy</legacyItalic>, is returned.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="642e55659e28b2bc39c6def6f99a19e9" id="tgt3" class="tgtSentence">This tutorial uses the default server program:</caps:sentence>
        </para>
        <code>Sub RDSTutorial1()
   Dim DS as New RDS.DataSpace
   Dim DF as Object
   Set DF = DS.("RDSServer.DataFactory", "http://yourServer")
...</code>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt4" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt5" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt6" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt7" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics>
        <link xlink:href="5e74c2da-65ee-4de4-8b41-6eac45c3632e">Step 2: Invoke the Server Program (RDS Tutorial)</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">In the most general case, use the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method to specify the default server program, <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>, or your own custom server program (business object).</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A server program is instantiated on the server, and a reference to the server program, or <legacyItalic>proxy</legacyItalic>, is returned.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">This tutorial uses the default server program:</caps:sentence>
        </para>
        <code>Sub RDSTutorial1()
   Dim DS as New RDS.DataSpace
   Dim DF as Object
   Set DF = DS.("RDSServer.DataFactory", "http://yourServer")
...</code>
        <alert class="important">
          <para>
            <caps:sentence id="src4" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics>
        <link xlink:href="5e74c2da-65ee-4de4-8b41-6eac45c3632e">Step 2: Invoke the Server Program (RDS Tutorial)</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
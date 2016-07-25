---
title: "Step 5: DataControl is Made Usable (RDS Tutorial)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ed5c4a24-9804-4c85-817e-317652acb9b4
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
# Step 5: DataControl is Made Usable (RDS Tutorial)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8cdcf7d622dd9759116f17e40eb054ad" id="tgt1" class="tgtSentence">The returned <legacyBold>Recordset</legacyBold> object is available for use.</caps:sentence>
          <caps:sentence sentenceid="9e0e8f913d461aa8fde8d10789587782" id="tgt2" class="tgtSentence"> You can examine, navigate, or edit it as you would any other <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="1b54b0c5abab98ab5438977d55c9fb70" id="tgt3" class="tgtSentence"> What you can do with the <legacyBold>Recordset</legacyBold> depends on your environment.</caps:sentence>
          <caps:sentence sentenceid="65bc066e84908fc8f5cb3b87ed277df6" id="tgt4" class="tgtSentence"> Visual Basic and Visual C++ have visual controls that can use a <legacyBold>Recordset</legacyBold> directly or indirectly with the aid of an enabling data control.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt5" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt6" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt7" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt8" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="dcbee87de8f68d55b5500a2aed147f4c" id="tgt9" class="tgtSentence">For example, if you are displaying a Web page in Microsoft Internet Explorer, you might want to display the <legacyBold>Recordset</legacyBold> object data in a visual control.</caps:sentence>
          <caps:sentence sentenceid="fbaeff482918c4585f573d5ebb18cad8" id="tgt10" class="tgtSentence"> Visual controls on a Web page cannot access a <legacyBold>Recordset</legacyBold> object directly.</caps:sentence>
          <caps:sentence sentenceid="56ff380296df14806f64e7b589e98f83" id="tgt11" class="tgtSentence"> However, they can access the <legacyBold>Recordset</legacyBold> object through the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="768972ef76b5a225fc3f5d1001d12fe9" id="tgt12" class="tgtSentence"> The <legacyBold>RDS.DataControl</legacyBold> becomes usable by a visual control when its <legacyLink xlink:href="a29e3fb9-306d-497a-9a59-1856a914e5e9">SourceRecordset</legacyLink> property is set to the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b5e888a41c404cfbb97ccdf121e5de62" id="tgt13" class="tgtSentence">The visual control object must have its <legacyBold>DATASRC</legacyBold> parameter set to the <legacyBold>RDS.DataControl</legacyBold>, and its <legacyBold>DATAFLD</legacyBold> property set to a <legacyBold>Recordset</legacyBold> object field (column).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="65804e812f40d5dd26c2796a928f7985" id="tgt14" class="tgtSentence">In this tutorial, set the <legacyBold>SourceRecordset</legacyBold> property:</caps:sentence>
        </para>
        <code>Sub RDSTutorial5()
   Dim DS as New RDS.DataSpace
   Dim RS as ADODB.Recordset
   Dim DC as New RDS.DataControl
   Dim DF as Object
   Set DF = DS.<codeFeaturedElement xmlns="">CreateObject</codeFeaturedElement>("RDSServer.DataFactory", "http://yourServer")
   Set RS = DF.<codeFeaturedElement xmlns="">Query</codeFeaturedElement> ("DSN=Pubs", "SELECT * FROM Authors")
   DC.<codeFeaturedElement xmlns="">SourceRecordset</codeFeaturedElement> = RS         ' Visual controls can now bind to DC.
...</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="b1e927d6-7d50-4978-9eef-045043cdce7a">Step 6: Changes are Sent to the Server (RDS Tutorial)</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The returned <legacyBold>Recordset</legacyBold> object is available for use.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can examine, navigate, or edit it as you would any other <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> What you can do with the <legacyBold>Recordset</legacyBold> depends on your environment.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Visual Basic and Visual C++ have visual controls that can use a <legacyBold>Recordset</legacyBold> directly or indirectly with the aid of an enabling data control.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src5" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src9" class="srcSentence">For example, if you are displaying a Web page in Microsoft Internet Explorer, you might want to display the <legacyBold>Recordset</legacyBold> object data in a visual control.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> Visual controls on a Web page cannot access a <legacyBold>Recordset</legacyBold> object directly.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> However, they can access the <legacyBold>Recordset</legacyBold> object through the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink>.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> The <legacyBold>RDS.DataControl</legacyBold> becomes usable by a visual control when its <legacyLink xlink:href="a29e3fb9-306d-497a-9a59-1856a914e5e9">SourceRecordset</legacyLink> property is set to the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">The visual control object must have its <legacyBold>DATASRC</legacyBold> parameter set to the <legacyBold>RDS.DataControl</legacyBold>, and its <legacyBold>DATAFLD</legacyBold> property set to a <legacyBold>Recordset</legacyBold> object field (column).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">In this tutorial, set the <legacyBold>SourceRecordset</legacyBold> property:</caps:sentence>
        </para>
        <code>Sub RDSTutorial5()
   Dim DS as New RDS.DataSpace
   Dim RS as ADODB.Recordset
   Dim DC as New RDS.DataControl
   Dim DF as Object
   Set DF = DS.<codeFeaturedElement xmlns="">CreateObject</codeFeaturedElement>("RDSServer.DataFactory", "http://yourServer")
   Set RS = DF.<codeFeaturedElement xmlns="">Query</codeFeaturedElement> ("DSN=Pubs", "SELECT * FROM Authors")
   DC.<codeFeaturedElement xmlns="">SourceRecordset</codeFeaturedElement> = RS         ' Visual controls can now bind to DC.
...</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="b1e927d6-7d50-4978-9eef-045043cdce7a">Step 6: Changes are Sent to the Server (RDS Tutorial)</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
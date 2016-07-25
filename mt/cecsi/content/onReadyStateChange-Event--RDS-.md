---
title: "onReadyStateChange Event (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: bf2ae3ac-bfe4-4709-b50a-ea7c282c3164
caps.latest.revision: 14
caps.handback.revision: 14
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
# onReadyStateChange Event (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="833f45f52cedb1da69a2854fe9e63b5f" id="tgt1" class="tgtSentence">The <legacyBold>onReadyStateChange</legacyBold> event is called whenever the value of the <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState</legacyLink> property changes.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>onReadyStateChange</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt6" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1cf11503bad61f4684df6656dd531075" id="tgt7" class="tgtSentence">The <legacyBold>ReadyState</legacyBold> property reflects the progress of an <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object as it asynchronously retrieves data into its <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="6e8bae6b865fc22ad3b39064008112ed" id="tgt8" class="tgtSentence"> Use the <legacyBold>onReadyStateChange</legacyBold> event to monitor changes in the <legacyBold>ReadyState</legacyBold> property whenever they occur.</caps:sentence>
            <caps:sentence sentenceid="8e1aeb8ac1f194e58283f190c7d71621" id="tgt9" class="tgtSentence"> This is more efficient than periodically checking the property's value.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>onReadyStateChange</legacyBold> event is called whenever the value of the <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState</legacyLink> property changes.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>onReadyStateChange</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <legacyBold>ReadyState</legacyBold> property reflects the progress of an <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object as it asynchronously retrieves data into its <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Use the <legacyBold>onReadyStateChange</legacyBold> event to monitor changes in the <legacyBold>ReadyState</legacyBold> property whenever they occur.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> This is more efficient than periodically checking the property's value.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
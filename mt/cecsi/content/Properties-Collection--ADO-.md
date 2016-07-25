---
title: "Properties Collection (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82
caps.latest.revision: 9
caps.handback.revision: 9
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
# Properties Collection (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8cb0f5999ee4e961da1b579ef00c8807" id="tgt1" class="tgtSentence">Contains all the <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink> objects for a specific instance of an object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="3190671be772602e212e515078123ef4" id="tgt2" class="tgtSentence">Some ADO objects have a <legacyBold>Properties</legacyBold> collection made up of <legacyBold>Property</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="47b134bbe089fb545eb8df4b2778f9e8" id="tgt3" class="tgtSentence"> Each <legacyBold>Property</legacyBold> object corresponds to a characteristic of the ADO object specific to the provider.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="02a0486c44ad4bb6041a2d59e71f4da2" id="tgt4" class="tgtSentence">See the <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink> object topic for a more detailed explanation of how to use <legacyBold>Property</legacyBold> objects.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="a9438dfb64c6ac61c12d2ea5c3bd65aa" id="tgt5" class="tgtSentence">The <legacyBold>Dynamic Properties</legacyBold> of the <legacyBold>Recordset</legacyBold> object go out of scope (become unavailable) when the <legacyBold>Recordset</legacyBold> is closed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt6" class="tgtSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="0a6e10161c7d3e65baa8409595c08a43" id="tgt7" class="tgtSentence">
                  <legacyLink xlink:href="03dc1e08-5f03-49e5-8596-76b306b931bd">Properties Collection Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property Object</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all the <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink> objects for a specific instance of an object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Some ADO objects have a <legacyBold>Properties</legacyBold> collection made up of <legacyBold>Property</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Each <legacyBold>Property</legacyBold> object corresponds to a characteristic of the ADO object specific to the provider.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src4" class="srcSentence">See the <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink> object topic for a more detailed explanation of how to use <legacyBold>Property</legacyBold> objects.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src5" class="srcSentence">The <legacyBold>Dynamic Properties</legacyBold> of the <legacyBold>Recordset</legacyBold> object go out of scope (become unavailable) when the <legacyBold>Recordset</legacyBold> is closed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">
                  <legacyLink xlink:href="03dc1e08-5f03-49e5-8596-76b306b931bd">Properties Collection Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property Object</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
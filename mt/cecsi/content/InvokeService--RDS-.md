---
title: "InvokeService (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ad45c676-ec7e-4a3a-9a6b-a54f75eb3012
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
# InvokeService (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3c214402e67d208662dafc82f4752ce5" id="tgt1" class="tgtSentence">Returns a pointer to the requested interface on a more capable version of the object.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="20827e3adfa88537ab8adfa70f7ffa15" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to  <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
object.<legacyBold>InvokeService</legacyBold>(REFID <parameterReference>riid</parameterReference>, IUknown* <parameterReference>punkNotSoFunctionalInterface</parameterReference>, IUknown** <parameterReference>ppunkMoreFunctionalInterface</parameterReference>) As HRESULT</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <para>
            <parameterReference>riid</parameterReference>
          </para>
          <para>
            <caps:sentence sentenceid="9852cc698fc38918cb9681c04c9d0d6a" id="tgt6" class="tgtSentence">[in] The identifier of the interface being requested.</caps:sentence>
          </para>
          <para>
            <parameterReference>punkNotSoFunctionalInterface</parameterReference>
          </para>
          <para>
            <caps:sentence sentenceid="22108c341774713ff9867d0570cb8151" id="tgt7" class="tgtSentence">[in] The less capable source object.</caps:sentence>
          </para>
          <para>
            <parameterReference>ppunkMoreFunctionalInterface</parameterReference>
          </para>
          <para>
            <caps:sentence sentenceid="6da553cb5cf375c9463ae694145ed8dc" id="tgt8" class="tgtSentence">[out] The address of the pointer variable that receives the interface pointer requested in <parameterReference>riid</parameterReference>.</caps:sentence>
            <caps:sentence sentenceid="8683b11a2f62634f46e52dc0d1b4c87c" id="tgt9" class="tgtSentence"> Upon successful return, the <parameterReference>ppunkMoreFunctionalInterface</parameterReference> parameter contains the requested interface pointer to the object.</caps:sentence>
            <caps:sentence sentenceid="0fd5690b3adf218687a4080c4d94a37d" id="tgt10" class="tgtSentence"> If the object does not support the interface specified in <parameterReference>riid</parameterReference>, <parameterReference>ppunkMoreFunctionalInterface</parameterReference> is set to NULL.</caps:sentence>
          </para>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="92834181f751fe3e04a99071aa0d09d1" id="tgt11" class="tgtSentence">An HRESULT value that indicates if the call to the <legacyBold>InvokeService</legacyBold> method was successful.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ffe26b834e80458a325145ecf85806f2" id="tgt12" class="tgtSentence">The RDS cursor engine implementation of <legacyBold>InvokeService</legacyBold> takes the input rowset (or multiple results object), populates the cursor engine from the input rowset, and then returns a pointer on itself.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt13" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="01044c3a-ed38-4144-bc43-fe38a6d22d04">IRDSService Interface (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c2c6af1a-3c44-4c9d-ad33-b381552c71af">RDS Methods</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Returns a pointer to the requested interface on a more capable version of the object.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to  <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
object.<legacyBold>InvokeService</legacyBold>(REFID <parameterReference>riid</parameterReference>, IUknown* <parameterReference>punkNotSoFunctionalInterface</parameterReference>, IUknown** <parameterReference>ppunkMoreFunctionalInterface</parameterReference>) As HRESULT</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <para>
            <parameterReference>riid</parameterReference>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">[in] The identifier of the interface being requested.</caps:sentence>
          </para>
          <para>
            <parameterReference>punkNotSoFunctionalInterface</parameterReference>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">[in] The less capable source object.</caps:sentence>
          </para>
          <para>
            <parameterReference>ppunkMoreFunctionalInterface</parameterReference>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">[out] The address of the pointer variable that receives the interface pointer requested in <parameterReference>riid</parameterReference>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Upon successful return, the <parameterReference>ppunkMoreFunctionalInterface</parameterReference> parameter contains the requested interface pointer to the object.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> If the object does not support the interface specified in <parameterReference>riid</parameterReference>, <parameterReference>ppunkMoreFunctionalInterface</parameterReference> is set to NULL.</caps:sentence>
          </para>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">An HRESULT value that indicates if the call to the <legacyBold>InvokeService</legacyBold> method was successful.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">The RDS cursor engine implementation of <legacyBold>InvokeService</legacyBold> takes the input rowset (or multiple results object), populates the cursor engine from the input rowset, and then returns a pointer on itself.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="01044c3a-ed38-4144-bc43-fe38a6d22d04">IRDSService Interface (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c2c6af1a-3c44-4c9d-ad33-b381552c71af">RDS Methods</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
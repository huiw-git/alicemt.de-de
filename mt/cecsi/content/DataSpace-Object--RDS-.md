---
title: "DataSpace Object (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 9194bffa-5bdf-4dff-af86-f7158c23bfa7
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
# DataSpace Object (RDS)
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
          <caps:sentence sentenceid="41182eccd33d7ef1743065f133c89c47" id="tgt5" class="tgtSentence">Creates client-side proxies to custom business objects located on the middle tier.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="590daef9cefba70ed9acea7225512d0f" id="tgt6" class="tgtSentence">Remote Data Service needs business object proxies so that client-side components can communicate with business objects located on the middle tier.</caps:sentence>
          <caps:sentence sentenceid="459d68e53942c9ae9a39e459596bf11c" id="tgt7" class="tgtSentence"> Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> data across process or machine boundaries.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="65f47ea3c9f8ab02919bcaa86bad7d00" id="tgt8" class="tgtSentence">Remote Data Service uses the <legacyBold>RDS.DataSpace</legacyBold> object's <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method to create business object proxies.</caps:sentence>
          <caps:sentence sentenceid="bf688afcc84bf2903312739520ba3019" id="tgt9" class="tgtSentence"> The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created.</caps:sentence>
          <caps:sentence sentenceid="bcb5e49b5406368c5d372188726e7ed1" id="tgt10" class="tgtSentence"> Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="46dee9dbb5acda7cada0e200624c648f" id="tgt11" class="tgtSentence">RDS behaves in a "stateless" manner when the <legacyBold>RDS.DataSpace</legacyBold> object uses the HTTP or HTTPS protocols.</caps:sentence>
            <caps:sentence sentenceid="d9b1cc717e17590fc4bfc1445016ae17" id="tgt12" class="tgtSentence"> That is, any internal information about a client request is discarded after the server returns a response.</caps:sentence>
          </para>
        </alert>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="1b6fd0c20150368156be81ed2198c1cd" id="tgt13" class="tgtSentence">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request.</caps:sentence>
            <caps:sentence sentenceid="0bf1fd204d7e4ebc945a710c78284195" id="tgt14" class="tgtSentence"> When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object.</caps:sentence>
            <caps:sentence sentenceid="4256d33ae9f068e6dd3fa9656fcd345b" id="tgt15" class="tgtSentence"> After the business object responds to the request, the server destroys the business object and closes the connection.</caps:sentence>
          </para>
        </alert>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="c98ed19c583e78635564e4e92f5ceebb" id="tgt16" class="tgtSentence">This behavior means you cannot pass data from one request to another using a business object property or variable.</caps:sentence>
            <caps:sentence sentenceid="9555a0976aec4ae72be75ec0ba27725f" id="tgt17" class="tgtSentence"> You must employ some other mechanism, such as a file or a method argument, to persist state data.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="c914a21af88d69f974314368d1655ef5" id="tgt18" class="tgtSentence">The class ID for the <legacyBold>RDS.DataSpace</legacyBold> object is BD96C556-65A3-11D0-983A-00C04FC29E36.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7d34d8c21df8dc98076e5f7a4281a7b2" id="tgt19" class="tgtSentence">The <legacyBold>DataSpace</legacyBold> object is safe for scripting.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt20" class="tgtSentence">This section contains the following topic.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="a4af7e0f18c6c011193844bbc59771f0" id="tgt21" class="tgtSentence">
                <legacyLink xlink:href="c4a1f2e7-19ff-465e-9d9a-275ac0f4dc6a">DataSpace Object (RDS) Properties, Methods, and Events</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="12b0e160-5e5c-441f-bed7-ac0bd061e003">VBScript Example</link>
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
          <caps:sentence id="src5" class="srcSentence">Creates client-side proxies to custom business objects located on the middle tier.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">Remote Data Service needs business object proxies so that client-side components can communicate with business objects located on the middle tier.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> data across process or machine boundaries.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">Remote Data Service uses the <legacyBold>RDS.DataSpace</legacyBold> object's <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method to create business object proxies.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src11" class="srcSentence">RDS behaves in a "stateless" manner when the <legacyBold>RDS.DataSpace</legacyBold> object uses the HTTP or HTTPS protocols.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> That is, any internal information about a client request is discarded after the server returns a response.</caps:sentence>
          </para>
        </alert>
        <alert class="note">
          <para>
            <caps:sentence id="src13" class="srcSentence">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> After the business object responds to the request, the server destroys the business object and closes the connection.</caps:sentence>
          </para>
        </alert>
        <alert class="note">
          <para>
            <caps:sentence id="src16" class="srcSentence">This behavior means you cannot pass data from one request to another using a business object property or variable.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> You must employ some other mechanism, such as a file or a method argument, to persist state data.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src18" class="srcSentence">The class ID for the <legacyBold>RDS.DataSpace</legacyBold> object is BD96C556-65A3-11D0-983A-00C04FC29E36.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src19" class="srcSentence">The <legacyBold>DataSpace</legacyBold> object is safe for scripting.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src20" class="srcSentence">This section contains the following topic.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src21" class="srcSentence">
                <legacyLink xlink:href="c4a1f2e7-19ff-465e-9d9a-275ac0f4dc6a">DataSpace Object (RDS) Properties, Methods, and Events</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="12b0e160-5e5c-441f-bed7-ac0bd061e003">VBScript Example</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
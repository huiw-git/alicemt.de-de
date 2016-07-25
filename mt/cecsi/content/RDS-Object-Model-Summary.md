---
title: "RDS Object Model Summary"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 909f9af7-31db-4eec-ad52-650ce74dac2f
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
# RDS Object Model Summary
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
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a8cfde6331bd59eb2ac96f8911c4b666" id="tgt5" class="tgtSentence">Object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt6" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9d2129a620e95cd7d500c337bf0a691d" id="tgt7" class="tgtSentence">
                    <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2793c75e34b643b6db43720d811275ce" id="tgt8" class="tgtSentence">This object contains a method to obtain a server proxy.</caps:sentence>
                  <caps:sentence sentenceid="b7d1d9f7bb2b4a09640192e2be107d4f" id="tgt9" class="tgtSentence"> The proxy may be the default or a custom server program (business object).</caps:sentence>
                  <caps:sentence sentenceid="c5cddf3df085615f2206e6815ecb7342" id="tgt10" class="tgtSentence"> The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="7d34d8c21df8dc98076e5f7a4281a7b2" id="tgt11" class="tgtSentence">The <legacyBold>DataSpace</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="626c0eae4ab6b27314c2b71dcbbc165b" id="tgt12" class="tgtSentence">
                    <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="04de93dfe4a1b5e6d7bf4514a09c07f7" id="tgt13" class="tgtSentence">This object represents the default server program.</caps:sentence>
                  <caps:sentence sentenceid="e4af4aa46285f5e1485d0e5f22f31f04" id="tgt14" class="tgtSentence"> It executes the default RDS data retrieval and update behavior.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="82b1226bccf255679e6095923fee537d" id="tgt15" class="tgtSentence">The <legacyBold>DataFactory</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="584f508cc617e7e5444f492b9ba6ad4d" id="tgt16" class="tgtSentence">
                    <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5509c66ce3c5b298f0e267bfcbce82f2" id="tgt17" class="tgtSentence">This object can automatically invoke the <legacyBold>RDS.DataSpace</legacyBold> and <legacyBold>RDSServer.DataFactory</legacyBold> objects.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="743a04796850751ec4929e7a791e7976" id="tgt18" class="tgtSentence">Use this object to invoke the default RDS data retrieval or update behavior.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="aa83cad218e49ced2d0ef7d314b6e052" id="tgt19" class="tgtSentence">This object also provides the means for visual controls to access the returned <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="28f049480346ad6d467b76d12e8663d9" id="tgt20" class="tgtSentence">The <legacyBold>DataControl</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
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
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">
                    <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">This object contains a method to obtain a server proxy.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> The proxy may be the default or a custom server program (business object).</caps:sentence>
                  <caps:sentence id="src10" class="srcSentence"> The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src11" class="srcSentence">The <legacyBold>DataSpace</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">
                    <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">This object represents the default server program.</caps:sentence>
                  <caps:sentence id="src14" class="srcSentence"> It executes the default RDS data retrieval and update behavior.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src15" class="srcSentence">The <legacyBold>DataFactory</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">
                    <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">This object can automatically invoke the <legacyBold>RDS.DataSpace</legacyBold> and <legacyBold>RDSServer.DataFactory</legacyBold> objects.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Use this object to invoke the default RDS data retrieval or update behavior.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src19" class="srcSentence">This object also provides the means for visual controls to access the returned <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src20" class="srcSentence">The <legacyBold>DataControl</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
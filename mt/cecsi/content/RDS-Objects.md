---
title: "RDS Objects"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f2ac8b3b-f968-41c4-a504-7aee3538b7c7
caps.latest.revision: 16
caps.handback.revision: 16
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
# RDS Objects
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerOrientationDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
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
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">
                    <caps:sentence sentenceid="47714cd41e121094ee7a15f22679a18c" id="tgt5" class="tgtSentence">DataControl (RDS)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1b14627e46816649871f6caa5a555c59" id="tgt6" class="tgtSentence">Binds a data query <legacyBold>Recordset</legacyBold> to one or more controls (for example, a text box, grid control, or combo box) to display the <legacyBold>Recordset</legacyBold> data on a Web page.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="28f049480346ad6d467b76d12e8663d9" id="tgt7" class="tgtSentence">The <legacyBold>DataControl</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">
                    <caps:sentence sentenceid="b7c58cea367bd2e656b2c50f6e61481a" id="tgt8" class="tgtSentence">DataFactory (RDSServer)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="446cff1155167e5c758db48a568db079" id="tgt9" class="tgtSentence">Implements methods that provide read/write data access to specified data sources for client-side applications.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="82b1226bccf255679e6095923fee537d" id="tgt10" class="tgtSentence">The <legacyBold>DataFactory</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">
                    <caps:sentence sentenceid="a5cf1fa4a9813cfdc46cbd2fc2ab68f7" id="tgt11" class="tgtSentence">DataSpace (RDS)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="41182eccd33d7ef1743065f133c89c47" id="tgt12" class="tgtSentence">Creates client-side proxies to custom business objects located on the middle tier.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="7d34d8c21df8dc98076e5f7a4281a7b2" id="tgt13" class="tgtSentence">The <legacyBold>DataSpace</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="01044c3a-ed38-4144-bc43-fe38a6d22d04">IRDSService Interface (RDS)</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="70e9c15e895d8cfd856a5d3be02cd932" id="tgt14" class="tgtSentence">Exposes the <link xlink:href="ad45c676-ec7e-4a3a-9a6b-a54f75eb3012">InvokeService (RDS)</link> method, which is used to return a pointer to the requested interface on a more capable version of the object.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="ca9fa99e-1a9f-4deb-80d4-6942555fb22a">RDS API Reference</link>
      </relatedTopics>
    </developerOrientationDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerOrientationDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
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
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">
                    <caps:sentence id="src5" class="srcSentence">DataControl (RDS)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Binds a data query <legacyBold>Recordset</legacyBold> to one or more controls (for example, a text box, grid control, or combo box) to display the <legacyBold>Recordset</legacyBold> data on a Web page.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src7" class="srcSentence">The <legacyBold>DataControl</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">
                    <caps:sentence id="src8" class="srcSentence">DataFactory (RDSServer)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Implements methods that provide read/write data access to specified data sources for client-side applications.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src10" class="srcSentence">The <legacyBold>DataFactory</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">
                    <caps:sentence id="src11" class="srcSentence">DataSpace (RDS)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Creates client-side proxies to custom business objects located on the middle tier.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src13" class="srcSentence">The <legacyBold>DataSpace</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="01044c3a-ed38-4144-bc43-fe38a6d22d04">IRDSService Interface (RDS)</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Exposes the <link xlink:href="ad45c676-ec7e-4a3a-9a6b-a54f75eb3012">InvokeService (RDS)</link> method, which is used to return a pointer to the requested interface on a more capable version of the object.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="ca9fa99e-1a9f-4deb-80d4-6942555fb22a">RDS API Reference</link>
      </relatedTopics>
    </developerOrientationDocument>
  </caps:SxSSource>
</caps:SxS>
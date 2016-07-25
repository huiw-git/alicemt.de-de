---
title: "Server Property (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d2727ce7-da9f-4271-ae3c-9334ef477c14
caps.latest.revision: 15
caps.handback.revision: 15
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
# Server Property (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d83384173b7083a80591fa427e48f892" id="tgt1" class="tgtSentence">Indicates the Internet Information Services (IIS) name and communication protocol.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c465c133dce14a8824d6850fbaf4fdfb" id="tgt2" class="tgtSentence">You can set the <unmanagedCodeEntityReference>Server</unmanagedCodeEntityReference> property at design time in the OBJECT tags of the<legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0"> RDS.DataControl</legacyLink> object, or at run time in scripting code.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt7" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="81788ba0d7d02d81c063dbca621ba11b" id="tgt8" class="tgtSentence">Protocol</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0bf989a585ac714d8015a6791134393e" id="tgt9" class="tgtSentence">Design-time syntax</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="80791b3ae7002cb88c246876d9faa8f8" id="tgt10" class="tgtSentence">HTTP</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <codeFeaturedElement>&lt;PARAM NAME="Server" VALUE="http:</codeFeaturedElement>
                    <legacyItalic>//awebsrvr:port</legacyItalic>
                    <codeFeaturedElement>"&gt;</codeFeaturedElement>
                  </code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5e056c500a1c4b6a7110b50d807bade5" id="tgt11" class="tgtSentence">HTTPS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <codeFeaturedElement>&lt;PARAM NAME="Server" VALUE="https:</codeFeaturedElement>//<legacyItalic>awebsrvr:port</legacyItalic><codeFeaturedElement>"&gt;</codeFeaturedElement></code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c14f7a73c9cca3dec4ca6c9c3e722f2b" id="tgt12" class="tgtSentence">DCOM</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <codeFeaturedElement>&lt;PARAM NAME="Server" VALUE="</codeFeaturedElement>
                    <legacyItalic>computername</legacyItalic>
                    <codeFeaturedElement>"&gt;</codeFeaturedElement>
                  </code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbd0c217f849f5c8cf3333884d9e7779" id="tgt13" class="tgtSentence">In-process</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <codeFeaturedElement>&lt;PARAM NAME="Server" VALUE=""&gt;</codeFeaturedElement>
                  </code>
                </TD>
              </tr>
            </tbody>
          </table>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="81788ba0d7d02d81c063dbca621ba11b" id="tgt14" class="tgtSentence">Protocol</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5a62a039b419caab17b837656988ec3a" id="tgt15" class="tgtSentence">Run-time syntax</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="80791b3ae7002cb88c246876d9faa8f8" id="tgt16" class="tgtSentence">HTTP</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <legacyItalic>DataControl</legacyItalic>
                    <codeFeaturedElement>.Server="http://</codeFeaturedElement>
                    <legacyItalic>awebsrvr:port</legacyItalic>
                    <codeFeaturedElement>"</codeFeaturedElement>
                  </code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5e056c500a1c4b6a7110b50d807bade5" id="tgt17" class="tgtSentence">HTTPS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <legacyItalic>DataControl</legacyItalic>.<codeFeaturedElement>Server="https://</codeFeaturedElement><legacyItalic>awebsrvr:port</legacyItalic><codeFeaturedElement>"</codeFeaturedElement></code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c14f7a73c9cca3dec4ca6c9c3e722f2b" id="tgt18" class="tgtSentence">DCOM</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <legacyItalic>DataControl</legacyItalic>.<codeFeaturedElement>Server="</codeFeaturedElement><legacyItalic>computername</legacyItalic><codeFeaturedElement>"</codeFeaturedElement></code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbd0c217f849f5c8cf3333884d9e7779" id="tgt19" class="tgtSentence">In-process</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <legacyItalic>DataControl</legacyItalic>.<codeFeaturedElement>Server=""</codeFeaturedElement></code>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt20" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="4dd607ff80b91d1263aabc56b0a82fa7" id="tgt21" class="tgtSentence">
                <legacyItalic>awebsrvr</legacyItalic>or <legacyItalic>computername</legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b662417b518c693c92c1b899722ac5af" id="tgt22" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="901555fb06e346cb065ceb9808dcfc25" id="tgt23" class="tgtSentence">port</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt24" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="21d8bec3f8e96d5778f2520f06a2ed87" id="tgt25" class="tgtSentence"> A port that is used to connect to a server running IIS.</caps:sentence>
                <caps:sentence sentenceid="8759b881b33c3464a48f7b04b4b90319" id="tgt26" class="tgtSentence"> The port number is set in Internet Explorer (on the <legacyBold>View</legacyBold> menu, click <legacyBold>Options</legacyBold>, and then select the <legacyBold>Connection</legacyBold> tab) or in IIS.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="5410803de64b24c3bce2e6be4e78df92" id="tgt27" class="tgtSentence">DataControl</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="828490da16877cdbdeeca7991f4d5603" id="tgt28" class="tgtSentence">An object variable that represents an <legacyBold>RDS.DataControl</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1cffe8b94801415cf55c46a3707db920" id="tgt29" class="tgtSentence">The server is the location where the <legacyBold>RDS.DataControl</legacyBold> request (that is, a query or update) is processed.</caps:sentence>
            <caps:sentence sentenceid="e005de9b7fa0fc81ad3ed16ef2beeabf" id="tgt30" class="tgtSentence"> By default, all requests are processed by the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object, <legacyLink xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">MSDFMAP.Handler</legacyLink> component, and <legacyLink xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">MSDFMAP.INI</legacyLink> file on the specified server.</caps:sentence>
            <caps:sentence sentenceid="78515b6ecefd6ddb8a24653d3f55b8e5" id="tgt31" class="tgtSentence"> Remember that when changing servers to reconcile settings in the old and new <legacyBold>MSDFMAP.INI</legacyBold> files.</caps:sentence>
            <caps:sentence sentenceid="7c19533a58558bd5fde790455748460f" id="tgt32" class="tgtSentence"> Incompatibilities may cause requests that succeed on one server to fail on another.</caps:sentence>
            <caps:sentence sentenceid="4eda1fc7f83f0f3010603fc42a4e52dd" id="tgt33" class="tgtSentence"> If the Server property is set to the empty string "", these objects will be used on the local computer.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt34" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0fe57af9-a4d0-4986-a2e3-beaa4d26ed58">VBScript Example</link>
        <link xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect Property (RDS)</link>
        <link xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL Property (RDS)</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the Internet Information Services (IIS) name and communication protocol.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">You can set the <unmanagedCodeEntityReference>Server</unmanagedCodeEntityReference> property at design time in the OBJECT tags of the<legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0"> RDS.DataControl</legacyLink> object, or at run time in scripting code.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Protocol</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Design-time syntax</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">HTTP</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <codeFeaturedElement>&lt;PARAM NAME="Server" VALUE="http:</codeFeaturedElement>
                    <legacyItalic>//awebsrvr:port</legacyItalic>
                    <codeFeaturedElement>"&gt;</codeFeaturedElement>
                  </code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">HTTPS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <codeFeaturedElement>&lt;PARAM NAME="Server" VALUE="https:</codeFeaturedElement>//<legacyItalic>awebsrvr:port</legacyItalic><codeFeaturedElement>"&gt;</codeFeaturedElement></code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">DCOM</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <codeFeaturedElement>&lt;PARAM NAME="Server" VALUE="</codeFeaturedElement>
                    <legacyItalic>computername</legacyItalic>
                    <codeFeaturedElement>"&gt;</codeFeaturedElement>
                  </code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">In-process</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <codeFeaturedElement>&lt;PARAM NAME="Server" VALUE=""&gt;</codeFeaturedElement>
                  </code>
                </TD>
              </tr>
            </tbody>
          </table>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Protocol</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Run-time syntax</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">HTTP</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <legacyItalic>DataControl</legacyItalic>
                    <codeFeaturedElement>.Server="http://</codeFeaturedElement>
                    <legacyItalic>awebsrvr:port</legacyItalic>
                    <codeFeaturedElement>"</codeFeaturedElement>
                  </code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">HTTPS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <legacyItalic>DataControl</legacyItalic>.<codeFeaturedElement>Server="https://</codeFeaturedElement><legacyItalic>awebsrvr:port</legacyItalic><codeFeaturedElement>"</codeFeaturedElement></code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">DCOM</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <legacyItalic>DataControl</legacyItalic>.<codeFeaturedElement>Server="</codeFeaturedElement><legacyItalic>computername</legacyItalic><codeFeaturedElement>"</codeFeaturedElement></code>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">In-process</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <code>
                    <legacyItalic>DataControl</legacyItalic>.<codeFeaturedElement>Server=""</codeFeaturedElement></code>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src21" class="srcSentence">
                <legacyItalic>awebsrvr</legacyItalic>or <legacyItalic>computername</legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src22" class="srcSentence">A <languageKeyword>String</languageKeyword> value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src23" class="srcSentence">port</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src24" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> A port that is used to connect to a server running IIS.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> The port number is set in Internet Explorer (on the <legacyBold>View</legacyBold> menu, click <legacyBold>Options</legacyBold>, and then select the <legacyBold>Connection</legacyBold> tab) or in IIS.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src27" class="srcSentence">DataControl</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src28" class="srcSentence">An object variable that represents an <legacyBold>RDS.DataControl</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">The server is the location where the <legacyBold>RDS.DataControl</legacyBold> request (that is, a query or update) is processed.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> By default, all requests are processed by the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object, <legacyLink xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">MSDFMAP.Handler</legacyLink> component, and <legacyLink xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">MSDFMAP.INI</legacyLink> file on the specified server.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> Remember that when changing servers to reconcile settings in the old and new <legacyBold>MSDFMAP.INI</legacyBold> files.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> Incompatibilities may cause requests that succeed on one server to fail on another.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> If the Server property is set to the empty string "", these objects will be used on the local computer.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src34" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0fe57af9-a4d0-4986-a2e3-beaa4d26ed58">VBScript Example</link>
        <link xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect Property (RDS)</link>
        <link xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL Property (RDS)</link>
        <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
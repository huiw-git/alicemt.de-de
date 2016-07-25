---
title: "Understanding the Customization File"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 136f74bf-8d86-4a41-be66-c86cbcf81548
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
# Understanding the Customization File
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="980f2cf175d84434efcc25c10edae8e7" id="tgt1" class="tgtSentence">Each section header in the customization file consists of square brackets (<legacyBold>[]</legacyBold>) containing a type and parameter.</caps:sentence>
          <caps:sentence sentenceid="caa23f1aef45eef0181abba1016ff55b" id="tgt2" class="tgtSentence"> The four section types are indicated by the literal strings <legacyBold>connect</legacyBold>, <legacyBold>sql</legacyBold>, <legacyBold>userlist</legacyBold>, or <legacyBold>logs</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="db1fd31ed0dbd23202f07c554413bfa1" id="tgt3" class="tgtSentence"> The parameter is the literal string, the default, a user-specified identifier, or nothing.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt4" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt5" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt6" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt7" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="5d45d0aa068d347c494e3b57e6265d70" id="tgt8" class="tgtSentence">Therefore, each section is marked with one of the following section headers: </caps:sentence>
        </para>
        <code>
          <codeFeaturedElement>[ connect</codeFeaturedElement>
          <codeFeaturedElement>default ]</codeFeaturedElement>
          <codeFeaturedElement>[ connect  </codeFeaturedElement>
          <legacyItalic>identifier </legacyItalic>
          <codeFeaturedElement>]</codeFeaturedElement>
          <codeFeaturedElement>[ sql  default ]</codeFeaturedElement>
          <codeFeaturedElement>[ sql  </codeFeaturedElement>
          <legacyItalic>identifier </legacyItalic>
          <codeFeaturedElement>]</codeFeaturedElement>
          <codeFeaturedElement>[ userlist  </codeFeaturedElement>
          <legacyItalic>identifier </legacyItalic>
          <codeFeaturedElement>]</codeFeaturedElement>
          <codeFeaturedElement>[ logs ]</codeFeaturedElement>
        </code>
        <para>
          <caps:sentence sentenceid="bc55e0e9ba883a60f533e30253afb288" id="tgt9" class="tgtSentence">The section headers have the following parts.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f4c9385f1902f7334b00b9b4ecd164de" id="tgt10" class="tgtSentence">Part</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt11" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b0aac5f9925017ea2cab54bc14d9ddfe" id="tgt12" class="tgtSentence">               <legacyBold>connect</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ca3f5a4f5b2f97e37201d4b8797cb0b5" id="tgt13" class="tgtSentence">A literal string that modifies a connection string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6dd550bfdf1bebf1edba8f236ce4c20f" id="tgt14" class="tgtSentence">               <legacyBold>sql</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="12b3de47b6d577477bc16188c079b7e7" id="tgt15" class="tgtSentence">A literal string that modifies a command string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7273f124b2ad2f2c4b426ac9a10fb584" id="tgt16" class="tgtSentence">               <legacyBold>userlist</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6d2d1bb5180d6191bc87b129bb1970e8" id="tgt17" class="tgtSentence">A literal string that modifies the access rights of a specific user.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="93d04cc9804a8b011d3c29a55baf1f53" id="tgt18" class="tgtSentence">               <legacyBold>logs</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4e36233de2eccae1835a9fb64f3751a8" id="tgt19" class="tgtSentence">A literal string that specifies a log file recording operational errors.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="90aea4943a7b8586ea23e5a71bb0f8b7" id="tgt20" class="tgtSentence">               <legacyBold>default</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cedf36ae20588ea5c99055e453c04142" id="tgt21" class="tgtSentence">A literal string that is used if no identifier is specified or found.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="511bcdb4f96be0c8f559a5e2c152833d" id="tgt22" class="tgtSentence">               <legacyItalic>identifier</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d5634368bcd32a524ebf3e80af76f59" id="tgt23" class="tgtSentence">A string that matches a string in the <legacyBold>connect</legacyBold> or <legacyBold>command</legacyBold> string.</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="d11e843f313a2fd2d631d930cfd82c2b" id="tgt24" class="tgtSentence">Use this section if the section header contains <legacyBold>connect</legacyBold> and the identifier string is found in the connection string.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="0fdcb97db577c6678315b7d6451a8a5e" id="tgt25" class="tgtSentence">Use this section if the section header contains <legacyBold>sql</legacyBold> and the identifier string is found in the command string.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="0560dffd0d73b1aa7c236d10495ea25b" id="tgt26" class="tgtSentence">Use this section if the section header contains <legacyBold>userlist</legacyBold> and the identifier string matches a <legacyBold>connect</legacyBold> section identifier.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="cde666de459dc5b04351486f7fcfc9c9" id="tgt27" class="tgtSentence">The <legacyBold>DataFactory</legacyBold> calls the handler, passing client parameters.</caps:sentence>
          <caps:sentence sentenceid="6b1942aac6242ed233d41dc5d312cf97" id="tgt28" class="tgtSentence"> The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers.</caps:sentence>
          <caps:sentence sentenceid="96d6f7b1378a3e8b4caee45f778ef90c" id="tgt29" class="tgtSentence"> If a match is found, the contents of that section are applied to the client parameter.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="950dc46951e2fb80536d3a12f85252cc" id="tgt30" class="tgtSentence">A particular section is used under the following circumstances:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="aa82984f1b7f703db02566d330747aa8" id="tgt31" class="tgtSentence">A <legacyBold>connect</legacyBold> section is used if the value part of the client connect string keyword, "<legacyBold>Data Source=</legacyBold><legacyItalic>value</legacyItalic>", matches a <legacyBold>connect</legacyBold> section identifier<legacyItalic>.</legacyItalic></caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b4c60eefb38a7e48675dec6c7f81f3ac" id="tgt32" class="tgtSentence">An <legacyBold>sql</legacyBold> section is used if the client command string contains a string that matches an <legacyBold>sql</legacyBold> section identifier.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d19aaab342a0a1354fcc9623ee2b1923" id="tgt33" class="tgtSentence">A <legacyBold>connect</legacyBold> or <legacyBold>sql</legacyBold> section with a default parameter is used if there is no matching identifier.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9c967afa5e52202bc23baf4d33a08df0" id="tgt34" class="tgtSentence">A <legacyBold>userlist</legacyBold> section is used if the <legacyBold>userlist</legacyBold> section identifier matches a <legacyBold>connect</legacyBold> section identifier.</caps:sentence>
              <caps:sentence sentenceid="ef1867f3b99d77d2b046592266582e10" id="tgt35" class="tgtSentence"> If there is a match, the contents of the <legacyBold>userlist</legacyBold> section are applied to the connection governed by the <legacyBold>connect</legacyBold> section.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="094d1765cfac86941d079bbaffdec838" id="tgt36" class="tgtSentence">If the string in a connection or command string does not match the identifier in any <legacyBold>connect</legacyBold> or <legacyBold>sql</legacyBold> section header, and there is no <legacyBold>connect</legacyBold> or <legacyBold>sql</legacyBold> section header with a default parameter, then the client string is used without modification.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ad1bf294bbb09dda9832dc47b3b760ed" id="tgt37" class="tgtSentence">The <legacyBold>logs</legacyBold> section is used whenever the <legacyBold>DataFactory</legacyBold> is in operation.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Each section header in the customization file consists of square brackets (<legacyBold>[]</legacyBold>) containing a type and parameter.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The four section types are indicated by the literal strings <legacyBold>connect</legacyBold>, <legacyBold>sql</legacyBold>, <legacyBold>userlist</legacyBold>, or <legacyBold>logs</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The parameter is the literal string, the default, a user-specified identifier, or nothing.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src4" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src8" class="srcSentence">Therefore, each section is marked with one of the following section headers: </caps:sentence>
        </para>
        <code>
          <codeFeaturedElement>[ connect</codeFeaturedElement>
          <codeFeaturedElement>default ]</codeFeaturedElement>
          <codeFeaturedElement>[ connect  </codeFeaturedElement>
          <legacyItalic>identifier </legacyItalic>
          <codeFeaturedElement>]</codeFeaturedElement>
          <codeFeaturedElement>[ sql  default ]</codeFeaturedElement>
          <codeFeaturedElement>[ sql  </codeFeaturedElement>
          <legacyItalic>identifier </legacyItalic>
          <codeFeaturedElement>]</codeFeaturedElement>
          <codeFeaturedElement>[ userlist  </codeFeaturedElement>
          <legacyItalic>identifier </legacyItalic>
          <codeFeaturedElement>]</codeFeaturedElement>
          <codeFeaturedElement>[ logs ]</codeFeaturedElement>
        </code>
        <para>
          <caps:sentence id="src9" class="srcSentence">The section headers have the following parts.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Part</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">               <legacyBold>connect</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">A literal string that modifies a connection string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">               <legacyBold>sql</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">A literal string that modifies a command string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">               <legacyBold>userlist</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">A literal string that modifies the access rights of a specific user.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">               <legacyBold>logs</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">A literal string that specifies a log file recording operational errors.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">               <legacyBold>default</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">A literal string that is used if no identifier is specified or found.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">               <legacyItalic>identifier</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">A string that matches a string in the <legacyBold>connect</legacyBold> or <legacyBold>command</legacyBold> string.</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src24" class="srcSentence">Use this section if the section header contains <legacyBold>connect</legacyBold> and the identifier string is found in the connection string.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src25" class="srcSentence">Use this section if the section header contains <legacyBold>sql</legacyBold> and the identifier string is found in the command string.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src26" class="srcSentence">Use this section if the section header contains <legacyBold>userlist</legacyBold> and the identifier string matches a <legacyBold>connect</legacyBold> section identifier.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src27" class="srcSentence">The <legacyBold>DataFactory</legacyBold> calls the handler, passing client parameters.</caps:sentence>
          <caps:sentence id="src28" class="srcSentence"> The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers.</caps:sentence>
          <caps:sentence id="src29" class="srcSentence"> If a match is found, the contents of that section are applied to the client parameter.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src30" class="srcSentence">A particular section is used under the following circumstances:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src31" class="srcSentence">A <legacyBold>connect</legacyBold> section is used if the value part of the client connect string keyword, "<legacyBold>Data Source=</legacyBold><legacyItalic>value</legacyItalic>", matches a <legacyBold>connect</legacyBold> section identifier<legacyItalic>.</legacyItalic></caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src32" class="srcSentence">An <legacyBold>sql</legacyBold> section is used if the client command string contains a string that matches an <legacyBold>sql</legacyBold> section identifier.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src33" class="srcSentence">A <legacyBold>connect</legacyBold> or <legacyBold>sql</legacyBold> section with a default parameter is used if there is no matching identifier.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src34" class="srcSentence">A <legacyBold>userlist</legacyBold> section is used if the <legacyBold>userlist</legacyBold> section identifier matches a <legacyBold>connect</legacyBold> section identifier.</caps:sentence>
              <caps:sentence id="src35" class="srcSentence"> If there is a match, the contents of the <legacyBold>userlist</legacyBold> section are applied to the connection governed by the <legacyBold>connect</legacyBold> section.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src36" class="srcSentence">If the string in a connection or command string does not match the identifier in any <legacyBold>connect</legacyBold> or <legacyBold>sql</legacyBold> section header, and there is no <legacyBold>connect</legacyBold> or <legacyBold>sql</legacyBold> section header with a default parameter, then the client string is used without modification.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src37" class="srcSentence">The <legacyBold>logs</legacyBold> section is used whenever the <legacyBold>DataFactory</legacyBold> is in operation.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
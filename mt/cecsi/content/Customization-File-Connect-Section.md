---
title: "Customization File Connect Section"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d50eb3cc-a822-486f-b80b-65bb50547ecd
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
# Customization File Connect Section
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7b50edc250ced18bd19190b616a27108" id="tgt1" class="tgtSentence">The default behavior of the handler is to deny all connections.</caps:sentence>
          <caps:sentence sentenceid="f5c09728383d6094a2ca39a49e0b0126" id="tgt2" class="tgtSentence"> The <legacyBold>connect</legacyBold> section specifies exceptions to that behavior.</caps:sentence>
          <caps:sentence sentenceid="b93dc1045a97b83387e861c65e680926" id="tgt3" class="tgtSentence"> For example, if all the <legacyBold>connect</legacyBold> sections were absent or empty, then by default no connections could be made.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="87607a7c9edf35b2a56d8cbc6de10690" id="tgt4" class="tgtSentence">The <legacyBold>connect</legacyBold> section can contain:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="a73ff88609c5e08e330d6c747a522470" id="tgt5" class="tgtSentence">A default access entry that specifies the default read and write operations allowed on this connection.</caps:sentence>
              <caps:sentence sentenceid="866eb728da9dbb8b90b2568010816ba0" id="tgt6" class="tgtSentence"> If there is no default access entry in the section, the section will be ignored.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5eff0d60e8e90a7806943d856f3dad2a" id="tgt7" class="tgtSentence">A new connection string that replaces the client connection string.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt8" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt9" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt10" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt11" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt12" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e389f1fc0753a22ee45a6c86050dbad5" id="tgt13" class="tgtSentence">A default access entry is of the form:</caps:sentence>
          </para>
          <code>
            <codeFeaturedElement>Access=</codeFeaturedElement>
            <legacyItalic>accessRight</legacyItalic>
          </code>
          <para>
            <caps:sentence sentenceid="e6ad191a3883b7b5cf1e9ab14d755835" id="tgt14" class="tgtSentence">A replacement connection string entry is of the form:</caps:sentence>
          </para>
          <code>
            <codeFeaturedElement>Connect=</codeFeaturedElement>
            <legacyItalic>connectionString</legacyItalic>
          </code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f4c9385f1902f7334b00b9b4ecd164de" id="tgt15" class="tgtSentence">Part</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt16" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b0aac5f9925017ea2cab54bc14d9ddfe" id="tgt17" class="tgtSentence">               <legacyBold>Connect</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="839b3c19ecb39103b8aa63b521649bb0" id="tgt18" class="tgtSentence">A literal string that indicates this is a connection string entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bebba15eace506e1785f4593852ed1d0" id="tgt19" class="tgtSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>connectionString</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="903244269bb2dfdcbd552a17fba3e81b" id="tgt20" class="tgtSentence">A string that replaces the whole client connection string.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="642ef32af3b3c814f3a25a0db94605e2" id="tgt21" class="tgtSentence">               <legacyBold>Access</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62994285b6c06c1e41ef0d80c07be586" id="tgt22" class="tgtSentence">A literal string that indicates this is an access entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0f7c4099affad257934cff34f605e05d" id="tgt23" class="tgtSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>accessRight</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e54cdf7fb604c370ce1fd97b522a9adb" id="tgt24" class="tgtSentence">One of the following access rights:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="094852ba98234868328f46fb588f331c" id="tgt25" class="tgtSentence">                   <legacyBold>NoAccess </legacyBold>— User cannot access the data source.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="e644167d860b296395f79195d690b3c7" id="tgt26" class="tgtSentence">                   <legacyBold>ReadOnly </legacyBold>— User can read the data source.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="e86ed39232883f88ad312554f59e12ac" id="tgt27" class="tgtSentence">                   <legacyBold>ReadWrite </legacyBold>— User can read or write to the data source.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="4cb019ce82929e5727d8a75bf462b864" id="tgt28" class="tgtSentence">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the <legacyBold>connect default </legacyBold>section to <codeInline>Access=ReadWrite</codeInline>, and delete or comment out any other <legacyBold>connect </legacyBold><legacyItalic>identifier </legacyItalic>section.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</link>
        <link xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The default behavior of the handler is to deny all connections.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyBold>connect</legacyBold> section specifies exceptions to that behavior.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For example, if all the <legacyBold>connect</legacyBold> sections were absent or empty, then by default no connections could be made.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">The <legacyBold>connect</legacyBold> section can contain:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">A default access entry that specifies the default read and write operations allowed on this connection.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> If there is no default access entry in the section, the section will be ignored.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">A new connection string that replaces the client connection string.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence id="src8" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">A default access entry is of the form:</caps:sentence>
          </para>
          <code>
            <codeFeaturedElement>Access=</codeFeaturedElement>
            <legacyItalic>accessRight</legacyItalic>
          </code>
          <para>
            <caps:sentence id="src14" class="srcSentence">A replacement connection string entry is of the form:</caps:sentence>
          </para>
          <code>
            <codeFeaturedElement>Connect=</codeFeaturedElement>
            <legacyItalic>connectionString</legacyItalic>
          </code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Part</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">               <legacyBold>Connect</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">A literal string that indicates this is a connection string entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>connectionString</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">A string that replaces the whole client connection string.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">               <legacyBold>Access</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">A literal string that indicates this is an access entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>accessRight</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">One of the following access rights:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">                   <legacyBold>NoAccess </legacyBold>— User cannot access the data source.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">                   <legacyBold>ReadOnly </legacyBold>— User can read the data source.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">                   <legacyBold>ReadWrite </legacyBold>— User can read or write to the data source.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src28" class="srcSentence">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the <legacyBold>connect default </legacyBold>section to <codeInline>Access=ReadWrite</codeInline>, and delete or comment out any other <legacyBold>connect </legacyBold><legacyItalic>identifier </legacyItalic>section.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</link>
        <link xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
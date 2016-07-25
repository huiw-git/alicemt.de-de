---
title: "Customization File UserList Section"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 42e8ec20-eaac-4a95-8cb8-4bba93a75bcb
caps.latest.revision: 11
caps.handback.revision: 11
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
# Customization File UserList Section
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="48dae832efc324429828fd62ae7d232a" id="tgt1" class="tgtSentence">The <legacyBold>userlist</legacyBold> section pertains to the <legacyBold>connect</legacyBold> section with the same section <legacyItalic>identifier</legacyItalic> parameter.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="881a71f4b9b8f0b80946ba4a24ba17d9" id="tgt2" class="tgtSentence">This section can contain a <legacyItalic>user access entry</legacyItalic>, which specifies access rights for the specified user and overrides the <legacyItalic>default</legacyItalic> <legacyItalic>access entry </legacyItalic>in the matching <legacyBold>connect</legacyBold> section.</caps:sentence>
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
          <para>
            <caps:sentence sentenceid="5eedf05c65c8033fee7a4d275aca5b52" id="tgt8" class="tgtSentence">A user access entry is of the form:</caps:sentence>
          </para>
          <para>
            <legacyItalic>
              <caps:sentence sentenceid="14c4b06b824ec593239362517f538b29" id="tgt9" class="tgtSentence">userName</caps:sentence>
            </legacyItalic>
            <legacyBold>
              <caps:sentence sentenceid="43ec3e5dee6e706af7766fffea512721" id="tgt10" class="tgtSentence">=</caps:sentence>
            </legacyBold>
            <legacyBold>
              <legacyItalic>
                <caps:sentence sentenceid="e1963e6f3ed87bdf88b7ef87afdcb932" id="tgt11" class="tgtSentence">accessRights</caps:sentence>
              </legacyItalic>
            </legacyBold>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f4c9385f1902f7334b00b9b4ecd164de" id="tgt12" class="tgtSentence">Part</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt13" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence sentenceid="14c4b06b824ec593239362517f538b29" id="tgt14" class="tgtSentence">userName</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1cb44e4a25ccb61981636191422a0abd" id="tgt15" class="tgtSentence">The <legacyItalic>user name</legacyItalic> of the person employing this connection.</caps:sentence>
                    <caps:sentence sentenceid="b25d8f027815a44e099c51d7c63e35b0" id="tgt16" class="tgtSentence"> Valid user names are established with the IIS <legacyBold>Service Manager</legacyBold> dialog.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold></legacyBold>
                    <legacyBold>
                      <legacyItalic>
                        <caps:sentence sentenceid="e1963e6f3ed87bdf88b7ef87afdcb932" id="tgt17" class="tgtSentence">accessRights</caps:sentence>
                      </legacyItalic>
                    </legacyBold>
                    <legacyBold></legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e54cdf7fb604c370ce1fd97b522a9adb" id="tgt18" class="tgtSentence">One of the following access rights:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8d577dc5d83097d439173f5da75985f5" id="tgt19" class="tgtSentence">
                          <legacyBold>NoAccess</legacyBold> — User cannot access the data source.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c0d696e528f737e6fd44ce32f4f50412" id="tgt20" class="tgtSentence">
                          <legacyBold>ReadOnly</legacyBold> — User can read the data source.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d0d421ff024e38ac6c9133d95624556b" id="tgt21" class="tgtSentence">
                          <legacyBold>ReadWrite</legacyBold> — User can read or write to the data source.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>userlist</legacyBold> section pertains to the <legacyBold>connect</legacyBold> section with the same section <legacyItalic>identifier</legacyItalic> parameter.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">This section can contain a <legacyItalic>user access entry</legacyItalic>, which specifies access rights for the specified user and overrides the <legacyItalic>default</legacyItalic> <legacyItalic>access entry </legacyItalic>in the matching <legacyBold>connect</legacyBold> section.</caps:sentence>
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
          <para>
            <caps:sentence id="src8" class="srcSentence">A user access entry is of the form:</caps:sentence>
          </para>
          <para>
            <legacyItalic>
              <caps:sentence id="src9" class="srcSentence">userName</caps:sentence>
            </legacyItalic>
            <legacyBold>
              <caps:sentence id="src10" class="srcSentence">=</caps:sentence>
            </legacyBold>
            <legacyBold>
              <legacyItalic>
                <caps:sentence id="src11" class="srcSentence">accessRights</caps:sentence>
              </legacyItalic>
            </legacyBold>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Part</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence id="src14" class="srcSentence">userName</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">The <legacyItalic>user name</legacyItalic> of the person employing this connection.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> Valid user names are established with the IIS <legacyBold>Service Manager</legacyBold> dialog.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold></legacyBold>
                    <legacyBold>
                      <legacyItalic>
                        <caps:sentence id="src17" class="srcSentence">accessRights</caps:sentence>
                      </legacyItalic>
                    </legacyBold>
                    <legacyBold></legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">One of the following access rights:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">
                          <legacyBold>NoAccess</legacyBold> — User cannot access the data source.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">
                          <legacyBold>ReadOnly</legacyBold> — User can read the data source.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">
                          <legacyBold>ReadWrite</legacyBold> — User can read or write to the data source.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</link>
        <link xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
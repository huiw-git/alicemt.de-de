---
title: "Customization File Logs Section"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a368e264-865c-41ee-be00-d9097255c2ea
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
# Customization File Logs Section
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="424669f5352e91358c313b49b40e9c7c" id="tgt1" class="tgtSentence">The <legacyBold>logs</legacyBold> section contains a log file entry, which specifies the name of a file that records errors during the operation of the <legacyBold>DataFactory</legacyBold>.</caps:sentence>
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
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt6" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f91427f4f833fba546668bcb241720b5" id="tgt7" class="tgtSentence">A log file entry is of the form:</caps:sentence>
          </para>
          <code>
            <codeFeaturedElement>err=</codeFeaturedElement>
            <legacyItalic>FileName</legacyItalic>
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
                    <caps:sentence sentenceid="f4c9385f1902f7334b00b9b4ecd164de" id="tgt8" class="tgtSentence">Part</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt9" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6b77aaa499c582f6bc9ba2e3763a0bf2" id="tgt10" class="tgtSentence">               <legacyBold>err</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="971d3640a2e2382a92c7c59ca9a17e81" id="tgt11" class="tgtSentence">A literal string that indicates this is a log file entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="95f30aee648dfabd8cfe0036a7e902ac" id="tgt12" class="tgtSentence">               <legacyItalic>FileName</legacyItalic>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c9c7f5abecfab7ce35b23eb59d3c7119" id="tgt13" class="tgtSentence">A complete path and file name.</caps:sentence>
                    <caps:sentence sentenceid="684bc080f56d75d6b9029e0ea154ff4f" id="tgt14" class="tgtSentence"> The typical file name is <legacyBold>c:\msdfmap.log</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="c67a7f4c6594f8cfd7ad006d03d6876f" id="tgt15" class="tgtSentence">The log file will contain the user name, HRESULT, date, and time of each error.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>logs</legacyBold> section contains a log file entry, which specifies the name of a file that records errors during the operation of the <legacyBold>DataFactory</legacyBold>.</caps:sentence>
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
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">A log file entry is of the form:</caps:sentence>
          </para>
          <code>
            <codeFeaturedElement>err=</codeFeaturedElement>
            <legacyItalic>FileName</legacyItalic>
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
                    <caps:sentence id="src8" class="srcSentence">Part</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">               <legacyBold>err</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">A literal string that indicates this is a log file entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">               <legacyItalic>FileName</legacyItalic>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">A complete path and file name.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> The typical file name is <legacyBold>c:\msdfmap.log</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src15" class="srcSentence">The log file will contain the user name, HRESULT, date, and time of each error.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
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
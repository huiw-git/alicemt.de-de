---
title: "Customization File SQL Section"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e65c2871-9986-44ff-b8b7-7f5eda91b3fa
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
# Customization File SQL Section
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="858ca1a6374518481397de77cca834ac" id="tgt1" class="tgtSentence">The <legacyBold>sql</legacyBold> section can contain a new SQL string that replaces the client command string.</caps:sentence>
          <caps:sentence sentenceid="67ef9498a47e2391a7576fc87beedee7" id="tgt2" class="tgtSentence"> If there is no SQL string in the section, the section will be ignored.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="55adf269916fff90e0fca599b0682507" id="tgt7" class="tgtSentence">The new SQL string may be <legacyItalic>parameterized</legacyItalic>.</caps:sentence>
          <caps:sentence sentenceid="e751962c025d484bbcd3b5b34e0079bf" id="tgt8" class="tgtSentence"> That is, parameters in the <legacyBold>sql</legacyBold> section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an <legacyItalic>identifier</legacyItalic> in the client command string (designated by a comma-delimited list in parentheses).</caps:sentence>
          <caps:sentence sentenceid="d670af9ee1f9b4c0e23392f2b250ca0d" id="tgt9" class="tgtSentence"> The identifier and argument list behave like a function call.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b8f417353a6cb3e631c84585820d329e" id="tgt10" class="tgtSentence">For example, assume the client command string is <codeInline>"CustomerByID(4)"</codeInline>, the SQL section header is <codeInline>[SQL CustomerByID]</codeInline>, and the new SQL section string is <codeInline>"SELECT * FROM Customers WHERE CustomerID = ?". </codeInline>The Handler will generate <codeInline>"SELECT * FROM Customers WHERE CustomerID = 4"</codeInline> and use that string to query the data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a9daf74e9d1af82576667a2d90f5e6aa" id="tgt11" class="tgtSentence">If the new SQL statement is the null string (""), then the section is ignored.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="71fab35a34f90b015e94b84dbeaf51c3" id="tgt12" class="tgtSentence">If the new SQL statement string is not valid, then the execution of the statement will fail.</caps:sentence>
          <caps:sentence sentenceid="a3eae017d04438d2d91c54337bec8c1b" id="tgt13" class="tgtSentence"> The client parameter is effectively ignored.</caps:sentence>
          <caps:sentence sentenceid="b1685f7815ad6180d98cc8794e72c134" id="tgt14" class="tgtSentence"> You can do this intentionally to "turn off" all client SQL commands by specifying:</caps:sentence>
        </para>
        <code>[SQL default] 
SQL = " "</code>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt15" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0bd5c6b4e660804932b5b3aec2afe883" id="tgt16" class="tgtSentence">A replacement SQL string entry is of the form:</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ea14501049f0dc8e72fa2aaf45cf81d4" id="tgt17" class="tgtSentence">         <legacyBold>SQL=</legacyBold><legacyBold><legacyItalic>sqlString</legacyItalic></legacyBold>       </caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f4c9385f1902f7334b00b9b4ecd164de" id="tgt18" class="tgtSentence">Part</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt19" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6dd550bfdf1bebf1edba8f236ce4c20f" id="tgt20" class="tgtSentence">               <legacyBold>SQL</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1f2bc3f6f767b2c114bf89e1bacd813d" id="tgt21" class="tgtSentence">A literal string that indicates this is an SQL section entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c1fa43c91064bf56536ccfcede8b43a" id="tgt22" class="tgtSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>sqlString</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a69e04bdf80190f3d0b4c255f01ae7f3" id="tgt23" class="tgtSentence">An SQL string that replaces the client string.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>sql</legacyBold> section can contain a new SQL string that replaces the client command string.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> If there is no SQL string in the section, the section will be ignored.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src7" class="srcSentence">The new SQL string may be <legacyItalic>parameterized</legacyItalic>.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> That is, parameters in the <legacyBold>sql</legacyBold> section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an <legacyItalic>identifier</legacyItalic> in the client command string (designated by a comma-delimited list in parentheses).</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> The identifier and argument list behave like a function call.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">For example, assume the client command string is <codeInline>"CustomerByID(4)"</codeInline>, the SQL section header is <codeInline>[SQL CustomerByID]</codeInline>, and the new SQL section string is <codeInline>"SELECT * FROM Customers WHERE CustomerID = ?". </codeInline>The Handler will generate <codeInline>"SELECT * FROM Customers WHERE CustomerID = 4"</codeInline> and use that string to query the data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">If the new SQL statement is the null string (""), then the section is ignored.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">If the new SQL statement string is not valid, then the execution of the statement will fail.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> The client parameter is effectively ignored.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> You can do this intentionally to "turn off" all client SQL commands by specifying:</caps:sentence>
        </para>
        <code>[SQL default] 
SQL = " "</code>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src16" class="srcSentence">A replacement SQL string entry is of the form:</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">         <legacyBold>SQL=</legacyBold><legacyBold><legacyItalic>sqlString</legacyItalic></legacyBold>       </caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Part</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">               <legacyBold>SQL</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">A literal string that indicates this is an SQL section entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>sqlString</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">An SQL string that replaces the client string.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</link>
        <link xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
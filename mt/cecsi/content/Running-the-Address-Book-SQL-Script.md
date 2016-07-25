---
title: "Running the Address Book SQL Script"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 409b3f8b-0ced-4867-acbe-b245dcdf6702
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
# Running the Address Book SQL Script
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
          <caps:sentence sentenceid="e2b686df1d68f971ea7c07cf17352a51" id="tgt5" class="tgtSentence">You must use either the ISQL/Query Analyzer command-line utility or the SQL Server Enterprise Manager to run the included SQL script (Sampleemp.sql) that:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="fe33ee66a9ab9fe4afe59b8f7c102973" id="tgt6" class="tgtSentence">Creates a new database, AddrBookDB, on the default device.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="51f74f94c90a69a5db7ccf6a186e1164" id="tgt7" class="tgtSentence">Connects to the database, AddrBookDB.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="af00d52f1b740c98e5e5d50fc1a50f0b" id="tgt8" class="tgtSentence">Creates an Employee table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b55db05439ad34c01572873b8199b821" id="tgt9" class="tgtSentence">Populates the table with sample data.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1385bf6b1c83fd52c8937103d694f700" id="tgt10" class="tgtSentence">Runs a simple SELECT statement to verify the population of the database table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f0c6ffb2b8d0396729a77149a443ce54" id="tgt11" class="tgtSentence">Sets up a user account called "adcdemo" with a password of "adcdemo."</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="eb8d0bcaefc591d2cef3b3a26671ef34" id="tgt12" class="tgtSentence">To run the Sampleemp.sql script in Microsoft SQL Server 6.5</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5c18a3c2af4abd64df21d7a3324ff2ec" id="tgt13" class="tgtSentence">Click <legacyBold>Start</legacyBold>, point to <legacyBold>Programs</legacyBold>, and then point to <legacyBold>Microsoft SQL Server 6.5</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="b09cbd030d93422b88f33b05faabf30d" id="tgt14" class="tgtSentence"> Click <legacyBold>SQL Enterprise Manager</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ae3bbbe600080e2e8f04ba2be30c895a" id="tgt15" class="tgtSentence">From the <legacyBold>Tools</legacyBold> menu, click <legacyBold>SQL Query Tool</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="391a30830bcff7748145e94eba3861ba" id="tgt16" class="tgtSentence">Click <legacyBold>Load SQL Script</legacyBold> and browse to c:\Platform SDK\Samples\DataAccess\RDS\AddressBook.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a4161ca3212a6a0bfba163a0ec6bbbed" id="tgt17" class="tgtSentence">Select the file Sampleemp.sql.</caps:sentence>
                    <caps:sentence sentenceid="b6bfb3ad83145d34f1ed972c3639bb24" id="tgt18" class="tgtSentence"> Click <legacyBold>Open</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d8231ffb6d8ccb864bb0b3eb53b8fd50" id="tgt19" class="tgtSentence">Click the <legacyBold>Execute Query</legacyBold> button (the green arrow on the toolbar).</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="2518966c5fd8385eb125eff355467341" id="tgt20" class="tgtSentence">After it executes, close the <legacyBold>Query</legacyBold> and <legacyBold>Enterprise Manager</legacyBold> windows.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="e220b2e71bbcd69237e2ea191d97866c" id="tgt21" class="tgtSentence">To run the Sampleemp.sql script in Microsoft SQL Server 7.0</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e787ecf9c4a3604ba46e43cf4d4dee5a" id="tgt22" class="tgtSentence">Click <legacyBold>Start</legacyBold>, point to <legacyBold>Programs</legacyBold>, and then point to <legacyBold>Microsoft SQL Server 7.0</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="687412f0498014a1394898dc958fa844" id="tgt23" class="tgtSentence"> Click <legacyBold>Enterprise Manager</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a590a994cb5c72f94a006ec21d2191a4" id="tgt24" class="tgtSentence">Be sure that the SQL Server that you want to use is selected from your list of registered servers in Enterprise Manager.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d803e2513fe2a4ac8b3f655c46ecde36" id="tgt25" class="tgtSentence">From the <legacyBold>Tools</legacyBold> menu, click <legacyBold>SQL Server Query Analyzer</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ab3d32d0c7a08bdf713635c6fe79ae11" id="tgt26" class="tgtSentence">Click the <legacyBold>Load SQL Script</legacyBold> button (the open folder on the toolbar) and browse to c:\Platform SDK\Samples\DataAccess\RDS\AddressBook.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a4161ca3212a6a0bfba163a0ec6bbbed" id="tgt27" class="tgtSentence">Select the file Sampleemp.sql.</caps:sentence>
                    <caps:sentence sentenceid="b6bfb3ad83145d34f1ed972c3639bb24" id="tgt28" class="tgtSentence"> Click <legacyBold>Open</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="453d0aad85299f81eb75e7cd6a1d30a8" id="tgt29" class="tgtSentence">Click the <legacyBold>Execute Query</legacyBold> button (the green arrow on the toolbar) or <legacyBold>F5</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="db12ccb2e0ec72e05c994a656385631d" id="tgt30" class="tgtSentence">After it executes, close the <legacyBold>Query</legacyBold>, <legacyBold>Query Analyzer</legacyBold>, and <legacyBold>Enterprise Manager</legacyBold> windows.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3a2644e9-d634-4ae6-a5b7-13fb7b317ec7">Running the Address Book Sample Application</link>
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
          <caps:sentence id="src5" class="srcSentence">You must use either the ISQL/Query Analyzer command-line utility or the SQL Server Enterprise Manager to run the included SQL script (Sampleemp.sql) that:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Creates a new database, AddrBookDB, on the default device.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Connects to the database, AddrBookDB.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Creates an Employee table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Populates the table with sample data.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Runs a simple SELECT statement to verify the population of the database table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Sets up a user account called "adcdemo" with a password of "adcdemo."</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src12" class="srcSentence">To run the Sampleemp.sql script in Microsoft SQL Server 6.5</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Click <legacyBold>Start</legacyBold>, point to <legacyBold>Programs</legacyBold>, and then point to <legacyBold>Microsoft SQL Server 6.5</legacyBold>.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> Click <legacyBold>SQL Enterprise Manager</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">From the <legacyBold>Tools</legacyBold> menu, click <legacyBold>SQL Query Tool</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Click <legacyBold>Load SQL Script</legacyBold> and browse to c:\Platform SDK\Samples\DataAccess\RDS\AddressBook.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Select the file Sampleemp.sql.</caps:sentence>
                    <caps:sentence id="src18" class="srcSentence"> Click <legacyBold>Open</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Click the <legacyBold>Execute Query</legacyBold> button (the green arrow on the toolbar).</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">After it executes, close the <legacyBold>Query</legacyBold> and <legacyBold>Enterprise Manager</legacyBold> windows.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src21" class="srcSentence">To run the Sampleemp.sql script in Microsoft SQL Server 7.0</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Click <legacyBold>Start</legacyBold>, point to <legacyBold>Programs</legacyBold>, and then point to <legacyBold>Microsoft SQL Server 7.0</legacyBold>.</caps:sentence>
                    <caps:sentence id="src23" class="srcSentence"> Click <legacyBold>Enterprise Manager</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Be sure that the SQL Server that you want to use is selected from your list of registered servers in Enterprise Manager.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">From the <legacyBold>Tools</legacyBold> menu, click <legacyBold>SQL Server Query Analyzer</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Click the <legacyBold>Load SQL Script</legacyBold> button (the open folder on the toolbar) and browse to c:\Platform SDK\Samples\DataAccess\RDS\AddressBook.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Select the file Sampleemp.sql.</caps:sentence>
                    <caps:sentence id="src28" class="srcSentence"> Click <legacyBold>Open</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Click the <legacyBold>Execute Query</legacyBold> button (the green arrow on the toolbar) or <legacyBold>F5</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">After it executes, close the <legacyBold>Query</legacyBold>, <legacyBold>Query Analyzer</legacyBold>, and <legacyBold>Enterprise Manager</legacyBold> windows.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3a2644e9-d634-4ae6-a5b7-13fb7b317ec7">Running the Address Book Sample Application</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
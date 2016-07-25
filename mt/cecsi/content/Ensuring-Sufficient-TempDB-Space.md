---
title: "Ensuring Sufficient TempDB Space"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 09130db1-6248-4234-a1e5-a9c8e1622c06
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
# Ensuring Sufficient TempDB Space
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9d263af8db627c44422048ea0c3e7ed0" id="tgt1" class="tgtSentence">If errors occur while handling <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB.</caps:sentence>
          <caps:sentence sentenceid="345d63b8c5fd6292255c570b6c85996c" id="tgt2" class="tgtSentence"> (Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the <legacyBold>Recordset</legacyBold>, which requires some temporary space.)</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="9aa347cf7f56c92c16744e3896111bbf" id="tgt7" class="tgtSentence">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</caps:sentence>
          </para>
        </alert>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="19f0f448498789e53b1d9ad41d2a8e3b" id="tgt8" class="tgtSentence">By default inMicrosoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed.</caps:sentence>
            <caps:sentence sentenceid="2e5ab113a5d929fdc6cc979306b7e10f" id="tgt9" class="tgtSentence"> Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence sentenceid="4d78da99534809e8f1797ffb5406435a" id="tgt10" class="tgtSentence">To increase the TempDB space on SQL Server 6.5</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="4879f1570eb9631709ad8458cd5ec084" id="tgt11" class="tgtSentence">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="d142dc1ae22fe5b0c61e3118021d78d5" id="tgt12" class="tgtSentence">Select a (physical) device to expand, such as Master, and double-click the device to open the <legacyBold>Edit Database Device</legacyBold> dialog box.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="6e068156e56a5f8abfbf88499ce0bcac" id="tgt13" class="tgtSentence">This dialog box shows how much space the current databases are using.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="105b297706d70e20477c154324b33b02" id="tgt14" class="tgtSentence">In the <legacyBold>Size</legacyBold> box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="aa5f763a0139e564ed372413e60c02fb" id="tgt15" class="tgtSentence">Click <legacyBold>Change Now</legacyBold> to increase the amount of space to which the (logical) TempDB can expand.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="6792ffb308123167da7f8c972e177c78" id="tgt16" class="tgtSentence">Open the Databases tree on the server, and then double-click <legacyBold>TempDB</legacyBold> to open the <legacyBold>Edit Database</legacyBold> dialog box.</caps:sentence>
                  <caps:sentence sentenceid="b76fa3a3e13538e4c31f7a60192bb746" id="tgt17" class="tgtSentence"> The <legacyBold>Database</legacyBold> tab lists the amount of space currently allocated to TempDB (<legacyBold>Data Size</legacyBold>).</caps:sentence>
                  <caps:sentence sentenceid="cb5a797c4717f025c5dda84eb75dbb23" id="tgt18" class="tgtSentence"> By default, this is 2 MB.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="bbb34b2eb0963fa57debb4fc807778a7" id="tgt19" class="tgtSentence">Under the <legacyBold>Size</legacyBold> group, click <legacyBold>Expand</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="ea7b6483c1019350ebc1b0b33b0352fc" id="tgt20" class="tgtSentence"> The graphs show the available and allocated space on each of the physical devices.</caps:sentence>
                  <caps:sentence sentenceid="d8e9ced29fcb0b94ce08c7ec7b1b7bda" id="tgt21" class="tgtSentence"> The bars in maroon color represent available space.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="0f914d8b1c0b29c07e7733abcd38dc55" id="tgt22" class="tgtSentence">Select a <legacyBold>Log Device</legacyBold>, such as Master,to display the available size in the <legacyBold>Size (MB)</legacyBold> box.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="9e1fff6ca17390d91305bca77403aaa3" id="tgt23" class="tgtSentence">Click <legacyBold>Expand Now</legacyBold> to allocate that space to the TempDB database.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="3878b3fa8922558210450627b2d53ad8" id="tgt24" class="tgtSentence">The <legacyBold>Edit Database</legacyBold> dialog box displays the new allocated size for TempDB.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
          <conclusion>
            <content>
              <para>
                <caps:sentence sentenceid="d585c9734a196967c2bc2b6990d124b6" id="tgt25" class="tgtSentence">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</caps:sentence>
              </para>
            </content>
          </conclusion>
        </procedure>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">If errors occur while handling <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> (Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the <legacyBold>Recordset</legacyBold>, which requires some temporary space.)</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <alert class="important">
          <para>
            <caps:sentence id="src7" class="srcSentence">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</caps:sentence>
          </para>
        </alert>
        <alert class="note">
          <para>
            <caps:sentence id="src8" class="srcSentence">By default inMicrosoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence id="src10" class="srcSentence">To increase the TempDB space on SQL Server 6.5</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Select a (physical) device to expand, such as Master, and double-click the device to open the <legacyBold>Edit Database Device</legacyBold> dialog box.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src13" class="srcSentence">This dialog box shows how much space the current databases are using.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src14" class="srcSentence">In the <legacyBold>Size</legacyBold> box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Click <legacyBold>Change Now</legacyBold> to increase the amount of space to which the (logical) TempDB can expand.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Open the Databases tree on the server, and then double-click <legacyBold>TempDB</legacyBold> to open the <legacyBold>Edit Database</legacyBold> dialog box.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> The <legacyBold>Database</legacyBold> tab lists the amount of space currently allocated to TempDB (<legacyBold>Data Size</legacyBold>).</caps:sentence>
                  <caps:sentence id="src18" class="srcSentence"> By default, this is 2 MB.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Under the <legacyBold>Size</legacyBold> group, click <legacyBold>Expand</legacyBold>.</caps:sentence>
                  <caps:sentence id="src20" class="srcSentence"> The graphs show the available and allocated space on each of the physical devices.</caps:sentence>
                  <caps:sentence id="src21" class="srcSentence"> The bars in maroon color represent available space.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Select a <legacyBold>Log Device</legacyBold>, such as Master,to display the available size in the <legacyBold>Size (MB)</legacyBold> box.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Click <legacyBold>Expand Now</legacyBold> to allocate that space to the TempDB database.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src24" class="srcSentence">The <legacyBold>Edit Database</legacyBold> dialog box displays the new allocated size for TempDB.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
          <conclusion>
            <content>
              <para>
                <caps:sentence id="src25" class="srcSentence">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</caps:sentence>
              </para>
            </content>
          </conclusion>
        </procedure>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
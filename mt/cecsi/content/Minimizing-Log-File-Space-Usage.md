---
title: "Minimizing Log File Space Usage"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 669662a0-e20f-483e-ab28-53f66c524c98
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
# Minimizing Log File Space Usage
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3191f54bd6a8d039a8b25c9c7f735d1b" id="tgt1" class="tgtSentence">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database.</caps:sentence>
          <caps:sentence sentenceid="37d92f775df2637f7a2529ac43e625fb" id="tgt2" class="tgtSentence"> You can set the log file to <legacyBold>Truncate on Checkpoint </legacyBold>to significantly extend the life of the log file for a database.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence sentenceid="eee769c52c45143640ac955244a68e10" id="tgt7" class="tgtSentence">To enable Truncate on Checkpoint in Microsoft SQL Server 6.5</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="4879f1570eb9631709ad8458cd5ec084" id="tgt8" class="tgtSentence">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="aa0cbb499f1d450c96d9af905f6f85b0" id="tgt9" class="tgtSentence">Double-click the name of the database on which this feature will be enabled.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="039487539bd04e66192e08f7c7da7e6c" id="tgt10" class="tgtSentence">From the <legacyBold>Database</legacyBold> tab, select <legacyBold>Truncate</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="512f8f2dd536b341543110a5fb8c0e6b" id="tgt11" class="tgtSentence">From the <legacyBold>Options</legacyBold> tab, select <legacyBold>Truncate Log on Checkpoint</legacyBold>, and then click <legacyBold>OK</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
        <procedure>
          <title>
            <caps:sentence sentenceid="77f3eddd64fa8ca44c18aa8cf07c41e0" id="tgt12" class="tgtSentence">To enable Truncate on Checkpoint in Microsoft SQL Server 7.0</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="120b1be2d60d693818557cdf1bae27bf" id="tgt13" class="tgtSentence">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="1318fbb03cfcfbb67ccbac387e4d462e" id="tgt14" class="tgtSentence">Right-click the name of the database on which this feature will be enabled and choose <legacyBold>Properties</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="512f8f2dd536b341543110a5fb8c0e6b" id="tgt15" class="tgtSentence">From the <legacyBold>Options</legacyBold> tab, select <legacyBold>Truncate Log on Checkpoint</legacyBold>, and then click <legacyBold>OK</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
          <conclusion>
            <content>
              <para>
                <caps:sentence sentenceid="fbc7c6a70e29e8c13d35ce249fe8a726" id="tgt16" class="tgtSentence">For more information about the <legacyBold>Truncate on Checkpoint</legacyBold> feature, see the Microsoft SQL Server documentation.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can set the log file to <legacyBold>Truncate on Checkpoint </legacyBold>to significantly extend the life of the log file for a database.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence id="src7" class="srcSentence">To enable Truncate on Checkpoint in Microsoft SQL Server 6.5</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Double-click the name of the database on which this feature will be enabled.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src10" class="srcSentence">From the <legacyBold>Database</legacyBold> tab, select <legacyBold>Truncate</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src11" class="srcSentence">From the <legacyBold>Options</legacyBold> tab, select <legacyBold>Truncate Log on Checkpoint</legacyBold>, and then click <legacyBold>OK</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
        <procedure>
          <title>
            <caps:sentence id="src12" class="srcSentence">To enable Truncate on Checkpoint in Microsoft SQL Server 7.0</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Right-click the name of the database on which this feature will be enabled and choose <legacyBold>Properties</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src15" class="srcSentence">From the <legacyBold>Options</legacyBold> tab, select <legacyBold>Truncate Log on Checkpoint</legacyBold>, and then click <legacyBold>OK</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
          <conclusion>
            <content>
              <para>
                <caps:sentence id="src16" class="srcSentence">For more information about the <legacyBold>Truncate on Checkpoint</legacyBold> feature, see the Microsoft SQL Server documentation.</caps:sentence>
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
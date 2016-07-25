---
title: "System Requirements for the Address Book Application"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: da385405-1c9a-478b-9bf6-fba70015324c
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
# System Requirements for the Address Book Application
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="22f6e152f958e9172ac82f431d300747" id="tgt1" class="tgtSentence">To set up the Address Book sample application, you need to meet the following software and database requirements:</caps:sentence>
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
          <caps:sentence sentenceid="674593793bab8c222fa55ee830059d29" id="tgt6" class="tgtSentence">Software Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f8c290383ed8a4abfe7c3a9d720a353b" id="tgt7" class="tgtSentence">The server computer software requirements for running this Web application include:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="83f7004f5ea7d6b08b9323ba33156e90" id="tgt8" class="tgtSentence">Microsoft Windows NT® Server 4.0, with Service Pack 3 or later, or Microsoft Windows® 2000 Server.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d2df498c6b7ed1ab784d0a4ba0fd683c" id="tgt9" class="tgtSentence">Microsoft Internet Information Services (IIS) version 3.0 or later, with Active Server Pages.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="9d6d06437c4cd27c6d2f2d0399559f45" id="tgt10" class="tgtSentence">The client computer software requirements for running this Web application include:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="09fd362df4bc85e26835ed6c3c70e4fd" id="tgt11" class="tgtSentence">Microsoft Internet Explorer 4.0 or later.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0d8c0be6190728f9222e6e87c14a0de2" id="tgt12" class="tgtSentence">Microsoft Windows NT 4.0 Workstation or Server, Windows 2000, or Microsoft Windows 98.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="11a74a00e5cfb28d4862ecd9d77b6283" id="tgt13" class="tgtSentence">Database Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4db8cbc83bcc2e594db7fb403a592c06" id="tgt14" class="tgtSentence">To use this sample, you must have:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="a1b5481c6498fdb1ac976328ef091dc0" id="tgt15" class="tgtSentence">An operational Microsoft® SQL Server version 6.5 or later database server.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9be03e91d0e728e6d9a70ee5b1ea9df1" id="tgt16" class="tgtSentence">Privileges to create the database and populate it with the sample data.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="55933b2844d2629503abedbe4c84f45c" id="tgt17" class="tgtSentence">Verification of the populated data through Enterprise Manager or the ISQL utilities (called Query Analyzer in SQL Server 7.0).</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="b05a67974ead7837dce49d8ffbc34b95" id="tgt18" class="tgtSentence">If you do not have privileges, your database administrator may need to set up the system and give you access permission to the database, or set up the database for you.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="409b3f8b-0ced-4867-acbe-b245dcdf6702">Running the Address Book SQL Script</link>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="3a2644e9-d634-4ae6-a5b7-13fb7b317ec7">Running the Address Book Sample Application</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To set up the Address Book sample application, you need to meet the following software and database requirements:</caps:sentence>
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
          <caps:sentence id="src6" class="srcSentence">Software Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">The server computer software requirements for running this Web application include:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Microsoft Windows NT® Server 4.0, with Service Pack 3 or later, or Microsoft Windows® 2000 Server.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Microsoft Internet Information Services (IIS) version 3.0 or later, with Active Server Pages.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src10" class="srcSentence">The client computer software requirements for running this Web application include:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Microsoft Internet Explorer 4.0 or later.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Microsoft Windows NT 4.0 Workstation or Server, Windows 2000, or Microsoft Windows 98.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Database Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">To use this sample, you must have:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">An operational Microsoft® SQL Server version 6.5 or later database server.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">Privileges to create the database and populate it with the sample data.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">Verification of the populated data through Enterprise Manager or the ISQL utilities (called Query Analyzer in SQL Server 7.0).</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src18" class="srcSentence">If you do not have privileges, your database administrator may need to set up the system and give you access permission to the database, or set up the database for you.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="409b3f8b-0ced-4867-acbe-b245dcdf6702">Running the Address Book SQL Script</link>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="3a2644e9-d634-4ae6-a5b7-13fb7b317ec7">Running the Address Book Sample Application</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
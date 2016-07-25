---
title: "Securing RDS Applications"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 82fb1330-d6c6-4c17-ad3e-d417ff822b25
caps.latest.revision: 14
caps.handback.revision: 14
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
# Securing RDS Applications
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="172ab0e769bae56487ef1923f02355e3" id="tgt1" class="tgtSentence">This topic provides security information for RDS.</caps:sentence>
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
          <caps:sentence sentenceid="3594df02ecaeda291c37ee216c3e97ad" id="tgt6" class="tgtSentence">Microsoft Internet Explorer Security Issues</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="efd18f294b9bc61637522adeae8c2d4d" id="tgt7" class="tgtSentence">With new security enhancements added to Microsoft Internet Explorer, some ADO and RDS objects are restricted to running only in a "safe" mode environment.</caps:sentence>
            <caps:sentence sentenceid="16394e99240b3094fa32e0b457236109" id="tgt8" class="tgtSentence"> This requires that you are aware of these issues, including different zones, security levels, restrictive behavior, unsafe operations, and customized security settings.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a2d6f928c10edac31b4f2cc2aca9f66b" id="tgt9" class="tgtSentence">Security and Your Web Server</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="eb83576d475a05df910ba975f07e878c" id="tgt10" class="tgtSentence">If you use the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object on your Internet Web server, remember that doing so creates a potential security risk.</caps:sentence>
            <caps:sentence sentenceid="2210c0eb43e22cc52893c149a31b3c1e" id="tgt11" class="tgtSentence"> External users who obtain valid data source name (DSN), user ID, and password information could write pages to send any query to that data source.</caps:sentence>
            <caps:sentence sentenceid="fd6845ca4e75f9fe9a8e44b770a4d346" id="tgt12" class="tgtSentence"> If you want more restricted access to a data source, one option is to unregister and delete the <legacyBold>RDSServer.DataFactory</legacyBold> object (msadcf.dll), and instead use custom business objects with hard-coded queries.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="79be200815c21b272c5e6d5da3ea8cfb" id="tgt13" class="tgtSentence">For more information on the security implications of using the RDSServer.DataFactory object, see the Microsoft Security Bulletin MS99-025 on the Microsoft Security Web site.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ccb60bdb82d92218f0c5e090b2a9f731" id="tgt14" class="tgtSentence">Client Impersonation and Security</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="89c9a0c809deccc5c4e81c0d881e4f10" id="tgt15" class="tgtSentence">If the <legacyBold>Password Authentication</legacyBold> property for your IIS Web server is set to Windows NT Challenge/Response authentication (for Windows NT 4.0) or to Integrated Windows authentication (for Windows 2000), then business objects are invoked under the client's security context.</caps:sentence>
            <caps:sentence sentenceid="e403cbcce677ccc202838402afb77a98" id="tgt16" class="tgtSentence"> This is a new feature in RDS 1.5 that allows Client Impersonation over HTTP.</caps:sentence>
            <caps:sentence sentenceid="57477942e80aa3ceb6bbcfdc376e8b4a" id="tgt17" class="tgtSentence"> When working in this mode, the logon to the Web server (IIS) is not anonymous but uses the user ID and password that the client computer is running under.</caps:sentence>
            <caps:sentence sentenceid="4fc8a3844b6c08e4d0c2236a668924b9" id="tgt18" class="tgtSentence"> If the ODBC DSNs are set up to use Trusted Connection, then access to databases, such as SQL Server, also happens under the client's security context.</caps:sentence>
            <caps:sentence sentenceid="74f822a3a9790057fe2ff2bf1d3dc4e8" id="tgt19" class="tgtSentence"> But this only works if the database is on the same computer as the IIS; the client credentials cannot be carried over to yet another computer.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ed04ab8aaf1401b73d8ca36949e1e5b7" id="tgt20" class="tgtSentence">For example, a client, John Doe, with userid="JohnD" and password="secret" is logged on to a client computer.</caps:sentence>
            <caps:sentence sentenceid="622b6c9c676037b0a8fb0eb82fd49f87" id="tgt21" class="tgtSentence"> He runs a browser-based application that needs to access the <legacyBold>RDSServer.DataFactory</legacyBold> object to create a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> by executing an SQL query on the "MyServer" computer running IIS.</caps:sentence>
            <caps:sentence sentenceid="e1df5bc40a56a15d9fdd32c05de2fe44" id="tgt22" class="tgtSentence"> MyServer, a system running Windows NT Server 4.0, is set up to use Windows NT Challenge/Response authentication, its ODBC DSN has "Use Trusted Connection" selected, and the server also contains the SQL Server data source.</caps:sentence>
            <caps:sentence sentenceid="0eef1c4dc241f05d3e651baa2694ab71" id="tgt23" class="tgtSentence"> When a request is received on the Web server, it asks the client for the user ID and password.</caps:sentence>
            <caps:sentence sentenceid="be214d3a92233699dc350f54ce343c4c" id="tgt24" class="tgtSentence"> Thus, the request is logged on MyServer as coming from "JohnD"/"Secret" instead of IUSER_MyServer (which is the default when Anonymous Password Authentication is on).</caps:sentence>
            <caps:sentence sentenceid="a231c7cbc39ea6a780a2d59800a1e2b3" id="tgt25" class="tgtSentence"> Similarly, when logging on to SQL Server, "JohnD"/"Secret" is used.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="73612a56396f3577cd5dd9bd7b03ce22" id="tgt26" class="tgtSentence">Consequently, the IIS Windows NT Challenge/Response authentication mode allows HTML pages to be created without the user being explicitly prompted for the user ID and password information needed to log on to the database.</caps:sentence>
            <caps:sentence sentenceid="21bde55161dbef3c6dc431bedf22d223" id="tgt27" class="tgtSentence"> If the IIS Basic Authentication were being used, then this also would be required.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c67139b6bc23ace55fce46f0c5c2d663" id="tgt28" class="tgtSentence">Password Authentication</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="58da07a50209b30b5067928be9a736a7" id="tgt29" class="tgtSentence">RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response authentication (called Integrated Windows authentication in Windows 2000).</caps:sentence>
            <caps:sentence sentenceid="6219902b8afc98b41594f52ab4ff8d03" id="tgt30" class="tgtSentence"> These settings define how a Web server controls access through it, such as requiring that a client computer have explicit access privileges on the NT Web server.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This topic provides security information for RDS.</caps:sentence>
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
          <caps:sentence id="src6" class="srcSentence">Microsoft Internet Explorer Security Issues</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">With new security enhancements added to Microsoft Internet Explorer, some ADO and RDS objects are restricted to running only in a "safe" mode environment.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> This requires that you are aware of these issues, including different zones, security levels, restrictive behavior, unsafe operations, and customized security settings.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Security and Your Web Server</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">If you use the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object on your Internet Web server, remember that doing so creates a potential security risk.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> External users who obtain valid data source name (DSN), user ID, and password information could write pages to send any query to that data source.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> If you want more restricted access to a data source, one option is to unregister and delete the <legacyBold>RDSServer.DataFactory</legacyBold> object (msadcf.dll), and instead use custom business objects with hard-coded queries.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">For more information on the security implications of using the RDSServer.DataFactory object, see the Microsoft Security Bulletin MS99-025 on the Microsoft Security Web site.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Client Impersonation and Security</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">If the <legacyBold>Password Authentication</legacyBold> property for your IIS Web server is set to Windows NT Challenge/Response authentication (for Windows NT 4.0) or to Integrated Windows authentication (for Windows 2000), then business objects are invoked under the client's security context.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> This is a new feature in RDS 1.5 that allows Client Impersonation over HTTP.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> When working in this mode, the logon to the Web server (IIS) is not anonymous but uses the user ID and password that the client computer is running under.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> If the ODBC DSNs are set up to use Trusted Connection, then access to databases, such as SQL Server, also happens under the client's security context.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> But this only works if the database is on the same computer as the IIS; the client credentials cannot be carried over to yet another computer.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">For example, a client, John Doe, with userid="JohnD" and password="secret" is logged on to a client computer.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> He runs a browser-based application that needs to access the <legacyBold>RDSServer.DataFactory</legacyBold> object to create a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> by executing an SQL query on the "MyServer" computer running IIS.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> MyServer, a system running Windows NT Server 4.0, is set up to use Windows NT Challenge/Response authentication, its ODBC DSN has "Use Trusted Connection" selected, and the server also contains the SQL Server data source.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> When a request is received on the Web server, it asks the client for the user ID and password.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> Thus, the request is logged on MyServer as coming from "JohnD"/"Secret" instead of IUSER_MyServer (which is the default when Anonymous Password Authentication is on).</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> Similarly, when logging on to SQL Server, "JohnD"/"Secret" is used.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src26" class="srcSentence">Consequently, the IIS Windows NT Challenge/Response authentication mode allows HTML pages to be created without the user being explicitly prompted for the user ID and password information needed to log on to the database.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> If the IIS Basic Authentication were being used, then this also would be required.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">Password Authentication</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response authentication (called Integrated Windows authentication in Windows 2000).</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> These settings define how a Web server controls access through it, such as requiring that a client computer have explicit access privileges on the NT Web server.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
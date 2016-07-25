---
title: "OLE DB Providers (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6e0488c3-934d-4976-99dc-65c580dc7a3c
caps.latest.revision: 10
caps.handback.revision: 10
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
# OLE DB Providers (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b3c53561d97eba72594958d217910691" id="tgt1" class="tgtSentence">OLE DB defines a set of COM interfaces to provide applications with uniform access to data that is stored in diverse information sources.</caps:sentence>
          <caps:sentence sentenceid="c7df3e498fd88f3b39e6c64798df2763" id="tgt2" class="tgtSentence"> This approach allows a data source to share its data through the interfaces that support the amount of DBMS functionality appropriate to the data source.</caps:sentence>
          <caps:sentence sentenceid="27b8f5ee2ccf2d78b7607e9f82c1c112" id="tgt3" class="tgtSentence"> By design, the high-performance architecture of OLE DB is based on its use of a flexible, component-based services model.</caps:sentence>
          <caps:sentence sentenceid="5722407804028ed99f345ee7ce5896bd" id="tgt4" class="tgtSentence"> Rather than having a prescribed number of intermediary layers between the application and the data, OLE DB requires only as many components as are needed to accomplish a particular task.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0784780697cd5aed926c0e2a3c29dac1" id="tgt5" class="tgtSentence">For example, suppose a user wants to run a query.</caps:sentence>
          <caps:sentence sentenceid="11b2982dd65c4db343189d550c2c0b1b" id="tgt6" class="tgtSentence"> Consider the following scenarios:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="eac728172102d40be1280dd95ed2ebd3" id="tgt7" class="tgtSentence">The data resides in a relational database for which there currently exists an ODBC driver but no native OLE DB provider: The application uses ADO to talk to the OLE DB Provider for ODBC, which then loads the appropriate ODBC driver.</caps:sentence>
              <caps:sentence sentenceid="9d31d37f007ff915d01b8454df56b7a2" id="tgt8" class="tgtSentence"> The driver passes the SQL statement to the DBMS, which retrieves the data.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c969f536142a9436ed577c9fc83bf850" id="tgt9" class="tgtSentence">The data resides in Microsoft SQL Server for which there is a native OLE DB provider: The application uses ADO to talk directly to the OLE DB Provider for Microsoft SQL Server.</caps:sentence>
              <caps:sentence sentenceid="26c825caf05c49dc9a648336e67f3197" id="tgt10" class="tgtSentence"> No intermediaries are required.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b771d8644c02f182075ba738eacb91e8" id="tgt11" class="tgtSentence">The data resides in Microsoft Exchange Server, for which there is an OLE DB provider but which does not expose an engine to process SQL queries: The application uses ADO to talk to the OLE DB Provider for Microsoft Exchange and calls upon an OLE DB query processor component to handle the querying.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="376445ff5ae28271f85a938342055e80" id="tgt12" class="tgtSentence">The data resides in the Microsoft NTFS file system in the form of documents: Data is accessed by using a native OLE DB provider over Microsoft Indexing Service, which indexes the content and properties of documents in the file system to enable efficient content searches.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="a3473e3ab7c94a540fb134f329a90282" id="tgt13" class="tgtSentence">In all the preceding examples, the application can query the data.</caps:sentence>
          <caps:sentence sentenceid="e7b25f767d6fd63fad16c173d33bafe7" id="tgt14" class="tgtSentence"> The user's needs are met with a minimum number of components.</caps:sentence>
          <caps:sentence sentenceid="3bb87ee34e6042058ca9cb8a12a72f1e" id="tgt15" class="tgtSentence"> In each case, additional components are used only if needed, and only the required components are invoked.</caps:sentence>
          <caps:sentence sentenceid="0c84b47b1f84d95a4cf58e80f358eb4b" id="tgt16" class="tgtSentence"> This demand-loading of reusable and shareable components greatly contributes to high performance when OLE DB is used.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7cc58f399e2b9596ece0c8cdf962876c" id="tgt17" class="tgtSentence">Providers fall into two categories: those providing data and those providing services.</caps:sentence>
          <caps:sentence sentenceid="4ca41bc5c622169e053c91d3b9076238" id="tgt18" class="tgtSentence"> A data provider owns its own data and exposes it in tabular form to your application.</caps:sentence>
          <caps:sentence sentenceid="47ac85ebf8230290356f468e3144e6a8" id="tgt19" class="tgtSentence"> A service provider encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</caps:sentence>
          <caps:sentence sentenceid="f45df1a456ce47b57d91dee796d9a4d4" id="tgt20" class="tgtSentence"> A service provider can also be further defined as a service component, which must work in conjunction with other service providers or components.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="12807f7ad79e5d23a5c4fa9a3bd6b8aa" id="tgt21" class="tgtSentence">ADO provides a consistent, higher level interface to the various OLE DB providers.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt22" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="11702985c8e68bd508b53ef9de6ce857" id="tgt23" class="tgtSentence">             <legacyLink xlink:href="877b9f25-60c4-4ab6-8052-2c28a3849e89">Data Providers</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6b75b40c8a5110c47cae6aab795b0902" id="tgt24" class="tgtSentence">             <legacyLink xlink:href="1fd7a374-587b-4ca9-9204-3a4019b67a71">Service Providers and Components</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">OLE DB defines a set of COM interfaces to provide applications with uniform access to data that is stored in diverse information sources.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This approach allows a data source to share its data through the interfaces that support the amount of DBMS functionality appropriate to the data source.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> By design, the high-performance architecture of OLE DB is based on its use of a flexible, component-based services model.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Rather than having a prescribed number of intermediary layers between the application and the data, OLE DB requires only as many components as are needed to accomplish a particular task.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">For example, suppose a user wants to run a query.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Consider the following scenarios:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">The data resides in a relational database for which there currently exists an ODBC driver but no native OLE DB provider: The application uses ADO to talk to the OLE DB Provider for ODBC, which then loads the appropriate ODBC driver.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> The driver passes the SQL statement to the DBMS, which retrieves the data.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">The data resides in Microsoft SQL Server for which there is a native OLE DB provider: The application uses ADO to talk directly to the OLE DB Provider for Microsoft SQL Server.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> No intermediaries are required.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">The data resides in Microsoft Exchange Server, for which there is an OLE DB provider but which does not expose an engine to process SQL queries: The application uses ADO to talk to the OLE DB Provider for Microsoft Exchange and calls upon an OLE DB query processor component to handle the querying.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">The data resides in the Microsoft NTFS file system in the form of documents: Data is accessed by using a native OLE DB provider over Microsoft Indexing Service, which indexes the content and properties of documents in the file system to enable efficient content searches.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src13" class="srcSentence">In all the preceding examples, the application can query the data.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> The user's needs are met with a minimum number of components.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> In each case, additional components are used only if needed, and only the required components are invoked.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> This demand-loading of reusable and shareable components greatly contributes to high performance when OLE DB is used.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src17" class="srcSentence">Providers fall into two categories: those providing data and those providing services.</caps:sentence>
          <caps:sentence id="src18" class="srcSentence"> A data provider owns its own data and exposes it in tabular form to your application.</caps:sentence>
          <caps:sentence id="src19" class="srcSentence"> A service provider encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> A service provider can also be further defined as a service component, which must work in conjunction with other service providers or components.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src21" class="srcSentence">ADO provides a consistent, higher level interface to the various OLE DB providers.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src22" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src23" class="srcSentence">             <legacyLink xlink:href="877b9f25-60c4-4ab6-8052-2c28a3849e89">Data Providers</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src24" class="srcSentence">             <legacyLink xlink:href="1fd7a374-587b-4ca9-9204-3a4019b67a71">Service Providers and Components</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
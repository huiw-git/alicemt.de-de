---
title: "Connecting to Data Sources"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 82770486-37bd-4c90-885f-6817a7c77ad7
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
# Connecting to Data Sources
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="48d2a63a9a80ac91163b0a128899ce0a" id="tgt1" class="tgtSentence">An ADO <legacyBold>Connection</legacyBold> object represents a unique session with a data source, including a DBMS, a file store, or a comma-delimited text file.</caps:sentence>
          <caps:sentence sentenceid="6c7163b98667846e6cc5d8625b22a906" id="tgt2" class="tgtSentence"> In the case of a client/server database system, the ADO connection can be an actual network connection to the server.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="35c8d840fb47519aa33f3bd9b7c818e7" id="tgt3" class="tgtSentence">The <legacyBold>Connection</legacyBold> object supports various <legacyLink xlink:href="f571b74d-b796-4009-9c66-6a36ab995a2a">properties and methods</legacyLink> for specifying connection configurations, opening and closing connections, creating and executing commands against the data source, and providing information about the design of the underlying data source in the form of schema rowsets, etc. Depending on the functionality supported by the provider, some collections, methods, or properties of a <legacyBold>Connection</legacyBold> object might not be available.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b796e32a415237095ff34d34098a4634" id="tgt4" class="tgtSentence">You can connect to a data source either by using a <legacyBold>Connection</legacyBold> object or by using a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt5" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="360855b4d905f540e7eb4e072dbc2e97" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="4b34f971-5699-43e7-9b15-137d334fa66e">Using a Connection Object</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1ee4d6781f9c4113d520006dd465f641" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="01c630d8-eb35-4bd0-a99f-7c0f85316cc1">Using a Recordset Object</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="68772c73ad23808d9b9b624f13103880" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="14eae122-2d1e-40c8-b88e-b7cb8dfbc93b">Creating a Connection String</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9a23be7da2ce23ad0ec3239dec7f1ac5" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="49456201-b085-4851-9686-e814136b07be">Specifying Connection Properties</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f83fa8f0a67e282abb492978e2c32048" id="tgt10" class="tgtSentence">             <legacyLink xlink:href="189240e8-3ffa-4024-81a9-c6cb5d17eee0">Controlling Transactions</legacyLink>           </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">An ADO <legacyBold>Connection</legacyBold> object represents a unique session with a data source, including a DBMS, a file store, or a comma-delimited text file.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> In the case of a client/server database system, the ADO connection can be an actual network connection to the server.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">The <legacyBold>Connection</legacyBold> object supports various <legacyLink xlink:href="f571b74d-b796-4009-9c66-6a36ab995a2a">properties and methods</legacyLink> for specifying connection configurations, opening and closing connections, creating and executing commands against the data source, and providing information about the design of the underlying data source in the form of schema rowsets, etc. Depending on the functionality supported by the provider, some collections, methods, or properties of a <legacyBold>Connection</legacyBold> object might not be available.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">You can connect to a data source either by using a <legacyBold>Connection</legacyBold> object or by using a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="4b34f971-5699-43e7-9b15-137d334fa66e">Using a Connection Object</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="01c630d8-eb35-4bd0-a99f-7c0f85316cc1">Using a Recordset Object</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="14eae122-2d1e-40c8-b88e-b7cb8dfbc93b">Creating a Connection String</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="49456201-b085-4851-9686-e814136b07be">Specifying Connection Properties</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">             <legacyLink xlink:href="189240e8-3ffa-4024-81a9-c6cb5d17eee0">Controlling Transactions</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
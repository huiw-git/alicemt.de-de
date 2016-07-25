---
title: "Specifying Connection Properties"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 49456201-b085-4851-9686-e814136b07be
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
# Specifying Connection Properties
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bdc8d754290813e9409464198c076403" id="tgt1" class="tgtSentence">You can supply much of the information specified by a <legacyLink xlink:href="14eae122-2d1e-40c8-b88e-b7cb8dfbc93b">connection string</legacyLink> by setting properties of the <legacyBold>Connection</legacyBold> object before opening the connection.</caps:sentence>
          <caps:sentence sentenceid="877b8eca6ecad3577665900405aa86a2" id="tgt2" class="tgtSentence"> For example, you could achieve the same effect as the connection string discussed in <link xlink:href="14eae122-2d1e-40c8-b88e-b7cb8dfbc93b">Creating a Connection string</link> by using the following code.</caps:sentence>
        </para>
        <code>With objConn
.Provider = "SQLOLEDB"
.Properties("Data Source") = "MySqlServer"
   .Properties("Integrated Security") = "SSPI"
.Open
.DefaultDatabase = "Northwind"
End With</code>
        <para>
          <caps:sentence sentenceid="d181a36fc0b7e79318a6483793beaa6d" id="tgt3" class="tgtSentence">DefaultDatabase is set only after you open the connection.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="30bb4ee01bf0e3ffc7a984cb7fe49cda" id="tgt4" class="tgtSentence">In ADO you must not use a password containing semicolons (";") unless the password is enclosed in single quotation marks.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">You can supply much of the information specified by a <legacyLink xlink:href="14eae122-2d1e-40c8-b88e-b7cb8dfbc93b">connection string</legacyLink> by setting properties of the <legacyBold>Connection</legacyBold> object before opening the connection.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For example, you could achieve the same effect as the connection string discussed in <link xlink:href="14eae122-2d1e-40c8-b88e-b7cb8dfbc93b">Creating a Connection string</link> by using the following code.</caps:sentence>
        </para>
        <code>With objConn
.Provider = "SQLOLEDB"
.Properties("Data Source") = "MySqlServer"
   .Properties("Integrated Security") = "SSPI"
.Open
.DefaultDatabase = "Northwind"
End With</code>
        <para>
          <caps:sentence id="src3" class="srcSentence">DefaultDatabase is set only after you open the connection.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src4" class="srcSentence">In ADO you must not use a password containing semicolons (";") unless the password is enclosed in single quotation marks.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
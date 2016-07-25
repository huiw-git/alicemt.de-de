---
title: "SQLState Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f9e25967-54b0-444d-af2a-0d2c75365d3e
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
# SQLState Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0e2df6d1a4f83ee3a861e8a278c14290" id="tgt1" class="tgtSentence">Indicates the SQL state for a given <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7b14210f8abd63b3340b9772628d7545" id="tgt3" class="tgtSentence">Returns a five-character <languageKeyword>String</languageKeyword> value that follows the ANSI SQL standard and indicates the error code.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="5acae7ef76cb9daebe00ac879cae8891" id="tgt4" class="tgtSentence">Use the <legacyBold>SQLState</legacyBold> property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement.</caps:sentence>
            <caps:sentence sentenceid="2931f795f1603d4bad2e552e18c10729" id="tgt5" class="tgtSentence"> For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors.</caps:sentence>
            <caps:sentence sentenceid="693478af22cda2371fe944d56b357614" id="tgt6" class="tgtSentence"> These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5c728458-d85c-497c-afcf-2cfa36c3342a">Visual Basic Example</link>
        <link xlink:href="5321fc0f-cd0c-4e2a-a5bc-0008fba86b59">Visual C++ Example</link>
        <link xlink:href="7fd0eebc-99f4-490e-9b62-0b62b1884d6b">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the SQL state for a given <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a five-character <languageKeyword>String</languageKeyword> value that follows the ANSI SQL standard and indicates the error code.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>SQLState</legacyBold> property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5c728458-d85c-497c-afcf-2cfa36c3342a">Visual Basic Example</link>
        <link xlink:href="5321fc0f-cd0c-4e2a-a5bc-0008fba86b59">Visual C++ Example</link>
        <link xlink:href="7fd0eebc-99f4-490e-9b62-0b62b1884d6b">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
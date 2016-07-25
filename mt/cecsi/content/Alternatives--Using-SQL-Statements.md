---
title: "Alternatives: Using SQL Statements"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8b528b23-063d-45ea-8dea-6a90d4060b20
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
# Alternatives: Using SQL Statements
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c13f59bb447e109e1f1166f2f663ab70" id="tgt1" class="tgtSentence">ADO also allows using commands as alternatives to its built-in properties and methods for editing data.</caps:sentence>
          <caps:sentence sentenceid="d9cb3ac0f85232914d987217c9e08a2e" id="tgt2" class="tgtSentence"> Depending upon your provider, all operations mentioned in this section could also be accomplished by passing commands to your data source.</caps:sentence>
          <caps:sentence sentenceid="fe3b42c941fa67f84ea3a2ec100e3a2d" id="tgt3" class="tgtSentence"> For example, SQL UPDATE statements can be used to modify data without using the <legacyBold>Value</legacyBold> property of a <legacyBold>Field</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="5ada8019d23ac7212c3f2c8092d9dfd3" id="tgt4" class="tgtSentence"> SQL INSERT statements can be used to add new records to a data source, rather than the ADO method <legacyBold>AddNew</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="4f7b2721766224e464d19be2cd265093" id="tgt5" class="tgtSentence"> For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="34507f475c078fa1291d0b9f1a98277a" id="tgt6" class="tgtSentence">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</caps:sentence>
        </para>
        <code>    'BeginSQLDelete
    strSQL = "DELETE FROM Shippers WHERE ShipperID = " &amp; intId
    objConn1.Execute strSQL, , adCmdText + adExecuteNoRecords
    'EndSQLDelete</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO also allows using commands as alternatives to its built-in properties and methods for editing data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Depending upon your provider, all operations mentioned in this section could also be accomplished by passing commands to your data source.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For example, SQL UPDATE statements can be used to modify data without using the <legacyBold>Value</legacyBold> property of a <legacyBold>Field</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> SQL INSERT statements can be used to add new records to a data source, rather than the ADO method <legacyBold>AddNew</legacyBold>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</caps:sentence>
        </para>
        <code>    'BeginSQLDelete
    strSQL = "DELETE FROM Shippers WHERE ShipperID = " &amp; intId
    objConn1.Execute strSQL, , adCmdText + adExecuteNoRecords
    'EndSQLDelete</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
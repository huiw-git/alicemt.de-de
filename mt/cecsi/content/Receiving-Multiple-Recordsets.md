---
title: "Receiving Multiple Recordsets"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2a7ad7a6-f00d-4355-b0b5-d0ab957b0566
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
# Receiving Multiple Recordsets
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e5694b0113e6e3114b4f578e2b36c698" id="tgt1" class="tgtSentence">The <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink> supports returning multiple <legacyBold>Recordset</legacyBold> objects for a single command containing multiple SQL statements, one <legacyBold>Recordset</legacyBold> per SQL statement.</caps:sentence>
          <caps:sentence sentenceid="ea17d0894e6ca831fc152391eadcf144" id="tgt2" class="tgtSentence"> The order in which the <legacyBold>Recordset</legacyBold>s are returned follows the order in which the SQL statements are placed in the command text.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="880ddbc1d72c5ac5d58c5c65ff124efe" id="tgt3" class="tgtSentence">The Microsoft OLE DB Provider for SQL Server also returns multiple resultsets to ADO when the command contains a COMPUTE clause.</caps:sentence>
          <caps:sentence sentenceid="44b9cb6613b11daa2ad40f2ef15db481" id="tgt4" class="tgtSentence"> For example, a command containing the following SQL statement will return the results in two <legacyBold>Recordset</legacyBold> objects: one for the rowset of (<legacyItalic>ProductID</legacyItalic>, <legacyItalic>ProductName</legacyItalic>, <legacyItalic>UnitPrice</legacyItalic>), and the other for the average price of all products in the table.</caps:sentence>
        </para>
        <code>SELECT ProductID, ProductName, UnitPrice 
  FROM PRODUCTS 
  COMPUTE AVG(UnitPrice)</code>
        <para>
          <caps:sentence sentenceid="c393e70fef6a164860e1ee746cbe0007" id="tgt5" class="tgtSentence">You can use the <legacyBold>Recordset.NextRecordset</legacyBold> method to enumerate the two objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1ca9c73efce1b18568cdd4982f82a239" id="tgt6" class="tgtSentence">For more information, see <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink> supports returning multiple <legacyBold>Recordset</legacyBold> objects for a single command containing multiple SQL statements, one <legacyBold>Recordset</legacyBold> per SQL statement.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The order in which the <legacyBold>Recordset</legacyBold>s are returned follows the order in which the SQL statements are placed in the command text.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">The Microsoft OLE DB Provider for SQL Server also returns multiple resultsets to ADO when the command contains a COMPUTE clause.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example, a command containing the following SQL statement will return the results in two <legacyBold>Recordset</legacyBold> objects: one for the rowset of (<legacyItalic>ProductID</legacyItalic>, <legacyItalic>ProductName</legacyItalic>, <legacyItalic>UnitPrice</legacyItalic>), and the other for the average price of all products in the table.</caps:sentence>
        </para>
        <code>SELECT ProductID, ProductName, UnitPrice 
  FROM PRODUCTS 
  COMPUTE AVG(UnitPrice)</code>
        <para>
          <caps:sentence id="src5" class="srcSentence">You can use the <legacyBold>Recordset.NextRecordset</legacyBold> method to enumerate the two objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">For more information, see <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
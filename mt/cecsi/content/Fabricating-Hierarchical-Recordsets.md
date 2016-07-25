---
title: "Fabricating Hierarchical Recordsets"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a584e642-a4a3-418e-bc20-3aff81a5625a
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
# Fabricating Hierarchical Recordsets
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="eb989565daf2be14477a3fffcf67d639" id="tgt1" class="tgtSentence">The following example shows how to fabricate a hierarchical Recordset without an underlying data source by using the data shaping grammar to define columns for parent, child, and grandchild <legacyBold>Recordsets</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="880b84112aca53a59d585583adfb35a7" id="tgt2" class="tgtSentence">To fabricate a hierarchical <legacyBold>Recordset</legacyBold>, you must specify the <link xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</link> (MSDataShape), and you can specify a Data Provider value of NONE in the connection string parameter of the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="74588fe300ccda6ea58f5108d69984c7" id="tgt3" class="tgtSentence"> For more information, see <legacyLink xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</legacyLink>.</caps:sentence>
        </para>
        <code>Dim cn As New ADODB.Connection
Dim rsCustomers As New ADODB.Recordset

cn.Open "Provider=MSDataShape;Data Provider=NONE;"
 
strShape = _
"SHAPE APPEND NEW adInteger AS CustID," &amp; _
            " NEW adChar(25) AS FirstName," &amp; _
            " NEW adChar(25) AS LastName," &amp; _
            " NEW adChar(12) AS SSN," &amp; _
            " NEW adChar(50) AS Address," &amp; _
         " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," &amp; _
                        " NEW adInteger AS CustID," &amp; _
                        " NEW adChar(20) AS BodyColor, " &amp; _
                     " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," &amp; _
                                    " NEW adChar(20) AS Make, " &amp; _
                                    " NEW adChar(20) AS Model," &amp; _
                                    " NEW adChar(4) AS Year) " &amp; _
                        " AS VINS RELATE VIN_NO TO VIN_NO))" &amp; _
            " AS Vehicles RELATE CustID TO CustID) "
 
rsCustomers.Open strShape, cn, adOpenStatic, adLockOptimistic, -1</code>
        <para>
          <caps:sentence sentenceid="e583249161b278c3c270e5eeb65040bf" id="tgt4" class="tgtSentence">As soon as the <legacyBold>Recordset</legacyBold> has been fabricated, it can be populated, manipulated, or persisted to a file.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</link>
        <link xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">Shape APPEND Clause</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following example shows how to fabricate a hierarchical Recordset without an underlying data source by using the data shaping grammar to define columns for parent, child, and grandchild <legacyBold>Recordsets</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">To fabricate a hierarchical <legacyBold>Recordset</legacyBold>, you must specify the <link xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</link> (MSDataShape), and you can specify a Data Provider value of NONE in the connection string parameter of the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For more information, see <legacyLink xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</legacyLink>.</caps:sentence>
        </para>
        <code>Dim cn As New ADODB.Connection
Dim rsCustomers As New ADODB.Recordset

cn.Open "Provider=MSDataShape;Data Provider=NONE;"
 
strShape = _
"SHAPE APPEND NEW adInteger AS CustID," &amp; _
            " NEW adChar(25) AS FirstName," &amp; _
            " NEW adChar(25) AS LastName," &amp; _
            " NEW adChar(12) AS SSN," &amp; _
            " NEW adChar(50) AS Address," &amp; _
         " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," &amp; _
                        " NEW adInteger AS CustID," &amp; _
                        " NEW adChar(20) AS BodyColor, " &amp; _
                     " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," &amp; _
                                    " NEW adChar(20) AS Make, " &amp; _
                                    " NEW adChar(20) AS Model," &amp; _
                                    " NEW adChar(4) AS Year) " &amp; _
                        " AS VINS RELATE VIN_NO TO VIN_NO))" &amp; _
            " AS Vehicles RELATE CustID TO CustID) "
 
rsCustomers.Open strShape, cn, adOpenStatic, adLockOptimistic, -1</code>
        <para>
          <caps:sentence id="src4" class="srcSentence">As soon as the <legacyBold>Recordset</legacyBold> has been fabricated, it can be populated, manipulated, or persisted to a file.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</link>
        <link xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">Shape APPEND Clause</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
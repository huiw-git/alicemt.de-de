---
title: "Resync Command Property-Dynamic (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 4e2bb601-0fe8-4d61-b00e-38341d85a6bb
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
# Resync Command Property-Dynamic (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="75205c0cb364dc50b430e0cbd480fbe3" id="tgt1" class="tgtSentence">Specifies a user-supplied command string that the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method issues to refresh the data in the table named in the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> dynamic property.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5311cc30a6ec1ae7db468ceb40afaaf8" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value which is a command string.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="0387c6540e0912555360a140735c0652" id="tgt4" class="tgtSentence">The <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object is the result of a JOIN operation executed on multiple base tables.</caps:sentence>
            <caps:sentence sentenceid="426fa331c6ddcc82fb458ba9254a9c7e" id="tgt5" class="tgtSentence"> The rows affected depend on the <legacyItalic>AffectRecords</legacyItalic> parameter of the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="3ba20fdfba7d5f4000cd7dd9e30aabfc" id="tgt6" class="tgtSentence"> The standard <legacyBold>Resync</legacyBold> method is executed if the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> and <legacyBold>Resync Command</legacyBold> properties are not set.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4b77a024979fdf27745a8b209067f83d" id="tgt7" class="tgtSentence">The command string of the <legacyBold>Resync Command</legacyBold> property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed.</caps:sentence>
            <caps:sentence sentenceid="97b3abf8a8f2b35a8fd45878b597dbee" id="tgt8" class="tgtSentence"> The command string contains a parameter for each primary key column in the <legacyBold>Unique Table</legacyBold>; otherwise, a run-time error is returned.</caps:sentence>
            <caps:sentence sentenceid="8a9051beb59a8ab23db17523da481807" id="tgt9" class="tgtSentence"> The parameters are automatically filled in with primary key values from the row to be refreshed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fafb428267d99e98429c64ecb82b5850" id="tgt10" class="tgtSentence">Here are two examples based on SQL:</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b444607503217bc344e4299725d7ac39" id="tgt11" class="tgtSentence">1) The <legacyBold>Recordset</legacyBold> is defined by a command:</caps:sentence>
          </para>
          <code>SELECT * FROM Customers JOIN Orders ON 
   Customers.CustomerID = Orders.CustomerID
   WHERE city = 'Seattle'
   ORDER BY CustomerID</code>
          <para>
            <caps:sentence sentenceid="1a5819ef75e397cd58d5afc665f57325" id="tgt12" class="tgtSentence">The <legacyBold>Resync Command</legacyBold> property is set to:</caps:sentence>
          </para>
          <code>"SELECT * FROM 
   (SELECT * FROM Customers JOIN Orders 
   ON Customers.CustomerID = Orders.CustomerID
   city = 'Seattle' ORDER BY CustomerID)
WHERE Orders.OrderID = ?"</code>
          <para>
            <caps:sentence sentenceid="ee70944dd2ad1c2ede7dbc1e7bcd7a9d" id="tgt13" class="tgtSentence">The <legacyBold>Unique Table</legacyBold> is <legacyItalic>Orders</legacyItalic> and its primary key, <legacyItalic>OrderID</legacyItalic>, is parameterized.</caps:sentence>
            <caps:sentence sentenceid="6e3ca146396e5d2c1181aa01ebf90dc5" id="tgt14" class="tgtSentence"> The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ba9b6ac4ac30fa3ab9743d0ff23560ae" id="tgt15" class="tgtSentence">2) The <legacyBold>Recordset</legacyBold> is defined by a stored procedure:</caps:sentence>
          </para>
          <code>CREATE PROC Custorders @CustomerID char(5) AS 
SELECT * FROM Customers JOIN Orders ON 
Customers.CustomerID = Orders.CustomerID 
WHERE Customers.CustomerID = @CustomerID</code>
          <para>
            <caps:sentence sentenceid="a2f7613372b13f2cce6e7e512156bed2" id="tgt16" class="tgtSentence">The <legacyBold>Resync</legacyBold> method should execute the following stored procedure:</caps:sentence>
          </para>
          <code>CREATE PROC CustordersResync @ordid int AS 
SELECT * FROM Customers JOIN Orders ON 
Customers.CustomerID = Orders.CustomerID
WHERE Orders.ordid  = @ordid</code>
          <para>
            <caps:sentence sentenceid="1a5819ef75e397cd58d5afc665f57325" id="tgt17" class="tgtSentence">The <legacyBold>Resync Command</legacyBold> property is set to:</caps:sentence>
          </para>
          <code>"{call CustordersResync (?)}"</code>
          <para>
            <caps:sentence sentenceid="baba997a61d9aaa4630c7bce219e40aa" id="tgt18" class="tgtSentence">Once again, the <legacyBold>Unique Table</legacyBold> is <legacyItalic>Orders</legacyItalic> and its primary key, <legacyItalic>OrderID</legacyItalic>, is parameterized.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8fecb13caeef048872b5fbacf59eaca4" id="tgt19" class="tgtSentence">
              <legacyBold>Resync Command</legacyBold> is a dynamic property appended to the <legacyBold>Recordset</legacyBold> object <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt20" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies a user-supplied command string that the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method issues to refresh the data in the table named in the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> dynamic property.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value which is a command string.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object is the result of a JOIN operation executed on multiple base tables.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The rows affected depend on the <legacyItalic>AffectRecords</legacyItalic> parameter of the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The standard <legacyBold>Resync</legacyBold> method is executed if the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> and <legacyBold>Resync Command</legacyBold> properties are not set.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The command string of the <legacyBold>Resync Command</legacyBold> property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The command string contains a parameter for each primary key column in the <legacyBold>Unique Table</legacyBold>; otherwise, a run-time error is returned.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The parameters are automatically filled in with primary key values from the row to be refreshed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">Here are two examples based on SQL:</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">1) The <legacyBold>Recordset</legacyBold> is defined by a command:</caps:sentence>
          </para>
          <code>SELECT * FROM Customers JOIN Orders ON 
   Customers.CustomerID = Orders.CustomerID
   WHERE city = 'Seattle'
   ORDER BY CustomerID</code>
          <para>
            <caps:sentence id="src12" class="srcSentence">The <legacyBold>Resync Command</legacyBold> property is set to:</caps:sentence>
          </para>
          <code>"SELECT * FROM 
   (SELECT * FROM Customers JOIN Orders 
   ON Customers.CustomerID = Orders.CustomerID
   city = 'Seattle' ORDER BY CustomerID)
WHERE Orders.OrderID = ?"</code>
          <para>
            <caps:sentence id="src13" class="srcSentence">The <legacyBold>Unique Table</legacyBold> is <legacyItalic>Orders</legacyItalic> and its primary key, <legacyItalic>OrderID</legacyItalic>, is parameterized.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">2) The <legacyBold>Recordset</legacyBold> is defined by a stored procedure:</caps:sentence>
          </para>
          <code>CREATE PROC Custorders @CustomerID char(5) AS 
SELECT * FROM Customers JOIN Orders ON 
Customers.CustomerID = Orders.CustomerID 
WHERE Customers.CustomerID = @CustomerID</code>
          <para>
            <caps:sentence id="src16" class="srcSentence">The <legacyBold>Resync</legacyBold> method should execute the following stored procedure:</caps:sentence>
          </para>
          <code>CREATE PROC CustordersResync @ordid int AS 
SELECT * FROM Customers JOIN Orders ON 
Customers.CustomerID = Orders.CustomerID
WHERE Orders.ordid  = @ordid</code>
          <para>
            <caps:sentence id="src17" class="srcSentence">The <legacyBold>Resync Command</legacyBold> property is set to:</caps:sentence>
          </para>
          <code>"{call CustordersResync (?)}"</code>
          <para>
            <caps:sentence id="src18" class="srcSentence">Once again, the <legacyBold>Unique Table</legacyBold> is <legacyItalic>Orders</legacyItalic> and its primary key, <legacyItalic>OrderID</legacyItalic>, is parameterized.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">
              <legacyBold>Resync Command</legacyBold> is a dynamic property appended to the <legacyBold>Recordset</legacyBold> object <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
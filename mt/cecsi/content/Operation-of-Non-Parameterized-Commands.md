---
title: "Operation of Non-Parameterized Commands"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9700e50a-9f17-4ba3-8afb-f750741dc6ca
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
# Operation of Non-Parameterized Commands
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8306369badba61a4d5483e746a2833d3" id="tgt1" class="tgtSentence">For non-parameterized commands, all the provider commands are executed and the <legacyBold>Recordsets</legacyBold> are created during command execution.</caps:sentence>
          <caps:sentence sentenceid="80647a5d0d7f13b9c19517ee0ac97402" id="tgt2" class="tgtSentence"> If the command is executed synchronously, all the <legacyBold>Recordsets</legacyBold> will be fully populated.</caps:sentence>
          <caps:sentence sentenceid="c14543c102b1c0a5ac8996579dff3699" id="tgt3" class="tgtSentence"> If an asynchronous population mode was selected, the populated state of the <legacyBold>Recordsets</legacyBold> will depend on the population mode and the size of the <legacyBold>Recordsets</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b53b940f1a2e8d693c0719fa9847aa58" id="tgt4" class="tgtSentence">For example, the <legacyItalic>parent-command</legacyItalic> could return a <legacyBold>Recordset</legacyBold> of customers for a company from a Customers table, and the <legacyItalic>child-command</legacyItalic> could return a <legacyBold>Recordset</legacyBold> of orders for all customers from an Orders table.</caps:sentence>
        </para>
        <code>SHAPE {SELECT * FROM Customers} 
   APPEND ({SELECT * FROM Orders} AS chapOrders 
   RELATE customerID TO customerID)</code>
        <para>
          <caps:sentence sentenceid="ecf39e8b7029460cfb226118332015e6" id="tgt5" class="tgtSentence">For non-parameterized parent-child relationships, each parent and child <legacyBold>Recordset</legacyBold> object must have a column in common to associate them.</caps:sentence>
          <caps:sentence sentenceid="2c1144ef8db016d3092dd947aaa17239" id="tgt6" class="tgtSentence"> The columns are named in the RELATE clause, <legacyItalic>parent-column</legacyItalic> first and then <legacyItalic>child-column</legacyItalic>.</caps:sentence>
          <caps:sentence sentenceid="02677071ca5ab0ed0da12dd24766e960" id="tgt7" class="tgtSentence"> The columns may have different names in their respective <legacyBold>Recordset</legacyBold> objects but must refer to the same information in order to specify a meaningful relation.</caps:sentence>
          <caps:sentence sentenceid="1d72e2cf98ff4e5a229cdd9eabb702fa" id="tgt8" class="tgtSentence"> For example, the <legacyBold>Customers</legacyBold> and <legacyBold>Orders</legacyBold> <legacyBold>Recordset</legacyBold> objects could both have a customerID field.</caps:sentence>
          <caps:sentence sentenceid="53f2d1e805a254d35a97ff09ff5abd9b" id="tgt9" class="tgtSentence"> Because the membership of the child <legacyBold>Recordset</legacyBold> is determined by the provider command, the child <legacyBold>Recordset</legacyBold> can contain orphaned rows.</caps:sentence>
          <caps:sentence sentenceid="48b48bf0959a47e1a208af2b9690519d" id="tgt10" class="tgtSentence"> These orphaned rows are inaccessible without additional reshaping.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0049f8c42627dd11e211549c28ce4bb9" id="tgt11" class="tgtSentence">Data shaping appends a chapter column to the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="952281315d0917294d90f3a78b95a911" id="tgt12" class="tgtSentence"> The values in the chapter column are references to rows in the child <legacyBold>Recordset</legacyBold>, which satisfy the RELATE clause.</caps:sentence>
          <caps:sentence sentenceid="6d4562882c99da9fb365717ed6c8c071" id="tgt13" class="tgtSentence"> That is, the same value is in the <legacyItalic>parent-column</legacyItalic> of a given parent row as is in the <legacyItalic>child-column </legacyItalic>of all the rows of the chapter child.</caps:sentence>
          <caps:sentence sentenceid="e5e11dfb5ece76f788c1dc2ac62e529a" id="tgt14" class="tgtSentence"> When multiple TO clauses are used in the same RELATE clause, they are implicitly combined using an AND operator.</caps:sentence>
          <caps:sentence sentenceid="541dffc82c927d0b62be4924a350c790" id="tgt15" class="tgtSentence"> If the parent columns in the RELATE clause do not constitute a key to the parent <legacyBold>Recordset</legacyBold>, a single child row can have multiple parent rows.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ccb662b685f034b1c0c75e56c9e07c6d" id="tgt16" class="tgtSentence">When you access the reference in the chapter column, ADO automatically retrieves the <legacyBold>Recordset</legacyBold> represented by the reference.</caps:sentence>
          <caps:sentence sentenceid="3f4a2b96e15ea69228c3068b8ce1402e" id="tgt17" class="tgtSentence"> Note that in a non-parameterized command, although the entire child <legacyBold>Recordset</legacyBold> has been retrieved, the chapter only presents a subset of rows.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3b3f952f1f63115b2f792760bdc98e57" id="tgt18" class="tgtSentence">If the appended column has no <legacyItalic>chapter-alias</legacyItalic>, a name will be generated for it automatically.</caps:sentence>
          <caps:sentence sentenceid="c9b6c7b29d36546a2870a51ff0d66d2e" id="tgt19" class="tgtSentence"> A <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object for the column will be appended to the <legacyBold>Recordset</legacyBold> object's <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection, and its data type will be <legacyBold>adChapter</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3ebefc452fcb566d56f258d2209c224b" id="tgt20" class="tgtSentence">For information about navigating a hierarchical <legacyBold>Recordset</legacyBold>, see <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">For non-parameterized commands, all the provider commands are executed and the <legacyBold>Recordsets</legacyBold> are created during command execution.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> If the command is executed synchronously, all the <legacyBold>Recordsets</legacyBold> will be fully populated.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> If an asynchronous population mode was selected, the populated state of the <legacyBold>Recordsets</legacyBold> will depend on the population mode and the size of the <legacyBold>Recordsets</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">For example, the <legacyItalic>parent-command</legacyItalic> could return a <legacyBold>Recordset</legacyBold> of customers for a company from a Customers table, and the <legacyItalic>child-command</legacyItalic> could return a <legacyBold>Recordset</legacyBold> of orders for all customers from an Orders table.</caps:sentence>
        </para>
        <code>SHAPE {SELECT * FROM Customers} 
   APPEND ({SELECT * FROM Orders} AS chapOrders 
   RELATE customerID TO customerID)</code>
        <para>
          <caps:sentence id="src5" class="srcSentence">For non-parameterized parent-child relationships, each parent and child <legacyBold>Recordset</legacyBold> object must have a column in common to associate them.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The columns are named in the RELATE clause, <legacyItalic>parent-column</legacyItalic> first and then <legacyItalic>child-column</legacyItalic>.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> The columns may have different names in their respective <legacyBold>Recordset</legacyBold> objects but must refer to the same information in order to specify a meaningful relation.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> For example, the <legacyBold>Customers</legacyBold> and <legacyBold>Orders</legacyBold> <legacyBold>Recordset</legacyBold> objects could both have a customerID field.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> Because the membership of the child <legacyBold>Recordset</legacyBold> is determined by the provider command, the child <legacyBold>Recordset</legacyBold> can contain orphaned rows.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> These orphaned rows are inaccessible without additional reshaping.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">Data shaping appends a chapter column to the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> The values in the chapter column are references to rows in the child <legacyBold>Recordset</legacyBold>, which satisfy the RELATE clause.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> That is, the same value is in the <legacyItalic>parent-column</legacyItalic> of a given parent row as is in the <legacyItalic>child-column </legacyItalic>of all the rows of the chapter child.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> When multiple TO clauses are used in the same RELATE clause, they are implicitly combined using an AND operator.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> If the parent columns in the RELATE clause do not constitute a key to the parent <legacyBold>Recordset</legacyBold>, a single child row can have multiple parent rows.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src16" class="srcSentence">When you access the reference in the chapter column, ADO automatically retrieves the <legacyBold>Recordset</legacyBold> represented by the reference.</caps:sentence>
          <caps:sentence id="src17" class="srcSentence"> Note that in a non-parameterized command, although the entire child <legacyBold>Recordset</legacyBold> has been retrieved, the chapter only presents a subset of rows.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src18" class="srcSentence">If the appended column has no <legacyItalic>chapter-alias</legacyItalic>, a name will be generated for it automatically.</caps:sentence>
          <caps:sentence id="src19" class="srcSentence"> A <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object for the column will be appended to the <legacyBold>Recordset</legacyBold> object's <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection, and its data type will be <legacyBold>adChapter</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src20" class="srcSentence">For information about navigating a hierarchical <legacyBold>Recordset</legacyBold>, see <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
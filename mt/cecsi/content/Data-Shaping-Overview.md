---
title: "Data Shaping Overview"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4cb5fd29-4e56-46ac-ae48-a6771c321c0c
caps.latest.revision: 9
caps.handback.revision: 9
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
# Data Shaping Overview
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="328da94bcc7e6759b9e8989bc3144c9d" id="tgt1" class="tgtSentence">       <legacyItalic>Data shaping</legacyItalic> means building hierarchical relationships between two or more logical entities in a query.</caps:sentence>
          <caps:sentence sentenceid="e0291d0b2df1374be6228654a53ede42" id="tgt2" class="tgtSentence"> The hierarchy can be seen in parent-child relationships between a record of one <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and one or more records (also known as a chapter) of another <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="7059a506004559fa29c29e7cdf68c65a" id="tgt3" class="tgtSentence"> In a parent-child relationship, the parent <legacyBold>Recordset</legacyBold> contains the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="499452b8ea09aad3f835da52f0bd5c7a" id="tgt4" class="tgtSentence"> An example of such a hierarchical relationship is customers and orders.</caps:sentence>
          <caps:sentence sentenceid="779afd5e44f9360435219c1f21eb52cd" id="tgt5" class="tgtSentence"> For every customer in a database, there can be zero or more orders.</caps:sentence>
          <caps:sentence sentenceid="372ccfede8df03dea9158d6b1ff4dbaf" id="tgt6" class="tgtSentence"> The hierarchical relationship can be recursive, meaning that grandchild records can be nested in a child record.</caps:sentence>
          <caps:sentence sentenceid="19b5108e2bee3367a3802dc6eed71c71" id="tgt7" class="tgtSentence"> In principle, a hierarchical record can be nested to any depth.</caps:sentence>
          <caps:sentence sentenceid="f349abb36760b342160595c87d4b3ddf" id="tgt8" class="tgtSentence"> In practice, ADO limits the recursion to a maximum of 512 <legacyBold>Recordset</legacyBold>s.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ba15ba654747fcb5aa106c69204d8d87" id="tgt9" class="tgtSentence">In general, columns of a shaped <legacyBold>Recordset</legacyBold> can contain data from a data provider such as Microsoft® SQL Server, references to another <legacyBold>Recordset</legacyBold>, values derived from a calculation on a single row of a <legacyBold>Recordset</legacyBold>, or values derived from an operation over a column of an entire <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="f8c2ba001e6c943c5a96f013d548e841" id="tgt10" class="tgtSentence"> A column can also be newly fabricated and empty.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f00920d339e44473254cdde6f1d43c9d" id="tgt11" class="tgtSentence">When you retrieve the value of a column that contains a reference to another <legacyBold>Recordset</legacyBold>, ADO automatically returns the actual <legacyBold>Recordset</legacyBold> represented by the reference.</caps:sentence>
          <caps:sentence sentenceid="2a3b0c67c4b02750ba02dc06ff8bfabf" id="tgt12" class="tgtSentence"> The reference to a <legacyBold>Recordset</legacyBold> is actually a reference to a subset of the child, called a <legacyItalic>chapter</legacyItalic>.</caps:sentence>
          <caps:sentence sentenceid="7d8fdbada3462978ea12fa5c2c0f4b98" id="tgt13" class="tgtSentence"> A single parent can reference more than one child <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="65c73063f62876bfbb7275843a2753d4" id="tgt14" class="tgtSentence">ADO support for data shaping enables you to query a data source and return a <legacyBold>Recordset</legacyBold> in which a (parent) record represents a (child) <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="1cb12065437ef4b52096dd746e9776b4" id="tgt15" class="tgtSentence"> In the customer-order scenario, you can use data shaping to retrieve customers' information as well as the orders placed by each customer in a single query.</caps:sentence>
          <caps:sentence sentenceid="04c31ef9464ad5133f1ab57b7bcd9755" id="tgt16" class="tgtSentence"> The resultant <legacyBold>Recordset</legacyBold> is also known as shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1e9e2bb28ff485228cb846b4d9c1d6ea" id="tgt17" class="tgtSentence">In addition, data shaping in ADO allows you to create new <legacyBold>Recordset</legacyBold> objects without an underlying data source by using the <legacyBold>NEW</legacyBold> keyword to describe the fields of the parent and child <legacyBold>Recordsets</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="45f6cd46189814c69636672ab43b9308" id="tgt18" class="tgtSentence"> The new <legacyBold>Recordset</legacyBold> object can then be populated with data and persistently stored.</caps:sentence>
          <caps:sentence sentenceid="f8838a5076507dbdb8ba94fb3a6f2cc2" id="tgt19" class="tgtSentence"> Developers can also perform various calculations or aggregations (for example, <legacyBold>SUM</legacyBold>, <legacyBold>AVG</legacyBold>, and <legacyBold>MAX</legacyBold>) on child fields.</caps:sentence>
          <caps:sentence sentenceid="43cb6bd536d1852a4c56fa3c8d9b66d6" id="tgt20" class="tgtSentence"> Data shaping can also create a parent <legacyBold>Recordset</legacyBold> from a child <legacyBold>Recordset</legacyBold> by grouping records in the child and placing one row in the parent for each group in the child.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="14eaec6781a25cfdead004eaf5f9a9e4" id="tgt21" class="tgtSentence">Regular SQL allows you to retrieve data using <legacyBold>JOIN</legacyBold> syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</caps:sentence>
          <caps:sentence sentenceid="fbe11493cd1263709b095cb85fbe1004" id="tgt22" class="tgtSentence"> Data shaping can relate a single parent record in the parent <legacyBold>Recordset</legacyBold> to multiple child records in the child <legacyBold>Recordset</legacyBold>, avoiding the redundancy of a <legacyBold>JOIN</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="04dec12c42ae9b47d9ccb14867a2f0f1" id="tgt23" class="tgtSentence"> Most people find the parent-child multiple <legacyBold>Recordset</legacyBold> programming model more natural and easier to work with than the single <legacyBold>Recordset</legacyBold> <legacyBold>JOIN</legacyBold> model.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">       <legacyItalic>Data shaping</legacyItalic> means building hierarchical relationships between two or more logical entities in a query.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The hierarchy can be seen in parent-child relationships between a record of one <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and one or more records (also known as a chapter) of another <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> In a parent-child relationship, the parent <legacyBold>Recordset</legacyBold> contains the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> An example of such a hierarchical relationship is customers and orders.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> For every customer in a database, there can be zero or more orders.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The hierarchical relationship can be recursive, meaning that grandchild records can be nested in a child record.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> In principle, a hierarchical record can be nested to any depth.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> In practice, ADO limits the recursion to a maximum of 512 <legacyBold>Recordset</legacyBold>s.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">In general, columns of a shaped <legacyBold>Recordset</legacyBold> can contain data from a data provider such as Microsoft® SQL Server, references to another <legacyBold>Recordset</legacyBold>, values derived from a calculation on a single row of a <legacyBold>Recordset</legacyBold>, or values derived from an operation over a column of an entire <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> A column can also be newly fabricated and empty.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">When you retrieve the value of a column that contains a reference to another <legacyBold>Recordset</legacyBold>, ADO automatically returns the actual <legacyBold>Recordset</legacyBold> represented by the reference.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> The reference to a <legacyBold>Recordset</legacyBold> is actually a reference to a subset of the child, called a <legacyItalic>chapter</legacyItalic>.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> A single parent can reference more than one child <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">ADO support for data shaping enables you to query a data source and return a <legacyBold>Recordset</legacyBold> in which a (parent) record represents a (child) <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> In the customer-order scenario, you can use data shaping to retrieve customers' information as well as the orders placed by each customer in a single query.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> The resultant <legacyBold>Recordset</legacyBold> is also known as shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src17" class="srcSentence">In addition, data shaping in ADO allows you to create new <legacyBold>Recordset</legacyBold> objects without an underlying data source by using the <legacyBold>NEW</legacyBold> keyword to describe the fields of the parent and child <legacyBold>Recordsets</legacyBold>.</caps:sentence>
          <caps:sentence id="src18" class="srcSentence"> The new <legacyBold>Recordset</legacyBold> object can then be populated with data and persistently stored.</caps:sentence>
          <caps:sentence id="src19" class="srcSentence"> Developers can also perform various calculations or aggregations (for example, <legacyBold>SUM</legacyBold>, <legacyBold>AVG</legacyBold>, and <legacyBold>MAX</legacyBold>) on child fields.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> Data shaping can also create a parent <legacyBold>Recordset</legacyBold> from a child <legacyBold>Recordset</legacyBold> by grouping records in the child and placing one row in the parent for each group in the child.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src21" class="srcSentence">Regular SQL allows you to retrieve data using <legacyBold>JOIN</legacyBold> syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> Data shaping can relate a single parent record in the parent <legacyBold>Recordset</legacyBold> to multiple child records in the child <legacyBold>Recordset</legacyBold>, avoiding the redundancy of a <legacyBold>JOIN</legacyBold>.</caps:sentence>
          <caps:sentence id="src23" class="srcSentence"> Most people find the parent-child multiple <legacyBold>Recordset</legacyBold> programming model more natural and easier to work with than the single <legacyBold>Recordset</legacyBold> <legacyBold>JOIN</legacyBold> model.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
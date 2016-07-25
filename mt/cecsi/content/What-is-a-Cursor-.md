---
title: "What is a Cursor?"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 596eb4b6-c22f-4cde-b23f-172dd66c3161
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
# What is a Cursor?
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="981454cfbd14335cd56353d40995725f" id="tgt1" class="tgtSentence">Operations in a relational database act on a complete set of rows.</caps:sentence>
          <caps:sentence sentenceid="034b2f768a7485366141701d9ee2f6a6" id="tgt2" class="tgtSentence"> The set of rows returned by a SELECT statement consists of all the rows that satisfy the conditions in the WHERE clause of the statement.</caps:sentence>
          <caps:sentence sentenceid="fe502de60fabdc13dd442edc2d499edc" id="tgt3" class="tgtSentence"> This complete set of rows returned by the statement is known as the result set.</caps:sentence>
          <caps:sentence sentenceid="a4e66651212ccb45ae3477791c9437a5" id="tgt4" class="tgtSentence"> Applications, especially those that are interactive and online, cannot always work effectively with the entire result set as a unit.</caps:sentence>
          <caps:sentence sentenceid="6893021d25ed85d69eef1b90194b27c2" id="tgt5" class="tgtSentence"> These applications need a mechanism to work with one row or a small block of rows at a time.</caps:sentence>
          <caps:sentence sentenceid="657623837ccbadb41d437bab59a5a3b9" id="tgt6" class="tgtSentence"> Cursors are an extension to result sets that provide that mechanism.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="02cf9b893f1892f3945e2e8f1236438f" id="tgt7" class="tgtSentence">A cursor is implemented by a cursor library.</caps:sentence>
          <caps:sentence sentenceid="3e3d0fca2b6dedcb016d0ce79be37b2c" id="tgt8" class="tgtSentence"> A cursor library is software, often implemented as a part of a database system or a data access API, that is used to manage attributes of data returned from a data source (a result set).</caps:sentence>
          <caps:sentence sentenceid="95e59e9b9330e8d5df0da81c67fb151d" id="tgt9" class="tgtSentence"> These attributes include concurrency management, position in the result set, number of rows returned, and whether you can move forward or backward (or both) through the result set (scrollability).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f0cb95ae399f9b342e5846847173a9ce" id="tgt10" class="tgtSentence">A cursor keeps track of the position in the result set, and allows you to perform multiple operations row by row against a result set, with or without returning to the original table.</caps:sentence>
          <caps:sentence sentenceid="5a8e678f099c296d67dfcb806f9a9e7d" id="tgt11" class="tgtSentence"> In other words, cursors conceptually return a result set based on tables within the databases.</caps:sentence>
          <caps:sentence sentenceid="73916967d862e1f5e840e1a0059677a9" id="tgt12" class="tgtSentence"> The cursor is so named because it indicates the current position in the result set, just as the cursor on a computer screen indicates current position.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fe16bbb197516c20ffafd2cff5fe92f5" id="tgt13" class="tgtSentence">It is important to become familiar with the concept of cursors before moving on to learn the specifics of their usage in ADO.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e1b721d4ba56c5946299d8d62cdcfce3" id="tgt14" class="tgtSentence">Using cursors, you can:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="6136fe42347be0d568fe6a96c3ef5320" id="tgt15" class="tgtSentence">Specify positioning at specific rows in the result set.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4d066418b2a580cba92bf2cd36aefd24" id="tgt16" class="tgtSentence">Retrieve one row or a block of rows based on the current result set position.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ce8ce53969a69174b0a2878fb370e2cb" id="tgt17" class="tgtSentence">Modify data in the rows at the current position in the result set.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="bb88558816c56a8e631725c0eaff7898" id="tgt18" class="tgtSentence">Define different levels of sensitivity to data changes made by other users.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="69e826727c30d9ff215c5475617870bf" id="tgt19" class="tgtSentence">For example, consider an application that displays a list of available products to a potential buyer.</caps:sentence>
          <caps:sentence sentenceid="e8aa29a813bffc4346ea32790ef79634" id="tgt20" class="tgtSentence"> The buyer scrolls through the list to see product details and cost, and finally selects a product for purchase.</caps:sentence>
          <caps:sentence sentenceid="9d98fa591794f8d312a2c0e7ae05b15e" id="tgt21" class="tgtSentence"> Additional scrolling and selection occurs for the remainder of the list.</caps:sentence>
          <caps:sentence sentenceid="2f4b889604149fe787b5cf1ab4f95f3d" id="tgt22" class="tgtSentence"> As far as the buyer is concerned, the products appear one at a time, but the application uses a scrollable cursor to browse up and down through the result set.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8c65ade7c24d0c2258012d730271a744" id="tgt23" class="tgtSentence">You can use cursors in a variety of ways:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="40f775ee444003bd3c17aca05956d2de" id="tgt24" class="tgtSentence">With no rows at all.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a85e444db7e4918a7505f1ecce927a47" id="tgt25" class="tgtSentence">With some or all of the rows in a single table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4e10869c64d7d787dd5132e028958d97" id="tgt26" class="tgtSentence">With some or all of the rows from logically joined tables.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e347c671094d5d3e8cdd65308392f1a0" id="tgt27" class="tgtSentence">As read-only or updateable at the cursor or field level.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ec99a3d4f5d19b857feb387257af9100" id="tgt28" class="tgtSentence">As forward-only or fully scrollable.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8849ce2b7a003eff8aacf11a78a21816" id="tgt29" class="tgtSentence">With the cursor keyset located on the server.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e9c721935c9f4f67a3780db987574cd1" id="tgt30" class="tgtSentence">Sensitive to underlying table changes caused by other applications (such as membership, sort, inserts, updates, and deletes).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d1cb9e77950f63bd5dfb1618da02ed76" id="tgt31" class="tgtSentence">Existing on either the server or the client.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="0e29300d5df85456664d6312408252be" id="tgt32" class="tgtSentence">Read-only cursors help users browse through the result set, and read/write cursors can implement individual row updates.</caps:sentence>
          <caps:sentence sentenceid="a9141a232c522c961a4cc5e17edbc7a2" id="tgt33" class="tgtSentence"> Complex cursors can be defined with keysets that point back to base table rows.</caps:sentence>
          <caps:sentence sentenceid="063bac80d316b8063f9c8e2f01f744cc" id="tgt34" class="tgtSentence"> Although some cursors are read-only in a forward direction, others can move back and forth and provide a dynamic refresh of the result set based on changes that other applications are making to the database.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="d870bf30eb1bd74ecba27317c9bb24d6" id="tgt35" class="tgtSentence">Not all applications need to use cursors to access or update data.</caps:sentence>
          <caps:sentence sentenceid="d8ae928d3c1acf068e7adfaef453970b" id="tgt36" class="tgtSentence"> Some queries simply do not require direct row updating by using a cursor.</caps:sentence>
          <caps:sentence sentenceid="baf74b146b24e45ba2b3927af46b4a77" id="tgt37" class="tgtSentence"> Cursors should be one of the last techniques you choose to retrieve data—and then you should choose the lowest impact cursor possible.</caps:sentence>
          <caps:sentence sentenceid="82cf0940b34e194ef6d341d58b3e376c" id="tgt38" class="tgtSentence"> When you create a result set by using a stored procedure, the result set is not updateable using cursor edit or update methods.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="1724529909565537523a32e123e88e3a" id="tgt39" class="tgtSentence">Concurrency</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="231a813f7b6b69ebb10f0d3b06ddc79e" id="tgt40" class="tgtSentence">In some multiuser applications it is very important for the data presented to the end user to be as current as possible.</caps:sentence>
            <caps:sentence sentenceid="406ca2c2472f43af2487b1f756748902" id="tgt41" class="tgtSentence"> A classic example of such a system is an airline reservation system, where many users might be contending for the same seat on a given flight (and therefore, a single record).</caps:sentence>
            <caps:sentence sentenceid="0231c97c845974bc9f323aebbb7e27e1" id="tgt42" class="tgtSentence"> In a case like this, the application design must handle concurrent operations on a single record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0018e742d606987b3d61754429857b21" id="tgt43" class="tgtSentence">In other applications, concurrency is not as important.</caps:sentence>
            <caps:sentence sentenceid="05ca65282b053a58eefa1c7315798b95" id="tgt44" class="tgtSentence"> In such cases, the expense involved in keeping the data current at all times cannot be justified.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4757fe07fd492a8be0ea6a760d683d6e" id="tgt45" class="tgtSentence">Position</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4b33d539c1f2a954e7330ffd3e3db7cf" id="tgt46" class="tgtSentence">A cursor also keeps track of the current position in a result set.</caps:sentence>
            <caps:sentence sentenceid="8a8a0b25d779d51c4db23631c6b2cd41" id="tgt47" class="tgtSentence"> Think of the cursor position as a pointer to the current record, similar to the way an array index points to the value at that particular location in the array.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="6899dad99ec6842393439553ace9d372" id="tgt48" class="tgtSentence">Scrollability</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e2c98ab7719c6d99a5eb2f1b795085c8" id="tgt49" class="tgtSentence">The type of cursor employed by your application also affects the ability to move forward and backward through the rows in a result set; this is sometimes referred to as scrollability.</caps:sentence>
            <caps:sentence sentenceid="c0c3061222625e2b329594d0ed2e06f0" id="tgt50" class="tgtSentence"> The ability to move forward <legacyItalic>and</legacyItalic> backward through a result set adds to the complexity of the cursor, and is therefore more expensive to implement.</caps:sentence>
            <caps:sentence sentenceid="8d44fa2febacd1409010a1df9a970db5" id="tgt51" class="tgtSentence"> For this reason, you should ask for a cursor with this functionality only when necessary.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Operations in a relational database act on a complete set of rows.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The set of rows returned by a SELECT statement consists of all the rows that satisfy the conditions in the WHERE clause of the statement.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This complete set of rows returned by the statement is known as the result set.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Applications, especially those that are interactive and online, cannot always work effectively with the entire result set as a unit.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> These applications need a mechanism to work with one row or a small block of rows at a time.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Cursors are an extension to result sets that provide that mechanism.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">A cursor is implemented by a cursor library.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> A cursor library is software, often implemented as a part of a database system or a data access API, that is used to manage attributes of data returned from a data source (a result set).</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> These attributes include concurrency management, position in the result set, number of rows returned, and whether you can move forward or backward (or both) through the result set (scrollability).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">A cursor keeps track of the position in the result set, and allows you to perform multiple operations row by row against a result set, with or without returning to the original table.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> In other words, cursors conceptually return a result set based on tables within the databases.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> The cursor is so named because it indicates the current position in the result set, just as the cursor on a computer screen indicates current position.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">It is important to become familiar with the concept of cursors before moving on to learn the specifics of their usage in ADO.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">Using cursors, you can:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">Specify positioning at specific rows in the result set.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">Retrieve one row or a block of rows based on the current result set position.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">Modify data in the rows at the current position in the result set.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">Define different levels of sensitivity to data changes made by other users.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src19" class="srcSentence">For example, consider an application that displays a list of available products to a potential buyer.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> The buyer scrolls through the list to see product details and cost, and finally selects a product for purchase.</caps:sentence>
          <caps:sentence id="src21" class="srcSentence"> Additional scrolling and selection occurs for the remainder of the list.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> As far as the buyer is concerned, the products appear one at a time, but the application uses a scrollable cursor to browse up and down through the result set.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src23" class="srcSentence">You can use cursors in a variety of ways:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src24" class="srcSentence">With no rows at all.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src25" class="srcSentence">With some or all of the rows in a single table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src26" class="srcSentence">With some or all of the rows from logically joined tables.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src27" class="srcSentence">As read-only or updateable at the cursor or field level.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src28" class="srcSentence">As forward-only or fully scrollable.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src29" class="srcSentence">With the cursor keyset located on the server.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src30" class="srcSentence">Sensitive to underlying table changes caused by other applications (such as membership, sort, inserts, updates, and deletes).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src31" class="srcSentence">Existing on either the server or the client.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src32" class="srcSentence">Read-only cursors help users browse through the result set, and read/write cursors can implement individual row updates.</caps:sentence>
          <caps:sentence id="src33" class="srcSentence"> Complex cursors can be defined with keysets that point back to base table rows.</caps:sentence>
          <caps:sentence id="src34" class="srcSentence"> Although some cursors are read-only in a forward direction, others can move back and forth and provide a dynamic refresh of the result set based on changes that other applications are making to the database.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src35" class="srcSentence">Not all applications need to use cursors to access or update data.</caps:sentence>
          <caps:sentence id="src36" class="srcSentence"> Some queries simply do not require direct row updating by using a cursor.</caps:sentence>
          <caps:sentence id="src37" class="srcSentence"> Cursors should be one of the last techniques you choose to retrieve data—and then you should choose the lowest impact cursor possible.</caps:sentence>
          <caps:sentence id="src38" class="srcSentence"> When you create a result set by using a stored procedure, the result set is not updateable using cursor edit or update methods.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src39" class="srcSentence">Concurrency</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src40" class="srcSentence">In some multiuser applications it is very important for the data presented to the end user to be as current as possible.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> A classic example of such a system is an airline reservation system, where many users might be contending for the same seat on a given flight (and therefore, a single record).</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> In a case like this, the application design must handle concurrent operations on a single record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src43" class="srcSentence">In other applications, concurrency is not as important.</caps:sentence>
            <caps:sentence id="src44" class="srcSentence"> In such cases, the expense involved in keeping the data current at all times cannot be justified.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src45" class="srcSentence">Position</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src46" class="srcSentence">A cursor also keeps track of the current position in a result set.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> Think of the cursor position as a pointer to the current record, similar to the way an array index points to the value at that particular location in the array.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src48" class="srcSentence">Scrollability</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src49" class="srcSentence">The type of cursor employed by your application also affects the ability to move forward and backward through the rows in a result set; this is sometimes referred to as scrollability.</caps:sentence>
            <caps:sentence id="src50" class="srcSentence"> The ability to move forward <legacyItalic>and</legacyItalic> backward through a result set adds to the complexity of the cursor, and is therefore more expensive to implement.</caps:sentence>
            <caps:sentence id="src51" class="srcSentence"> For this reason, you should ask for a cursor with this functionality only when necessary.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
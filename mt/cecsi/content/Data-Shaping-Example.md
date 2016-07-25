---
title: "Data Shaping Example"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1bfdcad4-52e1-45bc-ad21-783657ef0a44
caps.latest.revision: 12
caps.handback.revision: 12
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
# Data Shaping Example
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="77206b75ae491ec60f2a16a6270c28e2" id="tgt1" class="tgtSentence">The following data shaping command demonstrates how to build a hierarchical <legacyBold>Recordset</legacyBold> from the <legacyBold>Customers</legacyBold> and <legacyBold>Orders</legacyBold> tables in the Northwind database.</caps:sentence>
        </para>
        <code>SHAPE {SELECT CustomerID, ContactName FROM Customers} 
APPEND ({SELECT OrderID, OrderDate, CustomerID FROM Orders} AS chapOrders 
RELATE customerID TO customerID) </code>
        <para>
          <caps:sentence sentenceid="40b75ba0eabdcd0fbe31c08c66f6681d" id="tgt2" class="tgtSentence">When this command is used to open a <legacyBold>Recordset</legacyBold> object (as shown in <legacyLink xlink:href="d95dd499-19e2-4ce7-b16e-f56a04a9519c">Visual Basic Example of Data Shaping</legacyLink>), it creates a chapter (<legacyBold>chapOrders</legacyBold>) for each record returned from the <legacyBold>Customers</legacyBold> table.</caps:sentence>
          <caps:sentence sentenceid="d21614da8bb54ef095b2b70a9114680d" id="tgt3" class="tgtSentence"> This chapter consists of a subset of the <legacyBold>Recordset</legacyBold> returned from the <legacyBold>Orders</legacyBold> table.</caps:sentence>
          <caps:sentence sentenceid="d144b9432860c482ec89f4036774e3a0" id="tgt4" class="tgtSentence"> The <legacyBold>chapOrders</legacyBold> chapter contains all the requested information about the orders placed by the given customer.</caps:sentence>
          <caps:sentence sentenceid="ba2255f9f2a8f5630cbcadf58ef66d2e" id="tgt5" class="tgtSentence"> In this example, the chapter consists of three columns: <legacyBold>OrderID</legacyBold>, <legacyBold>OrderDate</legacyBold>, and <legacyBold>CustomerID</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="08a3693024da30c9351a71ab886cc6fe" id="tgt6" class="tgtSentence">The first two entries of the resultant shaped <legacyBold>Recordset</legacyBold> are as follows:</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7912f14085c37cde4936705217c61725" id="tgt7" class="tgtSentence">CustomerID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7154a6311c0213102becf9a13147c8b8" id="tgt8" class="tgtSentence">ContactName</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="08d25c66d8b38adb872a5ffec31ca906" id="tgt9" class="tgtSentence">OrderID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="651d2e9b164fa24a1745f6395a4896ca" id="tgt10" class="tgtSentence">OrderDate</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7912f14085c37cde4936705217c61725" id="tgt11" class="tgtSentence">CustomerID</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a9af2e8748ce30509057cd62b4399976" id="tgt12" class="tgtSentence">ALFKI</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e56de42b2919938442620917795f440c" id="tgt13" class="tgtSentence">Maria Ander</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fc84ad56f9f547eb89c72b9bac209312" id="tgt14" class="tgtSentence">10643</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="8640ff6ca914c9855203ac93e4c05119" id="tgt15" class="tgtSentence">10692</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="e2c2ff9c7fb57db574e461fbe467d84e" id="tgt16" class="tgtSentence">10702</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="8c12cbc89eb07068855968f976662a18" id="tgt17" class="tgtSentence">10835</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="ed7336aa18ce41622a5b41a6a62f4fea" id="tgt18" class="tgtSentence">10952</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="35569d4c2d840bb30f2ee92838b6f177" id="tgt19" class="tgtSentence">11011</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f488c25575233ba5e003212bba50af9a" id="tgt20" class="tgtSentence">1997-08-25</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="61ab9d129be24e782960b5b56ba1582b" id="tgt21" class="tgtSentence">1997-10-03</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="40125bfd6cd29eba73b507ae54da362e" id="tgt22" class="tgtSentence">1997-10-13</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="bbcd7fe634b75e5c1f07c2bb9dafda5f" id="tgt23" class="tgtSentence">1998-01-15</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="7b0ff302d91db63594fb7960911cf55e" id="tgt24" class="tgtSentence">1998-03-16</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="fa677f506258fc6cc9e6afd215c4429c" id="tgt25" class="tgtSentence">1998-04-09</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a9af2e8748ce30509057cd62b4399976" id="tgt26" class="tgtSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="a9af2e8748ce30509057cd62b4399976" id="tgt27" class="tgtSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="a9af2e8748ce30509057cd62b4399976" id="tgt28" class="tgtSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="a9af2e8748ce30509057cd62b4399976" id="tgt29" class="tgtSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="a9af2e8748ce30509057cd62b4399976" id="tgt30" class="tgtSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="a9af2e8748ce30509057cd62b4399976" id="tgt31" class="tgtSentence">ALFKI</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="74e6d7c2301b67a480f57c014f238e29" id="tgt32" class="tgtSentence">ANATR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="01baa2278d69244149937904eec5f9c9" id="tgt33" class="tgtSentence">Ana Trujillo</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9efb1a59d7b58e69996cf0e32cb71098" id="tgt34" class="tgtSentence">10308</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="40b8498f89a8b101cd6fc6bb690231f9" id="tgt35" class="tgtSentence">10625</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="4564e13a85364d6743e38059a8544f34" id="tgt36" class="tgtSentence">10759</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="d0267f7d1df3e03cb7f645c7a34849be" id="tgt37" class="tgtSentence">10926</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5dad443fc3a41d70b5b6c9b096778dc2" id="tgt38" class="tgtSentence">1996-09-18</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="5afa1b513ff4b3f999c92b65271f5e58" id="tgt39" class="tgtSentence">1997-08-08</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="313bb1a02c0bb49545198e178b4c04d5" id="tgt40" class="tgtSentence">1997-11-28</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="f7f0508d9b278f53fa5778b4f1a0bd4a" id="tgt41" class="tgtSentence">1998-03-04</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="74e6d7c2301b67a480f57c014f238e29" id="tgt42" class="tgtSentence">ANATR</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="74e6d7c2301b67a480f57c014f238e29" id="tgt43" class="tgtSentence">ANATR</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="74e6d7c2301b67a480f57c014f238e29" id="tgt44" class="tgtSentence">ANATR</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="74e6d7c2301b67a480f57c014f238e29" id="tgt45" class="tgtSentence">ANATR</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="11c0c8910c36542b8d8ebf0ef9e88b87" id="tgt46" class="tgtSentence">In a SHAPE command, APPEND is used to create a child <legacyBold>Recordset</legacyBold> related to the parent <legacyBold>Recordset</legacyBold> (as returned from the provider-specific command immediately after the SHAPE keyword that was discussed earlier) by the RELATE clause.</caps:sentence>
          <caps:sentence sentenceid="9f6ccf415c39e365acd5a62357c59751" id="tgt47" class="tgtSentence"> The parent and child typically have at least one column in common: The value of the column in a row of the parent is the same as the value of the column in all rows of the child.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="45dea429ecea04b99cd964a0a36a6fce" id="tgt48" class="tgtSentence">There is a second way to use SHAPE commands: namely, to generate a parent <legacyBold>Recordset</legacyBold> from a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="98d1efe6efef1c53896164b8bab0fceb" id="tgt49" class="tgtSentence"> The records in the child <legacyBold>Recordset</legacyBold> are grouped, typically by using the BY clause, and one row is added to the parent <legacyBold>Recordset</legacyBold> for each resulting group in the child.</caps:sentence>
          <caps:sentence sentenceid="b01b910d335b0ff49b5962c5d9dc4c0f" id="tgt50" class="tgtSentence"> If the BY clause is omitted, the child <legacyBold>Recordset</legacyBold> will form a single group and the parent <legacyBold>Recordset</legacyBold> will contain exactly one row.</caps:sentence>
          <caps:sentence sentenceid="d4c9d7c2ebc20b3df1711162eb950a3f" id="tgt51" class="tgtSentence"> This is useful for computing "grand total" aggregates over the entire child <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="10da4750d46a62cbf585385bf8543272" id="tgt52" class="tgtSentence">The SHAPE command construct also enables you to programmatically create a shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="75784b905eba8a0347ffb6b71c2c4037" id="tgt53" class="tgtSentence"> You can then access the components of the <legacyBold>Recordset</legacyBold> programmatically or through an appropriate visual control.</caps:sentence>
          <caps:sentence sentenceid="92ff679b4e20fe8477fc3750d9dacb1a" id="tgt54" class="tgtSentence"> A shape command is issued like any other ADO command text.</caps:sentence>
          <caps:sentence sentenceid="58af986f3b2c9155ce86c2170b84ffd3" id="tgt55" class="tgtSentence"> For more information, see <legacyLink xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="bc7594560fae55b1469e4afb7b7a387c" id="tgt56" class="tgtSentence">Regardless of which way the parent <legacyBold>Recordset</legacyBold> is formed, it will contain a chapter column that is used to relate it to a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="e34346d7765ccf8a5877690bddb8ed37" id="tgt57" class="tgtSentence"> If you want, the parent <legacyBold>Recordset</legacyBold> can also have columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</caps:sentence>
          <caps:sentence sentenceid="32a52d5b20b12eae8a66afc500a15c62" id="tgt58" class="tgtSentence"> Both the parent and the child <legacyBold>Recordset</legacyBold> can have columns that contain an expression on the row in the <legacyBold>Recordset</legacyBold>, as well as columns which are new and initially empty.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c9dadd48d6208680b95c780938b8f03c" id="tgt59" class="tgtSentence">This section continues with the following topic.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="d95dd499-19e2-4ce7-b16e-f56a04a9519c">
                <caps:sentence sentenceid="a23d4104ea3ef9d13b15ba44fc857ffa" id="tgt60" class="tgtSentence">Visual Basic Example of Data Shaping</caps:sentence>
              </legacyLink>
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
          <caps:sentence id="src1" class="srcSentence">The following data shaping command demonstrates how to build a hierarchical <legacyBold>Recordset</legacyBold> from the <legacyBold>Customers</legacyBold> and <legacyBold>Orders</legacyBold> tables in the Northwind database.</caps:sentence>
        </para>
        <code>SHAPE {SELECT CustomerID, ContactName FROM Customers} 
APPEND ({SELECT OrderID, OrderDate, CustomerID FROM Orders} AS chapOrders 
RELATE customerID TO customerID) </code>
        <para>
          <caps:sentence id="src2" class="srcSentence">When this command is used to open a <legacyBold>Recordset</legacyBold> object (as shown in <legacyLink xlink:href="d95dd499-19e2-4ce7-b16e-f56a04a9519c">Visual Basic Example of Data Shaping</legacyLink>), it creates a chapter (<legacyBold>chapOrders</legacyBold>) for each record returned from the <legacyBold>Customers</legacyBold> table.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This chapter consists of a subset of the <legacyBold>Recordset</legacyBold> returned from the <legacyBold>Orders</legacyBold> table.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The <legacyBold>chapOrders</legacyBold> chapter contains all the requested information about the orders placed by the given customer.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> In this example, the chapter consists of three columns: <legacyBold>OrderID</legacyBold>, <legacyBold>OrderDate</legacyBold>, and <legacyBold>CustomerID</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">The first two entries of the resultant shaped <legacyBold>Recordset</legacyBold> are as follows:</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">CustomerID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">ContactName</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">OrderID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">OrderDate</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">CustomerID</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">ALFKI</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Maria Ander</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">10643</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src15" class="srcSentence">10692</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src16" class="srcSentence">10702</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src17" class="srcSentence">10835</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src18" class="srcSentence">10952</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src19" class="srcSentence">11011</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">1997-08-25</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src21" class="srcSentence">1997-10-03</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src22" class="srcSentence">1997-10-13</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src23" class="srcSentence">1998-01-15</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src24" class="srcSentence">1998-03-16</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src25" class="srcSentence">1998-04-09</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src27" class="srcSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src28" class="srcSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src29" class="srcSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src30" class="srcSentence">ALFKI</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src31" class="srcSentence">ALFKI</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">ANATR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Ana Trujillo</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">10308</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src35" class="srcSentence">10625</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src36" class="srcSentence">10759</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src37" class="srcSentence">10926</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">1996-09-18</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src39" class="srcSentence">1997-08-08</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src40" class="srcSentence">1997-11-28</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src41" class="srcSentence">1998-03-04</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">ANATR</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src43" class="srcSentence">ANATR</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src44" class="srcSentence">ANATR</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src45" class="srcSentence">ANATR</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src46" class="srcSentence">In a SHAPE command, APPEND is used to create a child <legacyBold>Recordset</legacyBold> related to the parent <legacyBold>Recordset</legacyBold> (as returned from the provider-specific command immediately after the SHAPE keyword that was discussed earlier) by the RELATE clause.</caps:sentence>
          <caps:sentence id="src47" class="srcSentence"> The parent and child typically have at least one column in common: The value of the column in a row of the parent is the same as the value of the column in all rows of the child.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src48" class="srcSentence">There is a second way to use SHAPE commands: namely, to generate a parent <legacyBold>Recordset</legacyBold> from a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src49" class="srcSentence"> The records in the child <legacyBold>Recordset</legacyBold> are grouped, typically by using the BY clause, and one row is added to the parent <legacyBold>Recordset</legacyBold> for each resulting group in the child.</caps:sentence>
          <caps:sentence id="src50" class="srcSentence"> If the BY clause is omitted, the child <legacyBold>Recordset</legacyBold> will form a single group and the parent <legacyBold>Recordset</legacyBold> will contain exactly one row.</caps:sentence>
          <caps:sentence id="src51" class="srcSentence"> This is useful for computing "grand total" aggregates over the entire child <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src52" class="srcSentence">The SHAPE command construct also enables you to programmatically create a shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src53" class="srcSentence"> You can then access the components of the <legacyBold>Recordset</legacyBold> programmatically or through an appropriate visual control.</caps:sentence>
          <caps:sentence id="src54" class="srcSentence"> A shape command is issued like any other ADO command text.</caps:sentence>
          <caps:sentence id="src55" class="srcSentence"> For more information, see <legacyLink xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src56" class="srcSentence">Regardless of which way the parent <legacyBold>Recordset</legacyBold> is formed, it will contain a chapter column that is used to relate it to a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src57" class="srcSentence"> If you want, the parent <legacyBold>Recordset</legacyBold> can also have columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</caps:sentence>
          <caps:sentence id="src58" class="srcSentence"> Both the parent and the child <legacyBold>Recordset</legacyBold> can have columns that contain an expression on the row in the <legacyBold>Recordset</legacyBold>, as well as columns which are new and initially empty.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src59" class="srcSentence">This section continues with the following topic.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="d95dd499-19e2-4ce7-b16e-f56a04a9519c">
                <caps:sentence id="src60" class="srcSentence">Visual Basic Example of Data Shaping</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
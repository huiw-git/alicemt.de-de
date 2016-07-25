---
title: "Operation of Parameterized Commands"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4fae0d54-83b6-4ead-99cc-bcf532daa121
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
# Operation of Parameterized Commands
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c918c833887c601c0f6de570f22c5329" id="tgt1" class="tgtSentence">If you are working with a large child <legacyBold>Recordset</legacyBold>, especially compared to the size of the parent <legacyBold>Recordset</legacyBold>, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="260d708a2e20ea36c354d216bc5aea75" id="tgt2" class="tgtSentence">A <legacyItalic>non-parameterized command</legacyItalic> retrieves both the entire parent and child <legacyBold>Recordsets</legacyBold>, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="bf2071f26c296ccad0b7f8851afa7b35" id="tgt3" class="tgtSentence">A <legacyItalic>parameterized command</legacyItalic> retrieves the entire parent <legacyBold>Recordset</legacyBold>, but retrieves only the chapter <legacyBold>Recordset</legacyBold> when the chapter column is accessed.</caps:sentence>
          <caps:sentence sentenceid="d9341d7d341744d9bd8caf33094fb07a" id="tgt4" class="tgtSentence"> This difference in retrieval strategy can yield significant performance benefits.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f2f7d2fa7ffa71805779b4b9e87c6027" id="tgt5" class="tgtSentence">For example, you can specify the following:</caps:sentence>
        </para>
        <code>SHAPE {SELECT * FROM customer} 
   APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
   RELATE cust_id TO PARAMETER 0)</code>
        <para>
          <caps:sentence sentenceid="10223209a2fcaa51b5dc7ec9681d130b" id="tgt6" class="tgtSentence">The parent and child tables have a column name in common, cust_id<legacyItalic>. </legacyItalic>The <legacyItalic>child-command</legacyItalic> has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="0e939529510509e93866644e13171d89" id="tgt7" class="tgtSentence">The PARAMETER clause pertains solely to the shape command syntax.</caps:sentence>
            <caps:sentence sentenceid="7151cee2b76431056c36c8b828f84fcc" id="tgt8" class="tgtSentence"> It is not associated with either the ADO <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object or the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="7cc196591b0ab3df8574473a86870b66" id="tgt9" class="tgtSentence">When the parameterized shape command is executed, the following occurs:  </caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence sentenceid="156dba94f2fd73c8447350c628833115" id="tgt10" class="tgtSentence">The <legacyItalic>parent-command</legacyItalic> is executed and returns a parent <legacyBold>Recordset</legacyBold> from the Customers table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e088e822f94c6ad51425940aebe97838" id="tgt11" class="tgtSentence">A chapter column is appended to the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="88d9c35aea85be5e7555b3ea40ae64fe" id="tgt12" class="tgtSentence">When the chapter column of a parent row is accessed, the <legacyItalic>child-command</legacyItalic> is executed using the value of the customer.cust_id as the value of the parameter.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="07d6a69e46d9a69157bb89f1277af64e" id="tgt13" class="tgtSentence">All rows in the data provider rowset created in step 3 are used to populate the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="4800e8bd18cd6b687f7cb0d45634c50d" id="tgt14" class="tgtSentence"> In this example, that is all the rows in the Orders table in which the cust_id equals the value of customer.cust_id.</caps:sentence>
              <caps:sentence sentenceid="1c35016637b2d687c53b2035cb99529e" id="tgt15" class="tgtSentence"> By default, the child <legacyBold>Recordset</legacyBold>s will be cached on the client until all references to the parent <legacyBold>Recordset</legacyBold> are released.</caps:sentence>
              <caps:sentence sentenceid="62a01e45b09818f023e6f45da8a75a72" id="tgt16" class="tgtSentence"> To change this behavior, set the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">dynamic property</legacyLink> <legacyBold>Cache Child Rows</legacyBold> to <legacyBold>False</legacyBold>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9e89f6897680deb1e67d9ca23a8ab4f8" id="tgt17" class="tgtSentence">A reference to the retrieved child rows (that is, the chapter of the child <legacyBold>Recordset</legacyBold>) is placed in the chapter column of the current row of the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="421c5d834c154ba717469cfebd2f1511" id="tgt18" class="tgtSentence">Steps 3–5 are repeated when the chapter column of another row is accessed.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="bd1e1e4beb52911a1473b33f484861c7" id="tgt19" class="tgtSentence">The <legacyBold>Cache Child Rows</legacyBold> dynamic property is set to <legacyBold>True</legacyBold> by default.</caps:sentence>
          <caps:sentence sentenceid="00a2aa33ad740a5d397b2db06b9f5ea3" id="tgt20" class="tgtSentence"> The caching behavior varies depending upon the parameter values of the query.</caps:sentence>
          <caps:sentence sentenceid="b3b4eb34887fad82224b0a516169a105" id="tgt21" class="tgtSentence"> In a query with a single parameter, the child <legacyBold>Recordset</legacyBold> for a given parameter value will be cached between requests for a child with that value.</caps:sentence>
          <caps:sentence sentenceid="d18db814442192326b2c4f64cdae76b2" id="tgt22" class="tgtSentence"> The following code demonstrates this:</caps:sentence>
        </para>
        <code>SCmd = "SHAPE {select * from customer} " &amp; _
         "APPEND({select * from orders where cust_id = ?} " &amp; _
         "RELATE cust_id TO PARAMETER 0) AS chpCustOrder"
Rst1.Open sCmd, Cnn1
Set RstChild = Rst1("chpCustOrder").Value
Rst1.MoveNext      ' Next cust_id passed to Param 0, &amp; new rs fetched 
                   ' into RstChild.
Rst1.MovePrevious  ' RstChild now holds cached rs, saving round trip.</code>
        <para>
          <caps:sentence sentenceid="8a53fe189cae29518df86ca0c36b669a" id="tgt23" class="tgtSentence">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="efc2fd53fdcd7f23982bf3435a835de8" id="tgt24" class="tgtSentence">Parameterized Commands and Complex Parent Child Relations</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7eebf005ff3781d69c50a922e20970db" id="tgt25" class="tgtSentence">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</caps:sentence>
            <caps:sentence sentenceid="f1c69bee72ad426c367f82491852569d" id="tgt26" class="tgtSentence"> For example, consider a Little League database with two tables: one consisting of the teams (team_id, team_name) and the other of games (date, home_team, visiting_team).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cc856ac947f62b8f2b158d6399f62e8d" id="tgt27" class="tgtSentence">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child <legacyBold>Recordset</legacyBold> for each team contains its complete schedule.</caps:sentence>
            <caps:sentence sentenceid="a44a907e39e804f908a929704b3c4bf0" id="tgt28" class="tgtSentence"> You can create chapters that contain the home schedule or the road schedule, but not both.</caps:sentence>
            <caps:sentence sentenceid="907740fa411eba3c83254a77ca3d614f" id="tgt29" class="tgtSentence"> This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</caps:sentence>
            <caps:sentence sentenceid="221a097bca45f3614d2b92344f275a16" id="tgt30" class="tgtSentence"> So, if your command included "RELATE team_id TO home_team, team_id TO visiting_team", you would get only games where a team was playing itself.</caps:sentence>
            <caps:sentence sentenceid="94773a1d84093a30bf2c988d20b8c134" id="tgt31" class="tgtSentence"> What you want is "(team_id=home_team) OR (team_id=visiting_team)", but the Shape provider does not support the OR clause.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e28aefc0724b97e04db750585591cf7b" id="tgt32" class="tgtSentence">To obtain the desired result, you can use a parameterized command.</caps:sentence>
            <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt33" class="tgtSentence"> For example:</caps:sentence>
          </para>
          <code>SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
        RELATE team_id TO PARAMETER 0, 
               team_id TO PARAMETER 1) </code>
          <para>
            <caps:sentence sentenceid="30c6d2d3d4def470843dd25b47da1988" id="tgt34" class="tgtSentence">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="5d857b676781c70c92c31d2fe88eda3e" id="tgt35" class="tgtSentence">When using WHERE clauses, parameters can not use the SQL data types for text, ntext and image or an error will result that contains the following description: <codeInline>Invalid operator for data type</codeInline>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
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
          <caps:sentence id="src1" class="srcSentence">If you are working with a large child <legacyBold>Recordset</legacyBold>, especially compared to the size of the parent <legacyBold>Recordset</legacyBold>, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">A <legacyItalic>non-parameterized command</legacyItalic> retrieves both the entire parent and child <legacyBold>Recordsets</legacyBold>, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">A <legacyItalic>parameterized command</legacyItalic> retrieves the entire parent <legacyBold>Recordset</legacyBold>, but retrieves only the chapter <legacyBold>Recordset</legacyBold> when the chapter column is accessed.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> This difference in retrieval strategy can yield significant performance benefits.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">For example, you can specify the following:</caps:sentence>
        </para>
        <code>SHAPE {SELECT * FROM customer} 
   APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
   RELATE cust_id TO PARAMETER 0)</code>
        <para>
          <caps:sentence id="src6" class="srcSentence">The parent and child tables have a column name in common, cust_id<legacyItalic>. </legacyItalic>The <legacyItalic>child-command</legacyItalic> has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src7" class="srcSentence">The PARAMETER clause pertains solely to the shape command syntax.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> It is not associated with either the ADO <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object or the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src9" class="srcSentence">When the parameterized shape command is executed, the following occurs:  </caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">The <legacyItalic>parent-command</legacyItalic> is executed and returns a parent <legacyBold>Recordset</legacyBold> from the Customers table.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">A chapter column is appended to the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">When the chapter column of a parent row is accessed, the <legacyItalic>child-command</legacyItalic> is executed using the value of the customer.cust_id as the value of the parameter.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">All rows in the data provider rowset created in step 3 are used to populate the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> In this example, that is all the rows in the Orders table in which the cust_id equals the value of customer.cust_id.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> By default, the child <legacyBold>Recordset</legacyBold>s will be cached on the client until all references to the parent <legacyBold>Recordset</legacyBold> are released.</caps:sentence>
              <caps:sentence id="src16" class="srcSentence"> To change this behavior, set the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">dynamic property</legacyLink> <legacyBold>Cache Child Rows</legacyBold> to <legacyBold>False</legacyBold>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">A reference to the retrieved child rows (that is, the chapter of the child <legacyBold>Recordset</legacyBold>) is placed in the chapter column of the current row of the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">Steps 3–5 are repeated when the chapter column of another row is accessed.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src19" class="srcSentence">The <legacyBold>Cache Child Rows</legacyBold> dynamic property is set to <legacyBold>True</legacyBold> by default.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> The caching behavior varies depending upon the parameter values of the query.</caps:sentence>
          <caps:sentence id="src21" class="srcSentence"> In a query with a single parameter, the child <legacyBold>Recordset</legacyBold> for a given parameter value will be cached between requests for a child with that value.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> The following code demonstrates this:</caps:sentence>
        </para>
        <code>SCmd = "SHAPE {select * from customer} " &amp; _
         "APPEND({select * from orders where cust_id = ?} " &amp; _
         "RELATE cust_id TO PARAMETER 0) AS chpCustOrder"
Rst1.Open sCmd, Cnn1
Set RstChild = Rst1("chpCustOrder").Value
Rst1.MoveNext      ' Next cust_id passed to Param 0, &amp; new rs fetched 
                   ' into RstChild.
Rst1.MovePrevious  ' RstChild now holds cached rs, saving round trip.</code>
        <para>
          <caps:sentence id="src23" class="srcSentence">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Parameterized Commands and Complex Parent Child Relations</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> For example, consider a Little League database with two tables: one consisting of the teams (team_id, team_name) and the other of games (date, home_team, visiting_team).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child <legacyBold>Recordset</legacyBold> for each team contains its complete schedule.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> You can create chapters that contain the home schedule or the road schedule, but not both.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> So, if your command included "RELATE team_id TO home_team, team_id TO visiting_team", you would get only games where a team was playing itself.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> What you want is "(team_id=home_team) OR (team_id=visiting_team)", but the Shape provider does not support the OR clause.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">To obtain the desired result, you can use a parameterized command.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> For example:</caps:sentence>
          </para>
          <code>SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
        RELATE team_id TO PARAMETER 0, 
               team_id TO PARAMETER 1) </code>
          <para>
            <caps:sentence id="src34" class="srcSentence">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src35" class="srcSentence">When using WHERE clauses, parameters can not use the SQL data types for text, ntext and image or an error will result that contains the following description: <codeInline>Invalid operator for data type</codeInline>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
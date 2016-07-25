---
title: "Shape Commands in General"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1fac7831-a187-4b15-9b43-aad380c5556c
caps.latest.revision: 15
caps.handback.revision: 15
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
# Shape Commands in General
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b524a7ee0ee34a0ead183bbc9c2a4f4f" id="tgt1" class="tgtSentence">Data shaping defines the columns of a shaped <legacyBold>Recordset</legacyBold>, the relationships between the entities represented by the columns, and the manner in which the <legacyBold>Recordset</legacyBold> is populated with data.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7104fb8d1d5e8d2ce5acd32b6078340b" id="tgt2" class="tgtSentence">A shaped <legacyBold>Recordset</legacyBold> can consist of the following types of columns.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d37312b6f9f3a2bb636fce084861ff34" id="tgt3" class="tgtSentence">Column type</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt4" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8d777f385d3dfec8815d20f7496026dc" id="tgt5" class="tgtSentence">data</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c966a31dabcbb9cf57f3ca3ed1e04c04" id="tgt6" class="tgtSentence">Fields from a <legacyBold>Recordset</legacyBold> returned by a query command to a data provider, table, or previously shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7a3e56dbf4b75792017d682faf64ac07" id="tgt7" class="tgtSentence">chapter</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b7a609a5eaadc576bdb4246550e32e8f" id="tgt8" class="tgtSentence">A reference to another <legacyBold>Recordset</legacyBold>, called a <legacyItalic>chapter</legacyItalic>.</caps:sentence>
                  <caps:sentence sentenceid="4098cdb0c63f2c79c9d16036f04961c0" id="tgt9" class="tgtSentence"> Chapter columns make it possible to define a <legacyItalic>parent-child</legacyItalic> relationship where the <legacyItalic>parent</legacyItalic> is the <legacyBold>Recordset</legacyBold> that contains the chapter column and the <legacyItalic>child</legacyItalic> is the <legacyBold>Recordset</legacyBold> represented by the chapter.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="39adbeb6bc21a3133e5fdcf1ec05d1a0" id="tgt10" class="tgtSentence">aggregate</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="74295d1edca623f4528aaaf920960ffe" id="tgt11" class="tgtSentence">The value of the column is derived by executing an <legacyItalic>aggregate function</legacyItalic> on all the rows or a column of all the rows of a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="856cc9228b955f7476bf571469333037" id="tgt12" class="tgtSentence"> (See Aggregate Functions in the following topic, <legacyLink xlink:href="0590b466-2a36-49a2-868e-028ef5e49394">Aggregate Functions, the CALC Function, and the NEW Keyword</legacyLink>.)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="06b3ba65c954b020b9fc31fbb25d162b" id="tgt13" class="tgtSentence">calculated expression</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3024a8859e25a68c95012682912daa94" id="tgt14" class="tgtSentence">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="df3a2c21f538814fee23190f8154a0b4" id="tgt15" class="tgtSentence"> The expression is the argument to the CALC function.</caps:sentence>
                  <caps:sentence sentenceid="c90cf743663b4b1b3d026b942c0c5497" id="tgt16" class="tgtSentence"> (See Calculated Expression in the following topic, <legacyLink xlink:href="0590b466-2a36-49a2-868e-028ef5e49394">Aggregate Functions, the CALC Function, and the NEW Keyword</legacyLink> and in <legacyLink xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications Functions</legacyLink>.)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="22af645d1859cb5ca6da0c484f1f37ea" id="tgt17" class="tgtSentence">new</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="defdc25655cbc76541a4ac62d0b4010e" id="tgt18" class="tgtSentence">Empty, fabricated fields, which can be populated with data at a later time.</caps:sentence>
                  <caps:sentence sentenceid="ab32132111cea59ca0f6a6af996268ff" id="tgt19" class="tgtSentence"> The column is defined with the NEW keyword.</caps:sentence>
                  <caps:sentence sentenceid="2c4e6a53106a7791cacbc95419db5146" id="tgt20" class="tgtSentence"> (See NEW keyword in the following topic, <legacyLink xlink:href="0590b466-2a36-49a2-868e-028ef5e49394">Aggregate Functions, the CALC Function, and the NEW Keyword</legacyLink>.)</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="d0d8d1a561b1e5fd5a6a621967ad3c5e" id="tgt21" class="tgtSentence">A shape command can contain a clause that specifies a query command to an underlying data provider that will return a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="d028419d45b1b6d9fd09494958d70a32" id="tgt22" class="tgtSentence"> The query's syntax depends on the requirements of the underlying data provider.</caps:sentence>
          <caps:sentence sentenceid="cf4d7142b98d238e843fef26eb04ad85" id="tgt23" class="tgtSentence"> This will usually be SQL, although ADO does not require the use of any particular query language.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="77669dba7a3fd087ba4cc1ac255cd199" id="tgt24" class="tgtSentence">Shape commands can be issued by <legacyBold>Recordset</legacyBold> objects or by setting the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property of the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object and then calling the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7994c9f1d3bc97c95a5dcb17ed5674c1" id="tgt25" class="tgtSentence">You could use a SQL JOIN clause to relate two tables; however, a hierarchical <legacyBold>Recordset</legacyBold> can represent the information more efficiently.</caps:sentence>
          <caps:sentence sentenceid="b57ca5abeb42685e8123009977f882a7" id="tgt26" class="tgtSentence"> Each row of a <legacyBold>Recordset</legacyBold> created by a JOIN repeats information redundantly from one of the tables.</caps:sentence>
          <caps:sentence sentenceid="949f0dae2b9799da5e68de954295855d" id="tgt27" class="tgtSentence"> A hierarchical <legacyBold>Recordset</legacyBold> has only one parent <legacyBold>Recordset</legacyBold> for each of multiple child <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="294934a00e8bf689d6c417e5665db73d" id="tgt28" class="tgtSentence">Shape commands can be nested.</caps:sentence>
          <caps:sentence sentenceid="c616aeeabc3178831a62d0abba030bf2" id="tgt29" class="tgtSentence"> That is, the <legacyItalic>parent-command</legacyItalic> or<legacyItalic> child-command </legacyItalic>may itself be another shape command.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1fdd51d1ee4731ef577f2697ae08906c" id="tgt30" class="tgtSentence">The shape provider always returns a client cursor, even when the user specifies a cursor location of <legacyBold>adUseServer</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e678de8ab0704bc3eb548fc13f1a56e6" id="tgt31" class="tgtSentence">You can access the <legacyBold>Recordset</legacyBold> components of the shaped <legacyBold>Recordset</legacyBold> programmatically or through an appropriate visual control.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7b7e6ec27f5a23b46a260045d1d88569" id="tgt32" class="tgtSentence">Microsoft provides a visual tool that generates shape commands (see the <externalLink><linkText>Data Environment Designer</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=5689</linkUri></externalLink> in the Visual Basic 6 documentation) and another that displays hierarchical cursors (see "Using the Microsoft Hierarchical Flexgrid Control" in the Visual Basic 6 documentation).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3ebefc452fcb566d56f258d2209c224b" id="tgt33" class="tgtSentence">For information about navigating a hierarchical <legacyBold>Recordset</legacyBold>, see <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f17237b4a55007c46e32a699a2c0d79c" id="tgt34" class="tgtSentence">For precise information about syntactically correct shape commands, see <legacyLink xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt35" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="0590b466-2a36-49a2-868e-028ef5e49394">
                <caps:sentence sentenceid="6cf6a24194f35c7a921d895235cc788e" id="tgt36" class="tgtSentence">Aggregate Functions, the CALC Function, and the NEW Keyword</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="d6001863-7733-4c32-817f-081e48587fa1">
                <caps:sentence sentenceid="51ae17c349dc9d368eeb7e3d9409e529" id="tgt37" class="tgtSentence">Issuing Commands to the Underlying Data Provider</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Data shaping defines the columns of a shaped <legacyBold>Recordset</legacyBold>, the relationships between the entities represented by the columns, and the manner in which the <legacyBold>Recordset</legacyBold> is populated with data.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">A shaped <legacyBold>Recordset</legacyBold> can consist of the following types of columns.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Column type</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">data</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Fields from a <legacyBold>Recordset</legacyBold> returned by a query command to a data provider, table, or previously shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">chapter</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">A reference to another <legacyBold>Recordset</legacyBold>, called a <legacyItalic>chapter</legacyItalic>.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> Chapter columns make it possible to define a <legacyItalic>parent-child</legacyItalic> relationship where the <legacyItalic>parent</legacyItalic> is the <legacyBold>Recordset</legacyBold> that contains the chapter column and the <legacyItalic>child</legacyItalic> is the <legacyBold>Recordset</legacyBold> represented by the chapter.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">aggregate</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">The value of the column is derived by executing an <legacyItalic>aggregate function</legacyItalic> on all the rows or a column of all the rows of a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence id="src12" class="srcSentence"> (See Aggregate Functions in the following topic, <legacyLink xlink:href="0590b466-2a36-49a2-868e-028ef5e49394">Aggregate Functions, the CALC Function, and the NEW Keyword</legacyLink>.)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">calculated expression</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> The expression is the argument to the CALC function.</caps:sentence>
                  <caps:sentence id="src16" class="srcSentence"> (See Calculated Expression in the following topic, <legacyLink xlink:href="0590b466-2a36-49a2-868e-028ef5e49394">Aggregate Functions, the CALC Function, and the NEW Keyword</legacyLink> and in <legacyLink xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications Functions</legacyLink>.)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">new</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Empty, fabricated fields, which can be populated with data at a later time.</caps:sentence>
                  <caps:sentence id="src19" class="srcSentence"> The column is defined with the NEW keyword.</caps:sentence>
                  <caps:sentence id="src20" class="srcSentence"> (See NEW keyword in the following topic, <legacyLink xlink:href="0590b466-2a36-49a2-868e-028ef5e49394">Aggregate Functions, the CALC Function, and the NEW Keyword</legacyLink>.)</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src21" class="srcSentence">A shape command can contain a clause that specifies a query command to an underlying data provider that will return a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> The query's syntax depends on the requirements of the underlying data provider.</caps:sentence>
          <caps:sentence id="src23" class="srcSentence"> This will usually be SQL, although ADO does not require the use of any particular query language.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src24" class="srcSentence">Shape commands can be issued by <legacyBold>Recordset</legacyBold> objects or by setting the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property of the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object and then calling the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src25" class="srcSentence">You could use a SQL JOIN clause to relate two tables; however, a hierarchical <legacyBold>Recordset</legacyBold> can represent the information more efficiently.</caps:sentence>
          <caps:sentence id="src26" class="srcSentence"> Each row of a <legacyBold>Recordset</legacyBold> created by a JOIN repeats information redundantly from one of the tables.</caps:sentence>
          <caps:sentence id="src27" class="srcSentence"> A hierarchical <legacyBold>Recordset</legacyBold> has only one parent <legacyBold>Recordset</legacyBold> for each of multiple child <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src28" class="srcSentence">Shape commands can be nested.</caps:sentence>
          <caps:sentence id="src29" class="srcSentence"> That is, the <legacyItalic>parent-command</legacyItalic> or<legacyItalic> child-command </legacyItalic>may itself be another shape command.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src30" class="srcSentence">The shape provider always returns a client cursor, even when the user specifies a cursor location of <legacyBold>adUseServer</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src31" class="srcSentence">You can access the <legacyBold>Recordset</legacyBold> components of the shaped <legacyBold>Recordset</legacyBold> programmatically or through an appropriate visual control.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src32" class="srcSentence">Microsoft provides a visual tool that generates shape commands (see the <externalLink><linkText>Data Environment Designer</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=5689</linkUri></externalLink> in the Visual Basic 6 documentation) and another that displays hierarchical cursors (see "Using the Microsoft Hierarchical Flexgrid Control" in the Visual Basic 6 documentation).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src33" class="srcSentence">For information about navigating a hierarchical <legacyBold>Recordset</legacyBold>, see <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src34" class="srcSentence">For precise information about syntactically correct shape commands, see <legacyLink xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src35" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="0590b466-2a36-49a2-868e-028ef5e49394">
                <caps:sentence id="src36" class="srcSentence">Aggregate Functions, the CALC Function, and the NEW Keyword</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="d6001863-7733-4c32-817f-081e48587fa1">
                <caps:sentence id="src37" class="srcSentence">Issuing Commands to the Underlying Data Provider</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
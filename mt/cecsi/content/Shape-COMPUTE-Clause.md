---
title: "Shape COMPUTE Clause"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3fdfead2-b5ab-4163-9b1d-3d2143a5db8c
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
# Shape COMPUTE Clause
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="446efc22c65b45fec9e74e5d0896276c" id="tgt1" class="tgtSentence">A shape COMPUTE clause generates a parent <legacyBold>Recordset</legacyBold>, whose columns consist of a reference to the child <legacyBold>Recordset</legacyBold>; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child <legacyBold>Recordset</legacyBold> or a previously shaped <legacyBold>Recordset</legacyBold>; and any columns from the child <legacyBold>Recordset</legacyBold> listed in the optional BY clause.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt2" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>SHAPE <legacyItalic xmlns="">child-command</legacyItalic> [AS] <legacyItalic xmlns="">child-alias</legacyItalic>
   COMPUTE <legacyItalic xmlns="">child-alias</legacyItalic> [[AS] <legacyItalic xmlns="">name</legacyItalic>], [<legacyItalic xmlns="">appended-column-list</legacyItalic>]
   [BY <legacyItalic xmlns="">grp-field-list</legacyItalic>]</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt3" class="tgtSentence">Description</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="87e7a3e02e35ba2f38799721c7c49110" id="tgt4" class="tgtSentence">The parts of this clause are as follows:  </caps:sentence>
          </para>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="83a63a9b083cb004cc4fee39bce5680f" id="tgt5" class="tgtSentence"> <legacyItalic>child-command</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="568170884244520375914e651666df8d" id="tgt6" class="tgtSentence">Consists of one of the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e4b8289505728486a3a6b0c178599488" id="tgt7" class="tgtSentence">A query command within curly braces ("{}") that returns a child <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                    <caps:sentence sentenceid="7836e2a3e5649a925c57c005f820624c" id="tgt8" class="tgtSentence"> The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</caps:sentence>
                    <caps:sentence sentenceid="6b23d3186a0b9b1b2e98b9fb48a39d21" id="tgt9" class="tgtSentence"> This will typically be the SQL language, although ADO does not require any particular query language.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bcfafbe16ca7210077fa433c50900a68" id="tgt10" class="tgtSentence">The name of an existing shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="54b07ba495b9e4a4cb5ffd1fbb98f9ee" id="tgt11" class="tgtSentence">Another shape command.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="df545ab3bf7577d15fffac44f7484154" id="tgt12" class="tgtSentence">The TABLE keyword, followed by the name of a table in the data provider.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="fd7a393c43fdae313065fe8bf08ddbd2" id="tgt13" class="tgtSentence"> <legacyItalic>child-alias</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="27a50a9f6d6578556511c27329989938" id="tgt14" class="tgtSentence">An alias used to refer to the <legacyBold>Recordset</legacyBold> returned by the <legacyItalic>child-command.</legacyItalic> The <legacyItalic>child-alias</legacyItalic> is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c11f7959bd1ca4c3fedd7e36a138041b" id="tgt15" class="tgtSentence"> <legacyItalic>appended-column-list</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5acf4ad95ea0fdb528baf70b79674fb4" id="tgt16" class="tgtSentence">A list in which each element defines a column in the generated parent.</caps:sentence>
                <caps:sentence sentenceid="ca65e6351d075b4a6afec313189d1d6a" id="tgt17" class="tgtSentence"> Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d9a64b9b78900feea98c1bd841ccfddf" id="tgt18" class="tgtSentence"> <legacyItalic>grp-field-list</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ec9f58b07fc1b9bd7d53263d2d864f87" id="tgt19" class="tgtSentence">A list of columns in the parent and child <legacyBold>Recordset</legacyBold> objects that specifies how rows should be grouped in the child.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e4c311f68a490636fe671a1d295ac2f4" id="tgt20" class="tgtSentence">For each column in the <legacyItalic>grp-field-list,</legacyItalic> there is a corresponding column in the child and parent <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
                <caps:sentence sentenceid="445f09b9d7d2e532a4a831e866993d13" id="tgt21" class="tgtSentence"> For each row in the parent <legacyBold>Recordset</legacyBold>, the <legacyItalic>grp-field-list</legacyItalic> columns have unique values, and the child <legacyBold>Recordset</legacyBold> referenced by the parent row consists solely of child rows whose <legacyItalic>grp-field-list</legacyItalic> columns have the same values as the parent row.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <para>
            <caps:sentence sentenceid="cdba5cd16a49d5748ccd7d81027ca5e7" id="tgt22" class="tgtSentence">If the BY clause is included, the child <legacyBold>Recordset</legacyBold>'s rows will be grouped based on the columns in the COMPUTE clause.</caps:sentence>
            <caps:sentence sentenceid="7564bfa63b2d34e57a7456b38041cbf7" id="tgt23" class="tgtSentence"> The parent <legacyBold>Recordset</legacyBold> will contain one row for each group of rows in the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="df4cae325ebf8630790de2b0f79206a1" id="tgt24" class="tgtSentence">If the BY clause is omitted, the entire child <legacyBold>Recordset</legacyBold> is treated as a single group and the parent <legacyBold>Recordset</legacyBold> will contain exactly one row.</caps:sentence>
            <caps:sentence sentenceid="b89defd6d21d2de8438a4df89a0967d6" id="tgt25" class="tgtSentence"> That row will reference the entire child <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="3626d56edd321579997230f31a565ad0" id="tgt26" class="tgtSentence"> Omitting the BY clause allows you to compute "grand total" aggregates over the entire child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fa3a10105c9b5660cbdf9bbc8079647f" id="tgt27" class="tgtSentence">For example:</caps:sentence>
          </para>
          <code>         SHAPE {select * from Orders} AS orders             COMPUTE orders, SUM(orders.OrderAmount) as TotalSales       </code>
          <para>
            <caps:sentence sentenceid="c29075f9cb56888a2d53a6a372dadc49" id="tgt28" class="tgtSentence">Regardless of which way the parent <legacyBold>Recordset</legacyBold> is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="32accd42d3126904fb189a4df8ad2bca" id="tgt29" class="tgtSentence"> If you wish, the parent <legacyBold>Recordset</legacyBold> may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</caps:sentence>
            <caps:sentence sentenceid="9b643edfa8bddbb0bf17b17393df670e" id="tgt30" class="tgtSentence"> Both the parent and the child <legacyBold>Recordset</legacyBold> may contain columns that contain an expression on the row in the <legacyBold>Recordset</legacyBold>, as well as columns that are new and initially empty.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f7235a61fdc3adc78d866fd8085d44db" id="tgt31" class="tgtSentence">Operation</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ca9599d18a765cb1aa660a6f53758ca1" id="tgt32" class="tgtSentence">The <legacyItalic>child-command</legacyItalic> is issued to the provider, which returns a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5d7c12681a9b1042e2a9dde4c886b5a7" id="tgt33" class="tgtSentence">The COMPUTE clause specifies the columns of the parent <legacyBold>Recordset</legacyBold>, which may be a reference to the child <legacyBold>Recordset</legacyBold>, one or more aggregates, a calculated expression, or new columns.</caps:sentence>
            <caps:sentence sentenceid="a9f3ae0ae51acb2510b63ff72adc392f" id="tgt34" class="tgtSentence"> If there is a BY clause, the columns it defines are also appended to the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="59b6508d31b346efe46149cf0e2b2e6c" id="tgt35" class="tgtSentence"> The BY clause specifies how the rows of the child <legacyBold>Recordset</legacyBold> are grouped.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f5f403e14d9d4fe05d673f6271059cab" id="tgt36" class="tgtSentence">For example, assume you have a table, named Demographics, which consists of State, City, and Population fields.</caps:sentence>
            <caps:sentence sentenceid="fe975b0252aed0f9b3a68b833c8bc93e" id="tgt37" class="tgtSentence"> (The population figures in the table are provided solely as an example).</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9ed39e2ea931586b6a985a6942ef573e" id="tgt38" class="tgtSentence">State</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ed5d2eaed1a1fadcc41ad1d58ed603e" id="tgt39" class="tgtSentence">City</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="248081ecb337c85ec8e4330e6099625a" id="tgt40" class="tgtSentence">Population</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c68c559d956d4ca20f435ed74a6e71e6" id="tgt41" class="tgtSentence">WA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="122fcc42899566d24a5e1d649db18a0a" id="tgt42" class="tgtSentence">Seattle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b2241e1bd982856733e6fcacff4a22f" id="tgt43" class="tgtSentence">700,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e81c4e4f2b7b93b481e13a8553c2ae1b" id="tgt44" class="tgtSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b99e089d3eea51ec04894f1f00848b54" id="tgt45" class="tgtSentence">Medford</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e05695d29cb4a9339534e5a9c273fa14" id="tgt46" class="tgtSentence">200,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e81c4e4f2b7b93b481e13a8553c2ae1b" id="tgt47" class="tgtSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06036321a2c2f161efafa86984f44168" id="tgt48" class="tgtSentence">Portland</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="471f04c5f2bc4100e10e1f33687eaa7d" id="tgt49" class="tgtSentence">400,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5435c69ed3bcc5b2e4d580e393e373d3" id="tgt50" class="tgtSentence">CA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ecee8ea1192b669fb2f3172f5c16ed2" id="tgt51" class="tgtSentence">Los Angeles</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0e0556ac49070999edc6b0263f494860" id="tgt52" class="tgtSentence">800,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5435c69ed3bcc5b2e4d580e393e373d3" id="tgt53" class="tgtSentence">CA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a982954198d9f88c312a7df019d033a" id="tgt54" class="tgtSentence">San Diego</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4604f43816d8a5651cfb5149428e2a80" id="tgt55" class="tgtSentence">600,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c68c559d956d4ca20f435ed74a6e71e6" id="tgt56" class="tgtSentence">WA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="159418ace308c35fd97ee655dabf8262" id="tgt57" class="tgtSentence">Tacoma</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f44c1b1f0109a89955ddb586fbc4b3ad" id="tgt58" class="tgtSentence">500,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e81c4e4f2b7b93b481e13a8553c2ae1b" id="tgt59" class="tgtSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c75c2b1f897895af1bffeaab692ddd1c" id="tgt60" class="tgtSentence">Corvallis</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f9f539d3a6d16b92b2f1ea8867ad020f" id="tgt61" class="tgtSentence">300,000</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="45ac43cefb1858d36aa09de34b61e6ce" id="tgt62" class="tgtSentence">Now, issue this shape command:</caps:sentence>
          </para>
          <code>rst.Open  "SHAPE {select * from demographics} AS rs "  &amp; _
          "COMPUTE rs, SUM(rs.population) BY state", _
           objConnection</code>
          <para>
            <caps:sentence sentenceid="5aa281fd62b676c8f7cbf914d6201af5" id="tgt63" class="tgtSentence">This command opens a shaped <legacyBold>Recordset</legacyBold> with two levels.</caps:sentence>
            <caps:sentence sentenceid="bee317ba8e4e64d6e2639a2ccc9e4d50" id="tgt64" class="tgtSentence"> The parent level is a generated <legacyBold>Recordset</legacyBold> with an aggregate column (<codeInline>SUM(rs.population)</codeInline>), a column referencing the child <legacyBold>Recordset</legacyBold> (<codeInline>rs</codeInline>), and a column for grouping the child <legacyBold>Recordset</legacyBold> (<codeInline>state</codeInline>).</caps:sentence>
            <caps:sentence sentenceid="f5cf18d6035fd27c1f299516da9e77b1" id="tgt65" class="tgtSentence"> The child level is the <legacyBold>Recordset</legacyBold> returned by the query command (<codeInline>select * from demographics</codeInline>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d9858a3cab80cb98d23ff6866069d71b" id="tgt66" class="tgtSentence">The child <legacyBold>Recordset</legacyBold> detail rows will be grouped by state, but otherwise in no particular order.</caps:sentence>
            <caps:sentence sentenceid="044997dc80fce496f3f871d67ad31eca" id="tgt67" class="tgtSentence"> That is, the groups will not be in alphabetical or numerical order.</caps:sentence>
            <caps:sentence sentenceid="16649b72fe0f53fbff725c35eb82b01c" id="tgt68" class="tgtSentence"> If you want the parent <legacyBold>Recordset</legacyBold> to be ordered, you can use the <legacyBold>Recordset</legacyBold> <legacyBold>Sort</legacyBold> method to order the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4c8b89c239d468c750b80e9366356990" id="tgt69" class="tgtSentence">You can now navigate the opened parent <legacyBold>Recordset</legacyBold> and access the child detail <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="85c938a8f9c7527b873326b185034945" id="tgt70" class="tgtSentence"> For more information, see <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f051632fcda6d10db5a3ce2ee9c417bf" id="tgt71" class="tgtSentence">Resultant Parent and Child Detail Recordsets</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="d0e45878043844ffc41aac437e86b602" id="tgt72" class="tgtSentence">Parent</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8413bb4cb5e20839973a02d32e1a3a7e" id="tgt73" class="tgtSentence">SUM (rs.Population)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3a2d7564baee79182ebc7b65084aabd1" id="tgt74" class="tgtSentence">rs</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9ed39e2ea931586b6a985a6942ef573e" id="tgt75" class="tgtSentence">State</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1df8aaafe8c25954f1c8795add85e7d8" id="tgt76" class="tgtSentence">1,300,000</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f720f21641c0f0e9d82ab4d7b130102e" id="tgt77" class="tgtSentence">Reference to child1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5435c69ed3bcc5b2e4d580e393e373d3" id="tgt78" class="tgtSentence">CA</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fdb091a1392869a2a92da10ad3fceb6e" id="tgt79" class="tgtSentence">1,200,000</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="90daf45beac580e2b44b3f62a87859db" id="tgt80" class="tgtSentence">Reference to child2</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c68c559d956d4ca20f435ed74a6e71e6" id="tgt81" class="tgtSentence">WA</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2209e1b2e3c8da61eca3dc82fb07c13a" id="tgt82" class="tgtSentence">1,100,000</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0e4785f6d3fdb2e97c7dac55a99a054e" id="tgt83" class="tgtSentence">Reference to child3</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e81c4e4f2b7b93b481e13a8553c2ae1b" id="tgt84" class="tgtSentence">OR</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="27cfbe367a1294dc60aef746fb69e797" id="tgt85" class="tgtSentence">Child1</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9ed39e2ea931586b6a985a6942ef573e" id="tgt86" class="tgtSentence">State</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ed5d2eaed1a1fadcc41ad1d58ed603e" id="tgt87" class="tgtSentence">City</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="248081ecb337c85ec8e4330e6099625a" id="tgt88" class="tgtSentence">Population</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5435c69ed3bcc5b2e4d580e393e373d3" id="tgt89" class="tgtSentence">CA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ecee8ea1192b669fb2f3172f5c16ed2" id="tgt90" class="tgtSentence">Los Angeles</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0e0556ac49070999edc6b0263f494860" id="tgt91" class="tgtSentence">800,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5435c69ed3bcc5b2e4d580e393e373d3" id="tgt92" class="tgtSentence">CA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a982954198d9f88c312a7df019d033a" id="tgt93" class="tgtSentence">San Diego</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4604f43816d8a5651cfb5149428e2a80" id="tgt94" class="tgtSentence">600,000</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="bf94099de6e08e39478cee3d06c5fe47" id="tgt95" class="tgtSentence">Child2</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9ed39e2ea931586b6a985a6942ef573e" id="tgt96" class="tgtSentence">State</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ed5d2eaed1a1fadcc41ad1d58ed603e" id="tgt97" class="tgtSentence">City</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="248081ecb337c85ec8e4330e6099625a" id="tgt98" class="tgtSentence">Population</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c68c559d956d4ca20f435ed74a6e71e6" id="tgt99" class="tgtSentence">WA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="122fcc42899566d24a5e1d649db18a0a" id="tgt100" class="tgtSentence">Seattle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b2241e1bd982856733e6fcacff4a22f" id="tgt101" class="tgtSentence">700,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c68c559d956d4ca20f435ed74a6e71e6" id="tgt102" class="tgtSentence">WA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="159418ace308c35fd97ee655dabf8262" id="tgt103" class="tgtSentence">Tacoma</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f44c1b1f0109a89955ddb586fbc4b3ad" id="tgt104" class="tgtSentence">500,000</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="08fda666c89a81db2667d287bd951481" id="tgt105" class="tgtSentence">Child3</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9ed39e2ea931586b6a985a6942ef573e" id="tgt106" class="tgtSentence">State</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ed5d2eaed1a1fadcc41ad1d58ed603e" id="tgt107" class="tgtSentence">City</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="248081ecb337c85ec8e4330e6099625a" id="tgt108" class="tgtSentence">Population</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e81c4e4f2b7b93b481e13a8553c2ae1b" id="tgt109" class="tgtSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b99e089d3eea51ec04894f1f00848b54" id="tgt110" class="tgtSentence">Medford</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e05695d29cb4a9339534e5a9c273fa14" id="tgt111" class="tgtSentence">200,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e81c4e4f2b7b93b481e13a8553c2ae1b" id="tgt112" class="tgtSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06036321a2c2f161efafa86984f44168" id="tgt113" class="tgtSentence">Portland</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="471f04c5f2bc4100e10e1f33687eaa7d" id="tgt114" class="tgtSentence">400,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e81c4e4f2b7b93b481e13a8553c2ae1b" id="tgt115" class="tgtSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c75c2b1f897895af1bffeaab692ddd1c" id="tgt116" class="tgtSentence">Corvallis</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f9f539d3a6d16b92b2f1ea8867ad020f" id="tgt117" class="tgtSentence">300,000</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</link>
        <link xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">Data Shaping Summary</link>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</link>
        <link xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">Shape APPEND Clause</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
        <link xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value Property</link>
        <link xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications Functions</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">A shape COMPUTE clause generates a parent <legacyBold>Recordset</legacyBold>, whose columns consist of a reference to the child <legacyBold>Recordset</legacyBold>; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child <legacyBold>Recordset</legacyBold> or a previously shaped <legacyBold>Recordset</legacyBold>; and any columns from the child <legacyBold>Recordset</legacyBold> listed in the optional BY clause.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>SHAPE <legacyItalic xmlns="">child-command</legacyItalic> [AS] <legacyItalic xmlns="">child-alias</legacyItalic>
   COMPUTE <legacyItalic xmlns="">child-alias</legacyItalic> [[AS] <legacyItalic xmlns="">name</legacyItalic>], [<legacyItalic xmlns="">appended-column-list</legacyItalic>]
   [BY <legacyItalic xmlns="">grp-field-list</legacyItalic>]</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Description</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The parts of this clause are as follows:  </caps:sentence>
          </para>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>child-command</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Consists of one of the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">A query command within curly braces ("{}") that returns a child <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                    <caps:sentence id="src8" class="srcSentence"> The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</caps:sentence>
                    <caps:sentence id="src9" class="srcSentence"> This will typically be the SQL language, although ADO does not require any particular query language.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">The name of an existing shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Another shape command.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">The TABLE keyword, followed by the name of a table in the data provider.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </definition>
            <definedTerm>
              <caps:sentence id="src13" class="srcSentence"> <legacyItalic>child-alias</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src14" class="srcSentence">An alias used to refer to the <legacyBold>Recordset</legacyBold> returned by the <legacyItalic>child-command.</legacyItalic> The <legacyItalic>child-alias</legacyItalic> is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src15" class="srcSentence"> <legacyItalic>appended-column-list</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src16" class="srcSentence">A list in which each element defines a column in the generated parent.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src18" class="srcSentence"> <legacyItalic>grp-field-list</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src19" class="srcSentence">A list of columns in the parent and child <legacyBold>Recordset</legacyBold> objects that specifies how rows should be grouped in the child.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src20" class="srcSentence">For each column in the <legacyItalic>grp-field-list,</legacyItalic> there is a corresponding column in the child and parent <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> For each row in the parent <legacyBold>Recordset</legacyBold>, the <legacyItalic>grp-field-list</legacyItalic> columns have unique values, and the child <legacyBold>Recordset</legacyBold> referenced by the parent row consists solely of child rows whose <legacyItalic>grp-field-list</legacyItalic> columns have the same values as the parent row.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <para>
            <caps:sentence id="src22" class="srcSentence">If the BY clause is included, the child <legacyBold>Recordset</legacyBold>'s rows will be grouped based on the columns in the COMPUTE clause.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> The parent <legacyBold>Recordset</legacyBold> will contain one row for each group of rows in the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">If the BY clause is omitted, the entire child <legacyBold>Recordset</legacyBold> is treated as a single group and the parent <legacyBold>Recordset</legacyBold> will contain exactly one row.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> That row will reference the entire child <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> Omitting the BY clause allows you to compute "grand total" aggregates over the entire child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">For example:</caps:sentence>
          </para>
          <code>         SHAPE {select * from Orders} AS orders             COMPUTE orders, SUM(orders.OrderAmount) as TotalSales       </code>
          <para>
            <caps:sentence id="src28" class="srcSentence">Regardless of which way the parent <legacyBold>Recordset</legacyBold> is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> If you wish, the parent <legacyBold>Recordset</legacyBold> may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> Both the parent and the child <legacyBold>Recordset</legacyBold> may contain columns that contain an expression on the row in the <legacyBold>Recordset</legacyBold>, as well as columns that are new and initially empty.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src31" class="srcSentence">Operation</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src32" class="srcSentence">The <legacyItalic>child-command</legacyItalic> is issued to the provider, which returns a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src33" class="srcSentence">The COMPUTE clause specifies the columns of the parent <legacyBold>Recordset</legacyBold>, which may be a reference to the child <legacyBold>Recordset</legacyBold>, one or more aggregates, a calculated expression, or new columns.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> If there is a BY clause, the columns it defines are also appended to the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> The BY clause specifies how the rows of the child <legacyBold>Recordset</legacyBold> are grouped.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src36" class="srcSentence">For example, assume you have a table, named Demographics, which consists of State, City, and Population fields.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> (The population figures in the table are provided solely as an example).</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">State</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">City</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Population</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">WA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Seattle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">700,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Medford</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">200,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Portland</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">400,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">CA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Los Angeles</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">800,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">CA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">San Diego</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">600,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">WA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Tacoma</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">500,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">Corvallis</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">300,000</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src62" class="srcSentence">Now, issue this shape command:</caps:sentence>
          </para>
          <code>rst.Open  "SHAPE {select * from demographics} AS rs "  &amp; _
          "COMPUTE rs, SUM(rs.population) BY state", _
           objConnection</code>
          <para>
            <caps:sentence id="src63" class="srcSentence">This command opens a shaped <legacyBold>Recordset</legacyBold> with two levels.</caps:sentence>
            <caps:sentence id="src64" class="srcSentence"> The parent level is a generated <legacyBold>Recordset</legacyBold> with an aggregate column (<codeInline>SUM(rs.population)</codeInline>), a column referencing the child <legacyBold>Recordset</legacyBold> (<codeInline>rs</codeInline>), and a column for grouping the child <legacyBold>Recordset</legacyBold> (<codeInline>state</codeInline>).</caps:sentence>
            <caps:sentence id="src65" class="srcSentence"> The child level is the <legacyBold>Recordset</legacyBold> returned by the query command (<codeInline>select * from demographics</codeInline>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src66" class="srcSentence">The child <legacyBold>Recordset</legacyBold> detail rows will be grouped by state, but otherwise in no particular order.</caps:sentence>
            <caps:sentence id="src67" class="srcSentence"> That is, the groups will not be in alphabetical or numerical order.</caps:sentence>
            <caps:sentence id="src68" class="srcSentence"> If you want the parent <legacyBold>Recordset</legacyBold> to be ordered, you can use the <legacyBold>Recordset</legacyBold> <legacyBold>Sort</legacyBold> method to order the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src69" class="srcSentence">You can now navigate the opened parent <legacyBold>Recordset</legacyBold> and access the child detail <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src70" class="srcSentence"> For more information, see <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src71" class="srcSentence">Resultant Parent and Child Detail Recordsets</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src72" class="srcSentence">Parent</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">SUM (rs.Population)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">rs</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">State</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src76" class="srcSentence">1,300,000</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">Reference to child1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src78" class="srcSentence">CA</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">1,200,000</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">Reference to child2</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">WA</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src82" class="srcSentence">1,100,000</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">Reference to child3</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">OR</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src85" class="srcSentence">Child1</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">State</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">City</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">Population</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">CA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">Los Angeles</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">800,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">CA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">San Diego</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">600,000</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src95" class="srcSentence">Child2</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">State</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src97" class="srcSentence">City</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">Population</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">WA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Seattle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">700,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">WA</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src103" class="srcSentence">Tacoma</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">500,000</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src105" class="srcSentence">Child3</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">State</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">City</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">Population</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Medford</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">200,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">Portland</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">400,000</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">OR</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">Corvallis</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">300,000</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</link>
        <link xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">Data Shaping Summary</link>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</link>
        <link xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">Shape APPEND Clause</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
        <link xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value Property</link>
        <link xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications Functions</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
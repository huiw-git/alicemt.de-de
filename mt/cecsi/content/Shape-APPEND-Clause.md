---
title: "Shape APPEND Clause"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f90fcf55-6b24-401d-94e1-d65bd24bd342
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
# Shape APPEND Clause
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a5abdfd64201969fef1d0b0a4b3fcad2" id="tgt1" class="tgtSentence">The shape command APPEND clause appends a column or columns to a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="2e78c1dcf58e703bf398d724b5ee6b9a" id="tgt2" class="tgtSentence"> Frequently, these columns are chapter columns, which refer to a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt3" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>SHAPE [<legacyItalic xmlns="">parent-command</legacyItalic> [[AS] <legacyItalic xmlns="">parent-alias</legacyItalic>]] APPEND <legacyItalic xmlns="">column-list</legacyItalic></code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt4" class="tgtSentence">Description</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="87e7a3e02e35ba2f38799721c7c49110" id="tgt5" class="tgtSentence">The parts of this clause are as follows:  </caps:sentence>
          </para>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="46829ab980d59840e4860151f621b270" id="tgt6" class="tgtSentence"> <legacyItalic>parent-command</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ee9be02cef0ffb29747f9b5a65aa029e" id="tgt7" class="tgtSentence">Zero or one of the following (you can omit the <legacyItalic>parent-command</legacyItalic> completely):</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6060498f29f3b4324448e0aaa3a6ad4c" id="tgt8" class="tgtSentence">A provider command enclosed in braces ("{}") that returns a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                    <caps:sentence sentenceid="7836e2a3e5649a925c57c005f820624c" id="tgt9" class="tgtSentence"> The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</caps:sentence>
                    <caps:sentence sentenceid="6b23d3186a0b9b1b2e98b9fb48a39d21" id="tgt10" class="tgtSentence"> This will typically be the SQL language, although ADO does not require any particular query language.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3e5f385cfeef5f195b48963573585394" id="tgt11" class="tgtSentence">Another shape command embedded in parentheses.</caps:sentence>
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
              <caps:sentence sentenceid="7e61f72fc23d6f61dfd8fdb96f498144" id="tgt13" class="tgtSentence"> <legacyItalic>parent-alias</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="014cb4236220774aab755da446bb6efd" id="tgt14" class="tgtSentence">An optional alias that refers to the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="40d2c5c3148a17726d1e0b26ca568cbc" id="tgt15" class="tgtSentence"> <legacyItalic>column-list</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b3d304d9afacd618193b2a77a21dc30c" id="tgt16" class="tgtSentence">One or more of the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5d3d1af45b43ae74a025d72826a38eef" id="tgt17" class="tgtSentence">An aggregate column.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="016f05633b69dc2b7b4b196de2b1e22c" id="tgt18" class="tgtSentence">A calculated column.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="458eabc8cc8aed20e11d74ed9b4a74b9" id="tgt19" class="tgtSentence">A new column created by using the NEW clause.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9ba75fc02a40dbaaf7cb61ec55cf147b" id="tgt20" class="tgtSentence">A chapter column.</caps:sentence>
                    <caps:sentence sentenceid="0389800ad66b0892bef88c3b86c0accf" id="tgt21" class="tgtSentence"> A chapter column definition is enclosed in parentheses ("()").</caps:sentence>
                    <caps:sentence sentenceid="4b40635b358027adf91d1b735272b8cd" id="tgt22" class="tgtSentence"> See the following syntax.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </definition>
          </definitionTable>
          <code>SHAPE [<legacyItalic xmlns="">parent-command</legacyItalic> [[AS] <legacyItalic xmlns="">parent-alias</legacyItalic>]]
   APPEND (<legacyItalic xmlns="">child-recordset</legacyItalic> [ [[AS] <legacyItalic xmlns="">child-alias</legacyItalic>] 
      RELATE <legacyItalic xmlns="">parent-column</legacyItalic> TO <legacyItalic xmlns="">child-column</legacyItalic> | PARAMETER <legacyItalic xmlns="">param-number</legacyItalic>, <codeFeaturedElement xmlns="">...</codeFeaturedElement> ])
   [[AS] <legacyItalic xmlns="">chapter-alias</legacyItalic>] 
   [, <codeFeaturedElement xmlns="">...</codeFeaturedElement> ]</code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="461ac86703b3cd05357e038e25a2d650" id="tgt23" class="tgtSentence"> <legacyItalic>child-recordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6060498f29f3b4324448e0aaa3a6ad4c" id="tgt24" class="tgtSentence">A provider command enclosed in braces ("{}") that returns a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                    <caps:sentence sentenceid="7836e2a3e5649a925c57c005f820624c" id="tgt25" class="tgtSentence"> The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</caps:sentence>
                    <caps:sentence sentenceid="6b23d3186a0b9b1b2e98b9fb48a39d21" id="tgt26" class="tgtSentence"> This will typically be the SQL language, although ADO does not require any particular query language.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3e5f385cfeef5f195b48963573585394" id="tgt27" class="tgtSentence">Another shape command embedded in parentheses.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bcfafbe16ca7210077fa433c50900a68" id="tgt28" class="tgtSentence">The name of an existing shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="df545ab3bf7577d15fffac44f7484154" id="tgt29" class="tgtSentence">The TABLE keyword, followed by the name of a table in the data provider.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="fd7a393c43fdae313065fe8bf08ddbd2" id="tgt30" class="tgtSentence"> <legacyItalic>child-alias</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0616f0b806c644b8ce87b41a898f29f3" id="tgt31" class="tgtSentence">An alias that refers to the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="547067d6450e3f44e84967764f5f8f5e" id="tgt32" class="tgtSentence"> <legacyItalic>parent-column</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b3eab432297bd4d298b85aed698a65a3" id="tgt33" class="tgtSentence">A column in the <legacyBold>Recordset</legacyBold> returned by the <legacyItalic>parent-command.</legacyItalic></caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="360f0cd871108789fe41f95e41eaa87d" id="tgt34" class="tgtSentence"> <legacyItalic>child-column</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="90da81c1e13af4f8c8636de0a08fbb6e" id="tgt35" class="tgtSentence">A column in the <legacyBold>Recordset</legacyBold> returned by the <legacyItalic>child-command</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="6081bc06f67082973e3cc9bb818061dd" id="tgt36" class="tgtSentence"> <legacyItalic>param-number</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="81f0a98e4005fe7faa1e7f36f31a5d12" id="tgt37" class="tgtSentence">See <legacyLink xlink:href="4fae0d54-83b6-4ead-99cc-bcf532daa121">Operation of Parameterized Commands</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="fca114995489a478bb8a19a83b45bcb2" id="tgt38" class="tgtSentence"> <legacyItalic>chapter-alias</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="365bfa1a2d9168a6d7ae7410a5e71ae4" id="tgt39" class="tgtSentence">An alias that refers to the chapter column appended to the parent.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="08b519ea86350c281f8639fd0ba67249" id="tgt40" class="tgtSentence">The <legacyItalic>"parent-column </legacyItalic>TO <legacyItalic>child-column" </legacyItalic>clause is actually a list, where each relation defined is separated by a comma</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="522afb324e29071660d89d5173be1630" id="tgt41" class="tgtSentence">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9ee01220f3d5083ab2d5fe3a8d0de4cb" id="tgt42" class="tgtSentence">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider.</caps:sentence>
            <caps:sentence sentenceid="56871ae98add3d94e630d723702baa3d" id="tgt43" class="tgtSentence"> For example, in the following SHAPE command,</caps:sentence>
          </para>
          <code>SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2)</code>
          <para>
            <caps:sentence sentenceid="b413f9d5b6d9efa024211aa7e8ce07d6" id="tgt44" class="tgtSentence">SHAPE will execute two commands: <codeInline>select * from t1</codeInline> and (<codeInline>select * from t2 RELATE k1 TO k2)</codeInline>.</caps:sentence>
            <caps:sentence sentenceid="21066b93ec31d17103ac1cd99df2895b" id="tgt45" class="tgtSentence"> If the user supplies a compound command that consists of multiple provider commands separated by semicolons, SHAPE is not able to distinguish the difference.</caps:sentence>
            <caps:sentence sentenceid="afcdb830ef1e62802617d9d767ede100" id="tgt46" class="tgtSentence"> So in the following SHAPE command,</caps:sentence>
          </para>
          <code>SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2)</code>
          <para>
            <caps:sentence sentenceid="2f6d88366b061f15c73c1c963f745185" id="tgt47" class="tgtSentence">SHAPE executes <codeInline>select * from t1; drop table t1</codeInline> and (<codeInline>select * from t2 RELATE k1 TO k2), </codeInline>not realizing that <codeInline>drop table t1</codeInline> is a separate and in this case, dangerous, provider command.</caps:sentence>
            <caps:sentence sentenceid="4f541071cfb200f73a4ed6774276e7e8" id="tgt48" class="tgtSentence"> Applications must always validate the user input to prevent such potential hacker attacks from occurring.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt49" class="tgtSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="01d77a56e89a47d02e20e11a049ef117" id="tgt50" class="tgtSentence">
                  <legacyLink xlink:href="9700e50a-9f17-4ba3-8afb-f750741dc6ca">Operation of Non-Parameterized Commands</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a27bd35d4fe42cbab62434c51528c476" id="tgt51" class="tgtSentence">
                  <legacyLink xlink:href="4fae0d54-83b6-4ead-99cc-bcf532daa121">Operation of Parameterized Commands</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f12ae980f8ad4c96ece95ebad9242b26" id="tgt52" class="tgtSentence">
                  <legacyLink xlink:href="e8ca40e8-459c-40e2-8dd3-3ec6d5ee7b51">Hybrid Commands</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d76ddd3db45f0227d8c6dd39ac0bc8f3" id="tgt53" class="tgtSentence">
                  <legacyLink xlink:href="a576bf81-8f3c-4ba1-817b-87e89a8da684">Intervening Shape COMPUTE Clauses</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
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
          <caps:sentence id="src1" class="srcSentence">The shape command APPEND clause appends a column or columns to a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Frequently, these columns are chapter columns, which refer to a child <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>SHAPE [<legacyItalic xmlns="">parent-command</legacyItalic> [[AS] <legacyItalic xmlns="">parent-alias</legacyItalic>]] APPEND <legacyItalic xmlns="">column-list</legacyItalic></code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Description</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The parts of this clause are as follows:  </caps:sentence>
          </para>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>parent-command</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Zero or one of the following (you can omit the <legacyItalic>parent-command</legacyItalic> completely):</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">A provider command enclosed in braces ("{}") that returns a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                    <caps:sentence id="src9" class="srcSentence"> The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</caps:sentence>
                    <caps:sentence id="src10" class="srcSentence"> This will typically be the SQL language, although ADO does not require any particular query language.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Another shape command embedded in parentheses.</caps:sentence>
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
              <caps:sentence id="src13" class="srcSentence"> <legacyItalic>parent-alias</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src14" class="srcSentence">An optional alias that refers to the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src15" class="srcSentence"> <legacyItalic>column-list</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src16" class="srcSentence">One or more of the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">An aggregate column.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">A calculated column.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">A new column created by using the NEW clause.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">A chapter column.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> A chapter column definition is enclosed in parentheses ("()").</caps:sentence>
                    <caps:sentence id="src22" class="srcSentence"> See the following syntax.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </definition>
          </definitionTable>
          <code>SHAPE [<legacyItalic xmlns="">parent-command</legacyItalic> [[AS] <legacyItalic xmlns="">parent-alias</legacyItalic>]]
   APPEND (<legacyItalic xmlns="">child-recordset</legacyItalic> [ [[AS] <legacyItalic xmlns="">child-alias</legacyItalic>] 
      RELATE <legacyItalic xmlns="">parent-column</legacyItalic> TO <legacyItalic xmlns="">child-column</legacyItalic> | PARAMETER <legacyItalic xmlns="">param-number</legacyItalic>, <codeFeaturedElement xmlns="">...</codeFeaturedElement> ])
   [[AS] <legacyItalic xmlns="">chapter-alias</legacyItalic>] 
   [, <codeFeaturedElement xmlns="">...</codeFeaturedElement> ]</code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src23" class="srcSentence"> <legacyItalic>child-recordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">A provider command enclosed in braces ("{}") that returns a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                    <caps:sentence id="src25" class="srcSentence"> The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</caps:sentence>
                    <caps:sentence id="src26" class="srcSentence"> This will typically be the SQL language, although ADO does not require any particular query language.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Another shape command embedded in parentheses.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">The name of an existing shaped <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">The TABLE keyword, followed by the name of a table in the data provider.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </definition>
            <definedTerm>
              <caps:sentence id="src30" class="srcSentence"> <legacyItalic>child-alias</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src31" class="srcSentence">An alias that refers to the child <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src32" class="srcSentence"> <legacyItalic>parent-column</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src33" class="srcSentence">A column in the <legacyBold>Recordset</legacyBold> returned by the <legacyItalic>parent-command.</legacyItalic></caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src34" class="srcSentence"> <legacyItalic>child-column</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src35" class="srcSentence">A column in the <legacyBold>Recordset</legacyBold> returned by the <legacyItalic>child-command</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src36" class="srcSentence"> <legacyItalic>param-number</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src37" class="srcSentence">See <legacyLink xlink:href="4fae0d54-83b6-4ead-99cc-bcf532daa121">Operation of Parameterized Commands</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src38" class="srcSentence"> <legacyItalic>chapter-alias</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src39" class="srcSentence">An alias that refers to the chapter column appended to the parent.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence id="src40" class="srcSentence">The <legacyItalic>"parent-column </legacyItalic>TO <legacyItalic>child-column" </legacyItalic>clause is actually a list, where each relation defined is separated by a comma</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src41" class="srcSentence">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src42" class="srcSentence">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> For example, in the following SHAPE command,</caps:sentence>
          </para>
          <code>SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2)</code>
          <para>
            <caps:sentence id="src44" class="srcSentence">SHAPE will execute two commands: <codeInline>select * from t1</codeInline> and (<codeInline>select * from t2 RELATE k1 TO k2)</codeInline>.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> If the user supplies a compound command that consists of multiple provider commands separated by semicolons, SHAPE is not able to distinguish the difference.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> So in the following SHAPE command,</caps:sentence>
          </para>
          <code>SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2)</code>
          <para>
            <caps:sentence id="src47" class="srcSentence">SHAPE executes <codeInline>select * from t1; drop table t1</codeInline> and (<codeInline>select * from t2 RELATE k1 TO k2), </codeInline>not realizing that <codeInline>drop table t1</codeInline> is a separate and in this case, dangerous, provider command.</caps:sentence>
            <caps:sentence id="src48" class="srcSentence"> Applications must always validate the user input to prevent such potential hacker attacks from occurring.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src49" class="srcSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src50" class="srcSentence">
                  <legacyLink xlink:href="9700e50a-9f17-4ba3-8afb-f750741dc6ca">Operation of Non-Parameterized Commands</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src51" class="srcSentence">
                  <legacyLink xlink:href="4fae0d54-83b6-4ead-99cc-bcf532daa121">Operation of Parameterized Commands</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src52" class="srcSentence">
                  <legacyLink xlink:href="e8ca40e8-459c-40e2-8dd3-3ec6d5ee7b51">Hybrid Commands</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src53" class="srcSentence">
                  <legacyLink xlink:href="a576bf81-8f3c-4ba1-817b-87e89a8da684">Intervening Shape COMPUTE Clauses</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
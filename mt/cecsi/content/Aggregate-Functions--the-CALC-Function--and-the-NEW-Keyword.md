---
title: "Aggregate Functions, the CALC Function, and the NEW Keyword"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0590b466-2a36-49a2-868e-028ef5e49394
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
# Aggregate Functions, the CALC Function, and the NEW Keyword
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c5448a0ae144ef8a38639034ef5122e8" id="tgt1" class="tgtSentence">Data shaping supports the following functions.</caps:sentence>
          <caps:sentence sentenceid="87952613cfb15c40a3f99b1bb0e0c30a" id="tgt2" class="tgtSentence"> The name assigned to the chapter containing the column to be operated on is the <legacyItalic>chapter-alias</legacyItalic>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3d39fcf3522ad289e86e58dccbb8eede" id="tgt3" class="tgtSentence">A chapter-alias can be fully qualified, consisting of each chapter column name leading to the chapter containing the <legacyItalic>column-name, </legacyItalic>all separated by periods.</caps:sentence>
          <caps:sentence sentenceid="2ec44b882c56a7b8de9f199956ba322f" id="tgt4" class="tgtSentence"> For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="31253bfcbb346d6eae089deb20f273ee" id="tgt5" class="tgtSentence">Aggregate Functions</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt6" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="34aa98d9b7666090a40d31161c516f82" id="tgt7" class="tgtSentence">SUM(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4567ad12340ef8971facae3445d5b092" id="tgt8" class="tgtSentence">Calculates the sum of all values in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="907cf51ba5fbe0991bd0f5f7579a2c55" id="tgt9" class="tgtSentence">AVG(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ded7b32ffffac25940b8087c155d60f1" id="tgt10" class="tgtSentence">Calculates the average of all values in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0285e227460915609d78c4e951f6b7bb" id="tgt11" class="tgtSentence">MAX(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="29763919c5766eff31ce06abb577c91d" id="tgt12" class="tgtSentence">Calculates the maximum value in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="69dd8b782d87da4d46fa04a614c96f7f" id="tgt13" class="tgtSentence">MIN(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1a1a8519cc2648726a433eb836da4da3" id="tgt14" class="tgtSentence">Calculates the minimum value in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3f2f215da93c1709f6002bc3a2e597fd" id="tgt15" class="tgtSentence">COUNT(<legacyItalic>chapter-alias</legacyItalic>[.<legacyItalic>column-name</legacyItalic>])</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bc8eeab3ed4fc64f5637d2c8ed3e9fa7" id="tgt16" class="tgtSentence">Counts the number of rows in the specified alias.</caps:sentence>
                  <caps:sentence sentenceid="31b4a0420bb0706129311b4eee387b81" id="tgt17" class="tgtSentence"> If a column is specified, only rows for which that column is non-Null are included in the count.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="69d7ae31b5e212a25453282787f910f9" id="tgt18" class="tgtSentence">STDEV(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2742b6b3887cae482c089a540ddd026d" id="tgt19" class="tgtSentence">Calculates the standard deviation in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="89fc945042f7a1974dda7d83ef963b17" id="tgt20" class="tgtSentence">ANY(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6010bf52ff3e48d480d61a4b364b0f48" id="tgt21" class="tgtSentence">A value of the specified column.</caps:sentence>
                  <caps:sentence sentenceid="81309c14bd08bffc2de5426aba865438" id="tgt22" class="tgtSentence"> ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="4c642807269b47c676e4fff099331677" id="tgt23" class="tgtSentence">               <legacyBold>Note   </legacyBold>If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="06b3ba65c954b020b9fc31fbb25d162b" id="tgt24" class="tgtSentence">Calculated expression</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt25" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7902c102ee889149a41c6f2ef5eeb216" id="tgt26" class="tgtSentence">CALC(<legacyItalic>expression</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="015ac5acecf4aea37784cd0ec7a3a54a" id="tgt27" class="tgtSentence">Calculates an arbitrary expression, but only on the row of the <legacyBold>Recordset</legacyBold> containing the CALC function.</caps:sentence>
                  <caps:sentence sentenceid="0dc2d219002688a527f6940f5166e42e" id="tgt28" class="tgtSentence"> Any expression using these <legacyLink xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications (VBA) Functions</legacyLink> is allowed.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b30c8fa0747768503e6c1e15313ae8db" id="tgt29" class="tgtSentence">NEW keyword</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt30" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6aaf2689a259faa85e358d306343acd5" id="tgt31" class="tgtSentence">NEW <legacyItalic>field-type</legacyItalic> [(<legacyItalic>width</legacyItalic> | <legacyItalic>scale </legacyItalic>| <legacyItalic>precision</legacyItalic> | <legacyItalic>error</legacyItalic> [, <legacyItalic>scale</legacyItalic> | <legacyItalic>error</legacyItalic>])]</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cf2ffcd8be57caa7b9381c6e0471a013" id="tgt32" class="tgtSentence">Adds an empty column of the specified type to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="c338aece88ff3096f67b3e35243dc5ab" id="tgt33" class="tgtSentence">The <legacyItalic>field-type</legacyItalic> passed with the NEW keyword can be any of the following data types.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e8a57d669aacab7ce4699ea6eb9f9773" id="tgt34" class="tgtSentence">OLE DB data types</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4d2c06ef91c1d45ad3cba93d85c9fccb" id="tgt35" class="tgtSentence">ADO data type equivalent(s)</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6f7b06e2c7523aa9c6e7b656b274c42b" id="tgt36" class="tgtSentence">DBTYPE_BSTR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7f745527b6485673f9e42dd4fe054fb1" id="tgt37" class="tgtSentence">adBSTR</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="514618e7c343dfd584286beb00dd0003" id="tgt38" class="tgtSentence">DBTYPE_BOOL</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="37d52c4baad3447a789a5339c3378dbc" id="tgt39" class="tgtSentence">adBoolean</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a490ecbf59326064a5a97b91009f9df7" id="tgt40" class="tgtSentence">DBTYPE_DECIMAL</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="baaa708f94b121de5139624d4fd370cd" id="tgt41" class="tgtSentence">adDecimal</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ce331478643b7a286cb1beab75e0004f" id="tgt42" class="tgtSentence">DBTYPE_UI1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="989f37e5e05fa5d68baa0dd99b5424b9" id="tgt43" class="tgtSentence">adUnsignedTinyInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3d6b33b88fcf1df138587862fcbe3bb0" id="tgt44" class="tgtSentence">DBTYPE_I1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="85d11b42b09e2a64eb79ec906f814369" id="tgt45" class="tgtSentence">adTinyInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="98609c92f8835eace021d525f2085370" id="tgt46" class="tgtSentence">DBTYPE_UI2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="74a795a334418d7a5667aa2034211e53" id="tgt47" class="tgtSentence">adUnsignedSmallInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2f0e15f7298b47a51d58bcdd17e62678" id="tgt48" class="tgtSentence">DBTYPE_UI4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="16a77b22ef1a3830fe42b79fa1b6f6bb" id="tgt49" class="tgtSentence">adUnsignedInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6cd48dc4ff4928f2397139fdf0002bae" id="tgt50" class="tgtSentence">DBTYPE_I8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fd6cbae79d8c56e2c73513d41af2ba7" id="tgt51" class="tgtSentence">adBigInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="be0b7d3814fa5d6fe041d7b416e71f06" id="tgt52" class="tgtSentence">DBTYPE_UI8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="22210ae9448d5f570738afade201f348" id="tgt53" class="tgtSentence">adUnsignedBigInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ae0530cffe052e07c127331c41ee970c" id="tgt54" class="tgtSentence">DBTYPE_GUID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fcafaddea899221c3d28f9fa5f19902c" id="tgt55" class="tgtSentence">adGuid</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="aa7c078564f0a1fd2dd522eb005be5b1" id="tgt56" class="tgtSentence">DBTYPE_BYTES</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="11d754324a1a25f02a09e5cabcd73ac9" id="tgt57" class="tgtSentence">adBinary, AdVarBinary, adLongVarBinary</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="990daf0d56b5c4aa95bfa0ae42607e81" id="tgt58" class="tgtSentence">DBTYPE_STR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c5b8d79e58dc5051b0bab2f21bf68e73" id="tgt59" class="tgtSentence">adChar, adVarChar, adLongVarChar</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7a2dab2dfbccb778fc5ca3cb7afa4f07" id="tgt60" class="tgtSentence">DBTYPE_WSTR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="de8d1e3cd284e9241bbe235f574321c3" id="tgt61" class="tgtSentence">adWChar, adVarWChar, adLongVarWChar</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d6edc604207451d0494e9f21ec20b38c" id="tgt62" class="tgtSentence">DBTYPE_NUMERIC</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="05d4cf9c8094b00fde5bfa5407085a6e" id="tgt63" class="tgtSentence">adNumeric</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c59676f5bf10e89d7d1b4abeea4fe436" id="tgt64" class="tgtSentence">DBTYPE_DBDATE</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6fac38c34de456eb0aaa8a475ba3aae2" id="tgt65" class="tgtSentence">adDBDate</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4ffd61d4f6681172f4d9b7ee5077fbdb" id="tgt66" class="tgtSentence">DBTYPE_DBTIME</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5eb84d814fa77850ebcb992b74227ee6" id="tgt67" class="tgtSentence">adDBTime</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="17d43b60caa5a9dbab2c0d70cc280a85" id="tgt68" class="tgtSentence">DBTYPE_DBTIMESTAMP</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c69c01b6333a51fc8588b19feace0cfe" id="tgt69" class="tgtSentence">adDBTimeStamp</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="28c3366f88a8c7f3394c1efaa9fdde82" id="tgt70" class="tgtSentence">DBTYPE_VARNUMERIC</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="80bc70e7d8e9b47f761f411b82722f9d" id="tgt71" class="tgtSentence">adVarNumeric</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="63ab496907e50592a646b7869307d54c" id="tgt72" class="tgtSentence">DBTYPE_FILETIME</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="58298a73bdbf93666a0022f248f336fa" id="tgt73" class="tgtSentence">adFileTime</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f6f805647bbe303f5b4452f4a052c8ae" id="tgt74" class="tgtSentence">DBTYPE_ERROR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="87792d622adc7a98d79ba5c4651a83cc" id="tgt75" class="tgtSentence">adError</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="4a2e146a0901556439ea5a1684852251" id="tgt76" class="tgtSentence">When the new field is of type decimal (in OLE DB, DBTYPE_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Data shaping supports the following functions.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The name assigned to the chapter containing the column to be operated on is the <legacyItalic>chapter-alias</legacyItalic>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">A chapter-alias can be fully qualified, consisting of each chapter column name leading to the chapter containing the <legacyItalic>column-name, </legacyItalic>all separated by periods.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Aggregate Functions</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">SUM(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Calculates the sum of all values in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">AVG(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Calculates the average of all values in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">MAX(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Calculates the maximum value in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">MIN(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Calculates the minimum value in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">COUNT(<legacyItalic>chapter-alias</legacyItalic>[.<legacyItalic>column-name</legacyItalic>])</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Counts the number of rows in the specified alias.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> If a column is specified, only rows for which that column is non-Null are included in the count.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">STDEV(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Calculates the standard deviation in the specified column.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">ANY(<legacyItalic>chapter-alias</legacyItalic>.<legacyItalic>column-name</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">A value of the specified column.</caps:sentence>
                  <caps:sentence id="src22" class="srcSentence"> ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src23" class="srcSentence">               <legacyBold>Note   </legacyBold>If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Calculated expression</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">CALC(<legacyItalic>expression</legacyItalic>)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Calculates an arbitrary expression, but only on the row of the <legacyBold>Recordset</legacyBold> containing the CALC function.</caps:sentence>
                  <caps:sentence id="src28" class="srcSentence"> Any expression using these <legacyLink xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications (VBA) Functions</legacyLink> is allowed.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">NEW keyword</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">NEW <legacyItalic>field-type</legacyItalic> [(<legacyItalic>width</legacyItalic> | <legacyItalic>scale </legacyItalic>| <legacyItalic>precision</legacyItalic> | <legacyItalic>error</legacyItalic> [, <legacyItalic>scale</legacyItalic> | <legacyItalic>error</legacyItalic>])]</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Adds an empty column of the specified type to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src33" class="srcSentence">The <legacyItalic>field-type</legacyItalic> passed with the NEW keyword can be any of the following data types.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">OLE DB data types</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">ADO data type equivalent(s)</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">DBTYPE_BSTR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">adBSTR</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">DBTYPE_BOOL</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">adBoolean</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">DBTYPE_DECIMAL</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">adDecimal</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">DBTYPE_UI1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">adUnsignedTinyInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src44" class="srcSentence">DBTYPE_I1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">adTinyInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">DBTYPE_UI2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">adUnsignedSmallInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src48" class="srcSentence">DBTYPE_UI4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">adUnsignedInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src50" class="srcSentence">DBTYPE_I8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src51" class="srcSentence">adBigInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">DBTYPE_UI8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">adUnsignedBigInt</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">DBTYPE_GUID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">adGuid</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">DBTYPE_BYTES</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">adBinary, AdVarBinary, adLongVarBinary</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src58" class="srcSentence">DBTYPE_STR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">adChar, adVarChar, adLongVarChar</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src60" class="srcSentence">DBTYPE_WSTR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src61" class="srcSentence">adWChar, adVarWChar, adLongVarWChar</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src62" class="srcSentence">DBTYPE_NUMERIC</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src63" class="srcSentence">adNumeric</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src64" class="srcSentence">DBTYPE_DBDATE</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src65" class="srcSentence">adDBDate</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src66" class="srcSentence">DBTYPE_DBTIME</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src67" class="srcSentence">adDBTime</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src68" class="srcSentence">DBTYPE_DBTIMESTAMP</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src69" class="srcSentence">adDBTimeStamp</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src70" class="srcSentence">DBTYPE_VARNUMERIC</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src71" class="srcSentence">adVarNumeric</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src72" class="srcSentence">DBTYPE_FILETIME</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src73" class="srcSentence">adFileTime</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src74" class="srcSentence">DBTYPE_ERROR</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src75" class="srcSentence">adError</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src76" class="srcSentence">When the new field is of type decimal (in OLE DB, DBTYPE_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</caps:sentence>
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
---
title: "CommandTypeEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 4b1feb9c-a855-40fe-a906-efe688687e9f
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
# CommandTypeEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4bcbba0bc95b2cb08e67ec1c2657ed0d" id="tgt1" class="tgtSentence">Specifies how a command argument should be interpreted.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a6507705d8879bc26cc9208e057a166b" id="tgt2" class="tgtSentence">It is important to validate user-supplied <parameterReference>CommandString</parameterReference> values to avoid giving application users the opportunity to inject potentially dangerous commands for ADO to execute.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt3" class="tgtSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt4" class="tgtSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt5" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="5008c5add78cafc182fc91be7d54213d" id="tgt6" class="tgtSentence">adCmdUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt7" class="tgtSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a1f91cfd35a756aa04a3a393aa18debf" id="tgt8" class="tgtSentence">Does not specify the command type argument.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1f09f42761002b429e87225a6ec202f2" id="tgt9" class="tgtSentence">adCmdText</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt10" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fc114ad86e918f80fe7508d079d518c7" id="tgt11" class="tgtSentence">Evaluates <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> as a textual definition of a command or stored procedure call.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="b757c4e24b016d51a9023bf2768cc20f" id="tgt12" class="tgtSentence">adCmdTable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt13" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1bb67edec1192526b073d34dbdf1fb00" id="tgt14" class="tgtSentence">Evaluates <legacyBold>CommandText</legacyBold> as a table name whose columns are all returned by an internally generated SQL query.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1ac7a6eeb099cbfb2002c42e1c8e06b3" id="tgt15" class="tgtSentence">adCmdStoredProc</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt16" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5fe4769a7609d74e0035d7c81986cdaf" id="tgt17" class="tgtSentence">Evaluates <legacyBold>CommandText</legacyBold> as a stored procedure name.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="d02148feb77e0ae95782748f7acd2703" id="tgt18" class="tgtSentence">adCmdUnknown</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c9f0f895fb98ab9159f51fd0297e236d" id="tgt19" class="tgtSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt20" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="79831905b504e95a11c21cdea2544fdb" id="tgt21" class="tgtSentence"> Indicates that the type of command in the <legacyBold>CommandText</legacyBold> property is not known.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="35621f36d0b67352a1fd70813c188142" id="tgt22" class="tgtSentence">When the type of command is not known, ADO will make several attempts to interpret the <legacyBold>CommandText</legacyBold>.</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="53b73da6709d16233623d82eb5e414fc" id="tgt23" class="tgtSentence">
                        <legacyBold>CommandText</legacyBold> is interpreted as a textual definition of a command or stored procedure call.</caps:sentence>
                      <caps:sentence sentenceid="2385206a5a7c8a48a1b447956ce964ed" id="tgt24" class="tgtSentence"> This is the same behavior as <legacyBold>adCmdText</legacyBold>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="ecf7db84e091eaf067ef1173e7ec3e47" id="tgt25" class="tgtSentence">
                        <legacyBold>CommandText</legacyBold> is the name of a stored procedure.</caps:sentence>
                      <caps:sentence sentenceid="4f1fed3f150fbd6aa6af7ac776064480" id="tgt26" class="tgtSentence"> This is the same behavior as <legacyBold>adCmdStoredProc</legacyBold>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="cbad86f343bb931465e6c95ba1a85a6c" id="tgt27" class="tgtSentence">
                        <legacyBold>CommandText</legacyBold> is interpreted as the name of a table.</caps:sentence>
                      <caps:sentence sentenceid="5ffec79a91147fb57151e8263cbc8b9f" id="tgt28" class="tgtSentence"> All columns are returned by an internally generated SQL query.</caps:sentence>
                      <caps:sentence sentenceid="35082cf705355d1a44fcc7fe645ed17e" id="tgt29" class="tgtSentence"> This is the same behavior as <legacyBold>adCmdTable</legacyBold>.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="c2aa4772d7e10bc345c3cf9280243d99" id="tgt30" class="tgtSentence">adCmdFile</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f718499c1c8cef6730f9fd03c8125cab" id="tgt31" class="tgtSentence">256</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3efe96996d2ca07b5682c770fcc72c2a" id="tgt32" class="tgtSentence">Evaluates <legacyBold>CommandText</legacyBold> as the file name of a persistently stored <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
                  <caps:sentence sentenceid="c58a29fc1f714f4667a1d0077e84873b" id="tgt33" class="tgtSentence"> Used with <legacyBold>Recordset.</legacyBold><legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> or <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> only.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e6472c5e7d810055e4c217d64f420c12" id="tgt34" class="tgtSentence">adCmdTableDirect</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="10a7cdd970fe135cf4f7bb55c0e3b59f" id="tgt35" class="tgtSentence">512</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6f380cc79d31abb4fc768de826ba89b6" id="tgt36" class="tgtSentence">Evaluates <legacyBold>CommandText</legacyBold> as a table name whose columns are all returned.</caps:sentence>
                  <caps:sentence sentenceid="116d1030da4bfbbca70d238e6942b96e" id="tgt37" class="tgtSentence"> Used with <legacyBold>Recordset.Open</legacyBold> or <legacyBold>Requery</legacyBold> only.</caps:sentence>
                  <caps:sentence sentenceid="77d47b749ba845460936b66fb591a5ea" id="tgt38" class="tgtSentence"> To use the <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek</legacyLink> method, the <legacyBold>Recordset</legacyBold> must be opened with <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="69b12725e1886a9ea83f921a087de76b" id="tgt39" class="tgtSentence">This value cannot be combined with the <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> value <legacyBold>adAsyncExecute</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt40" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt41" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt42" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4d509748ca0851c06ae5491400df71fc" id="tgt43" class="tgtSentence">AdoEnums.CommandType.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="444f266db6464cb38e5ab27d75425ee8" id="tgt44" class="tgtSentence">AdoEnums.CommandType.TEXT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a61ccff92866e6f8b78292a74d1dcc95" id="tgt45" class="tgtSentence">AdoEnums.CommandType.TABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="41827704b7fab13ea93b9c6d6927411d" id="tgt46" class="tgtSentence">AdoEnums.CommandType.STOREDPROC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d718f8af79dc6a6d3c0e9e9c383488a0" id="tgt47" class="tgtSentence">AdoEnums.CommandType.UNKNOWN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="29643b0a7374bf5f9a6b6b8abe9fad27" id="tgt48" class="tgtSentence">AdoEnums.CommandType.FILE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="95255820495f3d539bf3bf9993a792c0" id="tgt49" class="tgtSentence">AdoEnums.CommandType.TABLEDIRECT</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt50" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType Property</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies how a command argument should be interpreted.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">It is important to validate user-supplied <parameterReference>CommandString</parameterReference> values to avoid giving application users the opportunity to inject potentially dangerous commands for ADO to execute.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src6" class="srcSentence">adCmdUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Does not specify the command type argument.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src9" class="srcSentence">adCmdText</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Evaluates <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> as a textual definition of a command or stored procedure call.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src12" class="srcSentence">adCmdTable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Evaluates <legacyBold>CommandText</legacyBold> as a table name whose columns are all returned by an internally generated SQL query.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src15" class="srcSentence">adCmdStoredProc</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Evaluates <legacyBold>CommandText</legacyBold> as a stored procedure name.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src18" class="srcSentence">adCmdUnknown</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src21" class="srcSentence"> Indicates that the type of command in the <legacyBold>CommandText</legacyBold> property is not known.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src22" class="srcSentence">When the type of command is not known, ADO will make several attempts to interpret the <legacyBold>CommandText</legacyBold>.</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src23" class="srcSentence">
                        <legacyBold>CommandText</legacyBold> is interpreted as a textual definition of a command or stored procedure call.</caps:sentence>
                      <caps:sentence id="src24" class="srcSentence"> This is the same behavior as <legacyBold>adCmdText</legacyBold>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src25" class="srcSentence">
                        <legacyBold>CommandText</legacyBold> is the name of a stored procedure.</caps:sentence>
                      <caps:sentence id="src26" class="srcSentence"> This is the same behavior as <legacyBold>adCmdStoredProc</legacyBold>.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src27" class="srcSentence">
                        <legacyBold>CommandText</legacyBold> is interpreted as the name of a table.</caps:sentence>
                      <caps:sentence id="src28" class="srcSentence"> All columns are returned by an internally generated SQL query.</caps:sentence>
                      <caps:sentence id="src29" class="srcSentence"> This is the same behavior as <legacyBold>adCmdTable</legacyBold>.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src30" class="srcSentence">adCmdFile</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">256</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Evaluates <legacyBold>CommandText</legacyBold> as the file name of a persistently stored <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
                  <caps:sentence id="src33" class="srcSentence"> Used with <legacyBold>Recordset.</legacyBold><legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> or <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> only.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src34" class="srcSentence">adCmdTableDirect</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">512</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">Evaluates <legacyBold>CommandText</legacyBold> as a table name whose columns are all returned.</caps:sentence>
                  <caps:sentence id="src37" class="srcSentence"> Used with <legacyBold>Recordset.Open</legacyBold> or <legacyBold>Requery</legacyBold> only.</caps:sentence>
                  <caps:sentence id="src38" class="srcSentence"> To use the <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek</legacyLink> method, the <legacyBold>Recordset</legacyBold> must be opened with <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src39" class="srcSentence">This value cannot be combined with the <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> value <legacyBold>adAsyncExecute</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src40" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src41" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">AdoEnums.CommandType.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">AdoEnums.CommandType.TEXT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">AdoEnums.CommandType.TABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">AdoEnums.CommandType.STOREDPROC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">AdoEnums.CommandType.UNKNOWN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">AdoEnums.CommandType.FILE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">AdoEnums.CommandType.TABLEDIRECT</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src50" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType Property</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
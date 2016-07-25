---
title: "CreateRecordset Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6840b1e5-c04d-4d3e-9dcc-42128c83492f
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
# CreateRecordset Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a7c148a85078bacd815d5aa2d9608ebe" id="tgt1" class="tgtSentence">Creates an empty, disconnected <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>object</parameterReference>.<legacyBold>CreateRecordset(</legacyBold><parameterReference>ColumnInfos</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7dac69667e814ea09c728e6d30f5074d" id="tgt6" class="tgtSentence"> <legacyItalic>Object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="01c89f2d936f2d2313dd54927e6caed1" id="tgt7" class="tgtSentence">An object variable that represents an <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> or <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="862413e908d529d3ae86ab2449573ba3" id="tgt8" class="tgtSentence"> <legacyItalic>ColumnsInfos</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="207ea0e8bf2fdbe652a37eb42b051cb6" id="tgt9" class="tgtSentence">A <legacyBold>Variant</legacyBold> array of attributes that defines each column in the <legacyBold>Recordset</legacyBold> created.</caps:sentence>
                <caps:sentence sentenceid="1abdfa7f66e6c07ad8f04d1ad365bc67" id="tgt10" class="tgtSentence"> Each column definition contains an array of four required attributes and one optional attribute.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d2eb444e35c0a71f0a85df8194acb5b6" id="tgt11" class="tgtSentence">Attribute</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt12" class="tgtSentence">Description</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt13" class="tgtSentence">Name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8d3be3de360d24ed9f22a3f45fafe252" id="tgt14" class="tgtSentence">Name of the column header.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt15" class="tgtSentence">Type</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9ea3f49e0a496956a9c6e55a64c895c6" id="tgt16" class="tgtSentence">Integer of the data type.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f7bd60b75b29d79b660a2859395c1a24" id="tgt17" class="tgtSentence">Size</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d24aae51cd4ba02a0efca44177f7904f" id="tgt18" class="tgtSentence">Integer of the width in characters, regardless of data type.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ea2245bb2401e71ec547bc838fca69cd" id="tgt19" class="tgtSentence">Nullability</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="29ee814631f7c3f5b32a2d58c3921d5f" id="tgt20" class="tgtSentence">Boolean value.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8708eacd38e28e928324513d4b1c967a" id="tgt21" class="tgtSentence">Scale (Optional)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4651d8c143c813ed073ee9987df5b891" id="tgt22" class="tgtSentence">This optional attribute defines the scale for numeric fields.</caps:sentence>
                        <caps:sentence sentenceid="fec0e47c0547d141695d56f4eb9d3e3d" id="tgt23" class="tgtSentence"> If this value is not specified, numeric values will be truncated to a scale of three.</caps:sentence>
                        <caps:sentence sentenceid="cb0da34d0b8aa7e6c724231fe16958de" id="tgt24" class="tgtSentence"> Precision is not affected, but the number of digits following the decimal point will be truncated to three.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="fed67ca1cbd8de00fa40159c713d3ff5" id="tgt25" class="tgtSentence">The set of column arrays is then grouped into an array, which defines the <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="aa613a0dc8275c79d38f9e7c6e45189e" id="tgt26" class="tgtSentence">The server-side business object can populate the resulting <legacyBold>Recordset</legacyBold> with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1bbebbc5ed0a57ce03e9f92ec16c3d4f" id="tgt27" class="tgtSentence">The following table lists the <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> values supported by the <legacyBold>CreateRecordset</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="d02c2dbf4dfaa4d592e87d62069622c9" id="tgt28" class="tgtSentence"> The number listed is the reference number used to define fields.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="270e4bb3734133326cc536a33e8d8c35" id="tgt29" class="tgtSentence">Each of the data types is either fixed length or variable length.</caps:sentence>
            <caps:sentence sentenceid="bd713538a9b9410ef84a10c253cfda18" id="tgt30" class="tgtSentence"> Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</caps:sentence>
            <caps:sentence sentenceid="593066e22e3e48ab974765a3b9317255" id="tgt31" class="tgtSentence"> Variable-length data types allow a size from 1 to 32767.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="01579ab699be4897ff2f7d3ffc8d32c0" id="tgt32" class="tgtSentence">For some of the variable data types, the type can be coerced to the type noted in the Substitution column.</caps:sentence>
            <caps:sentence sentenceid="d1eb1e1ecea4952f2e3ddc6a68caf048" id="tgt33" class="tgtSentence"> You will not see the substitutions until after the <legacyBold>Recordset</legacyBold> is created and filled.</caps:sentence>
            <caps:sentence sentenceid="95130d70f3b76d74d7cbad45982c5ce1" id="tgt34" class="tgtSentence"> Then you can check for the actual data type, if necessary.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2fa47f7c65fec19cc163b195725e3844" id="tgt35" class="tgtSentence">Length</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt36" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b1bc248a7ff2b2e95569f56de68615df" id="tgt37" class="tgtSentence">Number</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1bb0cf38d2ef3662d97f6a4ece67bad2" id="tgt38" class="tgtSentence">Substitution</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt39" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="85d11b42b09e2a64eb79ec906f814369" id="tgt40" class="tgtSentence">adTinyInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c74d97b01eae257e44aa9d5bade97baf" id="tgt41" class="tgtSentence">16</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt42" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="acd69f55330d1a293418dc7b32cbe6e4" id="tgt43" class="tgtSentence">adSmallInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt44" class="tgtSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt45" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e106331f00ed23951a7dc9af8cd06713" id="tgt46" class="tgtSentence">adInteger</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt47" class="tgtSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt48" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="7fd6cbae79d8c56e2c73513d41af2ba7" id="tgt49" class="tgtSentence">adBigInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98f13708210194c475687be6106a3b84" id="tgt50" class="tgtSentence">20</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt51" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="989f37e5e05fa5d68baa0dd99b5424b9" id="tgt52" class="tgtSentence">adUnsignedTinyInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="70efdf2ec9b086079795c442636b55fb" id="tgt53" class="tgtSentence">17</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt54" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="74a795a334418d7a5667aa2034211e53" id="tgt55" class="tgtSentence">adUnsignedSmallInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f4922f45568161a8cdf4ad2299f6d23" id="tgt56" class="tgtSentence">18</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt57" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="16a77b22ef1a3830fe42b79fa1b6f6bb" id="tgt58" class="tgtSentence">adUnsignedInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1f0e3dad99908345f7439f8ffabdffc4" id="tgt59" class="tgtSentence">19</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt60" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="22210ae9448d5f570738afade201f348" id="tgt61" class="tgtSentence">adUnsignedBigInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c59dc048e8850243be8079a5c74d079" id="tgt62" class="tgtSentence">21</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt63" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9812bbda5facc1b577b5c856d206c2ed" id="tgt64" class="tgtSentence">adSingle</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt65" class="tgtSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt66" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3586e7d98462e80c73b1761d62068c67" id="tgt67" class="tgtSentence">adDouble</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4da3b7fbbce2345d7772b0674a318d5" id="tgt68" class="tgtSentence">5</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt69" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="0a13bde8511b0925c309bffab8e44d8d" id="tgt70" class="tgtSentence">adCurrency</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1679091c5a880faf6fb5e6087eb1b2dc" id="tgt71" class="tgtSentence">6</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt72" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="baaa708f94b121de5139624d4fd370cd" id="tgt73" class="tgtSentence">adDecimal</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aab3238922bcc25a6f606eb525ffdc56" id="tgt74" class="tgtSentence">14</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt75" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="05d4cf9c8094b00fde5bfa5407085a6e" id="tgt76" class="tgtSentence">adNumeric</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1afa34a7f984eeabdbb0a7d494132ee5" id="tgt77" class="tgtSentence">131</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt78" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="37d52c4baad3447a789a5339c3378dbc" id="tgt79" class="tgtSentence">adBoolean</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6512bd43d9caa6e02c990b0a82652dca" id="tgt80" class="tgtSentence">11</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt81" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="87792d622adc7a98d79ba5c4651a83cc" id="tgt82" class="tgtSentence">adError</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3d9446802a44259755d38e6d163e820" id="tgt83" class="tgtSentence">10</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt84" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="fcafaddea899221c3d28f9fa5f19902c" id="tgt85" class="tgtSentence">adGuid</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32bb90e8976aab5298d5da10fe66f21d" id="tgt86" class="tgtSentence">72</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt87" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a4691ca345fe64053b75f6a47fbe59ae" id="tgt88" class="tgtSentence">adDate</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f14e45fceea167a5a36dedd4bea2543" id="tgt89" class="tgtSentence">7</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt90" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="6fac38c34de456eb0aaa8a475ba3aae2" id="tgt91" class="tgtSentence">adDBDate</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9fc3d7152ba9336a670e36d0ed79bc43" id="tgt92" class="tgtSentence">133</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt93" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5eb84d814fa77850ebcb992b74227ee6" id="tgt94" class="tgtSentence">adDBTime</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="02522a2b2726fb0a03bb19f2d8d9524d" id="tgt95" class="tgtSentence">134</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cec315e3d0975e5cc2811d5d8725f149" id="tgt96" class="tgtSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="c69c01b6333a51fc8588b19feace0cfe" id="tgt97" class="tgtSentence">adDBTimestamp</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7f1de29e6da19d22b51c68001e7e0e54" id="tgt98" class="tgtSentence">135</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f14e45fceea167a5a36dedd4bea2543" id="tgt99" class="tgtSentence">7</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt100" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="7f745527b6485673f9e42dd4fe054fb1" id="tgt101" class="tgtSentence">adBSTR</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c9f0f895fb98ab9159f51fd0297e236d" id="tgt102" class="tgtSentence">8</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9b8619251a19057cff70779273e95aa6" id="tgt103" class="tgtSentence">130</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt104" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="4ab5d02d6d5fa47015df49dca8e37e64" id="tgt105" class="tgtSentence">adChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1f491a404d6854880943e5c3cd9ca25" id="tgt106" class="tgtSentence">129</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3644a684f98ea8fe223c713b77189a77" id="tgt107" class="tgtSentence">200</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt108" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="7dd6bf1d1df5e28da053bfbca442d30c" id="tgt109" class="tgtSentence">adVarChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3644a684f98ea8fe223c713b77189a77" id="tgt110" class="tgtSentence">200</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt111" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="1106c550f9e7a8f03ade6efc13a0d0bc" id="tgt112" class="tgtSentence">adLongVarChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="757b505cfd34c64c85ca5b5690ee5293" id="tgt113" class="tgtSentence">201</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3644a684f98ea8fe223c713b77189a77" id="tgt114" class="tgtSentence">200</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt115" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="31cffe7361c8c1218dd4dc870415854d" id="tgt116" class="tgtSentence">adWChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9b8619251a19057cff70779273e95aa6" id="tgt117" class="tgtSentence">130</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt118" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt119" class="tgtSentence">adVarWChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="854d6fae5ee42911677c739ee1734486" id="tgt120" class="tgtSentence">202</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9b8619251a19057cff70779273e95aa6" id="tgt121" class="tgtSentence">130</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt122" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="f942abab3e464218a8ae29cba5e0298b" id="tgt123" class="tgtSentence">adLongVarWChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e2c0be24560d78c5e599c2a9c9d0bbd2" id="tgt124" class="tgtSentence">203</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9b8619251a19057cff70779273e95aa6" id="tgt125" class="tgtSentence">130</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt126" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a27e3ed03d8955ded2458feaeb8910d4" id="tgt127" class="tgtSentence">adBinary</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="76dc611d6ebaafc66cc0879c71b5db5c" id="tgt128" class="tgtSentence">128</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt129" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9cc4c6da9ab426bb85508670e8edb76d" id="tgt130" class="tgtSentence">adVarBinary</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="274ad4786c3abca69fa097b85867d9a4" id="tgt131" class="tgtSentence">204</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e04aa5104d082e4a51d241391941ba26" id="tgt132" class="tgtSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a5f319a1b95636a165fab0c05b0d1ad6" id="tgt133" class="tgtSentence">adLongVarBinary</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eae27d77ca20db309e056e3d2dcd7d69" id="tgt134" class="tgtSentence">205</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="274ad4786c3abca69fa097b85867d9a4" id="tgt135" class="tgtSentence">204</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt136" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2de8fd02-0f49-4d47-8bd3-397726d1c644">Visual Basic Example</link>
        <link xlink:href="cce0d8b5-e87b-4f7b-a8a0-37d5025a1f5d">VBScript Example</link>
        <link xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Creates an empty, disconnected <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>object</parameterReference>.<legacyBold>CreateRecordset(</legacyBold><parameterReference>ColumnInfos</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>Object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An object variable that represents an <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> or <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>ColumnsInfos</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">A <legacyBold>Variant</legacyBold> array of attributes that defines each column in the <legacyBold>Recordset</legacyBold> created.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> Each column definition contains an array of four required attributes and one optional attribute.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src11" class="srcSentence">Attribute</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src12" class="srcSentence">Description</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">Name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">Name of the column header.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">Type</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">Integer of the data type.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">Size</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">Integer of the width in characters, regardless of data type.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">Nullability</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">Boolean value.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">Scale (Optional)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">This optional attribute defines the scale for numeric fields.</caps:sentence>
                        <caps:sentence id="src23" class="srcSentence"> If this value is not specified, numeric values will be truncated to a scale of three.</caps:sentence>
                        <caps:sentence id="src24" class="srcSentence"> Precision is not affected, but the number of digits following the decimal point will be truncated to three.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src25" class="srcSentence">The set of column arrays is then grouped into an array, which defines the <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src26" class="srcSentence">The server-side business object can populate the resulting <legacyBold>Recordset</legacyBold> with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">The following table lists the <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> values supported by the <legacyBold>CreateRecordset</legacyBold> method.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> The number listed is the reference number used to define fields.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">Each of the data types is either fixed length or variable length.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> Variable-length data types allow a size from 1 to 32767.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">For some of the variable data types, the type can be coerced to the type noted in the Substitution column.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> You will not see the substitutions until after the <legacyBold>Recordset</legacyBold> is created and filled.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> Then you can check for the actual data type, if necessary.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Length</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Number</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Substitution</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src40" class="srcSentence">adTinyInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">16</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src43" class="srcSentence">adSmallInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src46" class="srcSentence">adInteger</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src49" class="srcSentence">adBigInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">20</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src52" class="srcSentence">adUnsignedTinyInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">17</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src55" class="srcSentence">adUnsignedSmallInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">18</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src58" class="srcSentence">adUnsignedInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">19</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src61" class="srcSentence">adUnsignedBigInt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">21</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src64" class="srcSentence">adSingle</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src67" class="srcSentence">adDouble</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">5</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src70" class="srcSentence">adCurrency</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">6</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src73" class="srcSentence">adDecimal</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">14</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src76" class="srcSentence">adNumeric</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">131</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src79" class="srcSentence">adBoolean</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">11</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src82" class="srcSentence">adError</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">10</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src85" class="srcSentence">adGuid</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">72</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src88" class="srcSentence">adDate</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">7</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src91" class="srcSentence">adDBDate</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">133</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src94" class="srcSentence">adDBTime</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">134</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">Fixed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src97" class="srcSentence">adDBTimestamp</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">135</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">7</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src101" class="srcSentence">adBSTR</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">8</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src103" class="srcSentence">130</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src105" class="srcSentence">adChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">129</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">200</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src109" class="srcSentence">adVarChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">200</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src112" class="srcSentence">adLongVarChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">201</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">200</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src116" class="srcSentence">adWChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">130</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src119" class="srcSentence">adVarWChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">202</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">130</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src122" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src123" class="srcSentence">adLongVarWChar</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">203</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">130</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src127" class="srcSentence">adBinary</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">128</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src130" class="srcSentence">adVarBinary</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src131" class="srcSentence">204</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">Variable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src133" class="srcSentence">adLongVarBinary</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">205</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">204</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src136" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2de8fd02-0f49-4d47-8bd3-397726d1c644">Visual Basic Example</link>
        <link xlink:href="cce0d8b5-e87b-4f7b-a8a0-37d5025a1f5d">VBScript Example</link>
        <link xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
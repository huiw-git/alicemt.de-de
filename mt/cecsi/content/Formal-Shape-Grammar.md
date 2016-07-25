---
title: "Formal Shape Grammar"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea691475-0f03-4abe-a785-b77e77712d1d
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
# Formal Shape Grammar
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4c982699c36401f56d7aad82bc8efab1" id="tgt1" class="tgtSentence">This is the formal grammar for creating any shape command:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="1e19212c8d6e681010f9406892812f05" id="tgt2" class="tgtSentence">Required grammatical terms are text strings delimited by angle brackets ("&lt;&gt;").</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5f57cd157b026ab0443baeb491f78072" id="tgt3" class="tgtSentence">Optional terms are delimited by square brackets ("[ ]").</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="7524e79d90a9b257eb80fe0a33feb01e" id="tgt4" class="tgtSentence">Alternatives are indicated by a virgule ("|").</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5026d4a96a60fae4dca6f86ae4897e7d" id="tgt5" class="tgtSentence">Repeating alternatives are indicated by an ellipsis ("...").</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="96f73508852b7ef632d63252077e3a64" id="tgt6" class="tgtSentence">             <legacyItalic>Alpha</legacyItalic> indicates a string of alphabetical letters.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="da60b8b991441b1779cd31ac5eb67460" id="tgt7" class="tgtSentence">             <legacyItalic>Digit</legacyItalic> indicates a string of numbers.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ef00dbc4e6e0fd99ac8d90dbb9abef72" id="tgt8" class="tgtSentence">             <legacyItalic>Unicode-digit</legacyItalic> indicates a string of unicode digits.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="b7fb76107fed2bdf161388b25f6da4c6" id="tgt9" class="tgtSentence">All other terms are literals.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b4dad0fe5fbef2c0e24d9db1cc69e5a2" id="tgt10" class="tgtSentence">Term</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="30618b3b44fa316257d07e387759fae5" id="tgt11" class="tgtSentence">Definition</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="fcea8459a47545828394a63175d19d4c" id="tgt12" class="tgtSentence">&lt;shape-command&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d6264d44887c82a0e6a83f01f68ef249" id="tgt13" class="tgtSentence">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0b07eed303fb034e89c40c2f31489d34" id="tgt14" class="tgtSentence">&lt;table-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2ae1eaa0be253484719ae5fa3e4ae1c1" id="tgt15" class="tgtSentence">{&lt;provider-command-text&gt;} |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="7550cf088e9a3dfd64993e3c8cc1b58e" id="tgt16" class="tgtSentence">(&lt;shape-command&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="28a403a1c64846ed754ff3956694db03" id="tgt17" class="tgtSentence">TABLE &lt;quoted-name&gt; |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="e004d66a728ca647a6e869a58840866a" id="tgt18" class="tgtSentence">&lt;quoted-name&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c000c0b5e3b0e772ad85ff41e699c64a" id="tgt19" class="tgtSentence">&lt;shape-action&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="62d85fa7648d19b69bf796e32e61e12f" id="tgt20" class="tgtSentence">APPEND &lt;aliased-field-list&gt; | </caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="0dba65c47d4d8c629141e02732244556" id="tgt21" class="tgtSentence">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f335439fca5fc8d8da541f3d46a61093" id="tgt22" class="tgtSentence">&lt;aliased-field-list&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fb08d472b908d3ab9968b442149a039d" id="tgt23" class="tgtSentence">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="12ccaafca6eae48490313dcbca4f5f2d" id="tgt24" class="tgtSentence">&lt;aliased-field&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="84447e4f52e0d5db8f8e562d3c9025b3" id="tgt25" class="tgtSentence">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f661ebd8ec7f209b8210b65c79242430" id="tgt26" class="tgtSentence">&lt;field-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="34465e7e55e4167362e7bd09f8071b15" id="tgt27" class="tgtSentence">(&lt;relation-exp&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="436ac949d648b4227e8a5faf281bb182" id="tgt28" class="tgtSentence">&lt;calculated-exp&gt; |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="ec8460dda61aa6ba082d37a1823955e1" id="tgt29" class="tgtSentence">&lt;aggregate-exp&gt; |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="468015ac64f4a1a8605411d5a83d2e74" id="tgt30" class="tgtSentence">&lt;new-exp&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="dcfaff77640340400df907e17564c601" id="tgt31" class="tgtSentence">&lt;relation_exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9b863d75f62cd0eff5852f82c5bf83e9" id="tgt32" class="tgtSentence">&lt;table-exp&gt; [[AS] &lt;alias&gt;] </caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="7d560aa59d8c6d725e1be6bb4df3f229" id="tgt33" class="tgtSentence">   RELATE &lt;relation-cond-list&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="baedcf31119c73dfaaed05bec1d18b4e" id="tgt34" class="tgtSentence">&lt;relation-cond-list&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ca21104fd4ead5a5513210452b703cb1" id="tgt35" class="tgtSentence">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="053e816845bcc325c5fcbcec505bcfc4" id="tgt36" class="tgtSentence">&lt;relation-cond&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="62f5eab969c2193ca987644122e52594" id="tgt37" class="tgtSentence">&lt;field-name&gt; TO &lt;child-ref&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2a8425983cc1b99446a8b66b7ea0abf5" id="tgt38" class="tgtSentence">&lt;child-ref&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="372ab3fcf3cc5a256ba0ab627c5fa76e" id="tgt39" class="tgtSentence">&lt;field-name&gt; | </caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="eda61d2b51ea1eb5dce9e2edda0fb1d9" id="tgt40" class="tgtSentence">PARAMETER &lt;param-ref&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f443efaa78e4cbf63eed14d1587b087a" id="tgt41" class="tgtSentence">&lt;param-ref&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d80b5def5ed1be6e26d91c2709f14170" id="tgt42" class="tgtSentence">&lt;number&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="dcbf6815803e0f565ff193d11373e445" id="tgt43" class="tgtSentence">&lt;field-list&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fd0f23f6e10b5ea85e013dc58c67e02e" id="tgt44" class="tgtSentence">&lt;field-name&gt; [, &lt;field-name&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9b90ddae5e5554475d5915825af69652" id="tgt45" class="tgtSentence">&lt;aggregate-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8cc4b7081c821c600cf351b0a6886fd6" id="tgt46" class="tgtSentence">SUM(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="964e78fd2747ef9a38c523f211a1ee92" id="tgt47" class="tgtSentence">AVG(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="435116e374b08e62158228da13413dec" id="tgt48" class="tgtSentence">MIN(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="ec8d97e53d85e0a926adb4aff1a9dccf" id="tgt49" class="tgtSentence">MAX(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="dc5966b24a7f8af289e8c3c1f9742e6f" id="tgt50" class="tgtSentence">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="f8d5ac164b40d3042474fee08518eed7" id="tgt51" class="tgtSentence">STDEV(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="f59eebe4b5a0e40681b6b04bf8ef21f2" id="tgt52" class="tgtSentence">ANY(&lt;qualified-field-name&gt;) </caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3a29925fa14b06e4c961f9a9016386a3" id="tgt53" class="tgtSentence">&lt;calculated-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e8f82603eca7220715e324d56185ec54" id="tgt54" class="tgtSentence">CALC(&lt;expression&gt;)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="788be1091fc08436fe187a1d0b6b14ec" id="tgt55" class="tgtSentence">&lt;qualified-field-name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d23f48c77ba7954793aaafd656c9ac4" id="tgt56" class="tgtSentence">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e3bb5a736f6767bdf66118380bef947d" id="tgt57" class="tgtSentence">&lt;alias&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e004d66a728ca647a6e869a58840866a" id="tgt58" class="tgtSentence">&lt;quoted-name&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7b4b75f3878240e6e8a8fbbfe087aaac" id="tgt59" class="tgtSentence">&lt;field-name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5ff29b4abd35827fd9b06ff2fe2c8501" id="tgt60" class="tgtSentence">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e004d66a728ca647a6e869a58840866a" id="tgt61" class="tgtSentence">&lt;quoted-name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2a146265dd3975167f4bbc1a5d9e7f12" id="tgt62" class="tgtSentence">"&lt;string&gt;" |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="ec0c9e8a4d29be6556daf03d20858992" id="tgt63" class="tgtSentence">'&lt;string&gt;' |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="8bd8dee1922230ce31d8a38300acd10a" id="tgt64" class="tgtSentence">[&lt;string&gt;] |</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="8a11bc632ea32a57b3e3693c7987c420" id="tgt65" class="tgtSentence">&lt;name&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="16c0b67169c8ac95c1ab35f3fb9145b0" id="tgt66" class="tgtSentence">&lt;qualified-name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b46becc1edcf9efa4e0de9d4b1db6b53" id="tgt67" class="tgtSentence">alias[.alias...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8a11bc632ea32a57b3e3693c7987c420" id="tgt68" class="tgtSentence">&lt;name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7f8d90119a1fcd674dc046fddb749044" id="tgt69" class="tgtSentence">alpha [ alpha | digit | _ | # | : | ...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d80b5def5ed1be6e26d91c2709f14170" id="tgt70" class="tgtSentence">&lt;number&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="971265b0b98d4ccd3e5c248195174e90" id="tgt71" class="tgtSentence">digit [digit...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="468015ac64f4a1a8605411d5a83d2e74" id="tgt72" class="tgtSentence">&lt;new-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3a688ebfde1d0dc6a7a1488820c0e338" id="tgt73" class="tgtSentence">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="fa0bfbfed2929c5c071e29bb9f88fb97" id="tgt74" class="tgtSentence">&lt;field-type&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1a31ed64875a0dc79275105ce5065900" id="tgt75" class="tgtSentence">An OLE DB or ADO data type.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="98c455a79ddfebb79781bff588e7b37e" id="tgt76" class="tgtSentence">&lt;string&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9ee118822fa82a3d192ccc9738e7577a" id="tgt77" class="tgtSentence">unicode-char [unicode-char...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="41256fb142f22f4bfc3f76fe922f5535" id="tgt78" class="tgtSentence">&lt;expression&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3936ed3c9684090e91ea03d9c549a1be" id="tgt79" class="tgtSentence">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</link>
        <link xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">Data Shaping Summary</link>
        <link xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</link>
        <link xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">Shape APPEND Clause</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
        <link xlink:href="3fdfead2-b5ab-4163-9b1d-3d2143a5db8c">Shape COMPUTE Clause</link>
        <link xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications Functions</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This is the formal grammar for creating any shape command:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">Required grammatical terms are text strings delimited by angle brackets ("&lt;&gt;").</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Optional terms are delimited by square brackets ("[ ]").</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Alternatives are indicated by a virgule ("|").</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Repeating alternatives are indicated by an ellipsis ("...").</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyItalic>Alpha</legacyItalic> indicates a string of alphabetical letters.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyItalic>Digit</legacyItalic> indicates a string of numbers.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyItalic>Unicode-digit</legacyItalic> indicates a string of unicode digits.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src9" class="srcSentence">All other terms are literals.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Term</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Definition</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">&lt;shape-command&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">&lt;table-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">{&lt;provider-command-text&gt;} |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src16" class="srcSentence">(&lt;shape-command&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src17" class="srcSentence">TABLE &lt;quoted-name&gt; |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src18" class="srcSentence">&lt;quoted-name&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">&lt;shape-action&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">APPEND &lt;aliased-field-list&gt; | </caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src21" class="srcSentence">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">&lt;aliased-field-list&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">&lt;aliased-field&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">&lt;field-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">(&lt;relation-exp&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src28" class="srcSentence">&lt;calculated-exp&gt; |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src29" class="srcSentence">&lt;aggregate-exp&gt; |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src30" class="srcSentence">&lt;new-exp&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">&lt;relation_exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">&lt;table-exp&gt; [[AS] &lt;alias&gt;] </caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src33" class="srcSentence">   RELATE &lt;relation-cond-list&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">&lt;relation-cond-list&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">&lt;relation-cond&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">&lt;field-name&gt; TO &lt;child-ref&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">&lt;child-ref&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">&lt;field-name&gt; | </caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src40" class="srcSentence">PARAMETER &lt;param-ref&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">&lt;param-ref&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">&lt;number&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">&lt;field-list&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src44" class="srcSentence">&lt;field-name&gt; [, &lt;field-name&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">&lt;aggregate-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">SUM(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src47" class="srcSentence">AVG(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src48" class="srcSentence">MIN(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src49" class="srcSentence">MAX(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src50" class="srcSentence">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src51" class="srcSentence">STDEV(&lt;qualified-field-name&gt;) |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src52" class="srcSentence">ANY(&lt;qualified-field-name&gt;) </caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">&lt;calculated-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">CALC(&lt;expression&gt;)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">&lt;qualified-field-name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">&lt;alias&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src58" class="srcSentence">&lt;quoted-name&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">&lt;field-name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src60" class="srcSentence">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src61" class="srcSentence">&lt;quoted-name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src62" class="srcSentence">"&lt;string&gt;" |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src63" class="srcSentence">'&lt;string&gt;' |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src64" class="srcSentence">[&lt;string&gt;] |</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src65" class="srcSentence">&lt;name&gt;</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src66" class="srcSentence">&lt;qualified-name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src67" class="srcSentence">alias[.alias...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src68" class="srcSentence">&lt;name&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src69" class="srcSentence">alpha [ alpha | digit | _ | # | : | ...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src70" class="srcSentence">&lt;number&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src71" class="srcSentence">digit [digit...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src72" class="srcSentence">&lt;new-exp&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src73" class="srcSentence">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src74" class="srcSentence">&lt;field-type&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src75" class="srcSentence">An OLE DB or ADO data type.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src76" class="srcSentence">&lt;string&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src77" class="srcSentence">unicode-char [unicode-char...]</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src78" class="srcSentence">&lt;expression&gt;</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src79" class="srcSentence">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</link>
        <link xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">Data Shaping Summary</link>
        <link xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</link>
        <link xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">Shape APPEND Clause</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
        <link xlink:href="3fdfead2-b5ab-4163-9b1d-3d2143a5db8c">Shape COMPUTE Clause</link>
        <link xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications Functions</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
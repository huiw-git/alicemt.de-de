---
title: "DataTypeEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 2c57eca6-9336-4b06-ba10-9fef5926b1d0
caps.latest.revision: 13
caps.handback.revision: 13
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
# DataTypeEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bf28d0c1ce4e687ffb2c6bd7ab46d295" id="tgt1" class="tgtSentence">Specifies the data type of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink>, <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink>, or <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="4bd3a5291ede7f14d844cf82cb636c07" id="tgt2" class="tgtSentence"> The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</caps:sentence>
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
                    <caps:sentence sentenceid="a2bb81657b574221195a4776115173ca" id="tgt6" class="tgtSentence">AdArray</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f41b03f46687b6430a40b0d6624a472f" id="tgt7" class="tgtSentence">0x2000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="acf37793ba13953d6ec7ed563e614ecd" id="tgt8" class="tgtSentence">A flag value, always combined with another data type constant, that indicates an array of the other data type.</caps:sentence>
                  <caps:sentence sentenceid="b24ec5f7e1eb39e9892fe6700cea4980" id="tgt9" class="tgtSentence"> Does not apply to ADOX.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9ff3d0efe061e2450271af2131d97142" id="tgt10" class="tgtSentence">
                    <legacyBold>adBigInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="98f13708210194c475687be6106a3b84" id="tgt11" class="tgtSentence">20</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e1b1e84604f7c1fdeb9f31269ea3121f" id="tgt12" class="tgtSentence">Indicates an eight-byte signed integer (DBTYPE_I8).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="951a876dd3c53e625733c01b7c429be4" id="tgt13" class="tgtSentence">
                    <legacyBold>adBinary</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="76dc611d6ebaafc66cc0879c71b5db5c" id="tgt14" class="tgtSentence">128</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="920a3cc556b0a0a72bf3908509a76ed3" id="tgt15" class="tgtSentence">Indicates a binary value (DBTYPE_BYTES).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="40a4b8196adbcddb0dc0122b7732df17" id="tgt16" class="tgtSentence">
                    <legacyBold>adBoolean</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6512bd43d9caa6e02c990b0a82652dca" id="tgt17" class="tgtSentence">11</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="54153a462d8ae96bf04c7cb7192ca015" id="tgt18" class="tgtSentence">Indicates a <languageKeyword>Boolean</languageKeyword> value (DBTYPE_BOOL).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="242c3f63a4cde02d8145b3a435ffa44b" id="tgt19" class="tgtSentence">
                    <legacyBold>adBSTR</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c9f0f895fb98ab9159f51fd0297e236d" id="tgt20" class="tgtSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e8efc9845e8a11346eda7fb64f7a61ed" id="tgt21" class="tgtSentence">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="86daceb810da3c6c0924e64af29f318f" id="tgt22" class="tgtSentence">
                    <legacyBold>adChapter</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="42a0e188f5033bc65bf8d78622277c4e" id="tgt23" class="tgtSentence">136</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fb65cc9e32e2f148ea6fdc7799112648" id="tgt24" class="tgtSentence">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="783c4b53e06ec593660065e5173d1589" id="tgt25" class="tgtSentence">
                    <legacyBold>adChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d1f491a404d6854880943e5c3cd9ca25" id="tgt26" class="tgtSentence">129</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="339d4400d9617070b7d710eade738a07" id="tgt27" class="tgtSentence">Indicates a string value (DBTYPE_STR).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="57e47b7876b2b90be6f834d9784546e0" id="tgt28" class="tgtSentence">
                    <legacyBold>adCurrency</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1679091c5a880faf6fb5e6087eb1b2dc" id="tgt29" class="tgtSentence">6</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4a8cabdb300b8317b6b1f242ec10cca3" id="tgt30" class="tgtSentence">Indicates a currency value (DBTYPE_CY).</caps:sentence>
                  <caps:sentence sentenceid="e4c4270af5689cdafd0b04f320068640" id="tgt31" class="tgtSentence"> Currency is a fixed-point number with four digits to the right of the decimal point.</caps:sentence>
                  <caps:sentence sentenceid="0a2ac0b9fc5f5e39e26150970b1266f9" id="tgt32" class="tgtSentence"> It is stored in an eight-byte signed integer scaled by 10,000.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="969c5f8d0607c3059331949ecf5cfd98" id="tgt33" class="tgtSentence">
                    <legacyBold>adDate</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8f14e45fceea167a5a36dedd4bea2543" id="tgt34" class="tgtSentence">7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ee07315c1c11f35f86cb7125aefa3843" id="tgt35" class="tgtSentence">Indicates a date value (DBTYPE_DATE).</caps:sentence>
                  <caps:sentence sentenceid="0aba67e0a1b9379d1776d45a02991cf9" id="tgt36" class="tgtSentence"> A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d5c5f8d72fd9df98b2afaf74c011ea42" id="tgt37" class="tgtSentence">
                    <legacyBold>adDBDate</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9fc3d7152ba9336a670e36d0ed79bc43" id="tgt38" class="tgtSentence">133</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="47e010b11cf1a7da9aa9900f07eb4cdc" id="tgt39" class="tgtSentence">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ada9d6c39e1470fd37d4691baedb4542" id="tgt40" class="tgtSentence">
                    <legacyBold>adDBTime</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="02522a2b2726fb0a03bb19f2d8d9524d" id="tgt41" class="tgtSentence">134</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="988c3d994a817b52ee3da358f1180097" id="tgt42" class="tgtSentence">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7c4241c4b2947a517873cb1ece871782" id="tgt43" class="tgtSentence">
                    <legacyBold>adDBTimeStamp</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7f1de29e6da19d22b51c68001e7e0e54" id="tgt44" class="tgtSentence">135</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a877a561f528cddd0fbe6a487e496724" id="tgt45" class="tgtSentence">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="fb9cf342a5d74ced9079465d8fe3102f" id="tgt46" class="tgtSentence">
                    <legacyBold>adDecimal</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="aab3238922bcc25a6f606eb525ffdc56" id="tgt47" class="tgtSentence">14</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="486cea8f77c266fa265748b41b74b188" id="tgt48" class="tgtSentence">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="252910eaf0d7087e5cbb187b273b38cd" id="tgt49" class="tgtSentence">
                    <legacyBold>adDouble</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e4da3b7fbbce2345d7772b0674a318d5" id="tgt50" class="tgtSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c3a1913782f390712aa6731f0f4d91f5" id="tgt51" class="tgtSentence">Indicates a double-precision floating-point value (DBTYPE_R8).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="97d09fe232ce163b811c964848658900" id="tgt52" class="tgtSentence">
                    <legacyBold>adEmpty</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt53" class="tgtSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e2546d0f3289d93dd6da210bcda45091" id="tgt54" class="tgtSentence">Specifies no value (DBTYPE_EMPTY).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7bfb405d67904bbea0f463bd7d7cde37" id="tgt55" class="tgtSentence">
                    <legacyBold>adError</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d3d9446802a44259755d38e6d163e820" id="tgt56" class="tgtSentence">10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9f41949bbdc6bca1f575e82fbbfec73a" id="tgt57" class="tgtSentence">Indicates a 32-bit error code (DBTYPE_ERROR).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7583512eee4349ea35ac6aa985800c77" id="tgt58" class="tgtSentence">
                    <legacyBold>adFileTime</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ea5d2f1c4608232e07d3aa3d998e5135" id="tgt59" class="tgtSentence">64</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4ff285984d46d6d5e8bbc60dfd95417f" id="tgt60" class="tgtSentence">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4a08bfd545860e8224761b14a4b998fa" id="tgt61" class="tgtSentence">
                    <legacyBold>adGUID</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="32bb90e8976aab5298d5da10fe66f21d" id="tgt62" class="tgtSentence">72</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4e1e56e3145647b22ac2a60c13d59acd" id="tgt63" class="tgtSentence">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="befea97099ee66dd075a742d3293795f" id="tgt64" class="tgtSentence">
                    <legacyBold>adIDispatch</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="45c48cce2e2d7fbdea1afc51c7c6ad26" id="tgt65" class="tgtSentence">9</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c26011c5582e4a5504fcf7b83cb62b9b" id="tgt66" class="tgtSentence">Indicates a pointer to an <legacyBold>IDispatch</legacyBold> interface on a COM object (DBTYPE_IDISPATCH).</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="2a81f7e88fab795b7c7b5946cbf9430e" id="tgt67" class="tgtSentence">
                    <embeddedLabel>Note</embeddedLabel>   This data type is currently not supported by ADO.</caps:sentence>
                  <caps:sentence sentenceid="2112d6f9d1b8fc5a06cac0f2f17d35b1" id="tgt68" class="tgtSentence"> Usage may cause unpredictable results.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e2993c2ef80c26d52cfc71b14281dcdd" id="tgt69" class="tgtSentence">
                    <legacyBold>adInteger</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt70" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c417d66878ffc6b4eb6e1f8fda7a8aa3" id="tgt71" class="tgtSentence">Indicates a four-byte signed integer (DBTYPE_I4).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a94e370aa452d546a58b767faa04f1a1" id="tgt72" class="tgtSentence">
                    <legacyBold>adIUnknown</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c51ce410c124a10e0db5e4b97fc2af39" id="tgt73" class="tgtSentence">13</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a13c0ca02dad254d89b51cd31c665b49" id="tgt74" class="tgtSentence">Indicates a pointer to an <legacyBold>IUnknown</legacyBold> interface on a COM object (DBTYPE_IUNKNOWN).</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="72b2fea085c1bb713c7e3b298e76d425" id="tgt75" class="tgtSentence">
                    <embeddedLabel>Note</embeddedLabel>
                    <legacyBold>   </legacyBold>This data type is currently not supported by ADO.</caps:sentence>
                  <caps:sentence sentenceid="2112d6f9d1b8fc5a06cac0f2f17d35b1" id="tgt76" class="tgtSentence"> Usage may cause unpredictable results.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a84a971bb29c50a706411cd2c867a5d2" id="tgt77" class="tgtSentence">
                    <legacyBold>adLongVarBinary</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eae27d77ca20db309e056e3d2dcd7d69" id="tgt78" class="tgtSentence">205</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f25e5ea8e6ba0aecf303b8dacc34098e" id="tgt79" class="tgtSentence">Indicates a long binary value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9d8490d8bcb79209bcc9fa47eba7b0c4" id="tgt80" class="tgtSentence">
                    <legacyBold>adLongVarChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="757b505cfd34c64c85ca5b5690ee5293" id="tgt81" class="tgtSentence">201</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="502bd97f11ab2e6e4febb169e44f0be3" id="tgt82" class="tgtSentence">Indicates a long string value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f8388e59a07c1ca01764f0757f5cb58b" id="tgt83" class="tgtSentence">
                    <legacyBold>adLongVarWChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e2c0be24560d78c5e599c2a9c9d0bbd2" id="tgt84" class="tgtSentence">203</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="aa32e50a06bec0315316af6f7ecaed79" id="tgt85" class="tgtSentence">Indicates a long null-terminated Unicode string value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="68e6f594ea96e3d5064ad634aa58d714" id="tgt86" class="tgtSentence">
                    <legacyBold>adNumeric</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1afa34a7f984eeabdbb0a7d494132ee5" id="tgt87" class="tgtSentence">131</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d11714fbea653a6440e2db1656f0ceea" id="tgt88" class="tgtSentence">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d7d28df0fbf9eb77d247dab53a076ab7" id="tgt89" class="tgtSentence">
                    <legacyBold>adPropVariant</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="013d407166ec4fa56eb1e1f8cbe183b9" id="tgt90" class="tgtSentence">138</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="de12cc7f26ae931fcbd7e2e4d645cc7f" id="tgt91" class="tgtSentence">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7176728e9c7b7445fe476e9660957b81" id="tgt92" class="tgtSentence">
                    <legacyBold>adSingle</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt93" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fcc7291a9f682e0efe97e3c923b50466" id="tgt94" class="tgtSentence">Indicates a single-precision floating-point value (DBTYPE_R4).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="767c7dc9697af2a1ff0b77777e0c2619" id="tgt95" class="tgtSentence">
                    <legacyBold>adSmallInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt96" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b0f78e9c87e1a1d09f1e65fc0b38ac40" id="tgt97" class="tgtSentence">Indicates a two-byte signed integer (DBTYPE_I2).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f7c198f051ea80cb6c6898e6e76c3ac8" id="tgt98" class="tgtSentence">
                    <legacyBold>adTinyInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c74d97b01eae257e44aa9d5bade97baf" id="tgt99" class="tgtSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0e209e6769d00df5a0997c38a7e5cbd4" id="tgt100" class="tgtSentence">Indicates a one-byte signed integer (DBTYPE_I1).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7ac027853cd50b43f374dca068f651dc" id="tgt101" class="tgtSentence">
                    <legacyBold>adUnsignedBigInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3c59dc048e8850243be8079a5c74d079" id="tgt102" class="tgtSentence">21</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="04f24dd1cc13b45366d7ebff3589372e" id="tgt103" class="tgtSentence">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d7de7c12f601fcde1880dd435504246d" id="tgt104" class="tgtSentence">
                    <legacyBold>adUnsignedInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1f0e3dad99908345f7439f8ffabdffc4" id="tgt105" class="tgtSentence">19</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="80f36e905b37d61a7a256963c7b8b7df" id="tgt106" class="tgtSentence">Indicates a four-byte unsigned integer (DBTYPE_UI4).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="898ccaf346e867cfc52468caf2a6babd" id="tgt107" class="tgtSentence">
                    <legacyBold>adUnsignedSmallInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6f4922f45568161a8cdf4ad2299f6d23" id="tgt108" class="tgtSentence">18</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f70d676a8a2960f24201e5e3f9e93b7a" id="tgt109" class="tgtSentence">Indicates a two-byte unsigned integer (DBTYPE_UI2).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d8b1f13cdd230498828336402da5113" id="tgt110" class="tgtSentence">
                    <legacyBold>adUnsignedTinyInt</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="70efdf2ec9b086079795c442636b55fb" id="tgt111" class="tgtSentence">17</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fe610d1f566d9f3553d7c945f1a6131e" id="tgt112" class="tgtSentence">Indicates a one-byte unsigned integer (DBTYPE_UI1).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c920170053551e7546e6bf54669b122e" id="tgt113" class="tgtSentence">
                    <legacyBold>adUserDefined</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="65ded5353c5ee48d0b7d48c591b8f430" id="tgt114" class="tgtSentence">132</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b0c206356b693d02321d244982e194cb" id="tgt115" class="tgtSentence">Indicates a user-defined variable (DBTYPE_UDT).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a8450e1416d7a650c617fba8dc57cddf" id="tgt116" class="tgtSentence">
                    <legacyBold>adVarBinary</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="274ad4786c3abca69fa097b85867d9a4" id="tgt117" class="tgtSentence">204</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0e0277a4c9f500145842e65aa3c1ee78" id="tgt118" class="tgtSentence">Indicates a binary value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d646bdce4789043b6e3e157c7d1413e" id="tgt119" class="tgtSentence">
                    <legacyBold>adVarChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3644a684f98ea8fe223c713b77189a77" id="tgt120" class="tgtSentence">200</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="19495f1efc40d52a2a21e39bbf7da0fc" id="tgt121" class="tgtSentence">Indicates a string value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="78f9cde5f680458c18e98ee101484244" id="tgt122" class="tgtSentence">
                    <legacyBold>adVariant</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c20ad4d76fe97759aa27a0c99bff6710" id="tgt123" class="tgtSentence">12</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ad9196699efe2037d47357922116d83f" id="tgt124" class="tgtSentence">Indicates an Automation <languageKeyword>Variant</languageKeyword> (DBTYPE_VARIANT).</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="72b2fea085c1bb713c7e3b298e76d425" id="tgt125" class="tgtSentence">
                    <embeddedLabel>Note</embeddedLabel>
                    <legacyBold>   </legacyBold>This data type is currently not supported by ADO.</caps:sentence>
                  <caps:sentence sentenceid="2112d6f9d1b8fc5a06cac0f2f17d35b1" id="tgt126" class="tgtSentence"> Usage may cause unpredictable results.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d0c61991b3c49297c8fb4805697dd5a9" id="tgt127" class="tgtSentence">
                    <legacyBold>adVarNumeric</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e00da03b685a0dd18fb6a08af0923de0" id="tgt128" class="tgtSentence">139</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ac3e5db94b74575fd78cfdd604922779" id="tgt129" class="tgtSentence">Indicates a numeric value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4d6de72faf4548e03c7d5e33a0fed19e" id="tgt130" class="tgtSentence">
                    <legacyBold>adVarWChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="854d6fae5ee42911677c739ee1734486" id="tgt131" class="tgtSentence">202</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3b18e2c12463577d4977333d553afed4" id="tgt132" class="tgtSentence">Indicates a null-terminated Unicode character string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7a566f8f32dad615f20e9b2bd797def8" id="tgt133" class="tgtSentence">
                    <legacyBold>adWChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9b8619251a19057cff70779273e95aa6" id="tgt134" class="tgtSentence">130</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="664dc76123d94d7fa475dda5e1ebe6b6" id="tgt135" class="tgtSentence">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt136" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt137" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt138" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0303663e1027deaafb942f28466fb5d8" id="tgt139" class="tgtSentence">AdoEnums.DataType.ARRAY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f9ebe89e0e0ea6772ddcf74cf25926b" id="tgt140" class="tgtSentence">AdoEnums.DataType.BIGINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="29c0ac13d34ce2c8da3dec5292587750" id="tgt141" class="tgtSentence">AdoEnums.DataType.BINARY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="739c624dee4e563dac707d4a479f43eb" id="tgt142" class="tgtSentence">AdoEnums.DataType.BOOLEAN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="99f76996448bfe463ca261a40da62836" id="tgt143" class="tgtSentence">AdoEnums.DataType.BSTR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2a034da7199fe6cd137434a5eef7e134" id="tgt144" class="tgtSentence">AdoEnums.DataType.CHAPTER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4991415cedf0f1259eb2f9f74676635d" id="tgt145" class="tgtSentence">AdoEnums.DataType.CHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b23ef80861a6a1b8fba7d68eb1e709c" id="tgt146" class="tgtSentence">AdoEnums.DataType.CURRENCY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="59903a7158fac170f5877bcb509b0296" id="tgt147" class="tgtSentence">AdoEnums.DataType.DATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5c9b846a7b931c3ac9ec0e73929ad85e" id="tgt148" class="tgtSentence">AdoEnums.DataType.DBDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="edaa151b1a5095f2a3a702c0addcb489" id="tgt149" class="tgtSentence">AdoEnums.DataType.DBTIME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1ec7283cd80493bd56a8067c245be54" id="tgt150" class="tgtSentence">AdoEnums.DataType.DBTIMESTAMP</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="184dac74ad14a9f38deadaa64461d854" id="tgt151" class="tgtSentence">AdoEnums.DataType.DECIMAL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa745f19645e075b0c4b072c1a33643e" id="tgt152" class="tgtSentence">AdoEnums.DataType.DOUBLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c7cb78de8112464c26c656e70832d65c" id="tgt153" class="tgtSentence">AdoEnums.DataType.EMPTY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b86554da5ea3172f67abb9774b6193ce" id="tgt154" class="tgtSentence">AdoEnums.DataType.ERROR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="acf948192c6932b4614fa28cb88524aa" id="tgt155" class="tgtSentence">AdoEnums.DataType.FILETIME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc80d3ecf3cb7092bded0f6850ff9e8a" id="tgt156" class="tgtSentence">AdoEnums.DataType.GUID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92c3efcd41c82fe13d102a3e4732248a" id="tgt157" class="tgtSentence">AdoEnums.DataType.IDISPATCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="51a739dc33270399485ecef3face2cd8" id="tgt158" class="tgtSentence">AdoEnums.DataType.INTEGER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5476dbf675830c2d7cde3035d7d5d51" id="tgt159" class="tgtSentence">AdoEnums.DataType.IUNKNOWN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a105fc5133d671af6336cd3b67c5cd19" id="tgt160" class="tgtSentence">AdoEnums.DataType.LONGVARBINARY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b1879ac190ddd49edf6dd2784beb7977" id="tgt161" class="tgtSentence">AdoEnums.DataType.LONGVARCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="452e216f50b6808ce740a3468cd5ec53" id="tgt162" class="tgtSentence">AdoEnums.DataType.LONGVARWCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63558d3800ee5c3c15c447458e2e69be" id="tgt163" class="tgtSentence">AdoEnums.DataType.NUMERIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c87f49de99244efad3ee64ec660d287a" id="tgt164" class="tgtSentence">AdoEnums.DataType.PROPVARIANT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f4d0ca4e243c1447f93e72fce3c437f5" id="tgt165" class="tgtSentence">AdoEnums.DataType.SINGLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1c0fae1b000a29f34073fd054b609bd0" id="tgt166" class="tgtSentence">AdoEnums.DataType.SMALLINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae25537d9bfee1c688cef71b5b40b9c1" id="tgt167" class="tgtSentence">AdoEnums.DataType.TINYINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="314fd9061474dd735856a5981f307ec5" id="tgt168" class="tgtSentence">AdoEnums.DataType.UNSIGNEDBIGINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3e5adb900d9ea1917175048ed94176bb" id="tgt169" class="tgtSentence">AdoEnums.DataType.UNSIGNEDINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="91046856d185db2b2465a634ab2c11b3" id="tgt170" class="tgtSentence">AdoEnums.DataType.UNSIGNEDSMALLINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c475db763ca77dda7375d48f22b05182" id="tgt171" class="tgtSentence">AdoEnums.DataType.UNSIGNEDTINYINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="88e0e6e4b3892bfb2fc5018aa26677ec" id="tgt172" class="tgtSentence">AdoEnums.DataType.USERDEFINED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1711ea8c4577b763ef8904bbc2e2b24c" id="tgt173" class="tgtSentence">AdoEnums.DataType.VARBINARY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8530f92aec879d0e5d64d82ec73e8656" id="tgt174" class="tgtSentence">AdoEnums.DataType.VARCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1c6efa880b56bb2d01a9e3ea9db33963" id="tgt175" class="tgtSentence">AdoEnums.DataType.VARIANT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="66e1e0302213ab6ab21210f8deda10b8" id="tgt176" class="tgtSentence">AdoEnums.DataType.VARNUMERIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a96618f4ceaaafeca33b200ad293c920" id="tgt177" class="tgtSentence">AdoEnums.DataType.VARWCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fc0bb78e2d277a260fc64461c1cd3e5" id="tgt178" class="tgtSentence">AdoEnums.DataType.WCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt179" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter Method</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type Property</link>
                  </para>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the data type of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink>, <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink>, or <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</caps:sentence>
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
                    <caps:sentence id="src6" class="srcSentence">AdArray</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">0x2000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">A flag value, always combined with another data type constant, that indicates an array of the other data type.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> Does not apply to ADOX.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">
                    <legacyBold>adBigInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">20</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Indicates an eight-byte signed integer (DBTYPE_I8).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">
                    <legacyBold>adBinary</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">128</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Indicates a binary value (DBTYPE_BYTES).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">
                    <legacyBold>adBoolean</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">11</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Indicates a <languageKeyword>Boolean</languageKeyword> value (DBTYPE_BOOL).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">
                    <legacyBold>adBSTR</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">
                    <legacyBold>adChapter</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">136</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">
                    <legacyBold>adChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">129</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Indicates a string value (DBTYPE_STR).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">
                    <legacyBold>adCurrency</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">6</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Indicates a currency value (DBTYPE_CY).</caps:sentence>
                  <caps:sentence id="src31" class="srcSentence"> Currency is a fixed-point number with four digits to the right of the decimal point.</caps:sentence>
                  <caps:sentence id="src32" class="srcSentence"> It is stored in an eight-byte signed integer scaled by 10,000.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">
                    <legacyBold>adDate</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">Indicates a date value (DBTYPE_DATE).</caps:sentence>
                  <caps:sentence id="src36" class="srcSentence"> A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">
                    <legacyBold>adDBDate</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">133</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">
                    <legacyBold>adDBTime</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">134</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">
                    <legacyBold>adDBTimeStamp</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src44" class="srcSentence">135</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">
                    <legacyBold>adDecimal</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">14</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src48" class="srcSentence">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">
                    <legacyBold>adDouble</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src50" class="srcSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src51" class="srcSentence">Indicates a double-precision floating-point value (DBTYPE_R8).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">
                    <legacyBold>adEmpty</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">Specifies no value (DBTYPE_EMPTY).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">
                    <legacyBold>adError</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">Indicates a 32-bit error code (DBTYPE_ERROR).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src58" class="srcSentence">
                    <legacyBold>adFileTime</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">64</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src60" class="srcSentence">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src61" class="srcSentence">
                    <legacyBold>adGUID</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src62" class="srcSentence">72</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src63" class="srcSentence">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src64" class="srcSentence">
                    <legacyBold>adIDispatch</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src65" class="srcSentence">9</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src66" class="srcSentence">Indicates a pointer to an <legacyBold>IDispatch</legacyBold> interface on a COM object (DBTYPE_IDISPATCH).</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src67" class="srcSentence">
                    <embeddedLabel>Note</embeddedLabel>   This data type is currently not supported by ADO.</caps:sentence>
                  <caps:sentence id="src68" class="srcSentence"> Usage may cause unpredictable results.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src69" class="srcSentence">
                    <legacyBold>adInteger</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src70" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src71" class="srcSentence">Indicates a four-byte signed integer (DBTYPE_I4).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src72" class="srcSentence">
                    <legacyBold>adIUnknown</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src73" class="srcSentence">13</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src74" class="srcSentence">Indicates a pointer to an <legacyBold>IUnknown</legacyBold> interface on a COM object (DBTYPE_IUNKNOWN).</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src75" class="srcSentence">
                    <embeddedLabel>Note</embeddedLabel>
                    <legacyBold>   </legacyBold>This data type is currently not supported by ADO.</caps:sentence>
                  <caps:sentence id="src76" class="srcSentence"> Usage may cause unpredictable results.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src77" class="srcSentence">
                    <legacyBold>adLongVarBinary</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src78" class="srcSentence">205</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src79" class="srcSentence">Indicates a long binary value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src80" class="srcSentence">
                    <legacyBold>adLongVarChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src81" class="srcSentence">201</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src82" class="srcSentence">Indicates a long string value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src83" class="srcSentence">
                    <legacyBold>adLongVarWChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src84" class="srcSentence">203</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src85" class="srcSentence">Indicates a long null-terminated Unicode string value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src86" class="srcSentence">
                    <legacyBold>adNumeric</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src87" class="srcSentence">131</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src88" class="srcSentence">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src89" class="srcSentence">
                    <legacyBold>adPropVariant</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src90" class="srcSentence">138</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src91" class="srcSentence">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src92" class="srcSentence">
                    <legacyBold>adSingle</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src93" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src94" class="srcSentence">Indicates a single-precision floating-point value (DBTYPE_R4).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src95" class="srcSentence">
                    <legacyBold>adSmallInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src96" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src97" class="srcSentence">Indicates a two-byte signed integer (DBTYPE_I2).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src98" class="srcSentence">
                    <legacyBold>adTinyInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src99" class="srcSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src100" class="srcSentence">Indicates a one-byte signed integer (DBTYPE_I1).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src101" class="srcSentence">
                    <legacyBold>adUnsignedBigInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src102" class="srcSentence">21</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src103" class="srcSentence">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src104" class="srcSentence">
                    <legacyBold>adUnsignedInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src105" class="srcSentence">19</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src106" class="srcSentence">Indicates a four-byte unsigned integer (DBTYPE_UI4).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src107" class="srcSentence">
                    <legacyBold>adUnsignedSmallInt</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src108" class="srcSentence">18</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src109" class="srcSentence">Indicates a two-byte unsigned integer (DBTYPE_UI2).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src110" class="srcSentence">
                    <legacyBold>adUnsignedTinyInt</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src111" class="srcSentence">17</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src112" class="srcSentence">Indicates a one-byte unsigned integer (DBTYPE_UI1).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src113" class="srcSentence">
                    <legacyBold>adUserDefined</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src114" class="srcSentence">132</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src115" class="srcSentence">Indicates a user-defined variable (DBTYPE_UDT).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src116" class="srcSentence">
                    <legacyBold>adVarBinary</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src117" class="srcSentence">204</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src118" class="srcSentence">Indicates a binary value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src119" class="srcSentence">
                    <legacyBold>adVarChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src120" class="srcSentence">200</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src121" class="srcSentence">Indicates a string value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src122" class="srcSentence">
                    <legacyBold>adVariant</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src123" class="srcSentence">12</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src124" class="srcSentence">Indicates an Automation <languageKeyword>Variant</languageKeyword> (DBTYPE_VARIANT).</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src125" class="srcSentence">
                    <embeddedLabel>Note</embeddedLabel>
                    <legacyBold>   </legacyBold>This data type is currently not supported by ADO.</caps:sentence>
                  <caps:sentence id="src126" class="srcSentence"> Usage may cause unpredictable results.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src127" class="srcSentence">
                    <legacyBold>adVarNumeric</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src128" class="srcSentence">139</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src129" class="srcSentence">Indicates a numeric value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src130" class="srcSentence">
                    <legacyBold>adVarWChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src131" class="srcSentence">202</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src132" class="srcSentence">Indicates a null-terminated Unicode character string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src133" class="srcSentence">
                    <legacyBold>adWChar</legacyBold>  </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src134" class="srcSentence">130</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src135" class="srcSentence">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src136" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src137" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">AdoEnums.DataType.ARRAY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">AdoEnums.DataType.BIGINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">AdoEnums.DataType.BINARY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">AdoEnums.DataType.BOOLEAN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">AdoEnums.DataType.BSTR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">AdoEnums.DataType.CHAPTER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">AdoEnums.DataType.CHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">AdoEnums.DataType.CURRENCY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">AdoEnums.DataType.DATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src148" class="srcSentence">AdoEnums.DataType.DBDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">AdoEnums.DataType.DBTIME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">AdoEnums.DataType.DBTIMESTAMP</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">AdoEnums.DataType.DECIMAL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">AdoEnums.DataType.DOUBLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">AdoEnums.DataType.EMPTY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">AdoEnums.DataType.ERROR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src155" class="srcSentence">AdoEnums.DataType.FILETIME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">AdoEnums.DataType.GUID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">AdoEnums.DataType.IDISPATCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">AdoEnums.DataType.INTEGER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">AdoEnums.DataType.IUNKNOWN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">AdoEnums.DataType.LONGVARBINARY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">AdoEnums.DataType.LONGVARCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">AdoEnums.DataType.LONGVARWCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">AdoEnums.DataType.NUMERIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">AdoEnums.DataType.PROPVARIANT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">AdoEnums.DataType.SINGLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">AdoEnums.DataType.SMALLINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">AdoEnums.DataType.TINYINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">AdoEnums.DataType.UNSIGNEDBIGINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">AdoEnums.DataType.UNSIGNEDINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">AdoEnums.DataType.UNSIGNEDSMALLINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">AdoEnums.DataType.UNSIGNEDTINYINT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">AdoEnums.DataType.USERDEFINED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">AdoEnums.DataType.VARBINARY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">AdoEnums.DataType.VARCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">AdoEnums.DataType.VARIANT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">AdoEnums.DataType.VARNUMERIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">AdoEnums.DataType.VARWCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">AdoEnums.DataType.WCHAR</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src179" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter Method</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type Property</link>
                  </para>
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
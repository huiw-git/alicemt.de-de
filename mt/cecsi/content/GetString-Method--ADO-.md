---
title: "GetString Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 92452940-b2a7-456e-94fc-3780c71da33c
caps.latest.revision: 11
caps.handback.revision: 11
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
# GetString Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b57c6d07ae720ba49471e2330a85f31d" id="tgt1" class="tgtSentence">Returns the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> as a string.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Variant</parameterReference> = <parameterReference>recordset.</parameterReference><legacyBold>GetString</legacyBold><parameterReference>(StringFormat, NumRows, ColumnDelimiter, RowDelimiter, NullExpr)</parameterReference></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="2e7a503de4bf031fec371ce35b3964c7" id="tgt2" class="tgtSentence">Returns the <legacyBold>Recordset</legacyBold> as a string-valued <languageKeyword>Variant</languageKeyword> (BSTR).</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d7c9c755b9a0802344e913e9071715db" id="tgt3" class="tgtSentence"> <legacyItalic>StringFormat</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="9e0490ac31bdb5961806a53d34213983" id="tgt4" class="tgtSentence">A <legacyLink xlink:href="28f7d1ec-092b-4323-a39d-d3f882c6c81a">StringFormatEnum</legacyLink> value that specifies how the <legacyBold>Recordset</legacyBold> should be converted to a string.</caps:sentence>
                <caps:sentence sentenceid="a7aa9bf756f991c7542a433146ccfb88" id="tgt5" class="tgtSentence"> The <legacyItalic>RowDelimiter</legacyItalic>, <legacyItalic>ColumnDelimiter</legacyItalic>, and <legacyItalic>NullExpr</legacyItalic> parameters are used only with a <legacyItalic>StringFormat</legacyItalic> of <legacyBold>adClipString</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="088277e415001e13418d65919856712f" id="tgt6" class="tgtSentence"> <legacyItalic>NumRows</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt7" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="fc14d2c526c93c4454ffdd17739cde9e" id="tgt8" class="tgtSentence"> The number of rows to be converted in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="482e14373642b33d88199a799e06ecfc" id="tgt9" class="tgtSentence"> If <legacyItalic>NumRows </legacyItalic>is not specified, or if it is greater than the total number of rows in the <legacyBold>Recordset</legacyBold>, then all the rows in the <legacyBold>Recordset</legacyBold> are converted.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="ac19de9738a2fd5cc7d15fdf5cce45dc" id="tgt10" class="tgtSentence"> <legacyItalic>ColumnDelimiter</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt11" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="5f0f88c1f1adce52674d3fe795b5d399" id="tgt12" class="tgtSentence"> A delimiter used between columns, if specified, otherwise the TAB character.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="b7eb3d9f88e408727b5ecdbc426ee793" id="tgt13" class="tgtSentence"> <legacyItalic>RowDelimiter</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt14" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="0d87176a9f803b84e09a0751dc02c05f" id="tgt15" class="tgtSentence"> A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e506595b24bd89fa7116dce2bb918774" id="tgt16" class="tgtSentence"> <legacyItalic>NullExpr</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt17" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="b497d661fc90dace80ac6f288acc3942" id="tgt18" class="tgtSentence"> An expression used in place of a null value, if specified, otherwise the empty string.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="16e8656fca0a0472da24a95383aebe22" id="tgt19" class="tgtSentence">Row data, but no schema data, is saved to the string.</caps:sentence>
            <caps:sentence sentenceid="ccab6e639271a00d560fda8638f71911" id="tgt20" class="tgtSentence"> Therefore, a <legacyBold>Recordset</legacyBold> cannot be reopened using this string.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fece7f322fa0b9ed7a4eab5fe582803b" id="tgt21" class="tgtSentence">This method is equivalent to the RDO <legacyBold>GetClipString</legacyBold> method.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt22" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="14c96d71-46a8-4782-b474-80ce348e8bff">Visual Basic Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Returns the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> as a string.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Variant</parameterReference> = <parameterReference>recordset.</parameterReference><legacyBold>GetString</legacyBold><parameterReference>(StringFormat, NumRows, ColumnDelimiter, RowDelimiter, NullExpr)</parameterReference></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns the <legacyBold>Recordset</legacyBold> as a string-valued <languageKeyword>Variant</languageKeyword> (BSTR).</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>StringFormat</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A <legacyLink xlink:href="28f7d1ec-092b-4323-a39d-d3f882c6c81a">StringFormatEnum</legacyLink> value that specifies how the <legacyBold>Recordset</legacyBold> should be converted to a string.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> The <legacyItalic>RowDelimiter</legacyItalic>, <legacyItalic>ColumnDelimiter</legacyItalic>, and <legacyItalic>NullExpr</legacyItalic> parameters are used only with a <legacyItalic>StringFormat</legacyItalic> of <legacyBold>adClipString</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>NumRows</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> The number of rows to be converted in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> If <legacyItalic>NumRows </legacyItalic>is not specified, or if it is greater than the total number of rows in the <legacyBold>Recordset</legacyBold>, then all the rows in the <legacyBold>Recordset</legacyBold> are converted.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>ColumnDelimiter</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> A delimiter used between columns, if specified, otherwise the TAB character.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src13" class="srcSentence"> <legacyItalic>RowDelimiter</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src14" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src16" class="srcSentence"> <legacyItalic>NullExpr</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src17" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> An expression used in place of a null value, if specified, otherwise the empty string.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src19" class="srcSentence">Row data, but no schema data, is saved to the string.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Therefore, a <legacyBold>Recordset</legacyBold> cannot be reopened using this string.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">This method is equivalent to the RDO <legacyBold>GetClipString</legacyBold> method.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="14c96d71-46a8-4782-b474-80ce348e8bff">Visual Basic Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
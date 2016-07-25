---
title: "ReadText Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: be5a409e-cf87-4859-9ea5-713401755a77
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
# ReadText Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a7b3a16b55518805df11a5b35cd3965c" id="tgt1" class="tgtSentence">Reads specified number of characters from a text <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>String = Stream</parameterReference>
          <legacyBold>.ReadText ( </legacyBold>
          <parameterReference>NumChars</parameterReference>
          <legacyBold>)</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="6d68b096497386493a5cc876f517f9c7" id="tgt2" class="tgtSentence">NumChars</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="4817887de6899a9eeaf4c80b9e16c875" id="tgt4" class="tgtSentence"> A <languageKeyword>Long</languageKeyword> value that specifies the number of characters to read from the file, or a <legacyLink xlink:href="cfa1b416-003a-436f-a21b-bd2397e54db3">StreamReadEnum</legacyLink> value.</caps:sentence>
                <caps:sentence sentenceid="a24c09a910512361efacb840a35848e0" id="tgt5" class="tgtSentence"> The default value is <legacyBold>adReadAll</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="a2fd9a9d22508150494e0a9f318b04fc" id="tgt6" class="tgtSentence">The <legacyBold>ReadText </legacyBold>method reads a specified number of characters, an entire line, or the entire stream from a <legacyBold>Stream</legacyBold> object and returns the resulting string.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9860625a58b6e1c343250882c00de0f9" id="tgt7" class="tgtSentence">If <legacyItalic>NumChar</legacyItalic> is more than the number of characters left in the stream, only the characters remaining are returned.</caps:sentence>
            <caps:sentence sentenceid="51f4e556abc03851d08ed4052ff84856" id="tgt8" class="tgtSentence"> The string read is not padded to match the length specified by <legacyItalic>NumChar</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="41844b799ee49c99c35a70d9a795fbeb" id="tgt9" class="tgtSentence"> If there are no characters left to read, a variant whose value is null is returned.</caps:sentence>
            <caps:sentence sentenceid="edf6e1b5004ce85ac3ec17c71cecc065" id="tgt10" class="tgtSentence">
              <legacyBold>ReadText</legacyBold> cannot be used to read backwards.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="328fe4bdcb7e37c5f603ce45c195f96d" id="tgt11" class="tgtSentence">The <legacyBold>ReadText</legacyBold> method is used with text streams (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
              <caps:sentence sentenceid="ed30cdf44650943437c8297eacabec17" id="tgt12" class="tgtSentence"> For binary streams (<legacyBold>Type</legacyBold> is <legacyBold>adTypeBinary</legacyBold>), use <legacyLink xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">Read</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="4868c9743503b1e4f898020764c3aa42" id="tgt13" class="tgtSentence">Queries that result in a large amount of XML data being returned through the <legacyBold>ReadText</legacyBold> method of the ActiveX Data Object (ADO) Stream object may take a great deal of time to execute; if this is done in a COM+ component that is invoked from an ASP page, the user's session may time out.</caps:sentence>
            <caps:sentence sentenceid="0ae11edd11e6e70567908ae76fdd1482" id="tgt14" class="tgtSentence"> ADO converts Stream object data from UTF-8 encoding to Unicode; the frequent memory reallocation involved in conversion of such a large quantity of data at once is quite time-consuming.</caps:sentence>
            <caps:sentence sentenceid="63c560516296c7cbac5bb1e13a1f5dc0" id="tgt15" class="tgtSentence"> To resolve, make repeated calls to the <legacyBold>ReadText</legacyBold> method of the ADO command object, and specify a smaller number of characters.</caps:sentence>
            <caps:sentence sentenceid="87c4799b35be803b65beb6e5ef19924c" id="tgt16" class="tgtSentence"> Tests have shown that a value equivalent to 128K (131,072) is optimal.</caps:sentence>
            <caps:sentence sentenceid="3288ef15c1f77701a4dfcc8daea552d0" id="tgt17" class="tgtSentence"> Response time decreases as this value is decreased.</caps:sentence>
            <caps:sentence sentenceid="46364ea21d241803255faa133558722a" id="tgt18" class="tgtSentence"> For more information, see Knowledge Base article 280067, "PRB: Retrieving very large XML Documents from SQL Server 2000 by using ReadText method of ADO stream object may be slow", in the Microsoft Knowledge Base at http://support.microsoft.com.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt19" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">Read Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Reads specified number of characters from a text <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>String = Stream</parameterReference>
          <legacyBold>.ReadText ( </legacyBold>
          <parameterReference>NumChars</parameterReference>
          <legacyBold>)</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src2" class="srcSentence">NumChars</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A <languageKeyword>Long</languageKeyword> value that specifies the number of characters to read from the file, or a <legacyLink xlink:href="cfa1b416-003a-436f-a21b-bd2397e54db3">StreamReadEnum</legacyLink> value.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> The default value is <legacyBold>adReadAll</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">The <legacyBold>ReadText </legacyBold>method reads a specified number of characters, an entire line, or the entire stream from a <legacyBold>Stream</legacyBold> object and returns the resulting string.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">If <legacyItalic>NumChar</legacyItalic> is more than the number of characters left in the stream, only the characters remaining are returned.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The string read is not padded to match the length specified by <legacyItalic>NumChar</legacyItalic>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If there are no characters left to read, a variant whose value is null is returned.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence">
              <legacyBold>ReadText</legacyBold> cannot be used to read backwards.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src11" class="srcSentence">The <legacyBold>ReadText</legacyBold> method is used with text streams (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
              <caps:sentence id="src12" class="srcSentence"> For binary streams (<legacyBold>Type</legacyBold> is <legacyBold>adTypeBinary</legacyBold>), use <legacyLink xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">Read</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src13" class="srcSentence">Queries that result in a large amount of XML data being returned through the <legacyBold>ReadText</legacyBold> method of the ActiveX Data Object (ADO) Stream object may take a great deal of time to execute; if this is done in a COM+ component that is invoked from an ASP page, the user's session may time out.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> ADO converts Stream object data from UTF-8 encoding to Unicode; the frequent memory reallocation involved in conversion of such a large quantity of data at once is quite time-consuming.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> To resolve, make repeated calls to the <legacyBold>ReadText</legacyBold> method of the ADO command object, and specify a smaller number of characters.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Tests have shown that a value equivalent to 128K (131,072) is optimal.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Response time decreases as this value is decreased.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> For more information, see Knowledge Base article 280067, "PRB: Retrieving very large XML Documents from SQL Server 2000 by using ReadText method of ADO stream object may be slow", in the Microsoft Knowledge Base at http://support.microsoft.com.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src19" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">Read Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
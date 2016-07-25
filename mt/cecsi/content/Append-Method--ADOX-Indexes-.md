---
title: "Append Method (ADOX Indexes)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6695769f-275b-4b70-81bd-1a5f7d74926c
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
# Append Method (ADOX Indexes)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9f4711d5d67449ed780b733000486eaf" id="tgt1" class="tgtSentence">Adds a new <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink> object to the <legacyLink xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Indexes</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>Index</parameterReference> [<legacyBold>,</legacyBold><parameterReference>Columns</parameterReference>]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7e3038a4b387913b9ba7364277db23fd" id="tgt2" class="tgtSentence"> <legacyItalic>Index</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a699eb154e95828fbda2c7658855bb41" id="tgt3" class="tgtSentence">The <legacyBold>Index</legacyBold> object to append or the name of the index to create and append.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="ce9288687c2a5d8dbfd57bb07b79fbd0" id="tgt4" class="tgtSentence"> <legacyItalic>Columns</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt5" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="ddf1fabb8f597c392a13a7861a59b2fa" id="tgt6" class="tgtSentence"> A <legacyBold>Variant</legacyBold> value that specifies the name(s) of the column(s) to be indexed.</caps:sentence>
                <caps:sentence sentenceid="bb5810dab3ac33beb3d412a2d0a1fa6c" id="tgt7" class="tgtSentence"> The <legacyItalic>Columns </legacyItalic>parameter corresponds to the value(s) of the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property of a <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> object or objects.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="8bec55c5c87105955779f13382c773f5" id="tgt8" class="tgtSentence">The <legacyItalic>Columns</legacyItalic> parameter can take either the name of a column or an array of column names.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bde20878e9fecaaa87b2eebb88a41a1a" id="tgt9" class="tgtSentence">An error will occur if the provider does not support creating indexes.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="50f87e27-1bf9-427c-9b1d-704a672434d2">Indexes Append Method Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
        <link xlink:href="38e3492c-c1e1-42e3-a71a-befdc90204db">Append Method (Procedures)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append Method (Users)</link>
        <link xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append Method (Views)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Adds a new <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink> object to the <legacyLink xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Indexes</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>Index</parameterReference> [<legacyBold>,</legacyBold><parameterReference>Columns</parameterReference>]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Index</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">The <legacyBold>Index</legacyBold> object to append or the name of the index to create and append.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>Columns</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> A <legacyBold>Variant</legacyBold> value that specifies the name(s) of the column(s) to be indexed.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> The <legacyItalic>Columns </legacyItalic>parameter corresponds to the value(s) of the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property of a <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> object or objects.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <legacyItalic>Columns</legacyItalic> parameter can take either the name of a column or an array of column names.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">An error will occur if the provider does not support creating indexes.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="50f87e27-1bf9-427c-9b1d-704a672434d2">Indexes Append Method Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
        <link xlink:href="38e3492c-c1e1-42e3-a71a-befdc90204db">Append Method (Procedures)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append Method (Users)</link>
        <link xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append Method (Views)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
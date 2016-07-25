---
title: "Append Method (ADOX Keys)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 215a5391-f422-42ec-99ea-4e6fbb5d3d64
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
# Append Method (ADOX Keys)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="84173cc444ddaaa61ad8b5689824b55b" id="tgt1" class="tgtSentence">Adds a new <legacyLink xlink:href="55f116fe-4d56-4892-bffe-0cdd6fc727c9">Key</legacyLink> object to the <legacyLink xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Keys</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>Key</parameterReference> [<legacyBold>,</legacyBold><parameterReference>KeyType</parameterReference>] [<legacyBold>,</legacyBold><parameterReference>Column</parameterReference>] [<legacyBold>,</legacyBold><parameterReference>RelatedTable</parameterReference>] [<legacyBold>,</legacyBold><parameterReference>RelatedColumn</parameterReference>]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="6cbd6d430305ac4d5fa469160a8fbb84" id="tgt2" class="tgtSentence"> <legacyItalic>Key</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="c5b14096493eb1eef8cb96e7918cf50a" id="tgt3" class="tgtSentence">The <unmanagedCodeEntityReference>Key</unmanagedCodeEntityReference> object to append or the name of the key to create and append.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="fdf29d45257580e748137c901e881722" id="tgt4" class="tgtSentence"> <legacyItalic>KeyType</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt5" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="5b161fa494dfb87b0adf57a58148c8ec" id="tgt6" class="tgtSentence"> A <languageKeyword>Long</languageKeyword> value that specifies the type of key.</caps:sentence>
                <caps:sentence sentenceid="5aec2c433935a6033eff4002ddae50e3" id="tgt7" class="tgtSentence"> The <legacyItalic>Key </legacyItalic>parameter corresponds to the <legacyLink xlink:href="8ca2f1fd-eb1e-490c-a28b-67eda92e0fc7">Type</legacyLink> property of a <unmanagedCodeEntityReference>Key</unmanagedCodeEntityReference> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="b675456188a4503724031c21550e43c9" id="tgt8" class="tgtSentence"> <legacyItalic>Column</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt9" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="d1fecb9a06fc76f883f31db51792e2ce" id="tgt10" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that specifies the name of the column to be indexed.</caps:sentence>
                <caps:sentence sentenceid="f475644a01678a0055185cea1aa6a513" id="tgt11" class="tgtSentence"> The <legacyItalic>Columns </legacyItalic>parameter corresponds to the value of the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property of a <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a9650fe5a34152c9a0478f0e24cdaa23" id="tgt12" class="tgtSentence"> <legacyItalic>RelatedTable</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt13" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="9997ff6774ebc794e85fc56c83dbee10" id="tgt14" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that specifies the name of the related table.</caps:sentence>
                <caps:sentence sentenceid="d77e6a97c4e6bc83360aa7709646a4ec" id="tgt15" class="tgtSentence"> The <legacyItalic>RelatedTable </legacyItalic>parameter corresponds to the value of the <unmanagedCodeEntityReference>Name</unmanagedCodeEntityReference> property of a <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="9194faa75e0a04fb8486f43b31778d2f" id="tgt16" class="tgtSentence"> <legacyItalic>RelatedColumn</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt17" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="2281bfe05c9c471ee7c1aa1ad65f46cb" id="tgt18" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that specifies the name of the related column for a foreign key.</caps:sentence>
                <caps:sentence sentenceid="9a40927c160fb90730c5d364be8896f5" id="tgt19" class="tgtSentence"> The <parameterReference>RelatedColumn</parameterReference> parameter corresponds to the value of the <unmanagedCodeEntityReference>Name</unmanagedCodeEntityReference> property of a <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="8bec55c5c87105955779f13382c773f5" id="tgt20" class="tgtSentence">The <legacyItalic>Columns</legacyItalic> parameter can take either the name of a column or an array of column names.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt21" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
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
          <caps:sentence id="src1" class="srcSentence">Adds a new <legacyLink xlink:href="55f116fe-4d56-4892-bffe-0cdd6fc727c9">Key</legacyLink> object to the <legacyLink xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Keys</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>Key</parameterReference> [<legacyBold>,</legacyBold><parameterReference>KeyType</parameterReference>] [<legacyBold>,</legacyBold><parameterReference>Column</parameterReference>] [<legacyBold>,</legacyBold><parameterReference>RelatedTable</parameterReference>] [<legacyBold>,</legacyBold><parameterReference>RelatedColumn</parameterReference>]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Key</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">The <unmanagedCodeEntityReference>Key</unmanagedCodeEntityReference> object to append or the name of the key to create and append.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>KeyType</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> A <languageKeyword>Long</languageKeyword> value that specifies the type of key.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> The <legacyItalic>Key </legacyItalic>parameter corresponds to the <legacyLink xlink:href="8ca2f1fd-eb1e-490c-a28b-67eda92e0fc7">Type</legacyLink> property of a <unmanagedCodeEntityReference>Key</unmanagedCodeEntityReference> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>Column</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that specifies the name of the column to be indexed.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> The <legacyItalic>Columns </legacyItalic>parameter corresponds to the value of the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property of a <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>RelatedTable</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that specifies the name of the related table.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> The <legacyItalic>RelatedTable </legacyItalic>parameter corresponds to the value of the <unmanagedCodeEntityReference>Name</unmanagedCodeEntityReference> property of a <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src16" class="srcSentence"> <legacyItalic>RelatedColumn</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src17" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that specifies the name of the related column for a foreign key.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> The <parameterReference>RelatedColumn</parameterReference> parameter corresponds to the value of the <unmanagedCodeEntityReference>Name</unmanagedCodeEntityReference> property of a <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src20" class="srcSentence">The <legacyItalic>Columns</legacyItalic> parameter can take either the name of a column or an array of column names.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
        <link xlink:href="38e3492c-c1e1-42e3-a71a-befdc90204db">Append Method (Procedures)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append Method (Users)</link>
        <link xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append Method (Views)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Open Method (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a87d8080-a238-45e5-bc80-9a8625b3810f
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
# Open Method (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1640413a86bb25dab21e8944c5ce8917" id="tgt1" class="tgtSentence">Retrieves the results of a multidimensional query and returns the results to a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Cellset</parameterReference>.<legacyBold>Open </legacyBold><parameterReference>Source</parameterReference><legacyBold>, </legacyBold><parameterReference>ActiveConnection</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="b86002c905ed82eb6c9ab27bfdb86afd" id="tgt2" class="tgtSentence"> <legacyItalic>Source</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="5b22e5cc0f3b520441bd48e75a5ca991" id="tgt4" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</caps:sentence>
                <caps:sentence sentenceid="237edafaaf786d231df29236ac01f6b1" id="tgt5" class="tgtSentence"> The <legacyItalic>Source </legacyItalic>argument corresponds to the <legacyLink xlink:href="875a99ea-7f1a-4570-87b1-5ecbebbcf845">Source</legacyLink> property.</caps:sentence>
                <caps:sentence sentenceid="3a635d922af03a57497586e7869cff3d" id="tgt6" class="tgtSentence"> For more information about MDX, see the <legacyLink xlink:href="8a7673c6-3ca1-4411-9f1e-adf1e47df4f3">OLE DB for Online Analytical Processing (OLAP)</legacyLink> documentation in the Microsoft Data Access Components SDK.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="b998383d7912d34117ef4638f8034b42" id="tgt7" class="tgtSentence"> <legacyItalic>ActiveConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="12821ed7438bac48b964534cec2804b7" id="tgt9" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> that evaluates to a string specifying either a valid ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object variable name or a definition for a connection.</caps:sentence>
                <caps:sentence sentenceid="10b23267b11f93b5d9c28c7ffffe701d" id="tgt10" class="tgtSentence"> The <legacyItalic>ActiveConnection </legacyItalic>argument specifies the connection in which to open the <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="7eb5ded68a3a4bfb72043c81396b3433" id="tgt11" class="tgtSentence"> If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</caps:sentence>
                <caps:sentence sentenceid="7f2929caded4a132d9c0922c18c399b2" id="tgt12" class="tgtSentence"> The <legacyItalic>ActiveConnection </legacyItalic>argument corresponds to the <legacyLink xlink:href="2509b32c-a995-4364-9152-d8c83129bdd8">ActiveConnection</legacyLink> property.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7356c0327e5166dff1757c60d35bee79" id="tgt13" class="tgtSentence">The <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="2509b32c-a995-4364-9152-d8c83129bdd8">ActiveConnection Property</link>
        <link xlink:href="a3aa594d-f9d4-4654-8625-ec20153ff5d9">Close Method</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="875a99ea-7f1a-4570-87b1-5ecbebbcf845">Source Property</link>
        <link xlink:href="06d480ca-9eb6-4570-a45d-a73539bddd32">State Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Retrieves the results of a multidimensional query and returns the results to a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Cellset</parameterReference>.<legacyBold>Open </legacyBold><parameterReference>Source</parameterReference><legacyBold>, </legacyBold><parameterReference>ActiveConnection</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Source</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> The <legacyItalic>Source </legacyItalic>argument corresponds to the <legacyLink xlink:href="875a99ea-7f1a-4570-87b1-5ecbebbcf845">Source</legacyLink> property.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> For more information about MDX, see the <legacyLink xlink:href="8a7673c6-3ca1-4411-9f1e-adf1e47df4f3">OLE DB for Online Analytical Processing (OLAP)</legacyLink> documentation in the Microsoft Data Access Components SDK.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>ActiveConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> that evaluates to a string specifying either a valid ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object variable name or a definition for a connection.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> The <legacyItalic>ActiveConnection </legacyItalic>argument specifies the connection in which to open the <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> The <legacyItalic>ActiveConnection </legacyItalic>argument corresponds to the <legacyLink xlink:href="2509b32c-a995-4364-9152-d8c83129bdd8">ActiveConnection</legacyLink> property.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">The <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="2509b32c-a995-4364-9152-d8c83129bdd8">ActiveConnection Property</link>
        <link xlink:href="a3aa594d-f9d4-4654-8625-ec20153ff5d9">Close Method</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="875a99ea-7f1a-4570-87b1-5ecbebbcf845">Source Property</link>
        <link xlink:href="06d480ca-9eb6-4570-a45d-a73539bddd32">State Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
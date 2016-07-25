---
title: "Create Method (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 64f5c21c-b581-42d8-bdc7-c4f1bebaf105
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
# Create Method (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bc9cf08a9b2f2e45aaae18638f160234" id="tgt1" class="tgtSentence">Creates a new catalog.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Catalog</parameterReference>
          <legacyBold>.Create </legacyBold>
          <parameterReference>ConnectString</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="9aa81b0cde73a6f67ffb7415dbf32a62" id="tgt2" class="tgtSentence"> <parameterReference>ConnectString </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="bc355984d90b1e713840c02b8897d776" id="tgt3" class="tgtSentence">A <languageKeyword>String</languageKeyword> value used to connect to the data source.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="73f50a70330bf70a18aad5f86afbb2d5" id="tgt4" class="tgtSentence">The <legacyBold>Create</legacyBold> method creates and opens a new ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> to the data source specified in <legacyItalic>ConnectString</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="9a0b2a0571cd5d357ff07381250736e7" id="tgt5" class="tgtSentence"> If successful, the new <legacyBold>Connection</legacyBold> object is assigned to the <legacyLink xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="33eb19cb9928f438334be9a50174c458" id="tgt6" class="tgtSentence">An error will occur if the provider does not support creating new catalogs.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d7ea0244-596a-404e-8f30-71cadab8d8fc">Create Method Example (VB)</link>
        <link xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Creates a new catalog.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Catalog</parameterReference>
          <legacyBold>.Create </legacyBold>
          <parameterReference>ConnectString</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <parameterReference>ConnectString </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>String</languageKeyword> value used to connect to the data source.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <legacyBold>Create</legacyBold> method creates and opens a new ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> to the data source specified in <legacyItalic>ConnectString</legacyItalic>.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> If successful, the new <legacyBold>Connection</legacyBold> object is assigned to the <legacyLink xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">An error will occur if the provider does not support creating new catalogs.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d7ea0244-596a-404e-8f30-71cadab8d8fc">Create Method Example (VB)</link>
        <link xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
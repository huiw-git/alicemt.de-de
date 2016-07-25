---
title: "Append Method (ADOX Procedures)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 38e3492c-c1e1-42e3-a71a-befdc90204db
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
# Append Method (ADOX Procedures)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b9758c160f7810b1a8edc554ec05d011" id="tgt1" class="tgtSentence">Adds a new <legacyLink xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure</legacyLink> object to the <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Procedures</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>Name</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Command</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="126d3eb305aa375299a9b5255f84a45f" id="tgt2" class="tgtSentence"> <legacyItalic>Name</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="962f4e3cc3412fa244a1be08eaa6efa0" id="tgt3" class="tgtSentence">A <legacyBold>String</legacyBold> value that specifies the name of the procedure to create and append.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8bcdbb096b15caba05f42701acefa5ea" id="tgt4" class="tgtSentence"> <legacyItalic>Command</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b8672ef2be629934d29bc8525130882a" id="tgt5" class="tgtSentence">An ADO <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object that represents the procedure to create and append.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b7a9a1cc03e00cb4c80a4907fe94a953" id="tgt6" class="tgtSentence">Creates a new procedure in the data source with the name and attributes specified in the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5d0d1399c1a986951fc3f7acd1d8aefb" id="tgt7" class="tgtSentence">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</caps:sentence>
            <caps:sentence sentenceid="96d6f70d89daf6b9b0fa0cb8d66da2ef" id="tgt8" class="tgtSentence">
              <legacyBold>Append</legacyBold> will fail if the provider does not support persisting commands.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="78baf3cd2df4b1fa42b358822c4423c9" id="tgt9" class="tgtSentence">When using the OLE DB Provider for Microsoft Jet, the <legacyBold>Procedures</legacyBold> collection <legacyBold>Append</legacyBold> method will allow you to specify a <legacyBold>View</legacyBold> rather than a <legacyBold>Procedure</legacyBold> in the <legacyItalic>Command</legacyItalic> parameter.</caps:sentence>
              <caps:sentence sentenceid="a87501bd6b53bd007f139e740682c60e" id="tgt10" class="tgtSentence"> The <legacyBold>View</legacyBold> will be added to the data source and will be added to the <legacyBold>Procedures</legacyBold> collection.</caps:sentence>
              <caps:sentence sentenceid="1539a37bf1e9a14263084351f75bcad0" id="tgt11" class="tgtSentence"> After the <legacyBold>Append</legacyBold>, if the <legacyBold>Procedures</legacyBold> and <legacyBold>Views</legacyBold> collections are refreshed, the <legacyBold>View</legacyBold> will no longer be in the <legacyBold>Procedures</legacyBold> collection and will appear in the <legacyBold>Views</legacyBold> collection.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
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
          <caps:sentence id="src1" class="srcSentence">Adds a new <legacyLink xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure</legacyLink> object to the <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Procedures</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>Name</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Command</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Name</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <legacyBold>String</legacyBold> value that specifies the name of the procedure to create and append.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>Command</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">An ADO <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object that represents the procedure to create and append.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Creates a new procedure in the data source with the name and attributes specified in the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence">
              <legacyBold>Append</legacyBold> will fail if the provider does not support persisting commands.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src9" class="srcSentence">When using the OLE DB Provider for Microsoft Jet, the <legacyBold>Procedures</legacyBold> collection <legacyBold>Append</legacyBold> method will allow you to specify a <legacyBold>View</legacyBold> rather than a <legacyBold>Procedure</legacyBold> in the <legacyItalic>Command</legacyItalic> parameter.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> The <legacyBold>View</legacyBold> will be added to the data source and will be added to the <legacyBold>Procedures</legacyBold> collection.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> After the <legacyBold>Append</legacyBold>, if the <legacyBold>Procedures</legacyBold> and <legacyBold>Views</legacyBold> collections are refreshed, the <legacyBold>View</legacyBold> will no longer be in the <legacyBold>Procedures</legacyBold> collection and will appear in the <legacyBold>Views</legacyBold> collection.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append Method (Users)</link>
        <link xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append Method (Views)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
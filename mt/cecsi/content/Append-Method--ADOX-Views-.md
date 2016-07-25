---
title: "Append Method (ADOX Views)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6070fd58-3237-4c77-a966-5b39ce5d57e4
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
# Append Method (ADOX Views)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="10f4be86f75d3e6435b317b4a8fc2d87" id="tgt1" class="tgtSentence">Creates a new <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> object and appends it to the <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Views</parameterReference>
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
              <caps:sentence sentenceid="22b7f4e9e8916e9f600d9de7d2dbc303" id="tgt2" class="tgtSentence"> <parameterReference>Name </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7124c888c8847dac4244fc4260f692b3" id="tgt3" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that specifies the name of the view to create.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="864b53a181ec29a270993b47a820f75a" id="tgt4" class="tgtSentence"> <parameterReference>Command </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="cb574ca933cb59c59e96cc02c68df03c" id="tgt5" class="tgtSentence">An ADO <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object that represents the view to create.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="3756b17f23628a021834bce339c547f0" id="tgt6" class="tgtSentence">Creates a new view in the data source with the name and attributes specified in the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d1878add7d774dea72237cb7a786411b" id="tgt7" class="tgtSentence">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider.</caps:sentence>
            <caps:sentence sentenceid="96d6f70d89daf6b9b0fa0cb8d66da2ef" id="tgt8" class="tgtSentence">
              <legacyBold>Append</legacyBold> will fail if the provider does not support persisting commands.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="33774500a288550d914f3dd05c4151e8" id="tgt9" class="tgtSentence">When using the OLE DB Provider for Microsoft Jet, the <legacyBold>Views</legacyBold> collection <legacyBold>Append</legacyBold> method will allow you to specify a <legacyBold>Procedure</legacyBold> rather than a <legacyBold>View</legacyBold> in the <legacyItalic>Command</legacyItalic> parameter.</caps:sentence>
              <caps:sentence sentenceid="08c1392c202358a7c86265128e6be304" id="tgt10" class="tgtSentence"> The <legacyBold>Procedure</legacyBold> will be added to the data source and will be added to the <legacyBold>Views</legacyBold> collection.</caps:sentence>
              <caps:sentence sentenceid="0dce2e79828fe13f3539da79edb6db9a" id="tgt11" class="tgtSentence"> After the <legacyBold>Append</legacyBold>, if the <legacyBold>Procedures</legacyBold> and <legacyBold>Views</legacyBold> collections are refreshed, the <legacyBold>Procedure</legacyBold> will no longer be in the <legacyBold>Views</legacyBold> collection and will appear in the <legacyBold>Procedures</legacyBold> collection.</caps:sentence>
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
            <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
        <link xlink:href="38e3492c-c1e1-42e3-a71a-befdc90204db">Append Method (Procedures)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append Method (Users)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Creates a new <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> object and appends it to the <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Views</parameterReference>
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
              <caps:sentence id="src2" class="srcSentence"> <parameterReference>Name </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>String</languageKeyword> value that specifies the name of the view to create.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <parameterReference>Command </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">An ADO <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object that represents the view to create.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Creates a new view in the data source with the name and attributes specified in the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence">
              <legacyBold>Append</legacyBold> will fail if the provider does not support persisting commands.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src9" class="srcSentence">When using the OLE DB Provider for Microsoft Jet, the <legacyBold>Views</legacyBold> collection <legacyBold>Append</legacyBold> method will allow you to specify a <legacyBold>Procedure</legacyBold> rather than a <legacyBold>View</legacyBold> in the <legacyItalic>Command</legacyItalic> parameter.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> The <legacyBold>Procedure</legacyBold> will be added to the data source and will be added to the <legacyBold>Views</legacyBold> collection.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> After the <legacyBold>Append</legacyBold>, if the <legacyBold>Procedures</legacyBold> and <legacyBold>Views</legacyBold> collections are refreshed, the <legacyBold>Procedure</legacyBold> will no longer be in the <legacyBold>Views</legacyBold> collection and will appear in the <legacyBold>Procedures</legacyBold> collection.</caps:sentence>
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
            <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
        <link xlink:href="38e3492c-c1e1-42e3-a71a-befdc90204db">Append Method (Procedures)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append Method (Users)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
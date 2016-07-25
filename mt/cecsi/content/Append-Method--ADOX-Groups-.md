---
title: "Append Method (ADOX Groups)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 56b94fc6-7ef0-4e4a-82a3-033b94c46036
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
# Append Method (ADOX Groups)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c8f4b7806eb2f2a669af01f664f9039a" id="tgt1" class="tgtSentence">Adds a new <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> object to the <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Groups</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>Group</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="c6953ff90fa9be5f614ea95387c8f429" id="tgt2" class="tgtSentence"> <legacyItalic>Group</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7011a3812f01aeb03d8c842be888b88c" id="tgt3" class="tgtSentence">The <legacyBold>Group</legacyBold> object to append or the name of the group to create and append.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="30b8c51fb892b8371ec778832efc0a4f" id="tgt4" class="tgtSentence">The <legacyBold>Groups</legacyBold> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all of the catalog's group accounts.</caps:sentence>
            <caps:sentence sentenceid="5169498867f7b81768234480dd58593d" id="tgt5" class="tgtSentence"> The <legacyBold>Groups</legacyBold> collection for a <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> represents only the group to which the user belongs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8014a6529244bec25baa97b5ebc977a7" id="tgt6" class="tgtSentence">An error will occur if the provider does not support creating groups.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d25f3b46f8ad8e51569b2aa62e8de1db" id="tgt7" class="tgtSentence">Before appending a <legacyBold>Group</legacyBold> object to the <legacyBold>Groups</legacyBold> collection of a <legacyBold>User</legacyBold> object, a <legacyBold>Group</legacyBold> object with the same <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> as the one to be appended must already exist in the <legacyBold>Groups</legacyBold> collection of the <legacyBold>Catalog</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c9426757-9cdd-4a95-b506-d3d011569109">Groups and Users Append, ChangePassword Methods Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
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
          <caps:sentence id="src1" class="srcSentence">Adds a new <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> object to the <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Groups</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>Group</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Group</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">The <legacyBold>Group</legacyBold> object to append or the name of the group to create and append.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <legacyBold>Groups</legacyBold> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all of the catalog's group accounts.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The <legacyBold>Groups</legacyBold> collection for a <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> represents only the group to which the user belongs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">An error will occur if the provider does not support creating groups.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src7" class="srcSentence">Before appending a <legacyBold>Group</legacyBold> object to the <legacyBold>Groups</legacyBold> collection of a <legacyBold>User</legacyBold> object, a <legacyBold>Group</legacyBold> object with the same <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> as the one to be appended must already exist in the <legacyBold>Groups</legacyBold> collection of the <legacyBold>Catalog</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c9426757-9cdd-4a95-b506-d3d011569109">Groups and Users Append, ChangePassword Methods Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
        <link xlink:href="38e3492c-c1e1-42e3-a71a-befdc90204db">Append Method (Procedures)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append Method (Users)</link>
        <link xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append Method (Views)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
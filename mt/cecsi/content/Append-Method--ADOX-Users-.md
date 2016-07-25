---
title: "Append Method (ADOX Users)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b80bc5d5-78ca-4f75-956b-2ac658029cc7
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
# Append Method (ADOX Users)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b495b93827816ae48b10bb50f2f6568b" id="tgt1" class="tgtSentence">Adds a new <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> object to the <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Users</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>User</parameterReference>[<legacyBold>,</legacyBold><parameterReference>Password</parameterReference>]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d8af1aa20975af3ce11d8079a26ccdd1" id="tgt2" class="tgtSentence"> <legacyItalic>User</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="2a7adbb1455b255617fa809a28727a80" id="tgt3" class="tgtSentence">A <languageKeyword>Variant</languageKeyword> value that contains the <legacyBold>User</legacyBold> object to append or the name of the user to create and append.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d83fe9057df78601fffb657095e0114f" id="tgt4" class="tgtSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt5" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="98f3091eea0777d050a5f3ce42886766" id="tgt6" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that contains the password for the user.</caps:sentence>
                <caps:sentence sentenceid="25833ff2333e273aacb2e54615997e87" id="tgt7" class="tgtSentence"> The <legacyItalic>Password </legacyItalic>parameter corresponds to the value specified by the <legacyLink xlink:href="d187fbc6-5fac-4abb-803d-bf344dcf0302">ChangePassword</legacyLink> method of a <legacyBold>User</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="57962730cee9528a06202a44912bda4f" id="tgt8" class="tgtSentence">The <legacyBold>Users</legacyBold> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all the catalog's users.</caps:sentence>
            <caps:sentence sentenceid="4bb7f2b5441729b6db5686fca781455e" id="tgt9" class="tgtSentence"> The <legacyBold>Users</legacyBold> collection for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> represents only the users that have a membership in the specific group.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="57dc42d415e1a58c8bc824322f2a29ed" id="tgt10" class="tgtSentence">An error will occur if the provider does not support creating users.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="4287c7e33448f248a3a6964cc0769d86" id="tgt11" class="tgtSentence">Before appending a <legacyBold>User</legacyBold> object to the <legacyBold>Users</legacyBold> collection of a <legacyBold>Group</legacyBold> object, a <legacyBold>User</legacyBold> object with the same <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> as the one to be appended must already exist in the <legacyBold>Users</legacyBold> collection of the <legacyBold>Catalog</legacyBold>.</caps:sentence>
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
            <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c9426757-9cdd-4a95-b506-d3d011569109">Groups and Users Append, ChangePassword Methods Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
        <link xlink:href="38e3492c-c1e1-42e3-a71a-befdc90204db">Append Method (Procedures)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append Method (Views)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Adds a new <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> object to the <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Users</parameterReference>
          <legacyBold>.Append </legacyBold>
          <parameterReference>User</parameterReference>[<legacyBold>,</legacyBold><parameterReference>Password</parameterReference>]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>User</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>Variant</languageKeyword> value that contains the <legacyBold>User</legacyBold> object to append or the name of the user to create and append.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that contains the password for the user.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> The <legacyItalic>Password </legacyItalic>parameter corresponds to the value specified by the <legacyLink xlink:href="d187fbc6-5fac-4abb-803d-bf344dcf0302">ChangePassword</legacyLink> method of a <legacyBold>User</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <legacyBold>Users</legacyBold> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all the catalog's users.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The <legacyBold>Users</legacyBold> collection for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> represents only the users that have a membership in the specific group.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">An error will occur if the provider does not support creating users.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src11" class="srcSentence">Before appending a <legacyBold>User</legacyBold> object to the <legacyBold>Users</legacyBold> collection of a <legacyBold>Group</legacyBold> object, a <legacyBold>User</legacyBold> object with the same <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> as the one to be appended must already exist in the <legacyBold>Users</legacyBold> collection of the <legacyBold>Catalog</legacyBold>.</caps:sentence>
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
            <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c9426757-9cdd-4a95-b506-d3d011569109">Groups and Users Append, ChangePassword Methods Example (VB)</link>
        <link xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append Method (Columns)</link>
        <link xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append Method (Groups)</link>
        <link xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append Method (Indexes)</link>
        <link xlink:href="215a5391-f422-42ec-99ea-4e6fbb5d3d64">Append Method (Keys)</link>
        <link xlink:href="38e3492c-c1e1-42e3-a71a-befdc90204db">Append Method (Procedures)</link>
        <link xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append Method (Tables)</link>
        <link xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append Method (Views)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
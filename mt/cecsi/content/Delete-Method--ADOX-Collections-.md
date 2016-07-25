---
title: "Delete Method (ADOX Collections)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e6b6e3a4-8952-4d79-81f4-51019c338374
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
# Delete Method (ADOX Collections)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="87ffdac1b88d787912dfda1344d5b84a" id="tgt1" class="tgtSentence">Removes an object from a collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Collection</parameterReference>
          <legacyBold>.Delete </legacyBold>
          <parameterReference>Name</parameterReference>
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
                <caps:sentence sentenceid="ff6cac245e6966dca4f824fb6c910382" id="tgt3" class="tgtSentence">A <languageKeyword>Variant</languageKeyword> that specifies the name or ordinal position (index) of the object to delete.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ace9d9d6711c568853d975b94d5f4fd0" id="tgt4" class="tgtSentence">An error will occur if the <legacyItalic>Name</legacyItalic> does not exist in the collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="61251a29082c72556ac43ff2637ab4a2" id="tgt5" class="tgtSentence">For <legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables</legacyLink> and <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink> collections, an error will occur if the provider does not support deleting tables or users, respectively.</caps:sentence>
            <caps:sentence sentenceid="33b6484a83cf3a726991fe6704b9da17" id="tgt6" class="tgtSentence"> For <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink> and <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink> collections, <legacyBold>Delete</legacyBold> will fail if the provider does not support persisting commands.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
                  </para>
                </TD>
                <TD></TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Removes an object from a collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Collection</parameterReference>
          <legacyBold>.Delete </legacyBold>
          <parameterReference>Name</parameterReference>
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
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>Variant</languageKeyword> that specifies the name or ordinal position (index) of the object to delete.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">An error will occur if the <legacyItalic>Name</legacyItalic> does not exist in the collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">For <legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables</legacyLink> and <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink> collections, an error will occur if the provider does not support deleting tables or users, respectively.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink> and <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink> collections, <legacyBold>Delete</legacyBold> will fail if the provider does not support persisting commands.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
                  </para>
                </TD>
                <TD></TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "GetChildren Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b3f09bac-4f66-49f6-aa5a-6fbb4fb28338
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
# GetChildren Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d25b568617e3013b04114c5bc490cf02" id="tgt1" class="tgtSentence">Returns a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> whose rows represent the children of a collection <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference> recordset = record.</parameterReference>
          <legacyBold>GetChildren</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="b8e96f104fe39142afab491bc0abb587" id="tgt2" class="tgtSentence">A <legacyBold>Recordset</legacyBold> object for which each row represents a child of the current <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="720853c3c743c74ab626e5bc9652163b" id="tgt3" class="tgtSentence"> For example, the children of a <legacyBold>Record</legacyBold> that represents a directory would be the files and subdirectories contained within the parent directory.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d03e3de3fd4f6cd4b94dbd8c162ec93d" id="tgt4" class="tgtSentence">The provider determines what columns exist in the returned <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="c2691f809efc4ba4ebdf9fca2e9a27f9" id="tgt5" class="tgtSentence"> For example, a document source provider always returns a resource <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt6" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Returns a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> whose rows represent the children of a collection <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference> recordset = record.</parameterReference>
          <legacyBold>GetChildren</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <legacyBold>Recordset</legacyBold> object for which each row represents a child of the current <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> For example, the children of a <legacyBold>Record</legacyBold> that represents a directory would be the files and subdirectories contained within the parent directory.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The provider determines what columns exist in the returned <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For example, a document source provider always returns a resource <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Delete Method (ADO Parameters Collection)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 160c575e-df63-4ade-a2d3-5fd8f72e70cc
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
# Delete Method (ADO Parameters Collection)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="661a3f70f2b4945e43e995e96e69faac" id="tgt1" class="tgtSentence">Deletes an object from the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Parameters.Delete</legacyBold>
          <parameterReference>Index</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7e3038a4b387913b9ba7364277db23fd" id="tgt2" class="tgtSentence"> <legacyItalic>Index</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5e147fe861c0767308c51d3f6023e425" id="tgt3" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that contains the name of the object you want to delete, or the object's ordinal position (index) in the collection.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9e9baffdc6a68c40b2c222218338d482" id="tgt4" class="tgtSentence">Using the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method on a collection lets you remove one of the objects in the collection.</caps:sentence>
            <caps:sentence sentenceid="8661e628a90d99df7c541a02e34fae7c" id="tgt5" class="tgtSentence"> This method is available only on the <unmanagedCodeEntityReference>Parameters</unmanagedCodeEntityReference> collection of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="f685d93a86260b39581dbd5e6e9e0a02" id="tgt6" class="tgtSentence"> You must use the <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object's <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property or its collection index when calling the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method—an object variable is not a valid argument.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">Delete Method (ADO Fields Collection)</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
        <link xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Deletes an object from the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Parameters.Delete</legacyBold>
          <parameterReference>Index</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Index</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>String</languageKeyword> value that contains the name of the object you want to delete, or the object's ordinal position (index) in the collection.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Using the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method on a collection lets you remove one of the objects in the collection.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This method is available only on the <unmanagedCodeEntityReference>Parameters</unmanagedCodeEntityReference> collection of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> You must use the <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object's <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property or its collection index when calling the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method—an object variable is not a valid argument.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">Delete Method (ADO Fields Collection)</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
        <link xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
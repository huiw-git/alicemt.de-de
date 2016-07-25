---
title: "Delete Method (ADO Fields Collection)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 25bedc25-c51c-4cab-96ce-930b959965d9
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
# Delete Method (ADO Fields Collection)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e5be006650c1d79a19d5217ea2d91390" id="tgt1" class="tgtSentence">Deletes an object from the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Fields.Delete</legacyBold>
          <parameterReference>Field</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d7e78c5decb259c3b69adf485200377d" id="tgt2" class="tgtSentence"> <legacyItalic>Field</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a702e9899103e87439273c27598e901d" id="tgt3" class="tgtSentence">A <languageKeyword>Variant</languageKeyword> that designates the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object to delete.</caps:sentence>
                <caps:sentence sentenceid="4190d7a329b7d4e972973626d1fd609a" id="tgt4" class="tgtSentence"> This parameter can be the name of the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object or the ordinal position of the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object itself.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d95119c530608025bfbbf27f6bb74605" id="tgt5" class="tgtSentence">Calling the <unmanagedCodeEntityReference>Fields.Delete</unmanagedCodeEntityReference> method on an open <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> causes a run-time error.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt6" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
        <link xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Deletes an object from the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Fields.Delete</legacyBold>
          <parameterReference>Field</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Field</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>Variant</languageKeyword> that designates the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object to delete.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> This parameter can be the name of the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object or the ordinal position of the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object itself.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Calling the <unmanagedCodeEntityReference>Fields.Delete</unmanagedCodeEntityReference> method on an open <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> causes a run-time error.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
        <link xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Supports Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 298fc41c-0b55-42fc-b373-c5133b4da6a5
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
# Supports Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="007069a7e00d9d9708062074ebcd036a" id="tgt1" class="tgtSentence">Determines whether a specified <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object supports a particular type of functionality.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>boolean</parameterReference> = <parameterReference>recordset</parameterReference><legacyBold>.Supports(</legacyBold><parameterReference>CursorOptions </parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="14cffd90219b4421ce536914f5f7c8af" id="tgt2" class="tgtSentence">Returns a <languageKeyword>Boolean</languageKeyword> value that indicates whether all of the features identified by the <legacyItalic>CursorOptions</legacyItalic> argument are supported by the provider.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>CursorOptions </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a30a214f7d2830947f5ae34f51fade20" id="tgt3" class="tgtSentence">A <languageKeyword>Long</languageKeyword> expression that consists of one or more <legacyLink xlink:href="4e10cda7-ce81-4466-94c2-844d38191cf1">CursorOptionEnum</legacyLink> values.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7e76fee1e044a9eab40fcb4411dcf2b9" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method to determine what types of functionality a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports.</caps:sentence>
            <caps:sentence sentenceid="57e3e2d0986d67f22bff352f9931834b" id="tgt5" class="tgtSentence"> If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports the features whose corresponding constants are in <parameterReference>CursorOptions</parameterReference>, the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method returns <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence sentenceid="441517b080b3d23089b66e0009af68b5" id="tgt6" class="tgtSentence"> Otherwise, it returns <languageKeyword>False</languageKeyword>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="91efa1929101d93ccfdb63af349027a5" id="tgt7" class="tgtSentence">Although the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method may return <languageKeyword>True</languageKeyword> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</caps:sentence>
              <caps:sentence sentenceid="b209fcbfe9f09756010094e1e8036dda" id="tgt8" class="tgtSentence"> The <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</caps:sentence>
              <caps:sentence sentenceid="3fa75c382b2223f56a1f98cd29f1e83a" id="tgt9" class="tgtSentence"> For example, the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method may indicate that a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="135aab26-ff5c-4fd9-910f-65cdead0b47e">Visual Basic Example</link>
        <link xlink:href="6e174179-9d95-41b9-b72b-6cdbdca6e255">Visual C++ Example</link>
        <link xlink:href="eb7a5d97-0f3c-4bd4-b66d-cd1c454c4a93">Visual J++ Example</link>
        <link xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Determines whether a specified <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object supports a particular type of functionality.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>boolean</parameterReference> = <parameterReference>recordset</parameterReference><legacyBold>.Supports(</legacyBold><parameterReference>CursorOptions </parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <languageKeyword>Boolean</languageKeyword> value that indicates whether all of the features identified by the <legacyItalic>CursorOptions</legacyItalic> argument are supported by the provider.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>CursorOptions </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>Long</languageKeyword> expression that consists of one or more <legacyLink xlink:href="4e10cda7-ce81-4466-94c2-844d38191cf1">CursorOptionEnum</legacyLink> values.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method to determine what types of functionality a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports the features whose corresponding constants are in <parameterReference>CursorOptions</parameterReference>, the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method returns <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Otherwise, it returns <languageKeyword>False</languageKeyword>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src7" class="srcSentence">Although the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method may return <languageKeyword>True</languageKeyword> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> The <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> For example, the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference> method may indicate that a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="135aab26-ff5c-4fd9-910f-65cdead0b47e">Visual Basic Example</link>
        <link xlink:href="6e174179-9d95-41b9-b72b-6cdbdca6e255">Visual C++ Example</link>
        <link xlink:href="eb7a5d97-0f3c-4bd4-b66d-cd1c454c4a93">Visual J++ Example</link>
        <link xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "GetSchemaObject Method (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 36b754b4-6b17-4dd1-a925-bca46938b7c4
caps.latest.revision: 12
caps.handback.revision: 12
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
# GetSchemaObject Method (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c5fac8a7ef54a90f0a23948f352a8931" id="tgt1" class="tgtSentence">Retrieves an ADO MD schema object (<legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension</legacyLink>, <legacyLink xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy</legacyLink>, <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink>, or <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink>) by its <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>object</parameterReference> = <parameterReference>CubeDef</parameterReference>.<legacyBold>GetSchemaObject (</legacyBold><parameterReference>ObjType</parameterReference>, <parameterReference>UniqueName</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>ObjType </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f0a104e35e8696cba2afd6c230094b15" id="tgt2" class="tgtSentence">A <legacyLink xlink:href="bf53939f-5543-40ac-a707-aa35e9bde1dd">SchemaObjectTypeEnum</legacyLink> value specifying what type of schema object (Dimension, Hierarchy, Level, or Member) to retrieve.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>UniqueName </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="847cf43cc647fcd7613ac1c18cd9e33b" id="tgt3" class="tgtSentence">A <languageKeyword>String</languageKeyword> specifying the <unmanagedCodeEntityReference>UniqueName</unmanagedCodeEntityReference> property value of the object to retrieve.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b688687af50af652938bc701e5ffc351" id="tgt4" class="tgtSentence">
              <unmanagedCodeEntityReference>GetSchemaObject</unmanagedCodeEntityReference> retrieves objects using their unique names, as specified by the <unmanagedCodeEntityReference>UniqueName</unmanagedCodeEntityReference> property.</caps:sentence>
            <caps:sentence sentenceid="322413018f46d3d01cbfcf918b9b2cca" id="tgt5" class="tgtSentence"> The names of parent objects do not need to be known, and parent collections do not need to be populated to retrieve a schema object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt6" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef Object</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Retrieves an ADO MD schema object (<legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension</legacyLink>, <legacyLink xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy</legacyLink>, <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink>, or <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink>) by its <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>object</parameterReference> = <parameterReference>CubeDef</parameterReference>.<legacyBold>GetSchemaObject (</legacyBold><parameterReference>ObjType</parameterReference>, <parameterReference>UniqueName</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>ObjType </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src2" class="srcSentence">A <legacyLink xlink:href="bf53939f-5543-40ac-a707-aa35e9bde1dd">SchemaObjectTypeEnum</legacyLink> value specifying what type of schema object (Dimension, Hierarchy, Level, or Member) to retrieve.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>UniqueName </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>String</languageKeyword> specifying the <unmanagedCodeEntityReference>UniqueName</unmanagedCodeEntityReference> property value of the object to retrieve.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">
              <unmanagedCodeEntityReference>GetSchemaObject</unmanagedCodeEntityReference> retrieves objects using their unique names, as specified by the <unmanagedCodeEntityReference>UniqueName</unmanagedCodeEntityReference> property.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The names of parent objects do not need to be known, and parent collections do not need to be populated to retrieve a schema object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef Object</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
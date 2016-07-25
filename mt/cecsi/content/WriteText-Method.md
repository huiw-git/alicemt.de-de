---
title: "WriteText Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 7a669048-13f4-4574-a2b1-985e089729d5
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
# WriteText Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="389fd1c955e93b11270bd01befdda46c" id="tgt1" class="tgtSentence">Writes a specified text string to a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.WriteText</legacyBold>
          <parameterReference>Data</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Options</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="3ba365d1bbc5f56b9b06e523c3045738" id="tgt2" class="tgtSentence"> <legacyItalic>Data</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="06a64f1c37a3bff6078ee60b00851529" id="tgt3" class="tgtSentence">A <legacyBold>String</legacyBold> value that contains the text in characters to be written.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt4" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt5" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="159ab38e62c2184ca2ea501cda62ab6a" id="tgt6" class="tgtSentence"> A <legacyLink xlink:href="bdbf3405-a0bd-4f02-85d4-e3fe8da3f3f7">StreamWriteEnum</legacyLink> value that specifies whether a line separator character must be written at the end of the specified string.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="79564d8eb2b227e400d82a2c8159562f" id="tgt7" class="tgtSentence">Specified strings are written to the <legacyBold>Stream</legacyBold> object without any intervening spaces or characters between each string.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="49c3e1f283d458ff9c43a3963d273f8b" id="tgt8" class="tgtSentence">The current <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> is set to the character following the written data.</caps:sentence>
            <caps:sentence sentenceid="c1dd31802558149a331877162546d64f" id="tgt9" class="tgtSentence"> The <legacyBold>WriteText</legacyBold> method does not truncate the rest of the data in a stream.</caps:sentence>
            <caps:sentence sentenceid="be381b978f79ca750545476622b8add5" id="tgt10" class="tgtSentence"> If you want to truncate these characters, call <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4263f49bca1abdd729d4740232b9378e" id="tgt11" class="tgtSentence">If you write past the current <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink> position, the <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> of the <legacyBold>Stream</legacyBold> will be increased to contain any new characters, and <legacyBold>EOS</legacyBold> will move to the new last byte in the <legacyBold>Stream</legacyBold>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="7f9beb0307e5098ae1ee97e5f9c93718" id="tgt12" class="tgtSentence">The <legacyBold>WriteText</legacyBold> method is used with text streams (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
              <caps:sentence sentenceid="a6f47978e371b209fbd0f59a0fbed41f" id="tgt13" class="tgtSentence"> For binary streams (<legacyBold>Type</legacyBold> is <legacyBold>adTypeBinary</legacyBold>), use <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Writes a specified text string to a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.WriteText</legacyBold>
          <parameterReference>Data</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Options</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Data</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <legacyBold>String</legacyBold> value that contains the text in characters to be written.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> A <legacyLink xlink:href="bdbf3405-a0bd-4f02-85d4-e3fe8da3f3f7">StreamWriteEnum</legacyLink> value that specifies whether a line separator character must be written at the end of the specified string.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">Specified strings are written to the <legacyBold>Stream</legacyBold> object without any intervening spaces or characters between each string.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The current <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> is set to the character following the written data.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The <legacyBold>WriteText</legacyBold> method does not truncate the rest of the data in a stream.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> If you want to truncate these characters, call <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If you write past the current <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink> position, the <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> of the <legacyBold>Stream</legacyBold> will be increased to contain any new characters, and <legacyBold>EOS</legacyBold> will move to the new last byte in the <legacyBold>Stream</legacyBold>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src12" class="srcSentence">The <legacyBold>WriteText</legacyBold> method is used with text streams (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> For binary streams (<legacyBold>Type</legacyBold> is <legacyBold>adTypeBinary</legacyBold>), use <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
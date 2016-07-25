---
title: "Read Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 838502de-80f1-4eeb-8838-dd3d9403e567
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
# Read Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="edcfd1033891a806776859e7d15d1717" id="tgt1" class="tgtSentence">Reads a specified number of bytes from a binary <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Variant = Stream</parameterReference>
          <legacyBold>.Read ( </legacyBold>
          <parameterReference>NumBytes</parameterReference>
          <legacyBold>)</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="8ca4fca3013e7e7836f43f4132259aaf" id="tgt2" class="tgtSentence"> <legacyItalic>NumBytes</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="0f9e3cc3202631e0ed2d86fe45632f68" id="tgt4" class="tgtSentence"> A <legacyBold>Long</legacyBold> value that specifies the number of bytes to read from the file or the <legacyLink xlink:href="cfa1b416-003a-436f-a21b-bd2397e54db3">StreamReadEnum</legacyLink> value <legacyBold>adReadAll</legacyBold>, which is the default.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="d1d7f9a0cbb114084de72a682a9e962a" id="tgt5" class="tgtSentence">The <legacyBold>Read </legacyBold>method reads a specified number of bytes or the entire stream from a <legacyBold>Stream</legacyBold> object and returns the resulting data as a <legacyBold>Variant</legacyBold>.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4a51f5750de717ef88d86796e38a1689" id="tgt6" class="tgtSentence">If <legacyItalic>NumBytes</legacyItalic> is more than the number of bytes left in the <legacyBold>Stream</legacyBold>, only the bytes remaining are returned.</caps:sentence>
            <caps:sentence sentenceid="a709f0cddb5b813147e8f2fb0268423a" id="tgt7" class="tgtSentence"> The data read is not padded to match the length specified by <legacyItalic>NumBytes</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="45f7babef24a8bf1ccd73f36f0693792" id="tgt8" class="tgtSentence"> If there are no bytes left to read, a variant with a null value is returned.</caps:sentence>
            <caps:sentence sentenceid="3de8b4adec4c9b66ba5403d1d59107f4" id="tgt9" class="tgtSentence">
              <legacyBold>Read</legacyBold> cannot be used to read backwards.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="8542475c084726e07496dc71ed24fb1a" id="tgt10" class="tgtSentence"> <legacyItalic>NumBytes</legacyItalic> always measures bytes.</caps:sentence>
              <caps:sentence sentenceid="9467ec017e32a23d9b08301c95b67313" id="tgt11" class="tgtSentence"> For text <legacyBold>Stream</legacyBold> objects (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>), use <legacyLink xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">ReadText</legacyLink>.</caps:sentence>
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
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">ReadText Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Reads a specified number of bytes from a binary <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Variant = Stream</parameterReference>
          <legacyBold>.Read ( </legacyBold>
          <parameterReference>NumBytes</parameterReference>
          <legacyBold>)</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>NumBytes</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A <legacyBold>Long</legacyBold> value that specifies the number of bytes to read from the file or the <legacyLink xlink:href="cfa1b416-003a-436f-a21b-bd2397e54db3">StreamReadEnum</legacyLink> value <legacyBold>adReadAll</legacyBold>, which is the default.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The <legacyBold>Read </legacyBold>method reads a specified number of bytes or the entire stream from a <legacyBold>Stream</legacyBold> object and returns the resulting data as a <legacyBold>Variant</legacyBold>.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">If <legacyItalic>NumBytes</legacyItalic> is more than the number of bytes left in the <legacyBold>Stream</legacyBold>, only the bytes remaining are returned.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The data read is not padded to match the length specified by <legacyItalic>NumBytes</legacyItalic>.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> If there are no bytes left to read, a variant with a null value is returned.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence">
              <legacyBold>Read</legacyBold> cannot be used to read backwards.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>NumBytes</legacyItalic> always measures bytes.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> For text <legacyBold>Stream</legacyBold> objects (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>), use <legacyLink xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">ReadText</legacyLink>.</caps:sentence>
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
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">ReadText Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
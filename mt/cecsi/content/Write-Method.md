---
title: "Write Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 02982e6a-ac5f-4af2-b82e-ce12534b84b2
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
# Write Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9a7734aab8dece8e5d8e68cac78b8f78" id="tgt1" class="tgtSentence">Writes binary data to a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.Write</legacyBold>
          <parameterReference>Buffer</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="a4cc9f846c66106f7ab4e59dfba4de66" id="tgt2" class="tgtSentence"> <legacyItalic>Buffer</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="bd4b40585b20f9d8e603d9dd6643e5a6" id="tgt3" class="tgtSentence">A <languageKeyword>Variant</languageKeyword> that contains an array of bytes to be written.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="f2a7b750cb6813fa429238010ebbc54d" id="tgt4" class="tgtSentence">Specified bytes are written to the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object without any intervening spaces between each byte.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e30516a2921f003635cd16148c4a9ddf" id="tgt5" class="tgtSentence">The current <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> is set to the byte following the written data.</caps:sentence>
            <caps:sentence sentenceid="9f0e9f347f08138c2f6fc151e3648155" id="tgt6" class="tgtSentence"> The <unmanagedCodeEntityReference>Write</unmanagedCodeEntityReference> method does not truncate the rest of the data in a stream.</caps:sentence>
            <caps:sentence sentenceid="3f3ae87fac651ad6a31ae252038555a6" id="tgt7" class="tgtSentence"> If you want to truncate these bytes, call <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dff450529115142a4df4633ec9dae9ab" id="tgt8" class="tgtSentence">If you write past the current <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink> position, the <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> will be increased to contain any new bytes, and <unmanagedCodeEntityReference>EOS</unmanagedCodeEntityReference> will move to the new last byte in the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="efcf769b2b3320c2acaa200b3dd03f2f" id="tgt9" class="tgtSentence">The <unmanagedCodeEntityReference>Write</unmanagedCodeEntityReference> method is used with binary streams (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeBinary</legacyBold>).</caps:sentence>
              <caps:sentence sentenceid="2ac02ddc0cb281f429cf0adac5506dfe" id="tgt10" class="tgtSentence"> For text streams (<legacyBold>Type</legacyBold> is <legacyBold>adTypeText</legacyBold>), use <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt11" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Writes binary data to a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.Write</legacyBold>
          <parameterReference>Buffer</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Buffer</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>Variant</languageKeyword> that contains an array of bytes to be written.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Specified bytes are written to the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object without any intervening spaces between each byte.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">The current <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> is set to the byte following the written data.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The <unmanagedCodeEntityReference>Write</unmanagedCodeEntityReference> method does not truncate the rest of the data in a stream.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If you want to truncate these bytes, call <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">If you write past the current <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink> position, the <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> will be increased to contain any new bytes, and <unmanagedCodeEntityReference>EOS</unmanagedCodeEntityReference> will move to the new last byte in the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src9" class="srcSentence">The <unmanagedCodeEntityReference>Write</unmanagedCodeEntityReference> method is used with binary streams (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeBinary</legacyBold>).</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> For text streams (<legacyBold>Type</legacyBold> is <legacyBold>adTypeText</legacyBold>), use <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
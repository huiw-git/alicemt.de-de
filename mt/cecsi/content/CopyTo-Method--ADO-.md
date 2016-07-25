---
title: "CopyTo Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b4aa5714-916b-48b8-8b09-cc2708379602
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
# CopyTo Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f108b6e922d391457c77ab583e82b7aa" id="tgt1" class="tgtSentence">Copies the specified number of characters or bytes (depending on <legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink>) in the <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> to another <legacyBold>Stream</legacyBold> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.CopyTo</legacyBold>
          <parameterReference>DestStream</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>NumChars</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="028c2b8697b157dc8c789b24f285d080" id="tgt2" class="tgtSentence"> <legacyItalic>DestStream</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="6d5e73638148859eb8374a63516519ac" id="tgt3" class="tgtSentence">An object variable value that contains a reference to an open <legacyBold>Stream</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="54d2a6f278dce73e59e23a4d7711a683" id="tgt4" class="tgtSentence"> The current <legacyBold>Stream</legacyBold> is copied to the destination <legacyBold>Stream</legacyBold> specified by <legacyItalic>DestStream</legacyItalic>.</caps:sentence>
                <caps:sentence sentenceid="8d10ce121a355ab5d030739138933365" id="tgt5" class="tgtSentence"> The destination <legacyBold>Stream</legacyBold> must already be open.</caps:sentence>
                <caps:sentence sentenceid="1661638ab3ef875f7ebffd14e3ed40b6" id="tgt6" class="tgtSentence"> If not, a run-time error occurs.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="739cd8beb133048b912a9811b8a98b28" id="tgt7" class="tgtSentence">The <legacyItalic>DestStream</legacyItalic> parameter may not be a proxy of <legacyBold>Stream</legacyBold> object because this requires access to a private interface on the <legacyBold>Stream</legacyBold> object that cannot be remoted to the client.</caps:sentence>
                </para>
              </alert>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8a44f34955fc9bcb05b93f7af901420f" id="tgt8" class="tgtSentence"> <legacyItalic>NumChars</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt9" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="cd9e1dfa2d6bc7c3a9a771f787f84135" id="tgt10" class="tgtSentence"> An <languageKeyword>Integer</languageKeyword> value that specifies the number of bytes or characters to be copied from the current position in the source <legacyBold>Stream</legacyBold> to the destination <legacyBold>Stream</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="9097152625c80d8cb1c6eb499a77e2b6" id="tgt11" class="tgtSentence"> The default value is –1, which specifies that all characters or bytes are copied from the current position to <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="a02e7b33e60c8f929606d557f45b76f0" id="tgt12" class="tgtSentence">This method copies the specified number of characters or bytes, starting from the current position specified by the <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> property.</caps:sentence>
            <caps:sentence sentenceid="2ae91a601de56a1be580a3e2e0a7b208" id="tgt13" class="tgtSentence"> If the specified number is more than the available number of bytes until <legacyBold>EOS</legacyBold>, then only characters or bytes from the current position to <legacyBold>EOS</legacyBold> are copied.</caps:sentence>
            <caps:sentence sentenceid="357b6c47cb4b883c13a26ebcf9fbe146" id="tgt14" class="tgtSentence"> If the value of <legacyItalic>NumChars </legacyItalic>is –1, or omitted, all characters or bytes starting from the current position are copied.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="959b350e2e2f139de0795c4b83edee54" id="tgt15" class="tgtSentence">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated.</caps:sentence>
            <caps:sentence sentenceid="fda09e8cdc2f102c5fbb0107ced727f9" id="tgt16" class="tgtSentence">
              <legacyBold>Position</legacyBold> becomes the byte immediately following the last byte copied.</caps:sentence>
            <caps:sentence sentenceid="3f3ae87fac651ad6a31ae252038555a6" id="tgt17" class="tgtSentence"> If you want to truncate these bytes, call <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="432490f29f729662cadcfe627c703ad0" id="tgt18" class="tgtSentence">
              <legacyBold>CopyTo</legacyBold> should be used to copy data to a destination <legacyBold>Stream</legacyBold> of the same type as the source <legacyBold>Stream</legacyBold> (their <legacyBold>Type</legacyBold> property settings are both <legacyBold>adTypeText</legacyBold> or both <legacyBold>adTypeBinary</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="e4c25343f6e854e9d93cd28c9096b62d" id="tgt19" class="tgtSentence"> For text <legacyBold>Stream</legacyBold> objects, you can change the <legacyLink xlink:href="e42507cb-9b46-4ce4-8191-2948eaf14ca2">Charset</legacyLink> property setting of the destination <legacyBold>Stream</legacyBold> to translate from one character set to another.</caps:sentence>
            <caps:sentence sentenceid="d33bba57f4737582c12426926cc1396a" id="tgt20" class="tgtSentence"> Also, text <legacyBold>Stream</legacyBold> objects can be successfully copied into binary <legacyBold>Stream</legacyBold> objects, but binary <legacyBold>Stream</legacyBold> objects cannot be copied into text <legacyBold>Stream</legacyBold> objects.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt21" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Copies the specified number of characters or bytes (depending on <legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink>) in the <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> to another <legacyBold>Stream</legacyBold> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.CopyTo</legacyBold>
          <parameterReference>DestStream</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>NumChars</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>DestStream</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">An object variable value that contains a reference to an open <legacyBold>Stream</legacyBold> object.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> The current <legacyBold>Stream</legacyBold> is copied to the destination <legacyBold>Stream</legacyBold> specified by <legacyItalic>DestStream</legacyItalic>.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> The destination <legacyBold>Stream</legacyBold> must already be open.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> If not, a run-time error occurs.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src7" class="srcSentence">The <legacyItalic>DestStream</legacyItalic> parameter may not be a proxy of <legacyBold>Stream</legacyBold> object because this requires access to a private interface on the <legacyBold>Stream</legacyBold> object that cannot be remoted to the client.</caps:sentence>
                </para>
              </alert>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>NumChars</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> An <languageKeyword>Integer</languageKeyword> value that specifies the number of bytes or characters to be copied from the current position in the source <legacyBold>Stream</legacyBold> to the destination <legacyBold>Stream</legacyBold>.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> The default value is –1, which specifies that all characters or bytes are copied from the current position to <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">This method copies the specified number of characters or bytes, starting from the current position specified by the <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> property.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> If the specified number is more than the available number of bytes until <legacyBold>EOS</legacyBold>, then only characters or bytes from the current position to <legacyBold>EOS</legacyBold> are copied.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> If the value of <legacyItalic>NumChars </legacyItalic>is –1, or omitted, all characters or bytes starting from the current position are copied.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence">
              <legacyBold>Position</legacyBold> becomes the byte immediately following the last byte copied.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> If you want to truncate these bytes, call <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">
              <legacyBold>CopyTo</legacyBold> should be used to copy data to a destination <legacyBold>Stream</legacyBold> of the same type as the source <legacyBold>Stream</legacyBold> (their <legacyBold>Type</legacyBold> property settings are both <legacyBold>adTypeText</legacyBold> or both <legacyBold>adTypeBinary</legacyBold>).</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> For text <legacyBold>Stream</legacyBold> objects, you can change the <legacyLink xlink:href="e42507cb-9b46-4ce4-8191-2948eaf14ca2">Charset</legacyLink> property setting of the destination <legacyBold>Stream</legacyBold> to translate from one character set to another.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Also, text <legacyBold>Stream</legacyBold> objects can be successfully copied into binary <legacyBold>Stream</legacyBold> objects, but binary <legacyBold>Stream</legacyBold> objects cannot be copied into text <legacyBold>Stream</legacyBold> objects.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "SkipLine Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 0abc00fe-ee09-4c8e-b1f2-48ee9c5f3329
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
# SkipLine Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d090fc163569f3b60f4ccae59a4afaf8" id="tgt1" class="tgtSentence">Skips one entire line when reading a text <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>.<legacyBold>SkipLine</legacyBold></legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="00c04583d293218555402e2db484db18" id="tgt2" class="tgtSentence">All characters up to and including the next line separator are skipped.</caps:sentence>
            <caps:sentence sentenceid="7d9173e3d8d93bcf9ecf4c18aecad95a" id="tgt3" class="tgtSentence"> By default, the <legacyLink xlink:href="0b20fbb8-6b83-48ec-b442-f96c8a4bafbb">LineSeparator</legacyLink> is <legacyBold>adCRLF</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="76ed9d97eccae73513bfd1d33fca7942" id="tgt4" class="tgtSentence"> If you attempt to skip past <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink>, the current position will remain at <unmanagedCodeEntityReference>EOS</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="668c05fcd771de9cae297119d528145e" id="tgt5" class="tgtSentence">The <unmanagedCodeEntityReference>SkipLine</unmanagedCodeEntityReference> method is used with text streams (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt6" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
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
          <caps:sentence id="src1" class="srcSentence">Skips one entire line when reading a text <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>.<legacyBold>SkipLine</legacyBold></legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">All characters up to and including the next line separator are skipped.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> By default, the <legacyLink xlink:href="0b20fbb8-6b83-48ec-b442-f96c8a4bafbb">LineSeparator</legacyLink> is <legacyBold>adCRLF</legacyBold>.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> If you attempt to skip past <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink>, the current position will remain at <unmanagedCodeEntityReference>EOS</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">The <unmanagedCodeEntityReference>SkipLine</unmanagedCodeEntityReference> method is used with text streams (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
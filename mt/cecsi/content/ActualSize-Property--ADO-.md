---
title: "ActualSize Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 722803d0-cef5-4d4c-b79d-3f2f58052229
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
# ActualSize Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5ec85ba9a0ef9f20eabd39bb4ed0f964" id="tgt1" class="tgtSentence">Indicates the actual length of a field’s value in bytes.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0642a3db1d38d0a78e50a544b500b3e2" id="tgt3" class="tgtSentence">Returns a <legacyBold>Long</legacyBold> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="fed3e2a6f7bf6332d17473e5d1457f72" id="tgt4" class="tgtSentence">Use the <legacyBold>ActualSize</legacyBold> property to return the actual length of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object's value.</caps:sentence>
            <caps:sentence sentenceid="53564252c1c08e7f138fab1e8bb68bc5" id="tgt5" class="tgtSentence"> For all fields, the <legacyBold>ActualSize</legacyBold> property is read-only.</caps:sentence>
            <caps:sentence sentenceid="79acffd43cc12809fad5b9d3cc4908db" id="tgt6" class="tgtSentence"> If ADO cannot determine the length of the <legacyBold>Field</legacyBold> object's value, the <legacyBold>ActualSize</legacyBold> property returns <legacyBold>adUnknown</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="455c0d1179b023bb1b739b42552d6be0" id="tgt7" class="tgtSentence">The <legacyBold>ActualSize</legacyBold> and <legacyLink xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize</legacyLink> properties are different, as shown in the following example.</caps:sentence>
            <caps:sentence sentenceid="b95f68ae148cc8467e185be147466c10" id="tgt8" class="tgtSentence"> A <legacyBold>Field</legacyBold> object with a declared type of <legacyBold>adVarChar</legacyBold> and a maximum length of 50 characters returns a <legacyBold>DefinedSize</legacyBold> property value of 50, but the <legacyBold>ActualSize</legacyBold> property value it returns is the length of the data stored in the field for the current record.</caps:sentence>
            <caps:sentence sentenceid="527dd57a077e40d8474127469f188e1b" id="tgt9" class="tgtSentence">
              <legacyBold>Fields</legacyBold> with a <legacyBold>DefinedSize</legacyBold> greater than 255 bytes are treated as variable length columns.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bff2c273-b535-4b32-83b3-0336a406859c">Visual Basic Example</link>
        <link xlink:href="05f7cc97-b806-41d2-939d-a955d10844c4">Visual C++ Example</link>
        <link xlink:href="2a0936e6-6452-4fef-9295-50407a13d691">Visual J++ Example</link>
        <link xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the actual length of a field’s value in bytes.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyBold>Long</legacyBold> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>ActualSize</legacyBold> property to return the actual length of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object's value.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For all fields, the <legacyBold>ActualSize</legacyBold> property is read-only.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> If ADO cannot determine the length of the <legacyBold>Field</legacyBold> object's value, the <legacyBold>ActualSize</legacyBold> property returns <legacyBold>adUnknown</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <legacyBold>ActualSize</legacyBold> and <legacyLink xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize</legacyLink> properties are different, as shown in the following example.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> A <legacyBold>Field</legacyBold> object with a declared type of <legacyBold>adVarChar</legacyBold> and a maximum length of 50 characters returns a <legacyBold>DefinedSize</legacyBold> property value of 50, but the <legacyBold>ActualSize</legacyBold> property value it returns is the length of the data stored in the field for the current record.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence">
              <legacyBold>Fields</legacyBold> with a <legacyBold>DefinedSize</legacyBold> greater than 255 bytes are treated as variable length columns.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bff2c273-b535-4b32-83b3-0336a406859c">Visual Basic Example</link>
        <link xlink:href="05f7cc97-b806-41d2-939d-a955d10844c4">Visual C++ Example</link>
        <link xlink:href="2a0936e6-6452-4fef-9295-50407a13d691">Visual J++ Example</link>
        <link xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
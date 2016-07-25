---
title: "NumericScale Property (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 573ee5d1-57c7-4a27-be79-a0e12944ad9b
caps.latest.revision: 10
caps.handback.revision: 10
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
# NumericScale Property (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a7f719e87575c6d4be2991bf178cdcb6" id="tgt1" class="tgtSentence">Indicates the scale of a numeric value in the column.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a6a9efc3be12b86e3a364ddfb45ff809" id="tgt3" class="tgtSentence">Sets and returns a <legacyBold>Byte</legacyBold> value that is the scale of data values in the column when the <legacyLink xlink:href="5c6718b6-f728-478a-8afb-5d17b0a91d1f">Type</legacyLink> property is <legacyBold>adNumeric</legacyBold> or <legacyBold>adDecimal</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="2d4df34f8d81a785ef3c9d3a076d2fc0" id="tgt4" class="tgtSentence">
              <legacyBold>NumericScale</legacyBold> is ignored for all other data types.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="99c4521c5ccd0cc5fa60793838d3728d" id="tgt5" class="tgtSentence">The default value is zero (0).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="602220c07727570d372e5a6fa110e0f2" id="tgt6" class="tgtSentence">
              <legacyBold>NumericScale</legacyBold> is read-only for <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects already appended to a collection.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ea2ec614-34c8-41b7-8ebd-063798bd56b4">ADOX Code Example: NumericScale and Precision Properties Example (VB)</link>
        <link xlink:href="5c6718b6-f728-478a-8afb-5d17b0a91d1f">Type Property (Column)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the scale of a numeric value in the column.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets and returns a <legacyBold>Byte</legacyBold> value that is the scale of data values in the column when the <legacyLink xlink:href="5c6718b6-f728-478a-8afb-5d17b0a91d1f">Type</legacyLink> property is <legacyBold>adNumeric</legacyBold> or <legacyBold>adDecimal</legacyBold>.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence">
              <legacyBold>NumericScale</legacyBold> is ignored for all other data types.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The default value is zero (0).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">
              <legacyBold>NumericScale</legacyBold> is read-only for <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects already appended to a collection.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ea2ec614-34c8-41b7-8ebd-063798bd56b4">ADOX Code Example: NumericScale and Precision Properties Example (VB)</link>
        <link xlink:href="5c6718b6-f728-478a-8afb-5d17b0a91d1f">Type Property (Column)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
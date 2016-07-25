---
title: "Precision Property (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 0e0ecbbf-d7de-49d4-a128-5a519ecd54ba
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
# Precision Property (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="78a3134a6b36a0f69f98e791c7e59920" id="tgt1" class="tgtSentence">Indicates the maximum precision of data values in the <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="46f8f93c41b1c6c53186b92b26887f66" id="tgt3" class="tgtSentence">Sets and returns a <languageKeyword>Long</languageKeyword> value that is the maximum precision of data values in the column when the <legacyLink xlink:href="5c6718b6-f728-478a-8afb-5d17b0a91d1f">Type</legacyLink> property is a numeric type.</caps:sentence>
            <caps:sentence sentenceid="8bfa994eaaae5e39929713ab91bf1f83" id="tgt4" class="tgtSentence">
              <legacyBold>Precision</legacyBold> is ignored for all other data types.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d2da731bc79fb2323f4ff4830320e0f0" id="tgt5" class="tgtSentence">The default value is zero (<legacyBold>0</legacyBold>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="76027cb29c7c78e70106847618b687e9" id="tgt6" class="tgtSentence">This property is read-only for <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects already appended to a collection.</caps:sentence>
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
        <link xlink:href="ea2ec614-34c8-41b7-8ebd-063798bd56b4">NumericScale and Precision Properties Example (VB)</link>
        <link xlink:href="5c6718b6-f728-478a-8afb-5d17b0a91d1f">Type Property (Column)</link>
        <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the maximum precision of data values in the <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets and returns a <languageKeyword>Long</languageKeyword> value that is the maximum precision of data values in the column when the <legacyLink xlink:href="5c6718b6-f728-478a-8afb-5d17b0a91d1f">Type</legacyLink> property is a numeric type.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence">
              <legacyBold>Precision</legacyBold> is ignored for all other data types.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The default value is zero (<legacyBold>0</legacyBold>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">This property is read-only for <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects already appended to a collection.</caps:sentence>
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
        <link xlink:href="ea2ec614-34c8-41b7-8ebd-063798bd56b4">NumericScale and Precision Properties Example (VB)</link>
        <link xlink:href="5c6718b6-f728-478a-8afb-5d17b0a91d1f">Type Property (Column)</link>
        <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
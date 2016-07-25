---
title: "SortOrder Property (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 04510b19-9cb2-4895-b23b-f7790123eb04
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
# SortOrder Property (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ae044017b675021a539cdb12d4ed3348" id="tgt1" class="tgtSentence">Indicates the sort sequence for the column (index columns only).</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="822ba4bf83d7f995bc298d011265207f" id="tgt3" class="tgtSentence">Sets and returns a <languageKeyword>Long</languageKeyword> value that can be one of the <legacyLink xlink:href="0b9d46e7-29d9-4ca1-a23a-056403106a71">SortOrderEnum</legacyLink> constants.</caps:sentence>
            <caps:sentence sentenceid="81271704f27a0a3835d28b1fcf569140" id="tgt4" class="tgtSentence"> The default value is <legacyBold>adSortAscending</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="f314a9a45b362a04a1eaffaf7280333b" id="tgt5" class="tgtSentence">This property only applies to <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects in the <legacyLink xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns</legacyLink> collection of an <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt6" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d9502254-d89b-4bcb-94f1-6418f89e7f30">SortOrder Property Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
        <link xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the sort sequence for the column (index columns only).</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets and returns a <languageKeyword>Long</languageKeyword> value that can be one of the <legacyLink xlink:href="0b9d46e7-29d9-4ca1-a23a-056403106a71">SortOrderEnum</legacyLink> constants.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>adSortAscending</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">This property only applies to <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects in the <legacyLink xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns</legacyLink> collection of an <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d9502254-d89b-4bcb-94f1-6418f89e7f30">SortOrder Property Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
        <link xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
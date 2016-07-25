---
title: "ADOX Object Model"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 31c0781c-96c8-4460-90ea-134066154fc7
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
# ADOX Object Model
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3f32789811cb2062edf43614b8f3c4bc" id="tgt1" class="tgtSentence">The following diagram illustrates how objects are represented and related in ADOX.</caps:sentence>
          <caps:sentence sentenceid="6e31f1c51244efc0f6047366b0e95d37" id="tgt2" class="tgtSentence"> For more information about a specific object or collection, see the specific reference topic, or <legacyLink xlink:href="3f5287e9-f62c-40c4-bb59-985102be956e">ADOX Objects</legacyLink> and <legacyLink xlink:href="c0c90ba9-0471-4381-96f1-376de22fa2ee">ADOX Collections</legacyLink>.</caps:sentence>
        </para>
        <mediaLink>
          <image xlink:href="239a4b23-e529-41a4-b4c2-3495dd313202"></image>
        </mediaLink>
        <para>
          <caps:sentence sentenceid="60544ebaf246ad4cc6c7c8b65e566e0d" id="tgt3" class="tgtSentence">Each of the <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink>, <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink>, and <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects also has a standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef700465-2e97-46e8-8213-2d662501e540">ADOX API Reference</link>
        <link xlink:href="438e4369-f7e8-4dca-a709-dd501a3ca83f">ADOX Code Examples</link>
        <link xlink:href="c0c90ba9-0471-4381-96f1-376de22fa2ee">ADOX Collections</link>
        <link xlink:href="9d91f511-d46f-44ef-97ef-77bf93836186">ADOX Enumerated Constants</link>
        <link xlink:href="8de11ef7-034c-4613-91df-2244171f0b9a">ADOX Methods</link>
        <link xlink:href="3f5287e9-f62c-40c4-bb59-985102be956e">ADOX Objects</link>
        <link xlink:href="2ddf19e4-312e-4d21-8053-a6fc4b738ad4">ADOX Properties</link>
        <link xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">Microsoft ADOX Programmer's Reference</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following diagram illustrates how objects are represented and related in ADOX.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For more information about a specific object or collection, see the specific reference topic, or <legacyLink xlink:href="3f5287e9-f62c-40c4-bb59-985102be956e">ADOX Objects</legacyLink> and <legacyLink xlink:href="c0c90ba9-0471-4381-96f1-376de22fa2ee">ADOX Collections</legacyLink>.</caps:sentence>
        </para>
        <mediaLink>
          <image xlink:href="239a4b23-e529-41a4-b4c2-3495dd313202"></image>
        </mediaLink>
        <para>
          <caps:sentence id="src3" class="srcSentence">Each of the <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink>, <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink>, and <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects also has a standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef700465-2e97-46e8-8213-2d662501e540">ADOX API Reference</link>
        <link xlink:href="438e4369-f7e8-4dca-a709-dd501a3ca83f">ADOX Code Examples</link>
        <link xlink:href="c0c90ba9-0471-4381-96f1-376de22fa2ee">ADOX Collections</link>
        <link xlink:href="9d91f511-d46f-44ef-97ef-77bf93836186">ADOX Enumerated Constants</link>
        <link xlink:href="8de11ef7-034c-4613-91df-2244171f0b9a">ADOX Methods</link>
        <link xlink:href="3f5287e9-f62c-40c4-bb59-985102be956e">ADOX Objects</link>
        <link xlink:href="2ddf19e4-312e-4d21-8053-a6fc4b738ad4">ADOX Properties</link>
        <link xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">Microsoft ADOX Programmer's Reference</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
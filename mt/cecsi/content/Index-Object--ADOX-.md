---
title: "Index Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6b9578c0-bc94-46b9-b801-c18e14b04b31
caps.latest.revision: 9
caps.handback.revision: 9
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
# Index Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a4465b6187b6bbd70f419a8ca30a51ef" id="tgt1" class="tgtSentence">Represents an index from a database table.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b4de2c6f39d715a517b31c4452437689" id="tgt2" class="tgtSentence">The following code creates a new <legacyBold>Index</legacyBold>:</caps:sentence>
          </para>
          <code>Dim obj As New Index</code>
          <para>
            <caps:sentence sentenceid="be364be6a292563ddb20b557ea43d8ee" id="tgt3" class="tgtSentence">With the properties and collections of an <legacyBold>Index</legacyBold> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="ae70ae028a84a4534b11c71f0a45b6ad" id="tgt4" class="tgtSentence">Identify the index with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="33498517df6484475e9b72be21a65e75" id="tgt5" class="tgtSentence">Access the database columns of the index with the <legacyLink xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3c5b70d99df3ea3ecb7419f64a90a48d" id="tgt6" class="tgtSentence">Specify whether the index keys must be unique with the <legacyLink xlink:href="85fd4bd0-393b-4dc1-9d73-80dced4f2fbe">Unique</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a9c55865643ed4ece42761e3990b70e5" id="tgt7" class="tgtSentence">Specify whether the index is the primary key for a table with the <legacyLink xlink:href="30185312-5e09-4804-852d-e505d660113a">PrimaryKey</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6e509ee799c704bd7287b88499c077e4" id="tgt8" class="tgtSentence">Specify whether records that have null values in their index fields have index entries with the <legacyLink xlink:href="313b0bf7-3f37-4823-8fca-bd9c80e078a7">IndexNulls</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="21e253e059358d1ee2a59f6ba57f71e4" id="tgt9" class="tgtSentence">Specify whether the index is clustered with the <legacyLink xlink:href="9b62fb35-de43-425a-83ca-77af4e33fea9">Clustered</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2c355542be3baa589e8cf6b0f4a8104f" id="tgt10" class="tgtSentence">Access provider-specific index properties with the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="5714b5a99cb008753e4f66d62c157e69" id="tgt11" class="tgtSentence">An error will occur when appending a <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> to the <legacyBold>Columns</legacyBold> collection of an <legacyBold>Index</legacyBold> if the <legacyBold>Column</legacyBold> does not exist in a <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink> object already appended to the <legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables</legacyLink> collection.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="29de35a46a55dfbf538bab320c74a0c2" id="tgt12" class="tgtSentence">Your data provider may not support all properties of <legacyBold>Index</legacyBold> objects.</caps:sentence>
              <caps:sentence sentenceid="723040a8fa0fdf80590c80c4481e3f55" id="tgt13" class="tgtSentence"> An error will occur if you have set a value for a property that is not supported by the provider.</caps:sentence>
              <caps:sentence sentenceid="008deb004bd824d23abe4c9226ab3313" id="tgt14" class="tgtSentence"> For new <legacyBold>Index</legacyBold> objects, the error will occur when the object is appended to the collection.</caps:sentence>
              <caps:sentence sentenceid="75f584dc269e8644adb6e3125f193185" id="tgt15" class="tgtSentence"> For existing objects, the error will occur when setting the property.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="90ee75035765b81a8ba0b59e7c45b76c" id="tgt16" class="tgtSentence">When creating <legacyBold>Index</legacyBold> objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</caps:sentence>
              <caps:sentence sentenceid="2ad1596882d2bb3dea74288c43cc341a" id="tgt17" class="tgtSentence"> For more information about which properties your provider supports, see your provider documentation.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt18" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="5360dc663b19018a2c072ad9ad1298da" id="tgt19" class="tgtSentence">
                  <legacyLink xlink:href="6f4e92e1-e7cb-45d8-aa86-cd749474f825">Index Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="50f87e27-1bf9-427c-9b1d-704a672434d2">Indexes Append Method Example (VB)</link>
        <link xlink:href="45204669-32c0-4690-aab9-ddf0fd71ae48">IndexNulls Property Example (VB)</link>
        <link xlink:href="f536acac-06ea-4b39-bfba-ee9902b01615">PrimaryKey and Unique Properties Example (VB)</link>
        <link xlink:href="d9502254-d89b-4bcb-94f1-6418f89e7f30">SortOrder Property Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
        <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents an index from a database table.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The following code creates a new <legacyBold>Index</legacyBold>:</caps:sentence>
          </para>
          <code>Dim obj As New Index</code>
          <para>
            <caps:sentence id="src3" class="srcSentence">With the properties and collections of an <legacyBold>Index</legacyBold> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Identify the index with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Access the database columns of the index with the <legacyLink xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Specify whether the index keys must be unique with the <legacyLink xlink:href="85fd4bd0-393b-4dc1-9d73-80dced4f2fbe">Unique</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Specify whether the index is the primary key for a table with the <legacyLink xlink:href="30185312-5e09-4804-852d-e505d660113a">PrimaryKey</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Specify whether records that have null values in their index fields have index entries with the <legacyLink xlink:href="313b0bf7-3f37-4823-8fca-bd9c80e078a7">IndexNulls</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Specify whether the index is clustered with the <legacyLink xlink:href="9b62fb35-de43-425a-83ca-77af4e33fea9">Clustered</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Access provider-specific index properties with the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src11" class="srcSentence">An error will occur when appending a <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> to the <legacyBold>Columns</legacyBold> collection of an <legacyBold>Index</legacyBold> if the <legacyBold>Column</legacyBold> does not exist in a <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink> object already appended to the <legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables</legacyLink> collection.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src12" class="srcSentence">Your data provider may not support all properties of <legacyBold>Index</legacyBold> objects.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> An error will occur if you have set a value for a property that is not supported by the provider.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> For new <legacyBold>Index</legacyBold> objects, the error will occur when the object is appended to the collection.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> For existing objects, the error will occur when setting the property.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src16" class="srcSentence">When creating <legacyBold>Index</legacyBold> objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> For more information about which properties your provider supports, see your provider documentation.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src18" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">
                  <legacyLink xlink:href="6f4e92e1-e7cb-45d8-aa86-cd749474f825">Index Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="50f87e27-1bf9-427c-9b1d-704a672434d2">Indexes Append Method Example (VB)</link>
        <link xlink:href="45204669-32c0-4690-aab9-ddf0fd71ae48">IndexNulls Property Example (VB)</link>
        <link xlink:href="f536acac-06ea-4b39-bfba-ee9902b01615">PrimaryKey and Unique Properties Example (VB)</link>
        <link xlink:href="d9502254-d89b-4bcb-94f1-6418f89e7f30">SortOrder Property Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
        <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Key Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 55f116fe-4d56-4892-bffe-0cdd6fc727c9
caps.latest.revision: 8
caps.handback.revision: 8
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
# Key Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7aeb517d9c7f3078a9e4340e4508a506" id="tgt1" class="tgtSentence">Represents a primary, foreign, or unique key field from a database table.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7e932f7231fe6193b9bcda1f0ff787d9" id="tgt2" class="tgtSentence">The following code creates a new <legacyBold>Key</legacyBold>:</caps:sentence>
          </para>
          <code>Dim obj As New Key</code>
          <para>
            <caps:sentence sentenceid="3780fb8cecd19ef19308f543f96b3d21" id="tgt3" class="tgtSentence">With the properties and collections of a <legacyBold>Key</legacyBold> object, you can:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="631265bdbd89dcdc1280967d13bd57b4" id="tgt4" class="tgtSentence">Identify the key with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4561ae6c16a7434bba5a2947e7cb24f7" id="tgt5" class="tgtSentence">Determine whether the key is primary, foreign, or unique with the <legacyLink xlink:href="8ca2f1fd-eb1e-490c-a28b-67eda92e0fc7">Type</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1f34467b7a1f69649484354932e676f" id="tgt6" class="tgtSentence">Access the database columns of the key with the <legacyLink xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b188715e475671f04d777a7e5bb9af66" id="tgt7" class="tgtSentence">Specify the name of the related table with the <legacyLink xlink:href="cb54c6bc-2be2-40b1-bc11-90c10651b878">RelatedTable</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e0c4a8bf2dee55c4ed64e64e8e61f210" id="tgt8" class="tgtSentence">Determine the action performed on deletion or update of a primary key with the <legacyLink xlink:href="87bd4c0a-cae3-4007-a939-4193acaa00ac">DeleteRule</legacyLink> and <legacyLink xlink:href="f4e21060-40cb-4790-8611-4086a092dda2">UpdateRule</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt9" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="fba47748-53dd-4a5c-8c00-72e48bbc5bb0">
                  <caps:sentence sentenceid="b9b2e341b2f29c2fe81d93ffe4b63c71" id="tgt10" class="tgtSentence">Key Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
        <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a primary, foreign, or unique key field from a database table.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The following code creates a new <legacyBold>Key</legacyBold>:</caps:sentence>
          </para>
          <code>Dim obj As New Key</code>
          <para>
            <caps:sentence id="src3" class="srcSentence">With the properties and collections of a <legacyBold>Key</legacyBold> object, you can:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Identify the key with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Determine whether the key is primary, foreign, or unique with the <legacyLink xlink:href="8ca2f1fd-eb1e-490c-a28b-67eda92e0fc7">Type</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Access the database columns of the key with the <legacyLink xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Specify the name of the related table with the <legacyLink xlink:href="cb54c6bc-2be2-40b1-bc11-90c10651b878">RelatedTable</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Determine the action performed on deletion or update of a primary key with the <legacyLink xlink:href="87bd4c0a-cae3-4007-a939-4193acaa00ac">DeleteRule</legacyLink> and <legacyLink xlink:href="f4e21060-40cb-4790-8611-4086a092dda2">UpdateRule</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src9" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="fba47748-53dd-4a5c-8c00-72e48bbc5bb0">
                  <caps:sentence id="src10" class="srcSentence">Key Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
        <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Columns Collection (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 23b9fea8-4f76-4a51-95ce-1a6ce4560b34
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
# Columns Collection (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d4d6506b3395806bb4fe055a9082c16f" id="tgt1" class="tgtSentence">Contains all <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects of a table, index, or key.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="867e39f589c6b327b423e1e25eb0868a" id="tgt2" class="tgtSentence">The <legacyLink xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append</legacyLink> method for a <legacyBold>Columns</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt3" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="d379dea278e339160e637dcf0e53c15b" id="tgt4" class="tgtSentence">Add a new column to the collection with the <legacyBold>Append</legacyBold> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ed0be1c652e041a462a56d678a7a9845" id="tgt5" class="tgtSentence">The remaining properties and methods are standard to ADO collections.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt6" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="aba7968a6be09e889e275c68d4af3940" id="tgt7" class="tgtSentence">Access a column in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="41105438a729c8b5bc9758a830f2cf41" id="tgt8" class="tgtSentence">Return the number of columns contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="39ac4306a1e8ce060f2635311f3bd1bf" id="tgt9" class="tgtSentence">Remove a column from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2cece3526fcf35dcf7ce17482562dd9f" id="tgt10" class="tgtSentence">Update the objects in the collection to reflect the current database's schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="3a0f0607ecd99ed2c777f5b69dfaeecf" id="tgt11" class="tgtSentence">An error will occur when appending a <legacyBold>Column</legacyBold> to the <legacyBold>Columns</legacyBold> collection of an <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink> if the <legacyBold>Column</legacyBold> does not exist in a <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink> that is already appended to the <legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables</legacyLink> collection.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt12" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="3d9ec89a-cc85-4091-b6f0-2bb6a6826d5e">
                  <caps:sentence sentenceid="8119e550d6779e1e19a50ced87ec1c91" id="tgt13" class="tgtSentence">Columns Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="d9502254-d89b-4bcb-94f1-6418f89e7f30">SortOrder Property Example (VB)</link>
        <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink> objects of a table, index, or key.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <legacyLink xlink:href="7a46d23c-efef-4ec7-815d-cd3ac86787dd">Append</legacyLink> method for a <legacyBold>Columns</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Add a new column to the collection with the <legacyBold>Append</legacyBold> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src5" class="srcSentence">The remaining properties and methods are standard to ADO collections.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Access a column in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Return the number of columns contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Remove a column from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Update the objects in the collection to reflect the current database's schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src11" class="srcSentence">An error will occur when appending a <legacyBold>Column</legacyBold> to the <legacyBold>Columns</legacyBold> collection of an <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink> if the <legacyBold>Column</legacyBold> does not exist in a <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink> that is already appended to the <legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables</legacyLink> collection.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src12" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="3d9ec89a-cc85-4091-b6f0-2bb6a6826d5e">
                  <caps:sentence id="src13" class="srcSentence">Columns Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="d9502254-d89b-4bcb-94f1-6418f89e7f30">SortOrder Property Example (VB)</link>
        <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
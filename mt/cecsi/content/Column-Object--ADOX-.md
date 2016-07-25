---
title: "Column Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6e772783-1bc8-4ea7-94b2-7d7a52ea5c47
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
# Column Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="70bc7f5d5ce77a98beea8615647134f8" id="tgt1" class="tgtSentence">Represents a column from a table, index, or key.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="08bd34e2214e2ef9807466fa492856fc" id="tgt2" class="tgtSentence">The following code creates a new <legacyBold>Column</legacyBold>:</caps:sentence>
          </para>
          <para>
            <codeInline>Dim obj As New Column</codeInline>
          </para>
          <para>
            <caps:sentence sentenceid="6b5cb21fd71e594985bff3fb8bf10d03" id="tgt3" class="tgtSentence">With the properties and collections of a <legacyBold>Column</legacyBold> object, you can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="e0339f58736606bbc86efbd9b00b5bf2" id="tgt4" class="tgtSentence">Identify the column with the <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="831a743f377a02b3f64c2ff09825a0bf" id="tgt5" class="tgtSentence">Specify the data type of the column with the <link xlink:href="8ca2f1fd-eb1e-490c-a28b-67eda92e0fc7">Type Property (Key) (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4f40a2c6f9492f63a3ef16934c86b7b7" id="tgt6" class="tgtSentence">Determine if the column is fixed-length, or if it can contain null values with the <link xlink:href="e3abb359-79a3-4c22-b3a8-2900817e0d23">Attributes Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3a30bd5d7a7081b03b1286f15a18f096" id="tgt7" class="tgtSentence">Specify the maximum size of the column with the <link xlink:href="762b8937-c31c-4e90-bb85-506d991e8280">DefinedSize Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f0d020aa379b895986783658cfffa449" id="tgt8" class="tgtSentence">For numeric data values, specify the scale with the <link xlink:href="573ee5d1-57c7-4a27-be79-a0e12944ad9b">NumericScale Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2ae8547ad2f8a2a25b563b06fa185459" id="tgt9" class="tgtSentence">For numeric data value, specify the maximum precision with the <link xlink:href="0e0ecbbf-d7de-49d4-a128-5a519ecd54ba">Precision Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fdade29147894bfe28b3842b5ec8dbe9" id="tgt10" class="tgtSentence">Specify the <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link> that owns the column with the <link xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">ParentCatalog Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c03f2648f6f56118e9c5cfc9c82b1782" id="tgt11" class="tgtSentence">For key columns, specify the name of the related column in the related table with the <link xlink:href="2f2ca019-c785-4c08-beb1-3a2d3b47823e">RelatedColumn Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0e8b444f2e6a63123fd5b042b286dc9a" id="tgt12" class="tgtSentence">For index columns, specify whether the sort order is ascending or descending with the <link xlink:href="04510b19-9cb2-4895-b23b-f7790123eb04">SortOrder Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dc48a91d44a1086df1c3e8bcd3c89074" id="tgt13" class="tgtSentence">Access provider-specific properties with the <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection (ADO)</link> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="c80581c4a92a3cd6fea577b7eebf3e3c" id="tgt14" class="tgtSentence">Not all properties of <legacyBold>Column</legacyBold> objects may be supported by your data provider.</caps:sentence>
              <caps:sentence sentenceid="fcea6f04f236e00fe8bc1d98b27e8435" id="tgt15" class="tgtSentence"> An error will occur if you have set a value for a property that the provider does not support.</caps:sentence>
              <caps:sentence sentenceid="f35dec2a0785e9f538b612ec0c989321" id="tgt16" class="tgtSentence"> For new <legacyBold>Column</legacyBold> objects, the error will occur when the object is appended to the collection.</caps:sentence>
              <caps:sentence sentenceid="75f584dc269e8644adb6e3125f193185" id="tgt17" class="tgtSentence"> For existing objects, the error will occur when setting the property.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="a955e5c0b9f2464f14b6bc2b7c24cb73" id="tgt18" class="tgtSentence">When creating <legacyBold>Column</legacyBold> objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</caps:sentence>
              <caps:sentence sentenceid="2ad1596882d2bb3dea74288c43cc341a" id="tgt19" class="tgtSentence"> For more information about which properties your provider supports, see your provider documentation.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt20" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="f87d46fb-4b33-42b5-8a54-6d2c4577c69a">Column Object Properties, Methods, and Events</link>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="ea2ec614-34c8-41b7-8ebd-063798bd56b4">ADOX Code Example: NumericScale and Precision Properties Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="d9502254-d89b-4bcb-94f1-6418f89e7f30">SortOrder Property Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection (ADOX)</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a column from a table, index, or key.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The following code creates a new <legacyBold>Column</legacyBold>:</caps:sentence>
          </para>
          <para>
            <codeInline>Dim obj As New Column</codeInline>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">With the properties and collections of a <legacyBold>Column</legacyBold> object, you can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Identify the column with the <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Specify the data type of the column with the <link xlink:href="8ca2f1fd-eb1e-490c-a28b-67eda92e0fc7">Type Property (Key) (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Determine if the column is fixed-length, or if it can contain null values with the <link xlink:href="e3abb359-79a3-4c22-b3a8-2900817e0d23">Attributes Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Specify the maximum size of the column with the <link xlink:href="762b8937-c31c-4e90-bb85-506d991e8280">DefinedSize Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">For numeric data values, specify the scale with the <link xlink:href="573ee5d1-57c7-4a27-be79-a0e12944ad9b">NumericScale Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">For numeric data value, specify the maximum precision with the <link xlink:href="0e0ecbbf-d7de-49d4-a128-5a519ecd54ba">Precision Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Specify the <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link> that owns the column with the <link xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">ParentCatalog Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">For key columns, specify the name of the related column in the related table with the <link xlink:href="2f2ca019-c785-4c08-beb1-3a2d3b47823e">RelatedColumn Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">For index columns, specify whether the sort order is ascending or descending with the <link xlink:href="04510b19-9cb2-4895-b23b-f7790123eb04">SortOrder Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Access provider-specific properties with the <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection (ADO)</link> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src14" class="srcSentence">Not all properties of <legacyBold>Column</legacyBold> objects may be supported by your data provider.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> An error will occur if you have set a value for a property that the provider does not support.</caps:sentence>
              <caps:sentence id="src16" class="srcSentence"> For new <legacyBold>Column</legacyBold> objects, the error will occur when the object is appended to the collection.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> For existing objects, the error will occur when setting the property.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src18" class="srcSentence">When creating <legacyBold>Column</legacyBold> objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</caps:sentence>
              <caps:sentence id="src19" class="srcSentence"> For more information about which properties your provider supports, see your provider documentation.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src20" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="f87d46fb-4b33-42b5-8a54-6d2c4577c69a">Column Object Properties, Methods, and Events</link>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="ea2ec614-34c8-41b7-8ebd-063798bd56b4">ADOX Code Example: NumericScale and Precision Properties Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="d9502254-d89b-4bcb-94f1-6418f89e7f30">SortOrder Property Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection (ADOX)</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Table Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a6d74000-0828-49ba-850a-63da865f8802
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
# Table Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a3a580873f938490c386ca6e5062c8a2" id="tgt1" class="tgtSentence">Represents a database table including columns, indexes, and keys.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="43af2c9ea2adf10c318a9191d1192a48" id="tgt2" class="tgtSentence">The following code creates a new <legacyBold>Table</legacyBold>:</caps:sentence>
          </para>
          <code>Dim obj As New Table</code>
          <para>
            <caps:sentence sentenceid="ba292ef762a11fd00b9011be21eb478e" id="tgt3" class="tgtSentence">With the properties and collections of a <legacyBold>Table</legacyBold> object, you can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="146daee31d7fe396ad33b8532677cdf1" id="tgt4" class="tgtSentence">Identify the table with the <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1eadbea2aa10ba8d9f6390c6e444d1fb" id="tgt5" class="tgtSentence">Determine the type of table with the <link xlink:href="7b6e14bb-fb69-4d74-aaca-f5d380f4d887">Type Property (Table) (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="55657326f7184ee77db1e37af0f1b89e" id="tgt6" class="tgtSentence">Access the database columns of the table with the <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection (ADOX)</link> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="bc030cb6277c8092a08a81c85795d215" id="tgt7" class="tgtSentence">Access the indexes of the table with the <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection (ADOX)</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a6fe9cf3498148aa1bcc57c48cf9fec1" id="tgt8" class="tgtSentence">Access the keys of the table with the <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection (ADOX)</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d850f9298d6f769b4cd8bdd9753fe92e" id="tgt9" class="tgtSentence">Specify the Catalog that owns the table with the <link xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">ParentCatalog Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2b525648f99a649960e4841f6ce3c187" id="tgt10" class="tgtSentence">Return date information with the <link xlink:href="2bf4b00d-045c-444e-8af7-8af6297ed418">DateCreated Property (ADOX)</link> and <link xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified Property (ADOX)</link> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4ff3176e0e6458aa3306769128898426" id="tgt11" class="tgtSentence">Access provider-specific table properties with the <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection (ADO)</link> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="ce973ba4d09a500128df1d644a94f042" id="tgt12" class="tgtSentence">Your data provider may not support all properties of <legacyBold>Table</legacyBold> objects.</caps:sentence>
              <caps:sentence sentenceid="fcea6f04f236e00fe8bc1d98b27e8435" id="tgt13" class="tgtSentence"> An error will occur if you have set a value for a property that the provider does not support.</caps:sentence>
              <caps:sentence sentenceid="a278bb9a721ee64bf391bec07da1a442" id="tgt14" class="tgtSentence"> For new <legacyBold>Table</legacyBold> objects, the error will occur when the object is appended to the collection.</caps:sentence>
              <caps:sentence sentenceid="75f584dc269e8644adb6e3125f193185" id="tgt15" class="tgtSentence"> For existing objects, the error will occur when setting the property.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="fdc821f51f975ac1e36c6a4a2e6a1d22" id="tgt16" class="tgtSentence">When creating <legacyBold>Table</legacyBold> objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</caps:sentence>
              <caps:sentence sentenceid="2ad1596882d2bb3dea74288c43cc341a" id="tgt17" class="tgtSentence"> For more information about which properties your provider supports, see your provider documentation.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt18" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="140d1517-6f0c-4fc9-9deb-9658982d88ed">Table Object Properties, Methods, and Events</link>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection (ADOX)</link>
        <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection (ADOX)</link>
        <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection (ADOX)</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection (ADO)</link>
        <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection (ADOX)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a database table including columns, indexes, and keys.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The following code creates a new <legacyBold>Table</legacyBold>:</caps:sentence>
          </para>
          <code>Dim obj As New Table</code>
          <para>
            <caps:sentence id="src3" class="srcSentence">With the properties and collections of a <legacyBold>Table</legacyBold> object, you can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Identify the table with the <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Determine the type of table with the <link xlink:href="7b6e14bb-fb69-4d74-aaca-f5d380f4d887">Type Property (Table) (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Access the database columns of the table with the <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection (ADOX)</link> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Access the indexes of the table with the <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection (ADOX)</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Access the keys of the table with the <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection (ADOX)</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Specify the Catalog that owns the table with the <link xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">ParentCatalog Property (ADOX)</link> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Return date information with the <link xlink:href="2bf4b00d-045c-444e-8af7-8af6297ed418">DateCreated Property (ADOX)</link> and <link xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified Property (ADOX)</link> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Access provider-specific table properties with the <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection (ADO)</link> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src12" class="srcSentence">Your data provider may not support all properties of <legacyBold>Table</legacyBold> objects.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> An error will occur if you have set a value for a property that the provider does not support.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> For new <legacyBold>Table</legacyBold> objects, the error will occur when the object is appended to the collection.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> For existing objects, the error will occur when setting the property.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src16" class="srcSentence">When creating <legacyBold>Table</legacyBold> objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> For more information about which properties your provider supports, see your provider documentation.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src18" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="140d1517-6f0c-4fc9-9deb-9658982d88ed">Table Object Properties, Methods, and Events</link>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection (ADOX)</link>
        <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection (ADOX)</link>
        <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection (ADOX)</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection (ADO)</link>
        <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection (ADOX)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
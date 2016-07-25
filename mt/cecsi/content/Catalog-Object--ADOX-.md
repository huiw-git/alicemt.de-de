---
title: "Catalog Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: bb651639-a488-4e38-b6de-0ed99fa4dd92
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
# Catalog Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9292ff6a3321bf01810a5150d87f2588" id="tgt1" class="tgtSentence">Contains collections (<legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables</legacyLink>, <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink>, <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink>, <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups</legacyLink>, and <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink>) that describe the schema catalog of a data source.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="595c7cde239d6f643600430ef9b19e2e" id="tgt2" class="tgtSentence">You can modify the <legacyBold>Catalog</legacyBold> object by adding or removing objects or by modifying existing objects.</caps:sentence>
            <caps:sentence sentenceid="41b9981eab32971ee65bbf88e08f5bde" id="tgt3" class="tgtSentence"> Some providers may not support all of the <legacyBold>Catalog</legacyBold> objects or may support only viewing schema information.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8c549f81aaea07d93dbe5f1a90a736af" id="tgt4" class="tgtSentence">With the properties and methods of a <legacyBold>Catalog</legacyBold> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="676296a4f1cb93032570b934db232174" id="tgt5" class="tgtSentence">Open the catalog by setting the <legacyLink xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection</legacyLink> property to an ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object or a valid connection string.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="80b72440a4f06358bcad64dead01a323" id="tgt6" class="tgtSentence">Create a new catalog with the <legacyLink xlink:href="64f5c21c-b581-42d8-bdc7-c4f1bebaf105">Create</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ca78713f53cd56bf4634931ac81cd9be" id="tgt7" class="tgtSentence">Determine the owners of the objects in a <legacyBold>Catalog</legacyBold> with the <legacyLink xlink:href="8965adf0-9075-4125-8142-73eb700029c3">GetObjectOwner</legacyLink> and <legacyLink xlink:href="e5170a37-9d6e-43db-bfb6-9b6631fa3048">SetObjectOwner</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt8" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="90a05168-87d0-45e8-8b32-0b64fec74ad2">
                  <caps:sentence sentenceid="8ae391ec0addc901005dee752e38ac67" id="tgt9" class="tgtSentence">Catalog Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="413263a8-05c0-4404-929d-69f82b987ba3">Command and CommandText Properties Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="d7ea0244-596a-404e-8f30-71cadab8d8fc">Create Method Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="7df1089e-69b7-476e-9244-19947c087351">Parameters Collection, Command Property Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="499679bd-287b-487d-bdfb-3803abffec1c">Procedures Refresh Method Example (VB)</link>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
        <link xlink:href="cdad2d66-6ade-40dc-9e74-e40cfa9bc127">Views Refresh Method Example (VB)</link>
        <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
        <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
        <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection</link>
        <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
        <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains collections (<legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables</legacyLink>, <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink>, <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink>, <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups</legacyLink>, and <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink>) that describe the schema catalog of a data source.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">You can modify the <legacyBold>Catalog</legacyBold> object by adding or removing objects or by modifying existing objects.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Some providers may not support all of the <legacyBold>Catalog</legacyBold> objects or may support only viewing schema information.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">With the properties and methods of a <legacyBold>Catalog</legacyBold> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Open the catalog by setting the <legacyLink xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection</legacyLink> property to an ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object or a valid connection string.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Create a new catalog with the <legacyLink xlink:href="64f5c21c-b581-42d8-bdc7-c4f1bebaf105">Create</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Determine the owners of the objects in a <legacyBold>Catalog</legacyBold> with the <legacyLink xlink:href="8965adf0-9075-4125-8142-73eb700029c3">GetObjectOwner</legacyLink> and <legacyLink xlink:href="e5170a37-9d6e-43db-bfb6-9b6631fa3048">SetObjectOwner</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src8" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="90a05168-87d0-45e8-8b32-0b64fec74ad2">
                  <caps:sentence id="src9" class="srcSentence">Catalog Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="413263a8-05c0-4404-929d-69f82b987ba3">Command and CommandText Properties Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="d7ea0244-596a-404e-8f30-71cadab8d8fc">Create Method Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="7df1089e-69b7-476e-9244-19947c087351">Parameters Collection, Command Property Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="499679bd-287b-487d-bdfb-3803abffec1c">Procedures Refresh Method Example (VB)</link>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
        <link xlink:href="cdad2d66-6ade-40dc-9e74-e40cfa9bc127">Views Refresh Method Example (VB)</link>
        <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
        <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
        <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection</link>
        <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
        <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
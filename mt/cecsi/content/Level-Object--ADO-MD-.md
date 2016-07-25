---
title: "Level Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 37815869-ed30-45fd-9aea-0a986c1b305c
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
# Level Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="01d2108552f17d407f82d820f351d7bc" id="tgt1" class="tgtSentence">Contains a set of members, each of which has the same rank within a hierarchy.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d1cd0749b43c6295d8f001677f4f9ec1" id="tgt2" class="tgtSentence">With the collections and properties of a <legacyBold>Level</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="ff0b1a2f56fbf072a1b9cd18da279c4b" id="tgt3" class="tgtSentence">Identify the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> and <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7ea61814935f1dac2844849a7c968a4c" id="tgt4" class="tgtSentence">Return a string to use when displaying the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="d90763b8-ba3f-48f8-95b2-e6a0e52296e1">Caption</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="12e6e1ade37c1a637783df2ddc12c767" id="tgt5" class="tgtSentence">Return a meaningful string that describes the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d1cd9eb5d2a8ed8c4132bfe20d309286" id="tgt6" class="tgtSentence">Return the <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects that make up the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="00957a03c356b9cd18d68015a6e2869a" id="tgt7" class="tgtSentence">Return the number of levels from the root of the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="e41f2644-617d-4c09-80a4-feb5cf736186">Depth</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="22a436cf730f5dbd662c8a2a55477d40" id="tgt8" class="tgtSentence">Use the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection to obtain additional information about the <legacyBold>Level</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="39452e7aa7674a533008488280c4b581" id="tgt9" class="tgtSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence sentenceid="4be124b7b0fe47f8aff65d60ff33d8e3" id="tgt10" class="tgtSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence sentenceid="8cf7e6aaac62008f842531d45619b20d" id="tgt11" class="tgtSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence sentenceid="d4f2c74aa9a9fd8ed47f1fcb6abfc159" id="tgt12" class="tgtSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt13" class="tgtSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt14" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5d7e0fc6b79887409423ef63225b9d7d" id="tgt15" class="tgtSentence">CatalogName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04cb6c195b8d635e037ff86d9a364798" id="tgt16" class="tgtSentence">The name of the catalog to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4cb11b458b08fa21cd892d581872ba9" id="tgt17" class="tgtSentence">CubeName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="797d1434a96d32d967df4c7c554bc573" id="tgt18" class="tgtSentence">The name of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt19" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e50f3d9f2c3fa44acf5b6440a9515dbb" id="tgt20" class="tgtSentence">A meaningful description of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4d26f95a5429ce235ad24dc5f7b6047" id="tgt21" class="tgtSentence">DimensionUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b85311c03ed6fa7068686491ffd1d72a" id="tgt22" class="tgtSentence">The unambiguous name of the <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">dimension</legacyLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f7c7bbf6d0de799a2e1a5a2a9199ed6" id="tgt23" class="tgtSentence">HierarchyUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="daf6316a662faea79fefb2d39fc0beda" id="tgt24" class="tgtSentence">The unambiguous name of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f9dfec033e0c41d87b9c189d7491eb9f" id="tgt25" class="tgtSentence">LevelCaption</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d2c38815af6d8f5f6a31edd538f7075c" id="tgt26" class="tgtSentence">A label or caption associated with the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="69fc7ccc944e3ddebbc85f06985c5ec8" id="tgt27" class="tgtSentence">LevelCardinality</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="767a30b3302bcba41330a5b1cbb7bec9" id="tgt28" class="tgtSentence">The number of members in the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1778010027285131935a7e16ede61ece" id="tgt29" class="tgtSentence">LevelGUID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4dcb557ca4b3e69839789f991a9a4c9b" id="tgt30" class="tgtSentence">The GUID of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="269f51f9b46986e02c6e10755f3e9cbf" id="tgt31" class="tgtSentence">LevelName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5a88a4501b999224bc5e0012b9573d8" id="tgt32" class="tgtSentence">Name of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="964a1593396e6a3149f033f5ebb09dc6" id="tgt33" class="tgtSentence">LevelNumber</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54db6816b516c0adab71fb89fe56b37f" id="tgt34" class="tgtSentence">The distance between the level and the root of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e2593beafb0575123cb7499d5c4ca58c" id="tgt35" class="tgtSentence">LevelType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="728174036160c390ab7f4ce3b6e42080" id="tgt36" class="tgtSentence">The type of level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4420b38cd3c245cffe50f1121cdb9ff5" id="tgt37" class="tgtSentence">LevelUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fd185c066a31949f5ca88cb7822ce80f" id="tgt38" class="tgtSentence">The unambiguous name of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26bec1185fbcce3e5c4e8dde8baee2c9" id="tgt39" class="tgtSentence">SchemaName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="370cece091feab6ef06b845679594dd9" id="tgt40" class="tgtSentence">The name of the schema to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt41" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="855d21c6107c4ef0d60a56096298f805" id="tgt42" class="tgtSentence">
                  <legacyLink xlink:href="fdff70b0-95d0-447f-9359-97b8d159420d">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="4d72a912-ef53-4989-9fca-214937574116">VBScript Example</link>
        <link xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy Object</link>
        <link xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">Levels Collection</link>
        <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains a set of members, each of which has the same rank within a hierarchy.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">With the collections and properties of a <legacyBold>Level</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src3" class="srcSentence">Identify the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> and <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Return a string to use when displaying the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="d90763b8-ba3f-48f8-95b2-e6a0e52296e1">Caption</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Return a meaningful string that describes the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Return the <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects that make up the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Return the number of levels from the root of the <legacyBold>Level</legacyBold> with the <legacyLink xlink:href="e41f2644-617d-4c09-80a4-feb5cf736186">Depth</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Use the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection to obtain additional information about the <legacyBold>Level</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">CatalogName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">The name of the catalog to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">CubeName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">The name of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">A meaningful description of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">DimensionUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">The unambiguous name of the <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">dimension</legacyLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">HierarchyUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">The unambiguous name of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">LevelCaption</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">A label or caption associated with the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">LevelCardinality</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">The number of members in the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">LevelGUID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">The GUID of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">LevelName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Name of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">LevelNumber</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">The distance between the level and the root of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">LevelType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">The type of level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">LevelUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">The unambiguous name of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">SchemaName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">The name of the schema to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src41" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src42" class="srcSentence">
                  <legacyLink xlink:href="fdff70b0-95d0-447f-9359-97b8d159420d">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="4d72a912-ef53-4989-9fca-214937574116">VBScript Example</link>
        <link xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy Object</link>
        <link xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">Levels Collection</link>
        <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
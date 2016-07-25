---
title: "Hierarchy Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 034af340-ac79-494e-ba5e-2b57da1cb9de
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
# Hierarchy Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d8d3a435f76e1e326848db5d186290df" id="tgt1" class="tgtSentence">Represents one way in which the members of a <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">dimension</legacyLink> can be aggregated or "rolled up."</caps:sentence>
          <caps:sentence sentenceid="5b5dfb281f9c05be727911add517b3c3" id="tgt2" class="tgtSentence"> A dimension can be aggregated along one or more hierarchies.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="76acaf9d6f6bf0d6519aae6a23fe98e1" id="tgt3" class="tgtSentence">With the collections and properties of a <legacyBold>Hierarchy</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="d82ee3de0a46faaac46d3663e5793b2c" id="tgt4" class="tgtSentence">Identify the <legacyBold>Hierarchy</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> and <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fcdc058c0e476e67b79b68959893ba80" id="tgt5" class="tgtSentence">Return a meaningful string that describes the <legacyBold>Hierarchy</legacyBold> with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fecd0168a267e09e02275b7a47dad96a" id="tgt6" class="tgtSentence">Return the <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> objects that make up the <legacyBold>Hierarchy</legacyBold> with the <legacyLink xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">Levels</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ce5a7afa3cdf59dce5212b8741ea125a" id="tgt7" class="tgtSentence">Use the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection to obtain additional information about the <legacyBold>Hierarchy</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="39452e7aa7674a533008488280c4b581" id="tgt8" class="tgtSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence sentenceid="4be124b7b0fe47f8aff65d60ff33d8e3" id="tgt9" class="tgtSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence sentenceid="8cf7e6aaac62008f842531d45619b20d" id="tgt10" class="tgtSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence sentenceid="d4f2c74aa9a9fd8ed47f1fcb6abfc159" id="tgt11" class="tgtSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt12" class="tgtSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt13" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1e4e4f11306ac85467c92f793c570dbe" id="tgt14" class="tgtSentence">AllMember</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bdb542ce6a85b7e0a215f38cbb61998b" id="tgt15" class="tgtSentence">The member at the highest level of rollup in the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5d7e0fc6b79887409423ef63225b9d7d" id="tgt16" class="tgtSentence">CatalogName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04cb6c195b8d635e037ff86d9a364798" id="tgt17" class="tgtSentence">The name of the catalog to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4cb11b458b08fa21cd892d581872ba9" id="tgt18" class="tgtSentence">CubeName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="797d1434a96d32d967df4c7c554bc573" id="tgt19" class="tgtSentence">The name of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="229daf4a54a54b8264c0ff7ea7af350f" id="tgt20" class="tgtSentence">DefaultMember</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="286b9cd2aef787acfcdcbfae18346da7" id="tgt21" class="tgtSentence">The unique name of the default member for this hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt22" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="99b107e124021944b3c322494a8635c0" id="tgt23" class="tgtSentence">A meaningful description of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d63b82b88cfdef93e24794fdb7e8de1" id="tgt24" class="tgtSentence">DimensionType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="263dbed1ac5af18398b7e9fec61248a3" id="tgt25" class="tgtSentence">The type of dimension to which this hierarchy belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4d26f95a5429ce235ad24dc5f7b6047" id="tgt26" class="tgtSentence">DimensionUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="621499158ae222beac0700e0d15b768f" id="tgt27" class="tgtSentence">The unambiguous name of the dimension.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eabc77014a37093f8258b23ac243e540" id="tgt28" class="tgtSentence">HierarchyCaption</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3778543311a6574d4a56ad4d71fcfbac" id="tgt29" class="tgtSentence">A label or caption associated with the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="abf6e7260ff3caed7d1a8712bd36a291" id="tgt30" class="tgtSentence">HierarchyCardinality</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0c9877b84f6a3e6b16074b3d750a1538" id="tgt31" class="tgtSentence">The number of members in the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ee9c8289fe137619f1d0c4e4d1a1c8be" id="tgt32" class="tgtSentence">HierarchyGUID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5db3267bb080efba7fd41977c8b1f9f1" id="tgt33" class="tgtSentence">The GUID of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a2a224aac14dee508562045925417df3" id="tgt34" class="tgtSentence">HierarchyName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="999459017103b74913b45403695cfa53" id="tgt35" class="tgtSentence">The name of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f7c7bbf6d0de799a2e1a5a2a9199ed6" id="tgt36" class="tgtSentence">HierarchyUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="daf6316a662faea79fefb2d39fc0beda" id="tgt37" class="tgtSentence">The unambiguous name of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26bec1185fbcce3e5c4e8dde8baee2c9" id="tgt38" class="tgtSentence">SchemaName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="370cece091feab6ef06b845679594dd9" id="tgt39" class="tgtSentence">The name of the schema to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt40" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="d9209cd243e84d35927dbe15d24714e4" id="tgt41" class="tgtSentence">
                  <legacyLink xlink:href="8ec0b00e-0e18-4f1b-9bbf-42168670bf5f">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="4d72a912-ef53-4989-9fca-214937574116">VBScript Example</link>
        <link xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension Object</link>
        <link xlink:href="bef0fcb1-8060-4faa-84f0-3d52e9c4526f">Hierarchies Collection</link>
        <link xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">Levels Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents one way in which the members of a <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">dimension</legacyLink> can be aggregated or "rolled up."</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A dimension can be aggregated along one or more hierarchies.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">With the collections and properties of a <legacyBold>Hierarchy</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Identify the <legacyBold>Hierarchy</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> and <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Return a meaningful string that describes the <legacyBold>Hierarchy</legacyBold> with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Return the <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> objects that make up the <legacyBold>Hierarchy</legacyBold> with the <legacyLink xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">Levels</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Use the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection to obtain additional information about the <legacyBold>Hierarchy</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">AllMember</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">The member at the highest level of rollup in the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">CatalogName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">The name of the catalog to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">CubeName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">The name of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">DefaultMember</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">The unique name of the default member for this hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">A meaningful description of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">DimensionType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">The type of dimension to which this hierarchy belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">DimensionUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">The unambiguous name of the dimension.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">HierarchyCaption</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">A label or caption associated with the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">HierarchyCardinality</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">The number of members in the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">HierarchyGUID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">The GUID of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">HierarchyName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">The name of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">HierarchyUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">The unambiguous name of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">SchemaName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">The name of the schema to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src40" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src41" class="srcSentence">
                  <legacyLink xlink:href="8ec0b00e-0e18-4f1b-9bbf-42168670bf5f">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="4d72a912-ef53-4989-9fca-214937574116">VBScript Example</link>
        <link xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension Object</link>
        <link xlink:href="bef0fcb1-8060-4faa-84f0-3d52e9c4526f">Hierarchies Collection</link>
        <link xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">Levels Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
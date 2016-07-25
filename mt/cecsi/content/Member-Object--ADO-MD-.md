---
title: "Member Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3dedf755-0741-4c3f-8b4e-bff8ff8809c8
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
# Member Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="fa45d4dbeb51f6322de0904a5757f1bc" id="tgt1" class="tgtSentence">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4673ff1b16685d0825a9a0f0c1a857a0" id="tgt2" class="tgtSentence">The properties of a <legacyBold>Member</legacyBold> differ depending on the context in which it is used.</caps:sentence>
            <caps:sentence sentenceid="bd75664e74379b15f1982ec28245a9f0" id="tgt3" class="tgtSentence"> A <legacyBold>Member</legacyBold> of a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> in a <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> has a <legacyLink xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children</legacyLink> property that returns the <legacyBold>Members</legacyBold> on the next lower level in the hierarchy from the current <legacyBold>Member</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="b800cb9a44a3c45dcee33e42552de2af" id="tgt4" class="tgtSentence"> For a <legacyBold>Member</legacyBold> of a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink>, the <legacyBold>Children</legacyBold> collection is always empty.</caps:sentence>
            <caps:sentence sentenceid="8e4afd8df8f839066d57126cee715f6e" id="tgt5" class="tgtSentence"> Also, the <legacyLink xlink:href="34698910-64b9-41d8-8531-9de12f2b1e32">Type</legacyLink> property applies only to <legacyBold>Members</legacyBold> of a <legacyBold>Level</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a0663a128d11ca1d89f506c82636d785" id="tgt6" class="tgtSentence">A <legacyBold>Member</legacyBold> of <legacyBold>Position</legacyBold> has two properties that are useful when displaying the <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink>: <legacyLink xlink:href="bf39dd36-fc7a-4f6e-86c0-fa71430c0d86">DrilledDown</legacyLink> and <legacyLink xlink:href="510842e0-e8dc-4b33-9517-bd1c6df0cf3c">ParentSameAsPrev</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="5e4e2e3f02c9b560dd2346eb5dff2d7a" id="tgt7" class="tgtSentence"> An error will occur if these properties are accessed on a <legacyBold>Member</legacyBold> of a <legacyBold>Level</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="95cafb5064d2bc04d329fda43695f7e9" id="tgt8" class="tgtSentence">With the collections and properties of a <legacyBold>Member</legacyBold> object of a <legacyBold>Level</legacyBold>, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="a75cca717683111cbc5f49d898e6682d" id="tgt9" class="tgtSentence">Identify the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> and <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2aa86693fc149322f387137524abc6bc" id="tgt10" class="tgtSentence">Return a string to use when displaying the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="d90763b8-ba3f-48f8-95b2-e6a0e52296e1">Caption</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed60ee724db9bda6453482a25aed202b" id="tgt11" class="tgtSentence">Return a meaningful string that describes a measure or formula <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6216c8e1886f0b30e606b37fd3c1a394" id="tgt12" class="tgtSentence">Determine the nature of the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="34698910-64b9-41d8-8531-9de12f2b1e32">Type</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f75c4252c56f32529f0bcf9558e16a95" id="tgt13" class="tgtSentence">Obtain information about the <legacyBold>Level</legacyBold> of the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="8a1cfe2c-f207-4445-b152-ade090f64608">LevelDepth</legacyLink> and <legacyLink xlink:href="bf3b4466-9a0b-446e-9e04-fed944e3a493">LevelName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5cefa10c36ad8d28982e04ceaa290021" id="tgt14" class="tgtSentence">Obtain related <legacyBold>Members</legacyBold> in a <legacyLink xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy</legacyLink> with the <legacyLink xlink:href="32c278c1-d8e1-4bb7-9ecd-2fbfdffee34b">Parent</legacyLink> and <legacyLink xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6af9f7fa23c4d3dee6ae3a7f09ff5b77" id="tgt15" class="tgtSentence">Count the children of a <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="5463be22-ca50-43ea-9c92-468fc8eda280">ChildCount</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="22a436cf730f5dbd662c8a2a55477d40" id="tgt16" class="tgtSentence">Use the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection to obtain additional information about the <legacyBold>Level</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="52ff292c86e2289054ae55ec1b47f02f" id="tgt17" class="tgtSentence">With the collections and properties of a <legacyBold>Member</legacyBold> of a <legacyBold>Position</legacyBold> along an <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink>, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="a75cca717683111cbc5f49d898e6682d" id="tgt18" class="tgtSentence">Identify the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> and <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2aa86693fc149322f387137524abc6bc" id="tgt19" class="tgtSentence">Return a string to use when displaying the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="d90763b8-ba3f-48f8-95b2-e6a0e52296e1">Caption</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed60ee724db9bda6453482a25aed202b" id="tgt20" class="tgtSentence">Return a meaningful string that describes a measure or formula <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f75c4252c56f32529f0bcf9558e16a95" id="tgt21" class="tgtSentence">Obtain information about the <legacyBold>Level</legacyBold> of the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="8a1cfe2c-f207-4445-b152-ade090f64608">LevelDepth</legacyLink> and <legacyLink xlink:href="bf3b4466-9a0b-446e-9e04-fed944e3a493">LevelName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6af9f7fa23c4d3dee6ae3a7f09ff5b77" id="tgt22" class="tgtSentence">Count the children of a <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="5463be22-ca50-43ea-9c92-468fc8eda280">ChildCount</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed3ccdc81c019284881d2a501932fca7" id="tgt23" class="tgtSentence">Use the <legacyLink xlink:href="bf39dd36-fc7a-4f6e-86c0-fa71430c0d86">DrilledDown</legacyLink> property to determine whether there is at least one child on the <legacyBold>Axis</legacyBold> immediately following this <legacyBold>Member</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a58f776b39a9231706a830c861942e81" id="tgt24" class="tgtSentence">Use the <legacyLink xlink:href="510842e0-e8dc-4b33-9517-bd1c6df0cf3c">ParentSameAsPrev</legacyLink> property to determine whether the parent of this <legacyBold>Member</legacyBold> is the same as the parent of the immediately preceding <legacyBold>Member</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="22a436cf730f5dbd662c8a2a55477d40" id="tgt25" class="tgtSentence">Use the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection to obtain additional information about the <legacyBold>Level</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="39452e7aa7674a533008488280c4b581" id="tgt26" class="tgtSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence sentenceid="4be124b7b0fe47f8aff65d60ff33d8e3" id="tgt27" class="tgtSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence sentenceid="8cf7e6aaac62008f842531d45619b20d" id="tgt28" class="tgtSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence sentenceid="d4f2c74aa9a9fd8ed47f1fcb6abfc159" id="tgt29" class="tgtSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt30" class="tgtSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt31" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5d7e0fc6b79887409423ef63225b9d7d" id="tgt32" class="tgtSentence">CatalogName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04cb6c195b8d635e037ff86d9a364798" id="tgt33" class="tgtSentence">The name of the catalog to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f868a5f80306c9e5ce7184783eda253e" id="tgt34" class="tgtSentence">ChildrenCardinality</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a56abe69f5700ff32895351a16c69795" id="tgt35" class="tgtSentence">The number of children that the member has.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4cb11b458b08fa21cd892d581872ba9" id="tgt36" class="tgtSentence">CubeName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="797d1434a96d32d967df4c7c554bc573" id="tgt37" class="tgtSentence">The name of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt38" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1dd2d47c180d532935cb9514c00e26cf" id="tgt39" class="tgtSentence">A meaningful description of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4d26f95a5429ce235ad24dc5f7b6047" id="tgt40" class="tgtSentence">DimensionUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b85311c03ed6fa7068686491ffd1d72a" id="tgt41" class="tgtSentence">The unambiguous name of the <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">dimension</legacyLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f7c7bbf6d0de799a2e1a5a2a9199ed6" id="tgt42" class="tgtSentence">HierarchyUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="daf6316a662faea79fefb2d39fc0beda" id="tgt43" class="tgtSentence">The unambiguous name of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="964a1593396e6a3149f033f5ebb09dc6" id="tgt44" class="tgtSentence">LevelNumber</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54db6816b516c0adab71fb89fe56b37f" id="tgt45" class="tgtSentence">The distance between the level and the root of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4420b38cd3c245cffe50f1121cdb9ff5" id="tgt46" class="tgtSentence">LevelUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fd185c066a31949f5ca88cb7822ce80f" id="tgt47" class="tgtSentence">The unambiguous name of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1315a33d898cb657cef17e56148a728d" id="tgt48" class="tgtSentence">MemberCaption</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5208385ab5d5c1727c07ac02a8d6ad41" id="tgt49" class="tgtSentence">A label or caption associated with the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1ed06a97259f4d1e867fe56ae9fe5e8" id="tgt50" class="tgtSentence">MemberGUID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="067def9224ea700b74daecd1ae5e586a" id="tgt51" class="tgtSentence">The GUID of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8bff26e311bc44f5d4122e2667d3fbf" id="tgt52" class="tgtSentence">MemberName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9641802ae0da9c03f00566dd44be4208" id="tgt53" class="tgtSentence">The name of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a972b5400590c44badcb743326fbb2a3" id="tgt54" class="tgtSentence">MemberOrdinal</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d89cc299054e06536500696f9f6d88a8" id="tgt55" class="tgtSentence">The ordinal number of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2a1ad192c2dade34abb0462b7fe7af5" id="tgt56" class="tgtSentence">MemberType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="139346e0fbc798df8e2bae054724899a" id="tgt57" class="tgtSentence">The type of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4f5563ee3aa62839bc40c86eb02b4bf2" id="tgt58" class="tgtSentence">MemberUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="38bd6f453f461307b0796f4c2dc6abce" id="tgt59" class="tgtSentence">The unambiguous name of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a43058d92ea9d546ddf0e20f6105f4ea" id="tgt60" class="tgtSentence">ParentCount</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e6325fa37352824d3bf2f019e3adbd85" id="tgt61" class="tgtSentence">The count of the number of parents that this member has.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="edf33e20ce72e8a5ca0cf38ab37891f5" id="tgt62" class="tgtSentence">ParentLevel</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="470d21d414dec26a3f89896434e7e89a" id="tgt63" class="tgtSentence">The level number of the member's parent.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="593e5d7502b40fa742544f08903f8133" id="tgt64" class="tgtSentence">ParentUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="91b0258b9a0546b8f6681620988126f0" id="tgt65" class="tgtSentence">The unambiguous name of the member's parent.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26bec1185fbcce3e5c4e8dde8baee2c9" id="tgt66" class="tgtSentence">SchemaName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="370cece091feab6ef06b845679594dd9" id="tgt67" class="tgtSentence">The name of the schema to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt68" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="c82cf3f224cee9a9324ddbfd78666f99" id="tgt69" class="tgtSentence">
                  <legacyLink xlink:href="dadd6e7e-b5b4-4ede-8747-ae67ec917d90">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="3aae1107-2f81-413c-8eda-ef96c3df1b8a">Visual Basic Example</link>
        <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The properties of a <legacyBold>Member</legacyBold> differ depending on the context in which it is used.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> A <legacyBold>Member</legacyBold> of a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> in a <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> has a <legacyLink xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children</legacyLink> property that returns the <legacyBold>Members</legacyBold> on the next lower level in the hierarchy from the current <legacyBold>Member</legacyBold>.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> For a <legacyBold>Member</legacyBold> of a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink>, the <legacyBold>Children</legacyBold> collection is always empty.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Also, the <legacyLink xlink:href="34698910-64b9-41d8-8531-9de12f2b1e32">Type</legacyLink> property applies only to <legacyBold>Members</legacyBold> of a <legacyBold>Level</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">A <legacyBold>Member</legacyBold> of <legacyBold>Position</legacyBold> has two properties that are useful when displaying the <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink>: <legacyLink xlink:href="bf39dd36-fc7a-4f6e-86c0-fa71430c0d86">DrilledDown</legacyLink> and <legacyLink xlink:href="510842e0-e8dc-4b33-9517-bd1c6df0cf3c">ParentSameAsPrev</legacyLink>.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> An error will occur if these properties are accessed on a <legacyBold>Member</legacyBold> of a <legacyBold>Level</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">With the collections and properties of a <legacyBold>Member</legacyBold> object of a <legacyBold>Level</legacyBold>, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Identify the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> and <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Return a string to use when displaying the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="d90763b8-ba3f-48f8-95b2-e6a0e52296e1">Caption</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Return a meaningful string that describes a measure or formula <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Determine the nature of the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="34698910-64b9-41d8-8531-9de12f2b1e32">Type</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Obtain information about the <legacyBold>Level</legacyBold> of the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="8a1cfe2c-f207-4445-b152-ade090f64608">LevelDepth</legacyLink> and <legacyLink xlink:href="bf3b4466-9a0b-446e-9e04-fed944e3a493">LevelName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">Obtain related <legacyBold>Members</legacyBold> in a <legacyLink xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy</legacyLink> with the <legacyLink xlink:href="32c278c1-d8e1-4bb7-9ecd-2fbfdffee34b">Parent</legacyLink> and <legacyLink xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">Count the children of a <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="5463be22-ca50-43ea-9c92-468fc8eda280">ChildCount</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">Use the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection to obtain additional information about the <legacyBold>Level</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src17" class="srcSentence">With the collections and properties of a <legacyBold>Member</legacyBold> of a <legacyBold>Position</legacyBold> along an <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink>, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">Identify the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> and <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">Return a string to use when displaying the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="d90763b8-ba3f-48f8-95b2-e6a0e52296e1">Caption</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">Return a meaningful string that describes a measure or formula <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src21" class="srcSentence">Obtain information about the <legacyBold>Level</legacyBold> of the <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="8a1cfe2c-f207-4445-b152-ade090f64608">LevelDepth</legacyLink> and <legacyLink xlink:href="bf3b4466-9a0b-446e-9e04-fed944e3a493">LevelName</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">Count the children of a <legacyBold>Member</legacyBold> with the <legacyLink xlink:href="5463be22-ca50-43ea-9c92-468fc8eda280">ChildCount</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">Use the <legacyLink xlink:href="bf39dd36-fc7a-4f6e-86c0-fa71430c0d86">DrilledDown</legacyLink> property to determine whether there is at least one child on the <legacyBold>Axis</legacyBold> immediately following this <legacyBold>Member</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src24" class="srcSentence">Use the <legacyLink xlink:href="510842e0-e8dc-4b33-9517-bd1c6df0cf3c">ParentSameAsPrev</legacyLink> property to determine whether the parent of this <legacyBold>Member</legacyBold> is the same as the parent of the immediately preceding <legacyBold>Member</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src25" class="srcSentence">Use the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection to obtain additional information about the <legacyBold>Level</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src26" class="srcSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">CatalogName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">The name of the catalog to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">ChildrenCardinality</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">The number of children that the member has.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">CubeName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">The name of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">A meaningful description of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">DimensionUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">The unambiguous name of the <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">dimension</legacyLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">HierarchyUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">The unambiguous name of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">LevelNumber</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">The distance between the level and the root of the hierarchy.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">LevelUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">The unambiguous name of the level.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">MemberCaption</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">A label or caption associated with the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">MemberGUID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">The GUID of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">MemberName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">The name of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">MemberOrdinal</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">The ordinal number of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">MemberType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">The type of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">MemberUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">The unambiguous name of the member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">ParentCount</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">The count of the number of parents that this member has.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">ParentLevel</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">The level number of the member's parent.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">ParentUniqueName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">The unambiguous name of the member's parent.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">SchemaName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">The name of the schema to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src68" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src69" class="srcSentence">
                  <legacyLink xlink:href="dadd6e7e-b5b4-4ede-8747-ae67ec917d90">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="3aae1107-2f81-413c-8eda-ef96c3df1b8a">Visual Basic Example</link>
        <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "CubeDef Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: feb2581c-fc41-471c-bb69-29f8a55fda70
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
# CubeDef Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4068788ec46da9ecafa06632f164f750" id="tgt1" class="tgtSentence">Represents a cube from a multidimensional schema, containing a set of related dimensions.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d6522eb612ceb2f0097ccdf7e390e58a" id="tgt2" class="tgtSentence">With the collections and properties of a <legacyBold>CubeDef</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="bd8cd49674fcb08204d6a20acd023f70" id="tgt3" class="tgtSentence">Identify a <legacyBold>CubeDef</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f2ae9c196bdd3159e9d3a6d1348152f5" id="tgt4" class="tgtSentence">Return a string that describes the cube with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="253b89ec8bc28217961cfc86e801ecbf" id="tgt5" class="tgtSentence">Return the dimensions that make up the cube with the <legacyLink xlink:href="eaf6f4e7-2ea0-49a3-89ee-e219e025257c">Dimensions</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="37d0b303fbff58871e37e4dde555b3fa" id="tgt6" class="tgtSentence">Obtain additional information about the <legacyBold>CubeDef </legacyBold>with the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="39452e7aa7674a533008488280c4b581" id="tgt7" class="tgtSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence sentenceid="4be124b7b0fe47f8aff65d60ff33d8e3" id="tgt8" class="tgtSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence sentenceid="8cf7e6aaac62008f842531d45619b20d" id="tgt9" class="tgtSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence sentenceid="d4f2c74aa9a9fd8ed47f1fcb6abfc159" id="tgt10" class="tgtSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt11" class="tgtSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt12" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5d7e0fc6b79887409423ef63225b9d7d" id="tgt13" class="tgtSentence">CatalogName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04cb6c195b8d635e037ff86d9a364798" id="tgt14" class="tgtSentence">The name of the catalog to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c28d91e6a5c3fa5f9e0d25f9b91edf8b" id="tgt15" class="tgtSentence">CreatedOn</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b9fc8f70bef1676ebe618becb994feb0" id="tgt16" class="tgtSentence">Date and time of cube creation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f821cfca72b14a8c7e891772d898ba4" id="tgt17" class="tgtSentence">CubeGUID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16a0d0396a1e9fd43002268a42ecae48" id="tgt18" class="tgtSentence">Cube GUID.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4cb11b458b08fa21cd892d581872ba9" id="tgt19" class="tgtSentence">CubeName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="797d1434a96d32d967df4c7c554bc573" id="tgt20" class="tgtSentence">The name of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfd0f93853035842f2321a11dce27cb6" id="tgt21" class="tgtSentence">CubeType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cca74385a89e48ca06dc9c2c0b40ea57" id="tgt22" class="tgtSentence">The type of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="07c46eb245a12158eb632d4f4b7647ca" id="tgt23" class="tgtSentence">DataUpdatedBy</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae3a049896ca2f27d5165641fdfdee45" id="tgt24" class="tgtSentence">User ID of the person doing the last data update.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt25" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b39d1b1dc5b35f6307e75f420c79b7aa" id="tgt26" class="tgtSentence">A meaningful description of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fbd5f24880520401e2a3a5b42f974bb" id="tgt27" class="tgtSentence">LastSchemaUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cc902e7832d69afb067cf249ef7e4ad4" id="tgt28" class="tgtSentence">Date and time of last schema update.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26bec1185fbcce3e5c4e8dde8baee2c9" id="tgt29" class="tgtSentence">SchemaName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="370cece091feab6ef06b845679594dd9" id="tgt30" class="tgtSentence">The name of the schema to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6a2b22a516a18afc98c100a186acd0ce" id="tgt31" class="tgtSentence">SchemaUpdatedBy</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c5e0ded506034ca2c1292866c15f4608" id="tgt32" class="tgtSentence">User ID of the person doing the last schema update.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt33" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="cca8a1a0974d38119c7d50d9fcb46611" id="tgt34" class="tgtSentence">
                  <legacyLink xlink:href="5dac737a-b77e-47d3-9228-cd52b7a97b0a">Properties, Methods, and Events</legacyLink> </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="4d72a912-ef53-4989-9fca-214937574116">VBScript Example</link>
        <link xlink:href="11f6f896-d69c-44a4-94cd-d54c93140e4a">Catalog Object</link>
        <link xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs Collection</link>
        <link xlink:href="eaf6f4e7-2ea0-49a3-89ee-e219e025257c">Dimensions Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a cube from a multidimensional schema, containing a set of related dimensions.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">With the collections and properties of a <legacyBold>CubeDef</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src3" class="srcSentence">Identify a <legacyBold>CubeDef</legacyBold> with the <legacyLink xlink:href="4a04380b-51dc-4aaf-8d25-123cdd589641">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Return a string that describes the cube with the <legacyLink xlink:href="6d626d35-0bf3-4f24-9934-ad9c9c91273a">Description</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Return the dimensions that make up the cube with the <legacyLink xlink:href="eaf6f4e7-2ea0-49a3-89ee-e219e025257c">Dimensions</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Obtain additional information about the <legacyBold>CubeDef </legacyBold>with the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">CatalogName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">The name of the catalog to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">CreatedOn</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Date and time of cube creation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">CubeGUID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Cube GUID.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">CubeName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">The name of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">CubeType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">The type of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">DataUpdatedBy</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">User ID of the person doing the last data update.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">A meaningful description of the cube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">LastSchemaUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Date and time of last schema update.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">SchemaName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">The name of the schema to which this cube belongs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">SchemaUpdatedBy</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">User ID of the person doing the last schema update.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src33" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">
                  <legacyLink xlink:href="5dac737a-b77e-47d3-9228-cd52b7a97b0a">Properties, Methods, and Events</legacyLink> </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="4d72a912-ef53-4989-9fca-214937574116">VBScript Example</link>
        <link xlink:href="11f6f896-d69c-44a4-94cd-d54c93140e4a">Catalog Object</link>
        <link xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs Collection</link>
        <link xlink:href="eaf6f4e7-2ea0-49a3-89ee-e219e025257c">Dimensions Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
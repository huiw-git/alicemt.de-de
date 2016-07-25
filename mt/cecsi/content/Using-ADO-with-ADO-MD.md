---
title: "Using ADO with ADO MD"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cfae435e-2ac3-4312-8c1e-9ca4a74cd875
caps.latest.revision: 11
caps.handback.revision: 11
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
# Using ADO with ADO MD
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="21e24650f2f83336483131ebc11c22ef" id="tgt1" class="tgtSentence">ADO and ADO MD are related but separate object models.</caps:sentence>
          <caps:sentence sentenceid="21537a7c40058b1aa2210516667a430b" id="tgt2" class="tgtSentence"> ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information.</caps:sentence>
          <caps:sentence sentenceid="08900162398a871c45c1b52e53e907c3" id="tgt3" class="tgtSentence"> ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b58843ae8fac449c2f0b7490fad3ff8c" id="tgt4" class="tgtSentence">When you work with an MDP, you can choose to use ADO, ADO MD, or both with your application.</caps:sentence>
          <caps:sentence sentenceid="bca4f31ad7e0b82a98b635a8169d35e0" id="tgt5" class="tgtSentence"> By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f7fa9a63c38e26a530f9b24dc17c20fb" id="tgt6" class="tgtSentence">It is frequently useful for consumers to get a flattened, tabular view of a multidimensional dataset.</caps:sentence>
          <caps:sentence sentenceid="f78ce86e47d59287a1485552edfb3c5a" id="tgt7" class="tgtSentence"> You can do this by using the ADO <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="affcdeca2ddf3f18ea53c58ac5a4bced" id="tgt8" class="tgtSentence"> Specify the source for your <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> as the <legacyBold><legacyItalic>Source</legacyItalic></legacyBold> parameter for the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method of a <legacyBold>Recordset</legacyBold>, rather than as the source for an ADO MD <legacyBold>Cellset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="6c0f0e93fcfc7a52a8b4f7d1048201e7" id="tgt9" class="tgtSentence">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</caps:sentence>
          <caps:sentence sentenceid="16492b71337af5d4bc0fcc90ee9c949c" id="tgt10" class="tgtSentence"> The ADO <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method on the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object lets the user open a <legacyBold>Recordset</legacyBold> that contains schema information.</caps:sentence>
          <caps:sentence sentenceid="4b7d4d6e82e7270c45918ef4e0371c27" id="tgt11" class="tgtSentence"> The <legacyBold><legacyItalic>QueryType</legacyItalic></legacyBold> parameter of the <legacyBold>OpenSchema</legacyBold> method has several <legacyLink xlink:href="21c97651-297f-469f-b5b5-c48af72b62a8">SchemaEnum</legacyLink> values that relate specifically to MDPs.</caps:sentence>
          <caps:sentence sentenceid="84d0e282d4212ec64fb268fe90abd153" id="tgt12" class="tgtSentence"> These values are as follows:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="dda42265911dd462041e07d279115ef8" id="tgt13" class="tgtSentence">
                <legacyBold>adSchemaCubes</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3f49b82a9cfe55d8a432a44422d2e7e0" id="tgt14" class="tgtSentence">
                <legacyBold>adSchemaDimensions</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6fef8fedae56999156ea430191fc2370" id="tgt15" class="tgtSentence">
                <legacyBold>adSchemaHierarchies</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f650133ec41d9017e472c088754c0b20" id="tgt16" class="tgtSentence">
                <legacyBold>adSchemaLevels</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e1c50ed03c168ca24b68a0cfd44dbb5d" id="tgt17" class="tgtSentence">
                <legacyBold>adSchemaMeasures</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e8353750cd8f7eef7e78aad82c2a8301" id="tgt18" class="tgtSentence">
                <legacyBold>adSchemaMembers</legacyBold>           </caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="da7a4d2b2bf1997c545230a7a7d614e4" id="tgt19" class="tgtSentence">To use ADO enumeration values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries.</caps:sentence>
          <caps:sentence sentenceid="c9b7a130053dc0fffa5c5c01bc7469f8" id="tgt20" class="tgtSentence"> For example, you can use the ADO <legacyBold>adState</legacyBold> enumeration values with the ADO MD <legacyLink xlink:href="06d480ca-9eb6-4570-a45d-a73539bddd32">State</legacyLink> property.</caps:sentence>
          <caps:sentence sentenceid="ea72806088039cbe45e19e4962c768b2" id="tgt21" class="tgtSentence"> For more information about how to establish references to libraries, see the documentation of your development tool.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="42d6b1fc4ee713f8bb6d78979add6f9d" id="tgt22" class="tgtSentence">For more information about the ADO objects and methods, see the <legacyLink xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">Microsoft ADO MD Programmer's Reference</link>
        <link xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</link>
        <link xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</link>
        <link xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO and ADO MD are related but separate object models.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">When you work with an MDP, you can choose to use ADO, ADO MD, or both with your application.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">It is frequently useful for consumers to get a flattened, tabular view of a multidimensional dataset.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> You can do this by using the ADO <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Specify the source for your <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> as the <legacyBold><legacyItalic>Source</legacyItalic></legacyBold> parameter for the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method of a <legacyBold>Recordset</legacyBold>, rather than as the source for an ADO MD <legacyBold>Cellset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> The ADO <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method on the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object lets the user open a <legacyBold>Recordset</legacyBold> that contains schema information.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> The <legacyBold><legacyItalic>QueryType</legacyItalic></legacyBold> parameter of the <legacyBold>OpenSchema</legacyBold> method has several <legacyLink xlink:href="21c97651-297f-469f-b5b5-c48af72b62a8">SchemaEnum</legacyLink> values that relate specifically to MDPs.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> These values are as follows:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">
                <legacyBold>adSchemaCubes</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">
                <legacyBold>adSchemaDimensions</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">
                <legacyBold>adSchemaHierarchies</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">
                <legacyBold>adSchemaLevels</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">
                <legacyBold>adSchemaMeasures</legacyBold>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">
                <legacyBold>adSchemaMembers</legacyBold>           </caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src19" class="srcSentence">To use ADO enumeration values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> For example, you can use the ADO <legacyBold>adState</legacyBold> enumeration values with the ADO MD <legacyLink xlink:href="06d480ca-9eb6-4570-a45d-a73539bddd32">State</legacyLink> property.</caps:sentence>
          <caps:sentence id="src21" class="srcSentence"> For more information about how to establish references to libraries, see the documentation of your development tool.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src22" class="srcSentence">For more information about the ADO objects and methods, see the <legacyLink xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">Microsoft ADO MD Programmer's Reference</link>
        <link xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</link>
        <link xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</link>
        <link xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
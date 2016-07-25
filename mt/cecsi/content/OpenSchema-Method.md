---
title: "OpenSchema Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 850cf3ce-f18f-4e7c-8597-96c1dc504866
caps.latest.revision: 20
caps.handback.revision: 20
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
# OpenSchema Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="04d9fa93dcd673016cb8daafcc94a69d" id="tgt1" class="tgtSentence">Obtains database schema information from the provider.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set </legacyBold>
          <parameterReference>recordset</parameterReference> = <parameterReference>connection</parameterReference><legacyBold>.OpenSchema(</legacyBold><parameterReference>QueryType</parameterReference>, <parameterReference>Criteria</parameterReference>, <parameterReference>SchemaID</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="73e020dd5f67589c498ce0063660e6b6" id="tgt2" class="tgtSentence">Returns a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object that contains schema information.</caps:sentence>
            <caps:sentence sentenceid="1dc0ab54292e0cc69ec97a737ec5541f" id="tgt3" class="tgtSentence"> The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> will be opened as a read-only, static cursor.</caps:sentence>
            <caps:sentence sentenceid="5766f12eec8c05ed50b2bfc81ef7e862" id="tgt4" class="tgtSentence"> The <legacyItalic>QueryType</legacyItalic> determines what columns appear in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="363344a4b8186b0a49d6b9fd254094fb" id="tgt5" class="tgtSentence"> <parameterReference>QueryType </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="112324ee5b507f27070a356e764ad24b" id="tgt6" class="tgtSentence">Any <legacyLink xlink:href="21c97651-297f-469f-b5b5-c48af72b62a8">SchemaEnum</legacyLink> value that represents the type of schema query to run.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8c31844a449a3521dd863259bea609c1" id="tgt7" class="tgtSentence"> <parameterReference>Criteria </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="a4c2d65ce6fb71d5034fc080cacab773" id="tgt9" class="tgtSentence"> An array of query constraints for each <parameterReference>QueryType</parameterReference> option, as listed in <legacyLink xlink:href="21c97651-297f-469f-b5b5-c48af72b62a8">SchemaEnum</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="2d7313e8e06f3384b6aabeed541aedec" id="tgt10" class="tgtSentence"> <parameterReference>SchemaID </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e207a6cb51846f6814e768e7f600e8b3" id="tgt11" class="tgtSentence">The GUID for a provider-schema query not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence sentenceid="d8692170dd69eeb4bf8cc719b38c0696" id="tgt12" class="tgtSentence"> This parameter is required if <parameterReference>QueryType</parameterReference> is set to <legacyBold>adSchemaProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="f921273f925b6c6a09dfad3a7ea57851" id="tgt13" class="tgtSentence">The <unmanagedCodeEntityReference>OpenSchema</unmanagedCodeEntityReference> method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9653244982515c6ac91a9f70df7c1cb9" id="tgt14" class="tgtSentence">The <parameterReference>QueryType</parameterReference> argument is a GUID that indicates the columns (schemas) returned.</caps:sentence>
            <caps:sentence sentenceid="c4883666b703a2b0b263b6b1b91b4441" id="tgt15" class="tgtSentence"> The OLE DB specification has a full list of schemas.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="41728abdcf2c103e67d612e722fda752" id="tgt16" class="tgtSentence">The <parameterReference>Criteria</parameterReference> argument limits the results of a schema query.</caps:sentence>
            <caps:sentence sentenceid="f539357df3ddeb5a1aefc8138796df66" id="tgt17" class="tgtSentence">
              <parameterReference>Criteria</parameterReference> specifies an array of values that must occur in a corresponding subset of columns, called constraint columns, in the resulting <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="84b390a215b40141f1cbcb9a3b80783e" id="tgt18" class="tgtSentence">The constant <legacyBold>adSchemaProviderSpecific</legacyBold> is used for the <parameterReference>QueryType</parameterReference> argument if the provider defines its own nonstandard schema queries outside those listed previously.</caps:sentence>
            <caps:sentence sentenceid="60da55c8d35fcf358feba90d4e80a70f" id="tgt19" class="tgtSentence"> When this constant is used, the <parameterReference>SchemaID</parameterReference> argument is required to pass the GUID of the schema query to execute.</caps:sentence>
            <caps:sentence sentenceid="54e249de2f419c07def5cfcd805bdb01" id="tgt20" class="tgtSentence"> If <parameterReference>QueryType</parameterReference> is set to <legacyBold>adSchemaProviderSpecific</legacyBold> but <parameterReference>SchemaID</parameterReference> is not provided, an error will result.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6a7e155d8268e54185a809af0a74754a" id="tgt21" class="tgtSentence">Providers are not required to support all the OLE DB standard schema queries.</caps:sentence>
            <caps:sentence sentenceid="8e6350e4221e0a78d71c5b5f33006dde" id="tgt22" class="tgtSentence"> Specifically, only <legacyBold>adSchemaTables</legacyBold>, <legacyBold>adSchemaColumns</legacyBold>, and <legacyBold>adSchemaProviderTypes</legacyBold> are required by the OLE DB specification.</caps:sentence>
            <caps:sentence sentenceid="8f71cbf993a85425b9928934cabefda8" id="tgt23" class="tgtSentence"> However, the provider is not required to support the <parameterReference>Criteria</parameterReference> constraints listed earlier for those schema queries.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="076d83923500b99a4a2dd7acf3c6a054" id="tgt24" class="tgtSentence">
                <legacyBold>Remote Data Service Usage</legacyBold>   The <unmanagedCodeEntityReference>OpenSchema</unmanagedCodeEntityReference> method is not available on a client-side <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="417a5090c75a110d0406b86cae656c6b" id="tgt25" class="tgtSentence">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> returned from the <unmanagedCodeEntityReference>OpenSchema</unmanagedCodeEntityReference> method on the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object cannot be compared to other variables.</caps:sentence>
              <caps:sentence sentenceid="c1b56ba848c1eb7f865632acc7b19ec3" id="tgt26" class="tgtSentence"> For more information about OLE DB data types, see <legacyLink xlink:href="6039292f-74e0-49b2-b133-17bc117ebf6a">Data Types in OLE DB (OLE DB)</legacyLink> and <legacyLink xlink:href="e3a0533a-2196-4eb0-a31e-92fe9556ada6">Appendix A: Data Types</legacyLink> in the Microsoft OLE DB Programmer's Reference.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="453b72bd64e04dd0b72e51507a2fee8f" id="tgt27" class="tgtSentence">
                <legacyBold>Visual C/C++ Users</legacyBold>   When not using client-side cursors, retrieving the "ORDINAL_POSITION" of a column schema in ADO returns a variant of type VT_R8 in MDAC 2.7, MDAC 2.8, and Windows Data Access Components (Windows DAC) 6.0, while the type used in MDAC 2.6 was VT_I4.</caps:sentence>
              <caps:sentence sentenceid="c3aaaeaccd27f40ea718c66aa30de68b" id="tgt28" class="tgtSentence"> Programs written for MDAC 2.6 that only look for a variant returned of type VT_I4 would get a zero for every ordinal if run under MDAC 2.7, MDAC 2.8, and Windows DAC 6.0 without modification.</caps:sentence>
              <caps:sentence sentenceid="a2bcf050ef82744fae4c087f11a0db83" id="tgt29" class="tgtSentence"> This change was made because the data type that OLE DB returns is DBTYPE_UI4, and in the signed VT_I4 type there is not enough room to contain all possible values without possibly truncation occurring and thereby causing a loss of data.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt30" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="455a02f0-8143-4562-8648-8fb45ffd334c">Visual Basic Example</link>
        <link xlink:href="6f3da460-0f49-41e0-999d-a754ec1d887e">Visual C++ Example</link>
        <link xlink:href="4c1240f1-7464-47db-9761-2d547419aedd">Visual J++ Example</link>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Obtains database schema information from the provider.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set </legacyBold>
          <parameterReference>recordset</parameterReference> = <parameterReference>connection</parameterReference><legacyBold>.OpenSchema(</legacyBold><parameterReference>QueryType</parameterReference>, <parameterReference>Criteria</parameterReference>, <parameterReference>SchemaID</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object that contains schema information.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> will be opened as a read-only, static cursor.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The <legacyItalic>QueryType</legacyItalic> determines what columns appear in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <parameterReference>QueryType </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Any <legacyLink xlink:href="21c97651-297f-469f-b5b5-c48af72b62a8">SchemaEnum</legacyLink> value that represents the type of schema query to run.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <parameterReference>Criteria </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> An array of query constraints for each <parameterReference>QueryType</parameterReference> option, as listed in <legacyLink xlink:href="21c97651-297f-469f-b5b5-c48af72b62a8">SchemaEnum</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <parameterReference>SchemaID </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">The GUID for a provider-schema query not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> This parameter is required if <parameterReference>QueryType</parameterReference> is set to <legacyBold>adSchemaProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">The <unmanagedCodeEntityReference>OpenSchema</unmanagedCodeEntityReference> method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">The <parameterReference>QueryType</parameterReference> argument is a GUID that indicates the columns (schemas) returned.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The OLE DB specification has a full list of schemas.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">The <parameterReference>Criteria</parameterReference> argument limits the results of a schema query.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence">
              <parameterReference>Criteria</parameterReference> specifies an array of values that must occur in a corresponding subset of columns, called constraint columns, in the resulting <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">The constant <legacyBold>adSchemaProviderSpecific</legacyBold> is used for the <parameterReference>QueryType</parameterReference> argument if the provider defines its own nonstandard schema queries outside those listed previously.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> When this constant is used, the <parameterReference>SchemaID</parameterReference> argument is required to pass the GUID of the schema query to execute.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> If <parameterReference>QueryType</parameterReference> is set to <legacyBold>adSchemaProviderSpecific</legacyBold> but <parameterReference>SchemaID</parameterReference> is not provided, an error will result.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">Providers are not required to support all the OLE DB standard schema queries.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Specifically, only <legacyBold>adSchemaTables</legacyBold>, <legacyBold>adSchemaColumns</legacyBold>, and <legacyBold>adSchemaProviderTypes</legacyBold> are required by the OLE DB specification.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> However, the provider is not required to support the <parameterReference>Criteria</parameterReference> constraints listed earlier for those schema queries.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src24" class="srcSentence">
                <legacyBold>Remote Data Service Usage</legacyBold>   The <unmanagedCodeEntityReference>OpenSchema</unmanagedCodeEntityReference> method is not available on a client-side <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src25" class="srcSentence">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> returned from the <unmanagedCodeEntityReference>OpenSchema</unmanagedCodeEntityReference> method on the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object cannot be compared to other variables.</caps:sentence>
              <caps:sentence id="src26" class="srcSentence"> For more information about OLE DB data types, see <legacyLink xlink:href="6039292f-74e0-49b2-b133-17bc117ebf6a">Data Types in OLE DB (OLE DB)</legacyLink> and <legacyLink xlink:href="e3a0533a-2196-4eb0-a31e-92fe9556ada6">Appendix A: Data Types</legacyLink> in the Microsoft OLE DB Programmer's Reference.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src27" class="srcSentence">
                <legacyBold>Visual C/C++ Users</legacyBold>   When not using client-side cursors, retrieving the "ORDINAL_POSITION" of a column schema in ADO returns a variant of type VT_R8 in MDAC 2.7, MDAC 2.8, and Windows Data Access Components (Windows DAC) 6.0, while the type used in MDAC 2.6 was VT_I4.</caps:sentence>
              <caps:sentence id="src28" class="srcSentence"> Programs written for MDAC 2.6 that only look for a variant returned of type VT_I4 would get a zero for every ordinal if run under MDAC 2.7, MDAC 2.8, and Windows DAC 6.0 without modification.</caps:sentence>
              <caps:sentence id="src29" class="srcSentence"> This change was made because the data type that OLE DB returns is DBTYPE_UI4, and in the signed VT_I4 type there is not enough room to contain all possible values without possibly truncation occurring and thereby causing a loss of data.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src30" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="455a02f0-8143-4562-8648-8fb45ffd334c">Visual Basic Example</link>
        <link xlink:href="6f3da460-0f49-41e0-999d-a754ec1d887e">Visual C++ Example</link>
        <link xlink:href="4c1240f1-7464-47db-9761-2d547419aedd">Visual J++ Example</link>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
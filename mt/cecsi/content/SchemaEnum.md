---
title: "SchemaEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 21c97651-297f-469f-b5b5-c48af72b62a8
caps.latest.revision: 14
caps.handback.revision: 14
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
# SchemaEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f10f653abc86108111b24efe6e6f62ab" id="tgt1" class="tgtSentence">Specifies the type of schema <legacyBold>Recordset</legacyBold> that the <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method retrieves.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="536d807c05fb6481a21c520e5fb5ed42" id="tgt2" class="tgtSentence">Additional information about the function and columns returned for each ADO constant can be found in topics in <legacyLink xlink:href="2b5fbf03-e50d-44ee-bc57-5a57666c55f1">Appendix B: Schema Rowsets</legacyLink> of the OLE DB Programmer's Reference.</caps:sentence>
            <caps:sentence sentenceid="f012cdcd70a45b11fb6cf42b0edb78c9" id="tgt3" class="tgtSentence"> The name of each topic is listed in parentheses in the Description section of the following table.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5c7b13abf7e6884078718bc30d61bfa4" id="tgt4" class="tgtSentence">Additional information about the function and columns returned for each ADO MD constant can be found in topics in <legacyLink xlink:href="d20bb2a6-68bd-423f-9ec8-eb930cd0c144">OLE DB for OLAP Objects and Schema Rowsets</legacyLink> in the OLE DB for Online Analytical Processing (OLAP) documentation.</caps:sentence>
            <caps:sentence sentenceid="a84f61d1c54167518ff205e9f7b0de86" id="tgt5" class="tgtSentence"> The name of each topic is listed in parentheses in the Description column of the following table.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9b00369348af61b5b88e7b56d9e30e8a" id="tgt6" class="tgtSentence">You can translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> topic.</caps:sentence>
            <caps:sentence sentenceid="f6ce822b6f5b89209bc48ba635b4b421" id="tgt7" class="tgtSentence"> For example, an OLE DB data type of <legacyBold>DBTYPE_WSTR</legacyBold> is equivalent to an ADO data type of <legacyBold>adWChar</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3f39788cabb6c9c3f19ef74ff6e071a0" id="tgt8" class="tgtSentence">ADO generates schema-like results for the constants, <legacyBold>adSchemaDBInfoKeywords</legacyBold> and <legacyBold>adSchemaDBInfoLiterals</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="f14c878c841c38d803f2d1722469f27f" id="tgt9" class="tgtSentence"> ADO creates a <legacyBold>Recordset</legacyBold>, and then fills each row with the values returned respectively by the <legacyBold>IDBInfo::GetKeywords</legacyBold> and <legacyBold>IDBInfo::GetLiteralInfo</legacyBold> methods.</caps:sentence>
            <caps:sentence sentenceid="a5ed0514c2d7f8fc0bd6387349a58454" id="tgt10" class="tgtSentence"> Additional information about these methods can be found in the <legacyLink xlink:href="3f5ad97f-3fc6-4f21-b691-f6911e4007f3">IDBInfo</legacyLink> section of the OLE DB Programmer's Reference.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt11" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt12" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt13" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1980c3c792ec12a5851e5259ca342f07" id="tgt14" class="tgtSentence">Constraint Columns</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="91b2d98707d20eab9c4d78e68a527807" id="tgt15" class="tgtSentence">
                      <legacyBold>adSchemaAsserts</legacyBold>    </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt16" class="tgtSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa04371ae9781e71115a3e42ac47d30d" id="tgt17" class="tgtSentence">Returns the assertions defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="0ae0abd34ef8ac356133f57fa7940797" id="tgt18" class="tgtSentence">(ASSERTIONS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc6c738074b4d39be5977388885b0c88" id="tgt19" class="tgtSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f7a200686737ecb35041483177bfdefd" id="tgt20" class="tgtSentence">
                      <legacyBold>adSchemaCatalogs</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt21" class="tgtSentence">1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c78a4ce1fea7a04dab36d865a14bc8aa" id="tgt22" class="tgtSentence">Returns the physical attributes associated with catalogs accessible from the DBMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="a1752880ad847f8b562bea4ec14c6e05" id="tgt23" class="tgtSentence">(CATALOGS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="449a7974f8ec4c54d1897e5083fc3606" id="tgt24" class="tgtSentence">CATALOG_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b080d0d6f810dbc94aa510ca20682524" id="tgt25" class="tgtSentence">
                      <legacyBold>adSchemaCharacterSets</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt26" class="tgtSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30bf75433a685efda3770b6b1214d247" id="tgt27" class="tgtSentence">Returns the character sets defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="a2bdb6da8ad2fad1e0da0fa0e9dee7ff" id="tgt28" class="tgtSentence">(CHARACTER_SETS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="319179cbfea26ce0e733f9d8e0da1003" id="tgt29" class="tgtSentence">CHARACTER_SET_CATALOG CHARACTER_SET_SCHEMA CHARACTER_SET_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="155be743d8a23acbbf8feda6b4d6ca48" id="tgt30" class="tgtSentence">
                      <legacyBold>adSchemaCheckConstraints</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4da3b7fbbce2345d7772b0674a318d5" id="tgt31" class="tgtSentence">5</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f10ac2b9fadfa909d067019118a65e5e" id="tgt32" class="tgtSentence">Returns the check constraints defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="3b528ca2862d98e3b25444b82edf3636" id="tgt33" class="tgtSentence">(CHECK_CONSTRAINTS) Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc6c738074b4d39be5977388885b0c88" id="tgt34" class="tgtSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d3e87b766ff87a998e1979f379e7e0f" id="tgt35" class="tgtSentence">
                      <legacyBold>adSchemaCollations</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt36" class="tgtSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4c0aa8003cbe41cbeaa33da500db190c" id="tgt37" class="tgtSentence">Returns the character collations defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d00283ffcdebafc1c267fcbb28611937" id="tgt38" class="tgtSentence">(COLLATIONS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="317916f664a65a41c9033aa68d5608e7" id="tgt39" class="tgtSentence">COLLATION_CATALOG COLLATION_SCHEMA COLLATION_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f03ea07f6ae07464044bcf14c3f94c9" id="tgt40" class="tgtSentence">
                      <legacyBold>adSchemaColumnPrivileges</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c51ce410c124a10e0db5e4b97fc2af39" id="tgt41" class="tgtSentence">13</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ff374194a721459aa111186e91d8d91c" id="tgt42" class="tgtSentence">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="a6107b82977ed437ca343ce018717b73" id="tgt43" class="tgtSentence">(COLUMN_PRIVILEGES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f716085d0481515c7de01f6a32204c05" id="tgt44" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME COLUMN_NAME GRANTOR GRANTEE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3830e2c125e309209cc1ea2337df634a" id="tgt45" class="tgtSentence">
                      <legacyBold>adSchemaColumns</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt46" class="tgtSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="585fe9ac51f62bb54d40f22e31746b49" id="tgt47" class="tgtSentence">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b9911b415e4c05cd51a56fc7dce34601" id="tgt48" class="tgtSentence">(COLUMNS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c6190d1f1331d488ee255bcd58fd9e4b" id="tgt49" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6783b5dd1f59e222b85b6b4d3df771ff" id="tgt50" class="tgtSentence">
                      <legacyBold>adSchemaColumnsDomainUsage</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6512bd43d9caa6e02c990b0a82652dca" id="tgt51" class="tgtSentence">11</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b307214086a8648a2ca1cf1277d6a465" id="tgt52" class="tgtSentence">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="8fd625f41d4e36a3337dd716207f57da" id="tgt53" class="tgtSentence">(COLUMN_DOMAIN_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1faac5f83db6f8d1290fef0445d24107" id="tgt54" class="tgtSentence">DOMAIN_CATALOG DOMAIN_SCHEMA DOMAIN_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="93cccc98a7866292cf04418b9636667e" id="tgt55" class="tgtSentence">
                      <legacyBold>adSchemaConstraintColumnUsage</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1679091c5a880faf6fb5e6087eb1b2dc" id="tgt56" class="tgtSentence">6</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="463b24a4ab58581e08dceb9f2b6de6f2" id="tgt57" class="tgtSentence">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="7dde4353e67c073aa7e7d8b3f1d9a88e" id="tgt58" class="tgtSentence">(CONSTRAINT_COLUMN_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c6190d1f1331d488ee255bcd58fd9e4b" id="tgt59" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e99e3ce835c82666e8b22de51261637d" id="tgt60" class="tgtSentence">adSchemaConstraintTableUsage</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f14e45fceea167a5a36dedd4bea2543" id="tgt61" class="tgtSentence">7</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="271c3417f35aad9fde9b90502c62fd7b" id="tgt62" class="tgtSentence">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="cc84966cfc288becbcfc379e944dc9db" id="tgt63" class="tgtSentence">(CONSTRAINT_TABLE_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c3f010e61203634a15882d4af2612805" id="tgt64" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0899732c1576d79a7cf3d227373ab046" id="tgt65" class="tgtSentence">
                      <legacyBold>adSchemaCubes</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6364d3f0f495b6ab9dcf8d3b5c6e0b01" id="tgt66" class="tgtSentence">32</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4f56cf47a08cedf586aa325e5b7cf607" id="tgt67" class="tgtSentence">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="081e088e176d0e0417e54a0d23c741e1" id="tgt68" class="tgtSentence">(CUBES Rowset*)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="85bc25ca093a1326a4760d9aa8728890" id="tgt69" class="tgtSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a993ba741d0c4026b1ea0f12f741da62" id="tgt70" class="tgtSentence">
                      <legacyBold>adSchemaDBInfoKeywords</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34173cb38f07f89ddbebc2ac9128303f" id="tgt71" class="tgtSentence">30</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f8343ddb2f51ad4bdce935c7dc61d7f" id="tgt72" class="tgtSentence">Returns a list of provider-specific keywords.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f7c88e9c73444946f85220a7fef207dd" id="tgt73" class="tgtSentence">(IDBInfo::GetKeywords)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87942d9f16a9a5cb97a799e15ef3d183" id="tgt74" class="tgtSentence">&lt;None&gt;</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9122e5ae72f3b5bc9998de23ab2e32be" id="tgt75" class="tgtSentence">
                      <legacyBold>adSchemaDBInfoLiterals</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c16a5320fa475530d9583c34fd356ef5" id="tgt76" class="tgtSentence">31</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a1f595042330eda517b1b88eae4e7eb1" id="tgt77" class="tgtSentence">Returns a list of provider-specific literals used in text commands.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e35032721108e8f4d563df1a82b4b8b5" id="tgt78" class="tgtSentence">(IDBInfo::GetLiteralInfo)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87942d9f16a9a5cb97a799e15ef3d183" id="tgt79" class="tgtSentence">&lt;None&gt;</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9d036c6e3ea2cfd0fb845fa436caa2d0" id="tgt80" class="tgtSentence">
                      <legacyBold>adSchemaDimensions</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="182be0c5cdcd5072bb1864cdee4d3d6e" id="tgt81" class="tgtSentence">33</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d49b22066c50b9578f283d510ad50a17" id="tgt82" class="tgtSentence">Returns information about the dimensions in a given cube.</caps:sentence>
                    <caps:sentence sentenceid="8c2e538730f5968c5375bf2baacc4376" id="tgt83" class="tgtSentence"> It has one row for each dimension.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="028c095ae9cba74cda61b03de0a63078" id="tgt84" class="tgtSentence">(DIMENSIONS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="86f5e8994784f001a82907d38517f26f" id="tgt85" class="tgtSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_NAME DIMENSION_UNIQUE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ec35adeb42891a48a8f4d26a04a3e25" id="tgt86" class="tgtSentence">
                      <legacyBold>adSchemaForeignKeys</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="02e74f10e0327ad868d138f2b4fdd6f0" id="tgt87" class="tgtSentence">27</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00ab0ca396014be0be52895110a33f5b" id="tgt88" class="tgtSentence">Returns the foreign key columns defined in the catalog by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="771bef8fc16b59d1cb655518b82e626a" id="tgt89" class="tgtSentence">(FOREIGN_KEYS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cc1688f5e4b6bfd492985c8e489f26f" id="tgt90" class="tgtSentence">PK_TABLE_CATALOG PK_TABLE_SCHEMA PK_TABLE_NAME FK_TABLE_CATALOG FK_TABLE_SCHEMA FK_TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4e3fe5f1fa1b06f9b1239d15bab5f712" id="tgt91" class="tgtSentence">
                      <legacyBold>adSchemaHierarchies</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e369853df766fa44e1ed0ff613f563bd" id="tgt92" class="tgtSentence">34</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5ec26ed77854aad3496119493a76cef4" id="tgt93" class="tgtSentence">Returns information about the hierarchies available in a dimension.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="c5d6d8fd46dd2f813793c7d83321413a" id="tgt94" class="tgtSentence">(HIERARCHIES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b17115859cd6ce4c7dcfa58cb13ecdf1" id="tgt95" class="tgtSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_UNIQUE_NAME HIERARCHY_NAME HIERARCHY_UNIQUE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8d15fe275ffb49406cacd7a9449f5b95" id="tgt96" class="tgtSentence">
                      <legacyBold>adSchemaIndexes</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c20ad4d76fe97759aa27a0c99bff6710" id="tgt97" class="tgtSentence">12</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d8749aeda9a863c9911e582e58a0e91a" id="tgt98" class="tgtSentence">Returns the indexes defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="952d01eb439c7eec987974429ac3c4ec" id="tgt99" class="tgtSentence">(INDEXES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ce9e1ce33e261791e7d3cd63ca6f2138" id="tgt100" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA INDEX_NAME TYPE TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f42ee85f69f739ba71835a258e0101a" id="tgt101" class="tgtSentence">
                      <legacyBold>adSchemaKeyColumnUsage</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c9f0f895fb98ab9159f51fd0297e236d" id="tgt102" class="tgtSentence">8</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a4308fd4174bd30dc37bd46e6df1d8ae" id="tgt103" class="tgtSentence">Returns the columns defined in the catalog that are constrained as keys by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="98c6ac964c974ddb9092b065f5657c32" id="tgt104" class="tgtSentence">(KEY_COLUMN_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e1d94e351f0e42c0ecb94bcea0d15edd" id="tgt105" class="tgtSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME TABLE_CATALOG TABLE_SCHEMA TABLE_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="768d042822a82b2a289ffc8e5510a0f1" id="tgt106" class="tgtSentence">
                      <legacyBold>adSchemaLevels</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1c383cd30b7c298ab50293adfecb7b18" id="tgt107" class="tgtSentence">35</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5b17dd1abe310cd72c08e1ee800d0b02" id="tgt108" class="tgtSentence">Returns information about the levels available in a dimension.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="0d7c6b763e4fd41fc32b2580c80ff5e8" id="tgt109" class="tgtSentence">(LEVELS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ef6f64f3b1f5f5d2947a62db05872866" id="tgt110" class="tgtSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_UNIQUE_NAME HIERARCHY_UNIQUE_NAME LEVEL_NAME LEVEL_UNIQUE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a62643228ca819678d597583de89c9f7" id="tgt111" class="tgtSentence">
                      <legacyBold>adSchemaMeasures</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="19ca14e7ea6328a42e0eb13d585e4c22" id="tgt112" class="tgtSentence">36</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ccbf6b428b7f369f4a77fd7e497c9b68" id="tgt113" class="tgtSentence">Returns information about the available measures.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="07aa055a9d465ffd6b62155385d20558" id="tgt114" class="tgtSentence">(MEASURES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44ae5bbdafaacb887da97cb31ebb6f4f" id="tgt115" class="tgtSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME MEASURE_NAME MEASURE_UNIQUE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5bc6d5cf6c19c563a3d5b17489c31875" id="tgt116" class="tgtSentence">
                      <legacyBold>adSchemaMembers</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a5771bce93e200c36f7cd9dfd0e5deaa" id="tgt117" class="tgtSentence">38</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f1e99c50ef6673ec1fd4405a0d55d83f" id="tgt118" class="tgtSentence">Returns information about the available members.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="69ac4ed2c65df1856305fd24d8bb3a02" id="tgt119" class="tgtSentence">(MEMBERS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="377b819225d91e217657c49b3a9397f9" id="tgt120" class="tgtSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_UNIQUE_NAME HIERARCHY_UNIQUE_NAME LEVEL_UNIQUE_NAME LEVEL_NUMBER MEMBER_NAME MEMBER_UNIQUE_NAME MEMBER_CAPTION MEMBER_TYPE Tree operator.</caps:sentence>
                    <caps:sentence sentenceid="61aae6d35d0bf482332d8dc0da0e975a" id="tgt121" class="tgtSentence"> For more information, see OLE DB for Online Analytical Processing (OLAP).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b5e873853519dd836a37318c8a07b93" id="tgt122" class="tgtSentence">
                      <legacyBold>adSchemaPrimaryKeys</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="33e75ff09dd601bbe69f351039152189" id="tgt123" class="tgtSentence">28</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="55f0451bfa9136e8ce07da2f633bdc8f" id="tgt124" class="tgtSentence">Returns the primary key columns defined in the catalog by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b5eaf2d3d57984d843b9ebb5fedca814" id="tgt125" class="tgtSentence">(PRIMARY_KEYS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f753c1b12327845f584ea8c54f37d55" id="tgt126" class="tgtSentence">PK_TABLE_CATALOG PK_TABLE_SCHEMA PK_TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="56d620b747e3b5c414526f185b9ea2f6" id="tgt127" class="tgtSentence">
                      <legacyBold>adSchemaProcedureColumns</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ea9ab1baa0efb9e19094440c317e21b" id="tgt128" class="tgtSentence">29</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bef867752e649ba9c3df850551c56dfd" id="tgt129" class="tgtSentence">Returns information about the columns of rowsets returned by procedures.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b149d099091acd6e181b552fbd83e024" id="tgt130" class="tgtSentence">(PROCEDURE_COLUMNS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="40438a500e459c5d6c4e7dde0ff8b0b9" id="tgt131" class="tgtSentence">PROCEDURE_CATALOG PROCEDURE_SCHEMA PROCEDURE_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d8147c1e3352b2bd8e1a5e61d1d8bf02" id="tgt132" class="tgtSentence">
                      <legacyBold>adSchemaProcedureParameters</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4e732ced3463d06de0ca9a15b6153677" id="tgt133" class="tgtSentence">26</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94e0844f971915bfb7025d52092d1350" id="tgt134" class="tgtSentence">Returns information about the parameters and return codes of procedures.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="503f88209bb3161ade83815736ae3453" id="tgt135" class="tgtSentence">(PROCEDURE_PARAMETERS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cdd878629a5dcd145327c418fc420c29" id="tgt136" class="tgtSentence">PROCEDURE_CATALOG PROCEDURE_SCHEMA PROCEDURE_NAME PARAMETER_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c2a8747b90aec6a02beaf0ebbc219c5" id="tgt137" class="tgtSentence">
                      <legacyBold>adSchemaProcedures</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c74d97b01eae257e44aa9d5bade97baf" id="tgt138" class="tgtSentence">16</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c3d80113aa7863dab23ce8048a328575" id="tgt139" class="tgtSentence">Returns the procedures defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b8a6a66bdd28f632dd82ee6c4816d912" id="tgt140" class="tgtSentence">(PROCEDURES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="443c0f6ee788c9a4f711ef903e0f46b8" id="tgt141" class="tgtSentence">PROCEDURE_CATALOG PROCEDURE_SCHEMA PROCEDURE_NAME PROCEDURE_TYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa73f50171a2da9eb02a2b88d2f6a953" id="tgt142" class="tgtSentence">
                      <legacyBold>adSchemaProperties</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a5bfc9e07964f8dddeb95fc584cd965d" id="tgt143" class="tgtSentence">37</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ca2ac96521b2c02db9c3aef9c78aac1" id="tgt144" class="tgtSentence">Returns information about the available properties for each level of the dimension.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="52f532408c7e82078e1169e3677b033e" id="tgt145" class="tgtSentence">(PROPERTIES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5c702441fe915f111b4d297f1fca5ecf" id="tgt146" class="tgtSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_UNIQUE_NAME HIERARCHY_UNIQUE_NAME LEVEL_UNIQUE_NAME MEMBER_UNIQUE_NAME PROPERTY_TYPE PROPERTY_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92305ec1ad13e1e496c39083859d2937" id="tgt147" class="tgtSentence">
                      <legacyBold>adSchemaProviderSpecific</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt148" class="tgtSentence">-1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1eed554aaa376238d169bedaa35c801c" id="tgt149" class="tgtSentence">Used if the provider defines its own nonstandard schema queries.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30654f6ec7e1a0b30ccb75448d331bd2" id="tgt150" class="tgtSentence">&lt;Provider specific&gt;</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="869c3846beac39eb65b5e58a43d376be" id="tgt151" class="tgtSentence">adSchemaProviderTypes</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b6d767d2f8ed5d21a44b0e5886680cb9" id="tgt152" class="tgtSentence">22</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="460521033d4644313bc30df6eb697652" id="tgt153" class="tgtSentence">Returns the (base) data types supported by the data provider.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="bb64e67d3bfa4fbe1a6ba7a5c92b859f" id="tgt154" class="tgtSentence">(PROVIDER_TYPES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e956b92a2d312fea9b6debd811f42f7b" id="tgt155" class="tgtSentence">DATA_TYPE BEST_MATCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90bb8bf0dde5c52a94abbc8fde55551e" id="tgt156" class="tgtSentence">
                      <legacyBold>AdSchemaReferentialConstraints</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45c48cce2e2d7fbdea1afc51c7c6ad26" id="tgt157" class="tgtSentence">9</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="413cff280d4465133f57668efd6c7322" id="tgt158" class="tgtSentence">Returns the referential constraints defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="8ba710a44879165d1b615066646333bd" id="tgt159" class="tgtSentence">(REFERENTIAL_CONSTRAINTS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc6c738074b4d39be5977388885b0c88" id="tgt160" class="tgtSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9dcb64d46140ec99e575d54ee3b0d05d" id="tgt161" class="tgtSentence">
                      <legacyBold>adSchemaSchemata</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="70efdf2ec9b086079795c442636b55fb" id="tgt162" class="tgtSentence">17</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="afe922d3930e5915b87618f6f864f9ff" id="tgt163" class="tgtSentence">Returns the schemas (database objects) that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="54c036a21c90af82b95ef9ec07ac4998" id="tgt164" class="tgtSentence">(SCHEMATA Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b21b9ce41e52217892032c23fb58e4ec" id="tgt165" class="tgtSentence">CATALOG_NAME SCHEMA_NAME SCHEMA_OWNER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="08da9ca034a5159f20171a2c9ba8b587" id="tgt166" class="tgtSentence">
                      <legacyBold>adSchemaSQLLanguages</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f4922f45568161a8cdf4ad2299f6d23" id="tgt167" class="tgtSentence">18</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a99ae1b34afc337cef4a5487e3c2a5b8" id="tgt168" class="tgtSentence">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="ed79bb9fbba84952437d4c8c351076b5" id="tgt169" class="tgtSentence">(SQL_LANGUAGES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87942d9f16a9a5cb97a799e15ef3d183" id="tgt170" class="tgtSentence">&lt;None&gt;</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db88e43c60c35620431784878f2e0782" id="tgt171" class="tgtSentence">
                      <legacyBold>adSchemaStatistics</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1f0e3dad99908345f7439f8ffabdffc4" id="tgt172" class="tgtSentence">19</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be521b27d5611e2d6c1c776e60f359be" id="tgt173" class="tgtSentence">Returns the statistics defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1e4a4fff98c8212f3caf47e8d0b93266" id="tgt174" class="tgtSentence">(STATISTICS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c3f010e61203634a15882d4af2612805" id="tgt175" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e43dc09a3f70200e166210c98039cccf" id="tgt176" class="tgtSentence">
                      <legacyBold>adSchemaTableConstraints</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3d9446802a44259755d38e6d163e820" id="tgt177" class="tgtSentence">10</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7f3bb39c6641042354d235ff9cf82ab8" id="tgt178" class="tgtSentence">Returns the table constraints defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="fb6f5b627e81d6ba60780f8e776eec62" id="tgt179" class="tgtSentence">(TABLE_CONSTRAINTS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f3ed03a1bd32179e483029830120b599" id="tgt180" class="tgtSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME TABLE_CATALOG TABLE_SCHEMA TABLE_NAME CONSTRAINT_TYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba8a029c980021193bf2651e92f202e8" id="tgt181" class="tgtSentence">
                      <legacyBold>adSchemaTablePrivileges</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aab3238922bcc25a6f606eb525ffdc56" id="tgt182" class="tgtSentence">14</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="de18ba5adc48ee5368f11858974dfc24" id="tgt183" class="tgtSentence">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="41846c5b60d5bdfe21e227794dc3a6e2" id="tgt184" class="tgtSentence">(TABLE_PRIVILEGES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cd7f306f3402b50cbe93d21bcd652fa4" id="tgt185" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME GRANTOR GRANTEE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2308f1a575a0f790f15ed6fbba37737a" id="tgt186" class="tgtSentence">
                      <legacyBold>adSchemaTables</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98f13708210194c475687be6106a3b84" id="tgt187" class="tgtSentence">20</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12d09efbbe759819ebd6733c9a3f950b" id="tgt188" class="tgtSentence">Returns the tables (including views) defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="10b82035db1412fed65b1f5e04661fad" id="tgt189" class="tgtSentence">(TABLES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17a136ca75a8ae876029b4dcf39482ca" id="tgt190" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME TABLE_TYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae60fcbc6749d40825e60d205bdc4c03" id="tgt191" class="tgtSentence">
                      <legacyBold>adSchemaTranslations</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c59dc048e8850243be8079a5c74d079" id="tgt192" class="tgtSentence">21</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87fdb6a643dcb960ce17a7cd03db6b4b" id="tgt193" class="tgtSentence">Returns the character translations defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1fc6d56f61b244ad4a8deb8b81d2e18f" id="tgt194" class="tgtSentence">(TRANSLATIONS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5710a314a21602fb8318a8702fa33b01" id="tgt195" class="tgtSentence">TRANSLATION_CATALOG TRANSLATION_SCHEMA TRANSLATION_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba7015f20b60a887685178f542131640" id="tgt196" class="tgtSentence">
                      <legacyBold>adSchemaTrustees</legacyBold>    </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d67d8ab4f4c10bf22aa353e27879133c" id="tgt197" class="tgtSentence">39</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8efc7c9e1c53492a25acfb399445dbcb" id="tgt198" class="tgtSentence">Reserved for future use.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="73a67e64fab18499b71b89ccc2176102" id="tgt199" class="tgtSentence">
                      <legacyBold>adSchemaUsagePrivileges</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9bf31c7ff062936a96d3c8bd1f8f2ff3" id="tgt200" class="tgtSentence">15</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e32f0cc174f4391b2ee0d47ee3f8ce9f" id="tgt201" class="tgtSentence">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="81be6b18f83127b66d78e10563a97fa2" id="tgt202" class="tgtSentence">(USAGE_PRIVILEGES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44571e0476e7b1b55f945e029e6f0612" id="tgt203" class="tgtSentence">OBJECT_CATALOG OBJECT_SCHEMA OBJECT_NAME OBJECT_TYPE GRANTOR GRANTEE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cdf6cba24240d2797b369fb31306d937" id="tgt204" class="tgtSentence">
                      <legacyBold>adSchemaViewColumnUsage</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ff1de774005f8da13f42943881c655f" id="tgt205" class="tgtSentence">24</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c818826c97b035fcf1089f597d811444" id="tgt206" class="tgtSentence">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="78fd3146ed8a8eab9ab3f369db9ca526" id="tgt207" class="tgtSentence">(VIEW_COLUMN_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fe8d34e731c30d50e9d3f2d119f567" id="tgt208" class="tgtSentence">VIEW_CATALOG VIEW_SCHEMA VIEW_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="380fc384b63e5a1321e451692910e36f" id="tgt209" class="tgtSentence">
                      <legacyBold>adSchemaViews</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37693cfc748049e45d87b8c7d8b9aacd" id="tgt210" class="tgtSentence">23</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1508aedc7444f6b27cf5177f88305453" id="tgt211" class="tgtSentence">Returns the views defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="0891787d3e62ed8c0c007b1532579d3e" id="tgt212" class="tgtSentence">(VIEWS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c3f010e61203634a15882d4af2612805" id="tgt213" class="tgtSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0992b14ebbec6b5c6e6895484ecb772e" id="tgt214" class="tgtSentence">
                      <legacyBold>adSchemaViewTableUsage</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8e296a067a37563370ded05f5a3bf3ec" id="tgt215" class="tgtSentence">25</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b6464c7a19ec0692f24ee7738a16bc18" id="tgt216" class="tgtSentence">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b1d5dbe78ab9e297166727f61d13a042" id="tgt217" class="tgtSentence">(VIEW_TABLE_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fe8d34e731c30d50e9d3f2d119f567" id="tgt218" class="tgtSentence">VIEW_CATALOG VIEW_SCHEMA VIEW_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt219" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt220" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt221" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="764bf289d3670ed8bf032a6a4a2f4482" id="tgt222" class="tgtSentence">AdoEnums.Schema.ASSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="efbe9559a8d8710da05b710042d45f0b" id="tgt223" class="tgtSentence">AdoEnums.Schema.CATALOGS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8c1917dc731ae81dd4504d16249225c2" id="tgt224" class="tgtSentence">AdoEnums.Schema.CHARACTERSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45bfba1ddea44e47c46684b7d7de65c4" id="tgt225" class="tgtSentence">AdoEnums.Schema.CHECKCONSTRAINTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7409821659a593621a1719359c7adad5" id="tgt226" class="tgtSentence">AdoEnums.Schema.COLLATIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="293f66bc2c46844983e3c7156d2fa94b" id="tgt227" class="tgtSentence">AdoEnums.Schema.COLUMNPRIVILEGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="57676a77ca5b3f4cceaaecae09f84ef4" id="tgt228" class="tgtSentence">AdoEnums.Schema.COLUMNS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b6cade4a8fb731329495533db1dc456c" id="tgt229" class="tgtSentence">AdoEnums.Schema.COLUMNSDOMAINUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cddccdd6fd0862d5a691076c03f6f4c7" id="tgt230" class="tgtSentence">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c7f62ec3d9ecd393a89e1dc62980b91" id="tgt231" class="tgtSentence">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="38eeabcf3915eb218cc87dd6d6d5e7d8" id="tgt232" class="tgtSentence">AdoEnums.Schema.CUBES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8016043da8be717a2907ebdb6ff6c1b8" id="tgt233" class="tgtSentence">AdoEnums.Schema.DBINFOKEYWORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="354eaf6c6434f11290852aa0354916dd" id="tgt234" class="tgtSentence">AdoEnums.Schema.DBINFOLITERALS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="79fbe841a7f3b74cca2bf42cdb922ad1" id="tgt235" class="tgtSentence">AdoEnums.Schema.DIMENSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9190446d2c66d21b3afc267ce0edbd9f" id="tgt236" class="tgtSentence">AdoEnums.Schema.FOREIGNKEYS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="33dff8c8b70bf229615229e22b6e8d18" id="tgt237" class="tgtSentence">AdoEnums.Schema.HIERARCHIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0edd11ca6bfda8120dd6e8ffc1579094" id="tgt238" class="tgtSentence">AdoEnums.Schema.INDEXES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a580a456abe181380f7b4576df5ee15" id="tgt239" class="tgtSentence">AdoEnums.Schema.KEYCOLUMNUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9350b07fdf2075c58ac5559ad99a93f6" id="tgt240" class="tgtSentence">AdoEnums.Schema.LEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="41e08b18f8b7996703a09d61e98d385e" id="tgt241" class="tgtSentence">AdoEnums.Schema.MEASURES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="69fee2aa6f0cb5356d938daadc4c3a6f" id="tgt242" class="tgtSentence">AdoEnums.Schema.MEMBERS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cd3d420a839b4dc5ee84d5290d1d077c" id="tgt243" class="tgtSentence">AdoEnums.Schema.PRIMARYKEYS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="79a32a0bb99229d0a6eb8d85dd3062f6" id="tgt244" class="tgtSentence">AdoEnums.Schema.PROCEDURECOLUMNS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db35749544858fed935ce61ae1548cbe" id="tgt245" class="tgtSentence">AdoEnums.Schema.PROCEDUREPARAMETERS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="73fee402beeac5a9a4171fa790361d1f" id="tgt246" class="tgtSentence">AdoEnums.Schema.PROCEDURES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c666537c7011411e2f92326fe4354d9" id="tgt247" class="tgtSentence">AdoEnums.Schema.PROPERTIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="69b352be9dff0b3a8b3a1bce931c076a" id="tgt248" class="tgtSentence">AdoEnums.Schema.PROVIDERSPECIFIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="10d4935d71a4c8eda8c3cdb8d9e2e33c" id="tgt249" class="tgtSentence">AdoEnums.Schema.PROVIDERTYPES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f6777978afcad82e60433d659111be9" id="tgt250" class="tgtSentence">AdoEnums.Schema.REFERENTIALCONTRAINTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f4037a228abd721e99c39fd133afc902" id="tgt251" class="tgtSentence">AdoEnums.Schema.SCHEMATA</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3bb1fa2bb159dbb35d694ea8bc974c1b" id="tgt252" class="tgtSentence">AdoEnums.Schema.SQLLANGUAGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="919859a53a473a5afee18f0e35b07b99" id="tgt253" class="tgtSentence">AdoEnums.Schema.STATISTICS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2679c0c25dd78c235b38e44fe0d81e3a" id="tgt254" class="tgtSentence">AdoEnums.Schema.TABLECONSTRAINTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fbf0282f2ffa47ef0c04421dba24688b" id="tgt255" class="tgtSentence">AdoEnums.Schema.TABLEPRIVILEGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ff31f793b2364dc6eccfd3eccb383cd" id="tgt256" class="tgtSentence">AdoEnums.Schema.TABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="864a26fc5fb8b19da7c9c6c45380e60a" id="tgt257" class="tgtSentence">AdoEnums.Schema.TRANSLATIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b8c309b5b26f78f1879137d0109642fe" id="tgt258" class="tgtSentence">AdoEnums.Schema.TRUSTEES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d68350ee54d54666c5dff18fe1bab5b2" id="tgt259" class="tgtSentence">AdoEnums.Schema.USAGEPRIVILEGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17f0ccce108fe32bd1c60fdad57afda7" id="tgt260" class="tgtSentence">AdoEnums.Schema.VIEWCOLUMNUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4c39ac311c4c24841f9c4c419b367da0" id="tgt261" class="tgtSentence">AdoEnums.Schema.VIEWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6dccb5aa894c197e42571e4c1c3ca4f" id="tgt262" class="tgtSentence">AdoEnums.Schema.VIEWTABLEUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt263" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies the type of schema <legacyBold>Recordset</legacyBold> that the <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method retrieves.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Additional information about the function and columns returned for each ADO constant can be found in topics in <legacyLink xlink:href="2b5fbf03-e50d-44ee-bc57-5a57666c55f1">Appendix B: Schema Rowsets</legacyLink> of the OLE DB Programmer's Reference.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The name of each topic is listed in parentheses in the Description section of the following table.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">Additional information about the function and columns returned for each ADO MD constant can be found in topics in <legacyLink xlink:href="d20bb2a6-68bd-423f-9ec8-eb930cd0c144">OLE DB for OLAP Objects and Schema Rowsets</legacyLink> in the OLE DB for Online Analytical Processing (OLAP) documentation.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The name of each topic is listed in parentheses in the Description column of the following table.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">You can translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> topic.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> For example, an OLE DB data type of <legacyBold>DBTYPE_WSTR</legacyBold> is equivalent to an ADO data type of <legacyBold>adWChar</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">ADO generates schema-like results for the constants, <legacyBold>adSchemaDBInfoKeywords</legacyBold> and <legacyBold>adSchemaDBInfoLiterals</legacyBold>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> ADO creates a <legacyBold>Recordset</legacyBold>, and then fills each row with the values returned respectively by the <legacyBold>IDBInfo::GetKeywords</legacyBold> and <legacyBold>IDBInfo::GetLiteralInfo</legacyBold> methods.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Additional information about these methods can be found in the <legacyLink xlink:href="3f5ad97f-3fc6-4f21-b691-f6911e4007f3">IDBInfo</legacyLink> section of the OLE DB Programmer's Reference.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Constraint Columns</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">
                      <legacyBold>adSchemaAsserts</legacyBold>    </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Returns the assertions defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">(ASSERTIONS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">
                      <legacyBold>adSchemaCatalogs</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Returns the physical attributes associated with catalogs accessible from the DBMS.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">(CATALOGS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">CATALOG_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">
                      <legacyBold>adSchemaCharacterSets</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Returns the character sets defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">(CHARACTER_SETS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">CHARACTER_SET_CATALOG CHARACTER_SET_SCHEMA CHARACTER_SET_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">
                      <legacyBold>adSchemaCheckConstraints</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">5</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Returns the check constraints defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">(CHECK_CONSTRAINTS) Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">
                      <legacyBold>adSchemaCollations</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Returns the character collations defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">(COLLATIONS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">COLLATION_CATALOG COLLATION_SCHEMA COLLATION_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">
                      <legacyBold>adSchemaColumnPrivileges</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">13</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">(COLUMN_PRIVILEGES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME COLUMN_NAME GRANTOR GRANTEE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">
                      <legacyBold>adSchemaColumns</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">(COLUMNS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">
                      <legacyBold>adSchemaColumnsDomainUsage</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">11</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">(COLUMN_DOMAIN_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">DOMAIN_CATALOG DOMAIN_SCHEMA DOMAIN_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">
                      <legacyBold>adSchemaConstraintColumnUsage</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">6</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">(CONSTRAINT_COLUMN_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src60" class="srcSentence">adSchemaConstraintTableUsage</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">7</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">(CONSTRAINT_TABLE_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">
                      <legacyBold>adSchemaCubes</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">32</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">(CUBES Rowset*)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">
                      <legacyBold>adSchemaDBInfoKeywords</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">30</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Returns a list of provider-specific keywords.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">(IDBInfo::GetKeywords)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">&lt;None&gt;</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">
                      <legacyBold>adSchemaDBInfoLiterals</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">31</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">Returns a list of provider-specific literals used in text commands.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">(IDBInfo::GetLiteralInfo)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">&lt;None&gt;</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">
                      <legacyBold>adSchemaDimensions</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">33</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">Returns information about the dimensions in a given cube.</caps:sentence>
                    <caps:sentence id="src83" class="srcSentence"> It has one row for each dimension.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">(DIMENSIONS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_NAME DIMENSION_UNIQUE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">
                      <legacyBold>adSchemaForeignKeys</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">27</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">Returns the foreign key columns defined in the catalog by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">(FOREIGN_KEYS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">PK_TABLE_CATALOG PK_TABLE_SCHEMA PK_TABLE_NAME FK_TABLE_CATALOG FK_TABLE_SCHEMA FK_TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">
                      <legacyBold>adSchemaHierarchies</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">34</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">Returns information about the hierarchies available in a dimension.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">(HIERARCHIES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_UNIQUE_NAME HIERARCHY_NAME HIERARCHY_UNIQUE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">
                      <legacyBold>adSchemaIndexes</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src97" class="srcSentence">12</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">Returns the indexes defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">(INDEXES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA INDEX_NAME TYPE TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">
                      <legacyBold>adSchemaKeyColumnUsage</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">8</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src103" class="srcSentence">Returns the columns defined in the catalog that are constrained as keys by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">(KEY_COLUMN_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME TABLE_CATALOG TABLE_SCHEMA TABLE_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">
                      <legacyBold>adSchemaLevels</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">35</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">Returns information about the levels available in a dimension.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">(LEVELS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_UNIQUE_NAME HIERARCHY_UNIQUE_NAME LEVEL_NAME LEVEL_UNIQUE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">
                      <legacyBold>adSchemaMeasures</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">36</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">Returns information about the available measures.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">(MEASURES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME MEASURE_NAME MEASURE_UNIQUE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">
                      <legacyBold>adSchemaMembers</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">38</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">Returns information about the available members.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">(MEMBERS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_UNIQUE_NAME HIERARCHY_UNIQUE_NAME LEVEL_UNIQUE_NAME LEVEL_NUMBER MEMBER_NAME MEMBER_UNIQUE_NAME MEMBER_CAPTION MEMBER_TYPE Tree operator.</caps:sentence>
                    <caps:sentence id="src121" class="srcSentence"> For more information, see OLE DB for Online Analytical Processing (OLAP).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src122" class="srcSentence">
                      <legacyBold>adSchemaPrimaryKeys</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src123" class="srcSentence">28</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">Returns the primary key columns defined in the catalog by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">(PRIMARY_KEYS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">PK_TABLE_CATALOG PK_TABLE_SCHEMA PK_TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">
                      <legacyBold>adSchemaProcedureColumns</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">29</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">Returns information about the columns of rowsets returned by procedures.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">(PROCEDURE_COLUMNS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src131" class="srcSentence">PROCEDURE_CATALOG PROCEDURE_SCHEMA PROCEDURE_NAME COLUMN_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">
                      <legacyBold>adSchemaProcedureParameters</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">26</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">Returns information about the parameters and return codes of procedures.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">(PROCEDURE_PARAMETERS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">PROCEDURE_CATALOG PROCEDURE_SCHEMA PROCEDURE_NAME PARAMETER_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">
                      <legacyBold>adSchemaProcedures</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">16</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">Returns the procedures defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">(PROCEDURES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">PROCEDURE_CATALOG PROCEDURE_SCHEMA PROCEDURE_NAME PROCEDURE_TYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">
                      <legacyBold>adSchemaProperties</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">37</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">Returns information about the available properties for each level of the dimension.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">(PROPERTIES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">CATALOG_NAME SCHEMA_NAME CUBE_NAME DIMENSION_UNIQUE_NAME HIERARCHY_UNIQUE_NAME LEVEL_UNIQUE_NAME MEMBER_UNIQUE_NAME PROPERTY_TYPE PROPERTY_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">
                      <legacyBold>adSchemaProviderSpecific</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src148" class="srcSentence">-1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">Used if the provider defines its own nonstandard schema queries.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">&lt;Provider specific&gt;</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src151" class="srcSentence">adSchemaProviderTypes</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">22</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">Returns the (base) data types supported by the data provider.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">(PROVIDER_TYPES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src155" class="srcSentence">DATA_TYPE BEST_MATCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">
                      <legacyBold>AdSchemaReferentialConstraints</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">9</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">Returns the referential constraints defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">(REFERENTIAL_CONSTRAINTS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">
                      <legacyBold>adSchemaSchemata</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">17</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">Returns the schemas (database objects) that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">(SCHEMATA Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">CATALOG_NAME SCHEMA_NAME SCHEMA_OWNER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">
                      <legacyBold>adSchemaSQLLanguages</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">18</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">(SQL_LANGUAGES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">&lt;None&gt;</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">
                      <legacyBold>adSchemaStatistics</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">19</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">Returns the statistics defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">(STATISTICS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">
                      <legacyBold>adSchemaTableConstraints</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">10</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">Returns the table constraints defined in the catalog that are owned by a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">(TABLE_CONSTRAINTS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">CONSTRAINT_CATALOG CONSTRAINT_SCHEMA CONSTRAINT_NAME TABLE_CATALOG TABLE_SCHEMA TABLE_NAME CONSTRAINT_TYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">
                      <legacyBold>adSchemaTablePrivileges</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">14</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">(TABLE_PRIVILEGES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME GRANTOR GRANTEE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">
                      <legacyBold>adSchemaTables</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">20</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">Returns the tables (including views) defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">(TABLES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src190" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME TABLE_TYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">
                      <legacyBold>adSchemaTranslations</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">21</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src193" class="srcSentence">Returns the character translations defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">(TRANSLATIONS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">TRANSLATION_CATALOG TRANSLATION_SCHEMA TRANSLATION_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">
                      <legacyBold>adSchemaTrustees</legacyBold>    </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src197" class="srcSentence">39</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">Reserved for future use.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">
                      <legacyBold>adSchemaUsagePrivileges</legacyBold>   </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">15</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">(USAGE_PRIVILEGES Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">OBJECT_CATALOG OBJECT_SCHEMA OBJECT_NAME OBJECT_TYPE GRANTOR GRANTEE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">
                      <legacyBold>adSchemaViewColumnUsage</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">24</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src206" class="srcSentence">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">(VIEW_COLUMN_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src208" class="srcSentence">VIEW_CATALOG VIEW_SCHEMA VIEW_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">
                      <legacyBold>adSchemaViews</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src210" class="srcSentence">23</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src211" class="srcSentence">Returns the views defined in the catalog that are accessible to a given user.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">(VIEWS Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">TABLE_CATALOG TABLE_SCHEMA TABLE_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">
                      <legacyBold>adSchemaViewTableUsage</legacyBold>  </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src215" class="srcSentence">25</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src216" class="srcSentence">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src217" class="srcSentence">(VIEW_TABLE_USAGE Rowset)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src218" class="srcSentence">VIEW_CATALOG VIEW_SCHEMA VIEW_NAME</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src219" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src220" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src221" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src222" class="srcSentence">AdoEnums.Schema.ASSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src223" class="srcSentence">AdoEnums.Schema.CATALOGS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">AdoEnums.Schema.CHARACTERSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src225" class="srcSentence">AdoEnums.Schema.CHECKCONSTRAINTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src226" class="srcSentence">AdoEnums.Schema.COLLATIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src227" class="srcSentence">AdoEnums.Schema.COLUMNPRIVILEGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src228" class="srcSentence">AdoEnums.Schema.COLUMNS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src229" class="srcSentence">AdoEnums.Schema.COLUMNSDOMAINUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src230" class="srcSentence">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">AdoEnums.Schema.CUBES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src233" class="srcSentence">AdoEnums.Schema.DBINFOKEYWORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src234" class="srcSentence">AdoEnums.Schema.DBINFOLITERALS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src235" class="srcSentence">AdoEnums.Schema.DIMENSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src236" class="srcSentence">AdoEnums.Schema.FOREIGNKEYS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src237" class="srcSentence">AdoEnums.Schema.HIERARCHIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src238" class="srcSentence">AdoEnums.Schema.INDEXES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src239" class="srcSentence">AdoEnums.Schema.KEYCOLUMNUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src240" class="srcSentence">AdoEnums.Schema.LEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src241" class="srcSentence">AdoEnums.Schema.MEASURES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src242" class="srcSentence">AdoEnums.Schema.MEMBERS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src243" class="srcSentence">AdoEnums.Schema.PRIMARYKEYS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">AdoEnums.Schema.PROCEDURECOLUMNS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src245" class="srcSentence">AdoEnums.Schema.PROCEDUREPARAMETERS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">AdoEnums.Schema.PROCEDURES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">AdoEnums.Schema.PROPERTIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src248" class="srcSentence">AdoEnums.Schema.PROVIDERSPECIFIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">AdoEnums.Schema.PROVIDERTYPES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src250" class="srcSentence">AdoEnums.Schema.REFERENTIALCONTRAINTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src251" class="srcSentence">AdoEnums.Schema.SCHEMATA</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src252" class="srcSentence">AdoEnums.Schema.SQLLANGUAGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src253" class="srcSentence">AdoEnums.Schema.STATISTICS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src254" class="srcSentence">AdoEnums.Schema.TABLECONSTRAINTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src255" class="srcSentence">AdoEnums.Schema.TABLEPRIVILEGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src256" class="srcSentence">AdoEnums.Schema.TABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src257" class="srcSentence">AdoEnums.Schema.TRANSLATIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src258" class="srcSentence">AdoEnums.Schema.TRUSTEES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src259" class="srcSentence">AdoEnums.Schema.USAGEPRIVILEGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src260" class="srcSentence">AdoEnums.Schema.VIEWCOLUMNUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src261" class="srcSentence">AdoEnums.Schema.VIEWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src262" class="srcSentence">AdoEnums.Schema.VIEWTABLEUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src263" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Execute Method (ADO Connection)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 03c69320-96b2-4d85-8d49-a13b13e31578
caps.latest.revision: 12
caps.handback.revision: 12
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
# Execute Method (ADO Connection)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a98ac61157e1ba1b52017824b3b84379" id="tgt1" class="tgtSentence">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set recordset = connection.Execute (CommandText, RecordsAffected, Options)</legacyBold>
          <legacyBold>Set recordset = connection.Execute (CommandText, RecordsAffected, Options)</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="9d7d45dea9c30ad442b67716ae60ec50" id="tgt2" class="tgtSentence">Returns a <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link> object reference.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="ad16afd7aef42c7ceff619db8e3c6992" id="tgt3" class="tgtSentence"> <legacyItalic>CommandText</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="bb513d70192997e7f2db232db13a80bc" id="tgt4" class="tgtSentence">A <legacyBold>String</legacyBold> value that contains the SQL statement, stored procedure, a URL, or provider-specific text to execute.</caps:sentence>
                <caps:sentence sentenceid="3e9fb2f61239073d1d3611df70f33fc7" id="tgt5" class="tgtSentence">
                  <legacyBold>Optionally</legacyBold>, table names can be used but only if the provider is SQL aware.</caps:sentence>
                <caps:sentence sentenceid="f133af3e1d1bf4fb2c115b2dc7479ad4" id="tgt6" class="tgtSentence"> For example if a table name of "Customers" is used, ADO will automatically prepend the standard SQL Select syntax to form and pass "SELECT * FROM Customers" as a <token>tsql</token> statement to the provider.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="7818b1bda08fe42f7ac5dcd9cc7471dc" id="tgt7" class="tgtSentence"> <legacyItalic>RecordsAffected</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="ecc4f294aa113f2a687815946c341a51" id="tgt9" class="tgtSentence"> A <legacyBold>Long</legacyBold> variable to which the provider returns the number of records that the operation affected.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt10" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt11" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="43cd08054d5099666245d4a578999e39" id="tgt12" class="tgtSentence"> A <legacyBold>Long</legacyBold> value that indicates how the provider should evaluate the CommandText argument.</caps:sentence>
                <caps:sentence sentenceid="7acf9f80953451576618cf89b3f50af9" id="tgt13" class="tgtSentence"> Can be a bitmask of one or more <link xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</link> or <link xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</link> values.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <para>
            <caps:sentence sentenceid="faeb42ab21a1831d6a58acab8faef927" id="tgt14" class="tgtSentence">
              <embeddedLabel>Note</embeddedLabel>   Use the <legacyBold>ExecuteOptionEnum</legacyBold> value <legacyBold>adExecuteNoRecords</legacyBold> to improve performance by minimizing internal processing and for applications that you are porting from Visual Basic 6.0.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fea2002c6fc65f2143de26c995dca102" id="tgt15" class="tgtSentence">Do not use <legacyBold>adExecuteStream</legacyBold> with the <legacyBold>Execute</legacyBold> method of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a87bf58a8fccee25df93047186736601" id="tgt16" class="tgtSentence">Do not use the CommandTypeEnum values of adCmdFile or adCmdTableDirect with Execute.</caps:sentence>
            <caps:sentence sentenceid="1e30a20095000f66296fa9e78d5ad50c" id="tgt17" class="tgtSentence"> These values can only be used as options with the <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> and <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link> methods of a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="5a387d6221f6907eecc50de773bf0237" id="tgt18" class="tgtSentence">Using the <legacyBold>Execute</legacyBold> method on a <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object_ADO</link> object executes whatever query you pass to the method in the CommandText argument on the specified connection.</caps:sentence>
            <caps:sentence sentenceid="36ff2537d985a36ac457c61aec70e092" id="tgt19" class="tgtSentence"> If the CommandText argument specifies a row-returning query, any results that the execution generates are stored in a new <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="79b049b70b054bce4b60761e23866afd" id="tgt20" class="tgtSentence"> If the command is not intended to return results (for example, an SQL UPDATE query) the provider returns <legacyBold>Nothing</legacyBold> as long as the option <legacyBold>adExecuteNoRecords</legacyBold> is specified; otherwise Execute returns a closed <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d3842fbe23f610b1f592e6ed7db0a236" id="tgt21" class="tgtSentence">The returned <legacyBold>Recordset</legacyBold> object is always a read-only, forward-only cursor.</caps:sentence>
            <caps:sentence sentenceid="13de08ba2121fb95bc7fe2eb9c7ca1d8" id="tgt22" class="tgtSentence"> If you need a <legacyBold>Recordset</legacyBold> object with more functionality, first create a <legacyBold>Recordset</legacyBold> object with the desired property settings, then use the <legacyBold>Recordset</legacyBold> object's <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> method to execute the query and return the desired cursor type.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9186eacc267bb5777363f028db350e18" id="tgt23" class="tgtSentence">The contents of the <legacyItalic>CommandText</legacyItalic> argument are specific to the provider and can be standard SQL syntax or any special command format that the provider supports.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6dcecc210474cadcba02f7d7f512db41" id="tgt24" class="tgtSentence">An ExecuteComplete event will be issued when this operation concludes.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="f3f88d72bcbf9f19cb312ee3ef92c570" id="tgt25" class="tgtSentence">URLs using the http scheme will automatically invoke the <link xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</link>.</caps:sentence>
              <caps:sentence sentenceid="e83309b4084e8b984ee10bc9cd22b418" id="tgt26" class="tgtSentence"> For more information, see <link xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</link>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt27" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set recordset = connection.Execute (CommandText, RecordsAffected, Options)</legacyBold>
          <legacyBold>Set recordset = connection.Execute (CommandText, RecordsAffected, Options)</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link> object reference.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>CommandText</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A <legacyBold>String</legacyBold> value that contains the SQL statement, stored procedure, a URL, or provider-specific text to execute.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence">
                  <legacyBold>Optionally</legacyBold>, table names can be used but only if the provider is SQL aware.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> For example if a table name of "Customers" is used, ADO will automatically prepend the standard SQL Select syntax to form and pass "SELECT * FROM Customers" as a <token>tsql</token> statement to the provider.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>RecordsAffected</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> A <legacyBold>Long</legacyBold> variable to which the provider returns the number of records that the operation affected.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> A <legacyBold>Long</legacyBold> value that indicates how the provider should evaluate the CommandText argument.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> Can be a bitmask of one or more <link xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</link> or <link xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</link> values.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <para>
            <caps:sentence id="src14" class="srcSentence">
              <embeddedLabel>Note</embeddedLabel>   Use the <legacyBold>ExecuteOptionEnum</legacyBold> value <legacyBold>adExecuteNoRecords</legacyBold> to improve performance by minimizing internal processing and for applications that you are porting from Visual Basic 6.0.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">Do not use <legacyBold>adExecuteStream</legacyBold> with the <legacyBold>Execute</legacyBold> method of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">Do not use the CommandTypeEnum values of adCmdFile or adCmdTableDirect with Execute.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> These values can only be used as options with the <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> and <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link> methods of a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src18" class="srcSentence">Using the <legacyBold>Execute</legacyBold> method on a <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object_ADO</link> object executes whatever query you pass to the method in the CommandText argument on the specified connection.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> If the CommandText argument specifies a row-returning query, any results that the execution generates are stored in a new <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> If the command is not intended to return results (for example, an SQL UPDATE query) the provider returns <legacyBold>Nothing</legacyBold> as long as the option <legacyBold>adExecuteNoRecords</legacyBold> is specified; otherwise Execute returns a closed <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">The returned <legacyBold>Recordset</legacyBold> object is always a read-only, forward-only cursor.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> If you need a <legacyBold>Recordset</legacyBold> object with more functionality, first create a <legacyBold>Recordset</legacyBold> object with the desired property settings, then use the <legacyBold>Recordset</legacyBold> object's <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> method to execute the query and return the desired cursor type.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">The contents of the <legacyItalic>CommandText</legacyItalic> argument are specific to the provider and can be standard SQL syntax or any special command format that the provider supports.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">An ExecuteComplete event will be issued when this operation concludes.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src25" class="srcSentence">URLs using the http scheme will automatically invoke the <link xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</link>.</caps:sentence>
              <caps:sentence id="src26" class="srcSentence"> For more information, see <link xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</link>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
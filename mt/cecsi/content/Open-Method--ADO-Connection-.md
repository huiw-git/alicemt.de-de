---
title: "Open Method (ADO Connection)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 663defab-5545-4973-9036-24d5882c9737
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
# Open Method (ADO Connection)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="dbc01469e8610f34f53bb155be4d9319" id="tgt1" class="tgtSentence">Opens a connection to a data source.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>connection</parameterReference>
          <legacyBold>.Open</legacyBold>
          <parameterReference>ConnectionString</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>UserID</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Password, Options</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d78656013dfd2e3c848a339806ae4610" id="tgt2" class="tgtSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="e609ab3adef2510705d3ed8c24873074" id="tgt4" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains connection information.</caps:sentence>
                <caps:sentence sentenceid="82b1736649f56787f6d6f0c21ee19e46" id="tgt5" class="tgtSentence"> See the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property for details on valid settings.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5b457185e24aac84a61f0966d85535a8" id="tgt6" class="tgtSentence"> <legacyItalic>UserID</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt7" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="4e34e3e86a0a9157cd5c1540110f5263" id="tgt8" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains a user name to use when establishing the connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d83fe9057df78601fffb657095e0114f" id="tgt9" class="tgtSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt10" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="da730dfe245112f7c7f4909d1b2d761d" id="tgt11" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains a password to use when establishing the connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt12" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt13" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="bbec8cb033e669d3e318371729c0c91b" id="tgt14" class="tgtSentence"> A <legacyLink xlink:href="bff07eeb-dee3-4e4e-9b2d-d56061ea744d">ConnectOptionEnum</legacyLink> value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="82fef6cce55180bfe212bd7b668f64e9" id="tgt15" class="tgtSentence">Using the <legacyBold>Open</legacyBold> method on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object establishes the physical connection to a data source.</caps:sentence>
            <caps:sentence sentenceid="4b3368747f1dc1b7814d600e0bfc7bc7" id="tgt16" class="tgtSentence"> After this method successfully completes, the connection is live and you can issue commands against it and process the results.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9425f97b0bf80006bdacee8b4b2e7dd3" id="tgt17" class="tgtSentence">Use the optional <legacyItalic>ConnectionString</legacyItalic> argument to specify either a connection string containing a series of <legacyItalic>argument</legacyItalic> <legacyItalic>= value</legacyItalic> statements separated by semicolons, or a file or directory resource identified with a URL.</caps:sentence>
            <caps:sentence sentenceid="fc6c8c6a741c06792e595f557d909ffd" id="tgt18" class="tgtSentence"> The <legacyBold>ConnectionString</legacyBold> property automatically inherits the value used for the <legacyItalic>ConnectionString</legacyItalic> argument.</caps:sentence>
            <caps:sentence sentenceid="a58c429922c42fb417a18d12e6c1e475" id="tgt19" class="tgtSentence"> Therefore, you can either set the <legacyBold>ConnectionString</legacyBold> property of the <legacyBold>Connection</legacyBold> object before opening it, or use the <legacyItalic>ConnectionString</legacyItalic> argument to set or override the current connection parameters during the <legacyBold>Open</legacyBold> method call.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e73efa1f6cfc6cf1cab34092a1d05bb6" id="tgt20" class="tgtSentence">If you pass user and password information both in the <legacyItalic>ConnectionString</legacyItalic> argument and in the optional <legacyItalic>UserID</legacyItalic> and <legacyItalic>Password</legacyItalic> arguments, the <legacyItalic>UserID</legacyItalic> and <legacyItalic>Password</legacyItalic> arguments will override the values specified in <legacyItalic>ConnectionString</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d64c3bd314f2bf8a08e1505cc0182c6a" id="tgt21" class="tgtSentence">When you have concluded your operations over an open <legacyBold>Connection</legacyBold>, use the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method to free any associated system resources.</caps:sentence>
            <caps:sentence sentenceid="8b2817eca9b660ab3f7f255253d5d7b0" id="tgt22" class="tgtSentence"> Closing an object does not remove it from memory; you can change its property settings and use the <legacyBold>Open</legacyBold> method to open it again later.</caps:sentence>
            <caps:sentence sentenceid="16320cdfb1b7a9ef595f587a121331f6" id="tgt23" class="tgtSentence"> To completely eliminate an object from memory, set the object variable to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="72bb71f331f822eb0487eed727da5dd4" id="tgt24" class="tgtSentence">
                <legacyBold> Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Connection</legacyBold> object, the <legacyBold>Open</legacyBold> method doesn't actually establish a connection to the server until a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is opened on the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt25" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt26" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
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
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1311d561-0e86-40f5-8cbc-ad8f13e626d1">Visual Basic Example</link>
        <link xlink:href="66eca011-e258-4d8f-bd67-e017bcf0871b">VBScript Example</link>
        <link xlink:href="f74a81fd-cbcc-4143-b9f8-774c88dd4fad">Visual C++ Example</link>
        <link xlink:href="0b7dd9f8-4751-48fb-a75d-c6f75d80d928">Visual J++ Example</link>
        <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Opens a connection to a data source.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>connection</parameterReference>
          <legacyBold>.Open</legacyBold>
          <parameterReference>ConnectionString</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>UserID</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Password, Options</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains connection information.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> See the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property for details on valid settings.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>UserID</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains a user name to use when establishing the connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains a password to use when establishing the connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> A <legacyLink xlink:href="bff07eeb-dee3-4e4e-9b2d-d56061ea744d">ConnectOptionEnum</legacyLink> value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">Using the <legacyBold>Open</legacyBold> method on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object establishes the physical connection to a data source.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> After this method successfully completes, the connection is live and you can issue commands against it and process the results.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">Use the optional <legacyItalic>ConnectionString</legacyItalic> argument to specify either a connection string containing a series of <legacyItalic>argument</legacyItalic> <legacyItalic>= value</legacyItalic> statements separated by semicolons, or a file or directory resource identified with a URL.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> The <legacyBold>ConnectionString</legacyBold> property automatically inherits the value used for the <legacyItalic>ConnectionString</legacyItalic> argument.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> Therefore, you can either set the <legacyBold>ConnectionString</legacyBold> property of the <legacyBold>Connection</legacyBold> object before opening it, or use the <legacyItalic>ConnectionString</legacyItalic> argument to set or override the current connection parameters during the <legacyBold>Open</legacyBold> method call.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">If you pass user and password information both in the <legacyItalic>ConnectionString</legacyItalic> argument and in the optional <legacyItalic>UserID</legacyItalic> and <legacyItalic>Password</legacyItalic> arguments, the <legacyItalic>UserID</legacyItalic> and <legacyItalic>Password</legacyItalic> arguments will override the values specified in <legacyItalic>ConnectionString</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">When you have concluded your operations over an open <legacyBold>Connection</legacyBold>, use the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method to free any associated system resources.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Closing an object does not remove it from memory; you can change its property settings and use the <legacyBold>Open</legacyBold> method to open it again later.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> To completely eliminate an object from memory, set the object variable to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src24" class="srcSentence">
                <legacyBold> Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Connection</legacyBold> object, the <legacyBold>Open</legacyBold> method doesn't actually establish a connection to the server until a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is opened on the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src25" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src26" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
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
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1311d561-0e86-40f5-8cbc-ad8f13e626d1">Visual Basic Example</link>
        <link xlink:href="66eca011-e258-4d8f-bd67-e017bcf0871b">VBScript Example</link>
        <link xlink:href="f74a81fd-cbcc-4143-b9f8-774c88dd4fad">Visual C++ Example</link>
        <link xlink:href="0b7dd9f8-4751-48fb-a75d-c6f75d80d928">Visual J++ Example</link>
        <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
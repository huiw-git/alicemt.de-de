---
title: "ADO Objects and Collections"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7a745aae-9372-49b6-8dae-b9c93e5f3216
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
# ADO Objects and Collections
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="67b2d52061f7a51227c053f6c3391c33" id="tgt1" class="tgtSentence">ADO consists of the following nine objects and four collections.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c496bbc3481207a663fc513bc12f87fd" id="tgt2" class="tgtSentence">Object or Collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt3" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="51318171a8fbcf5d407e1c7b239f32d4" id="tgt4" class="tgtSentence">               <legacyBold>Connection</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1873fef004e2667f571f80196fb36a2d" id="tgt5" class="tgtSentence">Represents a unique session with a data source.</caps:sentence>
                  <caps:sentence sentenceid="64357d8f6ff931f30b4f56186d2584cb" id="tgt6" class="tgtSentence"> In the case of a client/server database system, it may be equivalent to an actual network connection to the server.</caps:sentence>
                  <caps:sentence sentenceid="8b1f37db8421e94019898cbf52bd64ae" id="tgt7" class="tgtSentence"> Depending on the functionality supported by the provider, some collections, methods, or properties of a <legacyBold>Connection</legacyBold> object may not be available.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0e1d19e1e63ef0bc2109d8592fdac95d" id="tgt8" class="tgtSentence">               <legacyBold>Command</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="54bc96ae782c2ef5117080376950b82f" id="tgt9" class="tgtSentence">Used to define a specific command, such as a SQL query, intended to run against a data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="955dc464633518a45c7a3b2118bb703c" id="tgt10" class="tgtSentence">               <legacyBold>Recordset</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c8539f3ead60efbc64bb1fe5e92cf1e8" id="tgt11" class="tgtSentence">Represents the entire set of records from a base table or the results of an executed command.</caps:sentence>
                  <caps:sentence sentenceid="d6466e3858ae41d65ba9dea975bdc2c1" id="tgt12" class="tgtSentence"> All <legacyBold>Recordset</legacyBold> objects consist of records (rows) and fields (columns).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="375fccbb36dcb8478740877384f44551" id="tgt13" class="tgtSentence">               <legacyBold>Record</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="71e1a94325742cde3aca4302d04f2b4a" id="tgt14" class="tgtSentence">Represents a single row of data, either from a <legacyBold>Recordset</legacyBold> or from the provider.</caps:sentence>
                  <caps:sentence sentenceid="6ad7eacf2ba87b6b5fc6596cc6947098" id="tgt15" class="tgtSentence"> This record could represent a database record or some other type of object such as a file or directory, depending upon your provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="bed4dbd74925cbb2642eb3843e01b487" id="tgt16" class="tgtSentence">               <legacyBold>Stream</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="da306238124ff342f77435555dfd3b5c" id="tgt17" class="tgtSentence">Represents a stream of binary or text data.</caps:sentence>
                  <caps:sentence sentenceid="4b6ed6e9cce0ad068ad8da5c40743637" id="tgt18" class="tgtSentence"> For example, an XML document can be loaded into a stream for command input or returned from certain providers as the results of a query.</caps:sentence>
                  <caps:sentence sentenceid="e6d94527352eff2e6be01860163f1360" id="tgt19" class="tgtSentence"> A <legacyBold>Stream</legacyBold> object can be used to manipulate fields or records containing these streams of data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4a611c284877f966871969fb86394ca6" id="tgt20" class="tgtSentence">               <legacyBold>Parameter</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f70c777369b1cc168e11fa16437fcacb" id="tgt21" class="tgtSentence">Represents a parameter or argument associated with a <legacyBold>Command</legacyBold> object, based on a parameterized query or stored procedure.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b1d3ca6bd01de01d6942442a287c827a" id="tgt22" class="tgtSentence">               <legacyBold>Field</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d1cda4d581ef6976217bd90991d964f8" id="tgt23" class="tgtSentence">Represents a column of data with a common data type.</caps:sentence>
                  <caps:sentence sentenceid="36b4e0a1649153562210d038a5ac8329" id="tgt24" class="tgtSentence"> Each <legacyBold>Field</legacyBold> object corresponds to a column in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8b57957a948c2a24011a03e4106b7411" id="tgt25" class="tgtSentence">               <legacyBold>Property</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6521cf765ed6ad32e5d8d733cfddea17" id="tgt26" class="tgtSentence">Represents a characteristic of an ADO object that is defined by the provider.</caps:sentence>
                  <caps:sentence sentenceid="ea2195cc86a72a9eb0d9705cad8964ba" id="tgt27" class="tgtSentence"> ADO objects have two types of properties: built-in and dynamic.</caps:sentence>
                  <caps:sentence sentenceid="fb23454d5e0444d4fb900a637a8d63b1" id="tgt28" class="tgtSentence"> Built-in properties are those properties implemented in ADO and immediately available to any new object.</caps:sentence>
                  <caps:sentence sentenceid="88a287018736bd37dae19998ef954fdb" id="tgt29" class="tgtSentence"> The <legacyBold>Property</legacyBold> object is a container for dynamic properties, defined by the underlying provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="5f9d96c30c79777bc5e04a3700b07108" id="tgt30" class="tgtSentence">               <legacyBold>Error</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f5fafb6469e9e044910d3d57714f0bde" id="tgt31" class="tgtSentence">Contains details about data access errors that pertain to a single operation involving the provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3a3d3c3b146a2ef5c8338dd43a8e77cf" id="tgt32" class="tgtSentence">               <legacyBold>Fields</legacyBold> collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="722c8bd43f0eb76de22350de766504fb" id="tgt33" class="tgtSentence">Contains all the <legacyBold>Field</legacyBold> objects of a <legacyBold>Recordset</legacyBold> or <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4f20036938d6bbff92f6d52d479f2240" id="tgt34" class="tgtSentence">               <legacyBold>Properties</legacyBold> collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d74164d01b6e9a22d928a7738fd13b1a" id="tgt35" class="tgtSentence">Contains all the <legacyBold>Property</legacyBold> objects for a specific instance of an object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="209084ae2bf52cad68b93e0c8d001b8d" id="tgt36" class="tgtSentence">               <legacyBold>Parameters</legacyBold> collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e30f3cce52a1950d5a741e2555f19e75" id="tgt37" class="tgtSentence">Contains all the <legacyBold>Parameter</legacyBold> objects of a <legacyBold>Command</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f41c10488183648dc0f1c3ada1be6f48" id="tgt38" class="tgtSentence">               <legacyBold>Errors</legacyBold> collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="76801cd1b4e6dd1034fe8db6f40bf266" id="tgt39" class="tgtSentence">Contains all the <legacyBold>Error</legacyBold> objects created in response to a single provider-related failure.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO consists of the following nine objects and four collections.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Object or Collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">               <legacyBold>Connection</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Represents a unique session with a data source.</caps:sentence>
                  <caps:sentence id="src6" class="srcSentence"> In the case of a client/server database system, it may be equivalent to an actual network connection to the server.</caps:sentence>
                  <caps:sentence id="src7" class="srcSentence"> Depending on the functionality supported by the provider, some collections, methods, or properties of a <legacyBold>Connection</legacyBold> object may not be available.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">               <legacyBold>Command</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Used to define a specific command, such as a SQL query, intended to run against a data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">               <legacyBold>Recordset</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Represents the entire set of records from a base table or the results of an executed command.</caps:sentence>
                  <caps:sentence id="src12" class="srcSentence"> All <legacyBold>Recordset</legacyBold> objects consist of records (rows) and fields (columns).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">               <legacyBold>Record</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Represents a single row of data, either from a <legacyBold>Recordset</legacyBold> or from the provider.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> This record could represent a database record or some other type of object such as a file or directory, depending upon your provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">               <legacyBold>Stream</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Represents a stream of binary or text data.</caps:sentence>
                  <caps:sentence id="src18" class="srcSentence"> For example, an XML document can be loaded into a stream for command input or returned from certain providers as the results of a query.</caps:sentence>
                  <caps:sentence id="src19" class="srcSentence"> A <legacyBold>Stream</legacyBold> object can be used to manipulate fields or records containing these streams of data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">               <legacyBold>Parameter</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Represents a parameter or argument associated with a <legacyBold>Command</legacyBold> object, based on a parameterized query or stored procedure.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">               <legacyBold>Field</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Represents a column of data with a common data type.</caps:sentence>
                  <caps:sentence id="src24" class="srcSentence"> Each <legacyBold>Field</legacyBold> object corresponds to a column in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">               <legacyBold>Property</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">Represents a characteristic of an ADO object that is defined by the provider.</caps:sentence>
                  <caps:sentence id="src27" class="srcSentence"> ADO objects have two types of properties: built-in and dynamic.</caps:sentence>
                  <caps:sentence id="src28" class="srcSentence"> Built-in properties are those properties implemented in ADO and immediately available to any new object.</caps:sentence>
                  <caps:sentence id="src29" class="srcSentence"> The <legacyBold>Property</legacyBold> object is a container for dynamic properties, defined by the underlying provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">               <legacyBold>Error</legacyBold> object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Contains details about data access errors that pertain to a single operation involving the provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">               <legacyBold>Fields</legacyBold> collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Contains all the <legacyBold>Field</legacyBold> objects of a <legacyBold>Recordset</legacyBold> or <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">               <legacyBold>Properties</legacyBold> collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">Contains all the <legacyBold>Property</legacyBold> objects for a specific instance of an object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">               <legacyBold>Parameters</legacyBold> collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Contains all the <legacyBold>Parameter</legacyBold> objects of a <legacyBold>Command</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">               <legacyBold>Errors</legacyBold> collection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">Contains all the <legacyBold>Error</legacyBold> objects created in response to a single provider-related failure.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
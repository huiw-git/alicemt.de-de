---
title: "Microsoft Data Shaping Service for OLE DB (ADO Service Provider)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 523009ce-e01b-4e2d-a7df-816d7688aff0
caps.latest.revision: 16
caps.handback.revision: 16
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
# Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="c11dccd1d3ac27d629272c19f9c6d3c0" id="tgt1" class="tgtSentence">This feature will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt2" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="16ae3d6fb80b787e37060343dad775f3" id="tgt3" class="tgtSentence"> Instead, applications should use XML.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="a765ec3f0e3fb6c61e801f636b92d315" id="tgt4" class="tgtSentence">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects from a data provider.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="0975fcf10aa159131d858087aa78f2ce" id="tgt5" class="tgtSentence">Provider Keyword</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a5de351870fd6a34a0194e81b9437bfb" id="tgt6" class="tgtSentence">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</caps:sentence>
          </para>
          <code>"Provider=<codeFeaturedElement xmlns="">MSDataShape</codeFeaturedElement>"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c9cc4b2425ec47fd6141efc88965a1d3" id="tgt7" class="tgtSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9b4020f0fca7a98d4f20089b56390d51" id="tgt8" class="tgtSentence">When this service provider is invoked, the following dynamic properties are added to the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of the<legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d"> Connection</legacyLink> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcebf220c946d5172f9d79c5c958f905" id="tgt9" class="tgtSentence">Dynamic Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt10" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1354715e5825ca5e3cd1d051f1b1eee1" id="tgt11" class="tgtSentence">
                      <legacyBold>Unique Reshape Names</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9d1591a4cc6743494dedeab10186ec42" id="tgt12" class="tgtSentence">Indicates whether <legacyBold>Recordset </legacyBold>objects with duplicate values for their <legacyBold>Reshape Name</legacyBold> properties are allowed.</caps:sentence>
                    <caps:sentence sentenceid="99f1429535dcfbd16d78f55322153be0" id="tgt13" class="tgtSentence"> If this dynamic property is <legacyBold>True</legacyBold> and a new <legacyBold>Recordset</legacyBold> is created with the same user-specified reshape name as an existing <legacyBold>Recordset</legacyBold>, then the new <legacyBold>Recordset</legacyBold> object's reshape name is modified to make it unique.</caps:sentence>
                    <caps:sentence sentenceid="2b352bbabd9f9eef56875464639d962a" id="tgt14" class="tgtSentence"> If this property is <languageKeyword>False</languageKeyword> and a new <legacyBold>Recordset</legacyBold> is created with the same user-specified reshape name as the existing <legacyBold>Recordset</legacyBold>, both <legacyBold>Recordset</legacyBold> objects will have the same reshape name.</caps:sentence>
                    <caps:sentence sentenceid="fe4637b4583468038d1bf6a37156a1e9" id="tgt15" class="tgtSentence"> Therefore, neither <legacyBold>Recordset</legacyBold> can be reshaped as long as both recordsets exist.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="7fcc9970c342dc36d0641b7bfd995425" id="tgt16" class="tgtSentence">The default value of the property is <legacyBold>False</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="4554a68f24dcbb0859b10f28517ef45f" id="tgt17" class="tgtSentence">Data Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03c34cbc5e7af7997faa8b52a2bf4105" id="tgt18" class="tgtSentence">Indicates the name of the provider that will supply rows to be shaped.</caps:sentence>
                    <caps:sentence sentenceid="8b8f4ffcb64a05e56fb8bc8ec07a6afd" id="tgt19" class="tgtSentence"> This value can be NONE if a provider will not be used to supply rows.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="8bd791fbfc05cb3c118eb9bb517c1898" id="tgt20" class="tgtSentence">You can also set writable dynamic properties by specifying their names as keywords in the connection string.</caps:sentence>
            <caps:sentence sentenceid="e408085adb3d449b63e6c78311ee918f" id="tgt21" class="tgtSentence"> For example, in Microsoft Visual Basic, set the <legacyBold>Data Provider</legacyBold> dynamic property to "MSDASQL" by specifying:</caps:sentence>
          </para>
          <code>Dim cn as New ADODB.Connection
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL"</code>
          <para>
            <caps:sentence sentenceid="caeed3ef67fafbd7200a0e3d6f555846" id="tgt22" class="tgtSentence">You can also set or retrieve a dynamic property by specifying its name as the index to the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> property.</caps:sentence>
            <caps:sentence sentenceid="ccf1590c6a030ee25ffb01578cb0f793" id="tgt23" class="tgtSentence"> For example, the following code example gets and prints the current value of the <legacyBold>Data Provider</legacyBold> dynamic property, then sets a new value if cn.DataProvider has been set to "MSDataShape" (either directly or indirectly through the connection string) and the connection has not been opened:</caps:sentence>
          </para>
          <code>Debug.Print cn.Properties("Data Provider")
cn.Properties("Data Provider") = "MSDASQL"</code>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="7f824eca461a1cd6187935e534044176" id="tgt24" class="tgtSentence">The dynamic property, <unmanagedCodeEntityReference>Data Provider</unmanagedCodeEntityReference>, can be set only on an unopened <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
              <caps:sentence sentenceid="ed3e6f612e19d34ca8d232477c9f92fa" id="tgt25" class="tgtSentence"> Once the connection is opened, the <unmanagedCodeEntityReference>Data Provider</unmanagedCodeEntityReference> property becomes read-only.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="f430b75048eb04a9a1f1477fb6486289" id="tgt26" class="tgtSentence">For more information about data shaping, see <legacyLink xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">Data Shaping</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">This feature will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Instead, applications should use XML.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src4" class="srcSentence">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects from a data provider.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Provider Keyword</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</caps:sentence>
          </para>
          <code>"Provider=<codeFeaturedElement xmlns="">MSDataShape</codeFeaturedElement>"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">When this service provider is invoked, the following dynamic properties are added to the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of the<legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d"> Connection</legacyLink> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Dynamic Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">
                      <legacyBold>Unique Reshape Names</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Indicates whether <legacyBold>Recordset </legacyBold>objects with duplicate values for their <legacyBold>Reshape Name</legacyBold> properties are allowed.</caps:sentence>
                    <caps:sentence id="src13" class="srcSentence"> If this dynamic property is <legacyBold>True</legacyBold> and a new <legacyBold>Recordset</legacyBold> is created with the same user-specified reshape name as an existing <legacyBold>Recordset</legacyBold>, then the new <legacyBold>Recordset</legacyBold> object's reshape name is modified to make it unique.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> If this property is <languageKeyword>False</languageKeyword> and a new <legacyBold>Recordset</legacyBold> is created with the same user-specified reshape name as the existing <legacyBold>Recordset</legacyBold>, both <legacyBold>Recordset</legacyBold> objects will have the same reshape name.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> Therefore, neither <legacyBold>Recordset</legacyBold> can be reshaped as long as both recordsets exist.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">The default value of the property is <legacyBold>False</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src17" class="srcSentence">Data Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Indicates the name of the provider that will supply rows to be shaped.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> This value can be NONE if a provider will not be used to supply rows.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src20" class="srcSentence">You can also set writable dynamic properties by specifying their names as keywords in the connection string.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> For example, in Microsoft Visual Basic, set the <legacyBold>Data Provider</legacyBold> dynamic property to "MSDASQL" by specifying:</caps:sentence>
          </para>
          <code>Dim cn as New ADODB.Connection
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL"</code>
          <para>
            <caps:sentence id="src22" class="srcSentence">You can also set or retrieve a dynamic property by specifying its name as the index to the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> property.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> For example, the following code example gets and prints the current value of the <legacyBold>Data Provider</legacyBold> dynamic property, then sets a new value if cn.DataProvider has been set to "MSDataShape" (either directly or indirectly through the connection string) and the connection has not been opened:</caps:sentence>
          </para>
          <code>Debug.Print cn.Properties("Data Provider")
cn.Properties("Data Provider") = "MSDASQL"</code>
          <alert class="note">
            <para>
              <caps:sentence id="src24" class="srcSentence">The dynamic property, <unmanagedCodeEntityReference>Data Provider</unmanagedCodeEntityReference>, can be set only on an unopened <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
              <caps:sentence id="src25" class="srcSentence"> Once the connection is opened, the <unmanagedCodeEntityReference>Data Provider</unmanagedCodeEntityReference> property becomes read-only.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src26" class="srcSentence">For more information about data shaping, see <legacyLink xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">Data Shaping</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
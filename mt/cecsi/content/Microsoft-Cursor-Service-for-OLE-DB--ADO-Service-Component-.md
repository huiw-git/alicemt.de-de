---
title: "Microsoft Cursor Service for OLE DB (ADO Service Component)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 420d0989-7cfb-4c66-a7b5-f4199d13165d
caps.latest.revision: 15
caps.handback.revision: 15
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
# Microsoft Cursor Service for OLE DB (ADO Service Component)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6b0e1792af25b26f79d13fa64f1e490a" id="tgt1" class="tgtSentence">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers.</caps:sentence>
          <caps:sentence sentenceid="30844917f46be14f2582cf876650e389" id="tgt2" class="tgtSentence"> As a result, the user perceives relatively uniform functionality from all data providers.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="690c81a4fb2ae8d6095d2edbd0a8bbfb" id="tgt3" class="tgtSentence">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods.</caps:sentence>
          <caps:sentence sentenceid="5ae9e4cadbdb4a4a6812311ba1c6ac47" id="tgt4" class="tgtSentence"> For example, the <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find</legacyLink> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="dc07c463e9d3bf2990402a4ff15c9a54" id="tgt5" class="tgtSentence">The Cursor Service enables support for batch updating in all cases.</caps:sentence>
          <caps:sentence sentenceid="71b34842bd0a14fd1d55e63fe0edc98a" id="tgt6" class="tgtSentence"> It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="d7df5b64df1181ef1d62d646a13aa860" id="tgt7" class="tgtSentence">Keyword</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5e89b665e4197af6be13a7a5b93a33f7" id="tgt8" class="tgtSentence">To invoke this service component, set the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> or <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object's <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
          <code>connection.CursorLocation=adUseClient
recordset.CursorLocation=adUseClient</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c9cc4b2425ec47fd6141efc88965a1d3" id="tgt9" class="tgtSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7666395ca5aa2f67866635d874e5e51e" id="tgt10" class="tgtSentence">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the <legacyBold>Recordset </legacyBold>object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
            <caps:sentence sentenceid="904432f98e5446b7d1acfbd689539fab" id="tgt11" class="tgtSentence"> The full list of <legacyBold>Connection</legacyBold> and <legacyBold>Recordset</legacyBold> object dynamic properties is listed in the <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">ADO Dynamic Property Index</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="e015809438bb5173f8596b22c0a6f652" id="tgt12" class="tgtSentence"> The associated OLE DB property names, where appropriate, are included in parentheses after the ADO property name.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f948eaea5aaaf626a1fbcde4ec3e3f2d" id="tgt13" class="tgtSentence">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked.</caps:sentence>
            <caps:sentence sentenceid="cd040a7f0e75d0bb76e7e6bdaee644f7" id="tgt14" class="tgtSentence"> For example, setting the <legacyItalic>Command Time out</legacyItalic> property on a <legacyBold>Recordset</legacyBold> will not be visible to the underlying data provider.</caps:sentence>
          </para>
          <code>
Recordset1.CursorLocation = adUseClient     'invokes cursor service
Recordset1.Open "authors", _
    "Provider=SQLOLEDB;Data Source=DBServer;User Id=MyUserID;" &amp; _
    "Password=MyPassword;Initial Catalog=pubs;",,adCmdTable
Recordset1.Properties.Item("Command Time out") = 50
' 'Command Time out' property on DBServer is still default (30).
</code>
          <para>
            <caps:sentence sentenceid="a55b2f62d84b1f8a6719120a9b6adb07" id="tgt15" class="tgtSentence">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service.</caps:sentence>
            <caps:sentence sentenceid="8e25e1c404d9d28e07dba9d4ed868d8a" id="tgt16" class="tgtSentence"> Command object property settings are always passed to the underlying data provider regardless of cursor location.</caps:sentence>
            <caps:sentence sentenceid="d7d7ff6fb83202c47109bfac144a0f3a" id="tgt17" class="tgtSentence"> Therefore, you can also use a command object to set the properties at any time.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="101d7b2161bf01b0edfd0b3b203f5224" id="tgt18" class="tgtSentence">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</caps:sentence>
            </para>
          </alert>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a3d69a40cc5ec31232a11100ae6c951" id="tgt19" class="tgtSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt20" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fb11517d1bae3775861a4e4e4100bc78" id="tgt21" class="tgtSentence">Auto Recalc (DBPROP_ADC_AUTORECALC)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0962c1243a161204c300f5ab9e7c4c5a" id="tgt22" class="tgtSentence">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated.</caps:sentence>
                    <caps:sentence sentenceid="15f4993a5f11407bc72cffef90f2f84a" id="tgt23" class="tgtSentence"> The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed.</caps:sentence>
                    <caps:sentence sentenceid="ec264ef8a7d02923fd2e70e8798bcad4" id="tgt24" class="tgtSentence"> If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a68eaae7547802259ca82c19b94207d8" id="tgt25" class="tgtSentence">Batch Size (DBPROP_ADC_BATCHSIZE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b0cb1aeb68134baa6784ecff084c4e0b" id="tgt26" class="tgtSentence">Indicates the number of update statements that can be batched before being sent to the data store.</caps:sentence>
                    <caps:sentence sentenceid="529b9710640fcc2bdb75a1cd779df0be" id="tgt27" class="tgtSentence"> The more statements in a batch, the fewer round trips to the data store.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ef5c0a351d739750e7fd09f61574cc40" id="tgt28" class="tgtSentence">Cache Child Rows (DBPROP_ADC_CACHECHILDROWS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ccad586cf3025fb4a31285d10b47605" id="tgt29" class="tgtSentence">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe960ca50c2c8fb3dc9164670519a087" id="tgt30" class="tgtSentence">Cursor Engine Version (DBPROP_ADC_CEVER)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="137a8c97b5a62d3de90ead17bb68fe59" id="tgt31" class="tgtSentence">Indicates the version of the Cursor Service being used.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="830bcf7ba0db2c5d896249a2efdf4a7d" id="tgt32" class="tgtSentence">Maintain Change Status (DBPROP_ADC_MAINTAINCHANGESTATUS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39be7f6c2a7767090dd5d36881d0ab3f" id="tgt33" class="tgtSentence">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">
                      <caps:sentence sentenceid="c14f7a753888287112058264fa40b72d" id="tgt34" class="tgtSentence">Optimize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5d26c75b8c224144fa15dda8b61a7750" id="tgt35" class="tgtSentence">Indicates whether an index should be created.</caps:sentence>
                    <caps:sentence sentenceid="83d26e6c419894ded7396aa57b29a9bf" id="tgt36" class="tgtSentence"> When set to <legacyBold>True</legacyBold>, authorizes the temporary creation of indexes to improve the execution of certain operations.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="690229d1-46cc-42e6-a57d-4438251fe248">
                      <caps:sentence sentenceid="32db6247d3f003bc7a5d97b7b4165920" id="tgt37" class="tgtSentence">Reshape Name</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8b9865464fbca5886f229aa28052794" id="tgt38" class="tgtSentence">Indicates the name of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="8b5d45711fea80a3ffbc0bb81e58a9bd" id="tgt39" class="tgtSentence"> Can be referenced within the current, or subsequent, data shaping commands.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="4e2bb601-0fe8-4d61-b00e-38341d85a6bb">
                      <caps:sentence sentenceid="0dd7af9563cc090b0f27867527af0395" id="tgt40" class="tgtSentence">Resync Command</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d0eee17688451e14c7e97d0aa6ccc7f9" id="tgt41" class="tgtSentence">Indicates a custom command string that is used by the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method when the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> property is in effect.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">
                      <caps:sentence sentenceid="f5c39b758518eb085ca020b4de55ce76" id="tgt42" class="tgtSentence">Unique Catalog</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="926426a17ab9fac4fad95bfb79897277" id="tgt43" class="tgtSentence">Indicates the name of the database containing the table referenced in the <legacyBold>Unique Table</legacyBold> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">
                      <caps:sentence sentenceid="ccfa118b2e3c050a4247f4faa7dfbc4d" id="tgt44" class="tgtSentence">Unique Schema</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe1bfff99ba55aae71b3205c9de9e006" id="tgt45" class="tgtSentence">Indicates the name of the owner of the table referenced in the <legacyBold>Unique Table</legacyBold> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">
                      <caps:sentence sentenceid="78d4188fdc2991f037b3e3902e9e6e72" id="tgt46" class="tgtSentence">Unique Table</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9eeb59cab62d54e68e02e909c3b248f" id="tgt47" class="tgtSentence">Indicates the name of the one table in a <legacyBold>Recordset</legacyBold> created from multiple tables that can be modified by insertions, updates, or deletions.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="007b61b596d8f180daecbd7d35398ada" id="tgt48" class="tgtSentence">Update Criteria (DBPROP_ADC_UPDATECRITERIA)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c09c5b5fa7787ff682e916922d349207" id="tgt49" class="tgtSentence">Indicates which fields in the <legacyBold>WHERE</legacyBold> clause are used to handle collisions occurring during an update.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ddaadcc406ddfe556bca037ee71ce06e" id="tgt50" class="tgtSentence">
                      <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink>               <legacyUnderline>               </legacyUnderline>(DBPROP_ADC_UPDATERESYNC)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdf714cd7c4b30ecf2d2ad1c6b75791" id="tgt51" class="tgtSentence">Indicates whether the <legacyBold>Resync</legacyBold> method is implicitly invoked after the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method (and its behavior), when the <legacyBold>Unique Table</legacyBold> property is in effect.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="8227914accdc4a314a5ebe8cd6a8e93b" id="tgt52" class="tgtSentence">You can also set or retrieve a dynamic property by specifying its name as the index to the <legacyBold>Properties</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="3d272db45fe38c6d04875ef3b1da541b" id="tgt53" class="tgtSentence"> For example, get and print the current value of the <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> dynamic property, then set a new value, as follows:</caps:sentence>
          </para>
          <code>Debug.Print rs.Properties("Optimize")
rs.Properties("Optimize") = True</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="fecd210c4e243340b7e30faa373e6267" id="tgt54" class="tgtSentence">Built-in Property Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5e2ff40274e67adcf8e5d8a9782cc95c" id="tgt55" class="tgtSentence">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a3d69a40cc5ec31232a11100ae6c951" id="tgt56" class="tgtSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt57" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4640abb0bdf777d31dffe3bb1d525931" id="tgt58" class="tgtSentence">
                      <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="345cf68a7f2fc15f1ea5c2d4eb47b6ef" id="tgt59" class="tgtSentence">Supplements the types of cursors that are available for a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44cccc0523541cd1a8530071be8b5bbb" id="tgt60" class="tgtSentence">
                      <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ca3de28690d1f1a8b2cb351972b8b7bf" id="tgt61" class="tgtSentence">Supplements the types of locks available for a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="cbc406cf26236f7e6ac1164fba01f484" id="tgt62" class="tgtSentence"> Enables batch updates.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3683ffa0-6f93-4906-9533-ef6942f24f39">
                      <caps:sentence sentenceid="cadc8c8db42409733582cb3e2298ef87" id="tgt63" class="tgtSentence">Sort</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b813bf8ca9df7d709a7057c930f86472" id="tgt64" class="tgtSentence">Specifies one or more field names that the <legacyBold>Recordset</legacyBold> is sorted on, and whether each field is sorted in ascending or descending order.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b0bfb0800cbe97c299f1800ddbea004d" id="tgt65" class="tgtSentence">Method Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="741eccb617f4f0bd88f5be02e382f179" id="tgt66" class="tgtSentence">The Cursor Service for OLE DB enables or affects the behavior of the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object's <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method; and the <legacyBold>Recordset</legacyBold> object's <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink>, <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, and <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> methods.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> As a result, the user perceives relatively uniform functionality from all data providers.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example, the <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find</legacyLink> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The Cursor Service enables support for batch updating in all cases.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Keyword</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">To invoke this service component, set the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> or <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object's <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
          <code>connection.CursorLocation=adUseClient
recordset.CursorLocation=adUseClient</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the <legacyBold>Recordset </legacyBold>object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The full list of <legacyBold>Connection</legacyBold> and <legacyBold>Recordset</legacyBold> object dynamic properties is listed in the <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">ADO Dynamic Property Index</legacyLink>.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The associated OLE DB property names, where appropriate, are included in parentheses after the ADO property name.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> For example, setting the <legacyItalic>Command Time out</legacyItalic> property on a <legacyBold>Recordset</legacyBold> will not be visible to the underlying data provider.</caps:sentence>
          </para>
          <code>
Recordset1.CursorLocation = adUseClient     'invokes cursor service
Recordset1.Open "authors", _
    "Provider=SQLOLEDB;Data Source=DBServer;User Id=MyUserID;" &amp; _
    "Password=MyPassword;Initial Catalog=pubs;",,adCmdTable
Recordset1.Properties.Item("Command Time out") = 50
' 'Command Time out' property on DBServer is still default (30).
</code>
          <para>
            <caps:sentence id="src15" class="srcSentence">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Command object property settings are always passed to the underlying data provider regardless of cursor location.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Therefore, you can also use a command object to set the properties at any time.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src18" class="srcSentence">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</caps:sentence>
            </para>
          </alert>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Auto Recalc (DBPROP_ADC_AUTORECALC)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated.</caps:sentence>
                    <caps:sentence id="src23" class="srcSentence"> The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed.</caps:sentence>
                    <caps:sentence id="src24" class="srcSentence"> If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Batch Size (DBPROP_ADC_BATCHSIZE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Indicates the number of update statements that can be batched before being sent to the data store.</caps:sentence>
                    <caps:sentence id="src27" class="srcSentence"> The more statements in a batch, the fewer round trips to the data store.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Cache Child Rows (DBPROP_ADC_CACHECHILDROWS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Cursor Engine Version (DBPROP_ADC_CEVER)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Indicates the version of the Cursor Service being used.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Maintain Change Status (DBPROP_ADC_MAINTAINCHANGESTATUS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">
                      <caps:sentence id="src34" class="srcSentence">Optimize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Indicates whether an index should be created.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> When set to <legacyBold>True</legacyBold>, authorizes the temporary creation of indexes to improve the execution of certain operations.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="690229d1-46cc-42e6-a57d-4438251fe248">
                      <caps:sentence id="src37" class="srcSentence">Reshape Name</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Indicates the name of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                    <caps:sentence id="src39" class="srcSentence"> Can be referenced within the current, or subsequent, data shaping commands.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="4e2bb601-0fe8-4d61-b00e-38341d85a6bb">
                      <caps:sentence id="src40" class="srcSentence">Resync Command</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Indicates a custom command string that is used by the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method when the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> property is in effect.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">
                      <caps:sentence id="src42" class="srcSentence">Unique Catalog</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Indicates the name of the database containing the table referenced in the <legacyBold>Unique Table</legacyBold> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">
                      <caps:sentence id="src44" class="srcSentence">Unique Schema</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Indicates the name of the owner of the table referenced in the <legacyBold>Unique Table</legacyBold> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">
                      <caps:sentence id="src46" class="srcSentence">Unique Table</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Indicates the name of the one table in a <legacyBold>Recordset</legacyBold> created from multiple tables that can be modified by insertions, updates, or deletions.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Update Criteria (DBPROP_ADC_UPDATECRITERIA)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Indicates which fields in the <legacyBold>WHERE</legacyBold> clause are used to handle collisions occurring during an update.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">
                      <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink>               <legacyUnderline>               </legacyUnderline>(DBPROP_ADC_UPDATERESYNC)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Indicates whether the <legacyBold>Resync</legacyBold> method is implicitly invoked after the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method (and its behavior), when the <legacyBold>Unique Table</legacyBold> property is in effect.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src52" class="srcSentence">You can also set or retrieve a dynamic property by specifying its name as the index to the <legacyBold>Properties</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src53" class="srcSentence"> For example, get and print the current value of the <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> dynamic property, then set a new value, as follows:</caps:sentence>
          </para>
          <code>Debug.Print rs.Properties("Optimize")
rs.Properties("Optimize") = True</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src54" class="srcSentence">Built-in Property Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src55" class="srcSentence">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">
                      <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Supplements the types of cursors that are available for a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">
                      <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">Supplements the types of locks available for a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                    <caps:sentence id="src62" class="srcSentence"> Enables batch updates.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3683ffa0-6f93-4906-9533-ef6942f24f39">
                      <caps:sentence id="src63" class="srcSentence">Sort</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">Specifies one or more field names that the <legacyBold>Recordset</legacyBold> is sorted on, and whether each field is sorted in ascending or descending order.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src65" class="srcSentence">Method Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src66" class="srcSentence">The Cursor Service for OLE DB enables or affects the behavior of the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object's <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method; and the <legacyBold>Recordset</legacyBold> object's <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink>, <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, and <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> methods.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Provider Support for ADOX (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64234ce5-dc46-4c8a-a316-61956b6b9abb
caps.latest.revision: 5
caps.handback.revision: 5
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
# Provider Support for ADOX (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="554b97c56b9c7a700a9ab977e38b07e7" id="tgt1" class="tgtSentence">Certain features of ADOX are unsupported, depending on your OLE DB data provider.</caps:sentence>
          <caps:sentence sentenceid="9b5f38c94477f74df886ecd4ac9c942c" id="tgt2" class="tgtSentence"> ADOX is fully supported with the <legacyLink xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="8202129464d3a3c13dedbfc42d76ddbc" id="tgt3" class="tgtSentence"> The unsupported features with the <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink>, the <legacyLink xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</legacyLink>, or the <legacyLink xlink:href="44fae9dd-5585-4cd6-8bbd-3248a78931b4">Microsoft OLE DB Provider for Oracle</legacyLink> are listed in the following tables.</caps:sentence>
          <caps:sentence sentenceid="3d0b1328d5c49c2f50a62eaadd2cc761" id="tgt4" class="tgtSentence"> ADOX is not supported by any other Microsoft OLE DB providers.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="c87e1b32e0e41d9a0e382032944e8f76" id="tgt5" class="tgtSentence">Microsoft OLE DB Provider for SQL Server</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c496bbc3481207a663fc513bc12f87fd" id="tgt6" class="tgtSentence">Object or Collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd7928bc30325cdd9b3490e535a55bb" id="tgt7" class="tgtSentence">Usage Restriction</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34d7bc312e59aa7282fe61d68ef1fe58" id="tgt8" class="tgtSentence">               <legacyBold>Tables</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="47b6bdc9596b3a29f8285afaaef1ecbe" id="tgt9" class="tgtSentence">Properties are read/write prior to object creation, and read-only when referencing an existing object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="baffc572e887986d503f25f4c59df92d" id="tgt10" class="tgtSentence">               <legacyBold>Views</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c09589c1d899d7078d12ce227e0973f0" id="tgt11" class="tgtSentence">               <legacyBold>Views</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f7b08bf77b4cceb3f05398810c174ff" id="tgt12" class="tgtSentence">               <legacyBold>Procedures</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt13" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0bbf05aa3e214b1c0b6969bed3c0c797" id="tgt14" class="tgtSentence">               <legacyBold>Procedure</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba3ae2d9b9f95487b9d9cb20b8e07067" id="tgt15" class="tgtSentence">The <legacyBold>Command</legacyBold> property is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54a8e1e9fdb32e34519c82dd4df3ba0c" id="tgt16" class="tgtSentence">               <legacyBold>Keys</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt17" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="df19c6f606c5784121164628328731d5" id="tgt18" class="tgtSentence">               <legacyBold>Users</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6b36a4423047c307db0a5a9e707dd7a" id="tgt19" class="tgtSentence">               <legacyBold>Users</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="690536b2516b5533e931ef04f637bfb2" id="tgt20" class="tgtSentence">               <legacyBold>Groups</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="603343238d598defbded489d26c1ac2f" id="tgt21" class="tgtSentence">               <legacyBold>Groups</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d6abca3ce8fa57bb33203ab88be81395" id="tgt22" class="tgtSentence">Microsoft OLE DB Provider for ODBC</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c496bbc3481207a663fc513bc12f87fd" id="tgt23" class="tgtSentence">Object or Collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd7928bc30325cdd9b3490e535a55bb" id="tgt24" class="tgtSentence">Usage Restriction</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75ace33b5a3e3c235e39cfc42a0491ea" id="tgt25" class="tgtSentence">               <legacyBold>Catalog</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d116ad7f5b58566ad7b227daa9800d9e" id="tgt26" class="tgtSentence">The <legacyBold>Create</legacyBold> method is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34d7bc312e59aa7282fe61d68ef1fe58" id="tgt27" class="tgtSentence">               <legacyBold>Tables</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt28" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                    <caps:sentence sentenceid="069534dfdea8cd64e09a5d399beb6341" id="tgt29" class="tgtSentence"> Properties are read/write prior to object creation, and read-only when referencing an existing object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f7b08bf77b4cceb3f05398810c174ff" id="tgt30" class="tgtSentence">               <legacyBold>Procedures</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt31" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0bbf05aa3e214b1c0b6969bed3c0c797" id="tgt32" class="tgtSentence">               <legacyBold>Procedure</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba3ae2d9b9f95487b9d9cb20b8e07067" id="tgt33" class="tgtSentence">The <legacyBold>Command</legacyBold> property is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb84868bd53347aa3f8eb1394b93c613" id="tgt34" class="tgtSentence">               <legacyBold>Indexes</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt35" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54a8e1e9fdb32e34519c82dd4df3ba0c" id="tgt36" class="tgtSentence">               <legacyBold>Keys</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt37" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="df19c6f606c5784121164628328731d5" id="tgt38" class="tgtSentence">               <legacyBold>Users</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6b36a4423047c307db0a5a9e707dd7a" id="tgt39" class="tgtSentence">               <legacyBold>Users</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="690536b2516b5533e931ef04f637bfb2" id="tgt40" class="tgtSentence">               <legacyBold>Groups</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="603343238d598defbded489d26c1ac2f" id="tgt41" class="tgtSentence">               <legacyBold>Groups</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="726db96d1a9d92af9984537b59b0aa0d" id="tgt42" class="tgtSentence">Microsoft OLE DB Provider for Oracle</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c496bbc3481207a663fc513bc12f87fd" id="tgt43" class="tgtSentence">Object or Collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd7928bc30325cdd9b3490e535a55bb" id="tgt44" class="tgtSentence">Usage Restriction</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75ace33b5a3e3c235e39cfc42a0491ea" id="tgt45" class="tgtSentence">               <legacyBold>Catalog</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d116ad7f5b58566ad7b227daa9800d9e" id="tgt46" class="tgtSentence">The <legacyBold>Create</legacyBold> method is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34d7bc312e59aa7282fe61d68ef1fe58" id="tgt47" class="tgtSentence">               <legacyBold>Tables</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt48" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                    <caps:sentence sentenceid="069534dfdea8cd64e09a5d399beb6341" id="tgt49" class="tgtSentence"> Properties are read/write prior to object creation, and read-only when referencing an existing object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="baffc572e887986d503f25f4c59df92d" id="tgt50" class="tgtSentence">               <legacyBold>Views</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt51" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba87213c339668724daccb4943651e68" id="tgt52" class="tgtSentence">               <legacyBold>View</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba3ae2d9b9f95487b9d9cb20b8e07067" id="tgt53" class="tgtSentence">The <legacyBold>Command</legacyBold> property is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="33f4091d0a07f2fe6b9d4e7fe90497e3" id="tgt54" class="tgtSentence">               <legacyBold>Procedures</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt55" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0bbf05aa3e214b1c0b6969bed3c0c797" id="tgt56" class="tgtSentence">               <legacyBold>Procedure</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba3ae2d9b9f95487b9d9cb20b8e07067" id="tgt57" class="tgtSentence">The <legacyBold>Command</legacyBold> property is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb84868bd53347aa3f8eb1394b93c613" id="tgt58" class="tgtSentence">               <legacyBold>Indexes</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt59" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54a8e1e9fdb32e34519c82dd4df3ba0c" id="tgt60" class="tgtSentence">               <legacyBold>Keys</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="506bad7ac28243feb5d63a25176544b7" id="tgt61" class="tgtSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="df19c6f606c5784121164628328731d5" id="tgt62" class="tgtSentence">               <legacyBold>Users</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6b36a4423047c307db0a5a9e707dd7a" id="tgt63" class="tgtSentence">               <legacyBold>Users</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="690536b2516b5533e931ef04f637bfb2" id="tgt64" class="tgtSentence">               <legacyBold>Groups</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="603343238d598defbded489d26c1ac2f" id="tgt65" class="tgtSentence">               <legacyBold>Groups</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Certain features of ADOX are unsupported, depending on your OLE DB data provider.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> ADOX is fully supported with the <legacyLink xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</legacyLink>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The unsupported features with the <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink>, the <legacyLink xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</legacyLink>, or the <legacyLink xlink:href="44fae9dd-5585-4cd6-8bbd-3248a78931b4">Microsoft OLE DB Provider for Oracle</legacyLink> are listed in the following tables.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> ADOX is not supported by any other Microsoft OLE DB providers.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Microsoft OLE DB Provider for SQL Server</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">Object or Collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Usage Restriction</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">               <legacyBold>Tables</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Properties are read/write prior to object creation, and read-only when referencing an existing object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">               <legacyBold>Views</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">               <legacyBold>Views</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">               <legacyBold>Procedures</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">               <legacyBold>Procedure</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">The <legacyBold>Command</legacyBold> property is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">               <legacyBold>Keys</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">               <legacyBold>Users</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">               <legacyBold>Users</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">               <legacyBold>Groups</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">               <legacyBold>Groups</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Microsoft OLE DB Provider for ODBC</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Object or Collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Usage Restriction</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">               <legacyBold>Catalog</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">The <legacyBold>Create</legacyBold> method is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">               <legacyBold>Tables</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                    <caps:sentence id="src29" class="srcSentence"> Properties are read/write prior to object creation, and read-only when referencing an existing object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">               <legacyBold>Procedures</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">               <legacyBold>Procedure</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">The <legacyBold>Command</legacyBold> property is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">               <legacyBold>Indexes</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">               <legacyBold>Keys</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">               <legacyBold>Users</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">               <legacyBold>Users</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">               <legacyBold>Groups</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">               <legacyBold>Groups</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src42" class="srcSentence">Microsoft OLE DB Provider for Oracle</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Object or Collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Usage Restriction</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">               <legacyBold>Catalog</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">The <legacyBold>Create</legacyBold> method is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">               <legacyBold>Tables</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                    <caps:sentence id="src49" class="srcSentence"> Properties are read/write prior to object creation, and read-only when referencing an existing object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">               <legacyBold>Views</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">               <legacyBold>View</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">The <legacyBold>Command</legacyBold> property is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">               <legacyBold>Procedures</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">               <legacyBold>Procedure</legacyBold> object</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">The <legacyBold>Command</legacyBold> property is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">               <legacyBold>Indexes</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">               <legacyBold>Keys</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">The <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods are not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">               <legacyBold>Users</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">               <legacyBold>Users</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">               <legacyBold>Groups</legacyBold> collection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">               <legacyBold>Groups</legacyBold> is not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
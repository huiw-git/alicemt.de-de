---
title: "ADO Dynamic Property Index"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 80d389dd-46ef-459f-b0d4-6f712fc4f32d
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
# ADO Dynamic Property Index
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9c547e0f5c31c572a8ddcf7ec433fe35" id="tgt1" class="tgtSentence">Data providers, service providers, and service components can add dynamic properties to the <legacyBold>Properties</legacyBold> collections of the unopened <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> and <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects.</caps:sentence>
          <caps:sentence sentenceid="9db28ca6239b2a1a2624d331225f557d" id="tgt2" class="tgtSentence"> A given provider may also insert additional properties when these objects are opened.</caps:sentence>
          <caps:sentence sentenceid="8cc83a8ee1aec1775680fb31e1fd7173" id="tgt3" class="tgtSentence"> Some of these properties are listed in the <legacyLink xlink:href="d7b06d72-f792-4328-93a2-5006b9e2c581">ADO Dynamic Properties</legacyLink> section.</caps:sentence>
          <caps:sentence sentenceid="b01d527ef91391a0823c01cb10750a40" id="tgt4" class="tgtSentence"> More are listed under the specific providers in the <legacyLink xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</legacyLink> section.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f527fb4922be6609d5f4af1b5ba15c11" id="tgt5" class="tgtSentence">The following tables are cross-indexes of the ADO and OLE DB names for each standard OLE DB provider dynamic property.</caps:sentence>
          <caps:sentence sentenceid="f7d73dfe0602cc487c49aed784915c0c" id="tgt6" class="tgtSentence"> Your providers may add more properties than listed here.</caps:sentence>
          <caps:sentence sentenceid="449ef15a09fd3afc95a7a6cb256df950" id="tgt7" class="tgtSentence"> For the specific information about provider-specific dynamic properties, see your provider documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e42fcd75e6a641587d04ef2afad819b4" id="tgt8" class="tgtSentence">The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</caps:sentence>
          <caps:sentence sentenceid="38817b7da38a9c3d2b2619d4fb86c646" id="tgt9" class="tgtSentence"> For more information about these standard properties, search or browse the index in the <externalLink><linkText>OLE DB documentation</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms722784.aspx</linkUri></externalLink>for the OLE DB property by its name.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="cc03d661ba78db29ad696232fbdfd45d" id="tgt10" class="tgtSentence">Connection Dynamic Properties</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt11" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt12" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42da7b3adedde15ba58b5e8f720f0729" id="tgt13" class="tgtSentence">Active Sessions</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5db97e3405ada5593894afe7c26e912a" id="tgt14" class="tgtSentence">DBPROP_ACTIVESESSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5fb6f6fbeeed9d35163820f4cad357a5" id="tgt15" class="tgtSentence">Asynchable Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a69ebf5e5b867b80a10c033ec247f235" id="tgt16" class="tgtSentence">DBPROP_ASYNCTXNABORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1553c09566f739d416c34417c3eed8bc" id="tgt17" class="tgtSentence">Asynchable Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8fb4c7f494cd85116f18f4e23dfa3ce2" id="tgt18" class="tgtSentence">DBPROP_ASYNCTNXCOMMIT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ac1b75d9d496be787670b775f6cbc81" id="tgt19" class="tgtSentence">Autocommit Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ed9f459c36be0b771e14849bddd615a" id="tgt20" class="tgtSentence">DBPROP_SESS_AUTOCOMMITISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04e7adcf92320728ff99be4ae9e20b80" id="tgt21" class="tgtSentence">Catalog Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cc7d88f9c70b084ff349547378be6ea7" id="tgt22" class="tgtSentence">DBPROP_CATALOGLOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0d5a9974623ad1d08ec1a87d28e3382b" id="tgt23" class="tgtSentence">Catalog Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5ec52858196e5661e26c0593dc0055f3" id="tgt24" class="tgtSentence">DBPROP_CATALOGTERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ccf0f62c35ce6f4ad47c504191cbc48" id="tgt25" class="tgtSentence">Column Definition</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4036e684cbb10c6c00160fb3f89fec78" id="tgt26" class="tgtSentence">DBPROP_COLUMNDEFINITION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf6acbf359c2d19032f195b15434cbdf" id="tgt27" class="tgtSentence">Connect Timeout</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb371d4f9db6357d81826f393345882e" id="tgt28" class="tgtSentence">DBPROP_INIT_TIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6cf2a5823099e39d4bfcd079068b384d" id="tgt29" class="tgtSentence">Current Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1975407cf7846b03983297436f6feaec" id="tgt30" class="tgtSentence">DBPROP_CURRENTCATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f0262ef78817e828a92d75e9749b4f9" id="tgt31" class="tgtSentence">Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f628f4ca9169da470c6349e4dadfd7b" id="tgt32" class="tgtSentence">DBPROP_INIT_DATASOURCE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4cc4008aeaa109c055aa7289fe8955f6" id="tgt33" class="tgtSentence">Data Source Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f70e2b308e36cc86cb62a25d0cc89d0" id="tgt34" class="tgtSentence">DBPROP_DATASOURCENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0902cf5b7d19a0cc4c0d745125932c99" id="tgt35" class="tgtSentence">Data Source Object Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6168b0502be04b450b621cc21978b79" id="tgt36" class="tgtSentence">DBPROP_DSOTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44576fc26ad5240af73f0f7304ac0161" id="tgt37" class="tgtSentence">DBMS Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8bfb66db9f6b9a9d8249efb32f35bc2" id="tgt38" class="tgtSentence">DBPROP_DBMSNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0865166992725c390cf3955eb7005314" id="tgt39" class="tgtSentence">DBMS Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="91a28922f266288ed023d4fb5e1a9f41" id="tgt40" class="tgtSentence">DBPROP_DBMSVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="01a074046ca4de7469fdd27ef0f56b30" id="tgt41" class="tgtSentence">Extended Properties</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ad981c384f6deb06078fb96a4f6db4af" id="tgt42" class="tgtSentence">DBPROP_INIT_PROVIDERSTRING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fc489b2e87836669c99f48d36447d508" id="tgt43" class="tgtSentence">GROUP BY Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b73b41cab609c063b7570db22674bb0" id="tgt44" class="tgtSentence">DBPROP_GROUPBY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7970e9c2391aaf6904a12c0b64590ee7" id="tgt45" class="tgtSentence">Heterogeneous Table Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8732f1c0c3c20adc7bc8f5f878f4e95f" id="tgt46" class="tgtSentence">DBPROP_HETEROGENEOUSTABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3cc7d428494725fbc1c4117841759a1b" id="tgt47" class="tgtSentence">Identifier Case Sensitivity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f959d99f6f9ff2380e84ed5f89a6545" id="tgt48" class="tgtSentence">DBPROP_IDENTIFIERCASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d61a95016e0ce8932a33ae801954fdbe" id="tgt49" class="tgtSentence">Initial Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="966c4e343eb272d1b5309d5b41dcd77e" id="tgt50" class="tgtSentence">DBPROP_INIT_CATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6d922da801c791516e0fde80744ddda1" id="tgt51" class="tgtSentence">Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b826970c6bc792cec29c7154b97b055f" id="tgt52" class="tgtSentence">DBPROP_SUPPORTEDTXNISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="36d2944c902a8b3bfc937a35534e6d67" id="tgt53" class="tgtSentence">Isolation Retention</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1180eb611191e300302c020a0433017a" id="tgt54" class="tgtSentence">DBPROP_SUPPORTEDTXNISORETAIN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d42b4f73ee8bf025a3c06cfa5499f55" id="tgt55" class="tgtSentence">Locale Identifier</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a119da28f65a0343b705f027db4eb589" id="tgt56" class="tgtSentence">DBPROP_INIT_LCID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5189de027922f81005951e6efe0efd5" id="tgt57" class="tgtSentence">Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4c7b060f7306f6b592e88374da28bc30" id="tgt58" class="tgtSentence">DBPROP_INIT_LOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d632dbafbc50f25c220bda2bd1d5eb79" id="tgt59" class="tgtSentence">Maximum Index Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0a5f4509b189658a32142048499fb311" id="tgt60" class="tgtSentence">DBPROP_MAXINDEXSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a3cbd82a49b4e695c986f9e21e08bec0" id="tgt61" class="tgtSentence">Maximum Row Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6414b671b9497a028ae03e2ff2baa8a2" id="tgt62" class="tgtSentence">DBPROP_MAXROWSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3fe8d182c92e2a2da388835b24f6a538" id="tgt63" class="tgtSentence">Maximum Row Size Includes BLOB</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82a79937366130603485b2e8243110f3" id="tgt64" class="tgtSentence">DBPROP_MAXROWSIZEINCLUDESBLOB</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="72fa89be4e41d4eec9682e3012510c70" id="tgt65" class="tgtSentence">Maximum Tables in SELECT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12775fa00655f15737d2b126875edf54" id="tgt66" class="tgtSentence">DBPROP_MAXTABLESINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="15d61712450a686a7f365adf4fef581f" id="tgt67" class="tgtSentence">Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e24a70a829cb0fe614e775e6b781aeef" id="tgt68" class="tgtSentence">DBPROP_INIT_MODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5fa88b3a7f2866a505f6869084d9dbac" id="tgt69" class="tgtSentence">Multiple Parameter Sets</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5b07a57182c870a463947bbe8862f2a" id="tgt70" class="tgtSentence">DBPROP_MULTIPLEPARAMSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34467f0701793e142a97280886a37d11" id="tgt71" class="tgtSentence">Multiple Results</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c6d16a5ed96ee324aaea5d56f93b9ca" id="tgt72" class="tgtSentence">DBPROP_MULTIPLERESULTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94a2500d5a620b62d088ba5e147f9300" id="tgt73" class="tgtSentence">Multiple Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4d0892bbf21bca8cbb05c7688e4481a" id="tgt74" class="tgtSentence">DBPROP_MULTIPLESTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49a7ede339dd477496917e520e53b211" id="tgt75" class="tgtSentence">Multi-Table Update</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45718feaf0858fc05c6e2c5653af9fa5" id="tgt76" class="tgtSentence">DBPROP_MULTITABLEUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="068577c6d2defffb1af7047830fb7e89" id="tgt77" class="tgtSentence">NULL Collation Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="169e04896d93bdec8bd59547b5636cf4" id="tgt78" class="tgtSentence">DBPROP_NULLCOLLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="51a10c8ee8acbdda689781c851e4dbfb" id="tgt79" class="tgtSentence">NULL Concatenation Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="86d53a1e665c382405ca707e70950ee9" id="tgt80" class="tgtSentence">DBPROP_CONCATNULLBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b6cc341a84e9a5f17c1bb02869de8f68" id="tgt81" class="tgtSentence">OLE DB Services</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="20f1f64900731090c77cd859723438e1" id="tgt82" class="tgtSentence">DBPROP_INIT_OLEDBSERVICES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54d02916d0ddd080374282c66901c59c" id="tgt83" class="tgtSentence">OLE DB Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8678185cda69da06b0b18cdede8c9aaf" id="tgt84" class="tgtSentence">DBPROP_PROVIDEROLEDBVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c77b810e588a10689239bf12710a9027" id="tgt85" class="tgtSentence">OLE Object Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9aa0a480916fc5befab6d11935037f12" id="tgt86" class="tgtSentence">DBPROP_OLEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="305717e26f640fcebb5c11bdf62692b0" id="tgt87" class="tgtSentence">Open Rowset Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="467a15dbf1a07da68a090197a6350d8e" id="tgt88" class="tgtSentence">DBPROP_OPENROWSETSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d8d10a19d6045a2990194103e79da9e6" id="tgt89" class="tgtSentence">ORDER BY Columns in Select List</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17519abd080309120a91fbe406545057" id="tgt90" class="tgtSentence">DBPROP_ORDERBYCOLUMNSINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c8bdd56df539c7147de1a6309ccf033" id="tgt91" class="tgtSentence">Output Parameter Availability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b3bb7f1b82d23d1accfa030b4372da90" id="tgt92" class="tgtSentence">DBPROP_OUTPUTPARAMETERAVAILABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ec1f372d153601374fe2b3be37c84a7" id="tgt93" class="tgtSentence">Pass By Ref Accessors</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b063a15f21255c314931eb858f8c898" id="tgt94" class="tgtSentence">DBPROP_BYREFACCESSORS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f4dcc3b5aa765d61d8327deb882cf99" id="tgt95" class="tgtSentence">Password</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a4dad287f50102726dc53803031a610a" id="tgt96" class="tgtSentence">DBPROP_AUTH_PASSWORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="503154ffbc8d4b9909f934dd562a5753" id="tgt97" class="tgtSentence">Persist Security Info</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7902596f88afd8b04b6b61fc09d1a39e" id="tgt98" class="tgtSentence">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d99d60bd887e031a71ff6eff10d6d3d4" id="tgt99" class="tgtSentence">Persistent ID Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ea254ecd2f23ef9f83d15db428137a57" id="tgt100" class="tgtSentence">DBPROP_PERSISTENTIDTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="77b5b43a8424c46e81df1ab0fc6e466d" id="tgt101" class="tgtSentence">Prepare Abort Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c461cd8da2a2986434667ac22d8c4113" id="tgt102" class="tgtSentence">DBPROP_PREPAREABORTBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc732b57d8b179ab01d66f1adcddf935" id="tgt103" class="tgtSentence">Prepare Commit Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5956c34c7c59de311a271e3cc843ced" id="tgt104" class="tgtSentence">DBPROP_PREPARECOMMITBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b307899aa47ab53211ca988c38acf75e" id="tgt105" class="tgtSentence">Procedure Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39fca27d3fe2656d61424456d445849b" id="tgt106" class="tgtSentence">DBPROP_PROCEDURETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ae35dbb42614d2429b7d6d181a950bb" id="tgt107" class="tgtSentence">Prompt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a23c8807135a34f56166fc290ce391c" id="tgt108" class="tgtSentence">DBPROP_INIT_PROMPT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ebbb5df827311326b2ebdcd6cf839f95" id="tgt109" class="tgtSentence">Provider Friendly Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="590bff2f7b8796e1277a936f16a2a7ff" id="tgt110" class="tgtSentence">DBPROP_PROVIDERFRIENDLYNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe158741a51803d31ec342eea567a79" id="tgt111" class="tgtSentence">Provider Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af443c478802f07802f2dc40b36c12b0" id="tgt112" class="tgtSentence">DBPROP_PROVIDERFILENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6ee1f505ae87ddc1ca51166091edec7" id="tgt113" class="tgtSentence">Provider Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d547dd6794dc65d1cbc34bc9a3646cab" id="tgt114" class="tgtSentence">DBPROP_PROVIDERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="14bb11993e3371d739eebc9648db4ec8" id="tgt115" class="tgtSentence">Read-Only Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fbaa45e63afd58892cad4204394e4b4a" id="tgt116" class="tgtSentence">DBPROP_DATASOURCEREADONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b68e1280ee9c56976f9918f1b143ae9b" id="tgt117" class="tgtSentence">Rowset Conversions on Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e9ea492c28f4f9e0ebe6ab7b04499f0a" id="tgt118" class="tgtSentence">DBPROP_ROWSETCONVERSIONSONCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4e214d42f27db2df22d820f4339ab38" id="tgt119" class="tgtSentence">Schema Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="177617f0fc571a0b532c7358fec97041" id="tgt120" class="tgtSentence">DBPROP_SCHEMATERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="996b43fdeae58150436e00ab086e55f9" id="tgt121" class="tgtSentence">Schema Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af6ca7abc5e28a6ba9bc5998e88fc4de" id="tgt122" class="tgtSentence">DBPROP_SCHEMAUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3887b124c8b8b2ac1076ac2fbc50a5a8" id="tgt123" class="tgtSentence">SQL Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67a078a8eabce39c390405b03eaf82df" id="tgt124" class="tgtSentence">DBPROP_SQLSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82b1c99e1276c7b9329843b82cb249a2" id="tgt125" class="tgtSentence">Structured Storage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a912ffa112b5c65343d1368268679294" id="tgt126" class="tgtSentence">DBPROP_STRUCTUREDSTORAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a51c825ecd8a692b685d0736d13a30c8" id="tgt127" class="tgtSentence">Subquery Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2dc44fc06f6f61c8b1e7f8c8b1dc7226" id="tgt128" class="tgtSentence">DBPROP_SUBQUERIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1fa0c9780d8a58f26e201af8cdc9d7d5" id="tgt129" class="tgtSentence">Table Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c25b152bb6a5d33613780d82b09f83f" id="tgt130" class="tgtSentence">DBPROP_TABLETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26e3db30e914b1bf231f1dc48149a6ab" id="tgt131" class="tgtSentence">Transaction DDL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d94fb60768ed9e61630670c5b707db5e" id="tgt132" class="tgtSentence">DBPROP_SUPPORTEDTXNDDL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3bd756a1167a9bff574b512092d53350" id="tgt133" class="tgtSentence">User ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d9c5665b97893aac40b03266365060d" id="tgt134" class="tgtSentence">DBPROP_AUTH_USERID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f28564ce8593a50b9cf507aecccd8cd6" id="tgt135" class="tgtSentence">User Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0673f982c2e13e63312a0a61aed98966" id="tgt136" class="tgtSentence">DBPROP_USERNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98487bfe9fe529e4a2738b2ad9eacaec" id="tgt137" class="tgtSentence">Window Handle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3a92acd985b6ab8b1df6d3cd4df47e83" id="tgt138" class="tgtSentence">DBPROP_INIT_HWND</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0d8dea92a1ae91e40f5bc79d56f722e5" id="tgt139" class="tgtSentence">Recordset Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="242d1d1d3e51788fead303b34707a620" id="tgt140" class="tgtSentence">Note that the <legacyBold>Dynamic Properties</legacyBold> of the <legacyBold>Recordset</legacyBold> object go out of scope (become unavailable) when the <legacyBold>Recordset</legacyBold> is closed.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt141" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt142" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d33d5718660dbb261dc40b878ec4b591" id="tgt143" class="tgtSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6886831ffa7619b0308b059afaf5299c" id="tgt144" class="tgtSentence">DBPROP_IACCESSOR </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5e5cd95860891cad64474412ee90af1a" id="tgt145" class="tgtSentence">IChapteredRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="28dbf41d74f2a648a563b28d2ecef878" id="tgt146" class="tgtSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="611a4238fcdbad4f6e89046493e35de0" id="tgt147" class="tgtSentence">DBPROP_ICOLUMNSINFO </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6317b9d062ca4ded11773f5df0c39062" id="tgt148" class="tgtSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e506f15e9aee3d9c423b57397f93e437" id="tgt149" class="tgtSentence">DBPROP_ICOLUMNSROWSET </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63e99e63156fc90f114fa402662387ef" id="tgt150" class="tgtSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="72822068521469c9d1b00837d0bb2b5f" id="tgt151" class="tgtSentence">DBPROP_ICONNECTIONPOINTCONTAINER </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="280d1ffb462810568a6fdc7ed49c472c" id="tgt152" class="tgtSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45afed999f9128204c1b1e5adf7405f8" id="tgt153" class="tgtSentence">ILockBytes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2ccb5efefd400811707e523c510a723b" id="tgt154" class="tgtSentence">DBPROP_ILOCKBYTES </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5e86d5adb921fd6e7b7616e2cc6d0b1" id="tgt155" class="tgtSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ef63b2b4842ade544d4de2158e797717" id="tgt156" class="tgtSentence">DBPROP_IROWSET </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6dc1de1d52cfbefb671e60c2a7b1f89e" id="tgt157" class="tgtSentence">IDBAsynchStatus</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49b1de26969426b6df7a2e31533f0152" id="tgt158" class="tgtSentence">DBPROP_IDBASYNCHSTATUS </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8d31569998e304eab8571ce72e0e3cdb" id="tgt159" class="tgtSentence">IParentRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5cf35ba4349e6da426be07d34952411e" id="tgt160" class="tgtSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8996770a4fa8fc8c1d34e7bfd27e9ac7" id="tgt161" class="tgtSentence">DBPROP_IROWSETCHANGE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0ac1e43ea5712672b6adf48cdf5246e0" id="tgt162" class="tgtSentence">IRowsetExactScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="10f6850c6aa126774a1d937b6ec6d3fb" id="tgt163" class="tgtSentence">IRowsetFind</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="723200bb730018eee26e94815a1c7c49" id="tgt164" class="tgtSentence">DBPROP_IROWSETFIND </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f7deea1588ac1cc7f77f6df70c1434b" id="tgt165" class="tgtSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ee54a0493768ecf57b6f9a7d9c266fc7" id="tgt166" class="tgtSentence">DBPROP_IROWSETIDENTITY </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1c6d3c5946bb65aba4e55669cac68a" id="tgt167" class="tgtSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9783eacb32f857e8004608899a034194" id="tgt168" class="tgtSentence">DBPROP_IROWSETINFO </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92f23aaea36b3e3b3f1b4b456d4b0f8a" id="tgt169" class="tgtSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5397d060180ea2090c106629535da25d" id="tgt170" class="tgtSentence">DBPROP_IROWSETLOCATE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a509122e4f7b09d76c968a5d3cee6757" id="tgt171" class="tgtSentence">IRowsetRefresh</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="256184aacfccffaac0db8222f19512cb" id="tgt172" class="tgtSentence">DBPROP_IROWSETREFRESH </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82189c22157ca5dbc1566ce5b8fee507" id="tgt173" class="tgtSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="151e636103f6679064656728e4630284" id="tgt174" class="tgtSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="93d134a5c63e2c41ace79e55ee5d8d7e" id="tgt175" class="tgtSentence">DBPROP_IROWSETSCROLL </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="869692d9e5c7b7dc7dcfdaf30a7bd348" id="tgt176" class="tgtSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44cec27e40673b096878ecdc71c37074" id="tgt177" class="tgtSentence">DBPROP_IROWSETUPDATE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="27946685b7e1a1c23dd6257c28381045" id="tgt178" class="tgtSentence">IRowsetView</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12da5d7a9ebaad01f868a8dcc81e60cf" id="tgt179" class="tgtSentence">DBPROP_IROWSETVIEW </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e3f7c5b1879950f9342e7cced01273f3" id="tgt180" class="tgtSentence">IRowsetIndex</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="96d2d585adaf07fa94444ad86f2b27d9" id="tgt181" class="tgtSentence">DBPROP_IROWSETINDEX </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fd77e41428ef2a86d5994c0a4e658f" id="tgt182" class="tgtSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d68076b032d02d8500bb2f2390398843" id="tgt183" class="tgtSentence">DBPROP_ISEQUENTIALSTREAM </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="40f5759c2cdc1f9b68e6b0c162714753" id="tgt184" class="tgtSentence">IStorage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cbb7ca66e24930a3d780c32379f73ae" id="tgt185" class="tgtSentence">DBPROP_ISTORAGE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2d5d0d1cb71d3cef4032b3cad9fcb77" id="tgt186" class="tgtSentence">IStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9b1853e47e4ef917c973ed53c6ce7a26" id="tgt187" class="tgtSentence">DBPROP_ISTREAM </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="130702210bcc45e1afd88b1f2aae1a0b" id="tgt188" class="tgtSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2baf6836f95476cf303d01619e33d3a2" id="tgt189" class="tgtSentence">DBPROP_ISUPPORTERRORINFO </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1594fad277e4590ddbbf46e340c4d10c" id="tgt190" class="tgtSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3ae70d0cfd08d73c0e8657de04e3ba3" id="tgt191" class="tgtSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7bc03dfea4165f8cc7279ecbcee1f41e" id="tgt192" class="tgtSentence">Append-Only Rowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="323934bf263c92d3fce05577ebb64799" id="tgt193" class="tgtSentence">DBPROP_APPENDONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dbbc616fd0604ee68420a8ccf53969d9" id="tgt194" class="tgtSentence">Asynchronous Rowset Processing</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0ec674b74922731c6fe3932e0764544a" id="tgt195" class="tgtSentence">DBPROP_ROWSET_ASYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="327b772024f35ad789d92527ca64a8ba" id="tgt196" class="tgtSentence">Auto Recalc</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b6857e30b5fd697a0d66ea47e384ce3" id="tgt197" class="tgtSentence">DBPROP_ADC_AUTORECALC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="19792b50eb9b914ebb3896bdd560bcfa" id="tgt198" class="tgtSentence">Background Fetch Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9bdade0f8b89d2c6ba0ba8684a2c84b4" id="tgt199" class="tgtSentence">DBPROP_ASYNCHFETCHSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c37936c53964a93832b28f3989ddb2ef" id="tgt200" class="tgtSentence">Background Thread Priority</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="364e03e07b11e64add28863ecfff2e3b" id="tgt201" class="tgtSentence">DBPROP_ASYNCHTHREADPRIORITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b794c3472cd5959995fef64fdf565cd7" id="tgt202" class="tgtSentence">Batch Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="acb345f1417a9b65ea83c32e73b67fe2" id="tgt203" class="tgtSentence">DBPROP_ADC_BATCHSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b52683364c551ef6f2a83a9b61aca26" id="tgt204" class="tgtSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7eade57591bcbdf71a01307c5fa55333" id="tgt205" class="tgtSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39674232a2f3f57e87b6f56e9fcd620c" id="tgt206" class="tgtSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c5692554e1273a4cc28709961881f78" id="tgt207" class="tgtSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab13a6b41c0fedc395cff5ae82b531b6" id="tgt208" class="tgtSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5397d060180ea2090c106629535da25d" id="tgt209" class="tgtSentence">DBPROP_IROWSETLOCATE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="422691e4a2607d6fbf9785c231c0ea8a" id="tgt210" class="tgtSentence">Bookmarks Ordered</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa7751ca5633df65e31f1c633c547600" id="tgt211" class="tgtSentence">DBPROP_ORDEREDBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5db1f76cd6c6b2450b1bb5be91470318" id="tgt212" class="tgtSentence">Cache Child Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b35c873606757affdcdff277f5748e6" id="tgt213" class="tgtSentence">DBPROP_ADC_CACHECHILDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="187e822fb45791582a5f5e12e783c1c0" id="tgt214" class="tgtSentence">Cache Deferred Columns</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8683aa6604e702bc21392138b519177" id="tgt215" class="tgtSentence">DBPROP_CACHEDEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="246a7d96dd79b612bad343d03ea2bec6" id="tgt216" class="tgtSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75cbb9fc61a14afcadf102cfdd0a6733" id="tgt217" class="tgtSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="534d9e8ffeeeff5bf0f381032bbefd20" id="tgt218" class="tgtSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3eac3ca56c13d98b9d1f1d8ef5620027" id="tgt219" class="tgtSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30f3aa8c0ff671730367a69d810898b9" id="tgt220" class="tgtSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32873d7085b6feb780bf00ea59c3a386" id="tgt221" class="tgtSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ece0c04224a4c71df58445121e0aa118" id="tgt222" class="tgtSentence">Column Writable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fe0ab4d24b04b7f23827a14cb6c9ea2" id="tgt223" class="tgtSentence">DBPROP_MAYWRITECOLUMN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="68484ede52d011ad20cc9399010ba11a" id="tgt224" class="tgtSentence">Command Time Out</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ff64c42d8e170982b23167bd7148d889" id="tgt225" class="tgtSentence">DBPROP_COMMANDTIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0811caf5ace745f82ce469f72c6400d3" id="tgt226" class="tgtSentence">Cursor Engine Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a9b6f4d21958526a309e58c4b499d84d" id="tgt227" class="tgtSentence">DBPROP_ADC_CEVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec83d16d5fb11f0a7e532fe6a91dfc36" id="tgt228" class="tgtSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af283d090de02b75e79bf25ce7aa945a" id="tgt229" class="tgtSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c34dec6888b6b898acb79b0597922c27" id="tgt230" class="tgtSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7906ea7eac0a5466ea33c9bf87d083db" id="tgt231" class="tgtSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c24d8cc4559e441d51781708292d746" id="tgt232" class="tgtSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b5c3be77a4c5f0654fd6637b3fd2b44" id="tgt233" class="tgtSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f1ce7d926d49686f2b0ea6d20aa718e6" id="tgt234" class="tgtSentence">Filter Operations</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5edb9a334d3dcb47fff0ae82990f4b4d" id="tgt235" class="tgtSentence">DBPROP_FILTERCOMPAREOPS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="452fca443453a880852d9e18b969f4f8" id="tgt236" class="tgtSentence">Find Operations</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a625465dbe8d6b813361c162bcdc8935" id="tgt237" class="tgtSentence">DBPROP_FINDCOMPAREOPS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e42ed0d2724f3fe3f85117b59b1b6591" id="tgt238" class="tgtSentence">Hidden Columns (Count)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db9ec5de7fe13b4ed459ba0cf6258eb2" id="tgt239" class="tgtSentence">DBPROP_HIDDENCOLUMNS </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f518893e9bb8f74c9382260d0f79450b" id="tgt240" class="tgtSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2bdf72f0b7184d9ebe2e4086c598ee58" id="tgt241" class="tgtSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="215599a847f963e27588b79210d3ea56" id="tgt242" class="tgtSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be4b610383a4b1af3438c855f29cb110" id="tgt243" class="tgtSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c9fbbb80f5342a86f4dc9020eb519eab" id="tgt244" class="tgtSentence">Initial Fetch Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ecbfbb801fc326133bb4c11ae1bf1c25" id="tgt245" class="tgtSentence">DBPROP_ASYNCHPREFETCHSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34cd68a4ad9a3b16548954ff8184424c" id="tgt246" class="tgtSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbe0ebf1ce342bea12faf4f9960e35db" id="tgt247" class="tgtSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="627482c800288bba5eaa6324bec11b5a" id="tgt248" class="tgtSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8709209928583492b7e8ee9057e1dcd2" id="tgt249" class="tgtSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6457b0ea1522c0956c7b017db927a374" id="tgt250" class="tgtSentence">Maintain Change Status</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cc4696d4ecf686e9bd663f1dfed78ffd" id="tgt251" class="tgtSentence">DBPROP_ADC_MAINTAINCHANGESTATUS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37f4175871594fd8b8484066ab57df1f" id="tgt252" class="tgtSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="610508ace43dba0c007eb22818d91137" id="tgt253" class="tgtSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09b385ae7a340805af12a182ddf23eb4" id="tgt254" class="tgtSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f76fd118082b0c0ce064d13a83f97d8" id="tgt255" class="tgtSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2a235cb612ded93059abe7d46a49fe3" id="tgt256" class="tgtSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2048410c3ee67fb1184d889ab1cdb77" id="tgt257" class="tgtSentence">DBPROP_MAXROWS </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8112db23cce9278ba61947c470e76c84" id="tgt258" class="tgtSentence">Memory Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab00228ad48e6044d3e6fa7f306b6984" id="tgt259" class="tgtSentence">DBPROP_MEMORYUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9cf646cc11e82fcf71add13e9d665dd" id="tgt260" class="tgtSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17bc94f9006a838977a349a959373da8" id="tgt261" class="tgtSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c018979b39f45a0e004063ce0373c75f" id="tgt262" class="tgtSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00045b5ae2bb643fd385c818dc8e48c6" id="tgt263" class="tgtSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cd5ca965481ad65661cdb310d078fa3" id="tgt264" class="tgtSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7319271b36838a8630e00ceb4554a65" id="tgt265" class="tgtSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf6cb25fea1126c44957f7d00a3a2c4f" id="tgt266" class="tgtSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2e7ff400a4ef4b66e01a7d0219e3d034" id="tgt267" class="tgtSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe7ca5c576c7eb49b58dec45de3b371" id="tgt268" class="tgtSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4267002726b89c5712c11b77ab4b758" id="tgt269" class="tgtSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f08474ed3d97c8e3919ffe184b8cb02e" id="tgt270" class="tgtSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ffd196cae96727a7c58c6701e3c65c1" id="tgt271" class="tgtSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45b7a56f3096b95b93f70ce662332136" id="tgt272" class="tgtSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8d7e45b16c6a09599199e5237263f63" id="tgt273" class="tgtSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="780561121ea65efc60d011b3855083ed" id="tgt274" class="tgtSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8bbf20691fd6dfdc3b55d73bb1b4df42" id="tgt275" class="tgtSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c89b03f5c13331074eed0814571479b" id="tgt276" class="tgtSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1be32916280f74ae0b5b31424efe2e97" id="tgt277" class="tgtSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b02473597f9e0fb7e5b9b7e239f0c8da" id="tgt278" class="tgtSentence">Private1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="360431977c32a0e461c2a887196342cf" id="tgt279" class="tgtSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="015f02a3c579b5978974bb340adbc2ed" id="tgt280" class="tgtSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2fee318949f99eb5f0586e8492ffbaa" id="tgt281" class="tgtSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46634a21ff13d23b96f57f1b7a8e74b3" id="tgt282" class="tgtSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af57e2554f3db187894681afa3ebb162" id="tgt283" class="tgtSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="120451667e76bd8d13d0f0fce84d89e0" id="tgt284" class="tgtSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90f54100a94260ff7c00300f6cfd91d3" id="tgt285" class="tgtSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe1dffe626e729c9881c31329af50b19" id="tgt286" class="tgtSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32db6247d3f003bc7a5d97b7b4165920" id="tgt287" class="tgtSentence">Reshape Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4c8d209de79abd4bfc1996d89b3cff26" id="tgt288" class="tgtSentence">DBPROP_ADC_RESHAPENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0dd7af9563cc090b0f27867527af0395" id="tgt289" class="tgtSentence">Resync Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f234c0cb4d747f0d4ff38eb9fe2856fd" id="tgt290" class="tgtSentence">DBPROP_ADC_CUSTOMRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="993c9b2a5a406fa810a7c0a353c0241d" id="tgt291" class="tgtSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62dbebf39ca99d9e0f7d2548b1a1e897" id="tgt292" class="tgtSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="594965351c01632879dd3120d6bdf6d1" id="tgt293" class="tgtSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dacf8514ed973feacfcb951277d7a7e0" id="tgt294" class="tgtSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26a6a1d6d267ebfa661503a67852b551" id="tgt295" class="tgtSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78e460d27437866f950bef1a322f4fad" id="tgt296" class="tgtSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1082afc70d114a04c5a7c028f54bbef" id="tgt297" class="tgtSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af912945703d4c7e5769a4a5e275c429" id="tgt298" class="tgtSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e89662e8e842b5980db8ce27cddbb136" id="tgt299" class="tgtSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f0866326f49f046b4c2d341fbf8b4a8" id="tgt300" class="tgtSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1a3b43e5bc3c750c8484e75d2dc513" id="tgt301" class="tgtSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d147a76184915ab68be6596b43255f" id="tgt302" class="tgtSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d60a3e481cd7af54f8384abea4e16a7c" id="tgt303" class="tgtSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65b8fe6df5aa2933471401a6b676fba7" id="tgt304" class="tgtSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1198df197cf7df924a1b241c2b2f0043" id="tgt305" class="tgtSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18919c01495e96c385f2eaf5938a7b03" id="tgt306" class="tgtSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdb695a9cc13c0f5e2c73bda79d0aaf" id="tgt307" class="tgtSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a40c17ef17a290d8ff208c5db8518c1" id="tgt308" class="tgtSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78cbcb8d94e6c7daf9e961f93e6b2886" id="tgt309" class="tgtSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d19dc5275a879b3a434a516970425f79" id="tgt310" class="tgtSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5b98c46a74cf81a3a5714e4746025dc3" id="tgt311" class="tgtSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb5fb6c60c1d012edd101ab61e996364" id="tgt312" class="tgtSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8a7611a82fb7d9716f4f12a82fb60754" id="tgt313" class="tgtSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3528ed34871b6b038968af4a908dc081" id="tgt314" class="tgtSentence">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16753e39b4d45199dca719ac2995aeb1" id="tgt315" class="tgtSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="824f2ba91f8243744ab6a8227fbb157f" id="tgt316" class="tgtSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adc2bf5dd51cf373e1aacf17aef14bbd" id="tgt317" class="tgtSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ac6cf4fa0ff0c7b5050593b220d13af2" id="tgt318" class="tgtSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="415a343da7783a4dd06c09c7a67f8825" id="tgt319" class="tgtSentence">Server Cursor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfd7e7c46ce15b85949bbb20dc2eb8f6" id="tgt320" class="tgtSentence">DBPROP_SERVERCURSOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="692ef25d05bb91b856cf5d0564cf74fd" id="tgt321" class="tgtSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87f408e0686b76395d281e685f65bc08" id="tgt322" class="tgtSentence">DBPROP_BOOKMARKSKIPPED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2463d9a101f9c39973277d105f8bf119" id="tgt323" class="tgtSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f0289c4d7472816b838bf34a3b92d2c" id="tgt324" class="tgtSentence">DBPROP_STRONGIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f5c39b758518eb085ca020b4de55ce76" id="tgt325" class="tgtSentence">Unique Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="863986e96eaa43b468537657a0e0b978" id="tgt326" class="tgtSentence">DBPROP_ADC_UNIQUECATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3d6c9ba3726667cb820e5f392952aca6" id="tgt327" class="tgtSentence">Unique Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fe0a5bebaaa20210a94be8f859bc9b3" id="tgt328" class="tgtSentence">DBPROP_UNIQUEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ccfa118b2e3c050a4247f4faa7dfbc4d" id="tgt329" class="tgtSentence">Unique Schema</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7156d31f96369634a66e9598e8a461e2" id="tgt330" class="tgtSentence">DBPROP_ADC_UNIQUESCHEMA</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78d4188fdc2991f037b3e3902e9e6e72" id="tgt331" class="tgtSentence">Unique Table</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="496f838f794f780555193f4e4d9c10f4" id="tgt332" class="tgtSentence">DBPROP_ADC_UNIQUETABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11c74d1c21dc5dbb8b802a7408596d87" id="tgt333" class="tgtSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2086801d6ac44d08784890faac1a126" id="tgt334" class="tgtSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4379727161de9d8593f2c5d233f2ffe4" id="tgt335" class="tgtSentence">Update Criteria</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f46a0f3686caa8e5d8afbb63615233f8" id="tgt336" class="tgtSentence">DBPROP_ADC_UPDATECRITERIA</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4c7e997b553022372be79e3b4ab383a7" id="tgt337" class="tgtSentence">Update Resync</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0004f5c68bcc434b8cecf7a6c20e7e3d" id="tgt338" class="tgtSentence">DBPROP_ADC_UPDATERESYNC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7a56dd282a8abf8100c423430ec8e4ac" id="tgt339" class="tgtSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd43d482f9e85ec89014c21fbd361a4" id="tgt340" class="tgtSentence">DBPROP_BOOKMARKS</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Data providers, service providers, and service components can add dynamic properties to the <legacyBold>Properties</legacyBold> collections of the unopened <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> and <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A given provider may also insert additional properties when these objects are opened.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Some of these properties are listed in the <legacyLink xlink:href="d7b06d72-f792-4328-93a2-5006b9e2c581">ADO Dynamic Properties</legacyLink> section.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> More are listed under the specific providers in the <legacyLink xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</legacyLink> section.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The following tables are cross-indexes of the ADO and OLE DB names for each standard OLE DB provider dynamic property.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Your providers may add more properties than listed here.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> For the specific information about provider-specific dynamic properties, see your provider documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> For more information about these standard properties, search or browse the index in the <externalLink><linkText>OLE DB documentation</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms722784.aspx</linkUri></externalLink>for the OLE DB property by its name.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Connection Dynamic Properties</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Active Sessions</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">DBPROP_ACTIVESESSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Asynchable Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">DBPROP_ASYNCTXNABORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Asynchable Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">DBPROP_ASYNCTNXCOMMIT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Autocommit Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">DBPROP_SESS_AUTOCOMMITISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Catalog Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">DBPROP_CATALOGLOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Catalog Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">DBPROP_CATALOGTERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Column Definition</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">DBPROP_COLUMNDEFINITION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Connect Timeout</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">DBPROP_INIT_TIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Current Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">DBPROP_CURRENTCATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">DBPROP_INIT_DATASOURCE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Data Source Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">DBPROP_DATASOURCENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Data Source Object Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">DBPROP_DSOTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">DBMS Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">DBPROP_DBMSNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">DBMS Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">DBPROP_DBMSVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Extended Properties</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">DBPROP_INIT_PROVIDERSTRING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">GROUP BY Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">DBPROP_GROUPBY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Heterogeneous Table Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">DBPROP_HETEROGENEOUSTABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Identifier Case Sensitivity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">DBPROP_IDENTIFIERCASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Initial Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">DBPROP_INIT_CATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">DBPROP_SUPPORTEDTXNISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Isolation Retention</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">DBPROP_SUPPORTEDTXNISORETAIN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Locale Identifier</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">DBPROP_INIT_LCID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">DBPROP_INIT_LOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Maximum Index Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">DBPROP_MAXINDEXSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">Maximum Row Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">DBPROP_MAXROWSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Maximum Row Size Includes BLOB</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">DBPROP_MAXROWSIZEINCLUDESBLOB</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">Maximum Tables in SELECT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">DBPROP_MAXTABLESINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">DBPROP_INIT_MODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">Multiple Parameter Sets</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">DBPROP_MULTIPLEPARAMSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">Multiple Results</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">DBPROP_MULTIPLERESULTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">Multiple Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">DBPROP_MULTIPLESTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">Multi-Table Update</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">DBPROP_MULTITABLEUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">NULL Collation Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">DBPROP_NULLCOLLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">NULL Concatenation Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">DBPROP_CONCATNULLBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">OLE DB Services</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">DBPROP_INIT_OLEDBSERVICES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">OLE DB Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">DBPROP_PROVIDEROLEDBVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">OLE Object Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">DBPROP_OLEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">Open Rowset Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">DBPROP_OPENROWSETSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">ORDER BY Columns in Select List</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">DBPROP_ORDERBYCOLUMNSINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">Output Parameter Availability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">DBPROP_OUTPUTPARAMETERAVAILABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">Pass By Ref Accessors</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">DBPROP_BYREFACCESSORS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">Password</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">DBPROP_AUTH_PASSWORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src97" class="srcSentence">Persist Security Info</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">Persistent ID Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">DBPROP_PERSISTENTIDTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">Prepare Abort Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">DBPROP_PREPAREABORTBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src103" class="srcSentence">Prepare Commit Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">DBPROP_PREPARECOMMITBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">Procedure Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">DBPROP_PROCEDURETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">Prompt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">DBPROP_INIT_PROMPT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">Provider Friendly Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">DBPROP_PROVIDERFRIENDLYNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">Provider Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">DBPROP_PROVIDERFILENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">Provider Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">DBPROP_PROVIDERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">Read-Only Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">DBPROP_DATASOURCEREADONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">Rowset Conversions on Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">DBPROP_ROWSETCONVERSIONSONCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">Schema Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">DBPROP_SCHEMATERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">Schema Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src122" class="srcSentence">DBPROP_SCHEMAUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src123" class="srcSentence">SQL Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">DBPROP_SQLSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">Structured Storage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">DBPROP_STRUCTUREDSTORAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">Subquery Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">DBPROP_SUBQUERIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">Table Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">DBPROP_TABLETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src131" class="srcSentence">Transaction DDL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">DBPROP_SUPPORTEDTXNDDL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">User ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">DBPROP_AUTH_USERID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">User Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">DBPROP_USERNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">Window Handle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">DBPROP_INIT_HWND</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src139" class="srcSentence">Recordset Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src140" class="srcSentence">Note that the <legacyBold>Dynamic Properties</legacyBold> of the <legacyBold>Recordset</legacyBold> object go out of scope (become unavailable) when the <legacyBold>Recordset</legacyBold> is closed.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">DBPROP_IACCESSOR </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">IChapteredRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">DBPROP_ICOLUMNSINFO </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src148" class="srcSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">DBPROP_ICOLUMNSROWSET </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">DBPROP_ICONNECTIONPOINTCONTAINER </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">ILockBytes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">DBPROP_ILOCKBYTES </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src155" class="srcSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">DBPROP_IROWSET </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">IDBAsynchStatus</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">DBPROP_IDBASYNCHSTATUS </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">IParentRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">DBPROP_IROWSETCHANGE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">IRowsetExactScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">IRowsetFind</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">DBPROP_IROWSETFIND </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">DBPROP_IROWSETIDENTITY </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">DBPROP_IROWSETINFO </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">DBPROP_IROWSETLOCATE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">IRowsetRefresh</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">DBPROP_IROWSETREFRESH </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">DBPROP_IROWSETSCROLL </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">DBPROP_IROWSETUPDATE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">IRowsetView</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">DBPROP_IROWSETVIEW </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">IRowsetIndex</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">DBPROP_IROWSETINDEX </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">DBPROP_ISEQUENTIALSTREAM </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">IStorage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">DBPROP_ISTORAGE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">IStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">DBPROP_ISTREAM </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">DBPROP_ISUPPORTERRORINFO </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src190" class="srcSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">Append-Only Rowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src193" class="srcSentence">DBPROP_APPENDONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">Asynchronous Rowset Processing</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">DBPROP_ROWSET_ASYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">Auto Recalc</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src197" class="srcSentence">DBPROP_ADC_AUTORECALC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">Background Fetch Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">DBPROP_ASYNCHFETCHSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">Background Thread Priority</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">DBPROP_ASYNCHTHREADPRIORITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">Batch Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">DBPROP_ADC_BATCHSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src206" class="srcSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src208" class="srcSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">DBPROP_IROWSETLOCATE </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src210" class="srcSentence">Bookmarks Ordered</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src211" class="srcSentence">DBPROP_ORDEREDBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">Cache Child Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">DBPROP_ADC_CACHECHILDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">Cache Deferred Columns</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src215" class="srcSentence">DBPROP_CACHEDEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src216" class="srcSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src217" class="srcSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src218" class="srcSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src219" class="srcSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src220" class="srcSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src221" class="srcSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src222" class="srcSentence">Column Writable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src223" class="srcSentence">DBPROP_MAYWRITECOLUMN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">Command Time Out</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src225" class="srcSentence">DBPROP_COMMANDTIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src226" class="srcSentence">Cursor Engine Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src227" class="srcSentence">DBPROP_ADC_CEVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src228" class="srcSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src229" class="srcSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src230" class="srcSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src233" class="srcSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src234" class="srcSentence">Filter Operations</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src235" class="srcSentence">DBPROP_FILTERCOMPAREOPS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src236" class="srcSentence">Find Operations</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src237" class="srcSentence">DBPROP_FINDCOMPAREOPS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src238" class="srcSentence">Hidden Columns (Count)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src239" class="srcSentence">DBPROP_HIDDENCOLUMNS </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src240" class="srcSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src241" class="srcSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src242" class="srcSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src243" class="srcSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">Initial Fetch Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src245" class="srcSentence">DBPROP_ASYNCHPREFETCHSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src248" class="srcSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src250" class="srcSentence">Maintain Change Status</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src251" class="srcSentence">DBPROP_ADC_MAINTAINCHANGESTATUS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src252" class="srcSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src253" class="srcSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src254" class="srcSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src255" class="srcSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src256" class="srcSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src257" class="srcSentence">DBPROP_MAXROWS </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src258" class="srcSentence">Memory Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src259" class="srcSentence">DBPROP_MEMORYUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src260" class="srcSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src261" class="srcSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src262" class="srcSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src263" class="srcSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src264" class="srcSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src265" class="srcSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src267" class="srcSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src268" class="srcSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src269" class="srcSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src270" class="srcSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src271" class="srcSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src272" class="srcSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src273" class="srcSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src274" class="srcSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src275" class="srcSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src276" class="srcSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src277" class="srcSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src278" class="srcSentence">Private1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>               </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src280" class="srcSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src281" class="srcSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src282" class="srcSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src283" class="srcSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src284" class="srcSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src285" class="srcSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src286" class="srcSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src287" class="srcSentence">Reshape Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src288" class="srcSentence">DBPROP_ADC_RESHAPENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src289" class="srcSentence">Resync Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src290" class="srcSentence">DBPROP_ADC_CUSTOMRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src291" class="srcSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src292" class="srcSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src293" class="srcSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src294" class="srcSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src295" class="srcSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src296" class="srcSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src297" class="srcSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src298" class="srcSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src299" class="srcSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src300" class="srcSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src301" class="srcSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src302" class="srcSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src303" class="srcSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src304" class="srcSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src305" class="srcSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src306" class="srcSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src307" class="srcSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src308" class="srcSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src309" class="srcSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src310" class="srcSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src311" class="srcSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src312" class="srcSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src313" class="srcSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src314" class="srcSentence">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src315" class="srcSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src316" class="srcSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src317" class="srcSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src318" class="srcSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src319" class="srcSentence">Server Cursor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src320" class="srcSentence">DBPROP_SERVERCURSOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src321" class="srcSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src322" class="srcSentence">DBPROP_BOOKMARKSKIPPED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src323" class="srcSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src324" class="srcSentence">DBPROP_STRONGIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src325" class="srcSentence">Unique Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src326" class="srcSentence">DBPROP_ADC_UNIQUECATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src327" class="srcSentence">Unique Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src328" class="srcSentence">DBPROP_UNIQUEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src329" class="srcSentence">Unique Schema</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src330" class="srcSentence">DBPROP_ADC_UNIQUESCHEMA</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src331" class="srcSentence">Unique Table</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src332" class="srcSentence">DBPROP_ADC_UNIQUETABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src333" class="srcSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src334" class="srcSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src335" class="srcSentence">Update Criteria</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src336" class="srcSentence">DBPROP_ADC_UPDATECRITERIA</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src337" class="srcSentence">Update Resync</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src338" class="srcSentence">DBPROP_ADC_UPDATERESYNC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src339" class="srcSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src340" class="srcSentence">DBPROP_BOOKMARKS</caps:sentence>
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
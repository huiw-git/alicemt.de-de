---
title: "RightsEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 55ee67c7-a583-42aa-849a-78264b4cb614
caps.latest.revision: 10
caps.handback.revision: 10
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
# RightsEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4e1bf689d17ba58905f47f888441fc37" id="tgt1" class="tgtSentence">Specifies the rights or permissions for a group or user on an object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt2" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt3" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt4" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a1e63bdaade1f403bcefd264223b978" id="tgt5" class="tgtSentence">
                      <legacyBold>adRightCreate</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0ce7291a5d83345c496e171d9d036642" id="tgt6" class="tgtSentence">16384 (&amp;H4000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30d4501cc8ac3901efc33e33e0e7ed54" id="tgt7" class="tgtSentence">The user or group has permission to create new objects of this type.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a744b6a850ecb547ea947e45052f368b" id="tgt8" class="tgtSentence">
                      <legacyBold>adRightDelete</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c69633a3e224524bdc8ae6216f0d7279" id="tgt9" class="tgtSentence">65536 (&amp;H10000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7e13771b3134523c790881e0b6f4887f" id="tgt10" class="tgtSentence">The user or group has permission to delete data from an object.</caps:sentence>
                    <caps:sentence sentenceid="0594c110513ca2a4dabec6e202f87417" id="tgt11" class="tgtSentence"> For objects such as <legacyBold>Tables</legacyBold>, the user has permission to delete data values from records.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f20dd3746f57160fab93587ff6baebc" id="tgt12" class="tgtSentence">
                      <legacyBold>adRightDrop</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cf9e1aa636f5ca610145840ce639127" id="tgt13" class="tgtSentence">256 (&amp;H100)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="50e950625967be7b8d7582ad0a93e59a" id="tgt14" class="tgtSentence">The user or group has permission to remove objects from the catalog.</caps:sentence>
                    <caps:sentence sentenceid="3d957fd6b8245d2b543a2eb0c763de27" id="tgt15" class="tgtSentence"> For example, <legacyBold>Tables</legacyBold> can be deleted by a DROP TABLE SQL command.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b0a73f56634795a48aeea20375757714" id="tgt16" class="tgtSentence">
                      <legacyBold>adRightExclusive</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="735701794ddddb8617cbea5304e9edb7" id="tgt17" class="tgtSentence">512 (&amp;H200)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc848e195389302ebfc17919908d0dd8" id="tgt18" class="tgtSentence">The user or group has permission to access the object exclusively.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a04aa9e2d71428347a3c78719e1cacab" id="tgt19" class="tgtSentence">
                      <legacyBold>adRightExecute</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26679eb4397cd8cdeb5a68d000b84e59" id="tgt20" class="tgtSentence">536870912 (&amp;H20000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00426dc78ee20ee1315616d642286a19" id="tgt21" class="tgtSentence">The user or group has permission to execute the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adfa88f7945281ccd27c241d90cb81c2" id="tgt22" class="tgtSentence">
                      <legacyBold>adRightFull</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="23d1de355827f5a97f39e19de16c2be4" id="tgt23" class="tgtSentence">268435456 (&amp;H10000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8221ce2b1284360180f9b20db120fdd" id="tgt24" class="tgtSentence">The user or group has all permissions on the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c48571604b1a54fbba8ac8e1643724c" id="tgt25" class="tgtSentence">
                      <legacyBold>adRightInsert</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="639fb850bea9f16bf3f31f67ea24bb55" id="tgt26" class="tgtSentence">32768 (&amp;H8000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ac5088d0bfe9cbb1a60241e2a6f2192b" id="tgt27" class="tgtSentence">The user or group has permission to insert the object.</caps:sentence>
                    <caps:sentence sentenceid="c549c00366726263493a328035950a4f" id="tgt28" class="tgtSentence"> For objects such as <legacyBold>Tables</legacyBold>, the user has permission to insert data into the table.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5e5f2d967850e43f62964b4553c4a3bd" id="tgt29" class="tgtSentence">
                      <legacyBold>adRightMaximumAllowed</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b09493e51077b99709e9a30c890ee54d" id="tgt30" class="tgtSentence">33554432 (&amp;H2000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2119f405e0206c84d6fb1d6163fefd5" id="tgt31" class="tgtSentence">The user or group has the maximum number of permissions allowed by the provider.</caps:sentence>
                    <caps:sentence sentenceid="456a4cc5947c133ce2307fcd569b850f" id="tgt32" class="tgtSentence"> Specific permissions are provider-dependent.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a4523b89dc21a051db8091d0a286a8f1" id="tgt33" class="tgtSentence">
                      <legacyBold>adRightNone</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt34" class="tgtSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b5898101c59d035509495800ca064486" id="tgt35" class="tgtSentence">The user or group has no permissions for the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f88bc72d70470af97605edce876b6be1" id="tgt36" class="tgtSentence">
                      <legacyBold>adRightRead</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ebfd34e55346d868c9130db5557481ed" id="tgt37" class="tgtSentence">-2147483648 (&amp;H80000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0126ae2c532896931057e018061ed2d6" id="tgt38" class="tgtSentence">The user or group has permission to read the object.</caps:sentence>
                    <caps:sentence sentenceid="95cca6ec0428732c15bf3031eba8cead" id="tgt39" class="tgtSentence"> For objects such as <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Tables</legacyLink>, the user has permission to read the data in the table.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6d0eb2d45ff6ba56d7d52e101bd05637" id="tgt40" class="tgtSentence">
                      <legacyBold>adRightReadDesign</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="02b77facdfd275f0eefbf08cbd58f8d4" id="tgt41" class="tgtSentence">1024 (&amp;H400)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2ffae890dc2ae5224c617732ef87307" id="tgt42" class="tgtSentence">The user or group has permission to read the design for the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82e5ceb2a3e68f455928b35ed5a939ae" id="tgt43" class="tgtSentence">
                      <legacyBold>adRightReadPermissions</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ac6c836d70974e83c6224a51ace6a11" id="tgt44" class="tgtSentence">131072 (&amp;H20000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d0f5464b2686b2076a81fea823c374b" id="tgt45" class="tgtSentence">The user or group can view, but not change, the specific permissions for an object in the catalog.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e55064c925e58c0d524954b90e00be52" id="tgt46" class="tgtSentence">
                      <legacyBold>adRightReference</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f13b5f0a0b3e3b13f70bef3b654effa0" id="tgt47" class="tgtSentence">8192 (&amp;H2000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ce369adf871450279eb7be690ec3ad9e" id="tgt48" class="tgtSentence">The user or group has permission to reference the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="15bfcb7e9575b337109615d776e91f20" id="tgt49" class="tgtSentence">
                      <legacyBold>adRightUpdate</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d92977d58401035f3a4fe5c331422d7" id="tgt50" class="tgtSentence">1073741824 (&amp;H40000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7220a538cb43755fb32e96dc596a65ef" id="tgt51" class="tgtSentence">The user or group has permission to update the object.</caps:sentence>
                    <caps:sentence sentenceid="dda48ead3b3567e9cf350cf19c50c531" id="tgt52" class="tgtSentence"> For objects such as <legacyBold>Tables</legacyBold>, the user has permission to update the data in the table.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8b9caf1b91dcdce7ed415401b7a7d11" id="tgt53" class="tgtSentence">
                      <legacyBold>adRightWithGrant</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="73fa3b7abafa47ed10c10639ea22dd30" id="tgt54" class="tgtSentence">4096 (&amp;H1000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="69066124053c6a2db8de357155126028" id="tgt55" class="tgtSentence">The user or group has permission to grant permissions on the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="873b5e6df6d58da2a1d92117ba4cd054" id="tgt56" class="tgtSentence">
                      <legacyBold>adRightWriteDesign</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="10ffaa62157f46864c7a2b9bfcf60c98" id="tgt57" class="tgtSentence">2048 (&amp;H800)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3fbdcad5c5050330207e4e8f4a02c179" id="tgt58" class="tgtSentence">The user or group has permission to modify the design for the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42c8c9ee5cbe174f41a906cf1db6e9af" id="tgt59" class="tgtSentence">
                      <legacyBold>adRightWriteOwner</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="031dc63b660ee94ace7b844e24f0b7a3" id="tgt60" class="tgtSentence">524288 (&amp;H80000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e18ef97e6303069d602e06a99adafcab" id="tgt61" class="tgtSentence">The user or group has permission to modify the owner of the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ff15b533c751ac7cd2b89e0460b17ddc" id="tgt62" class="tgtSentence">
                      <legacyBold>adRightWritePermissions</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a78692551436fd50857bd5d87bfd658f" id="tgt63" class="tgtSentence">262144 (&amp;H40000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9892fc3236683d5ed3e118804633749c" id="tgt64" class="tgtSentence">The user or group can modify the specific permissions for an object in the catalog.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt65" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions Method</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the rights or permissions for a group or user on an object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src2" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src3" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">
                      <legacyBold>adRightCreate</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">16384 (&amp;H4000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">The user or group has permission to create new objects of this type.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">
                      <legacyBold>adRightDelete</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">65536 (&amp;H10000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">The user or group has permission to delete data from an object.</caps:sentence>
                    <caps:sentence id="src11" class="srcSentence"> For objects such as <legacyBold>Tables</legacyBold>, the user has permission to delete data values from records.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">
                      <legacyBold>adRightDrop</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">256 (&amp;H100)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">The user or group has permission to remove objects from the catalog.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> For example, <legacyBold>Tables</legacyBold> can be deleted by a DROP TABLE SQL command.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">
                      <legacyBold>adRightExclusive</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">512 (&amp;H200)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">The user or group has permission to access the object exclusively.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">
                      <legacyBold>adRightExecute</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">536870912 (&amp;H20000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">The user or group has permission to execute the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">
                      <legacyBold>adRightFull</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">268435456 (&amp;H10000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">The user or group has all permissions on the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">
                      <legacyBold>adRightInsert</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">32768 (&amp;H8000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">The user or group has permission to insert the object.</caps:sentence>
                    <caps:sentence id="src28" class="srcSentence"> For objects such as <legacyBold>Tables</legacyBold>, the user has permission to insert data into the table.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">
                      <legacyBold>adRightMaximumAllowed</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">33554432 (&amp;H2000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">The user or group has the maximum number of permissions allowed by the provider.</caps:sentence>
                    <caps:sentence id="src32" class="srcSentence"> Specific permissions are provider-dependent.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">
                      <legacyBold>adRightNone</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">The user or group has no permissions for the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">
                      <legacyBold>adRightRead</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">-2147483648 (&amp;H80000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">The user or group has permission to read the object.</caps:sentence>
                    <caps:sentence id="src39" class="srcSentence"> For objects such as <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Tables</legacyLink>, the user has permission to read the data in the table.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">
                      <legacyBold>adRightReadDesign</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">1024 (&amp;H400)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">The user or group has permission to read the design for the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">
                      <legacyBold>adRightReadPermissions</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">131072 (&amp;H20000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">The user or group can view, but not change, the specific permissions for an object in the catalog.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">
                      <legacyBold>adRightReference</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">8192 (&amp;H2000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">The user or group has permission to reference the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">
                      <legacyBold>adRightUpdate</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">1073741824 (&amp;H40000000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">The user or group has permission to update the object.</caps:sentence>
                    <caps:sentence id="src52" class="srcSentence"> For objects such as <legacyBold>Tables</legacyBold>, the user has permission to update the data in the table.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">
                      <legacyBold>adRightWithGrant</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">4096 (&amp;H1000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">The user or group has permission to grant permissions on the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">
                      <legacyBold>adRightWriteDesign</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">2048 (&amp;H800)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">The user or group has permission to modify the design for the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">
                      <legacyBold>adRightWriteOwner</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">524288 (&amp;H80000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">The user or group has permission to modify the owner of the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">
                      <legacyBold>adRightWritePermissions</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">262144 (&amp;H40000)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">The user or group can modify the specific permissions for an object in the catalog.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src65" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions Method</link>
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
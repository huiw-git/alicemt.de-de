---
title: "IsolationLevelEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8e17a7bc-b8a3-4ae2-b6c9-ce088ad31fdf
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
# IsolationLevelEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="fc655b768116a70ebad72a009a4c8144" id="tgt1" class="tgtSentence">Specifies the level of transaction isolation for a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
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
                  <legacyBold>
                    <caps:sentence sentenceid="b48662ca211a117da172c873b797eaa6" id="tgt5" class="tgtSentence">adXactUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt6" class="tgtSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9132126db5f03ad97d30ed0d5cc32aee" id="tgt7" class="tgtSentence">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="9e983dba4a829d174a973f08a828f186" id="tgt8" class="tgtSentence">adXactChaos</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c74d97b01eae257e44aa9d5bade97baf" id="tgt9" class="tgtSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e1ab50100cfc976bcc1c1072aa6aa360" id="tgt10" class="tgtSentence">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="f35c94995a79ed9ac378c39499dd04c3" id="tgt11" class="tgtSentence">adXactBrowse</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f718499c1c8cef6730f9fd03c8125cab" id="tgt12" class="tgtSentence">256</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="63aed7720919948c4796db7b645bf66d" id="tgt13" class="tgtSentence">Indicates that from one transaction you can view uncommitted changes in other transactions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="0ea813265ec306f81dedd15a58480313" id="tgt14" class="tgtSentence">adXactReadUncommitted</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f718499c1c8cef6730f9fd03c8125cab" id="tgt15" class="tgtSentence">256</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a1fc606533d949b0e9ab64f3df50c70d" id="tgt16" class="tgtSentence">Same as <legacyBold>adXactBrowse</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="615b4b7aeabf746b5f54438439b21772" id="tgt17" class="tgtSentence">adXactCursorStability</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f7efa4f864ae9b88d43527f4b14f750f" id="tgt18" class="tgtSentence">4096</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5099547935962adb0b6c6fee28f5ca05" id="tgt19" class="tgtSentence">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="edbd9f0f5f6b54bd854ccc1817be81e4" id="tgt20" class="tgtSentence">adXactReadCommitted</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f7efa4f864ae9b88d43527f4b14f750f" id="tgt21" class="tgtSentence">4096</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e5b273b64997b3a23a55593e3ebe630f" id="tgt22" class="tgtSentence">Same as <legacyBold>adXactCursorStability</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="31ab7cd6f53288c0dc746e4c45a6f449" id="tgt23" class="tgtSentence">adXactRepeatableRead</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="297ce0b3c836ae307023d7c2c3a7b1ec" id="tgt24" class="tgtSentence">65536</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a80e1053be189ac76792763795e5d4df" id="tgt25" class="tgtSentence">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="a1df038de8a593a93e082513e198510a" id="tgt26" class="tgtSentence">adXactIsolated</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d28a0516bcf63a800bda4f18f5ad2e6" id="tgt27" class="tgtSentence">1048576</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="450eade994c99c4a40af2807844f9830" id="tgt28" class="tgtSentence">Indicates that transactions are conducted in isolation of other transactions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="a3511d36c9e8749a161f970d822b6be3" id="tgt29" class="tgtSentence">adXactSerializable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d28a0516bcf63a800bda4f18f5ad2e6" id="tgt30" class="tgtSentence">1048576</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7cc25f89da8bc9aabc240fc2a338aaa6" id="tgt31" class="tgtSentence">Same as <legacyBold>adXactIsolated</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt32" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt33" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt34" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9886689068c712d5268878fd08636fa" id="tgt35" class="tgtSentence">AdoEnums.IsolationLevel.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b0dec62913b04bc40d896dc1979554cd" id="tgt36" class="tgtSentence">AdoEnums.IsolationLevel.CHAOS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="817ceb97c001b472924f09850e168e2c" id="tgt37" class="tgtSentence">AdoEnums.IsolationLevel.BROWSE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8fdfe0010420fc201703d311fa5d3172" id="tgt38" class="tgtSentence">AdoEnums.IsolationLevel.READUNCOMMITTED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d446e4ceae3749f95c22524a0304f39" id="tgt39" class="tgtSentence">AdoEnums.IsolationLevel.CURSORSTABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bb560713365802a5f0467a7ad8a4ef57" id="tgt40" class="tgtSentence">AdoEnums.IsolationLevel.READCOMMITTED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="15f46ac2320aaecb4e781cb5cfd982c2" id="tgt41" class="tgtSentence">AdoEnums.IsolationLevel.REPEATABLEREAD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b1fca58e0cf3143f2a21883c11258d32" id="tgt42" class="tgtSentence">AdoEnums.IsolationLevel.ISOLATED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b5c43fcd7a6ebb17ae206aaa4c6fe495" id="tgt43" class="tgtSentence">AdoEnums.IsolationLevel.SERIALIZABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt44" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ea84e4b2-fbf2-4eef-b9ce-796b22e21800">IsolationLevel Property</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the level of transaction isolation for a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
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
                  <legacyBold>
                    <caps:sentence id="src5" class="srcSentence">adXactUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src8" class="srcSentence">adXactChaos</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src11" class="srcSentence">adXactBrowse</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">256</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Indicates that from one transaction you can view uncommitted changes in other transactions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src14" class="srcSentence">adXactReadUncommitted</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">256</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Same as <legacyBold>adXactBrowse</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src17" class="srcSentence">adXactCursorStability</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">4096</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src20" class="srcSentence">adXactReadCommitted</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">4096</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Same as <legacyBold>adXactCursorStability</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src23" class="srcSentence">adXactRepeatableRead</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">65536</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src26" class="srcSentence">adXactIsolated</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">1048576</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">Indicates that transactions are conducted in isolation of other transactions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src29" class="srcSentence">adXactSerializable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">1048576</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Same as <legacyBold>adXactIsolated</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src32" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src33" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">AdoEnums.IsolationLevel.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">AdoEnums.IsolationLevel.CHAOS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">AdoEnums.IsolationLevel.BROWSE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">AdoEnums.IsolationLevel.READUNCOMMITTED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">AdoEnums.IsolationLevel.CURSORSTABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">AdoEnums.IsolationLevel.READCOMMITTED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">AdoEnums.IsolationLevel.REPEATABLEREAD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">AdoEnums.IsolationLevel.ISOLATED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">AdoEnums.IsolationLevel.SERIALIZABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src44" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ea84e4b2-fbf2-4eef-b9ce-796b22e21800">IsolationLevel Property</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
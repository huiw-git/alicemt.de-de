---
title: "CursorLocationEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: acb255ff-1734-4b70-89bb-aef862b4c63b
caps.latest.revision: 11
caps.handback.revision: 11
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
# CursorLocationEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ef0be5e775d6e0cf81a5925cdd91f528" id="tgt1" class="tgtSentence">Specifies the location of the cursor service.</caps:sentence>
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
                    <caps:sentence sentenceid="938a115a0c496e8091db16e0e35ef407" id="tgt5" class="tgtSentence">adUseClient</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt6" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9a261ae63a1d61c9d4012308194c5c2c" id="tgt7" class="tgtSentence">Uses client-side cursors supplied by a local cursor library.</caps:sentence>
                  <caps:sentence sentenceid="81b8ada712cab960b4e9d5f481d77672" id="tgt8" class="tgtSentence"> Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</caps:sentence>
                  <caps:sentence sentenceid="bb8b3136e8f6c422328b5f6c7eda0243" id="tgt9" class="tgtSentence"> For backward compatibility, the synonym <legacyBold>adUseClientBatch</legacyBold> is also supported.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8ff4798221904bd05855a70d7daf6c5f" id="tgt10" class="tgtSentence">adUseNone</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt11" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="548cdbb45071ef06eae3643df96325c1" id="tgt12" class="tgtSentence">Does not use cursor services.</caps:sentence>
                  <caps:sentence sentenceid="edbd135d04a914ccb9f8232beb9f3950" id="tgt13" class="tgtSentence"> (This constant is obsolete and appears solely for the sake of backward compatibility.)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="c6f93d1164149db0c7ed183ff91f0397" id="tgt14" class="tgtSentence">adUseServer</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt15" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt16" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="8195c2dbd295ccfb81ad2b5fd9da4a0d" id="tgt17" class="tgtSentence"> Uses cursors supplied by the data provider or driver.</caps:sentence>
                  <caps:sentence sentenceid="cb34782100985a0ea24953c0bc142904" id="tgt18" class="tgtSentence"> These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</caps:sentence>
                  <caps:sentence sentenceid="6d7ad8f3990f1ff1af03e0abc3bb58d0" id="tgt19" class="tgtSentence"> However, some features of the <link xlink:href="1ac3bd9b-2d45-4cc8-88ec-bd8a218cfb49">The Microsoft Cursor Service for OLE DB</link>, such as disassociated</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="a97e897806478e630816e28926eb82a9" id="tgt20" class="tgtSentence">
                    <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects, cannot be simulated with server-side cursors and these features will be unavailable with this setting.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt21" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt22" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt23" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d2bd55470d9e9aaba6149de77ab6ab5" id="tgt24" class="tgtSentence">AdoEnums.CursorLocation.CLIENT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3eb17ad87cdc62a6a62a17e1268e23fd" id="tgt25" class="tgtSentence">AdoEnums.CursorLocation.NONE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0c60bd6e49ae0a38ceb7bc7c72dcc2ba" id="tgt26" class="tgtSentence">AdoEnums.CursorLocation.SERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt27" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation Property</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the location of the cursor service.</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adUseClient</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Uses client-side cursors supplied by a local cursor library.</caps:sentence>
                  <caps:sentence id="src8" class="srcSentence"> Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> For backward compatibility, the synonym <legacyBold>adUseClientBatch</legacyBold> is also supported.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src10" class="srcSentence">adUseNone</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Does not use cursor services.</caps:sentence>
                  <caps:sentence id="src13" class="srcSentence"> (This constant is obsolete and appears solely for the sake of backward compatibility.)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src14" class="srcSentence">adUseServer</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> Uses cursors supplied by the data provider or driver.</caps:sentence>
                  <caps:sentence id="src18" class="srcSentence"> These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</caps:sentence>
                  <caps:sentence id="src19" class="srcSentence"> However, some features of the <link xlink:href="1ac3bd9b-2d45-4cc8-88ec-bd8a218cfb49">The Microsoft Cursor Service for OLE DB</link>, such as disassociated</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src20" class="srcSentence">
                    <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects, cannot be simulated with server-side cursors and these features will be unavailable with this setting.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src22" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">AdoEnums.CursorLocation.CLIENT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">AdoEnums.CursorLocation.NONE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">AdoEnums.CursorLocation.SERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation Property</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "CursorTypeEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ffc6e245-4471-42ae-84dd-e85bddfce983
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
# CursorTypeEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="13c69709a9ad5519426e50ed68111ebd" id="tgt1" class="tgtSentence">Specifies the type of cursor used in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
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
                    <caps:sentence sentenceid="dd3159b765db1230581855f821108fff" id="tgt5" class="tgtSentence">adOpenDynamic</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt6" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fd7f48b67e43ec04d176a73021877b9a" id="tgt7" class="tgtSentence">Uses a dynamic cursor.</caps:sentence>
                  <caps:sentence sentenceid="d31cac09a73fa5714abcd16958fa046d" id="tgt8" class="tgtSentence"> Additions, changes, and deletions by other users are visible, and all types of movement through the <legacyBold>Recordset</legacyBold> are allowed, except for bookmarks, if the provider doesn't support them.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="629274f70ace2c20070e33b1b130418a" id="tgt9" class="tgtSentence">adOpenForwardOnly</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt10" class="tgtSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt11" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="c2267666608847eb6583071f881b2b1c" id="tgt12" class="tgtSentence"> Uses a forward-only cursor.</caps:sentence>
                  <caps:sentence sentenceid="e0941442f37cd91b7f11fe97c1924c73" id="tgt13" class="tgtSentence"> Identical to a static cursor, except that you can only scroll forward through records.</caps:sentence>
                  <caps:sentence sentenceid="aacdf97f14ee89333162d85b5e86d557" id="tgt14" class="tgtSentence"> This improves performance when you need to make only one pass through a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="02a6f8f6d7741bd6e3492f65321a2d74" id="tgt15" class="tgtSentence">adOpenKeyset</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt16" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8fca58ddafe7ba5e23fceb93372f12fb" id="tgt17" class="tgtSentence">Uses a keyset cursor.</caps:sentence>
                  <caps:sentence sentenceid="cedb6c15813a3f842d72d389beed1b95" id="tgt18" class="tgtSentence"> Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="87929c4ef829f74fbbea4b06f4040f00" id="tgt19" class="tgtSentence"> Data changes by other users are still visible.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="a3e1578a2c48c601424f4577e6b7dd88" id="tgt20" class="tgtSentence">adOpenStatic</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt21" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="11474f567a965b0960e68122cb490f21" id="tgt22" class="tgtSentence">Uses a static cursor, which is a static copy of a set of records that you can use to find data or generate reports.</caps:sentence>
                  <caps:sentence sentenceid="b3b9ab1c6bc44f40e6db70b3757e2565" id="tgt23" class="tgtSentence"> Additions, changes, or deletions by other users are not visible.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="437946566b247afe8d9dd911c88a56e4" id="tgt24" class="tgtSentence">adOpenUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt25" class="tgtSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="237cc08b5e1400a94c0932ee695e514e" id="tgt26" class="tgtSentence">Does not specify the type of cursor.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt27" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt28" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt29" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a57597713286f03fdad3b7399ca81a49" id="tgt30" class="tgtSentence">AdoEnums.CursorType.DYNAMIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0f3e8ae4073b6de8da9a7c6118829f45" id="tgt31" class="tgtSentence">AdoEnums.CursorType.FORWARDONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ed27f1e9e7948f54f0033e70b4f97d89" id="tgt32" class="tgtSentence">AdoEnums.CursorType.KEYSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b36120133a930354f00fbab15de5b559" id="tgt33" class="tgtSentence">AdoEnums.CursorType.STATIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="15752e680887b6e61c0d9a3ade5401bb" id="tgt34" class="tgtSentence">AdoEnums.CursorType.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt35" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType Property</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the type of cursor used in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adOpenDynamic</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Uses a dynamic cursor.</caps:sentence>
                  <caps:sentence id="src8" class="srcSentence"> Additions, changes, and deletions by other users are visible, and all types of movement through the <legacyBold>Recordset</legacyBold> are allowed, except for bookmarks, if the provider doesn't support them.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src9" class="srcSentence">adOpenForwardOnly</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src12" class="srcSentence"> Uses a forward-only cursor.</caps:sentence>
                  <caps:sentence id="src13" class="srcSentence"> Identical to a static cursor, except that you can only scroll forward through records.</caps:sentence>
                  <caps:sentence id="src14" class="srcSentence"> This improves performance when you need to make only one pass through a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src15" class="srcSentence">adOpenKeyset</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Uses a keyset cursor.</caps:sentence>
                  <caps:sentence id="src18" class="srcSentence"> Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence id="src19" class="srcSentence"> Data changes by other users are still visible.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src20" class="srcSentence">adOpenStatic</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Uses a static cursor, which is a static copy of a set of records that you can use to find data or generate reports.</caps:sentence>
                  <caps:sentence id="src23" class="srcSentence"> Additions, changes, or deletions by other users are not visible.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src24" class="srcSentence">adOpenUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">Does not specify the type of cursor.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src28" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">AdoEnums.CursorType.DYNAMIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">AdoEnums.CursorType.FORWARDONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">AdoEnums.CursorType.KEYSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">AdoEnums.CursorType.STATIC</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">AdoEnums.CursorType.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src35" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType Property</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
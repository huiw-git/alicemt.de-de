---
title: "SeekEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f0ec0c92-8253-47c6-9a14-e5dbccbad219
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
# SeekEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e07081b90688b5828d6a5265231ee4b6" id="tgt1" class="tgtSentence">Specifies the type of <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek</legacyLink> to execute.</caps:sentence>
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
                    <caps:sentence sentenceid="441cea2f9e010a12161f048112cc01cd" id="tgt5" class="tgtSentence">adSeekFirstEQ</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt6" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8aed9eae653c4dfa45668c69b46fa85c" id="tgt7" class="tgtSentence">Seeks the first key equal to <legacyItalic>KeyValues</legacyItalic>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="a628e2bc481e92e0415c257892a880cf" id="tgt8" class="tgtSentence">adSeekLastEQ</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt9" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2721012c43a05e4bf03e540a00b00621" id="tgt10" class="tgtSentence">Seeks the last key equal to <legacyItalic>KeyValues</legacyItalic>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="85a4e443d046072871bfe6fa2bddfdc1" id="tgt11" class="tgtSentence">adSeekAfterEQ</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt12" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fb9d262e9f93fc21a9515c98e16ddf8a" id="tgt13" class="tgtSentence">Seeks either a key equal to <legacyItalic>KeyValues</legacyItalic> or just after where that match would have occurred.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="c4096b9f2e4e6deb147c50e80dcf47a9" id="tgt14" class="tgtSentence">adSeekAfter</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c9f0f895fb98ab9159f51fd0297e236d" id="tgt15" class="tgtSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2d4bf0d6681626cdb6c2a891c49655c8" id="tgt16" class="tgtSentence">Seeks a key just after where a match with <legacyItalic>KeyValues </legacyItalic>would have occurred.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="cf427ce74990f9c8e511444f5194a1be" id="tgt17" class="tgtSentence">adSeekBeforeEQ</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c74d97b01eae257e44aa9d5bade97baf" id="tgt18" class="tgtSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="79a9deeb303873fc50c3e3e9a2dab29f" id="tgt19" class="tgtSentence">Seeks either a key equal to <legacyItalic>KeyValues</legacyItalic>or just before where that match would have occurred.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8e9cea91f89272dd185d0dbbd1e4ea7a" id="tgt20" class="tgtSentence">adSeekBefore</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6364d3f0f495b6ab9dcf8d3b5c6e0b01" id="tgt21" class="tgtSentence">32</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e1b2ff883bd992b824df73841a66ad0b" id="tgt22" class="tgtSentence">Seeks a key just before where a match with <legacyItalic>KeyValues </legacyItalic>would have occurred.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt23" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt24" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt25" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e7db6e2c3c217055aefbcd8525e0ea66" id="tgt26" class="tgtSentence">AdoEnums.Seek.FIRSTEQ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="800e27db79da3fa254c9581a4c61d943" id="tgt27" class="tgtSentence">AdoEnums.Seek.LASTEQ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16572f9cfbb73e43c4ab3e6dde48a6e1" id="tgt28" class="tgtSentence">AdoEnums.Seek.AFTEREQ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11cfd42a70a183477d4d628a23b872ea" id="tgt29" class="tgtSentence">AdoEnums.Seek.AFTER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5582c1cd78ae00379694cbd2dabcdb09" id="tgt30" class="tgtSentence">AdoEnums.Seek.BEFOREEQ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fffafecaae43d0ea2f2d76ff105d702" id="tgt31" class="tgtSentence">AdoEnums.Seek.BEFORE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt32" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek Method</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the type of <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek</legacyLink> to execute.</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adSeekFirstEQ</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Seeks the first key equal to <legacyItalic>KeyValues</legacyItalic>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src8" class="srcSentence">adSeekLastEQ</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Seeks the last key equal to <legacyItalic>KeyValues</legacyItalic>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src11" class="srcSentence">adSeekAfterEQ</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Seeks either a key equal to <legacyItalic>KeyValues</legacyItalic> or just after where that match would have occurred.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src14" class="srcSentence">adSeekAfter</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Seeks a key just after where a match with <legacyItalic>KeyValues </legacyItalic>would have occurred.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src17" class="srcSentence">adSeekBeforeEQ</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Seeks either a key equal to <legacyItalic>KeyValues</legacyItalic>or just before where that match would have occurred.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src20" class="srcSentence">adSeekBefore</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">32</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Seeks a key just before where a match with <legacyItalic>KeyValues </legacyItalic>would have occurred.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src24" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">AdoEnums.Seek.FIRSTEQ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">AdoEnums.Seek.LASTEQ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">AdoEnums.Seek.AFTEREQ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">AdoEnums.Seek.AFTER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">AdoEnums.Seek.BEFOREEQ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">AdoEnums.Seek.BEFORE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src32" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek Method</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
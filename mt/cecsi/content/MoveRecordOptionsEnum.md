---
title: "MoveRecordOptionsEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f53c2ce4-1021-4a45-92b8-775e8bebad99
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
# MoveRecordOptionsEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f7606e1a63f9c69d0a55471edcec35dd" id="tgt1" class="tgtSentence">Specifies the behavior of the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord</legacyLink> method.</caps:sentence>
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
                    <caps:sentence sentenceid="7a4f5c4bf952a95327e5ec07790c08b8" id="tgt5" class="tgtSentence">adMoveUnspecified</caps:sentence>
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
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt7" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="40244c0ae7a942da0bb898f43b5d59fe" id="tgt8" class="tgtSentence"> Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1358bd1ea5404ee584bd3bd78abc17e7" id="tgt9" class="tgtSentence">adMoveOverWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt10" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ddb657ff99491b7f1c7135ae92c03c51" id="tgt11" class="tgtSentence">Overwrites the destination file or directory, even if it already exists.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="07220d3e7afbc271c486cbbc6aeeb342" id="tgt12" class="tgtSentence">adMoveDontUpdateLinks</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt13" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f6f1e5a484d5dd85f240235915f51823" id="tgt14" class="tgtSentence">Modifies the default behavior of <legacyBold>MoveRecord</legacyBold> method by not updating the hypertext links of the source <legacyBold>Record</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="04306271c79388006fb2f68359ae7eaa" id="tgt15" class="tgtSentence"> The default behavior depends on the capabilities of the provider.</caps:sentence>
                  <caps:sentence sentenceid="1d381370adcc5edd0d1365c5b796c726" id="tgt16" class="tgtSentence"> Move operation updates links if the provider is capable.</caps:sentence>
                  <caps:sentence sentenceid="f7065079a7b080f41693ec08ed72741b" id="tgt17" class="tgtSentence"> If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="23e25b153892f190937b97f937626dda" id="tgt18" class="tgtSentence">adMoveAllowEmulation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt19" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a2288b14b8529191022521b663676db5" id="tgt20" class="tgtSentence">Requests that the provider attempt to simulate the move (using download, upload, and delete operations).</caps:sentence>
                  <caps:sentence sentenceid="5d8050dddf9dfa3724cafaa427989813" id="tgt21" class="tgtSentence"> If the attempt to move the <legacyBold>Record</legacyBold> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt22" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2feceb55ab2f12074bf5420d2fcd6fc5" id="tgt23" class="tgtSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt24" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord Method</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the behavior of the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord</legacyLink> method.</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adMoveUnspecified</caps:sentence>
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
                  <caps:sentence id="src7" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src8" class="srcSentence"> Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src9" class="srcSentence">adMoveOverWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Overwrites the destination file or directory, even if it already exists.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src12" class="srcSentence">adMoveDontUpdateLinks</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Modifies the default behavior of <legacyBold>MoveRecord</legacyBold> method by not updating the hypertext links of the source <legacyBold>Record</legacyBold>.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> The default behavior depends on the capabilities of the provider.</caps:sentence>
                  <caps:sentence id="src16" class="srcSentence"> Move operation updates links if the provider is capable.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src18" class="srcSentence">adMoveAllowEmulation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Requests that the provider attempt to simulate the move (using download, upload, and delete operations).</caps:sentence>
                  <caps:sentence id="src21" class="srcSentence"> If the attempt to move the <legacyBold>Record</legacyBold> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src23" class="srcSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord Method</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
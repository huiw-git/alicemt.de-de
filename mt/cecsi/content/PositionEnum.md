---
title: "PositionEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e69af0a5-3405-4b72-9c6e-6b188ff746fd
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
# PositionEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="836e44518d80dc1f282d6b73a2874d80" id="tgt1" class="tgtSentence">Specifies the current position of the record pointer within a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
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
                  <caps:sentence sentenceid="a87317160c92d1f0a141dfe3080dcdc2" id="tgt5" class="tgtSentence">
                    <legacyBold>adPosBOF</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5d7b9adcbe1c629ec722529dd12e5129" id="tgt6" class="tgtSentence">-2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="43eed84cef08a8fb1224443e37ca9af5" id="tgt7" class="tgtSentence">Indicates that the current record pointer is at BOF (that is, the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> property is <legacyBold>True</legacyBold>).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0722092dd67b268269fcb2fa08d2c572" id="tgt8" class="tgtSentence">
                    <legacyBold>adPosEOF</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b3149ecea4628efd23d2f86e5a723472" id="tgt9" class="tgtSentence">-3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e21bab7a4da6adbe76b5bef6cad5a2b2" id="tgt10" class="tgtSentence">Indicates that the current record pointer is at EOF (that is, the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> property is <legacyBold>True</legacyBold>).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7f7f82e3d4ce0dba7c908a7ff0a34948" id="tgt11" class="tgtSentence">
                    <legacyBold>adPosUnknown</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt12" class="tgtSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="21a0c16bd611861a15605ab17b044801" id="tgt13" class="tgtSentence">Indicates that the <legacyBold>Recordset</legacyBold> is empty, the current position is unknown, or the provider does not support the <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> or <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink> property.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt14" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt15" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt16" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7767fff1e227009959d80b7c59b4daa0" id="tgt17" class="tgtSentence">AdoEnums.Position.BOF</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b501a210b8e25b863caeb9b97a8fbf9d" id="tgt18" class="tgtSentence">AdoEnums.Position.EOF</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4269160a4bb74497634ef7fafd9512d6" id="tgt19" class="tgtSentence">AdoEnums.Position.UNKNOWN</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt20" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition Property</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the current position of the record pointer within a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
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
                  <caps:sentence id="src5" class="srcSentence">
                    <legacyBold>adPosBOF</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">-2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Indicates that the current record pointer is at BOF (that is, the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> property is <legacyBold>True</legacyBold>).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">
                    <legacyBold>adPosEOF</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">-3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Indicates that the current record pointer is at EOF (that is, the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> property is <legacyBold>True</legacyBold>).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">
                    <legacyBold>adPosUnknown</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Indicates that the <legacyBold>Recordset</legacyBold> is empty, the current position is unknown, or the provider does not support the <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> or <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink> property.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">AdoEnums.Position.BOF</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">AdoEnums.Position.EOF</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">AdoEnums.Position.UNKNOWN</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition Property</link>
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
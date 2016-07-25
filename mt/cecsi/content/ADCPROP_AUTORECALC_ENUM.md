---
title: "ADCPROP_AUTORECALC_ENUM"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ded4f087-87b9-4efa-8026-bde53d3e9e8a
caps.latest.revision: 9
caps.handback.revision: 9
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
# ADCPROP_AUTORECALC_ENUM
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9893057ce96b99a5442d40f7e9761c69" id="tgt1" class="tgtSentence">Specifies when the <legacyLink xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">MSDataShape</legacyLink> provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b96834c1c2f5cd137e3665d37228fe0e" id="tgt2" class="tgtSentence">These constants are only used with the <legacyBold>MSDataShape</legacyBold> provider and the <legacyBold>Recordset</legacyBold> "<legacyBold>Auto Recalc</legacyBold>" dynamic property, which is referenced in the <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">ADO Dynamic Property Index</legacyLink> and documented in the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink> or <legacyLink xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</legacyLink> documentation.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt3" class="tgtSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt4" class="tgtSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt5" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="999ee1266c5c9d82183685edfcaacf26" id="tgt6" class="tgtSentence">
                    <legacyBold>adRecalcAlways</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt7" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt8" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="e8b703dfc79f25667c771a9076e4fbe1" id="tgt9" class="tgtSentence"> Recalculates whenever the <legacyBold>MSDataShape</legacyBold> provider determines values that the calculated columns depend upon have changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="fbfb30b64ccaa37225530fe5d76d6fae" id="tgt10" class="tgtSentence">
                    <legacyBold>adRecalcUpFront</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt11" class="tgtSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="700ec7addc645fc7048d8d78e8da0ff9" id="tgt12" class="tgtSentence">Calculates only when initially building the hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt13" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2feceb55ab2f12074bf5420d2fcd6fc5" id="tgt14" class="tgtSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Specifies when the <legacyLink xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">MSDataShape</legacyLink> provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">These constants are only used with the <legacyBold>MSDataShape</legacyBold> provider and the <legacyBold>Recordset</legacyBold> "<legacyBold>Auto Recalc</legacyBold>" dynamic property, which is referenced in the <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">ADO Dynamic Property Index</legacyLink> and documented in the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink> or <legacyLink xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</legacyLink> documentation.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">
                    <legacyBold>adRecalcAlways</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> Recalculates whenever the <legacyBold>MSDataShape</legacyBold> provider determines values that the calculated columns depend upon have changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">
                    <legacyBold>adRecalcUpFront</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Calculates only when initially building the hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
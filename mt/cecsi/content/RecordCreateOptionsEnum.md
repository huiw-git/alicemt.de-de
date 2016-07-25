---
title: "RecordCreateOptionsEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6d746670-0850-4065-9cd4-168dea1d3ea9
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
# RecordCreateOptionsEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="477ab0803026ea2763d9db2b6ee2206a" id="tgt1" class="tgtSentence">Specifies whether an existing <legacyBold>Record</legacyBold> should be opened or a new <legacyBold>Record</legacyBold> created for the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method.</caps:sentence>
          <caps:sentence sentenceid="4614f350c587bea521f4503285b7ba9d" id="tgt2" class="tgtSentence"> The values can be combined with an AND operator.</caps:sentence>
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
                  <legacyBold>
                    <caps:sentence sentenceid="bba096d295c461a7be3a6608e86a220a" id="tgt6" class="tgtSentence">adCreateCollection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f41b03f46687b6430a40b0d6624a472f" id="tgt7" class="tgtSentence">0x2000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="de588814527b62af4b7761f485c6f1f9" id="tgt8" class="tgtSentence">Creates a new <legacyBold>Record</legacyBold> at the node specified by <legacyItalic>Source</legacyItalic> parameter, instead of opening an existing <legacyBold>Record</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="fee58f28eadfc48843be0abf56ab2ff4" id="tgt9" class="tgtSentence"> If the source points to an existing node, then a run-time error occurs, unless <legacyBold>adCreateCollection</legacyBold> is combined with <legacyBold>adOpenIfExists</legacyBold> or <legacyBold>adCreateOverwrite</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="050c529773f0c70fca88671e6aef1375" id="tgt10" class="tgtSentence">adCreateNonCollection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt11" class="tgtSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a4ee781502ca41320ce5ff86e05eb515" id="tgt12" class="tgtSentence">Creates a new <legacyBold>Record</legacyBold> of type <legacyLink xlink:href="f557e537-015d-4ba7-8a41-a6f00b366a91">adSimpleRecord</legacyLink>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="048b1d028fcc63610e8ac78d1792d3af" id="tgt13" class="tgtSentence">adCreateOverwrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="468939a9b8dcf5f83a54d9dea4be60a2" id="tgt14" class="tgtSentence">0x4000000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2025e9ece6e94f04d296a345a7780d05" id="tgt15" class="tgtSentence">Modifies the creation flags <legacyBold>adCreateCollection</legacyBold>, <legacyBold>adCreateNonCollection</legacyBold>, and <legacyBold>adCreateStructDoc</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="a67667374ca6d02dab04bc42af7c8b2f" id="tgt16" class="tgtSentence"> When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <legacyBold>Record</legacyBold>, then the existing <legacyBold>Record</legacyBold> is overwritten and a new one is created in its place.</caps:sentence>
                  <caps:sentence sentenceid="3bbb73e86560554f6db566786401ec45" id="tgt17" class="tgtSentence"> This value cannot be used together with <legacyBold>adOpenIfExists</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="0527a67a177bdc39ba58ed53e1cf97c7" id="tgt18" class="tgtSentence">adCreateStructDoc</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b1c24d059a4f1a268581dc8942bce83a" id="tgt19" class="tgtSentence">0x80000000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bf4313f28ca6ece896771cd2cd0dded7" id="tgt20" class="tgtSentence">Creates a new <legacyBold>Record</legacyBold> of type <legacyLink xlink:href="f557e537-015d-4ba7-8a41-a6f00b366a91">adStructDoc</legacyLink>, instead of opening an existing <legacyBold>Record</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="dd3122d429e16dcd3b3b07abead29bd7" id="tgt21" class="tgtSentence">adFailIfNotExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt22" class="tgtSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt23" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="93e70943b64d2ced1d0ea6e33e5730cc" id="tgt24" class="tgtSentence"> Results in a run-time error if <legacyItalic>Source </legacyItalic>points to a non-existent node.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="04ce0239f85a8b2a4c01422c5e76b329" id="tgt25" class="tgtSentence">adOpenIfExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0296d013beadbb665bbaad8984206f3d" id="tgt26" class="tgtSentence">0x2000000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2025e9ece6e94f04d296a345a7780d05" id="tgt27" class="tgtSentence">Modifies the creation flags <legacyBold>adCreateCollection</legacyBold>, <legacyBold>adCreateNonCollection</legacyBold>, and <legacyBold>adCreateStructDoc</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="c9ae16412e319768beda72f5c242ddd2" id="tgt28" class="tgtSentence"> When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <legacyBold>Record</legacyBold> object, then the provider must open the existing <legacyBold>Record</legacyBold> instead of creating a new one.</caps:sentence>
                  <caps:sentence sentenceid="7da616ad59c261db1197ebde2713acf4" id="tgt29" class="tgtSentence"> This value cannot be used together with <legacyBold>adCreateOverwrite</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt30" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2feceb55ab2f12074bf5420d2fcd6fc5" id="tgt31" class="tgtSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt32" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies whether an existing <legacyBold>Record</legacyBold> should be opened or a new <legacyBold>Record</legacyBold> created for the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The values can be combined with an AND operator.</caps:sentence>
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
                  <legacyBold>
                    <caps:sentence id="src6" class="srcSentence">adCreateCollection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">0x2000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Creates a new <legacyBold>Record</legacyBold> at the node specified by <legacyItalic>Source</legacyItalic> parameter, instead of opening an existing <legacyBold>Record</legacyBold>.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> If the source points to an existing node, then a run-time error occurs, unless <legacyBold>adCreateCollection</legacyBold> is combined with <legacyBold>adOpenIfExists</legacyBold> or <legacyBold>adCreateOverwrite</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src10" class="srcSentence">adCreateNonCollection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Creates a new <legacyBold>Record</legacyBold> of type <legacyLink xlink:href="f557e537-015d-4ba7-8a41-a6f00b366a91">adSimpleRecord</legacyLink>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src13" class="srcSentence">adCreateOverwrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">0x4000000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Modifies the creation flags <legacyBold>adCreateCollection</legacyBold>, <legacyBold>adCreateNonCollection</legacyBold>, and <legacyBold>adCreateStructDoc</legacyBold>.</caps:sentence>
                  <caps:sentence id="src16" class="srcSentence"> When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <legacyBold>Record</legacyBold>, then the existing <legacyBold>Record</legacyBold> is overwritten and a new one is created in its place.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> This value cannot be used together with <legacyBold>adOpenIfExists</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src18" class="srcSentence">adCreateStructDoc</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">0x80000000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Creates a new <legacyBold>Record</legacyBold> of type <legacyLink xlink:href="f557e537-015d-4ba7-8a41-a6f00b366a91">adStructDoc</legacyLink>, instead of opening an existing <legacyBold>Record</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src21" class="srcSentence">adFailIfNotExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src24" class="srcSentence"> Results in a run-time error if <legacyItalic>Source </legacyItalic>points to a non-existent node.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src25" class="srcSentence">adOpenIfExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">0x2000000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Modifies the creation flags <legacyBold>adCreateCollection</legacyBold>, <legacyBold>adCreateNonCollection</legacyBold>, and <legacyBold>adCreateStructDoc</legacyBold>.</caps:sentence>
                  <caps:sentence id="src28" class="srcSentence"> When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <legacyBold>Record</legacyBold> object, then the provider must open the existing <legacyBold>Record</legacyBold> instead of creating a new one.</caps:sentence>
                  <caps:sentence id="src29" class="srcSentence"> This value cannot be used together with <legacyBold>adCreateOverwrite</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src30" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src31" class="srcSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src32" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
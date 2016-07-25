---
title: "ConnectOptionEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: bff07eeb-dee3-4e4e-9b2d-d56061ea744d
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
# ConnectOptionEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b7dbbcb0bb96a3159bdfefec465e7965" id="tgt1" class="tgtSentence">Specifies whether the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object should return after the connection is established (synchronously) or before (asynchronously).</caps:sentence>
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
                    <caps:sentence sentenceid="ff0e9043b62b844081d45a450e4a4b1d" id="tgt5" class="tgtSentence">adAsyncConnect</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c74d97b01eae257e44aa9d5bade97baf" id="tgt6" class="tgtSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5cd343a34f6fe3e5284191d462d474cb" id="tgt7" class="tgtSentence">Opens the connection asynchronously.</caps:sentence>
                  <caps:sentence sentenceid="fbbdc26c87debf6a4bae8cd8904395d4" id="tgt8" class="tgtSentence"> The <legacyLink xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">ConnectComplete</legacyLink> event may be used to determine when the connection is available.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="6c672791b201f16e6ef99d7ca5a07994" id="tgt9" class="tgtSentence">adConnectUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt10" class="tgtSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt11" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="295fcfffc5ca677c50106ab01e176008" id="tgt12" class="tgtSentence"> Opens the connection synchronously.</caps:sentence>
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
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt14" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt15" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be118a675b731e9a2ad5e7756f24241f" id="tgt16" class="tgtSentence">AdoEnums.ConnectOption.ASYNCCONNECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c573055417fa754d118968671a282b5" id="tgt17" class="tgtSentence">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt18" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies whether the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object should return after the connection is established (synchronously) or before (asynchronously).</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adAsyncConnect</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Opens the connection asynchronously.</caps:sentence>
                  <caps:sentence id="src8" class="srcSentence"> The <legacyLink xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">ConnectComplete</legacyLink> event may be used to determine when the connection is available.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src9" class="srcSentence">adConnectUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src12" class="srcSentence"> Opens the connection synchronously.</caps:sentence>
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
            <caps:sentence id="src14" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">AdoEnums.ConnectOption.ASYNCCONNECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src18" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
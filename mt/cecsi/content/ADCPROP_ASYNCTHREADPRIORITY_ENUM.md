---
title: "ADCPROP_ASYNCTHREADPRIORITY_ENUM"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f0965617-17d8-41e0-98d0-f824274735a6
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
# ADCPROP_ASYNCTHREADPRIORITY_ENUM
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="48a99afde97935a0736bfa9c28e13172" id="tgt1" class="tgtSentence">For an RDS <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, specifies the execution priority of the asynchronous thread that retrieves data.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="66509f13da80480de1b63ed33376affa" id="tgt2" class="tgtSentence">Use these constants with the <legacyBold>Recordset</legacyBold> "<legacyBold>Background Thread Priority</legacyBold>" dynamic property, which is referenced in the ADO-to-OLE DB Dynamic Property index and documented in the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink> documentation.</caps:sentence>
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
                  <caps:sentence sentenceid="d744780172bdf34bfc0e9598eb774886" id="tgt6" class="tgtSentence">
                    <legacyBold>adPriorityAboveNormal</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt7" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="805c39ad495cd86f2e01992121c653dd" id="tgt8" class="tgtSentence">Sets priority between normal and highest.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3b6319556f2f751210e397445bdcae1d" id="tgt9" class="tgtSentence">
                    <legacyBold>adPriorityBelowNormal</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt10" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c09f09d2800ab8fb140f829ca1ba466d" id="tgt11" class="tgtSentence">Sets priority between lowest and normal.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="38083a38b26a94a293c80e7fc55f72c5" id="tgt12" class="tgtSentence">
                    <legacyBold>adPriorityHighest</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e4da3b7fbbce2345d7772b0674a318d5" id="tgt13" class="tgtSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="24b4ff76e5f8affa4ce4a5def6b591c9" id="tgt14" class="tgtSentence">Sets priority to the highest possible.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b35f6ac4acd8d1ca609f31cf68072556" id="tgt15" class="tgtSentence">
                    <legacyBold>AdPriorityLowest</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt16" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="033d652b7c1f1d1c0c948ee0ad683f22" id="tgt17" class="tgtSentence">Sets priority to the lowest possible.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="33a4c77aeff8496fbcf7af9b640dd847" id="tgt18" class="tgtSentence">
                    <legacyBold>adPriorityNormal</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt19" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d0470deb4151af25de62ce1069567bda" id="tgt20" class="tgtSentence">Sets priority to normal.</caps:sentence>
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
                    <caps:sentence sentenceid="31bf5da7d232753c1a09b032a8d5d0b4" id="tgt24" class="tgtSentence">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="667771469c3688fc533bbdf656b01e01" id="tgt25" class="tgtSentence">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adff05581811d4d071a041649bd4a887" id="tgt26" class="tgtSentence">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bd1c9d3ad7fed956c7d62f648adfd216" id="tgt27" class="tgtSentence">AdoEnums.AdcPropAsyncThreadPriority.LOWEST </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7cbbae82051bf5adb776608749937160" id="tgt28" class="tgtSentence">AdoEnums.AdcPropAsyncThreadPriority.NORMAL </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">For an RDS <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, specifies the execution priority of the asynchronous thread that retrieves data.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Use these constants with the <legacyBold>Recordset</legacyBold> "<legacyBold>Background Thread Priority</legacyBold>" dynamic property, which is referenced in the ADO-to-OLE DB Dynamic Property index and documented in the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink> documentation.</caps:sentence>
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
                    <legacyBold>adPriorityAboveNormal</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Sets priority between normal and highest.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">
                    <legacyBold>adPriorityBelowNormal</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Sets priority between lowest and normal.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">
                    <legacyBold>adPriorityHighest</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Sets priority to the highest possible.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">
                    <legacyBold>AdPriorityLowest</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Sets priority to the lowest possible.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">
                    <legacyBold>adPriorityNormal</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Sets priority to normal.</caps:sentence>
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
                    <caps:sentence id="src24" class="srcSentence">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">AdoEnums.AdcPropAsyncThreadPriority.LOWEST </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">AdoEnums.AdcPropAsyncThreadPriority.NORMAL </caps:sentence>
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
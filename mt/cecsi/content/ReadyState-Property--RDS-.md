---
title: "ReadyState Property (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 5be75bc7-1171-4440-a37e-c8cc6b5cd865
caps.latest.revision: 13
caps.handback.revision: 13
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
# ReadyState Property (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4488876bd7aa6a5a8c34eff37df83f78" id="tgt1" class="tgtSentence">Indicates the progress of a <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl</legacyLink> object as it retrieves data into its <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt6" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4ca0eed7704c59ee631791c2e9159339" id="tgt7" class="tgtSentence">Sets or returns one of the following values.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt8" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt9" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="cfdba154db7e6215f1a24d2421da21f7" id="tgt10" class="tgtSentence">adcReadyStateLoaded</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78fd947b44a5d54549eccbdca90cf1cf" id="tgt11" class="tgtSentence">The current query is still executing and no rows have been fetched.</caps:sentence>
                    <caps:sentence sentenceid="fe876ca04c3762e658136b87c2741eae" id="tgt12" class="tgtSentence"> The <legacyBold>DataControl </legacyBold>object's <legacyBold>Recordset</legacyBold> is not available for use.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="785e941e93aeb58c8c4c5bcdcca58013" id="tgt13" class="tgtSentence">adcReadyStateInteractive</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a3edb42875be26469784118711745ac0" id="tgt14" class="tgtSentence">An initial set of rows retrieved by the current query has been stored in the <legacyBold>DataControl</legacyBold> object's <legacyBold>Recordset</legacyBold> and are available for use.</caps:sentence>
                    <caps:sentence sentenceid="8d3ba98402c0f0ea95c3f3b81ef5f930" id="tgt15" class="tgtSentence"> The remaining rows are still being fetched.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="23fc9a34c8634cdb8a2a06471f7900e0" id="tgt16" class="tgtSentence">adcReadyStateComplete</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="76041083f9cadfb047e6b1616fabfb48" id="tgt17" class="tgtSentence">All rows retrieved by the current query have been stored in the <legacyBold>DataControl</legacyBold> object's <legacyBold>Recordset</legacyBold> and are available for use.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d377f7a69eb69c97bda031ae49c85556" id="tgt18" class="tgtSentence">This state will also exist if an operation aborted due to an error, or if the <legacyBold>Recordset</legacyBold> object is not initialized.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="daa7a43089eedbb8f628ff04585e4d43" id="tgt19" class="tgtSentence">Each client-side executable file that uses these constants must provide declarations for them.</caps:sentence>
              <caps:sentence sentenceid="bcad0601757e1785b2146faf3893cf28" id="tgt20" class="tgtSentence"> You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the default installation folder for the RDS library.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e00a530e4961565959e73169b201e62f" id="tgt21" class="tgtSentence">Use the <legacyLink xlink:href="bf2ae3ac-bfe4-4709-b50a-ea7c282c3164">onReadyStateChange</legacyLink> event to monitor changes in the <legacyBold>ReadyState</legacyBold> property during an asynchronous query operation.</caps:sentence>
            <caps:sentence sentenceid="6a8b61bc19f2b5f063f22d216f9fcee0" id="tgt22" class="tgtSentence"> This is more efficient than periodically checking the value of the property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ec4fc82ae86eef5563e1b7b634d72c5e" id="tgt23" class="tgtSentence">If an error occurs during an asynchronous operation, the <legacyBold>ReadyState</legacyBold> property changes to <legacyBold>adcReadyStateComplete</legacyBold>, the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property changes from <legacyBold>adStateExecuting</legacyBold> to <legacyBold>adStateClosed</legacyBold>, and the <legacyBold>Recordset</legacyBold> object <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property remains <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt24" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e3e18da4-0511-4ece-a35d-699978bc28c6">VBScript Example</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the progress of a <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl</legacyLink> object as it retrieves data into its <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">Sets or returns one of the following values.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src10" class="srcSentence">adcReadyStateLoaded</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">The current query is still executing and no rows have been fetched.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> The <legacyBold>DataControl </legacyBold>object's <legacyBold>Recordset</legacyBold> is not available for use.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src13" class="srcSentence">adcReadyStateInteractive</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">An initial set of rows retrieved by the current query has been stored in the <legacyBold>DataControl</legacyBold> object's <legacyBold>Recordset</legacyBold> and are available for use.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> The remaining rows are still being fetched.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src16" class="srcSentence">adcReadyStateComplete</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">All rows retrieved by the current query have been stored in the <legacyBold>DataControl</legacyBold> object's <legacyBold>Recordset</legacyBold> and are available for use.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">This state will also exist if an operation aborted due to an error, or if the <legacyBold>Recordset</legacyBold> object is not initialized.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence id="src19" class="srcSentence">Each client-side executable file that uses these constants must provide declarations for them.</caps:sentence>
              <caps:sentence id="src20" class="srcSentence"> You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the default installation folder for the RDS library.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">Use the <legacyLink xlink:href="bf2ae3ac-bfe4-4709-b50a-ea7c282c3164">onReadyStateChange</legacyLink> event to monitor changes in the <legacyBold>ReadyState</legacyBold> property during an asynchronous query operation.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> This is more efficient than periodically checking the value of the property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">If an error occurs during an asynchronous operation, the <legacyBold>ReadyState</legacyBold> property changes to <legacyBold>adcReadyStateComplete</legacyBold>, the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property changes from <legacyBold>adStateExecuting</legacyBold> to <legacyBold>adStateClosed</legacyBold>, and the <legacyBold>Recordset</legacyBold> object <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property remains <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e3e18da4-0511-4ece-a35d-699978bc28c6">VBScript Example</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions Property (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
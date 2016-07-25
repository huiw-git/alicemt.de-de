---
title: "ExecuteOptions Property (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 62a4fd88-afc3-4f1f-b978-40710a30c4e9
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
# ExecuteOptions Property (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="66b34e5b6f2b187341b98b1c6aa3c1bf" id="tgt1" class="tgtSentence">Indicates whether asynchronous execution is enabled.</caps:sentence>
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
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt8" class="tgtSentence">Constant</caps:sentence>
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
                      <caps:sentence sentenceid="6debef663c1e36752b8f3b9cb2de92cb" id="tgt10" class="tgtSentence">adcExecSync</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="93011b4d18f349eb3d15a3cbfb489524" id="tgt11" class="tgtSentence">Executes the next refresh of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> synchronously.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82cd55001be072e5bf865bd16c8b3cdb" id="tgt12" class="tgtSentence">
                      <legacyBold>adcExecAsync</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt13" class="tgtSentence">Default.</caps:sentence>
                    <caps:sentence sentenceid="363b888c06028252abba3ee935e8bf7b" id="tgt14" class="tgtSentence"> Executes the next refresh of the <legacyBold>Recordset</legacyBold> asynchronously.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="06df185b4efbe1c9d6dcd25bfe3463e1" id="tgt15" class="tgtSentence">Each executable file that uses these constants must provide declarations for them.</caps:sentence>
              <caps:sentence sentenceid="7cd279a5018a48835389972ad003631d" id="tgt16" class="tgtSentence"> You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the default installation folder for the RDS library.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7c9dfd524a0258ce9a8ff7ef4d0b0433" id="tgt17" class="tgtSentence">If <legacyBold>ExecuteOptions</legacyBold> is set to <legacyBold>adcExecAsync</legacyBold>, then this asynchronously executes the next <legacyBold>Refresh</legacyBold> call on the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="54ebf15e12c57c852e9368c27409d81c" id="tgt18" class="tgtSentence">If you try to call <legacyLink xlink:href="3957197a-f543-4d6b-9e11-67a77c2063b7">Reset</legacyLink>, <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh</legacyLink>, <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges</legacyLink>, <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink>, or <legacyLink xlink:href="a29e3fb9-306d-497a-9a59-1856a914e5e9">Recordset</legacyLink> while another asynchronous operation that might change the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's <legacyBold>Recordset</legacyBold> is executing, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7a1f45cc6a9d138462668cd9663bc93b" id="tgt19" class="tgtSentence">If an error occurs during an asynchronous operation, the <legacyBold>RDS.DataControl</legacyBold> object's <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState</legacyLink> value changes from <legacyBold>adcReadyStateLoaded</legacyBold> to <legacyBold>adcReadyStateComplete</legacyBold>, and the <legacyBold>Recordset</legacyBold> property value remains <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt20" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="753a4a3d-0fba-40b8-86e7-50b34182ca69">VBScript Example</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates whether asynchronous execution is enabled.</caps:sentence>
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
                    <caps:sentence id="src8" class="srcSentence">Constant</caps:sentence>
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
                      <caps:sentence id="src10" class="srcSentence">adcExecSync</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Executes the next refresh of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> synchronously.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">
                      <legacyBold>adcExecAsync</legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Default.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> Executes the next refresh of the <legacyBold>Recordset</legacyBold> asynchronously.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence id="src15" class="srcSentence">Each executable file that uses these constants must provide declarations for them.</caps:sentence>
              <caps:sentence id="src16" class="srcSentence"> You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the default installation folder for the RDS library.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">If <legacyBold>ExecuteOptions</legacyBold> is set to <legacyBold>adcExecAsync</legacyBold>, then this asynchronously executes the next <legacyBold>Refresh</legacyBold> call on the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If you try to call <legacyLink xlink:href="3957197a-f543-4d6b-9e11-67a77c2063b7">Reset</legacyLink>, <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh</legacyLink>, <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges</legacyLink>, <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink>, or <legacyLink xlink:href="a29e3fb9-306d-497a-9a59-1856a914e5e9">Recordset</legacyLink> while another asynchronous operation that might change the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's <legacyBold>Recordset</legacyBold> is executing, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">If an error occurs during an asynchronous operation, the <legacyBold>RDS.DataControl</legacyBold> object's <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState</legacyLink> value changes from <legacyBold>adcReadyStateLoaded</legacyBold> to <legacyBold>adcReadyStateComplete</legacyBold>, and the <legacyBold>Recordset</legacyBold> property value remains <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="753a4a3d-0fba-40b8-86e7-50b34182ca69">VBScript Example</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "FetchOptions Property (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 7b2e254a-9354-4541-bc98-bb185276388f
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
# FetchOptions Property (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b5fe9c28d1d773e1ea267b403c271900" id="tgt1" class="tgtSentence">Indicates the type of asynchronous fetching.</caps:sentence>
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
          <caps:sentence sentenceid="70c2a55a1add6ab5667b13923844418d" id="tgt6" class="tgtSentence">Setting and Return Values</caps:sentence>
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
                      <caps:sentence sentenceid="4437db806a77bd4544e07b995bb01104" id="tgt10" class="tgtSentence">adcFetchUpFront</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1fb16f7a162dc6ae2247ca3814e50e05" id="tgt11" class="tgtSentence">All the records of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> are fetched before control is returned to the application.</caps:sentence>
                    <caps:sentence sentenceid="48f3bade069415576263b4c4fa24690a" id="tgt12" class="tgtSentence"> The complete <legacyBold>Recordset</legacyBold> is fetched before the application is allowed to do anything with it.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="aea313c7941a21c499b5bec79542d941" id="tgt13" class="tgtSentence">adcFetchBackground</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ebd89e2f7f6a97399d6ecb5445f1b869" id="tgt14" class="tgtSentence">Control can return to the application as soon as the first batch of records has been fetched.</caps:sentence>
                    <caps:sentence sentenceid="30c221bb9e6d88bdc6a8de19654379c4" id="tgt15" class="tgtSentence"> A subsequent read of the <legacyBold>Recordset</legacyBold> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="6f21b90f4ab93a7ece7218f369eeaa56" id="tgt16" class="tgtSentence">adcFetchAsync</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt17" class="tgtSentence">Default.</caps:sentence>
                    <caps:sentence sentenceid="54771a5e63ddff8d70a15b5a90047b35" id="tgt18" class="tgtSentence"> Control returns immediately to the application while records are fetched in the background.</caps:sentence>
                    <caps:sentence sentenceid="09aa5e46fb3742ea0d54e644f7db6aeb" id="tgt19" class="tgtSentence"> If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <legacyBold>Recordset</legacyBold> has been reached.</caps:sentence>
                    <caps:sentence sentenceid="9a2c74b2647194b628d143ff877ad12f" id="tgt20" class="tgtSentence"> For example, a call to <legacyLink xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveLast</legacyLink> will move the current record position to the last record actually fetched, even though more records will continue to populate the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="daa7a43089eedbb8f628ff04585e4d43" id="tgt21" class="tgtSentence">Each client-side executable file that uses these constants must provide declarations for them.</caps:sentence>
              <caps:sentence sentenceid="bcad0601757e1785b2146faf3893cf28" id="tgt22" class="tgtSentence"> You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the default installation folder for the RDS library.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d2db6cbced34146d0cd355f499f4120f" id="tgt23" class="tgtSentence">In a Web application, you will usually want to use <legacyBold>adcFetchAsync</legacyBold> (the default value), because it provides better performance.</caps:sentence>
            <caps:sentence sentenceid="59a67e198f963692029ca1cbaf8fda21" id="tgt24" class="tgtSentence"> In a compiled client application, you will usually want to use <legacyBold>adcFetchBackground</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt25" class="tgtSentence">Applies To</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Indicates the type of asynchronous fetching.</caps:sentence>
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
          <caps:sentence id="src6" class="srcSentence">Setting and Return Values</caps:sentence>
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
                      <caps:sentence id="src10" class="srcSentence">adcFetchUpFront</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">All the records of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> are fetched before control is returned to the application.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> The complete <legacyBold>Recordset</legacyBold> is fetched before the application is allowed to do anything with it.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src13" class="srcSentence">adcFetchBackground</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Control can return to the application as soon as the first batch of records has been fetched.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> A subsequent read of the <legacyBold>Recordset</legacyBold> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src16" class="srcSentence">adcFetchAsync</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Default.</caps:sentence>
                    <caps:sentence id="src18" class="srcSentence"> Control returns immediately to the application while records are fetched in the background.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <legacyBold>Recordset</legacyBold> has been reached.</caps:sentence>
                    <caps:sentence id="src20" class="srcSentence"> For example, a call to <legacyLink xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveLast</legacyLink> will move the current record position to the last record actually fetched, even though more records will continue to populate the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence id="src21" class="srcSentence">Each client-side executable file that uses these constants must provide declarations for them.</caps:sentence>
              <caps:sentence id="src22" class="srcSentence"> You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the default installation folder for the RDS library.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src23" class="srcSentence">In a Web application, you will usually want to use <legacyBold>adcFetchAsync</legacyBold> (the default value), because it provides better performance.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> In a compiled client application, you will usually want to use <legacyBold>adcFetchBackground</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src25" class="srcSentence">Applies To</caps:sentence>
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
---
title: "RDS Properties"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4e04cbd-21fc-44a1-9f21-49aa68746934
caps.latest.revision: 12
caps.handback.revision: 12
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
# RDS Properties
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerOrientationDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt1" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt2" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt3" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt4" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e46da445319d0f9a00f76e8adbd30cc7" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8e451d7388e496b57de8c5267d3b5a5b" id="tgt6" class="tgtSentence">Indicates the database name from which the query and update operations are run.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9a100ff7899d66e1f7e9d26613d19462" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="66b34e5b6f2b187341b98b1c6aa3c1bf" id="tgt8" class="tgtSentence">Indicates whether asynchronous execution is enabled.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="da8ecdb9fc42f3613f3ead948bd39f46" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b5fe9c28d1d773e1ea267b403c271900" id="tgt10" class="tgtSentence">Indicates the type of asynchronous fetching.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="1bb5ab44d73e9601bab3de5be8fa1963" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="0a5473e8-8ce6-4518-83fb-4920b827e285">FilterColumn (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2397e523633cd9655b985e4d030b0483" id="tgt12" class="tgtSentence">Indicates the column on which to evaluate the filter criteria.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2ba8547f890ac7133871b075d20ac244" id="tgt13" class="tgtSentence">             <legacyLink xlink:href="24eb03ba-ccfd-4353-b6af-03586b2da6fd">FilterCriterion (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a0390903b425f3dfae50c15afc526565" id="tgt14" class="tgtSentence">Indicates the evaluation operator to use in the filter value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="12694d8f68095495335fa29a60db0c8f" id="tgt15" class="tgtSentence">             <legacyLink xlink:href="28f17186-b842-4cf9-b320-a9bb941c481b">FilterValue (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9f1c090e8c2cdb607b8938764f328b7a" id="tgt16" class="tgtSentence">Indicates the value to filter records.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="1f5dabf1c3a9d9de644e103971a5df65" id="tgt17" class="tgtSentence">             <legacyLink xlink:href="fdc34362-6d47-4727-b171-8d033159408e">Handler (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a92b0a14616c8db862b04017e932ee8f" id="tgt18" class="tgtSentence">Indicates the name of a server-side customization program (<legacyItalic>handler</legacyItalic>) that extends the functionality of the <legacyBold>RDSServer.DataFactory</legacyBold>, and any parameters used by the <legacyItalic>handler</legacyItalic>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e734cf62a5cedf6a195b668cdc3b1ecf" id="tgt19" class="tgtSentence">             <legacyLink xlink:href="4d1c8892-4bbc-4e71-bf4b-ba52c0ea9549">InternetTimeout (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2e20e00ef7e14e4bb1125d0d4f6278b3" id="tgt20" class="tgtSentence">Indicates the number of milliseconds to wait before a request times out.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="974c179a23c2a446d151a636b89d106f" id="tgt21" class="tgtSentence">             <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="585dc41e113b44a680bc67ac6fd1cdc3" id="tgt22" class="tgtSentence">Indicates the progress of a <legacyBold>DataControl</legacyBold> object as it fetches data into its <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="02406fbb539126c38a02e1f7ea7ece38" id="tgt23" class="tgtSentence">             <legacyLink xlink:href="a29e3fb9-306d-497a-9a59-1856a914e5e9">Recordset and SourceRecordset (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f597695e48568e76d6aceef07ea9044a" id="tgt24" class="tgtSentence">Indicates the <legacyBold>Recordset</legacyBold> object returned from a custom business object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="69b179dd7f2f7acb3ae103cce9e4ffa4" id="tgt25" class="tgtSentence">             <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d83384173b7083a80591fa427e48f892" id="tgt26" class="tgtSentence">Indicates the Internet Information Services (IIS) name and communication protocol.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="07a5916c133549693703d67dfe8c97f1" id="tgt27" class="tgtSentence">             <legacyLink xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="15e09159a2692eaa90a5d370554a3b34" id="tgt28" class="tgtSentence">Indicates by which column to sort the records.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3bfee90b228bfbabf0b6d08f6d3ab562" id="tgt29" class="tgtSentence">             <legacyLink xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="36a7e86405b22bbd9c5d16af2bd13f7b" id="tgt30" class="tgtSentence">Indicates whether a sort order is ascending or descending.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7817fac68c43dd6bbeb1a7f4fbf4a275" id="tgt31" class="tgtSentence">             <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6babf4da702c13ee573da41a0efb8055" id="tgt32" class="tgtSentence">Indicates the query string used to retrieve the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c92268ea60d290c11cade7b8efe1be6e" id="tgt33" class="tgtSentence">             <legacyLink xlink:href="8c56b233-1be8-442c-8d0e-a4c96465bc99">URL (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="514a720ff0a038e3fbdd4a415bb8bd88" id="tgt34" class="tgtSentence">Indicates a string that contains a relative or absolute URL.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerOrientationDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerOrientationDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Indicates the database name from which the query and update operations are run.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Indicates whether asynchronous execution is enabled.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Indicates the type of asynchronous fetching.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="0a5473e8-8ce6-4518-83fb-4920b827e285">FilterColumn (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Indicates the column on which to evaluate the filter criteria.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">             <legacyLink xlink:href="24eb03ba-ccfd-4353-b6af-03586b2da6fd">FilterCriterion (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Indicates the evaluation operator to use in the filter value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">             <legacyLink xlink:href="28f17186-b842-4cf9-b320-a9bb941c481b">FilterValue (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Indicates the value to filter records.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">             <legacyLink xlink:href="fdc34362-6d47-4727-b171-8d033159408e">Handler (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Indicates the name of a server-side customization program (<legacyItalic>handler</legacyItalic>) that extends the functionality of the <legacyBold>RDSServer.DataFactory</legacyBold>, and any parameters used by the <legacyItalic>handler</legacyItalic>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">             <legacyLink xlink:href="4d1c8892-4bbc-4e71-bf4b-ba52c0ea9549">InternetTimeout (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Indicates the number of milliseconds to wait before a request times out.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">             <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Indicates the progress of a <legacyBold>DataControl</legacyBold> object as it fetches data into its <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">             <legacyLink xlink:href="a29e3fb9-306d-497a-9a59-1856a914e5e9">Recordset and SourceRecordset (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Indicates the <legacyBold>Recordset</legacyBold> object returned from a custom business object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">             <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">Indicates the Internet Information Services (IIS) name and communication protocol.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">             <legacyLink xlink:href="f6f80f67-f0fb-4e63-a5f5-8fdf312aac63">SortColumn (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">Indicates by which column to sort the records.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">             <legacyLink xlink:href="1d9d8715-e4ad-4ff3-bf7f-f1dc0532d8c2">SortDirection (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Indicates whether a sort order is ascending or descending.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">             <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Indicates the query string used to retrieve the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">             <legacyLink xlink:href="8c56b233-1be8-442c-8d0e-a4c96465bc99">URL (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">Indicates a string that contains a relative or absolute URL.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerOrientationDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "RDS Methods"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c2c6af1a-3c44-4c9d-ad33-b381552c71af
caps.latest.revision: 14
caps.handback.revision: 14
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
# RDS Methods
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
                  <caps:sentence sentenceid="cd286704726b16657bee5645cf2fe0d4" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="77dac816e9afab97779cda8a243c6ef3" id="tgt6" class="tgtSentence">Cancels execution of a pending, asynchronous method call.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7a2f21eec55d7e086ded7c3caea448cd" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="72953f2eb0f32e866dcf60e153736cae" id="tgt8" class="tgtSentence">Cancels any changes made to the current or new row of a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="1aebd0c25f342686562821f48aa6d47e" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe">ConvertToString (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="aee45ac384947f48aad09327d1f7c526" id="tgt10" class="tgtSentence">Converts a <legacyBold>Recordset</legacyBold> to a MIME string that represents the recordset data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="70e3e689292e45b9935c08660030b92e" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3044ca97bc21c354c1fb2ef9d2c100cb" id="tgt12" class="tgtSentence">Creates the proxy for the target business object and returns a pointer to it.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="887cfbcefcdf44bc28794f4841a077bf" id="tgt13" class="tgtSentence">             <legacyLink xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d24f4cb1f6ec05ed0400cf8c6b3371ab" id="tgt14" class="tgtSentence">Creates an empty, disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="911bf75ef6542caa3ebe98d5f5a3823a" id="tgt15" class="tgtSentence">             <legacyLink xlink:href="2d9c30e9-ab5b-4920-91b8-48454c2fb5d8">Execute Method (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="83111389742a4da396906a86c32f02c0" id="tgt16" class="tgtSentence">Execute the request and create an advanced data rowset (for use with ADO 2.5 and later).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="db5fd51cba83569c18e72b8b6f87d29b" id="tgt17" class="tgtSentence">             <legacyLink xlink:href="9f131c8d-1497-416d-8209-abb481c38f7b">Execute21 Method (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c2c67f08cb46e6d877cc1e361cf9aedf" id="tgt18" class="tgtSentence">Execute the request and create an advanced data rowset (for use with ADO 2.1).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="ad45c676-ec7e-4a3a-9a6b-a54f75eb3012">InvokeService</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3c214402e67d208662dafc82f4752ce5" id="tgt19" class="tgtSentence">Returns a pointer to the requested interface on a more capable version of the object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="65eef3b52b7cf3467e4cec1bbb4044c4" id="tgt20" class="tgtSentence">             <legacyLink xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, MovePrevious (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c39d2ccc18ff879ab6d2be2318c921c3" id="tgt21" class="tgtSentence">Moves to the first, last, next, or previous record in a specified <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e94ed5db517c97eca7f520db52b0c3e3" id="tgt22" class="tgtSentence">             <legacyLink xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3055d4afcb8c4ddf39c3c2716b47e44b" id="tgt23" class="tgtSentence">Uses a valid SQL query string to return a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7392e73ef2c1eaff33d722a052b66dac" id="tgt24" class="tgtSentence">             <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5f450ea862e8c78103e4ad35c6156bd2" id="tgt25" class="tgtSentence">Requeries the data source specified in the <legacyBold>Connect</legacyBold> property and updates the query results.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="abd4f5bc7b22ea7ddf73b43ed0212f7e" id="tgt26" class="tgtSentence">             <legacyLink xlink:href="3957197a-f543-4d6b-9e11-67a77c2063b7">Reset (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0361801cd58dbf9ce24c1af4afd243ab" id="tgt27" class="tgtSentence">Executes the sort or filter on a client-side <legacyBold>Recordset</legacyBold>, based on the specified sort and filter properties.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4ed15a607030858200c23baffcd8004b" id="tgt28" class="tgtSentence">             <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f9ad27b9a73845d52da8fd2914506cd8" id="tgt29" class="tgtSentence">Submits pending changes of the locally cached and updatable <legacyBold>Recordset</legacyBold> to the data source specified in the <legacyBold>Connect</legacyBold> property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="1a787f975f46f616745431c47374e33c" id="tgt30" class="tgtSentence">             <legacyLink xlink:href="7af42866-7db2-4174-8251-388a2cf741f2">Synchronize Method (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4e4b332919376afe363b393e1e2390ac" id="tgt31" class="tgtSentence">Synchronize the given recordset with the database specified by the connection string (for use with ADO 2.5 and later).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e1d02a9b9c61535181d6381903400032" id="tgt32" class="tgtSentence">             <legacyLink xlink:href="6b35f136-9d9a-4bdd-8144-67decfd3c4e9">Synchronize21 Method (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="62a93a8e3e6ee068a2788ee01b958928" id="tgt33" class="tgtSentence">Synchronize the given recordset with the database specified by the connection string (for use with ADO 2.1).</caps:sentence>
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
                  <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Cancels execution of a pending, asynchronous method call.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Cancels any changes made to the current or new row of a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe">ConvertToString (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Converts a <legacyBold>Recordset</legacyBold> to a MIME string that represents the recordset data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Creates the proxy for the target business object and returns a pointer to it.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">             <legacyLink xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Creates an empty, disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">             <legacyLink xlink:href="2d9c30e9-ab5b-4920-91b8-48454c2fb5d8">Execute Method (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Execute the request and create an advanced data rowset (for use with ADO 2.5 and later).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">             <legacyLink xlink:href="9f131c8d-1497-416d-8209-abb481c38f7b">Execute21 Method (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Execute the request and create an advanced data rowset (for use with ADO 2.1).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="ad45c676-ec7e-4a3a-9a6b-a54f75eb3012">InvokeService</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Returns a pointer to the requested interface on a more capable version of the object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">             <legacyLink xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, MovePrevious (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Moves to the first, last, next, or previous record in a specified <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">             <legacyLink xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Uses a valid SQL query string to return a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">             <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Requeries the data source specified in the <legacyBold>Connect</legacyBold> property and updates the query results.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">             <legacyLink xlink:href="3957197a-f543-4d6b-9e11-67a77c2063b7">Reset (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Executes the sort or filter on a client-side <legacyBold>Recordset</legacyBold>, based on the specified sort and filter properties.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">             <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">Submits pending changes of the locally cached and updatable <legacyBold>Recordset</legacyBold> to the data source specified in the <legacyBold>Connect</legacyBold> property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">             <legacyLink xlink:href="7af42866-7db2-4174-8251-388a2cf741f2">Synchronize Method (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Synchronize the given recordset with the database specified by the connection string (for use with ADO 2.5 and later).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">             <legacyLink xlink:href="6b35f136-9d9a-4bdd-8144-67decfd3c4e9">Synchronize21 Method (RDS)</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Synchronize the given recordset with the database specified by the connection string (for use with ADO 2.1).</caps:sentence>
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
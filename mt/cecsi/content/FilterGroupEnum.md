---
title: "FilterGroupEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b22e725e-84bd-4286-a070-290c278c3783
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
# FilterGroupEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d54add50bc7f4ab85a3f678b6ccf7cdb" id="tgt1" class="tgtSentence">Specifies the group of records to be filtered from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
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
                    <caps:sentence sentenceid="1857773d7edaa9878930a931eaefcafd" id="tgt5" class="tgtSentence">adFilterAffectedRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt6" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e5ecbb917a86535b6840c235f3ec75e1" id="tgt7" class="tgtSentence">Filters for viewing only records affected by the last <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink>, <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> call.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="bbd31c5031fd1cff8356ecc5191887f8" id="tgt8" class="tgtSentence">adFilterConflictingRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e4da3b7fbbce2345d7772b0674a318d5" id="tgt9" class="tgtSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="83e8e3cc58970e86f91b20cd0093682b" id="tgt10" class="tgtSentence">Filters for viewing the records that failed the last batch update.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="765ec4835d56528d2c5080b7bc8ddc46" id="tgt11" class="tgtSentence">adFilterFetchedRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt12" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d820724d9c6d805185883a31b8a9eeee" id="tgt13" class="tgtSentence">Filters for viewing the records in the current cache—that is, the results of the last call to retrieve records from the database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="4b1682708d5c41379ca7659ee41f44be" id="tgt14" class="tgtSentence">adFilterNone</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt15" class="tgtSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="81d05a51f063816f8ccc4b006352c420" id="tgt16" class="tgtSentence">Removes the current filter and restores all records for viewing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="6def8421f6835fc4d92bf0904ea85c5f" id="tgt17" class="tgtSentence">adFilterPendingRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt18" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="aeb1fdc1f9791a49499ab760b28ebfcd" id="tgt19" class="tgtSentence">Filters for viewing only records that have changed but have not yet been sent to the server.</caps:sentence>
                  <caps:sentence sentenceid="6431ab163aa327a213f2bf0178c11263" id="tgt20" class="tgtSentence"> Applicable only for batch update mode.</caps:sentence>
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
                    <caps:sentence sentenceid="3f4b965128b94abf28958aba8f646da8" id="tgt24" class="tgtSentence">AdoEnums.FilterGroup.AFFECTEDRECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="851bacbc5a92cc7751e61891e36c9bb5" id="tgt25" class="tgtSentence">AdoEnums.FilterGroup.CONFLICTINGRECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3fcdd7a31e766bf3b9a2d813da1a2286" id="tgt26" class="tgtSentence">AdoEnums.FilterGroup.FETCHEDRECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d575b289b07df3d483c7bb11762a69d5" id="tgt27" class="tgtSentence">AdoEnums.FilterGroup.NONE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f38d9710d1941bcb39e53c6e47773538" id="tgt28" class="tgtSentence">AdoEnums.FilterGroup.PENDINGRECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt29" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the group of records to be filtered from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adFilterAffectedRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Filters for viewing only records affected by the last <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink>, <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> call.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src8" class="srcSentence">adFilterConflictingRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Filters for viewing the records that failed the last batch update.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src11" class="srcSentence">adFilterFetchedRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Filters for viewing the records in the current cache—that is, the results of the last call to retrieve records from the database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src14" class="srcSentence">adFilterNone</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Removes the current filter and restores all records for viewing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src17" class="srcSentence">adFilterPendingRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Filters for viewing only records that have changed but have not yet been sent to the server.</caps:sentence>
                  <caps:sentence id="src20" class="srcSentence"> Applicable only for batch update mode.</caps:sentence>
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
                    <caps:sentence id="src24" class="srcSentence">AdoEnums.FilterGroup.AFFECTEDRECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">AdoEnums.FilterGroup.CONFLICTINGRECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">AdoEnums.FilterGroup.FETCHEDRECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">AdoEnums.FilterGroup.NONE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">AdoEnums.FilterGroup.PENDINGRECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src29" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
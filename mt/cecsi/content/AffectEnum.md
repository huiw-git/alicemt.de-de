---
title: "AffectEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 1ab921a0-6c57-43b4-9291-701b2599f3e8
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
# AffectEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="06f399c4af59d53b225101fe022d0288" id="tgt1" class="tgtSentence">Specifies which records are affected by an operation.</caps:sentence>
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
                  <caps:sentence sentenceid="ae16a82e2560d032f513b6cdab70d1bd" id="tgt5" class="tgtSentence">
                    <legacyBold>adAffectAll</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt6" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f9ab507e0f854bcb95c0c02ffa0fdbf8" id="tgt7" class="tgtSentence">If there is not a <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> applied to the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, affects all records.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="4245d0fa23e5b298f350c745ae33dcbc" id="tgt8" class="tgtSentence">If the <unmanagedCodeEntityReference>Filter</unmanagedCodeEntityReference> property is set to a string criteria (such as "Author='Smith'"), then the operation affects visible records in the current chapter.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="c56f58c0ba5ac77db6c9d82ce02a9bb4" id="tgt9" class="tgtSentence">If the <unmanagedCodeEntityReference>Filter</unmanagedCodeEntityReference> property is set to a member of the <legacyLink xlink:href="b22e725e-84bd-4286-a070-290c278c3783">FilterGroupEnum</legacyLink> or an array of bookmarks, then the operation will affect all rows of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
                </para>
                <alert class="note">
                  <para>
                    <caps:sentence sentenceid="f8e552c752e6f369966f0766ae12dbde" id="tgt10" class="tgtSentence"> <legacyBold>adAffectAll</legacyBold> is hidden in the Visual Basic Object Browser.</caps:sentence>
                  </para>
                </alert>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="eab2ed259f25dba20adebdd904ea0912" id="tgt11" class="tgtSentence">
                    <legacyBold>adAffectAllChapters</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt12" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fdb960a0b21408d75925378783822d97" id="tgt13" class="tgtSentence">Affects all records in all sibling chapters of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, including those not visible via any <unmanagedCodeEntityReference>Filter</unmanagedCodeEntityReference> that is currently applied.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2227da3e27c1192055dbe08bff9a2ac8" id="tgt14" class="tgtSentence">adAffectCurrent</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt15" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d01db9623528d79afeb202f62769528c" id="tgt16" class="tgtSentence">Affects only the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="c2d6559bb78e37c081aaeeffc0eb6e42" id="tgt17" class="tgtSentence">adAffectGroup</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt18" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="42382e35b9614fb2e379e18813b743d3" id="tgt19" class="tgtSentence">Affects only records that satisfy the current <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property setting.</caps:sentence>
                  <caps:sentence sentenceid="5317b0bf9654d4ce5e2307cd47d7aa97" id="tgt20" class="tgtSentence"> You must set the <unmanagedCodeEntityReference>Filter</unmanagedCodeEntityReference> property to a <unmanagedCodeEntityReference>FilterGroupEnum</unmanagedCodeEntityReference> value or an array of <unmanagedCodeEntityReference>Bookmarks</unmanagedCodeEntityReference> to use this option.</caps:sentence>
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
                    <caps:sentence sentenceid="f94f1d1b376744cf84ca9aa975643795" id="tgt24" class="tgtSentence">AdoEnums.Affect.ALL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4eddeb1fcb991b13067faa949050909" id="tgt25" class="tgtSentence">AdoEnums.Affect.ALLCHAPTERS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e051089fe7f446bcf917d3692e3cfa57" id="tgt26" class="tgtSentence">AdoEnums.Affect.CURRENT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="36fbf912ca786b57599687b1aea3798c" id="tgt27" class="tgtSentence">AdoEnums.Affect.GROUP</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt28" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies which records are affected by an operation.</caps:sentence>
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
                  <caps:sentence id="src5" class="srcSentence">
                    <legacyBold>adAffectAll</legacyBold> </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">If there is not a <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> applied to the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, affects all records.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src8" class="srcSentence">If the <unmanagedCodeEntityReference>Filter</unmanagedCodeEntityReference> property is set to a string criteria (such as "Author='Smith'"), then the operation affects visible records in the current chapter.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src9" class="srcSentence">If the <unmanagedCodeEntityReference>Filter</unmanagedCodeEntityReference> property is set to a member of the <legacyLink xlink:href="b22e725e-84bd-4286-a070-290c278c3783">FilterGroupEnum</legacyLink> or an array of bookmarks, then the operation will affect all rows of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
                </para>
                <alert class="note">
                  <para>
                    <caps:sentence id="src10" class="srcSentence"> <legacyBold>adAffectAll</legacyBold> is hidden in the Visual Basic Object Browser.</caps:sentence>
                  </para>
                </alert>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">
                    <legacyBold>adAffectAllChapters</legacyBold>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Affects all records in all sibling chapters of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, including those not visible via any <unmanagedCodeEntityReference>Filter</unmanagedCodeEntityReference> that is currently applied.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src14" class="srcSentence">adAffectCurrent</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Affects only the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src17" class="srcSentence">adAffectGroup</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Affects only records that satisfy the current <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property setting.</caps:sentence>
                  <caps:sentence id="src20" class="srcSentence"> You must set the <unmanagedCodeEntityReference>Filter</unmanagedCodeEntityReference> property to a <unmanagedCodeEntityReference>FilterGroupEnum</unmanagedCodeEntityReference> value or an array of <unmanagedCodeEntityReference>Bookmarks</unmanagedCodeEntityReference> to use this option.</caps:sentence>
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
                    <caps:sentence id="src24" class="srcSentence">AdoEnums.Affect.ALL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">AdoEnums.Affect.ALLCHAPTERS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">AdoEnums.Affect.CURRENT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">AdoEnums.Affect.GROUP</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
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
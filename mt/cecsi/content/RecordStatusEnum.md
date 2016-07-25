---
title: "RecordStatusEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 506fdd70-4452-4e83-95d5-c94311988dfa
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
# RecordStatusEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2ffef141cdec61644cf692b512e6251b" id="tgt1" class="tgtSentence">Specifies the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">status</legacyLink> of a record with regard to batch updates and other bulk operations.</caps:sentence>
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
                    <caps:sentence sentenceid="135902a3e6c0276f935d31fedc4343a5" id="tgt5" class="tgtSentence">adRecCanceled</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c31ff34c5741f41aaab689b057de2aed" id="tgt6" class="tgtSentence">0x100</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c1ef444711fcfd2aa1c3c3e1a32ce677" id="tgt7" class="tgtSentence">Indicates that the record was not saved because the operation was canceled.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="877ff7fa6f7a35796462da5d61efc054" id="tgt8" class="tgtSentence">adRecCantRelease</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9c40b1bf1523fa0d7eb38ed802bb6d11" id="tgt9" class="tgtSentence">0x400</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9666a9053e0c9b20298cad401697c336" id="tgt10" class="tgtSentence">Indicates that the new record was not saved because the existing record was locked.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1ef7a2f251b6fdcf89d3e0c52cb04b1d" id="tgt11" class="tgtSentence">adRecConcurrencyViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e7bcf8b6b16031f77e27a07c581ce92b" id="tgt12" class="tgtSentence">0x800</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fc804aa4759d441e6e2ef464bd76c7ee" id="tgt13" class="tgtSentence">Indicates that the record was not saved because optimistic concurrency was in use.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="5187d51283694056de1adc281d409331" id="tgt14" class="tgtSentence">adRecDBDeleted</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="efd66904e73acaef7840c416afe41725" id="tgt15" class="tgtSentence">0x40000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4cabc4108509401d82b407800f118262" id="tgt16" class="tgtSentence">Indicates that the record has already been deleted from the data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="c63648deba989d0e30a7979e37da1414" id="tgt17" class="tgtSentence">adRecDeleted</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c59fa8ebbc79e63a41006d9cb98e468d" id="tgt18" class="tgtSentence">0x4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="13ac0e3f5604c73b037008b57e39022f" id="tgt19" class="tgtSentence">Indicates that the record was deleted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="17c396aa9abe16469cd8b09c9c7f51dc" id="tgt20" class="tgtSentence">adRecIntegrityViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="77176f38a4aeb7cbc5591c30e3536bc2" id="tgt21" class="tgtSentence">0x1000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9a97a557e87ed3092c3d9a62e12cd403" id="tgt22" class="tgtSentence">Indicates that the record was not saved because the user violated integrity constraints.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="852e8e3e931a18965c0cb3aadcfbff9c" id="tgt23" class="tgtSentence">adRecInvalid</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7f6a417be70d8c2743207d53badb5c83" id="tgt24" class="tgtSentence">0x10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6255754cbad104378a13ce165299dfb8" id="tgt25" class="tgtSentence">Indicates that the record was not saved because its bookmark is invalid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="15d6db37023aef1196d1df04236ebdd5" id="tgt26" class="tgtSentence">adRecMaxChangesExceeded</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f41b03f46687b6430a40b0d6624a472f" id="tgt27" class="tgtSentence">0x2000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="dab1d9b04c12a0db140d3573e50a8f5e" id="tgt28" class="tgtSentence">Indicates that the record was not saved because there were too many pending changes.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e297ecc2f260f221beb379e3660c29b8" id="tgt29" class="tgtSentence">adRecModified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="70f97d5da645a10e3dc2b005a86d2cd7" id="tgt30" class="tgtSentence">0x2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="03cbe9125d6fe3ee2548a49d11f21ea1" id="tgt31" class="tgtSentence">Indicates that the record was modified.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="d232741c67569981a573fc465a6de99f" id="tgt32" class="tgtSentence">adRecMultipleChanges</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b0723edc0cca12c5fa732c5e2df9cd90" id="tgt33" class="tgtSentence">0x40</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="12a8cea2f09e1fd3c4f38695e65fe47b" id="tgt34" class="tgtSentence">Indicates that the record was not saved because it would have affected multiple records.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="7eea314495a5c0306b9998491970d115" id="tgt35" class="tgtSentence">adRecNew</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0138b5d63d66121d8a6e680d23720fa7" id="tgt36" class="tgtSentence">0x1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="80b180ae08711f7b84cb6efab66b2328" id="tgt37" class="tgtSentence">Indicates that the record is new.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="d3eaed84cd02c00c143dd39710cef68b" id="tgt38" class="tgtSentence">adRecObjectOpen</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="53097f7414e99594ac5b8a15c3fc2fff" id="tgt39" class="tgtSentence">0x4000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fadeb55b728e6ada6b43d412d324d456" id="tgt40" class="tgtSentence">Indicates that the record was not saved because of a conflict with an open storage object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="57250c3202ee50244cda50e22bba0ea4" id="tgt41" class="tgtSentence">adRecOK</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt42" class="tgtSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2649324ca6bf1229be740377c7b75e98" id="tgt43" class="tgtSentence">Indicates that the record was successfully updated.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="d80ecd6bdd61bdf8c277bb1a31884f6d" id="tgt44" class="tgtSentence">adRecOutOfMemory</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2c19da7a85d14d73f4f3c32213fb3ce4" id="tgt45" class="tgtSentence">0x8000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="54d1aac1325b043805726d0e4c9dbdce" id="tgt46" class="tgtSentence">Indicates that the record was not saved because the computer has run out of memory.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="4a0d47b1a7fcad5b383411b43d848205" id="tgt47" class="tgtSentence">adRecPendingChanges</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="86339579fe78c05cb63c5eefc948bd77" id="tgt48" class="tgtSentence">0x80</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1706e02b0b1fb8577f489623e12dc58e" id="tgt49" class="tgtSentence">Indicates that the record was not saved because it refers to a pending insert.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="0a56f1b30d56133cb5522cfdffaa7639" id="tgt50" class="tgtSentence">adRecPermissionDenied</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d391cf999fd4648a0975af64a61802d" id="tgt51" class="tgtSentence">0x10000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8f440cffb10184812d022a2d32007b26" id="tgt52" class="tgtSentence">Indicates that the record was not saved because the user has insufficient permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="75866dcd3868311eec3bcaaba99ac921" id="tgt53" class="tgtSentence">adRecSchemaViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5a03448e3c97608b71324f913efa7b86" id="tgt54" class="tgtSentence">0x20000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5a4b9237df1edaee3952f2f40b6df26e" id="tgt55" class="tgtSentence">Indicates that the record was not saved because it violates the structure of the underlying database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2280f840cfcf2a14c3824aaaac4f1501" id="tgt56" class="tgtSentence">adRecUnmodified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b045dea7dac3110bf77b78932b0849ff" id="tgt57" class="tgtSentence">0x8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5194943ec58b17184214e3b80c1c2344" id="tgt58" class="tgtSentence">Indicates that the record was not modified.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt59" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="58447de3e2d138e0d6746ab13ae3e7e5" id="tgt60" class="tgtSentence">AdoEnums.RecordStatus.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt61" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt62" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a64e1892663680ad3bd7e70f39c52c67" id="tgt63" class="tgtSentence">AdoEnums.RecordStatus.CANCELED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="782c8214cc3f5ccdd89d3c85e915a3db" id="tgt64" class="tgtSentence">AdoEnums.RecordStatus.CANTRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d2b73d622810090f6d96ef7555fbeead" id="tgt65" class="tgtSentence">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a726ef7acc712baa87f00c297b6a46c7" id="tgt66" class="tgtSentence">AdoEnums.RecordStatus.DBDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7e49af40d5bbdffc3fe919eb152f75e7" id="tgt67" class="tgtSentence">AdoEnums.RecordStatus.DELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b4f987b8b45483f727e1747d5ba64df" id="tgt68" class="tgtSentence">AdoEnums.RecordStatus.INTEGRITYVIOLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="69ccce426ecb8836027f3ba3aa673375" id="tgt69" class="tgtSentence">AdoEnums.RecordStatus.INVALID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2f82c3a784fb9f75b2295e15dae9364d" id="tgt70" class="tgtSentence">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc9262aefbbde742b6212e7371e27983" id="tgt71" class="tgtSentence">AdoEnums.RecordStatus.MODIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75a0a906cf5266f988d89291c46644a2" id="tgt72" class="tgtSentence">AdoEnums.RecordStatus.MULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae05d4c9231d2e77801793bbc5de54ca" id="tgt73" class="tgtSentence">AdoEnums.RecordStatus.NEW</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b699368e96eb955f2f9a4dea9f33f957" id="tgt74" class="tgtSentence">AdoEnums.RecordStatus.OBJECTOPEN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6b37895b05cbcc9d5aa0bf1fbf4bcf3" id="tgt75" class="tgtSentence">AdoEnums.RecordStatus.OK</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7cc825464d0d24830673bd1539224a68" id="tgt76" class="tgtSentence">AdoEnums.RecordStatus.OUTOFMEMORY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2f6a677ac3d082d5adbed3f1d0fbc7b6" id="tgt77" class="tgtSentence">AdoEnums.RecordStatus.PENDINGCHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="132a233d98f182aacf7434a06a7f5987" id="tgt78" class="tgtSentence">AdoEnums.RecordStatus.PERMISSIONDENIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c22c9df8eb982aa836b5c16cee4e30bd" id="tgt79" class="tgtSentence">AdoEnums.RecordStatus.SCHEMAVIOLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7f1b30e8a30c4fb51acf43f9eb5a7f06" id="tgt80" class="tgtSentence">AdoEnums.RecordStatus.UNMODIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt81" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status Property (ADO Recordset)</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">status</legacyLink> of a record with regard to batch updates and other bulk operations.</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adRecCanceled</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">0x100</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Indicates that the record was not saved because the operation was canceled.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src8" class="srcSentence">adRecCantRelease</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">0x400</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Indicates that the new record was not saved because the existing record was locked.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src11" class="srcSentence">adRecConcurrencyViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">0x800</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Indicates that the record was not saved because optimistic concurrency was in use.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src14" class="srcSentence">adRecDBDeleted</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">0x40000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Indicates that the record has already been deleted from the data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src17" class="srcSentence">adRecDeleted</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">0x4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Indicates that the record was deleted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src20" class="srcSentence">adRecIntegrityViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">0x1000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Indicates that the record was not saved because the user violated integrity constraints.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src23" class="srcSentence">adRecInvalid</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">0x10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Indicates that the record was not saved because its bookmark is invalid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src26" class="srcSentence">adRecMaxChangesExceeded</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">0x2000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">Indicates that the record was not saved because there were too many pending changes.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src29" class="srcSentence">adRecModified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">0x2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Indicates that the record was modified.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src32" class="srcSentence">adRecMultipleChanges</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">0x40</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">Indicates that the record was not saved because it would have affected multiple records.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src35" class="srcSentence">adRecNew</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">0x1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Indicates that the record is new.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src38" class="srcSentence">adRecObjectOpen</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">0x4000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">Indicates that the record was not saved because of a conflict with an open storage object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src41" class="srcSentence">adRecOK</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">Indicates that the record was successfully updated.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src44" class="srcSentence">adRecOutOfMemory</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">0x8000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">Indicates that the record was not saved because the computer has run out of memory.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src47" class="srcSentence">adRecPendingChanges</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src48" class="srcSentence">0x80</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">Indicates that the record was not saved because it refers to a pending insert.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src50" class="srcSentence">adRecPermissionDenied</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src51" class="srcSentence">0x10000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">Indicates that the record was not saved because the user has insufficient permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src53" class="srcSentence">adRecSchemaViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">0x20000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">Indicates that the record was not saved because it violates the structure of the underlying database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src56" class="srcSentence">adRecUnmodified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">0x8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src58" class="srcSentence">Indicates that the record was not modified.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src59" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src60" class="srcSentence">AdoEnums.RecordStatus.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src61" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">AdoEnums.RecordStatus.CANCELED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">AdoEnums.RecordStatus.CANTRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">AdoEnums.RecordStatus.DBDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">AdoEnums.RecordStatus.DELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">AdoEnums.RecordStatus.INTEGRITYVIOLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">AdoEnums.RecordStatus.INVALID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">AdoEnums.RecordStatus.MODIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">AdoEnums.RecordStatus.MULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">AdoEnums.RecordStatus.NEW</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">AdoEnums.RecordStatus.OBJECTOPEN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">AdoEnums.RecordStatus.OK</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">AdoEnums.RecordStatus.OUTOFMEMORY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">AdoEnums.RecordStatus.PENDINGCHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">AdoEnums.RecordStatus.PERMISSIONDENIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">AdoEnums.RecordStatus.SCHEMAVIOLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">AdoEnums.RecordStatus.UNMODIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src81" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status Property (ADO Recordset)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "FieldStatusEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e06da1e2-303f-41b2-a3b0-61e233da152c
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
# FieldStatusEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9c80bea92133ca435f0a4268344f66f3" id="tgt1" class="tgtSentence">Specifies the <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">status</legacyLink> of a <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="97992dd7ae5548ec1fd6c7ab6a4186bf" id="tgt2" class="tgtSentence">The <legacyBold>adFieldPending*</legacyBold> values indicate the operation that caused the status to be set, and may be combined with other status values.</caps:sentence>
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
                  <legacyBold>
                    <caps:sentence sentenceid="2de80ae80f9bff784712a5851d622bff" id="tgt6" class="tgtSentence">adFieldAlreadyExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4e732ced3463d06de0ca9a15b6153677" id="tgt7" class="tgtSentence">26</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="217328a3240ae13f7c3f2d9e201a1cc4" id="tgt8" class="tgtSentence">Indicates that the specified field already exists.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3d7b4f4ec54bbb2da46814eb8155bc09" id="tgt9" class="tgtSentence">adFieldBadStatus</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c20ad4d76fe97759aa27a0c99bff6710" id="tgt10" class="tgtSentence">12</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2aaef0e66568028718eb281eef99cbaf" id="tgt11" class="tgtSentence">Indicates that an invalid status value was sent from ADO to the OLE DB provider.</caps:sentence>
                  <caps:sentence sentenceid="553a086cf8e2f2dd82d14afaed9c08c9" id="tgt12" class="tgtSentence"> Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> and <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status</legacyLink>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8d025eba4e3fda100f25c67131920700" id="tgt13" class="tgtSentence">adFieldCannotComplete</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="98f13708210194c475687be6106a3b84" id="tgt14" class="tgtSentence">20</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0ef8e591c5b4e8d5b87c14282c49baca" id="tgt15" class="tgtSentence">Indicates that the server of the URL specified by <legacyLink xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source</legacyLink> could not complete the operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="b6bc466b87ef18401248fb6ac8fa761d" id="tgt16" class="tgtSentence">adFieldCannotDeleteSource</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="37693cfc748049e45d87b8c7d8b9aacd" id="tgt17" class="tgtSentence">23</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f4aff880105688069f13efc2803633fc" id="tgt18" class="tgtSentence">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="9192adabe07456ce07960e43af87136b" id="tgt19" class="tgtSentence">adFieldCantConvertValue</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt20" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bde2b3df3a5a33471493b08d2332fc03" id="tgt21" class="tgtSentence">Indicates that the field cannot be retrieved or stored without loss of data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="213f61b411a6e7834bf44f7cf9dbed79" id="tgt22" class="tgtSentence">adFieldCantCreate</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8f14e45fceea167a5a36dedd4bea2543" id="tgt23" class="tgtSentence">7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="414ac1db99291a6c7052bc15a4b0341f" id="tgt24" class="tgtSentence">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="a1f9acc8efa559f14970b747f4633560" id="tgt25" class="tgtSentence">adFieldDataOverflow</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1679091c5a880faf6fb5e6087eb1b2dc" id="tgt26" class="tgtSentence">6</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7c576b90ac07bcf7e1fd9b5583ed3765" id="tgt27" class="tgtSentence">Indicates that the data returned from the provider overflowed the data type of the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="cb99106ed58fbd14c9270a39a7056dfb" id="tgt28" class="tgtSentence">adFieldDefault</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c51ce410c124a10e0db5e4b97fc2af39" id="tgt29" class="tgtSentence">13</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="669def5f60d47353e542c318d4425303" id="tgt30" class="tgtSentence">Indicates that the default value for the field was used when setting data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1151fc1f4f11b52d83c98f74d4c982ce" id="tgt31" class="tgtSentence">adFieldDoesNotExist</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c74d97b01eae257e44aa9d5bade97baf" id="tgt32" class="tgtSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9bef8de5031164ad54e3e95b1812ca1d" id="tgt33" class="tgtSentence">Indicates that the field specified does not exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="bfa207aaf434694ab62a7caf4ec0e761" id="tgt34" class="tgtSentence">adFieldIgnore</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9bf31c7ff062936a96d3c8bd1f8f2ff3" id="tgt35" class="tgtSentence">15</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0fc2f749250887556e1e240c4d7c8cc2" id="tgt36" class="tgtSentence">Indicates that this field was skipped when setting data values in the source.</caps:sentence>
                  <caps:sentence sentenceid="804887cffa81627ca02e703122174ac5" id="tgt37" class="tgtSentence"> The provider set no value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="c25d382dbdde1c71cd132bbcb7a6327d" id="tgt38" class="tgtSentence">adFieldIntegrityViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d3d9446802a44259755d38e6d163e820" id="tgt39" class="tgtSentence">10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bc2e45b03fb84d92f4323be023d680db" id="tgt40" class="tgtSentence">Indicates that the field cannot be modified because it is a calculated or derived entity.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="a52354527fee0b619093331a22b9ac03" id="tgt41" class="tgtSentence">adFieldInvalidURL</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="70efdf2ec9b086079795c442636b55fb" id="tgt42" class="tgtSentence">17</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="230b6efd22d4eef20076a6f54230c280" id="tgt43" class="tgtSentence">Indicates that the data source URL contains invalid characters.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="ba2f48c564dc50c0e94e4993ef0d1f39" id="tgt44" class="tgtSentence">adFieldIsNull</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt45" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9ce383f3fadb813dcf898d0b40818e0f" id="tgt46" class="tgtSentence">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="ac742e39b7489909bea78f7de66e9b0b" id="tgt47" class="tgtSentence">adFieldOK</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt48" class="tgtSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt49" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="ea0dcaa5ff8ac198d4a8071848ea5bf9" id="tgt50" class="tgtSentence"> Indicates that the field was successfully added or deleted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3d2a8b07bfb2401ad32a1c670a194570" id="tgt51" class="tgtSentence">adFieldOutOfSpace</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b6d767d2f8ed5d21a44b0e5886680cb9" id="tgt52" class="tgtSentence">22</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="39fb6e7c1b881de8abe9b088605291ff" id="tgt53" class="tgtSentence">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="634f530dfee8ebf57e4dff472a5c2f06" id="tgt54" class="tgtSentence">adFieldPendingChange</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="efd66904e73acaef7840c416afe41725" id="tgt55" class="tgtSentence">0x40000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0ac6eda1f3d027baaad13cd1f0347d63" id="tgt56" class="tgtSentence">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field which previously had a status of <legacyBold>adFieldOK</legacyBold> has changed.</caps:sentence>
                  <caps:sentence sentenceid="bcdd8c7e749dd0a97ab7926ca7e54ae7" id="tgt57" class="tgtSentence"> The final form of the field will modify the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection after the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method is called.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2e9275013b0a5340d4442d7e358477d5" id="tgt58" class="tgtSentence">adFieldPendingDelete</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5a03448e3c97608b71324f913efa7b86" id="tgt59" class="tgtSentence">0x20000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="84fdeab8d70e992c3fb8af32c08ed0ab" id="tgt60" class="tgtSentence">Indicates that the <legacyBold>Delete</legacyBold> operation caused the status to be set.</caps:sentence>
                  <caps:sentence sentenceid="4a7063be120b554d20261d9835000887" id="tgt61" class="tgtSentence"> The field has been marked for deletion from the <legacyBold>Fields</legacyBold> collection after the <legacyBold>Update</legacyBold> method is called.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1bf0fba38714f16b2b81407935951850" id="tgt62" class="tgtSentence">adFieldPendingInsert</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d391cf999fd4648a0975af64a61802d" id="tgt63" class="tgtSentence">0x10000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5980e272afce1fa8dc13c44953db03fd" id="tgt64" class="tgtSentence">Indicates that the <legacyBold>Append </legacyBold>operation caused the status to be set.</caps:sentence>
                  <caps:sentence sentenceid="26ed2a6877ec6242a89cc124547cc3ff" id="tgt65" class="tgtSentence"> The <legacyBold>Field</legacyBold> has been marked to be added to the <legacyBold>Fields</legacyBold> collection after the <legacyBold>Update</legacyBold> method is called.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2f02ba6fc3f7d3338e1b3f5c2ead3400" id="tgt66" class="tgtSentence">adFieldPendingUnknown</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="22131b63d911b93896cbb783aa61ce7e" id="tgt67" class="tgtSentence">0x80000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b69a93b29c99ee4e41e9e3d6106198c3" id="tgt68" class="tgtSentence">Indicates that the provider cannot determine what operation caused field status to be set.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="0a25069685b2ca027a6eaea6fa4607ed" id="tgt69" class="tgtSentence">adFieldPendingUnknownDelete</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9e3d286851aaf74d6829d5c4949fd5fd" id="tgt70" class="tgtSentence">0x100000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="55ca301527cde44d48fe7b6d015df405" id="tgt71" class="tgtSentence">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <legacyBold>Fields</legacyBold> collection after the <legacyBold>Update</legacyBold> method is called.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3c7120931e1e51477c89f11f2a1b0757" id="tgt72" class="tgtSentence">adFieldPermissionDenied</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="45c48cce2e2d7fbdea1afc51c7c6ad26" id="tgt73" class="tgtSentence">9</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="807b67fb80608aae0245012aaa59201c" id="tgt74" class="tgtSentence">Indicates that the field cannot be modified because it is defined as read-only.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="7020b4d44f5a06ce7578595d50c9321c" id="tgt75" class="tgtSentence">adFieldReadOnly</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1ff1de774005f8da13f42943881c655f" id="tgt76" class="tgtSentence">24</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="45db4e469e5e07b6e01fdef039df0399" id="tgt77" class="tgtSentence">Indicates that the field in the data source is defined as read-only.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e562d830d85a003e7b705bd90aaca471" id="tgt78" class="tgtSentence">adFieldResourceExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1f0e3dad99908345f7439f8ffabdffc4" id="tgt79" class="tgtSentence">19</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="17f606064d61d6de3f5658107c13cc86" id="tgt80" class="tgtSentence">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="575f9c3a240e36f4d53915726ac110de" id="tgt81" class="tgtSentence">adFieldResourceLocked</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6f4922f45568161a8cdf4ad2299f6d23" id="tgt82" class="tgtSentence">18</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e4d0bbfdac7eeff58988a6946eafab54" id="tgt83" class="tgtSentence">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="5cce0d9dd7cf60e99291191db37377a6" id="tgt84" class="tgtSentence">adFieldResourceOutOfScope</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8e296a067a37563370ded05f5a3bf3ec" id="tgt85" class="tgtSentence">25</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="18eec661761b4059ec656322bc981ff5" id="tgt86" class="tgtSentence">Indicates that a source or destination URL is outside the scope of the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="b6eefc728ddb465d711f504e21f074c5" id="tgt87" class="tgtSentence">adFieldSchemaViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6512bd43d9caa6e02c990b0a82652dca" id="tgt88" class="tgtSentence">11</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="23f7c4c3460606e034177fc292b8bd48" id="tgt89" class="tgtSentence">Indicates that the value violated the data source schema constraint for the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3b175b2fda2cfb9f63b4e8c7ec2e24d3" id="tgt90" class="tgtSentence">adFieldSignMismatch</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e4da3b7fbbce2345d7772b0674a318d5" id="tgt91" class="tgtSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7ca02b8af81caef3d023e147abb74e51" id="tgt92" class="tgtSentence">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="30f93eeb94631340498cf1f71a741108" id="tgt93" class="tgtSentence">adFieldTruncated</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt94" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9217039c72903eeb53f2c3aa4d5f2e96" id="tgt95" class="tgtSentence">Indicates that variable-length data was truncated when reading from the data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="9ae8c5219ff421ccefef8fa042b992f7" id="tgt96" class="tgtSentence">adFieldUnavailable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c9f0f895fb98ab9159f51fd0297e236d" id="tgt97" class="tgtSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="11915ead90aeaccdb68bb6d82e6ead92" id="tgt98" class="tgtSentence">Indicates that the provider could not determine the value when reading from the data source.</caps:sentence>
                  <caps:sentence sentenceid="ae0bb498cc11f67d91dcd510869a9946" id="tgt99" class="tgtSentence"> For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="6355ce9611504584f7e76aae260084d7" id="tgt100" class="tgtSentence">adFieldVolumeNotFound</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3c59dc048e8850243be8079a5c74d079" id="tgt101" class="tgtSentence">21</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1cec12974b40adb0c3b7b398af4a5944" id="tgt102" class="tgtSentence">Indicates that the provider is unable to locate the storage volume indicated by the URL.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt103" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2feceb55ab2f12074bf5420d2fcd6fc5" id="tgt104" class="tgtSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt105" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status Property (ADO Field)</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">status</legacyLink> of a <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">The <legacyBold>adFieldPending*</legacyBold> values indicate the operation that caused the status to be set, and may be combined with other status values.</caps:sentence>
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
                  <legacyBold>
                    <caps:sentence id="src6" class="srcSentence">adFieldAlreadyExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">26</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Indicates that the specified field already exists.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src9" class="srcSentence">adFieldBadStatus</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">12</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Indicates that an invalid status value was sent from ADO to the OLE DB provider.</caps:sentence>
                  <caps:sentence id="src12" class="srcSentence"> Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> and <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status</legacyLink>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src13" class="srcSentence">adFieldCannotComplete</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">20</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Indicates that the server of the URL specified by <legacyLink xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source</legacyLink> could not complete the operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src16" class="srcSentence">adFieldCannotDeleteSource</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">23</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src19" class="srcSentence">adFieldCantConvertValue</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Indicates that the field cannot be retrieved or stored without loss of data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src22" class="srcSentence">adFieldCantCreate</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src25" class="srcSentence">adFieldDataOverflow</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">6</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Indicates that the data returned from the provider overflowed the data type of the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src28" class="srcSentence">adFieldDefault</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">13</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Indicates that the default value for the field was used when setting data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src31" class="srcSentence">adFieldDoesNotExist</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Indicates that the field specified does not exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src34" class="srcSentence">adFieldIgnore</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">15</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">Indicates that this field was skipped when setting data values in the source.</caps:sentence>
                  <caps:sentence id="src37" class="srcSentence"> The provider set no value.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src38" class="srcSentence">adFieldIntegrityViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">Indicates that the field cannot be modified because it is a calculated or derived entity.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src41" class="srcSentence">adFieldInvalidURL</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">17</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">Indicates that the data source URL contains invalid characters.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src44" class="srcSentence">adFieldIsNull</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src47" class="srcSentence">adFieldOK</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src48" class="srcSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src50" class="srcSentence"> Indicates that the field was successfully added or deleted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src51" class="srcSentence">adFieldOutOfSpace</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">22</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src54" class="srcSentence">adFieldPendingChange</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">0x40000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field which previously had a status of <legacyBold>adFieldOK</legacyBold> has changed.</caps:sentence>
                  <caps:sentence id="src57" class="srcSentence"> The final form of the field will modify the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection after the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method is called.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src58" class="srcSentence">adFieldPendingDelete</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">0x20000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src60" class="srcSentence">Indicates that the <legacyBold>Delete</legacyBold> operation caused the status to be set.</caps:sentence>
                  <caps:sentence id="src61" class="srcSentence"> The field has been marked for deletion from the <legacyBold>Fields</legacyBold> collection after the <legacyBold>Update</legacyBold> method is called.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src62" class="srcSentence">adFieldPendingInsert</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src63" class="srcSentence">0x10000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src64" class="srcSentence">Indicates that the <legacyBold>Append </legacyBold>operation caused the status to be set.</caps:sentence>
                  <caps:sentence id="src65" class="srcSentence"> The <legacyBold>Field</legacyBold> has been marked to be added to the <legacyBold>Fields</legacyBold> collection after the <legacyBold>Update</legacyBold> method is called.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src66" class="srcSentence">adFieldPendingUnknown</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src67" class="srcSentence">0x80000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src68" class="srcSentence">Indicates that the provider cannot determine what operation caused field status to be set.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src69" class="srcSentence">adFieldPendingUnknownDelete</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src70" class="srcSentence">0x100000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src71" class="srcSentence">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <legacyBold>Fields</legacyBold> collection after the <legacyBold>Update</legacyBold> method is called.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src72" class="srcSentence">adFieldPermissionDenied</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src73" class="srcSentence">9</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src74" class="srcSentence">Indicates that the field cannot be modified because it is defined as read-only.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src75" class="srcSentence">adFieldReadOnly</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src76" class="srcSentence">24</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src77" class="srcSentence">Indicates that the field in the data source is defined as read-only.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src78" class="srcSentence">adFieldResourceExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src79" class="srcSentence">19</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src80" class="srcSentence">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src81" class="srcSentence">adFieldResourceLocked</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src82" class="srcSentence">18</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src83" class="srcSentence">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src84" class="srcSentence">adFieldResourceOutOfScope</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src85" class="srcSentence">25</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src86" class="srcSentence">Indicates that a source or destination URL is outside the scope of the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src87" class="srcSentence">adFieldSchemaViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src88" class="srcSentence">11</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src89" class="srcSentence">Indicates that the value violated the data source schema constraint for the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src90" class="srcSentence">adFieldSignMismatch</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src91" class="srcSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src92" class="srcSentence">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src93" class="srcSentence">adFieldTruncated</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src94" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src95" class="srcSentence">Indicates that variable-length data was truncated when reading from the data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src96" class="srcSentence">adFieldUnavailable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src97" class="srcSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src98" class="srcSentence">Indicates that the provider could not determine the value when reading from the data source.</caps:sentence>
                  <caps:sentence id="src99" class="srcSentence"> For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src100" class="srcSentence">adFieldVolumeNotFound</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src101" class="srcSentence">21</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src102" class="srcSentence">Indicates that the provider is unable to locate the storage volume indicated by the URL.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src103" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src104" class="srcSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src105" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status Property (ADO Field)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
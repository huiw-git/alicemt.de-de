---
title: "Field-Related Error Information"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5e7b1af4-996b-47c5-9161-c5575ad4fec9
caps.latest.revision: 3
caps.handback.revision: 3
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
# Field-Related Error Information
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c17c5cf6970c8be2dfb74146547f715d" id="tgt1" class="tgtSentence">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the <legacyBold>Field</legacyBold> object's <legacyBold>Status</legacyBold> property.</caps:sentence>
          <caps:sentence sentenceid="d79d954b9c37b88a2f1c2e94b594c24c" id="tgt2" class="tgtSentence"> This property has been enhanced to provide specific information about the problem.</caps:sentence>
          <caps:sentence sentenceid="fe8558d586eb25e489524743dd23ff29" id="tgt3" class="tgtSentence"> So, for example, when a call to <legacyBold>UpdateBatch</legacyBold> fails, the cause of the problem can be determined by examining the <legacyBold>Status</legacyBold> property of the <legacyBold>Fields</legacyBold> in each of the effected records.</caps:sentence>
          <caps:sentence sentenceid="0d256aa1a40730b46e94473b78b4adc3" id="tgt4" class="tgtSentence"> The property will contain one of the values in the <legacyBold>FieldStatusEnum</legacyBold> constant.</caps:sentence>
          <caps:sentence sentenceid="285856431f7f0545ce5c83cfdcabb93a" id="tgt5" class="tgtSentence"> The following table includes those values that are of particular interest when an error occurs.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt6" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt7" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt8" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9192adabe07456ce07960e43af87136b" id="tgt9" class="tgtSentence">adFieldCantConvertValue</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt10" class="tgtSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bde2b3df3a5a33471493b08d2332fc03" id="tgt11" class="tgtSentence">Indicates that the field cannot be retrieved or stored without loss of data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a1f9acc8efa559f14970b747f4633560" id="tgt12" class="tgtSentence">adFieldDataOverflow</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1679091c5a880faf6fb5e6087eb1b2dc" id="tgt13" class="tgtSentence">6</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c576b90ac07bcf7e1fd9b5583ed3765" id="tgt14" class="tgtSentence">Indicates that the data returned from the provider overflowed the data type of the field.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="cb99106ed58fbd14c9270a39a7056dfb" id="tgt15" class="tgtSentence">adFieldDefault</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c51ce410c124a10e0db5e4b97fc2af39" id="tgt16" class="tgtSentence">13</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="669def5f60d47353e542c318d4425303" id="tgt17" class="tgtSentence">Indicates that the default value for the field was used when setting data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="bfa207aaf434694ab62a7caf4ec0e761" id="tgt18" class="tgtSentence">adFieldIgnore</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9bf31c7ff062936a96d3c8bd1f8f2ff3" id="tgt19" class="tgtSentence">15</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0fc2f749250887556e1e240c4d7c8cc2" id="tgt20" class="tgtSentence">Indicates that this field was skipped when setting data values in the source.</caps:sentence>
                    <caps:sentence sentenceid="0f7bdd2dd1d497b740f9ddabc8343302" id="tgt21" class="tgtSentence"> No value was set by the provider.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="c25d382dbdde1c71cd132bbcb7a6327d" id="tgt22" class="tgtSentence">adFieldIntegrityViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3d9446802a44259755d38e6d163e820" id="tgt23" class="tgtSentence">10</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bc2e45b03fb84d92f4323be023d680db" id="tgt24" class="tgtSentence">Indicates that the field cannot be modified because it is a calculated or derived entity.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="ba2f48c564dc50c0e94e4993ef0d1f39" id="tgt25" class="tgtSentence">adFieldIsNull</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt26" class="tgtSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9aacb1c31ef26abb6b9971e910c02d71" id="tgt27" class="tgtSentence">Indicates that the provider returned a null value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3d2a8b07bfb2401ad32a1c670a194570" id="tgt28" class="tgtSentence">adFieldOutOfSpace</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b6d767d2f8ed5d21a44b0e5886680cb9" id="tgt29" class="tgtSentence">22</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39fb6e7c1b881de8abe9b088605291ff" id="tgt30" class="tgtSentence">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the <legacyBold>Field</legacyBold> object's <legacyBold>Status</legacyBold> property.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This property has been enhanced to provide specific information about the problem.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> So, for example, when a call to <legacyBold>UpdateBatch</legacyBold> fails, the cause of the problem can be determined by examining the <legacyBold>Status</legacyBold> property of the <legacyBold>Fields</legacyBold> in each of the effected records.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The property will contain one of the values in the <legacyBold>FieldStatusEnum</legacyBold> constant.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> The following table includes those values that are of particular interest when an error occurs.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src9" class="srcSentence">adFieldCantConvertValue</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Indicates that the field cannot be retrieved or stored without loss of data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src12" class="srcSentence">adFieldDataOverflow</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">6</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Indicates that the data returned from the provider overflowed the data type of the field.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src15" class="srcSentence">adFieldDefault</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">13</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Indicates that the default value for the field was used when setting data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src18" class="srcSentence">adFieldIgnore</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">15</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Indicates that this field was skipped when setting data values in the source.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> No value was set by the provider.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src22" class="srcSentence">adFieldIntegrityViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">10</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Indicates that the field cannot be modified because it is a calculated or derived entity.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src25" class="srcSentence">adFieldIsNull</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Indicates that the provider returned a null value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src28" class="srcSentence">adFieldOutOfSpace</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">22</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</caps:sentence>
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
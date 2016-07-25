---
title: "Cursor and Lock Characteristics"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 459c29cb-4230-42bf-8cc2-f3132ccc7aba
caps.latest.revision: 8
caps.handback.revision: 8
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
# Cursor and Lock Characteristics
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1ea6bd264e94449350324addbe05245f" id="tgt1" class="tgtSentence">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ecb3e5e2111962e0ba18e9e86df23617" id="tgt2" class="tgtSentence">Cursor or lock type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="faee742e2b3290f02a639a53e875a4a9" id="tgt3" class="tgtSentence">Advantages</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eee807afe84fa8929a981009cda95720" id="tgt4" class="tgtSentence">Disadvantages</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="629274f70ace2c20070e33b1b130418a" id="tgt5" class="tgtSentence">adOpenForwardOnly</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="610a03b8034715a7d3df4f9dba49b23c" id="tgt6" class="tgtSentence">Low resource requirements</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8c5c4722d9b2c08f2d3f786897bd7885" id="tgt7" class="tgtSentence">Cannot scroll backward</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="42a38d32c297f7e8c3886935d1d4f270" id="tgt8" class="tgtSentence">No data concurrency</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a3e1578a2c48c601424f4577e6b7dd88" id="tgt9" class="tgtSentence">adOpenStatic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3a61b62ba165c5935d2b35e5d4e25592" id="tgt10" class="tgtSentence">Scrollable</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="42a38d32c297f7e8c3886935d1d4f270" id="tgt11" class="tgtSentence">No data concurrency</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="02a6f8f6d7741bd6e3492f65321a2d74" id="tgt12" class="tgtSentence">adOpenKeyset</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ac77ca3307eed26f8a201e0ca214123e" id="tgt13" class="tgtSentence">Some data concurrency</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3a61b62ba165c5935d2b35e5d4e25592" id="tgt14" class="tgtSentence">Scrollable</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f725caf0c647546cdcd86539ef9b3397" id="tgt15" class="tgtSentence">Higher resource requirements</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2f3f4f5ce159ca646824ac4e783f48d9" id="tgt16" class="tgtSentence">Not available in disconnected scenario</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="dd3159b765db1230581855f821108fff" id="tgt17" class="tgtSentence">adOpenDynamic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="bea132f5f255e476d677be9887c235e8" id="tgt18" class="tgtSentence">High data concurrency</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3a61b62ba165c5935d2b35e5d4e25592" id="tgt19" class="tgtSentence">Scrollable</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="242964387b440e2f9aee5e143d6fe497" id="tgt20" class="tgtSentence">Highest resource requirements</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2f3f4f5ce159ca646824ac4e783f48d9" id="tgt21" class="tgtSentence">Not available in disconnected scenario</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="206b3571b04c113b4d0a4193a707efb2" id="tgt22" class="tgtSentence">adLockReadOnly</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="610a03b8034715a7d3df4f9dba49b23c" id="tgt23" class="tgtSentence">Low resource requirements</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="e5af810ec0d9c30c733fb632f2dc6063" id="tgt24" class="tgtSentence">Highly scalable</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f908c53578dfd412a25746a5371cfc43" id="tgt25" class="tgtSentence">Data not updatable through cursor</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="7ea6949dd6117ed20e65d11b751dce53" id="tgt26" class="tgtSentence">adLockBatchOptimistic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b639db90d1ca9024c880fe362c26f43c" id="tgt27" class="tgtSentence">Batch updates </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5e785e027815870b27b2effe66d09184" id="tgt28" class="tgtSentence">Allows disconnected scenarios</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="469ac784831d07f0d8c616fdd9ff6a52" id="tgt29" class="tgtSentence">Other users able to access data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d8617bce368af0b6dd4602db4cbf67b8" id="tgt30" class="tgtSentence">Data can be changed by multiple users at once</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a471c1dd4035ab5600e576bd780cf587" id="tgt31" class="tgtSentence">adLockPessimistic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a415ad25d0ddca0899a39a51d712820e" id="tgt32" class="tgtSentence">Data cannot be changed by other users while locked</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="46d300010bd365bbd6d91f8705c0ed7c" id="tgt33" class="tgtSentence">Prevents other users from accessing data while locked</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="95c61c35a284e29b0938d92a5bdf7803" id="tgt34" class="tgtSentence">adLockOptimistic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="469ac784831d07f0d8c616fdd9ff6a52" id="tgt35" class="tgtSentence">Other users able to access data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d8617bce368af0b6dd4602db4cbf67b8" id="tgt36" class="tgtSentence">Data can be changed by multiple users at once</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src2" class="srcSentence">Cursor or lock type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src3" class="srcSentence">Advantages</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">Disadvantages</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src5" class="srcSentence">adOpenForwardOnly</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src6" class="srcSentence">Low resource requirements</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src7" class="srcSentence">Cannot scroll backward</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src8" class="srcSentence">No data concurrency</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src9" class="srcSentence">adOpenStatic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src10" class="srcSentence">Scrollable</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src11" class="srcSentence">No data concurrency</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src12" class="srcSentence">adOpenKeyset</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">Some data concurrency</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">Scrollable</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">Higher resource requirements</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">Not available in disconnected scenario</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src17" class="srcSentence">adOpenDynamic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">High data concurrency</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">Scrollable</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">Highest resource requirements</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">Not available in disconnected scenario</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src22" class="srcSentence">adLockReadOnly</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">Low resource requirements</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src24" class="srcSentence">Highly scalable</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">Data not updatable through cursor</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src26" class="srcSentence">adLockBatchOptimistic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">Batch updates </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">Allows disconnected scenarios</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">Other users able to access data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">Data can be changed by multiple users at once</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src31" class="srcSentence">adLockPessimistic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">Data cannot be changed by other users while locked</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">Prevents other users from accessing data while locked</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src34" class="srcSentence">adLockOptimistic</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Other users able to access data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">Data can be changed by multiple users at once</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "EventStatusEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ebfd4cda-4017-4873-9d28-38b1c7db12a8
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
# EventStatusEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="207994c22dec15814b7ee4f04edfd92f" id="tgt1" class="tgtSentence">Specifies the current status of the execution of an event.</caps:sentence>
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
                    <caps:sentence sentenceid="a6fbefabf48fb6103f9d1e559830e502" id="tgt5" class="tgtSentence">adStatusCancel</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt6" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2c200b2478860f3246c0d137c0566a90" id="tgt7" class="tgtSentence">Requests cancellation of the operation that caused the event to occur.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1f0c5bcc52b8cbf247ba11d9c20f775e" id="tgt8" class="tgtSentence">adStatusCantDeny</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt9" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="89afde8accb202bd3a95fa5803a952d1" id="tgt10" class="tgtSentence">Indicates that the operation cannot request cancellation of the pending operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="87ba7c6bf305161a500f998f2204d0d9" id="tgt11" class="tgtSentence">adStatusErrorsOccurred</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt12" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="de10e506159040312e3ebaca9a957afb" id="tgt13" class="tgtSentence">Indicates that the operation that caused the event failed due to an error or errors.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="39ee47069a63fbab10f720490efa48af" id="tgt14" class="tgtSentence">adStatusOK</caps:sentence>
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
                  <caps:sentence sentenceid="4da779084a1139d3d96de3fbf907e41d" id="tgt16" class="tgtSentence">Indicates that the operation that caused the event was successful.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="425d2d59e2915d6f5ff65e209e5a1a97" id="tgt17" class="tgtSentence">adStatusUnwantedEvent</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e4da3b7fbbce2345d7772b0674a318d5" id="tgt18" class="tgtSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d3e3a6affea5f6cb1b9e1a396cf611eb" id="tgt19" class="tgtSentence">Prevents subsequent notifications before the event method has finished executing.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt20" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt21" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt22" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a1ad2df548698cb4314a4f0cae467df9" id="tgt23" class="tgtSentence">AdoEnums.EventStatus.CANCEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bb91cb14b133b2417920e07b0a0c3655" id="tgt24" class="tgtSentence">AdoEnums.EventStatus.CANTDENY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42a1a4febd48bbac3cfd3612f7475fde" id="tgt25" class="tgtSentence">AdoEnums.EventStatus.ERRORSOCCURRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04cb2545b9ff46c4231c93fe3cfff114" id="tgt26" class="tgtSentence">AdoEnums.EventStatus.OK</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fda5f7452776771c1163dfb8f5cec528" id="tgt27" class="tgtSentence">AdoEnums.EventStatus.UNWANTEDEVENT</caps:sentence>
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
                    <link xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">ConnectComplete and Disconnect Events</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="475de5e2-f634-4954-9edf-0027a6ba38d6">EndOfRecordset Event</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete Event</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="a28d3858-566c-468d-b070-d1de4339fbea">FetchComplete Event</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="468c87dd-e3bc-4084-9941-94d10743d4e9">InfoMessage Event</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField and FieldChangeComplete Events</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">WillChangeRecord and RecordChangeComplete Events</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset and RecordsetChangeComplete Events</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="da561d58-eb58-446c-a4fd-1838c76073c0">WillConnect Event</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="dd755e46-f589-48a3-93a9-51ff998d44b5">WillExecute Event</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove and MoveComplete Events</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies the current status of the execution of an event.</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adStatusCancel</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Requests cancellation of the operation that caused the event to occur.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src8" class="srcSentence">adStatusCantDeny</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Indicates that the operation cannot request cancellation of the pending operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src11" class="srcSentence">adStatusErrorsOccurred</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Indicates that the operation that caused the event failed due to an error or errors.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src14" class="srcSentence">adStatusOK</caps:sentence>
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
                  <caps:sentence id="src16" class="srcSentence">Indicates that the operation that caused the event was successful.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src17" class="srcSentence">adStatusUnwantedEvent</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Prevents subsequent notifications before the event method has finished executing.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">AdoEnums.EventStatus.CANCEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">AdoEnums.EventStatus.CANTDENY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">AdoEnums.EventStatus.ERRORSOCCURRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">AdoEnums.EventStatus.OK</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">AdoEnums.EventStatus.UNWANTEDEVENT</caps:sentence>
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
                    <link xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">ConnectComplete and Disconnect Events</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="475de5e2-f634-4954-9edf-0027a6ba38d6">EndOfRecordset Event</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete Event</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="a28d3858-566c-468d-b070-d1de4339fbea">FetchComplete Event</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="468c87dd-e3bc-4084-9941-94d10743d4e9">InfoMessage Event</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField and FieldChangeComplete Events</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">WillChangeRecord and RecordChangeComplete Events</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset and RecordsetChangeComplete Events</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="da561d58-eb58-446c-a4fd-1838c76073c0">WillConnect Event</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="dd755e46-f589-48a3-93a9-51ff998d44b5">WillExecute Event</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove and MoveComplete Events</link>
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
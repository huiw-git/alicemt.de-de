---
title: "Event Parameters"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bd5c5afa-d301-4899-acda-40f98a6afa4d
caps.latest.revision: 9
caps.handback.revision: 9
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
# Event Parameters
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5dbcda24a58882a573ca39552354d14f" id="tgt1" class="tgtSentence">Every event handler has a status parameter that controls the event handler.</caps:sentence>
          <caps:sentence sentenceid="9ddf5f42903073841e01d4742ac632fd" id="tgt2" class="tgtSentence"> For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event.</caps:sentence>
          <caps:sentence sentenceid="c5de01fb0143b3b640afbd8781b4de08" id="tgt3" class="tgtSentence"> Most Complete events also have an error parameter to provide information about any error that might have occurred, and one or more object parameters that refer to the ADO objects used to perform the operation.</caps:sentence>
          <caps:sentence sentenceid="29a46a62addab65cf7a174ff8893db60" id="tgt4" class="tgtSentence"> For example, the <legacyLink xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete</legacyLink> event includes object parameters for the <legacyBold>Command</legacyBold>, <legacyBold>Recordset</legacyBold>, and <legacyBold>Connection</legacyBold> objects associated with the event.</caps:sentence>
          <caps:sentence sentenceid="b7640dae251d9c7fcdb5e5d55e93a7f7" id="tgt5" class="tgtSentence"> In the following Microsoft® Visual Basic® example, you can see the pCommand, pRecordset, and pConnection objects which represent the <legacyBold>Command</legacyBold>, <legacyBold>Recordset</legacyBold>, and <legacyBold>Connection</legacyBold> objects that are used by the <legacyBold>Execute</legacyBold> method.</caps:sentence>
        </para>
        <code>Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _
     ByVal pError As ADODB.Error, _
     adStatus As ADODB.EventStatusEnum, _
     ByVal pCommand As ADODB.Command, _
     ByVal pRecordset As ADODB.Recordset, _
     ByVal pConnection As ADODB.Connection)</code>
        <para>
          <caps:sentence sentenceid="bd3f15566b75654fcd07ae7100ed7496" id="tgt6" class="tgtSentence">Except for the <legacyBold>Error </legacyBold>object, the same parameters are passed to the Will events.</caps:sentence>
          <caps:sentence sentenceid="6dcce6212679579cb4f55ee3dde3a083" id="tgt7" class="tgtSentence"> This lets you examine each of the objects that will be used in the pending operation and determine whether the operation should be allowed to finish.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="27ef15286dcc5adc0151486885fbab38" id="tgt8" class="tgtSentence">Some event handlers have a <legacyItalic>Reason</legacyItalic> parameter, which provides additional information about why the event occurred.</caps:sentence>
          <caps:sentence sentenceid="b1f827ac44d60f4cf6952bfddec2baa1" id="tgt9" class="tgtSentence"> For example, the <legacyBold>WillMove</legacyBold> and <legacyBold>MoveComplete</legacyBold> events can occur because of any one of the navigation methods (<legacyBold>MoveNext</legacyBold>, <legacyBold>MovePrevious</legacyBold>, and so on) being called or as the result of a requery.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="ba074da1846d2db05094f52469fdb20b" id="tgt10" class="tgtSentence">Status Parameter</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="95cf2590d762f6de71f0ece74df455c1" id="tgt11" class="tgtSentence">When the event-handler routine is called, the <legacyItalic>Status</legacyItalic> parameter is set to one of the following values.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt12" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt13" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae840d9a957983be5e79a16f9c573ba1" id="tgt14" class="tgtSentence">               <legacyBold>adStatusOK</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a8cca661b2b53c6b40ba94e29f156fad" id="tgt15" class="tgtSentence">Passed to both Will and Complete events.</caps:sentence>
                    <caps:sentence sentenceid="1df216c8135aac8bf8bf93233c3a7c92" id="tgt16" class="tgtSentence"> This value means that the operation that caused the event completed successfully.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0fbcde6c284dc63737629acf977b21f2" id="tgt17" class="tgtSentence">               <legacyBold>adStatusErrorsOccurred</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f9a0e5692019068c4a7f5d71a55255a" id="tgt18" class="tgtSentence">Passed to Complete events only.</caps:sentence>
                    <caps:sentence sentenceid="0b63a624321122d9eb423e9fe0d7c86a" id="tgt19" class="tgtSentence"> This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation.</caps:sentence>
                    <caps:sentence sentenceid="12b76013acc94b80c8dfdd38aeb94911" id="tgt20" class="tgtSentence"> Check the <legacyItalic>Error</legacyItalic> parameter for more details.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3d1fb11cc8ee4852ec1b7dd1d7e678b7" id="tgt21" class="tgtSentence">               <legacyBold>adStatusCantDeny</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="24efc14cdfed8eb80696936672976e8d" id="tgt22" class="tgtSentence">Passed to Will events only.</caps:sentence>
                    <caps:sentence sentenceid="e43d0904a15e5f6fff6843f9a460f1fd" id="tgt23" class="tgtSentence"> This value means that the operation cannot be canceled by the Will event.</caps:sentence>
                    <caps:sentence sentenceid="80c98b5f9fd1b797079526f1d90e8a62" id="tgt24" class="tgtSentence"> It must be performed.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="e0b6d1b15bf827a18cc3328ec537b963" id="tgt25" class="tgtSentence">If you determine in your Will event that the operation should continue, leave the <legacyItalic>Status</legacyItalic> parameter unchanged.</caps:sentence>
            <caps:sentence sentenceid="9a8b0edc039c9c2ff972f9dc58e3165b" id="tgt26" class="tgtSentence"> As long as the incoming status parameter was not set to <legacyBold>adStatusCantDeny</legacyBold>, however, you can cancel the pending operation by changing <legacyItalic>Status</legacyItalic> to <legacyBold>adStatusCancel</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="9fa4818f54e3d5642b772bf2f11600ce" id="tgt27" class="tgtSentence"> When you do this, the Complete event associated with the operation has its <legacyItalic>Status</legacyItalic> parameter set to <legacyBold>adStatusErrorsOccurred</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="7319331e492388d7db6adefe54bc1c63" id="tgt28" class="tgtSentence"> The <legacyBold>Error</legacyBold> object passed to the Complete event will contain the value <legacyBold>adErrOperationCancelled</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d73223d364dc04c3de24c3988bdb38f9" id="tgt29" class="tgtSentence">If you no longer want to process an event, you can set <legacyItalic>Status</legacyItalic> to <legacyBold>adStatusUnwantedEvent</legacyBold> and your application will no longer receive notification of that event.</caps:sentence>
            <caps:sentence sentenceid="e1cdbd45df69a6bfaa1e2efa0a6b2093" id="tgt30" class="tgtSentence"> However, remember that some events can be raised for more than one reason.</caps:sentence>
            <caps:sentence sentenceid="28df08e50dc678a898fa04a058849a4e" id="tgt31" class="tgtSentence"> In that case, you must specify <legacyBold>adStatusUnwantedEvent</legacyBold> for each possible reason.</caps:sentence>
            <caps:sentence sentenceid="1d94f3f0ebf2b4763f7ec0b71b7b34e2" id="tgt32" class="tgtSentence"> For example, to stop receiving notification of pending <legacyBold>RecordChange</legacyBold> events, you must set the <legacyItalic>Status</legacyItalic> parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> for <legacyBold>adRsnAddNew</legacyBold>, <legacyBold>adRsnDelete</legacyBold>, <legacyBold>adRsnUpdate</legacyBold>, <legacyBold>adRsnUndoUpdate</legacyBold>, <legacyBold>adRsnUndoAddNew</legacyBold>, <legacyBold>adRsnUndoDelete</legacyBold>, and <legacyBold>adRsnFirstChange</legacyBold> as they occur.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt33" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt34" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6dcecb87d765b26db58b41160fe8c658" id="tgt35" class="tgtSentence">               <legacyBold>adStatusUnwantedEvent</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b04f75d81e3e07c675fe520bc1e19e6f" id="tgt36" class="tgtSentence">Request that this event handler receive no further notifications.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1cf2ce4cc24fa1df4741741d35ecab2d" id="tgt37" class="tgtSentence">               <legacyBold>adStatusCancel</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="79fbf7082bfedeaa19e3266cbf7be0e8" id="tgt38" class="tgtSentence">Request cancellation of the operation that is about to occur.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="3b91dd973f2616ea65f4b1f75e64ddd2" id="tgt39" class="tgtSentence">Error Parameter</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6be43eb5cf7137cc867e5a57a60d4d4d" id="tgt40" class="tgtSentence">The <legacyItalic>Error</legacyItalic> parameter is a reference to an ADO <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="89adac332ebb27ee1ec2717b313c46e2" id="tgt41" class="tgtSentence"> When the <legacyItalic>Status</legacyItalic> parameter is set to <legacyBold>adStatusErrorsOccurred</legacyBold>, the <legacyBold>Error</legacyBold> object contains details about why the operation failed.</caps:sentence>
            <caps:sentence sentenceid="ea44fa85af90bf1acff62ffbdb9f951b" id="tgt42" class="tgtSentence"> If the Will event associated with a Complete event has canceled the operation by setting the <legacyItalic>Status</legacyItalic> parameter to <legacyBold>adStatusCancel</legacyBold>, the error object is always set to <legacyBold>adErrOperationCancelled</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="86e1729e6a5bb0737c1e872882869c02" id="tgt43" class="tgtSentence">Object Parameter</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e9b16ca72cbb658df55d517cd973ea3f" id="tgt44" class="tgtSentence">Each event receives one or more objects representing the objects that are involved in the operation.</caps:sentence>
            <caps:sentence sentenceid="a339954978aa9457c71be9b9093b534a" id="tgt45" class="tgtSentence"> For example, the <legacyBold>ExecuteComplete</legacyBold> event receives a <legacyBold>Command</legacyBold> object, a <legacyBold>Recordset</legacyBold> object, and a <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b6ef6da5130ec19de4d7da18f9baf47b" id="tgt46" class="tgtSentence">Reason Parameter</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b2f6bdda6b45a58619effe6b02464f69" id="tgt47" class="tgtSentence">The <legacyItalic>Reason</legacyItalic> parameter, <legacyItalic>adReason</legacyItalic>, provides additional information about why the event occurred.</caps:sentence>
            <caps:sentence sentenceid="5ba7db1ea1871878dd43c8999fdca947" id="tgt48" class="tgtSentence"> Events with an <legacyItalic>adReason</legacyItalic> parameter may be called several times, even for the same operation, for a different reason every time.</caps:sentence>
            <caps:sentence sentenceid="ea2e7761722fd8f9133a5e5b85a3226c" id="tgt49" class="tgtSentence"> For example, the <legacyBold>WillChangeRecord</legacyBold> event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</caps:sentence>
            <caps:sentence sentenceid="a9168d27d0f1900037ee98c713c1187b" id="tgt50" class="tgtSentence"> If you want to process an event only when it occurs for a particular reason, you can use the <legacyItalic>adReason</legacyItalic> parameter to filter out the occurrences you are not interested in.</caps:sentence>
            <caps:sentence sentenceid="b750b5084b5521b90338685143cecb65" id="tgt51" class="tgtSentence"> For example, if you wanted to process record-change events only when they occur because a record was added, you can use something like the following.</caps:sentence>
          </para>
          <code>' BeginEventExampleVB01
Private Sub rsTest_WillChangeRecord(ByVal adReason As ADODB.EventReasonEnum, ByVal cRecords As Long, adStatus As ADODB.EventStatusEnum, ByVal pRecordset As ADODB.Recordset)
   If adReason = adRsnAddNew Then
       ' Process event
       '...
   Else
       ' Cancel event notification for all
       ' other possible adReason values.
       adStatus = adStatusUnwantedEvent
   End If
End Sub
' EndEventExampleVB01</code>
          <para>
            <caps:sentence sentenceid="468650c6adc28911b45591d5bc101912" id="tgt52" class="tgtSentence">In this case, notification can potentially occur for each of the other reasons.</caps:sentence>
            <caps:sentence sentenceid="cc0de5b1708bb05a7fc99cd984ad6f6f" id="tgt53" class="tgtSentence"> However, it will occur only once for each reason.</caps:sentence>
            <caps:sentence sentenceid="e17452c072916b56372c7f16091589f0" id="tgt54" class="tgtSentence"> After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bb52982a7edb36be350ab268fc8cd57b" id="tgt55" class="tgtSentence">In contrast, you need to set <legacyItalic>adStatus</legacyItalic> to <legacyBold>adStatusUnwantedEvent</legacyBold> only one time to request that an event handler without an <legacyBold>adReason</legacyBold> parameter stop receiving event notifications.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">How Event Handlers Work Together</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Every event handler has a status parameter that controls the event handler.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Most Complete events also have an error parameter to provide information about any error that might have occurred, and one or more object parameters that refer to the ADO objects used to perform the operation.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example, the <legacyLink xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete</legacyLink> event includes object parameters for the <legacyBold>Command</legacyBold>, <legacyBold>Recordset</legacyBold>, and <legacyBold>Connection</legacyBold> objects associated with the event.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> In the following Microsoft® Visual Basic® example, you can see the pCommand, pRecordset, and pConnection objects which represent the <legacyBold>Command</legacyBold>, <legacyBold>Recordset</legacyBold>, and <legacyBold>Connection</legacyBold> objects that are used by the <legacyBold>Execute</legacyBold> method.</caps:sentence>
        </para>
        <code>Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _
     ByVal pError As ADODB.Error, _
     adStatus As ADODB.EventStatusEnum, _
     ByVal pCommand As ADODB.Command, _
     ByVal pRecordset As ADODB.Recordset, _
     ByVal pConnection As ADODB.Connection)</code>
        <para>
          <caps:sentence id="src6" class="srcSentence">Except for the <legacyBold>Error </legacyBold>object, the same parameters are passed to the Will events.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> This lets you examine each of the objects that will be used in the pending operation and determine whether the operation should be allowed to finish.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">Some event handlers have a <legacyItalic>Reason</legacyItalic> parameter, which provides additional information about why the event occurred.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> For example, the <legacyBold>WillMove</legacyBold> and <legacyBold>MoveComplete</legacyBold> events can occur because of any one of the navigation methods (<legacyBold>MoveNext</legacyBold>, <legacyBold>MovePrevious</legacyBold>, and so on) being called or as the result of a requery.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Status Parameter</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">When the event-handler routine is called, the <legacyItalic>Status</legacyItalic> parameter is set to one of the following values.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">               <legacyBold>adStatusOK</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Passed to both Will and Complete events.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> This value means that the operation that caused the event completed successfully.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">               <legacyBold>adStatusErrorsOccurred</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Passed to Complete events only.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation.</caps:sentence>
                    <caps:sentence id="src20" class="srcSentence"> Check the <legacyItalic>Error</legacyItalic> parameter for more details.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">               <legacyBold>adStatusCantDeny</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Passed to Will events only.</caps:sentence>
                    <caps:sentence id="src23" class="srcSentence"> This value means that the operation cannot be canceled by the Will event.</caps:sentence>
                    <caps:sentence id="src24" class="srcSentence"> It must be performed.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src25" class="srcSentence">If you determine in your Will event that the operation should continue, leave the <legacyItalic>Status</legacyItalic> parameter unchanged.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> As long as the incoming status parameter was not set to <legacyBold>adStatusCantDeny</legacyBold>, however, you can cancel the pending operation by changing <legacyItalic>Status</legacyItalic> to <legacyBold>adStatusCancel</legacyBold>.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> When you do this, the Complete event associated with the operation has its <legacyItalic>Status</legacyItalic> parameter set to <legacyBold>adStatusErrorsOccurred</legacyBold>.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> The <legacyBold>Error</legacyBold> object passed to the Complete event will contain the value <legacyBold>adErrOperationCancelled</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">If you no longer want to process an event, you can set <legacyItalic>Status</legacyItalic> to <legacyBold>adStatusUnwantedEvent</legacyBold> and your application will no longer receive notification of that event.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> However, remember that some events can be raised for more than one reason.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> In that case, you must specify <legacyBold>adStatusUnwantedEvent</legacyBold> for each possible reason.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> For example, to stop receiving notification of pending <legacyBold>RecordChange</legacyBold> events, you must set the <legacyItalic>Status</legacyItalic> parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> for <legacyBold>adRsnAddNew</legacyBold>, <legacyBold>adRsnDelete</legacyBold>, <legacyBold>adRsnUpdate</legacyBold>, <legacyBold>adRsnUndoUpdate</legacyBold>, <legacyBold>adRsnUndoAddNew</legacyBold>, <legacyBold>adRsnUndoDelete</legacyBold>, and <legacyBold>adRsnFirstChange</legacyBold> as they occur.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">               <legacyBold>adStatusUnwantedEvent</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Request that this event handler receive no further notifications.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">               <legacyBold>adStatusCancel</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Request cancellation of the operation that is about to occur.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src39" class="srcSentence">Error Parameter</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src40" class="srcSentence">The <legacyItalic>Error</legacyItalic> parameter is a reference to an ADO <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> When the <legacyItalic>Status</legacyItalic> parameter is set to <legacyBold>adStatusErrorsOccurred</legacyBold>, the <legacyBold>Error</legacyBold> object contains details about why the operation failed.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> If the Will event associated with a Complete event has canceled the operation by setting the <legacyItalic>Status</legacyItalic> parameter to <legacyBold>adStatusCancel</legacyBold>, the error object is always set to <legacyBold>adErrOperationCancelled</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src43" class="srcSentence">Object Parameter</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src44" class="srcSentence">Each event receives one or more objects representing the objects that are involved in the operation.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> For example, the <legacyBold>ExecuteComplete</legacyBold> event receives a <legacyBold>Command</legacyBold> object, a <legacyBold>Recordset</legacyBold> object, and a <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src46" class="srcSentence">Reason Parameter</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src47" class="srcSentence">The <legacyItalic>Reason</legacyItalic> parameter, <legacyItalic>adReason</legacyItalic>, provides additional information about why the event occurred.</caps:sentence>
            <caps:sentence id="src48" class="srcSentence"> Events with an <legacyItalic>adReason</legacyItalic> parameter may be called several times, even for the same operation, for a different reason every time.</caps:sentence>
            <caps:sentence id="src49" class="srcSentence"> For example, the <legacyBold>WillChangeRecord</legacyBold> event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</caps:sentence>
            <caps:sentence id="src50" class="srcSentence"> If you want to process an event only when it occurs for a particular reason, you can use the <legacyItalic>adReason</legacyItalic> parameter to filter out the occurrences you are not interested in.</caps:sentence>
            <caps:sentence id="src51" class="srcSentence"> For example, if you wanted to process record-change events only when they occur because a record was added, you can use something like the following.</caps:sentence>
          </para>
          <code>' BeginEventExampleVB01
Private Sub rsTest_WillChangeRecord(ByVal adReason As ADODB.EventReasonEnum, ByVal cRecords As Long, adStatus As ADODB.EventStatusEnum, ByVal pRecordset As ADODB.Recordset)
   If adReason = adRsnAddNew Then
       ' Process event
       '...
   Else
       ' Cancel event notification for all
       ' other possible adReason values.
       adStatus = adStatusUnwantedEvent
   End If
End Sub
' EndEventExampleVB01</code>
          <para>
            <caps:sentence id="src52" class="srcSentence">In this case, notification can potentially occur for each of the other reasons.</caps:sentence>
            <caps:sentence id="src53" class="srcSentence"> However, it will occur only once for each reason.</caps:sentence>
            <caps:sentence id="src54" class="srcSentence"> After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src55" class="srcSentence">In contrast, you need to set <legacyItalic>adStatus</legacyItalic> to <legacyBold>adStatusUnwantedEvent</legacyBold> only one time to request that an event handler without an <legacyBold>adReason</legacyBold> parameter stop receiving event notifications.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">How Event Handlers Work Together</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "WillMove and MoveComplete Events (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 1a3d1042-4f30-4526-a0c7-853c242496db
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
# WillMove and MoveComplete Events (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="429ffc696171d8ae742bcc768ece14bd" id="tgt1" class="tgtSentence">The <unmanagedCodeEntityReference>WillMove</unmanagedCodeEntityReference> event is called before a pending operation changes the current position in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="d29239a681a9fadf0b07a63503336b06" id="tgt2" class="tgtSentence"> The <unmanagedCodeEntityReference>MoveComplete</unmanagedCodeEntityReference> event is called after the current position in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> changes.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillMove</legacyBold>
          <parameterReference>adReason, adStatus, pRecordset</parameterReference>
          <legacyBold>MoveComplete</legacyBold>
          <parameterReference>adReason, pError, adStatus, pRecordset</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="cfc42fd2012a7022ed833ee7d0a1a497" id="tgt3" class="tgtSentence"> <legacyItalic>adReason</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="bd7731ee70daa4e5100898c98df1bcda" id="tgt4" class="tgtSentence">An <legacyLink xlink:href="7d4a5496-ec2d-4936-b36a-7049a82be4b4">EventReasonEnum</legacyLink> value that specifies the reason for this event.</caps:sentence>
                <caps:sentence sentenceid="10922422057a37e3b6507144b797a37d" id="tgt5" class="tgtSentence"> Its value can be <legacyBold>adRsnMoveFirst</legacyBold>, <legacyBold>adRsnMoveLast</legacyBold>, <legacyBold>adRsnMoveNext</legacyBold>, <legacyBold>adRsnMovePrevious</legacyBold>, <legacyBold>adRsnMove</legacyBold>, or <legacyBold>adRsnRequery</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c53ca6f9660a98f2e3bddd392afe3c26" id="tgt6" class="tgtSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f8547f0cddb40fb6c028ac5705fb05df" id="tgt7" class="tgtSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="b3fb167b8503c4494df55493a39d4f67" id="tgt8" class="tgtSentence"> It describes the error that occurred if the value of <legacyItalic>adStatus</legacyItalic> is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise the parameter is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt9" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt10" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7eac4914ce70f76c69b595ffc141bb6c" id="tgt11" class="tgtSentence">When <unmanagedCodeEntityReference>WillMove</unmanagedCodeEntityReference> is called, this parameter is set to <legacyBold>adStatusOK </legacyBold>if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence sentenceid="66b086c867ad146cc20957db5cf35f3c" id="tgt12" class="tgtSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7382d579ae72cde5f773e2dd53aa0015" id="tgt13" class="tgtSentence">When <unmanagedCodeEntityReference>MoveComplete</unmanagedCodeEntityReference> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1dadfd0b8d054aa10450ca36a7e54c3c" id="tgt14" class="tgtSentence">Before <unmanagedCodeEntityReference>WillMove</unmanagedCodeEntityReference> returns, set this parameter to <legacyBold>adStatusCancel</legacyBold> to request cancellation of the pending operation, or set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d40f25e6efe268584b00822d6e09df34" id="tgt15" class="tgtSentence">Before <unmanagedCodeEntityReference>MoveComplete</unmanagedCodeEntityReference> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c294ce2e8a8edf29ce067cff9e0573d5" id="tgt16" class="tgtSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="53149f493e54df5ed6ad8939a01a7e3e" id="tgt17" class="tgtSentence">A <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="2f2a47345f4f296625b7689924d7dcc5" id="tgt18" class="tgtSentence"> The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b11e18500a6fae32fee12f9d32b42470" id="tgt19" class="tgtSentence">A <unmanagedCodeEntityReference>WillMove</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>MoveComplete</unmanagedCodeEntityReference> event may occur due to the following <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> operations: <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink>, <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveLast</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveNext</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MovePrevious</legacyLink>, <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink>, and <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="becc764f8765f6b1849442d31c30c081" id="tgt20" class="tgtSentence"> These events may occur because of the following properties: <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink>, <legacyLink xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index</legacyLink>, <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink>, <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink>, and <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="5ab9c7563b99baf6b911f914683b69a5" id="tgt21" class="tgtSentence"> These events also occur if a child <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> has <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> events connected and the parent <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is moved.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0cb120cd09e4d579a5517c74e0345439" id="tgt22" class="tgtSentence">You must set the <parameterReference>adStatus</parameterReference> parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> for each possible <parameterReference>adReason</parameterReference> value in order to completely stop event notification for any event that includes an <parameterReference>adReason</parameterReference> parameter.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <unmanagedCodeEntityReference>WillMove</unmanagedCodeEntityReference> event is called before a pending operation changes the current position in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <unmanagedCodeEntityReference>MoveComplete</unmanagedCodeEntityReference> event is called after the current position in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> changes.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillMove</legacyBold>
          <parameterReference>adReason, adStatus, pRecordset</parameterReference>
          <legacyBold>MoveComplete</legacyBold>
          <parameterReference>adReason, pError, adStatus, pRecordset</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>adReason</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">An <legacyLink xlink:href="7d4a5496-ec2d-4936-b36a-7049a82be4b4">EventReasonEnum</legacyLink> value that specifies the reason for this event.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> Its value can be <legacyBold>adRsnMoveFirst</legacyBold>, <legacyBold>adRsnMoveLast</legacyBold>, <legacyBold>adRsnMoveNext</legacyBold>, <legacyBold>adRsnMovePrevious</legacyBold>, <legacyBold>adRsnMove</legacyBold>, or <legacyBold>adRsnRequery</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> It describes the error that occurred if the value of <legacyItalic>adStatus</legacyItalic> is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise the parameter is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src11" class="srcSentence">When <unmanagedCodeEntityReference>WillMove</unmanagedCodeEntityReference> is called, this parameter is set to <legacyBold>adStatusOK </legacyBold>if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src13" class="srcSentence">When <unmanagedCodeEntityReference>MoveComplete</unmanagedCodeEntityReference> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src14" class="srcSentence">Before <unmanagedCodeEntityReference>WillMove</unmanagedCodeEntityReference> returns, set this parameter to <legacyBold>adStatusCancel</legacyBold> to request cancellation of the pending operation, or set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src15" class="srcSentence">Before <unmanagedCodeEntityReference>MoveComplete</unmanagedCodeEntityReference> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src16" class="srcSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src17" class="srcSentence">A <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src19" class="srcSentence">A <unmanagedCodeEntityReference>WillMove</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>MoveComplete</unmanagedCodeEntityReference> event may occur due to the following <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> operations: <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink>, <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveLast</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveNext</legacyLink>, <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MovePrevious</legacyLink>, <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink>, and <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink>.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> These events may occur because of the following properties: <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink>, <legacyLink xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index</legacyLink>, <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink>, <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink>, and <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink>.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> These events also occur if a child <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> has <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> events connected and the parent <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is moved.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">You must set the <parameterReference>adStatus</parameterReference> parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> for each possible <parameterReference>adReason</parameterReference> value in order to completely stop event notification for any event that includes an <parameterReference>adReason</parameterReference> parameter.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
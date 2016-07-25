---
title: "WillChangeRecord and RecordChangeComplete Events (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cbc369fd-63af-4a7d-96ae-efa91b78ca69
caps.latest.revision: 11
caps.handback.revision: 11
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
# WillChangeRecord and RecordChangeComplete Events (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0fd8fa85cd76aaab5d43c1a552ce60a9" id="tgt1" class="tgtSentence">The <legacyBold>WillChangeRecord</legacyBold> event is called before one or more records (rows) in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> change.</caps:sentence>
          <caps:sentence sentenceid="a2e1556da471ad666e87b5a85c728a23" id="tgt2" class="tgtSentence"> The <legacyBold>RecordChangeComplete</legacyBold> event is called after one or more records change.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillChangeRecord</legacyBold>
          <parameterReference>adReason</parameterReference>, <parameterReference>cRecords</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference><legacyBold>RecordChangeComplete</legacyBold><parameterReference>adReason</parameterReference>, <parameterReference>cRecords</parameterReference>, <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
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
                <caps:sentence sentenceid="11baecf01e9329b45508bf2db954a354" id="tgt5" class="tgtSentence"> Its value can be <legacyBold>adRsnAddNew</legacyBold>, <legacyBold>adRsnDelete</legacyBold>, <legacyBold>adRsnUpdate</legacyBold>, <legacyBold>adRsnUndoUpdate</legacyBold>, <legacyBold>adRsnUndoAddNew</legacyBold>, <legacyBold>adRsnUndoDelete</legacyBold>, or <legacyBold>adRsnFirstChange</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="88d82164170c3e299f14e08de25fa806" id="tgt6" class="tgtSentence"> <legacyItalic>cRecords</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="8b04a0b9cef1f2ce2d3fd436e6e9c777" id="tgt7" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value that indicates the number of records changing (affected).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c53ca6f9660a98f2e3bddd392afe3c26" id="tgt8" class="tgtSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f8547f0cddb40fb6c028ac5705fb05df" id="tgt9" class="tgtSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="43299bc9d9503a6718044f2f89e37d89" id="tgt10" class="tgtSentence"> It describes the error that occurred if the value of <legacyItalic>adStatus</legacyItalic> is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt11" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt12" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="73f76741575866fd6fdd72387e582764" id="tgt13" class="tgtSentence">When <legacyBold>WillChangeRecord</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK </legacyBold>if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence sentenceid="66b086c867ad146cc20957db5cf35f3c" id="tgt14" class="tgtSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2d543db372823d03ea318d2357a30156" id="tgt15" class="tgtSentence">When <legacyBold>RecordChangeComplete</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="0f4bb6bd1187ea2c6c96058868061105" id="tgt16" class="tgtSentence">Before <legacyBold>WillChangeRecord</legacyBold> returns, set this parameter to <legacyBold>adStatusCancel</legacyBold> to request cancellation of the operation that caused this event or set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6f09109257dce8602a29c4c1c02ba8fd" id="tgt17" class="tgtSentence">Before <legacyBold>RecordChangeComplete</legacyBold> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c294ce2e8a8edf29ce067cff9e0573d5" id="tgt18" class="tgtSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7210e9c9b35007dd06fe386a735520b7" id="tgt19" class="tgtSentence">A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="d5e823f3b7e5899b8d3ac62d8a76dc4a" id="tgt20" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ee22d00749a7fd7eb7b75be2ad16323e" id="tgt21" class="tgtSentence">A <legacyBold>WillChangeRecord</legacyBold> or <legacyBold>RecordChangeComplete</legacyBold> event may occur for the first changed field in a row due to the following <legacyBold>Recordset</legacyBold> operations: <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>, <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink>, <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink>, <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, and <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="77aa352f448ddf3e5a60f0b18945a5da" id="tgt22" class="tgtSentence"> The value of the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink> determines which operations cause the events to occur.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b34314502a93e62441c19bb44d797fdd" id="tgt23" class="tgtSentence">During the <legacyBold>WillChangeRecord</legacyBold> event, the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property is set to <legacyBold>adFilterAffectedRecords</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="dc2a22b9669ae97fe8e3440b1b3ebde7" id="tgt24" class="tgtSentence"> You cannot change this property while processing the event.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4d20be3fe9ed1ce76c526a474acc627d" id="tgt25" class="tgtSentence">You must set the <legacyBold>adStatus</legacyBold> parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> for each possible <legacyBold>adReason</legacyBold> value to completely stop event notification for any event that includes an <legacyBold>adReason</legacyBold> parameter.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>WillChangeRecord</legacyBold> event is called before one or more records (rows) in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> change.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyBold>RecordChangeComplete</legacyBold> event is called after one or more records change.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillChangeRecord</legacyBold>
          <parameterReference>adReason</parameterReference>, <parameterReference>cRecords</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference><legacyBold>RecordChangeComplete</legacyBold><parameterReference>adReason</parameterReference>, <parameterReference>cRecords</parameterReference>, <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
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
                <caps:sentence id="src5" class="srcSentence"> Its value can be <legacyBold>adRsnAddNew</legacyBold>, <legacyBold>adRsnDelete</legacyBold>, <legacyBold>adRsnUpdate</legacyBold>, <legacyBold>adRsnUndoUpdate</legacyBold>, <legacyBold>adRsnUndoAddNew</legacyBold>, <legacyBold>adRsnUndoDelete</legacyBold>, or <legacyBold>adRsnFirstChange</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>cRecords</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">A <languageKeyword>Long</languageKeyword> value that indicates the number of records changing (affected).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> It describes the error that occurred if the value of <legacyItalic>adStatus</legacyItalic> is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src11" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src12" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src13" class="srcSentence">When <legacyBold>WillChangeRecord</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK </legacyBold>if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src15" class="srcSentence">When <legacyBold>RecordChangeComplete</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src16" class="srcSentence">Before <legacyBold>WillChangeRecord</legacyBold> returns, set this parameter to <legacyBold>adStatusCancel</legacyBold> to request cancellation of the operation that caused this event or set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src17" class="srcSentence">Before <legacyBold>RecordChangeComplete</legacyBold> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src18" class="srcSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src19" class="srcSentence">A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> The <legacyBold>Recordset</legacyBold> for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">A <legacyBold>WillChangeRecord</legacyBold> or <legacyBold>RecordChangeComplete</legacyBold> event may occur for the first changed field in a row due to the following <legacyBold>Recordset</legacyBold> operations: <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>, <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink>, <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink>, <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, and <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink>.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> The value of the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink> determines which operations cause the events to occur.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">During the <legacyBold>WillChangeRecord</legacyBold> event, the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property is set to <legacyBold>adFilterAffectedRecords</legacyBold>.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> You cannot change this property while processing the event.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">You must set the <legacyBold>adStatus</legacyBold> parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> for each possible <legacyBold>adReason</legacyBold> value to completely stop event notification for any event that includes an <legacyBold>adReason</legacyBold> parameter.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
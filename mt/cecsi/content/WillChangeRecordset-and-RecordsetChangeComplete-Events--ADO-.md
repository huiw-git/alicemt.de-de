---
title: "WillChangeRecordset and RecordsetChangeComplete Events (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d5d44659-e0d9-46d9-a297-99c43555082f
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
# WillChangeRecordset and RecordsetChangeComplete Events (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6a0b05dd5431650c9d178fcc264f814f" id="tgt1" class="tgtSentence">The <legacyBold>WillChangeRecordset</legacyBold> event is called before a pending operation changes the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="d824b4141e94750ce45507310b9d248c" id="tgt2" class="tgtSentence"> The <legacyBold>RecordsetChangeComplete</legacyBold> event is called after the <legacyBold>Recordset</legacyBold> has changed.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillChangeRecordset </legacyBold>
          <parameterReference>adReason</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference><legacyBold>RecordsetChangeComplete </legacyBold><parameterReference>adReason</parameterReference>, <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
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
                <caps:sentence sentenceid="5b1e4a1a28767a4ac547a9234818bdf1" id="tgt5" class="tgtSentence"> Its value can be <legacyBold>adRsnRequery</legacyBold>, <legacyBold>adRsnResynch</legacyBold>, <legacyBold>adRsnClose</legacyBold>, <legacyBold>adRsnOpen</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt6" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt7" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e5e01dc7063fb703676ceb2fabb8ad3a" id="tgt8" class="tgtSentence">When <legacyBold>WillChangeRecordset</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence sentenceid="66b086c867ad146cc20957db5cf35f3c" id="tgt9" class="tgtSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="95e109cc0e48f323a86aabf5a8bb8554" id="tgt10" class="tgtSentence">When <legacyBold>RecordsetChangeComplete</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed, or <legacyBold>adStatusCancel</legacyBold> if the operation associated with the previously accepted <legacyBold>WillChangeRecordset</legacyBold> event has been canceled.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="930217bf8483cc7b2cadaaeab7bc13e4" id="tgt11" class="tgtSentence">Before <legacyBold>WillChangeRecordset</legacyBold> returns, set this parameter to <legacyBold>adStatusCancel</legacyBold> to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c91e101fa54a9cfddd30bf1ec4192ac4" id="tgt12" class="tgtSentence">Before <legacyBold>WillChangeRecordset</legacyBold> or <legacyBold>RecordsetChangeComplete</legacyBold> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c53ca6f9660a98f2e3bddd392afe3c26" id="tgt13" class="tgtSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f8547f0cddb40fb6c028ac5705fb05df" id="tgt14" class="tgtSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="43299bc9d9503a6718044f2f89e37d89" id="tgt15" class="tgtSentence"> It describes the error that occurred if the value of <legacyItalic>adStatus</legacyItalic> is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c294ce2e8a8edf29ce067cff9e0573d5" id="tgt16" class="tgtSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7210e9c9b35007dd06fe386a735520b7" id="tgt17" class="tgtSentence">A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="d5e823f3b7e5899b8d3ac62d8a76dc4a" id="tgt18" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="018cb2976ac21f60f6ae5648c05364bc" id="tgt19" class="tgtSentence">A <legacyBold>WillChangeRecordset</legacyBold> or <legacyBold>RecordsetChangeComplete</legacyBold> event may occur because of the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> or <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> methods.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="aac36d289ec017f6094ae0946d0a7635" id="tgt20" class="tgtSentence">If the provider does not support bookmarks, a <legacyBold>RecordsetChange</legacyBold> event notification occurs every time that new rows are retrieved from the provider.</caps:sentence>
            <caps:sentence sentenceid="e1ef286e2ab224eb069adf93259315bc" id="tgt21" class="tgtSentence"> The frequency of this event depends on the <legacyBold>RecordsetCacheSize</legacyBold> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4d20be3fe9ed1ce76c526a474acc627d" id="tgt22" class="tgtSentence">You must set the <legacyBold>adStatus</legacyBold> parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> for each possible <legacyBold>adReason</legacyBold> value to completely stop event notification for any event that includes an <legacyBold>adReason</legacyBold> parameter.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>WillChangeRecordset</legacyBold> event is called before a pending operation changes the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyBold>RecordsetChangeComplete</legacyBold> event is called after the <legacyBold>Recordset</legacyBold> has changed.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillChangeRecordset </legacyBold>
          <parameterReference>adReason</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference><legacyBold>RecordsetChangeComplete </legacyBold><parameterReference>adReason</parameterReference>, <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
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
                <caps:sentence id="src5" class="srcSentence"> Its value can be <legacyBold>adRsnRequery</legacyBold>, <legacyBold>adRsnResynch</legacyBold>, <legacyBold>adRsnClose</legacyBold>, <legacyBold>adRsnOpen</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src8" class="srcSentence">When <legacyBold>WillChangeRecordset</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src10" class="srcSentence">When <legacyBold>RecordsetChangeComplete</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed, or <legacyBold>adStatusCancel</legacyBold> if the operation associated with the previously accepted <legacyBold>WillChangeRecordset</legacyBold> event has been canceled.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src11" class="srcSentence">Before <legacyBold>WillChangeRecordset</legacyBold> returns, set this parameter to <legacyBold>adStatusCancel</legacyBold> to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src12" class="srcSentence">Before <legacyBold>WillChangeRecordset</legacyBold> or <legacyBold>RecordsetChangeComplete</legacyBold> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src13" class="srcSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src14" class="srcSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> It describes the error that occurred if the value of <legacyItalic>adStatus</legacyItalic> is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src16" class="srcSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src17" class="srcSentence">A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> The <legacyBold>Recordset</legacyBold> for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src19" class="srcSentence">A <legacyBold>WillChangeRecordset</legacyBold> or <legacyBold>RecordsetChangeComplete</legacyBold> event may occur because of the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> or <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> methods.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">If the provider does not support bookmarks, a <legacyBold>RecordsetChange</legacyBold> event notification occurs every time that new rows are retrieved from the provider.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> The frequency of this event depends on the <legacyBold>RecordsetCacheSize</legacyBold> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">You must set the <legacyBold>adStatus</legacyBold> parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> for each possible <legacyBold>adReason</legacyBold> value to completely stop event notification for any event that includes an <legacyBold>adReason</legacyBold> parameter.</caps:sentence>
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
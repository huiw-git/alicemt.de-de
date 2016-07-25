---
title: "EndOfRecordset Event (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 475de5e2-f634-4954-9edf-0027a6ba38d6
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
# EndOfRecordset Event (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4eef4c40574ae14248b155660e421402" id="tgt1" class="tgtSentence">The <legacyBold>EndOfRecordset</legacyBold> event is called when there is an attempt to move to a row past the end of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>EndOfRecordset</legacyBold>
          <parameterReference>fMoreData</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="43da5967697091672d4ada48dbd4f521" id="tgt2" class="tgtSentence"> <legacyItalic>fMoreData</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="3fd53c7a6fc2a4c75c7b9cccbb1572d7" id="tgt3" class="tgtSentence">A <legacyBold>VARIANT_BOOL</legacyBold> value that, if set to VARIANT_TRUE, indicates more rows have been added to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt4" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt5" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="70d5f72e834dae9dc63cd43712910ea6" id="tgt6" class="tgtSentence">When <legacyBold>EndOfRecordset</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK </legacyBold>if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence sentenceid="ad228b7f76aed0d4d92e82d70b8117e0" id="tgt7" class="tgtSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the operation that caused this event.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a92321227a49788b05b3a6e4a3826773" id="tgt8" class="tgtSentence">Before <legacyBold>EndOfRecordset</legacyBold> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c294ce2e8a8edf29ce067cff9e0573d5" id="tgt9" class="tgtSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7210e9c9b35007dd06fe386a735520b7" id="tgt10" class="tgtSentence">A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="d5e823f3b7e5899b8d3ac62d8a76dc4a" id="tgt11" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e54e80f6fd7ca9e208efd9868e7d216a" id="tgt12" class="tgtSentence">An <legacyBold>EndOfRecordset</legacyBold> event may occur if the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveNext</legacyLink> operation fails.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e46eef656121518463b6c03f1f6745d5" id="tgt13" class="tgtSentence">This event handler is called when an attempt is made to move past the end of the <legacyBold>Recordset</legacyBold> object, perhaps as a result of calling <legacyBold>MoveNext</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="1882cd05670e3a5a64626794ec81ebaf" id="tgt14" class="tgtSentence"> However, while in this event, you could retrieve more records from a database and append them to the end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="c19b56ce2aafa03a4aaada18072c51b9" id="tgt15" class="tgtSentence"> In that case, set <legacyItalic>fMoreData</legacyItalic> to VARIANT_TRUE, and return from <legacyBold>EndOfRecordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="9c93381ef4c0bfaa7440a5506d28d532" id="tgt16" class="tgtSentence"> Then call <legacyBold>MoveNext</legacyBold> again to access the newly retrieved records.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>EndOfRecordset</legacyBold> event is called when there is an attempt to move to a row past the end of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>EndOfRecordset</legacyBold>
          <parameterReference>fMoreData</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>fMoreData</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <legacyBold>VARIANT_BOOL</legacyBold> value that, if set to VARIANT_TRUE, indicates more rows have been added to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src6" class="srcSentence">When <legacyBold>EndOfRecordset</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK </legacyBold>if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the operation that caused this event.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src8" class="srcSentence">Before <legacyBold>EndOfRecordset</legacyBold> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> The <legacyBold>Recordset</legacyBold> for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">An <legacyBold>EndOfRecordset</legacyBold> event may occur if the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveNext</legacyLink> operation fails.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">This event handler is called when an attempt is made to move past the end of the <legacyBold>Recordset</legacyBold> object, perhaps as a result of calling <legacyBold>MoveNext</legacyBold>.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> However, while in this event, you could retrieve more records from a database and append them to the end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> In that case, set <legacyItalic>fMoreData</legacyItalic> to VARIANT_TRUE, and return from <legacyBold>EndOfRecordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Then call <legacyBold>MoveNext</legacyBold> again to access the newly retrieved records.</caps:sentence>
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
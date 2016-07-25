---
title: "WillChangeField and FieldChangeComplete Events (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3e49fb89-c45b-4d39-823e-3cc887c59b37
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
# WillChangeField and FieldChangeComplete Events (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ff10f62de9f6c6604d69ff57bdb91326" id="tgt1" class="tgtSentence">The <legacyBold>WillChangeField</legacyBold> event is called before a pending operation changes the value of one or more <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="dd02f04635801150452eabc41992932b" id="tgt2" class="tgtSentence"> The <legacyBold>FieldChangeComplete</legacyBold> event is called after the value of one or more <legacyBold>Field</legacyBold> objects has changed.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillChangeField</legacyBold>
          <parameterReference>cFields</parameterReference>, <parameterReference>Fields</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference><legacyBold>FieldChangeComplete </legacyBold><parameterReference>cFields</parameterReference>, <parameterReference>Fields</parameterReference>, <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="590e57dd9582cdd246efb54a0dc77aa1" id="tgt3" class="tgtSentence"> <legacyItalic>cFields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ab46d84b92e299025ed17090c138d3a2" id="tgt4" class="tgtSentence">A <languageKeyword>Long</languageKeyword> that indicates the number of <legacyBold>Field</legacyBold> objects in <legacyItalic>Fields</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8bddbd1d644449f57c976b7c137a00a3" id="tgt5" class="tgtSentence"> <legacyItalic>Fields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f7a3bffe41441cfc1ed65b25db8a8cff" id="tgt6" class="tgtSentence">For <legacyBold>WillChangeField</legacyBold>, the <legacyItalic>Fields</legacyItalic> parameter is an array of <legacyBold>Variants</legacyBold> that contains <legacyBold>Field</legacyBold> objects with the original values.</caps:sentence>
                <caps:sentence sentenceid="54d509c16724b1a8a4f6443027c3d66e" id="tgt7" class="tgtSentence"> For <legacyBold>FieldChangeComplete</legacyBold>, the <legacyItalic>Fields</legacyItalic> parameter is an array of <legacyBold>Variants</legacyBold> that contains <legacyBold>Field</legacyBold> objects with the changed values.</caps:sentence>
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
                <caps:sentence sentenceid="4d1c1910436ca6373466f85c2b2eb57d" id="tgt13" class="tgtSentence">When <legacyBold>WillChangeField</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK </legacyBold>if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence sentenceid="66b086c867ad146cc20957db5cf35f3c" id="tgt14" class="tgtSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="06f33e671a00a6a6add93fc1aee53f80" id="tgt15" class="tgtSentence">When <legacyBold>FieldChangeComplete</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="07ed43a8725b549c3bdaf2bb7820b10f" id="tgt16" class="tgtSentence">Before <legacyBold>WillChangeField</legacyBold> returns, set this parameter to <legacyBold>adStatusCancel</legacyBold> to request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="9edbca4086479bf4cd83bf92129a8461" id="tgt17" class="tgtSentence">Before <legacyBold>FieldChangeComplete</legacyBold> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
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
            <caps:sentence sentenceid="1e5445a42a9dec7641ff64e9a83bf8f6" id="tgt21" class="tgtSentence">A <legacyBold>WillChangeField</legacyBold> or <legacyBold>FieldChangeComplete</legacyBold> event may occur when setting the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property and calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method with field and value array parameters.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>WillChangeField</legacyBold> event is called before a pending operation changes the value of one or more <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyBold>FieldChangeComplete</legacyBold> event is called after the value of one or more <legacyBold>Field</legacyBold> objects has changed.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillChangeField</legacyBold>
          <parameterReference>cFields</parameterReference>, <parameterReference>Fields</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference><legacyBold>FieldChangeComplete </legacyBold><parameterReference>cFields</parameterReference>, <parameterReference>Fields</parameterReference>, <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>cFields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A <languageKeyword>Long</languageKeyword> that indicates the number of <legacyBold>Field</legacyBold> objects in <legacyItalic>Fields</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>Fields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">For <legacyBold>WillChangeField</legacyBold>, the <legacyItalic>Fields</legacyItalic> parameter is an array of <legacyBold>Variants</legacyBold> that contains <legacyBold>Field</legacyBold> objects with the original values.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> For <legacyBold>FieldChangeComplete</legacyBold>, the <legacyItalic>Fields</legacyItalic> parameter is an array of <legacyBold>Variants</legacyBold> that contains <legacyBold>Field</legacyBold> objects with the changed values.</caps:sentence>
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
                <caps:sentence id="src13" class="srcSentence">When <legacyBold>WillChangeField</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK </legacyBold>if the operation that caused the event was successful.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if this event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src15" class="srcSentence">When <legacyBold>FieldChangeComplete</legacyBold> is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src16" class="srcSentence">Before <legacyBold>WillChangeField</legacyBold> returns, set this parameter to <legacyBold>adStatusCancel</legacyBold> to request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src17" class="srcSentence">Before <legacyBold>FieldChangeComplete</legacyBold> returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
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
            <caps:sentence id="src21" class="srcSentence">A <legacyBold>WillChangeField</legacyBold> or <legacyBold>FieldChangeComplete</legacyBold> event may occur when setting the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property and calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method with field and value array parameters.</caps:sentence>
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
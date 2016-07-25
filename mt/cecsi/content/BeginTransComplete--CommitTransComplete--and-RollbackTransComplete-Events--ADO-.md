---
title: "BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8
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
# BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0741a6a8110f5ca271ba2e01160439b3" id="tgt1" class="tgtSentence">These events will be called after the associated operation on the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object finishes executing.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="a1084963009ef2a8d58dc62fc481a1b1" id="tgt2" class="tgtSentence">
                <legacyBold>BeginTransComplete</legacyBold> is called after the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans</legacyLink> operation.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="eec68b2924a01ea62ded5e1a7c22afd4" id="tgt3" class="tgtSentence">
                <legacyBold>CommitTransComplete</legacyBold> is called after the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">CommitTrans</legacyLink> operation.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="020699c2242caf6af3f936876165e718" id="tgt4" class="tgtSentence">
                <legacyBold>RollbackTransComplete</legacyBold> is called after the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">RollbackTrans</legacyLink> operation.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>BeginTransComplete</legacyBold>
          <parameterReference>TransactionLevel, pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pConnection</parameterReference><legacyBold>CommitTransComplete </legacyBold><parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pConnection</parameterReference><legacyBold>RollbackTransComplete </legacyBold><parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pConnection</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="4be57b60df206a12aa8d8c56fc5157aa" id="tgt5" class="tgtSentence"> <legacyItalic>TransactionLevel</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="95425775632c0b0214ddf8ca95089fab" id="tgt6" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value that contains the new transaction level of the <legacyBold>BeginTrans</legacyBold> that caused this event.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c53ca6f9660a98f2e3bddd392afe3c26" id="tgt7" class="tgtSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f8547f0cddb40fb6c028ac5705fb05df" id="tgt8" class="tgtSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="2b8d757213ad1845feef072cfed00998" id="tgt9" class="tgtSentence"> It describes the error that occurred if the value of EventStatusEnum is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt10" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt11" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
                <caps:sentence sentenceid="92b649826bf3634f01bd2a26a22c92c0" id="tgt12" class="tgtSentence"> When any of these events is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="09af91386cc2fae932aa157037f38a7b" id="tgt13" class="tgtSentence">These events can prevent subsequent notifications by setting this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> before the event returns.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5f727b94f6dccd2318ee30175b2c25bc" id="tgt14" class="tgtSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ae9ad11e458a93b82436a981d50c7f02" id="tgt15" class="tgtSentence">The <legacyBold>Connection</legacyBold> object for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="962927d5e2ba7ea67287900d96407439" id="tgt16" class="tgtSentence">In Visual C++, multiple <legacyBold>Connections</legacyBold> can share the same event handling method.</caps:sentence>
            <caps:sentence sentenceid="52584e79e7a189c43eaf9772f64deb8c" id="tgt17" class="tgtSentence"> The method uses the returned <legacyBold>Connection</legacyBold> object to determine which object caused the event.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c86ff6f35fbf8ebfcc29dce9f8068b9d" id="tgt18" class="tgtSentence">If the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property is set to <legacyBold>adXactCommitRetaining</legacyBold> or <legacyBold>adXactAbortRetaining</legacyBold>, a new transaction starts after committing or rolling back a transaction.</caps:sentence>
            <caps:sentence sentenceid="e62a62e47f0bccd6b025b990fb8188c5" id="tgt19" class="tgtSentence"> Use the <legacyBold>BeginTransComplete</legacyBold> event to ignore all but the first transaction start event.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="27f502f8-d66a-4b44-9071-a05993d3fabb">Visual J++ Example</link>
        <link xlink:href="aa7de324-cd71-4bd0-8043-24229f4a785e">Visual Basic Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans, CommitTrans, and RollbackTrans Methods</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">These events will be called after the associated operation on the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object finishes executing.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">
                <legacyBold>BeginTransComplete</legacyBold> is called after the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans</legacyLink> operation.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">
                <legacyBold>CommitTransComplete</legacyBold> is called after the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">CommitTrans</legacyLink> operation.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">
                <legacyBold>RollbackTransComplete</legacyBold> is called after the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">RollbackTrans</legacyLink> operation.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>BeginTransComplete</legacyBold>
          <parameterReference>TransactionLevel, pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pConnection</parameterReference><legacyBold>CommitTransComplete </legacyBold><parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pConnection</parameterReference><legacyBold>RollbackTransComplete </legacyBold><parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pConnection</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>TransactionLevel</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A <languageKeyword>Long</languageKeyword> value that contains the new transaction level of the <legacyBold>BeginTrans</legacyBold> that caused this event.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> It describes the error that occurred if the value of EventStatusEnum is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> When any of these events is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src13" class="srcSentence">These events can prevent subsequent notifications by setting this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> before the event returns.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src14" class="srcSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src15" class="srcSentence">The <legacyBold>Connection</legacyBold> object for which this event occurred.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src16" class="srcSentence">In Visual C++, multiple <legacyBold>Connections</legacyBold> can share the same event handling method.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> The method uses the returned <legacyBold>Connection</legacyBold> object to determine which object caused the event.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property is set to <legacyBold>adXactCommitRetaining</legacyBold> or <legacyBold>adXactAbortRetaining</legacyBold>, a new transaction starts after committing or rolling back a transaction.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> Use the <legacyBold>BeginTransComplete</legacyBold> event to ignore all but the first transaction start event.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="27f502f8-d66a-4b44-9071-a05993d3fabb">Visual J++ Example</link>
        <link xlink:href="aa7de324-cd71-4bd0-8043-24229f4a785e">Visual Basic Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans, CommitTrans, and RollbackTrans Methods</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
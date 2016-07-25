---
title: "ConnectComplete and Disconnect Events (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 568f5252-d069-4d99-a01b-2ada87ad1304
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
# ConnectComplete and Disconnect Events (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d5cd2d4a8c07643b41cdf3fcd138a958" id="tgt1" class="tgtSentence">The <legacyBold>ConnectComplete</legacyBold> event is called after a connection starts.</caps:sentence>
          <caps:sentence sentenceid="88764bc55d00e49d10e7c34be2753cba" id="tgt2" class="tgtSentence"> The <legacyBold>Disconnect</legacyBold> event is called after a connection ends.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>ConnectComplete</legacyBold>
          <parameterReference>pError, adStatus, pConnection</parameterReference>
          <legacyBold>Disconnect </legacyBold>
          <parameterReference>adStatus, pConnection</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="c53ca6f9660a98f2e3bddd392afe3c26" id="tgt3" class="tgtSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f8547f0cddb40fb6c028ac5705fb05df" id="tgt4" class="tgtSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="111b62a957c256c8f3286367f312d38e" id="tgt5" class="tgtSentence"> It describes the error that occurred if the value of <legacyItalic>adStatus </legacyItalic>is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt6" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a899dae251ae19d27e6fa69d9b632770" id="tgt7" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> value that always returns <legacyBold>adStatusOK</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a0cb29275fe8ec477daf960225a3cdac" id="tgt8" class="tgtSentence">When <legacyBold>ConnectComplete</legacyBold> is called, this parameter is set to <legacyBold>adStatusCancel</legacyBold> if a <legacyBold>WillConnect</legacyBold> event has requested cancellation of the pending connection.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="da30b4d63909ec7dd7fde91c0c368c8d" id="tgt9" class="tgtSentence">Before either event returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
                <caps:sentence sentenceid="4c3ac4cb164bd5e5460600173631c2ee" id="tgt10" class="tgtSentence"> However, closing and reopening the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> causes these events to occur again.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5f727b94f6dccd2318ee30175b2c25bc" id="tgt11" class="tgtSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d14cb05ffc57e7dabce3f9f29c43ef44" id="tgt12" class="tgtSentence">The <legacyBold>Connection</legacyBold> object for which this event applies.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>ConnectComplete</legacyBold> event is called after a connection starts.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyBold>Disconnect</legacyBold> event is called after a connection ends.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>ConnectComplete</legacyBold>
          <parameterReference>pError, adStatus, pConnection</parameterReference>
          <legacyBold>Disconnect </legacyBold>
          <parameterReference>adStatus, pConnection</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> It describes the error that occurred if the value of <legacyItalic>adStatus </legacyItalic>is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> value that always returns <legacyBold>adStatusOK</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src8" class="srcSentence">When <legacyBold>ConnectComplete</legacyBold> is called, this parameter is set to <legacyBold>adStatusCancel</legacyBold> if a <legacyBold>WillConnect</legacyBold> event has requested cancellation of the pending connection.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src9" class="srcSentence">Before either event returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> However, closing and reopening the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> causes these events to occur again.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src11" class="srcSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src12" class="srcSentence">The <legacyBold>Connection</legacyBold> object for which this event applies.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
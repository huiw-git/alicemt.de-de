---
title: "InfoMessage Event (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 468c87dd-e3bc-4084-9941-94d10743d4e9
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
# InfoMessage Event (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="85078f6d1842833d42c048abeef65554" id="tgt1" class="tgtSentence">The <legacyBold>InfoMessage</legacyBold> event is called whenever a warning occurs during a <legacyBold>ConnectionEvent</legacyBold> operation.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>InfoMessage</legacyBold>
          <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pConnection</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="c53ca6f9660a98f2e3bddd392afe3c26" id="tgt2" class="tgtSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f8547f0cddb40fb6c028ac5705fb05df" id="tgt3" class="tgtSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="10d9b0297070f97e93c7f61ad0228895" id="tgt4" class="tgtSentence"> This parameter contains any errors that are returned.</caps:sentence>
                <caps:sentence sentenceid="6ca5cc1d6825f0f908dbae39c2bac720" id="tgt5" class="tgtSentence"> If multiple errors are returned, enumerate the <legacyBold>Errors</legacyBold> collection to find them.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt6" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt7" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
                <caps:sentence sentenceid="082e0f01e058b537c04bcdeddd2f08cd" id="tgt8" class="tgtSentence"> If a warning occurs, <legacyItalic>adStatus</legacyItalic> is set to <legacyBold>adStatusOK</legacyBold> and the <legacyItalic>pError</legacyItalic> contains the warning.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8985571e1d46609bfa3d241fbd64c1f1" id="tgt9" class="tgtSentence">Before this event returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5f727b94f6dccd2318ee30175b2c25bc" id="tgt10" class="tgtSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="797f40e229d84e753becd0ba7ea841ac" id="tgt11" class="tgtSentence">A <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="9fa335ebc354ce14d434709be769a7de" id="tgt12" class="tgtSentence"> The connection for which the warning occurred.</caps:sentence>
                <caps:sentence sentenceid="6645b6565756a8df6c052b7c2c099c4a" id="tgt13" class="tgtSentence"> For example, warnings can occur when opening a <legacyBold>Connection</legacyBold> object or executing a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> on a <legacyBold>Connection</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>InfoMessage</legacyBold> event is called whenever a warning occurs during a <legacyBold>ConnectionEvent</legacyBold> operation.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>InfoMessage</legacyBold>
          <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pConnection</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> This parameter contains any errors that are returned.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> If multiple errors are returned, enumerate the <legacyBold>Errors</legacyBold> collection to find them.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> If a warning occurs, <legacyItalic>adStatus</legacyItalic> is set to <legacyBold>adStatusOK</legacyBold> and the <legacyItalic>pError</legacyItalic> contains the warning.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src9" class="srcSentence">Before this event returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">A <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> The connection for which the warning occurred.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> For example, warnings can occur when opening a <legacyBold>Connection</legacyBold> object or executing a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> on a <legacyBold>Connection</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
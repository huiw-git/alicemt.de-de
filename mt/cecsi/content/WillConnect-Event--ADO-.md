---
title: "WillConnect Event (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: da561d58-eb58-446c-a4fd-1838c76073c0
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
# WillConnect Event (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="242254f9367d51385944a24ef7b5685e" id="tgt1" class="tgtSentence">The <legacyBold>WillConnect</legacyBold> event is called before a connection starts.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3c8e04723e1b565aa0ba378ebf0d26a7" id="tgt2" class="tgtSentence">
            <embeddedLabel>Applies To:</embeddedLabel> <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link></caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillConnect</legacyBold>
          <parameterReference>ConnectionString, UserID, Password, Options, adStatus, pConnection</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d78656013dfd2e3c848a339806ae4610" id="tgt3" class="tgtSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="1a74403c04c98c653c22243fe3faa400" id="tgt4" class="tgtSentence">A <languageKeyword>String</languageKeyword> that contains connection information for the pending connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5b457185e24aac84a61f0966d85535a8" id="tgt5" class="tgtSentence"> <legacyItalic>UserID</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="6b69256db57adb9d30ab8186d366f21d" id="tgt6" class="tgtSentence">A <languageKeyword>String</languageKeyword> that contains a user name for the pending connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d83fe9057df78601fffb657095e0114f" id="tgt7" class="tgtSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="db4d2a947abc2e48a46837246f283f95" id="tgt8" class="tgtSentence">A <languageKeyword>String</languageKeyword> that contains a password for the pending connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt9" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="12411d9c44a0caa11e902939bf295b11" id="tgt10" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value that indicates how the provider should evaluate the <legacyItalic>ConnectionString</legacyItalic>.</caps:sentence>
                <caps:sentence sentenceid="3d062c2b92d8a85c41ebd836aa6206ad" id="tgt11" class="tgtSentence"> Your only option is <legacyBold>adAsyncOpen</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt12" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt13" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e6efe592c31bbd814f79c6e5bc5b0100" id="tgt14" class="tgtSentence">When this event is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> by default.</caps:sentence>
                <caps:sentence sentenceid="18ddea9776660a7e06950e5b6e998d5c" id="tgt15" class="tgtSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if the event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8985571e1d46609bfa3d241fbd64c1f1" id="tgt16" class="tgtSentence">Before this event returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
                <caps:sentence sentenceid="40b745c4f168080ff7ba9c1b62365c2f" id="tgt17" class="tgtSentence"> Set this parameter to <legacyBold>adStatusCancel</legacyBold> to request the connection operation that caused cancellation of this notification.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5f727b94f6dccd2318ee30175b2c25bc" id="tgt18" class="tgtSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="cfc1b61264c2138e08354353169dda2b" id="tgt19" class="tgtSentence">The <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object for which this event notification applies.</caps:sentence>
                <caps:sentence sentenceid="ef067d5eef662e8a87b68e55657526e2" id="tgt20" class="tgtSentence"> Changes to the parameters of the <legacyBold>Connection</legacyBold> by the <legacyBold>WillConnect</legacyBold> event handler will have no effect on the <legacyBold>Connection</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="acdb4d74117abaf1a5e3a5d84a017a8d" id="tgt21" class="tgtSentence">When <legacyBold>WillConnect</legacyBold> is called, the <legacyItalic>ConnectionString</legacyItalic>, <legacyItalic>UserID</legacyItalic>, <legacyItalic>Password</legacyItalic>, and <legacyItalic>Options</legacyItalic> parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns.</caps:sentence>
            <caps:sentence sentenceid="6240dae00b3c8272944a67104ce29156" id="tgt22" class="tgtSentence">
              <legacyBold>WillConnect</legacyBold> may return a request that the pending connection be canceled.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7807725997dc66cd1b853840ac996ec0" id="tgt23" class="tgtSentence">When this event is canceled, <legacyBold>ConnectComplete</legacyBold> will be called with its <legacyItalic>adStatus </legacyItalic>parameter set to <legacyBold>adStatusErrorsOccurred</legacyBold>.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>WillConnect</legacyBold> event is called before a connection starts.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">
            <embeddedLabel>Applies To:</embeddedLabel> <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link></caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillConnect</legacyBold>
          <parameterReference>ConnectionString, UserID, Password, Options, adStatus, pConnection</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A <languageKeyword>String</languageKeyword> that contains connection information for the pending connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>UserID</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A <languageKeyword>String</languageKeyword> that contains a user name for the pending connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">A <languageKeyword>String</languageKeyword> that contains a password for the pending connection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">A <languageKeyword>Long</languageKeyword> value that indicates how the provider should evaluate the <legacyItalic>ConnectionString</legacyItalic>.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> Your only option is <legacyBold>adAsyncOpen</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src14" class="srcSentence">When this event is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> by default.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> It is set to <legacyBold>adStatusCantDeny</legacyBold> if the event cannot request cancellation of the pending operation.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src16" class="srcSentence">Before this event returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> Set this parameter to <legacyBold>adStatusCancel</legacyBold> to request the connection operation that caused cancellation of this notification.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src18" class="srcSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src19" class="srcSentence">The <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object for which this event notification applies.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> Changes to the parameters of the <legacyBold>Connection</legacyBold> by the <legacyBold>WillConnect</legacyBold> event handler will have no effect on the <legacyBold>Connection</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">When <legacyBold>WillConnect</legacyBold> is called, the <legacyItalic>ConnectionString</legacyItalic>, <legacyItalic>UserID</legacyItalic>, <legacyItalic>Password</legacyItalic>, and <legacyItalic>Options</legacyItalic> parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence">
              <legacyBold>WillConnect</legacyBold> may return a request that the pending connection be canceled.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">When this event is canceled, <legacyBold>ConnectComplete</legacyBold> will be called with its <legacyItalic>adStatus </legacyItalic>parameter set to <legacyBold>adStatusErrorsOccurred</legacyBold>.</caps:sentence>
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
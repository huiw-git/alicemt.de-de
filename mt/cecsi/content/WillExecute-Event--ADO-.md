---
title: "WillExecute Event (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: dd755e46-f589-48a3-93a9-51ff998d44b5
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
# WillExecute Event (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="718e9f211e8e261806afc2a54739aecd" id="tgt1" class="tgtSentence">The <legacyBold>WillExecute</legacyBold> event is called just before a pending command executes on a connection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillExecute Source, CursorType, LockType, Options, adStatus, pCommand, pRecordset, pConnection</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="b86002c905ed82eb6c9ab27bfdb86afd" id="tgt2" class="tgtSentence"> <legacyItalic>Source</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="55331084ebe06294ccdb789e8075456b" id="tgt3" class="tgtSentence">A <legacyBold>String</legacyBold> that contains an SQL command or a stored procedure name.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a273f6ee95bdfedf2da25b6463963c4e" id="tgt4" class="tgtSentence"> <legacyItalic>CursorType</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="81d2512b8c7b8bf9648b7c1af5a2ddb5" id="tgt5" class="tgtSentence">A <link xlink:href="ffc6e245-4471-42ae-84dd-e85bddfce983">CursorTypeEnum</link> that contains the type of cursor for the <legacyBold>Recordset</legacyBold> that will be opened.</caps:sentence>
                <caps:sentence sentenceid="2c17b851b5a4cf37dbadc479dc217812" id="tgt6" class="tgtSentence"> With this parameter, you can change the cursor to any type during a <legacyBold>Recordset</legacyBold> <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> operation.</caps:sentence>
                <caps:sentence sentenceid="1fdb2b9f7c0749f5c30517fd688b01b4" id="tgt7" class="tgtSentence">
                  <legacyItalic>CursorType</legacyItalic> will be ignored for any other operation.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="2f911df9a5a60c73393585db9d3f960d" id="tgt8" class="tgtSentence"> <legacyItalic>LockType </legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="2c80503b3896a2d6347efdfa77b460e5" id="tgt9" class="tgtSentence">A <link xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</link> that contains the lock type for the <legacyBold>Recordset</legacyBold> that will be opened.</caps:sentence>
                <caps:sentence sentenceid="bff4d806ee61c554314c04c541d04ed4" id="tgt10" class="tgtSentence"> With this parameter, you can change the lock to any type during a <legacyBold>Recordset</legacyBold> <legacyBold>Open</legacyBold> operation.</caps:sentence>
                <caps:sentence sentenceid="3fbaff6afe383ea65ebb3baf90c7f13f" id="tgt11" class="tgtSentence">
                  <legacyItalic>LockType</legacyItalic> will be ignored for any other operation.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt12" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="6be57d101e453dc545f0945ac9a9b79a" id="tgt13" class="tgtSentence">A <legacyBold>Long</legacyBold> value that indicates options that can be used to execute the command or open the <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt14" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="2f4581b9dec2e7a4fe6f5d41526374bc" id="tgt15" class="tgtSentence">An <link xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</link> status value that may be <legacyBold>adStatusCantDeny</legacyBold> or <legacyBold>adStatusOK</legacyBold> when this event is called.</caps:sentence>
                <caps:sentence sentenceid="688ab546d40b78c73d84127efa7d7b1d" id="tgt16" class="tgtSentence"> If it is <legacyBold>adStatusCantDeny</legacyBold>, this event may not request cancellation of the pending operation.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5394b8297011941c03c77aa2932cdf9e" id="tgt17" class="tgtSentence"> <legacyItalic>pCommand </legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f55b0b1b7f40111de43b528ef7393bbd" id="tgt18" class="tgtSentence">The <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object_ADO</link> object for which this event notification applies.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="9f4e8ca16886f6377c992d99ff161eee" id="tgt19" class="tgtSentence"> <legacyItalic>pRecordset </legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="2a12c7f75d3e8c471c7902231c10208f" id="tgt20" class="tgtSentence">The <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link> object for which this event notification applies.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="278b61cd5092c800cb987f4739f2ac5c" id="tgt21" class="tgtSentence"> <legacyItalic>pConnection </legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="73f998bdf820c6e3a745ab028d6d5b2c" id="tgt22" class="tgtSentence">The <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object_ADO</link> object for which this event notification applies.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="fefe95f4ce6c0ae525f6d7d3a0d87736" id="tgt23" class="tgtSentence">A <legacyBold>WillExecute</legacyBold> event may occur due to a Connection.</caps:sentence>
            <caps:sentence sentenceid="4d3d9584a9f0871c15b6e9a9cce1ae75" id="tgt24" class="tgtSentence">
              <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>, <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>, or <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> method The <legacyItalic>pConnection</legacyItalic> parameter should always contain a valid reference to a <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="37d64f56150a2c35731b049c23f5c378" id="tgt25" class="tgtSentence"> If the event is due to <legacyBold>Connection.Execute</legacyBold>, the <legacyItalic>pRecordset</legacyItalic> and <legacyItalic>pCommand</legacyItalic> parameters are set to <legacyBold>Nothing</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="b2ced7109d78bba0ec3789544af3e122" id="tgt26" class="tgtSentence"> If the event is due to <legacyBold>Recordset.Open</legacyBold>, the <legacyItalic>pRecordset</legacyItalic> parameter will reference the <legacyBold>Recordset</legacyBold> object and the <legacyItalic>pCommand</legacyItalic> parameter is set to <legacyBold>Nothing</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="3d019bd7f44d249727d40a56def288f7" id="tgt27" class="tgtSentence"> If the event is due to <legacyBold>Command.Execute</legacyBold>, the <legacyItalic>pCommand</legacyItalic> parameter will reference the <legacyBold>Command</legacyBold> object and the <legacyItalic>pRecordset</legacyItalic> parameter is set to <legacyBold>Nothing</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="454a4bfb1da665c9cacb679c733738a8" id="tgt28" class="tgtSentence">
              <legacyBold>WillExecute</legacyBold> allows you to examine and modify the pending execution parameters.</caps:sentence>
            <caps:sentence sentenceid="7a244796cffd30854ac2a2a13b12b989" id="tgt29" class="tgtSentence"> This event may return a request that the pending command be canceled.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="42bf3d8bab08cf3451c6769ebad860ed" id="tgt30" class="tgtSentence">If the original source for a <legacyBold>Command</legacyBold> is a stream specified by the <link xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream Property (ADO)</link> property, assigning a new string to the <legacyBold>WillExecute</legacyBold> <legacyItalic>Source</legacyItalic> parameter changes the source of the <legacyBold>Command</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="601737adcfa26e30c1c09d04e595431d" id="tgt31" class="tgtSentence"> The <legacyBold>CommandStream</legacyBold> property will be cleared and the <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property (ADO)</link> property will be updated with the new source.</caps:sentence>
              <caps:sentence sentenceid="95cc2d7be1a745c9948be4b9e6faf3ef" id="tgt32" class="tgtSentence"> The original stream specified by <legacyBold>CommandStream</legacyBold> will be released and cannot be accessed.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="26bfab9218bf3b44d11b4d939647b89d" id="tgt33" class="tgtSentence">If the dialect of the new source string differs from the original setting of the <link xlink:href="329c3a71-ba88-4009-b04f-2f52195a5957">Dialect Property</link> property (which corresponded to the <legacyBold>CommandStream</legacyBold>), the correct dialect must be specified by setting the <legacyBold>Dialect</legacyBold> property of the command object referenced by <legacyItalic>pCommand</legacyItalic>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">ADO Events Model Example (VC++)</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object_ADO</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>WillExecute</legacyBold> event is called just before a pending command executes on a connection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>WillExecute Source, CursorType, LockType, Options, adStatus, pCommand, pRecordset, pConnection</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Source</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <legacyBold>String</legacyBold> that contains an SQL command or a stored procedure name.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>CursorType</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">A <link xlink:href="ffc6e245-4471-42ae-84dd-e85bddfce983">CursorTypeEnum</link> that contains the type of cursor for the <legacyBold>Recordset</legacyBold> that will be opened.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> With this parameter, you can change the cursor to any type during a <legacyBold>Recordset</legacyBold> <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> operation.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence">
                  <legacyItalic>CursorType</legacyItalic> will be ignored for any other operation.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>LockType </legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">A <link xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</link> that contains the lock type for the <legacyBold>Recordset</legacyBold> that will be opened.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> With this parameter, you can change the lock to any type during a <legacyBold>Recordset</legacyBold> <legacyBold>Open</legacyBold> operation.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence">
                  <legacyItalic>LockType</legacyItalic> will be ignored for any other operation.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">A <legacyBold>Long</legacyBold> value that indicates options that can be used to execute the command or open the <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src14" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src15" class="srcSentence">An <link xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</link> status value that may be <legacyBold>adStatusCantDeny</legacyBold> or <legacyBold>adStatusOK</legacyBold> when this event is called.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> If it is <legacyBold>adStatusCantDeny</legacyBold>, this event may not request cancellation of the pending operation.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src17" class="srcSentence"> <legacyItalic>pCommand </legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src18" class="srcSentence">The <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object_ADO</link> object for which this event notification applies.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src19" class="srcSentence"> <legacyItalic>pRecordset </legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src20" class="srcSentence">The <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link> object for which this event notification applies.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src21" class="srcSentence"> <legacyItalic>pConnection </legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src22" class="srcSentence">The <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object_ADO</link> object for which this event notification applies.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src23" class="srcSentence">A <legacyBold>WillExecute</legacyBold> event may occur due to a Connection.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence">
              <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>, <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>, or <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> method The <legacyItalic>pConnection</legacyItalic> parameter should always contain a valid reference to a <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> If the event is due to <legacyBold>Connection.Execute</legacyBold>, the <legacyItalic>pRecordset</legacyItalic> and <legacyItalic>pCommand</legacyItalic> parameters are set to <legacyBold>Nothing</legacyBold>.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> If the event is due to <legacyBold>Recordset.Open</legacyBold>, the <legacyItalic>pRecordset</legacyItalic> parameter will reference the <legacyBold>Recordset</legacyBold> object and the <legacyItalic>pCommand</legacyItalic> parameter is set to <legacyBold>Nothing</legacyBold>.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> If the event is due to <legacyBold>Command.Execute</legacyBold>, the <legacyItalic>pCommand</legacyItalic> parameter will reference the <legacyBold>Command</legacyBold> object and the <legacyItalic>pRecordset</legacyItalic> parameter is set to <legacyBold>Nothing</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">
              <legacyBold>WillExecute</legacyBold> allows you to examine and modify the pending execution parameters.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> This event may return a request that the pending command be canceled.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src30" class="srcSentence">If the original source for a <legacyBold>Command</legacyBold> is a stream specified by the <link xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream Property (ADO)</link> property, assigning a new string to the <legacyBold>WillExecute</legacyBold> <legacyItalic>Source</legacyItalic> parameter changes the source of the <legacyBold>Command</legacyBold>.</caps:sentence>
              <caps:sentence id="src31" class="srcSentence"> The <legacyBold>CommandStream</legacyBold> property will be cleared and the <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property (ADO)</link> property will be updated with the new source.</caps:sentence>
              <caps:sentence id="src32" class="srcSentence"> The original stream specified by <legacyBold>CommandStream</legacyBold> will be released and cannot be accessed.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src33" class="srcSentence">If the dialect of the new source string differs from the original setting of the <link xlink:href="329c3a71-ba88-4009-b04f-2f52195a5957">Dialect Property</link> property (which corresponded to the <legacyBold>CommandStream</legacyBold>), the correct dialect must be specified by setting the <legacyBold>Dialect</legacyBold> property of the command object referenced by <legacyItalic>pCommand</legacyItalic>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">ADO Events Model Example (VC++)</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object_ADO</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
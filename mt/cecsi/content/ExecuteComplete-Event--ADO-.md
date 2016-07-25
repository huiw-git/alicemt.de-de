---
title: "ExecuteComplete Event (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 62470d42-e511-494c-bec4-ad4591734b7b
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
# ExecuteComplete Event (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6d304824cc37993162f87ec6f2e29772" id="tgt1" class="tgtSentence">The <legacyBold>ExecuteComplete </legacyBold>event is called after a command has finished executing.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>ExecuteComplete</legacyBold>
          <parameterReference>RecordsAffected</parameterReference>, <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pCommand</parameterReference>, <parameterReference>pRecordset</parameterReference>, <parameterReference>pConnection</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7818b1bda08fe42f7ac5dcd9cc7471dc" id="tgt2" class="tgtSentence"> <legacyItalic>RecordsAffected</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="97427743176e3a28ef0a1a9712c07342" id="tgt3" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value indicating the number of records affected by the command.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c53ca6f9660a98f2e3bddd392afe3c26" id="tgt4" class="tgtSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f8547f0cddb40fb6c028ac5705fb05df" id="tgt5" class="tgtSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="2293462f9188d996fcdacbc2e8fc1c94" id="tgt6" class="tgtSentence"> It describes the error that occurred if the value of <legacyBold>adStatus</legacyBold> is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda6b14f9e80afe763b226db4bdbc27b" id="tgt7" class="tgtSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt8" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
                <caps:sentence sentenceid="ef21ca19734d9ff419b93e1cb5a3228c" id="tgt9" class="tgtSentence"> When this event is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8985571e1d46609bfa3d241fbd64c1f1" id="tgt10" class="tgtSentence">Before this event returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="423822ba3d5792f5f0410bc0c9d1fae1" id="tgt11" class="tgtSentence"> <legacyItalic>pCommand</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="479e2a00fc5c440a285b19a2d1ad722c" id="tgt12" class="tgtSentence">The <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object that was executed.</caps:sentence>
                <caps:sentence sentenceid="a6d9dcae0fef398690df828998f34830" id="tgt13" class="tgtSentence"> Contains a <legacyBold>Command</legacyBold> object even when calling <legacyBold>Connection.Execute</legacyBold> or <legacyBold>Recordset.Open</legacyBold> without explicitly creating a <legacyBold>Command</legacyBold>, in which cases the <legacyBold>Command</legacyBold> object is created internally by ADO.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c294ce2e8a8edf29ce067cff9e0573d5" id="tgt14" class="tgtSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="cc0567cf470be7f93cffcc0ac6b9e436" id="tgt15" class="tgtSentence">A <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object that is the result of the executed command.</caps:sentence>
                <caps:sentence sentenceid="af15e58fcc1538b66cf7c4c818621d0a" id="tgt16" class="tgtSentence"> This <legacyBold>Recordset</legacyBold> may be empty.</caps:sentence>
                <caps:sentence sentenceid="8459bd0a5c0aaa519bf7429028bbe261" id="tgt17" class="tgtSentence"> You should never destroy this Recordset object from within this event handler.</caps:sentence>
                <caps:sentence sentenceid="a3cd0e10d4b1d89eda2ded57e32197b2" id="tgt18" class="tgtSentence"> Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5f727b94f6dccd2318ee30175b2c25bc" id="tgt19" class="tgtSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="797f40e229d84e753becd0ba7ea841ac" id="tgt20" class="tgtSentence">A <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="d771510c2b8a31515e3d0602f923a2f7" id="tgt21" class="tgtSentence"> The connection over which the operation was executed.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="c25663cbf9000383dbb66e7bef6cf77e" id="tgt22" class="tgtSentence">An <legacyBold>ExecuteComplete</legacyBold> event may occur due to the <legacyBold>Connection.</legacyBold><legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink>, <legacyBold>Command.</legacyBold><legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink>, <legacyBold>Recordset.</legacyBold><legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink>, <legacyBold>Recordset.</legacyBold><legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink>, or <legacyBold>Recordset.</legacyBold><legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink> methods.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>ExecuteComplete </legacyBold>event is called after a command has finished executing.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>ExecuteComplete</legacyBold>
          <parameterReference>RecordsAffected</parameterReference>, <parameterReference>pError</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pCommand</parameterReference>, <parameterReference>pRecordset</parameterReference>, <parameterReference>pConnection</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>RecordsAffected</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>Long</languageKeyword> value indicating the number of records affected by the command.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>pError</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">An <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> It describes the error that occurred if the value of <legacyBold>adStatus</legacyBold> is <legacyBold>adStatusErrorsOccurred</legacyBold>; otherwise it is not set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>adStatus</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> When this event is called, this parameter is set to <legacyBold>adStatusOK</legacyBold> if the operation that caused the event was successful, or to <legacyBold>adStatusErrorsOccurred</legacyBold> if the operation failed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src10" class="srcSentence">Before this event returns, set this parameter to <legacyBold>adStatusUnwantedEvent</legacyBold> to prevent subsequent notifications.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src11" class="srcSentence"> <legacyItalic>pCommand</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src12" class="srcSentence">The <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object that was executed.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> Contains a <legacyBold>Command</legacyBold> object even when calling <legacyBold>Connection.Execute</legacyBold> or <legacyBold>Recordset.Open</legacyBold> without explicitly creating a <legacyBold>Command</legacyBold>, in which cases the <legacyBold>Command</legacyBold> object is created internally by ADO.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src14" class="srcSentence"> <legacyItalic>pRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src15" class="srcSentence">A <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object that is the result of the executed command.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> This <legacyBold>Recordset</legacyBold> may be empty.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> You should never destroy this Recordset object from within this event handler.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src19" class="srcSentence"> <legacyItalic>pConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src20" class="srcSentence">A <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> The connection over which the operation was executed.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src22" class="srcSentence">An <legacyBold>ExecuteComplete</legacyBold> event may occur due to the <legacyBold>Connection.</legacyBold><legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink>, <legacyBold>Command.</legacyBold><legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink>, <legacyBold>Recordset.</legacyBold><legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink>, <legacyBold>Recordset.</legacyBold><legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink>, or <legacyBold>Recordset.</legacyBold><legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink> methods.</caps:sentence>
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
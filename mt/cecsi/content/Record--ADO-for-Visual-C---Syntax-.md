---
title: "Record (ADO for Visual C++ Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: c4ce8532-a4d8-4f74-9488-9389b6695958
caps.latest.revision: 9
caps.handback.revision: 9
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
# Record (ADO for Visual C++ Syntax)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt1" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <code>Cancel(void)
Close(void)
CopyRecord(BSTR Source, BSTR Destination, BSTR UserName, BSTR Password, CopyRecordOptionsEnum Options, VARIANT_BOOL Async, BSTR *pbstrNewURL)
DeleteRecord(BSTR Source, VARIANT_BOOL Async)
GetChildren(_ADORecordset **ppRSet)
MoveRecord(BSTR Source, BSTR Destination, BSTR UserName, BSTR Password, MoveRecordOptionsEnum Options, VARIANT_BOOL Async, BSTR *pbstrNewURL)
Open(VARIANT Source, VARIANT ActiveConnection, ConnectModeEnum Mode, RecordCreateOptionsEnum CreateOptions, RecordOpenOptionsEnum Options, BSTR UserName, BSTR Password)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt2" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>get_ActiveConnection(VARIANT *pvar)
put_ActiveConnection(BSTR bstrConn)
putref_ActiveConnection(_ADOConnection *Con)
get_Fields(ADOFields **ppFlds)
get_Mode(ConnectModeEnum *pMode)
put_Mode(ConnectModeEnum Mode)
get_ParentURL(BSTR *pbstrParentURL)
get_RecordType(RecordTypeEnum *pType)
get_Source(VARIANT *pvar)
put_Source(BSTR Source)
putref_Source(IDispatch *Source)
get_State(ObjectStateEnum *pState)</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <code>Cancel(void)
Close(void)
CopyRecord(BSTR Source, BSTR Destination, BSTR UserName, BSTR Password, CopyRecordOptionsEnum Options, VARIANT_BOOL Async, BSTR *pbstrNewURL)
DeleteRecord(BSTR Source, VARIANT_BOOL Async)
GetChildren(_ADORecordset **ppRSet)
MoveRecord(BSTR Source, BSTR Destination, BSTR UserName, BSTR Password, MoveRecordOptionsEnum Options, VARIANT_BOOL Async, BSTR *pbstrNewURL)
Open(VARIANT Source, VARIANT ActiveConnection, ConnectModeEnum Mode, RecordCreateOptionsEnum CreateOptions, RecordOpenOptionsEnum Options, BSTR UserName, BSTR Password)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>get_ActiveConnection(VARIANT *pvar)
put_ActiveConnection(BSTR bstrConn)
putref_ActiveConnection(_ADOConnection *Con)
get_Fields(ADOFields **ppFlds)
get_Mode(ConnectModeEnum *pMode)
put_Mode(ConnectModeEnum Mode)
get_ParentURL(BSTR *pbstrParentURL)
get_RecordType(RecordTypeEnum *pType)
get_Source(VARIANT *pvar)
put_Source(BSTR Source)
putref_Source(IDispatch *Source)
get_State(ObjectStateEnum *pState)</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
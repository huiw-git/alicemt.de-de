---
title: "Command (ADO for Visual C++ Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: cf12cbd1-25f7-4bb5-aa94-0fe823b3b6d6
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
# Command (ADO for Visual C++ Syntax)
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
CreateParameter(BSTR Name, DataTypeEnum Type, ParameterDirectionEnum Direction, long Size, VARIANT Value, _ADOParameter **ppiprm)
Execute(VARIANT *RecordsAffected, VARIANT *Parameters, long Options, _ADORecordset **ppirs)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt2" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>get_ActiveConnection(_ADOConnection **ppvObject)
put_ActiveConnection(VARIANT vConn)
putref_ActiveConnection(_ADOConnection *pCon)
get_CommandText(BSTR *pbstr)
put_CommandText(BSTR bstr)
get_CommandTimeout(LONG *pl)
put_CommandTimeout(LONG Timeout)
get_CommandType(CommandTypeEnum *plCmdType)
put_CommandType(CommandTypeEnum lCmdType)
get_Name(BSTR *pbstrName)
put_Name(BSTR bstrName)
get_Prepared(VARIANT_BOOL *pfPrepared)
put_Prepared(VARIANT_BOOL fPrepared)
get_State(LONG *plObjState)
get_Parameters(ADOParameters **ppvObject)</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
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
CreateParameter(BSTR Name, DataTypeEnum Type, ParameterDirectionEnum Direction, long Size, VARIANT Value, _ADOParameter **ppiprm)
Execute(VARIANT *RecordsAffected, VARIANT *Parameters, long Options, _ADORecordset **ppirs)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>get_ActiveConnection(_ADOConnection **ppvObject)
put_ActiveConnection(VARIANT vConn)
putref_ActiveConnection(_ADOConnection *pCon)
get_CommandText(BSTR *pbstr)
put_CommandText(BSTR bstr)
get_CommandTimeout(LONG *pl)
put_CommandTimeout(LONG Timeout)
get_CommandType(CommandTypeEnum *plCmdType)
put_CommandType(CommandTypeEnum lCmdType)
get_Name(BSTR *pbstrName)
put_Name(BSTR bstrName)
get_Prepared(VARIANT_BOOL *pfPrepared)
put_Prepared(VARIANT_BOOL fPrepared)
get_State(LONG *plObjState)
get_Parameters(ADOParameters **ppvObject)</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
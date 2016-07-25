---
title: "Command (Visual C++ Syntax Index with #import)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ccb6ffbc-7303-4124-8a0c-f6356f2c82d9
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
# Command (Visual C++ Syntax Index with #import)
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
          <code>HRESULT Cancel( );
_RecordsetPtr Execute( VARIANT * RecordsAffected, VARIANT * Parameters, long Options );
_ParameterPtr CreateParameter( _bstr_t Name, enum DataTypeEnum Type, enum ParameterDirectionEnum Direction, long Size, const _variant_t &amp; Value = vtMissing );</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt2" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>_ConnectionPtr GetActiveConnection( );
void PutRefActiveConnection( struct _Connection * ppvObject );
void PutActiveConnection( const _variant_t &amp; ppvObject ); __declspec(property(get=GetActiveConnection,put=PutRefActiveConnection)) _ConnectionPtr ActiveConnection;
_bstr_t GetCommandText( );
void PutCommandText( _bstr_t pbstr );
__declspec(property(get=GetCommandText,put=PutCommandText)) _bstr_t
    CommandText;
long GetCommandTimeout( );
void PutCommandTimeout( long pl );
__declspec(property(get=GetCommandTimeout,put=PutCommandTimeout)) long CommandTimeout;
void PutCommandType( enum CommandTypeEnum plCmdType );
enum CommandTypeEnum GetCommandType( );
__declspec(property(get=GetCommandType,put=PutCommandType)) enum CommandTypeEnum CommandType;
VARIANT_BOOL GetPrepared( );
void PutPrepared( VARIANT_BOOL pfPrepared );
__declspec(property(get=GetPrepared,put=PutPrepared)) VARIANT_BOOL Prepared;
ParametersPtr GetParameters( );
__declspec(property(get=GetParameters)) ParametersPtr Parameters;
_bstr_t GetName( );
void PutName( _bstr_t pbstrName );
__declspec(property(get=GetName,put=PutName)) _bstr_t Name;
long GetState( );
__declspec(property(get=GetState)) long State;</code>
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
          <code>HRESULT Cancel( );
_RecordsetPtr Execute( VARIANT * RecordsAffected, VARIANT * Parameters, long Options );
_ParameterPtr CreateParameter( _bstr_t Name, enum DataTypeEnum Type, enum ParameterDirectionEnum Direction, long Size, const _variant_t &amp; Value = vtMissing );</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>_ConnectionPtr GetActiveConnection( );
void PutRefActiveConnection( struct _Connection * ppvObject );
void PutActiveConnection( const _variant_t &amp; ppvObject ); __declspec(property(get=GetActiveConnection,put=PutRefActiveConnection)) _ConnectionPtr ActiveConnection;
_bstr_t GetCommandText( );
void PutCommandText( _bstr_t pbstr );
__declspec(property(get=GetCommandText,put=PutCommandText)) _bstr_t
    CommandText;
long GetCommandTimeout( );
void PutCommandTimeout( long pl );
__declspec(property(get=GetCommandTimeout,put=PutCommandTimeout)) long CommandTimeout;
void PutCommandType( enum CommandTypeEnum plCmdType );
enum CommandTypeEnum GetCommandType( );
__declspec(property(get=GetCommandType,put=PutCommandType)) enum CommandTypeEnum CommandType;
VARIANT_BOOL GetPrepared( );
void PutPrepared( VARIANT_BOOL pfPrepared );
__declspec(property(get=GetPrepared,put=PutPrepared)) VARIANT_BOOL Prepared;
ParametersPtr GetParameters( );
__declspec(property(get=GetParameters)) ParametersPtr Parameters;
_bstr_t GetName( );
void PutName( _bstr_t pbstrName );
__declspec(property(get=GetName,put=PutName)) _bstr_t Name;
long GetState( );
__declspec(property(get=GetState)) long State;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Connection (Visual C++ Syntax Index with #import)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 03f47eda-840d-4cab-83d9-ccddd873f342
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
# Connection (Visual C++ Syntax Index with #import)
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
HRESULT Close( );
_RecordsetPtr Execute( _bstr_t CommandText, VARIANT *
    RecordsAffected,     long Options );
long BeginTrans( );
HRESULT CommitTrans( );
HRESULT RollbackTrans( );
HRESULT Open( _bstr_t ConnectionString, _bstr_t UserID,
    _bstr_t Password,     long Options );
_RecordsetPtr OpenSchema( enum SchemaEnum Schema, const
    _variant_t &amp;     Restrictions = vtMissing, const _variant_t &amp; 
    SchemaID = vtMissing );</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt2" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>_bstr_t GetConnectionString( );
void PutConnectionString( _bstr_t pbstr );
__declspec(property(get=GetConnectionString,put=PutConnectionString))
    _bstr_t ConnectionString;
long GetCommandTimeout( );
void PutCommandTimeout( long plTimeout );
__declspec(property(get=GetCommandTimeout,put=PutCommandTimeout)) long
    CommandTimeout;
long GetConnectionTimeout( );
void PutConnectionTimeout( long plTimeout );
__declspec(property(get=GetConnectionTimeout,put=PutConnectionTimeout))
    long ConnectionTimeout;
_bstr_t GetVersion( );
__declspec(property(get=GetVersion)) _bstr_t Version;
ErrorsPtr GetErrors( );
__declspec(property(get=GetErrors)) ErrorsPtr Errors;
_bstr_t GetDefaultDatabase( );
void PutDefaultDatabase( _bstr_t pbstr );
__declspec(property(get=GetDefaultDatabase,put=PutDefaultDatabase))
    _bstr_t DefaultDatabase;
enum IsolationLevelEnum GetIsolationLevel( );
void PutIsolationLevel( enum IsolationLevelEnum Level );
__declspec(property(get=GetIsolationLevel,put=PutIsolationLevel)) enum
    IsolationLevelEnum IsolationLevel;
long GetAttributes( );
void PutAttributes( long plAttr );
__declspec(property(get=GetAttributes,put=PutAttributes)) long
    Attributes;
enum CursorLocationEnum GetCursorLocation( );
void PutCursorLocation( enum CursorLocationEnum plCursorLoc );
__declspec(property(get=GetCursorLocation,put=PutCursorLocation)) enum
    CursorLocationEnum CursorLocation;
enum ConnectModeEnum GetMode( );
void PutMode( enum ConnectModeEnum plMode );
__declspec(property(get=GetMode,put=PutMode)) enum ConnectModeEnum
    Mode;
_bstr_t GetProvider( );
void PutProvider( _bstr_t pbstr );
__declspec(property(get=GetProvider,put=PutProvider)) _bstr_t
    Provider;
long GetState( );
__declspec(property(get=GetState)) long State;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
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
HRESULT Close( );
_RecordsetPtr Execute( _bstr_t CommandText, VARIANT *
    RecordsAffected,     long Options );
long BeginTrans( );
HRESULT CommitTrans( );
HRESULT RollbackTrans( );
HRESULT Open( _bstr_t ConnectionString, _bstr_t UserID,
    _bstr_t Password,     long Options );
_RecordsetPtr OpenSchema( enum SchemaEnum Schema, const
    _variant_t &amp;     Restrictions = vtMissing, const _variant_t &amp; 
    SchemaID = vtMissing );</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>_bstr_t GetConnectionString( );
void PutConnectionString( _bstr_t pbstr );
__declspec(property(get=GetConnectionString,put=PutConnectionString))
    _bstr_t ConnectionString;
long GetCommandTimeout( );
void PutCommandTimeout( long plTimeout );
__declspec(property(get=GetCommandTimeout,put=PutCommandTimeout)) long
    CommandTimeout;
long GetConnectionTimeout( );
void PutConnectionTimeout( long plTimeout );
__declspec(property(get=GetConnectionTimeout,put=PutConnectionTimeout))
    long ConnectionTimeout;
_bstr_t GetVersion( );
__declspec(property(get=GetVersion)) _bstr_t Version;
ErrorsPtr GetErrors( );
__declspec(property(get=GetErrors)) ErrorsPtr Errors;
_bstr_t GetDefaultDatabase( );
void PutDefaultDatabase( _bstr_t pbstr );
__declspec(property(get=GetDefaultDatabase,put=PutDefaultDatabase))
    _bstr_t DefaultDatabase;
enum IsolationLevelEnum GetIsolationLevel( );
void PutIsolationLevel( enum IsolationLevelEnum Level );
__declspec(property(get=GetIsolationLevel,put=PutIsolationLevel)) enum
    IsolationLevelEnum IsolationLevel;
long GetAttributes( );
void PutAttributes( long plAttr );
__declspec(property(get=GetAttributes,put=PutAttributes)) long
    Attributes;
enum CursorLocationEnum GetCursorLocation( );
void PutCursorLocation( enum CursorLocationEnum plCursorLoc );
__declspec(property(get=GetCursorLocation,put=PutCursorLocation)) enum
    CursorLocationEnum CursorLocation;
enum ConnectModeEnum GetMode( );
void PutMode( enum ConnectModeEnum plMode );
__declspec(property(get=GetMode,put=PutMode)) enum ConnectModeEnum
    Mode;
_bstr_t GetProvider( );
void PutProvider( _bstr_t pbstr );
__declspec(property(get=GetProvider,put=PutProvider)) _bstr_t
    Provider;
long GetState( );
__declspec(property(get=GetState)) long State;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
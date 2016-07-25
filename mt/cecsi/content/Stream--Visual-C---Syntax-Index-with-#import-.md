---
title: "Stream (Visual C++ Syntax Index with #import)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e59d0687-1f5a-45c5-9d0a-c1f27079495d
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
# Stream (Visual C++ Syntax Index with #import)
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

HRESULT CopyTo( struct _Stream * DestStream, int CharNumber );

HRESULT Flush( );

HRESULT LoadFromFile( _bstr_t FileName );

HRESULT Open( const _variant_t &amp; Source, enum
    ConnectModeEnum Mode, enum     StreamOpenOptionsEnum Options, _bstr_t
    UserName, _bstr_t Password );

_variant_t Read( long NumBytes );

_bstr_t ReadText( long NumChars );

HRESULT SaveToFile( _bstr_t FileName, enum SaveOptionsEnum
    Options );

HRESULT SetEOS( );

HRESULT SkipLine( );

HRESULT Write( const _variant_t &amp; Buffer );

HRESULT WriteText( _bstr_t Data, enum StreamWriteEnum
    Options );</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt2" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>_bstr_t GetCharset( );
void PutCharset( _bstr_t pbstrCharset );
__declspec(property(get=GetCharset,put=PutCharset)) _bstr_t Charset;

VARIANT_BOOL GetEOS( );
__declspec(property(get=GetEOS)) VARIANT_BOOL EOS;

enum LineSeparatorEnum GetLineSeparator( );
void PutLineSeparator( enum LineSeparatorEnum pLS );
__declspec(property(get=GetLineSeparator,put=PutLineSeparator)) enum
    LineSeparatorEnum LineSeparator;

enum ConnectModeEnum GetMode( );
void PutMode( enum ConnectModeEnum pMode );
__declspec(property(get=GetMode,put=PutMode)) enum ConnectModeEnum Mode;

long GetPosition( );
void PutPosition( long pPos );
__declspec(property(get=GetPosition,put=PutPosition)) long Position;

long GetSize( );
__declspec(property(get=GetSize)) long Size;

enum ObjectStateEnum GetState( );
__declspec(property(get=GetState)) enum ObjectStateEnum State;

enum StreamTypeEnum GetType( );
void PutType( enum StreamTypeEnum ptype );
__declspec(property(get=GetType,put=PutType)) enum StreamTypeEnum Type;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
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

HRESULT CopyTo( struct _Stream * DestStream, int CharNumber );

HRESULT Flush( );

HRESULT LoadFromFile( _bstr_t FileName );

HRESULT Open( const _variant_t &amp; Source, enum
    ConnectModeEnum Mode, enum     StreamOpenOptionsEnum Options, _bstr_t
    UserName, _bstr_t Password );

_variant_t Read( long NumBytes );

_bstr_t ReadText( long NumChars );

HRESULT SaveToFile( _bstr_t FileName, enum SaveOptionsEnum
    Options );

HRESULT SetEOS( );

HRESULT SkipLine( );

HRESULT Write( const _variant_t &amp; Buffer );

HRESULT WriteText( _bstr_t Data, enum StreamWriteEnum
    Options );</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>_bstr_t GetCharset( );
void PutCharset( _bstr_t pbstrCharset );
__declspec(property(get=GetCharset,put=PutCharset)) _bstr_t Charset;

VARIANT_BOOL GetEOS( );
__declspec(property(get=GetEOS)) VARIANT_BOOL EOS;

enum LineSeparatorEnum GetLineSeparator( );
void PutLineSeparator( enum LineSeparatorEnum pLS );
__declspec(property(get=GetLineSeparator,put=PutLineSeparator)) enum
    LineSeparatorEnum LineSeparator;

enum ConnectModeEnum GetMode( );
void PutMode( enum ConnectModeEnum pMode );
__declspec(property(get=GetMode,put=PutMode)) enum ConnectModeEnum Mode;

long GetPosition( );
void PutPosition( long pPos );
__declspec(property(get=GetPosition,put=PutPosition)) long Position;

long GetSize( );
__declspec(property(get=GetSize)) long Size;

enum ObjectStateEnum GetState( );
__declspec(property(get=GetState)) enum ObjectStateEnum State;

enum StreamTypeEnum GetType( );
void PutType( enum StreamTypeEnum ptype );
__declspec(property(get=GetType,put=PutType)) enum StreamTypeEnum Type;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
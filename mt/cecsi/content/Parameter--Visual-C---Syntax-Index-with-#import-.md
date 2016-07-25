---
title: "Parameter (Visual C++ Syntax Index with #import)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6b43cf70-9695-47b0-9e68-f36898859b6b
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
# Parameter (Visual C++ Syntax Index with #import)
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
          <code>HRESULT AppendChunk( const _variant_t &amp; Val );</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt2" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>long GetAttributes( );
void PutAttributes( long plParmAttribs );
__declspec(property(get=GetAttributes,put=PutAttributes)) long
    Attributes;

enum ParameterDirectionEnum GetDirection( );
void PutDirection( enum ParameterDirectionEnum plParmDirection );
__declspec(property(get=GetDirection,put=PutDirection)) enum
    ParameterDirectionEnum Direction;

_bstr_t GetName( );
void PutName( _bstr_t pbstr );
__declspec(property(get=GetName,put=PutName)) _bstr_t Name;

unsigned char GetNumericScale( );
void PutNumericScale( unsigned char pbScale );
__declspec(property(get=GetNumericScale,put=PutNumericScale)) unsigned
    char NumericScale;

unsigned char GetPrecision( );
void PutPrecision( unsigned char pbPrecision );
__declspec(property(get=GetPrecision,put=PutPrecision)) unsigned char
    Precision;

long GetSize( );
void PutSize( long pl );
__declspec(property(get=GetSize,put=PutSize)) long Size;

enum DataTypeEnum GetType( );
void PutType( enum DataTypeEnum psDataType );
__declspec(property(get=GetType,put=PutType)) enum DataTypeEnum Type;

_variant_t GetValue( );
void PutValue( const _variant_t &amp; pvar );
__declspec(property(get=GetValue,put=PutValue)) _variant_t Value;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
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
          <code>HRESULT AppendChunk( const _variant_t &amp; Val );</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>long GetAttributes( );
void PutAttributes( long plParmAttribs );
__declspec(property(get=GetAttributes,put=PutAttributes)) long
    Attributes;

enum ParameterDirectionEnum GetDirection( );
void PutDirection( enum ParameterDirectionEnum plParmDirection );
__declspec(property(get=GetDirection,put=PutDirection)) enum
    ParameterDirectionEnum Direction;

_bstr_t GetName( );
void PutName( _bstr_t pbstr );
__declspec(property(get=GetName,put=PutName)) _bstr_t Name;

unsigned char GetNumericScale( );
void PutNumericScale( unsigned char pbScale );
__declspec(property(get=GetNumericScale,put=PutNumericScale)) unsigned
    char NumericScale;

unsigned char GetPrecision( );
void PutPrecision( unsigned char pbPrecision );
__declspec(property(get=GetPrecision,put=PutPrecision)) unsigned char
    Precision;

long GetSize( );
void PutSize( long pl );
__declspec(property(get=GetSize,put=PutSize)) long Size;

enum DataTypeEnum GetType( );
void PutType( enum DataTypeEnum psDataType );
__declspec(property(get=GetType,put=PutType)) enum DataTypeEnum Type;

_variant_t GetValue( );
void PutValue( const _variant_t &amp; pvar );
__declspec(property(get=GetValue,put=PutValue)) _variant_t Value;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
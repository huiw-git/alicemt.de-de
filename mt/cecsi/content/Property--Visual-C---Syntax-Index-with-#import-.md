---
title: "Property (Visual C++ Syntax Index with #import)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 80988ca7-f514-438d-bf6f-9390dfe93fc3
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
# Property (Visual C++ Syntax Index with #import)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt1" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>long GetAttributes( );
void PutAttributes( long plAttributes );
__declspec(property(get=GetAttributes,put=PutAttributes)) long
    Attributes;

_bstr_t GetName( );
__declspec(property(get=GetName)) _bstr_t Name;

enum DataTypeEnum GetType( );
__declspec(property(get=GetType)) enum DataTypeEnum Type;

_variant_t GetValue( );
void PutValue( const _variant_t &amp; pval );
__declspec(property(get=GetValue,put=PutValue)) _variant_t Value;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>long GetAttributes( );
void PutAttributes( long plAttributes );
__declspec(property(get=GetAttributes,put=PutAttributes)) long
    Attributes;

_bstr_t GetName( );
__declspec(property(get=GetName)) _bstr_t Name;

enum DataTypeEnum GetType( );
__declspec(property(get=GetType)) enum DataTypeEnum Type;

_variant_t GetValue( );
void PutValue( const _variant_t &amp; pval );
__declspec(property(get=GetValue,put=PutValue)) _variant_t Value;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
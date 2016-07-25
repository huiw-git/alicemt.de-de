---
title: "RecordsetEvents (Visual C++ Syntax Index with #import)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b7021f11-8242-4e9f-92e9-1a4472673fb1
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
# RecordsetEvents (Visual C++ Syntax Index with #import)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt1" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <code>HRESULT WillChangeField( long cFields, const
    _variant_t &amp; Fields, enum     EventStatusEnum * adStatus, struct
    _Recordset * pRecordset );

HRESULT FieldChangeComplete( long cFields, const
    _variant_t &amp; Fields,     struct Error * pError, enum EventStatusEnum
    * adStatus, struct     _Recordset * pRecordset );

HRESULT WillChangeRecord( enum EventReasonEnum
    adReason, long cRecords,     enum EventStatusEnum * adStatus, struct
    _Recordset * pRecordset );

HRESULT RecordChangeComplete( enum EventReasonEnum
    adReason, long     cRecords, struct Error * pError, enum
    EventStatusEnum * adStatus,     struct _Recordset * pRecordset );

HRESULT WillChangeRecordset( enum EventReasonEnum
    adReason, enum     EventStatusEnum * adStatus, struct _Recordset *
    pRecordset );

HRESULT RecordsetChangeComplete( enum
    EventReasonEnum adReason, struct     Error * pError, enum
    EventStatusEnum * adStatus, struct _Recordset *     pRecordset );

HRESULT WillMove( enum EventReasonEnum adReason, enum
    EventStatusEnum *     adStatus, struct _Recordset * pRecordset );

HRESULT MoveComplete( enum EventReasonEnum adReason, struct
    Error *     pError, enum EventStatusEnum * adStatus, struct
    _Recordset * pRecordset );

HRESULT EndOfRecordset( VARIANT_BOOL * fMoreData, enum
    EventStatusEnum *     adStatus, struct _Recordset * pRecordset );

HRESULT FetchProgress( long Progress, long MaxProgress,
    enum     EventStatusEnum * adStatus, struct _Recordset * pRecordset );

HRESULT FetchComplete( struct Error * pError, enum
    EventStatusEnum *     adStatus, struct _Recordset * pRecordset );</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <code>HRESULT WillChangeField( long cFields, const
    _variant_t &amp; Fields, enum     EventStatusEnum * adStatus, struct
    _Recordset * pRecordset );

HRESULT FieldChangeComplete( long cFields, const
    _variant_t &amp; Fields,     struct Error * pError, enum EventStatusEnum
    * adStatus, struct     _Recordset * pRecordset );

HRESULT WillChangeRecord( enum EventReasonEnum
    adReason, long cRecords,     enum EventStatusEnum * adStatus, struct
    _Recordset * pRecordset );

HRESULT RecordChangeComplete( enum EventReasonEnum
    adReason, long     cRecords, struct Error * pError, enum
    EventStatusEnum * adStatus,     struct _Recordset * pRecordset );

HRESULT WillChangeRecordset( enum EventReasonEnum
    adReason, enum     EventStatusEnum * adStatus, struct _Recordset *
    pRecordset );

HRESULT RecordsetChangeComplete( enum
    EventReasonEnum adReason, struct     Error * pError, enum
    EventStatusEnum * adStatus, struct _Recordset *     pRecordset );

HRESULT WillMove( enum EventReasonEnum adReason, enum
    EventStatusEnum *     adStatus, struct _Recordset * pRecordset );

HRESULT MoveComplete( enum EventReasonEnum adReason, struct
    Error *     pError, enum EventStatusEnum * adStatus, struct
    _Recordset * pRecordset );

HRESULT EndOfRecordset( VARIANT_BOOL * fMoreData, enum
    EventStatusEnum *     adStatus, struct _Recordset * pRecordset );

HRESULT FetchProgress( long Progress, long MaxProgress,
    enum     EventStatusEnum * adStatus, struct _Recordset * pRecordset );

HRESULT FetchComplete( struct Error * pError, enum
    EventStatusEnum *     adStatus, struct _Recordset * pRecordset );</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
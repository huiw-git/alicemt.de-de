---
title: "Recordset (ADO for Visual C++ Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: affc847c-a533-4c8a-bdff-3682fdb5df5f
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
# Recordset (ADO for Visual C++ Syntax)
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
          <code>AddNew(VARIANT FieldList, VARIANT Values)
Cancel(void)
CancelBatch(AffectEnum AffectRecords)
CancelUpdate(void)
Clone(LockTypeEnum LockType, _ADORecordset **ppvObject)
Close(void)
CompareBookmarks(VARIANT Bookmark1, VARIANT Bookmark2, CompareEnum *pCompare)
Delete(AffectEnum AffectRecords)
Find(BSTR Criteria, LONG SkipRecords, SearchDirectionEnum SearchDirection, VARIANT Start)
GetRows(long Rows, VARIANT Start, VARIANT Fields, VARIANT *pvar)
GetString(StringFormatEnum StringFormat, long NumRows, BSTR ColumnDelimeter, BSTR RowDelimeter, BSTR NullExpr, BSTR *pRetString)
Move(long NumRecords, VARIANT Start)
MoveFirst(void)
MoveLast(void)
MoveNext(void)
MovePrevious(void)
NextRecordset(VARIANT *RecordsAffected, _ADORecordset **ppiRs)
Open(VARIANT Source, VARIANT ActiveConnection, CursorTypeEnum CursorType, LockTypeEnum LockType, LONG Options)
Requery(LONG Options)
Resync(AffectEnum AffectRecords, ResyncEnum ResyncValues)
Save(BSTR FileName, PersistFormatEnum PersistFormat)
Supports(CursorOptionEnum CursorOptions, VARIANT_BOOL *pb)
Update(VARIANT Fields, VARIANT Values)
UpdateBatch(AffectEnum AffectRecords)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt2" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>get_AbsolutePage(PositionEnum *pl)
put_AbsolutePage(PositionEnum Page)
get_AbsolutePosition(PositionEnum *pl)
put_AbsolutePosition(PositionEnum Position)
get_ActiveCommand(IDispatch **ppCmd)
get_ActiveConnection(VARIANT *pvar)
put_ActiveConnection(VARIANT vConn)
putref_ActiveConnection(IDispatch *pconn)
get_BOF(VARIANT_BOOL *pb)
get_Bookmark(VARIANT *pvBookmark)
put_Bookmark(VARIANT vBookmark)
get_CacheSize(long *pl)
put_CacheSize(long CacheSize)
get_CursorLocation(CursorLocationEnum *plCursorLoc)
put_CursorLocation(CursorLocationEnum lCursorLoc)
get_CursorType(CursorTypeEnum *plCursorType)
put_CursorType(CursorTypeEnum lCursorType)
get_DataMember(BSTR *pbstrDataMember)
put_DataMember(BSTR bstrDataMember)
get_DataSource(IUnknown **ppunkDataSource)
putref_DataSource(IUnknown *punkDataSource)
get_EditMode(EditModeEnum *pl)
get_EOF(VARIANT_BOOL *pb)
get_Filter(VARIANT *Criteria)
put_Filter(VARIANT Criteria)
get_LockType(LockTypeEnum *plLockType)
put_LockType(LockTypeEnum lLockType)
get_MarshalOptions(MarshalOptionsEnum *peMarshal)
put_MarshalOptions(MarshalOptionsEnum eMarshal)
get_MaxRecords(long *plMaxRecords)
put_MaxRecords(long lMaxRecords)
get_PageCount(long *pl)
get_PageSize(long *pl)
put_PageSize(long PageSize)
get_RecordCount(long *pl)
get_Sort(BSTR *Criteria)
put_Sort(BSTR Criteria)
get_Source(VARIANT *pvSource)
put_Source(BSTR bstrConn)
putref_Source(IDispatch *pcmd)
get_State(LONG *plObjState)
get_Status(long *pl)
get_StayInSync(VARIANT_BOOL *pbStayInSync)
put_StayInSync(VARIANT_BOOL bStayInSync)
get_Fields(ADOFields **ppvObject)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt3" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <code>EndOfRecordset(VARIANT_BOOL *fMoreData, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
FetchComplete(ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
FetchProgress(long Progress, long MaxProgress, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
FieldChangeComplete(LONG cFields, VARIANT Fields, ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
MoveComplete(EventReasonEnum adReason, ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
RecordChangeComplete(EventReasonEnum adReason, LONG cRecords, ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
RecordsetChangeComplete(EventReasonEnum adReason, ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
WillChangeField(LONG cFields, VARIANT Fields, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
WillChangeRecord(EventReasonEnum adReason, LONG cRecords, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
WillChangeRecordset(EventReasonEnum adReason, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
WillMove(EventReasonEnum adReason, EventStatusEnum *adStatus, _ADORecordset *pRecordset)</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
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
          <code>AddNew(VARIANT FieldList, VARIANT Values)
Cancel(void)
CancelBatch(AffectEnum AffectRecords)
CancelUpdate(void)
Clone(LockTypeEnum LockType, _ADORecordset **ppvObject)
Close(void)
CompareBookmarks(VARIANT Bookmark1, VARIANT Bookmark2, CompareEnum *pCompare)
Delete(AffectEnum AffectRecords)
Find(BSTR Criteria, LONG SkipRecords, SearchDirectionEnum SearchDirection, VARIANT Start)
GetRows(long Rows, VARIANT Start, VARIANT Fields, VARIANT *pvar)
GetString(StringFormatEnum StringFormat, long NumRows, BSTR ColumnDelimeter, BSTR RowDelimeter, BSTR NullExpr, BSTR *pRetString)
Move(long NumRecords, VARIANT Start)
MoveFirst(void)
MoveLast(void)
MoveNext(void)
MovePrevious(void)
NextRecordset(VARIANT *RecordsAffected, _ADORecordset **ppiRs)
Open(VARIANT Source, VARIANT ActiveConnection, CursorTypeEnum CursorType, LockTypeEnum LockType, LONG Options)
Requery(LONG Options)
Resync(AffectEnum AffectRecords, ResyncEnum ResyncValues)
Save(BSTR FileName, PersistFormatEnum PersistFormat)
Supports(CursorOptionEnum CursorOptions, VARIANT_BOOL *pb)
Update(VARIANT Fields, VARIANT Values)
UpdateBatch(AffectEnum AffectRecords)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <code>get_AbsolutePage(PositionEnum *pl)
put_AbsolutePage(PositionEnum Page)
get_AbsolutePosition(PositionEnum *pl)
put_AbsolutePosition(PositionEnum Position)
get_ActiveCommand(IDispatch **ppCmd)
get_ActiveConnection(VARIANT *pvar)
put_ActiveConnection(VARIANT vConn)
putref_ActiveConnection(IDispatch *pconn)
get_BOF(VARIANT_BOOL *pb)
get_Bookmark(VARIANT *pvBookmark)
put_Bookmark(VARIANT vBookmark)
get_CacheSize(long *pl)
put_CacheSize(long CacheSize)
get_CursorLocation(CursorLocationEnum *plCursorLoc)
put_CursorLocation(CursorLocationEnum lCursorLoc)
get_CursorType(CursorTypeEnum *plCursorType)
put_CursorType(CursorTypeEnum lCursorType)
get_DataMember(BSTR *pbstrDataMember)
put_DataMember(BSTR bstrDataMember)
get_DataSource(IUnknown **ppunkDataSource)
putref_DataSource(IUnknown *punkDataSource)
get_EditMode(EditModeEnum *pl)
get_EOF(VARIANT_BOOL *pb)
get_Filter(VARIANT *Criteria)
put_Filter(VARIANT Criteria)
get_LockType(LockTypeEnum *plLockType)
put_LockType(LockTypeEnum lLockType)
get_MarshalOptions(MarshalOptionsEnum *peMarshal)
put_MarshalOptions(MarshalOptionsEnum eMarshal)
get_MaxRecords(long *plMaxRecords)
put_MaxRecords(long lMaxRecords)
get_PageCount(long *pl)
get_PageSize(long *pl)
put_PageSize(long PageSize)
get_RecordCount(long *pl)
get_Sort(BSTR *Criteria)
put_Sort(BSTR Criteria)
get_Source(VARIANT *pvSource)
put_Source(BSTR bstrConn)
putref_Source(IDispatch *pcmd)
get_State(LONG *plObjState)
get_Status(long *pl)
get_StayInSync(VARIANT_BOOL *pbStayInSync)
put_StayInSync(VARIANT_BOOL bStayInSync)
get_Fields(ADOFields **ppvObject)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <code>EndOfRecordset(VARIANT_BOOL *fMoreData, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
FetchComplete(ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
FetchProgress(long Progress, long MaxProgress, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
FieldChangeComplete(LONG cFields, VARIANT Fields, ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
MoveComplete(EventReasonEnum adReason, ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
RecordChangeComplete(EventReasonEnum adReason, LONG cRecords, ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
RecordsetChangeComplete(EventReasonEnum adReason, ADOError *pError, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
WillChangeField(LONG cFields, VARIANT Fields, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
WillChangeRecord(EventReasonEnum adReason, LONG cRecords, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
WillChangeRecordset(EventReasonEnum adReason, EventStatusEnum *adStatus, _ADORecordset *pRecordset)
WillMove(EventReasonEnum adReason, EventStatusEnum *adStatus, _ADORecordset *pRecordset)</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
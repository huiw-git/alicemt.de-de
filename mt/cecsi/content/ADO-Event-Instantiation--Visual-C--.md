---
title: "ADO Event Instantiation: Visual C++"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 385ad90a-37d0-497c-94aa-935d21fed78f
caps.latest.revision: 11
caps.handback.revision: 11
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
# ADO Event Instantiation: Visual C++
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3ad39bffde783d6717c3cc67ae6203d4" id="tgt1" class="tgtSentence">This is a schematic description of how to instantiate ADO events in Microsoft® Visual C++®.</caps:sentence>
          <caps:sentence sentenceid="778bbedd95c806a133cddc77b25d768b" id="tgt2" class="tgtSentence"> See <legacyLink xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">ADO Events Model Example (VC++)</legacyLink> for a complete description.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2122358c2c31754707ddf697b5241aea" id="tgt3" class="tgtSentence">Create classes derived from the <legacyBold>ConnectionEventsVt</legacyBold> and <legacyBold>RecordsetEventsVt</legacyBold> interfaces found in the file adoint.h.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC01
class CConnEvent : public ConnectionEventsVt
{
    public:
    STDMETHODIMP InfoMessage( 
            ADOError *pError,
            EventStatusEnum *adStatus,
            _ADOConnection *pConnection);
...
}

class CRstEvent : public RecordsetEventsVt 
{
    public:
        STDMETHODIMP WillChangeField( 
                LONG cFields,
                VARIANT Fields,
                EventStatusEnum *adStatus,
                _ADORecordset *pRecordset);
...
}
// EndEventExampleVC01</code>
        <para>
          <caps:sentence sentenceid="9d52a260a7a43a9e271ecb01f953a023" id="tgt4" class="tgtSentence">Implement each of the event-handler methods in both classes.</caps:sentence>
          <caps:sentence sentenceid="95774d90b7f4f2085a310d1ac1500962" id="tgt5" class="tgtSentence"> It is sufficient that each method merely return an HRESULT of S_OK.</caps:sentence>
          <caps:sentence sentenceid="e3187c3032b717e352f653454ca3278b" id="tgt6" class="tgtSentence"> However, when you make it known that your event handlers are available, they will be called continuously by default.</caps:sentence>
          <caps:sentence sentenceid="fe0ab3d8fed8010abff856f44ce550dc" id="tgt7" class="tgtSentence"> Instead, you might want to request no further notification after the first time by setting <legacyBold>adStatus</legacyBold> to <legacyBold>adStatusUnwantedEvent</legacyBold>.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC02
STDMETHODIMP CConnEvent::ConnectComplete(
            ADOError *pError,
            EventStatusEnum *adStatus,
            _ADOConnection *pConnection) 
        {
        *adStatus = adStatusUnwantedEvent;
        return S_OK;
        }

// EndEventExampleVC02</code>
        <para>
          <caps:sentence sentenceid="28df271b3892e83a35a1b41fe9979397" id="tgt8" class="tgtSentence">The event classes inherit from <legacyBold>IUnknown</legacyBold>, so you must also implement the <legacyBold>QueryInterface</legacyBold>, <legacyBold>AddRef</legacyBold>, and <legacyBold>Release</legacyBold> methods.</caps:sentence>
          <caps:sentence sentenceid="80add47c5dd2c61a2d990c7c292841ef" id="tgt9" class="tgtSentence"> Also implement class constructors and destructors.</caps:sentence>
          <caps:sentence sentenceid="f172d1a7899b336eed1031024bf9d37b" id="tgt10" class="tgtSentence"> Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4a910995fe836ce61c62bfdd56ba7761" id="tgt11" class="tgtSentence">Make it known that your event handlers are available by issuing <legacyBold>QueryInterface</legacyBold> on the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> and <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> objects for the <legacyBold>IConnectionPointContainer</legacyBold> and <legacyBold>IConnectionPoint</legacyBold> interfaces.</caps:sentence>
          <caps:sentence sentenceid="61bf2d788556d21dd2816777eb4c896e" id="tgt12" class="tgtSentence"> Then issue <legacyBold>IConnectionPoint::Advise</legacyBold> for each class.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4e56b68e19c57b84b27c7f6f6d04ab88" id="tgt13" class="tgtSentence">For example, assume you are using a Boolean function that returns <legacyBold>True</legacyBold> if it successfully informs a <legacyBold>Recordset</legacyBold> object that you have event handlers available.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC03
HRESULT    hr;
DWORD      dwEvtClass;
IConnectionPointContainer    *pCPC = NULL;
IConnectionPoint             *pCP = NULL;
CRstEvent                    *pRStEvent = NULL;
...
_RecordsetPtr                pRs;
pRs.CreateInstance(__uuidof(Recordset));
pRStEvent = new CRstEvent;
if (pRStEvent == NULL) return FALSE;
...
hr = pRs-&gt;QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&amp;pCPC);
if (FAILED(hr)) return FALSE;
hr = pCPC-&gt;FindConnectionPoint(RecordsetEvents, &amp;pCP);
pCPC-&gt;Release();    // Always Release now, even before checking.
if (FAILED(hr)) return FALSE;
hr = pCP-&gt;Advise(pRstEvent, &amp;dwEvtClass);   //Turn on event support.
pCP-&gt;Release();
if (FAILED(hr)) return FALSE;
...
return TRUE;
...
// EndEventExampleVC03</code>
        <para>
          <caps:sentence sentenceid="4a03fadc83c3b2373e8f1abd90c5e6d6" id="tgt14" class="tgtSentence">At this point, events for the <legacyBold>RecordsetEvent</legacyBold> family are enabled and your methods will be called as <legacyBold>Recordset</legacyBold> events occur.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="eb3a53260e3f5519a1b363762283ecef" id="tgt15" class="tgtSentence">Later, when you want to make your event handlers unavailable, get the connection point again and issue the <legacyBold>IConnectionPoint::Unadvise</legacyBold> method.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC04
...
hr = pCP-&gt;Unadvise(dwEvtClass);    //Turn off event support.
pCP-&gt;Release();
if (FAILED(hr)) return FALSE;
...
// EndEventExampleVC04</code>
        <para>
          <caps:sentence sentenceid="bad9f0c32a26c36edd45ade2305bbeb1" id="tgt16" class="tgtSentence">You must release interfaces and destroy class objects as appropriate.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="13d0c125f06b29fbab1df5d203d10f34" id="tgt17" class="tgtSentence">The following code shows a complete example of a <legacyBold>Recordset</legacyBold> Event sink class.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC05.cpp
// compile with: /LD
#include &lt;adoint.h&gt;

class CADORecordsetEvents : public RecordsetEventsVt {

public:
   ULONG m_ulRefCount;
   CADORecordsetEvents():m_ulRefCount(1){}

   STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) {
      if (IsEqualIID(__uuidof(IUnknown), iid) || IsEqualIID(__uuidof(RecordsetEventsVt), iid)) {
         *ppvObject = this;
         return S_OK;
      }
      else 
         return E_NOINTERFACE;
   }

   STDMETHOD_(ULONG, AddRef)() {
      return m_ulRefCount++;
   }

   STDMETHOD_(ULONG, Release)() {
      if (--m_ulRefCount == 0) {
         delete this;
         return 0;
      }
      else 
         return m_ulRefCount;
   }


   STDMETHOD(WillChangeField)( LONG cFields, 
                               VARIANT Fields, 
                               EventStatusEnum *adStatus,
                               _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(FieldChangeComplete)( LONG cFields,
                                   VARIANT Fields,
                                   ADOError *pError,
                                   EventStatusEnum *adStatus,
                                   _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(WillChangeRecord)( EventReasonEnum adReason,
                                LONG cRecords,
                                EventStatusEnum *adStatus,
                                _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(RecordChangeComplete)( EventReasonEnum adReason,
                                    LONG cRecords,
                                    ADOError  *pError,
                                    EventStatusEnum  *adStatus,
                                    _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(WillChangeRecordset)( EventReasonEnum adReason,
                                   EventStatusEnum *adStatus,
                                   _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(RecordsetChangeComplete)( EventReasonEnum adReason,
                                       ADOError *pError,
                                       EventStatusEnum  *adStatus,
                                       _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(WillMove)( EventReasonEnum adReason,
                        EventStatusEnum  *adStatus,
                        _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(MoveComplete)( EventReasonEnum adReason,
                            ADOError *pError,
                            EventStatusEnum *adStatus,
                            _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(EndOfRecordset)( VARIANT_BOOL *fMoreData,
                              EventStatusEnum *adStatus,
                              _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(FetchProgress)( long Progress,
                             long MaxProgress,
                             EventStatusEnum *adStatus,
                             _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(FetchComplete)( ADOError *pError,
                             EventStatusEnum *adStatus,
                             _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }
};</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This is a schematic description of how to instantiate ADO events in Microsoft® Visual C++®.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> See <legacyLink xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">ADO Events Model Example (VC++)</legacyLink> for a complete description.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Create classes derived from the <legacyBold>ConnectionEventsVt</legacyBold> and <legacyBold>RecordsetEventsVt</legacyBold> interfaces found in the file adoint.h.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC01
class CConnEvent : public ConnectionEventsVt
{
    public:
    STDMETHODIMP InfoMessage( 
            ADOError *pError,
            EventStatusEnum *adStatus,
            _ADOConnection *pConnection);
...
}

class CRstEvent : public RecordsetEventsVt 
{
    public:
        STDMETHODIMP WillChangeField( 
                LONG cFields,
                VARIANT Fields,
                EventStatusEnum *adStatus,
                _ADORecordset *pRecordset);
...
}
// EndEventExampleVC01</code>
        <para>
          <caps:sentence id="src4" class="srcSentence">Implement each of the event-handler methods in both classes.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> It is sufficient that each method merely return an HRESULT of S_OK.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> However, when you make it known that your event handlers are available, they will be called continuously by default.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Instead, you might want to request no further notification after the first time by setting <legacyBold>adStatus</legacyBold> to <legacyBold>adStatusUnwantedEvent</legacyBold>.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC02
STDMETHODIMP CConnEvent::ConnectComplete(
            ADOError *pError,
            EventStatusEnum *adStatus,
            _ADOConnection *pConnection) 
        {
        *adStatus = adStatusUnwantedEvent;
        return S_OK;
        }

// EndEventExampleVC02</code>
        <para>
          <caps:sentence id="src8" class="srcSentence">The event classes inherit from <legacyBold>IUnknown</legacyBold>, so you must also implement the <legacyBold>QueryInterface</legacyBold>, <legacyBold>AddRef</legacyBold>, and <legacyBold>Release</legacyBold> methods.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> Also implement class constructors and destructors.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">Make it known that your event handlers are available by issuing <legacyBold>QueryInterface</legacyBold> on the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> and <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> objects for the <legacyBold>IConnectionPointContainer</legacyBold> and <legacyBold>IConnectionPoint</legacyBold> interfaces.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Then issue <legacyBold>IConnectionPoint::Advise</legacyBold> for each class.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">For example, assume you are using a Boolean function that returns <legacyBold>True</legacyBold> if it successfully informs a <legacyBold>Recordset</legacyBold> object that you have event handlers available.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC03
HRESULT    hr;
DWORD      dwEvtClass;
IConnectionPointContainer    *pCPC = NULL;
IConnectionPoint             *pCP = NULL;
CRstEvent                    *pRStEvent = NULL;
...
_RecordsetPtr                pRs;
pRs.CreateInstance(__uuidof(Recordset));
pRStEvent = new CRstEvent;
if (pRStEvent == NULL) return FALSE;
...
hr = pRs-&gt;QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&amp;pCPC);
if (FAILED(hr)) return FALSE;
hr = pCPC-&gt;FindConnectionPoint(RecordsetEvents, &amp;pCP);
pCPC-&gt;Release();    // Always Release now, even before checking.
if (FAILED(hr)) return FALSE;
hr = pCP-&gt;Advise(pRstEvent, &amp;dwEvtClass);   //Turn on event support.
pCP-&gt;Release();
if (FAILED(hr)) return FALSE;
...
return TRUE;
...
// EndEventExampleVC03</code>
        <para>
          <caps:sentence id="src14" class="srcSentence">At this point, events for the <legacyBold>RecordsetEvent</legacyBold> family are enabled and your methods will be called as <legacyBold>Recordset</legacyBold> events occur.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src15" class="srcSentence">Later, when you want to make your event handlers unavailable, get the connection point again and issue the <legacyBold>IConnectionPoint::Unadvise</legacyBold> method.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC04
...
hr = pCP-&gt;Unadvise(dwEvtClass);    //Turn off event support.
pCP-&gt;Release();
if (FAILED(hr)) return FALSE;
...
// EndEventExampleVC04</code>
        <para>
          <caps:sentence id="src16" class="srcSentence">You must release interfaces and destroy class objects as appropriate.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src17" class="srcSentence">The following code shows a complete example of a <legacyBold>Recordset</legacyBold> Event sink class.</caps:sentence>
        </para>
        <code>// BeginEventExampleVC05.cpp
// compile with: /LD
#include &lt;adoint.h&gt;

class CADORecordsetEvents : public RecordsetEventsVt {

public:
   ULONG m_ulRefCount;
   CADORecordsetEvents():m_ulRefCount(1){}

   STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) {
      if (IsEqualIID(__uuidof(IUnknown), iid) || IsEqualIID(__uuidof(RecordsetEventsVt), iid)) {
         *ppvObject = this;
         return S_OK;
      }
      else 
         return E_NOINTERFACE;
   }

   STDMETHOD_(ULONG, AddRef)() {
      return m_ulRefCount++;
   }

   STDMETHOD_(ULONG, Release)() {
      if (--m_ulRefCount == 0) {
         delete this;
         return 0;
      }
      else 
         return m_ulRefCount;
   }


   STDMETHOD(WillChangeField)( LONG cFields, 
                               VARIANT Fields, 
                               EventStatusEnum *adStatus,
                               _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(FieldChangeComplete)( LONG cFields,
                                   VARIANT Fields,
                                   ADOError *pError,
                                   EventStatusEnum *adStatus,
                                   _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(WillChangeRecord)( EventReasonEnum adReason,
                                LONG cRecords,
                                EventStatusEnum *adStatus,
                                _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(RecordChangeComplete)( EventReasonEnum adReason,
                                    LONG cRecords,
                                    ADOError  *pError,
                                    EventStatusEnum  *adStatus,
                                    _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(WillChangeRecordset)( EventReasonEnum adReason,
                                   EventStatusEnum *adStatus,
                                   _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(RecordsetChangeComplete)( EventReasonEnum adReason,
                                       ADOError *pError,
                                       EventStatusEnum  *adStatus,
                                       _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(WillMove)( EventReasonEnum adReason,
                        EventStatusEnum  *adStatus,
                        _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(MoveComplete)( EventReasonEnum adReason,
                            ADOError *pError,
                            EventStatusEnum *adStatus,
                            _ADORecordset  *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(EndOfRecordset)( VARIANT_BOOL *fMoreData,
                              EventStatusEnum *adStatus,
                              _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(FetchProgress)( long Progress,
                             long MaxProgress,
                             EventStatusEnum *adStatus,
                             _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }

   STDMETHOD(FetchComplete)( ADOError *pError,
                             EventStatusEnum *adStatus,
                             _ADORecordset *pRecordset) {
      *adStatus = adStatusUnwantedEvent; 
      return S_OK;
   }
};</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
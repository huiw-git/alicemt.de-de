---
title: "Save and Open Methods Example (VC++)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 334ae655-8cac-48e6-8d00-1d28f3436e1e
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
# Save and Open Methods Example (VC++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8f5943566ac3f1497b24e66f4ab5e7b8" id="tgt1" class="tgtSentence">These three examples demonstrate how the <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> and <legacyBold>Open</legacyBold> methods can be used together.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="33fc9ec945fa73146d1d12df79e4131d" id="tgt2" class="tgtSentence">Assume you are going on a business trip and want to take along a table from a database.</caps:sentence>
          <caps:sentence sentenceid="8054f8bd1920e9ce7ceb1e89d7377432" id="tgt3" class="tgtSentence"> Before you go, you access the data as a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> and save it in a transportable form.</caps:sentence>
          <caps:sentence sentenceid="f41452cfb169839ec79b311153fa986f" id="tgt4" class="tgtSentence"> When you arrive at your destination, you access the <legacyBold>Recordset</legacyBold> as a local, disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="318229428d7091769d4d86d9ae5ecdf1" id="tgt5" class="tgtSentence"> You make changes to the <legacyBold>Recordset</legacyBold>, then save it again.</caps:sentence>
          <caps:sentence sentenceid="5246b8ffedd82fe70f31966fc3d5a404" id="tgt6" class="tgtSentence"> Finally, when you return home, you connect to the database again and update it with the changes you made on the road.</caps:sentence>
        </para>
        <code>// BeginSaveCpp.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

#include &lt;ole2.h&gt;
#include &lt;stdio.h&gt;
#include &lt;conio.h&gt;
#include &lt;io.h&gt;

// Function declarations
inline void TESTHR(HRESULT x) { if FAILED(x) _com_issue_error(x); };
bool FileExists();
void SaveX1();
void SaveX2();
void SaveX3();
void PrintProviderError(_ConnectionPtr pConnection);
void PrintComError(_com_error &amp;e);

int main() {
   if ( FAILED(::CoInitialize(NULL)) )
      return -1;

   // If File exists in the specified directory, then display error
   if (!FileExists()) {
      SaveX1();
      SaveX2();
      SaveX3();
   }

   ::CoUninitialize();
}

// First, access and save the authors table.
void SaveX1() {
   HRESULT hr = S_OK;

   // Define ADO object pointers.  Initialize pointers on define.
   // These are in the ADODB::  namespace.
   _RecordsetPtr pRstAuthors = NULL;

   // Definitions of other variables
   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source' ; Initial Catalog='pubs'; Integrated Security='SSPI';");

   try {
      TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset)));

      pRstAuthors-&gt;Open("SELECT * FROM authors",strCnn, adOpenDynamic, 
         adLockBatchOptimistic, adCmdText);

      // For sake of illustration, save the Recordset to a diskette in XML format.
      pRstAuthors-&gt;Save("c:\\pubs.xml", adPersistXML);
   }
   catch(_com_error &amp;e) {
      // Notify the user of errors, if any.
      // Pass a connection pointer accessed from the Recordset.
      _variant_t vtConnect = pRstAuthors-&gt;GetActiveConnection();

      // GetActiveConnection returns connect string if connection
      // is not open, else returns Connection object.
      switch(vtConnect.vt) {
      case VT_BSTR:
         PrintComError(e);
         break;
      case VT_DISPATCH:
         PrintProviderError(vtConnect);
         break;
      default:
         printf("Errors occured.");
         break;
      }
   }

   if (pRstAuthors)
      if (pRstAuthors-&gt;State == adStateOpen)
         pRstAuthors-&gt;Close();
}

// At this point, you have arrived at your destination.
// You will access the authors table as a local, disconnected Recordset. 
// Don't forget you must have the MSPersist provider on the machine you 
// are using in order to access the saved file, c:\pubs.xml.
void SaveX2() {
   HRESULT hr = S_OK;

   // Define ADO object pointers.  Initialize pointers on define.
   // These are in the ADODB::  namespace.
   _RecordsetPtr pRstAuthors = NULL;

   try {
      TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset)));

      // For sake of illustration, we specify all parameters.
      pRstAuthors-&gt;Open("c:\\pubs.xml", "Provider='MSPersist';", adOpenForwardOnly, adLockBatchOptimistic, adCmdFile);

      // Now you have a local, disconnected Recordset.
      // (In this example, changes will not be saved).
      pRstAuthors-&gt;Find("au_lname = 'Carson'", NULL, adSearchForward);
      if (pRstAuthors-&gt;EndOfFile) {
         printf("Name not found ...\n");
         pRstAuthors-&gt;Close();
         return;
      }
      pRstAuthors-&gt;GetFields()-&gt;GetItem("City")-&gt;PutValue("Chicago");
      pRstAuthors-&gt;Update();

      // Save changes in ADTG format this time, purely for sake of  illustration. 
      // Note that the previous version is still on the diskette as c:\pubs.xml.
      pRstAuthors-&gt;Save("c:\\pubs.adtg", adPersistADTG);
   }
   catch(_com_error &amp;e){
      // Notify the user of errors if any.
      // Pass a connection pointer accessed from the Recordset.
      _variant_t vtConnect = pRstAuthors-&gt;GetActiveConnection();

      // GetActiveConnection returns connect string if connection
      // is not open, else returns Connection object.
      switch(vtConnect.vt) {
      case VT_BSTR:
         PrintComError(e);
         break;
      case VT_DISPATCH:
         PrintProviderError(vtConnect);
         break;
      default:
         printf("Errors occured.");
         break;
      }
   }

   if (pRstAuthors)
      if (pRstAuthors-&gt;State == adStateOpen)
         pRstAuthors-&gt;Close();
}

// Now update the database with changes.
void SaveX3() {
   HRESULT hr = S_OK;

   // Define ADO object pointers.  Initialize pointers on define.
   // These are in the ADODB::  namespace.
   _RecordsetPtr pRstAuthors = NULL;
   _ConnectionPtr pCnn = NULL;

   // Definitions of other variables
   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source'; Initial Catalog='pubs'; Integrated Security='SSPI';");

   try {
      TESTHR(pCnn.CreateInstance(__uuidof(Connection)));

      TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset)));

      // If there is no ActiveConnection, you can open with defaults.
      pRstAuthors-&gt;Open("c:\\pubs.adtg", "Provider=MSPersist;",
         adOpenForwardOnly, adLockBatchOptimistic, adCmdFile);

      // Connect to the database, associate the Recordset with the connection, 
      // then update the database table with the changed Recordset.
      pCnn-&gt;Open(strCnn, "", "", NULL);

      pRstAuthors-&gt;PutActiveConnection(_variant_t((IDispatch *) pCnn));
      pRstAuthors-&gt;UpdateBatch(adAffectAll);
   }
   catch(_com_error &amp;e) {
      // Notify the user of errors if any.
      // Pass a connection pointer accessed from the Recordset.
      _variant_t vtConnect = pRstAuthors-&gt;GetActiveConnection();

      // GetActiveConnection returns connect string if connection
      // is not open, else returns Connection object.
      switch(vtConnect.vt) {
      case VT_BSTR:
         PrintComError(e);
         break;
      case VT_DISPATCH:
         PrintProviderError(vtConnect);
         break;
      default:
         printf("Errors occured.");
         break;
      }
   }

   if (pRstAuthors)
      if (pRstAuthors-&gt;State == adStateOpen)
         pRstAuthors-&gt;Close();
   if (pCnn)
      if (pCnn-&gt;State == adStateOpen)
         pCnn-&gt;Close();
}

void PrintProviderError(_ConnectionPtr pConnection) {
   // Print Provider Errors from Connection object.
   // pErr is a record object in the Connection's Error collection.
   ErrorPtr pErr = NULL;

   if ( (pConnection-&gt;Errors-&gt;Count) &gt; 0) {
      long nCount = pConnection-&gt;Errors-&gt;Count;

      // Collection ranges from 0 to nCount -1.
      for ( long i = 0 ; i &lt; nCount ; i++) {
         pErr = pConnection-&gt;Errors-&gt;GetItem(i);
         printf("Error number: %x\t%s\n", pErr-&gt;Number, (LPCSTR) pErr-&gt;Description);
      }
   }
}

void PrintComError(_com_error &amp;e) {
   _bstr_t bstrSource(e.Source());
   _bstr_t bstrDescription(e.Description());

   // Print COM errors. 
   printf("Error\n");
   printf("\tCode = %08lx\n", e.Error());
   printf("\tCode meaning = %s\n", e.ErrorMessage());
   printf("\tSource = %s\n", (LPCSTR) bstrSource);
   printf("\tDescription = %s\n", (LPCSTR) bstrDescription);
}

bool FileExists() {
   struct _finddata_t xml_file;
   long hFile;

   if( (hFile = _findfirst("c:\\pubs.xml", &amp;xml_file )) != -1L)
   {
      printf( "File already exists!\n" );
      return(true);
   }
   else
      return (false);
}</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">These three examples demonstrate how the <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> and <legacyBold>Open</legacyBold> methods can be used together.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Assume you are going on a business trip and want to take along a table from a database.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Before you go, you access the data as a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> and save it in a transportable form.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> When you arrive at your destination, you access the <legacyBold>Recordset</legacyBold> as a local, disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> You make changes to the <legacyBold>Recordset</legacyBold>, then save it again.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Finally, when you return home, you connect to the database again and update it with the changes you made on the road.</caps:sentence>
        </para>
        <code>// BeginSaveCpp.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

#include &lt;ole2.h&gt;
#include &lt;stdio.h&gt;
#include &lt;conio.h&gt;
#include &lt;io.h&gt;

// Function declarations
inline void TESTHR(HRESULT x) { if FAILED(x) _com_issue_error(x); };
bool FileExists();
void SaveX1();
void SaveX2();
void SaveX3();
void PrintProviderError(_ConnectionPtr pConnection);
void PrintComError(_com_error &amp;e);

int main() {
   if ( FAILED(::CoInitialize(NULL)) )
      return -1;

   // If File exists in the specified directory, then display error
   if (!FileExists()) {
      SaveX1();
      SaveX2();
      SaveX3();
   }

   ::CoUninitialize();
}

// First, access and save the authors table.
void SaveX1() {
   HRESULT hr = S_OK;

   // Define ADO object pointers.  Initialize pointers on define.
   // These are in the ADODB::  namespace.
   _RecordsetPtr pRstAuthors = NULL;

   // Definitions of other variables
   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source' ; Initial Catalog='pubs'; Integrated Security='SSPI';");

   try {
      TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset)));

      pRstAuthors-&gt;Open("SELECT * FROM authors",strCnn, adOpenDynamic, 
         adLockBatchOptimistic, adCmdText);

      // For sake of illustration, save the Recordset to a diskette in XML format.
      pRstAuthors-&gt;Save("c:\\pubs.xml", adPersistXML);
   }
   catch(_com_error &amp;e) {
      // Notify the user of errors, if any.
      // Pass a connection pointer accessed from the Recordset.
      _variant_t vtConnect = pRstAuthors-&gt;GetActiveConnection();

      // GetActiveConnection returns connect string if connection
      // is not open, else returns Connection object.
      switch(vtConnect.vt) {
      case VT_BSTR:
         PrintComError(e);
         break;
      case VT_DISPATCH:
         PrintProviderError(vtConnect);
         break;
      default:
         printf("Errors occured.");
         break;
      }
   }

   if (pRstAuthors)
      if (pRstAuthors-&gt;State == adStateOpen)
         pRstAuthors-&gt;Close();
}

// At this point, you have arrived at your destination.
// You will access the authors table as a local, disconnected Recordset. 
// Don't forget you must have the MSPersist provider on the machine you 
// are using in order to access the saved file, c:\pubs.xml.
void SaveX2() {
   HRESULT hr = S_OK;

   // Define ADO object pointers.  Initialize pointers on define.
   // These are in the ADODB::  namespace.
   _RecordsetPtr pRstAuthors = NULL;

   try {
      TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset)));

      // For sake of illustration, we specify all parameters.
      pRstAuthors-&gt;Open("c:\\pubs.xml", "Provider='MSPersist';", adOpenForwardOnly, adLockBatchOptimistic, adCmdFile);

      // Now you have a local, disconnected Recordset.
      // (In this example, changes will not be saved).
      pRstAuthors-&gt;Find("au_lname = 'Carson'", NULL, adSearchForward);
      if (pRstAuthors-&gt;EndOfFile) {
         printf("Name not found ...\n");
         pRstAuthors-&gt;Close();
         return;
      }
      pRstAuthors-&gt;GetFields()-&gt;GetItem("City")-&gt;PutValue("Chicago");
      pRstAuthors-&gt;Update();

      // Save changes in ADTG format this time, purely for sake of  illustration. 
      // Note that the previous version is still on the diskette as c:\pubs.xml.
      pRstAuthors-&gt;Save("c:\\pubs.adtg", adPersistADTG);
   }
   catch(_com_error &amp;e){
      // Notify the user of errors if any.
      // Pass a connection pointer accessed from the Recordset.
      _variant_t vtConnect = pRstAuthors-&gt;GetActiveConnection();

      // GetActiveConnection returns connect string if connection
      // is not open, else returns Connection object.
      switch(vtConnect.vt) {
      case VT_BSTR:
         PrintComError(e);
         break;
      case VT_DISPATCH:
         PrintProviderError(vtConnect);
         break;
      default:
         printf("Errors occured.");
         break;
      }
   }

   if (pRstAuthors)
      if (pRstAuthors-&gt;State == adStateOpen)
         pRstAuthors-&gt;Close();
}

// Now update the database with changes.
void SaveX3() {
   HRESULT hr = S_OK;

   // Define ADO object pointers.  Initialize pointers on define.
   // These are in the ADODB::  namespace.
   _RecordsetPtr pRstAuthors = NULL;
   _ConnectionPtr pCnn = NULL;

   // Definitions of other variables
   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source'; Initial Catalog='pubs'; Integrated Security='SSPI';");

   try {
      TESTHR(pCnn.CreateInstance(__uuidof(Connection)));

      TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset)));

      // If there is no ActiveConnection, you can open with defaults.
      pRstAuthors-&gt;Open("c:\\pubs.adtg", "Provider=MSPersist;",
         adOpenForwardOnly, adLockBatchOptimistic, adCmdFile);

      // Connect to the database, associate the Recordset with the connection, 
      // then update the database table with the changed Recordset.
      pCnn-&gt;Open(strCnn, "", "", NULL);

      pRstAuthors-&gt;PutActiveConnection(_variant_t((IDispatch *) pCnn));
      pRstAuthors-&gt;UpdateBatch(adAffectAll);
   }
   catch(_com_error &amp;e) {
      // Notify the user of errors if any.
      // Pass a connection pointer accessed from the Recordset.
      _variant_t vtConnect = pRstAuthors-&gt;GetActiveConnection();

      // GetActiveConnection returns connect string if connection
      // is not open, else returns Connection object.
      switch(vtConnect.vt) {
      case VT_BSTR:
         PrintComError(e);
         break;
      case VT_DISPATCH:
         PrintProviderError(vtConnect);
         break;
      default:
         printf("Errors occured.");
         break;
      }
   }

   if (pRstAuthors)
      if (pRstAuthors-&gt;State == adStateOpen)
         pRstAuthors-&gt;Close();
   if (pCnn)
      if (pCnn-&gt;State == adStateOpen)
         pCnn-&gt;Close();
}

void PrintProviderError(_ConnectionPtr pConnection) {
   // Print Provider Errors from Connection object.
   // pErr is a record object in the Connection's Error collection.
   ErrorPtr pErr = NULL;

   if ( (pConnection-&gt;Errors-&gt;Count) &gt; 0) {
      long nCount = pConnection-&gt;Errors-&gt;Count;

      // Collection ranges from 0 to nCount -1.
      for ( long i = 0 ; i &lt; nCount ; i++) {
         pErr = pConnection-&gt;Errors-&gt;GetItem(i);
         printf("Error number: %x\t%s\n", pErr-&gt;Number, (LPCSTR) pErr-&gt;Description);
      }
   }
}

void PrintComError(_com_error &amp;e) {
   _bstr_t bstrSource(e.Source());
   _bstr_t bstrDescription(e.Description());

   // Print COM errors. 
   printf("Error\n");
   printf("\tCode = %08lx\n", e.Error());
   printf("\tCode meaning = %s\n", e.ErrorMessage());
   printf("\tSource = %s\n", (LPCSTR) bstrSource);
   printf("\tDescription = %s\n", (LPCSTR) bstrDescription);
}

bool FileExists() {
   struct _finddata_t xml_file;
   long hFile;

   if( (hFile = _findfirst("c:\\pubs.xml", &amp;xml_file )) != -1L)
   {
      printf( "File already exists!\n" );
      return(true);
   }
   else
      return (false);
}</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Version Property Example (VC++)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2440b6ff-2536-497c-a5f4-41db0cf1945e
caps.latest.revision: 12
caps.handback.revision: 12
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
# Version Property Example (VC++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5b990d7f1587fd3fb32b764b4ca20a25" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version</legacyLink> property of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object to display the current ADO version.</caps:sentence>
          <caps:sentence sentenceid="b8915aa4e5c14684ae21ef58f033a74a" id="tgt2" class="tgtSentence"> It also uses several dynamic properties to show:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="d6a801bbed0ac3f8a0f9b3999db386db" id="tgt3" class="tgtSentence">Current DBMS name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4389a8dcc21edbbd402929cc385c7049" id="tgt4" class="tgtSentence">OLE DB version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="caa768ca03304f1a57ca8077712bcde1" id="tgt5" class="tgtSentence">Provider name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ea3e9081f441ae96055d1c4976a9adb0" id="tgt6" class="tgtSentence">ODBC version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5f195e9ab22407f8348677bb30de766f" id="tgt7" class="tgtSentence">ODBC driver name and version.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="a955ec3a31d8205c3ae07b07b7fefc6d" id="tgt8" class="tgtSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <system>Trusted_Connection=yes</system> or <system>Integrated Security = SSPI</system> instead of user ID and password information in the connection string.</caps:sentence>
          </para>
        </alert>
        <code>// BeginVersionCpp.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

#include &lt;ole2.h&gt;
#include &lt;stdio.h&gt;
#include &lt;conio.h&gt;

// Function declarations
inline void TESTHR(HRESULT x) { if FAILED(x) _com_issue_error(x); };
void VersionX();
void PrintProviderError(_ConnectionPtr pConnection);
void PrintComError(_com_error &amp;e);

int main() {
    if (FAILED(::CoInitialize(NULL)))
        return -1;

    VersionX();

    ::CoUninitialize();
}

void VersionX() {
    HRESULT hr = S_OK;

   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source'; Initial Catalog='pubs'; Integrated Security='SSPI';");

    // Define ADO object pointers.  Initialize pointers on define.
    // These are in the ADODB::  namespace.
    _ConnectionPtr pConnection = NULL;

    try {
        // Open connection.
        TESTHR(pConnection.CreateInstance(__uuidof(Connection)));
        pConnection-&gt;Open (strCnn, "", "", adConnectUnspecified);

        printf("ADO Version   : %s\n\n",(LPCSTR) pConnection-&gt;Version);
        printf("DBMS Name   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("DBMS Name")-&gt;Value);
        printf("DBMS Version   : %s\n\n",(LPCSTR) (_bstr_t)
            pConnection-&gt;Properties-&gt;GetItem("DBMS Version")-&gt;Value);
        printf("OLE DB Version   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("OLE DB Version")-&gt;Value);
        printf("Provider Name   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Provider Name")-&gt;Value);
        printf("Provider Version   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Provider Version")-&gt;Value);
        printf("Driver Name   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Driver Name")-&gt;Value);
        printf("Driver Version   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Driver Version")-&gt;Value);
        printf("Driver ODBC Version   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Driver ODBC Version")-&gt;Value);

    }

    catch (_com_error &amp;e) {
        // Notify the user of errors if any.
        PrintProviderError(pConnection);
        PrintComError(e);
    }

    if (pConnection)
        if (pConnection-&gt;State == adStateOpen)
            pConnection-&gt;Close();
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

    // Print Com errors.
   printf("Error\n");
   printf("\tCode = %08lx\n", e.Error());
   printf("\tCode meaning = %s\n", e.ErrorMessage());
   printf("\tSource = %s\n", (LPCSTR) bstrSource);
   printf("\tDescription = %s\n", (LPCSTR) bstrDescription);
}</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version</legacyLink> property of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object to display the current ADO version.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It also uses several dynamic properties to show:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Current DBMS name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">OLE DB version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Provider name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">ODBC version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">ODBC driver name and version.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src8" class="srcSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <system>Trusted_Connection=yes</system> or <system>Integrated Security = SSPI</system> instead of user ID and password information in the connection string.</caps:sentence>
          </para>
        </alert>
        <code>// BeginVersionCpp.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

#include &lt;ole2.h&gt;
#include &lt;stdio.h&gt;
#include &lt;conio.h&gt;

// Function declarations
inline void TESTHR(HRESULT x) { if FAILED(x) _com_issue_error(x); };
void VersionX();
void PrintProviderError(_ConnectionPtr pConnection);
void PrintComError(_com_error &amp;e);

int main() {
    if (FAILED(::CoInitialize(NULL)))
        return -1;

    VersionX();

    ::CoUninitialize();
}

void VersionX() {
    HRESULT hr = S_OK;

   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source'; Initial Catalog='pubs'; Integrated Security='SSPI';");

    // Define ADO object pointers.  Initialize pointers on define.
    // These are in the ADODB::  namespace.
    _ConnectionPtr pConnection = NULL;

    try {
        // Open connection.
        TESTHR(pConnection.CreateInstance(__uuidof(Connection)));
        pConnection-&gt;Open (strCnn, "", "", adConnectUnspecified);

        printf("ADO Version   : %s\n\n",(LPCSTR) pConnection-&gt;Version);
        printf("DBMS Name   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("DBMS Name")-&gt;Value);
        printf("DBMS Version   : %s\n\n",(LPCSTR) (_bstr_t)
            pConnection-&gt;Properties-&gt;GetItem("DBMS Version")-&gt;Value);
        printf("OLE DB Version   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("OLE DB Version")-&gt;Value);
        printf("Provider Name   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Provider Name")-&gt;Value);
        printf("Provider Version   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Provider Version")-&gt;Value);
        printf("Driver Name   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Driver Name")-&gt;Value);
        printf("Driver Version   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Driver Version")-&gt;Value);
        printf("Driver ODBC Version   : %s\n\n",(LPCSTR) (_bstr_t) 
            pConnection-&gt;Properties-&gt;GetItem("Driver ODBC Version")-&gt;Value);

    }

    catch (_com_error &amp;e) {
        // Notify the user of errors if any.
        PrintProviderError(pConnection);
        PrintComError(e);
    }

    if (pConnection)
        if (pConnection-&gt;State == adStateOpen)
            pConnection-&gt;Close();
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

    // Print Com errors.
   printf("Error\n");
   printf("\tCode = %08lx\n", e.Error());
   printf("\tCode meaning = %s\n", e.ErrorMessage());
   printf("\tSource = %s\n", (LPCSTR) bstrSource);
   printf("\tDescription = %s\n", (LPCSTR) bstrDescription);
}</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Filter and RecordCount Properties Example (VC++)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b71346cb-3b09-4b8c-a600-976171a1c336
caps.latest.revision: 14
caps.handback.revision: 14
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
# Filter and RecordCount Properties Example (VC++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4d47aa6a0c6d8e766d3621bc53f7c224" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property to open a new <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> based on a specified condition applied to an existing <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="732c93ed8d68e27f715c56b3694c07be" id="tgt2" class="tgtSentence"> It uses the <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink> property to show the number of records in the two <legacyBold>Recordsets</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="19eda6c14654c5704e827a60e783f9dd" id="tgt3" class="tgtSentence"> The FilterField function is required for this procedure to run.</caps:sentence>
        </para>
      </introduction>
      <codeExample>
        <code>// BeginFilterCpp.cpp
// compile with: /EHsc /c
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

#include &lt;stdio.h&gt;
#include &lt;ole2.h&gt;
#include &lt;conio.h&gt;
#include "icrsint.h"

// Class extracts only Pub Name and Country Name.
class CPublishers : public CADORecordBinding {
   BEGIN_ADO_BINDING(CPublishers)

   // Column Pub Name is the 2nd field in the recordset
   ADO_VARIABLE_LENGTH_ENTRY2(2, adVarChar, m_szP_pubname, sizeof(m_szP_pubname), 
                              lP_pubnameStatus, TRUE)

   // Column Country Name is the 5th field in the recordset
   ADO_VARIABLE_LENGTH_ENTRY2(5, adVarChar, m_szP_country, sizeof(m_szP_country), 
                              lP_countryStatus, TRUE)

   END_ADO_BINDING()

public:
   CHAR m_szP_pubname[50];
   ULONG lP_pubnameStatus;
   CHAR m_szP_country[50];
   ULONG lP_countryStatus;
};

// Function declarations
inline void TESTHR(HRESULT x) { if FAILED(x) _com_issue_error(x); };
void FilterX();
_RecordsetPtr FilterField(_RecordsetPtr rstTemp, _bstr_t strField, _bstr_t strFilter);
void FilterX2();
void PrintProviderError(_ConnectionPtr pCnn1);
void PrintComError(_com_error &amp;e);

inline char* mygets(char* strDest, int n) {
   char strExBuff[10];
   char* pstrRet = fgets(strDest, n, stdin);

   if (pstrRet == NULL)
      return NULL;

   if (!strrchr(strDest, '\n'))
      // Exhaust the input buffer.
      do {
         fgets(strExBuff, sizeof(strExBuff), stdin);
      } while (!strrchr(strExBuff, '\n'));
   else
      // Replace '\n' with '\0'
      strDest[strrchr(strDest, '\n') - strDest] = '\0';

   return pstrRet;
}

int main() {
   HRESULT hr = S_OK;

   if ( FAILED(::CoInitialize(NULL)) )
      return -1;

   FilterX();
   FilterX2();

   ::CoUninitialize();
}

void FilterX() {
   // Define ADO object pointers, initialize pointers on define.  These are in the ADODB::  namespace.
   _RecordsetPtr rstPublishers = NULL;
   _RecordsetPtr rstPublishersCountry = NULL;

   // Define Other Variables
   HRESULT hr = S_OK;
   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source'; Initial Catalog='pubs'; Integrated Security='SSPI';");
   int intPublisherCount = 0;
   long recCount = 0;
   _bstr_t strCountry; 
   _bstr_t strMessage;
   char *tempStr;
   CHAR sz_CountryName[50];
   bool boolFlag = TRUE;
   char * token1;

   try {
      // Open recordset with data from Publishers table.
      rstPublishers.CreateInstance(__uuidof(Recordset));
      rstPublishersCountry.CreateInstance(__uuidof(Recordset));

      rstPublishers-&gt;CursorType = adOpenStatic;

      TESTHR(rstPublishers-&gt;Open("publishers", strCnn, adOpenStatic , adLockReadOnly, adCmdTable));

      // Populate the Recordset.
      intPublisherCount = rstPublishers-&gt;RecordCount;

      // Get user input.
      printf("Enter a country to filter on:");
      mygets(sz_CountryName, 50);

      // Trim the string
      tempStr = strtok_s(sz_CountryName, "  \t", &amp;token1);
      strCountry = tempStr;
      if (tempStr == NULL)
         boolFlag = FALSE;

      if (boolFlag) {
         if (strcmp(sz_CountryName,"")) {
            // Open a filtered Recordset object.
            rstPublishersCountry = FilterField(rstPublishers, "Country", strCountry);
            recCount = rstPublishersCountry-&gt;GetRecordCount();
            if (recCount == 0)
               printf("\nNo publishers from that country.\n");
            else {
               // Print number of records for the original recordset object and the 
               // filtered Recordset object.
               printf("\nOrders in original recordset:\n%d", intPublisherCount);
               printf("\nOrders in filtered recordset (Country = '%s'): \n%d\n\n", 
                      (LPCSTR)strCountry, rstPublishersCountry-&gt;RecordCount);
            }
         }
      }
   }
   catch(_com_error &amp;e) {
      // Notify the user of errors if any.
      _variant_t vtConnect = rstPublishers-&gt;GetActiveConnection();

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

   // Clean up objects before exit.
   if (rstPublishers)
      if (rstPublishers-&gt;State == adStateOpen)
         rstPublishers-&gt;Close();
   if (rstPublishersCountry)
      if (rstPublishersCountry-&gt;State == adStateOpen)
         rstPublishersCountry-&gt;Close();
}

_RecordsetPtr FilterField(_RecordsetPtr rstTemp,_bstr_t strField, _bstr_t strFilter) {
   // Set a filter on the specified Recordset object and then open a new Recordset object.
   rstTemp-&gt;Filter  = strField + " = '" + strFilter + "'";
   return rstTemp;
}

void FilterX2() {
   _RecordsetPtr rstPublishers;
   CPublishers publishers;

   // Define Other Variables
   HRESULT hr = S_OK;
   IADORecordBinding *picRs = NULL;   // Interface Pointer declared

   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source'; Initial Catalog='pubs'; Integrated Security='SSPI';");
   try {
      // Open recordset with data from Publishers table.
      rstPublishers.CreateInstance(__uuidof(Recordset)); 
      rstPublishers-&gt;CursorType = adOpenStatic;

      TESTHR(rstPublishers-&gt;Open("SELECT * FROM publishers WHERE "
         "Country='USA'", strCnn, adOpenStatic, adLockReadOnly, adCmdText));

      // Open an IADORecordBinding interface pointer 
      // which we'll use for Binding Recordset to a class
      TESTHR(rstPublishers-&gt;QueryInterface(__uuidof(IADORecordBinding), (LPVOID*)&amp;picRs));

      // Bind the Recordset to a C++ Class here 
      TESTHR(picRs-&gt;BindToRecordset(&amp;publishers));

      // Print current data in recordset.
      rstPublishers-&gt;MoveFirst();

      while (!rstPublishers-&gt;EndOfFile) {
         printf("%s, %s\n", 
            publishers.lP_pubnameStatus == adFldOK ? 
            publishers.m_szP_pubname: "&lt;NULL&gt;",
            publishers.lP_countryStatus == adFldOK ? 
            publishers.m_szP_country: "&lt;NULL&gt;");

         rstPublishers-&gt;MoveNext();
      }
   }
   catch (_com_error &amp;e) {
      // Notify the user of errors if any.
      _variant_t vtConnect = rstPublishers-&gt;GetActiveConnection();

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

   // Clean up objects before exit.  Release the IADORecordset Interface here   
   if (picRs)
      picRs-&gt;Release();

   if (rstPublishers)
      if (rstPublishers-&gt;State == adStateOpen)
         rstPublishers-&gt;Close();
}

void PrintProviderError(_ConnectionPtr pCnn1) {
   // Print Provider Errors from Connection object.
   // pErr is a record object in the Connection's Error collection.
   ErrorPtr pErr  = NULL;

   if ( (pCnn1-&gt;Errors-&gt;Count) &gt; 0) {
      long nCount = pCnn1-&gt;Errors-&gt;Count;
      // Collection ranges from 0 to nCount -1.
      for (long i = 0 ; i &lt; nCount ; i++) {
         pErr = pCnn1-&gt;Errors-&gt;GetItem(i);
         printf("\t Error number: %x\t%s", pErr-&gt;Number, (LPCSTR) pErr-&gt;Description);
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
      </codeExample>
      <section>
        <title>
          <caps:sentence sentenceid="ceb268093ddd5aa9df1769eda5d1c8cd" id="tgt4" class="tgtSentence">Sample Input</caps:sentence>
        </title>
        <content>
          <code>USA</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="fd092663f471aa93d2d7e515d6b47a8d" id="tgt5" class="tgtSentence">Sample Output</caps:sentence>
        </title>
        <content>
          <code>Orders in original recordset:
8
Orders in filtered recordset (Country = 'USA'):
6

New Moon Books, USA
Binnet &amp; Hardley, USA
Algodata Infosystems, USA
Five Lakes Publishing, USA
Ramona Publishers, USA
Scootney Books, USA</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link>
        <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property to open a new <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> based on a specified condition applied to an existing <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It uses the <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink> property to show the number of records in the two <legacyBold>Recordsets</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The FilterField function is required for this procedure to run.</caps:sentence>
        </para>
      </introduction>
      <codeExample>
        <code>// BeginFilterCpp.cpp
// compile with: /EHsc /c
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

#include &lt;stdio.h&gt;
#include &lt;ole2.h&gt;
#include &lt;conio.h&gt;
#include "icrsint.h"

// Class extracts only Pub Name and Country Name.
class CPublishers : public CADORecordBinding {
   BEGIN_ADO_BINDING(CPublishers)

   // Column Pub Name is the 2nd field in the recordset
   ADO_VARIABLE_LENGTH_ENTRY2(2, adVarChar, m_szP_pubname, sizeof(m_szP_pubname), 
                              lP_pubnameStatus, TRUE)

   // Column Country Name is the 5th field in the recordset
   ADO_VARIABLE_LENGTH_ENTRY2(5, adVarChar, m_szP_country, sizeof(m_szP_country), 
                              lP_countryStatus, TRUE)

   END_ADO_BINDING()

public:
   CHAR m_szP_pubname[50];
   ULONG lP_pubnameStatus;
   CHAR m_szP_country[50];
   ULONG lP_countryStatus;
};

// Function declarations
inline void TESTHR(HRESULT x) { if FAILED(x) _com_issue_error(x); };
void FilterX();
_RecordsetPtr FilterField(_RecordsetPtr rstTemp, _bstr_t strField, _bstr_t strFilter);
void FilterX2();
void PrintProviderError(_ConnectionPtr pCnn1);
void PrintComError(_com_error &amp;e);

inline char* mygets(char* strDest, int n) {
   char strExBuff[10];
   char* pstrRet = fgets(strDest, n, stdin);

   if (pstrRet == NULL)
      return NULL;

   if (!strrchr(strDest, '\n'))
      // Exhaust the input buffer.
      do {
         fgets(strExBuff, sizeof(strExBuff), stdin);
      } while (!strrchr(strExBuff, '\n'));
   else
      // Replace '\n' with '\0'
      strDest[strrchr(strDest, '\n') - strDest] = '\0';

   return pstrRet;
}

int main() {
   HRESULT hr = S_OK;

   if ( FAILED(::CoInitialize(NULL)) )
      return -1;

   FilterX();
   FilterX2();

   ::CoUninitialize();
}

void FilterX() {
   // Define ADO object pointers, initialize pointers on define.  These are in the ADODB::  namespace.
   _RecordsetPtr rstPublishers = NULL;
   _RecordsetPtr rstPublishersCountry = NULL;

   // Define Other Variables
   HRESULT hr = S_OK;
   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source'; Initial Catalog='pubs'; Integrated Security='SSPI';");
   int intPublisherCount = 0;
   long recCount = 0;
   _bstr_t strCountry; 
   _bstr_t strMessage;
   char *tempStr;
   CHAR sz_CountryName[50];
   bool boolFlag = TRUE;
   char * token1;

   try {
      // Open recordset with data from Publishers table.
      rstPublishers.CreateInstance(__uuidof(Recordset));
      rstPublishersCountry.CreateInstance(__uuidof(Recordset));

      rstPublishers-&gt;CursorType = adOpenStatic;

      TESTHR(rstPublishers-&gt;Open("publishers", strCnn, adOpenStatic , adLockReadOnly, adCmdTable));

      // Populate the Recordset.
      intPublisherCount = rstPublishers-&gt;RecordCount;

      // Get user input.
      printf("Enter a country to filter on:");
      mygets(sz_CountryName, 50);

      // Trim the string
      tempStr = strtok_s(sz_CountryName, "  \t", &amp;token1);
      strCountry = tempStr;
      if (tempStr == NULL)
         boolFlag = FALSE;

      if (boolFlag) {
         if (strcmp(sz_CountryName,"")) {
            // Open a filtered Recordset object.
            rstPublishersCountry = FilterField(rstPublishers, "Country", strCountry);
            recCount = rstPublishersCountry-&gt;GetRecordCount();
            if (recCount == 0)
               printf("\nNo publishers from that country.\n");
            else {
               // Print number of records for the original recordset object and the 
               // filtered Recordset object.
               printf("\nOrders in original recordset:\n%d", intPublisherCount);
               printf("\nOrders in filtered recordset (Country = '%s'): \n%d\n\n", 
                      (LPCSTR)strCountry, rstPublishersCountry-&gt;RecordCount);
            }
         }
      }
   }
   catch(_com_error &amp;e) {
      // Notify the user of errors if any.
      _variant_t vtConnect = rstPublishers-&gt;GetActiveConnection();

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

   // Clean up objects before exit.
   if (rstPublishers)
      if (rstPublishers-&gt;State == adStateOpen)
         rstPublishers-&gt;Close();
   if (rstPublishersCountry)
      if (rstPublishersCountry-&gt;State == adStateOpen)
         rstPublishersCountry-&gt;Close();
}

_RecordsetPtr FilterField(_RecordsetPtr rstTemp,_bstr_t strField, _bstr_t strFilter) {
   // Set a filter on the specified Recordset object and then open a new Recordset object.
   rstTemp-&gt;Filter  = strField + " = '" + strFilter + "'";
   return rstTemp;
}

void FilterX2() {
   _RecordsetPtr rstPublishers;
   CPublishers publishers;

   // Define Other Variables
   HRESULT hr = S_OK;
   IADORecordBinding *picRs = NULL;   // Interface Pointer declared

   _bstr_t strCnn("Provider='sqloledb'; Data Source='My_Data_Source'; Initial Catalog='pubs'; Integrated Security='SSPI';");
   try {
      // Open recordset with data from Publishers table.
      rstPublishers.CreateInstance(__uuidof(Recordset)); 
      rstPublishers-&gt;CursorType = adOpenStatic;

      TESTHR(rstPublishers-&gt;Open("SELECT * FROM publishers WHERE "
         "Country='USA'", strCnn, adOpenStatic, adLockReadOnly, adCmdText));

      // Open an IADORecordBinding interface pointer 
      // which we'll use for Binding Recordset to a class
      TESTHR(rstPublishers-&gt;QueryInterface(__uuidof(IADORecordBinding), (LPVOID*)&amp;picRs));

      // Bind the Recordset to a C++ Class here 
      TESTHR(picRs-&gt;BindToRecordset(&amp;publishers));

      // Print current data in recordset.
      rstPublishers-&gt;MoveFirst();

      while (!rstPublishers-&gt;EndOfFile) {
         printf("%s, %s\n", 
            publishers.lP_pubnameStatus == adFldOK ? 
            publishers.m_szP_pubname: "&lt;NULL&gt;",
            publishers.lP_countryStatus == adFldOK ? 
            publishers.m_szP_country: "&lt;NULL&gt;");

         rstPublishers-&gt;MoveNext();
      }
   }
   catch (_com_error &amp;e) {
      // Notify the user of errors if any.
      _variant_t vtConnect = rstPublishers-&gt;GetActiveConnection();

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

   // Clean up objects before exit.  Release the IADORecordset Interface here   
   if (picRs)
      picRs-&gt;Release();

   if (rstPublishers)
      if (rstPublishers-&gt;State == adStateOpen)
         rstPublishers-&gt;Close();
}

void PrintProviderError(_ConnectionPtr pCnn1) {
   // Print Provider Errors from Connection object.
   // pErr is a record object in the Connection's Error collection.
   ErrorPtr pErr  = NULL;

   if ( (pCnn1-&gt;Errors-&gt;Count) &gt; 0) {
      long nCount = pCnn1-&gt;Errors-&gt;Count;
      // Collection ranges from 0 to nCount -1.
      for (long i = 0 ; i &lt; nCount ; i++) {
         pErr = pCnn1-&gt;Errors-&gt;GetItem(i);
         printf("\t Error number: %x\t%s", pErr-&gt;Number, (LPCSTR) pErr-&gt;Description);
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
      </codeExample>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Sample Input</caps:sentence>
        </title>
        <content>
          <code>USA</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Sample Output</caps:sentence>
        </title>
        <content>
          <code>Orders in original recordset:
8
Orders in filtered recordset (Country = 'USA'):
6

New Moon Books, USA
Binnet &amp; Hardley, USA
Algodata Infosystems, USA
Five Lakes Publishing, USA
Ramona Publishers, USA
Scootney Books, USA</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link>
        <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
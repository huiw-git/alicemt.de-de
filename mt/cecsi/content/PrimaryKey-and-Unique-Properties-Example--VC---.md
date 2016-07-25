---
title: "PrimaryKey and Unique Properties Example (VC++)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d51814a2-ff7d-48ed-b719-99776da2091a
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
# PrimaryKey and Unique Properties Example (VC++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0822021728a85b6af8deea95455e565a" id="tgt1" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="30185312-5e09-4804-852d-e505d660113a">PrimaryKey</legacyLink> and <legacyLink xlink:href="85fd4bd0-393b-4dc1-9d73-80dced4f2fbe">Unique</legacyLink> properties of an <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="6376cd485b7478493d47e7e09066e218" id="tgt2" class="tgtSentence"> The code creates a new table with two columns.</caps:sentence>
          <caps:sentence sentenceid="99339e1e1cedd8556cd0e18486d72d82" id="tgt3" class="tgtSentence"> The <legacyBold>PrimaryKey</legacyBold> and <legacyBold>Unique</legacyBold> properties are used to make one column the primary key for which duplicate values are not allowed.</caps:sentence>
        </para>
        <code>// BeginPrimaryKeyCpp.cpp
// compile with: /EHsc
#import "msado15.dll" rename("EOF", "EndOfFile")
#import "msadox.dll" no_namespace

#include "iostream"
using namespace std;

inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);};

int main() {
   if ( FAILED(::CoInitialize(NULL)) )
      return -1;

   HRESULT hr = S_OK;

   // Define and initialize ADOX object pointers. These are in ADODB namespace.
   _CatalogPtr m_pCatalog = NULL;
   _TablePtr m_pTableNew = NULL;
   _IndexPtr m_pIndexNew  = NULL;
   _IndexPtr m_pIndex  = NULL;
   _ColumnPtr m_pColumn = NULL;

   // Define string variable
   _bstr_t strcnn("Provider='Microsoft.JET.OLEDB.4.0';Data Source = 'c:\\Northwind.mdb';");

   try {
      TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog)));
      TESTHR(hr = m_pTableNew.CreateInstance(__uuidof(Table)));
      TESTHR(hr = m_pIndexNew.CreateInstance(__uuidof(Index)));
      TESTHR(hr = m_pIndex.CreateInstance(__uuidof(Index)));
      TESTHR(hr = m_pColumn.CreateInstance(__uuidof(Column)));

      // Connect the catalog
      m_pCatalog-&gt;PutActiveConnection(strcnn);

      // Name new table
      m_pTableNew-&gt;Name = "NewTable";

      // Append a numeric and a text field to new table.
      m_pTableNew-&gt;Columns-&gt;Append("NumField", adInteger, 20);
      m_pTableNew-&gt;Columns-&gt;Append("TextField", adVarWChar, 20);

      // Append new Primary Key index on NumField column to new table
      m_pIndexNew-&gt;Name = "NumIndex";
      m_pIndexNew-&gt;Columns-&gt;Append("NumField", adInteger, 0);
      // here "-1" is required instead of "true".
      m_pIndexNew-&gt;PutPrimaryKey(-1);
      m_pIndexNew-&gt;PutUnique(-1);
      m_pTableNew-&gt;Indexes-&gt;Append(_variant_t ((IDispatch*)m_pIndexNew));

      // Append an index on Textfield to new table.  Note the different technique: Specifying 
      // index and column name as parameters of the Append method
      m_pTableNew-&gt;Indexes-&gt;Append("TextIndex", "TextField");

      // Append the new table
      m_pCatalog-&gt;Tables-&gt;Append(_variant_t ((IDispatch*)m_pTableNew));

      cout &lt;&lt; m_pTableNew-&gt;Indexes-&gt;Count &lt;&lt; " Indexes in " &lt;&lt; m_pTableNew-&gt;Name &lt;&lt; " Table" &lt;&lt; endl;
      m_pCatalog-&gt;Tables-&gt;Refresh();

      _variant_t vIndex;
      // Enumerate Indexes collection.
      for ( long lIndex = 0 ; lIndex &lt; m_pTableNew-&gt;Indexes-&gt;Count ; lIndex++ ) {
         vIndex = lIndex;
         m_pIndex = m_pTableNew-&gt;Indexes-&gt;GetItem(vIndex);
         cout &lt;&lt; "Index " &lt;&lt; m_pIndex-&gt;Name &lt;&lt; endl;
         cout &lt;&lt; "   Primary key = " &lt;&lt; (m_pIndex-&gt;GetPrimaryKey() ? "True" : "False") &lt;&lt; endl;
         cout &lt;&lt; "   Unique = "  &lt;&lt; (m_pIndex-&gt;GetUnique() ? "True" : "False") &lt;&lt; endl;

         // Enumerate Columns collection of each Index object.
         cout &lt;&lt; "    Columns" &lt;&lt; endl;

         for ( long lIndex = 0 ; lIndex &lt; m_pIndex-&gt;Columns-&gt;Count ; lIndex++ ) {
            vIndex = lIndex;
            m_pColumn = m_pIndex-&gt;Columns-&gt;GetItem(vIndex);
            cout &lt;&lt; "       " &lt;&lt; m_pColumn-&gt;Name &lt;&lt; endl;
         }
      }

      // Delete new table as this is a demonstration
      m_pCatalog-&gt;Tables-&gt;Delete(m_pTableNew-&gt;Name);
   }
   catch(_com_error &amp;e) {
      // Notify the user of errors if any.
      _bstr_t bstrSource(e.Source());
      _bstr_t bstrDescription(e.Description());

      printf("\n\tSource :  %s \n\tdescription : %s \n ", (LPCSTR)bstrSource, (LPCSTR)bstrDescription);
   }
   catch(...) {
      cout &lt;&lt; "Error occured in PrimaryKeyX...." &lt;&lt; endl;
   }

   m_pCatalog = NULL;
   ::CoUninitialize();
}</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example demonstrates the <legacyLink xlink:href="30185312-5e09-4804-852d-e505d660113a">PrimaryKey</legacyLink> and <legacyLink xlink:href="85fd4bd0-393b-4dc1-9d73-80dced4f2fbe">Unique</legacyLink> properties of an <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The code creates a new table with two columns.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The <legacyBold>PrimaryKey</legacyBold> and <legacyBold>Unique</legacyBold> properties are used to make one column the primary key for which duplicate values are not allowed.</caps:sentence>
        </para>
        <code>// BeginPrimaryKeyCpp.cpp
// compile with: /EHsc
#import "msado15.dll" rename("EOF", "EndOfFile")
#import "msadox.dll" no_namespace

#include "iostream"
using namespace std;

inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);};

int main() {
   if ( FAILED(::CoInitialize(NULL)) )
      return -1;

   HRESULT hr = S_OK;

   // Define and initialize ADOX object pointers. These are in ADODB namespace.
   _CatalogPtr m_pCatalog = NULL;
   _TablePtr m_pTableNew = NULL;
   _IndexPtr m_pIndexNew  = NULL;
   _IndexPtr m_pIndex  = NULL;
   _ColumnPtr m_pColumn = NULL;

   // Define string variable
   _bstr_t strcnn("Provider='Microsoft.JET.OLEDB.4.0';Data Source = 'c:\\Northwind.mdb';");

   try {
      TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog)));
      TESTHR(hr = m_pTableNew.CreateInstance(__uuidof(Table)));
      TESTHR(hr = m_pIndexNew.CreateInstance(__uuidof(Index)));
      TESTHR(hr = m_pIndex.CreateInstance(__uuidof(Index)));
      TESTHR(hr = m_pColumn.CreateInstance(__uuidof(Column)));

      // Connect the catalog
      m_pCatalog-&gt;PutActiveConnection(strcnn);

      // Name new table
      m_pTableNew-&gt;Name = "NewTable";

      // Append a numeric and a text field to new table.
      m_pTableNew-&gt;Columns-&gt;Append("NumField", adInteger, 20);
      m_pTableNew-&gt;Columns-&gt;Append("TextField", adVarWChar, 20);

      // Append new Primary Key index on NumField column to new table
      m_pIndexNew-&gt;Name = "NumIndex";
      m_pIndexNew-&gt;Columns-&gt;Append("NumField", adInteger, 0);
      // here "-1" is required instead of "true".
      m_pIndexNew-&gt;PutPrimaryKey(-1);
      m_pIndexNew-&gt;PutUnique(-1);
      m_pTableNew-&gt;Indexes-&gt;Append(_variant_t ((IDispatch*)m_pIndexNew));

      // Append an index on Textfield to new table.  Note the different technique: Specifying 
      // index and column name as parameters of the Append method
      m_pTableNew-&gt;Indexes-&gt;Append("TextIndex", "TextField");

      // Append the new table
      m_pCatalog-&gt;Tables-&gt;Append(_variant_t ((IDispatch*)m_pTableNew));

      cout &lt;&lt; m_pTableNew-&gt;Indexes-&gt;Count &lt;&lt; " Indexes in " &lt;&lt; m_pTableNew-&gt;Name &lt;&lt; " Table" &lt;&lt; endl;
      m_pCatalog-&gt;Tables-&gt;Refresh();

      _variant_t vIndex;
      // Enumerate Indexes collection.
      for ( long lIndex = 0 ; lIndex &lt; m_pTableNew-&gt;Indexes-&gt;Count ; lIndex++ ) {
         vIndex = lIndex;
         m_pIndex = m_pTableNew-&gt;Indexes-&gt;GetItem(vIndex);
         cout &lt;&lt; "Index " &lt;&lt; m_pIndex-&gt;Name &lt;&lt; endl;
         cout &lt;&lt; "   Primary key = " &lt;&lt; (m_pIndex-&gt;GetPrimaryKey() ? "True" : "False") &lt;&lt; endl;
         cout &lt;&lt; "   Unique = "  &lt;&lt; (m_pIndex-&gt;GetUnique() ? "True" : "False") &lt;&lt; endl;

         // Enumerate Columns collection of each Index object.
         cout &lt;&lt; "    Columns" &lt;&lt; endl;

         for ( long lIndex = 0 ; lIndex &lt; m_pIndex-&gt;Columns-&gt;Count ; lIndex++ ) {
            vIndex = lIndex;
            m_pColumn = m_pIndex-&gt;Columns-&gt;GetItem(vIndex);
            cout &lt;&lt; "       " &lt;&lt; m_pColumn-&gt;Name &lt;&lt; endl;
         }
      }

      // Delete new table as this is a demonstration
      m_pCatalog-&gt;Tables-&gt;Delete(m_pTableNew-&gt;Name);
   }
   catch(_com_error &amp;e) {
      // Notify the user of errors if any.
      _bstr_t bstrSource(e.Source());
      _bstr_t bstrDescription(e.Description());

      printf("\n\tSource :  %s \n\tdescription : %s \n ", (LPCSTR)bstrSource, (LPCSTR)bstrDescription);
   }
   catch(...) {
      cout &lt;&lt; "Error occured in PrimaryKeyX...." &lt;&lt; endl;
   }

   m_pCatalog = NULL;
   ::CoUninitialize();
}</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
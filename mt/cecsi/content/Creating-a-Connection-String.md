---
title: "Creating a Connection String"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 14eae122-2d1e-40c8-b88e-b7cb8dfbc93b
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
# Creating a Connection String
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f151a79908cc3199d32916702e45b775" id="tgt1" class="tgtSentence">A connection string consists of a list of argument/value pairs (that is, parameters), separated by semi-colons.</caps:sentence>
          <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt2" class="tgtSentence"> For example:</caps:sentence>
        </para>
        <code>"arg1=val1; arg2=val2; ... argN=valN;"</code>
        <para>
          <caps:sentence sentenceid="c1d3ca1c1af257e9603bc087e740304e" id="tgt3" class="tgtSentence">All the parameters must be recognized by either ADO or the specified provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8f4b3f84611e1501e39793c94498ca37" id="tgt4" class="tgtSentence">ADO recognizes the following five arguments in a connection string.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="03cde060e90acdd58ff9f0a4d785d43b" id="tgt5" class="tgtSentence">Argument</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt6" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="56ecc25a1ea1e9395ffe2d13c24e0ea2" id="tgt7" class="tgtSentence">               <legacyItalic>Provider</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2d7704648beb665496f61a27facfb14" id="tgt8" class="tgtSentence">Specifies the name of a provider to use for the connection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="efd6aa2723f2af8c606a10666697377b" id="tgt9" class="tgtSentence">               <legacyItalic>File Name</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a3a212bd1f03eaf7daa1955507182815" id="tgt10" class="tgtSentence">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e09249b6008b93ba11520edc3fb750da" id="tgt11" class="tgtSentence">               <legacyItalic>URL</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c828997e7783b63901a7412884013a85" id="tgt12" class="tgtSentence">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="10019bc603aef70d65b43398fdf9dd9b" id="tgt13" class="tgtSentence">               <legacyItalic>Remote Provider</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="665ec1c0d65eabbeb74cb50fcba38217" id="tgt14" class="tgtSentence">Specifies the name of a provider to use when opening a client-side connection.</caps:sentence>
                  <caps:sentence sentenceid="3a3a994bfe9d2acaa57f71f29e3756ef" id="tgt15" class="tgtSentence"> (Remote Data Service only.)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ea0d4692924741835c836218e0864219" id="tgt16" class="tgtSentence">               <legacyItalic>Remote Server</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5a13d97ffbc5aa7d4cdb665cd7beb5e8" id="tgt17" class="tgtSentence">Specifies the path name of the server to use when opening a client-side connection.</caps:sentence>
                  <caps:sentence sentenceid="3a3a994bfe9d2acaa57f71f29e3756ef" id="tgt18" class="tgtSentence"> (Remote Data Service only.)</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="bea62d0c5788dd5713d1add453d2b897" id="tgt19" class="tgtSentence">Other arguments are passed to the provider named in the <legacyItalic>Provider</legacyItalic> argument, without any processing by ADO.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e952f2ee1ee5e241a38ba137ab9b3980" id="tgt20" class="tgtSentence">The HelloData application in <legacyLink xlink:href="de4bcd56-dac2-45e6-95ab-9fd7f25878fc">HelloData: A Simple ADO Application</legacyLink> used the following connection string:</caps:sentence>
        </para>
        <code>m_sConnStr = "Provider=SQLOLEDB;Data Source=MySqlServer;" &amp; _
             "Initial Catalog=Northwind;Integrated Security='SSPI';"</code>
        <para>
          <caps:sentence sentenceid="40a73ae804feedee41b37ccdc54675ee" id="tgt21" class="tgtSentence">In this connection string, ADO recognizes only the <codeInline>"Provider=SQLOLEDB"</codeInline> parameter, which specifies the Microsoft OLE DB Provider for SQL Server as the ADO data source.</caps:sentence>
          <caps:sentence sentenceid="e6450758334077a318bfd380771a4459" id="tgt22" class="tgtSentence"> The rest of the argument/value pairs, <codeInline>"Data Source=MySqlServer; Initial Catalog=Northwind;Integrated Security='SSPI';"</codeInline>, are passed verbatim to this provider.</caps:sentence>
          <caps:sentence sentenceid="6b32cf00b40491fcc47ebbf725de5088" id="tgt23" class="tgtSentence"> The type and validity of such parameters are provider-specific.</caps:sentence>
          <caps:sentence sentenceid="da7b897fcad2ce6bf432440786b0af39" id="tgt24" class="tgtSentence"> For information about valid parameters that can be passed in the connection string, consult the individual provider's documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7b1157726d4d37ff67b3be6e1370e3f3" id="tgt25" class="tgtSentence">According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the <legacyItalic>Data Source</legacyItalic> parameter and "Database" for the <legacyItalic>Initial Catalog</legacyItalic> parameter.</caps:sentence>
          <caps:sentence sentenceid="5972bb5c927b85185eb47f40813b563f" id="tgt26" class="tgtSentence"> Thus, the following connection string would produce results identical to the one above:</caps:sentence>
        </para>
        <code>m_sConnStr = "Provider=SQLOLEDB;Server=MySqlServer;" &amp; _
             "Database=Northwind;Integrated Security='SSPI';"</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">A connection string consists of a list of argument/value pairs (that is, parameters), separated by semi-colons.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For example:</caps:sentence>
        </para>
        <code>"arg1=val1; arg2=val2; ... argN=valN;"</code>
        <para>
          <caps:sentence id="src3" class="srcSentence">All the parameters must be recognized by either ADO or the specified provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">ADO recognizes the following five arguments in a connection string.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Argument</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">               <legacyItalic>Provider</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Specifies the name of a provider to use for the connection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">               <legacyItalic>File Name</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">               <legacyItalic>URL</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">               <legacyItalic>Remote Provider</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Specifies the name of a provider to use when opening a client-side connection.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> (Remote Data Service only.)</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">               <legacyItalic>Remote Server</legacyItalic>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Specifies the path name of the server to use when opening a client-side connection.</caps:sentence>
                  <caps:sentence id="src18" class="srcSentence"> (Remote Data Service only.)</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src19" class="srcSentence">Other arguments are passed to the provider named in the <legacyItalic>Provider</legacyItalic> argument, without any processing by ADO.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src20" class="srcSentence">The HelloData application in <legacyLink xlink:href="de4bcd56-dac2-45e6-95ab-9fd7f25878fc">HelloData: A Simple ADO Application</legacyLink> used the following connection string:</caps:sentence>
        </para>
        <code>m_sConnStr = "Provider=SQLOLEDB;Data Source=MySqlServer;" &amp; _
             "Initial Catalog=Northwind;Integrated Security='SSPI';"</code>
        <para>
          <caps:sentence id="src21" class="srcSentence">In this connection string, ADO recognizes only the <codeInline>"Provider=SQLOLEDB"</codeInline> parameter, which specifies the Microsoft OLE DB Provider for SQL Server as the ADO data source.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> The rest of the argument/value pairs, <codeInline>"Data Source=MySqlServer; Initial Catalog=Northwind;Integrated Security='SSPI';"</codeInline>, are passed verbatim to this provider.</caps:sentence>
          <caps:sentence id="src23" class="srcSentence"> The type and validity of such parameters are provider-specific.</caps:sentence>
          <caps:sentence id="src24" class="srcSentence"> For information about valid parameters that can be passed in the connection string, consult the individual provider's documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src25" class="srcSentence">According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the <legacyItalic>Data Source</legacyItalic> parameter and "Database" for the <legacyItalic>Initial Catalog</legacyItalic> parameter.</caps:sentence>
          <caps:sentence id="src26" class="srcSentence"> Thus, the following connection string would produce results identical to the one above:</caps:sentence>
        </para>
        <code>m_sConnStr = "Provider=SQLOLEDB;Server=MySqlServer;" &amp; _
             "Database=Northwind;Integrated Security='SSPI';"</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
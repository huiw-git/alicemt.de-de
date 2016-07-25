---
title: "Using a Connection Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b34f971-5699-43e7-9b15-137d334fa66e
caps.latest.revision: 15
caps.handback.revision: 15
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
# Using a Connection Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b262cca5c67eec12f2e4bfd71b677f6f" id="tgt1" class="tgtSentence">Before opening a <legacyBold>Connection</legacyBold> object, you must define certain information about the data source and type of connection.</caps:sentence>
          <caps:sentence sentenceid="7cf9721f0d9452df1156bb28b368e406" id="tgt2" class="tgtSentence"> Most of this information is held by the <legacyItalic>ConnectionString</legacyItalic> parameter of the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open method</legacyLink> on the <legacyBold>Connection</legacyBold> object, or by the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString property</legacyLink> on the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="20a4ac8788dbc2f577379be61341479c" id="tgt3" class="tgtSentence"> A connection string consists of a list of argument/value pairs separated by semi-colons, with the values enclosed within single quotes.</caps:sentence>
          <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt4" class="tgtSentence"> For example:</caps:sentence>
        </para>
        <code>Dim sConn As String
sConn = "Provider='SQLOLEDB';Data Source='MySqlServer';" &amp; _
             "Initial Catalog='Northwind';Integrated Security='SSPI';"</code>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="c9ec309c4d58e56ec0f4d645151f2199" id="tgt5" class="tgtSentence">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string.</caps:sentence>
            <caps:sentence sentenceid="221f830de8cdc60fe9579ee1a80e7c47" id="tgt6" class="tgtSentence"> For more information about DSNs, see <legacyLink xlink:href="67cc4945-4850-4eb4-8da6-b835ddaeca4c">Managing Data Sources</legacyLink> in the ODBC Programmer's Reference.</caps:sentence>
            <caps:sentence sentenceid="24029318cbbd0d5b7c5f79a17bd1b4c3" id="tgt7" class="tgtSentence"> For more information about UDLs, see <legacyLink xlink:href="95c180ea-bd4f-4dca-b95a-576afd135bbc">Data Link API Overview</legacyLink> in the OLE DB Programmer's Reference.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="27463e164d06d4adb53f10958f1f93a8" id="tgt8" class="tgtSentence">Typically, you establish a connection by calling the <legacyBold>Connection.Open</legacyBold> method with an appropriate a <legacyItalic>connection string</legacyItalic> as its parameter.</caps:sentence>
          <caps:sentence sentenceid="3240e1e9d6e6ec7e70e5b9bf6a999bf1" id="tgt9" class="tgtSentence"> An example is shown in the following Visual Basic code snippet:</caps:sentence>
        </para>
        <code>Dim oConn As ADODB.Connection
Dim oRs As ADODB.Recordset
Dim sConn As String
Dim sSQL as String



' Open a connection.
Set oConn = New ADODB.Connection
.Open 

' Make a query over the connection.
sSQL = "SELECT ProductID, ProductName, CategoryID, UnitPrice " &amp; _
             "FROM Products"
Set oRs = New ADODB.Recordset
oRs.Open sSQL, , adOpenStatic, adLockBatchOptimistic, adCmdText
                      
MsgBox oRs.RecordCount
        
' Close the connection.
oConn.Close
Set oConn = Nothing
    </code>
        <para>
          <caps:sentence sentenceid="c1b585c70c3ad4f21de88a3805762da8" id="tgt10" class="tgtSentence">Here <legacyBold>oRs.Open</legacyBold> takes a <legacyBold>Connection</legacyBold> object (<legacyItalic>oConn</legacyItalic>) variable as the value of its <legacyItalic>ActiveConnection</legacyItalic> parameter.</caps:sentence>
          <caps:sentence sentenceid="3077a4f6ea17616a7ddda1f4bc328067" id="tgt11" class="tgtSentence"> Also, the <legacyBold>Connection.CursorLocation</legacyBold> property assumes the default value of <legacyBold>adUseServer</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="8666ddab1250b42b677eebf432c2b2ed" id="tgt12" class="tgtSentence"> Contrast this to the <legacyLink xlink:href="de4bcd56-dac2-45e6-95ab-9fd7f25878fc">HelloData</legacyLink> example in the preceding section.</caps:sentence>
          <caps:sentence sentenceid="1794456153acd8adca8c98f6789ddf30" id="tgt13" class="tgtSentence"> The following instruction would result in run-time errors.</caps:sentence>
        </para>
        <code>oRs.MarshalOptions = adMarshalModifiedOnly
' Disconnect the Recordset.
Set oRs.ActiveConnection = Nothing</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Before opening a <legacyBold>Connection</legacyBold> object, you must define certain information about the data source and type of connection.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Most of this information is held by the <legacyItalic>ConnectionString</legacyItalic> parameter of the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open method</legacyLink> on the <legacyBold>Connection</legacyBold> object, or by the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString property</legacyLink> on the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> A connection string consists of a list of argument/value pairs separated by semi-colons, with the values enclosed within single quotes.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example:</caps:sentence>
        </para>
        <code>Dim sConn As String
sConn = "Provider='SQLOLEDB';Data Source='MySqlServer';" &amp; _
             "Initial Catalog='Northwind';Integrated Security='SSPI';"</code>
        <alert class="note">
          <para>
            <caps:sentence id="src5" class="srcSentence">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For more information about DSNs, see <legacyLink xlink:href="67cc4945-4850-4eb4-8da6-b835ddaeca4c">Managing Data Sources</legacyLink> in the ODBC Programmer's Reference.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> For more information about UDLs, see <legacyLink xlink:href="95c180ea-bd4f-4dca-b95a-576afd135bbc">Data Link API Overview</legacyLink> in the OLE DB Programmer's Reference.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src8" class="srcSentence">Typically, you establish a connection by calling the <legacyBold>Connection.Open</legacyBold> method with an appropriate a <legacyItalic>connection string</legacyItalic> as its parameter.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> An example is shown in the following Visual Basic code snippet:</caps:sentence>
        </para>
        <code>Dim oConn As ADODB.Connection
Dim oRs As ADODB.Recordset
Dim sConn As String
Dim sSQL as String



' Open a connection.
Set oConn = New ADODB.Connection
.Open 

' Make a query over the connection.
sSQL = "SELECT ProductID, ProductName, CategoryID, UnitPrice " &amp; _
             "FROM Products"
Set oRs = New ADODB.Recordset
oRs.Open sSQL, , adOpenStatic, adLockBatchOptimistic, adCmdText
                      
MsgBox oRs.RecordCount
        
' Close the connection.
oConn.Close
Set oConn = Nothing
    </code>
        <para>
          <caps:sentence id="src10" class="srcSentence">Here <legacyBold>oRs.Open</legacyBold> takes a <legacyBold>Connection</legacyBold> object (<legacyItalic>oConn</legacyItalic>) variable as the value of its <legacyItalic>ActiveConnection</legacyItalic> parameter.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> Also, the <legacyBold>Connection.CursorLocation</legacyBold> property assumes the default value of <legacyBold>adUseServer</legacyBold>.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Contrast this to the <legacyLink xlink:href="de4bcd56-dac2-45e6-95ab-9fd7f25878fc">HelloData</legacyLink> example in the preceding section.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> The following instruction would result in run-time errors.</caps:sentence>
        </para>
        <code>oRs.MarshalOptions = adMarshalModifiedOnly
' Disconnect the Recordset.
Set oRs.ActiveConnection = Nothing</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
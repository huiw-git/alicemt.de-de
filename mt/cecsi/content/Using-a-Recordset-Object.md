---
title: "Using a Recordset Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 01c630d8-eb35-4bd0-a99f-7c0f85316cc1
caps.latest.revision: 10
caps.handback.revision: 10
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
# Using a Recordset Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bedc49c54cd8c6410632eac9b18bdd37" id="tgt1" class="tgtSentence">Alternatively, you can use <legacyBold>Recordset.Open</legacyBold> to implicitly establish a connection and issue a command over that connection in a single operation.</caps:sentence>
          <caps:sentence sentenceid="490f4c7be0d5392ddb973803d168419d" id="tgt2" class="tgtSentence"> For example, in Visual Basic:</caps:sentence>
        </para>
        <code>Dim oRs As ADODB.Recordset
Dim sConn As String
Dim sSQL as String

<codeFeaturedElement xmlns="">sConn = "Provider='SQLOLEDB';Data Source='MySqlServer';" &amp; _</codeFeaturedElement><codeFeaturedElement xmlns="">             "Initial Catalog='Northwind';Integrated Security='SSPI';"</codeFeaturedElement>

sSQL = "SELECT ProductID, ProductName, CategoryID, UnitPrice " &amp; _
             "FROM Products"

' Create and Open the Recordset object.
Set oRs = New ADODB.Recordset
oRs.CursorLocation = adUseClient
oRs.Open sSQL, <codeFeaturedElement xmlns="">sConn</codeFeaturedElement>, adOpenStatic, _
               adLockBatchOptimistic, adCmdText
                      
MsgBox oRs.RecordCount
        
oRs.MarshalOptions = adMarshalModifiedOnly
' Disconnect the Recordset.
Set oRs.ActiveConnection = Nothing
oRs.Close        
Set oRs = Nothing</code>
        <para>
          <caps:sentence sentenceid="65bbedc4961288dbf77a2c80cdffc0dd" id="tgt3" class="tgtSentence">Notice that <legacyBold>oRs.Open</legacyBold> takes a connection string (<legacyItalic>sConn</legacyItalic>), in place of a <legacyBold>Connection</legacyBold> object (<legacyItalic>oConn</legacyItalic>), as the value of its <legacyBold>ActiveConnection</legacyBold> parameter.</caps:sentence>
          <caps:sentence sentenceid="a3f4c0b70e21bbfd2f53f30aaee17b1f" id="tgt4" class="tgtSentence"> Also the client-side cursor type is enforced by setting the <legacyBold>CursorLocation</legacyBold> property on the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="24fd8be87b8c45ec7278227ed83f66db" id="tgt5" class="tgtSentence"> Again, contrast this with the <legacyBold>HelloData</legacyBold> example.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Alternatively, you can use <legacyBold>Recordset.Open</legacyBold> to implicitly establish a connection and issue a command over that connection in a single operation.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For example, in Visual Basic:</caps:sentence>
        </para>
        <code>Dim oRs As ADODB.Recordset
Dim sConn As String
Dim sSQL as String

<codeFeaturedElement xmlns="">sConn = "Provider='SQLOLEDB';Data Source='MySqlServer';" &amp; _</codeFeaturedElement><codeFeaturedElement xmlns="">             "Initial Catalog='Northwind';Integrated Security='SSPI';"</codeFeaturedElement>

sSQL = "SELECT ProductID, ProductName, CategoryID, UnitPrice " &amp; _
             "FROM Products"

' Create and Open the Recordset object.
Set oRs = New ADODB.Recordset
oRs.CursorLocation = adUseClient
oRs.Open sSQL, <codeFeaturedElement xmlns="">sConn</codeFeaturedElement>, adOpenStatic, _
               adLockBatchOptimistic, adCmdText
                      
MsgBox oRs.RecordCount
        
oRs.MarshalOptions = adMarshalModifiedOnly
' Disconnect the Recordset.
Set oRs.ActiveConnection = Nothing
oRs.Close        
Set oRs = Nothing</code>
        <para>
          <caps:sentence id="src3" class="srcSentence">Notice that <legacyBold>oRs.Open</legacyBold> takes a connection string (<legacyItalic>sConn</legacyItalic>), in place of a <legacyBold>Connection</legacyBold> object (<legacyItalic>oConn</legacyItalic>), as the value of its <legacyBold>ActiveConnection</legacyBold> parameter.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Also the client-side cursor type is enforced by setting the <legacyBold>CursorLocation</legacyBold> property on the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Again, contrast this with the <legacyBold>HelloData</legacyBold> example.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Controlling Transactions (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 189240e8-3ffa-4024-81a9-c6cb5d17eee0
caps.latest.revision: 4
caps.handback.revision: 4
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
# Controlling Transactions (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8cb9cb00419ebbe082c0c4ec602b99ce" id="tgt1" class="tgtSentence">ADO supports transaction processing within a connection with the help of the <legacyBold>BeginTrans</legacyBold>, <legacyBold>CommitTrans</legacyBold>, and <legacyBold>RollbackTrans</legacyBold> methods on a <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="bc0d7a025a164efe042af3bf709f5dfc" id="tgt2" class="tgtSentence"> The general idea of implementing transaction processing in ADO is illustrated in the following simple code snippet.</caps:sentence>
        </para>
        <code>Const DS = "MySqlServer"
Const DB = "Northwind"
Const DP = "SQLOLEDB"

Dim oConn As ADODB.Connection
Dim oRs As ADODB.Recordset
Dim sConn As String

sConn = "Provider=" &amp; DP &amp; _
          ";Data Source=" &amp; DS &amp; _
          ";Initial Catalog=" &amp; DB &amp; _
          ";Integrated Security=SSPI;"

sSQL = "SELECT ProductID, ProductName FROM Products"

Set oConn = New ADODB.Connection
oConn.Open sConn

' Create and Open the Recordset object.
Set oRs = New ADODB.Recordset
oRs.Open sSQL, oConn, adOpenStatic, adLockOptimistic, adCmdText

If oRs.RecordCount &gt; 1 Then
    
        
    oRs.MoveFirst
    Id1 = oRs("ProductID")
    Name1 = oRs("ProductName")
    oRs.MoveNext
    Id2 = oRs("ProductID")
    Name2 = oRs("ProductName")

    q = "Switch ID's of " &amp; Name1 &amp; " and " &amp; Name2 &amp; "?"
    If MsgBox(q, vbYesNo) = vbYes Then
        oRs.MoveFirst
        oRs("ProductName") = Name2
        oRs.Update
        
        oRs.MoveNext
        oRs("ProductName") = Name1
        oRs.Update
    
        If MsgBox("Save changes?", vbYesNo) = vbYes Then
            
        Else
            
        End If
    End If
    
End If
        
     
oRs.Close
oConn.Close</code>
        <para>
          <caps:sentence sentenceid="8e739d9beef557bf34a5f8ad0ec3370b" id="tgt3" class="tgtSentence">Here transaction processing is used to ensure that the two records are updated as one unit of operation, and that the two product names are either interchanged or not changed at all.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f863f073bda79250148d67958f37b72b" id="tgt4" class="tgtSentence">For detailed discussions of transaction processing see <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO supports transaction processing within a connection with the help of the <legacyBold>BeginTrans</legacyBold>, <legacyBold>CommitTrans</legacyBold>, and <legacyBold>RollbackTrans</legacyBold> methods on a <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The general idea of implementing transaction processing in ADO is illustrated in the following simple code snippet.</caps:sentence>
        </para>
        <code>Const DS = "MySqlServer"
Const DB = "Northwind"
Const DP = "SQLOLEDB"

Dim oConn As ADODB.Connection
Dim oRs As ADODB.Recordset
Dim sConn As String

sConn = "Provider=" &amp; DP &amp; _
          ";Data Source=" &amp; DS &amp; _
          ";Initial Catalog=" &amp; DB &amp; _
          ";Integrated Security=SSPI;"

sSQL = "SELECT ProductID, ProductName FROM Products"

Set oConn = New ADODB.Connection
oConn.Open sConn

' Create and Open the Recordset object.
Set oRs = New ADODB.Recordset
oRs.Open sSQL, oConn, adOpenStatic, adLockOptimistic, adCmdText

If oRs.RecordCount &gt; 1 Then
    
        
    oRs.MoveFirst
    Id1 = oRs("ProductID")
    Name1 = oRs("ProductName")
    oRs.MoveNext
    Id2 = oRs("ProductID")
    Name2 = oRs("ProductName")

    q = "Switch ID's of " &amp; Name1 &amp; " and " &amp; Name2 &amp; "?"
    If MsgBox(q, vbYesNo) = vbYes Then
        oRs.MoveFirst
        oRs("ProductName") = Name2
        oRs.Update
        
        oRs.MoveNext
        oRs("ProductName") = Name1
        oRs.Update
    
        If MsgBox("Save changes?", vbYesNo) = vbYes Then
            
        Else
            
        End If
    End If
    
End If
        
     
oRs.Close
oConn.Close</code>
        <para>
          <caps:sentence id="src3" class="srcSentence">Here transaction processing is used to ensure that the two records are updated as one unit of operation, and that the two product names are either interchanged or not changed at all.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">For detailed discussions of transaction processing see <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
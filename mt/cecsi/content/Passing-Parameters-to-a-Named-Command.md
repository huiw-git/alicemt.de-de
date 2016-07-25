---
title: "Passing Parameters to a Named Command"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 36e0cdbe-7f50-40f5-af0d-700f5d8dc75a
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
# Passing Parameters to a Named Command
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="126d0656e8b720d18389731ae2c417da" id="tgt1" class="tgtSentence">Just as the result of the command is passed out as an <legacyItalic>out</legacyItalic> variable of the named command, parameters for a parameterized command can been passed in as <legacyItalic>in</legacyItalic> variables to the named command.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="697587211ae0517f41f555f81cbb8fcb" id="tgt2" class="tgtSentence">The following code example tries to retrieve all the orders placed by the customer whose <legacyBold>CustomerID</legacyBold> is "ALKFI" from the Northwind database.</caps:sentence>
          <caps:sentence sentenceid="35112d4df39b1dd3f74e049d0a62b4ff" id="tgt3" class="tgtSentence"> The value of <legacyBold>CustomerID</legacyBold> is supplied at the time when the named command is called.</caps:sentence>
        </para>
        <code>    Const DS = "MySqlServer"
    Const DB = "Northwind"
    Const DP = "SQLOLEDB"
        
    Dim objConn As New ADODB.Connection
    Dim objRs As New ADODB.Recordset
    Dim objComm As New ADODB.Command
    
    CommandText = "SELECT OrderID, OrderDate, " &amp; _
                         "RequiredDate, ShippedDate " &amp; _
                         "FROM Orders " &amp; _
                         "WHERE <codeFeaturedElement xmlns="">CustomerID = ?</codeFeaturedElement> " &amp; _
                         "ORDER BY OrderID"

    ConnectionString = "Provider=" &amp; DP &amp; _
                       ";Data Source=" &amp; DS &amp; _
                       ";Initial Catalog=" &amp; DB &amp; _
                       ";Integrated Security=SSPI;"
    
    ' Connect to the data source.
    objConn.Open ConnectionString
    
    ' Set a named command.
    objComm.CommandText = CommandText
    objComm.CommandType = adCmdText
    objComm.Name = "GetOrdersOf"
    Set objComm.ActiveConnection = objConn

    ' Call the named command, passing a CustomerID value
    ' as the input parameter. 
    '    "ALFKI" is the required input parameter,
    '    objRs is the resultant output variable.
    objConn.GetOrdersOf <codeFeaturedElement xmlns="">"ALKFI"</codeFeaturedElement>, objRs
    
    ' Display the result.
    Debug.Print "All orders by ALFKI:"
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
    
    ' Clean up.
    objRs.Close
    objConn.Close
    Set objRs = Nothing
    Set objConn = Nothing
    Set objComm = Nothing</code>
        <para>
          <caps:sentence sentenceid="921ed35838a9e7fe658d57d890846213" id="tgt4" class="tgtSentence">Notice that all the input parameters must precede any output variable and the data types of parameters must match or can be converted to those of the corresponding fields.</caps:sentence>
          <caps:sentence sentenceid="2bd0b6447212808f75bdce29ddd69b22" id="tgt5" class="tgtSentence"> The following statement—</caps:sentence>
        </para>
        <code>objConn.GetOrdersOf 12345, objRs</code>
        <para>
          <caps:sentence sentenceid="ca84fb2e62c431412144c51c0f7863e5" id="tgt6" class="tgtSentence">—will result in an error of mismatched data types, because the required input parameter is of a <legacyBold>String</legacyBold> type, not of an <legacyBold>Integer</legacyBold> type.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b028c178bede67d1057b47b2e55ac2ad" id="tgt7" class="tgtSentence">The following call—</caps:sentence>
        </para>
        <code>objConn.GetOrdersOf "12345", objRs</code>
        <para>
          <caps:sentence sentenceid="93dc035647287b34d95f958c2668fc7b" id="tgt8" class="tgtSentence">—is valid, but will yield an empty result set because no such records exist in the database.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Just as the result of the command is passed out as an <legacyItalic>out</legacyItalic> variable of the named command, parameters for a parameterized command can been passed in as <legacyItalic>in</legacyItalic> variables to the named command.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">The following code example tries to retrieve all the orders placed by the customer whose <legacyBold>CustomerID</legacyBold> is "ALKFI" from the Northwind database.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The value of <legacyBold>CustomerID</legacyBold> is supplied at the time when the named command is called.</caps:sentence>
        </para>
        <code>    Const DS = "MySqlServer"
    Const DB = "Northwind"
    Const DP = "SQLOLEDB"
        
    Dim objConn As New ADODB.Connection
    Dim objRs As New ADODB.Recordset
    Dim objComm As New ADODB.Command
    
    CommandText = "SELECT OrderID, OrderDate, " &amp; _
                         "RequiredDate, ShippedDate " &amp; _
                         "FROM Orders " &amp; _
                         "WHERE <codeFeaturedElement xmlns="">CustomerID = ?</codeFeaturedElement> " &amp; _
                         "ORDER BY OrderID"

    ConnectionString = "Provider=" &amp; DP &amp; _
                       ";Data Source=" &amp; DS &amp; _
                       ";Initial Catalog=" &amp; DB &amp; _
                       ";Integrated Security=SSPI;"
    
    ' Connect to the data source.
    objConn.Open ConnectionString
    
    ' Set a named command.
    objComm.CommandText = CommandText
    objComm.CommandType = adCmdText
    objComm.Name = "GetOrdersOf"
    Set objComm.ActiveConnection = objConn

    ' Call the named command, passing a CustomerID value
    ' as the input parameter. 
    '    "ALFKI" is the required input parameter,
    '    objRs is the resultant output variable.
    objConn.GetOrdersOf <codeFeaturedElement xmlns="">"ALKFI"</codeFeaturedElement>, objRs
    
    ' Display the result.
    Debug.Print "All orders by ALFKI:"
    Do While Not objRs.EOF
        Debug.Print vbTab &amp; objRs(0) &amp; vbTab &amp; objRs(1) &amp; vbTab &amp; _
                    objRs(2) &amp; vbTab &amp; objRs(3)
        objRs.MoveNext
    Loop
    
    ' Clean up.
    objRs.Close
    objConn.Close
    Set objRs = Nothing
    Set objConn = Nothing
    Set objComm = Nothing</code>
        <para>
          <caps:sentence id="src4" class="srcSentence">Notice that all the input parameters must precede any output variable and the data types of parameters must match or can be converted to those of the corresponding fields.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> The following statement—</caps:sentence>
        </para>
        <code>objConn.GetOrdersOf 12345, objRs</code>
        <para>
          <caps:sentence id="src6" class="srcSentence">—will result in an error of mismatched data types, because the required input parameter is of a <legacyBold>String</legacyBold> type, not of an <legacyBold>Integer</legacyBold> type.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">The following call—</caps:sentence>
        </para>
        <code>objConn.GetOrdersOf "12345", objRs</code>
        <para>
          <caps:sentence id="src8" class="srcSentence">—is valid, but will yield an empty result set because no such records exist in the database.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
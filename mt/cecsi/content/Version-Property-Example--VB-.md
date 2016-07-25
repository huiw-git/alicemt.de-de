---
title: "Version Property Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 708efd50-2905-4168-b7e4-91b2e9b23539
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
# Version Property Example (VB)
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
              <caps:sentence sentenceid="8e354dca51c140654d6031602ee8a57b" id="tgt3" class="tgtSentence">the current DBMS name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4389a8dcc21edbbd402929cc385c7049" id="tgt4" class="tgtSentence">OLE DB version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9616554afe176ae4b2c8613a737f2997" id="tgt5" class="tgtSentence">             provider name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b8d5a99c50f14256031b7a67f185d246" id="tgt6" class="tgtSentence">             ODBC version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5f195e9ab22407f8348677bb30de766f" id="tgt7" class="tgtSentence">ODBC driver name and version.</caps:sentence>
            </para>
          </listItem>
        </list>
        <code>'BeginVersionVB
Public Sub Main()
    On Error GoTo ErrorHandler

    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
    Dim strVersionInfo As String
    
    ' Open connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
    
    strVersionInfo = "ADO Version: " &amp; Cnxn.Version &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "DBMS Name: " &amp; Cnxn.Properties("DBMS Name") &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "DBMS Version: " &amp; Cnxn.Properties("DBMS Version") &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "OLE DB Version: " &amp; Cnxn.Properties("OLE DB Version") &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "Provider Name: " &amp; Cnxn.Properties("Provider Name") &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "Provider Version: " &amp; Cnxn.Properties("Provider Version") &amp; vbCr
    
    MsgBox strVersionInfo

    ' clean up
    Cnxn.Close
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndVersionVB</code>
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
              <caps:sentence id="src3" class="srcSentence">the current DBMS name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">OLE DB version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             provider name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             ODBC version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">ODBC driver name and version.</caps:sentence>
            </para>
          </listItem>
        </list>
        <code>'BeginVersionVB
Public Sub Main()
    On Error GoTo ErrorHandler

    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
    Dim strVersionInfo As String
    
    ' Open connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
    
    strVersionInfo = "ADO Version: " &amp; Cnxn.Version &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "DBMS Name: " &amp; Cnxn.Properties("DBMS Name") &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "DBMS Version: " &amp; Cnxn.Properties("DBMS Version") &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "OLE DB Version: " &amp; Cnxn.Properties("OLE DB Version") &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "Provider Name: " &amp; Cnxn.Properties("Provider Name") &amp; vbCr
    strVersionInfo = strVersionInfo &amp; "Provider Version: " &amp; Cnxn.Properties("Provider Version") &amp; vbCr
    
    MsgBox strVersionInfo

    ' clean up
    Cnxn.Close
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    ' clean up
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndVersionVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
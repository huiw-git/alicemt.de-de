---
title: "Save and Open Methods Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ddccdf58-9c57-4c9b-8b7f-0cf193f955fb
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
# Save and Open Methods Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="56c9f1a3f78976a236b9a7ab1310c050" id="tgt1" class="tgtSentence">These three examples demonstrate how the <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> and <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> methods can be used together.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a7cad7fc2862eb1a6a79a9a2f78cfdbb" id="tgt2" class="tgtSentence">Assume that you are going on a business trip and want to take along a table from a database.</caps:sentence>
          <caps:sentence sentenceid="8054f8bd1920e9ce7ceb1e89d7377432" id="tgt3" class="tgtSentence"> Before you go, you access the data as a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> and save it in a transportable form.</caps:sentence>
          <caps:sentence sentenceid="f41452cfb169839ec79b311153fa986f" id="tgt4" class="tgtSentence"> When you arrive at your destination, you access the <legacyBold>Recordset</legacyBold> as a local, disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="4f96a7876f1f921edbe6d43f5f503610" id="tgt5" class="tgtSentence"> You make changes to the <legacyBold>Recordset</legacyBold>, and then save it again.</caps:sentence>
          <caps:sentence sentenceid="5246b8ffedd82fe70f31966fc3d5a404" id="tgt6" class="tgtSentence"> Finally, when you return home, you connect to the database again and update it with the changes you made on the road.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a3e31d7288b92adb8248252885944f04" id="tgt7" class="tgtSentence">First, access and save the <legacyBold><legacyItalic>Authors</legacyItalic></legacyBold> table.</caps:sentence>
        </para>
        <code>'BeginSaveVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string
    
Public Sub Main()
    On Error GoTo ErrorHandler

    'recordset and connection variables
    Dim rstAuthors As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
    Dim strSQLAuthors As String
     
    ' Open connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
    
    Set rstAuthors = New ADODB.Recordset
    strSQLAuthors = "SELECT au_id, au_lname, au_fname, city, phone FROM Authors"
    rstAuthors.Open strSQLAuthors, Cnxn, adOpenDynamic, adLockOptimistic, adCmdText
     
    'For sake of illustration, save the Recordset to a diskette in XML format
    rstAuthors.Save "c:\Pubs.xml", adPersistXML

    ' clean up
    rstAuthors.Close
    Cnxn.Close
    Set rstAuthors = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    'clean up
    If Not rstAuthors Is Nothing Then
        If rstAuthors.State = adStateOpen Then rstAuthors.Close
    End If
    Set rstAuthors = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndSaveVB</code>
        <para>
          <caps:sentence sentenceid="b15a673c96382fd96a0f64e0d6249575" id="tgt8" class="tgtSentence">At this point, you have arrived at your destination.</caps:sentence>
          <caps:sentence sentenceid="9d356d043844b326d416c44c7b697b55" id="tgt9" class="tgtSentence"> You will access the <legacyBold><legacyItalic>Authors</legacyItalic></legacyBold> table as a local, disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="bdec08d48439f50d501faff9570619a4" id="tgt10" class="tgtSentence"> You must have the <legacyBold>MSPersist</legacyBold> provider on the computer that you are using to access the saved file, a:\Pubs.xml.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "Save"</code>
        <para>
          <caps:sentence sentenceid="d75bb8a30347cb887f5fb10af27acedc" id="tgt11" class="tgtSentence">Finally, you return home.</caps:sentence>
          <caps:sentence sentenceid="f122a0b1bf58e7d4bc424b7fd9be09d5" id="tgt12" class="tgtSentence"> Now update the database with your changes.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "Save"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="a9b287f5-04b0-4514-8143-f67879ca9842">Recordset Persistence</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">These three examples demonstrate how the <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> and <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> methods can be used together.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Assume that you are going on a business trip and want to take along a table from a database.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Before you go, you access the data as a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> and save it in a transportable form.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> When you arrive at your destination, you access the <legacyBold>Recordset</legacyBold> as a local, disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> You make changes to the <legacyBold>Recordset</legacyBold>, and then save it again.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Finally, when you return home, you connect to the database again and update it with the changes you made on the road.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">First, access and save the <legacyBold><legacyItalic>Authors</legacyItalic></legacyBold> table.</caps:sentence>
        </para>
        <code>'BeginSaveVB

    'To integrate this code
    'replace the data source and initial catalog values
    'in the connection string
    
Public Sub Main()
    On Error GoTo ErrorHandler

    'recordset and connection variables
    Dim rstAuthors As ADODB.Recordset
    Dim Cnxn As ADODB.Connection
    Dim strCnxn As String
    Dim strSQLAuthors As String
     
    ' Open connection
    Set Cnxn = New ADODB.Connection
    strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" &amp; _
        "Initial Catalog='Pubs';Integrated Security='SSPI';"
    Cnxn.Open strCnxn
    
    Set rstAuthors = New ADODB.Recordset
    strSQLAuthors = "SELECT au_id, au_lname, au_fname, city, phone FROM Authors"
    rstAuthors.Open strSQLAuthors, Cnxn, adOpenDynamic, adLockOptimistic, adCmdText
     
    'For sake of illustration, save the Recordset to a diskette in XML format
    rstAuthors.Save "c:\Pubs.xml", adPersistXML

    ' clean up
    rstAuthors.Close
    Cnxn.Close
    Set rstAuthors = Nothing
    Set Cnxn = Nothing
    Exit Sub
    
ErrorHandler:
    'clean up
    If Not rstAuthors Is Nothing Then
        If rstAuthors.State = adStateOpen Then rstAuthors.Close
    End If
    Set rstAuthors = Nothing
    
    If Not Cnxn Is Nothing Then
        If Cnxn.State = adStateOpen Then Cnxn.Close
    End If
    Set Cnxn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
'EndSaveVB</code>
        <para>
          <caps:sentence id="src8" class="srcSentence">At this point, you have arrived at your destination.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> You will access the <legacyBold><legacyItalic>Authors</legacyItalic></legacyBold> table as a local, disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> You must have the <legacyBold>MSPersist</legacyBold> provider on the computer that you are using to access the saved file, a:\Pubs.xml.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "Save"</code>
        <para>
          <caps:sentence id="src11" class="srcSentence">Finally, you return home.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Now update the database with your changes.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "Save"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="a9b287f5-04b0-4514-8143-f67879ca9842">Recordset Persistence</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Status Property Example (Field) (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fdd09b60-39c7-44be-8008-e891a031f80e
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
# Status Property Example (Field) (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5f94f4f537eeab04a2d8118491aa1636" id="tgt1" class="tgtSentence">The following example opens a document from a read/write folder using the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Internet Publishing Provider</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="2e5af6ca403a6ae32e5f8d11067370ae" id="tgt2" class="tgtSentence"> The <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status</legacyLink> property of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object of the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> will first be set to <legacyBold>adFieldPendingInsert</legacyBold>, then be updated to <legacyBold>adFieldOk</legacyBold>.</caps:sentence>
        </para>
        <code>'BeginStatusFieldVB
    
 ' to integrate this code replace the values in the source string

Sub Main()
    
   Dim File As ADODB.Record
   Dim strFile As String
   Dim Cnxn As ADODB.Connection
   Dim strCnxn As String
   
   Set Cnxn = New ADODB.Connection
   strCnxn = "url=http://MyServer/"
   Cnxn.Open strCnxn
   
   Set File = New ADODB.Record
   strFile = "Folder/FileName"
   ' Open a read/write document
   File.Source = strFile
   File.ActiveConnection = Cnxn
   File.Mode = adModeReadWrite
   File.Open

   Debug.Print "Append a couple of fields"
   
   File.Fields.Append "chektest:fld1", adWChar, 42, adFldUpdatable, "fld1"
   File.Fields.Append "chektest:fld2", adWChar, 42, adFldUpdatable, "fld2"
   
   Debug.Print "status for the fields"
   Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert
   Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert
   
    'turn off error-handling to verify field status
   On Error Resume Next
   
   File.Fields.Update
   
   Debug.Print "Update succeeds"
   Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert + adFieldUnavailable
   Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert + adFieldUnavailable
    
    ' resume default error-handling
   On Error GoTo 0
     
     ' clean up
    File.Close
    Cnxn.Close
    Set File = Nothing
    Set Cnxn = Nothing
      
End Sub
'EndStatusFieldVB</code>
        <para>
          <caps:sentence sentenceid="99436db6aacde239175e02224d75701f" id="tgt3" class="tgtSentence">The following example deletes a known <legacyBold>Field</legacyBold> from a <legacyBold>Record</legacyBold> opened from a document.</caps:sentence>
          <caps:sentence sentenceid="e9d9cf48c1ad7887258fceb1cfdd75fe" id="tgt4" class="tgtSentence"> The <legacyBold>Status</legacyBold> property will first be set to <legacyBold>adFieldOK</legacyBold>, then <legacyBold>adFieldPendingUnknown</legacyBold>.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "StatusField"</code>
        <para>
          <caps:sentence sentenceid="a0b67b15e5b24f3bd4ccbcdbe2032ed0" id="tgt5" class="tgtSentence">The following code deletes a <legacyBold>Field</legacyBold> from a <legacyBold>Record</legacyBold> opened on a read-only document.</caps:sentence>
          <caps:sentence sentenceid="24487b5e9dce8510e250fd54e6c30a32" id="tgt6" class="tgtSentence">
            <legacyBold>Status</legacyBold> will be set to <legacyBold>adFieldPendingDelete</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="48e0e263b15de1a71857646936072f09" id="tgt7" class="tgtSentence"> At <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>, the delete will fail and <legacyBold>Status</legacyBold> will be <legacyBold>adFieldPendingDelete</legacyBold> plus <legacyBold>adFieldPermissionDenied</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="eabbf1df29a55adb29577b06e89cb75c" id="tgt8" class="tgtSentence">
            <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> clears the pending <legacyBold>Status</legacyBold> setting.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "StatusField"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status Property (ADO Field)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following example opens a document from a read/write folder using the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Internet Publishing Provider</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status</legacyLink> property of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object of the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> will first be set to <legacyBold>adFieldPendingInsert</legacyBold>, then be updated to <legacyBold>adFieldOk</legacyBold>.</caps:sentence>
        </para>
        <code>'BeginStatusFieldVB
    
 ' to integrate this code replace the values in the source string

Sub Main()
    
   Dim File As ADODB.Record
   Dim strFile As String
   Dim Cnxn As ADODB.Connection
   Dim strCnxn As String
   
   Set Cnxn = New ADODB.Connection
   strCnxn = "url=http://MyServer/"
   Cnxn.Open strCnxn
   
   Set File = New ADODB.Record
   strFile = "Folder/FileName"
   ' Open a read/write document
   File.Source = strFile
   File.ActiveConnection = Cnxn
   File.Mode = adModeReadWrite
   File.Open

   Debug.Print "Append a couple of fields"
   
   File.Fields.Append "chektest:fld1", adWChar, 42, adFldUpdatable, "fld1"
   File.Fields.Append "chektest:fld2", adWChar, 42, adFldUpdatable, "fld2"
   
   Debug.Print "status for the fields"
   Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert
   Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert
   
    'turn off error-handling to verify field status
   On Error Resume Next
   
   File.Fields.Update
   
   Debug.Print "Update succeeds"
   Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert + adFieldUnavailable
   Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert + adFieldUnavailable
    
    ' resume default error-handling
   On Error GoTo 0
     
     ' clean up
    File.Close
    Cnxn.Close
    Set File = Nothing
    Set Cnxn = Nothing
      
End Sub
'EndStatusFieldVB</code>
        <para>
          <caps:sentence id="src3" class="srcSentence">The following example deletes a known <legacyBold>Field</legacyBold> from a <legacyBold>Record</legacyBold> opened from a document.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The <legacyBold>Status</legacyBold> property will first be set to <legacyBold>adFieldOK</legacyBold>, then <legacyBold>adFieldPendingUnknown</legacyBold>.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "StatusField"</code>
        <para>
          <caps:sentence id="src5" class="srcSentence">The following code deletes a <legacyBold>Field</legacyBold> from a <legacyBold>Record</legacyBold> opened on a read-only document.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence">
            <legacyBold>Status</legacyBold> will be set to <legacyBold>adFieldPendingDelete</legacyBold>.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> At <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>, the delete will fail and <legacyBold>Status</legacyBold> will be <legacyBold>adFieldPendingDelete</legacyBold> plus <legacyBold>adFieldPermissionDenied</legacyBold>.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence">
            <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> clears the pending <legacyBold>Status</legacyBold> setting.</caps:sentence>
        </para>
        <code>Attribute VB_Name = "StatusField"</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status Property (ADO Field)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
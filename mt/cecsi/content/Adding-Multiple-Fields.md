---
title: "Adding Multiple Fields"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f3648ef4-9f36-4991-a868-83a617389844
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
# Adding Multiple Fields
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1cffbd6c0d92b5f616e5c3446867b588" id="tgt1" class="tgtSentence">Occasionally, it might be more efficient to pass in an array of fields and their corresponding values to the <legacyBold>AddNew</legacyBold> method, rather than setting <legacyBold>Value</legacyBold> multiple times for each new field.</caps:sentence>
          <caps:sentence sentenceid="e8e60a1a1121a4f2e08ccfb088ff470e" id="tgt2" class="tgtSentence"> If <legacyItalic>FieldList </legacyItalic>is an array, <legacyItalic>Values</legacyItalic> must also be an array with the same number of members; otherwise, an error occurs.</caps:sentence>
          <caps:sentence sentenceid="6d5f7dfe42c46001bb44fec1d817d720" id="tgt3" class="tgtSentence"> The order of field names must match the order of field values in each array.</caps:sentence>
          <caps:sentence sentenceid="4251937bb84117fc48e4117b12af2fc2" id="tgt4" class="tgtSentence"> The following code passes an array of fields and an array of values to the <legacyBold>AddNew</legacyBold> method.</caps:sentence>
        </para>
        <code>'BeginAddNew2
    Dim avarFldNames As Variant
    Dim avarFldValues As Variant
        
    avarFldNames = Array("CompanyName", "Phone")
    avarFldValues = Array("Sample Shipper 2", "(931) 555-6334")
    
    If objRs1.Supports(adAddNew) Then
        objRs1.AddNew avarFldNames, avarFldValues
    End If
    
    'Re-establish a Connection and update
    Set objRs1.ActiveConnection = GetNewConnection
    objRs1.UpdateBatch
'EndAddNew2</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Occasionally, it might be more efficient to pass in an array of fields and their corresponding values to the <legacyBold>AddNew</legacyBold> method, rather than setting <legacyBold>Value</legacyBold> multiple times for each new field.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> If <legacyItalic>FieldList </legacyItalic>is an array, <legacyItalic>Values</legacyItalic> must also be an array with the same number of members; otherwise, an error occurs.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The order of field names must match the order of field values in each array.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The following code passes an array of fields and an array of values to the <legacyBold>AddNew</legacyBold> method.</caps:sentence>
        </para>
        <code>'BeginAddNew2
    Dim avarFldNames As Variant
    Dim avarFldValues As Variant
        
    avarFldNames = Array("CompanyName", "Phone")
    avarFldValues = Array("Sample Shipper 2", "(931) 555-6334")
    
    If objRs1.Supports(adAddNew) Then
        objRs1.AddNew avarFldNames, avarFldValues
    End If
    
    'Re-establish a Connection and update
    Set objRs1.ActiveConnection = GetNewConnection
    objRs1.UpdateBatch
'EndAddNew2</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
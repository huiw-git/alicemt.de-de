---
title: "Step 3: Populate the Fields List Box"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 315c32dc-aeb1-4629-b30e-87b44e8f84d1
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
# Step 3: Populate the Fields List Box
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="04302538d49500190460701bb0d393eb" id="tgt1" class="tgtSentence">To populate the Fields list box, insert the following code into the Click event handler of <codeInline>lstMain</codeInline>:</caps:sentence>
        </para>
        <code>Private Sub lstMain_Click()
    Dim rec As Record
    Dim rs As Recordset
    Set rec = New Record
    Set rs = New Recordset
    grs.MoveFirst
    grs.Move lstMain.ListIndex
    lstDetails.Clear
    rec.Open grs
    Select Case rec.RecordType
        Case adCollectionRecord:
            Set rs = rec.GetChildren
            While Not rs.EOF
                lstDetails.AddItem rs(0)
                rs.MoveNext
            Wend
        Case adSimpleRecord:
            recFields rec, lstDetails, txtDetails
            
        Case adStructDoc:
    End Select
    
End Sub</code>
        <para>
          <caps:sentence sentenceid="1e9133400a6550c7b8577c6e149e976f" id="tgt2" class="tgtSentence">This code declares and instantiates local Record and Recordset objects, <codeInline>rec</codeInline> and <codeInline>rs</codeInline>, respectively.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="46a5d1bb792adf0d64e2db08ddf12b41" id="tgt3" class="tgtSentence">The row corresponding to the resource selected in <codeInline>lstMain</codeInline> is made the current row of <codeInline>grs</codeInline>.</caps:sentence>
          <caps:sentence sentenceid="901123702e785fc9c78e5f42f89dd647" id="tgt4" class="tgtSentence"> Then the Details list box is cleared and <codeInline>rec</codeInline> is opened with the current row of <codeInline>grs</codeInline> as the source.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="25597877518f525a951ba2f41829e6b8" id="tgt5" class="tgtSentence">If the resource is a collection record, as specified by <legacyLink xlink:href="790e46a2-13d2-451e-a8be-130bd9a206a4">RecordType</legacyLink>, the local Recordset <codeInline>rs</codeInline> is opened on the children of rec.</caps:sentence>
          <caps:sentence sentenceid="7438012371568d442744c0a42fa37339" id="tgt6" class="tgtSentence"> Then <codeInline>lstDetails</codeInline> is filled with the values from the rows of <codeInline>rs</codeInline>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3737781e190eacf2a8ab9036e64bb613" id="tgt7" class="tgtSentence">If the resource is a simple record, <codeInline>recFields</codeInline> is called.</caps:sentence>
          <caps:sentence sentenceid="7a8a3aaa60fd0d87f8af3cb6f570cabd" id="tgt8" class="tgtSentence"> For more information about <codeInline>recFields</codeInline>, see the next step.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="be41b8f7dc5be937145e9a320a19ae87" id="tgt9" class="tgtSentence">No code is implemented if the resource is a structured document.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</link>
        <link xlink:href="a1454493-1c86-46c2-ada8-d3c6fcdaf3c1">Step 2: Initialize the Main List Box</link>
        <link xlink:href="cb4273e2-c907-4a86-a621-3bf110088228">Step 4: Populate the Details Text Box</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To populate the Fields list box, insert the following code into the Click event handler of <codeInline>lstMain</codeInline>:</caps:sentence>
        </para>
        <code>Private Sub lstMain_Click()
    Dim rec As Record
    Dim rs As Recordset
    Set rec = New Record
    Set rs = New Recordset
    grs.MoveFirst
    grs.Move lstMain.ListIndex
    lstDetails.Clear
    rec.Open grs
    Select Case rec.RecordType
        Case adCollectionRecord:
            Set rs = rec.GetChildren
            While Not rs.EOF
                lstDetails.AddItem rs(0)
                rs.MoveNext
            Wend
        Case adSimpleRecord:
            recFields rec, lstDetails, txtDetails
            
        Case adStructDoc:
    End Select
    
End Sub</code>
        <para>
          <caps:sentence id="src2" class="srcSentence">This code declares and instantiates local Record and Recordset objects, <codeInline>rec</codeInline> and <codeInline>rs</codeInline>, respectively.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">The row corresponding to the resource selected in <codeInline>lstMain</codeInline> is made the current row of <codeInline>grs</codeInline>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Then the Details list box is cleared and <codeInline>rec</codeInline> is opened with the current row of <codeInline>grs</codeInline> as the source.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">If the resource is a collection record, as specified by <legacyLink xlink:href="790e46a2-13d2-451e-a8be-130bd9a206a4">RecordType</legacyLink>, the local Recordset <codeInline>rs</codeInline> is opened on the children of rec.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Then <codeInline>lstDetails</codeInline> is filled with the values from the rows of <codeInline>rs</codeInline>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">If the resource is a simple record, <codeInline>recFields</codeInline> is called.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> For more information about <codeInline>recFields</codeInline>, see the next step.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">No code is implemented if the resource is a structured document.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</link>
        <link xlink:href="a1454493-1c86-46c2-ada8-d3c6fcdaf3c1">Step 2: Initialize the Main List Box</link>
        <link xlink:href="cb4273e2-c907-4a86-a621-3bf110088228">Step 4: Populate the Details Text Box</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
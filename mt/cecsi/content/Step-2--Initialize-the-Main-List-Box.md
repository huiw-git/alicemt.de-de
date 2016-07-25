---
title: "Step 2: Initialize the Main List Box"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a1454493-1c86-46c2-ada8-d3c6fcdaf3c1
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
# Step 2: Initialize the Main List Box
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6f2a978264ff0912b8685af866511785" id="tgt1" class="tgtSentence">To declare global Record and Recordset objects, insert the following code into the (General) (Declarations) for Form1: </caps:sentence>
        </para>
        <code>Option Explicit
Dim grec As Record
Dim grs As Recordset</code>
        <para>
          <caps:sentence sentenceid="85809149228568792f1e3ad9cb6607b7" id="tgt2" class="tgtSentence">This code declares global object references for Record and Recordset objects that will be used later in this scenario.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="7db93605c162ce603ae84461c2206492" id="tgt3" class="tgtSentence">To connect to a URL and populate lstMain</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="747c2257afa0aebab558b39bd9b6f080" id="tgt4" class="tgtSentence">Insert the following code into the Form Load event handler for Form1: </caps:sentence>
          </para>
          <code>Private Sub Form_Load()
    Set grec = New Record
    Set grs = New Recordset
    grec.Open "", "URL=http://servername/foldername/", , _
        adOpenIfExists Or adCreateCollection
    Set grs = grec.GetChildren
    While Not grs.EOF
        lstMain.AddItem grs(0)
        grs.MoveNext
    Wend
End Sub</code>
          <para>
            <caps:sentence sentenceid="1eb129794b5d13b572a8ef2845635e2e" id="tgt5" class="tgtSentence">This code instantiates the global Record and Recordset objects.</caps:sentence>
            <caps:sentence sentenceid="888a8e92a24216c1ba8f8fabe00bd933" id="tgt6" class="tgtSentence"> The Record object, <codeInline>grec</codeInline>, is opened with a URL specified as the ActiveConnection.</caps:sentence>
            <caps:sentence sentenceid="f744419a4d0010ffb653abe1436246bf" id="tgt7" class="tgtSentence"> If the URL exists, it is opened; if it does not already exist, it is created.</caps:sentence>
            <caps:sentence sentenceid="6289a26f54b15055ab9fadc31f6401ec" id="tgt8" class="tgtSentence"> Note that you should replace "http://servername/foldername/" with a valid URL from your environment.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="99e10ef81d624b57fd1921ae1e625097" id="tgt9" class="tgtSentence">The Recordset object, <codeInline>grs</codeInline>, is opened on the children of the Record, <codeInline>grec</codeInline>.</caps:sentence>
            <caps:sentence sentenceid="8e4d110c03c90f96b3a4a7dac27c7c6e" id="tgt10" class="tgtSentence"> Then <codeInline>lstMain</codeInline> is populated with the file names of the resources published to the URL.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</link>
        <link xlink:href="77d3bfa5-fc9f-4a72-93b4-790c7d227988">Step 1: Set Up the Visual Basic Project</link>
        <link xlink:href="315c32dc-aeb1-4629-b30e-87b44e8f84d1">Step 3: Populate the Fields List Box</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To declare global Record and Recordset objects, insert the following code into the (General) (Declarations) for Form1: </caps:sentence>
        </para>
        <code>Option Explicit
Dim grec As Record
Dim grs As Recordset</code>
        <para>
          <caps:sentence id="src2" class="srcSentence">This code declares global object references for Record and Recordset objects that will be used later in this scenario.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">To connect to a URL and populate lstMain</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Insert the following code into the Form Load event handler for Form1: </caps:sentence>
          </para>
          <code>Private Sub Form_Load()
    Set grec = New Record
    Set grs = New Recordset
    grec.Open "", "URL=http://servername/foldername/", , _
        adOpenIfExists Or adCreateCollection
    Set grs = grec.GetChildren
    While Not grs.EOF
        lstMain.AddItem grs(0)
        grs.MoveNext
    Wend
End Sub</code>
          <para>
            <caps:sentence id="src5" class="srcSentence">This code instantiates the global Record and Recordset objects.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The Record object, <codeInline>grec</codeInline>, is opened with a URL specified as the ActiveConnection.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If the URL exists, it is opened; if it does not already exist, it is created.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Note that you should replace "http://servername/foldername/" with a valid URL from your environment.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The Recordset object, <codeInline>grs</codeInline>, is opened on the children of the Record, <codeInline>grec</codeInline>.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Then <codeInline>lstMain</codeInline> is populated with the file names of the resources published to the URL.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</link>
        <link xlink:href="77d3bfa5-fc9f-4a72-93b4-790c7d227988">Step 1: Set Up the Visual Basic Project</link>
        <link xlink:href="315c32dc-aeb1-4629-b30e-87b44e8f84d1">Step 3: Populate the Fields List Box</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
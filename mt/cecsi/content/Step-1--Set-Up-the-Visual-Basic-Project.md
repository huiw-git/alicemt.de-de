---
title: "Step 1: Set Up the Visual Basic Project"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77d3bfa5-fc9f-4a72-93b4-790c7d227988
caps.latest.revision: 5
caps.handback.revision: 5
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
# Step 1: Set Up the Visual Basic Project
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="70c1aa8c49520d215034d8f5825a5ae6" id="tgt1" class="tgtSentence">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</caps:sentence>
          <caps:sentence sentenceid="f2d9bf0b091500f0e8a20a4386f1641f" id="tgt2" class="tgtSentence"> You will first create a new project, and then add some controls to the default form in the project.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence sentenceid="c9b1c88ae4d45d2298bccc3f486a7094" id="tgt3" class="tgtSentence">To create an ADO project:</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="8b89eb4d90eb80c588670a23ce375612" id="tgt4" class="tgtSentence">In Microsoft Visual Basic, create a new Standard EXE project.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="a237b5415d4458bedc362a644834c747" id="tgt5" class="tgtSentence">From the Project menu, choose References.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="1584ddc226b07923e655a4dd18c98e9b" id="tgt6" class="tgtSentence">Select "Microsoft ActiveX Data Objects 2.5 Library" and click OK.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
        <procedure>
          <title>
            <caps:sentence sentenceid="62bbf4590652d42761e7bb43b5b8513b" id="tgt7" class="tgtSentence">To insert controls on the main form:</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="48988f636a61fd1e426b0996fdb8287c" id="tgt8" class="tgtSentence">Add a ListBox control to Form1.</caps:sentence>
                  <caps:sentence sentenceid="3371a76aa4eb30a5d48f7d5d872a4f1e" id="tgt9" class="tgtSentence"> Set its Name property to <userInputLocalizable>lstMain</userInputLocalizable>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="d17bb77d8a3d62869e56f71dab831293" id="tgt10" class="tgtSentence">Add another ListBox control to Form1.</caps:sentence>
                  <caps:sentence sentenceid="2b87aa8eb2f1eb1bb88d3b385ddb1e1b" id="tgt11" class="tgtSentence"> Set its Name property to <userInputLocalizable>lstDetails</userInputLocalizable>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="6f1b3f0c192d46dba9362bb74faadfa6" id="tgt12" class="tgtSentence">Add a TextBox control to Form1.</caps:sentence>
                  <caps:sentence sentenceid="e23f1bf4767ac61b64f07f1e46729a26" id="tgt13" class="tgtSentence"> Set its Name property to <userInputLocalizable>txtDetails</userInputLocalizable>.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <relatedTopics>
        <link xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</link>
        <link xlink:href="a1454493-1c86-46c2-ada8-d3c6fcdaf3c1">Step 2: Initialize the Main List Box</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You will first create a new project, and then add some controls to the default form in the project.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence id="src3" class="srcSentence">To create an ADO project:</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src4" class="srcSentence">In Microsoft Visual Basic, create a new Standard EXE project.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src5" class="srcSentence">From the Project menu, choose References.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Select "Microsoft ActiveX Data Objects 2.5 Library" and click OK.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
        <procedure>
          <title>
            <caps:sentence id="src7" class="srcSentence">To insert controls on the main form:</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Add a ListBox control to Form1.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> Set its Name property to <userInputLocalizable>lstMain</userInputLocalizable>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Add another ListBox control to Form1.</caps:sentence>
                  <caps:sentence id="src11" class="srcSentence"> Set its Name property to <userInputLocalizable>lstDetails</userInputLocalizable>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Add a TextBox control to Form1.</caps:sentence>
                  <caps:sentence id="src13" class="srcSentence"> Set its Name property to <userInputLocalizable>txtDetails</userInputLocalizable>.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <relatedTopics>
        <link xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</link>
        <link xlink:href="a1454493-1c86-46c2-ada8-d3c6fcdaf3c1">Step 2: Initialize the Main List Box</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
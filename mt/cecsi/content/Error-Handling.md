---
title: "Error Handling"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4909e413-f3b0-4183-8ad3-67b1434df742
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
# Error Handling
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="22b69954691f86c92a2f261470d1a40b" id="tgt1" class="tgtSentence">ADO uses several different methods to notify an application of errors that occur.</caps:sentence>
          <caps:sentence sentenceid="ca1061c1f36c328c23f4d96dea4ffa52" id="tgt2" class="tgtSentence"> This section discusses the types of errors that can occur when you are using ADO and how your application is notified.</caps:sentence>
          <caps:sentence sentenceid="3de6fe526e6c8e0a1f19f057982b71e2" id="tgt3" class="tgtSentence"> It concludes by making suggestions about how to handle those errors.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a9246ffd2e6122fa308abfe8f5f0c713" id="tgt4" class="tgtSentence">How Does ADO Report Errors?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5d6a7082a8e4804793affea4d8104e91" id="tgt5" class="tgtSentence">ADO notifies you about errors in several ways:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="2ee3ff0a854625b4f5835bc77c2040e0" id="tgt6" class="tgtSentence">ADO errors generate a run-time error.</caps:sentence>
                <caps:sentence sentenceid="74fddd6165957a3a222664c307ebee4c" id="tgt7" class="tgtSentence"> Handle an ADO error the same way you would any other run-time error, such as using an <legacyBold>On Error</legacyBold> statement in Visual Basic.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="304944385244a99dc871bd04b224d4e3" id="tgt8" class="tgtSentence">Your program can receive errors from OLE DB.</caps:sentence>
                <caps:sentence sentenceid="addebbd2683ee20ba62049b0690d12f9" id="tgt9" class="tgtSentence"> An OLE DB error generates a run-time error as well.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ba7ef6a47484114abf707438da482d76" id="tgt10" class="tgtSentence">If the error is specific to your data provider, one or more <legacyBold>Error</legacyBold> objects are placed in the <legacyBold>Errors</legacyBold> collection of the <legacyBold>Connection</legacyBold> object that was used to access the data store when the error occurred.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e7a4a5c24464d57e0c5ca2dfbbede5cd" id="tgt11" class="tgtSentence">If the process that raised an event also produced an error, error information is placed in an <legacyBold>Error</legacyBold> object and passed as a parameter to the event.</caps:sentence>
                <caps:sentence sentenceid="54c7e7f713fb6d9350c3e735434f4d9e" id="tgt12" class="tgtSentence"> See <legacyLink xlink:href="e9003457-0762-48b3-942f-0820266b158f">Handling ADO Events</legacyLink> for more information about events.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dcc6b84d50c8acf11c76c8ed85fb260f" id="tgt13" class="tgtSentence">Problems that occur when processing batch updates or other bulk operations involving a <legacyBold>Recordset</legacyBold> can be indicated by the <legacyBold>Status</legacyBold> property of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="d130d38a783aeb1f734f43b5a3f7ac60" id="tgt14" class="tgtSentence"> For example, schema constraint violations or insufficient permissions can be specified by <legacyBold>RecordStatusEnum</legacyBold> values.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ef28c2c280d79334573835237e6efd86" id="tgt15" class="tgtSentence">Problems that occur involving a particular <legacyBold>Field</legacyBold> in the current record are also indicated by the <legacyBold>Status</legacyBold> property of each <legacyBold>Field</legacyBold> in the <legacyBold>Fields</legacyBold> collection of the <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="e8ead6a4ad7f4a12ce92ba6139c73a0d" id="tgt16" class="tgtSentence"> For example, updates that could not be completed or incompatible data types can be specified by <legacyBold>FieldStatusEnum</legacyBold> values.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt17" class="tgtSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="cfcb1cb024ac94faf5a1ebfc6db08a2e" id="tgt18" class="tgtSentence">             <legacyLink xlink:href="9bb84114-a1df-4122-a1b8-ad98dcd85cc3">ADO Errors</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e74da7835d5a73eda17dbdb19189f6ca" id="tgt19" class="tgtSentence">             <legacyLink xlink:href="cc7d6ff9-2034-45c6-9d61-90b177010054">Provider Errors</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ad0fbafc3f189d150d7b244416674b1f" id="tgt20" class="tgtSentence">             <legacyLink xlink:href="5e7b1af4-996b-47c5-9161-c5575ad4fec9">Field-Related Error Information</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7add6610482d0b7302861f60d63d23d4" id="tgt21" class="tgtSentence">             <legacyLink xlink:href="7e103574-59ad-4790-b5f9-fa8d715e711e">Recordset-Related Error Information</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5508808253be1fbb0254684e65835341" id="tgt22" class="tgtSentence">             <legacyLink xlink:href="8c57f35e-3c04-4f17-bf3e-3ad053951530">Handling Errors In Other Languages</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dac557765594ae038d85eb72ff184033" id="tgt23" class="tgtSentence">             <legacyLink xlink:href="ea1d4a97-58c3-476b-a496-cc80db2a90d5">Anticipating Errors</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO uses several different methods to notify an application of errors that occur.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This section discusses the types of errors that can occur when you are using ADO and how your application is notified.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> It concludes by making suggestions about how to handle those errors.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">How Does ADO Report Errors?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">ADO notifies you about errors in several ways:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">ADO errors generate a run-time error.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> Handle an ADO error the same way you would any other run-time error, such as using an <legacyBold>On Error</legacyBold> statement in Visual Basic.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Your program can receive errors from OLE DB.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> An OLE DB error generates a run-time error as well.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">If the error is specific to your data provider, one or more <legacyBold>Error</legacyBold> objects are placed in the <legacyBold>Errors</legacyBold> collection of the <legacyBold>Connection</legacyBold> object that was used to access the data store when the error occurred.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">If the process that raised an event also produced an error, error information is placed in an <legacyBold>Error</legacyBold> object and passed as a parameter to the event.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> See <legacyLink xlink:href="e9003457-0762-48b3-942f-0820266b158f">Handling ADO Events</legacyLink> for more information about events.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Problems that occur when processing batch updates or other bulk operations involving a <legacyBold>Recordset</legacyBold> can be indicated by the <legacyBold>Status</legacyBold> property of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> For example, schema constraint violations or insufficient permissions can be specified by <legacyBold>RecordStatusEnum</legacyBold> values.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">Problems that occur involving a particular <legacyBold>Field</legacyBold> in the current record are also indicated by the <legacyBold>Status</legacyBold> property of each <legacyBold>Field</legacyBold> in the <legacyBold>Fields</legacyBold> collection of the <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> For example, updates that could not be completed or incompatible data types can be specified by <legacyBold>FieldStatusEnum</legacyBold> values.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src17" class="srcSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">             <legacyLink xlink:href="9bb84114-a1df-4122-a1b8-ad98dcd85cc3">ADO Errors</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">             <legacyLink xlink:href="cc7d6ff9-2034-45c6-9d61-90b177010054">Provider Errors</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">             <legacyLink xlink:href="5e7b1af4-996b-47c5-9161-c5575ad4fec9">Field-Related Error Information</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src21" class="srcSentence">             <legacyLink xlink:href="7e103574-59ad-4790-b5f9-fa8d715e711e">Recordset-Related Error Information</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">             <legacyLink xlink:href="8c57f35e-3c04-4f17-bf3e-3ad053951530">Handling Errors In Other Languages</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">             <legacyLink xlink:href="ea1d4a97-58c3-476b-a496-cc80db2a90d5">Anticipating Errors</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
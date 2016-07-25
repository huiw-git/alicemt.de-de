---
title: "Handling ADO Events"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9003457-0762-48b3-942f-0820266b158f
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
# Handling ADO Events
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e5e9e15ff5b82c91dc51e11686082d06" id="tgt1" class="tgtSentence">The ADO event model supports certain synchronous and asynchronous ADO operations that issue <legacyItalic>events</legacyItalic>, or notifications, before the operation starts or after it completes.</caps:sentence>
          <caps:sentence sentenceid="8a77eb46225c9e4e735e28cb83092b0b" id="tgt2" class="tgtSentence"> An event is actually a call to an event-handler routine that you define in your application.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="34d9822f7eb9ebf8429f07704b93ec9c" id="tgt3" class="tgtSentence">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation.</caps:sentence>
          <caps:sentence sentenceid="17588ea508e409783d0eb919f3008fde" id="tgt4" class="tgtSentence"> Because it has not been executed yet, you can either cancel the operation or allow it to complete.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ac0267f1bb1989c3628d2977ae136402" id="tgt5" class="tgtSentence">The events that occur after an operation completes are especially important if you use ADO asynchronously.</caps:sentence>
          <caps:sentence sentenceid="cfb5ac907478c161173dbe1683c8707e" id="tgt6" class="tgtSentence"> For example, an application that starts an asynchronous <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Recordset.Open</legacyLink> operation is notified by an execution complete event when the operation concludes.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="eae0c7a8a36d1867b386851d27ee23c8" id="tgt7" class="tgtSentence">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property of an object with a loop.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="e50a517c0c81266a5dd90395103aefae" id="tgt8" class="tgtSentence">To handle events, ADO needs to have a message pump or be used in a single-threaded apartment (STA) model.</caps:sentence>
            <caps:sentence sentenceid="0aaf53a0646384479a45c83357f1254c" id="tgt9" class="tgtSentence"> ADO events are internally handled by creating a hidden window.</caps:sentence>
            <caps:sentence sentenceid="bcb9e996acdf07fbe71bdfca3c0b3fe0" id="tgt10" class="tgtSentence"> ADO posts messages to this window when events need to be fired.</caps:sentence>
            <caps:sentence sentenceid="cf5caa1dc041605c11d8d63ca90dd0d9" id="tgt11" class="tgtSentence"> This is done to ensure that events are sent to the thread that called <unmanagedCodeEntityReference>IConnectionPoint::Advise</unmanagedCodeEntityReference> on the connection point.</caps:sentence>
            <caps:sentence sentenceid="cedfbe6631a1172a885e02d797623a9b" id="tgt12" class="tgtSentence"> This architecture can cause problems when the thread that should receive the notifications does not pump window messages.</caps:sentence>
            <caps:sentence sentenceid="e938d1edf47861b6ea07a7feed81bfae" id="tgt13" class="tgtSentence"> Potential problems include ADO events not being delivered to the thread and global window broadcasts timing out and possibly slowing down the entire system because the hidden windows do not process the messages.</caps:sentence>
            <caps:sentence sentenceid="cdf6c0a6f74ee5dfb186c2939ec0aa28" id="tgt14" class="tgtSentence"> STA threads typically have a message pump running so this issue does not manifest itself on STA threads.</caps:sentence>
            <caps:sentence sentenceid="c583ce2057d3bee1425a7fbe04e6cd11" id="tgt15" class="tgtSentence"> MTA threads, however, do not typically have a message pump so the issue will typically manifest itself on MTA threads.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt16" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">
                <caps:sentence sentenceid="0a49d5dd2699f6a2438b1f759d7bac76" id="tgt17" class="tgtSentence">ADO Event Handler Summary</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">
                <caps:sentence sentenceid="963a40767917043f50fd9bef4914f089" id="tgt18" class="tgtSentence">Types of Events</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">
                <caps:sentence sentenceid="20900e92212288da0a55fc05caecc5cf" id="tgt19" class="tgtSentence">Event Parameters</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">
                <caps:sentence sentenceid="13d3813e8b0609b44e7505697d033836" id="tgt20" class="tgtSentence">How Event Handlers Work Together</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">
                <caps:sentence sentenceid="54cb06fa5f39b9d3bfcc70802429d1d0" id="tgt21" class="tgtSentence">ADO Event Instantiation by Language</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The ADO event model supports certain synchronous and asynchronous ADO operations that issue <legacyItalic>events</legacyItalic>, or notifications, before the operation starts or after it completes.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> An event is actually a call to an event-handler routine that you define in your application.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Because it has not been executed yet, you can either cancel the operation or allow it to complete.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The events that occur after an operation completes are especially important if you use ADO asynchronously.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> For example, an application that starts an asynchronous <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Recordset.Open</legacyLink> operation is notified by an execution complete event when the operation concludes.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property of an object with a loop.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src8" class="srcSentence">To handle events, ADO needs to have a message pump or be used in a single-threaded apartment (STA) model.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> ADO events are internally handled by creating a hidden window.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> ADO posts messages to this window when events need to be fired.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> This is done to ensure that events are sent to the thread that called <unmanagedCodeEntityReference>IConnectionPoint::Advise</unmanagedCodeEntityReference> on the connection point.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> This architecture can cause problems when the thread that should receive the notifications does not pump window messages.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Potential problems include ADO events not being delivered to the thread and global window broadcasts timing out and possibly slowing down the entire system because the hidden windows do not process the messages.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> STA threads typically have a message pump running so this issue does not manifest itself on STA threads.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> MTA threads, however, do not typically have a message pump so the issue will typically manifest itself on MTA threads.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src16" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">
                <caps:sentence id="src17" class="srcSentence">ADO Event Handler Summary</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">
                <caps:sentence id="src18" class="srcSentence">Types of Events</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">
                <caps:sentence id="src19" class="srcSentence">Event Parameters</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">
                <caps:sentence id="src20" class="srcSentence">How Event Handlers Work Together</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">
                <caps:sentence id="src21" class="srcSentence">ADO Event Instantiation by Language</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
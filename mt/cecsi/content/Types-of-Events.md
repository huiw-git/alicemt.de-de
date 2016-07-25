---
title: "Types of Events"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f3327ea0-635a-43d4-bd78-c1674f62f1a2
caps.latest.revision: 8
caps.handback.revision: 8
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
# Types of Events
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8a423ad4741f00f9a06881f415e2bc3a" id="tgt1" class="tgtSentence">There are two basic types of events.</caps:sentence>
          <caps:sentence sentenceid="e07adc8ae976886c2305ef78e9ce5b81" id="tgt2" class="tgtSentence"> "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, <legacyBold>WillChangeRecordset</legacyBold> or <legacyBold>WillConnect</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="de567d92354ea94989ced7c93837168d" id="tgt3" class="tgtSentence"> Events that are called after an event has been completed usually include "Complete" in their names — for example, <legacyBold>RecordChangeComplete</legacyBold> or <legacyBold>ConnectComplete</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="7ad3951c00b3ce78ed6a982725e954a5" id="tgt4" class="tgtSentence"> Exceptions exist — such as <legacyBold>InfoMessage</legacyBold> — but these occur after the associated operation has completed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="d6db87ab357b51ae6ee601daf5e68c15" id="tgt5" class="tgtSentence">Will Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="934059c0b71b8837d64bcf8d5d21e73f" id="tgt6" class="tgtSentence">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</caps:sentence>
            <caps:sentence sentenceid="b039120b13da565a34ed6c4dbf47bfbc" id="tgt7" class="tgtSentence"> These event-handler routines usually have names of the form <legacyBold>Will</legacyBold><legacyBold><legacyItalic>Event</legacyItalic></legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a69c5779a595ebdb28bf24b0ead08b38" id="tgt8" class="tgtSentence">Complete Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="91c871c4b9d35f795d2442085cc840b9" id="tgt9" class="tgtSentence">Event handlers called after an operation completes can notify your application that an operation has concluded.</caps:sentence>
            <caps:sentence sentenceid="feac10c67f24019bfbee5f700426929c" id="tgt10" class="tgtSentence"> Such an event handler is also notified when a Will event handler cancels a pending operation.</caps:sentence>
            <caps:sentence sentenceid="e7d45accc5b4db5eaf1786b91c0ff032" id="tgt11" class="tgtSentence"> These event-handler routines usually have names of the form <legacyBold><legacyItalic>Event</legacyItalic></legacyBold><legacyBold>Complete</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="aa37d82d7781fa77b64433994cfcfb86" id="tgt12" class="tgtSentence">Will and Complete events are typically used in pairs.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16f166ba2ceaca92e52aea587fb0114f" id="tgt13" class="tgtSentence">Other Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="02a422011642f10b832c1e114aeacb3c" id="tgt14" class="tgtSentence">The other event handlers — that is, events whose names are not of the form <legacyBold>Will</legacyBold><legacyBold><legacyItalic>Event</legacyItalic></legacyBold> or <legacyBold><legacyItalic>Event</legacyItalic></legacyBold><legacyBold>Complete</legacyBold> — are called only after an operation completes.</caps:sentence>
            <caps:sentence sentenceid="d648debf03cc926b33672211ad3e036e" id="tgt15" class="tgtSentence"> These events are <legacyBold>Disconnect</legacyBold>, <legacyBold>EndOfRecordset</legacyBold>, and <legacyBold>InfoMessage</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">How Event Handlers Work Together</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">There are two basic types of events.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, <legacyBold>WillChangeRecordset</legacyBold> or <legacyBold>WillConnect</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Events that are called after an event has been completed usually include "Complete" in their names — for example, <legacyBold>RecordChangeComplete</legacyBold> or <legacyBold>ConnectComplete</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Exceptions exist — such as <legacyBold>InfoMessage</legacyBold> — but these occur after the associated operation has completed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Will Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> These event-handler routines usually have names of the form <legacyBold>Will</legacyBold><legacyBold><legacyItalic>Event</legacyItalic></legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Complete Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">Event handlers called after an operation completes can notify your application that an operation has concluded.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Such an event handler is also notified when a Will event handler cancels a pending operation.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> These event-handler routines usually have names of the form <legacyBold><legacyItalic>Event</legacyItalic></legacyBold><legacyBold>Complete</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">Will and Complete events are typically used in pairs.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Other Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">The other event handlers — that is, events whose names are not of the form <legacyBold>Will</legacyBold><legacyBold><legacyItalic>Event</legacyItalic></legacyBold> or <legacyBold><legacyItalic>Event</legacyItalic></legacyBold><legacyBold>Complete</legacyBold> — are called only after an operation completes.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> These events are <legacyBold>Disconnect</legacyBold>, <legacyBold>EndOfRecordset</legacyBold>, and <legacyBold>InfoMessage</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">How Event Handlers Work Together</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
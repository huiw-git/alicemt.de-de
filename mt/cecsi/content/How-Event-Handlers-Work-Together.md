---
title: "How Event Handlers Work Together"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a86c8a02-dd69-420d-8a47-0188b339858d
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
# How Event Handlers Work Together
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c66ce2944435e3531e9e8571225b2dbe" id="tgt1" class="tgtSentence">Unless you are programming in Visual Basic, all event handlers for <legacyBold>Connection</legacyBold> and <legacyBold>Recordset</legacyBold> events must be implemented, regardless of whether you actually process all of the events.</caps:sentence>
          <caps:sentence sentenceid="def54dd57019d54d030eb0b199b72da8" id="tgt2" class="tgtSentence"> The amount of implementation work you have to do depends on your programming language.</caps:sentence>
          <caps:sentence sentenceid="7ee950f366f18b58d2803786545d6f35" id="tgt3" class="tgtSentence"> For more information, see <legacyLink xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="73a9f6202c1b0f5edf74aaf5c57ddd64" id="tgt4" class="tgtSentence">Paired Event Handlers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8098ebef9c0368f1e01a3f70798632c7" id="tgt5" class="tgtSentence">Each Will event handler has an associated <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event handler.</caps:sentence>
            <caps:sentence sentenceid="97eb014210e3daa5530984307268f21d" id="tgt6" class="tgtSentence"> For example, when your application changes the value of a field, the <legacyBold>WillChangeField</legacyBold> event handler is called.</caps:sentence>
            <caps:sentence sentenceid="36f2e2f2c302967978b92a643fe035f8" id="tgt7" class="tgtSentence"> If the change is acceptable, your application leaves the <legacyBold>adStatus</legacyBold> parameter unchanged and the operation is performed.</caps:sentence>
            <caps:sentence sentenceid="4b2bc49da6a2a3f37d39e6038102b584" id="tgt8" class="tgtSentence"> When the operation completes, a <legacyBold>FieldChangeComplete</legacyBold> event notifies your application that the operation has finished.</caps:sentence>
            <caps:sentence sentenceid="3a4ad28a967cae710887be7d73ecc635" id="tgt9" class="tgtSentence"> If it completed successfully, <legacyBold>adStatus</legacyBold> contains <legacyBold>adStatusOK</legacyBold>; otherwise, <legacyBold>adStatus</legacyBold> contains <legacyBold>adStatusErrorsOccurred</legacyBold> and you must check the <legacyBold>Error</legacyBold> object to determine the cause of the error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a2ff0889980a0da0f23990070449d6ee" id="tgt10" class="tgtSentence">When <legacyBold>WillChangeField</legacyBold> is called, you might determine that the change should not be made.</caps:sentence>
            <caps:sentence sentenceid="e058ec45c9d778ca4aff45beaf390b05" id="tgt11" class="tgtSentence"> In that case, set <legacyBold>adStatus</legacyBold> to <legacyBold>adStatusCancel.</legacyBold> The operation is canceled and the <legacyBold>FieldChangeComplete</legacyBold> event receives an <legacyBold>adStatus</legacyBold> value of <legacyBold>adStatusErrorsOccurred</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="099f64a52dbca24e54241a213dc21874" id="tgt12" class="tgtSentence"> The <legacyBold>Error</legacyBold> object contains <legacyBold>adErrOperationCancelled</legacyBold> so that your <legacyBold>FieldChangeComplete</legacyBold> handler knows that the operation was canceled.</caps:sentence>
            <caps:sentence sentenceid="33780c02dd463b319fd00d1fb2e8cf18" id="tgt13" class="tgtSentence"> However, you need to check the value of the <legacyBold>adStatus</legacyBold> parameter before changing it, because setting <legacyBold>adStatus</legacyBold> to <legacyBold>adStatusCancel</legacyBold> has no effect if the parameter was set to <legacyBold>adStatusCantDeny</legacyBold> on entry to the procedure.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e5ad8a56033beff191b8f667816defba" id="tgt14" class="tgtSentence">Sometimes an operation can raise more than one event.</caps:sentence>
            <caps:sentence sentenceid="1fa8e9259b68f8185bb7257c34d9d526" id="tgt15" class="tgtSentence"> For example, the <legacyBold>Recordset</legacyBold> object has paired events for <legacyBold>Field</legacyBold> changes and <legacyBold>Record</legacyBold> changes.</caps:sentence>
            <caps:sentence sentenceid="0f84b93a5b44596621824105d04c1c53" id="tgt16" class="tgtSentence"> When your application changes the value of a <legacyBold>Field</legacyBold>, the <legacyBold>WillChangeField</legacyBold> event handler is called.</caps:sentence>
            <caps:sentence sentenceid="d34e35b7a28c71c94b21af824370bf73" id="tgt17" class="tgtSentence"> If it determines that the operation can continue, the <legacyBold>WillChangeRecord</legacyBold> event handler is also raised.</caps:sentence>
            <caps:sentence sentenceid="ce0570612d8e1ecb4741b71104ff1ef0" id="tgt18" class="tgtSentence"> If this handler also allows the event to continue, the change is made and the <legacyBold>FieldChangeComplete</legacyBold> and <legacyBold>RecordChangeComplete</legacyBold> event handlers are called.</caps:sentence>
            <caps:sentence sentenceid="71f36e3ed089fac8d78eb9350ac0c4e8" id="tgt19" class="tgtSentence"> The order in which the Will event handlers for a particular operation are called is not defined, so you should avoid writing code that depends on calling handlers in a particular sequence.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f6a8e681bb746c80b652e32b4fb56f62" id="tgt20" class="tgtSentence">In instances when multiple Will events are raised, one of the events might cancel the pending operation.</caps:sentence>
            <caps:sentence sentenceid="c1e4e556ae2a11dfcc6a8dbcdb81e67d" id="tgt21" class="tgtSentence"> For example, when your application changes the value of a <legacyBold>Field</legacyBold>, both <legacyBold>WillChangeField</legacyBold> and <legacyBold>WillChangeRecord</legacyBold> event handlers would normally be called.</caps:sentence>
            <caps:sentence sentenceid="6bf8dfc6a69152caf4beea31a08ffc14" id="tgt22" class="tgtSentence"> However, if the operation is canceled in the first event handler, its associated <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> handler is immediately called with <legacyBold>adStatusOperationCancelled</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="4f7cce627523803ffd1b8bdaf4dd3f03" id="tgt23" class="tgtSentence"> The second handler is never called.</caps:sentence>
            <caps:sentence sentenceid="9683cc7eaacdee4e10d2f57c5f2f0e93" id="tgt24" class="tgtSentence"> If, however, the first event handler allows the event to proceed, the other event handler will be called.</caps:sentence>
            <caps:sentence sentenceid="d103fa3a97b077067f58ea318c3308cd" id="tgt25" class="tgtSentence"> If it then cancels the operation, both <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> events will be called as in the earlier examples.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c0ae8342698de80f4a52dd31eb92ce16" id="tgt26" class="tgtSentence">Unpaired Event Handlers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5469b0ac7804f4b91d7b9e28e63b25cc" id="tgt27" class="tgtSentence">As long as the status passed to the event is not <legacyBold>adStatusCantDeny</legacyBold>, you can turn off event notifications for any event by returning <legacyBold>adStatusUnwantedEvent</legacyBold> in the <legacyItalic>Status</legacyItalic> parameter.</caps:sentence>
            <caps:sentence sentenceid="4b7663d6775001eb6c416889ce6ab8cd" id="tgt28" class="tgtSentence"> For example, when your <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event handler is called the first time, you can return <legacyBold>adStatusUnwantedEvent</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="617755e8be638ab2005bbeb57f8ed9a6" id="tgt29" class="tgtSentence"> You will subsequently receive only <unmanagedCodeEntityReference>Will</unmanagedCodeEntityReference> events.</caps:sentence>
            <caps:sentence sentenceid="b696598e74ed05a097ce3240624b81b2" id="tgt30" class="tgtSentence"> However, some events can be triggered for more than one reason.</caps:sentence>
            <caps:sentence sentenceid="6889256ecf48ade82a12e62e53ef6d68" id="tgt31" class="tgtSentence"> In that case, the event will have a <legacyItalic>Reason</legacyItalic> parameter.</caps:sentence>
            <caps:sentence sentenceid="3cb3caa399afeb0f4f56d9fc4005b733" id="tgt32" class="tgtSentence"> When you return <legacyBold>adStatusUnwantedEvent</legacyBold>, you will stop receiving notifications for that event only when they occur for that particular reason.</caps:sentence>
            <caps:sentence sentenceid="65f7b97ec522bef77469c4e172ef68af" id="tgt33" class="tgtSentence"> In other words, you will potentially receive notification for each possible reason that the event could be triggered.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="00b9ec94378879e48a1b8b2f9b7c0456" id="tgt34" class="tgtSentence">Single <unmanagedCodeEntityReference>Will</unmanagedCodeEntityReference> event handlers can be useful when you want to examine the parameters that will be used in an operation.</caps:sentence>
            <caps:sentence sentenceid="737f4f4be897f8a81ff81f3479170a40" id="tgt35" class="tgtSentence"> You can modify those operation parameters or cancel the operation.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e6552181e38650fbd2a7db1d38009e4b" id="tgt36" class="tgtSentence">Alternatively, leave <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event notification enabled.</caps:sentence>
            <caps:sentence sentenceid="4f1973d4c812305d37ef3e580896cb94" id="tgt37" class="tgtSentence"> When your first Will event handler is called, return <legacyBold>adStatusUnwantedEvent</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="6f6f8296d447b7d03edd1301ebc37c4d" id="tgt38" class="tgtSentence"> You will subsequently receive only <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> events.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="298761135393fa68282c46c794c3b514" id="tgt39" class="tgtSentence">Single <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event handlers can be useful for managing asynchronous operations.</caps:sentence>
            <caps:sentence sentenceid="cb161a1d194bf972073ab10d9df1f754" id="tgt40" class="tgtSentence"> Each asynchronous operation has an appropriate <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4b4be04c07737db5d45ef38e9c900da2" id="tgt41" class="tgtSentence">For example, it can take a long time to populate a large <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="1f71407038798e40f1594477c1940d80" id="tgt42" class="tgtSentence"> If your application is appropriately written, you can start a <codeInline>Recordset.Open(...,adAsyncExecute)</codeInline> operation and continue with other processing.</caps:sentence>
            <caps:sentence sentenceid="5e5455633d31c2412c4b910f3ffee49d" id="tgt43" class="tgtSentence"> You will eventually be notified when the <legacyBold>Recordset</legacyBold> is populated by an <legacyBold>ExecuteComplete</legacyBold> event.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="907788176d0fd6bff78024f7f51f4b3b" id="tgt44" class="tgtSentence">Single Event Handlers and Multiple Objects</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="330579e4269e95fb96202fc43af64da1" id="tgt45" class="tgtSentence">The flexibility of a programming language like Microsoft Visual C++® enables you to have one event handler process events from multiple objects.</caps:sentence>
            <caps:sentence sentenceid="152294babf0e3c250832fe3deed9950e" id="tgt46" class="tgtSentence"> For example, you could have one <legacyBold>Disconnect</legacyBold> event handler process events from several <legacyBold>Connection</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="8642ae90d9ad0d61a7187520220962a1" id="tgt47" class="tgtSentence"> If one of the connections ended, the <legacyBold>Disconnect</legacyBold> event handler would be called.</caps:sentence>
            <caps:sentence sentenceid="32e33be2279f6407ed7eda388adcb9d5" id="tgt48" class="tgtSentence"> You could tell which connection caused the event because the event-handler object parameter would be set to the corresponding <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="5ad42a16782015c5fd1099f9a6e73d8c" id="tgt49" class="tgtSentence">This technique cannot be used in Visual Basic because that language can correlate only one object to an event handler.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Unless you are programming in Visual Basic, all event handlers for <legacyBold>Connection</legacyBold> and <legacyBold>Recordset</legacyBold> events must be implemented, regardless of whether you actually process all of the events.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The amount of implementation work you have to do depends on your programming language.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For more information, see <legacyLink xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Paired Event Handlers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Each Will event handler has an associated <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event handler.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For example, when your application changes the value of a field, the <legacyBold>WillChangeField</legacyBold> event handler is called.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If the change is acceptable, your application leaves the <legacyBold>adStatus</legacyBold> parameter unchanged and the operation is performed.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> When the operation completes, a <legacyBold>FieldChangeComplete</legacyBold> event notifies your application that the operation has finished.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If it completed successfully, <legacyBold>adStatus</legacyBold> contains <legacyBold>adStatusOK</legacyBold>; otherwise, <legacyBold>adStatus</legacyBold> contains <legacyBold>adStatusErrorsOccurred</legacyBold> and you must check the <legacyBold>Error</legacyBold> object to determine the cause of the error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">When <legacyBold>WillChangeField</legacyBold> is called, you might determine that the change should not be made.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> In that case, set <legacyBold>adStatus</legacyBold> to <legacyBold>adStatusCancel.</legacyBold> The operation is canceled and the <legacyBold>FieldChangeComplete</legacyBold> event receives an <legacyBold>adStatus</legacyBold> value of <legacyBold>adStatusErrorsOccurred</legacyBold>.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The <legacyBold>Error</legacyBold> object contains <legacyBold>adErrOperationCancelled</legacyBold> so that your <legacyBold>FieldChangeComplete</legacyBold> handler knows that the operation was canceled.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> However, you need to check the value of the <legacyBold>adStatus</legacyBold> parameter before changing it, because setting <legacyBold>adStatus</legacyBold> to <legacyBold>adStatusCancel</legacyBold> has no effect if the parameter was set to <legacyBold>adStatusCantDeny</legacyBold> on entry to the procedure.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">Sometimes an operation can raise more than one event.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> For example, the <legacyBold>Recordset</legacyBold> object has paired events for <legacyBold>Field</legacyBold> changes and <legacyBold>Record</legacyBold> changes.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> When your application changes the value of a <legacyBold>Field</legacyBold>, the <legacyBold>WillChangeField</legacyBold> event handler is called.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> If it determines that the operation can continue, the <legacyBold>WillChangeRecord</legacyBold> event handler is also raised.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> If this handler also allows the event to continue, the change is made and the <legacyBold>FieldChangeComplete</legacyBold> and <legacyBold>RecordChangeComplete</legacyBold> event handlers are called.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> The order in which the Will event handlers for a particular operation are called is not defined, so you should avoid writing code that depends on calling handlers in a particular sequence.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">In instances when multiple Will events are raised, one of the events might cancel the pending operation.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> For example, when your application changes the value of a <legacyBold>Field</legacyBold>, both <legacyBold>WillChangeField</legacyBold> and <legacyBold>WillChangeRecord</legacyBold> event handlers would normally be called.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> However, if the operation is canceled in the first event handler, its associated <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> handler is immediately called with <legacyBold>adStatusOperationCancelled</legacyBold>.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> The second handler is never called.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> If, however, the first event handler allows the event to proceed, the other event handler will be called.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> If it then cancels the operation, both <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> events will be called as in the earlier examples.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src26" class="srcSentence">Unpaired Event Handlers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src27" class="srcSentence">As long as the status passed to the event is not <legacyBold>adStatusCantDeny</legacyBold>, you can turn off event notifications for any event by returning <legacyBold>adStatusUnwantedEvent</legacyBold> in the <legacyItalic>Status</legacyItalic> parameter.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> For example, when your <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event handler is called the first time, you can return <legacyBold>adStatusUnwantedEvent</legacyBold>.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> You will subsequently receive only <unmanagedCodeEntityReference>Will</unmanagedCodeEntityReference> events.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> However, some events can be triggered for more than one reason.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> In that case, the event will have a <legacyItalic>Reason</legacyItalic> parameter.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> When you return <legacyBold>adStatusUnwantedEvent</legacyBold>, you will stop receiving notifications for that event only when they occur for that particular reason.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> In other words, you will potentially receive notification for each possible reason that the event could be triggered.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src34" class="srcSentence">Single <unmanagedCodeEntityReference>Will</unmanagedCodeEntityReference> event handlers can be useful when you want to examine the parameters that will be used in an operation.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> You can modify those operation parameters or cancel the operation.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src36" class="srcSentence">Alternatively, leave <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event notification enabled.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> When your first Will event handler is called, return <legacyBold>adStatusUnwantedEvent</legacyBold>.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> You will subsequently receive only <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> events.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src39" class="srcSentence">Single <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event handlers can be useful for managing asynchronous operations.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> Each asynchronous operation has an appropriate <unmanagedCodeEntityReference>Complete</unmanagedCodeEntityReference> event.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src41" class="srcSentence">For example, it can take a long time to populate a large <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> If your application is appropriately written, you can start a <codeInline>Recordset.Open(...,adAsyncExecute)</codeInline> operation and continue with other processing.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> You will eventually be notified when the <legacyBold>Recordset</legacyBold> is populated by an <legacyBold>ExecuteComplete</legacyBold> event.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src44" class="srcSentence">Single Event Handlers and Multiple Objects</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src45" class="srcSentence">The flexibility of a programming language like Microsoft Visual C++® enables you to have one event handler process events from multiple objects.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> For example, you could have one <legacyBold>Disconnect</legacyBold> event handler process events from several <legacyBold>Connection</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> If one of the connections ended, the <legacyBold>Disconnect</legacyBold> event handler would be called.</caps:sentence>
            <caps:sentence id="src48" class="srcSentence"> You could tell which connection caused the event because the event-handler object parameter would be set to the corresponding <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src49" class="srcSentence">This technique cannot be used in Visual Basic because that language can correlate only one object to an event handler.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ADO Event Instantiation: ADO/WFC"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9ee4be21-657b-407a-afa4-0b27a6b096ce
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
# ADO Event Instantiation: ADO/WFC
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f8099dcbe74f4f0c1624e89bdd10116e" id="tgt1" class="tgtSentence">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface.</caps:sentence>
          <caps:sentence sentenceid="ad93ba23d0f8c82e5b6b06c301e2fa42" id="tgt2" class="tgtSentence"> In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence sentenceid="0df39096bf58db8648613885322191d0" id="tgt3" class="tgtSentence">To use ADO events in ADO/WFC</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="c9151cc54351c1cfff2b5cb8a4ac68cc" id="tgt4" class="tgtSentence">Define your own event handler to process an event.</caps:sentence>
                  <caps:sentence sentenceid="dfbbf3478df0b5dc30121c2899f1722b" id="tgt5" class="tgtSentence"> For example, if you wanted to process the <legacyBold>ConnectComplete</legacyBold> event in the <legacyBold>ConnectionEvent</legacyBold> family, you might use this code:</caps:sentence>
                </para>
                <code>public void onConnectComplete(Object sender,ConnectionEvent e)
{
    System.out.println("onConnectComplete:" + e);
}</code>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="878d8ed636d6034564db9c989b41a244" id="tgt6" class="tgtSentence">Define a handler object to represent your event handler.</caps:sentence>
                  <caps:sentence sentenceid="ca9370938bf49df85c28b02b73eb5e7d" id="tgt7" class="tgtSentence"> The handler object should be of data type <legacyBold>ConnectEventHandler</legacyBold> for an event of type <legacyBold>ConnectionEvent</legacyBold>, or data type <legacyBold>RecordsetEventHandler</legacyBold> for an event of type <legacyBold>RecordsetEvent</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="4b162ab94234d9875dc49b4a9eb8abc7" id="tgt8" class="tgtSentence"> For example, code the following for your <legacyBold>ConnectComplete</legacyBold> event handler:</caps:sentence>
                </para>
                <code>    ConnectionEventHandler handler = 
        new ConnectionEventHandler(this, "onConnectComplete");</code>
                <para>
                  <caps:sentence sentenceid="0cf284ba3f7dc8a45bb434852f2eb886" id="tgt9" class="tgtSentence">The first argument of the <legacyBold>ConnectionEventHandler</legacyBold> constructor is a reference to the class that contains the event handler named in the second argument.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="885a30a753bdae32736b4e9bd6bb6e77" id="tgt10" class="tgtSentence">The Microsoft Visual J++ compiler also supports an equivalent syntax:  </caps:sentence>
                </para>
                <code>    ConnectionEventHandler handler = 
        new ConnectionEventHandler(this.onConnectComplete);</code>
                <para>
                  <caps:sentence sentenceid="0881825875ccc7a85174c330dc17c933" id="tgt11" class="tgtSentence">The single argument is a reference to the desired class (<legacyBold>this</legacyBold>) and method within the class (<legacyBold>onConnectComplete</legacyBold>).</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="366588a391593940f71c01ca17bbbede" id="tgt12" class="tgtSentence">Add your event handler to a list of handlers designated to process a particular type of event.</caps:sentence>
                  <caps:sentence sentenceid="decda34da245b128213ebca1d04cc39d" id="tgt13" class="tgtSentence"> Use the method with a name such as <legacyBold>addOn</legacyBold><legacyItalic>EventName</legacyItalic>(<legacyItalic>handler</legacyItalic>).</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="e47cbd6af9a8318fa07fdf19f29ecb0e" id="tgt14" class="tgtSentence">ADO/WFC internally implements all the ADO event handlers.</caps:sentence>
                  <caps:sentence sentenceid="dbdef0c60e3c114a9915399eb463df20" id="tgt15" class="tgtSentence"> Therefore, an event caused by a <legacyBold>Connection</legacyBold> or <legacyBold>Recordset</legacyBold> operation is intercepted by an ADO/WFC event handler.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="0e26067e0a84eb9b9e1e13976c23b8dd" id="tgt16" class="tgtSentence">The ADO/WFC event handler passes ADO <legacyBold>ConnectionEvent</legacyBold> parameters in an instance of the ADO/WFC <legacyBold>ConnectionEvent</legacyBold> class, or ADO <legacyBold>RecordsetEvent</legacyBold> parameters in an instance of the ADO/WFC <legacyBold>RecordsetEvent</legacyBold> class.</caps:sentence>
                  <caps:sentence sentenceid="57656b3d7ba406a3310618e6f1ce9a61" id="tgt17" class="tgtSentence"> These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO <legacyBold>ConnectionEvent</legacyBold> or <legacyBold>RecordsetEvent</legacyBold> methods.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="f348c85ce3ba51f28be6a15f3bc6ba31" id="tgt18" class="tgtSentence">ADO/WFC then calls your event handler with the ADO/WFC event object.</caps:sentence>
                  <caps:sentence sentenceid="48eb3c397d78e213651c9577ebed59c7" id="tgt19" class="tgtSentence"> For example, your <legacyBold>onConnectComplete</legacyBold> handler has a signature like this:</caps:sentence>
                </para>
                <code>    public void onConnectComplete(Object sender,ConnectionEvent e)</code>
                <para>
                  <caps:sentence sentenceid="789d5d7360e6a4ade4e43e35604844cd" id="tgt20" class="tgtSentence">The first argument is the type of object that sent the event (<legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> or <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>), and the second argument is the ADO/WFC event object (<legacyBold>ConnectionEvent</legacyBold> or <legacyBold>RecordsetEvent</legacyBold>).</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="5f0d642fcf921dc736f249a0c3119082" id="tgt21" class="tgtSentence">The signature of your event handler is simpler than an ADO event.</caps:sentence>
                  <caps:sentence sentenceid="5027bcdf29665aad6aa89b7fc8d0e750" id="tgt22" class="tgtSentence"> However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="a896a5fba2c77955e3221be6973027ed" id="tgt23" class="tgtSentence">Return from your event handler to the ADO/WFC handler for the ADO event.</caps:sentence>
                  <caps:sentence sentenceid="29e53f2e2fd9a9de9de7a0d041d7ac19" id="tgt24" class="tgtSentence"> ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="c82ad1190de44240acc2c7cb02748ff9" id="tgt25" class="tgtSentence">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</caps:sentence>
                  <caps:sentence sentenceid="4b1f40833c4330c648ca0c9d60b7a96a" id="tgt26" class="tgtSentence"> Use the method with a name such as <legacyBold>removeOn</legacyBold><legacyItalic>EventName</legacyItalic>(<legacyItalic>handler</legacyItalic>).</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="1fdfa42e-897e-4770-b320-ab3720adabcc">ADO/WFC Programming </link>
        <link xlink:href="a14bbc36-87ec-409d-97b3-393b66b1b8e3">ADO/WFC Syntax Index</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">How Event Handlers Work Together</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence id="src3" class="srcSentence">To use ADO events in ADO/WFC</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Define your own event handler to process an event.</caps:sentence>
                  <caps:sentence id="src5" class="srcSentence"> For example, if you wanted to process the <legacyBold>ConnectComplete</legacyBold> event in the <legacyBold>ConnectionEvent</legacyBold> family, you might use this code:</caps:sentence>
                </para>
                <code>public void onConnectComplete(Object sender,ConnectionEvent e)
{
    System.out.println("onConnectComplete:" + e);
}</code>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Define a handler object to represent your event handler.</caps:sentence>
                  <caps:sentence id="src7" class="srcSentence"> The handler object should be of data type <legacyBold>ConnectEventHandler</legacyBold> for an event of type <legacyBold>ConnectionEvent</legacyBold>, or data type <legacyBold>RecordsetEventHandler</legacyBold> for an event of type <legacyBold>RecordsetEvent</legacyBold>.</caps:sentence>
                  <caps:sentence id="src8" class="srcSentence"> For example, code the following for your <legacyBold>ConnectComplete</legacyBold> event handler:</caps:sentence>
                </para>
                <code>    ConnectionEventHandler handler = 
        new ConnectionEventHandler(this, "onConnectComplete");</code>
                <para>
                  <caps:sentence id="src9" class="srcSentence">The first argument of the <legacyBold>ConnectionEventHandler</legacyBold> constructor is a reference to the class that contains the event handler named in the second argument.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src10" class="srcSentence">The Microsoft Visual J++ compiler also supports an equivalent syntax:  </caps:sentence>
                </para>
                <code>    ConnectionEventHandler handler = 
        new ConnectionEventHandler(this.onConnectComplete);</code>
                <para>
                  <caps:sentence id="src11" class="srcSentence">The single argument is a reference to the desired class (<legacyBold>this</legacyBold>) and method within the class (<legacyBold>onConnectComplete</legacyBold>).</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Add your event handler to a list of handlers designated to process a particular type of event.</caps:sentence>
                  <caps:sentence id="src13" class="srcSentence"> Use the method with a name such as <legacyBold>addOn</legacyBold><legacyItalic>EventName</legacyItalic>(<legacyItalic>handler</legacyItalic>).</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src14" class="srcSentence">ADO/WFC internally implements all the ADO event handlers.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> Therefore, an event caused by a <legacyBold>Connection</legacyBold> or <legacyBold>Recordset</legacyBold> operation is intercepted by an ADO/WFC event handler.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src16" class="srcSentence">The ADO/WFC event handler passes ADO <legacyBold>ConnectionEvent</legacyBold> parameters in an instance of the ADO/WFC <legacyBold>ConnectionEvent</legacyBold> class, or ADO <legacyBold>RecordsetEvent</legacyBold> parameters in an instance of the ADO/WFC <legacyBold>RecordsetEvent</legacyBold> class.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO <legacyBold>ConnectionEvent</legacyBold> or <legacyBold>RecordsetEvent</legacyBold> methods.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src18" class="srcSentence">ADO/WFC then calls your event handler with the ADO/WFC event object.</caps:sentence>
                  <caps:sentence id="src19" class="srcSentence"> For example, your <legacyBold>onConnectComplete</legacyBold> handler has a signature like this:</caps:sentence>
                </para>
                <code>    public void onConnectComplete(Object sender,ConnectionEvent e)</code>
                <para>
                  <caps:sentence id="src20" class="srcSentence">The first argument is the type of object that sent the event (<legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> or <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>), and the second argument is the ADO/WFC event object (<legacyBold>ConnectionEvent</legacyBold> or <legacyBold>RecordsetEvent</legacyBold>).</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src21" class="srcSentence">The signature of your event handler is simpler than an ADO event.</caps:sentence>
                  <caps:sentence id="src22" class="srcSentence"> However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Return from your event handler to the ADO/WFC handler for the ADO event.</caps:sentence>
                  <caps:sentence id="src24" class="srcSentence"> ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src25" class="srcSentence">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</caps:sentence>
                  <caps:sentence id="src26" class="srcSentence"> Use the method with a name such as <legacyBold>removeOn</legacyBold><legacyItalic>EventName</legacyItalic>(<legacyItalic>handler</legacyItalic>).</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <relatedTopics>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
        <link xlink:href="1fdfa42e-897e-4770-b320-ab3720adabcc">ADO/WFC Programming </link>
        <link xlink:href="a14bbc36-87ec-409d-97b3-393b66b1b8e3">ADO/WFC Syntax Index</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">How Event Handlers Work Together</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
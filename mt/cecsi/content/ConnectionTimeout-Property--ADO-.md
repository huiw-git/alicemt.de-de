---
title: "ConnectionTimeout Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8904a403-1383-4b4b-b53d-5c01d6f5deac
caps.latest.revision: 10
caps.handback.revision: 10
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
# ConnectionTimeout Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="556fed498f91841a5b9d0d960dc30c26" id="tgt1" class="tgtSentence">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b6d0f8c51f861005900445fe5ea93e87" id="tgt3" class="tgtSentence">Sets or returns a <legacyBold>Long</legacyBold> value that indicates, in seconds, how long to wait for the connection to open.</caps:sentence>
            <caps:sentence sentenceid="85e2938199651a2fad51d06904e94cdf" id="tgt4" class="tgtSentence"> Default is 15.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="c79399d4b4a1c7e972504f718ec083ee" id="tgt5" class="tgtSentence">Use the <legacyBold>ConnectionTimeout</legacyBold> property on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt.</caps:sentence>
            <caps:sentence sentenceid="588a8301a6db1ceb7e29a76138ba80a7" id="tgt6" class="tgtSentence"> If the time from the <legacyBold>ConnectionTimeout</legacyBold> property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt.</caps:sentence>
            <caps:sentence sentenceid="8850c2db881649b1c409c287201647a9" id="tgt7" class="tgtSentence"> If you set the property to zero, ADO will wait indefinitely until the connection is opened.</caps:sentence>
            <caps:sentence sentenceid="1a5c440f054eb3471da20b2398905dc9" id="tgt8" class="tgtSentence"> Make sure the provider to which you are writing code supports the <legacyBold>ConnectionTimeout</legacyBold> functionality.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="37a5422b77108262b26b3aff498c2c9b" id="tgt9" class="tgtSentence">The <legacyBold>ConnectionTimeout</legacyBold> property is read/write when the connection is closed and read-only when it is open.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4de7336a-b5ea-43f1-b750-5fa302b5b756">Visual Basic Example</link>
        <link xlink:href="c6bd2609-4c49-462f-a1aa-7bee0f615adb">Visual C++ Example</link>
        <link xlink:href="4c1e61ed-6569-44a9-b0c8-75b820a64cb6">Visual J++ Example</link>
        <link xlink:href="c611f857-d6b0-4dca-8925-f4a02e769eb0">CommandTimeout Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyBold>Long</legacyBold> value that indicates, in seconds, how long to wait for the connection to open.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Default is 15.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>ConnectionTimeout</legacyBold> property on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> If the time from the <legacyBold>ConnectionTimeout</legacyBold> property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If you set the property to zero, ADO will wait indefinitely until the connection is opened.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Make sure the provider to which you are writing code supports the <legacyBold>ConnectionTimeout</legacyBold> functionality.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <legacyBold>ConnectionTimeout</legacyBold> property is read/write when the connection is closed and read-only when it is open.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4de7336a-b5ea-43f1-b750-5fa302b5b756">Visual Basic Example</link>
        <link xlink:href="c6bd2609-4c49-462f-a1aa-7bee0f615adb">Visual C++ Example</link>
        <link xlink:href="4c1e61ed-6569-44a9-b0c8-75b820a64cb6">Visual J++ Example</link>
        <link xlink:href="c611f857-d6b0-4dca-8925-f4a02e769eb0">CommandTimeout Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
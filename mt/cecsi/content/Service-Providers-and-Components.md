---
title: "Service Providers and Components"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1fd7a374-587b-4ca9-9204-3a4019b67a71
caps.latest.revision: 13
caps.handback.revision: 13
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
# Service Providers and Components
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b050cb7f4735e64b3dfd97e7d292ed1b" id="tgt1" class="tgtSentence">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="952d377426af7bf218df45f7c5924c94" id="tgt2" class="tgtSentence">Universal Data Access provides a <legacyItalic>component architecture</legacyItalic> that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</caps:sentence>
          <caps:sentence sentenceid="72bf30adbba8fd7518da8d56738ecfb1" id="tgt3" class="tgtSentence"> Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</caps:sentence>
          <caps:sentence sentenceid="705f87852e13459356e0bf03ba52a194" id="tgt4" class="tgtSentence"> The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4166006dc5e919ca05989fc62e0da688" id="tgt5" class="tgtSentence">For example, a cursor engine, such as <legacyLink xlink:href="57638feb-4ecd-4051-becb-8f828d21cf44">The Cursor Service for OLE DB</legacyLink>, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data.</caps:sentence>
          <caps:sentence sentenceid="b837af2c6dca11149122fe2cb39000b1" id="tgt6" class="tgtSentence"> Other service providers commonly used by ADO include the <link xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider (ADO Service Provider)</link> (for saving data to a file), the <link xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</link> (for hierarchical <legacyBold>Recordsets</legacyBold>), and the <link xlink:href="a4360ed4-b70f-4734-9041-4025d033346b">Microsoft OLE DB Remoting Provider (ADO Service Provider)</link> (for invoking data providers on a remote computer).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0b322c11782e46c839deb5cb49fd4754" id="tgt7" class="tgtSentence">For more information about service and data providers, see <legacyLink xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Universal Data Access provides a <legacyItalic>component architecture</legacyItalic> that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">For example, a cursor engine, such as <legacyLink xlink:href="57638feb-4ecd-4051-becb-8f828d21cf44">The Cursor Service for OLE DB</legacyLink>, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Other service providers commonly used by ADO include the <link xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider (ADO Service Provider)</link> (for saving data to a file), the <link xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</link> (for hierarchical <legacyBold>Recordsets</legacyBold>), and the <link xlink:href="a4360ed4-b70f-4734-9041-4025d033346b">Microsoft OLE DB Remoting Provider (ADO Service Provider)</link> (for invoking data providers on a remote computer).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">For more information about service and data providers, see <legacyLink xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
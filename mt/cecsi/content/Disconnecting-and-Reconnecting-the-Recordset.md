---
title: "Disconnecting and Reconnecting the Recordset"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c5134af7-81d6-4de4-9fd1-cfe29973545e
caps.latest.revision: 3
caps.handback.revision: 3
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
# Disconnecting and Reconnecting the Recordset
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e0107d47ef2f8d494df7b0a45102c04e" id="tgt1" class="tgtSentence">One of the most powerful features found in ADO is the capability to open a client-side Recordset from a data source and then disconnect the Recordset from the data source.</caps:sentence>
          <caps:sentence sentenceid="7c582d3de752fb40bac387a2ff0ab78d" id="tgt2" class="tgtSentence"> Once the Recordset has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it.</caps:sentence>
          <caps:sentence sentenceid="1c735eea8191bb8c3381b21e76d51a3b" id="tgt3" class="tgtSentence"> You can continue to view and edit the data in the Recordset while it is disconnected and later reconnect to the data source and send your updates in batch mode.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="62b486a1501ec80a035fbba807fc11c4" id="tgt4" class="tgtSentence">To disconnect a Recordset, open it with a cursor location of adUseClient, and then set the ActiveConnection property equal to Nothing.</caps:sentence>
          <caps:sentence sentenceid="6dc76aed0b508df3e88d786d3b75a0b7" id="tgt5" class="tgtSentence"> (C++ users should set the ActiveConnection equal to NULL to disconnect.)</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0d6b3231899347c0ade072e166ceb1d1" id="tgt6" class="tgtSentence">We will use a disconnected Recordset later in this section when we discuss Recordset persistence to address a scenario in which we need to have the data in a Recordset available to an application while the client computer is not connected to a network.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">One of the most powerful features found in ADO is the capability to open a client-side Recordset from a data source and then disconnect the Recordset from the data source.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Once the Recordset has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> You can continue to view and edit the data in the Recordset while it is disconnected and later reconnect to the data source and send your updates in batch mode.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">To disconnect a Recordset, open it with a cursor location of adUseClient, and then set the ActiveConnection property equal to Nothing.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> (C++ users should set the ActiveConnection equal to NULL to disconnect.)</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">We will use a disconnected Recordset later in this section when we discuss Recordset persistence to address a scenario in which we need to have the data in a Recordset available to an application while the client computer is not connected to a network.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
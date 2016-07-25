---
title: "What is a Lock?"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f8989555-28c6-4c17-9bf8-7f44a8a5c407
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
# What is a Lock?
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ad57c33ce4854f7f0fa898a93ec84416" id="tgt1" class="tgtSentence">Locking is the process by which a DBMS restricts access to a row in a multi-user environment.</caps:sentence>
          <caps:sentence sentenceid="f91c79dd2dde557bf970c7164884e8a8" id="tgt2" class="tgtSentence"> When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released.</caps:sentence>
          <caps:sentence sentenceid="d8609697c5e15eea8c7e540823a33fc3" id="tgt3" class="tgtSentence"> This ensures that two users cannot simultaneously update the same column in a row.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="89e5c3dec56c7f9d5dd150318fea3b4f" id="tgt4" class="tgtSentence">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity.</caps:sentence>
          <caps:sentence sentenceid="e7ec04e546d261ffadd03d6ded32adb1" id="tgt5" class="tgtSentence"> In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0ba6a00f66cbe8599b21b9845d4a2c10" id="tgt6" class="tgtSentence">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="61cac66b1efaafb7a8119e33fb950027" id="tgt7" class="tgtSentence">Set the <legacyBold>LockType</legacyBold> property before opening a <legacyBold>Recordset</legacyBold> to specify what type of locking the provider should use when opening it.</caps:sentence>
          <caps:sentence sentenceid="1d326d701a2acb3a589e54fc01c36f78" id="tgt8" class="tgtSentence"> Read the property to return the type of locking in use on an open <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="d0dcae7612a5d567f68f718a11f1f963" id="tgt9" class="tgtSentence">Providers might not support all lock types.</caps:sentence>
          <caps:sentence sentenceid="8940e372a25502dc4c78273411641a85" id="tgt10" class="tgtSentence"> If a provider cannot support the requested <legacyBold>LockType</legacyBold> setting, it will substitute another type of locking.</caps:sentence>
          <caps:sentence sentenceid="1f539ebd4569bd5f952fafccaaeb5feb" id="tgt11" class="tgtSentence"> To determine the actual locking functionality available in a <legacyBold>Recordset</legacyBold> object, use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method with <legacyBold>adUpdate</legacyBold> and <legacyBold>adUpdateBatch</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="33dad31d77905f1e54586737b7d72630" id="tgt12" class="tgtSentence">The <legacyBold>adLockPessimistic</legacyBold> setting is not supported if the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient.</legacyBold> If an unsupported value is set, no error will result; the closest supported <legacyBold>LockType</legacyBold> will be used instead.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="27507c7f4fff0f0d93e3ed3405942c64" id="tgt13" class="tgtSentence">The <legacyBold>LockType</legacyBold> property is read/write when the <legacyBold>Recordset</legacyBold> is closed, and read-only when it is open.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt14" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="7e22b31ff242aaa845c684a451a9e185" id="tgt15" class="tgtSentence">             <legacyLink xlink:href="12a978c0-b8a0-4ef0-87f0-a43c13659272">Types of Locks</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Locking is the process by which a DBMS restricts access to a row in a multi-user environment.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This ensures that two users cannot simultaneously update the same column in a row.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">Set the <legacyBold>LockType</legacyBold> property before opening a <legacyBold>Recordset</legacyBold> to specify what type of locking the provider should use when opening it.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Read the property to return the type of locking in use on an open <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">Providers might not support all lock types.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> If a provider cannot support the requested <legacyBold>LockType</legacyBold> setting, it will substitute another type of locking.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> To determine the actual locking functionality available in a <legacyBold>Recordset</legacyBold> object, use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method with <legacyBold>adUpdate</legacyBold> and <legacyBold>adUpdateBatch</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">The <legacyBold>adLockPessimistic</legacyBold> setting is not supported if the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient.</legacyBold> If an unsupported value is set, no error will result; the closest supported <legacyBold>LockType</legacyBold> will be used instead.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">The <legacyBold>LockType</legacyBold> property is read/write when the <legacyBold>Recordset</legacyBold> is closed, and read-only when it is open.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">             <legacyLink xlink:href="12a978c0-b8a0-4ef0-87f0-a43c13659272">Types of Locks</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
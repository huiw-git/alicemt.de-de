---
title: "MarshalOptions Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 390c8abf-133e-40da-8b99-8f748a983e4f
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
# MarshalOptions Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="94f67b35b7851bf26d3aa39d264fce11" id="tgt1" class="tgtSentence">Indicates which records of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> are to be marshaled back to the server.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings And Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ad77ac32c3106e8370e2c9f2b1881893" id="tgt3" class="tgtSentence">Sets or returns a <legacyLink xlink:href="4013075d-dbea-4bbc-a6f4-c345a55c5633">MarshalOptionsEnum</legacyLink> value.</caps:sentence>
            <caps:sentence sentenceid="aaa5c6ffd1cde7d5357c59f272f7f1cb" id="tgt4" class="tgtSentence"> The default value is <legacyBold>adMarshalAll</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="5fc719c0fc6897938a8def8745535606" id="tgt5" class="tgtSentence">When using a client-side <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</caps:sentence>
            <caps:sentence sentenceid="d2e494170943de5ebce3850c5d2b352c" id="tgt6" class="tgtSentence"> Setting the <legacyBold>MarshalOptions</legacyBold> property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="c05c053cbf9712be02ee73af2db146e5" id="tgt7" class="tgtSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   This property is used only on a client-side <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ae576b2c-65aa-4838-872a-85e618806dc8">Visual Basic Example</link>
        <link xlink:href="a3b6fc09-ce21-450d-9063-bac505208d31">Visual C++ Example</link>
        <link xlink:href="9475c5f9-3a63-42cb-818c-4268e938a25c">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates which records of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> are to be marshaled back to the server.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings And Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyLink xlink:href="4013075d-dbea-4bbc-a6f4-c345a55c5633">MarshalOptionsEnum</legacyLink> value.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>adMarshalAll</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">When using a client-side <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Setting the <legacyBold>MarshalOptions</legacyBold> property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src7" class="srcSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   This property is used only on a client-side <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ae576b2c-65aa-4838-872a-85e618806dc8">Visual Basic Example</link>
        <link xlink:href="a3b6fc09-ce21-450d-9063-bac505208d31">Visual C++ Example</link>
        <link xlink:href="9475c5f9-3a63-42cb-818c-4268e938a25c">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
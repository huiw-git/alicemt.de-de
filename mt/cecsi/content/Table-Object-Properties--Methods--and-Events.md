---
title: "Table Object Properties, Methods, and Events"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 140d1517-6f0c-4fc9-9deb-9658982d88ed
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
# Table Object Properties, Methods, and Events
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="61ae1f92e68853d74174003a3c41b9e0" id="tgt1" class="tgtSentence">Properties/Collections</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b7e076faaf3289b08a413d6d0db41f88" id="tgt2" class="tgtSentence">
              <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f1eab7dbce53610ea16c04ed7a36b949" id="tgt3" class="tgtSentence">
              <link xlink:href="2bf4b00d-045c-444e-8af7-8af6297ed418">DateCreated Property</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9af7e3ea3a5eab80c6596ba1e72c9d7d" id="tgt4" class="tgtSentence">
              <link xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified Property</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a99a21cda3cfce81b384eb3617dd6367" id="tgt5" class="tgtSentence">
              <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="34370f550ec9aa9c29f01e47c0a3f5d6" id="tgt6" class="tgtSentence">
              <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7d130a37507f0f94486ed8feee49e62c" id="tgt7" class="tgtSentence">
              <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="99667976129f6fe6cf5c26af90961757" id="tgt8" class="tgtSentence">
              <link xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">ParentCatalog Property</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7327a3765f36800d418cd63c220a0df3" id="tgt9" class="tgtSentence">
              <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="196582e42bbf70b6df7adc7460f9befa" id="tgt10" class="tgtSentence">
              <link xlink:href="7b6e14bb-fb69-4d74-aaca-f5d380f4d887">Type Property (Table)</link>       </caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt11" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt12" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt13" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt14" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Properties/Collections</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">
              <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">
              <link xlink:href="2bf4b00d-045c-444e-8af7-8af6297ed418">DateCreated Property</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">
              <link xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified Property</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">
              <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">
              <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">
              <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">
              <link xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">ParentCatalog Property</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">
              <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</link>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">
              <link xlink:href="7b6e14bb-fb69-4d74-aaca-f5d380f4d887">Type Property (Table)</link>       </caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
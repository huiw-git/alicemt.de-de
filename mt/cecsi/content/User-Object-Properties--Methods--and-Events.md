---
title: "User Object Properties, Methods, and Events"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: becd590c-0db7-485c-8bf4-fa3456e4ba20
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
# User Object Properties, Methods, and Events
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
            <caps:sentence sentenceid="50390ab866f4686c87452c6232dcac54" id="tgt2" class="tgtSentence">
              <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property</legacyLink>       </caps:sentence>
          </para>
          <para>
            <legacyLink xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">
              <caps:sentence sentenceid="28ca5a0fd177325fe14e450d7867e314" id="tgt3" class="tgtSentence">ParentCatalog Property (ADOX)</caps:sentence>
            </legacyLink>
          </para>
          <para>
            <caps:sentence sentenceid="ed223f80e7cc015f000c257e3f65f03c" id="tgt4" class="tgtSentence">
              <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</legacyLink>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d533a67bac44c3f0d6b109b183bec388" id="tgt5" class="tgtSentence">
              <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</legacyLink>       </caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt6" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f566cf3bfce96040086e28d2740e8e9b" id="tgt7" class="tgtSentence">
              <legacyLink xlink:href="d187fbc6-5fac-4abb-803d-bf344dcf0302">ChangePassword Method</legacyLink>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="60a9b4eaefe70fb687eb39f30425dac6" id="tgt8" class="tgtSentence">
              <legacyLink xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions Method</legacyLink>       </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="05436e3a2d7b6293ae15c7c6272b4632" id="tgt9" class="tgtSentence">
              <legacyLink xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions Method</legacyLink>       </caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt10" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt11" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object</link>
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
              <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property</legacyLink>       </caps:sentence>
          </para>
          <para>
            <legacyLink xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">
              <caps:sentence id="src3" class="srcSentence">ParentCatalog Property (ADOX)</caps:sentence>
            </legacyLink>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">
              <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</legacyLink>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">
              <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</legacyLink>       </caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">
              <legacyLink xlink:href="d187fbc6-5fac-4abb-803d-bf344dcf0302">ChangePassword Method</legacyLink>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">
              <legacyLink xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions Method</legacyLink>       </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">
              <legacyLink xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions Method</legacyLink>       </caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
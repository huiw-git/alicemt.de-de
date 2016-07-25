---
title: "Views Collection (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a55d380c-2b7b-4b57-af74-8ba0b3de0db9
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
# Views Collection (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="83e0c0e213751e34c2f476d33ceddd23" id="tgt1" class="tgtSentence">Contains all <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> objects of a catalog.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d6e8472ba36553a448a209030b9db9e5" id="tgt2" class="tgtSentence">The <legacyLink xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append</legacyLink> method for a <legacyBold>Views</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt3" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="9caa5ee81a602e5b79b18480c3394757" id="tgt4" class="tgtSentence">Add a new view to the collection with the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ed0be1c652e041a462a56d678a7a9845" id="tgt5" class="tgtSentence">The remaining properties and methods are standard to ADO collections.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt6" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="01a4f10f603c29d8b8761556f066c2fe" id="tgt7" class="tgtSentence">Access a view in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6851386ed91d914ab23562d5c21f0152" id="tgt8" class="tgtSentence">Return the number of views contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2625860a53b99e9b94d4174a0037777a" id="tgt9" class="tgtSentence">Remove a view from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="918e7bfcf1fb8892b265d13bf57519fd" id="tgt10" class="tgtSentence">Update the objects in the collection to reflect the current database schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt11" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="04e119a4-39e1-45fe-8e39-c9b9afbfeb27">
                  <caps:sentence sentenceid="dfc788f9b014fac923c076990299fa76" id="tgt12" class="tgtSentence">Views Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
        <link xlink:href="cdad2d66-6ade-40dc-9e74-e40cfa9bc127">Views Refresh Method Example (VB)</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> objects of a catalog.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <legacyLink xlink:href="6070fd58-3237-4c77-a966-5b39ce5d57e4">Append</legacyLink> method for a <legacyBold>Views</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Add a new view to the collection with the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src5" class="srcSentence">The remaining properties and methods are standard to ADO collections.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Access a view in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Return the number of views contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Remove a view from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Update the objects in the collection to reflect the current database schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src11" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="04e119a4-39e1-45fe-8e39-c9b9afbfeb27">
                  <caps:sentence id="src12" class="srcSentence">Views Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
        <link xlink:href="cdad2d66-6ade-40dc-9e74-e40cfa9bc127">Views Refresh Method Example (VB)</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
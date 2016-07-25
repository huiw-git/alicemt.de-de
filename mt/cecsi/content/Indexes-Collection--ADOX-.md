---
title: "Indexes Collection (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 184cf536-455c-42be-bf1c-a5c25bade961
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
# Indexes Collection (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f5fae9a1b2f6d8d5b56e055c638513c0" id="tgt1" class="tgtSentence">Contains all <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink> objects of a table.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="77bfa8f64146141c79c7c9e19910a19a" id="tgt2" class="tgtSentence">The <legacyLink xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append</legacyLink> method for an <legacyBold>Indexes</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt3" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f5c252d514015c34fe9a7916d4d144a5" id="tgt4" class="tgtSentence">Add a new index to the collection with the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
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
                <caps:sentence sentenceid="363c98506e55f5fc4f2325ead2045e60" id="tgt7" class="tgtSentence">Access an index in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dd8faf07e2e1c4d08097efad60f1a23a" id="tgt8" class="tgtSentence">Return the number of indexes contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed3a079840f74b4c9cea7ddf20b00fac" id="tgt9" class="tgtSentence">Remove an index from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
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
                <legacyLink xlink:href="b27b5c37-3db2-4831-a447-ee6442e24d87">
                  <caps:sentence sentenceid="a62365ee79598f598f11842cb7723013" id="tgt12" class="tgtSentence">Indexes Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="50f87e27-1bf9-427c-9b1d-704a672434d2">Indexes Append Method Example (VB)</link>
        <link xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink> objects of a table.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <legacyLink xlink:href="6695769f-275b-4b70-81bd-1a5f7d74926c">Append</legacyLink> method for an <legacyBold>Indexes</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Add a new index to the collection with the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
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
                <caps:sentence id="src7" class="srcSentence">Access an index in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Return the number of indexes contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Remove an index from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
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
                <legacyLink xlink:href="b27b5c37-3db2-4831-a447-ee6442e24d87">
                  <caps:sentence id="src12" class="srcSentence">Indexes Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="50f87e27-1bf9-427c-9b1d-704a672434d2">Indexes Append Method Example (VB)</link>
        <link xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "OriginalValue Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac
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
# OriginalValue Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b118309edce7fbe2b295b59148bc0453" id="tgt1" class="tgtSentence">Indicates the value of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> that existed in the record before any changes were made.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="492af170a4038ae3c6d2445c7ee89eb7" id="tgt3" class="tgtSentence">Returns a <legacyBold>Variant</legacyBold> value that represents the value of a field prior to any change.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7a2fb1e4cf44f5feb3360a6c6018c742" id="tgt4" class="tgtSentence">Use the <legacyBold>OriginalValue</legacyBold> property to return the original field value for a field from the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="28dd28d167f31095aa1cbb6b60c7b6b2" id="tgt5" class="tgtSentence">In <legacyItalic>immediate update mode</legacyItalic> (in which the provider writes changes to the underlying data source after you call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method), the <legacyBold>OriginalValue</legacyBold> property returns the field value that existed prior to any changes (that is, since the last <legacyBold>Update</legacyBold> method call).</caps:sentence>
            <caps:sentence sentenceid="ab655b76a17b4f67de7485131eec71a4" id="tgt6" class="tgtSentence"> This is the same value that the <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method uses to replace the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5cedbceafe8dee7c4e2c217d9f94feff" id="tgt7" class="tgtSentence">In <legacyItalic>batch update mode</legacyItalic> (in which the provider caches multiple changes and writes them to the underlying data source only when you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method), the <legacyBold>OriginalValue</legacyBold> property returns the field value that existed prior to any changes (that is, since the last <legacyBold>UpdateBatch</legacyBold> method call).</caps:sentence>
            <caps:sentence sentenceid="f4f3b47cc5c7d83533601f9283ff5f08" id="tgt8" class="tgtSentence"> This is the same value that the <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> method uses to replace the <legacyBold>Value</legacyBold> property.</caps:sentence>
            <caps:sentence sentenceid="2c977e9b4726d7e21f0a42e1ecac68f2" id="tgt9" class="tgtSentence"> When you use this property with the <legacyLink xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue</legacyLink> property, you can resolve conflicts that arise from batch updates.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="de17f0f24b49f8364187891f8550ffbb" id="tgt10" class="tgtSentence">Record</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bae196e53554467284bb9209da703495" id="tgt11" class="tgtSentence">For <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> objects, the <legacyBold>OriginalValue</legacyBold> property will be empty for fields added before <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> is called.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1750804b-d7ef-47d6-8d73-1f51fa1cbe4a">Visual Basic Example</link>
        <link xlink:href="c5762ad2-f43b-453d-b44a-9c70210eb00f">Visual C++ Example</link>
        <link xlink:href="cfe62974-f768-437f-87c5-8106c4e23ad0">Visual J++ Example</link>
        <link xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the value of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> that existed in the record before any changes were made.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyBold>Variant</legacyBold> value that represents the value of a field prior to any change.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>OriginalValue</legacyBold> property to return the original field value for a field from the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">In <legacyItalic>immediate update mode</legacyItalic> (in which the provider writes changes to the underlying data source after you call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method), the <legacyBold>OriginalValue</legacyBold> property returns the field value that existed prior to any changes (that is, since the last <legacyBold>Update</legacyBold> method call).</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> This is the same value that the <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method uses to replace the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">In <legacyItalic>batch update mode</legacyItalic> (in which the provider caches multiple changes and writes them to the underlying data source only when you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method), the <legacyBold>OriginalValue</legacyBold> property returns the field value that existed prior to any changes (that is, since the last <legacyBold>UpdateBatch</legacyBold> method call).</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> This is the same value that the <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> method uses to replace the <legacyBold>Value</legacyBold> property.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> When you use this property with the <legacyLink xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue</legacyLink> property, you can resolve conflicts that arise from batch updates.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Record</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">For <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> objects, the <legacyBold>OriginalValue</legacyBold> property will be empty for fields added before <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> is called.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1750804b-d7ef-47d6-8d73-1f51fa1cbe4a">Visual Basic Example</link>
        <link xlink:href="c5762ad2-f43b-453d-b44a-9c70210eb00f">Visual C++ Example</link>
        <link xlink:href="cfe62974-f768-437f-87c5-8106c4e23ad0">Visual J++ Example</link>
        <link xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
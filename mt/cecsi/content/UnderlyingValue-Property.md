---
title: "UnderlyingValue Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 00a0c8b8-8b63-433f-95b8-020ab05874a0
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
# UnderlyingValue Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="47c2651b5dae1aff200f1a570f0f7147" id="tgt1" class="tgtSentence">Indicates the current value of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object in the database.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f9cfeec320275e0317144083094fcd0c" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Variant</languageKeyword> value that indicates the value of the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="07a4a3f15d2b8fc8b4bd028883c56728" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>UnderlyingValue</unmanagedCodeEntityReference> property to return the current field value from the database.</caps:sentence>
            <caps:sentence sentenceid="7e51e8de5e9080c0869f7de740e6e29c" id="tgt5" class="tgtSentence"> The field value in the <unmanagedCodeEntityReference>UnderlyingValue</unmanagedCodeEntityReference> property is the value that is visible to your transaction and may be the result of a recent update by another transaction.</caps:sentence>
            <caps:sentence sentenceid="a804e4675b268967b4399d488c0a408a" id="tgt6" class="tgtSentence"> This may differ from the <legacyLink xlink:href="6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac">OriginalValue</legacyLink> property, which reflects the value that was originally returned to the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4e76d1bcd9b3dbd8be0f9722f615e45c" id="tgt7" class="tgtSentence">This is similar to using the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method, but the <unmanagedCodeEntityReference>UnderlyingValue</unmanagedCodeEntityReference> property returns only the value for a specific field from the current record.</caps:sentence>
            <caps:sentence sentenceid="df596adb334a11a5f8e2c432dc743368" id="tgt8" class="tgtSentence"> This is the same value that the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method uses to replace the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="70ab20b91d4cc6bdc35f9886b6e66f23" id="tgt9" class="tgtSentence">When you use this property with the <unmanagedCodeEntityReference>OriginalValue</unmanagedCodeEntityReference> property, you can resolve conflicts that arise from batch updates.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="de17f0f24b49f8364187891f8550ffbb" id="tgt10" class="tgtSentence">Record</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b9013edf29ed1bbf31ec07d3cc4f51af" id="tgt11" class="tgtSentence">For <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> objects, this property will be empty for fields added before <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> is called.</caps:sentence>
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
        <link xlink:href="6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac">OriginalValue Property</link>
        <link xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the current value of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object in the database.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Variant</languageKeyword> value that indicates the value of the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>UnderlyingValue</unmanagedCodeEntityReference> property to return the current field value from the database.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The field value in the <unmanagedCodeEntityReference>UnderlyingValue</unmanagedCodeEntityReference> property is the value that is visible to your transaction and may be the result of a recent update by another transaction.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> This may differ from the <legacyLink xlink:href="6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac">OriginalValue</legacyLink> property, which reflects the value that was originally returned to the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">This is similar to using the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method, but the <unmanagedCodeEntityReference>UnderlyingValue</unmanagedCodeEntityReference> property returns only the value for a specific field from the current record.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> This is the same value that the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method uses to replace the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">When you use this property with the <unmanagedCodeEntityReference>OriginalValue</unmanagedCodeEntityReference> property, you can resolve conflicts that arise from batch updates.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Record</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">For <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> objects, this property will be empty for fields added before <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> is called.</caps:sentence>
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
        <link xlink:href="6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac">OriginalValue Property</link>
        <link xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
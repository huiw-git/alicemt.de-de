---
title: "ActiveCommand Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: fb4088d5-5968-42d6-aeaa-3955046bb4da
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
# ActiveCommand Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="270096d4856fdca6bd8472c44e3409a9" id="tgt1" class="tgtSentence">Indicates the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object that created the associated <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4e78185be3fc93ee93a0c916a38d3b55" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Variant</languageKeyword> that contains a <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="79aa835488fc134e3c0b2bff8da3c128" id="tgt4" class="tgtSentence"> Default is a null object reference.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="56735e7ccb56cb3dacaf1fddb4f23816" id="tgt5" class="tgtSentence">The <legacyBold>ActiveCommand</legacyBold> property is read-only.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0f8aae64c3dca72b03a86fc01a46ed91" id="tgt6" class="tgtSentence">If a <legacyBold>Command</legacyBold> object was not used to create the current <legacyBold>Recordset</legacyBold>, then a <legacyBold>Null</legacyBold> object reference is returned.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b395868e96052922e0da29ebfe283f0e" id="tgt7" class="tgtSentence">Use this property to find the associated <legacyBold>Command</legacyBold> object when you are given only the resulting <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
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
        <link xlink:href="23b06499-62df-4f46-88eb-6da392f9b456">Visual Basic Example</link>
        <link xlink:href="be09e2af-ba31-4168-8ccd-2461bb24e49a">JScript Example</link>
        <link xlink:href="8269ea29-912a-4d20-9360-f48b3746081f">VC++Example</link>
        <link xlink:href="f28637c7-05ab-482d-b1ce-bbfc41228050">VJ++Example</link>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object that created the associated <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Variant</languageKeyword> that contains a <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Default is a null object reference.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The <legacyBold>ActiveCommand</legacyBold> property is read-only.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">If a <legacyBold>Command</legacyBold> object was not used to create the current <legacyBold>Recordset</legacyBold>, then a <legacyBold>Null</legacyBold> object reference is returned.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">Use this property to find the associated <legacyBold>Command</legacyBold> object when you are given only the resulting <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
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
        <link xlink:href="23b06499-62df-4f46-88eb-6da392f9b456">Visual Basic Example</link>
        <link xlink:href="be09e2af-ba31-4168-8ccd-2461bb24e49a">JScript Example</link>
        <link xlink:href="8269ea29-912a-4d20-9360-f48b3746081f">VC++Example</link>
        <link xlink:href="f28637c7-05ab-482d-b1ce-bbfc41228050">VJ++Example</link>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
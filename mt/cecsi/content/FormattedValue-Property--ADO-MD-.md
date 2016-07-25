---
title: "FormattedValue Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 5c06451e-06ec-4da6-9a87-2d043469248a
caps.latest.revision: 12
caps.handback.revision: 12
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
# FormattedValue Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="97339775010cb8865f31a5484d08f596" id="tgt1" class="tgtSentence">Indicates the formatted display of a <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">cell</legacyLink> value.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="909426022f13cfc0404ae7793d8957d9" id="tgt3" class="tgtSentence">Returns a <languageKeyword>String</languageKeyword> and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="add546ed451440f5487cf1ba8283eb6a" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>FormattedValue</unmanagedCodeEntityReference> property to obtain the formatted display value of the <legacyLink xlink:href="70dc5cff-0b05-456d-b86b-2686fe4e7ce6">Value</legacyLink> property of a <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="891eba6680a70798c52edcd55efd36d1" id="tgt5" class="tgtSentence"> For example, if the value of a cell was 1056.87, and this value represented a dollar amount, <unmanagedCodeEntityReference>FormattedValue</unmanagedCodeEntityReference> would be $1,056.87.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt6" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="70dc5cff-0b05-456d-b86b-2686fe4e7ce6">Value Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the formatted display of a <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">cell</legacyLink> value.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>String</languageKeyword> and is read-only.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>FormattedValue</unmanagedCodeEntityReference> property to obtain the formatted display value of the <legacyLink xlink:href="70dc5cff-0b05-456d-b86b-2686fe4e7ce6">Value</legacyLink> property of a <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink> object.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For example, if the value of a cell was 1056.87, and this value represented a dollar amount, <unmanagedCodeEntityReference>FormattedValue</unmanagedCodeEntityReference> would be $1,056.87.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="70dc5cff-0b05-456d-b86b-2686fe4e7ce6">Value Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
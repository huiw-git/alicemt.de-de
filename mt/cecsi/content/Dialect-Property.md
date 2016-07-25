---
title: "Dialect Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 329c3a71-ba88-4009-b04f-2f52195a5957
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
# Dialect Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2dfaf1788686e0aede44bc28501d8732" id="tgt1" class="tgtSentence">Indicates the dialect of the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> or <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream</legacyLink> properties.</caps:sentence>
          <caps:sentence sentenceid="b4530a0af3cbefb79bc8523bd143e26d" id="tgt2" class="tgtSentence"> The dialect defines the syntax and general rules that the provider uses to parse the string or stream.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt3" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="180efcdf4fac1732cb0cdb205050b60f" id="tgt4" class="tgtSentence">The <unmanagedCodeEntityReference>Dialect</unmanagedCodeEntityReference> property contains a valid GUID that represents the dialect of the command text or stream.</caps:sentence>
            <caps:sentence sentenceid="68a1196017fb902460d043ca3825c60c" id="tgt5" class="tgtSentence"> The default value for this property is {C8B521FB-5CF3-11CE-ADE5-00AA0044773D}, which indicates that the provider should choose how to interpret the command text or stream.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e96e6f29c81fcf382dd778643a3834a9" id="tgt6" class="tgtSentence">ADO does not query the provider when the user reads the value of this property; it returns a string representation of the value currently stored in the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="565d78b58179091d3d2b7a3127b7e1c7" id="tgt7" class="tgtSentence">When the user sets the <unmanagedCodeEntityReference>Dialect</unmanagedCodeEntityReference> property, ADO validates the GUID and raises an error if the value supplied is not a valid GUID.</caps:sentence>
            <caps:sentence sentenceid="67daddf49cccae1835bb96dc94b6c611" id="tgt8" class="tgtSentence"> See the documentation for your provider to determine the GUID values supported by the <unmanagedCodeEntityReference>Dialect</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the dialect of the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> or <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream</legacyLink> properties.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The dialect defines the syntax and general rules that the provider uses to parse the string or stream.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <unmanagedCodeEntityReference>Dialect</unmanagedCodeEntityReference> property contains a valid GUID that represents the dialect of the command text or stream.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The default value for this property is {C8B521FB-5CF3-11CE-ADE5-00AA0044773D}, which indicates that the provider should choose how to interpret the command text or stream.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">ADO does not query the provider when the user reads the value of this property; it returns a string representation of the value currently stored in the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">When the user sets the <unmanagedCodeEntityReference>Dialect</unmanagedCodeEntityReference> property, ADO validates the GUID and raises an error if the value supplied is not a valid GUID.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> See the documentation for your provider to determine the GUID values supported by the <unmanagedCodeEntityReference>Dialect</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
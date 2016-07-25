---
title: "NamedParameters Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 42409387-026c-435f-a9b1-bf4167095875
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
# NamedParameters Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="57077ff980a40a6a5ce7c42c9b74e1c2" id="tgt1" class="tgtSentence">Indicates whether parameter names should be passed to the provider.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9bff1932e4d1d7911cad3f198152b4a3" id="tgt2" class="tgtSentence">When this property is true, ADO passes the value of the <unmanagedCodeEntityReference>Name</unmanagedCodeEntityReference> property of each parameter in the <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> collection for the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="7ddeef42024cecd19e1b2b0912a456a0" id="tgt3" class="tgtSentence"> The provider uses a parameter name to match parameters in the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> properties.</caps:sentence>
            <caps:sentence sentenceid="828ac83e59fa5eb684660e3df3a37c31" id="tgt4" class="tgtSentence"> If this property is false (the default), parameter names are ignored and the provider uses the order of parameters to match values to parameters in the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> properties.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt5" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object (ADO)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
        <link xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream Property</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates whether parameter names should be passed to the provider.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">When this property is true, ADO passes the value of the <unmanagedCodeEntityReference>Name</unmanagedCodeEntityReference> property of each parameter in the <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> collection for the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</legacyLink>.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The provider uses a parameter name to match parameters in the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> properties.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> If this property is false (the default), parameter names are ignored and the provider uses the order of parameters to match values to parameters in the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> properties.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object (ADO)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
        <link xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream Property</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
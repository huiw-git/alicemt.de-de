---
title: "Direction Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d5732578-3434-4dcd-a9f7-db1abd1b3b94
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
# Direction Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bd84f49e508066d71688153d4954e305" id="tgt1" class="tgtSentence">Indicates whether the <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">parameter</legacyLink> represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="46e691f8d35deeb54354d6780773a795" id="tgt3" class="tgtSentence">Sets or returns a <legacyLink xlink:href="c66aa6e6-d4f0-4f0f-9640-e08ae6cfdef3">ParameterDirectionEnum</legacyLink> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="f697ccdc2ba8b55f5add49998f7a8156" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>Direction</unmanagedCodeEntityReference> property to specify how a parameter is passed to or from a procedure.</caps:sentence>
            <caps:sentence sentenceid="c9517b07b07cd2b9077cb9ccb6bde8a2" id="tgt5" class="tgtSentence"> The <unmanagedCodeEntityReference>Direction</unmanagedCodeEntityReference> property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="eb1051a5bcda8a487f1a2a99d39061ee" id="tgt6" class="tgtSentence">Not all providers can determine the direction of parameters in their stored procedures.</caps:sentence>
            <caps:sentence sentenceid="78e1607e2d404c059c75e5a7c636e104" id="tgt7" class="tgtSentence"> In these cases, you must set the <unmanagedCodeEntityReference>Direction</unmanagedCodeEntityReference> property before you execute the query.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dade4531-0bcc-4a52-8f86-b110ba2a3f9d">Visual Basic Example</link>
        <link xlink:href="0d9917c4-9ef0-4d7a-b4ce-4f1fa6ce1817">Visual C++ Example</link>
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++ Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates whether the <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">parameter</legacyLink> represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyLink xlink:href="c66aa6e6-d4f0-4f0f-9640-e08ae6cfdef3">ParameterDirectionEnum</legacyLink> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>Direction</unmanagedCodeEntityReference> property to specify how a parameter is passed to or from a procedure.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The <unmanagedCodeEntityReference>Direction</unmanagedCodeEntityReference> property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">Not all providers can determine the direction of parameters in their stored procedures.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> In these cases, you must set the <unmanagedCodeEntityReference>Direction</unmanagedCodeEntityReference> property before you execute the query.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dade4531-0bcc-4a52-8f86-b110ba2a3f9d">Visual Basic Example</link>
        <link xlink:href="0d9917c4-9ef0-4d7a-b4ce-4f1fa6ce1817">Visual C++ Example</link>
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++ Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
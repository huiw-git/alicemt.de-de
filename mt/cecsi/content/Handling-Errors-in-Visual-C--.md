---
title: "Handling Errors in Visual C++"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b7576f07-020a-45f7-9e79-b5756f33f7ab
caps.latest.revision: 4
caps.handback.revision: 4
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
# Handling Errors in Visual C++
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0155031c9ca858577fe652e05954149c" id="tgt1" class="tgtSentence">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</caps:sentence>
          <caps:sentence sentenceid="0e145ddbe6bf9890ff1a651ebdd44fd9" id="tgt2" class="tgtSentence"> The #import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</caps:sentence>
          <caps:sentence sentenceid="ca49b10f2f78cb6798ce4f791c575399" id="tgt3" class="tgtSentence"> If the HRESULT indicates failure, the wrapper code throws a COM error by calling _com_issue_errorex() with the HRESULT return code as an argument.</caps:sentence>
          <caps:sentence sentenceid="e474c64e5bc7b3a17263051af3f48410" id="tgt4" class="tgtSentence"> COM error objects can be caught in a <legacyBold>try-catch</legacyBold> block.</caps:sentence>
          <caps:sentence sentenceid="db403a5f87b1d3fe79dc513296c0854a" id="tgt5" class="tgtSentence"> (For efficiency's sake, catch a reference to a _com_error object.)</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7f22d5d63bd849bc1746a6342266957c" id="tgt6" class="tgtSentence">Remember, these are ADO errors: they result from the ADO operation failing.</caps:sentence>
          <caps:sentence sentenceid="4a2f2917fa9995bf636d248699682a3b" id="tgt7" class="tgtSentence"> Errors returned by the underlying provider appear as <legacyBold>Error</legacyBold> objects in the <legacyBold>Connection</legacyBold> object's <legacyBold>Errors</legacyBold> collection.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="045a5b612ee10a3a858a44917674c8c3" id="tgt8" class="tgtSentence">The #import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</caps:sentence>
          <caps:sentence sentenceid="c58cdca5a046eb27aeabd01e87c98590" id="tgt9" class="tgtSentence"> However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</caps:sentence>
          <caps:sentence sentenceid="436a6f37470482cb9650077811e9d4ee" id="tgt10" class="tgtSentence"> See the topic Visual C++® Extensions for examples.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The #import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> If the HRESULT indicates failure, the wrapper code throws a COM error by calling _com_issue_errorex() with the HRESULT return code as an argument.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> COM error objects can be caught in a <legacyBold>try-catch</legacyBold> block.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> (For efficiency's sake, catch a reference to a _com_error object.)</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">Remember, these are ADO errors: they result from the ADO operation failing.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Errors returned by the underlying provider appear as <legacyBold>Error</legacyBold> objects in the <legacyBold>Connection</legacyBold> object's <legacyBold>Errors</legacyBold> collection.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">The #import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> See the topic Visual C++® Extensions for examples.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
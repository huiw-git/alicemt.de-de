---
title: "XML Security Considerations"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fadbd38e-6e7b-4b81-96ea-85169c664374
caps.latest.revision: 2
caps.handback.revision: 2
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
# XML Security Considerations
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c8bc29d809acadaf8c02fe2f3caa9d48" id="tgt1" class="tgtSentence">The ADO Save and Open methods on the Recordset object are not considered safe operations to run in Internet Explorer.</caps:sentence>
          <caps:sentence sentenceid="ac9a8d68af65d52858d2dcf7d4ad6849" id="tgt2" class="tgtSentence"> Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="51ac4ae57d08ad3fde30f07fcab6e171" id="tgt3" class="tgtSentence">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones.</caps:sentence>
          <caps:sentence sentenceid="4419f8c807d1810593df1881a058574c" id="tgt4" class="tgtSentence"> Under that configuration, the Recordset cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded.</caps:sentence>
          <caps:sentence sentenceid="c72aca505000d98b1c0ad952907fff41" id="tgt5" class="tgtSentence"> Specifically, when running inside the browser host, a Recordset can be saved back to a file only if it is on the same server from which the page was downloaded.</caps:sentence>
          <caps:sentence sentenceid="3ae1c0602bbf3002e104c961ccdc5ae0" id="tgt6" class="tgtSentence"> Similarly, you can open a Recordset by loading it from a file only if that file is on the same server from which the page was downloaded.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The ADO Save and Open methods on the Recordset object are not considered safe operations to run in Internet Explorer.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Under that configuration, the Recordset cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Specifically, when running inside the browser host, a Recordset can be saved back to a file only if it is on the same server from which the page was downloaded.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Similarly, you can open a Recordset by loading it from a file only if that file is on the same server from which the page was downloaded.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
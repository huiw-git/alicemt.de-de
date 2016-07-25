---
title: "ADO/WFC Programming"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1fdfa42e-897e-4770-b320-ab3720adabcc
caps.latest.revision: 8
caps.handback.revision: 8
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
# ADO/WFC Programming
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f49b1b3de9dba00656340eec77faef43" id="tgt1" class="tgtSentence">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways.</caps:sentence>
          <caps:sentence sentenceid="516de57b076ec3e656b13c638a0d546f" id="tgt2" class="tgtSentence"> First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user.</caps:sentence>
          <caps:sentence sentenceid="6a37a08151aa77e1be2098d8b9bfe877" id="tgt3" class="tgtSentence"> To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant.</caps:sentence>
          <caps:sentence sentenceid="627ac3c1b9aa2a7ed402506ce0fe6be0" id="tgt4" class="tgtSentence"> ADO has also been extended to work with event notifications in the WFC framework.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e17da93c6ad64d770af3047f017d8c3e" id="tgt5" class="tgtSentence">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events.</caps:sentence>
          <caps:sentence sentenceid="43e30613e3256b8d3a1c8d49ed112ee0" id="tgt6" class="tgtSentence"> However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++.</caps:sentence>
          <caps:sentence sentenceid="56a25ad79a3cbfaa2f22c821631b7f05" id="tgt7" class="tgtSentence"> For that reason, ADO/WFC also provides accessor functions on the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object that take native Java data types instead of the variant data type.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e7f2cd351010cc92ce1907d7ff05a195" id="tgt8" class="tgtSentence">For more detailed information within the ADO documentation about ADO/WFC packages, see <legacyLink xlink:href="a14bbc36-87ec-409d-97b3-393b66b1b8e3">the ADO/WFC Syntax Index</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="94df0b449c5ac2a44758c21115c39c85" id="tgt9" class="tgtSentence">For related information within the Visual J++ documentation, see <externalLink><linkText>Converting Visual Basic ADO Examples to Visual J++</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=5684</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4dd533a894455ce57f51db4a9192cbac" id="tgt10" class="tgtSentence">Referencing the Library</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="05dc765669bae7783ac91f1cddd802b0" id="tgt11" class="tgtSentence">To import the ADO/WFC data classes into your project, include the following line in your code:</caps:sentence>
          </para>
          <code>import com.ms.wfc.data.*;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="a14bbc36-87ec-409d-97b3-393b66b1b8e3">ADO/WFC Syntax Index</link>
        <link xlink:href="f9737a65-4b2f-47fa-b026-1494dca158eb">Using ADO with the Java Type Library Wizard</link>
        <link xlink:href="2d7cb5b5-8307-49dd-b07e-c07069bb1626">Using ADO with the Microsoft SDK for Java</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> ADO has also been extended to work with event notifications in the WFC framework.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> For that reason, ADO/WFC also provides accessor functions on the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object that take native Java data types instead of the variant data type.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">For more detailed information within the ADO documentation about ADO/WFC packages, see <legacyLink xlink:href="a14bbc36-87ec-409d-97b3-393b66b1b8e3">the ADO/WFC Syntax Index</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">For related information within the Visual J++ documentation, see <externalLink><linkText>Converting Visual Basic ADO Examples to Visual J++</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=5684</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Referencing the Library</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">To import the ADO/WFC data classes into your project, include the following line in your code:</caps:sentence>
          </para>
          <code>import com.ms.wfc.data.*;</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="a14bbc36-87ec-409d-97b3-393b66b1b8e3">ADO/WFC Syntax Index</link>
        <link xlink:href="f9737a65-4b2f-47fa-b026-1494dca158eb">Using ADO with the Java Type Library Wizard</link>
        <link xlink:href="2d7cb5b5-8307-49dd-b07e-c07069bb1626">Using ADO with the Microsoft SDK for Java</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
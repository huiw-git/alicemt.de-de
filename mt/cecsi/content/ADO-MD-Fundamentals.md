---
title: "ADO MD Fundamentals"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f6a20d9f-c1ab-474c-b9f3-82277e2a126d
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
# ADO MD Fundamentals
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="955cca2cf12a66225a82a0b1490cf1b8" id="tgt1" class="tgtSentence">Microsoft® ActiveX® Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic®, Microsoft Visual C++®, and Microsoft Visual J++®.</caps:sentence>
          <caps:sentence sentenceid="2e54172e41686672d2c98453e93617c2" id="tgt2" class="tgtSentence"> ADO MD extends Microsoft ActiveX® Data Objects (ADO) to include objects specific to multidimensional data, such as the <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> and <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> objects.</caps:sentence>
          <caps:sentence sentenceid="116f1b45d36eda66d7c4d0b8fff295a4" id="tgt3" class="tgtSentence"> With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="cd160290e1d32ffaa8b313de55f9d429" id="tgt4" class="tgtSentence">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</caps:sentence>
          <caps:sentence sentenceid="3d97df013f6032d94e0405de28f29948" id="tgt5" class="tgtSentence"> To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</caps:sentence>
          <caps:sentence sentenceid="3b57e7fc34dac6fe45564802ad559546" id="tgt6" class="tgtSentence"> An MDP presents data in multidimensional views instead of tabular views, which is how a tabular data provider (TDP) presents data.</caps:sentence>
          <caps:sentence sentenceid="a7639850b2bd46c562aa0f542fa53eea" id="tgt7" class="tgtSentence"> Refer to the documentation for your OLAP OLE DB provider for more information about the specific syntax and behavior supported by your provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="eb7325e2319ed2f632ba8a023c3cd627" id="tgt8" class="tgtSentence">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</caps:sentence>
          <caps:sentence sentenceid="5cdfeb172966ef0004ac3679b4667057" id="tgt9" class="tgtSentence"> For more information, see the <legacyLink xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">ADO Programmer's Guide</legacyLink> and <externalLink><linkText>OLE DB for Online Analytical Processing (OLAP)</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms717005.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt10" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="34737229b59718873e1beaef699c1441" id="tgt11" class="tgtSentence">
                <legacyLink xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3bef3c9b66ce946e88fd556f257a7bfa" id="tgt12" class="tgtSentence">
                <legacyLink xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="292aa77a7d5fb7b369d564e7c65bd486" id="tgt13" class="tgtSentence">
                <legacyLink xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f0d0615a5425f8673c356429287cfa6b" id="tgt14" class="tgtSentence">
                <legacyLink xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">Microsoft ADO Programmer's Guide</link>
        <link xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">Microsoft ADOX Programmer's Reference</link>
        <link xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</link>
        <link xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</link>
        <link xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</link>
        <link xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Microsoft® ActiveX® Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic®, Microsoft Visual C++®, and Microsoft Visual J++®.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> ADO MD extends Microsoft ActiveX® Data Objects (ADO) to include objects specific to multidimensional data, such as the <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> and <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> objects.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> An MDP presents data in multidimensional views instead of tabular views, which is how a tabular data provider (TDP) presents data.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Refer to the documentation for your OLAP OLE DB provider for more information about the specific syntax and behavior supported by your provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> For more information, see the <legacyLink xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">ADO Programmer's Guide</legacyLink> and <externalLink><linkText>OLE DB for Online Analytical Processing (OLAP)</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms717005.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">
                <legacyLink xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">
                <legacyLink xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">
                <legacyLink xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">
                <legacyLink xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">Microsoft ADO Programmer's Guide</link>
        <link xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">Microsoft ADOX Programmer's Reference</link>
        <link xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</link>
        <link xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</link>
        <link xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</link>
        <link xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
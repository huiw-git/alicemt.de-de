---
title: "Referencing the ADO Libraries In a Visual C++ Application"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d3ea12ec-bca8-48c3-af57-ce14576108c9
caps.latest.revision: 11
caps.handback.revision: 11
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
# Referencing the ADO Libraries In a Visual C++ Application
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e113e7eda134428d3a7a504a9cc6a188" id="tgt1" class="tgtSentence">To use the latest version of ADO in a Visual C++ application, use the following <codeInline>#import</codeInline> directive:</caps:sentence>
        </para>
        <code>#import "msado15.dll" \
    no_namespace rename("EOF", "EndOfFile")</code>
        <para>
          <caps:sentence sentenceid="99175b18499da082d54d8b271ce9c02e" id="tgt2" class="tgtSentence">To use ADO MD or ADOX, you must import <legacyItalic>msadomd.dll</legacyItalic> or <legacyItalic>msadox.dll</legacyItalic>, by using the syntax above.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="60cca08b90e3076e13f8a399bbb8cffc" id="tgt3" class="tgtSentence">Backward Compatibility</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="04c696289d827a72f84c5f51397008dd" id="tgt4" class="tgtSentence">To use any earlier version of ADO, replace <legacyItalic>msado15.dll</legacyItalic> above with one of the following type libraries.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="64e9defdf49b1e184ab3359b62a5a355" id="tgt5" class="tgtSentence">             <legacyItalic>msado27.tlb</legacyItalic>, ADO 2.7 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="878bfb2ac6865b572b7f78c96562fc24" id="tgt6" class="tgtSentence">             <legacyItalic>msado26.tlb</legacyItalic>, ADO 2.6 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="111f81e2df0109431988e18db5eb7c04" id="tgt7" class="tgtSentence">             <legacyItalic>msado25.tlb</legacyItalic>, ADO 2.5 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d096f9037f2104e45d03bb1b8eac2623" id="tgt8" class="tgtSentence">             <legacyItalic>msado21.tlb</legacyItalic>, ADO 2.1 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f562f38f7d6b4b0e2729aac334317bad" id="tgt9" class="tgtSentence">             <legacyItalic>msado20.tlb</legacyItalic>, ADO 2.0 Type Library</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To use the latest version of ADO in a Visual C++ application, use the following <codeInline>#import</codeInline> directive:</caps:sentence>
        </para>
        <code>#import "msado15.dll" \
    no_namespace rename("EOF", "EndOfFile")</code>
        <para>
          <caps:sentence id="src2" class="srcSentence">To use ADO MD or ADOX, you must import <legacyItalic>msadomd.dll</legacyItalic> or <legacyItalic>msadox.dll</legacyItalic>, by using the syntax above.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Backward Compatibility</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">To use any earlier version of ADO, replace <legacyItalic>msado15.dll</legacyItalic> above with one of the following type libraries.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">             <legacyItalic>msado27.tlb</legacyItalic>, ADO 2.7 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">             <legacyItalic>msado26.tlb</legacyItalic>, ADO 2.6 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">             <legacyItalic>msado25.tlb</legacyItalic>, ADO 2.5 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">             <legacyItalic>msado21.tlb</legacyItalic>, ADO 2.1 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">             <legacyItalic>msado20.tlb</legacyItalic>, ADO 2.0 Type Library</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ADO Code Examples VBScript"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 78bb9a95-7ac4-44b6-818b-d1787f952ed7
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
# ADO Code Examples VBScript
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="13ebf988f7336e243e276a35a5d9f94e" id="tgt1" class="tgtSentence">Use the following code examples to learn about how to use the ADO methods when writing in Microsoft® Visual Basic® Scripting Edition (VBScript).</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="a3a4362505f29dd00933c3ddd2b474e7" id="tgt2" class="tgtSentence">Paste the entire code example, from beginning to end, into your code editor.</caps:sentence>
            <caps:sentence sentenceid="d0af02b2a7f5e8d60d6ca45d510c2f3c" id="tgt3" class="tgtSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt4" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="dcdcaf0a-b9b0-4d81-8728-43c38c4c853b">
                  <caps:sentence sentenceid="be47f651bc705168667f5910cbd944ff" id="tgt5" class="tgtSentence">AddNew Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="36b96e3d-8cb0-4b79-bd93-ea5e0eb5679f">
                  <caps:sentence sentenceid="98233d675f1c3557b68c1c30c51cd4aa" id="tgt6" class="tgtSentence">Clone Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="78935d6d-1c1a-4306-a83a-1763210c69f9">
                  <caps:sentence sentenceid="a1081a4b0daeafbe6e015654eb215e1c" id="tgt7" class="tgtSentence">Delete Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="3a7bbf07-2fca-4892-95f4-eec93f2d5e91">
                  <caps:sentence sentenceid="950be02f7ec05d72aa6fe9e540ad3f9b" id="tgt8" class="tgtSentence">Execute, Requery, and Clear Methods Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="29ec4b95-8986-4970-943f-3da3ecb207a2">
                  <caps:sentence sentenceid="ebcead8b7d4b86937f99e99e3c6a3637" id="tgt9" class="tgtSentence">Move Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="911aa1dd-2786-4f34-992c-bb2fbdabcbdf">
                  <caps:sentence sentenceid="dad759272f6bf83feb0c6195efaf3f3e" id="tgt10" class="tgtSentence">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="66eca011-e258-4d8f-bd67-e017bcf0871b">
                  <caps:sentence sentenceid="7ea73172574459dd2907faad892906f0" id="tgt11" class="tgtSentence">Open and Close Methods Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1152893e-b617-40f1-88b6-81e82e2234f1">ADO Code Examples in Microsoft Visual Basic</link>
        <link xlink:href="af30b764-398f-4918-aaa7-3952226cf544">ADO Code Examples in Microsoft Visual C++</link>
        <link xlink:href="d1c82f1a-cf78-4bd6-9ad4-1eb526e2c474">ADO Code Examples in Microsoft Visual J++</link>
        <link xlink:href="1582e411-55ac-40f0-bd3d-9a10654e4b67">Appendix D: ADO Samples</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the following code examples to learn about how to use the ADO methods when writing in Microsoft® Visual Basic® Scripting Edition (VBScript).</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src2" class="srcSentence">Paste the entire code example, from beginning to end, into your code editor.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="dcdcaf0a-b9b0-4d81-8728-43c38c4c853b">
                  <caps:sentence id="src5" class="srcSentence">AddNew Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="36b96e3d-8cb0-4b79-bd93-ea5e0eb5679f">
                  <caps:sentence id="src6" class="srcSentence">Clone Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="78935d6d-1c1a-4306-a83a-1763210c69f9">
                  <caps:sentence id="src7" class="srcSentence">Delete Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="3a7bbf07-2fca-4892-95f4-eec93f2d5e91">
                  <caps:sentence id="src8" class="srcSentence">Execute, Requery, and Clear Methods Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="29ec4b95-8986-4970-943f-3da3ecb207a2">
                  <caps:sentence id="src9" class="srcSentence">Move Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="911aa1dd-2786-4f34-992c-bb2fbdabcbdf">
                  <caps:sentence id="src10" class="srcSentence">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="66eca011-e258-4d8f-bd67-e017bcf0871b">
                  <caps:sentence id="src11" class="srcSentence">Open and Close Methods Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1152893e-b617-40f1-88b6-81e82e2234f1">ADO Code Examples in Microsoft Visual Basic</link>
        <link xlink:href="af30b764-398f-4918-aaa7-3952226cf544">ADO Code Examples in Microsoft Visual C++</link>
        <link xlink:href="d1c82f1a-cf78-4bd6-9ad4-1eb526e2c474">ADO Code Examples in Microsoft Visual J++</link>
        <link xlink:href="1582e411-55ac-40f0-bd3d-9a10654e4b67">Appendix D: ADO Samples</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
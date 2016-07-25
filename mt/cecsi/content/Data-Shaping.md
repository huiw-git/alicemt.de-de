---
title: "Data Shaping"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 62bd7dc9-45b5-4ca9-8b52-457325e0ce9e
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
# Data Shaping
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt1" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">
                  <caps:sentence sentenceid="a2a7d883c731eb3c3200a331768ba864" id="tgt2" class="tgtSentence">Data Shaping Overview</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">
                  <caps:sentence sentenceid="8c1f92702a500efdebb895008084e294" id="tgt3" class="tgtSentence">Data ShapingExample</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="b1c965b7-3dad-4de6-9e0e-502ca8785be3">
                  <caps:sentence sentenceid="9b6bebd62b065d18dfa7f07a6acdad6b" id="tgt4" class="tgtSentence">Reshaping</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="4162d35f-2ce1-4218-80a5-b6933348837e">
                  <caps:sentence sentenceid="ab96fa058d96d4528f3517e6295d4eb0" id="tgt5" class="tgtSentence">Grandchild Aggregates</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="732f624f-8900-4608-9815-194302d22e8b">
                  <caps:sentence sentenceid="e57168269cec8c2732354416c6249b2e" id="tgt6" class="tgtSentence">Parameterized Commands with Intervening COMPUTE Commands</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="43798bb5-98a6-4ad6-9bf8-78154b3a1827">
                  <caps:sentence sentenceid="447aaec4c0376b00d6d62021c801a37b" id="tgt7" class="tgtSentence">Persisting Hierarchical Recordsets</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">
                  <caps:sentence sentenceid="2f20317e0462f86bb5aa16f27a620fa5" id="tgt8" class="tgtSentence">Required Providers for Data Shaping</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">
                  <caps:sentence sentenceid="15a2e52daee1de2e80dfadf01f66cc57" id="tgt9" class="tgtSentence">Shape Commands in General</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">
                  <caps:sentence sentenceid="0d0c4ea266224e94ba0ee042f9ad767d" id="tgt10" class="tgtSentence">Shape APPEND Clause</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="3fdfead2-b5ab-4163-9b1d-3d2143a5db8c">
                  <caps:sentence sentenceid="5a5de3319150d71cf780c7f8b459f263" id="tgt11" class="tgtSentence">Shape COMPUTE Clause</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="a584e642-a4a3-418e-bc20-3aff81a5625a">
                  <caps:sentence sentenceid="ec303831f4b03bdb80c9619b97751ef2" id="tgt12" class="tgtSentence">Fabricating Hierarchical Recordsets</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">
                  <caps:sentence sentenceid="062ffc0ede81b827c6f97b8a6b5d4e4b" id="tgt13" class="tgtSentence">Accessing Rows in a Hierarchical Recordset</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">
                  <caps:sentence sentenceid="6fc3574e408dc1678a2ead32794f54bd" id="tgt14" class="tgtSentence">Formal Shape Grammar</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">
                  <caps:sentence sentenceid="c91771f826faea3a7fa4853943b9ed19" id="tgt15" class="tgtSentence">Visual Basic for Applications Functions</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">
                  <caps:sentence id="src2" class="srcSentence">Data Shaping Overview</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">
                  <caps:sentence id="src3" class="srcSentence">Data ShapingExample</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="b1c965b7-3dad-4de6-9e0e-502ca8785be3">
                  <caps:sentence id="src4" class="srcSentence">Reshaping</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="4162d35f-2ce1-4218-80a5-b6933348837e">
                  <caps:sentence id="src5" class="srcSentence">Grandchild Aggregates</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="732f624f-8900-4608-9815-194302d22e8b">
                  <caps:sentence id="src6" class="srcSentence">Parameterized Commands with Intervening COMPUTE Commands</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="43798bb5-98a6-4ad6-9bf8-78154b3a1827">
                  <caps:sentence id="src7" class="srcSentence">Persisting Hierarchical Recordsets</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">
                  <caps:sentence id="src8" class="srcSentence">Required Providers for Data Shaping</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">
                  <caps:sentence id="src9" class="srcSentence">Shape Commands in General</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">
                  <caps:sentence id="src10" class="srcSentence">Shape APPEND Clause</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="3fdfead2-b5ab-4163-9b1d-3d2143a5db8c">
                  <caps:sentence id="src11" class="srcSentence">Shape COMPUTE Clause</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="a584e642-a4a3-418e-bc20-3aff81a5625a">
                  <caps:sentence id="src12" class="srcSentence">Fabricating Hierarchical Recordsets</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">
                  <caps:sentence id="src13" class="srcSentence">Accessing Rows in a Hierarchical Recordset</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">
                  <caps:sentence id="src14" class="srcSentence">Formal Shape Grammar</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">
                  <caps:sentence id="src15" class="srcSentence">Visual Basic for Applications Functions</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
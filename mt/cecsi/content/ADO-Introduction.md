---
title: "ADO Introduction"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c5b3a134-de22-4e9c-9489-9a1cc7a5dcfa
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
# ADO Introduction
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f1c92bd8c56a97619bdedec2d5039076" id="tgt1" class="tgtSentence">ActiveX Data Objects (ADO) is a high-level, easy-to-use interface to OLE DB.</caps:sentence>
          <caps:sentence sentenceid="7add70efdda92671b93804acafbc3370" id="tgt2" class="tgtSentence"> OLE DB is a low-level, high-performance interface to a variety of data stores.</caps:sentence>
          <caps:sentence sentenceid="64fb0122a90000f09a9316e59450e358" id="tgt3" class="tgtSentence"> Both ADO and OLE DB can work with relational (tabular) and nonrelational (hierarchical or stream) data.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c63cb43a2bf761086376334aebc8032f" id="tgt4" class="tgtSentence">ADO provides a layer of abstraction between your client or middle-tier application and the low-level OLE DB interfaces.</caps:sentence>
          <caps:sentence sentenceid="43f0d9cbc39ef3881786a14612bb57e9" id="tgt5" class="tgtSentence"> ADO uses a small set of Automation objects to provide a simple and efficient interface to OLE DB.</caps:sentence>
          <caps:sentence sentenceid="b50b64ba951688711589f66ffac64ea4" id="tgt6" class="tgtSentence"> This interface makes ADO a good choice for developers in higher level languages, such as Visual Basic and VBScript, who want to access data without having to learn the intricacies of COM and OLE DB.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt7" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">
                <caps:sentence sentenceid="2e6fab81b46e2224e167f2012f24d901" id="tgt8" class="tgtSentence">ADO History</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="557ee99f-3cc8-4578-9694-6b1b0788cfdd">
                <caps:sentence sentenceid="91be34c65f9b19671e6e3ba008bfd3e3" id="tgt9" class="tgtSentence">Prerequisites for Using the ADO Documentation</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="573f8f27-babd-4e2f-bf9a-270ee7024975">
                <caps:sentence sentenceid="b2c8118a8f611d5001c19b1305228ae1" id="tgt10" class="tgtSentence">Referencing the ADO Libraries</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="2fad33fb-c858-4dcb-98dc-3dfd0e555055">
                <caps:sentence sentenceid="a0c7ee5b289353c717e3fc12979c2197" id="tgt11" class="tgtSentence">ADO Task Table</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="38c8ad3c-d6f1-40f6-a394-bbba6ed861e5">
                <caps:sentence sentenceid="226a07780e20c610dee05ecbe0288183" id="tgt12" class="tgtSentence">ADO Technology Table</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="86b83a38-efdf-4831-a6d5-7e470d517d1c">ADO Security Design Issues</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ActiveX Data Objects (ADO) is a high-level, easy-to-use interface to OLE DB.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> OLE DB is a low-level, high-performance interface to a variety of data stores.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Both ADO and OLE DB can work with relational (tabular) and nonrelational (hierarchical or stream) data.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">ADO provides a layer of abstraction between your client or middle-tier application and the low-level OLE DB interfaces.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> ADO uses a small set of Automation objects to provide a simple and efficient interface to OLE DB.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> This interface makes ADO a good choice for developers in higher level languages, such as Visual Basic and VBScript, who want to access data without having to learn the intricacies of COM and OLE DB.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">
                <caps:sentence id="src8" class="srcSentence">ADO History</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="557ee99f-3cc8-4578-9694-6b1b0788cfdd">
                <caps:sentence id="src9" class="srcSentence">Prerequisites for Using the ADO Documentation</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="573f8f27-babd-4e2f-bf9a-270ee7024975">
                <caps:sentence id="src10" class="srcSentence">Referencing the ADO Libraries</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="2fad33fb-c858-4dcb-98dc-3dfd0e555055">
                <caps:sentence id="src11" class="srcSentence">ADO Task Table</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="38c8ad3c-d6f1-40f6-a394-bbba6ed861e5">
                <caps:sentence id="src12" class="srcSentence">ADO Technology Table</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="86b83a38-efdf-4831-a6d5-7e470d517d1c">ADO Security Design Issues</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Types of Cursors (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7cc01544-e814-403b-bbfe-a2750bf921bd
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
# Types of Cursors (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="66f4321de75175dbc09ee34eff1696a6" id="tgt1" class="tgtSentence">As a general rule, your application should use the simplest cursor that provides the required data access.</caps:sentence>
          <caps:sentence sentenceid="a385f462c2ac1705c7934eb450243a27" id="tgt2" class="tgtSentence"> Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance.</caps:sentence>
          <caps:sentence sentenceid="e85e05f0cbf0eb4924a7afde67d36a72" id="tgt3" class="tgtSentence"> In many cases, the default cursor options generate a more complex cursor than your application actually needs.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="664082f726c1935b0016721ff6fa6e71" id="tgt4" class="tgtSentence">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b9d42fb33f7a4b582b46a6a483454084" id="tgt5" class="tgtSentence">At its most basic, your cursor choice depends on whether you need to change or simply view the data:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="abe4355a347a5e4ab8e0991a6c9f427d" id="tgt6" class="tgtSentence">If you just need to scroll through a set of results, but not change data, use a <legacyLink xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">forward-only</legacyLink> or <legacyLink xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">static</legacyLink> cursor.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="46dc41838d72be82eff072452868fee6" id="tgt7" class="tgtSentence">If you have a large result set and need to select just a few rows, use a <legacyLink xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">keyset</legacyLink> cursor.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9d5b551fc52e3b0570fda57f4276bc12" id="tgt8" class="tgtSentence">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a <legacyLink xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">dynamic</legacyLink> cursor.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="7d700f63fda6584609cf2ffad0bd911c" id="tgt9" class="tgtSentence">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt10" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="4ea92b77b5dfaff8a9d166c4cbb5ff49" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="2a8548bf91e328d2c04363c4ea5850f1" id="tgt12" class="tgtSentence">             <legacyLink xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5cf50ac8c8887ecaa25d6e357581819f" id="tgt13" class="tgtSentence">             <legacyLink xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="472886794d99f7ee9c79750cb5c74313" id="tgt14" class="tgtSentence">             <legacyLink xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</link>
        <link xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</link>
        <link xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</link>
        <link xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">As a general rule, your application should use the simplest cursor that provides the required data access.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> In many cases, the default cursor options generate a more complex cursor than your application actually needs.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">At its most basic, your cursor choice depends on whether you need to change or simply view the data:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">If you just need to scroll through a set of results, but not change data, use a <legacyLink xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">forward-only</legacyLink> or <legacyLink xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">static</legacyLink> cursor.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">If you have a large result set and need to select just a few rows, use a <legacyLink xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">keyset</legacyLink> cursor.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a <legacyLink xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">dynamic</legacyLink> cursor.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src9" class="srcSentence">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">             <legacyLink xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">             <legacyLink xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">             <legacyLink xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="2b1e062f-3294-4a6f-8241-a17045c4df18">Forward-Only Cursors</link>
        <link xlink:href="cce93ace-c4ed-4c6c-940c-28a50ff2fd12">Static Cursors</link>
        <link xlink:href="14b51b17-6fd9-4146-af45-ca4b0fe6d48a">Keyset Cursors</link>
        <link xlink:href="00460f30-8cf7-494e-82df-41012f40ae51">Dynamic Cursors</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
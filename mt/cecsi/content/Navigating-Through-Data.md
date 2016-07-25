---
title: "Navigating Through Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d88c9aa-8ec8-4969-8fa1-1663fd29bfc4
caps.latest.revision: 9
caps.handback.revision: 9
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
# Navigating Through Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ac9c6ac1f9ba2ed59a4eb9e37b14429d" id="tgt1" class="tgtSentence">       <legacyBold>Recordset</legacyBold> supports various methods and properties to navigate through the resultant dataset.</caps:sentence>
          <caps:sentence sentenceid="00151d9389af8ed26f15acf4e0c47bc9" id="tgt2" class="tgtSentence"> We examine this functionality by going through a few scenarios with our sample <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt3" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="713b4606762dd583f385b48ab80e2c2e" id="tgt4" class="tgtSentence">             <legacyLink xlink:href="6caf6299-2eea-4d34-9b0e-b75aab07b740">Jumping to a Record</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="78330d67fa6514c8a0d7f028705dfe1a" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="9f8cf1b2-3def-453f-a0ff-4646c5f15262">More Ways to Move in a Recordset</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c0b5c4fdcfb0cc48cf2c91498d612248" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="cca244e6-84f8-4394-bca9-f7a819b8f4df">Using Bookmarks</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="25331ae0e4c29c5fefd6c7496dc0de2b" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="442b08c5-ccc7-4192-a1cc-22f250867782">Using Pages</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="2a1f873a225cea38a0ef45c1662ef2fd" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="c8f6fbcb-6675-4133-b37e-430de43949c1">Recordset Positioning</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">       <legacyBold>Recordset</legacyBold> supports various methods and properties to navigate through the resultant dataset.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> We examine this functionality by going through a few scenarios with our sample <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">             <legacyLink xlink:href="6caf6299-2eea-4d34-9b0e-b75aab07b740">Jumping to a Record</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="9f8cf1b2-3def-453f-a0ff-4646c5f15262">More Ways to Move in a Recordset</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="cca244e6-84f8-4394-bca9-f7a819b8f4df">Using Bookmarks</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="442b08c5-ccc7-4192-a1cc-22f250867782">Using Pages</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="c8f6fbcb-6675-4133-b37e-430de43949c1">Recordset Positioning</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
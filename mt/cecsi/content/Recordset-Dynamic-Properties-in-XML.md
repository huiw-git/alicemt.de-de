---
title: "Recordset Dynamic Properties in XML"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 52f8e379-812a-4db8-9210-94458926301c
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
# Recordset Dynamic Properties in XML
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c47af97ea6afe01e7009faa78c39a97b" id="tgt1" class="tgtSentence">The following Recordset provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format: </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="8e3aa41aa5a87aa2916050e3e9fc0cd3" id="tgt2" class="tgtSentence">Update Resync </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="89224278fde1531bbc3ef6ce436f73ba" id="tgt3" class="tgtSentence">Unique Table </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ceb2ff2709397acbf802455153ff48ba" id="tgt4" class="tgtSentence">Unique Schema </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="276f77273bbc7a83920f32755862d03c" id="tgt5" class="tgtSentence">Unique Catalog </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="def4b253313a49256caef587bfe56ee4" id="tgt6" class="tgtSentence">Resync Command </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3baa020dac757e3a681fbba920a42865" id="tgt7" class="tgtSentence">IRowsetChange </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0fee24c0d6439c4ab38bc1469c483611" id="tgt8" class="tgtSentence">IRowsetUpdate </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="40df3ccd63f90ce1a8a83dcbcb52df5d" id="tgt9" class="tgtSentence">CommandTimeout </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ca033b0feaa2b3ee0ba3e67793a8a5f1" id="tgt10" class="tgtSentence">BatchSize </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c82e79346c99068992900889b0d92e29" id="tgt11" class="tgtSentence">UpdateCriteria </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9ee70e6a8ae7535807f1635f65baaee4" id="tgt12" class="tgtSentence">Reshape Name </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5c68b11032e3d763df87a38db3e8a761" id="tgt13" class="tgtSentence">AutoRecalc </caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="aa0ef8afca545aa7d37891a7ea03a41e" id="tgt14" class="tgtSentence">These properties are saved in the schema section as attributes of the element definition for the Recordset being persisted.</caps:sentence>
          <caps:sentence sentenceid="87f4952cce48c11798e0970ee94c7ecd" id="tgt15" class="tgtSentence"> These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The following Recordset provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format: </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">Update Resync </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Unique Table </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Unique Schema </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Unique Catalog </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Resync Command </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">IRowsetChange </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">IRowsetUpdate </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">CommandTimeout </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">BatchSize </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">UpdateCriteria </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Reshape Name </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">AutoRecalc </caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src14" class="srcSentence">These properties are saved in the schema section as attributes of the element definition for the Recordset being persisted.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Anticipating Errors"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea1d4a97-58c3-476b-a496-cc80db2a90d5
caps.latest.revision: 5
caps.handback.revision: 5
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
# Anticipating Errors
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d7721419cb0f100bbadb2347aee309f1" id="tgt1" class="tgtSentence">Error prevention is at least as important as error handling.</caps:sentence>
          <caps:sentence sentenceid="6ba27d12b34642ecf427586673de2b0b" id="tgt2" class="tgtSentence"> This final section contains a short list of precautions your application can take to help make errors less likely to occur.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5f36323f2cdfb77a57aad9a2c748b7b7" id="tgt3" class="tgtSentence">Check the state of objects by checking the value in the <legacyBold>State</legacyBold> property before trying to perform an operation using those objects.</caps:sentence>
          <caps:sentence sentenceid="3edabf9634a64006fb13051fb0f6b325" id="tgt4" class="tgtSentence"> For example, if your application uses a global <legacyBold>Connection</legacyBold>, check its <legacyBold>State</legacyBold> property to see if it is already open before calling the <legacyBold>Open</legacyBold> method.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="5a67deb07a0e9f1915bfc6308b8071ad" id="tgt5" class="tgtSentence">Any program that accepts data from a user must include code to validate that data before sending it to the data store.</caps:sentence>
              <caps:sentence sentenceid="b9bd6cc6cc2f6cd693953c75fbf76b67" id="tgt6" class="tgtSentence"> You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems.</caps:sentence>
              <caps:sentence sentenceid="e61588b2fa279002a7aecd678d4bafe7" id="tgt7" class="tgtSentence"> You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="31fa79a00f3d5f639e0c7609e7c8146c" id="tgt8" class="tgtSentence">Check the data before you try to write any data to the data store.</caps:sentence>
          <caps:sentence sentenceid="9a72309194a3280e015456b33193d8cc" id="tgt9" class="tgtSentence"> The easiest way to do so is to handle the <legacyBold>WillMove</legacyBold> event or the <legacyBold>WillUpdateRecordset</legacyBold> event.</caps:sentence>
          <caps:sentence sentenceid="70d0cbfa841b9d3673997eadddbdc5a9" id="tgt10" class="tgtSentence"> For a more complete discussion of handling ADO events, see <link xlink:href="e9003457-0762-48b3-942f-0820266b158f">Handling ADO Events</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f4663515b4da2c7afb0c3ca691eeec72" id="tgt11" class="tgtSentence">Make sure that <legacyBold>Recordset</legacyBold> objects are not beyond the boundaries of the <legacyBold>Recordset</legacyBold> before attempting to move the record pointer.</caps:sentence>
          <caps:sentence sentenceid="5b8c63d8bfd1f1499a74b616284576f8" id="tgt12" class="tgtSentence"> If you try to <legacyBold>MoveNext</legacyBold> when <legacyBold>EOF</legacyBold> is True or <legacyBold>MovePrev</legacyBold> when <legacyBold>BOF</legacyBold> is True, an error will occur.</caps:sentence>
          <caps:sentence sentenceid="ab2ca9caddcdb6fc877a64e2ac432496" id="tgt13" class="tgtSentence"> If you perform any of the <legacyBold>Move</legacyBold> methods when both <legacyBold>EOF</legacyBold> and <legacyBold>BOF</legacyBold> are True, an error will be generated.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="89eb8ea779f2938d7c841d614bc126f5" id="tgt14" class="tgtSentence">Errors also will occur if you try to perform operations such as <legacyBold>Seek</legacyBold> and <legacyBold>Find</legacyBold> on an empty <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Error prevention is at least as important as error handling.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This final section contains a short list of precautions your application can take to help make errors less likely to occur.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Check the state of objects by checking the value in the <legacyBold>State</legacyBold> property before trying to perform an operation using those objects.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For example, if your application uses a global <legacyBold>Connection</legacyBold>, check its <legacyBold>State</legacyBold> property to see if it is already open before calling the <legacyBold>Open</legacyBold> method.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Any program that accepts data from a user must include code to validate that data before sending it to the data store.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence"> You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src8" class="srcSentence">Check the data before you try to write any data to the data store.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> The easiest way to do so is to handle the <legacyBold>WillMove</legacyBold> event or the <legacyBold>WillUpdateRecordset</legacyBold> event.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> For a more complete discussion of handling ADO events, see <link xlink:href="e9003457-0762-48b3-942f-0820266b158f">Handling ADO Events</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">Make sure that <legacyBold>Recordset</legacyBold> objects are not beyond the boundaries of the <legacyBold>Recordset</legacyBold> before attempting to move the record pointer.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> If you try to <legacyBold>MoveNext</legacyBold> when <legacyBold>EOF</legacyBold> is True or <legacyBold>MovePrev</legacyBold> when <legacyBold>BOF</legacyBold> is True, an error will occur.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> If you perform any of the <legacyBold>Move</legacyBold> methods when both <legacyBold>EOF</legacyBold> and <legacyBold>BOF</legacyBold> are True, an error will be generated.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">Errors also will occur if you try to perform operations such as <legacyBold>Seek</legacyBold> and <legacyBold>Find</legacyBold> on an empty <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
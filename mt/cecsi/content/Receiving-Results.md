---
title: "Receiving Results"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 791aa26e-7aae-477e-9f05-5cd46e1de095
caps.latest.revision: 10
caps.handback.revision: 10
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
# Receiving Results
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3f1ef373160f8457f5a3550a2c549350" id="tgt1" class="tgtSentence">In ADO most commands result in some information returned to the caller.</caps:sentence>
          <caps:sentence sentenceid="84bbd5fa941f5d1156c17b478180983f" id="tgt2" class="tgtSentence"> For commands returning rowset, the results are received in a <legacyBold>Recordset</legacyBold> object, which is probably the most used of the ADO objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a32bca7d79c994914930ffeddfe9d88f" id="tgt3" class="tgtSentence">There are several ways to receive data in a <legacyBold>Recordset </legacyBold>object from a data source, including calling the following:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="955a056db26ff4f7b458818ed0772bd8" id="tgt4" class="tgtSentence">             <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Connection.Execute method</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="55087bbd1a8ea3660bd743fd27de9170" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Command.Execute method</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="60ea5d30f80408eb0b6204eaca580a15" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Recordset.Open method</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6af6e9a591a2945af1169b053902fcc3" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="5a0ec8f9-5ba3-4f9f-b80d-2073aa049586">Connection.NamedCommand</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0102567e6086364daa581e4794a8f2c3" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="35ffdb79-a931-4271-a3bb-0cd804cf173e">Connection.StoredProcedure</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="e420095a04ccfed4b7fb973dba53720b" id="tgt9" class="tgtSentence">Receiving data in a <legacyBold>Recordset</legacyBold> object concludes the process of getting data, with the participation of a <legacyBold>Connection</legacyBold> object and a <legacyBold>Command</legacyBold> object, implicitly or explicitly.</caps:sentence>
          <caps:sentence sentenceid="3c0c25d3b9e30f3db2e2b79e3c8a60d7" id="tgt10" class="tgtSentence"> In a typical client/server application system, the whole process of getting data requires a round trip over the network for each filled <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="20866e0d49f0bd9a84d04a62799e1c7a" id="tgt11" class="tgtSentence">To receive more than one result sets means you would need to make several round trips over the network, one for each data set encapsulated in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="c495d2c8e69532e92722bce4828c0713" id="tgt12" class="tgtSentence"> For slow or congested networks, reducing the number of round trips may help improve the application's performances.</caps:sentence>
          <caps:sentence sentenceid="767f3a3885fa11bbf18a20e88975c22b" id="tgt13" class="tgtSentence"> Therefore, some providers offer support to receive multiple <legacyBold>Recordset</legacyBold>s in a single round trip.</caps:sentence>
          <caps:sentence sentenceid="74e65ca18b98d2238bc5c18af10aa6eb" id="tgt14" class="tgtSentence"> This is discussed in the following topic:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="588e2880e0324615708cf490c7b6e221" id="tgt15" class="tgtSentence">             <legacyLink xlink:href="2a7ad7a6-f00d-4355-b0b5-d0ab957b0566">Receiving Multiple Recordsets</legacyLink>           </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">In ADO most commands result in some information returned to the caller.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For commands returning rowset, the results are received in a <legacyBold>Recordset</legacyBold> object, which is probably the most used of the ADO objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">There are several ways to receive data in a <legacyBold>Recordset </legacyBold>object from a data source, including calling the following:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">             <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Connection.Execute method</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Command.Execute method</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Recordset.Open method</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="5a0ec8f9-5ba3-4f9f-b80d-2073aa049586">Connection.NamedCommand</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="35ffdb79-a931-4271-a3bb-0cd804cf173e">Connection.StoredProcedure</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src9" class="srcSentence">Receiving data in a <legacyBold>Recordset</legacyBold> object concludes the process of getting data, with the participation of a <legacyBold>Connection</legacyBold> object and a <legacyBold>Command</legacyBold> object, implicitly or explicitly.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> In a typical client/server application system, the whole process of getting data requires a round trip over the network for each filled <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">To receive more than one result sets means you would need to make several round trips over the network, one for each data set encapsulated in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> For slow or congested networks, reducing the number of round trips may help improve the application's performances.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> Therefore, some providers offer support to receive multiple <legacyBold>Recordset</legacyBold>s in a single round trip.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> This is discussed in the following topic:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">             <legacyLink xlink:href="2a7ad7a6-f00d-4355-b0b5-d0ab957b0566">Receiving Multiple Recordsets</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
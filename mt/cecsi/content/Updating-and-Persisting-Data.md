---
title: "Updating and Persisting Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8dc27274-4f96-43d1-913c-4ff7d01b9a27
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
# Updating and Persisting Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16318e9bd0a4511afa7b6888efdce64e" id="tgt1" class="tgtSentence">The preceding chapters have discussed how to use ADO to get to data in a data source, how to move around in the data, and even how to edit the data.</caps:sentence>
          <caps:sentence sentenceid="d4e1fe755f7591a604aa22dc98940824" id="tgt2" class="tgtSentence"> Of course, if the goal of your application is to allow users to make changes to the data, you will need to understand how to save those changes.</caps:sentence>
          <caps:sentence sentenceid="92821482b1f3b6c5d1c523e8e77a882d" id="tgt3" class="tgtSentence"> You can either persist the <legacyBold>Recordset</legacyBold> changes to a file using the <legacyBold>Save</legacyBold> method, or you can send the changes back to the data source for storage using the <legacyBold>Update</legacyBold> or <legacyBold>UpdateBatch</legacyBold> methods.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7c770f85cd9a77d47427057db2de2982" id="tgt4" class="tgtSentence">In the preceding chapters, you changed the data in several rows of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="1972e5b8123930ac400973c965c45934" id="tgt5" class="tgtSentence"> ADO supports two basic notions relating to the addition, deletion, and modification of rows of data.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a353864a964d39ad95db3233d6337b47" id="tgt6" class="tgtSentence">The first notion is that changes aren't immediately made to the <legacyBold>Recordset</legacyBold>; instead, they are made to an internal <legacyItalic>copy buffer</legacyItalic>.</caps:sentence>
          <caps:sentence sentenceid="21a63e89cae0fa09875faf5b40553a4b" id="tgt7" class="tgtSentence"> If you decide you don't want the changes, the modifications in the copy buffer are discarded.</caps:sentence>
          <caps:sentence sentenceid="79face484249ab29b209b0f071124b09" id="tgt8" class="tgtSentence"> If you decide to keep the changes, the changes in the copy buffer are applied to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="94f61f4e3d3fae773d2604b37c0a972f" id="tgt9" class="tgtSentence">The second notion is that changes are either propagated to the data source as soon as you declare the work on a row complete (that is, <legacyItalic>immediate</legacyItalic> mode), or all changes to a set of rows are collected until you declare the work for the set complete (that is, <legacyItalic>batch</legacyItalic> mode).</caps:sentence>
          <caps:sentence sentenceid="85550bf7aaaa5cef40f30bbc046b3dcb" id="tgt10" class="tgtSentence"> The <legacyBold>LockType</legacyBold> property determines when the changes are made to the underlying data source.</caps:sentence>
          <caps:sentence sentenceid="b2e8c564ce873dd73171ed9e44076bd8" id="tgt11" class="tgtSentence">
            <legacyBold>adLockOptimistic</legacyBold> or <legacyBold>adLockPessimistic</legacyBold> specifies immediate mode, while <legacyBold>adLockBatchOptimistic</legacyBold> specifies batch mode.</caps:sentence>
          <caps:sentence sentenceid="d5fd7fe745b92edbff7097678081d82e" id="tgt12" class="tgtSentence"> The <legacyBold>CursorLocation</legacyBold> property can affect which <legacyBold>LockType</legacyBold> settings are available.</caps:sentence>
          <caps:sentence sentenceid="04f49628c62841b65658c327ef1f45b8" id="tgt13" class="tgtSentence"> For instance, the <legacyBold>adLockPessimistic</legacyBold> setting is not supported if the <legacyBold>CursorLocation</legacyBold> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="07c9c1ba355944b9b02de6644a7373f4" id="tgt14" class="tgtSentence">In immediate mode, each invocation of the <legacyBold>Update</legacyBold> method propagates the changes to the data source.</caps:sentence>
          <caps:sentence sentenceid="d4aa9c897dafa5292ee4bb1cd897ed38" id="tgt15" class="tgtSentence"> In batch mode, each invocation of <legacyBold>Update</legacyBold> or movement of the current row position saves the changes to the copy buffer, but only the <legacyBold>UpdateBatch</legacyBold> method propagates the changes to the data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt16" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="ca21025c6e4603bba188175818e27681" id="tgt17" class="tgtSentence">             <legacyLink xlink:href="6508e4e9-e33a-4dad-b340-5d632fd78a91">Updating Data</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f33d23e0d8a8a636a7ac0098f6e7e06a" id="tgt18" class="tgtSentence">             <legacyLink xlink:href="21c162ca-2845-4dd8-a49d-e715aba8c461">Persisting Data</legacyLink>           </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The preceding chapters have discussed how to use ADO to get to data in a data source, how to move around in the data, and even how to edit the data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Of course, if the goal of your application is to allow users to make changes to the data, you will need to understand how to save those changes.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> You can either persist the <legacyBold>Recordset</legacyBold> changes to a file using the <legacyBold>Save</legacyBold> method, or you can send the changes back to the data source for storage using the <legacyBold>Update</legacyBold> or <legacyBold>UpdateBatch</legacyBold> methods.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">In the preceding chapters, you changed the data in several rows of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> ADO supports two basic notions relating to the addition, deletion, and modification of rows of data.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">The first notion is that changes aren't immediately made to the <legacyBold>Recordset</legacyBold>; instead, they are made to an internal <legacyItalic>copy buffer</legacyItalic>.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> If you decide you don't want the changes, the modifications in the copy buffer are discarded.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> If you decide to keep the changes, the changes in the copy buffer are applied to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">The second notion is that changes are either propagated to the data source as soon as you declare the work on a row complete (that is, <legacyItalic>immediate</legacyItalic> mode), or all changes to a set of rows are collected until you declare the work for the set complete (that is, <legacyItalic>batch</legacyItalic> mode).</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> The <legacyBold>LockType</legacyBold> property determines when the changes are made to the underlying data source.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence">
            <legacyBold>adLockOptimistic</legacyBold> or <legacyBold>adLockPessimistic</legacyBold> specifies immediate mode, while <legacyBold>adLockBatchOptimistic</legacyBold> specifies batch mode.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> The <legacyBold>CursorLocation</legacyBold> property can affect which <legacyBold>LockType</legacyBold> settings are available.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> For instance, the <legacyBold>adLockPessimistic</legacyBold> setting is not supported if the <legacyBold>CursorLocation</legacyBold> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">In immediate mode, each invocation of the <legacyBold>Update</legacyBold> method propagates the changes to the data source.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> In batch mode, each invocation of <legacyBold>Update</legacyBold> or movement of the current row position saves the changes to the copy buffer, but only the <legacyBold>UpdateBatch</legacyBold> method propagates the changes to the data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src16" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">             <legacyLink xlink:href="6508e4e9-e33a-4dad-b340-5d632fd78a91">Updating Data</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">             <legacyLink xlink:href="21c162ca-2845-4dd8-a49d-e715aba8c461">Persisting Data</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
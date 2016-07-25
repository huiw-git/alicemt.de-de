---
title: "Adding Records"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dd34669e-6f06-403b-9241-1c85c82aecc2
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
# Adding Records
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="69f0947c1b0282e9952216502a3f0b0b" id="tgt1" class="tgtSentence">Use the <legacyBold>AddNew</legacyBold> method to create and initialize a new record in an existing <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="020b1e6f726a8fc9a20cfae013aae787" id="tgt2" class="tgtSentence"> You can use the <legacyBold>Supports</legacyBold> method with a <legacyBold>CursorOptionEnum</legacyBold> value of <legacyBold>adAddNew</legacyBold> to verify whether you can add records to the current <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1cb96a2a2e98adf29fb830c7eb007ccb" id="tgt3" class="tgtSentence">After you call the <legacyBold>AddNew</legacyBold> method, the new record becomes the current record and remains current after you call the <legacyBold>Update</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="b59de2304b95e189575ba0bb7c9ad9e5" id="tgt4" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> object does not support bookmarks, you might not be able to access the new record once you move to another record.</caps:sentence>
          <caps:sentence sentenceid="cdd15c89fa85fe52f8702914c80dfb6d" id="tgt5" class="tgtSentence"> Therefore, depending on your cursor type, you might need to call the <legacyBold>Requery</legacyBold> method to make the new record accessible.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9dc9d6ab6669857c0fc597bcf3d40491" id="tgt6" class="tgtSentence">If you call <legacyBold>AddNew</legacyBold> while editing the current record or while adding a new record, ADO calls the <legacyBold>Update</legacyBold> method to save any changes and then creates the new record.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt7" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="0e1b97d0951dcd2987b6b873d3457369" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="cab4adff-f22f-4fb1-9217-f8138c795268">Adding Records Using AddNew</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b23e078b737836edaf47590bfb33caaa" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="f3648ef4-9f36-4991-a868-83a617389844">Adding Multiple Fields</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b8cd5b44742041f0678e6ac8bfe25e1e" id="tgt10" class="tgtSentence">             <legacyLink xlink:href="4c7e010d-08cd-4e22-9b32-23c36f02f88c">Determining Edit Mode</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="982e808841201760ffb16d1e325a44ca" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="ed314bb9-e188-4658-a68c-a2abc49610be">Using AddNew in Immediate and Batch Modes</legacyLink>           </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Use the <legacyBold>AddNew</legacyBold> method to create and initialize a new record in an existing <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can use the <legacyBold>Supports</legacyBold> method with a <legacyBold>CursorOptionEnum</legacyBold> value of <legacyBold>adAddNew</legacyBold> to verify whether you can add records to the current <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">After you call the <legacyBold>AddNew</legacyBold> method, the new record becomes the current record and remains current after you call the <legacyBold>Update</legacyBold> method.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> object does not support bookmarks, you might not be able to access the new record once you move to another record.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Therefore, depending on your cursor type, you might need to call the <legacyBold>Requery</legacyBold> method to make the new record accessible.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">If you call <legacyBold>AddNew</legacyBold> while editing the current record or while adding a new record, ADO calls the <legacyBold>Update</legacyBold> method to save any changes and then creates the new record.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="cab4adff-f22f-4fb1-9217-f8138c795268">Adding Records Using AddNew</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="f3648ef4-9f36-4991-a868-83a617389844">Adding Multiple Fields</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">             <legacyLink xlink:href="4c7e010d-08cd-4e22-9b32-23c36f02f88c">Determining Edit Mode</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="ed314bb9-e188-4658-a68c-a2abc49610be">Using AddNew in Immediate and Batch Modes</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
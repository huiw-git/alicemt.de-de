---
title: "Adding Records Using AddNew"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cab4adff-f22f-4fb1-9217-f8138c795268
caps.latest.revision: 12
caps.handback.revision: 12
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
# Adding Records Using AddNew
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2953d6348513408e6002fdab0fa5fc53" id="tgt1" class="tgtSentence">This is the basic syntax of the <legacyBold>AddNew</legacyBold> method:</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e3955acdc7d7b65505a14f5a795d0eb7" id="tgt2" class="tgtSentence">
            <legacyItalic>recordset</legacyItalic>.AddNew <legacyItalic>FieldList</legacyItalic>, <legacyItalic>Values</legacyItalic></caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4679d18d20ed77dc2ddb3f143b1fe8f8" id="tgt3" class="tgtSentence">The <legacyItalic>FieldList</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments are optional.</caps:sentence>
          <caps:sentence sentenceid="a1dce75223a961a7b48ced9cdad57f83" id="tgt4" class="tgtSentence">
            <legacyItalic>FieldList</legacyItalic> is either a single name or an array of names or ordinal positions of the fields in the new record.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b07a4b8fb4185147149a730a5b85f5e0" id="tgt5" class="tgtSentence">The <legacyItalic>Values</legacyItalic> argument is either a single value or an array of values for the fields in the new record.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9aeadaea71baa91a5066c85965a151df" id="tgt6" class="tgtSentence">Typically, when you intend to add a single record, you will call the <legacyBold>AddNew</legacyBold> method without any arguments.</caps:sentence>
          <caps:sentence sentenceid="f121b006ef91ce12356650d920fdad28" id="tgt7" class="tgtSentence"> Specifically, you will call <legacyBold>AddNew</legacyBold>; set the <legacyBold>Value</legacyBold> of each field in the new record; and then call <legacyBold>Update</legacyBold> or <legacyBold>UpdateBatch</legacyBold>, or both.</caps:sentence>
          <caps:sentence sentenceid="ed83b18f41bb0a2a17223eaf91f1dce8" id="tgt8" class="tgtSentence"> You can make sure that your <legacyBold>Recordset</legacyBold> supports adding new records by using the <legacyBold>Supports</legacyBold> property with the <legacyBold>adAddNew</legacyBold> enumerated constant.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0e3957415b419650f25e4a74592f0cfd" id="tgt9" class="tgtSentence">The following code uses this technique to add a new Shipper to the sample <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="4d828db9f269226eab714106b1bb74ac" id="tgt10" class="tgtSentence"> SQL Server supplies the ShipperID field value automatically.</caps:sentence>
          <caps:sentence sentenceid="fbfa61a04d60db5be77f1eea9f434311" id="tgt11" class="tgtSentence"> Therefore, the code does not try to supply a field value for the new records.</caps:sentence>
        </para>
        <code>    'BeginAddNew1.1
    If objRs.Supports(adAddNew) Then
        With objRs
            .AddNew
            .Fields("CompanyName") = "Sample Shipper"
            .Fields("Phone") = "(931) 555-6334"
            .Update
        End With
    End If
    'EndAddNew1.1</code>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="c6ac8689f35611dd5621a48971fe169f" id="tgt12" class="tgtSentence">Because this code uses a disconnected <legacyBold>Recordset</legacyBold> with a client-side cursor in batch mode, you must reconnect the <legacyBold>Recordset</legacyBold> to the data source with a new <legacyBold>Connection</legacyBold> object before you can call the <legacyBold>UpdateBatch</legacyBold> method to post changes to the database.</caps:sentence>
            <caps:sentence sentenceid="a55cebf5f22b088851541c73be64a1a3" id="tgt13" class="tgtSentence"> This is easily done by using the new function <legacyBold>GetNewConnection</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This is the basic syntax of the <legacyBold>AddNew</legacyBold> method:</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">
            <legacyItalic>recordset</legacyItalic>.AddNew <legacyItalic>FieldList</legacyItalic>, <legacyItalic>Values</legacyItalic></caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">The <legacyItalic>FieldList</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments are optional.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence">
            <legacyItalic>FieldList</legacyItalic> is either a single name or an array of names or ordinal positions of the fields in the new record.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The <legacyItalic>Values</legacyItalic> argument is either a single value or an array of values for the fields in the new record.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">Typically, when you intend to add a single record, you will call the <legacyBold>AddNew</legacyBold> method without any arguments.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Specifically, you will call <legacyBold>AddNew</legacyBold>; set the <legacyBold>Value</legacyBold> of each field in the new record; and then call <legacyBold>Update</legacyBold> or <legacyBold>UpdateBatch</legacyBold>, or both.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> You can make sure that your <legacyBold>Recordset</legacyBold> supports adding new records by using the <legacyBold>Supports</legacyBold> property with the <legacyBold>adAddNew</legacyBold> enumerated constant.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">The following code uses this technique to add a new Shipper to the sample <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> SQL Server supplies the ShipperID field value automatically.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> Therefore, the code does not try to supply a field value for the new records.</caps:sentence>
        </para>
        <code>    'BeginAddNew1.1
    If objRs.Supports(adAddNew) Then
        With objRs
            .AddNew
            .Fields("CompanyName") = "Sample Shipper"
            .Fields("Phone") = "(931) 555-6334"
            .Update
        End With
    End If
    'EndAddNew1.1</code>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Because this code uses a disconnected <legacyBold>Recordset</legacyBold> with a client-side cursor in batch mode, you must reconnect the <legacyBold>Recordset</legacyBold> to the data source with a new <legacyBold>Connection</legacyBold> object before you can call the <legacyBold>UpdateBatch</legacyBold> method to post changes to the database.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> This is easily done by using the new function <legacyBold>GetNewConnection</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
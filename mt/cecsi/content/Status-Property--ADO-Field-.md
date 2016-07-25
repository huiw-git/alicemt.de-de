---
title: "Status Property (ADO Field)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad
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
# Status Property (ADO Field)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8fd8574b2d1374ae4b46d5ec5f145ebf" id="tgt1" class="tgtSentence">Indicates the status of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bc103695c3c5d5b98223cbcf67699b11" id="tgt3" class="tgtSentence">Returns a <legacyLink xlink:href="e06da1e2-303f-41b2-a3b0-61e233da152c">FieldStatusEnum</legacyLink> value.</caps:sentence>
            <caps:sentence sentenceid="bb803502f869e6a41630736987c9be4c" id="tgt4" class="tgtSentence"> The default value is <legacyBold>adFieldOK</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="cc74aeb74c398c9ad34e432d8f60ff2a" id="tgt5" class="tgtSentence">Record Field Status</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="684e9c42052d87ae225381557ba317d2" id="tgt6" class="tgtSentence">Changes to the value of a <legacyBold>Field</legacyBold> object in the Fields collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object are cached until the object's <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method is called.</caps:sentence>
                <caps:sentence sentenceid="c7a0a2b111f4c6181c490766a6089e5b" id="tgt7" class="tgtSentence"> At that point, if the change to the Field's value caused an error, OLE DB raises the error <legacyBold>DB_E_ERRORSOCCURRED</legacyBold> (2147749409).</caps:sentence>
                <caps:sentence sentenceid="480fad0bdaf96600558848acf6b82a58" id="tgt8" class="tgtSentence"> The Status property of any of the <legacyBold>Field</legacyBold> objects in the <legacyBold>Fields</legacyBold> collection that caused the error will contain a value from the <legacyLink xlink:href="e06da1e2-303f-41b2-a3b0-61e233da152c">FieldStatusEnum</legacyLink> describing the cause of the problem.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="aaa1548fcc1f725315fcc32fbcf9fc44" id="tgt9" class="tgtSentence">To enhance performance, additions and deletions to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collections of the <legacyBold>Record</legacyBold> object are cached until the <legacyBold>Update</legacyBold> method is called, and then the changes are made in a batch optimistic update.</caps:sentence>
                <caps:sentence sentenceid="d946540afdf2d1eec13d892e6b5ef5a5" id="tgt10" class="tgtSentence"> If the <legacyBold>Update</legacyBold> method is not called, the server is not updated.</caps:sentence>
                <caps:sentence sentenceid="8e62065e44df74373c211b30cb0f047a" id="tgt11" class="tgtSentence"> If any updates fail then an OLE DB provider error (DB_E_ERRORSOCCURRED) is returned and the <legacyBold>Status</legacyBold> property indicates the combined values of the operation and error status code.</caps:sentence>
                <caps:sentence sentenceid="2cd7ee0e552d52aece38185b9a2a9ca3" id="tgt12" class="tgtSentence"> For example, <legacyBold>adFieldPendingInsert</legacyBold> <legacyBold>OR</legacyBold> <legacyBold>adFieldPermissionDenied</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="023e5632d7c0bf367bea6c66a8a95704" id="tgt13" class="tgtSentence"> The <legacyBold>Status</legacyBold> property for each <legacyBold>Field</legacyBold> can be used to determine why the <legacyBold>Field</legacyBold> was not added, modified, or deleted.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="64247bddcda31e50e69f17ef5dc25e30" id="tgt14" class="tgtSentence">Many types of problems encountered when adding, modifying, or deleting a <legacyBold>Field</legacyBold> are reported through the <legacyBold>Status</legacyBold> property.</caps:sentence>
                <caps:sentence sentenceid="30a7b8d55c2ce7e93c128e9141310ee2" id="tgt15" class="tgtSentence"> For example, if the user deletes a <legacyBold>Field</legacyBold>, it is marked for deletion from the <legacyBold>Fields</legacyBold> collection.</caps:sentence>
                <caps:sentence sentenceid="d1632f7d3914125c434cb83cd57c871f" id="tgt16" class="tgtSentence"> If the subsequent <legacyBold>Update</legacyBold> returns an error because the user tried to delete a <legacyBold>Field</legacyBold> for which they do not have permission, the <legacyBold>Field</legacyBold> will have a <legacyBold>Status</legacyBold> of <legacyBold>adFieldPermissionDenied</legacyBold> <legacyBold>OR</legacyBold> <legacyBold>adFieldPendingDelete</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="a2dc415248b2236f563c8c9d3350e4f5" id="tgt17" class="tgtSentence"> Calling the <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method restores original values and sets the <legacyBold>Status</legacyBold> to <legacyBold>adFieldOK</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ff443dc88ab3cbcbb0147f033947635f" id="tgt18" class="tgtSentence">Similarly, the <legacyBold>Update</legacyBold> method may return an error because a new <legacyBold>Field</legacyBold> was added and given an inappropriate value.</caps:sentence>
                <caps:sentence sentenceid="2c3c91d43982b2f4d184c41cb29846f0" id="tgt19" class="tgtSentence"> In that case the new <legacyBold>Field</legacyBold> will be in the <legacyBold>Fields</legacyBold> collection and have a status of <legacyBold>adFieldPendingInsert</legacyBold> and perhaps <legacyBold>adFieldCantCreate</legacyBold> (depending upon your provider).</caps:sentence>
                <caps:sentence sentenceid="4bc86add34dbf1a1f04b10a9dd68a7fb" id="tgt20" class="tgtSentence"> You can supply an appropriate value for the new <legacyBold>Field</legacyBold> and call <legacyBold>Update</legacyBold> again.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="6383c1eb70582a007ed9a63b482be932" id="tgt21" class="tgtSentence">Recordset Field Status</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="33bcaec7c41a2225d8094364d4114beb" id="tgt22" class="tgtSentence">Changes to the value of a <legacyBold>Field</legacyBold> object in the Fields collection of either a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> are cached until the object's <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method is called.</caps:sentence>
                <caps:sentence sentenceid="c7a0a2b111f4c6181c490766a6089e5b" id="tgt23" class="tgtSentence"> At that point, if the change to the Field's value caused an error, OLE DB raises the error <legacyBold>DB_E_ERRORSOCCURRED</legacyBold> (2147749409).</caps:sentence>
                <caps:sentence sentenceid="480fad0bdaf96600558848acf6b82a58" id="tgt24" class="tgtSentence"> The Status property of any of the <legacyBold>Field</legacyBold> objects in the <legacyBold>Fields</legacyBold> collection that caused the error will contain a value from the <legacyLink xlink:href="e06da1e2-303f-41b2-a3b0-61e233da152c">FieldStatusEnum</legacyLink> describing the cause of the problem.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt25" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="fdd09b60-39c7-44be-8008-e891a031f80e">Visual Basic Example</link>
        <link xlink:href="194ce221-49bd-4474-ba34-91453d329381">Visual C++ Example</link>
        <link xlink:href="d35cb991-2c5b-4d91-bc07-62104242cae7">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the status of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyLink xlink:href="e06da1e2-303f-41b2-a3b0-61e233da152c">FieldStatusEnum</legacyLink> value.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>adFieldOK</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src5" class="srcSentence">Record Field Status</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src6" class="srcSentence">Changes to the value of a <legacyBold>Field</legacyBold> object in the Fields collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object are cached until the object's <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method is called.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> At that point, if the change to the Field's value caused an error, OLE DB raises the error <legacyBold>DB_E_ERRORSOCCURRED</legacyBold> (2147749409).</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> The Status property of any of the <legacyBold>Field</legacyBold> objects in the <legacyBold>Fields</legacyBold> collection that caused the error will contain a value from the <legacyLink xlink:href="e06da1e2-303f-41b2-a3b0-61e233da152c">FieldStatusEnum</legacyLink> describing the cause of the problem.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src9" class="srcSentence">To enhance performance, additions and deletions to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collections of the <legacyBold>Record</legacyBold> object are cached until the <legacyBold>Update</legacyBold> method is called, and then the changes are made in a batch optimistic update.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> If the <legacyBold>Update</legacyBold> method is not called, the server is not updated.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> If any updates fail then an OLE DB provider error (DB_E_ERRORSOCCURRED) is returned and the <legacyBold>Status</legacyBold> property indicates the combined values of the operation and error status code.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> For example, <legacyBold>adFieldPendingInsert</legacyBold> <legacyBold>OR</legacyBold> <legacyBold>adFieldPermissionDenied</legacyBold>.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> The <legacyBold>Status</legacyBold> property for each <legacyBold>Field</legacyBold> can be used to determine why the <legacyBold>Field</legacyBold> was not added, modified, or deleted.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src14" class="srcSentence">Many types of problems encountered when adding, modifying, or deleting a <legacyBold>Field</legacyBold> are reported through the <legacyBold>Status</legacyBold> property.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> For example, if the user deletes a <legacyBold>Field</legacyBold>, it is marked for deletion from the <legacyBold>Fields</legacyBold> collection.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> If the subsequent <legacyBold>Update</legacyBold> returns an error because the user tried to delete a <legacyBold>Field</legacyBold> for which they do not have permission, the <legacyBold>Field</legacyBold> will have a <legacyBold>Status</legacyBold> of <legacyBold>adFieldPermissionDenied</legacyBold> <legacyBold>OR</legacyBold> <legacyBold>adFieldPendingDelete</legacyBold>.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> Calling the <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method restores original values and sets the <legacyBold>Status</legacyBold> to <legacyBold>adFieldOK</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src18" class="srcSentence">Similarly, the <legacyBold>Update</legacyBold> method may return an error because a new <legacyBold>Field</legacyBold> was added and given an inappropriate value.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> In that case the new <legacyBold>Field</legacyBold> will be in the <legacyBold>Fields</legacyBold> collection and have a status of <legacyBold>adFieldPendingInsert</legacyBold> and perhaps <legacyBold>adFieldCantCreate</legacyBold> (depending upon your provider).</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> You can supply an appropriate value for the new <legacyBold>Field</legacyBold> and call <legacyBold>Update</legacyBold> again.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src21" class="srcSentence">Recordset Field Status</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src22" class="srcSentence">Changes to the value of a <legacyBold>Field</legacyBold> object in the Fields collection of either a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> are cached until the object's <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method is called.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> At that point, if the change to the Field's value caused an error, OLE DB raises the error <legacyBold>DB_E_ERRORSOCCURRED</legacyBold> (2147749409).</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> The Status property of any of the <legacyBold>Field</legacyBold> objects in the <legacyBold>Fields</legacyBold> collection that caused the error will contain a value from the <legacyLink xlink:href="e06da1e2-303f-41b2-a3b0-61e233da152c">FieldStatusEnum</legacyLink> describing the cause of the problem.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src25" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="fdd09b60-39c7-44be-8008-e891a031f80e">Visual Basic Example</link>
        <link xlink:href="194ce221-49bd-4474-ba34-91453d329381">Visual C++ Example</link>
        <link xlink:href="d35cb991-2c5b-4d91-bc07-62104242cae7">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
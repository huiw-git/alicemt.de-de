---
title: "CancelUpdate Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: eaa856cc-c786-462e-890c-c896261b1741
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
# CancelUpdate Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4c02ae39715d12d39d8f974a75e7a4d8" id="tgt1" class="tgtSentence">Cancels any changes made to the current or new row of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, before calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>.<legacyBold>CancelUpdate</legacyBold><parameterReference>record.Fields</parameterReference>.<legacyBold>CancelUpdate</legacyBold></legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="c1e71ce69bff36c1582c5f180ea9a4ff" id="tgt2" class="tgtSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="162ea37c1399120e20d15424f5b134bb" id="tgt3" class="tgtSentence">Use the <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> method to cancel any changes made to the current row or to discard a newly added row.</caps:sentence>
                <caps:sentence sentenceid="509fe751d2ac2173ec4aece20ba40277" id="tgt4" class="tgtSentence"> You cannot cancel changes to the current row or a new row after you call the <unmanagedCodeEntityReference>Update</unmanagedCodeEntityReference> method, unless the changes are either part of a transaction that you can roll back with the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">RollbackTrans</legacyLink> method, or part of a batch update.</caps:sentence>
                <caps:sentence sentenceid="64061333709e50504e51199975246873" id="tgt5" class="tgtSentence"> In the case of a batch update, you can cancel the <unmanagedCodeEntityReference>Update</unmanagedCodeEntityReference> with the <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> method.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="29ccb6f8150d14dedb230f1dc36b015d" id="tgt6" class="tgtSentence">If you are adding a new row when you call the <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> method, the current row becomes the row that was current before the <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink> call.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="133b0421efa5c886974a70bdec5f8c0f" id="tgt7" class="tgtSentence">If you are in edit mode and want to move off the current record (for example, by using the <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>, or <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> methods), you can use <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> to cancel any pending changes.</caps:sentence>
                <caps:sentence sentenceid="923fce872068fdd49783c992c72483c5" id="tgt8" class="tgtSentence"> You may need to do this if the update cannot successfully be posted to the data source.</caps:sentence>
                <caps:sentence sentenceid="5038d43d7d6196dcae0fa1ca53d5b847" id="tgt9" class="tgtSentence"> For example, an attempted delete that fails due to referential integrity violations will leave the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> in edit mode after a call to <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="de17f0f24b49f8364187891f8550ffbb" id="tgt10" class="tgtSentence">Record</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cffeed90c5f64d37f3fa0e83d21be542" id="tgt11" class="tgtSentence">The <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> method cancels any pending insertions or deletions of <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects, and cancels pending updates of existing fields and restores them to their original values.</caps:sentence>
                <caps:sentence sentenceid="6b12553e80f7b74c4136d4fac6688fec" id="tgt12" class="tgtSentence"> The <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property of all fields in the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection is set to <legacyBold>adFieldOK</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt13" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="55bedd08-7440-4da4-b854-4ac9ef2fdedb">Visual Basic Example</link>
        <link xlink:href="cc59d23a-2f38-42f9-8b65-ed89009e87ec">Visual C++ Example</link>
        <link xlink:href="f93099ae-797d-4f0d-ac28-81405b2892e1">Visual J++ Example</link>
        <link xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew Method</link>
        <link xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel Method</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">EditMode Property</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Cancels any changes made to the current or new row of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, before calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>.<legacyBold>CancelUpdate</legacyBold><parameterReference>record.Fields</parameterReference>.<legacyBold>CancelUpdate</legacyBold></legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src2" class="srcSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src3" class="srcSentence">Use the <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> method to cancel any changes made to the current row or to discard a newly added row.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> You cannot cancel changes to the current row or a new row after you call the <unmanagedCodeEntityReference>Update</unmanagedCodeEntityReference> method, unless the changes are either part of a transaction that you can roll back with the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">RollbackTrans</legacyLink> method, or part of a batch update.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> In the case of a batch update, you can cancel the <unmanagedCodeEntityReference>Update</unmanagedCodeEntityReference> with the <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> method.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src6" class="srcSentence">If you are adding a new row when you call the <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> method, the current row becomes the row that was current before the <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink> call.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src7" class="srcSentence">If you are in edit mode and want to move off the current record (for example, by using the <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>, or <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> methods), you can use <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> to cancel any pending changes.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> You may need to do this if the update cannot successfully be posted to the data source.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> For example, an attempted delete that fails due to referential integrity violations will leave the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> in edit mode after a call to <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src10" class="srcSentence">Record</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src11" class="srcSentence">The <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> method cancels any pending insertions or deletions of <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects, and cancels pending updates of existing fields and restores them to their original values.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> The <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property of all fields in the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection is set to <legacyBold>adFieldOK</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="55bedd08-7440-4da4-b854-4ac9ef2fdedb">Visual Basic Example</link>
        <link xlink:href="cc59d23a-2f38-42f9-8b65-ed89009e87ec">Visual C++ Example</link>
        <link xlink:href="f93099ae-797d-4f0d-ac28-81405b2892e1">Visual J++ Example</link>
        <link xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew Method</link>
        <link xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel Method</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">EditMode Property</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
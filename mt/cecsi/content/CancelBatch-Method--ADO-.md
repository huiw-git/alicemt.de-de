---
title: "CancelBatch Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c
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
# CancelBatch Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a65d233746333e6dbd5df56e7ee2fd9b" id="tgt1" class="tgtSentence">Cancels a pending batch update.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>.<legacyBold>CancelBatch</legacyBold><parameterReference>AffectRecords</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="98a388e0912a0d881ac1f3ecb4016804" id="tgt2" class="tgtSentence"> <legacyItalic>AffectRecords</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="8198b173fcae22a2fd015f899307d030" id="tgt4" class="tgtSentence"> An <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink> value that indicates how many records the <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> method will affect.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d30ff6adb047eace77c9066f8431e8d1" id="tgt5" class="tgtSentence">Use the <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> method to cancel any pending updates in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> in batch update mode.</caps:sentence>
            <caps:sentence sentenceid="add3e35c8dfcce61538b3e5a50268d2a" id="tgt6" class="tgtSentence"> If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is in immediate update mode, calling <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> without <legacyBold>adAffectCurrent</legacyBold> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f9914e747483d540bbe7de8a66ea37cb" id="tgt7" class="tgtSentence">If you are editing the current record or are adding a new record when you call <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference>, ADO first calls the <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method to cancel any cached changes.</caps:sentence>
            <caps:sentence sentenceid="2a003bf257e8843d7964ec488e787f33" id="tgt8" class="tgtSentence"> After that, all pending changes in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> are canceled.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7d5788d7556269db3a5811c6dbeeaa74" id="tgt9" class="tgtSentence">The current record may be indeterminable after a <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> call, especially if you were in the process of adding a new record.</caps:sentence>
            <caps:sentence sentenceid="c0da94476e6ff1ffca8646b0a4b49be0" id="tgt10" class="tgtSentence"> For this reason, it is prudent to set the current record position to a known location in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> after the <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> call.</caps:sentence>
            <caps:sentence sentenceid="2d8ad7dbad65fb03188c71c3c98eeb57" id="tgt11" class="tgtSentence"> For example, call the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5ad16b825b1eae53951d17dd19dd29c3" id="tgt12" class="tgtSentence">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, if a record has been deleted by another user), the provider returns warnings to the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection but does not halt program execution.</caps:sentence>
            <caps:sentence sentenceid="4c7f463f068ed0b730457239bf177224" id="tgt13" class="tgtSentence"> A run-time error occurs only if there are conflicts on all the requested records.</caps:sentence>
            <caps:sentence sentenceid="632f15094e3f3ced63aea77cfe3187a6" id="tgt14" class="tgtSentence"> Use the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property (<legacyBold>adFilterAffectedRecords</legacyBold>) and the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property to locate records with conflicts.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt15" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="41625f6f-e12d-4d8d-9f60-0729ce64c31e">Visual Basic Example</link>
        <link xlink:href="bcb1468e-18bb-41b8-8902-6ee05b786eec">Visual C++ Example</link>
        <link xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel Method</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method</link>
        <link xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType Property</link>
        <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Cancels a pending batch update.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>.<legacyBold>CancelBatch</legacyBold><parameterReference>AffectRecords</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>AffectRecords</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> An <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink> value that indicates how many records the <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> method will affect.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> method to cancel any pending updates in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> in batch update mode.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is in immediate update mode, calling <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> without <legacyBold>adAffectCurrent</legacyBold> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If you are editing the current record or are adding a new record when you call <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference>, ADO first calls the <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method to cancel any cached changes.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> After that, all pending changes in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> are canceled.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The current record may be indeterminable after a <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> call, especially if you were in the process of adding a new record.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> For this reason, it is prudent to set the current record position to a known location in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> after the <unmanagedCodeEntityReference>CancelBatch</unmanagedCodeEntityReference> call.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> For example, call the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, if a record has been deleted by another user), the provider returns warnings to the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection but does not halt program execution.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> A run-time error occurs only if there are conflicts on all the requested records.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> Use the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property (<legacyBold>adFilterAffectedRecords</legacyBold>) and the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property to locate records with conflicts.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="41625f6f-e12d-4d8d-9f60-0729ce64c31e">Visual Basic Example</link>
        <link xlink:href="bcb1468e-18bb-41b8-8902-6ee05b786eec">Visual C++ Example</link>
        <link xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel Method</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method</link>
        <link xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType Property</link>
        <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
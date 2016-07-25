---
title: "UpdateBatch Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 23f9314c-b027-4a51-aeae-50caa2977740
caps.latest.revision: 11
caps.handback.revision: 11
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
# UpdateBatch Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a493d8b88708449aab867bbb27b84fc6" id="tgt1" class="tgtSentence">Writes all pending batch updates to disk.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.UpdateBatch</legacyBold>
          <parameterReference>AffectRecords</parameterReference>, <parameterReference>PreserveStatus</parameterReference></legacySyntax>
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
                <caps:sentence sentenceid="69cc4d53d49865b5b87971a79d52fc9f" id="tgt4" class="tgtSentence"> An <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink> value that indicates how many records the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method will affect.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="0798b851e2fa52b417d0ec19f655d369" id="tgt5" class="tgtSentence">PreserveStatus </caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt6" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="747cc9b8adcb23fa82c1eff53c832853" id="tgt7" class="tgtSentence"> A <languageKeyword>Boolean</languageKeyword> value that specifies whether or not local changes, as indicated by the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property, should be committed.</caps:sentence>
                <caps:sentence sentenceid="dda38821fb57d2412227e81233366bfc" id="tgt8" class="tgtSentence"> If this value is set to <languageKeyword>True</languageKeyword>, the <unmanagedCodeEntityReference>Status</unmanagedCodeEntityReference> property of each record remains unchanged after the update is completed.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="abf8c637942328d4b2ac0854397df5a1" id="tgt9" class="tgtSentence">Use the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method when modifying a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object in batch update mode to transmit all changes made in a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object to the underlying database.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d1463ea48f576e9a3dcade48b5ccaba9" id="tgt10" class="tgtSentence">If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports batch updating, you can cache multiple changes to one or more records locally until you call the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method.</caps:sentence>
            <caps:sentence sentenceid="e0484f2898692ed6fbc2b3f078e59994" id="tgt11" class="tgtSentence"> If you are editing the current record or adding a new record when you call the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method, ADO will automatically call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method to save any pending changes to the current record before transmitting the batched changes to the provider.</caps:sentence>
            <caps:sentence sentenceid="49229c0081f97b058513479e4d10c42b" id="tgt12" class="tgtSentence"> You should use batch updating with either a keyset or static cursor only.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="e47cc6c98178c41e427c2ee424ecfe20" id="tgt13" class="tgtSentence">Specifying <legacyBold>adAffectGroup</legacyBold> as the value for this parameter will result in an error when there are no visible records in the current <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> (such as a filter for which no records match).</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="8af5325c654db61041a15a612e6bf97c" id="tgt14" class="tgtSentence">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection and a run-time error occurs.</caps:sentence>
            <caps:sentence sentenceid="632f15094e3f3ced63aea77cfe3187a6" id="tgt15" class="tgtSentence"> Use the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property (<legacyBold>adFilterAffectedRecords</legacyBold>) and the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property to locate records with conflicts.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5edea7cdfb9ce64da82daf8a576b9bed" id="tgt16" class="tgtSentence">To cancel all pending batch updates, use the <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="da37c23beeefa4bb529ae0aec58e0def" id="tgt17" class="tgtSentence">If the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> and <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink> dynamic properties are set, and the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is the result of executing a JOIN operation on multiple tables, then the execution of the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method is implicitly followed by the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method, depending on the settings of the <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="70cc0760ee6476cdaf22b6ebb496e837" id="tgt18" class="tgtSentence">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="1c75f865fc17de53371ebd229018024a" id="tgt19" class="tgtSentence"> Update order is dependent upon the provider.</caps:sentence>
            <caps:sentence sentenceid="a157d7a363766c8c9601cc3090861671" id="tgt20" class="tgtSentence"> Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt21" class="tgtSentence">Applies To</caps:sentence>
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
        <link xlink:href="8e8728aa-267f-4468-9a04-8bb29457995c">Visual J++ Example</link>
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method</link>
        <link xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType Property</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Writes all pending batch updates to disk.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.UpdateBatch</legacyBold>
          <parameterReference>AffectRecords</parameterReference>, <parameterReference>PreserveStatus</parameterReference></legacySyntax>
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
                <caps:sentence id="src4" class="srcSentence"> An <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink> value that indicates how many records the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method will affect.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src5" class="srcSentence">PreserveStatus </caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> A <languageKeyword>Boolean</languageKeyword> value that specifies whether or not local changes, as indicated by the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property, should be committed.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> If this value is set to <languageKeyword>True</languageKeyword>, the <unmanagedCodeEntityReference>Status</unmanagedCodeEntityReference> property of each record remains unchanged after the update is completed.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">Use the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method when modifying a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object in batch update mode to transmit all changes made in a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object to the underlying database.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports batch updating, you can cache multiple changes to one or more records locally until you call the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> If you are editing the current record or adding a new record when you call the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method, ADO will automatically call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method to save any pending changes to the current record before transmitting the batched changes to the provider.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> You should use batch updating with either a keyset or static cursor only.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence">Specifying <legacyBold>adAffectGroup</legacyBold> as the value for this parameter will result in an error when there are no visible records in the current <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> (such as a filter for which no records match).</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src14" class="srcSentence">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection and a run-time error occurs.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Use the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property (<legacyBold>adFilterAffectedRecords</legacyBold>) and the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property to locate records with conflicts.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">To cancel all pending batch updates, use the <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">If the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> and <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink> dynamic properties are set, and the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is the result of executing a JOIN operation on multiple tables, then the execution of the <unmanagedCodeEntityReference>UpdateBatch</unmanagedCodeEntityReference> method is implicitly followed by the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method, depending on the settings of the <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> Update order is dependent upon the provider.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Applies To</caps:sentence>
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
        <link xlink:href="8e8728aa-267f-4468-9a04-8bb29457995c">Visual J++ Example</link>
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method</link>
        <link xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType Property</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
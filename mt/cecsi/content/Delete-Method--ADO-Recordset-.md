---
title: "Delete Method (ADO Recordset)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 1eb9209c-602c-4507-b0c2-6527a599b67d
caps.latest.revision: 13
caps.handback.revision: 13
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
# Delete Method (ADO Recordset)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c3482f6e47cc7207c6bf21a13b228a8f" id="tgt1" class="tgtSentence">Deletes the current record or a group of records.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>.<legacyBold>Delete </legacyBold><parameterReference>AffectRecords</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="98a388e0912a0d881ac1f3ecb4016804" id="tgt2" class="tgtSentence"> <legacyItalic>AffectRecords</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="99ecbe1d2053654b9d5eb8a8a3151ce7" id="tgt3" class="tgtSentence">An <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink> value that determines how many records the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method will affect.</caps:sentence>
                <caps:sentence sentenceid="59cb35c92d41d273f904f8f6d62ec545" id="tgt4" class="tgtSentence"> The default value is <legacyBold>adAffectCurrent</legacyBold>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="d9c177bf23125b96d6a034a17a4b429d" id="tgt5" class="tgtSentence">
                    <legacyBold>adAffectAll</legacyBold> and <legacyBold>adAffectAllChapters</legacyBold> are not valid arguments to <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference>.</caps:sentence>
                </para>
              </alert>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="0c6f6d227c42100d58260a4edd20f79e" id="tgt6" class="tgtSentence">Using the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method marks the current record or a group of records in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object for deletion.</caps:sentence>
            <caps:sentence sentenceid="9096ee60ded359ad433cc6cddd6bd98d" id="tgt7" class="tgtSentence"> If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object doesn't allow record deletion, an error occurs.</caps:sentence>
            <caps:sentence sentenceid="83e4e3b322d8bc9bff149c3e5f16ae47" id="tgt8" class="tgtSentence"> If you are in immediate update mode, deletions occur in the database immediately.</caps:sentence>
            <caps:sentence sentenceid="f66f522e29cbedee5cbf193b468accdc" id="tgt9" class="tgtSentence"> If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="60df9a63d53bef3e93dd6e1b567f2829" id="tgt10" class="tgtSentence"> This means that you must cancel the update with <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> before moving off the current record (for example, with <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink>, <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, or <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="488d9e7fab62247e44011552c2297764" id="tgt11" class="tgtSentence">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="81b9238b5325ea039c634e94dac0b023" id="tgt12" class="tgtSentence"> Use the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property to view the deleted records.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c743d6d076e678f099575dd99329aebb" id="tgt13" class="tgtSentence">Retrieving field values from the deleted record generates an error.</caps:sentence>
            <caps:sentence sentenceid="24994ae595d4f14ba6a5f3d11058ca2d" id="tgt14" class="tgtSentence"> After deleting the current record, the deleted record remains current until you move to a different record.</caps:sentence>
            <caps:sentence sentenceid="9ce855a7b9de04fc4b00eba498f61191" id="tgt15" class="tgtSentence"> Once you move away from the deleted record, it is no longer accessible.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f951918da1a6e495ceb3180733b4c6bc" id="tgt16" class="tgtSentence">If you nest deletions in a transaction, you can recover deleted records with the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">RollbackTrans</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="0eaee7283039c90188dc08c620afc4f0" id="tgt17" class="tgtSentence"> If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="924eea102406d65bbe186bf612c1dc54" id="tgt18" class="tgtSentence">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection but does not halt program execution.</caps:sentence>
            <caps:sentence sentenceid="4c7f463f068ed0b730457239bf177224" id="tgt19" class="tgtSentence"> A run-time error occurs only if there are conflicts on all the requested records.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="328a94810369e9add066d960cd6eb16e" id="tgt20" class="tgtSentence">If the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> dynamic property is set, and the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is the result of executing a JOIN operation on multiple tables, then the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method will only delete rows from the table named in the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> property.</caps:sentence>
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
        <link xlink:href="0c80e71b-9e3f-4d05-ab2a-9e78798dad88">Visual Basic Example</link>
        <link xlink:href="78935d6d-1c1a-4306-a83a-1763210c69f9">VBScript Example</link>
        <link xlink:href="7cc78fb5-2701-49dc-bc22-06613b10cecb">Visual C++ Example</link>
        <link xlink:href="838c4bcb-bd78-4c98-a3ac-b8bf6e750db2">Visual J++ Example</link>
        <link xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">Delete Method (ADO Fields Collection)</link>
        <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
        <link xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Deletes the current record or a group of records.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>.<legacyBold>Delete </legacyBold><parameterReference>AffectRecords</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>AffectRecords</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">An <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink> value that determines how many records the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method will affect.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>adAffectCurrent</legacyBold>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src5" class="srcSentence">
                    <legacyBold>adAffectAll</legacyBold> and <legacyBold>adAffectAllChapters</legacyBold> are not valid arguments to <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference>.</caps:sentence>
                </para>
              </alert>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Using the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method marks the current record or a group of records in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object for deletion.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object doesn't allow record deletion, an error occurs.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> If you are in immediate update mode, deletions occur in the database immediately.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> This means that you must cancel the update with <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> before moving off the current record (for example, with <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink>, <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, or <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Use the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property to view the deleted records.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">Retrieving field values from the deleted record generates an error.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> After deleting the current record, the deleted record remains current until you move to a different record.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Once you move away from the deleted record, it is no longer accessible.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">If you nest deletions in a transaction, you can recover deleted records with the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">RollbackTrans</legacyLink> method.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection but does not halt program execution.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> A run-time error occurs only if there are conflicts on all the requested records.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">If the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> dynamic property is set, and the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is the result of executing a JOIN operation on multiple tables, then the <unmanagedCodeEntityReference>Delete</unmanagedCodeEntityReference> method will only delete rows from the table named in the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> property.</caps:sentence>
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
        <link xlink:href="0c80e71b-9e3f-4d05-ab2a-9e78798dad88">Visual Basic Example</link>
        <link xlink:href="78935d6d-1c1a-4306-a83a-1763210c69f9">VBScript Example</link>
        <link xlink:href="7cc78fb5-2701-49dc-bc22-06613b10cecb">Visual C++ Example</link>
        <link xlink:href="838c4bcb-bd78-4c98-a3ac-b8bf6e750db2">Visual J++ Example</link>
        <link xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">Delete Method (ADO Fields Collection)</link>
        <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
        <link xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
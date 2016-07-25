---
title: "Deleting Records Using the Delete Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bfed5cfa-7f57-463b-9da2-0c612a079d30
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
# Deleting Records Using the Delete Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e3be91220578d28a5d331704a20e5395" id="tgt1" class="tgtSentence">Using the <legacyBold>Delete</legacyBold> method marks the current record or a group of records in a <legacyBold>Recordset</legacyBold> object for deletion. If the <legacyBold>Recordset</legacyBold> object does not allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to <legacyBold>Update. </legacyBold>This means that you must cancel the update using <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> before moving off the current record (for example, using <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink>, <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, or <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4e51d7a6cdc3db2f61bd6e9469ba64d7" id="tgt2" class="tgtSentence">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the <legacyBold>UpdateBatch</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="e96db3fc3d5c33929e0bf344410a0340" id="tgt3" class="tgtSentence"> (To view the deleted records, set the <legacyBold>Filter</legacyBold> property to <legacyBold>adFilterAffectedRecords</legacyBold> after <legacyBold>Delete</legacyBold> is called.)</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="923e1dfdba643297d226772bc287a054" id="tgt4" class="tgtSentence">Attempting to retrieve field values from the deleted record generates an error.</caps:sentence>
          <caps:sentence sentenceid="24994ae595d4f14ba6a5f3d11058ca2d" id="tgt5" class="tgtSentence"> After deleting the current record, the deleted record remains current until you move to a different record.</caps:sentence>
          <caps:sentence sentenceid="9ce855a7b9de04fc4b00eba498f61191" id="tgt6" class="tgtSentence"> Once you move away from the deleted record, it is no longer accessible.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="93fd705edb2d5bba9d65d383c929872d" id="tgt7" class="tgtSentence">If you nest deletions in a transaction, you can recover deleted records by using the <legacyBold>RollbackTrans</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="787c5b82276941f5ddd213613027a0c2" id="tgt8" class="tgtSentence"> If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the <legacyBold>CancelBatch</legacyBold> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9506ea6e51eda971b9d6e7ca8ea12823" id="tgt9" class="tgtSentence">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the <legacyBold>Errors</legacyBold> collection but does not halt program execution.</caps:sentence>
          <caps:sentence sentenceid="4c7f463f068ed0b730457239bf177224" id="tgt10" class="tgtSentence"> A run-time error occurs only if there are conflicts on all the requested records.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e5e00402a03bc51bf0b800f94ec403a7" id="tgt11" class="tgtSentence">If the <legacyBold>Unique Table</legacyBold> dynamic property is set and the <legacyBold>Recordset</legacyBold> is the result of executing a JOIN operation on multiple tables, the <legacyBold>Delete</legacyBold> method will delete rows only from the table named in the <legacyBold>Unique Table</legacyBold> property.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b083e047e1462fb6544358a0f8607da9" id="tgt12" class="tgtSentence">The <legacyBold>Delete</legacyBold> method takes an optional argument that allows you to specify which records are affected by the <legacyBold>Delete</legacyBold> operation.</caps:sentence>
          <caps:sentence sentenceid="fdaba09bd3d7bac5f5c95c603820619c" id="tgt13" class="tgtSentence"> The only valid values for this argument are either of the following ADO <legacyBold>AffectEnum</legacyBold> enumerated constants:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="38462825c4b3af587a809a497518ba8e" id="tgt14" class="tgtSentence">             <legacyBold>adAffectCurrent   </legacyBold>Affects only the current record.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="fe877aa9f8f8ad075747b6435ef59b66" id="tgt15" class="tgtSentence">             <legacyBold>adAffectGroup   </legacyBold>Affects only records that satisfy the current <legacyBold>Filter</legacyBold> property setting.</caps:sentence>
              <caps:sentence sentenceid="56f4a8c51f723e97a022c323e163a70b" id="tgt16" class="tgtSentence"> The <legacyBold>Filter</legacyBold> property must be set to a <legacyBold>FilterGroupEnum</legacyBold> value or an array of <legacyBold>Bookmarks</legacyBold> to use this option.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="4e96ad8cc83a97f1c6083f99ce211ec0" id="tgt17" class="tgtSentence">The following code shows an example of specifying <legacyBold>adAffectGroup</legacyBold> when calling the <legacyBold>Delete</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="b117cd87139043aa77cee85588916f36" id="tgt18" class="tgtSentence"> This example adds some records to the sample <legacyBold>Recordset</legacyBold> and updates the database.</caps:sentence>
          <caps:sentence sentenceid="efe5dfbd9a5917e664aa5776b752761f" id="tgt19" class="tgtSentence"> Then it filters the <legacyBold>Recordset</legacyBold> using the <legacyBold>adFilterAffectedRecords</legacyBold> filter enumerated constant, which leaves only the newly added records visible in the <legacyBold>Recordset.</legacyBold> Finally, it calls the <legacyBold>Delete</legacyBold> method and specifies that all of the records that satisfy the current <legacyBold>Filter</legacyBold> property setting (the new records) should be deleted.</caps:sentence>
        </para>
        <code>'BeginDeleteGroup
    'add some bogus records
    With objRs
        For i = 0 To 8
            .AddNew
            .Fields("CompanyName") = "Shipper Number " &amp; i + 1
            .Fields("Phone") = "(425) 555-000" &amp; (i + 1)
            .Update
        Next i
        
        ' update
        .UpdateBatch
        
        'filter on newly added records
        .Filter = adFilterAffectedRecords
        Debug.Print "Deleting the " &amp; .RecordCount &amp; _
                    " records you just added."
        
        'delete the newly added bogus records
        .Delete adAffectGroup
        .Filter = adFilterNone
        Debug.Print .RecordCount &amp; " records remain."
    End With
'EndDeleteGroup</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Using the <legacyBold>Delete</legacyBold> method marks the current record or a group of records in a <legacyBold>Recordset</legacyBold> object for deletion. If the <legacyBold>Recordset</legacyBold> object does not allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to <legacyBold>Update. </legacyBold>This means that you must cancel the update using <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> before moving off the current record (for example, using <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink>, <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink>, or <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the <legacyBold>UpdateBatch</legacyBold> method.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> (To view the deleted records, set the <legacyBold>Filter</legacyBold> property to <legacyBold>adFilterAffectedRecords</legacyBold> after <legacyBold>Delete</legacyBold> is called.)</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">Attempting to retrieve field values from the deleted record generates an error.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> After deleting the current record, the deleted record remains current until you move to a different record.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Once you move away from the deleted record, it is no longer accessible.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">If you nest deletions in a transaction, you can recover deleted records by using the <legacyBold>RollbackTrans</legacyBold> method.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the <legacyBold>CancelBatch</legacyBold> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the <legacyBold>Errors</legacyBold> collection but does not halt program execution.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> A run-time error occurs only if there are conflicts on all the requested records.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">If the <legacyBold>Unique Table</legacyBold> dynamic property is set and the <legacyBold>Recordset</legacyBold> is the result of executing a JOIN operation on multiple tables, the <legacyBold>Delete</legacyBold> method will delete rows only from the table named in the <legacyBold>Unique Table</legacyBold> property.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">The <legacyBold>Delete</legacyBold> method takes an optional argument that allows you to specify which records are affected by the <legacyBold>Delete</legacyBold> operation.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> The only valid values for this argument are either of the following ADO <legacyBold>AffectEnum</legacyBold> enumerated constants:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">             <legacyBold>adAffectCurrent   </legacyBold>Affects only the current record.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">             <legacyBold>adAffectGroup   </legacyBold>Affects only records that satisfy the current <legacyBold>Filter</legacyBold> property setting.</caps:sentence>
              <caps:sentence id="src16" class="srcSentence"> The <legacyBold>Filter</legacyBold> property must be set to a <legacyBold>FilterGroupEnum</legacyBold> value or an array of <legacyBold>Bookmarks</legacyBold> to use this option.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src17" class="srcSentence">The following code shows an example of specifying <legacyBold>adAffectGroup</legacyBold> when calling the <legacyBold>Delete</legacyBold> method.</caps:sentence>
          <caps:sentence id="src18" class="srcSentence"> This example adds some records to the sample <legacyBold>Recordset</legacyBold> and updates the database.</caps:sentence>
          <caps:sentence id="src19" class="srcSentence"> Then it filters the <legacyBold>Recordset</legacyBold> using the <legacyBold>adFilterAffectedRecords</legacyBold> filter enumerated constant, which leaves only the newly added records visible in the <legacyBold>Recordset.</legacyBold> Finally, it calls the <legacyBold>Delete</legacyBold> method and specifies that all of the records that satisfy the current <legacyBold>Filter</legacyBold> property setting (the new records) should be deleted.</caps:sentence>
        </para>
        <code>'BeginDeleteGroup
    'add some bogus records
    With objRs
        For i = 0 To 8
            .AddNew
            .Fields("CompanyName") = "Shipper Number " &amp; i + 1
            .Fields("Phone") = "(425) 555-000" &amp; (i + 1)
            .Update
        Next i
        
        ' update
        .UpdateBatch
        
        'filter on newly added records
        .Filter = adFilterAffectedRecords
        Debug.Print "Deleting the " &amp; .RecordCount &amp; _
                    " records you just added."
        
        'delete the newly added bogus records
        .Delete adAffectGroup
        .Filter = adFilterNone
        Debug.Print .RecordCount &amp; " records remain."
    End With
'EndDeleteGroup</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
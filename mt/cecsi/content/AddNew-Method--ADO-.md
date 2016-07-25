---
title: "AddNew Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a9f54be9-5763-45d0-a6eb-09981b03bc08
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
# AddNew Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a293f06112b3bd98ce381b69883bb666" id="tgt1" class="tgtSentence">Creates a new record for an updatable <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
recordset.AddNew FieldList, Values</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="c1e71ce69bff36c1582c5f180ea9a4ff" id="tgt2" class="tgtSentence">recordset</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7210e9c9b35007dd06fe386a735520b7" id="tgt3" class="tgtSentence">A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="9edc365ea68a6254b2a8481f894539c5" id="tgt4" class="tgtSentence">FieldList</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt5" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="2070bf49fedd661434db8bff9ae9d43a" id="tgt6" class="tgtSentence"> A single name, or an array of names or ordinal positions of the fields in the new record.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="f09cc7ee3a9a93273f4b80601cafb00c" id="tgt7" class="tgtSentence">Values</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="8663ae8760364fe7b88d7dce28fd62db" id="tgt9" class="tgtSentence"> A single value, or an array of values for the fields in the new record.</caps:sentence>
                <caps:sentence sentenceid="e8e60a1a1121a4f2e08ccfb088ff470e" id="tgt10" class="tgtSentence"> If <legacyItalic>Fieldlist </legacyItalic>is an array, <legacyItalic>Values</legacyItalic> must also be an array with the same number of members; otherwise, an error occurs.</caps:sentence>
                <caps:sentence sentenceid="6d5f7dfe42c46001bb44fec1d817d720" id="tgt11" class="tgtSentence"> The order of field names must match the order of field values in each array.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4f41b841db75d5707c734894e1954ddf" id="tgt12" class="tgtSentence">Use the <legacyBold>AddNew</legacyBold> method to create and initialize a new record.</caps:sentence>
            <caps:sentence sentenceid="50ddf9321b68b322b49f9310c461a6f4" id="tgt13" class="tgtSentence"> Use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method with <legacyBold>adAddNew</legacyBold> (a <legacyLink xlink:href="4e10cda7-ce81-4466-94c2-844d38191cf1">CursorOptionEnum</legacyLink> value) to verify whether you can add records to the current <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="db1b1a96b5eb183f75fdcaf7f2dbb2f6" id="tgt14" class="tgtSentence">After you call the <legacyBold>AddNew</legacyBold> method, the new record becomes the current record and remains current after you call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="34ba42eaa59086db672eba2e15a1b8e1" id="tgt15" class="tgtSentence"> Since the new record is appended to the <legacyBold>Recordset</legacyBold>, a call to <legacyBold>MoveNext</legacyBold> following the Update will move past the end of the <legacyBold>Recordset</legacyBold>, making <legacyBold>EOF</legacyBold> True.</caps:sentence>
            <caps:sentence sentenceid="2168216de0aa3f5e500167e0617a10ad" id="tgt16" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> object does not support bookmarks, you may not be able to access the new record once you move to another record.</caps:sentence>
            <caps:sentence sentenceid="ce64b08fc50df2fa2dae7fdefeb18a21" id="tgt17" class="tgtSentence"> Depending on your cursor type, you may need to call the <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> method to make the new record accessible.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9dc9d6ab6669857c0fc597bcf3d40491" id="tgt18" class="tgtSentence">If you call <legacyBold>AddNew</legacyBold> while editing the current record or while adding a new record, ADO calls the <legacyBold>Update</legacyBold> method to save any changes and then creates the new record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4c8bc67e924a287904f71d49a4e83fdb" id="tgt19" class="tgtSentence">The behavior of the <legacyBold>AddNew</legacyBold> method depends on the updating mode of the <legacyBold>Recordset</legacyBold> object and whether you pass the <legacyItalic>Fieldlist</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cfe049e5e38b01f25c4b235e8fb6cb34" id="tgt20" class="tgtSentence">In <legacyItalic>immediate update mode</legacyItalic> (in which the provider writes changes to the underlying data source once you call the <legacyBold>Update</legacyBold> method), calling the <legacyBold>AddNew</legacyBold> method without arguments sets the <legacyLink xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">EditMode</legacyLink> property to <legacyBold>adEditAdd</legacyBold> (an <legacyLink xlink:href="45d54b6e-db2c-4553-9fd0-528147d6da2f">EditModeEnum</legacyLink> value).</caps:sentence>
            <caps:sentence sentenceid="169d1f869b196172745b8f23ccd01141" id="tgt21" class="tgtSentence"> The provider caches any field value changes locally.</caps:sentence>
            <caps:sentence sentenceid="4d961623399e6956bee481fcfda9243f" id="tgt22" class="tgtSentence"> Calling the <legacyBold>Update</legacyBold> method posts the new record to the database and resets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditNone</legacyBold> (an <legacyBold>EditModeEnum</legacyBold> value).</caps:sentence>
            <caps:sentence sentenceid="751a8ef2eb57bb2e75d88e955f28f8fd" id="tgt23" class="tgtSentence"> If you pass the <legacyItalic>Fieldlist</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments, ADO immediately posts the new record to the database (no <legacyBold>Update</legacyBold> call is necessary); the <legacyBold>EditMode</legacyBold> property value does not change (<legacyBold>adEditNone</legacyBold>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="738e4ef88e827d69dba82d82407ec0a9" id="tgt24" class="tgtSentence">In <legacyItalic>batch update mode</legacyItalic> (in which the provider caches multiple changes and writes them to the underlying data source only when you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method), calling the <legacyBold>AddNew</legacyBold> method without arguments sets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditAdd</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="169d1f869b196172745b8f23ccd01141" id="tgt25" class="tgtSentence"> The provider caches any field value changes locally.</caps:sentence>
            <caps:sentence sentenceid="4979f216ab31f52e94314a58a5909266" id="tgt26" class="tgtSentence"> Calling the <legacyBold>Update</legacyBold> method adds the new record to the current <legacyBold>Recordset</legacyBold>, but the provider does not post the changes to the underlying database, or reset the <legacyBold>EditMode</legacyBold> to <legacyBold>adEditNone</legacyBold>, until you call the <legacyBold>UpdateBatch</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="98a491e7f626aa0422ba944f24e87e18" id="tgt27" class="tgtSentence"> If you pass the <legacyItalic>Fieldlist</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments, ADO sends the new record to the provider for storage in a cache and sets the <legacyBold>EditMode</legacyBold> to <legacyBold>adEditAdd</legacyBold>; you need to call the <legacyBold>UpdateBatch</legacyBold> method to post the new record to the underlying database.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <codeExample>
        <description>
          <content>
            <para>
              <caps:sentence sentenceid="bf4ab5aec569004508f22835c507c427" id="tgt28" class="tgtSentence">The following example shows how to use the AddNew method with the field list and value list included, to see how to include the field list and value list as arrays.</caps:sentence>
            </para>
          </content>
        </description>
        <code>create table aa1 (intf int, charf char(10))
insert into aa1 values (2, 'aa')

Dim cn As New adodb.Connection
Dim rs As New adodb.Recordset
Dim cmd As New adodb.Command

cn.ConnectionString = "Provider=SQLOLEDB;Data Source=alexverb2;uid=sa;pwd=foo$bar00;"

cn.Open
rs.Open "select * from xxx..aa1", cn, adOpenKeyset, adLockOptimistic

Dim fieldsArray(1) As Variant
fieldsArray(0) = "intf"
fieldsArray(1) = "charf"
Dim values(1) As Variant
values(0) = 4
values(1) = "as"
rs.AddNew fieldsArray, values
rs.Update</code>
      </codeExample>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt29" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d439e097-65f3-471d-8799-5a1263beb3c1">Visual Basic Example</link>
        <link xlink:href="dcdcaf0a-b9b0-4d81-8728-43c38c4c853b">VBScript Example</link>
        <link xlink:href="9cc8774b-6711-4837-b442-959eaf79343e">Visual C++ Example</link>
        <link xlink:href="12856ffb-8645-4fad-b51f-2c2967677c01">Visual J++ Example</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">EditMode Property</link>
        <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
        <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Creates a new record for an updatable <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
recordset.AddNew FieldList, Values</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src2" class="srcSentence">recordset</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src4" class="srcSentence">FieldList</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> A single name, or an array of names or ordinal positions of the fields in the new record.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src7" class="srcSentence">Values</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> A single value, or an array of values for the fields in the new record.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> If <legacyItalic>Fieldlist </legacyItalic>is an array, <legacyItalic>Values</legacyItalic> must also be an array with the same number of members; otherwise, an error occurs.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> The order of field names must match the order of field values in each array.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Use the <legacyBold>AddNew</legacyBold> method to create and initialize a new record.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method with <legacyBold>adAddNew</legacyBold> (a <legacyLink xlink:href="4e10cda7-ce81-4466-94c2-844d38191cf1">CursorOptionEnum</legacyLink> value) to verify whether you can add records to the current <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">After you call the <legacyBold>AddNew</legacyBold> method, the new record becomes the current record and remains current after you call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Since the new record is appended to the <legacyBold>Recordset</legacyBold>, a call to <legacyBold>MoveNext</legacyBold> following the Update will move past the end of the <legacyBold>Recordset</legacyBold>, making <legacyBold>EOF</legacyBold> True.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> object does not support bookmarks, you may not be able to access the new record once you move to another record.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Depending on your cursor type, you may need to call the <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> method to make the new record accessible.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If you call <legacyBold>AddNew</legacyBold> while editing the current record or while adding a new record, ADO calls the <legacyBold>Update</legacyBold> method to save any changes and then creates the new record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">The behavior of the <legacyBold>AddNew</legacyBold> method depends on the updating mode of the <legacyBold>Recordset</legacyBold> object and whether you pass the <legacyItalic>Fieldlist</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">In <legacyItalic>immediate update mode</legacyItalic> (in which the provider writes changes to the underlying data source once you call the <legacyBold>Update</legacyBold> method), calling the <legacyBold>AddNew</legacyBold> method without arguments sets the <legacyLink xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">EditMode</legacyLink> property to <legacyBold>adEditAdd</legacyBold> (an <legacyLink xlink:href="45d54b6e-db2c-4553-9fd0-528147d6da2f">EditModeEnum</legacyLink> value).</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> The provider caches any field value changes locally.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Calling the <legacyBold>Update</legacyBold> method posts the new record to the database and resets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditNone</legacyBold> (an <legacyBold>EditModeEnum</legacyBold> value).</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> If you pass the <legacyItalic>Fieldlist</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments, ADO immediately posts the new record to the database (no <legacyBold>Update</legacyBold> call is necessary); the <legacyBold>EditMode</legacyBold> property value does not change (<legacyBold>adEditNone</legacyBold>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">In <legacyItalic>batch update mode</legacyItalic> (in which the provider caches multiple changes and writes them to the underlying data source only when you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method), calling the <legacyBold>AddNew</legacyBold> method without arguments sets the <legacyBold>EditMode</legacyBold> property to <legacyBold>adEditAdd</legacyBold>.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> The provider caches any field value changes locally.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> Calling the <legacyBold>Update</legacyBold> method adds the new record to the current <legacyBold>Recordset</legacyBold>, but the provider does not post the changes to the underlying database, or reset the <legacyBold>EditMode</legacyBold> to <legacyBold>adEditNone</legacyBold>, until you call the <legacyBold>UpdateBatch</legacyBold> method.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> If you pass the <legacyItalic>Fieldlist</legacyItalic> and <legacyItalic>Values</legacyItalic> arguments, ADO sends the new record to the provider for storage in a cache and sets the <legacyBold>EditMode</legacyBold> to <legacyBold>adEditAdd</legacyBold>; you need to call the <legacyBold>UpdateBatch</legacyBold> method to post the new record to the underlying database.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <codeExample>
        <description>
          <content>
            <para>
              <caps:sentence id="src28" class="srcSentence">The following example shows how to use the AddNew method with the field list and value list included, to see how to include the field list and value list as arrays.</caps:sentence>
            </para>
          </content>
        </description>
        <code>create table aa1 (intf int, charf char(10))
insert into aa1 values (2, 'aa')

Dim cn As New adodb.Connection
Dim rs As New adodb.Recordset
Dim cmd As New adodb.Command

cn.ConnectionString = "Provider=SQLOLEDB;Data Source=alexverb2;uid=sa;pwd=foo$bar00;"

cn.Open
rs.Open "select * from xxx..aa1", cn, adOpenKeyset, adLockOptimistic

Dim fieldsArray(1) As Variant
fieldsArray(0) = "intf"
fieldsArray(1) = "charf"
Dim values(1) As Variant
values(0) = 4
values(1) = "as"
rs.AddNew fieldsArray, values
rs.Update</code>
      </codeExample>
      <section>
        <title>
          <caps:sentence id="src29" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d439e097-65f3-471d-8799-5a1263beb3c1">Visual Basic Example</link>
        <link xlink:href="dcdcaf0a-b9b0-4d81-8728-43c38c4c853b">VBScript Example</link>
        <link xlink:href="9cc8774b-6711-4837-b442-959eaf79343e">Visual C++ Example</link>
        <link xlink:href="12856ffb-8645-4fad-b51f-2c2967677c01">Visual J++ Example</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">EditMode Property</link>
        <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
        <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
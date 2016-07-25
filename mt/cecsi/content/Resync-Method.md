---
title: "Resync Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 73b355d4-a4c0-434b-bfc4-039b1c76b32e
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
# Resync Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="536e2dd853652b1bb83bd252b06f05c9" id="tgt1" class="tgtSentence">Refreshes the data in the current <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, from the underlying database.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Recordset</parameterReference>
          <legacyBold>.Resync</legacyBold>
          <parameterReference>AffectRecords, ResyncValues</parameterReference>
          <parameterReference>Record.Fields</parameterReference>
          <legacyBold>.Resync</legacyBold>
          <parameterReference>ResyncValues</parameterReference>
        </legacySyntax>
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
                <caps:sentence sentenceid="514112eff8f908ea64edce9be6afe099" id="tgt4" class="tgtSentence"> An <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink> value that determines how many records the <legacyBold>Resync</legacyBold> method will affect.</caps:sentence>
                <caps:sentence sentenceid="21476e0137e68e002d81cdb4716fec2f" id="tgt5" class="tgtSentence"> The default value is <legacyBold>adAffectAll</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="dee6dbf2b33c71894f12eeb9920db436" id="tgt6" class="tgtSentence"> This value is not available with the <legacyBold>Resync</legacyBold> method of the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="3c1b1a346f3d28a4df27118dbd814d7d" id="tgt7" class="tgtSentence"> <legacyItalic>ResyncValues</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="791899129f52d978722fff862fe6f372" id="tgt9" class="tgtSentence"> A <legacyLink xlink:href="d3df2c90-e570-4c40-a79a-25b3448a009c">ResyncEnum</legacyLink> value that specifies whether underlying values are overwritten.</caps:sentence>
                <caps:sentence sentenceid="aad9ffbffe993024bb11fe63dc867693" id="tgt10" class="tgtSentence"> The default value is <legacyBold>adResyncAllValues</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="c1e71ce69bff36c1582c5f180ea9a4ff" id="tgt11" class="tgtSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="7e44c3500b9b45d582b8e0f83924c2cb" id="tgt12" class="tgtSentence">Use the <legacyBold>Resync</legacyBold> method to resynchronize records in the current <legacyBold>Recordset</legacyBold> with the underlying database.</caps:sentence>
                <caps:sentence sentenceid="61a10f5c442f04c1ea8378638c9f5442" id="tgt13" class="tgtSentence"> This is useful if you are using either a static or forward-only cursor, but you want to see any changes in the underlying database.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7af3c55159a9056a82ff61ba85c3cdf9" id="tgt14" class="tgtSentence">If you set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>, <legacyBold>Resync</legacyBold> is only available for non-read-only <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="14b26b341d4f5640a6d185fde6b09dba" id="tgt15" class="tgtSentence">Unlike the <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> method, the <legacyBold>Resync</legacyBold> method does not re-execute the <legacyBold>Recordset</legacyBold> object's underlying command.</caps:sentence>
                <caps:sentence sentenceid="a219d0e24953bdeb19d1a3cd3581bda5" id="tgt16" class="tgtSentence"> New records in the underlying database will not be visible.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="67692df51f9b34a903fe8b692b3c4878" id="tgt17" class="tgtSentence">If the attempt to resynchronize fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection and a run-time error occurs.</caps:sentence>
                <caps:sentence sentenceid="79c48d385e371b67301569286fcd75f8" id="tgt18" class="tgtSentence"> Use the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property (<legacyBold>adFilterConflictingRecords</legacyBold>) and the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property to locate records with conflicts.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="77d75182d6c7537af882358180dc1848" id="tgt19" class="tgtSentence">If the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> and <legacyLink xlink:href="4e2bb601-0fe8-4d61-b00e-38341d85a6bb">Resync Command</legacyLink> dynamic properties are set, and the <legacyBold>Recordset</legacyBold> is the result of executing a JOIN operation on multiple tables, then the <legacyBold>Resync</legacyBold> method will execute the command given in the <legacyBold>Resync Command</legacyBold> property only on the table named in the <legacyBold>Unique Table</legacyBold> property.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="d05b6ed7d2345020440df396d6da7f73" id="tgt20" class="tgtSentence">Fields</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="041ac4797ca9780adcf68263967f2f76" id="tgt21" class="tgtSentence">Use the <legacyBold>Resync</legacyBold> method to resynchronize the values of the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object with the underlying data source.</caps:sentence>
                <caps:sentence sentenceid="c0593d8ce835cbfdf724b885db51b4af" id="tgt22" class="tgtSentence"> The <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property is not affected by this method.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2060c261b29b67c1c352db1c3fd4f59b" id="tgt23" class="tgtSentence">If <legacyItalic>ResyncValues</legacyItalic> is set to <legacyBold>adResyncAllValues</legacyBold> (the default value), the <legacyLink xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue</legacyLink>, <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink>, and <legacyLink xlink:href="6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac">OriginalValue</legacyLink> properties of <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects in the collection are synchronized.</caps:sentence>
                <caps:sentence sentenceid="20fbcd8a88bfe0052c30f637555bde05" id="tgt24" class="tgtSentence"> If <legacyItalic>ResyncValues</legacyItalic> is set to <legacyBold>adResyncUnderlyingValues</legacyBold>, only the <legacyBold>UnderlyingValue</legacyBold> property is synchronized.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="da6cbe9fd6fbd2d32a9184bcbdaf3f7c" id="tgt25" class="tgtSentence">The value of the <legacyBold>Status</legacyBold> property for each <legacyBold>Field</legacyBold> object at the time of the call also affects the behavior of <legacyBold>Resync</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="300835d4ec2e00da08de2da41afbef66" id="tgt26" class="tgtSentence"> For <legacyBold>Field</legacyBold> objects that have <legacyBold>Status</legacyBold> values of <legacyBold>adFieldPendingUnknown</legacyBold> or <legacyBold>adFieldPendingInsert</legacyBold>, <legacyBold>Resync</legacyBold> has no effect.</caps:sentence>
                <caps:sentence sentenceid="6794a2253905a533b5216893f8771785" id="tgt27" class="tgtSentence"> For <legacyBold>Status</legacyBold> values of <legacyBold>adFieldPendingChange</legacyBold> or <legacyBold>adFieldPendingDelete</legacyBold>, <legacyBold>Resync</legacyBold> synchronizes data values for fields that still exist at the data source.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7b57d088e5e80e11eb8922f4b3d58344" id="tgt28" class="tgtSentence">
                  <legacyBold>Resync</legacyBold> will not modify <legacyBold>Status</legacyBold> values of <legacyBold>Field</legacyBold> objects unless an error occurs when <legacyBold>Resync</legacyBold> is called.</caps:sentence>
                <caps:sentence sentenceid="8b979d28988e8ba7db6031ca0ddb038b" id="tgt29" class="tgtSentence"> For example, if the field no longer exists, the provider will return an appropriate <legacyBold>Status</legacyBold> value for the <legacyBold>Field</legacyBold> object, such as <legacyBold>adFieldDoesNotExist</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="445cc4415197c805590662bb44c73d2d" id="tgt30" class="tgtSentence"> Returned <legacyBold>Status</legacyBold> values can be logically combined within the value of the <legacyBold>Status</legacyBold> property.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt31" class="tgtSentence">Applies To</caps:sentence>
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
        <link xlink:href="ab95315c-fe15-458c-9e0c-937ae5596592">Visual Basic Example</link>
        <link xlink:href="d34dfd26-9ca7-4c9c-a918-396f05fecca9">Visual C++ Example</link>
        <link xlink:href="0ef0ed20-83ac-4047-9294-506fd82f7201">Visual J++ Example</link>
        <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method</link>
        <link xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Refreshes the data in the current <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, from the underlying database.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Recordset</parameterReference>
          <legacyBold>.Resync</legacyBold>
          <parameterReference>AffectRecords, ResyncValues</parameterReference>
          <parameterReference>Record.Fields</parameterReference>
          <legacyBold>.Resync</legacyBold>
          <parameterReference>ResyncValues</parameterReference>
        </legacySyntax>
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
                <caps:sentence id="src4" class="srcSentence"> An <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink> value that determines how many records the <legacyBold>Resync</legacyBold> method will affect.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> The default value is <legacyBold>adAffectAll</legacyBold>.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> This value is not available with the <legacyBold>Resync</legacyBold> method of the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>ResyncValues</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> A <legacyLink xlink:href="d3df2c90-e570-4c40-a79a-25b3448a009c">ResyncEnum</legacyLink> value that specifies whether underlying values are overwritten.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> The default value is <legacyBold>adResyncAllValues</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src11" class="srcSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src12" class="srcSentence">Use the <legacyBold>Resync</legacyBold> method to resynchronize records in the current <legacyBold>Recordset</legacyBold> with the underlying database.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> This is useful if you are using either a static or forward-only cursor, but you want to see any changes in the underlying database.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src14" class="srcSentence">If you set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>, <legacyBold>Resync</legacyBold> is only available for non-read-only <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src15" class="srcSentence">Unlike the <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> method, the <legacyBold>Resync</legacyBold> method does not re-execute the <legacyBold>Recordset</legacyBold> object's underlying command.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> New records in the underlying database will not be visible.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src17" class="srcSentence">If the attempt to resynchronize fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection and a run-time error occurs.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> Use the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property (<legacyBold>adFilterConflictingRecords</legacyBold>) and the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property to locate records with conflicts.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src19" class="srcSentence">If the <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table</legacyLink> and <legacyLink xlink:href="4e2bb601-0fe8-4d61-b00e-38341d85a6bb">Resync Command</legacyLink> dynamic properties are set, and the <legacyBold>Recordset</legacyBold> is the result of executing a JOIN operation on multiple tables, then the <legacyBold>Resync</legacyBold> method will execute the command given in the <legacyBold>Resync Command</legacyBold> property only on the table named in the <legacyBold>Unique Table</legacyBold> property.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src20" class="srcSentence">Fields</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src21" class="srcSentence">Use the <legacyBold>Resync</legacyBold> method to resynchronize the values of the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object with the underlying data source.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> The <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property is not affected by this method.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src23" class="srcSentence">If <legacyItalic>ResyncValues</legacyItalic> is set to <legacyBold>adResyncAllValues</legacyBold> (the default value), the <legacyLink xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue</legacyLink>, <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink>, and <legacyLink xlink:href="6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac">OriginalValue</legacyLink> properties of <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects in the collection are synchronized.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> If <legacyItalic>ResyncValues</legacyItalic> is set to <legacyBold>adResyncUnderlyingValues</legacyBold>, only the <legacyBold>UnderlyingValue</legacyBold> property is synchronized.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src25" class="srcSentence">The value of the <legacyBold>Status</legacyBold> property for each <legacyBold>Field</legacyBold> object at the time of the call also affects the behavior of <legacyBold>Resync</legacyBold>.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> For <legacyBold>Field</legacyBold> objects that have <legacyBold>Status</legacyBold> values of <legacyBold>adFieldPendingUnknown</legacyBold> or <legacyBold>adFieldPendingInsert</legacyBold>, <legacyBold>Resync</legacyBold> has no effect.</caps:sentence>
                <caps:sentence id="src27" class="srcSentence"> For <legacyBold>Status</legacyBold> values of <legacyBold>adFieldPendingChange</legacyBold> or <legacyBold>adFieldPendingDelete</legacyBold>, <legacyBold>Resync</legacyBold> synchronizes data values for fields that still exist at the data source.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src28" class="srcSentence">
                  <legacyBold>Resync</legacyBold> will not modify <legacyBold>Status</legacyBold> values of <legacyBold>Field</legacyBold> objects unless an error occurs when <legacyBold>Resync</legacyBold> is called.</caps:sentence>
                <caps:sentence id="src29" class="srcSentence"> For example, if the field no longer exists, the provider will return an appropriate <legacyBold>Status</legacyBold> value for the <legacyBold>Field</legacyBold> object, such as <legacyBold>adFieldDoesNotExist</legacyBold>.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> Returned <legacyBold>Status</legacyBold> values can be logically combined within the value of the <legacyBold>Status</legacyBold> property.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src31" class="srcSentence">Applies To</caps:sentence>
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
        <link xlink:href="ab95315c-fe15-458c-9e0c-937ae5596592">Visual Basic Example</link>
        <link xlink:href="d34dfd26-9ca7-4c9c-a918-396f05fecca9">Visual C++ Example</link>
        <link xlink:href="0ef0ed20-83ac-4047-9294-506fd82f7201">Visual J++ Example</link>
        <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method</link>
        <link xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
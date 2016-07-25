---
title: "GetRows Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 14b92860-4171-47d9-a413-dd60dd6a8880
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
# GetRows Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a516a3abced356e2766e514f5fea4c5f" id="tgt1" class="tgtSentence">Retrieves multiple records of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object into an array.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>array</parameterReference> = <parameterReference>recordset</parameterReference><legacyBold>.GetRows(</legacyBold><parameterReference>Rows</parameterReference><legacyBold>, </legacyBold><parameterReference>Start</parameterReference><legacyBold>, </legacyBold><parameterReference>Fields </parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="9fd8005ddf92ae9ab0902986b3e2015b" id="tgt2" class="tgtSentence">Returns a <languageKeyword>Variant</languageKeyword> whose value is a two-dimensional array.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="922eff7803dd1db7a50fbbdb89509358" id="tgt3" class="tgtSentence"> <legacyItalic>Rows</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt4" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="e678940472a940c6072c74a54fd906de" id="tgt5" class="tgtSentence"> A <legacyLink xlink:href="adc109b9-79f4-4946-a5eb-658e22e9a8a5">GetRowsOptionEnum</legacyLink> value that indicates the number of records to retrieve.</caps:sentence>
                <caps:sentence sentenceid="4d18fab97461c5924f8549252db26d4e" id="tgt6" class="tgtSentence"> The default is <legacyBold>adGetRowsRest</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="922ed5a49d50fca828b4bba43d2f705e" id="tgt7" class="tgtSentence"> <legacyItalic>Start</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="ec753acadbe14ec650c50079c10b0a15" id="tgt9" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value or <languageKeyword>Variant</languageKeyword> that evaluates to the bookmark for the record from which the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> operation should begin.</caps:sentence>
                <caps:sentence sentenceid="80aa3459d9b3cadc111520375fbb4ef6" id="tgt10" class="tgtSentence"> You can also use a <legacyLink xlink:href="55d273c4-ccee-48ef-ba90-8893d04313c8">BookmarkEnum</legacyLink> value.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8bddbd1d644449f57c976b7c137a00a3" id="tgt11" class="tgtSentence"> <legacyItalic>Fields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt12" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="a1d25f8385d460af20ccb013523c82d6" id="tgt13" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> that represents a single field name or ordinal position, or an array of field names or ordinal position numbers.</caps:sentence>
                <caps:sentence sentenceid="4574b1a89d1ce684bb91ea9f9e9a57d4" id="tgt14" class="tgtSentence"> ADO returns only the data in these fields.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7bb31d8c88f1e3b9c17bfc9689f0ca8f" id="tgt15" class="tgtSentence">Use the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> method to copy records from a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> into a two-dimensional array.</caps:sentence>
            <caps:sentence sentenceid="cf6420ef818e9d4a476f5a4cb6b286f0" id="tgt16" class="tgtSentence"> The first subscript identifies the field and the second identifies the record number.</caps:sentence>
            <caps:sentence sentenceid="12f1e9fed6ebe2ce23500d9928ea8bfa" id="tgt17" class="tgtSentence"> The <legacyItalic>array</legacyItalic> variable is automatically dimensioned to the correct size when the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> method returns the data.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f6fc0ef3ba8fde403ca5278e00294b20" id="tgt18" class="tgtSentence">If you do not specify a value for the <legacyItalic>Rows</legacyItalic> argument, the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> method automatically retrieves all the records in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="aa703ad2f12b30d58c669b781ac57acd" id="tgt19" class="tgtSentence"> If you request more records than are available, <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> returns only the number of available records.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e2df4d1c81db1f0e4dd383b491a6aebb" id="tgt20" class="tgtSentence">If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports bookmarks, you can specify at which record the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> method should begin retrieving data by passing the value of that record's <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink> property in the <legacyItalic>Start</legacyItalic> argument.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="196c6cf792ea159b9d661949c5669533" id="tgt21" class="tgtSentence">If you want to restrict the fields that the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> call returns, you can pass either a single field name/number or an array of field names/numbers in the <legacyItalic>Fields</legacyItalic> argument.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9f06fa7b8ae762cc747e959519505bb5" id="tgt22" class="tgtSentence">After you call <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference>, the next unread record becomes the current record, or the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> property is set to <languageKeyword>True</languageKeyword> if there are no more records.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt23" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="9f7c78bb-7bb8-4c4f-8e5a-4d3bfc8a208f">Visual Basic Example</link>
        <link xlink:href="08e5c5bf-f7de-4bf9-97a9-f214c128ad8c">Visual C++ Example</link>
        <link xlink:href="44dde820-9596-439c-97a8-037d40d873f0">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Retrieves multiple records of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object into an array.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>array</parameterReference> = <parameterReference>recordset</parameterReference><legacyBold>.GetRows(</legacyBold><parameterReference>Rows</parameterReference><legacyBold>, </legacyBold><parameterReference>Start</parameterReference><legacyBold>, </legacyBold><parameterReference>Fields </parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <languageKeyword>Variant</languageKeyword> whose value is a two-dimensional array.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>Rows</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> A <legacyLink xlink:href="adc109b9-79f4-4946-a5eb-658e22e9a8a5">GetRowsOptionEnum</legacyLink> value that indicates the number of records to retrieve.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> The default is <legacyBold>adGetRowsRest</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>Start</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> A <languageKeyword>String</languageKeyword> value or <languageKeyword>Variant</languageKeyword> that evaluates to the bookmark for the record from which the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> operation should begin.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> You can also use a <legacyLink xlink:href="55d273c4-ccee-48ef-ba90-8893d04313c8">BookmarkEnum</legacyLink> value.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src11" class="srcSentence"> <legacyItalic>Fields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src12" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> that represents a single field name or ordinal position, or an array of field names or ordinal position numbers.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> ADO returns only the data in these fields.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">Use the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> method to copy records from a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> into a two-dimensional array.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> The first subscript identifies the field and the second identifies the record number.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> The <legacyItalic>array</legacyItalic> variable is automatically dimensioned to the correct size when the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> method returns the data.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If you do not specify a value for the <legacyItalic>Rows</legacyItalic> argument, the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> method automatically retrieves all the records in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> If you request more records than are available, <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> returns only the number of available records.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports bookmarks, you can specify at which record the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> method should begin retrieving data by passing the value of that record's <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink> property in the <legacyItalic>Start</legacyItalic> argument.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">If you want to restrict the fields that the <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference> call returns, you can pass either a single field name/number or an array of field names/numbers in the <legacyItalic>Fields</legacyItalic> argument.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">After you call <unmanagedCodeEntityReference>GetRows</unmanagedCodeEntityReference>, the next unread record becomes the current record, or the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> property is set to <languageKeyword>True</languageKeyword> if there are no more records.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="9f7c78bb-7bb8-4c4f-8e5a-4d3bfc8a208f">Visual Basic Example</link>
        <link xlink:href="08e5c5bf-f7de-4bf9-97a9-f214c128ad8c">Visual C++ Example</link>
        <link xlink:href="44dde820-9596-439c-97a8-037d40d873f0">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
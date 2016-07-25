---
title: "Save Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5
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
# Save Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1fd25abbd55baca935b635b9a81dc982" id="tgt1" class="tgtSentence">Saves the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> in a file or <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
recordset.Save Destination, PersistFormat</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="004d43c096763731c9a280248b72895c" id="tgt2" class="tgtSentence"> <legacyItalic>Destination</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="32beb723ae316caeb878bf4ea78da24c" id="tgt4" class="tgtSentence"> A <legacyBold>Variant</legacyBold> that represents the complete path name of the file where the <legacyBold>Recordset</legacyBold> is to be saved, or a reference to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="910b705b366aa250079d326bea3b9aa1" id="tgt5" class="tgtSentence"> <legacyItalic>PersistFormat</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt6" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="7cdbc0f4d1220b59b1dd5b672940fae7" id="tgt7" class="tgtSentence"> A <link xlink:href="ebe1a2ab-e9f1-43a2-8f94-b190c9613d70">PersistFormatEnum</link> value that specifies the format in which the <legacyBold>Recordset</legacyBold> is to be saved (XML or ADTG).</caps:sentence>
                <caps:sentence sentenceid="9c251141e91a8544cdd885dce81a230b" id="tgt8" class="tgtSentence"> The default value is <legacyBold>adPersistADTG</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4e9655c01ec3d813554877fcf6b7b367" id="tgt9" class="tgtSentence">The <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link> method can only be invoked on an open <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="509e4847a09d5dbe2eeb530817ca03ea" id="tgt10" class="tgtSentence"> Use the <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> method to later restore the <legacyBold>Recordset</legacyBold> from <legacyItalic>Destination</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a32f31b8e1df61a56a9f9578696c434c" id="tgt11" class="tgtSentence">If the <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link> property is in effect for the <legacyBold>Recordset</legacyBold>, then only the rows accessible under the filter are saved.</caps:sentence>
            <caps:sentence sentenceid="82c74918f14b3b5dd7fc3d909562c166" id="tgt12" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> is hierarchical, then the current child <legacyBold>Recordset</legacyBold> and its children are saved, including the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="8f6b742cc0ad532f1ebb6a0df8025803" id="tgt13" class="tgtSentence"> If the Save method of a child <legacyBold>Recordset</legacyBold> is called, the child and all its children are saved, but the parent is not.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b7a4f26c39ec1397c58b454f5b75d7f4" id="tgt14" class="tgtSentence">The first time you save the <legacyBold>Recordset</legacyBold>, it is optional to specify <legacyItalic>Destination</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="9f29e42f6f99041922e85a78689a68a6" id="tgt15" class="tgtSentence"> If you omit <legacyItalic>Destination</legacyItalic>, a new file will be created with a name set to the value of the Source property of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="745b549e1ed6b6c883d9b22fe6c1a335" id="tgt16" class="tgtSentence">Omit <legacyItalic>Destination</legacyItalic> when you subsequently call <legacyBold>Save</legacyBold> after the first save, or a run-time error will occur.</caps:sentence>
            <caps:sentence sentenceid="4bbe8ea404e0077f6f66fa33de61e12e" id="tgt17" class="tgtSentence"> If you subsequently call <legacyBold>Save</legacyBold> with a new <legacyItalic>Destination</legacyItalic>, the <legacyBold>Recordset</legacyBold> is saved to the new destination.</caps:sentence>
            <caps:sentence sentenceid="0eda93c474a67f72e5ac3a8167b870e3" id="tgt18" class="tgtSentence"> However, the new destination and the original destination will both be open.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="41ab5bb8bff382d351ee9b6748e27a58" id="tgt19" class="tgtSentence">
              <legacyBold>Save</legacyBold> does not close the <legacyBold>Recordset</legacyBold> or <legacyItalic>Destination</legacyItalic>, so you can continue to work with the <legacyBold>Recordset</legacyBold> and save your most recent changes.</caps:sentence>
            <caps:sentence sentenceid="d7a5eb4e11f502865df05e31ce87ef0e" id="tgt20" class="tgtSentence">
              <legacyItalic>Destination</legacyItalic> remains open until the <legacyBold>Recordset</legacyBold> is closed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="aa699234cef3f01464f3a95f702a4fcf" id="tgt21" class="tgtSentence">For reasons of security, the <legacyBold>Save</legacyBold> method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c4ec459a8e74e1efc2614dde544b298d" id="tgt22" class="tgtSentence">If the <legacyBold>Save</legacyBold> method is called while an asynchronous <legacyBold>Recordset</legacyBold> fetch, execute, or update operation is in progress, then <legacyBold>Save</legacyBold> waits until the asynchronous operation is complete.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="054e595288959f8394d9cb46f621cc4f" id="tgt23" class="tgtSentence">Records are saved beginning with the first row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="dcf57846fd56bf9fee700c653654b226" id="tgt24" class="tgtSentence"> When the <legacyBold>Save</legacyBold> method is finished, the current row position is moved to the first row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e84f019323fb57c5befccf977190f239" id="tgt25" class="tgtSentence">For best results, set the <link xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation Property (ADO)</link> property to <legacyBold>adUseClient</legacyBold> with <legacyBold>Save</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="afd5045f9e5c1354100ecbb831500e1a" id="tgt26" class="tgtSentence"> If your provider does not support all of the functionality necessary to save <legacyBold>Recordset</legacyBold> objects, the Cursor Service will provide that functionality.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="01665ce6b9b63e3e8d78218a2473dd80" id="tgt27" class="tgtSentence">When a <legacyBold>Recordset</legacyBold> is persisted with the <legacyBold>CursorLocation</legacyBold> property set to <legacyBold>adUseServer</legacyBold>, the update capability for the <legacyBold>Recordset</legacyBold> is limited.</caps:sentence>
            <caps:sentence sentenceid="160b4735c9ce7dc53d6bc4c2664b4372" id="tgt28" class="tgtSentence"> Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality).</caps:sentence>
            <caps:sentence sentenceid="dc5f56b61737d7921ff8b910a2e5be1f" id="tgt29" class="tgtSentence"> The <link xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync Method</link> method is also unavailable in this configuration.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d058ba8c532dd20395da7fc3eaac854f" id="tgt30" class="tgtSentence">Saving a <legacyBold>Recordset</legacyBold> with <legacyBold>Fields</legacyBold> of type <legacyBold>adVariant</legacyBold>, <legacyBold>adIDispatch</legacyBold>, or <legacyBold>adIUnknown</legacyBold> is not supported by ADO and can cause unpredictable results.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="d132af0ac02b67da8e206eb32da85994" id="tgt31" class="tgtSentence">Only Filters in the form of Criteria Strings (e.g. OrderDate &gt; '12/31/1999') affect the contents of a persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="7e4c09dbf8789ac1a7e08bd8783b7737" id="tgt32" class="tgtSentence"> Filters created with an Array of <legacyBold>Bookmarks</legacyBold> or using a value from the <link xlink:href="b22e725e-84bd-4286-a070-290c278c3783">FilterGroupEnum</link> will not affect the contents of the persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="80a871dc71d031e14d1fbd28e20611df" id="tgt33" class="tgtSentence"> These rules apply to <legacyBold>Recordset</legacyBold>s created with either client-side or server-side cursors.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="43a57e3cbd66fa8764bad438b171e28c" id="tgt34" class="tgtSentence">Because the <legacyItalic>Destination</legacyItalic> parameter can accept any object that supports the OLE DB IStream interface, you can save a <legacyBold>Recordset</legacyBold> directly to the ASP Response object.</caps:sentence>
            <caps:sentence sentenceid="d03a20173dab58fe7860c1e44649a399" id="tgt35" class="tgtSentence"> For more details, please see the <legacyBold>XML Recordset Persistence Scenario</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8d46b5487ba3a63cd7608a9c2ac3ca62" id="tgt36" class="tgtSentence">You can also save a <legacyBold>Recordset</legacyBold> in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</caps:sentence>
          </para>
          <code>Dim xDOM As New MSXML.DOMDocument
Dim rsXML As New ADODB.Recordset
Dim sSQL As String, sConn As String

sSQL = "SELECT customerid, companyname, contactname FROM customers"
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"
rsXML.Open sSQL, sConn
rsXML.Save xDOM, adPersistXML   'Save Recordset directly into a DOM tree.
...</code>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="7b840565f37c7e3d7e24b0b4ce21d483" id="tgt37" class="tgtSentence">Two limitations apply when saving hierarchical Recordsets (data shapes) in XML format.</caps:sentence>
              <caps:sentence sentenceid="8ba9d90e3a52d6a9e40cf29cad79d738" id="tgt38" class="tgtSentence"> You cannot save into XML if the hierarchical <legacyBold>Recordset</legacyBold> contains pending updates, and you cannot save a parameterized hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="296adda22b332187b789196f8c5b2a77" id="tgt39" class="tgtSentence">A <legacyBold>Recordset</legacyBold> saved in XML format is saved using UTF-8 format.</caps:sentence>
            <caps:sentence sentenceid="72d9805f94241c47c46de20aff78ba32" id="tgt40" class="tgtSentence"> When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a <legacyBold>Recordset</legacyBold> from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt41" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object_ADO</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ddccdf58-9c57-4c9b-8b7f-0cf193f955fb">Save and Open Methods Example (VB)</link>
        <link xlink:href="334ae655-8cac-48e6-8d00-1d28f3436e1e">Save and Open Methods Example (VC++)</link>
        <link xlink:href="bc425816-ecf8-4739-b50e-4cd5c60a151c">Save and Open Methods Example (VJ++)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Saves the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> in a file or <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
recordset.Save Destination, PersistFormat</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Destination</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A <legacyBold>Variant</legacyBold> that represents the complete path name of the file where the <legacyBold>Recordset</legacyBold> is to be saved, or a reference to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>PersistFormat</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> A <link xlink:href="ebe1a2ab-e9f1-43a2-8f94-b190c9613d70">PersistFormatEnum</link> value that specifies the format in which the <legacyBold>Recordset</legacyBold> is to be saved (XML or ADTG).</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> The default value is <legacyBold>adPersistADTG</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link> method can only be invoked on an open <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Use the <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link> method to later restore the <legacyBold>Recordset</legacyBold> from <legacyItalic>Destination</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If the <link xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter Property</link> property is in effect for the <legacyBold>Recordset</legacyBold>, then only the rows accessible under the filter are saved.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> is hierarchical, then the current child <legacyBold>Recordset</legacyBold> and its children are saved, including the parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> If the Save method of a child <legacyBold>Recordset</legacyBold> is called, the child and all its children are saved, but the parent is not.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">The first time you save the <legacyBold>Recordset</legacyBold>, it is optional to specify <legacyItalic>Destination</legacyItalic>.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> If you omit <legacyItalic>Destination</legacyItalic>, a new file will be created with a name set to the value of the Source property of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">Omit <legacyItalic>Destination</legacyItalic> when you subsequently call <legacyBold>Save</legacyBold> after the first save, or a run-time error will occur.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> If you subsequently call <legacyBold>Save</legacyBold> with a new <legacyItalic>Destination</legacyItalic>, the <legacyBold>Recordset</legacyBold> is saved to the new destination.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> However, the new destination and the original destination will both be open.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">
              <legacyBold>Save</legacyBold> does not close the <legacyBold>Recordset</legacyBold> or <legacyItalic>Destination</legacyItalic>, so you can continue to work with the <legacyBold>Recordset</legacyBold> and save your most recent changes.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence">
              <legacyItalic>Destination</legacyItalic> remains open until the <legacyBold>Recordset</legacyBold> is closed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">For reasons of security, the <legacyBold>Save</legacyBold> method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">If the <legacyBold>Save</legacyBold> method is called while an asynchronous <legacyBold>Recordset</legacyBold> fetch, execute, or update operation is in progress, then <legacyBold>Save</legacyBold> waits until the asynchronous operation is complete.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">Records are saved beginning with the first row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> When the <legacyBold>Save</legacyBold> method is finished, the current row position is moved to the first row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">For best results, set the <link xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation Property (ADO)</link> property to <legacyBold>adUseClient</legacyBold> with <legacyBold>Save</legacyBold>.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> If your provider does not support all of the functionality necessary to save <legacyBold>Recordset</legacyBold> objects, the Cursor Service will provide that functionality.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">When a <legacyBold>Recordset</legacyBold> is persisted with the <legacyBold>CursorLocation</legacyBold> property set to <legacyBold>adUseServer</legacyBold>, the update capability for the <legacyBold>Recordset</legacyBold> is limited.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality).</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> The <link xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync Method</link> method is also unavailable in this configuration.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src30" class="srcSentence">Saving a <legacyBold>Recordset</legacyBold> with <legacyBold>Fields</legacyBold> of type <legacyBold>adVariant</legacyBold>, <legacyBold>adIDispatch</legacyBold>, or <legacyBold>adIUnknown</legacyBold> is not supported by ADO and can cause unpredictable results.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src31" class="srcSentence">Only Filters in the form of Criteria Strings (e.g. OrderDate &gt; '12/31/1999') affect the contents of a persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> Filters created with an Array of <legacyBold>Bookmarks</legacyBold> or using a value from the <link xlink:href="b22e725e-84bd-4286-a070-290c278c3783">FilterGroupEnum</link> will not affect the contents of the persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> These rules apply to <legacyBold>Recordset</legacyBold>s created with either client-side or server-side cursors.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src34" class="srcSentence">Because the <legacyItalic>Destination</legacyItalic> parameter can accept any object that supports the OLE DB IStream interface, you can save a <legacyBold>Recordset</legacyBold> directly to the ASP Response object.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> For more details, please see the <legacyBold>XML Recordset Persistence Scenario</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src36" class="srcSentence">You can also save a <legacyBold>Recordset</legacyBold> in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</caps:sentence>
          </para>
          <code>Dim xDOM As New MSXML.DOMDocument
Dim rsXML As New ADODB.Recordset
Dim sSQL As String, sConn As String

sSQL = "SELECT customerid, companyname, contactname FROM customers"
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"
rsXML.Open sSQL, sConn
rsXML.Save xDOM, adPersistXML   'Save Recordset directly into a DOM tree.
...</code>
          <alert class="note">
            <para>
              <caps:sentence id="src37" class="srcSentence">Two limitations apply when saving hierarchical Recordsets (data shapes) in XML format.</caps:sentence>
              <caps:sentence id="src38" class="srcSentence"> You cannot save into XML if the hierarchical <legacyBold>Recordset</legacyBold> contains pending updates, and you cannot save a parameterized hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src39" class="srcSentence">A <legacyBold>Recordset</legacyBold> saved in XML format is saved using UTF-8 format.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a <legacyBold>Recordset</legacyBold> from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src41" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object_ADO</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ddccdf58-9c57-4c9b-8b7f-0cf193f955fb">Save and Open Methods Example (VB)</link>
        <link xlink:href="334ae655-8cac-48e6-8d00-1d28f3436e1e">Save and Open Methods Example (VC++)</link>
        <link xlink:href="bc425816-ecf8-4739-b50e-4cd5c60a151c">Save and Open Methods Example (VJ++)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
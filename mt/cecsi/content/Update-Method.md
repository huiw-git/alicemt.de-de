---
title: "Update Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6b2a9c31-1a7e-40db-8a53-30720d0f6cc1
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
# Update Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="211b8a73c6f40313029363b2a2bdae37" id="tgt1" class="tgtSentence">Saves any changes you make to the current row of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.Update</legacyBold>
          <parameterReference>Fields</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Values</parameterReference>
          <parameterReference>record.Fields</parameterReference>
          <legacyBold>.Update</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="8bddbd1d644449f57c976b7c137a00a3" id="tgt2" class="tgtSentence"> <legacyItalic>Fields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="73027d9666dc5db0c921fcb11a335962" id="tgt4" class="tgtSentence"> A <legacyBold>Variant</legacyBold> that represents a single name, or a <legacyBold>Variant</legacyBold> array that represents names or ordinal positions of the field or fields you wish to modify.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="61722c2e1a284b5242344daad55553bf" id="tgt5" class="tgtSentence"> <legacyItalic>Values</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt6" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="01539cbb9b7d444db9fbdaca15279541" id="tgt7" class="tgtSentence"> A <legacyBold>Variant</legacyBold> that represents a single value, or a <legacyBold>Variant</legacyBold> array that represents values for the field or fields in the new record.</caps:sentence>
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
              <caps:sentence sentenceid="c1e71ce69bff36c1582c5f180ea9a4ff" id="tgt8" class="tgtSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9fc70c50e84019f78c547fb285cc3c44" id="tgt9" class="tgtSentence">Use the <legacyBold>Update</legacyBold> method to save any changes you make to the current record of a <legacyBold>Recordset</legacyBold> object since calling the <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink> method or since changing any field values in an existing record.</caps:sentence>
                <caps:sentence sentenceid="80b6f8ecc21600414fdaeea6d6bd3498" id="tgt10" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> object must support updates.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ece5f2dd2586753bcd6dd43bd8b4a6a2" id="tgt11" class="tgtSentence">To set field values, do one of the following:  </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cc6df3ec127298c08677594a17a112bf" id="tgt12" class="tgtSentence">Assign values to a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object's <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property and call the <legacyBold>Update</legacyBold> method.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="49add96fc3ad53e6b1631bbc86b47687" id="tgt13" class="tgtSentence">Pass a field name and a value as arguments with the <legacyBold>Update</legacyBold> call.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e3fd72aa80c95e1c8f014a4be01fb94d" id="tgt14" class="tgtSentence">Pass an array of field names and an array of values with the <legacyBold>Update</legacyBold> call.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="de5714ef33ea7a9405bc379fe8bc4610" id="tgt15" class="tgtSentence">When you use arrays of fields and values, there must be an equal number of elements in both arrays.</caps:sentence>
                <caps:sentence sentenceid="943cd835c0be82f856f6b6937058a49e" id="tgt16" class="tgtSentence"> Also, the order of field names must match the order of field values.</caps:sentence>
                <caps:sentence sentenceid="54966b1ae90c0d2c01368431ef02bb4f" id="tgt17" class="tgtSentence"> If the number and order of fields and values do not match, an error occurs.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a6e3f3660ed1c5c76870392f194c58c8" id="tgt18" class="tgtSentence">If the <legacyBold>Recordset</legacyBold> object supports batch updating, you can cache multiple changes to one or more records locally until you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method.</caps:sentence>
                <caps:sentence sentenceid="2f4896cabc48816935578cf0273dd102" id="tgt19" class="tgtSentence"> If you are editing the current record or adding a new record when you call the <legacyBold>UpdateBatch</legacyBold> method, ADO will automatically call the <legacyBold>Update</legacyBold> method to save any pending changes to the current record before transmitting the batched changes to the provider.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b51a087f6325960ab30d650f9d2a9981" id="tgt20" class="tgtSentence">If you move from the record you are adding or editing before calling the <legacyBold>Update</legacyBold> method, ADO will automatically call <legacyBold>Update</legacyBold> to save the changes.</caps:sentence>
                <caps:sentence sentenceid="e60719024f0f993f90a387e7744f6352" id="tgt21" class="tgtSentence"> You must call the <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method if you want to cancel any changes made to the current record or discard a newly added record.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d34acd3113224bf80ebcfbfdfccc0840" id="tgt22" class="tgtSentence">The current record remains current after you call the <legacyBold>Update</legacyBold> method.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="de17f0f24b49f8364187891f8550ffbb" id="tgt23" class="tgtSentence">Record</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="8f59f1a4672b1a28f26f3dfc4806f4a1" id="tgt24" class="tgtSentence">The <legacyBold>Update</legacyBold> method finalizes additions, deletions, and updates to fields in the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyBold>Record</legacyBold> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4b2adb185189a1894ea33537fcb43e51" id="tgt25" class="tgtSentence">For example, fields deleted with the <legacyBold>Delete</legacyBold> method are marked for deletion immediately but remain in the collection.</caps:sentence>
                <caps:sentence sentenceid="ae6fa39c5260a55375bc8ceff4a5f52b" id="tgt26" class="tgtSentence"> The <legacyBold>Update</legacyBold> method must be called to actually delete these fields from the provider's collection.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt27" class="tgtSentence">Applies To</caps:sentence>
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
        <link xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew Method</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">EditMode Property</link>
        <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Saves any changes you make to the current row of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.Update</legacyBold>
          <parameterReference>Fields</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Values</parameterReference>
          <parameterReference>record.Fields</parameterReference>
          <legacyBold>.Update</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Fields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A <legacyBold>Variant</legacyBold> that represents a single name, or a <legacyBold>Variant</legacyBold> array that represents names or ordinal positions of the field or fields you wish to modify.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>Values</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> A <legacyBold>Variant</legacyBold> that represents a single value, or a <legacyBold>Variant</legacyBold> array that represents values for the field or fields in the new record.</caps:sentence>
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
              <caps:sentence id="src8" class="srcSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src9" class="srcSentence">Use the <legacyBold>Update</legacyBold> method to save any changes you make to the current record of a <legacyBold>Recordset</legacyBold> object since calling the <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink> method or since changing any field values in an existing record.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> The <legacyBold>Recordset</legacyBold> object must support updates.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src11" class="srcSentence">To set field values, do one of the following:  </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Assign values to a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object's <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property and call the <legacyBold>Update</legacyBold> method.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Pass a field name and a value as arguments with the <legacyBold>Update</legacyBold> call.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Pass an array of field names and an array of values with the <legacyBold>Update</legacyBold> call.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src15" class="srcSentence">When you use arrays of fields and values, there must be an equal number of elements in both arrays.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> Also, the order of field names must match the order of field values.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> If the number and order of fields and values do not match, an error occurs.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src18" class="srcSentence">If the <legacyBold>Recordset</legacyBold> object supports batch updating, you can cache multiple changes to one or more records locally until you call the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> If you are editing the current record or adding a new record when you call the <legacyBold>UpdateBatch</legacyBold> method, ADO will automatically call the <legacyBold>Update</legacyBold> method to save any pending changes to the current record before transmitting the batched changes to the provider.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src20" class="srcSentence">If you move from the record you are adding or editing before calling the <legacyBold>Update</legacyBold> method, ADO will automatically call <legacyBold>Update</legacyBold> to save the changes.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> You must call the <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method if you want to cancel any changes made to the current record or discard a newly added record.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src22" class="srcSentence">The current record remains current after you call the <legacyBold>Update</legacyBold> method.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src23" class="srcSentence">Record</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src24" class="srcSentence">The <legacyBold>Update</legacyBold> method finalizes additions, deletions, and updates to fields in the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyBold>Record</legacyBold> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src25" class="srcSentence">For example, fields deleted with the <legacyBold>Delete</legacyBold> method are marked for deletion immediately but remain in the collection.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> The <legacyBold>Update</legacyBold> method must be called to actually delete these fields from the provider's collection.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">Applies To</caps:sentence>
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
        <link xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew Method</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">EditMode Property</link>
        <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
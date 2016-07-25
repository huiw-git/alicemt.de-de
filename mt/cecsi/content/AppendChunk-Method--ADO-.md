---
title: "AppendChunk Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: c648b5a8-d4f1-4d16-836e-3957feb03617
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
# AppendChunk Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a9b73600cf8d043899795a263028dd7f" id="tgt1" class="tgtSentence">Appends data to a large text or binary data <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink>, or to a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
object.AppendChunk Data</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7dac69667e814ea09c728e6d30f5074d" id="tgt2" class="tgtSentence"> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="de1cc8159fa712a30692cd8ccbabf066" id="tgt3" class="tgtSentence">A <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="3ba365d1bbc5f56b9b06e523c3045738" id="tgt4" class="tgtSentence"> <legacyItalic>Data</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="bd87a787196281986fcea4204d159c53" id="tgt5" class="tgtSentence">A <legacyBold>Variant</legacyBold> that contains the data to append to the object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7f1897742b51ee7db3e68e7d2995f0a6" id="tgt6" class="tgtSentence">Use the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method on a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object to fill it with long binary or character data.</caps:sentence>
            <caps:sentence sentenceid="fe0b4521492fa776638f9bfa53e36c26" id="tgt7" class="tgtSentence"> In situations where system memory is limited, you can use the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method to manipulate long values in portions rather than in their entirety.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="06e3d36fa30cea095545139854ad1fb9" id="tgt8" class="tgtSentence">Field</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a5dc245125d21151c6f1b5db5abfa1d0" id="tgt9" class="tgtSentence">If the <legacyBold>adFldLong</legacyBold> bit in the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property of a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object is set to <languageKeyword>true</languageKeyword>, you can use the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method for that field.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="3f677d0e1a26dca095fad362c240231d" id="tgt10" class="tgtSentence">The first <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> call on a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object writes data to the field, overwriting any existing data.</caps:sentence>
                <caps:sentence sentenceid="a362e339b9c8cc280d7ac814d15e3e38" id="tgt11" class="tgtSentence"> Subsequent <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> calls add to existing data.</caps:sentence>
                <caps:sentence sentenceid="edf8d2ffe9dec91a719ecdac4374cd34" id="tgt12" class="tgtSentence"> If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field.</caps:sentence>
                <caps:sentence sentenceid="e9b7537d44e687edd46a803c9b5426e4" id="tgt13" class="tgtSentence"> If you call the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method on the first field again, ADO interprets the call as a new <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> operation and overwrites the existing data.</caps:sentence>
                <caps:sentence sentenceid="ba2746ed229ad52b4ee3aad6fa19e7af" id="tgt14" class="tgtSentence"> Accessing fields in other <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects that are not clones of the first <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object will not disrupt <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> operations.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a59958afa820669562a368ac22648d34" id="tgt15" class="tgtSentence">If there is no current record when you call <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> on a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object, an error occurs.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="af371b6ae9aabddfeb0da15d0d61fd1d" id="tgt16" class="tgtSentence">The <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method does not operate on <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects of a <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object_ADO</link> object.</caps:sentence>
                  <caps:sentence sentenceid="5744fa6ac1cec044be002a3faeb61583" id="tgt17" class="tgtSentence"> It does not perform any operation and will produce a run-time error.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt18" class="tgtSentence">Parameter</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cbe856c03eb4d3fd28f788cd2689cb45" id="tgt19" class="tgtSentence">If the <legacyBold>adParamLong</legacyBold> bit in the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property of a <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object is set to <languageKeyword>true</languageKeyword>, you can use the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method for that parameter.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8faa796367b7a3295c22816f1f4c67be" id="tgt20" class="tgtSentence">The first <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> call on a <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object writes data to the parameter, overwriting any existing data.</caps:sentence>
                <caps:sentence sentenceid="9b2ae59bf628cca2069d1b834f030aef" id="tgt21" class="tgtSentence"> Subsequent <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> calls on a <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object add to existing parameter data.</caps:sentence>
                <caps:sentence sentenceid="988c16f42deffaa5defb51549f3de0d8" id="tgt22" class="tgtSentence"> An <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> call that passes a null value discards all of the parameter data.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt23" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c07862b5-e466-46bd-910b-59ac96709cb9">AppendChunk and GetChunk Methods Example (VB)</link>
        <link xlink:href="51aa99be-d5ca-46ac-8b3f-1b03ce4f0b2a">AppendChunk and GetChunk Methods Example (VC++)</link>
        <link xlink:href="c21d0e82-81b3-4b06-a91e-77efad17c093">AppendChunk and GetChunk Methods Example (VJ++)</link>
        <link xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes Property (ADO)</link>
        <link xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk Method (ADO)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Appends data to a large text or binary data <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink>, or to a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
object.AppendChunk Data</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>Data</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">A <legacyBold>Variant</legacyBold> that contains the data to append to the object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Use the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method on a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object to fill it with long binary or character data.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> In situations where system memory is limited, you can use the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method to manipulate long values in portions rather than in their entirety.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src8" class="srcSentence">Field</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src9" class="srcSentence">If the <legacyBold>adFldLong</legacyBold> bit in the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property of a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object is set to <languageKeyword>true</languageKeyword>, you can use the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method for that field.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src10" class="srcSentence">The first <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> call on a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object writes data to the field, overwriting any existing data.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> Subsequent <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> calls add to existing data.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> If you call the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method on the first field again, ADO interprets the call as a new <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> operation and overwrites the existing data.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> Accessing fields in other <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects that are not clones of the first <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object will not disrupt <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> operations.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src15" class="srcSentence">If there is no current record when you call <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> on a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object, an error occurs.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src16" class="srcSentence">The <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method does not operate on <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects of a <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object_ADO</link> object.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> It does not perform any operation and will produce a run-time error.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src18" class="srcSentence">Parameter</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src19" class="srcSentence">If the <legacyBold>adParamLong</legacyBold> bit in the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property of a <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object is set to <languageKeyword>true</languageKeyword>, you can use the <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> method for that parameter.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src20" class="srcSentence">The first <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> call on a <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object writes data to the parameter, overwriting any existing data.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> Subsequent <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> calls on a <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object add to existing parameter data.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> An <unmanagedCodeEntityReference>AppendChunk</unmanagedCodeEntityReference> call that passes a null value discards all of the parameter data.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c07862b5-e466-46bd-910b-59ac96709cb9">AppendChunk and GetChunk Methods Example (VB)</link>
        <link xlink:href="51aa99be-d5ca-46ac-8b3f-1b03ce4f0b2a">AppendChunk and GetChunk Methods Example (VC++)</link>
        <link xlink:href="c21d0e82-81b3-4b06-a91e-77efad17c093">AppendChunk and GetChunk Methods Example (VJ++)</link>
        <link xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes Property (ADO)</link>
        <link xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk Method (ADO)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
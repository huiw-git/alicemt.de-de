---
title: "GetChunk Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: fc268e22-205b-44a3-9038-ffed51e23e10
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
# GetChunk Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="776b9fce632b6949c5afca285f663396" id="tgt1" class="tgtSentence">Returns all, or a portion, of the contents of a large text or binary data <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>variable</parameterReference> = <parameterReference>field</parameterReference><legacyBold>.GetChunk(</legacyBold><parameterReference>Size</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="210082e66129ba0f956925be5b4d06c7" id="tgt2" class="tgtSentence">Returns a <legacyBold>Variant</legacyBold>.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="604149611f1d8c102b8ec214eec6b24a" id="tgt3" class="tgtSentence"> <legacyItalic>Size</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a771c28339d278d66a8a8c2a4d1a4be9" id="tgt4" class="tgtSentence">A <languageKeyword>Long</languageKeyword> expression that is equal to the number of bytes or characters that you want to retrieve.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d13a151ae504adcaf03f47a66e098b26" id="tgt5" class="tgtSentence">Use the <legacyBold>GetChunk</legacyBold> method on a <legacyBold>Field</legacyBold> object to retrieve part or all of its long binary or character data.</caps:sentence>
            <caps:sentence sentenceid="c2cec76508ba4838295bbe3699ef99e5" id="tgt6" class="tgtSentence"> In situations where system memory is limited, you can use the <legacyBold>GetChunk</legacyBold> method to manipulate long values in portions, rather than in their entirety.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7b5bf03eb6b230837f8a7003148c36bf" id="tgt7" class="tgtSentence">The data that a <legacyBold>GetChunk</legacyBold> call returns is assigned to <legacyItalic>variable</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="87c821fbfbed6d43eb38f1c1e26d5d91" id="tgt8" class="tgtSentence"> If <legacyItalic>Size</legacyItalic> is greater than the remaining data, the <legacyBold>GetChunk</legacyBold> method returns only the remaining data without padding <legacyItalic>variable</legacyItalic> with empty spaces.</caps:sentence>
            <caps:sentence sentenceid="1c42673677bcea79eea46cd595c540d4" id="tgt9" class="tgtSentence"> If the field is empty, the <legacyBold>GetChunk</legacyBold> method returns a null value.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="584c0f9e3872d656053a985a573b60b0" id="tgt10" class="tgtSentence">Each subsequent <legacyBold>GetChunk</legacyBold> call retrieves data starting from where the previous <legacyBold>GetChunk</legacyBold> call left off.</caps:sentence>
            <caps:sentence sentenceid="335486ca2178b28c8dbf604b4d77e300" id="tgt11" class="tgtSentence"> However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</caps:sentence>
            <caps:sentence sentenceid="50355b5b661ddc153bd9e3999dde1685" id="tgt12" class="tgtSentence"> If you call the <legacyBold>GetChunk</legacyBold> method on the first field again, ADO interprets the call as a new <legacyBold>GetChunk</legacyBold> operation and starts reading from the beginning of the data.</caps:sentence>
            <caps:sentence sentenceid="1387acc99aaedfa6713a368f99f7c2a6" id="tgt13" class="tgtSentence"> Accessing fields in other <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects that are not clones of the first <legacyBold>Recordset</legacyBold> object will not disrupt <legacyBold>GetChunk</legacyBold> operations.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3c93b397133ab1705c9b67658db722cb" id="tgt14" class="tgtSentence">If the <legacyBold>adFldLong</legacyBold> bit in the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property of a <legacyBold>Field</legacyBold> object is set to <legacyBold>True</legacyBold>, you can use the <legacyBold>GetChunk</legacyBold> method for that field.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e9f3970cfd4203365c63e687737f8c3c" id="tgt15" class="tgtSentence">If there is no current record when you use the <legacyBold>GetChunk</legacyBold> method on a <legacyBold>Field</legacyBold> object, error 3021 (no current record) occurs.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="b15f8b409c00564d3fd4ab016554cb55" id="tgt16" class="tgtSentence">The <legacyBold>GetChunk</legacyBold> method does not operate on <legacyBold>Field</legacyBold> objects of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object.</caps:sentence>
              <caps:sentence sentenceid="5744fa6ac1cec044be002a3faeb61583" id="tgt17" class="tgtSentence"> It does not perform any operation and will produce a run-time error.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt18" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c07862b5-e466-46bd-910b-59ac96709cb9">Visual Basic Example</link>
        <link xlink:href="51aa99be-d5ca-46ac-8b3f-1b03ce4f0b2a">Visual C++ Example</link>
        <link xlink:href="c21d0e82-81b3-4b06-a91e-77efad17c093">Visual J++ Example</link>
        <link xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk Method</link>
        <link xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Returns all, or a portion, of the contents of a large text or binary data <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>variable</parameterReference> = <parameterReference>field</parameterReference><legacyBold>.GetChunk(</legacyBold><parameterReference>Size</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <legacyBold>Variant</legacyBold>.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>Size</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A <languageKeyword>Long</languageKeyword> expression that is equal to the number of bytes or characters that you want to retrieve.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>GetChunk</legacyBold> method on a <legacyBold>Field</legacyBold> object to retrieve part or all of its long binary or character data.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> In situations where system memory is limited, you can use the <legacyBold>GetChunk</legacyBold> method to manipulate long values in portions, rather than in their entirety.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The data that a <legacyBold>GetChunk</legacyBold> call returns is assigned to <legacyItalic>variable</legacyItalic>.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> If <legacyItalic>Size</legacyItalic> is greater than the remaining data, the <legacyBold>GetChunk</legacyBold> method returns only the remaining data without padding <legacyItalic>variable</legacyItalic> with empty spaces.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If the field is empty, the <legacyBold>GetChunk</legacyBold> method returns a null value.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">Each subsequent <legacyBold>GetChunk</legacyBold> call retrieves data starting from where the previous <legacyBold>GetChunk</legacyBold> call left off.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> If you call the <legacyBold>GetChunk</legacyBold> method on the first field again, ADO interprets the call as a new <legacyBold>GetChunk</legacyBold> operation and starts reading from the beginning of the data.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Accessing fields in other <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects that are not clones of the first <legacyBold>Recordset</legacyBold> object will not disrupt <legacyBold>GetChunk</legacyBold> operations.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">If the <legacyBold>adFldLong</legacyBold> bit in the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property of a <legacyBold>Field</legacyBold> object is set to <legacyBold>True</legacyBold>, you can use the <legacyBold>GetChunk</legacyBold> method for that field.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">If there is no current record when you use the <legacyBold>GetChunk</legacyBold> method on a <legacyBold>Field</legacyBold> object, error 3021 (no current record) occurs.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src16" class="srcSentence">The <legacyBold>GetChunk</legacyBold> method does not operate on <legacyBold>Field</legacyBold> objects of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> It does not perform any operation and will produce a run-time error.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src18" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c07862b5-e466-46bd-910b-59ac96709cb9">Visual Basic Example</link>
        <link xlink:href="51aa99be-d5ca-46ac-8b3f-1b03ce4f0b2a">Visual C++ Example</link>
        <link xlink:href="c21d0e82-81b3-4b06-a91e-77efad17c093">Visual J++ Example</link>
        <link xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk Method</link>
        <link xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Seek Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 129293d2-19d3-4940-bf64-483ee72fb4a1
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
# Seek Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="433d23f166ad9cb008245a641470c747" id="tgt1" class="tgtSentence">Searches the index of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to quickly locate the row that matches the specified values, and changes the current row position to that row.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
recordset.Seek KeyValues, SeekOption</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="93aaebe854441af4ca89c1e68a63fb4e" id="tgt2" class="tgtSentence"> <legacyItalic>KeyValues</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="c4a74fe8c895b6a2628a409f07ec1226" id="tgt3" class="tgtSentence">An array of <languageKeyword>Variant</languageKeyword> values.</caps:sentence>
                <caps:sentence sentenceid="be8472705daae339d1561adf2fc15c01" id="tgt4" class="tgtSentence"> An index consists of one or more columns and the array contains a value to compare against each corresponding column.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cbafeec54c4505bc931bd4ee292a3fe3" id="tgt5" class="tgtSentence"> <legacyItalic>SeekOption</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7296d3dc11860d8d4309ac8c286f49ae" id="tgt6" class="tgtSentence">A <legacyLink xlink:href="f0ec0c92-8253-47c6-9a14-e5dbccbad219">SeekEnum</legacyLink> value that specifies the type of comparison to be made between the columns of the index and the corresponding <legacyItalic>KeyValues</legacyItalic>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="f0e37929e3e5eecac6a068a6282b6412" id="tgt7" class="tgtSentence">Use the <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference> method in conjunction with the <legacyLink xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index</legacyLink> property if the underlying provider supports indexes on the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="9b7db3ae5a35eafa1f45173418176a47" id="tgt8" class="tgtSentence"> Use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink><legacyBold>(adSeek)</legacyBold> method to determine whether the underlying provider supports <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference>, and the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference><legacyBold>(adIndex)</legacyBold> method to determine whether the provider supports indexes.</caps:sentence>
            <caps:sentence sentenceid="fa5399e0f37d2cdefd768b4befb9807b" id="tgt9" class="tgtSentence"> (For example, the <legacyLink xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</legacyLink> supports <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference>.)</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="05f29f406892b6c08384e9409be6531b" id="tgt10" class="tgtSentence">If <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference> does not find the desired row, no error occurs, and the row is positioned at the end of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="1067ee951f1ad1f77d33cfdcfc8a0e7e" id="tgt11" class="tgtSentence"> Set the <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property to the desired index before executing this method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3184107b314be3e45bcc6ccd5ab61425" id="tgt12" class="tgtSentence">This method is supported only with server-side cursors.</caps:sentence>
            <caps:sentence sentenceid="c0c3f728a14657182a92ff4c9ee2ee63" id="tgt13" class="tgtSentence"> Seek is not supported when the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object's <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property value is <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f1a36ffe6a86290b5364da2362868376" id="tgt14" class="tgtSentence">This method can only be used when the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object has been opened with a <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> value of <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt15" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="337c9eda-9ddf-49ac-94d3-b33114ba6224">Visual Basic Example</link>
        <link xlink:href="57bda520-e98b-443c-a8bc-d8430e89a383">Visual C++ Example</link>
        <link xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find Method</link>
        <link xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Searches the index of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to quickly locate the row that matches the specified values, and changes the current row position to that row.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
recordset.Seek KeyValues, SeekOption</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>KeyValues</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">An array of <languageKeyword>Variant</languageKeyword> values.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> An index consists of one or more columns and the array contains a value to compare against each corresponding column.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>SeekOption</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A <legacyLink xlink:href="f0ec0c92-8253-47c6-9a14-e5dbccbad219">SeekEnum</legacyLink> value that specifies the type of comparison to be made between the columns of the index and the corresponding <legacyItalic>KeyValues</legacyItalic>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">Use the <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference> method in conjunction with the <legacyLink xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index</legacyLink> property if the underlying provider supports indexes on the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink><legacyBold>(adSeek)</legacyBold> method to determine whether the underlying provider supports <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference>, and the <unmanagedCodeEntityReference>Supports</unmanagedCodeEntityReference><legacyBold>(adIndex)</legacyBold> method to determine whether the provider supports indexes.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> (For example, the <legacyLink xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</legacyLink> supports <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference>.)</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">If <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference> does not find the desired row, no error occurs, and the row is positioned at the end of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Set the <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property to the desired index before executing this method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">This method is supported only with server-side cursors.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Seek is not supported when the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object's <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property value is <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">This method can only be used when the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object has been opened with a <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> value of <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="337c9eda-9ddf-49ac-94d3-b33114ba6224">Visual Basic Example</link>
        <link xlink:href="57bda520-e98b-443c-a8bc-d8430e89a383">Visual C++ Example</link>
        <link xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find Method</link>
        <link xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
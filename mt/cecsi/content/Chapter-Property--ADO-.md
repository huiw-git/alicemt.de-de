---
title: "Chapter Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8aa90cb0-f588-4141-9dc9-3b22918394ee
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
# Chapter Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0b31ee14954fb74e1ede9117d9957d7e" id="tgt1" class="tgtSentence">Gets or sets an OLE DB <legacyBold>Chapter</legacyBold> object from/on an <link xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">ADORecordsetConstruction Interface</link> object.</caps:sentence>
          <caps:sentence sentenceid="ce11bcca029926b4ad52699d698e198d" id="tgt2" class="tgtSentence"> When you use <legacyBold>put_Chapter</legacyBold> to set the <unmanagedCodeEntityReference>Chapter</unmanagedCodeEntityReference> object, a subset of rows is turned into an ADO <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="7ed21172bf6c97df1e16b2e4b05e3f32" id="tgt3" class="tgtSentence"> This sets the current chapter of the <legacyBold>Rowset</legacyBold><codeInline> </codeInline>object.</caps:sentence>
          <caps:sentence sentenceid="2faf3d2c3600b1d016cc867f4bfec082" id="tgt4" class="tgtSentence"> This property is read/write.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt5" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT get_Chapter([out, retval] long* plChapter);
HRESULT put_Chapter([in] long lChapter);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt6" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="0a95ca9fb4cbe66216f82ddea3b656a0" id="tgt7" class="tgtSentence"> <parameterReference>plChapter </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="c7ff4cfb549c44cf4a03f1571c1ff7e2" id="tgt8" class="tgtSentence">Pointer to the handle of a chapter.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="7a1a1978db02a7aa0ec8e93030fe47d5" id="tgt9" class="tgtSentence"> <parameterReference>LChapter </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="3d02827fd877eb5acf1bbea54597fd78" id="tgt10" class="tgtSentence">Handle of a chapter.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt11" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b0cce4d047a8d72a110b11ffb0a6c357" id="tgt12" class="tgtSentence">This property method returns the standard HRESULT values, including S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt13" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">ADORecordsetConstruction</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Gets or sets an OLE DB <legacyBold>Chapter</legacyBold> object from/on an <link xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">ADORecordsetConstruction Interface</link> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When you use <legacyBold>put_Chapter</legacyBold> to set the <unmanagedCodeEntityReference>Chapter</unmanagedCodeEntityReference> object, a subset of rows is turned into an ADO <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</legacyLink> object.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This sets the current chapter of the <legacyBold>Rowset</legacyBold><codeInline> </codeInline>object.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> This property is read/write.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT get_Chapter([out, retval] long* plChapter);
HRESULT put_Chapter([in] long lChapter);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <parameterReference>plChapter </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Pointer to the handle of a chapter.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <parameterReference>LChapter </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">Handle of a chapter.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">This property method returns the standard HRESULT values, including S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">ADORecordsetConstruction</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
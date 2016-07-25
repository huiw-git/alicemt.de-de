---
title: "RowPosition Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 9d068fed-39bf-4842-afc3-686a2af2145d
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
# RowPosition Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f750ae4790bd9d35df15a787e9e2b6db" id="tgt1" class="tgtSentence">Gets or sets an OLE DB <legacyBold>RowPosition</legacyBold> object from/on an <legacyBold>ADORecordsetConstruction</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="2d328ef75a592d067d3f5cb4c3533f02" id="tgt2" class="tgtSentence"> When you use <legacyBold>put_RowPosition</legacyBold> to set the <legacyBold>RowPosition</legacyBold> object, the resulting <legacyBold>Recordset</legacyBold> object uses the <legacyBold>RowPosition</legacyBold> object to determine the current row.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2528cae64820cb6ec8186372a5abd076" id="tgt3" class="tgtSentence">Read/write.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt4" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT get_RowPosition([out, retval] IUnknown** ppRowPos);
HRESULT put_RowPosition([in] IUnknown* pRowPos);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt5" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="93d0fc9319bb1d7e00581d294f70975c" id="tgt6" class="tgtSentence"> <legacyItalic>ppRowPos</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5477b61cbd786ab98daff69887e475b0" id="tgt7" class="tgtSentence">Pointer to an OLE DB <legacyBold>RowPosition</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="db68f6139f25ca906b11f631f198c677" id="tgt8" class="tgtSentence"> <legacyItalic>PRowPos</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="84a34268614fb3da0de478260cf7ffd1" id="tgt9" class="tgtSentence">An OLE DB <legacyBold>RowPosition</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt10" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b0cce4d047a8d72a110b11ffb0a6c357" id="tgt11" class="tgtSentence">This property method returns the standard HRESULT values, including S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e64399ff97ea55b1d943da7cebec82fe" id="tgt12" class="tgtSentence">When this property is set, if the <legacyBold>Rowset</legacyBold> object on the <legacyBold>RowPosition</legacyBold> object is different from the <legacyBold>Rowset</legacyBold> object on the <legacyBold>Recordset</legacyBold> object, the former overrides the latter.</caps:sentence>
            <caps:sentence sentenceid="ed18942732dc66b0a31535abf004ad60" id="tgt13" class="tgtSentence"> The same behavior applies to the current <legacyBold>Chapter</legacyBold> of the <legacyBold>RowPosition</legacyBold> as well.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="048dee0ddf71c5bb6140da2189a1f7e6" id="tgt15" class="tgtSentence">
              <link xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">ADORecordsetConstruction</link>       </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Gets or sets an OLE DB <legacyBold>RowPosition</legacyBold> object from/on an <legacyBold>ADORecordsetConstruction</legacyBold> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When you use <legacyBold>put_RowPosition</legacyBold> to set the <legacyBold>RowPosition</legacyBold> object, the resulting <legacyBold>Recordset</legacyBold> object uses the <legacyBold>RowPosition</legacyBold> object to determine the current row.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Read/write.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT get_RowPosition([out, retval] IUnknown** ppRowPos);
HRESULT put_RowPosition([in] IUnknown* pRowPos);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>ppRowPos</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Pointer to an OLE DB <legacyBold>RowPosition</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>PRowPos</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">An OLE DB <legacyBold>RowPosition</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">This property method returns the standard HRESULT values, including S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">When this property is set, if the <legacyBold>Rowset</legacyBold> object on the <legacyBold>RowPosition</legacyBold> object is different from the <legacyBold>Rowset</legacyBold> object on the <legacyBold>Recordset</legacyBold> object, the former overrides the latter.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> The same behavior applies to the current <legacyBold>Chapter</legacyBold> of the <legacyBold>RowPosition</legacyBold> as well.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">
              <link xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">ADORecordsetConstruction</link>       </caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
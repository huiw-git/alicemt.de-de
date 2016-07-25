---
title: "Rowset Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 7d359294-4ff2-47e0-8111-0c221b24d80e
caps.latest.revision: 9
caps.handback.revision: 9
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
# Rowset Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c8828a75249e821ff2f1b349d7e9ba5d" id="tgt1" class="tgtSentence">Gets or sets an OLE DB <legacyBold>Rowset</legacyBold> object from/on an <legacyBold>ADORecordsetConstruction</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="3d81631f191f358bb3a6b1565b1e5e57" id="tgt2" class="tgtSentence"> When you use put_Rowset, the rowset is turned into an ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
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
          <code>HRESULT get_Rowset([out, retval] IUnknown** ppRowset);
HRESULT put_Rowset([in] IUnknown* pRowset);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt5" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="0b6089bc81050100e664061ba2562244" id="tgt6" class="tgtSentence"> <legacyItalic>ppRowset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="737ab7f6b1c72848721791c65e28d599" id="tgt7" class="tgtSentence">Pointer to an OLE DB <legacyBold>Rowset</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5dcc75c85bd5524ee4412667721afad5" id="tgt8" class="tgtSentence"> <legacyItalic>PRowset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="489faa8b267cb595f198060f794bc73c" id="tgt9" class="tgtSentence">An OLE DB <legacyBold>Rowset</legacyBold> object.</caps:sentence>
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
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="048dee0ddf71c5bb6140da2189a1f7e6" id="tgt13" class="tgtSentence">
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
          <caps:sentence id="src1" class="srcSentence">Gets or sets an OLE DB <legacyBold>Rowset</legacyBold> object from/on an <legacyBold>ADORecordsetConstruction</legacyBold> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When you use put_Rowset, the rowset is turned into an ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
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
          <code>HRESULT get_Rowset([out, retval] IUnknown** ppRowset);
HRESULT put_Rowset([in] IUnknown* pRowset);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>ppRowset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Pointer to an OLE DB <legacyBold>Rowset</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>PRowset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">An OLE DB <legacyBold>Rowset</legacyBold> object.</caps:sentence>
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
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">
              <link xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">ADORecordsetConstruction</link>       </caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
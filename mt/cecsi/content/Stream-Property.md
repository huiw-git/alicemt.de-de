---
title: "Stream Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 4a44f9f6-0265-4c00-8def-d85b6af923b1
caps.latest.revision: 5
caps.handback.revision: 5
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
# Stream Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9d71846d0d4b10c008628fc9fd215801" id="tgt1" class="tgtSentence">Gets or sets an OLE DB <legacyBold>Stream</legacyBold> object from/on an <legacyBold>ADOStreamConstruction</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2528cae64820cb6ec8186372a5abd076" id="tgt2" class="tgtSentence">Read/write.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt3" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT get_Stream([out, retval] IUnknown** ppStream);
HRESULT put_Stream([in] IUnknown* pStream);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt4" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="ee6e62fc342dc49ba6982874e3653b73" id="tgt5" class="tgtSentence">ppStream</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="fdfa7c9b9af5ee952a76713c7c0b1474" id="tgt6" class="tgtSentence">Pointer to an OLE DB <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="d97e2de024ad5a84ad01412797842a78" id="tgt7" class="tgtSentence">pStream</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ef38bbd7e54e46d9f3437d085eb07311" id="tgt8" class="tgtSentence">An OLE DB <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt9" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d32a6611f35cb5bc598d57c45ec99efc" id="tgt10" class="tgtSentence">This property method returns the standard HRESULT values.</caps:sentence>
            <caps:sentence sentenceid="082e697aed7014afce2627fa44f536f7" id="tgt11" class="tgtSentence"> This includes S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="92f5a939-3e1a-4b14-a9dd-90e6ce2dec74">ADOStreamConstruction</link>
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
          <caps:sentence id="src1" class="srcSentence">Gets or sets an OLE DB <legacyBold>Stream</legacyBold> object from/on an <legacyBold>ADOStreamConstruction</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Read/write.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT get_Stream([out, retval] IUnknown** ppStream);
HRESULT put_Stream([in] IUnknown* pStream);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src5" class="srcSentence">ppStream</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Pointer to an OLE DB <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src7" class="srcSentence">pStream</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">An OLE DB <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">This property method returns the standard HRESULT values.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> This includes S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="92f5a939-3e1a-4b14-a9dd-90e6ce2dec74">ADOStreamConstruction</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
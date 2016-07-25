---
title: "Row Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 21019d89-2dd1-4a26-ac6f-384b81d66949
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
# Row Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="787415454ee0906a7a57810b93a6db3f" id="tgt1" class="tgtSentence">Gets or sets an OLE DB <legacyBold>Row</legacyBold> object from or on an <link xlink:href="52a5429e-5829-455e-be3b-31f05cbecf2d">ADORecordConstruction Interface</link> object.</caps:sentence>
          <caps:sentence sentenceid="6bf77285588719dbb05d1c7bfd4a37b0" id="tgt2" class="tgtSentence"> When you use <legacyBold>put_Row</legacyBold> to set a <legacyBold>Row</legacyBold> object, a row is turned into an ADO <legacyBold>Record</legacyBold> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="d91ecbd5da27130109e2313eee2ff0dd" id="tgt3" class="tgtSentence">Read/write.Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT get_Row([out, retval] IUnknown** ppRow);
HRESULT put_Row([in] IUnknown* pRow);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt4" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="de6e431376b661ce1009571e5e9691ff" id="tgt5" class="tgtSentence"> <legacyItalic>ppRow</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="36912e9ffa976df72041e95c9ba4078e" id="tgt6" class="tgtSentence">Pointer to an OLE DB <legacyBold>Row</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e75267b4a99a202bbcb3e349904aa0cc" id="tgt7" class="tgtSentence"> <legacyItalic>PRow</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e5c15e729efd838f19822dbf8f7a3118" id="tgt8" class="tgtSentence">An OLE DB <legacyBold>Row</legacyBold> object.</caps:sentence>
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
            <caps:sentence sentenceid="b0cce4d047a8d72a110b11ffb0a6c357" id="tgt10" class="tgtSentence">This property method returns the standard HRESULT values, including S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt11" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="52a5429e-5829-455e-be3b-31f05cbecf2d">ADORecordConstruction Interface</link>
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
          <caps:sentence id="src1" class="srcSentence">Gets or sets an OLE DB <legacyBold>Row</legacyBold> object from or on an <link xlink:href="52a5429e-5829-455e-be3b-31f05cbecf2d">ADORecordConstruction Interface</link> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When you use <legacyBold>put_Row</legacyBold> to set a <legacyBold>Row</legacyBold> object, a row is turned into an ADO <legacyBold>Record</legacyBold> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Read/write.Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT get_Row([out, retval] IUnknown** ppRow);
HRESULT put_Row([in] IUnknown* pRow);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>ppRow</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Pointer to an OLE DB <legacyBold>Row</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>PRow</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">An OLE DB <legacyBold>Row</legacyBold> object.</caps:sentence>
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
            <caps:sentence id="src10" class="srcSentence">This property method returns the standard HRESULT values, including S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="52a5429e-5829-455e-be3b-31f05cbecf2d">ADORecordConstruction Interface</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
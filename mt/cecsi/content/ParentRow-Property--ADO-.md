---
title: "ParentRow Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 5ea8029b-eda4-490b-ae84-2ad036fb582f
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
# ParentRow Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2472504b1a5537a3bb8761eb1a34acef" id="tgt1" class="tgtSentence">Sets the container of an OLE DB <legacyBold>Row</legacyBold> object on an <legacyBold>ADORecordConstruction</legacyBold> object, so that the parent of the row is turned into an ADO <legacyBold>Record</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="bbc5f135869218bba11681c163f25f3d" id="tgt2" class="tgtSentence">Write-only.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt3" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT put_ParentRow([in] IUnknown* pParent);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt4" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="b0ebef982b09387b81da8c611e442bc7" id="tgt5" class="tgtSentence"> <legacyItalic>pParent</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="6b7f4df121e8f6e950c4446a27c163f2" id="tgt6" class="tgtSentence">A container of a row.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt7" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b0cce4d047a8d72a110b11ffb0a6c357" id="tgt8" class="tgtSentence">This property method returns the standard HRESULT values, including S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="52a5429e-5829-455e-be3b-31f05cbecf2d">ADORecordConstruction</link>
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
          <caps:sentence id="src1" class="srcSentence">Sets the container of an OLE DB <legacyBold>Row</legacyBold> object on an <legacyBold>ADORecordConstruction</legacyBold> object, so that the parent of the row is turned into an ADO <legacyBold>Record</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Write-only.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>HRESULT put_ParentRow([in] IUnknown* pParent);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>pParent</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A container of a row.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">This property method returns the standard HRESULT values, including S_OK and E_FAIL.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="52a5429e-5829-455e-be3b-31f05cbecf2d">ADORecordConstruction</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
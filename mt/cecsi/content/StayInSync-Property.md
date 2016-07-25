---
title: "StayInSync Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 502d69b5-dc9a-455d-b115-a03bd39a552b
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
# StayInSync Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c2b737e0082187e83466d6b8336fee6c" id="tgt1" class="tgtSentence">Indicates, in a hierarchical <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, whether the reference to the underlying child records (that is, the <legacyItalic>chapter</legacyItalic>) changes when the parent row position changes.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1fe8ce8eb6d7226e6d135a0bc4af4b31" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Boolean</languageKeyword> value.</caps:sentence>
            <caps:sentence sentenceid="b0a137c75fee32e97bdb4f11b1d6f04c" id="tgt4" class="tgtSentence"> The default value is <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence sentenceid="a6b01f4cb8dba643a21a2047c6ee5203" id="tgt5" class="tgtSentence"> If <languageKeyword>True</languageKeyword>, the chapter will be updated if the parent <legacyBold>Recordset</legacyBold> object changes row position; if <languageKeyword>False</languageKeyword>, the chapter will continue to refer to data in the previous chapter even though the parent <legacyBold>Recordset</legacyBold> object has changed row position.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="8a23fc1111fddc7b6c88efeef5162b18" id="tgt6" class="tgtSentence">This property applies to hierarchical recordsets, such as those supported by the <legacyLink xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</legacyLink>, and must be set on the parent <legacyBold>Recordset</legacyBold> before the child <legacyBold>Recordset</legacyBold> is retrieved.</caps:sentence>
            <caps:sentence sentenceid="c851139d1de873c955913f46e0d0e2d4" id="tgt7" class="tgtSentence"> This property simplifies navigating hierarchical recordsets.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b682bcc3-04b3-42b0-86f4-c17e0cd29baf">Visual Basic Example</link>
        <link xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates, in a hierarchical <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, whether the reference to the underlying child records (that is, the <legacyItalic>chapter</legacyItalic>) changes when the parent row position changes.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Boolean</languageKeyword> value.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> If <languageKeyword>True</languageKeyword>, the chapter will be updated if the parent <legacyBold>Recordset</legacyBold> object changes row position; if <languageKeyword>False</languageKeyword>, the chapter will continue to refer to data in the previous chapter even though the parent <legacyBold>Recordset</legacyBold> object has changed row position.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">This property applies to hierarchical recordsets, such as those supported by the <legacyLink xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</legacyLink>, and must be set on the parent <legacyBold>Recordset</legacyBold> before the child <legacyBold>Recordset</legacyBold> is retrieved.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> This property simplifies navigating hierarchical recordsets.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b682bcc3-04b3-42b0-86f4-c17e0cd29baf">Visual Basic Example</link>
        <link xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
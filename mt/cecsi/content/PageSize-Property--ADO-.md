---
title: "PageSize Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e57930a6-46c4-4a17-a3b6-f79e94d5c9c7
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
# PageSize Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="441cd76c7984db6fb4f378e231fd71da" id="tgt1" class="tgtSentence">Indicates how many records constitute one page in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d1fe5ef1749defe89c2f207196f94c0c" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that indicates how many records are on a page.</caps:sentence>
            <caps:sentence sentenceid="a76c3d86d5041a4d11b8a5c8e286a074" id="tgt4" class="tgtSentence"> The default is <legacyBold>10</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ef68b690e4a47410d2a1fe53fce933de" id="tgt5" class="tgtSentence">Use the <legacyBold>PageSize</legacyBold> property to determine how many records make up a logical page of data.</caps:sentence>
            <caps:sentence sentenceid="8afdc90afef07be6f4399d1f19bd9b6b" id="tgt6" class="tgtSentence"> Establishing a page size allows you to use the <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> property to move to the first record of a particular page.</caps:sentence>
            <caps:sentence sentenceid="c6a97d7ed05f6e1da740614167612c12" id="tgt7" class="tgtSentence"> This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="76b8e688de580089bedf04c8283b5ede" id="tgt8" class="tgtSentence">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6665ddf84f2394d53b4659abb2973ad0" id="tgt10" class="tgtSentence">
              <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>       </caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5aaada64-5115-4adc-8668-827348f32566">Visual Basic Example</link>
        <link xlink:href="38ca4e1b-c109-4fba-b590-bdd6994f770e">Visual C++ Example</link>
        <link xlink:href="05f9f20e-0697-46bf-b004-76d7fc2e5d52">Visual J++ Example</link>
        <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property</link>
        <link xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates how many records constitute one page in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that indicates how many records are on a page.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default is <legacyBold>10</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>PageSize</legacyBold> property to determine how many records make up a logical page of data.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Establishing a page size allows you to use the <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> property to move to the first record of a particular page.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">
              <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>       </caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5aaada64-5115-4adc-8668-827348f32566">Visual Basic Example</link>
        <link xlink:href="38ca4e1b-c109-4fba-b590-bdd6994f770e">Visual C++ Example</link>
        <link xlink:href="05f9f20e-0697-46bf-b004-76d7fc2e5d52">Visual J++ Example</link>
        <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property</link>
        <link xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
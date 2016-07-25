---
title: "AbsolutePage Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ddb58a35-ec3a-423c-a504-3c65e62c23d4
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
# AbsolutePage Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="38395bce232ffebb3d93a86ec4030a38" id="tgt1" class="tgtSentence">Indicates on which page the current record resides.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="fb9808cf395dfc1f1d108caec4f820d7" id="tgt3" class="tgtSentence">For 32-bit code, sets or returns a <languageKeyword>Long</languageKeyword> value from 1 to the number of pages in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object (<legacyLink xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount</legacyLink>), or returns one of the <legacyLink xlink:href="e69af0a5-3405-4b72-9c6e-6b188ff746fd">PositionEnum</legacyLink> values.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7ad7faa90f3eb75fcf0cc08bba2c8e9c" id="tgt4" class="tgtSentence">For 64-bit code, use a data type that provides for storage of a 64-bit value.</caps:sentence>
            <caps:sentence sentenceid="3b2d99f6c1e9a336b871567c86a093c7" id="tgt5" class="tgtSentence"> For example, you can use either <languageKeyword>Long</languageKeyword> or another value that can be 64-bit length such as DBORDINAL.</caps:sentence>
            <caps:sentence sentenceid="143c0ca11398c1b5ff7bc565e5cdddba" id="tgt6" class="tgtSentence"> Do not use <legacyBold>PositionEnum</legacyBold> values because they are limited to 32-bit length.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="331687d0b5a57b10621fa90652a6590e" id="tgt7" class="tgtSentence">This property can be used to identify the page number on which the current record is located.</caps:sentence>
            <caps:sentence sentenceid="88ec4323542575f6e453fd5f0498dd10" id="tgt8" class="tgtSentence"> It uses the <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize</legacyLink> property to logically divide the total rowset count of the <legacyBold>Recordset</legacyBold> object into a series of pages, each of which has the number of records equal to <legacyBold>PageSize</legacyBold> (except for the last page, which may have fewer records).</caps:sentence>
            <caps:sentence sentenceid="f493d8b74249676ab7220d3ce60d4999" id="tgt9" class="tgtSentence"> The provider must support the appropriate functionality for this property to be available.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="29507147d37ace68de71b80e0bf39a93" id="tgt10" class="tgtSentence">When getting or setting the <legacyBold>AbsolutePage</legacyBold> property, ADO uses the <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink> property and the <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize</legacyLink> property together as follows:</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="68a528dc609fe4d40047b90f9dba4acc" id="tgt11" class="tgtSentence">To get the <legacyBold>AbsolutePage</legacyBold>, ADO first retrieves the <legacyBold>AbsolutePosition</legacyBold>, and then divides it by the <legacyBold>PageSize</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="df99b49c0a59cecc0d8407283a2a764d" id="tgt12" class="tgtSentence">To set the <legacyBold>AbsolutePage</legacyBold>, ADO moves the <legacyBold>AbsolutePosition</legacyBold> as follows: it multiplies the <legacyBold>PageSize</legacyBold> by the new <legacyBold>AbsolutePage</legacyBold> value and then adds 1 to the value.</caps:sentence>
                <caps:sentence sentenceid="f7b99818695036bbae18d1dc80060c29" id="tgt13" class="tgtSentence"> As a result, the current position in the <legacyBold>Recordset</legacyBold> after successfully setting <legacyBold>AbsolutePage</legacyBold> is the first record in that page.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="64e52cb9abab54db97908a379d02bb68" id="tgt14" class="tgtSentence">Like the <legacyBold>AbsolutePosition</legacyBold> property, <legacyBold>AbsolutePage</legacyBold> is 1-based and equals 1 when the current record is the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="0b7f0e16bf1ff57965a799973a87e5a8" id="tgt15" class="tgtSentence"> Set this property to move to the first record of a particular page.</caps:sentence>
            <caps:sentence sentenceid="18397dbfd65d35be21e5a49af6afddc8" id="tgt16" class="tgtSentence"> Obtain the total number of pages from the <legacyBold>PageCount</legacyBold> property.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt17" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5aaada64-5115-4adc-8668-827348f32566">Visual Basic Example</link>
        <link xlink:href="38ca4e1b-c109-4fba-b590-bdd6994f770e">Visual C++ Example</link>
        <link xlink:href="05f9f20e-0697-46bf-b004-76d7fc2e5d52">Visual J++ Example</link>
        <link xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition Property</link>
        <link xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount Property</link>
        <link xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates on which page the current record resides.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">For 32-bit code, sets or returns a <languageKeyword>Long</languageKeyword> value from 1 to the number of pages in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object (<legacyLink xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount</legacyLink>), or returns one of the <legacyLink xlink:href="e69af0a5-3405-4b72-9c6e-6b188ff746fd">PositionEnum</legacyLink> values.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">For 64-bit code, use a data type that provides for storage of a 64-bit value.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For example, you can use either <languageKeyword>Long</languageKeyword> or another value that can be 64-bit length such as DBORDINAL.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Do not use <legacyBold>PositionEnum</legacyBold> values because they are limited to 32-bit length.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">This property can be used to identify the page number on which the current record is located.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> It uses the <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize</legacyLink> property to logically divide the total rowset count of the <legacyBold>Recordset</legacyBold> object into a series of pages, each of which has the number of records equal to <legacyBold>PageSize</legacyBold> (except for the last page, which may have fewer records).</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The provider must support the appropriate functionality for this property to be available.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">When getting or setting the <legacyBold>AbsolutePage</legacyBold> property, ADO uses the <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink> property and the <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize</legacyLink> property together as follows:</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">To get the <legacyBold>AbsolutePage</legacyBold>, ADO first retrieves the <legacyBold>AbsolutePosition</legacyBold>, and then divides it by the <legacyBold>PageSize</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">To set the <legacyBold>AbsolutePage</legacyBold>, ADO moves the <legacyBold>AbsolutePosition</legacyBold> as follows: it multiplies the <legacyBold>PageSize</legacyBold> by the new <legacyBold>AbsolutePage</legacyBold> value and then adds 1 to the value.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> As a result, the current position in the <legacyBold>Recordset</legacyBold> after successfully setting <legacyBold>AbsolutePage</legacyBold> is the first record in that page.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src14" class="srcSentence">Like the <legacyBold>AbsolutePosition</legacyBold> property, <legacyBold>AbsolutePage</legacyBold> is 1-based and equals 1 when the current record is the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Set this property to move to the first record of a particular page.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Obtain the total number of pages from the <legacyBold>PageCount</legacyBold> property.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src17" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5aaada64-5115-4adc-8668-827348f32566">Visual Basic Example</link>
        <link xlink:href="38ca4e1b-c109-4fba-b590-bdd6994f770e">Visual C++ Example</link>
        <link xlink:href="05f9f20e-0697-46bf-b004-76d7fc2e5d52">Visual J++ Example</link>
        <link xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition Property</link>
        <link xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount Property</link>
        <link xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">PageSize Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "DefinedSize Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3ee27314-a305-4fbc-8433-9ee9a909afd6
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
# DefinedSize Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="09c835ee4487f61e4e80ae9ca25affd4" id="tgt1" class="tgtSentence">Indicates the data capacity of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cc88bf84170817bd944e0a5e36efee85" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> value that reflects the defined size of a field, which depends on the data type of the field object; see <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> for more information.</caps:sentence>
            <caps:sentence sentenceid="19618a43586273f40f7f4388a7a576a3" id="tgt4" class="tgtSentence"> For a field that uses a fixed-length data type, the return value is the size of the data type in bytes.</caps:sentence>
            <caps:sentence sentenceid="10b007c5902810bd8602a2728cf166e9" id="tgt5" class="tgtSentence"> For a field that uses a variable-length data type, this is one of the following:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="a420dcced62cd66af504d3ff5d8a1373" id="tgt6" class="tgtSentence">The maximum length of the field in characters (for <legacyBold>adVarChar</legacyBold> and <legacyBold>adVarWChar</legacyBold>) or in bytes (for <legacyBold>adVarBinary</legacyBold>, and <legacyBold>adVarNumeric</legacyBold>) if the field has a defined length.</caps:sentence>
                <caps:sentence sentenceid="fe40fff2d0e3b5fc4ae811bb0612fd0b" id="tgt7" class="tgtSentence"> For example, <legacyBold>adVarChar(5)</legacyBold> field has a maximum length of 5.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dc92490d52375ae49ba8940369b5a385" id="tgt8" class="tgtSentence">The maximum length of the data type in characters (for <legacyBold>adChar</legacyBold> and <legacyBold>adWChar</legacyBold>) or in bytes (for <legacyBold>adBinary</legacyBold> and <legacyBold>adNumeric</legacyBold>) if the field does not have a defined length.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="31350268ae85e40331df206198505af0" id="tgt9" class="tgtSentence">~0 (bitwise, the value is not 0; all bits are set to 1) if neither the field nor the data type has a defined maximum length.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dfe67305ab141d1a005b1e319dc524bc" id="tgt10" class="tgtSentence">For data types that do not have a length, this is set to ~0 (bitwise, the value is not 0; all bits are set to 1).</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1553a9ef2a3b1a9808b9dee0ccd01e7a" id="tgt11" class="tgtSentence">Use the <legacyBold>DefinedSize</legacyBold> property to determine the data capacity of a <legacyBold>Field</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d5da4157b716cf630f531facfc6014a1" id="tgt12" class="tgtSentence">The <legacyBold>DefinedSize</legacyBold> and <legacyLink xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize</legacyLink> properties are different.</caps:sentence>
            <caps:sentence sentenceid="6f8e8c8a23d66628ad06a306c54f5f08" id="tgt13" class="tgtSentence"> For example, consider a <legacyBold>Field</legacyBold> object with a declared type of <legacyBold>adVarChar</legacyBold> and a <legacyBold>DefinedSize</legacyBold> property value of 50, containing a single character.</caps:sentence>
            <caps:sentence sentenceid="a668c4e94d5d93752769725252c1fe10" id="tgt14" class="tgtSentence"> The <legacyBold>ActualSize</legacyBold> property value it returns is the length in bytes of the single character.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt15" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bff2c273-b535-4b32-83b3-0336a406859c">Visual Basic Example</link>
        <link xlink:href="05f7cc97-b806-41d2-939d-a955d10844c4">Visual C++ Example</link>
        <link xlink:href="2a0936e6-6452-4fef-9295-50407a13d691">Visual J++ Example</link>
        <link xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the data capacity of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> value that reflects the defined size of a field, which depends on the data type of the field object; see <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> for more information.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> For a field that uses a fixed-length data type, the return value is the size of the data type in bytes.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For a field that uses a variable-length data type, this is one of the following:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">The maximum length of the field in characters (for <legacyBold>adVarChar</legacyBold> and <legacyBold>adVarWChar</legacyBold>) or in bytes (for <legacyBold>adVarBinary</legacyBold>, and <legacyBold>adVarNumeric</legacyBold>) if the field has a defined length.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> For example, <legacyBold>adVarChar(5)</legacyBold> field has a maximum length of 5.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">The maximum length of the data type in characters (for <legacyBold>adChar</legacyBold> and <legacyBold>adWChar</legacyBold>) or in bytes (for <legacyBold>adBinary</legacyBold> and <legacyBold>adNumeric</legacyBold>) if the field does not have a defined length.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">~0 (bitwise, the value is not 0; all bits are set to 1) if neither the field nor the data type has a defined maximum length.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">For data types that do not have a length, this is set to ~0 (bitwise, the value is not 0; all bits are set to 1).</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">Use the <legacyBold>DefinedSize</legacyBold> property to determine the data capacity of a <legacyBold>Field</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">The <legacyBold>DefinedSize</legacyBold> and <legacyLink xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize</legacyLink> properties are different.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> For example, consider a <legacyBold>Field</legacyBold> object with a declared type of <legacyBold>adVarChar</legacyBold> and a <legacyBold>DefinedSize</legacyBold> property value of 50, containing a single character.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The <legacyBold>ActualSize</legacyBold> property value it returns is the length in bytes of the single character.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bff2c273-b535-4b32-83b3-0336a406859c">Visual Basic Example</link>
        <link xlink:href="05f7cc97-b806-41d2-939d-a955d10844c4">Visual C++ Example</link>
        <link xlink:href="2a0936e6-6452-4fef-9295-50407a13d691">Visual J++ Example</link>
        <link xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
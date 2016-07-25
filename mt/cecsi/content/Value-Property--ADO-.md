---
title: "Value Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 48919c74-86d4-462e-99b9-8854ceb8d683
caps.latest.revision: 7
caps.handback.revision: 7
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
# Value Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4f81ca17cf3d84d98877b1a689017ecb" id="tgt1" class="tgtSentence">Indicates the value assigned to a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink>, <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink>, or <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f8b4e9e137a1bc3470119bfcdd985337" id="tgt3" class="tgtSentence">Sets or returns a <legacyBold>Variant</legacyBold> value that indicates the value of the object.</caps:sentence>
            <caps:sentence sentenceid="79a55e6d2c10c960fbdd2a31e06e6db8" id="tgt4" class="tgtSentence"> Default value depends on the <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="26f3f1d797acc6d228def028fcfa0956" id="tgt5" class="tgtSentence">Use the <legacyBold>Value</legacyBold> property to set or return data from <legacyBold>Field</legacyBold> objects, to set or return parameter values with <legacyBold>Parameter</legacyBold> objects, or to set or return property settings with <legacyBold>Property</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="796da67ff68dc01693e0b2478d220906" id="tgt6" class="tgtSentence"> Whether the <legacyBold>Value</legacyBold> property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="93f749aa43b282b8614b2d6294bd10e4" id="tgt7" class="tgtSentence">ADO allows setting and returning long binary data with the <legacyBold>Value</legacyBold> property.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1b5f07e43bdb93f1490548aba3bd52ba" id="tgt8" class="tgtSentence">For <legacyBold>Parameter </legacyBold>objects, ADO reads the <legacyBold>Value</legacyBold> property only once from the provider.</caps:sentence>
              <caps:sentence sentenceid="1ffbc60962a1aecdcbd1ff4836979494" id="tgt9" class="tgtSentence"> If a command contains a <legacyBold>Parameter</legacyBold> whose <legacyBold>Value</legacyBold> property is empty, and you create a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> from the command, ensure that you first close the <legacyBold>Recordset</legacyBold> before retrieving the <legacyBold>Value</legacyBold> property.</caps:sentence>
              <caps:sentence sentenceid="5c53cdfe3afa7a411e63fa4e0b71f771" id="tgt10" class="tgtSentence"> Otherwise, for some providers, the <legacyBold>Value</legacyBold> property may be empty, and won't contain the correct value.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="20d20e9a56046ceed8bb52397a6760bc" id="tgt11" class="tgtSentence">For new <legacyBold>Field</legacyBold> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, the <legacyBold>Value</legacyBold> property must be set before any other <legacyBold>Field</legacyBold> properties can be specified.</caps:sentence>
              <caps:sentence sentenceid="f9bc5a9add24e69e6fb5f7e8446be41c" id="tgt12" class="tgtSentence"> First, a specific value for the <legacyBold>Value</legacyBold> property must have been assigned and <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> on the <legacyBold>Fields</legacyBold> collection called.</caps:sentence>
              <caps:sentence sentenceid="7de5d83ef3be56f8b1667f4cd105e1ba" id="tgt13" class="tgtSentence"> Then, other properties such as <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> or <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> can be accessed.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2d4fe651-ef09-461b-8884-a70b6af4362e">Visual Basic Example</link>
        <link xlink:href="2a104245-56df-44f3-b9b7-b3d18643d57b">Visual C++ Example</link>
        <link xlink:href="707be908-20ef-4bd6-a12c-8dc87fadd6ed">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the value assigned to a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink>, <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink>, or <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyBold>Variant</legacyBold> value that indicates the value of the object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Default value depends on the <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>Value</legacyBold> property to set or return data from <legacyBold>Field</legacyBold> objects, to set or return parameter values with <legacyBold>Parameter</legacyBold> objects, or to set or return property settings with <legacyBold>Property</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Whether the <legacyBold>Value</legacyBold> property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">ADO allows setting and returning long binary data with the <legacyBold>Value</legacyBold> property.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src8" class="srcSentence">For <legacyBold>Parameter </legacyBold>objects, ADO reads the <legacyBold>Value</legacyBold> property only once from the provider.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> If a command contains a <legacyBold>Parameter</legacyBold> whose <legacyBold>Value</legacyBold> property is empty, and you create a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> from the command, ensure that you first close the <legacyBold>Recordset</legacyBold> before retrieving the <legacyBold>Value</legacyBold> property.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> Otherwise, for some providers, the <legacyBold>Value</legacyBold> property may be empty, and won't contain the correct value.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src11" class="srcSentence">For new <legacyBold>Field</legacyBold> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, the <legacyBold>Value</legacyBold> property must be set before any other <legacyBold>Field</legacyBold> properties can be specified.</caps:sentence>
              <caps:sentence id="src12" class="srcSentence"> First, a specific value for the <legacyBold>Value</legacyBold> property must have been assigned and <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> on the <legacyBold>Fields</legacyBold> collection called.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> Then, other properties such as <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> or <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> can be accessed.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2d4fe651-ef09-461b-8884-a70b6af4362e">Visual Basic Example</link>
        <link xlink:href="2a104245-56df-44f3-b9b7-b3d18643d57b">Visual C++ Example</link>
        <link xlink:href="707be908-20ef-4bd6-a12c-8dc87fadd6ed">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
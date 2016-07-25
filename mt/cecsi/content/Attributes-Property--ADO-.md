---
title: "Attributes Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: acc15d40-68a6-4ba9-85bd-12d331aecaa6
caps.latest.revision: 13
caps.handback.revision: 13
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
# Attributes Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="adeae33dff30274f1534f3f0eb18b858" id="tgt1" class="tgtSentence">Indicates one or more characteristics of an object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2809c302620fca149193ed87011bb9b5" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a5ecc184dc4dfc5896479261bb86ad9c" id="tgt4" class="tgtSentence">For a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property is read/write, and its value can be the sum of one or more <legacyLink xlink:href="e7dcecd3-7dc7-445c-b922-f700c3067fbc">XactAttributeEnum</legacyLink> values.</caps:sentence>
            <caps:sentence sentenceid="9e7991cc859fcde7e314020c599a0b0e" id="tgt5" class="tgtSentence"> The default is zero (0).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fe5e3f262933e2e69987f531a1dee48c" id="tgt6" class="tgtSentence">For a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object, the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property is read/write, and its value can be the sum of any one or more <legacyLink xlink:href="7ef6c728-5eda-4bde-8052-02d2db1d2cfe">ParameterAttributesEnum</legacyLink> values.</caps:sentence>
            <caps:sentence sentenceid="86304c502ffc703fd0d50a2b89f318ab" id="tgt7" class="tgtSentence"> The default is <legacyBold>adParamSigned</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4cc6027c9cf92d5a54bd613e9da26124" id="tgt8" class="tgtSentence">For a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object, the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property can be the sum of one or more <legacyLink xlink:href="6e34d886-005a-40dc-bd5c-6adcbf81e5cd">FieldAttributeEnum</legacyLink> values.</caps:sentence>
            <caps:sentence sentenceid="f3f67e0fc578a5c452aae5998a742738" id="tgt9" class="tgtSentence"> It is normally read-only.</caps:sentence>
            <caps:sentence sentenceid="cf9e929b7c1ea2ee03fccbecd8776346" id="tgt10" class="tgtSentence"> However, for new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> is read/write only after the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property for the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> has been specified and the new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> has been successfully added by the data provider by calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method of the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="69f82041198d63aee305e1152ef16508" id="tgt11" class="tgtSentence">For a <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink> object, the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property is read-only, and its value can be the sum of any one or more <legacyLink xlink:href="96a01955-a6b4-4cbf-9c73-52bcd1e9fb25">PropertyAttributesEnum</legacyLink> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="75f65d29ae9c5ca81456a3ca5d3ed995" id="tgt12" class="tgtSentence">Use the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property to set or return characteristics of <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> objects, <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> objects, <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects, or <unmanagedCodeEntityReference>Property</unmanagedCodeEntityReference> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7f9b3320b5b5d0bc25738394fbf3bdfe" id="tgt13" class="tgtSentence">When you set multiple attributes, you can sum the appropriate constants.</caps:sentence>
            <caps:sentence sentenceid="234e09b6b6b5f46bc233e8341502afcd" id="tgt14" class="tgtSentence"> If you set the property value to a sum including incompatible constants, an error occurs.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="740dc773d8102b73845f395859ee69b6" id="tgt15" class="tgtSentence">
                <legacyBold>Remote Data Service Usage   </legacyBold>This property is not available on a client-side <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt16" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="258bdce3-1819-44a2-9217-105879c789ef">Visual Basic Example</link>
        <link xlink:href="2db7c9ca-d7d0-4c8e-840b-b27d7933ec40">Visual C++ Example</link>
        <link xlink:href="625f8bcb-a9bb-4534-8768-00a9bcbe7b7f">Visual J++ Example</link>
        <link xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk Method</link>
        <link xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans, CommitTrans, and RollbackTrans Methods</link>
        <link xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates one or more characteristics of an object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">For a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property is read/write, and its value can be the sum of one or more <legacyLink xlink:href="e7dcecd3-7dc7-445c-b922-f700c3067fbc">XactAttributeEnum</legacyLink> values.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The default is zero (0).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">For a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object, the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property is read/write, and its value can be the sum of any one or more <legacyLink xlink:href="7ef6c728-5eda-4bde-8052-02d2db1d2cfe">ParameterAttributesEnum</legacyLink> values.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The default is <legacyBold>adParamSigned</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">For a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object, the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property can be the sum of one or more <legacyLink xlink:href="6e34d886-005a-40dc-bd5c-6adcbf81e5cd">FieldAttributeEnum</legacyLink> values.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> It is normally read-only.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> However, for new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> is read/write only after the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property for the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> has been specified and the new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> has been successfully added by the data provider by calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method of the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">For a <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property</legacyLink> object, the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property is read-only, and its value can be the sum of any one or more <legacyLink xlink:href="96a01955-a6b4-4cbf-9c73-52bcd1e9fb25">PropertyAttributesEnum</legacyLink> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Use the <unmanagedCodeEntityReference>Attributes</unmanagedCodeEntityReference> property to set or return characteristics of <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> objects, <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> objects, <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects, or <unmanagedCodeEntityReference>Property</unmanagedCodeEntityReference> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">When you set multiple attributes, you can sum the appropriate constants.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> If you set the property value to a sum including incompatible constants, an error occurs.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src15" class="srcSentence">
                <legacyBold>Remote Data Service Usage   </legacyBold>This property is not available on a client-side <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="258bdce3-1819-44a2-9217-105879c789ef">Visual Basic Example</link>
        <link xlink:href="2db7c9ca-d7d0-4c8e-840b-b27d7933ec40">Visual C++ Example</link>
        <link xlink:href="625f8bcb-a9bb-4534-8768-00a9bcbe7b7f">Visual J++ Example</link>
        <link xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk Method</link>
        <link xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans, CommitTrans, and RollbackTrans Methods</link>
        <link xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
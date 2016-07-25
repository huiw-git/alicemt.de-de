---
title: "NumericScale Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 29a02992-64be-4fcd-be13-445cba205893
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
# NumericScale Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b7ac00dc6b4f93cc8868925915f7bd9b" id="tgt1" class="tgtSentence">Indicates the scale of numeric values in a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> or <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5b10a7268d34569f95837ecd15316637" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Byte</languageKeyword> value that indicates the number of decimal places to which numeric values will be resolved.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="46ef3a8b5f28a45f75d7d2212bdec909" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>NumericScale</unmanagedCodeEntityReference> property to determine how many digits to the right of the decimal point will be used to represent values for a numeric <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="85927f5317b77bcf5704ac778bdf6b01" id="tgt5" class="tgtSentence">For <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> objects, the <unmanagedCodeEntityReference>NumericScale</unmanagedCodeEntityReference> property is read/write.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="06a642b70075f2e78f892bf4331d1016" id="tgt6" class="tgtSentence">For a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference><legacyBold> </legacyBold>object, <unmanagedCodeEntityReference>NumericScale</unmanagedCodeEntityReference> is normally read-only.</caps:sentence>
            <caps:sentence sentenceid="0576df4505ec5ff8f0e0147244d7067f" id="tgt7" class="tgtSentence"> However, for new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, <unmanagedCodeEntityReference>NumericScale</unmanagedCodeEntityReference> is read/write only after the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property for the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> has been specified and the data provider has successfully added the new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> by calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method of the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="9c1e2322-c225-49d1-a120-a343f23cea73">Visual Basic Example</link>
        <link xlink:href="55d91ba8-4d80-4df6-af8e-060a19ddc138">Visual C++ Example</link>
        <link xlink:href="ca9f10d2-b5d1-449b-807b-649ef4fbf0bb">Visual J++ Example</link>
        <link xlink:href="1fa38e78-6b5b-414d-ba0a-3dd26b29b766">Precision Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the scale of numeric values in a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> or <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Byte</languageKeyword> value that indicates the number of decimal places to which numeric values will be resolved.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>NumericScale</unmanagedCodeEntityReference> property to determine how many digits to the right of the decimal point will be used to represent values for a numeric <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">For <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> objects, the <unmanagedCodeEntityReference>NumericScale</unmanagedCodeEntityReference> property is read/write.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">For a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference><legacyBold> </legacyBold>object, <unmanagedCodeEntityReference>NumericScale</unmanagedCodeEntityReference> is normally read-only.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> However, for new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, <unmanagedCodeEntityReference>NumericScale</unmanagedCodeEntityReference> is read/write only after the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property for the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> has been specified and the data provider has successfully added the new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> by calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method of the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="9c1e2322-c225-49d1-a120-a343f23cea73">Visual Basic Example</link>
        <link xlink:href="55d91ba8-4d80-4df6-af8e-060a19ddc138">Visual C++ Example</link>
        <link xlink:href="ca9f10d2-b5d1-449b-807b-649ef4fbf0bb">Visual J++ Example</link>
        <link xlink:href="1fa38e78-6b5b-414d-ba0a-3dd26b29b766">Precision Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
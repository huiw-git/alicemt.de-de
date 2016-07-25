---
title: "Precision Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 1fa38e78-6b5b-414d-ba0a-3dd26b29b766
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
# Precision Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="24d82228281a0fbbad06f0079c73f9e2" id="tgt1" class="tgtSentence">Indicates the degree of precision for numeric values in a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object or for numeric <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c2c973b7c28f6b46bec4d84b785fbf98" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Byte</languageKeyword> value that indicates the maximum number of digits used to represent values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1aa890a702a663c8d2bd4215ecdca0a9" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>Precision</unmanagedCodeEntityReference> property to determine the maximum number of digits used to represent values for a numeric <legacyBold>Parameter</legacyBold> or <legacyBold>Field</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="14c9415f4a94bce080870f66a0549666" id="tgt5" class="tgtSentence">The value is read/write on a <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d6aea12b4c5c4eee5e59c8091ed8f653" id="tgt6" class="tgtSentence">For a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference><legacyBold> </legacyBold>object, <unmanagedCodeEntityReference>Precision</unmanagedCodeEntityReference> is normally read-only.</caps:sentence>
            <caps:sentence sentenceid="f3fb57efa1dfdc09214ab60cc7cfe602" id="tgt7" class="tgtSentence"> However, for new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, <unmanagedCodeEntityReference>Precision</unmanagedCodeEntityReference> is read/write only after the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property for the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> has been specified and the data provider has successfully added the new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> by calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method of the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection.</caps:sentence>
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
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
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
        <link xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the degree of precision for numeric values in a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object or for numeric <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Byte</languageKeyword> value that indicates the maximum number of digits used to represent values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>Precision</unmanagedCodeEntityReference> property to determine the maximum number of digits used to represent values for a numeric <legacyBold>Parameter</legacyBold> or <legacyBold>Field</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">The value is read/write on a <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">For a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference><legacyBold> </legacyBold>object, <unmanagedCodeEntityReference>Precision</unmanagedCodeEntityReference> is normally read-only.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> However, for new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, <unmanagedCodeEntityReference>Precision</unmanagedCodeEntityReference> is read/write only after the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property for the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> has been specified and the data provider has successfully added the new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> by calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method of the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection.</caps:sentence>
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
                    <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</link>
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
        <link xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
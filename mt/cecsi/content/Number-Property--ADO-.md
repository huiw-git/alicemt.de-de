---
title: "Number Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f92323c5-dd11-4a63-a505-d9014a0f067f
caps.latest.revision: 12
caps.handback.revision: 12
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
# Number Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="acf4ce16a98de4b9a115dbefb3483dcd" id="tgt1" class="tgtSentence">Indicates the number that uniquely identifies an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bc02a30b55d0bbd7788d54d44f99f938" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> value that may correspond to one of the <legacyLink xlink:href="9469ba3a-5e4f-4a10-bbb8-a51a6c9660ea">ErrorValueEnum</legacyLink> constants.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="2041b50bc21b227617c3b2a7f4292ebf" id="tgt4" class="tgtSentence">Use the <legacyBold>Number</legacyBold> property to determine which error occurred.</caps:sentence>
            <caps:sentence sentenceid="e547c451ebb1f8af8af2d7cb21670690" id="tgt5" class="tgtSentence"> The value of the property is a unique number that corresponds to the error condition.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="79c42285af12492143858a0ab9c9ebe2" id="tgt6" class="tgtSentence">The <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</caps:sentence>
            <caps:sentence sentenceid="19a3eee92f2a1456f35bc907b5b96690" id="tgt7" class="tgtSentence"> These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</caps:sentence>
            <caps:sentence sentenceid="fbf21a569cdfca9da06072b2ac147484" id="tgt8" class="tgtSentence"> For more information about these numbers, see <legacyLink xlink:href="ed74e62d-4948-4eeb-a7c9-fd7ad46af7fd">Errors (OLE DB)</legacyLink> in the <legacyLink xlink:href="3c5e2dd5-35e5-4a93-ac3a-3818bb43bbf8">OLE DB Programmer's Reference</legacyLink><legacyItalic>.</legacyItalic></caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5c728458-d85c-497c-afcf-2cfa36c3342a">Visual Basic Example</link>
        <link xlink:href="5321fc0f-cd0c-4e2a-a5bc-0008fba86b59">Visual C++ Example</link>
        <link xlink:href="7fd0eebc-99f4-490e-9b62-0b62b1884d6b">Visual J++ Example</link>
        <link xlink:href="4b5d6790-6c29-42aa-bf78-d9cfb8ad7965">Description Property</link>
        <link xlink:href="2b9ef441-993c-44d4-8f87-fac0979dac1d">HelpContext, HelpFile Properties</link>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the number that uniquely identifies an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> value that may correspond to one of the <legacyLink xlink:href="9469ba3a-5e4f-4a10-bbb8-a51a6c9660ea">ErrorValueEnum</legacyLink> constants.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Number</legacyBold> property to determine which error occurred.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The value of the property is a unique number that corresponds to the error condition.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">The <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> For more information about these numbers, see <legacyLink xlink:href="ed74e62d-4948-4eeb-a7c9-fd7ad46af7fd">Errors (OLE DB)</legacyLink> in the <legacyLink xlink:href="3c5e2dd5-35e5-4a93-ac3a-3818bb43bbf8">OLE DB Programmer's Reference</legacyLink><legacyItalic>.</legacyItalic></caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5c728458-d85c-497c-afcf-2cfa36c3342a">Visual Basic Example</link>
        <link xlink:href="5321fc0f-cd0c-4e2a-a5bc-0008fba86b59">Visual C++ Example</link>
        <link xlink:href="7fd0eebc-99f4-490e-9b62-0b62b1884d6b">Visual J++ Example</link>
        <link xlink:href="4b5d6790-6c29-42aa-bf78-d9cfb8ad7965">Description Property</link>
        <link xlink:href="2b9ef441-993c-44d4-8f87-fac0979dac1d">HelpContext, HelpFile Properties</link>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
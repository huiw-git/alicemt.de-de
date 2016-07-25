---
title: "Source Property (ADO Error)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 4044ba15-f013-4c4c-9fe1-b4410fe9a778
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
# Source Property (ADO Error)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5c894afcfc0b3196536804b814a03e1c" id="tgt1" class="tgtSentence">Indicates the name of the object or application that originally generated an error.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="21d8c818fdff050a0b7f51c8eb5ac737" id="tgt3" class="tgtSentence">Returns a <languageKeyword>String</languageKeyword> value that indicates the name of an object or application.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="2f8f9a2f075735083f6e9130e5930569" id="tgt4" class="tgtSentence">Use the <legacyBold>Source</legacyBold> property on an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object to determine the name of the object or application that originally generated an error.</caps:sentence>
            <caps:sentence sentenceid="a5dafca4e7e756ac524f068391a73be8" id="tgt5" class="tgtSentence"> This could be the object's class name or programmatic ID.</caps:sentence>
            <caps:sentence sentenceid="c21e85ad37881cc5f3119ed8e2700790" id="tgt6" class="tgtSentence"> For errors in ADO, the property value will be <legacyBold>ADODB.</legacyBold><legacyItalic>ObjectName</legacyItalic>, where <legacyItalic>ObjectName</legacyItalic> is the name of the object that triggered the error.</caps:sentence>
            <caps:sentence sentenceid="39dd4ca8fd5228176e148858d4b9b06a" id="tgt7" class="tgtSentence"> For ADOX and ADO MD, the value will be <legacyBold>ADOX.</legacyBold><legacyItalic>ObjectName </legacyItalic>and <legacyBold>ADOMD.</legacyBold><legacyItalic>ObjectName, </legacyItalic>respectively.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b0f7dc6a8e6a7476d2afa4e7d00008a4" id="tgt8" class="tgtSentence">Based on the error documentation from the <legacyBold>Source</legacyBold>, <legacyLink xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number</legacyLink>, and <legacyLink xlink:href="4b5d6790-6c29-42aa-bf78-d9cfb8ad7965">Description</legacyLink> properties of <legacyBold>Error</legacyBold> objects, you can write code that will handle the error appropriately.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="538ff3064d13216238cb914813b1d61e" id="tgt9" class="tgtSentence">The <legacyBold>Source</legacyBold> property is read-only for <legacyBold>Error</legacyBold> objects.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
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
        <link xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number Property</link>
        <link xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source Property (ADO Record)</link>
        <link xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source Property (ADO Recordset)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the name of the object or application that originally generated an error.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>String</languageKeyword> value that indicates the name of an object or application.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Source</legacyBold> property on an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object to determine the name of the object or application that originally generated an error.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This could be the object's class name or programmatic ID.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For errors in ADO, the property value will be <legacyBold>ADODB.</legacyBold><legacyItalic>ObjectName</legacyItalic>, where <legacyItalic>ObjectName</legacyItalic> is the name of the object that triggered the error.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> For ADOX and ADO MD, the value will be <legacyBold>ADOX.</legacyBold><legacyItalic>ObjectName </legacyItalic>and <legacyBold>ADOMD.</legacyBold><legacyItalic>ObjectName, </legacyItalic>respectively.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">Based on the error documentation from the <legacyBold>Source</legacyBold>, <legacyLink xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number</legacyLink>, and <legacyLink xlink:href="4b5d6790-6c29-42aa-bf78-d9cfb8ad7965">Description</legacyLink> properties of <legacyBold>Error</legacyBold> objects, you can write code that will handle the error appropriately.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <legacyBold>Source</legacyBold> property is read-only for <legacyBold>Error</legacyBold> objects.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
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
        <link xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number Property</link>
        <link xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source Property (ADO Record)</link>
        <link xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source Property (ADO Recordset)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "HelpContext, HelpFile Properties"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 2b9ef441-993c-44d4-8f87-fac0979dac1d
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
# HelpContext, HelpFile Properties
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2d8d520bcad1287dd477ff19c00b74ab" id="tgt1" class="tgtSentence">Indicates the Help file and topic associated with an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="d4955021ae0bc48f16f2570307e715fd" id="tgt3" class="tgtSentence">
                  <legacyBold>HelpContextID</legacyBold>     Returns a context ID, as a <languageKeyword>Long</languageKeyword> value, for a topic in a Help file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="514d9495dd9917340c56ddebb3188b25" id="tgt4" class="tgtSentence">
                  <legacyBold>HelpFile</legacyBold>     Returns a <languageKeyword>String</languageKeyword> value that evaluates to a fully resolved path to a Help file.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="f7118c66eab381b815a03fb8a6039ae3" id="tgt5" class="tgtSentence">If a Help file is specified in the <unmanagedCodeEntityReference>HelpFile</unmanagedCodeEntityReference> property, the <unmanagedCodeEntityReference>HelpContext</unmanagedCodeEntityReference> property is used to automatically display the Help topic it identifies.</caps:sentence>
            <caps:sentence sentenceid="401f5b9b4d7ac179c67f48f1c4dfe05d" id="tgt6" class="tgtSentence"> If there is no relevant help topic available, the <unmanagedCodeEntityReference>HelpContext</unmanagedCodeEntityReference> property returns zero and the <unmanagedCodeEntityReference>HelpFile</unmanagedCodeEntityReference> property returns a zero-length string ("").</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
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
        <link xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number Property</link>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the Help file and topic associated with an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src3" class="srcSentence">
                  <legacyBold>HelpContextID</legacyBold>     Returns a context ID, as a <languageKeyword>Long</languageKeyword> value, for a topic in a Help file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">
                  <legacyBold>HelpFile</legacyBold>     Returns a <languageKeyword>String</languageKeyword> value that evaluates to a fully resolved path to a Help file.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">If a Help file is specified in the <unmanagedCodeEntityReference>HelpFile</unmanagedCodeEntityReference> property, the <unmanagedCodeEntityReference>HelpContext</unmanagedCodeEntityReference> property is used to automatically display the Help topic it identifies.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> If there is no relevant help topic available, the <unmanagedCodeEntityReference>HelpContext</unmanagedCodeEntityReference> property returns zero and the <unmanagedCodeEntityReference>HelpFile</unmanagedCodeEntityReference> property returns a zero-length string ("").</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
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
        <link xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number Property</link>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
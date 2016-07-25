---
title: "Name Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: cfd0e29c-8310-44ab-85c3-5761184b865d
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
# Name Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="30300650b5d8747d508cc7d350f0e3be" id="tgt1" class="tgtSentence">Indicates the name of an object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7518325b3fceddced9861c766cbf7415" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that indicates the name of an object.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="aabac18cfd63a4445859441929a10aba" id="tgt4" class="tgtSentence">Use the <legacyBold>Name</legacyBold> property to assign a name to or retrieve the name of a <legacyBold>Command</legacyBold>, <legacyBold>Property</legacyBold>, <legacyBold>Field</legacyBold>, or <legacyBold>Parameter</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="59eba1083e4e70caa26adc27b5e83306" id="tgt5" class="tgtSentence">The value is read/write on a <legacyBold>Command</legacyBold> object and read-only on a <legacyBold>Property</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dd1f65922fe3879c77e3594312030e81" id="tgt6" class="tgtSentence">For a <legacyBold>Field</legacyBold> object, <legacyBold>Name</legacyBold> is normally read-only.</caps:sentence>
            <caps:sentence sentenceid="76ad66fdc77a40478fa034968884a53e" id="tgt7" class="tgtSentence"> However, for new <legacyBold>Field</legacyBold> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, <legacyBold>Name</legacyBold> is read/write only after the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property for the <legacyBold>Field</legacyBold> has been specified and the data provider has successfully added the new <legacyBold>Field</legacyBold> by calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method of the <legacyBold>Fields</legacyBold> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a247b072e036d4b03b6d187aeed77e71" id="tgt8" class="tgtSentence">For <legacyBold>Parameter</legacyBold> objects not yet appended to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection, the <legacyBold>Name</legacyBold> property is read/write.</caps:sentence>
            <caps:sentence sentenceid="cca8c1cfe38b4b464815ca94b10768cd" id="tgt9" class="tgtSentence"> For appended <legacyBold>Parameter</legacyBold> objects and all other objects, the <legacyBold>Name</legacyBold> property is read-only.</caps:sentence>
            <caps:sentence sentenceid="b2e9a95ccaf59e6d8a7711772b102027" id="tgt10" class="tgtSentence"> Names do not have to be unique within a collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="809a4748b3821bdf43edaf9c500cd01f" id="tgt11" class="tgtSentence">You can retrieve the <legacyBold>Name</legacyBold> property of an object by an ordinal reference, after which you can refer to the object directly by name.</caps:sentence>
            <caps:sentence sentenceid="4abcf3258115e3480a98ed7245015828" id="tgt12" class="tgtSentence"> For example, if <codeInline>rstMain.Properties(20).Name</codeInline> yields <codeInline>Updatability</codeInline>, you can subsequently refer to this property as <codeInline>rstMain.Properties("Updatability")</codeInline>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt13" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
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
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the name of an object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that indicates the name of an object.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Name</legacyBold> property to assign a name to or retrieve the name of a <legacyBold>Command</legacyBold>, <legacyBold>Property</legacyBold>, <legacyBold>Field</legacyBold>, or <legacyBold>Parameter</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">The value is read/write on a <legacyBold>Command</legacyBold> object and read-only on a <legacyBold>Property</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">For a <legacyBold>Field</legacyBold> object, <legacyBold>Name</legacyBold> is normally read-only.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> However, for new <legacyBold>Field</legacyBold> objects that have been appended to the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection of a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, <legacyBold>Name</legacyBold> is read/write only after the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property for the <legacyBold>Field</legacyBold> has been specified and the data provider has successfully added the new <legacyBold>Field</legacyBold> by calling the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method of the <legacyBold>Fields</legacyBold> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">For <legacyBold>Parameter</legacyBold> objects not yet appended to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection, the <legacyBold>Name</legacyBold> property is read/write.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> For appended <legacyBold>Parameter</legacyBold> objects and all other objects, the <legacyBold>Name</legacyBold> property is read-only.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Names do not have to be unique within a collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">You can retrieve the <legacyBold>Name</legacyBold> property of an object by an ordinal reference, after which you can refer to the object directly by name.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> For example, if <codeInline>rstMain.Properties(20).Name</codeInline> yields <codeInline>Updatability</codeInline>, you can subsequently refer to this property as <codeInline>rstMain.Properties("Updatability")</codeInline>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
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
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
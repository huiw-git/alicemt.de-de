---
title: "CommandType Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ca44809c-8647-48b6-a7fb-0be70a02f53e
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
# CommandType Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f4b8f7462343aa52cae0f5e75ca50112" id="tgt1" class="tgtSentence">Indicates the type of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9e465f7295a19d9c6b1c41071da2963d" id="tgt3" class="tgtSentence">Sets or returns one or more <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> values.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="71e4554df8f704de79bbc335fc0ec642" id="tgt4" class="tgtSentence">Do not use the <unmanagedCodeEntityReference>CommandTypeEnum</unmanagedCodeEntityReference> values of <legacyBold>adCmdFile</legacyBold> or <legacyBold>adCmdTableDirect</legacyBold> with <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference>.</caps:sentence>
              <caps:sentence sentenceid="4a690546de66b95d6f168329f4fcf200" id="tgt5" class="tgtSentence"> These values can only be used as options with the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> and <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> methods of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="aaf92632936f9f5fd7e0c7e51ab28dbf" id="tgt6" class="tgtSentence">Use the <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference> property to optimize evaluation of the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9f3e8bba36082257051f6083ba9bb591" id="tgt7" class="tgtSentence">If the <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference> property value is set to the default value, <legacyBold>adCmdUnknown</legacyBold>, you may experience diminished performance because ADO must make calls to the provider to determine if the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property is an SQL statement, a stored procedure, or a table name.</caps:sentence>
            <caps:sentence sentenceid="3fbe14e7137ffd616c336ff217b05728" id="tgt8" class="tgtSentence"> If you know what type of command you are using, setting the <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference> property instructs ADO to go directly to the relevant code.</caps:sentence>
            <caps:sentence sentenceid="05e921aaff4fff95e9de3f8741f73e16" id="tgt9" class="tgtSentence"> If the <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference> property does not match the type of command in the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property, an error occurs when you call the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dade4531-0bcc-4a52-8f86-b110ba2a3f9d">Visual Basic Example</link>
        <link xlink:href="0d9917c4-9ef0-4d7a-b4ce-4f1fa6ce1817">Visual C++ Example</link>
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++ Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the type of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns one or more <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> values.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src4" class="srcSentence">Do not use the <unmanagedCodeEntityReference>CommandTypeEnum</unmanagedCodeEntityReference> values of <legacyBold>adCmdFile</legacyBold> or <legacyBold>adCmdTableDirect</legacyBold> with <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference>.</caps:sentence>
              <caps:sentence id="src5" class="srcSentence"> These values can only be used as options with the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> and <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> methods of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Use the <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference> property to optimize evaluation of the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If the <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference> property value is set to the default value, <legacyBold>adCmdUnknown</legacyBold>, you may experience diminished performance because ADO must make calls to the provider to determine if the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property is an SQL statement, a stored procedure, or a table name.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> If you know what type of command you are using, setting the <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference> property instructs ADO to go directly to the relevant code.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If the <unmanagedCodeEntityReference>CommandType</unmanagedCodeEntityReference> property does not match the type of command in the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property, an error occurs when you call the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dade4531-0bcc-4a52-8f86-b110ba2a3f9d">Visual Basic Example</link>
        <link xlink:href="0d9917c4-9ef0-4d7a-b4ce-4f1fa6ce1817">Visual C++ Example</link>
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++ Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
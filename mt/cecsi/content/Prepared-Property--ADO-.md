---
title: "Prepared Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 11ca8825-765e-4bb4-a6ce-3f6564ad8755
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
# Prepared Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="199b94a5864737c07fa19d45954e2b2a" id="tgt1" class="tgtSentence">Indicates whether to save a compiled version of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> before execution.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f1df498ebbbf00b56b69649a745334f4" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Boolean</languageKeyword> value that, if set to <languageKeyword>True</languageKeyword>, indicates that the command should be prepared.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e05964a4244934eb2ce07f5b4971b320" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>Prepared</unmanagedCodeEntityReference> property to have the provider save a prepared (or compiled) version of the query specified in the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property before a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object's first execution.</caps:sentence>
            <caps:sentence sentenceid="387f3a56b074986f1cce0d08ff6c813b" id="tgt5" class="tgtSentence"> This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d01e8717686ddfc1585cddbb2b2fcfd1" id="tgt6" class="tgtSentence">If the property is <languageKeyword>False</languageKeyword>, the provider will execute the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object directly without creating a compiled version.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5eecb9f09a5bf0fd1d462dada135b868" id="tgt7" class="tgtSentence">If the provider does not support command preparation, it may return an error when this property is set to <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence sentenceid="aff789004fa341e1e19c0e410e738c35" id="tgt8" class="tgtSentence"> If the provider does not return an error, it simply ignores the request to prepare the command and sets the <unmanagedCodeEntityReference>Prepared</unmanagedCodeEntityReference> property to <languageKeyword>False</languageKeyword>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e3a3db2d-7f73-4288-ad08-5468f251d610">Visual Basic Example</link>
        <link xlink:href="f697ac1a-f125-42b5-bbf6-762a7fa30ae3">Visual C++ Example</link>
        <link xlink:href="fc52ea7c-1b3b-4874-9db9-4d2e01d794c3">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates whether to save a compiled version of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> before execution.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Boolean</languageKeyword> value that, if set to <languageKeyword>True</languageKeyword>, indicates that the command should be prepared.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>Prepared</unmanagedCodeEntityReference> property to have the provider save a prepared (or compiled) version of the query specified in the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property before a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object's first execution.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">If the property is <languageKeyword>False</languageKeyword>, the provider will execute the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object directly without creating a compiled version.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If the provider does not support command preparation, it may return an error when this property is set to <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> If the provider does not return an error, it simply ignores the request to prepare the command and sets the <unmanagedCodeEntityReference>Prepared</unmanagedCodeEntityReference> property to <languageKeyword>False</languageKeyword>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e3a3db2d-7f73-4288-ad08-5468f251d610">Visual Basic Example</link>
        <link xlink:href="f697ac1a-f125-42b5-bbf6-762a7fa30ae3">Visual C++ Example</link>
        <link xlink:href="fc52ea7c-1b3b-4874-9db9-4d2e01d794c3">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "CommandStream Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f78f61b6-87e0-48dc-961e-83d0e20da58e
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
# CommandStream Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a55801102c2b49571430872865f4d02e" id="tgt1" class="tgtSentence">Indicates the stream used as the input for a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="31be44374d533be6615d7ab845e7166a" id="tgt3" class="tgtSentence">Sets or returns the stream used as the input for a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="1a4560030da54f7acaa9339cd25d8d79" id="tgt4" class="tgtSentence"> The format for this stream is provider-specific; see your provider's documentation for details.</caps:sentence>
            <caps:sentence sentenceid="2598cef15b5474ff111c9281d256a30b" id="tgt5" class="tgtSentence"> This property is similar to the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property, which used to specify a string for the input of a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="237388636e8d0c4822783ba556a193bb" id="tgt6" class="tgtSentence">
              <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> are mutually exclusive.</caps:sentence>
            <caps:sentence sentenceid="bf9958f18048850ddd236a19bb412ffd" id="tgt7" class="tgtSentence"> When the user sets the <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> property, the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property will be set to the empty string ("").</caps:sentence>
            <caps:sentence sentenceid="d557937017a28d6d5e7592ff8cad56a6" id="tgt8" class="tgtSentence"> If the user sets the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property, the <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> property will be set to <languageKeyword>Nothing</languageKeyword>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bb0e5bf27cbb7c0b1a194847808e2693" id="tgt9" class="tgtSentence">The behaviors of the <legacyBold>Command.Parameters.Refresh</legacyBold> and <legacyBold>Command.Prepare</legacyBold> methods are defined by the provider.</caps:sentence>
            <caps:sentence sentenceid="46396bc1ec919dea17263de9be7f28be" id="tgt10" class="tgtSentence"> The values of parameters in a stream can not be refreshed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ad93a9d3da3c24a559b641679b270969" id="tgt11" class="tgtSentence">The input stream is not available to other ADO objects that return the source of a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="d1be5d618aad38316abf4c095eed9a3e" id="tgt12" class="tgtSentence"> For example, if the <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is set to a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object that has a stream as its input, <legacyBold>Recordset.Source</legacyBold> continues to return the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property, which contains an empty string (""), instead of the stream contents of the <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="246a69e0ccb099815fde51ad26083c9b" id="tgt13" class="tgtSentence">When using a command stream (as specified by <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference>), the only valid <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> values for the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property are <legacyBold>adCmdText</legacyBold> and <legacyBold>adCmdUnknown</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="b4d35a848a04b26a4ff80362bd1f7374" id="tgt14" class="tgtSentence"> Any other value causes an error.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt15" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
        <link xlink:href="329c3a71-ba88-4009-b04f-2f52195a5957">Dialect Property</link>
        <link xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the stream used as the input for a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns the stream used as the input for a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The format for this stream is provider-specific; see your provider's documentation for details.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This property is similar to the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property, which used to specify a string for the input of a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">
              <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> are mutually exclusive.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> When the user sets the <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> property, the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property will be set to the empty string ("").</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> If the user sets the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property, the <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> property will be set to <languageKeyword>Nothing</languageKeyword>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The behaviors of the <legacyBold>Command.Parameters.Refresh</legacyBold> and <legacyBold>Command.Prepare</legacyBold> methods are defined by the provider.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The values of parameters in a stream can not be refreshed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">The input stream is not available to other ADO objects that return the source of a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> For example, if the <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is set to a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object that has a stream as its input, <legacyBold>Recordset.Source</legacyBold> continues to return the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property, which contains an empty string (""), instead of the stream contents of the <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">When using a command stream (as specified by <unmanagedCodeEntityReference>CommandStream</unmanagedCodeEntityReference>), the only valid <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> values for the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property are <legacyBold>adCmdText</legacyBold> and <legacyBold>adCmdUnknown</legacyBold>.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> Any other value causes an error.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
        <link xlink:href="329c3a71-ba88-4009-b04f-2f52195a5957">Dialect Property</link>
        <link xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
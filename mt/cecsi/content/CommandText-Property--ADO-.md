---
title: "CommandText Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 4dd7e82a-8da5-4a4e-b439-11a29286fa0e
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
# CommandText Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bf4eb41278de970850ebd820f20a2f4d" id="tgt1" class="tgtSentence">Indicates the text of a command to be issued against a provider.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cf57f32d0ba9dcaac3dda0073e58cbb1" id="tgt3" class="tgtSentence">Gets or sets a <languageKeyword>String</languageKeyword> value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call.</caps:sentence>
            <caps:sentence sentenceid="783250a62f24211789c36f22b4b0fdb8" id="tgt4" class="tgtSentence"> The default is the empty string ("").</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="0d170eebd9ca60d30f5eeaefc4c93b65" id="tgt5" class="tgtSentence">Use the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property to set or return the text of a command represented by a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="fcee4cb5cc6f7bb816990042f713de62" id="tgt6" class="tgtSentence"> Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call.</caps:sentence>
            <caps:sentence sentenceid="b233045063527db9d0fb1ca21d5b576a" id="tgt7" class="tgtSentence"> An SQL statement must be of the particular dialect or version supported by the provider's query processor.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6f642a7b81c726cced430c6d9c6a13a6" id="tgt8" class="tgtSentence">If the <legacyLink xlink:href="11ca8825-765e-4bb4-a6ce-3f6564ad8755">Prepared</legacyLink> property of the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object is set to <languageKeyword>True</languageKeyword> and the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object is bound to an open connection when you set the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> or <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> methods.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="86b239fa75e83c22c159bbd2ef58134f" id="tgt9" class="tgtSentence">Depending on the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property setting, ADO may alter the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property.</caps:sentence>
            <caps:sentence sentenceid="f13f6a6548aec35e6ec04626ac7a6f43" id="tgt10" class="tgtSentence"> You can read the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property at any time to see the actual command text that ADO will use during execution.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8f2a6a47915a7b67a16ad416e5e99a8d" id="tgt11" class="tgtSentence">Use the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property to set or return a relative URL that specifies a resource, such as a file or directory.</caps:sentence>
            <caps:sentence sentenceid="cd6e7286d3df0648f1d199b4db742f38" id="tgt12" class="tgtSentence"> The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt13" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt14" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt15" class="tgtSentence">Applies To</caps:sentence>
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
        <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the text of a command to be issued against a provider.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Gets or sets a <languageKeyword>String</languageKeyword> value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default is the empty string ("").</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property to set or return the text of a command represented by a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> An SQL statement must be of the particular dialect or version supported by the provider's query processor.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">If the <legacyLink xlink:href="11ca8825-765e-4bb4-a6ce-3f6564ad8755">Prepared</legacyLink> property of the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object is set to <languageKeyword>True</languageKeyword> and the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object is bound to an open connection when you set the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> or <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> methods.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">Depending on the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property setting, ADO may alter the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> You can read the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property at any time to see the actual command text that ADO will use during execution.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">Use the <unmanagedCodeEntityReference>CommandText</unmanagedCodeEntityReference> property to set or return a relative URL that specifies a resource, such as a file or directory.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Applies To</caps:sentence>
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
        <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
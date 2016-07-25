---
title: "Parameter Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e010e794-7f0f-4026-8b5b-37328e437d63
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
# Parameter Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5a3c383707535982f2a8eb24d93912bc" id="tgt1" class="tgtSentence">Represents a parameter or argument associated with a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object based on a parameterized query or stored procedure.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="0070967a7a07f1a54937aafe9b5958a9" id="tgt2" class="tgtSentence">Many providers support parameterized commands.</caps:sentence>
            <caps:sentence sentenceid="d5abbb6ea5ef3870589ace0b15d826a2" id="tgt3" class="tgtSentence"> These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command.</caps:sentence>
            <caps:sentence sentenceid="4b0798efd67f705a4239851c78421b17" id="tgt4" class="tgtSentence"> For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="66f06723c5baa52a3900e36cdb2ce167" id="tgt5" class="tgtSentence">
              <legacyBold>Parameter</legacyBold> objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures.</caps:sentence>
            <caps:sentence sentenceid="27f14d5bcebb15a95ddacc6805347434" id="tgt6" class="tgtSentence"> Depending on the functionality of the provider, some collections, methods, or properties of a <legacyBold>Parameter</legacyBold> object may not be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fe92131b264a51140dc35a36db07fa94" id="tgt7" class="tgtSentence">With the collections, methods, and properties of a <legacyBold>Parameter</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="4edca217b949b22208f87d3ae555c85d" id="tgt8" class="tgtSentence">Set or return the name of a parameter with the <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a374c6fe65d8f3727f2b097a73b7ba51" id="tgt9" class="tgtSentence">Set or return the value of a parameter with the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property.</caps:sentence>
                <caps:sentence sentenceid="54f0541fcb762ae612f8417caccd8b0a" id="tgt10" class="tgtSentence">
                  <legacyBold>Value</legacyBold> is the default property of the <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="eff60652222f801ea492f71193bafc5b" id="tgt11" class="tgtSentence">Set or return parameter characteristics with the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink>, <legacyLink xlink:href="d5732578-3434-4dcd-a9f7-db1abd1b3b94">Direction</legacyLink>, <legacyLink xlink:href="1fa38e78-6b5b-414d-ba0a-3dd26b29b766">Precision</legacyLink>, <legacyLink xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale</legacyLink>, <legacyLink xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size</legacyLink>, and <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8cfae1801bb30f4892f401d1df7b27da" id="tgt12" class="tgtSentence">Pass long binary or character data to a parameter with the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c6c2f95bbd8e600ec1390f72e89d0c72" id="tgt13" class="tgtSentence">Access provider-specific attributes by using the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="e5a8c20a652bc8a0ef40064644f86944" id="tgt14" class="tgtSentence">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you want to call, you can use the <legacyLink xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter</legacyLink> method to create <legacyBold>Parameter</legacyBold> objects with the appropriate property settings and use the <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method to add them to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
            <caps:sentence sentenceid="4593c803d6d603f0f7e484ebe6ab9dee" id="tgt15" class="tgtSentence"> This lets you set and return parameter values without having to call the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method on the <legacyBold>Parameters</legacyBold> collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c31392f8c09fab7147617093aa4907cf" id="tgt16" class="tgtSentence">The <legacyBold>Parameter</legacyBold> object is not safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt17" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="96dbd54a9dcad9ddcfc1ad42603bf0cf" id="tgt18" class="tgtSentence">
                  <legacyLink xlink:href="53952466-4a9c-4396-bba6-cf44bec1da88">Parameter Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter Method</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a parameter or argument associated with a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object based on a parameterized query or stored procedure.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Many providers support parameterized commands.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">
              <legacyBold>Parameter</legacyBold> objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Depending on the functionality of the provider, some collections, methods, or properties of a <legacyBold>Parameter</legacyBold> object may not be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">With the collections, methods, and properties of a <legacyBold>Parameter</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Set or return the name of a parameter with the <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Set or return the value of a parameter with the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence">
                  <legacyBold>Value</legacyBold> is the default property of the <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Set or return parameter characteristics with the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink>, <legacyLink xlink:href="d5732578-3434-4dcd-a9f7-db1abd1b3b94">Direction</legacyLink>, <legacyLink xlink:href="1fa38e78-6b5b-414d-ba0a-3dd26b29b766">Precision</legacyLink>, <legacyLink xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale</legacyLink>, <legacyLink xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size</legacyLink>, and <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Pass long binary or character data to a parameter with the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Access provider-specific attributes by using the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src14" class="srcSentence">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you want to call, you can use the <legacyLink xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter</legacyLink> method to create <legacyBold>Parameter</legacyBold> objects with the appropriate property settings and use the <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method to add them to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> This lets you set and return parameter values without having to call the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method on the <legacyBold>Parameters</legacyBold> collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">The <legacyBold>Parameter</legacyBold> object is not safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">
                  <legacyLink xlink:href="53952466-4a9c-4396-bba6-cf44bec1da88">Parameter Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter Method</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
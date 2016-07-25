---
title: "Group Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e
caps.latest.revision: 9
caps.handback.revision: 9
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
# Group Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="351f462444c870f3123824990a4534e6" id="tgt1" class="tgtSentence">Represents a group account that has access permissions within a secured database.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e05d0690dc70344f28e071c863154f7b" id="tgt2" class="tgtSentence">The <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups</legacyLink> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all the catalog's group accounts.</caps:sentence>
            <caps:sentence sentenceid="5169498867f7b81768234480dd58593d" id="tgt3" class="tgtSentence"> The <legacyBold>Groups</legacyBold> collection for a <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> represents only the group to which the user belongs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c29911e4d8fbe5fbd62ed44f2e35aad8" id="tgt4" class="tgtSentence">With the properties, collections, and methods of a <legacyBold>Group</legacyBold> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="75822cb885ded0273ce205d1e7dfe63c" id="tgt5" class="tgtSentence">Identify the group with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="896f54b271c63b8f25789cb134276ab6" id="tgt6" class="tgtSentence">Determine whether a group has read, write, or delete permissions with the <legacyLink xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions</legacyLink> and <legacyLink xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f5a831f00c21ecf4c16eb8f3614cffc2" id="tgt7" class="tgtSentence">Access the user accounts that have memberships in the group with the <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="70cfb9c7f6eae3e43fd26bafb26757a1" id="tgt8" class="tgtSentence">Access provider-specific properties with the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt9" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f7d8bc553cdb2879c3ee45eea7dc3b70" id="tgt10" class="tgtSentence">
                  <legacyLink xlink:href="ba9642d0-9025-4eff-8885-e6e7f8154c73">Group Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
        <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a group account that has access permissions within a secured database.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups</legacyLink> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all the catalog's group accounts.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The <legacyBold>Groups</legacyBold> collection for a <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> represents only the group to which the user belongs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">With the properties, collections, and methods of a <legacyBold>Group</legacyBold> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Identify the group with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Determine whether a group has read, write, or delete permissions with the <legacyLink xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions</legacyLink> and <legacyLink xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Access the user accounts that have memberships in the group with the <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Access provider-specific properties with the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src9" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">
                  <legacyLink xlink:href="ba9642d0-9025-4eff-8885-e6e7f8154c73">Group Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
        <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
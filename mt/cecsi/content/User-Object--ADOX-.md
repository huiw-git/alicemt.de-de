---
title: "User Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f68e32ce-ef7c-407d-bdb5-d280947ae0e2
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
# User Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bef91ae23098e593c9dc83ba337e619b" id="tgt1" class="tgtSentence">Represents a user account that has access permissions within a secured database.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="95efcfd182d2df86bd3eb35709413fc5" id="tgt2" class="tgtSentence">The <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all the catalog's users.</caps:sentence>
            <caps:sentence sentenceid="7056ab9abb60650695bbc211f1388741" id="tgt3" class="tgtSentence"> The <unmanagedCodeEntityReference>Users</unmanagedCodeEntityReference> collection for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> represents only the users of the specific group.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="df16cf78a9aa03d9e7a4dab4ecd11336" id="tgt4" class="tgtSentence">With the properties, collections, and methods of a <unmanagedCodeEntityReference>User</unmanagedCodeEntityReference> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1b3d6a3a970e507772ed139c810ea8c3" id="tgt5" class="tgtSentence">Identify the user with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ad50dd397e8e3c1d6c4b7a1373a706b7" id="tgt6" class="tgtSentence">Change the password for a user with the <legacyLink xlink:href="d187fbc6-5fac-4abb-803d-bf344dcf0302">ChangePassword</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="822a056b402e3940960afc1a3d7c8308" id="tgt7" class="tgtSentence">Determine whether a user has read, write, or delete permissions with the <legacyLink xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions</legacyLink> and <legacyLink xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="854df4896eba26a97ebe4143871ad8df" id="tgt8" class="tgtSentence">Access the groups to which a user belongs with the <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="70cfb9c7f6eae3e43fd26bafb26757a1" id="tgt9" class="tgtSentence">Access provider-specific properties with the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b293e1a913c85d1b8ff76fb890861323" id="tgt10" class="tgtSentence">Determine the <legacyLink xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">ParentCatalog</legacyLink> for a user.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt11" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="c59294a70e32fe6fc4e250bf0d365738" id="tgt12" class="tgtSentence">
                  <legacyLink xlink:href="becd590c-0db7-485c-8bf4-fa3456e4ba20">User Object Properties, Methods, and Events</legacyLink> </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="aa366d98-8c7a-4189-bdd8-1d663b243d33">GetPermissions and SetPermissions Methods Example (VB)</link>
        <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
        <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a user account that has access permissions within a secured database.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users</legacyLink> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all the catalog's users.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The <unmanagedCodeEntityReference>Users</unmanagedCodeEntityReference> collection for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> represents only the users of the specific group.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">With the properties, collections, and methods of a <unmanagedCodeEntityReference>User</unmanagedCodeEntityReference> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Identify the user with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Change the password for a user with the <legacyLink xlink:href="d187fbc6-5fac-4abb-803d-bf344dcf0302">ChangePassword</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Determine whether a user has read, write, or delete permissions with the <legacyLink xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions</legacyLink> and <legacyLink xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Access the groups to which a user belongs with the <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Access provider-specific properties with the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Determine the <legacyLink xlink:href="a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273">ParentCatalog</legacyLink> for a user.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src11" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">
                  <legacyLink xlink:href="becd590c-0db7-485c-8bf4-fa3456e4ba20">User Object Properties, Methods, and Events</legacyLink> </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="aa366d98-8c7a-4189-bdd8-1d663b243d33">GetPermissions and SetPermissions Methods Example (VB)</link>
        <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
        <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
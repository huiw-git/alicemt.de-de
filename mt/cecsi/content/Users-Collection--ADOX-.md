---
title: "Users Collection (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 0a30fa74-6f10-4410-bd70-882e7c43cd46
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
# Users Collection (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="36792a5b861b4a31eb2748719c840c87" id="tgt1" class="tgtSentence">Contains all stored <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> objects of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">catalog</legacyLink> or <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">group</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9bf061687ecf19e483647cd7f8275c62" id="tgt2" class="tgtSentence">The <unmanagedCodeEntityReference>Users</unmanagedCodeEntityReference> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all the catalog's users.</caps:sentence>
            <caps:sentence sentenceid="6cbf681655332f6cae7d06aea9d06300" id="tgt3" class="tgtSentence"> The <unmanagedCodeEntityReference>Users</unmanagedCodeEntityReference> collection for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> represents only the users that have a membership in the specific group.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c06d82107f4fbd24915ff324222bd118" id="tgt4" class="tgtSentence">The <legacyLink xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append</legacyLink> method for a <unmanagedCodeEntityReference>Users</unmanagedCodeEntityReference> collection is unique for ADOX.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt5" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f9330f431712c8063d0ceb04c27a253a" id="tgt6" class="tgtSentence">Add a new user to the collection by using the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ed0be1c652e041a462a56d678a7a9845" id="tgt7" class="tgtSentence">The remaining properties and methods are standard to ADO collections.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt8" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="0a3efd22f3bc964b6222d02a11e59cce" id="tgt9" class="tgtSentence">Access a user in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0d8f7d0bf716c9c02ba0f7527fa1ff9c" id="tgt10" class="tgtSentence">Return the number of users contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a5a5bd6bcee8123921ae4c50f38eba75" id="tgt11" class="tgtSentence">Remove a user from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2cece3526fcf35dcf7ce17482562dd9f" id="tgt12" class="tgtSentence">Update the objects in the collection to reflect the current database's schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="4287c7e33448f248a3a6964cc0769d86" id="tgt13" class="tgtSentence">Before appending a <legacyBold>User</legacyBold> object to the <legacyBold>Users</legacyBold> collection of a <legacyBold>Group</legacyBold> object, a <legacyBold>User</legacyBold> object with the same <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> as the one to be appended must already exist in the <legacyBold>Users</legacyBold> collection of the <legacyBold>Catalog</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt14" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="ee2bc4abb2d655a74bf952a2dbc552d4" id="tgt15" class="tgtSentence">             <legacyLink xlink:href="1b89a12f-96bc-48b3-a88d-4da74780ea40">Users Collection Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="aa366d98-8c7a-4189-bdd8-1d663b243d33">GetPermissions and SetPermissions Methods Example (VB)</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all stored <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> objects of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">catalog</legacyLink> or <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">group</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <unmanagedCodeEntityReference>Users</unmanagedCodeEntityReference> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all the catalog's users.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The <unmanagedCodeEntityReference>Users</unmanagedCodeEntityReference> collection for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> represents only the users that have a membership in the specific group.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <legacyLink xlink:href="b80bc5d5-78ca-4f75-956b-2ac658029cc7">Append</legacyLink> method for a <unmanagedCodeEntityReference>Users</unmanagedCodeEntityReference> collection is unique for ADOX.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Add a new user to the collection by using the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src7" class="srcSentence">The remaining properties and methods are standard to ADO collections.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Access a user in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Return the number of users contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Remove a user from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Update the objects in the collection to reflect the current database's schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence">Before appending a <legacyBold>User</legacyBold> object to the <legacyBold>Users</legacyBold> collection of a <legacyBold>Group</legacyBold> object, a <legacyBold>User</legacyBold> object with the same <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> as the one to be appended must already exist in the <legacyBold>Users</legacyBold> collection of the <legacyBold>Catalog</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src14" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">             <legacyLink xlink:href="1b89a12f-96bc-48b3-a88d-4da74780ea40">Users Collection Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="aa366d98-8c7a-4189-bdd8-1d663b243d33">GetPermissions and SetPermissions Methods Example (VB)</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
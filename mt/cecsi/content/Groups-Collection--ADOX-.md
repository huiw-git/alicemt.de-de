---
title: "Groups Collection (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 09aa7b0a-69d5-4564-80a7-20ad8189670f
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
# Groups Collection (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4f8f7e6d82f0ccc76055a9a638fd3ed0" id="tgt1" class="tgtSentence">Contains all stored <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> objects of a catalog or user.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="30b8c51fb892b8371ec778832efc0a4f" id="tgt2" class="tgtSentence">The <legacyBold>Groups</legacyBold> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all of the catalog's group accounts.</caps:sentence>
            <caps:sentence sentenceid="5169498867f7b81768234480dd58593d" id="tgt3" class="tgtSentence"> The <legacyBold>Groups</legacyBold> collection for a <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> represents only the group to which the user belongs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c1c827f5e0a86739e227390c4fad87dc" id="tgt4" class="tgtSentence">The <legacyLink xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append</legacyLink> method for a <legacyBold>Groups</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt5" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="fb7e7cd6579180a46e8722c8ca9e1a62" id="tgt6" class="tgtSentence">Add a new security group to the collection with the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
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
                <caps:sentence sentenceid="3902e7ddca28477de511a28dda364278" id="tgt9" class="tgtSentence">Access a group in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f7edcf2351c712e45f0692cbcd6c0d59" id="tgt10" class="tgtSentence">Return the number of groups contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f30829e157aced2eddcc827ba595fadf" id="tgt11" class="tgtSentence">Remove a group from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="918e7bfcf1fb8892b265d13bf57519fd" id="tgt12" class="tgtSentence">Update the objects in the collection to reflect the current database schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="63833a0993dca14e1e95bcc86b78a9b3" id="tgt13" class="tgtSentence">Before appending a <unmanagedCodeEntityReference>Group</unmanagedCodeEntityReference> object to the <legacyBold>Groups</legacyBold> collection of a <unmanagedCodeEntityReference>User</unmanagedCodeEntityReference> object, a <unmanagedCodeEntityReference>Group</unmanagedCodeEntityReference> object with the same <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> as the one to be appended must already exist in the <legacyBold>Groups</legacyBold> collection of the <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt14" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="0776457f-bf78-4a79-96bf-a17136d45811">
                  <caps:sentence sentenceid="77b4443e561953c123c5dd14fa1ced91" id="tgt15" class="tgtSentence">Groups Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all stored <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> objects of a catalog or user.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <legacyBold>Groups</legacyBold> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> represents all of the catalog's group accounts.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The <legacyBold>Groups</legacyBold> collection for a <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> represents only the group to which the user belongs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <legacyLink xlink:href="56b94fc6-7ef0-4e4a-82a3-033b94c46036">Append</legacyLink> method for a <legacyBold>Groups</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Add a new security group to the collection with the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
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
                <caps:sentence id="src9" class="srcSentence">Access a group in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Return the number of groups contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Remove a group from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Update the objects in the collection to reflect the current database schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence">Before appending a <unmanagedCodeEntityReference>Group</unmanagedCodeEntityReference> object to the <legacyBold>Groups</legacyBold> collection of a <unmanagedCodeEntityReference>User</unmanagedCodeEntityReference> object, a <unmanagedCodeEntityReference>Group</unmanagedCodeEntityReference> object with the same <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> as the one to be appended must already exist in the <legacyBold>Groups</legacyBold> collection of the <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src14" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="0776457f-bf78-4a79-96bf-a17136d45811">
                  <caps:sentence id="src15" class="srcSentence">Groups Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
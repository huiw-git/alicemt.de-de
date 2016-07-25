---
title: "View Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 653421ce-7b94-43d0-9bc6-4900f8f2af45
caps.latest.revision: 8
caps.handback.revision: 8
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
# View Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2b5fe89b025058db9992da035595e2dc" id="tgt1" class="tgtSentence">Represents a filtered set of records or a virtual table.</caps:sentence>
          <caps:sentence sentenceid="b5a89ae6f789a82d3b1e6b0651673e70" id="tgt2" class="tgtSentence"> When used in conjunction with the ADO <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object, the <legacyBold>View</legacyBold> object can be used for adding, deleting, or modifying views.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="79f0948b46eab4fa0d27ca72beaa5e27" id="tgt3" class="tgtSentence">A view is a virtual table, created from other database tables or views.</caps:sentence>
            <caps:sentence sentenceid="ca82b6ac2fcdf9bdc1344e8d7f5e50f9" id="tgt4" class="tgtSentence"> The <legacyBold>View</legacyBold> object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fcfe3c01e5493df527883b79d66d96f8" id="tgt5" class="tgtSentence">With the properties of a <legacyBold>View</legacyBold> object, you can:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="c574016128d6804912c63f3b4a968342" id="tgt6" class="tgtSentence">Identify the view with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1c5f838707d7f816a0651228c4a821cd" id="tgt7" class="tgtSentence">Specify the ADO <legacyBold>Command</legacyBold> object that can be used to add, delete, or modify views with the <legacyLink xlink:href="bcc9146f-586f-4e69-9c10-863440c9cffa">Command</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1f6ac71f5a656b23e407d68029eef914" id="tgt8" class="tgtSentence">Return date information with the <legacyLink xlink:href="2bf4b00d-045c-444e-8af7-8af6297ed418">DateCreated</legacyLink> and <legacyLink xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt9" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="02b5ba88-cacd-4a68-881b-974824ea4a04">
                  <caps:sentence sentenceid="8823052124f58d18962334ab3390b97e" id="tgt10" class="tgtSentence">View Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
        <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a filtered set of records or a virtual table.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When used in conjunction with the ADO <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object, the <legacyBold>View</legacyBold> object can be used for adding, deleting, or modifying views.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">A view is a virtual table, created from other database tables or views.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The <legacyBold>View</legacyBold> object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">With the properties of a <legacyBold>View</legacyBold> object, you can:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Identify the view with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Specify the ADO <legacyBold>Command</legacyBold> object that can be used to add, delete, or modify views with the <legacyLink xlink:href="bcc9146f-586f-4e69-9c10-863440c9cffa">Command</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Return date information with the <legacyLink xlink:href="2bf4b00d-045c-444e-8af7-8af6297ed418">DateCreated</legacyLink> and <legacyLink xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src9" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="02b5ba88-cacd-4a68-881b-974824ea4a04">
                  <caps:sentence id="src10" class="srcSentence">View Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
        <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
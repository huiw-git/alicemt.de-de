---
title: "ActiveConnection Property (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 25fff69b-7556-4a28-b6f5-600a4bb0f607
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
# ActiveConnection Property (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6fa99c2c99b9f89d7ebf4921180cbe86" id="tgt1" class="tgtSentence">Indicates the ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object to which the <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> belongs.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2a9b727278d364d87677ac4d4d4bb7e4" id="tgt3" class="tgtSentence">Sets a <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object or a <languageKeyword>String</languageKeyword> containing the definition for a connection.</caps:sentence>
            <caps:sentence sentenceid="efb8f63ba0de7f03a4e6681db4eefd02" id="tgt4" class="tgtSentence"> Returns the active <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="6c12eb3c6c08d0e01eeccf487be81a0f" id="tgt5" class="tgtSentence">The default value is a null object reference.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt6" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="413263a8-05c0-4404-929d-69f82b987ba3">Command and CommandText Properties Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="7df1089e-69b7-476e-9244-19947c087351">Parameters Collection, Command Property Example (VB)</link>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="499679bd-287b-487d-bdfb-3803abffec1c">Procedures Refresh Method Example (VB)</link>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="cdad2d66-6ade-40dc-9e74-e40cfa9bc127">Views Refresh Method Example (VB)</link>
        <link xlink:href="64f5c21c-b581-42d8-bdc7-c4f1bebaf105">Create Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object to which the <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> belongs.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets a <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object or a <languageKeyword>String</languageKeyword> containing the definition for a connection.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Returns the active <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The default value is a null object reference.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="413263a8-05c0-4404-929d-69f82b987ba3">Command and CommandText Properties Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="7df1089e-69b7-476e-9244-19947c087351">Parameters Collection, Command Property Example (VB)</link>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="499679bd-287b-487d-bdfb-3803abffec1c">Procedures Refresh Method Example (VB)</link>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="cdad2d66-6ade-40dc-9e74-e40cfa9bc127">Views Refresh Method Example (VB)</link>
        <link xlink:href="64f5c21c-b581-42d8-bdc7-c4f1bebaf105">Create Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
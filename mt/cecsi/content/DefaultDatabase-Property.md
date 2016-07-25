---
title: "DefaultDatabase Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 41e8a8dd-e69c-4a09-8736-93502e01961c
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
# DefaultDatabase Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6f555191abbbfdcaf0f9a2b4285f0e22" id="tgt1" class="tgtSentence">Indicates the default database for a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db14c6556c23a78d8559bacff45f47a4" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that evaluates to the name of a database available from the provider.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="146a7c50698a5d18fef9ddd6fef63008" id="tgt4" class="tgtSentence">Use the <legacyBold>DefaultDatabase</legacyBold> property to set or return the name of the default database on a specific <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="795de7699b0d986913249003a3c46c56" id="tgt5" class="tgtSentence">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database.</caps:sentence>
            <caps:sentence sentenceid="282e6980b885fa876695d0afd8f783d2" id="tgt6" class="tgtSentence"> To access objects in a database other than the one specified in the <legacyBold>DefaultDatabase</legacyBold> property, you must qualify object names with the desired database name.</caps:sentence>
            <caps:sentence sentenceid="c1a3771eedbc15f1f0b5e793fbc5f6ff" id="tgt7" class="tgtSentence"> Upon connection, the provider will write default database information to the <legacyBold>DefaultDatabase</legacyBold> property.</caps:sentence>
            <caps:sentence sentenceid="0af4d8ceb294a0d415cc21187b6d1f09" id="tgt8" class="tgtSentence"> Some providers allow only one database per connection, in which case you cannot change the <legacyBold>DefaultDatabase</legacyBold> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f1bdae35a71b36ff94994835a01dd0d8" id="tgt9" class="tgtSentence">Some data sources and providers may not support this feature, and may return an error or an empty string.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="c6ff7f1256cc8c9fcf4b61745d333c0d" id="tgt10" class="tgtSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   This property is not available on a client-side <legacyBold>Connection</legacyBold> object.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt11" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="677e1dbe-bcf6-4028-a62c-e99b1c88bf7b">Visual Basic Example</link>
        <link xlink:href="d9868c99-425a-4b10-af67-1929ed513fda">Visual C++ Example</link>
        <link xlink:href="fdc26576-37d0-4fa1-9afa-75d0e7133675">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the default database for a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that evaluates to the name of a database available from the provider.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>DefaultDatabase</legacyBold> property to set or return the name of the default database on a specific <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> To access objects in a database other than the one specified in the <legacyBold>DefaultDatabase</legacyBold> property, you must qualify object names with the desired database name.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Upon connection, the provider will write default database information to the <legacyBold>DefaultDatabase</legacyBold> property.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Some providers allow only one database per connection, in which case you cannot change the <legacyBold>DefaultDatabase</legacyBold> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">Some data sources and providers may not support this feature, and may return an error or an empty string.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src10" class="srcSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   This property is not available on a client-side <legacyBold>Connection</legacyBold> object.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="677e1dbe-bcf6-4028-a62c-e99b1c88bf7b">Visual Basic Example</link>
        <link xlink:href="d9868c99-425a-4b10-af67-1929ed513fda">Visual C++ Example</link>
        <link xlink:href="fdc26576-37d0-4fa1-9afa-75d0e7133675">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Property Object (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b2a4767c-03c7-4935-a3bc-df3e1a38a009
caps.latest.revision: 5
caps.handback.revision: 5
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
# Property Object (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e13e71f844c46f3e873303d3a5bbc051" id="tgt1" class="tgtSentence">Represents a dynamic characteristic of an ADO object that is defined by the provider.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9691608e01c3641684541802db4843fd" id="tgt2" class="tgtSentence">ADO objects have two types of properties: built-in and dynamic.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="34660eaf25649fab722283c2e26ac948" id="tgt3" class="tgtSentence">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the <codeInline>MyObject.Property</codeInline> syntax.</caps:sentence>
            <caps:sentence sentenceid="0c882b91761a0a9da00acdc174ab1358" id="tgt4" class="tgtSentence"> They do not appear as <legacyBold>Property</legacyBold> objects in an object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection, so although you can change their values, you cannot modify their characteristics.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c6a5a17c8ed0eea2c0dfc3cb5a55fb16" id="tgt5" class="tgtSentence">Dynamic properties are defined by the underlying data provider, and appear in the <legacyBold>Properties</legacyBold> collection for the appropriate ADO object.</caps:sentence>
            <caps:sentence sentenceid="85e749c742fbd923ddef766108805a85" id="tgt6" class="tgtSentence"> For example, a property specific to the provider may indicate if a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object supports transactions or updating.</caps:sentence>
            <caps:sentence sentenceid="3de59f7c76ea0128dfe3142d0b0fbe67" id="tgt7" class="tgtSentence"> These additional properties will appear as <legacyBold>Property</legacyBold> objects in that <legacyBold>Recordset</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="2f8c841b4f27a9c305714f53cc1d177e" id="tgt8" class="tgtSentence"> Dynamic properties can be referenced only through the collection, using the <codeInline>MyObject.Properties(0)</codeInline> or <codeInline>MyObject.Properties("Name")</codeInline> syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1c08354a2624dc3b87b7587e5140890f" id="tgt9" class="tgtSentence">You cannot delete either kind of property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="eb642942e4196dd447ab5bae83bff696" id="tgt10" class="tgtSentence">A dynamic <legacyBold>Property</legacyBold> object has four built-in properties of its own:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3d54fbf7f193debf84ae3845e76a7524" id="tgt11" class="tgtSentence">The <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property is a string that identifies the property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0cba58492f9d421691ba1fba46f68fcc" id="tgt12" class="tgtSentence">The <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> property is an integer that specifies the property data type.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="cff778310dbc75c463e56090fd03f09e" id="tgt13" class="tgtSentence">The <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property is a variant that contains the property setting.</caps:sentence>
                <caps:sentence sentenceid="fb7ddeaca01dd43d87d9fa5d494c6252" id="tgt14" class="tgtSentence">
                  <legacyBold>Value</legacyBold> is the default property for a <legacyBold>Property</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a48f251c1d41c3905b0e609c4d3ab04f" id="tgt15" class="tgtSentence">The <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property is a long value that indicates characteristics of the property specific to the provider.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt16" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="0d69a7192cd03b11a3fa26d87babb035" id="tgt17" class="tgtSentence">
                  <legacyLink xlink:href="21f67a7d-6273-4648-9abd-2236650efa4c">Property Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a dynamic characteristic of an ADO object that is defined by the provider.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">ADO objects have two types of properties: built-in and dynamic.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the <codeInline>MyObject.Property</codeInline> syntax.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> They do not appear as <legacyBold>Property</legacyBold> objects in an object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection, so although you can change their values, you cannot modify their characteristics.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">Dynamic properties are defined by the underlying data provider, and appear in the <legacyBold>Properties</legacyBold> collection for the appropriate ADO object.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For example, a property specific to the provider may indicate if a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object supports transactions or updating.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> These additional properties will appear as <legacyBold>Property</legacyBold> objects in that <legacyBold>Recordset</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Dynamic properties can be referenced only through the collection, using the <codeInline>MyObject.Properties(0)</codeInline> or <codeInline>MyObject.Properties("Name")</codeInline> syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">You cannot delete either kind of property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">A dynamic <legacyBold>Property</legacyBold> object has four built-in properties of its own:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">The <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property is a string that identifies the property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">The <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> property is an integer that specifies the property data type.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">The <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property is a variant that contains the property setting.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence">
                  <legacyBold>Value</legacyBold> is the default property for a <legacyBold>Property</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">The <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property is a long value that indicates characteristics of the property specific to the provider.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src16" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">
                  <legacyLink xlink:href="21f67a7d-6273-4648-9abd-2236650efa4c">Property Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
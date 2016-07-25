---
title: "DataSpace (ADO/WFC Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 950d45d8-07de-467b-b255-f9a7b997204c
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
# DataSpace (ADO/WFC Syntax)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="998ef7781c1c2da7b81b0e1d79a912e3" id="tgt1" class="tgtSentence">The <legacyBold>createObject</legacyBold> method of the <legacyBold>DataSpace</legacyBold> class specifies both a business object to process client application requests (<legacyItalic>progid</legacyItalic>) and the communications protocol and server (<legacyItalic>connection</legacyItalic>).</caps:sentence>
          <caps:sentence sentenceid="fb777723248eca1d3beea143c54b56c9" id="tgt2" class="tgtSentence">
            <legacyBold>createObject</legacyBold> returns an <legacyLink xlink:href="f68f58bc-ad28-46cc-9fb3-099e1a678397">ObjectProxy</legacyLink> object that represents the server.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="bf01303ec05e42a8b2352d82e9a911f6" id="tgt3" class="tgtSentence">package com.ms.wfc.data</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="6ca268371eeb5d93eefeb68f96157666" id="tgt4" class="tgtSentence">Constructor</caps:sentence>
            </title>
            <content>
              <code>public DataSpace()</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt5" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public static ObjectProxy DataSpace.createObject(String
    progid, String connection)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt6" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public static int getInternetTimeout()
public static void setInternetTimeout(int plInetTimeout)</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>createObject</legacyBold> method of the <legacyBold>DataSpace</legacyBold> class specifies both a business object to process client application requests (<legacyItalic>progid</legacyItalic>) and the communications protocol and server (<legacyItalic>connection</legacyItalic>).</caps:sentence>
          <caps:sentence id="src2" class="srcSentence">
            <legacyBold>createObject</legacyBold> returns an <legacyLink xlink:href="f68f58bc-ad28-46cc-9fb3-099e1a678397">ObjectProxy</legacyLink> object that represents the server.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">package com.ms.wfc.data</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src4" class="srcSentence">Constructor</caps:sentence>
            </title>
            <content>
              <code>public DataSpace()</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src5" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public static ObjectProxy DataSpace.createObject(String
    progid, String connection)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src6" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public static int getInternetTimeout()
public static void setInternetTimeout(int plInetTimeout)</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
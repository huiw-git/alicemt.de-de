---
title: "Source Property (ADO Recordset)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a05ba2c9-2821-4343-8607-4de9b764ec91
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
# Source Property (ADO Recordset)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7e89ae12c68904629621773cf83463f5" id="tgt1" class="tgtSentence">Indicates the data source for a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="3cb6b736b22901a463198d30c54d4dff" id="tgt3" class="tgtSentence">Sets a <legacyBold>String</legacyBold> value or <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object reference; returns only a <legacyBold>String</legacyBold> value that indicates the source of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4b0ee85e6a1b5374c1adee977c4b2607" id="tgt4" class="tgtSentence">Use the <legacyBold>Source</legacyBold> property to specify a data source for a <legacyBold>Recordset</legacyBold> object using one of the following: a <legacyBold>Command</legacyBold> object variable, an SQL statement, a stored procedure, or a table name.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0ab6932ab91174a046858b0a972c3ad8" id="tgt5" class="tgtSentence">If you set the <legacyBold>Source</legacyBold> property to a <legacyBold>Command</legacyBold> object, the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property of the <legacyBold>Recordset</legacyBold> object will inherit the value of the <legacyBold>ActiveConnection</legacyBold> property for the specified <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="00d46b9aebb1af5bb11b1cb60e1206c3" id="tgt6" class="tgtSentence"> However, reading the <legacyBold>Source</legacyBold> property does not return a <legacyBold>Command</legacyBold> object; instead, it returns the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property of the <legacyBold>Command</legacyBold> object to which you set the <legacyBold>Source</legacyBold> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bbb87a41d7699f3f4c5f06917f7adae1" id="tgt7" class="tgtSentence">If the <legacyBold>Source</legacyBold> property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate <legacyItalic>Options</legacyItalic> argument with the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method call.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8307a261cf663f1cd5d07b5e47186f3a" id="tgt8" class="tgtSentence">The <legacyBold>Source</legacyBold> property is read/write for closed <legacyBold>Recordset</legacyBold> objects and read-only for open <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="7c83eb01-71c7-4c5d-9778-6270471c8164">Visual Basic Example</link>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
        <link xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source Property (ADO Record)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the data source for a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets a <legacyBold>String</legacyBold> value or <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object reference; returns only a <legacyBold>String</legacyBold> value that indicates the source of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Source</legacyBold> property to specify a data source for a <legacyBold>Recordset</legacyBold> object using one of the following: a <legacyBold>Command</legacyBold> object variable, an SQL statement, a stored procedure, or a table name.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">If you set the <legacyBold>Source</legacyBold> property to a <legacyBold>Command</legacyBold> object, the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property of the <legacyBold>Recordset</legacyBold> object will inherit the value of the <legacyBold>ActiveConnection</legacyBold> property for the specified <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> However, reading the <legacyBold>Source</legacyBold> property does not return a <legacyBold>Command</legacyBold> object; instead, it returns the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property of the <legacyBold>Command</legacyBold> object to which you set the <legacyBold>Source</legacyBold> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If the <legacyBold>Source</legacyBold> property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate <legacyItalic>Options</legacyItalic> argument with the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method call.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <legacyBold>Source</legacyBold> property is read/write for closed <legacyBold>Recordset</legacyBold> objects and read-only for open <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="7c83eb01-71c7-4c5d-9778-6270471c8164">Visual Basic Example</link>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
        <link xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source Property (ADO Record)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
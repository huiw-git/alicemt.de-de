---
title: "DataSource Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 300a702a-3544-48c5-b759-83b511fe97e0
caps.latest.revision: 6
caps.handback.revision: 6
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
# DataSource Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bee32433fe60c38519b4b115a27e555c" id="tgt1" class="tgtSentence">Indicates an object that contains data to be represented as a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="672ab9cd07b916a492fb8c35b46a4a98" id="tgt2" class="tgtSentence">This property is used to create data-bound controls with the Data Environment.</caps:sentence>
            <caps:sentence sentenceid="5aaf25de8a2cef7049afc04eab1ab20f" id="tgt3" class="tgtSentence"> The Data Environment maintains collections of data (data sources) containing named objects (data members) that will be represented as a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object<legacyItalic>.</legacyItalic></caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="be2210ff93f450cc8943cce7371bff70" id="tgt4" class="tgtSentence">The <legacyLink xlink:href="2c8fb09e-10ad-49b5-ab41-2603771780d9">DataMember</legacyLink> and <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> properties must be used in conjunction.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7b8f526b9d0ea695722069bef8a0480a" id="tgt5" class="tgtSentence">The object referenced must implement the <legacyBold>IDataSource</legacyBold> interface and must contain an <legacyBold>IRowset</legacyBold> interface.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="9366282e11c151558bdfaab4a264aa1b" id="tgt6" class="tgtSentence">Usage</caps:sentence>
            </title>
            <content>
              <code>Dim rs as New ADODB.Recordset
rs.DataMember = "Command"     'Name of the rowset to bind to.
Set rs.DataSource = myDE      'Name of the object containing an IRowset.</code>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2c8fb09e-10ad-49b5-ab41-2603771780d9">DataMember Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates an object that contains data to be represented as a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">This property is used to create data-bound controls with the Data Environment.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> The Data Environment maintains collections of data (data sources) containing named objects (data members) that will be represented as a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object<legacyItalic>.</legacyItalic></caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <legacyLink xlink:href="2c8fb09e-10ad-49b5-ab41-2603771780d9">DataMember</legacyLink> and <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> properties must be used in conjunction.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">The object referenced must implement the <legacyBold>IDataSource</legacyBold> interface and must contain an <legacyBold>IRowset</legacyBold> interface.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src6" class="srcSentence">Usage</caps:sentence>
            </title>
            <content>
              <code>Dim rs as New ADODB.Recordset
rs.DataMember = "Command"     'Name of the rowset to bind to.
Set rs.DataSource = myDE      'Name of the object containing an IRowset.</code>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2c8fb09e-10ad-49b5-ab41-2603771780d9">DataMember Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
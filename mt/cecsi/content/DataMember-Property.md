---
title: "DataMember Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 2c8fb09e-10ad-49b5-ab41-2603771780d9
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
# DataMember Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="375105796e32d7525f4511b2343cd746" id="tgt1" class="tgtSentence">Indicates the name of the data member that will be retrieved from the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> referenced by the <legacyLink xlink:href="300a702a-3544-48c5-b759-83b511fe97e0">DataSource</legacyLink> property.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="95c701ec7ef8444399749df7594c0234" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value.</caps:sentence>
            <caps:sentence sentenceid="93463317a5c761f4418e62b0b63a06ca" id="tgt4" class="tgtSentence"> The name is not case sensitive.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="672ab9cd07b916a492fb8c35b46a4a98" id="tgt5" class="tgtSentence">This property is used to create data-bound controls with the Data Environment.</caps:sentence>
            <caps:sentence sentenceid="7336fa76dbb592444e0650b4f67f2e1c" id="tgt6" class="tgtSentence"> The Data Environment maintains collections of data (data sources) containing named objects (data members) that will be represented as a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="13783a40f336904c00f96da658e86bb2" id="tgt7" class="tgtSentence">The <unmanagedCodeEntityReference>DataMember</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> properties must be used together.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3d2abdeb470e136cfdcbec5d4858fc36" id="tgt8" class="tgtSentence">The <unmanagedCodeEntityReference>DataMember</unmanagedCodeEntityReference> property determines which object specified by the <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> property will be represented as a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="ce0c9cc61245aaaaca506394157f6f25" id="tgt9" class="tgtSentence"> The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object must be closed before this property is set.</caps:sentence>
            <caps:sentence sentenceid="2592c1a83323421a2820ab7e4229728b" id="tgt10" class="tgtSentence"> An error is generated if the <unmanagedCodeEntityReference>DataMember</unmanagedCodeEntityReference> property is not set before the <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> property, or if the <unmanagedCodeEntityReference>DataMember</unmanagedCodeEntityReference> name is not recognized by the object specified in the <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="9366282e11c151558bdfaab4a264aa1b" id="tgt11" class="tgtSentence">Usage</caps:sentence>
            </title>
            <content>
              <code>Dim rs as New ADODB.Recordset
rs.DataMember = "Command"     'Name of the rowset to bind to
Set rs.DataSource = myDE      'Name of the object containing an IRowset</code>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="300a702a-3544-48c5-b759-83b511fe97e0">DataSource Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the name of the data member that will be retrieved from the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> referenced by the <legacyLink xlink:href="300a702a-3544-48c5-b759-83b511fe97e0">DataSource</legacyLink> property.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The name is not case sensitive.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">This property is used to create data-bound controls with the Data Environment.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The Data Environment maintains collections of data (data sources) containing named objects (data members) that will be represented as a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <unmanagedCodeEntityReference>DataMember</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> properties must be used together.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <unmanagedCodeEntityReference>DataMember</unmanagedCodeEntityReference> property determines which object specified by the <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> property will be represented as a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object must be closed before this property is set.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> An error is generated if the <unmanagedCodeEntityReference>DataMember</unmanagedCodeEntityReference> property is not set before the <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> property, or if the <unmanagedCodeEntityReference>DataMember</unmanagedCodeEntityReference> name is not recognized by the object specified in the <unmanagedCodeEntityReference>DataSource</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src11" class="srcSentence">Usage</caps:sentence>
            </title>
            <content>
              <code>Dim rs as New ADODB.Recordset
rs.DataMember = "Command"     'Name of the rowset to bind to
Set rs.DataSource = myDE      'Name of the object containing an IRowset</code>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="300a702a-3544-48c5-b759-83b511fe97e0">DataSource Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
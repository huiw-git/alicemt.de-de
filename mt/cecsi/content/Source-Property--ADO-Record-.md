---
title: "Source Property (ADO Record)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 2c18279e-6f35-4af0-b12e-8f1543d9ed20
caps.latest.revision: 12
caps.handback.revision: 12
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
# Source Property (ADO Record)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0da33f19a09d8bdbef502b3e4b23da4a" id="tgt1" class="tgtSentence">Indicates the data source or object represented by the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f0a0ef1d7681285a2d31c563af5bb628" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Variant</languageKeyword> value that indicates the entity represented by the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="bf0c9515272676d470fe84f3e96002a3" id="tgt4" class="tgtSentence">The <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property returns the <parameterReference>Source</parameterReference> argument of the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="d04ade0f9570d1cc034ee6931f5f026c" id="tgt5" class="tgtSentence"> It can contain an absolute or relative URL string.</caps:sentence>
            <caps:sentence sentenceid="04becdd5f4889a7f2c59fb8f9be2b769" id="tgt6" class="tgtSentence"> An absolute URL can be used without setting the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property to directly open the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="2bc2749eb220d0aa5af9039079cc6b1e" id="tgt7" class="tgtSentence"> An implicit <legacyBold>Connection</legacyBold> object is created in this case.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d41252476ba28a33f82bea45bce41c88" id="tgt8" class="tgtSentence">The <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property can also contain a reference to an already open <legacyBold>Recordset</legacyBold>, which opens a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object representing the current row in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="67f728dc12ce26b58c271c52c7ef41be" id="tgt9" class="tgtSentence">The <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property could also contain a reference to a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object which returns a single row of data from the provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="84d58252b8ae88cb97b2f9d97876ce62" id="tgt10" class="tgtSentence">If the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property is also set, then the <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property must point to some object that exists within the scope of that connection.</caps:sentence>
            <caps:sentence sentenceid="13801873bbce50814a221c4c3305dfed" id="tgt11" class="tgtSentence"> For example, in tree-structured namespaces, if the <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string.</caps:sentence>
            <caps:sentence sentenceid="e05b2f193c9c5968541c03ef39aeb0b8" id="tgt12" class="tgtSentence"> If the <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property contains a relative URL, then it is validated within the context set by the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c44259eabe70f3471fe9d7b92b780848" id="tgt13" class="tgtSentence">The <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property is read/write while the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object is closed, and is read-only while the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object is open.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt14" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt15" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt16" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
        <link xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source Property (ADO Recordset)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the data source or object represented by the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Variant</languageKeyword> value that indicates the entity represented by the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property returns the <parameterReference>Source</parameterReference> argument of the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> It can contain an absolute or relative URL string.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> An absolute URL can be used without setting the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property to directly open the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> An implicit <legacyBold>Connection</legacyBold> object is created in this case.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property can also contain a reference to an already open <legacyBold>Recordset</legacyBold>, which opens a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object representing the current row in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property could also contain a reference to a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object which returns a single row of data from the provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">If the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property is also set, then the <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property must point to some object that exists within the scope of that connection.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> For example, in tree-structured namespaces, if the <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> If the <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property contains a relative URL, then it is validated within the context set by the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">The <unmanagedCodeEntityReference>Source</unmanagedCodeEntityReference> property is read/write while the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object is closed, and is read-only while the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object is open.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src14" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4044ba15-f013-4c4c-9fe1-b4410fe9a778">Source Property (ADO Error)</link>
        <link xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source Property (ADO Recordset)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
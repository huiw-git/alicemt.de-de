---
title: "AbsolutePosition Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 79f8ee5e-fc70-46d8-8c29-ebf943c66592
caps.latest.revision: 13
caps.handback.revision: 13
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
# AbsolutePosition Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5b7cfb9c18b03749f868cfbf3df99b9c" id="tgt1" class="tgtSentence">Indicates the ordinal position of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object's current record.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="791013d6af01aa0d2d0eba339d27f616" id="tgt3" class="tgtSentence">For 32-bit code, sets or returns a <legacyBold>Long</legacyBold> value from 1 to the number of records in the <legacyBold>Recordset</legacyBold> object (<legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink>), or returns one of the <legacyLink xlink:href="e69af0a5-3405-4b72-9c6e-6b188ff746fd">PositionEnum</legacyLink> values.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7ad7faa90f3eb75fcf0cc08bba2c8e9c" id="tgt4" class="tgtSentence">For 64-bit code, use a data type that provides for storage of a 64-bit value.</caps:sentence>
            <caps:sentence sentenceid="7bb62cdcc18c06e5c0232fd0931456c9" id="tgt5" class="tgtSentence"> For example, you might use either Long or another value that is 64-bit length such as DBORDINAL.</caps:sentence>
            <caps:sentence sentenceid="794b7745e9f3e7e476330451d1348d56" id="tgt6" class="tgtSentence"> Do not use <legacyBold>PositionEnum</legacyBold> values since they are limited to 32-bit length.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="fe78499c58e59790ab59fca752481d39" id="tgt7" class="tgtSentence">In order to set the <legacyBold>AbsolutePosition</legacyBold> property, ADO requires that the OLE DB provider you are using implement the <externalLink><linkText>IRowsetLocate:IRowset</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms721190.aspx</linkUri></externalLink> interface.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="01b49347e55a2b391d2fdf8a5366dd6d" id="tgt8" class="tgtSentence">Accessing the <legacyBold>AbsolutePosition</legacyBold> property of a <legacyBold>Recordset</legacyBold> that was opened with either a forward-only or dynamic cursor raises the error <legacyBold>adErrFeatureNotAvailable</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="7a40768d4da1a057ace190a307c6f55e" id="tgt9" class="tgtSentence"> With other cursor types, the correct position will be returned as long as the OLE DB provider supports the <unmanagedCodeEntityReference>IRowsetScroll:IRowsetLocate</unmanagedCodeEntityReference> interface.</caps:sentence>
            <caps:sentence sentenceid="545ff90e4c25b21e645d903cc22fb709" id="tgt10" class="tgtSentence"> If the provider does not support the <unmanagedCodeEntityReference>IRowsetScroll</unmanagedCodeEntityReference> interface, the property is set to <legacyBold>adPosUnknown</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="ce3037d476d8444eec116c18958da108" id="tgt11" class="tgtSentence"> See the documentation for your provider to determine whether it supports <unmanagedCodeEntityReference>IRowsetScroll</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="374941d6a2e8c5f22c0b6a9d4d31d1bc" id="tgt12" class="tgtSentence">Use the <unmanagedCodeEntityReference>AbsolutePosition</unmanagedCodeEntityReference> property to move to a record based on its ordinal position in the <legacyBold>Recordset</legacyBold> object, or to determine the ordinal position of the current record.</caps:sentence>
            <caps:sentence sentenceid="f493d8b74249676ab7220d3ce60d4999" id="tgt13" class="tgtSentence"> The provider must support the appropriate functionality for this property to be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7259724f9aa8fa3ead5137f41fb5c187" id="tgt14" class="tgtSentence">Like the <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> property, <legacyBold>AbsolutePosition</legacyBold> is 1-based and equals 1 when the current record is the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="26742db1765456e5b9e422cd1f944038" id="tgt15" class="tgtSentence"> You can obtain the total number of records in the <legacyBold>Recordset</legacyBold> object from the <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4fd3b6c7dc481b79db094faca2f5bc8c" id="tgt16" class="tgtSentence">When you set the <legacyBold>AbsolutePosition</legacyBold> property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified.</caps:sentence>
            <caps:sentence sentenceid="38dd48b30a8656c20ede5f9dbe09596a" id="tgt17" class="tgtSentence"> The <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">CacheSize</legacyLink> property determines the size of this group.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d670f6ddbf984d9f58feb714f05e2912" id="tgt18" class="tgtSentence">You should not use the <legacyBold>AbsolutePosition</legacyBold> property as a surrogate record number.</caps:sentence>
              <caps:sentence sentenceid="fc1197fa9878f50b7559697bea304b14" id="tgt19" class="tgtSentence"> The position of a given record changes when you delete a preceding record.</caps:sentence>
              <caps:sentence sentenceid="5c732ff73310a4fa7776f6999d51ce1f" id="tgt20" class="tgtSentence"> There is also no assurance that a given record will have the same <legacyBold>AbsolutePosition</legacyBold> if the <legacyBold>Recordset</legacyBold> object is requeried or reopened.</caps:sentence>
              <caps:sentence sentenceid="bf96b1a3dcbc6beda43760c20046d993" id="tgt21" class="tgtSentence"> Bookmarks are still the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt22" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c4755799-c60a-4b5e-a01f-b85dd0e0a7f9">Visual Basic Example</link>
        <link xlink:href="48c07216-d199-4822-89f8-ce928d3d2b74">Visual C++ Example</link>
        <link xlink:href="74afb37a-92b5-4cab-be49-18fb866e4d53">Visual J++ Example</link>
        <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property</link>
        <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the ordinal position of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object's current record.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">For 32-bit code, sets or returns a <legacyBold>Long</legacyBold> value from 1 to the number of records in the <legacyBold>Recordset</legacyBold> object (<legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink>), or returns one of the <legacyLink xlink:href="e69af0a5-3405-4b72-9c6e-6b188ff746fd">PositionEnum</legacyLink> values.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">For 64-bit code, use a data type that provides for storage of a 64-bit value.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For example, you might use either Long or another value that is 64-bit length such as DBORDINAL.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Do not use <legacyBold>PositionEnum</legacyBold> values since they are limited to 32-bit length.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">In order to set the <legacyBold>AbsolutePosition</legacyBold> property, ADO requires that the OLE DB provider you are using implement the <externalLink><linkText>IRowsetLocate:IRowset</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms721190.aspx</linkUri></externalLink> interface.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">Accessing the <legacyBold>AbsolutePosition</legacyBold> property of a <legacyBold>Recordset</legacyBold> that was opened with either a forward-only or dynamic cursor raises the error <legacyBold>adErrFeatureNotAvailable</legacyBold>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> With other cursor types, the correct position will be returned as long as the OLE DB provider supports the <unmanagedCodeEntityReference>IRowsetScroll:IRowsetLocate</unmanagedCodeEntityReference> interface.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> If the provider does not support the <unmanagedCodeEntityReference>IRowsetScroll</unmanagedCodeEntityReference> interface, the property is set to <legacyBold>adPosUnknown</legacyBold>.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> See the documentation for your provider to determine whether it supports <unmanagedCodeEntityReference>IRowsetScroll</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">Use the <unmanagedCodeEntityReference>AbsolutePosition</unmanagedCodeEntityReference> property to move to a record based on its ordinal position in the <legacyBold>Recordset</legacyBold> object, or to determine the ordinal position of the current record.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> The provider must support the appropriate functionality for this property to be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">Like the <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> property, <legacyBold>AbsolutePosition</legacyBold> is 1-based and equals 1 when the current record is the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> You can obtain the total number of records in the <legacyBold>Recordset</legacyBold> object from the <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">When you set the <legacyBold>AbsolutePosition</legacyBold> property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> The <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">CacheSize</legacyLink> property determines the size of this group.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src18" class="srcSentence">You should not use the <legacyBold>AbsolutePosition</legacyBold> property as a surrogate record number.</caps:sentence>
              <caps:sentence id="src19" class="srcSentence"> The position of a given record changes when you delete a preceding record.</caps:sentence>
              <caps:sentence id="src20" class="srcSentence"> There is also no assurance that a given record will have the same <legacyBold>AbsolutePosition</legacyBold> if the <legacyBold>Recordset</legacyBold> object is requeried or reopened.</caps:sentence>
              <caps:sentence id="src21" class="srcSentence"> Bookmarks are still the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c4755799-c60a-4b5e-a01f-b85dd0e0a7f9">Visual Basic Example</link>
        <link xlink:href="48c07216-d199-4822-89f8-ce928d3d2b74">Visual C++ Example</link>
        <link xlink:href="74afb37a-92b5-4cab-be49-18fb866e4d53">Visual J++ Example</link>
        <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property</link>
        <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
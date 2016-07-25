---
title: "Provider Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 0ff70e72-0061-4ffc-90fb-e3ea23129bb2
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
# Provider Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="14f63dc17ca47cf5f1b09d18c675bcae" id="tgt1" class="tgtSentence">Indicates the name of the provider for a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="683ca426f47b50cc5ea1235b815105c7" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that indicates the provider name.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="3fac49d9b62994339978686ca5d4046a" id="tgt4" class="tgtSentence">Use the <unmanagedCodeEntityReference>Provider</unmanagedCodeEntityReference> property to set or return the name of the provider for a connection.</caps:sentence>
            <caps:sentence sentenceid="eb117131eabeb438861887daf4101270" id="tgt5" class="tgtSentence"> This property can also be set by the contents of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property or the <legacyItalic>ConnectionString</legacyItalic> argument of the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method; however, specifying a provider in more than one place while calling the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method can have unpredictable results.</caps:sentence>
            <caps:sentence sentenceid="56c38f9eb90c7528702a24905e6e185f" id="tgt6" class="tgtSentence"> If no provider is specified, the property will default to MSDASQL (<legacyLink xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</legacyLink>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="599f69fdec292552d6367cd2b427221a" id="tgt7" class="tgtSentence">The <unmanagedCodeEntityReference>Provider</unmanagedCodeEntityReference> property is read/write when the connection is closed and read-only when it is open.</caps:sentence>
            <caps:sentence sentenceid="4c06339496856daf6146c6dd95c205da" id="tgt8" class="tgtSentence"> The setting does not take effect until you either open the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object or access the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="3cbf9cd6f605490d002bb2d9221a3720" id="tgt9" class="tgtSentence"> If the setting is not valid, an error occurs.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="677e1dbe-bcf6-4028-a62c-e99b1c88bf7b">Visual Basic Example</link>
        <link xlink:href="677e1dbe-bcf6-4028-a62c-e99b1c88bf7b">Visual C++ Example</link>
        <link xlink:href="fdc26576-37d0-4fa1-9afa-75d0e7133675">Visual J++ Example</link>
        <link xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the name of the provider for a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that indicates the provider name.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <unmanagedCodeEntityReference>Provider</unmanagedCodeEntityReference> property to set or return the name of the provider for a connection.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This property can also be set by the contents of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property or the <legacyItalic>ConnectionString</legacyItalic> argument of the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method; however, specifying a provider in more than one place while calling the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method can have unpredictable results.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> If no provider is specified, the property will default to MSDASQL (<legacyLink xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</legacyLink>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <unmanagedCodeEntityReference>Provider</unmanagedCodeEntityReference> property is read/write when the connection is closed and read-only when it is open.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The setting does not take effect until you either open the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object or access the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If the setting is not valid, an error occurs.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="677e1dbe-bcf6-4028-a62c-e99b1c88bf7b">Visual Basic Example</link>
        <link xlink:href="677e1dbe-bcf6-4028-a62c-e99b1c88bf7b">Visual C++ Example</link>
        <link xlink:href="fdc26576-37d0-4fa1-9afa-75d0e7133675">Visual J++ Example</link>
        <link xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
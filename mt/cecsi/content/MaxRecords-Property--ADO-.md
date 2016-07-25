---
title: "MaxRecords Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 20c76571-8c9a-482c-a99e-726ab1d93f8b
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
# MaxRecords Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ce1cf7c047bea737fe173b5a28aac1d5" id="tgt1" class="tgtSentence">Indicates the maximum number of records to return to a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> from a query.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9183ae6f855308fb6a3a0a0b9ad8c46c" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that indicates the maximum number of records to return.</caps:sentence>
            <caps:sentence sentenceid="aab77863405cc7239e390ab49088a1b7" id="tgt4" class="tgtSentence"> Default is zero (<legacyBold>0</legacyBold>), which means no limit.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="a37dd61f74cf2aec7780ad014865064f" id="tgt5" class="tgtSentence">Use the <unmanagedCodeEntityReference>MaxRecords</unmanagedCodeEntityReference> property to limit the number of records that the provider returns from the data source.</caps:sentence>
            <caps:sentence sentenceid="47b937ee9ab9a962af470c3f475030d7" id="tgt6" class="tgtSentence"> The default setting of this property is zero, which means the provider returns all requested records.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4e468582bb659bb743f1b6b545778f9b" id="tgt7" class="tgtSentence">The <unmanagedCodeEntityReference>MaxRecords</unmanagedCodeEntityReference> property is read/write when the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is closed and read-only when it is open.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="630a3be4-7a87-41cf-997e-8bb50d89db1e">Visual Basic Example</link>
        <link xlink:href="af6b399b-e546-4de5-9cd1-5a6e0ec7ddc7">Visual C++ Example</link>
        <link xlink:href="f5f12f3b-8f45-4bfa-b70e-971b758e1898">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the maximum number of records to return to a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> from a query.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that indicates the maximum number of records to return.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Default is zero (<legacyBold>0</legacyBold>), which means no limit.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <unmanagedCodeEntityReference>MaxRecords</unmanagedCodeEntityReference> property to limit the number of records that the provider returns from the data source.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The default setting of this property is zero, which means the provider returns all requested records.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <unmanagedCodeEntityReference>MaxRecords</unmanagedCodeEntityReference> property is read/write when the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is closed and read-only when it is open.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="630a3be4-7a87-41cf-997e-8bb50d89db1e">Visual Basic Example</link>
        <link xlink:href="af6b399b-e546-4de5-9cd1-5a6e0ec7ddc7">Visual C++ Example</link>
        <link xlink:href="f5f12f3b-8f45-4bfa-b70e-971b758e1898">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
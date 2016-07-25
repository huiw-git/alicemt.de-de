---
title: "Index Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 1c79e271-21ec-41a8-8163-c5e89f0001a7
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
# Index Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0f9f1addc1a76688cf30289e90569999" id="tgt1" class="tgtSentence">Indicates the name of the index currently in effect for a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c9538784391e6089687f949871f71d66" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value, which is the name of the index.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="61b9e1d7ebe725714a83a976cb3e87a5" id="tgt4" class="tgtSentence">The index named by the <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property must have previously been declared on the base table underlying the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="7055101d311b20edc4fff1c9f9f02c9f" id="tgt5" class="tgtSentence"> That is, the index must have been declared programmatically either as an ADOX <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink> object, or when the base table was created.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="28cc116feb169e59cb27313720d4b0ab" id="tgt6" class="tgtSentence">A run-time error will occur if the index cannot be set.</caps:sentence>
            <caps:sentence sentenceid="47a3108cb33382635a882c8eff342d7b" id="tgt7" class="tgtSentence"> The <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property cannot be set under the following conditions:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="10a3b9acb33dbbaea105b4c382a5b8ef" id="tgt8" class="tgtSentence">Within a <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset</legacyLink> or <legacyBold>RecordsetChangeComplete</legacyBold> event handler.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="922a174c8a2298cdb1902063ea51d56f" id="tgt9" class="tgtSentence">If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is still executing an operation (which can be determined by the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f5b2cb1897dbc43e1cf90aaf35746c75" id="tgt10" class="tgtSentence">If a filter has been set on the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> with the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="8033696adf0677aae0ec841fcdc6c7b0" id="tgt11" class="tgtSentence">The <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property can always be set successfully if the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is closed, but the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1c165ecc246bb3d1c7a5ebd594116157" id="tgt12" class="tgtSentence">If the index can be set, the current row position may change.</caps:sentence>
            <caps:sentence sentenceid="29135cd94d4d3daa6ec1df97bdc9e221" id="tgt13" class="tgtSentence"> This will cause an update to the <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink> property, and will fire the <legacyBold>WillChangeRecordset</legacyBold>, <legacyBold>RecordsetChangeComplete</legacyBold>, <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove</legacyLink>, and <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">MoveComplete</legacyLink> events.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="11534444a14b74a270c187c49772cb23" id="tgt14" class="tgtSentence">If the index can be set and the <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType</legacyLink> property is <legacyBold>adLockPessimistic</legacyBold> or <legacyBold>adLockOptimistic</legacyBold>, then an implicit <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> operation is performed.</caps:sentence>
            <caps:sentence sentenceid="6d83dc82372ba8a1fefcc47da059f2ab" id="tgt15" class="tgtSentence"> This releases the current and affected groups.</caps:sentence>
            <caps:sentence sentenceid="a4e52eb92fa3d80d33cd3bc2795f3044" id="tgt16" class="tgtSentence"> Any existing filter is released, and the current row position is changed to the first row of the reordered <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0738ce02c4c2e76a6c9e8bdbb7fe8f26" id="tgt17" class="tgtSentence">The <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property is used in conjunction with the <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="653bfa35971aaa0071f949abd2171b60" id="tgt18" class="tgtSentence"> If the underlying provider does not support the <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property, and thus the <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference> method, consider using the <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find</legacyLink> method instead.</caps:sentence>
            <caps:sentence sentenceid="3b3087d5c0570675fb30b957cb691bc4" id="tgt19" class="tgtSentence"> Determine whether the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports indexes with the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink><legacyBold>(adIndex)</legacyBold> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b5f48c8c40719507cdd008194d6d9a49" id="tgt20" class="tgtSentence">The built-in <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property is not related to the dynamic <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> property, although they both deal with indexes.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt21" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="337c9eda-9ddf-49ac-94d3-b33114ba6224">Visual Basic Example</link>
        <link xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index Object</link>
        <link xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the name of the index currently in effect for a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value, which is the name of the index.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The index named by the <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property must have previously been declared on the base table underlying the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> That is, the index must have been declared programmatically either as an ADOX <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink> object, or when the base table was created.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">A run-time error will occur if the index cannot be set.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property cannot be set under the following conditions:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Within a <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset</legacyLink> or <legacyBold>RecordsetChangeComplete</legacyBold> event handler.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is still executing an operation (which can be determined by the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">If a filter has been set on the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> with the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src11" class="srcSentence">The <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property can always be set successfully if the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is closed, but the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">If the index can be set, the current row position may change.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> This will cause an update to the <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink> property, and will fire the <legacyBold>WillChangeRecordset</legacyBold>, <legacyBold>RecordsetChangeComplete</legacyBold>, <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove</legacyLink>, and <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">MoveComplete</legacyLink> events.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">If the index can be set and the <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType</legacyLink> property is <legacyBold>adLockPessimistic</legacyBold> or <legacyBold>adLockOptimistic</legacyBold>, then an implicit <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> operation is performed.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> This releases the current and affected groups.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Any existing filter is released, and the current row position is changed to the first row of the reordered <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">The <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property is used in conjunction with the <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek</legacyLink> method.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> If the underlying provider does not support the <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property, and thus the <unmanagedCodeEntityReference>Seek</unmanagedCodeEntityReference> method, consider using the <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find</legacyLink> method instead.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> Determine whether the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports indexes with the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink><legacyBold>(adIndex)</legacyBold> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">The built-in <unmanagedCodeEntityReference>Index</unmanagedCodeEntityReference> property is not related to the dynamic <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> property, although they both deal with indexes.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="337c9eda-9ddf-49ac-94d3-b33114ba6224">Visual Basic Example</link>
        <link xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index Object</link>
        <link xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
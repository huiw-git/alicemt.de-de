---
title: "Field Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b10a72fc-3c4b-4186-a70b-993dc9f7a092
caps.latest.revision: 8
caps.handback.revision: 8
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
# Field Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d1cda4d581ef6976217bd90991d964f8" id="tgt1" class="tgtSentence">Represents a column of data with a common data type.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="aa467645a2f388375a65368ef7532e3f" id="tgt2" class="tgtSentence">Each <legacyBold>Field</legacyBold> object corresponds to a column in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="6636fb87fd9073780f610b83ab5a9a78" id="tgt3" class="tgtSentence"> You use the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property of <legacyBold>Field</legacyBold> objects to set or return data for the current record.</caps:sentence>
            <caps:sentence sentenceid="cea30ca340c7dbfaa14105c4c8348231" id="tgt4" class="tgtSentence"> Depending on the functionality the provider exposes, some collections, methods, or properties of a <legacyBold>Field</legacyBold> object may not be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6567229310ed5822ad7034cfc14ada12" id="tgt5" class="tgtSentence">With the collections, methods, and properties of a <legacyBold>Field</legacyBold> object, you can do the following:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="df0f8208409cefb49501a8f4bc4382f5" id="tgt6" class="tgtSentence">Return the name of a field with the <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="33b57b6b7c7645c3786c6ea2c4a0104f" id="tgt7" class="tgtSentence">View or change the data in the field with the <legacyBold>Value</legacyBold> property.</caps:sentence>
                <caps:sentence sentenceid="53836c8fc854072ac0d39c0be12fba67" id="tgt8" class="tgtSentence">
                  <legacyBold>Value</legacyBold> is the default property of the <legacyBold>Field</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c05a428f71e21b1a468863272a631a56" id="tgt9" class="tgtSentence">Return the basic characteristics of a field with the <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink>, <legacyLink xlink:href="1fa38e78-6b5b-414d-ba0a-3dd26b29b766">Precision</legacyLink>, and <legacyLink xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="84f85ccbf32873bd4ad4193dcb31aa14" id="tgt10" class="tgtSentence">Return the declared size of a field with the <legacyLink xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5dca4bc08cb0124b16de49ca8b48ffbf" id="tgt11" class="tgtSentence">Return the actual size of the data in a given field with the <legacyLink xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="af5b5561b873105f152c32f150e0fbfb" id="tgt12" class="tgtSentence">Determine what types of functionality are supported for a given field with the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property and <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ef361570a9a9906c2cf53c9d1cd9f800" id="tgt13" class="tgtSentence">Manipulate the values of fields containing long binary or long character data with the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk</legacyLink> and <legacyLink xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="539d52b494b145962d8ce10c725e2c73" id="tgt14" class="tgtSentence">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the <legacyLink xlink:href="6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac">OriginalValue</legacyLink> and <legacyLink xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="9db09dbcb9fc343902ccaddaeb6c6312" id="tgt15" class="tgtSentence">All of the metadata properties (<legacyBold>Name</legacyBold>, <legacyBold>Type</legacyBold>, <legacyBold>DefinedSize</legacyBold>, <legacyBold>Precision</legacyBold>, and <legacyBold>NumericScale</legacyBold>) are available before opening the <legacyBold>Field</legacyBold> object's <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="a410665b89e30e2e8570de2f2ee34111" id="tgt16" class="tgtSentence"> Setting them at that time is useful for dynamically constructing forms.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt17" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="1e0fc395-14f3-499a-9309-701e9905729f">
                  <caps:sentence sentenceid="879cf2217d19fa7c2b1d5cdd966b0be1" id="tgt18" class="tgtSentence">Field Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a column of data with a common data type.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Each <legacyBold>Field</legacyBold> object corresponds to a column in the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> You use the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property of <legacyBold>Field</legacyBold> objects to set or return data for the current record.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Depending on the functionality the provider exposes, some collections, methods, or properties of a <legacyBold>Field</legacyBold> object may not be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">With the collections, methods, and properties of a <legacyBold>Field</legacyBold> object, you can do the following:

</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Return the name of a field with the <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">View or change the data in the field with the <legacyBold>Value</legacyBold> property.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence">
                  <legacyBold>Value</legacyBold> is the default property of the <legacyBold>Field</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Return the basic characteristics of a field with the <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink>, <legacyLink xlink:href="1fa38e78-6b5b-414d-ba0a-3dd26b29b766">Precision</legacyLink>, and <legacyLink xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Return the declared size of a field with the <legacyLink xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Return the actual size of the data in a given field with the <legacyLink xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Determine what types of functionality are supported for a given field with the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property and <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Manipulate the values of fields containing long binary or long character data with the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk</legacyLink> and <legacyLink xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the <legacyLink xlink:href="6e33c6ec-14d9-4b1d-ba9b-cb99862e7bac">OriginalValue</legacyLink> and <legacyLink xlink:href="00a0c8b8-8b63-433f-95b8-020ab05874a0">UnderlyingValue</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src15" class="srcSentence">All of the metadata properties (<legacyBold>Name</legacyBold>, <legacyBold>Type</legacyBold>, <legacyBold>DefinedSize</legacyBold>, <legacyBold>Precision</legacyBold>, and <legacyBold>NumericScale</legacyBold>) are available before opening the <legacyBold>Field</legacyBold> object's <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Setting them at that time is useful for dynamically constructing forms.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="1e0fc395-14f3-499a-9309-701e9905729f">
                  <caps:sentence id="src18" class="srcSentence">Field Object Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
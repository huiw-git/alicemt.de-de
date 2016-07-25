---
title: "State Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 0b993bac-2653-40b1-bcbb-5b57b6aae2bf
caps.latest.revision: 7
caps.handback.revision: 7
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
# State Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="21732cd5a6837465397a8132a5bcd9ac" id="tgt1" class="tgtSentence">Indicates for all applicable objects whether the state of the object is open or closed.</caps:sentence>
          <caps:sentence sentenceid="4166ec000b25cd7ba14b403bae71649a" id="tgt2" class="tgtSentence"> If the object is executing an asynchronous method, indicates whether the current state of the object is connecting, executing, or retrieving.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt3" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7c40f406a5029b02b1d11460d690766e" id="tgt4" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> value that can be an <legacyLink xlink:href="32746558-097b-4749-989e-519aadf7e3f4">ObjectStateEnum</legacyLink> value.</caps:sentence>
            <caps:sentence sentenceid="c9a32fc1d0bfac17b0531df7d4eb0a4e" id="tgt5" class="tgtSentence"> The default value is <legacyBold>adStateClosed</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="c6ebdad395ad2f2a620b53c7b99fa45b" id="tgt6" class="tgtSentence">You can use the <unmanagedCodeEntityReference>State</unmanagedCodeEntityReference> property to determine the current state of a given object at any time.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1783a69e55f8b89222e812850e9df303" id="tgt7" class="tgtSentence">The object's <unmanagedCodeEntityReference>State</unmanagedCodeEntityReference> property can have a combination of values.</caps:sentence>
            <caps:sentence sentenceid="c6ca1e440a8d3a2b25fcd5a62b37a163" id="tgt8" class="tgtSentence"> For example, if a statement is executing, this property will have a combined value of <legacyBold>adStateOpen</legacyBold> and <legacyBold>adStateExecuting</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5ae66adcb3ef4b67d5e6014c407426da" id="tgt9" class="tgtSentence">The <unmanagedCodeEntityReference>State</unmanagedCodeEntityReference> property is read-only.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4de7336a-b5ea-43f1-b750-5fa302b5b756">Visual Basic Example</link>
        <link xlink:href="c6bd2609-4c49-462f-a1aa-7bee0f615adb">Visual C++ Example</link>
        <link xlink:href="4c1e61ed-6569-44a9-b0c8-75b820a64cb6">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates for all applicable objects whether the state of the object is open or closed.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> If the object is executing an asynchronous method, indicates whether the current state of the object is connecting, executing, or retrieving.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> value that can be an <legacyLink xlink:href="32746558-097b-4749-989e-519aadf7e3f4">ObjectStateEnum</legacyLink> value.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> The default value is <legacyBold>adStateClosed</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">You can use the <unmanagedCodeEntityReference>State</unmanagedCodeEntityReference> property to determine the current state of a given object at any time.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The object's <unmanagedCodeEntityReference>State</unmanagedCodeEntityReference> property can have a combination of values.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> For example, if a statement is executing, this property will have a combined value of <legacyBold>adStateOpen</legacyBold> and <legacyBold>adStateExecuting</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <unmanagedCodeEntityReference>State</unmanagedCodeEntityReference> property is read-only.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4de7336a-b5ea-43f1-b750-5fa302b5b756">Visual Basic Example</link>
        <link xlink:href="c6bd2609-4c49-462f-a1aa-7bee0f615adb">Visual C++ Example</link>
        <link xlink:href="4c1e61ed-6569-44a9-b0c8-75b820a64cb6">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
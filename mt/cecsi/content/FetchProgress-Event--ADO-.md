---
title: "FetchProgress Event (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 301716fd-81fc-40eb-8a04-221ef7ab410e
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
# FetchProgress Event (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1e8673400c397c9277c926974de17881" id="tgt1" class="tgtSentence">The <unmanagedCodeEntityReference>FetchProgress</unmanagedCodeEntityReference><legacyBold> </legacyBold>event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>FetchProgress</legacyBold>
          <parameterReference>Progress</parameterReference>, <parameterReference>MaxProgress</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>Progress </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a7fe4b6f5acfdbf5b463c335d8077a59" id="tgt2" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value indicating the number of records that have currently been retrieved by the fetch operation.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>MaxProgress </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a9f7058d79bb11b7f1bd50cf0e0eddc8" id="tgt3" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value indicating the maximum number of records expected to be retrieved.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>adStatus </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5c78d6db71781f81b24720b7aadbc6c2" id="tgt4" class="tgtSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>pRecordset </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="310e3cb2fcbd832a4b3be5ab508202f0" id="tgt5" class="tgtSentence">A <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object that is the object for which the records are being retrieved.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="101144cd10a897fa028f054fb0599639" id="tgt6" class="tgtSentence">When using <unmanagedCodeEntityReference>FetchProgress</unmanagedCodeEntityReference> with a child <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, be aware that the <parameterReference>Progress</parameterReference> and <parameterReference>MaxProgress</parameterReference> parameter values are derived from the underlying <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Cursor Service</legacyLink> rowset.</caps:sentence>
            <caps:sentence sentenceid="ca97efd0dcffa95660b7aba19fc72029" id="tgt7" class="tgtSentence"> The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="52ae256509e7c95b7450959e7c803a7e" id="tgt8" class="tgtSentence">To use <unmanagedCodeEntityReference>FetchProgress</unmanagedCodeEntityReference> with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <unmanagedCodeEntityReference>FetchProgress</unmanagedCodeEntityReference><legacyBold> </legacyBold>event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>FetchProgress</legacyBold>
          <parameterReference>Progress</parameterReference>, <parameterReference>MaxProgress</parameterReference>, <parameterReference>adStatus</parameterReference>, <parameterReference>pRecordset</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>Progress </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src2" class="srcSentence">A <languageKeyword>Long</languageKeyword> value indicating the number of records that have currently been retrieved by the fetch operation.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>MaxProgress </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>Long</languageKeyword> value indicating the maximum number of records expected to be retrieved.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>adStatus </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">An <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink> status value.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>pRecordset </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">A <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object that is the object for which the records are being retrieved.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">When using <unmanagedCodeEntityReference>FetchProgress</unmanagedCodeEntityReference> with a child <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, be aware that the <parameterReference>Progress</parameterReference> and <parameterReference>MaxProgress</parameterReference> parameter values are derived from the underlying <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Cursor Service</legacyLink> rowset.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src8" class="srcSentence">To use <unmanagedCodeEntityReference>FetchProgress</unmanagedCodeEntityReference> with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="29530153-b963-4a7c-8665-2335f1d604a8">Visual C++ Example</link>
        <link xlink:href="b34f4472-5e04-4a2c-ab64-38d6eca31a69">ADO Event Handler Summary</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
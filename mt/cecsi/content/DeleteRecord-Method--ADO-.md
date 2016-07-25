---
title: "DeleteRecord Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 2726498c-dbd8-4266-983b-ae7d62c39142
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
# DeleteRecord Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f3f54bc621ea61ddd5410ae74a8f86b0" id="tgt1" class="tgtSentence">Deletes an entity represented by a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Record</parameterReference>
          <legacyBold>.DeleteRecord </legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Async</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="b86002c905ed82eb6c9ab27bfdb86afd" id="tgt2" class="tgtSentence"> <legacyItalic>Source</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="2d7df892191d60679f07ae80b7af88de" id="tgt4" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that contains a URL identifying the entity (for example, the file or directory) to be deleted.</caps:sentence>
                <caps:sentence sentenceid="3e41f347f82dcf1ef5371b93a401bf90" id="tgt5" class="tgtSentence"> If <legacyItalic>Source</legacyItalic> is omitted or specifies an empty string, the entity represented by the current <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> is deleted.</caps:sentence>
                <caps:sentence sentenceid="f65e9b5e053301cb263552667c3ab2b7" id="tgt6" class="tgtSentence"> If the Record is a collection record (<legacyLink xlink:href="790e46a2-13d2-451e-a8be-130bd9a206a4">RecordType</legacyLink> of <legacyBold>adCollectionRecord</legacyBold>, such as a directory) all children (for example, subdirectories) will also be deleted.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="4f96059e85234f10011f72092bee6b67" id="tgt7" class="tgtSentence"> <legacyItalic>Async</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="2a52a1db1aba34b79ea25b28b2483568" id="tgt9" class="tgtSentence"> A <languageKeyword>Boolean</languageKeyword> value that, when <languageKeyword>True</languageKeyword>, specifies that the delete operation is asychronous.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="0c8169ec6208aa68b4728f9076f4befe" id="tgt10" class="tgtSentence">Operations on the object represented by this <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> may fail after this method completes.</caps:sentence>
            <caps:sentence sentenceid="203ba33b226c266afc2c6e04fe5a458c" id="tgt11" class="tgtSentence"> After calling <unmanagedCodeEntityReference>DeleteRecord</unmanagedCodeEntityReference>, the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> should be closed because the behavior of the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> may become unpredictable depending upon when the provider updates the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> with the data source.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="02f4b17bf8de84f9ccb372a1181d4a90" id="tgt12" class="tgtSentence">If this <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> was obtained from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, then the results of this operation will not be reflected immediately in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="49496e3bd9d6e9c75ee49697ae61b465" id="tgt13" class="tgtSentence"> Refresh the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> by closing and re-opening it, or by executing the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> method, the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method, or the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
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
        <link xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">Delete Method (ADO Fields Collection)</link>
        <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Deletes an entity represented by a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Record</parameterReference>
          <legacyBold>.DeleteRecord </legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Async</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Source</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that contains a URL identifying the entity (for example, the file or directory) to be deleted.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> If <legacyItalic>Source</legacyItalic> is omitted or specifies an empty string, the entity represented by the current <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> is deleted.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> If the Record is a collection record (<legacyLink xlink:href="790e46a2-13d2-451e-a8be-130bd9a206a4">RecordType</legacyLink> of <legacyBold>adCollectionRecord</legacyBold>, such as a directory) all children (for example, subdirectories) will also be deleted.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>Async</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> A <languageKeyword>Boolean</languageKeyword> value that, when <languageKeyword>True</languageKeyword>, specifies that the delete operation is asychronous.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">Operations on the object represented by this <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> may fail after this method completes.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> After calling <unmanagedCodeEntityReference>DeleteRecord</unmanagedCodeEntityReference>, the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> should be closed because the behavior of the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> may become unpredictable depending upon when the provider updates the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> with the data source.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">If this <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> was obtained from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, then the results of this operation will not be reflected immediately in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Refresh the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> by closing and re-opening it, or by executing the <legacyBold>Recordset</legacyBold> <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> method, the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method, or the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
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
        <link xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">Delete Method (ADO Fields Collection)</link>
        <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
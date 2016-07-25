---
title: "CopyRecord Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b9bcf272-3c74-479f-95dd-0229a32e98fc
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
# CopyRecord Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4114e827e73e3614556d1843afe476f0" id="tgt1" class="tgtSentence">Copies an entity represented by a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">record</legacyLink> to another location.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Record</parameterReference>
          <legacyBold>.CopyRecord (</legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Destination</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>UserName</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Password</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Options</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Async</parameterReference>
          <legacyBold>)</legacyBold>
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
                <caps:sentence sentenceid="d1b67e1c33a0e446484840407f3dff29" id="tgt4" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that contains a URL specifying the entity to be copied (for example, a file or directory).</caps:sentence>
                <caps:sentence sentenceid="f9c255a438b81866ba63eb68fb943b82" id="tgt5" class="tgtSentence"> If <legacyItalic>Source </legacyItalic>is omitted or specifies an empty string, the file or directory represented by the current <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> will be copied.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="004d43c096763731c9a280248b72895c" id="tgt6" class="tgtSentence"> <legacyItalic>Destination</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt7" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="132cfa9200bbb01a44fcbfe650ca7ecd" id="tgt8" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that contains a URL specifying the location where <legacyItalic>Source</legacyItalic> will be copied.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="230b2555855f31ab54ada86334bb7da2" id="tgt9" class="tgtSentence"> <legacyItalic>UserName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt10" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="565a808fb9adf2dde14955a8e8ebd180" id="tgt11" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that contains the user ID that, if needed, authorizes access to <legacyItalic>Destination</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d83fe9057df78601fffb657095e0114f" id="tgt12" class="tgtSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt13" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="5c5ccaa1e9af1e2c04a108280f1511fe" id="tgt14" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value that contains the password that, if needed, verifies <legacyItalic>UserName</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt15" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt16" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="87c8de4495e7af380bdced5ba1c188e0" id="tgt17" class="tgtSentence"> A <legacyLink xlink:href="2fa4eec5-d50b-4fd3-8ae7-40af441ba12b">CopyRecordOptionsEnum</legacyLink> value that has a default value of <legacyBold>adCopyUnspecified</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="563bbfa209a2d8fcf4551a667bec9a36" id="tgt18" class="tgtSentence"> Specifies the behavior of this method.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="4f96059e85234f10011f72092bee6b67" id="tgt19" class="tgtSentence"> <legacyItalic>Async</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt20" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="1d9f649cfc6c56c4dd90c0ce9aedfece" id="tgt21" class="tgtSentence"> A <languageKeyword>Boolean</languageKeyword> value that, when <languageKeyword>True</languageKeyword>, specifies that this operation should be asynchronous.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="1f6f1beee2c905ee74c5463adc2da112" id="tgt22" class="tgtSentence">A <legacyBold>String </legacyBold>value that typically returns the value of <legacyItalic>Destination</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="ba90443fac67a179ba91323ae8b4fb20" id="tgt23" class="tgtSentence"> However, the exact value returned is provider-dependent.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="dd1a5589e8502518b3f410088c740dbf" id="tgt24" class="tgtSentence">The values of <legacyItalic>Source</legacyItalic> and <legacyItalic>Destination</legacyItalic> must not be identical; otherwise, a run-time error occurs.</caps:sentence>
            <caps:sentence sentenceid="48c31431320f56646c874f1be42e393c" id="tgt25" class="tgtSentence"> At least one of the server, path, or resource names must differ.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3ec4fde6a20b9db7312680273d64d9eb" id="tgt26" class="tgtSentence">All children (for example, subdirectories) of <legacyItalic>Source</legacyItalic> are copied recursively, unless <legacyBold>adCopyNonRecursive</legacyBold> is specified.</caps:sentence>
            <caps:sentence sentenceid="e110b5e75ea82747c5e1d503e37a7546" id="tgt27" class="tgtSentence"> In a recursive operation, <legacyItalic>Destination</legacyItalic> must not be a subdirectory of <legacyItalic>Source</legacyItalic>; otherwise, the operation will not complete.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ebee9054d834da8f930860aa5579bddd" id="tgt28" class="tgtSentence">This method fails if <legacyItalic>Destination</legacyItalic> identifies an existing entity (for example, a file or directory), unless <legacyBold>adCopyOverWrite</legacyBold> is specified.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="800cfb8a418c08f0244b47bce36e90a6" id="tgt29" class="tgtSentence">Use the <legacyBold>adCopyOverWrite</legacyBold> option judiciously.</caps:sentence>
              <caps:sentence sentenceid="28b21102db5d30a9ddfd9f2bee47da40" id="tgt30" class="tgtSentence"> For example, specifying this option when copying a file to a directory will <legacyItalic>delete</legacyItalic> the directory and replace it with the file.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt31" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt32" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt33" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">record</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Copies an entity represented by a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">record</legacyLink> to another location.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Record</parameterReference>
          <legacyBold>.CopyRecord (</legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Destination</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>UserName</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Password</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Options</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Async</parameterReference>
          <legacyBold>)</legacyBold>
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
                <caps:sentence id="src4" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that contains a URL specifying the entity to be copied (for example, a file or directory).</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> If <legacyItalic>Source </legacyItalic>is omitted or specifies an empty string, the file or directory represented by the current <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> will be copied.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>Destination</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that contains a URL specifying the location where <legacyItalic>Source</legacyItalic> will be copied.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>UserName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that contains the user ID that, if needed, authorizes access to <legacyItalic>Destination</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> A <languageKeyword>String</languageKeyword> value that contains the password that, if needed, verifies <legacyItalic>UserName</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src15" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src16" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> A <legacyLink xlink:href="2fa4eec5-d50b-4fd3-8ae7-40af441ba12b">CopyRecordOptionsEnum</legacyLink> value that has a default value of <legacyBold>adCopyUnspecified</legacyBold>.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> Specifies the behavior of this method.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src19" class="srcSentence"> <legacyItalic>Async</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src20" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> A <languageKeyword>Boolean</languageKeyword> value that, when <languageKeyword>True</languageKeyword>, specifies that this operation should be asynchronous.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src22" class="srcSentence">A <legacyBold>String </legacyBold>value that typically returns the value of <legacyItalic>Destination</legacyItalic>.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> However, the exact value returned is provider-dependent.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src24" class="srcSentence">The values of <legacyItalic>Source</legacyItalic> and <legacyItalic>Destination</legacyItalic> must not be identical; otherwise, a run-time error occurs.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> At least one of the server, path, or resource names must differ.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src26" class="srcSentence">All children (for example, subdirectories) of <legacyItalic>Source</legacyItalic> are copied recursively, unless <legacyBold>adCopyNonRecursive</legacyBold> is specified.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> In a recursive operation, <legacyItalic>Destination</legacyItalic> must not be a subdirectory of <legacyItalic>Source</legacyItalic>; otherwise, the operation will not complete.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">This method fails if <legacyItalic>Destination</legacyItalic> identifies an existing entity (for example, a file or directory), unless <legacyBold>adCopyOverWrite</legacyBold> is specified.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src29" class="srcSentence">Use the <legacyBold>adCopyOverWrite</legacyBold> option judiciously.</caps:sentence>
              <caps:sentence id="src30" class="srcSentence"> For example, specifying this option when copying a file to a directory will <legacyItalic>delete</legacyItalic> the directory and replace it with the file.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src31" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src32" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src33" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">record</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
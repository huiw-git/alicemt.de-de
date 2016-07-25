---
title: "Open Method (ADO Stream)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d26f48fb-904e-4932-a245-3b4332ca1600
caps.latest.revision: 14
caps.handback.revision: 14
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
# Open Method (ADO Stream)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="00bed337d03f4f0a0ec85ee4a865b511" id="tgt1" class="tgtSentence">Opens a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object to manipulate streams of binary or text data.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.Open</legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Mode</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>OpenOptions</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>UserName</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Password</parameterReference>
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
                <caps:sentence sentenceid="362719f22002805e213f9582c7a1bb6c" id="tgt4" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> value that specifies the source of data for the <legacyBold>Stream</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="f93c5d536886d6b32c36112012498dbc" id="tgt5" class="tgtSentence">
                  <legacyItalic>Source</legacyItalic> may contain an absolute URL string that points to an existing node in a well-known tree structure, such as an e-mail or file system.</caps:sentence>
                <caps:sentence sentenceid="dae703d77c26febc0762183f52598013" id="tgt6" class="tgtSentence"> A URL should be specified by using the URL keyword ("URL=<legacyItalic>scheme</legacyItalic>://<legacyItalic>server</legacyItalic>/<legacyItalic>folder</legacyItalic>").</caps:sentence>
                <caps:sentence sentenceid="86d6ed4e7d3dd83608814cc8bfe15a26" id="tgt7" class="tgtSentence"> Alternatively, <legacyItalic>Source</legacyItalic> may contain a reference to an already open <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, which opens the default stream associated with the <legacyBold>Record</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="2fde5059f2222cbc52662bf9c8f3ac61" id="tgt8" class="tgtSentence"> If <legacyItalic>Source</legacyItalic> is not specified, a <legacyBold>Stream</legacyBold> is instantiated and opened, associated with no underlying source by default.</caps:sentence>
                <caps:sentence sentenceid="91e4cb77d9cb636a471055e3afa0de19" id="tgt9" class="tgtSentence"> For more information about URL schemes and their associated providers, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a34287bbfa1f581118264867ed0b3373" id="tgt10" class="tgtSentence"> <legacyItalic>Mode</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt11" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="fddc1ecc32850f2b1293278f7fa3f717" id="tgt12" class="tgtSentence"> A <legacyLink xlink:href="3792c294-5161-4538-a908-22a5fc50b85f">ConnectModeEnum</legacyLink> value that specifies the access mode for the resultant <legacyBold>Stream</legacyBold> (for example, read/write or read-only).</caps:sentence>
                <caps:sentence sentenceid="85e1927a94753c75b24ec89ac05ac5b9" id="tgt13" class="tgtSentence"> Default value is <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="caa70fcc052f2b731d4d8d1a4266e0cc" id="tgt14" class="tgtSentence"> See the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property for more information about access modes.</caps:sentence>
                <caps:sentence sentenceid="3c1e3e63d4ddae19707e4d53aae267d5" id="tgt15" class="tgtSentence"> If <legacyItalic>Mode</legacyItalic> is not specified, it is inherited by the source object.</caps:sentence>
                <caps:sentence sentenceid="3ca5130abe548c084f88b64918c594a8" id="tgt16" class="tgtSentence"> For example, if the source <legacyBold>Record</legacyBold> is opened in read-only mode, the <legacyBold>Stream</legacyBold> will also be opened in read-only mode by default.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e18975ffce9e642d06613d204e11bd03" id="tgt17" class="tgtSentence"> <legacyItalic>OpenOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt18" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="a9eb5451d194164e4a2aacbdaac79073" id="tgt19" class="tgtSentence"> A <legacyLink xlink:href="85b6c57f-47ed-46ba-bd92-07882ae9e9d2">StreamOpenOptionsEnum</legacyLink> value.</caps:sentence>
                <caps:sentence sentenceid="ec8c2299a766a359b5c57f999c8de8c7" id="tgt20" class="tgtSentence"> Default value is <legacyBold>adOpenStreamUnspecified</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="230b2555855f31ab54ada86334bb7da2" id="tgt21" class="tgtSentence"> <legacyItalic>UserName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt22" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="5040e2efc27ff6b721c03b5340c85219" id="tgt23" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains the user identification that, if it is needed, accesses the <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d83fe9057df78601fffb657095e0114f" id="tgt24" class="tgtSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt25" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="2a42da9a78e4f090e4192475582a3b0a" id="tgt26" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains the password that, if it is needed, accesses the <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1e5114031b08bccec7e71a1c4eada3ba" id="tgt27" class="tgtSentence">When a <legacyBold>Record</legacyBold> object is passed in as the source parameter, the <legacyItalic>UserID</legacyItalic> and <legacyItalic>Password</legacyItalic> parameters are not used because access to the <legacyBold>Record</legacyBold> object is already available.</caps:sentence>
            <caps:sentence sentenceid="c588e297092d912979b060450dc88250" id="tgt28" class="tgtSentence"> Similarly, the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> of the <legacyBold>Record</legacyBold> object is transferred to the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="27b461959fdf038980ddef9a82775b40" id="tgt29" class="tgtSentence"> When <legacyItalic>Source</legacyItalic> is not specified, the <legacyBold>Stream</legacyBold> opened contains no data and has a <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> of zero (0).</caps:sentence>
            <caps:sentence sentenceid="0fa729b30b8357a4866daf15aba33d9a" id="tgt30" class="tgtSentence"> To avoid losing any data that is written to this <legacyBold>Stream</legacyBold> when the <legacyBold>Stream</legacyBold> is closed, save the <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="b4aa5714-916b-48b8-8b09-cc2708379602">CopyTo</legacyLink> or <legacyLink xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile</legacyLink> methods, or save it to another memory location.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="787774c65a08243a8afa7ff84532ef85" id="tgt31" class="tgtSentence">An <legacyItalic>OpenOptions</legacyItalic> value of <legacyBold>adOpenStreamFromRecord</legacyBold> identifies the contents of the <legacyItalic>Source</legacyItalic> parameter to be an already open <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="a720d1e8511672dc59e1821c50be0fa2" id="tgt32" class="tgtSentence"> The default behavior is to treat <legacyItalic>Source</legacyItalic> as a URL that points directly to a node in a tree structure, such as a file.</caps:sentence>
            <caps:sentence sentenceid="4734ad16b958fb4bd6f27151ce5614cb" id="tgt33" class="tgtSentence"> The default stream associated with that node is opened.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0f5f62044e573a728644168e8249dde9" id="tgt34" class="tgtSentence">While the <legacyBold>Stream</legacyBold> is not open, it is possible to read all the read-only properties of the <legacyBold>Stream</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="8b751d11380ab58c8bb13af13cfa20f3" id="tgt35" class="tgtSentence"> If a <legacyBold>Stream</legacyBold> is opened asynchronously, all subsequent operations (other than checking the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> and other read-only properties) are blocked until the <legacyBold>Open</legacyBold> operation is completed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="60fceea4d3edc44eb71aaab21dfba0a8" id="tgt36" class="tgtSentence">In addition to the options that were discussed earlier, by not specifying <legacyItalic>Source</legacyItalic>, you can create an instance of a <legacyBold>Stream</legacyBold> object in memory without associating it with an underlying source.</caps:sentence>
            <caps:sentence sentenceid="f69a5c4421b7425d6902b370102bd5dc" id="tgt37" class="tgtSentence"> You can dynamically add data to the stream by writing binary or text data to the <legacyBold>Stream</legacyBold> with <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink> or <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink>, or by loading data from a file with <legacyLink xlink:href="b18d8d38-7354-4a94-b637-6ac035faa433">LoadFromFile</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt38" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
        <link xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Opens a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object to manipulate streams of binary or text data.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.Open</legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Mode</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>OpenOptions</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>UserName</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>Password</parameterReference>
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
                <caps:sentence id="src4" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> value that specifies the source of data for the <legacyBold>Stream</legacyBold>.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence">
                  <legacyItalic>Source</legacyItalic> may contain an absolute URL string that points to an existing node in a well-known tree structure, such as an e-mail or file system.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> A URL should be specified by using the URL keyword ("URL=<legacyItalic>scheme</legacyItalic>://<legacyItalic>server</legacyItalic>/<legacyItalic>folder</legacyItalic>").</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> Alternatively, <legacyItalic>Source</legacyItalic> may contain a reference to an already open <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, which opens the default stream associated with the <legacyBold>Record</legacyBold>.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> If <legacyItalic>Source</legacyItalic> is not specified, a <legacyBold>Stream</legacyBold> is instantiated and opened, associated with no underlying source by default.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> For more information about URL schemes and their associated providers, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>Mode</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> A <legacyLink xlink:href="3792c294-5161-4538-a908-22a5fc50b85f">ConnectModeEnum</legacyLink> value that specifies the access mode for the resultant <legacyBold>Stream</legacyBold> (for example, read/write or read-only).</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> Default value is <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> See the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property for more information about access modes.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> If <legacyItalic>Mode</legacyItalic> is not specified, it is inherited by the source object.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> For example, if the source <legacyBold>Record</legacyBold> is opened in read-only mode, the <legacyBold>Stream</legacyBold> will also be opened in read-only mode by default.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src17" class="srcSentence"> <legacyItalic>OpenOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src18" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> A <legacyLink xlink:href="85b6c57f-47ed-46ba-bd92-07882ae9e9d2">StreamOpenOptionsEnum</legacyLink> value.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> Default value is <legacyBold>adOpenStreamUnspecified</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src21" class="srcSentence"> <legacyItalic>UserName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src22" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains the user identification that, if it is needed, accesses the <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src24" class="srcSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src25" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains the password that, if it is needed, accesses the <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src27" class="srcSentence">When a <legacyBold>Record</legacyBold> object is passed in as the source parameter, the <legacyItalic>UserID</legacyItalic> and <legacyItalic>Password</legacyItalic> parameters are not used because access to the <legacyBold>Record</legacyBold> object is already available.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> Similarly, the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> of the <legacyBold>Record</legacyBold> object is transferred to the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> When <legacyItalic>Source</legacyItalic> is not specified, the <legacyBold>Stream</legacyBold> opened contains no data and has a <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> of zero (0).</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> To avoid losing any data that is written to this <legacyBold>Stream</legacyBold> when the <legacyBold>Stream</legacyBold> is closed, save the <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="b4aa5714-916b-48b8-8b09-cc2708379602">CopyTo</legacyLink> or <legacyLink xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile</legacyLink> methods, or save it to another memory location.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src31" class="srcSentence">An <legacyItalic>OpenOptions</legacyItalic> value of <legacyBold>adOpenStreamFromRecord</legacyBold> identifies the contents of the <legacyItalic>Source</legacyItalic> parameter to be an already open <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> The default behavior is to treat <legacyItalic>Source</legacyItalic> as a URL that points directly to a node in a tree structure, such as a file.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> The default stream associated with that node is opened.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src34" class="srcSentence">While the <legacyBold>Stream</legacyBold> is not open, it is possible to read all the read-only properties of the <legacyBold>Stream</legacyBold>.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> If a <legacyBold>Stream</legacyBold> is opened asynchronously, all subsequent operations (other than checking the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> and other read-only properties) are blocked until the <legacyBold>Open</legacyBold> operation is completed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src36" class="srcSentence">In addition to the options that were discussed earlier, by not specifying <legacyItalic>Source</legacyItalic>, you can create an instance of a <legacyBold>Stream</legacyBold> object in memory without associating it with an underlying source.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> You can dynamically add data to the stream by writing binary or text data to the <legacyBold>Stream</legacyBold> with <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink> or <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink>, or by loading data from a file with <legacyLink xlink:href="b18d8d38-7354-4a94-b637-6ac035faa433">LoadFromFile</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src38" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
        <link xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
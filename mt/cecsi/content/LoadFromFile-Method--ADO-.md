---
title: "LoadFromFile Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b18d8d38-7354-4a94-b637-6ac035faa433
caps.latest.revision: 12
caps.handback.revision: 12
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
# LoadFromFile Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5c0bb41a6f0747b6c3322679984b9937" id="tgt1" class="tgtSentence">Loads the contents of an existing file into a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.LoadFromFile</legacyBold>
          <parameterReference>FileName</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="6d40986408932f434bbb5bdd3183deb1" id="tgt2" class="tgtSentence"> <legacyItalic>FileName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="808b37c9aed1390ceaefd208b1f6744d" id="tgt3" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that contains the name of a file to be loaded into the <legacyBold>Stream</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="c65992684723f68908fb8e7a347e93e0" id="tgt4" class="tgtSentence">
                  <legacyItalic>FileName</legacyItalic> can contain any valid path and name in UNC format.</caps:sentence>
                <caps:sentence sentenceid="9c56a7ee05142d06f131287622ed77f1" id="tgt5" class="tgtSentence"> If the specified file does not exist, a run-time error occurs.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="95da00dfdd829e00bb1f20fc3328f73c" id="tgt6" class="tgtSentence">This method can be used to load the contents of a local file into a <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="47b76c255d41a0fa1fba71d07466ff74" id="tgt7" class="tgtSentence"> This can be used to upload the contents of a local file to a server.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0763f7bc435fc974b4b9cdf41a8244ec" id="tgt8" class="tgtSentence">The <legacyBold>Stream</legacyBold> object must be already open before calling <legacyBold>LoadFromFile</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="bb0f9b3f7c0bd46d963132aa44d64611" id="tgt9" class="tgtSentence"> This method does not change the binding of the <legacyBold>Stream</legacyBold> object; it will still be bound to the object specified by the URL or <legacyBold>Record</legacyBold> with which the <legacyBold>Stream</legacyBold> was originally opened.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5a1961f846de061aa690300bea2fcf23" id="tgt10" class="tgtSentence">
              <legacyBold>LoadFromFile</legacyBold> overwrites the current contents of the <legacyBold>Stream</legacyBold> object with data read from the file.</caps:sentence>
            <caps:sentence sentenceid="48ec675ee892d506d93575f3dd673803" id="tgt11" class="tgtSentence"> Any existing bytes in the <legacyBold>Stream</legacyBold> are overwritten by the contents of the file.</caps:sentence>
            <caps:sentence sentenceid="085890031ecc5dc8bf464e165bf92c7d" id="tgt12" class="tgtSentence"> Any previously existing and remaining bytes following the <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink> created by <legacyBold>LoadFromFile</legacyBold>, are truncated.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dfb5d6c25891a05a26da8b8cc7fe50e9" id="tgt13" class="tgtSentence">After a call to <legacyBold>LoadFromFile</legacyBold>, the current position is set to the beginning of the <legacyBold>Stream</legacyBold> (<legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> is 0).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e349c01fe714d60b436c9b936ffb50e8" id="tgt14" class="tgtSentence">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt15" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
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
          <caps:sentence id="src1" class="srcSentence">Loads the contents of an existing file into a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.LoadFromFile</legacyBold>
          <parameterReference>FileName</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>FileName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>String</languageKeyword> value that contains the name of a file to be loaded into the <legacyBold>Stream</legacyBold>.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence">
                  <legacyItalic>FileName</legacyItalic> can contain any valid path and name in UNC format.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> If the specified file does not exist, a run-time error occurs.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">This method can be used to load the contents of a local file into a <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> This can be used to upload the contents of a local file to a server.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <legacyBold>Stream</legacyBold> object must be already open before calling <legacyBold>LoadFromFile</legacyBold>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> This method does not change the binding of the <legacyBold>Stream</legacyBold> object; it will still be bound to the object specified by the URL or <legacyBold>Record</legacyBold> with which the <legacyBold>Stream</legacyBold> was originally opened.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">
              <legacyBold>LoadFromFile</legacyBold> overwrites the current contents of the <legacyBold>Stream</legacyBold> object with data read from the file.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Any existing bytes in the <legacyBold>Stream</legacyBold> are overwritten by the contents of the file.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Any previously existing and remaining bytes following the <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink> created by <legacyBold>LoadFromFile</legacyBold>, are truncated.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">After a call to <legacyBold>LoadFromFile</legacyBold>, the current position is set to the beginning of the <legacyBold>Stream</legacyBold> (<legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> is 0).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
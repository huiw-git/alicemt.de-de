---
title: "SaveToFile Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8a8594f2-422b-4d2e-94f8-7fe337445900
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
# SaveToFile Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d35b4bdf296bec65e7477f1c614a3fb4" id="tgt1" class="tgtSentence">Saves the binary contents of a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> to a file.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.SaveToFile</legacyBold>
          <parameterReference>FileName</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>SaveOptions</parameterReference>
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
                <caps:sentence sentenceid="bbb5f68870a189344927cc73a308ad82" id="tgt3" class="tgtSentence">A <legacyBold>String</legacyBold> value that contains the fully-qualified name of the file to which the contents of the <legacyBold>Stream</legacyBold> will be saved.</caps:sentence>
                <caps:sentence sentenceid="8fe0d489426244004f64a32d833b7770" id="tgt4" class="tgtSentence"> You can save to any valid local location, or any location you have access to via a UNC value.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f2bffeecec1b11621059bfa42b62a608" id="tgt5" class="tgtSentence"> <legacyItalic>SaveOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="8deed0c36611845e23dbbd6900dbc138" id="tgt6" class="tgtSentence">A <legacyLink xlink:href="59339100-6e29-48d1-aea3-6873796d186b">SaveOptionsEnum</legacyLink> value that specifies whether a new file should be created by <legacyBold>SaveToFile</legacyBold>, if it does not already exist.</caps:sentence>
                <caps:sentence sentenceid="95c03afbba9073d6291cfebb11b0d678" id="tgt7" class="tgtSentence"> Default value is <legacyBold>adSaveCreateNotExists</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="45112b0380a6a8a81974237cbfa3c74f" id="tgt8" class="tgtSentence"> With these options you can specify that an error occurs if the specified file does not exist.</caps:sentence>
                <caps:sentence sentenceid="6668fbdcb3e46a65b28d6d8aa065c6c6" id="tgt9" class="tgtSentence"> You can also specify that <legacyBold>SaveToFile</legacyBold> overwrites the current contents of an existing file.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="8e4563168bf7284c1e38a6323a29c877" id="tgt10" class="tgtSentence">If you overwrite an existing file (when <legacyBold>adSaveCreateOverwrite</legacyBold> is set), <legacyBold>SaveToFile</legacyBold> truncates any bytes from the original existing file that follow the new <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e00657c7c196fe6eb669f5c75b270d17" id="tgt11" class="tgtSentence">
              <legacyBold>SaveToFile</legacyBold> may be used to copy the contents of a <legacyBold>Stream </legacyBold>object to a local file.</caps:sentence>
            <caps:sentence sentenceid="7993b1df7b5146c5fcfc07217393c215" id="tgt12" class="tgtSentence"> There is no change in the contents or properties of the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="e8f8c44fe852dedcdeaa4e75e0a37283" id="tgt13" class="tgtSentence"> The <legacyBold>Stream</legacyBold> object must be open before calling <legacyBold>SaveToFile</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="df49ea919ee35a87ab47d0794cafc523" id="tgt14" class="tgtSentence">This method does not change the association of the <legacyBold>Stream</legacyBold> object to its underlying source.</caps:sentence>
            <caps:sentence sentenceid="81f0c703aad9578d20d0deb5d149fe8a" id="tgt15" class="tgtSentence"> The <legacyBold>Stream</legacyBold> object will still be associated with the original URL or <legacyBold>Record</legacyBold> that was its source when opened.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ce67ebc6f9cae3389cc286580d354df8" id="tgt16" class="tgtSentence">After a <legacyBold>SaveToFile</legacyBold> operation, the current position (<legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink>) in the stream is set to the beginning of the stream (0).</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt17" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Saves the binary contents of a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> to a file.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Stream</parameterReference>
          <legacyBold>.SaveToFile</legacyBold>
          <parameterReference>FileName</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>SaveOptions</parameterReference>
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
                <caps:sentence id="src3" class="srcSentence">A <legacyBold>String</legacyBold> value that contains the fully-qualified name of the file to which the contents of the <legacyBold>Stream</legacyBold> will be saved.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> You can save to any valid local location, or any location you have access to via a UNC value.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>SaveOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A <legacyLink xlink:href="59339100-6e29-48d1-aea3-6873796d186b">SaveOptionsEnum</legacyLink> value that specifies whether a new file should be created by <legacyBold>SaveToFile</legacyBold>, if it does not already exist.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> Default value is <legacyBold>adSaveCreateNotExists</legacyBold>.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> With these options you can specify that an error occurs if the specified file does not exist.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> You can also specify that <legacyBold>SaveToFile</legacyBold> overwrites the current contents of an existing file.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence id="src10" class="srcSentence">If you overwrite an existing file (when <legacyBold>adSaveCreateOverwrite</legacyBold> is set), <legacyBold>SaveToFile</legacyBold> truncates any bytes from the original existing file that follow the new <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">
              <legacyBold>SaveToFile</legacyBold> may be used to copy the contents of a <legacyBold>Stream </legacyBold>object to a local file.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> There is no change in the contents or properties of the <legacyBold>Stream</legacyBold> object.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> The <legacyBold>Stream</legacyBold> object must be open before calling <legacyBold>SaveToFile</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">This method does not change the association of the <legacyBold>Stream</legacyBold> object to its underlying source.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The <legacyBold>Stream</legacyBold> object will still be associated with the original URL or <legacyBold>Record</legacyBold> that was its source when opened.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">After a <legacyBold>SaveToFile</legacyBold> operation, the current position (<legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink>) in the stream is set to the beginning of the stream (0).</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src17" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
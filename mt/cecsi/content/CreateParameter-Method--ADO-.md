---
title: "CreateParameter Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 9666fdcc-0544-4ed7-a97b-c415f2a56d7e
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
# CreateParameter Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4656a1e40ec0856aa726d4cb328aca4a" id="tgt1" class="tgtSentence">Creates a new <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object with the specified properties.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>parameter</parameterReference> = <parameterReference>command</parameterReference>.<legacyBold>CreateParameter (</legacyBold><parameterReference>Name</parameterReference><legacyBold>, </legacyBold><parameterReference>Type</parameterReference><legacyBold>, </legacyBold><parameterReference>Direction</parameterReference><legacyBold>, </legacyBold><parameterReference>Size</parameterReference><legacyBold>, </legacyBold><parameterReference>Value</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="3d6279c0ac36915f4a4cad0348c618b5" id="tgt2" class="tgtSentence">Returns a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="126d3eb305aa375299a9b5255f84a45f" id="tgt3" class="tgtSentence"> <legacyItalic>Name</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt4" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="4ef7293996e3f53df1d4366c36405797" id="tgt5" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains the name of the <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="3d5db6fea3d2a41199d7bdbdc219501c" id="tgt6" class="tgtSentence"> <legacyItalic>Type</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt7" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="b0afde174aa5514aae5041f9d9a70c7c" id="tgt8" class="tgtSentence"> A <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> value that specifies the data type of the <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d1ccca84613a5a9694f5af54ad398277" id="tgt9" class="tgtSentence"> <legacyItalic>Direction</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt10" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="1a0b309c8a64f80737a0487b48f8bf19" id="tgt11" class="tgtSentence"> A <legacyLink xlink:href="c66aa6e6-d4f0-4f0f-9640-e08ae6cfdef3">ParameterDirectionEnum</legacyLink> value that specifies the type of <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="604149611f1d8c102b8ec214eec6b24a" id="tgt12" class="tgtSentence"> <legacyItalic>Size</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt13" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="fdae7e319434bbbb029c0d459921da6d" id="tgt14" class="tgtSentence"> A <legacyBold>Long</legacyBold> value that specifies the maximum length for the parameter value in characters or bytes.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="586d4526025012f78b5f65abd7fde628" id="tgt15" class="tgtSentence"> <legacyItalic>Value</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt16" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="2fbc822e1a77f7699b76182e60a18fcd" id="tgt17" class="tgtSentence"> A <legacyBold>Variant</legacyBold> that specifies the value for the <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="446626288d4167d7e7b2a6566df84d85" id="tgt18" class="tgtSentence">Use the <legacyBold>CreateParameter</legacyBold> method to create a new <legacyBold>Parameter</legacyBold> object with a specified name, type, direction, size, and value.</caps:sentence>
            <caps:sentence sentenceid="325951975831cc6a7041b05862fb7a1b" id="tgt19" class="tgtSentence"> Any values you pass in the arguments are written to the corresponding <legacyBold>Parameter</legacyBold> properties.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="488ddf33a7e0e9a8901dc71cebcd8240" id="tgt20" class="tgtSentence">This method does not automatically append the <legacyBold>Parameter</legacyBold> object to the <legacyBold>Parameters</legacyBold> collection of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="1c4bc7687fb6062953b1024406ddec9c" id="tgt21" class="tgtSentence"> This lets you set additional properties whose values ADO will validate when you append the <legacyBold>Parameter</legacyBold> object to the collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="62c5fa85c5754803edadcc11486a73ad" id="tgt22" class="tgtSentence">If you specify a variable-length data type in the <legacyItalic>Type</legacyItalic> argument, you must either pass a <legacyItalic>Size</legacyItalic> argument or set the <legacyLink xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size</legacyLink> property of the <legacyBold>Parameter</legacyBold> object before appending it to the <legacyBold>Parameters</legacyBold> collection; otherwise, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a8f10ed48a69a04b21ea37e740bf3063" id="tgt23" class="tgtSentence">If you specify a numeric data type (<legacyBold>adNumeric</legacyBold> or <legacyBold>adDecimal</legacyBold>) in the <legacyItalic>Type</legacyItalic> argument, then you must also set the <legacyLink xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale</legacyLink> and <legacyLink xlink:href="1fa38e78-6b5b-414d-ba0a-3dd26b29b766">Precision</legacyLink> properties.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt24" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="46908cbd-434f-43e7-a794-ed0be0e0c0a7">Visual Basic Example</link>
        <link xlink:href="b57d144c-0a34-49c8-94cf-e5981edfcca6">Visual C++ Example</link>
        <link xlink:href="9673f232-fa58-4439-995a-b4066db628aa">Visual J++ Example</link>
        <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method</link>
        <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Creates a new <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object with the specified properties.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>parameter</parameterReference> = <parameterReference>command</parameterReference>.<legacyBold>CreateParameter (</legacyBold><parameterReference>Name</parameterReference><legacyBold>, </legacyBold><parameterReference>Type</parameterReference><legacyBold>, </legacyBold><parameterReference>Direction</parameterReference><legacyBold>, </legacyBold><parameterReference>Size</parameterReference><legacyBold>, </legacyBold><parameterReference>Value</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>Name</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains the name of the <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>Type</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> A <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> value that specifies the data type of the <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>Direction</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> A <legacyLink xlink:href="c66aa6e6-d4f0-4f0f-9640-e08ae6cfdef3">ParameterDirectionEnum</legacyLink> value that specifies the type of <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>Size</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> A <legacyBold>Long</legacyBold> value that specifies the maximum length for the parameter value in characters or bytes.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src15" class="srcSentence"> <legacyItalic>Value</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src16" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> A <legacyBold>Variant</legacyBold> that specifies the value for the <legacyBold>Parameter</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src18" class="srcSentence">Use the <legacyBold>CreateParameter</legacyBold> method to create a new <legacyBold>Parameter</legacyBold> object with a specified name, type, direction, size, and value.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> Any values you pass in the arguments are written to the corresponding <legacyBold>Parameter</legacyBold> properties.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">This method does not automatically append the <legacyBold>Parameter</legacyBold> object to the <legacyBold>Parameters</legacyBold> collection of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> This lets you set additional properties whose values ADO will validate when you append the <legacyBold>Parameter</legacyBold> object to the collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">If you specify a variable-length data type in the <legacyItalic>Type</legacyItalic> argument, you must either pass a <legacyItalic>Size</legacyItalic> argument or set the <legacyLink xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size</legacyLink> property of the <legacyBold>Parameter</legacyBold> object before appending it to the <legacyBold>Parameters</legacyBold> collection; otherwise, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">If you specify a numeric data type (<legacyBold>adNumeric</legacyBold> or <legacyBold>adDecimal</legacyBold>) in the <legacyItalic>Type</legacyItalic> argument, then you must also set the <legacyLink xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale</legacyLink> and <legacyLink xlink:href="1fa38e78-6b5b-414d-ba0a-3dd26b29b766">Precision</legacyLink> properties.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="46908cbd-434f-43e7-a794-ed0be0e0c0a7">Visual Basic Example</link>
        <link xlink:href="b57d144c-0a34-49c8-94cf-e5981edfcca6">Visual C++ Example</link>
        <link xlink:href="9673f232-fa58-4439-995a-b4066db628aa">Visual J++ Example</link>
        <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method</link>
        <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
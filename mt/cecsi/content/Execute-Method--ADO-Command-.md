---
title: "Execute Method (ADO Command)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f84a5ff3-0528-4ad7-9bea-9a15103378dd
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
# Execute Method (ADO Command)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a811e8d50279827ff9647def7eb2ec11" id="tgt1" class="tgtSentence">Executes the query, SQL statement, or stored procedure specified in the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> or <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream</legacyLink> property of the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command object</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>recordset</parameterReference> = <parameterReference>command</parameterReference>.<legacyBold>Execute( </legacyBold><parameterReference>RecordsAffected</parameterReference><legacyBold>, </legacyBold><parameterReference>Parameters</parameterReference><legacyBold>, </legacyBold><parameterReference>Options </parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="ebc08f787fbb553f78350e57b3139909" id="tgt2" class="tgtSentence">Returns a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object reference, a stream, or <legacyBold>Nothing</legacyBold>.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7818b1bda08fe42f7ac5dcd9cc7471dc" id="tgt3" class="tgtSentence"> <legacyItalic>RecordsAffected</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt4" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="ecc4f294aa113f2a687815946c341a51" id="tgt5" class="tgtSentence"> A <legacyBold>Long</legacyBold> variable to which the provider returns the number of records that the operation affected.</caps:sentence>
                <caps:sentence sentenceid="9cbdfc049e341a2ed2f2a616c430eccc" id="tgt6" class="tgtSentence"> The <legacyItalic>RecordsAffected</legacyItalic> parameter applies only for action queries or stored procedures.</caps:sentence>
                <caps:sentence sentenceid="842143d1477bfb18bf5f140cfb4c5330" id="tgt7" class="tgtSentence">
                  <legacyItalic>RecordsAffected</legacyItalic> does not return the number of records returned by a result-returning query or stored procedure.</caps:sentence>
                <caps:sentence sentenceid="79912501606853bc438e1493280f682e" id="tgt8" class="tgtSentence"> To obtain this information, use the <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink> property.</caps:sentence>
                <caps:sentence sentenceid="8fe257c676ce161b880fb9763ca1df85" id="tgt9" class="tgtSentence"> The <legacyBold>Execute</legacyBold> method will not return the correct information when used with <legacyBold>adAsyncExecute</legacyBold>, simply because when a command is executed asynchronously, the number of records affected may not yet be known at the time the method returns.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="dec089b1feed8f8846fb8f0e20f47730" id="tgt10" class="tgtSentence"> <legacyItalic>Parameters</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt11" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="e2b7e96b653a8ff1f51b96cbcf4d1c2d" id="tgt12" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> array of parameter values used in conjunction with the input string or stream specified in <legacyBold>CommandText</legacyBold> or <legacyBold>CommandStream</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="0700fedc69cd2853ae9cb088db2f5278" id="tgt13" class="tgtSentence"> (Output parameters will not return correct values when passed in this argument.)</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt14" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt15" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="5206dc52ce8ce9f6260427c6117714b8" id="tgt16" class="tgtSentence"> A <languageKeyword>Long</languageKeyword> value that indicates how the provider should evaluate the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> or the <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream</legacyLink> property of the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="75095fa53b65275aa0b64ec11fb1f831" id="tgt17" class="tgtSentence"> Can be a bitmask value made using <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> and/or <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> values.</caps:sentence>
                <caps:sentence sentenceid="06ceeb9da8ae471102598c2482795222" id="tgt18" class="tgtSentence"> For example, you could use <legacyBold>adCmdText</legacyBold> and <legacyBold>adExecuteNoRecords</legacyBold> in combination if you want to have ADO evaluate the value of the <legacyBold>CommandText</legacyBold> property as text, and indicate that the command should discard and not return any records that might be generated when the command text executes.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="f3f230f222a82423f9b14bb71195f871" id="tgt19" class="tgtSentence">Use the <legacyBold>ExecuteOptionEnum</legacyBold> value <legacyBold>adExecuteNoRecords</legacyBold> to improve performance by minimizing internal processing.</caps:sentence>
              <caps:sentence sentenceid="ce6145992684f1034e34a6b424863934" id="tgt20" class="tgtSentence"> If <legacyBold>adExecuteStream</legacyBold> was specified, the options <legacyBold>adAsyncFetch</legacyBold> and <legacyBold>adAsynchFetchNonBlocking</legacyBold> are ignored.</caps:sentence>
              <caps:sentence sentenceid="62f0bada9fb2f19dd0a97446e37c3cae" id="tgt21" class="tgtSentence"> Do not use the <legacyBold>CommandTypeEnum</legacyBold> values of <legacyBold>adCmdFile</legacyBold> or <legacyBold>adCmdTableDirect</legacyBold> with <legacyBold>Execute</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="461fa9b2f583be525714f7d70cf867cd" id="tgt22" class="tgtSentence"> These values can only be used as options with the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> and <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> methods of a <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4cf1ec22cf3ac31c67aa234a9f9b92f2" id="tgt23" class="tgtSentence">Using the <legacyBold>Execute</legacyBold> method on a <legacyBold>Command</legacyBold> object executes the query specified in the <legacyBold>CommandText</legacyBold> property or <legacyBold>CommandStream</legacyBold> property of the object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9a2d26d9f60b2025c1678dd7a06a235c" id="tgt24" class="tgtSentence">Results are returned in a <legacyBold>Recordset</legacyBold> (by default) or as a stream of binary information.</caps:sentence>
            <caps:sentence sentenceid="27c98394738df548010a48d1288ec73f" id="tgt25" class="tgtSentence"> To obtain a binary stream, specify <legacyBold>adExecuteStream</legacyBold> in <legacyItalic>Options</legacyItalic>, then supply a stream by setting <legacyBold>Command.Properties("Output Stream")</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="ac3dea713d2b49b0d8544c81ad472c80" id="tgt26" class="tgtSentence"> An ADO <legacyBold>Stream</legacyBold> object can be specified to receive the results, or another stream object such as the IIS Response object can be specified.</caps:sentence>
            <caps:sentence sentenceid="9a54f6bf4f8c53bda9bdb94e19bbfce8" id="tgt27" class="tgtSentence"> If no stream was specified before calling <legacyBold>Execute</legacyBold> with <legacyBold>adExecuteStream</legacyBold>, an error occurs.</caps:sentence>
            <caps:sentence sentenceid="6270e95cbfc9b708e9d683385bb88c76" id="tgt28" class="tgtSentence"> The position of the stream on return from <legacyBold>Execute</legacyBold> is provider specific.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e6b790053a2849bba68ccc7a3a43b589" id="tgt29" class="tgtSentence">If the command is not intended to return results (for example, an SQL UPDATE query) the provider returns <legacyBold>Nothing</legacyBold> as long as the option <legacyBold>adExecuteNoRecords</legacyBold> is specified; otherwise Execute returns a closed <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="e2a32fe563c873fa069093d9ef0e0755" id="tgt30" class="tgtSentence"> Some application languages allow you to ignore this return value if no <legacyBold>Recordset</legacyBold> is desired.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b6d5f3f8ad8bd90100bb1d0d98f5e03a" id="tgt31" class="tgtSentence">
              <legacyBold>Execute</legacyBold> raises an error if the user specifies a value for <legacyBold>CommandStream</legacyBold> when the <legacyBold>CommandType</legacyBold> is <legacyBold>adCmdStoredProc</legacyBold>, <legacyBold>adCmdTable</legacyBold>, or <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a9d3a4ee31d72b6560b2eece176af951" id="tgt32" class="tgtSentence">If the query has parameters, the current values for the <legacyBold>Command</legacyBold> object's parameters are used unless you override these with parameter values passed with the <legacyBold>Execute</legacyBold> call.</caps:sentence>
            <caps:sentence sentenceid="e25d95b6832e5931cfa64ee9220905fc" id="tgt33" class="tgtSentence"> You can override a subset of the parameters by omitting new values for some of the parameters when calling the <legacyBold>Execute</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="3984a9051fcaabc7d26b407c8c2c2c60" id="tgt34" class="tgtSentence"> The order in which you specify the parameters is the same order in which the method passes them.</caps:sentence>
            <caps:sentence sentenceid="60e9ab5c82afafe576d4521170c50d0a" id="tgt35" class="tgtSentence"> For example, if there were four (or more) parameters and you wanted to pass new values for only the first and fourth parameters, you would pass <codeInline>Array(var1,,,var4)</codeInline> as the <legacyItalic>Parameters</legacyItalic> argument.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="62ece879eda1b04f2eac961d8d00c2d6" id="tgt36" class="tgtSentence">Output parameters will not return correct values when passed in the <legacyItalic>Parameters</legacyItalic> argument.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="fea7888d509bcbea9690b07ce6b56f68" id="tgt37" class="tgtSentence">An <legacyLink xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete</legacyLink> event will be issued when this operation concludes.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="fdfd557b3dd67ca1cc6382d1add54378" id="tgt38" class="tgtSentence">When issuing commands containing URLs, those using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt39" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt40" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ed5e1b60-3769-4b26-a253-1d721e37941d">Visual Basic Example</link>
        <link xlink:href="3a7bbf07-2fca-4892-95f4-eec93f2d5e91">VBScript Example</link>
        <link xlink:href="ada6acc1-82eb-4cfa-8f2f-617a916ffd8d">Visual C++ Example</link>
        <link xlink:href="3c92cb19-c13b-4bb3-b4cd-75dc8f42057c">Visual J++ Example</link>
        <link xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream Property</link>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
        <link xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</link>
        <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>
        <link xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete Event</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Executes the query, SQL statement, or stored procedure specified in the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> or <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream</legacyLink> property of the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command object</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>recordset</parameterReference> = <parameterReference>command</parameterReference>.<legacyBold>Execute( </legacyBold><parameterReference>RecordsAffected</parameterReference><legacyBold>, </legacyBold><parameterReference>Parameters</parameterReference><legacyBold>, </legacyBold><parameterReference>Options </parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object reference, a stream, or <legacyBold>Nothing</legacyBold>.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>RecordsAffected</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> A <legacyBold>Long</legacyBold> variable to which the provider returns the number of records that the operation affected.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> The <legacyItalic>RecordsAffected</legacyItalic> parameter applies only for action queries or stored procedures.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence">
                  <legacyItalic>RecordsAffected</legacyItalic> does not return the number of records returned by a result-returning query or stored procedure.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> To obtain this information, use the <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink> property.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> The <legacyBold>Execute</legacyBold> method will not return the correct information when used with <legacyBold>adAsyncExecute</legacyBold>, simply because when a command is executed asynchronously, the number of records affected may not yet be known at the time the method returns.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>Parameters</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> array of parameter values used in conjunction with the input string or stream specified in <legacyBold>CommandText</legacyBold> or <legacyBold>CommandStream</legacyBold>.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> (Output parameters will not return correct values when passed in this argument.)</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src14" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src15" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> A <languageKeyword>Long</languageKeyword> value that indicates how the provider should evaluate the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> or the <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream</legacyLink> property of the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> Can be a bitmask value made using <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> and/or <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> values.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> For example, you could use <legacyBold>adCmdText</legacyBold> and <legacyBold>adExecuteNoRecords</legacyBold> in combination if you want to have ADO evaluate the value of the <legacyBold>CommandText</legacyBold> property as text, and indicate that the command should discard and not return any records that might be generated when the command text executes.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence id="src19" class="srcSentence">Use the <legacyBold>ExecuteOptionEnum</legacyBold> value <legacyBold>adExecuteNoRecords</legacyBold> to improve performance by minimizing internal processing.</caps:sentence>
              <caps:sentence id="src20" class="srcSentence"> If <legacyBold>adExecuteStream</legacyBold> was specified, the options <legacyBold>adAsyncFetch</legacyBold> and <legacyBold>adAsynchFetchNonBlocking</legacyBold> are ignored.</caps:sentence>
              <caps:sentence id="src21" class="srcSentence"> Do not use the <legacyBold>CommandTypeEnum</legacyBold> values of <legacyBold>adCmdFile</legacyBold> or <legacyBold>adCmdTableDirect</legacyBold> with <legacyBold>Execute</legacyBold>.</caps:sentence>
              <caps:sentence id="src22" class="srcSentence"> These values can only be used as options with the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> and <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> methods of a <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src23" class="srcSentence">Using the <legacyBold>Execute</legacyBold> method on a <legacyBold>Command</legacyBold> object executes the query specified in the <legacyBold>CommandText</legacyBold> property or <legacyBold>CommandStream</legacyBold> property of the object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">Results are returned in a <legacyBold>Recordset</legacyBold> (by default) or as a stream of binary information.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> To obtain a binary stream, specify <legacyBold>adExecuteStream</legacyBold> in <legacyItalic>Options</legacyItalic>, then supply a stream by setting <legacyBold>Command.Properties("Output Stream")</legacyBold>.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> An ADO <legacyBold>Stream</legacyBold> object can be specified to receive the results, or another stream object such as the IIS Response object can be specified.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> If no stream was specified before calling <legacyBold>Execute</legacyBold> with <legacyBold>adExecuteStream</legacyBold>, an error occurs.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> The position of the stream on return from <legacyBold>Execute</legacyBold> is provider specific.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">If the command is not intended to return results (for example, an SQL UPDATE query) the provider returns <legacyBold>Nothing</legacyBold> as long as the option <legacyBold>adExecuteNoRecords</legacyBold> is specified; otherwise Execute returns a closed <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> Some application languages allow you to ignore this return value if no <legacyBold>Recordset</legacyBold> is desired.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src31" class="srcSentence">
              <legacyBold>Execute</legacyBold> raises an error if the user specifies a value for <legacyBold>CommandStream</legacyBold> when the <legacyBold>CommandType</legacyBold> is <legacyBold>adCmdStoredProc</legacyBold>, <legacyBold>adCmdTable</legacyBold>, or <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">If the query has parameters, the current values for the <legacyBold>Command</legacyBold> object's parameters are used unless you override these with parameter values passed with the <legacyBold>Execute</legacyBold> call.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> You can override a subset of the parameters by omitting new values for some of the parameters when calling the <legacyBold>Execute</legacyBold> method.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> The order in which you specify the parameters is the same order in which the method passes them.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> For example, if there were four (or more) parameters and you wanted to pass new values for only the first and fourth parameters, you would pass <codeInline>Array(var1,,,var4)</codeInline> as the <legacyItalic>Parameters</legacyItalic> argument.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src36" class="srcSentence">Output parameters will not return correct values when passed in the <legacyItalic>Parameters</legacyItalic> argument.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src37" class="srcSentence">An <legacyLink xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete</legacyLink> event will be issued when this operation concludes.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src38" class="srcSentence">When issuing commands containing URLs, those using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src39" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src40" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ed5e1b60-3769-4b26-a253-1d721e37941d">Visual Basic Example</link>
        <link xlink:href="3a7bbf07-2fca-4892-95f4-eec93f2d5e91">VBScript Example</link>
        <link xlink:href="ada6acc1-82eb-4cfa-8f2f-617a916ffd8d">Visual C++ Example</link>
        <link xlink:href="3c92cb19-c13b-4bb3-b4cd-75dc8f42057c">Visual J++ Example</link>
        <link xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream Property</link>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
        <link xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</link>
        <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>
        <link xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete Event</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
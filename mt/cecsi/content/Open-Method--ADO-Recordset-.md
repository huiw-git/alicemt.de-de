---
title: "Open Method (ADO Recordset)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3236749c-4b71-4235-89e2-ccdfaaa9319d
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
# Open Method (ADO Recordset)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a693dac402d823e12409763d503e4ee2" id="tgt1" class="tgtSentence">Opens a cursor on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.Open</legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>ActiveConnection</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>CursorType</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>LockType</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Options</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>Source </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt2" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="09311963da6fffb87deee7d9009716ea" id="tgt3" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> that evaluates to a valid <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object, an SQL statement, a table name, a stored procedure call, a URL, or the name of a file or <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object containing a persistently stored <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>ActiveConnection </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt4" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="f8828f8f46a2046d57a814f24bdde1f3" id="tgt5" class="tgtSentence"> Either a <languageKeyword>Variant</languageKeyword> that evaluates to a valid <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object variable name, or a <languageKeyword>String</languageKeyword> that contains <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> parameters.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>CursorType </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt6" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="e3c9ac915a8223143f45aeff98439cde" id="tgt7" class="tgtSentence"> A <legacyLink xlink:href="ffc6e245-4471-42ae-84dd-e85bddfce983">CursorTypeEnum</legacyLink> value that determines the type of cursor that the provider should use when opening the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
                <caps:sentence sentenceid="f7890568d843229a0211c2a51c319424" id="tgt8" class="tgtSentence"> The default value is <legacyBold>adOpenForwardOnly</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>LockType </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt9" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="b7bdc0d265951f1295b4f8a2ee1fe6e4" id="tgt10" class="tgtSentence"> A <legacyLink xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</legacyLink> value that determines what type of locking (concurrency) the provider should use when opening the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
                <caps:sentence sentenceid="a26c9e32289b077755bd0b340d0557d8" id="tgt11" class="tgtSentence"> The default value is <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>Options </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt12" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="a8b45f816654f9436c89959284a23638" id="tgt13" class="tgtSentence"> A <languageKeyword>Long</languageKeyword> value that indicates how the provider should evaluate the <parameterReference>Source</parameterReference> argument if it represents something other than a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object, or that the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> should be restored from a file where it was previously saved.</caps:sentence>
                <caps:sentence sentenceid="f1a5267b6e6b91989e1aaf402118a166" id="tgt14" class="tgtSentence"> Can be one or more <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> or <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> values, which can be combined with a bitwise OR operator.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="fd7cba59aeb14b0eb5a9e7044f6afd2b" id="tgt15" class="tgtSentence">If you open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> from a <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> containing a persisted <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, using an <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> value of <legacyBold>adAsyncFetchNonBlocking</legacyBold> will have no effect; the fetch will be synchronous and blocking.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="3f66fb8c3512e7ff339fdd19bac69a05" id="tgt16" class="tgtSentence">The <legacyBold>ExecuteOpenEnum</legacyBold> values of <legacyBold>adExecuteNoRecords</legacyBold> or <legacyBold>adExecuteStream</legacyBold> should not be used with <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="20319314fefc4f77f55a83fad5227ea2" id="tgt17" class="tgtSentence">The default cursor for an ADO <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is a forward-only, read-only cursor located on the server.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="402a1beb8d09ee9b8ea121d768d11099" id="tgt18" class="tgtSentence">Using the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method on a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object opens a cursor that represents records from a base table, the results of a query, or a previously saved <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d9621f732e411f13abbbd4beca79196c" id="tgt19" class="tgtSentence">Use the optional <parameterReference>Source</parameterReference> argument to specify a data source using one of the following: a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object variable, an SQL statement, a stored procedure, a table name, a URL, or a complete file path name.</caps:sentence>
            <caps:sentence sentenceid="7003df56cf06f3d8a7041906591c8eef" id="tgt20" class="tgtSentence"> If <parameterReference>Source</parameterReference> is a file path name, it can be a full path ("c:\dir\file.rst"), a relative path ("..\file.rst"), or a URL ("http://files/file.rst").</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="28cfada7a216d6d59aee9d66de5d453b" id="tgt21" class="tgtSentence">It is not a good idea to use the <parameterReference>Source</parameterReference> argument of the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method to perform an action query that does not return records because there is no easy way to determine whether the call succeeded.</caps:sentence>
            <caps:sentence sentenceid="c59e341df3f0e7cf4a3da5bc169b965f" id="tgt22" class="tgtSentence"> The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> returned by such a query will be closed.</caps:sentence>
            <caps:sentence sentenceid="d5e29c617d37baa976bd74bf530d82a3" id="tgt23" class="tgtSentence"> To perform a query that does not return records, such as a SQL INSERT statement, call the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method of a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object or the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object instead.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="72d9ffd67a75d764ff524f22a9466e48" id="tgt24" class="tgtSentence">The <parameterReference>ActiveConnection</parameterReference> argument corresponds to the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property and specifies in which connection to open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="7eb5ded68a3a4bfb72043c81396b3433" id="tgt25" class="tgtSentence"> If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</caps:sentence>
            <caps:sentence sentenceid="2917b9e3fbe39083000fd07f3a84244c" id="tgt26" class="tgtSentence"> After you open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> with a client-side cursor by setting the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>, you can change the value of this property to send updates to another provider.</caps:sentence>
            <caps:sentence sentenceid="a9b7f61252024bc68d637e612949854b" id="tgt27" class="tgtSentence"> Or you can set this property to <legacyBold>Nothing</legacyBold> (in Microsoft Visual Basic) or NULL to disconnect the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> from any provider.</caps:sentence>
            <caps:sentence sentenceid="e6bbed85612f5e28f5bfe21bcf44b470" id="tgt28" class="tgtSentence"> Changing <parameterReference>ActiveConnection</parameterReference> for a server-side cursor generates an error, however.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dc1a4db51ae7ad46d10200eb3304bb01" id="tgt29" class="tgtSentence">For the other arguments that correspond directly to properties of a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object (<parameterReference>Source</parameterReference>, <parameterReference>CursorType</parameterReference>, and <parameterReference>LockType</parameterReference>), the relationship of the arguments to the properties is as follows:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3f2ca5e27d93eb15f6ee8805bb6cb59c" id="tgt30" class="tgtSentence">The property is read/write before the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is opened.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="30728e79960d23fa0e278264ed25dd0c" id="tgt31" class="tgtSentence">The property settings are used unless you pass the corresponding arguments when executing the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method.</caps:sentence>
                <caps:sentence sentenceid="989f8224516e70293fb557a2e07b8f05" id="tgt32" class="tgtSentence"> If you pass an argument, it overrides the corresponding property setting, and the property setting is updated with the argument value.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="130dfabb6c8588ba3a14f31ea3400f0f" id="tgt33" class="tgtSentence">After you open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, these properties become read-only.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="7a2cfca452f23a62d9d4012187de8a03" id="tgt34" class="tgtSentence">The <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property is read-only for <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects whose <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> property is set to a valid <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object, even if the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is not open.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="6c7998e0869005259ec5a7f3faa4350d" id="tgt35" class="tgtSentence">If you pass a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object in the <parameterReference>Source</parameterReference> argument and also pass an <parameterReference>ActiveConnection</parameterReference> argument, an error occurs.</caps:sentence>
            <caps:sentence sentenceid="6b0226c3d33495c393a3fbed5e0ade2c" id="tgt36" class="tgtSentence"> The <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property of the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object must already be set to a valid <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object or connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="eccf2ed228a87b4a06f6ce27e7bab87f" id="tgt37" class="tgtSentence">If you pass something other than a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object in the <parameterReference>Source</parameterReference> argument, you can use the <parameterReference>Options</parameterReference> argument to optimize evaluation of the <parameterReference>Source</parameterReference> argument.</caps:sentence>
            <caps:sentence sentenceid="d649d56e6f3197d388bc2aebe0ec1169" id="tgt38" class="tgtSentence"> If the <parameterReference>Options</parameterReference> argument is not defined, you may experience diminished performance because ADO must make calls to the provider to determine if the argument is an SQL statement, a stored procedure, a URL, or a table name.</caps:sentence>
            <caps:sentence sentenceid="a3c2aaded204d11aa8ae076bcaf042cf" id="tgt39" class="tgtSentence"> If you know what <parameterReference>Source</parameterReference> type you are using, setting the <parameterReference>Options</parameterReference> argument instructs ADO to jump directly to the relevant code.</caps:sentence>
            <caps:sentence sentenceid="40f53afbed78a1bcb882c806721613b7" id="tgt40" class="tgtSentence"> If the <parameterReference>Options</parameterReference> argument does not match the <parameterReference>Source</parameterReference> type, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="12cdf12fcb8f7ab326af22d522aa1ced" id="tgt41" class="tgtSentence">If you pass a <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object in the <parameterReference>Source</parameterReference> argument, you should not pass information into the other arguments.</caps:sentence>
            <caps:sentence sentenceid="23098fbdd200b4d0b11ea39542dc8a6d" id="tgt42" class="tgtSentence"> Doing so will generate an error.</caps:sentence>
            <caps:sentence sentenceid="d2be92f380a4bca173d27914158a51aa" id="tgt43" class="tgtSentence"> The <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> information is not retained when a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is opened from a <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4b04516a94a5bf78a5b7f9878f4d404b" id="tgt44" class="tgtSentence">The default for the <parameterReference>Options</parameterReference> argument is <legacyBold>adCmdFile</legacyBold> if no connection is associated with the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="f8bf7b8110190c52b1028f5259a241b1" id="tgt45" class="tgtSentence"> This will typically be the case for persistently stored <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e43bfab92eb46cdb50449f8cded2f2cd" id="tgt46" class="tgtSentence">If the data source returns no records, the provider sets both the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> and <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> properties to <languageKeyword>True</languageKeyword>, and the current record position is undefined.</caps:sentence>
            <caps:sentence sentenceid="544b1f120ca6a13d108deef0a14bea00" id="tgt47" class="tgtSentence"> You can still add new data to this empty <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object if the cursor type allows it.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ffe87232395d0479e5887b4187098409" id="tgt48" class="tgtSentence">When you have concluded your operations over an open <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, use the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method to free any associated system resources.</caps:sentence>
            <caps:sentence sentenceid="c9758c9d991bf7e20313c74b54565fb8" id="tgt49" class="tgtSentence"> Closing an object does not remove it from memory; you can change its property settings and use the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method to open it again later.</caps:sentence>
            <caps:sentence sentenceid="693863852351b388a81bf1f40a9c0b0d" id="tgt50" class="tgtSentence"> To completely eliminate an object from memory, set the object variable to <parameterReference>Nothing</parameterReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="940a8b5999afe59a0dd4dac463046e40" id="tgt51" class="tgtSentence">Before the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property is set, call <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> with no operands to create an instance of a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> created by appending fields to the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9d4900ef096ae7dbc343eac5d3d1d529" id="tgt52" class="tgtSentence">If you have set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>, you can retrieve rows asynchronously in one of two ways.</caps:sentence>
            <caps:sentence sentenceid="e1de0646e30c3852b345e8b44905e8fe" id="tgt53" class="tgtSentence"> The recommended method is to set <parameterReference>Options</parameterReference> to <legacyBold>adAsyncFetch</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="6a0d694af87b5fadfda75d606e39f404" id="tgt54" class="tgtSentence"> Alternatively, you can use the "Asynchronous Rowset Processing" dynamic property in the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection, but related retrieved events can be lost if you do not set the <parameterReference>Options</parameterReference> parameter to <legacyBold>adAsyncFetch</legacyBold>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="282331723524ce2456dbdbcfb8673900" id="tgt55" class="tgtSentence">Background fetching in the MS Remote provider is supported only through the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method's <parameterReference>Options</parameterReference> parameter.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt56" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt57" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="03d15b36fcd7206efa078ab22784fe40" id="tgt58" class="tgtSentence">Certain combinations of <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> and <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> values are not valid.</caps:sentence>
            <caps:sentence sentenceid="0440bed8e1eb88e7f9ac506385cc4d47" id="tgt59" class="tgtSentence"> For information about which options cannot be combined, see the topics for the <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink>, and <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt60" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1311d561-0e86-40f5-8cbc-ad8f13e626d1">Visual Basic Example</link>
        <link xlink:href="66eca011-e258-4d8f-bd67-e017bcf0871b">VBScript Example</link>
        <link xlink:href="f74a81fd-cbcc-4143-b9f8-774c88dd4fad">Visual C++ Example</link>
        <link xlink:href="0b7dd9f8-4751-48fb-a75d-c6f75d80d928">Visual J++ Example</link>
        <link xlink:href="ddccdf58-9c57-4c9b-8b7f-0cf193f955fb">Visual Basic Example</link>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Opens a cursor on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.Open</legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>ActiveConnection</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>CursorType</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>LockType</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Options</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>Source </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src2" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src3" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> that evaluates to a valid <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object, an SQL statement, a table name, a stored procedure call, a URL, or the name of a file or <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object containing a persistently stored <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>ActiveConnection </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> Either a <languageKeyword>Variant</languageKeyword> that evaluates to a valid <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object variable name, or a <languageKeyword>String</languageKeyword> that contains <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> parameters.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>CursorType </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> A <legacyLink xlink:href="ffc6e245-4471-42ae-84dd-e85bddfce983">CursorTypeEnum</legacyLink> value that determines the type of cursor that the provider should use when opening the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> The default value is <legacyBold>adOpenForwardOnly</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>LockType </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> A <legacyLink xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</legacyLink> value that determines what type of locking (concurrency) the provider should use when opening the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> The default value is <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>Options </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src12" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> A <languageKeyword>Long</languageKeyword> value that indicates how the provider should evaluate the <parameterReference>Source</parameterReference> argument if it represents something other than a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object, or that the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> should be restored from a file where it was previously saved.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> Can be one or more <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> or <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> values, which can be combined with a bitwise OR operator.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence id="src15" class="srcSentence">If you open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> from a <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> containing a persisted <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, using an <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> value of <legacyBold>adAsyncFetchNonBlocking</legacyBold> will have no effect; the fetch will be synchronous and blocking.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src16" class="srcSentence">The <legacyBold>ExecuteOpenEnum</legacyBold> values of <legacyBold>adExecuteNoRecords</legacyBold> or <legacyBold>adExecuteStream</legacyBold> should not be used with <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">The default cursor for an ADO <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is a forward-only, read-only cursor located on the server.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">Using the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method on a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object opens a cursor that represents records from a base table, the results of a query, or a previously saved <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">Use the optional <parameterReference>Source</parameterReference> argument to specify a data source using one of the following: a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object variable, an SQL statement, a stored procedure, a table name, a URL, or a complete file path name.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> If <parameterReference>Source</parameterReference> is a file path name, it can be a full path ("c:\dir\file.rst"), a relative path ("..\file.rst"), or a URL ("http://files/file.rst").</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">It is not a good idea to use the <parameterReference>Source</parameterReference> argument of the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method to perform an action query that does not return records because there is no easy way to determine whether the call succeeded.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> The <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> returned by such a query will be closed.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> To perform a query that does not return records, such as a SQL INSERT statement, call the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method of a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object or the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object instead.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">The <parameterReference>ActiveConnection</parameterReference> argument corresponds to the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property and specifies in which connection to open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> After you open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> with a client-side cursor by setting the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>, you can change the value of this property to send updates to another provider.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> Or you can set this property to <legacyBold>Nothing</legacyBold> (in Microsoft Visual Basic) or NULL to disconnect the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> from any provider.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> Changing <parameterReference>ActiveConnection</parameterReference> for a server-side cursor generates an error, however.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">For the other arguments that correspond directly to properties of a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object (<parameterReference>Source</parameterReference>, <parameterReference>CursorType</parameterReference>, and <parameterReference>LockType</parameterReference>), the relationship of the arguments to the properties is as follows:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">The property is read/write before the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is opened.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src31" class="srcSentence">The property settings are used unless you pass the corresponding arguments when executing the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> If you pass an argument, it overrides the corresponding property setting, and the property setting is updated with the argument value.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">After you open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, these properties become read-only.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src34" class="srcSentence">The <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property is read-only for <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects whose <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> property is set to a valid <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object, even if the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is not open.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src35" class="srcSentence">If you pass a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object in the <parameterReference>Source</parameterReference> argument and also pass an <parameterReference>ActiveConnection</parameterReference> argument, an error occurs.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> The <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property of the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object must already be set to a valid <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object or connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src37" class="srcSentence">If you pass something other than a <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object in the <parameterReference>Source</parameterReference> argument, you can use the <parameterReference>Options</parameterReference> argument to optimize evaluation of the <parameterReference>Source</parameterReference> argument.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> If the <parameterReference>Options</parameterReference> argument is not defined, you may experience diminished performance because ADO must make calls to the provider to determine if the argument is an SQL statement, a stored procedure, a URL, or a table name.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> If you know what <parameterReference>Source</parameterReference> type you are using, setting the <parameterReference>Options</parameterReference> argument instructs ADO to jump directly to the relevant code.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> If the <parameterReference>Options</parameterReference> argument does not match the <parameterReference>Source</parameterReference> type, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src41" class="srcSentence">If you pass a <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object in the <parameterReference>Source</parameterReference> argument, you should not pass information into the other arguments.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> Doing so will generate an error.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> The <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> information is not retained when a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is opened from a <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src44" class="srcSentence">The default for the <parameterReference>Options</parameterReference> argument is <legacyBold>adCmdFile</legacyBold> if no connection is associated with the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> This will typically be the case for persistently stored <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src46" class="srcSentence">If the data source returns no records, the provider sets both the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> and <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> properties to <languageKeyword>True</languageKeyword>, and the current record position is undefined.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> You can still add new data to this empty <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object if the cursor type allows it.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src48" class="srcSentence">When you have concluded your operations over an open <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, use the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method to free any associated system resources.</caps:sentence>
            <caps:sentence id="src49" class="srcSentence"> Closing an object does not remove it from memory; you can change its property settings and use the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method to open it again later.</caps:sentence>
            <caps:sentence id="src50" class="srcSentence"> To completely eliminate an object from memory, set the object variable to <parameterReference>Nothing</parameterReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src51" class="srcSentence">Before the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property is set, call <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> with no operands to create an instance of a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> created by appending fields to the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src52" class="srcSentence">If you have set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>, you can retrieve rows asynchronously in one of two ways.</caps:sentence>
            <caps:sentence id="src53" class="srcSentence"> The recommended method is to set <parameterReference>Options</parameterReference> to <legacyBold>adAsyncFetch</legacyBold>.</caps:sentence>
            <caps:sentence id="src54" class="srcSentence"> Alternatively, you can use the "Asynchronous Rowset Processing" dynamic property in the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection, but related retrieved events can be lost if you do not set the <parameterReference>Options</parameterReference> parameter to <legacyBold>adAsyncFetch</legacyBold>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src55" class="srcSentence">Background fetching in the MS Remote provider is supported only through the <unmanagedCodeEntityReference>Open</unmanagedCodeEntityReference> method's <parameterReference>Options</parameterReference> parameter.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src56" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src57" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src58" class="srcSentence">Certain combinations of <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> and <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> values are not valid.</caps:sentence>
            <caps:sentence id="src59" class="srcSentence"> For information about which options cannot be combined, see the topics for the <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink>, and <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src60" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1311d561-0e86-40f5-8cbc-ad8f13e626d1">Visual Basic Example</link>
        <link xlink:href="66eca011-e258-4d8f-bd67-e017bcf0871b">VBScript Example</link>
        <link xlink:href="f74a81fd-cbcc-4143-b9f8-774c88dd4fad">Visual C++ Example</link>
        <link xlink:href="0b7dd9f8-4751-48fb-a75d-c6f75d80d928">Visual J++ Example</link>
        <link xlink:href="ddccdf58-9c57-4c9b-8b7f-0cf193f955fb">Visual Basic Example</link>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
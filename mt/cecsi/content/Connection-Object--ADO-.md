---
title: "Connection Object (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ef6b1824-5b12-43db-89d7-8f3d13896d4d
caps.latest.revision: 5
caps.handback.revision: 5
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
# Connection Object (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="17dc7d8e216483c723a1979048ea0392" id="tgt1" class="tgtSentence">Represents an open connection to a data source.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="c6f273facf401ba4d939fd0f46ddfd88" id="tgt2" class="tgtSentence">A <legacyBold>Connection</legacyBold> object represents a unique session with a data source.</caps:sentence>
            <caps:sentence sentenceid="7c685a6598203adea37b4d55479dc435" id="tgt3" class="tgtSentence"> In a client/server database system, it may be equivalent to an actual network connection to the server.</caps:sentence>
            <caps:sentence sentenceid="8b1f37db8421e94019898cbf52bd64ae" id="tgt4" class="tgtSentence"> Depending on the functionality supported by the provider, some collections, methods, or properties of a <legacyBold>Connection</legacyBold> object may not be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fc703fe0582191b9d3217d3b8bdbe25a" id="tgt5" class="tgtSentence">With the collections, methods, and properties of a <legacyBold>Connection</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="dcfb6f8c9cbca414d93ac3f188e4aff8" id="tgt6" class="tgtSentence">Configure the connection before opening it with the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink>, <legacyLink xlink:href="8904a403-1383-4b4b-b53d-5c01d6f5deac">ConnectionTimeout</legacyLink>, and <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> properties.</caps:sentence>
                <caps:sentence sentenceid="2592a8aabea7d8923847b9ce2407d2f4" id="tgt7" class="tgtSentence">
                  <legacyBold>ConnectionString</legacyBold> is the default property of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f24f2718f6c6334fb609084c21cf837d" id="tgt8" class="tgtSentence">Set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to client to invoke the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink>, which supports batch updates.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f6adc14451c466dd8a4a01efdc0b8d3d" id="tgt9" class="tgtSentence">Set the default database for the connection with the <legacyLink xlink:href="41e8a8dd-e69c-4a09-8736-93502e01961c">DefaultDatabase</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f0b25b432cf8157f84b9adb7bb21286f" id="tgt10" class="tgtSentence">Set the level of isolation for the transactions opened on the connection with the <legacyLink xlink:href="ea84e4b2-fbf2-4eef-b9ce-796b22e21800">IsolationLevel</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="945b911a82a53f21e0cc9fd544049f59" id="tgt11" class="tgtSentence">Specify an OLE DB provider with the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="aae85b8f66568e545c31d3a91d56253d" id="tgt12" class="tgtSentence">Establish, and later break, the physical connection to the data source with the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> and <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1379beb767a96c8ce487eeeb36705acc" id="tgt13" class="tgtSentence">Execute a command on the connection with the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method and configure the execution with the <legacyLink xlink:href="c611f857-d6b0-4dca-8925-f4a02e769eb0">CommandTimeout</legacyLink> property.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="02e32905c17bd6aa187afb7ccf9a5fa2" id="tgt14" class="tgtSentence">To execute a query without using a Command object, pass a query string to the <legacyBold>Execute</legacyBold> method of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
                  <caps:sentence sentenceid="c0486db4628c5443cda9a29f728f2782" id="tgt15" class="tgtSentence"> However, a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object is required when you want to persist the command text and re-execute it, or use query parameters.</caps:sentence>
                </para>
              </alert>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9f553a152bc038084c2ecdbff768a615" id="tgt16" class="tgtSentence">Manage transactions on the open connection, including nested transactions if the provider supports them, with the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans</legacyLink>, <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">CommitTrans</legacyLink>, and <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">RollbackTrans</legacyLink> methods and the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b7d7db7ae96426593e92ce3cc58e7f80" id="tgt17" class="tgtSentence">Examine errors returned from the data source with the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ded47f2841b649e8f3b6aeb4b14ff38c" id="tgt18" class="tgtSentence">Read the version from the ADO implementation used with the <legacyLink xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="46f1edfa2e5972e5b2b2769fb51dce6d" id="tgt19" class="tgtSentence">Obtain schema information about your database with the <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="66fbf588b9ed718c952fe1eb5fffa34e" id="tgt20" class="tgtSentence">You can create <legacyBold>Connection</legacyBold> objects independently of any other previously defined object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bd1a0de1d55f598fc65588b25071b74e" id="tgt21" class="tgtSentence">You can execute named commands or stored procedures as if they were native methods on a <legacyBold>Connection</legacyBold> object, as shown in the next section.</caps:sentence>
            <caps:sentence sentenceid="85a58a7da0c3670304111a7a8d9395c2" id="tgt22" class="tgtSentence"> When a named command has the same name as that of a stored procedure, invoke the "native method call" on a <legacyBold>Connection</legacyBold> object always execute the named command instead of the store procedure.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="9b3b610e2c37045ff005316148af78bc" id="tgt23" class="tgtSentence">Do not use this feature (calling a named command or stored procedure as if it were a native method on the <legacyBold>Connection</legacyBold> object) in a Microsoft® .NET Framework application, because the underlying implementation of the feature conflicts with the way the .NET Framework interoperates with COM.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="59f721693ee9315c9774ed51298138cf" id="tgt24" class="tgtSentence">Execute a command as a native method of a Connection object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2dc9e2748b86a71882279ecd788b1cfe" id="tgt25" class="tgtSentence">To execute a command, give the command a name using the <legacyBold>Command</legacyBold> object <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property.</caps:sentence>
            <caps:sentence sentenceid="f98b8dcc532789efbc8e5d1775c58380" id="tgt26" class="tgtSentence"> Set the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object to the connection.</caps:sentence>
            <caps:sentence sentenceid="17d5b274ade82ffb55f29ce1cec964c6" id="tgt27" class="tgtSentence"> Then issue a statement where the command name is used as if it were a method on the <legacyBold>Connection</legacyBold> object, followed by any parameters, and a <legacyBold>Recordset</legacyBold> object if any rows are returned.</caps:sentence>
            <caps:sentence sentenceid="c80b18dc849a8d9ccaf5b93377fc2382" id="tgt28" class="tgtSentence"> Set the <legacyBold>Recordset</legacyBold> properties to customize the resulting <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt29" class="tgtSentence"> For example:</caps:sentence>
          </para>
          <code>Dim cnn As New ADODB.Connection
Dim cmd As New ADODB.Command
Dim rst As New ADODB.Recordset
...
cnn.Open "..."
cmd.Name = "yourCommandName"
cmd.ActiveConnection = cnn
...
'Your command name, any parameters, and an optional Recordset.
cnn. "parameter", rst</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a8a940267ad4916e5008b5a399e6fed6" id="tgt30" class="tgtSentence">Execute a stored procedure as a native method of a Connection object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e4eb26a7eebda661746b8308750d3cb0" id="tgt31" class="tgtSentence">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the <legacyBold>Connection</legacyBold> object, followed by any parameters.</caps:sentence>
            <caps:sentence sentenceid="b39a9ea97cc463deb746f7401f23c912" id="tgt32" class="tgtSentence"> ADO will make a "best guess" of parameter types.</caps:sentence>
            <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt33" class="tgtSentence"> For example:</caps:sentence>
          </para>
          <code>Dim cnn As New ADODB.Connection
...
'Your stored procedure name and any parameters.
cnn. "parameter"</code>
          <para>
            <caps:sentence sentenceid="857c40f138d02f65a37171b91e66e504" id="tgt34" class="tgtSentence">The <legacyBold>Connection</legacyBold> object is safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt35" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="bb7076ae15ac7a68b9624c6655c565ff" id="tgt36" class="tgtSentence">
                  <legacyLink xlink:href="f571b74d-b796-4009-9c66-6a36ab995a2a">Connection Object Properties, Methods, and Events</legacyLink>  </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents an open connection to a data source.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <legacyBold>Connection</legacyBold> object represents a unique session with a data source.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> In a client/server database system, it may be equivalent to an actual network connection to the server.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Depending on the functionality supported by the provider, some collections, methods, or properties of a <legacyBold>Connection</legacyBold> object may not be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">With the collections, methods, and properties of a <legacyBold>Connection</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Configure the connection before opening it with the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink>, <legacyLink xlink:href="8904a403-1383-4b4b-b53d-5c01d6f5deac">ConnectionTimeout</legacyLink>, and <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> properties.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence">
                  <legacyBold>ConnectionString</legacyBold> is the default property of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to client to invoke the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink>, which supports batch updates.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Set the default database for the connection with the <legacyLink xlink:href="41e8a8dd-e69c-4a09-8736-93502e01961c">DefaultDatabase</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Set the level of isolation for the transactions opened on the connection with the <legacyLink xlink:href="ea84e4b2-fbf2-4eef-b9ce-796b22e21800">IsolationLevel</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Specify an OLE DB provider with the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Establish, and later break, the physical connection to the data source with the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> and <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> methods.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Execute a command on the connection with the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method and configure the execution with the <legacyLink xlink:href="c611f857-d6b0-4dca-8925-f4a02e769eb0">CommandTimeout</legacyLink> property.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src14" class="srcSentence">To execute a query without using a Command object, pass a query string to the <legacyBold>Execute</legacyBold> method of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> However, a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object is required when you want to persist the command text and re-execute it, or use query parameters.</caps:sentence>
                </para>
              </alert>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">Manage transactions on the open connection, including nested transactions if the provider supports them, with the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans</legacyLink>, <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">CommitTrans</legacyLink>, and <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">RollbackTrans</legacyLink> methods and the <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">Examine errors returned from the data source with the <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">Read the version from the ADO implementation used with the <legacyLink xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">Obtain schema information about your database with the <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src20" class="srcSentence">You can create <legacyBold>Connection</legacyBold> objects independently of any other previously defined object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">You can execute named commands or stored procedures as if they were native methods on a <legacyBold>Connection</legacyBold> object, as shown in the next section.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> When a named command has the same name as that of a stored procedure, invoke the "native method call" on a <legacyBold>Connection</legacyBold> object always execute the named command instead of the store procedure.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src23" class="srcSentence">Do not use this feature (calling a named command or stored procedure as if it were a native method on the <legacyBold>Connection</legacyBold> object) in a Microsoft® .NET Framework application, because the underlying implementation of the feature conflicts with the way the .NET Framework interoperates with COM.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Execute a command as a native method of a Connection object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">To execute a command, give the command a name using the <legacyBold>Command</legacyBold> object <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> Set the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object to the connection.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> Then issue a statement where the command name is used as if it were a method on the <legacyBold>Connection</legacyBold> object, followed by any parameters, and a <legacyBold>Recordset</legacyBold> object if any rows are returned.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> Set the <legacyBold>Recordset</legacyBold> properties to customize the resulting <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> For example:</caps:sentence>
          </para>
          <code>Dim cnn As New ADODB.Connection
Dim cmd As New ADODB.Command
Dim rst As New ADODB.Recordset
...
cnn.Open "..."
cmd.Name = "yourCommandName"
cmd.ActiveConnection = cnn
...
'Your command name, any parameters, and an optional Recordset.
cnn. "parameter", rst</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src30" class="srcSentence">Execute a stored procedure as a native method of a Connection object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src31" class="srcSentence">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the <legacyBold>Connection</legacyBold> object, followed by any parameters.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> ADO will make a "best guess" of parameter types.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> For example:</caps:sentence>
          </para>
          <code>Dim cnn As New ADODB.Connection
...
'Your stored procedure name and any parameters.
cnn. "parameter"</code>
          <para>
            <caps:sentence id="src34" class="srcSentence">The <legacyBold>Connection</legacyBold> object is safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src35" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">
                  <legacyLink xlink:href="f571b74d-b796-4009-9c66-6a36ab995a2a">Connection Object Properties, Methods, and Events</legacyLink>  </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Command Object (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a02c22fb-542d-465e-a629-30fd59dcbebf
caps.latest.revision: 6
caps.handback.revision: 6
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
# Command Object (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="95a3eebb27707a64fb63822ddf5211ca" id="tgt1" class="tgtSentence">Defines a specific command that you intend to execute against a data source.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="6d4ce7138689d467ea3a251333af6801" id="tgt2" class="tgtSentence">Use a <legacyBold>Command</legacyBold> object to query a database and return records in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, to execute a bulk operation, or to manipulate the structure of a database.</caps:sentence>
            <caps:sentence sentenceid="005b5962989aa35ef0c2d10dfb9d0f5b" id="tgt3" class="tgtSentence"> Depending on the functionality of the provider, some <legacyBold>Command</legacyBold> collections, methods, or properties may generate an error when they are referenced.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5b562d074c45bc5f1ae82696e44fe1d3" id="tgt4" class="tgtSentence">With the collections, methods, and properties of a <legacyBold>Command</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="5e4064fd891b6570b04338ced5f31934" id="tgt5" class="tgtSentence">Define the executable text of the command (for example, an SQL statement) with the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property.</caps:sentence>
                <caps:sentence sentenceid="f7bcabc040e95f7d21dcf165d4e5fcd6" id="tgt6" class="tgtSentence"> Alternatively, for command or query structures other than simple strings (for example, XML template queries) define the command with the <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8a8a78f092862847c85740d1f94ca040" id="tgt7" class="tgtSentence">Optionally, indicate the command dialect used in the <legacyBold>CommandText</legacyBold> or <legacyBold>CommandStream</legacyBold> with the <legacyLink xlink:href="329c3a71-ba88-4009-b04f-2f52195a5957">Dialect</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ce217f759c2c3f7423801a681aa8f35b" id="tgt8" class="tgtSentence">Define parameterized queries or stored-procedure arguments with <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> objects and the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="35c4ec2378496e27369ecc797e936e2b" id="tgt9" class="tgtSentence">Indicate whether parameter names should be passed to the provider with the <legacyLink xlink:href="42409387-026c-435f-a9b1-bf4167095875">NamedParameters</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="356c630d8dbcdc52ec14dc82e9a6f4cc" id="tgt10" class="tgtSentence">Execute a command and return a <legacyBold>Recordset</legacyBold> object if appropriate with the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1a6aa3b1b263f01fdc7ecbb32a352e0d" id="tgt11" class="tgtSentence">Specify the type of command with the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property prior to execution to optimize performance.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ec41f1a8ea1e3b22d0b11e4e28c6d864" id="tgt12" class="tgtSentence">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the <legacyLink xlink:href="11ca8825-765e-4bb4-a6ce-3f6564ad8755">Prepared</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b3979757ddd30e4edb8b1a2e51b0f70b" id="tgt13" class="tgtSentence">Set the number of seconds that a provider will wait for a command to execute with the <legacyLink xlink:href="c611f857-d6b0-4dca-8925-f4a02e769eb0">CommandTimeout</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="cb49fb465b0d4fcbea49aae12750d595" id="tgt14" class="tgtSentence">Associate an open connection with a <legacyBold>Command</legacyBold> object by setting its <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c00215bf03766875cb124b07444a4ccf" id="tgt15" class="tgtSentence">Set the <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property to identify the <legacyBold>Command</legacyBold> object as a method on the associated <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d3b4102f4edf6505af15f9494d5cfc9b" id="tgt16" class="tgtSentence">Pass a <legacyBold>Command</legacyBold> object to the <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> property of a <legacyBold>Recordset</legacyBold> to obtain data.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="bdde921a583fd9dfe9fadf24b13a7ca0" id="tgt17" class="tgtSentence">Access provider-specific attributes with the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="933664577497d71db23a8e30acec4fde" id="tgt18" class="tgtSentence">To execute a query without using a <legacyBold>Command</legacyBold> object, pass a query string to the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method of a <legacyBold>Connection</legacyBold> object or to the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method of a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              <caps:sentence sentenceid="5a6bc7413de18737e3bd6d36cf514725" id="tgt19" class="tgtSentence"> However, a <legacyBold>Command</legacyBold> object is required when you want to persist the command text and re-execute it, or use query parameters.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="efcb09e3a2061c48199545d8ce640cb8" id="tgt20" class="tgtSentence">To create a <legacyBold>Command</legacyBold> object independently of a previously defined <legacyBold>Connection</legacyBold> object, set its <legacyBold>ActiveConnection</legacyBold> property to a valid connection string.</caps:sentence>
            <caps:sentence sentenceid="64aca38d6edb93832bcca77039a4433a" id="tgt21" class="tgtSentence"> ADO still creates a <legacyBold>Connection</legacyBold> object, but it does not assign that object to an object variable.</caps:sentence>
            <caps:sentence sentenceid="86738e8a78238c0310b7337699bc6b49" id="tgt22" class="tgtSentence"> However, if you are associating multiple <legacyBold>Command</legacyBold> objects with the same connection, you should explicitly create and open a <legacyBold>Connection</legacyBold> object; this assigns the <legacyBold>Connection</legacyBold> object to an object variable.</caps:sentence>
            <caps:sentence sentenceid="637f15c32edc3249f8d586bcdb65cd94" id="tgt23" class="tgtSentence"> Make sure that the <legacyBold>Connection</legacyBold> object was opened successfully before you assign it to the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object, because assigning a closed <legacyBold>Connection</legacyBold> object causes an error.</caps:sentence>
            <caps:sentence sentenceid="01419767f77b2a8bf5722c47f839fc79" id="tgt24" class="tgtSentence"> If you do not set the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object to this object variable, ADO creates a new <legacyBold>Connection</legacyBold> object for each <legacyBold>Command</legacyBold> object, even if you use the same connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="76f9cdb0f34fd239336c0c89248fb0ec" id="tgt25" class="tgtSentence">To execute a <legacyBold>Command</legacyBold>, call it by its <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property on the associated <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="76b84c82416d42459f561e8642671ec5" id="tgt26" class="tgtSentence"> The <legacyBold>Command</legacyBold> must have its <legacyBold>ActiveConnection</legacyBold> property set to the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="a1df4093c3264db56dd1a7b2291b7341" id="tgt27" class="tgtSentence"> If the <legacyBold>Command</legacyBold> has parameters, pass their values as arguments to the method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dbe6846207b58173bd0c17b461a0b8a3" id="tgt28" class="tgtSentence">If two or more <legacyBold>Command</legacyBold> objects are executed on the same connection and either <legacyBold>Command</legacyBold> object is a stored procedure with output parameters, an error occurs.</caps:sentence>
            <caps:sentence sentenceid="260ad36b38ab5d453277bb387d5c6c6d" id="tgt29" class="tgtSentence"> To execute each <legacyBold>Command</legacyBold> object, use separate connections or disconnect all other <legacyBold>Command</legacyBold> objects from the connection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1eedb596fe78d599cbc41a5a0655a92e" id="tgt30" class="tgtSentence">The <legacyBold>Parameters</legacyBold> collection is the default member of the <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="eedc8983db3e1e2c44d428cf0eced41d" id="tgt31" class="tgtSentence"> As a result, the following two code statements are equivalent.</caps:sentence>
          </para>
          <code>objCmd.Parameters.Item(0)
objCmd(0)</code>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="0b16ea45b1b39b44d1b7939a20f7d6aa" id="tgt32" class="tgtSentence">The <legacyBold>Command</legacyBold> object is not safe for scripting.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt33" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f9f34ac78e7695e28a5ba9bc9a9cfa54" id="tgt34" class="tgtSentence">
                  <legacyLink xlink:href="0389f21c-06da-4090-9da1-28d912f888d7">Command Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Defines a specific command that you intend to execute against a data source.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Use a <legacyBold>Command</legacyBold> object to query a database and return records in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, to execute a bulk operation, or to manipulate the structure of a database.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Depending on the functionality of the provider, some <legacyBold>Command</legacyBold> collections, methods, or properties may generate an error when they are referenced.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">With the collections, methods, and properties of a <legacyBold>Command</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Define the executable text of the command (for example, an SQL statement) with the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> Alternatively, for command or query structures other than simple strings (for example, XML template queries) define the command with the <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Optionally, indicate the command dialect used in the <legacyBold>CommandText</legacyBold> or <legacyBold>CommandStream</legacyBold> with the <legacyLink xlink:href="329c3a71-ba88-4009-b04f-2f52195a5957">Dialect</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Define parameterized queries or stored-procedure arguments with <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> objects and the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Indicate whether parameter names should be passed to the provider with the <legacyLink xlink:href="42409387-026c-435f-a9b1-bf4167095875">NamedParameters</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Execute a command and return a <legacyBold>Recordset</legacyBold> object if appropriate with the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Specify the type of command with the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property prior to execution to optimize performance.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the <legacyLink xlink:href="11ca8825-765e-4bb4-a6ce-3f6564ad8755">Prepared</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Set the number of seconds that a provider will wait for a command to execute with the <legacyLink xlink:href="c611f857-d6b0-4dca-8925-f4a02e769eb0">CommandTimeout</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">Associate an open connection with a <legacyBold>Command</legacyBold> object by setting its <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">Set the <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property to identify the <legacyBold>Command</legacyBold> object as a method on the associated <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">Pass a <legacyBold>Command</legacyBold> object to the <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> property of a <legacyBold>Recordset</legacyBold> to obtain data.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">Access provider-specific attributes with the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src18" class="srcSentence">To execute a query without using a <legacyBold>Command</legacyBold> object, pass a query string to the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method of a <legacyBold>Connection</legacyBold> object or to the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method of a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              <caps:sentence id="src19" class="srcSentence"> However, a <legacyBold>Command</legacyBold> object is required when you want to persist the command text and re-execute it, or use query parameters.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src20" class="srcSentence">To create a <legacyBold>Command</legacyBold> object independently of a previously defined <legacyBold>Connection</legacyBold> object, set its <legacyBold>ActiveConnection</legacyBold> property to a valid connection string.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> ADO still creates a <legacyBold>Connection</legacyBold> object, but it does not assign that object to an object variable.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> However, if you are associating multiple <legacyBold>Command</legacyBold> objects with the same connection, you should explicitly create and open a <legacyBold>Connection</legacyBold> object; this assigns the <legacyBold>Connection</legacyBold> object to an object variable.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> Make sure that the <legacyBold>Connection</legacyBold> object was opened successfully before you assign it to the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object, because assigning a closed <legacyBold>Connection</legacyBold> object causes an error.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> If you do not set the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Command</legacyBold> object to this object variable, ADO creates a new <legacyBold>Connection</legacyBold> object for each <legacyBold>Command</legacyBold> object, even if you use the same connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">To execute a <legacyBold>Command</legacyBold>, call it by its <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property on the associated <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> The <legacyBold>Command</legacyBold> must have its <legacyBold>ActiveConnection</legacyBold> property set to the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> If the <legacyBold>Command</legacyBold> has parameters, pass their values as arguments to the method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">If two or more <legacyBold>Command</legacyBold> objects are executed on the same connection and either <legacyBold>Command</legacyBold> object is a stored procedure with output parameters, an error occurs.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> To execute each <legacyBold>Command</legacyBold> object, use separate connections or disconnect all other <legacyBold>Command</legacyBold> objects from the connection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src30" class="srcSentence">The <legacyBold>Parameters</legacyBold> collection is the default member of the <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> As a result, the following two code statements are equivalent.</caps:sentence>
          </para>
          <code>objCmd.Parameters.Item(0)
objCmd(0)</code>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src32" class="srcSentence">The <legacyBold>Command</legacyBold> object is not safe for scripting.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src33" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">
                  <legacyLink xlink:href="0389f21c-06da-4090-9da1-28d912f888d7">Command Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
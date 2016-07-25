---
title: "Microsoft OLE DB Remoting Provider (ADO Service Provider)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a4360ed4-b70f-4734-9041-4025d033346b
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
# Microsoft OLE DB Remoting Provider (ADO Service Provider)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="43abfb5c1ac5f6bb0e48489af63883a8" id="tgt1" class="tgtSentence">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine.</caps:sentence>
          <caps:sentence sentenceid="8d963c149ccf03e47e8da3cbcece4115" id="tgt2" class="tgtSentence"> Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine.</caps:sentence>
          <caps:sentence sentenceid="f78060e4587a5c8ea56d3ec8e9f2cfdf" id="tgt3" class="tgtSentence"> Then specify the parameters used by the Remoting Provider to access the remote machine.</caps:sentence>
          <caps:sentence sentenceid="b5c728db3557a35133cb51bbc96da6f6" id="tgt4" class="tgtSentence"> You can then access the remote machine as if you were a local user.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt5" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt6" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt7" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="20827e3adfa88537ab8adfa70f7ffa15" id="tgt8" class="tgtSentence"> Applications that use RDS should migrate to  <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="0975fcf10aa159131d858087aa78f2ce" id="tgt9" class="tgtSentence">Provider Keyword</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="563e1c1a9f17df7a7c004ae28437e866" id="tgt10" class="tgtSentence">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string.</caps:sentence>
            <caps:sentence sentenceid="8510a1fe30a1d9cf79898335d9ba627c" id="tgt11" class="tgtSentence"> (Note the blank space in the provider name.)</caps:sentence>
          </para>
          <code>"Provider=<codeFeaturedElement xmlns="">MS Remote</codeFeaturedElement>"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5e0bd6e0ba57237c2892877bf8cfd5c8" id="tgt12" class="tgtSentence">Additional Keywords</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d0524eb1a816cedfe69f71b83a77d289" id="tgt13" class="tgtSentence">When this service provider is invoked, the following additional keywords are relevant.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7df5b64df1181ef1d62d646a13aa860" id="tgt14" class="tgtSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt15" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5f0262ef78817e828a92d75e9749b4f9" id="tgt16" class="tgtSentence">Data Source</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fb1e58526223de1aba5463bbb7171188" id="tgt17" class="tgtSentence">Specifies the name of the remote data source.</caps:sentence>
                    <caps:sentence sentenceid="c416908e41987887a29b9a21c940cb9c" id="tgt18" class="tgtSentence"> It is passed to the OLE DB Remoting Provider for processing.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="8e92b29197b0c6527f3fe18dcb8de0a8" id="tgt19" class="tgtSentence">This keyword is equivalent to the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c9cc4b2425ec47fd6141efc88965a1d3" id="tgt20" class="tgtSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1eca934536f297438288ac2147734c6a" id="tgt21" class="tgtSentence">When this service provider is invoked, the following dynamic properties are added to the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcebf220c946d5172f9d79c5c958f905" id="tgt22" class="tgtSentence">Dynamic Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt23" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a21dac75e2a4ccf9e610f983d6ffb955" id="tgt24" class="tgtSentence">DFMode</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7e1309ee455f468c630dec5f0bb26c62" id="tgt25" class="tgtSentence">Indicates the DataFactory Mode.</caps:sentence>
                    <caps:sentence sentenceid="952a52cd34f6258100c290d98532a218" id="tgt26" class="tgtSentence"> A string that specifies the desired version of the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory</legacyLink> object on the server.</caps:sentence>
                    <caps:sentence sentenceid="06b9c72a98cc6964a4e938cc99dbb755" id="tgt27" class="tgtSentence"> Set this property before opening a connection to request a particular version of the <legacyBold>DataFactory</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="421b3678ea1117782ae1c0215cdd6825" id="tgt28" class="tgtSentence"> If the requested version is not available, an attempt will be made to use the preceding version.</caps:sentence>
                    <caps:sentence sentenceid="ebfb3b184e5a0f25f2f2636d1f46cb41" id="tgt29" class="tgtSentence"> If there is no preceding version, an error will occur.</caps:sentence>
                    <caps:sentence sentenceid="66062e781f5e921e230838ea193dacb9" id="tgt30" class="tgtSentence"> If <legacyBold>DFMode</legacyBold> is less than the available version, an error will occur.</caps:sentence>
                    <caps:sentence sentenceid="aaf844b0b90d61d4b640805f7f90e5d0" id="tgt31" class="tgtSentence"> This property is read-only after a connection is made.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="9bcb4e8c181d5f9bfc5a2cc493acf013" id="tgt32" class="tgtSentence">Can be one of the following valid string values:  </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="71ef0ef18b58246c06ef0732e16a15d5" id="tgt33" class="tgtSentence">"25"—Version 2.5 (Default)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6ed92a6c919f3542bf0861753e607fac" id="tgt34" class="tgtSentence">"21"—Version 2.1</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ce24d50e489bb213be5fb31042c09b32" id="tgt35" class="tgtSentence">"20"—Version 2.0</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87d8c505f176915fcc1c671bff8c2ff5" id="tgt36" class="tgtSentence">"15"—Version 1.5</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e4e369f074cb84bed25279c04477591d" id="tgt37" class="tgtSentence">Command Properties</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="839fa0a0915b24462de02e5b320fb053" id="tgt38" class="tgtSentence">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider.</caps:sentence>
                    <caps:sentence sentenceid="f5a2f2025f9140cab6b9da3fac823e41" id="tgt39" class="tgtSentence"> The default value for this string is vt_empty.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="8573195c3bc42f3cf70666a753aa0ed8" id="tgt40" class="tgtSentence">Current DFMode</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="727ce11080bc86bb8fdae2b926b9d444" id="tgt41" class="tgtSentence">Indicates the actual version number of the <legacyBold>DataFactory</legacyBold> on the server.</caps:sentence>
                    <caps:sentence sentenceid="fcb0c1b21cfd472be3c04b839c16d080" id="tgt42" class="tgtSentence"> Check this property to see if the version requested in the <legacyBold>DFMode</legacyBold> property was honored.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e59fb79011e124500e2cc83739e420a9" id="tgt43" class="tgtSentence">Can be one of the following valid Long integer values:  </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3971fc9fea30fb70a1f50235d1dec7b0" id="tgt44" class="tgtSentence">25—Version 2.5 (Default)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5300d5351d19c4663aa02301a0375013" id="tgt45" class="tgtSentence">21—Version 2.1</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="03e52a2667b532e92e9d8547ba66822d" id="tgt46" class="tgtSentence">20—Version 2.0</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ae384ed203883e42c8f4d60511bc3b99" id="tgt47" class="tgtSentence">15—Version 1.5</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="ca216cccd282391559a54ec28bad9668" id="tgt48" class="tgtSentence">Adding "DFMode=20;" to your connection string when using the <legacyBold>MSRemote</legacyBold> provider can improve your server's performance when updating data.</caps:sentence>
                    <caps:sentence sentenceid="18b9a197e48e7b61eb5a91ef217de984" id="tgt49" class="tgtSentence"> With this setting, the <legacyBold>RDSServer.DataFactory</legacyBold> object on the server uses a less resource-intensive mode.</caps:sentence>
                    <caps:sentence sentenceid="a8d2d8a6036ca2d0e7a5221adf6181a6" id="tgt50" class="tgtSentence"> However, the following features are not available in this configuration:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5c9f7f3542245e91e0db395d1fdb5eae" id="tgt51" class="tgtSentence">Using parameterized queries.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="117102df81d2bded3a9ae162e62aa6c0" id="tgt52" class="tgtSentence">Getting parameter or column information before calling the <legacyBold>Execute</legacyBold> method.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1f507aa841c38a31012b9cc0b34220ca" id="tgt53" class="tgtSentence">Setting <legacyBold>Transact Updates</legacyBold> to <languageKeyword>True</languageKeyword>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="031d7d000b8e534eb4018bd110d67344" id="tgt54" class="tgtSentence">Getting row status.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5a346f9a9a4b3d216073b924cc091dc3" id="tgt55" class="tgtSentence">Calling the <legacyBold>Resync</legacyBold> method.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b3e76da31ae4d8ef243ba7a3e63bd066" id="tgt56" class="tgtSentence">Refreshing (explicitly or automatically) via the <legacyBold>Update Resync</legacyBold> property.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6293ff597fb42e3603762ee00d462763" id="tgt57" class="tgtSentence">Setting <legacyBold>Command</legacyBold> or <legacyBold>Recordset</legacyBold> properties.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d95b7a520d43039239509737972ee3dd" id="tgt58" class="tgtSentence">Using <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="c1cbfe271a40788a00e8bf8574d94d4b" id="tgt59" class="tgtSentence">Handler</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c67e8fb8ac828918e9fb3b9db541eb8" id="tgt60" class="tgtSentence">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>, and any parameters used by the handler<legacyItalic>,</legacyItalic> all separated by commas (",").</caps:sentence>
                    <caps:sentence sentenceid="0bf737f922a2550be7b9ac9be10c7587" id="tgt61" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="ea3734c49b12da12dc4b9cf2c7e8c22b" id="tgt62" class="tgtSentence">Internet Timeout</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="162c7e953c5ea2614c9a739111cbceb8" id="tgt63" class="tgtSentence">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server.</caps:sentence>
                    <caps:sentence sentenceid="291686e1f36aee06e68b54714c26ab22" id="tgt64" class="tgtSentence"> (The default is 5 minutes.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3f6f09d4fdf9fa3c833a79563ff02c8d" id="tgt65" class="tgtSentence">Remote Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="edf9c46df556d3646e73f28091d4a0a4" id="tgt66" class="tgtSentence">Indicates the name of the data provider to be used on the remote server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="06ac6d07e043107f7c51dd4ed9cefef0" id="tgt67" class="tgtSentence">Remote Server</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3631d429ad1982f89adbaf5c22f07f88" id="tgt68" class="tgtSentence">Indicates the server name and communication protocol to be used by this connection.</caps:sentence>
                    <caps:sentence sentenceid="d60b6a304ed049db4072e1b4b7d4ca07" id="tgt69" class="tgtSentence"> This property is equivalent to the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataContro</legacyLink> object <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server</legacyLink> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="1a0a38e72a7aac219771909b5f7d97eb" id="tgt70" class="tgtSentence">Transact Updates</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f40fdacfff562109ae711a090e9178ec" id="tgt71" class="tgtSentence">When set to <languageKeyword>True</languageKeyword>, this value indicates that when <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> is performed on the server, it will be done inside a transaction.</caps:sentence>
                    <caps:sentence sentenceid="d5d71882a63a0c5e21b9326a0008e094" id="tgt72" class="tgtSentence"> The default value for this Boolean dynamic property is <languageKeyword>False</languageKeyword>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="05e097f723b833dad74247ad30b2acb6" id="tgt73" class="tgtSentence">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</caps:sentence>
            <caps:sentence sentenceid="b127952c937f0a51cf2966348247e893" id="tgt74" class="tgtSentence"> For example, set the <legacyBold>Internet Timeout</legacyBold> dynamic property to five seconds by specifying:</caps:sentence>
          </para>
          <code>Dim cn as New ADODB.Connection
cn.Open "Provider=MS Remote;Internet Timeout=5000"</code>
          <para>
            <caps:sentence sentenceid="44926feac656dcccb0a13dbff7ba3728" id="tgt75" class="tgtSentence">You may also set or retrieve a dynamic property by specifying its name as the index to the <legacyBold>Properties</legacyBold> property.</caps:sentence>
            <caps:sentence sentenceid="58e498a88253c77cd387ef41edca6a97" id="tgt76" class="tgtSentence"> The following example shows how to get and print the current value of the <legacyBold>Internet Timeout</legacyBold> dynamic property, and then set a new value:</caps:sentence>
          </para>
          <code>Debug.Print cn.Properties("Internet Timeout")
cn.Properties("Internet Timeout") = 5000</code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="20448d865970951930a625b64a801a3f" id="tgt77" class="tgtSentence">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the <legacyItalic>ActiveConnection</legacyItalic> parameter of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyBold>Open</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="06d413361d170f64a2605e795742860b" id="tgt78" class="tgtSentence"> Starting with ADO 2.1, the provider may also be specified in the <legacyItalic>ConnectionString </legacyItalic>parameter of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object <legacyBold>Open</legacyBold> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9bc4124c64baaeef71c8661cf036c14f" id="tgt79" class="tgtSentence">The equivalent of the <legacyBold>RDS.DataControl</legacyBold> object <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> property is not available.</caps:sentence>
            <caps:sentence sentenceid="9e8d29e3416b2c1543ed5070a9cb93f6" id="tgt80" class="tgtSentence"> The <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyBold>Open</legacyBold> method <legacyItalic>Source </legacyItalic>argument is used instead.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="11f3c2c0735d4c2613df7d028a1be97d" id="tgt81" class="tgtSentence">
              <embeddedLabel>Note</embeddedLabel>   Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.</caps:sentence>
            <caps:sentence sentenceid="cf7a7d00f9583845040170cae7060f99" id="tgt82" class="tgtSentence"> Scenarios beyond three tiers have not been tested and should not be needed.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <codeExample>
        <description>
          <content>
            <para>
              <caps:sentence sentenceid="5335057bab72abe2a2099b1c846df854" id="tgt83" class="tgtSentence">This example performs a query on the <legacyBold>Authors</legacyBold> table of the <legacyBold>Pubs</legacyBold> database on a server named <legacyItalic>YourServer</legacyItalic>.</caps:sentence>
              <caps:sentence sentenceid="267209cd87b3de9354ab8c8de1657057" id="tgt84" class="tgtSentence"> The names of the remote data source and remote server are provided in the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method of the<legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d"> Connection</legacyLink> object, and the SQL query is specified in the<legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d"> Open</legacyLink> method of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
              <caps:sentence sentenceid="9a6bd802b339fd6361c4734d3faf3d37" id="tgt85" class="tgtSentence"> A <legacyBold>Recordset</legacyBold> object is returned, edited, and used to update the data source.</caps:sentence>
            </para>
          </content>
        </description>
        <code>Dim rs as New ADODB.Recordset
Dim cn as New ADODB.Connection
cn.Open  "<codeFeaturedElement xmlns="">Provider</codeFeaturedElement>=MS Remote;<codeFeaturedElement xmlns="">Data Source</codeFeaturedElement>=pubs;" &amp; _
         "<codeFeaturedElement xmlns="">Remote Server</codeFeaturedElement>=http://YourServer"
rs.<codeFeaturedElement xmlns="">Open</codeFeaturedElement> "SELECT * FROM authors", cn
...                'Edit the recordset
rs.<codeFeaturedElement xmlns="">UpdateBatch</codeFeaturedElement>     'Equivalent of RDS <codeFeaturedElement xmlns="">SubmitChanges</codeFeaturedElement>
...</code>
      </codeExample>
      <relatedTopics>
        <legacyLink xlink:href="4083b72f-68c4-4252-b366-abb70db5ca2b">
          <caps:sentence sentenceid="28d493f55a9a6fef4e4e76cd990756f5" id="tgt86" class="tgtSentence">Overview of the OLE DB Remoting Provider</caps:sentence>
        </legacyLink>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Then specify the parameters used by the Remoting Provider to access the remote machine.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> You can then access the remote machine as if you were a local user.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src5" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Applications that use RDS should migrate to  <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Provider Keyword</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> (Note the blank space in the provider name.)</caps:sentence>
          </para>
          <code>"Provider=<codeFeaturedElement xmlns="">MS Remote</codeFeaturedElement>"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Additional Keywords</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">When this service provider is invoked, the following additional keywords are relevant.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src16" class="srcSentence">Data Source</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Specifies the name of the remote data source.</caps:sentence>
                    <caps:sentence id="src18" class="srcSentence"> It is passed to the OLE DB Remoting Provider for processing.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">This keyword is equivalent to the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">When this service provider is invoked, the following dynamic properties are added to the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Dynamic Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src24" class="srcSentence">DFMode</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Indicates the DataFactory Mode.</caps:sentence>
                    <caps:sentence id="src26" class="srcSentence"> A string that specifies the desired version of the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory</legacyLink> object on the server.</caps:sentence>
                    <caps:sentence id="src27" class="srcSentence"> Set this property before opening a connection to request a particular version of the <legacyBold>DataFactory</legacyBold>.</caps:sentence>
                    <caps:sentence id="src28" class="srcSentence"> If the requested version is not available, an attempt will be made to use the preceding version.</caps:sentence>
                    <caps:sentence id="src29" class="srcSentence"> If there is no preceding version, an error will occur.</caps:sentence>
                    <caps:sentence id="src30" class="srcSentence"> If <legacyBold>DFMode</legacyBold> is less than the available version, an error will occur.</caps:sentence>
                    <caps:sentence id="src31" class="srcSentence"> This property is read-only after a connection is made.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Can be one of the following valid string values:  </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">"25"—Version 2.5 (Default)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">"21"—Version 2.1</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">"20"—Version 2.0</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">"15"—Version 1.5</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src37" class="srcSentence">Command Properties</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider.</caps:sentence>
                    <caps:sentence id="src39" class="srcSentence"> The default value for this string is vt_empty.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src40" class="srcSentence">Current DFMode</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Indicates the actual version number of the <legacyBold>DataFactory</legacyBold> on the server.</caps:sentence>
                    <caps:sentence id="src42" class="srcSentence"> Check this property to see if the version requested in the <legacyBold>DFMode</legacyBold> property was honored.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Can be one of the following valid Long integer values:  </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">25—Version 2.5 (Default)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">21—Version 2.1</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">20—Version 2.0</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">15—Version 1.5</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Adding "DFMode=20;" to your connection string when using the <legacyBold>MSRemote</legacyBold> provider can improve your server's performance when updating data.</caps:sentence>
                    <caps:sentence id="src49" class="srcSentence"> With this setting, the <legacyBold>RDSServer.DataFactory</legacyBold> object on the server uses a less resource-intensive mode.</caps:sentence>
                    <caps:sentence id="src50" class="srcSentence"> However, the following features are not available in this configuration:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Using parameterized queries.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Getting parameter or column information before calling the <legacyBold>Execute</legacyBold> method.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Setting <legacyBold>Transact Updates</legacyBold> to <languageKeyword>True</languageKeyword>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Getting row status.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src55" class="srcSentence">Calling the <legacyBold>Resync</legacyBold> method.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">Refreshing (explicitly or automatically) via the <legacyBold>Update Resync</legacyBold> property.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">Setting <legacyBold>Command</legacyBold> or <legacyBold>Recordset</legacyBold> properties.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Using <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src59" class="srcSentence">Handler</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>, and any parameters used by the handler<legacyItalic>,</legacyItalic> all separated by commas (",").</caps:sentence>
                    <caps:sentence id="src61" class="srcSentence"> A <languageKeyword>String</languageKeyword> value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src62" class="srcSentence">Internet Timeout</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server.</caps:sentence>
                    <caps:sentence id="src64" class="srcSentence"> (The default is 5 minutes.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src65" class="srcSentence">Remote Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">Indicates the name of the data provider to be used on the remote server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src67" class="srcSentence">Remote Server</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">Indicates the server name and communication protocol to be used by this connection.</caps:sentence>
                    <caps:sentence id="src69" class="srcSentence"> This property is equivalent to the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataContro</legacyLink> object <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server</legacyLink> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src70" class="srcSentence">Transact Updates</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">When set to <languageKeyword>True</languageKeyword>, this value indicates that when <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> is performed on the server, it will be done inside a transaction.</caps:sentence>
                    <caps:sentence id="src72" class="srcSentence"> The default value for this Boolean dynamic property is <languageKeyword>False</languageKeyword>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src73" class="srcSentence">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</caps:sentence>
            <caps:sentence id="src74" class="srcSentence"> For example, set the <legacyBold>Internet Timeout</legacyBold> dynamic property to five seconds by specifying:</caps:sentence>
          </para>
          <code>Dim cn as New ADODB.Connection
cn.Open "Provider=MS Remote;Internet Timeout=5000"</code>
          <para>
            <caps:sentence id="src75" class="srcSentence">You may also set or retrieve a dynamic property by specifying its name as the index to the <legacyBold>Properties</legacyBold> property.</caps:sentence>
            <caps:sentence id="src76" class="srcSentence"> The following example shows how to get and print the current value of the <legacyBold>Internet Timeout</legacyBold> dynamic property, and then set a new value:</caps:sentence>
          </para>
          <code>Debug.Print cn.Properties("Internet Timeout")
cn.Properties("Internet Timeout") = 5000</code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src77" class="srcSentence">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the <legacyItalic>ActiveConnection</legacyItalic> parameter of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyBold>Open</legacyBold> method.</caps:sentence>
            <caps:sentence id="src78" class="srcSentence"> Starting with ADO 2.1, the provider may also be specified in the <legacyItalic>ConnectionString </legacyItalic>parameter of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object <legacyBold>Open</legacyBold> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src79" class="srcSentence">The equivalent of the <legacyBold>RDS.DataControl</legacyBold> object <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> property is not available.</caps:sentence>
            <caps:sentence id="src80" class="srcSentence"> The <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyBold>Open</legacyBold> method <legacyItalic>Source </legacyItalic>argument is used instead.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src81" class="srcSentence">
              <embeddedLabel>Note</embeddedLabel>   Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.</caps:sentence>
            <caps:sentence id="src82" class="srcSentence"> Scenarios beyond three tiers have not been tested and should not be needed.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <codeExample>
        <description>
          <content>
            <para>
              <caps:sentence id="src83" class="srcSentence">This example performs a query on the <legacyBold>Authors</legacyBold> table of the <legacyBold>Pubs</legacyBold> database on a server named <legacyItalic>YourServer</legacyItalic>.</caps:sentence>
              <caps:sentence id="src84" class="srcSentence"> The names of the remote data source and remote server are provided in the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method of the<legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d"> Connection</legacyLink> object, and the SQL query is specified in the<legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d"> Open</legacyLink> method of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
              <caps:sentence id="src85" class="srcSentence"> A <legacyBold>Recordset</legacyBold> object is returned, edited, and used to update the data source.</caps:sentence>
            </para>
          </content>
        </description>
        <code>Dim rs as New ADODB.Recordset
Dim cn as New ADODB.Connection
cn.Open  "<codeFeaturedElement xmlns="">Provider</codeFeaturedElement>=MS Remote;<codeFeaturedElement xmlns="">Data Source</codeFeaturedElement>=pubs;" &amp; _
         "<codeFeaturedElement xmlns="">Remote Server</codeFeaturedElement>=http://YourServer"
rs.<codeFeaturedElement xmlns="">Open</codeFeaturedElement> "SELECT * FROM authors", cn
...                'Edit the recordset
rs.<codeFeaturedElement xmlns="">UpdateBatch</codeFeaturedElement>     'Equivalent of RDS <codeFeaturedElement xmlns="">SubmitChanges</codeFeaturedElement>
...</code>
      </codeExample>
      <relatedTopics>
        <legacyLink xlink:href="4083b72f-68c4-4252-b366-abb70db5ca2b">
          <caps:sentence id="src86" class="srcSentence">Overview of the OLE DB Remoting Provider</caps:sentence>
        </legacyLink>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
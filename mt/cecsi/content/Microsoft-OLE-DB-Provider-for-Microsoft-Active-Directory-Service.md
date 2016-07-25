---
title: "Microsoft OLE DB Provider for Microsoft Active Directory Service"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f9e81452-5675-4cfc-9949-cfbd2fe57534
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
# Microsoft OLE DB Provider for Microsoft Active Directory Service
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="de72153fcc40211772f12cfc92421fc7" id="tgt1" class="tgtSentence">The Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI.</caps:sentence>
          <caps:sentence sentenceid="5c70d03b0ee3967ab39000113dcfbdb2" id="tgt2" class="tgtSentence"> This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services.</caps:sentence>
          <caps:sentence sentenceid="39b45bcc5842547bfaceea80d4844c13" id="tgt3" class="tgtSentence"> ADSI itself is based on a provider model, so that if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly.</caps:sentence>
          <caps:sentence sentenceid="957200d6ac261067363efe2712cc9e60" id="tgt4" class="tgtSentence"> The ADSI provider is free-threaded and Unicode enabled.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="df209e37fa6496886af7a164ca15b629" id="tgt5" class="tgtSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d7d007f559a3125dcff85785bd6f6ccf" id="tgt6" class="tgtSentence">To connect to this provider, set the <legacyBold>Provider</legacyBold> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to the following:</caps:sentence>
          </para>
          <code>ADSDSOObject</code>
          <para>
            <caps:sentence sentenceid="248709408787db043727f63ce324962e" id="tgt7" class="tgtSentence">Reading the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property will return this string as well.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5cf5a4267aa499f9dca0d6e5a90731cb" id="tgt8" class="tgtSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8e7c992911b83e02cbdeee3d0d221aae" id="tgt9" class="tgtSentence">A typical connection string for this provider is as follows:</caps:sentence>
          </para>
          <code>"Provider=ADSDSOObject;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence sentenceid="44800748b36dd3eb967f88d17e2d260d" id="tgt10" class="tgtSentence">The string consists of the following keywords.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7df5b64df1181ef1d62d646a13aa860" id="tgt11" class="tgtSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt12" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9e9f3d70bd8c8957627eada96d967706" id="tgt13" class="tgtSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dd061336d5c2ce799d9ef056817205e7" id="tgt14" class="tgtSentence">Specifies the OLE DB Provider for Active Directory Service.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3bd756a1167a9bff574b512092d53350" id="tgt15" class="tgtSentence">User ID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="894ae1122beff71d90c743328e91d2dd" id="tgt16" class="tgtSentence">Specifies the user name.</caps:sentence>
                    <caps:sentence sentenceid="ebed1f161254d63c26866a4e2e425e02" id="tgt17" class="tgtSentence"> If this keyword is omitted, the current logon is used.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5f4dcc3b5aa765d61d8327deb882cf99" id="tgt18" class="tgtSentence">Password</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4df08222df3dae489cac77da63d403c" id="tgt19" class="tgtSentence">Specifies the user password.</caps:sentence>
                    <caps:sentence sentenceid="ed391dc9d82219d4eec9d7d1f71841cc" id="tgt20" class="tgtSentence"> If this keyword is omitted.</caps:sentence>
                    <caps:sentence sentenceid="c39690339e8f9b8b16d1da702296db78" id="tgt21" class="tgtSentence"> Then the current logon is used.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d4e879422e89d3713c1c025017b59b61" id="tgt22" class="tgtSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <languageKeyword>Trusted_Connection=yes</languageKeyword> or <languageKeyword>Integrated Security = SSPI</languageKeyword> instead of user ID and password information in the connection string.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="6100c52dada9c46bce92964c9f051df5" id="tgt23" class="tgtSentence">Command Text</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="41c9b48cdc409ec5b326c4dd7a1ab733" id="tgt24" class="tgtSentence">A four-part command text string is recognized by the provider in the following syntax:</caps:sentence>
          </para>
          <code>"Root; Filter; Attributes[; Scope]"</code>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt25" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt26" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence sentenceid="63a9f0ea7bb98050796b649e85481845" id="tgt27" class="tgtSentence">Root</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4f1a17e775b694fb621ffbac3fbaee39" id="tgt28" class="tgtSentence">Indicates the <legacyBold>ADsPath</legacyBold> object from which to start the search (that is, the root of the search).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence sentenceid="b2c97ae425dd751b0e48a3acae79cf4a" id="tgt29" class="tgtSentence">Filter</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fb0565cb23cea06ab196e51683e7133a" id="tgt30" class="tgtSentence">Indicates the search filter in the RFC 1960 format.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence sentenceid="736b91750e516139acc13c5eb6564f92" id="tgt31" class="tgtSentence">Attributes</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cdab45801aee23acbd14e750cb29ce4f" id="tgt32" class="tgtSentence">Indicates a comma-delimited list of attributes to be returned.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence sentenceid="31a1fd140be4bef2d11e121ec9a18a58" id="tgt33" class="tgtSentence">Scope</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt34" class="tgtSentence">Optional.</caps:sentence>
                    <caps:sentence sentenceid="169d85f5b25ae21528d95cfc8bb08b9f" id="tgt35" class="tgtSentence"> A <legacyBold>String</legacyBold> that specifies the scope of the search.</caps:sentence>
                    <caps:sentence sentenceid="9a737624959a8013208270cdd73ceef4" id="tgt36" class="tgtSentence"> Can be one of the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="89889295fdc3f9f60148569bcff50a4e" id="tgt37" class="tgtSentence">Base — Search only the base object (root of the search).</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b62fa79d86bb2f6a82c3da0aa7778600" id="tgt38" class="tgtSentence">OneLevel — Search only one level.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5673986497d6d3fd63bd1d96ad296c2d" id="tgt39" class="tgtSentence">Subtree — Search the whole subtree.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="fa3a10105c9b5660cbdf9bbc8079647f" id="tgt40" class="tgtSentence">For example:</caps:sentence>
          </para>
          <code>"&lt;LDAP://DC=ArcadiaBay,DC=COM&gt;;(objectClass=*);sn, givenName; subtree"</code>
          <para>
            <caps:sentence sentenceid="7e176ec004e73d9a171fafbf73560961" id="tgt41" class="tgtSentence">The provider also supports SQL SELECT for command text.</caps:sentence>
            <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt42" class="tgtSentence"> For example:</caps:sentence>
          </para>
          <code>"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'"</code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="06750a77c9cd3d870780a79548a50241" id="tgt43" class="tgtSentence">The provider does not accept stored procedure calls or simple table names (for example, the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property will always be <legacyBold>adCmdText</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="d854412c4bfa830a37bbc7091f02a8e2" id="tgt44" class="tgtSentence"> See the Active Directory Service Interfaces documentation for a more thorough description of the command text elements.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="002c1a21d972a03f6b6e5a266dd56653" id="tgt45" class="tgtSentence">Recordset Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e81ac9293e309239f305e4959cb3ca87" id="tgt46" class="tgtSentence">The following tables list the features available on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object opened by using this provider.</caps:sentence>
            <caps:sentence sentenceid="dcc8c5202ba1acbc6880de9f8a79b61b" id="tgt47" class="tgtSentence"> Only the static cursor type (<legacyBold>adOpenStatic</legacyBold>) is available.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="20ae87d89e3db6f3665deb61bbc2988c" id="tgt48" class="tgtSentence">For more information about <legacyBold>Recordset</legacyBold> behavior for your provider configuration, run the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method and enumerate the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of the <legacyBold>Recordset</legacyBold> to determine whether provider-specific dynamic properties are present.</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="706c78c8723f08e3461a9df98c4f9c9a" id="tgt49" class="tgtSentence">Availability of standard ADO Recordset properties:</caps:sentence>
            </embeddedLabel>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a8db4c996d8ed8289da5f957879ab94" id="tgt50" class="tgtSentence">Property</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f24431ce9f1b8885678b1ed611c4c214" id="tgt51" class="tgtSentence">Availability</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">
                      <caps:sentence sentenceid="2ecac8e7ef8b3884f4acf3190b2f0593" id="tgt52" class="tgtSentence">AbsolutePage</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt53" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">
                      <caps:sentence sentenceid="764a8561e40975325fb7bdcd8e66ce21" id="tgt54" class="tgtSentence">AbsolutePosition</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt55" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">
                      <caps:sentence sentenceid="736b2ee4856989f60b05c8ede807ff4f" id="tgt56" class="tgtSentence">ActiveConnection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt57" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">
                      <caps:sentence sentenceid="c9a3639b57c741dcd0334c28032e4280" id="tgt58" class="tgtSentence">BOF</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt59" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">
                      <caps:sentence sentenceid="fad9383ed4698856ed467fd49ecf4820" id="tgt60" class="tgtSentence">Bookmark</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt61" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">
                      <caps:sentence sentenceid="aee9ee3f775b6b5a790c444f68628b29" id="tgt62" class="tgtSentence">CacheSize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt63" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">
                      <caps:sentence sentenceid="ed2f88c61dd3d03f1ef6781f26d23e41" id="tgt64" class="tgtSentence">CursorLocation</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c0c0d8286aafb8ec8c54b16e860474d8" id="tgt65" class="tgtSentence">always <legacyBold>adUseServer</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">
                      <caps:sentence sentenceid="1cd5476188fe9c7cac9cc2ebcd2fb87a" id="tgt66" class="tgtSentence">CursorType</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="53278d396dc31e6b09f774fec91dc602" id="tgt67" class="tgtSentence">always <legacyBold>adOpenStatic</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">
                      <caps:sentence sentenceid="c3bd55f87129536ac1698eb00596ceb3" id="tgt68" class="tgtSentence">EditMode</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a8dbeccb6df009028c9e77ef50904920" id="tgt69" class="tgtSentence">always <legacyBold>adEditNone</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">
                      <caps:sentence sentenceid="2e51b1ab42e8a4a67f3445174be5191b" id="tgt70" class="tgtSentence">EOF</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt71" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">
                      <caps:sentence sentenceid="b2c97ae425dd751b0e48a3acae79cf4a" id="tgt72" class="tgtSentence">Filter</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt73" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">
                      <caps:sentence sentenceid="c2edea50ed670a7360991f97066b85ff" id="tgt74" class="tgtSentence">LockType</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt75" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">
                      <caps:sentence sentenceid="3b38b73230230562600faa0c7a4ae19a" id="tgt76" class="tgtSentence">MarshalOptions</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt77" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="20c76571-8c9a-482c-a99e-726ab1d93f8b">
                      <caps:sentence sentenceid="e8a190f33755a6a8fda424e1fe9f4255" id="tgt78" class="tgtSentence">MaxRecords</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt79" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">
                      <caps:sentence sentenceid="cf65c05c144f7132e7bd231b8a2b5ace" id="tgt80" class="tgtSentence">PageCount</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt81" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">
                      <caps:sentence sentenceid="7525d528a3457f0227997c25239c4507" id="tgt82" class="tgtSentence">PageSize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt83" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">
                      <caps:sentence sentenceid="3d21c0cd334398e6a80b987f79424c5a" id="tgt84" class="tgtSentence">RecordCount</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt85" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">
                      <caps:sentence sentenceid="36cd38f49b9afa08222c0dc9ebfe35eb" id="tgt86" class="tgtSentence">Source</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt87" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">
                      <caps:sentence sentenceid="9ed39e2ea931586b6a985a6942ef573e" id="tgt88" class="tgtSentence">State</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt89" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">
                      <caps:sentence sentenceid="9acb44549b41563697bb490144ec6258" id="tgt90" class="tgtSentence">Status</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt91" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="10e2c207f699d6be906027fdcdd722db" id="tgt92" class="tgtSentence">Availability of standard ADO Recordset methods:</caps:sentence>
            </embeddedLabel>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ea9f6aca279138c58f705c8d4cb4b8ce" id="tgt93" class="tgtSentence">Method</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2f1d62cf9a34dfc798c4242c77a0e113" id="tgt94" class="tgtSentence">Available?</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">
                      <caps:sentence sentenceid="2a99922bd3fcc215a7b3fcbd9667338a" id="tgt95" class="tgtSentence">AddNew</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt96" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">
                      <caps:sentence sentenceid="10aec35353f9c4096a71c38654c3d402" id="tgt97" class="tgtSentence">Cancel</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt98" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">
                      <caps:sentence sentenceid="ecb488ca7118773aa90cb428ed21379b" id="tgt99" class="tgtSentence">CancelBatch</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt100" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">
                      <caps:sentence sentenceid="07e957a04a9b08eadc8537a17615e387" id="tgt101" class="tgtSentence">CancelUpdate</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt102" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">
                      <caps:sentence sentenceid="d329fd777726c300d7a044e482b967e7" id="tgt103" class="tgtSentence">Clone</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt104" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">
                      <caps:sentence sentenceid="716f6b30598ba30945d84485e61c1027" id="tgt105" class="tgtSentence">Close</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt106" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">
                      <caps:sentence sentenceid="099af53f601532dbd31e0ea99ffdeb64" id="tgt107" class="tgtSentence">Delete</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt108" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="14b92860-4171-47d9-a413-dd60dd6a8880">
                      <caps:sentence sentenceid="d1b51a6e50f7a6a0f9879ebf15f2651d" id="tgt109" class="tgtSentence">GetRows</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt110" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">
                      <caps:sentence sentenceid="3734a903022249b3010be1897042568e" id="tgt111" class="tgtSentence">Move</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt112" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence sentenceid="50f8d4d3e73a87f26463b77a35f46c37" id="tgt113" class="tgtSentence">MoveFirst</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt114" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence sentenceid="aa4486cbb251418b54bf37a38e07877d" id="tgt115" class="tgtSentence">MoveLast</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt116" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence sentenceid="2651169204622cb80ec4b28ac12285ac" id="tgt117" class="tgtSentence">MoveNext</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt118" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence sentenceid="95caad3d8a11cee1b9d2914ef1e9667e" id="tgt119" class="tgtSentence">MovePrevious</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt120" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">
                      <caps:sentence sentenceid="1e8095fae1cbe555ea131424ef67f608" id="tgt121" class="tgtSentence">NextRecordset</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt122" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">
                      <caps:sentence sentenceid="7cef8a734855777c2a9d0caf42666e69" id="tgt123" class="tgtSentence">Open</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt124" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">
                      <caps:sentence sentenceid="65d807e47b5cdafc34fc06e6d25cafd6" id="tgt125" class="tgtSentence">Requery</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt126" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">
                      <caps:sentence sentenceid="e365ce2f3002afe909c5591eb5c69889" id="tgt127" class="tgtSentence">Resync</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt128" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">
                      <caps:sentence sentenceid="72225dfc0ffc1c4e8471c5824c2c63c2" id="tgt129" class="tgtSentence">Supports</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt130" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">
                      <caps:sentence sentenceid="3ac340832f29c11538fbe2d6f75e8bcc" id="tgt131" class="tgtSentence">Update</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt132" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">
                      <caps:sentence sentenceid="f4651adedf889c8f0a0b0e38a2ee96fa" id="tgt133" class="tgtSentence">UpdateBatch</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt134" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="09a3a897a45e45a92900aac482a1dc49" id="tgt135" class="tgtSentence">For more information about ADSI and the specifics of the provider, refer to the Active Directory Service Interfaces documentation or visit the ADSI Web page.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType Property</link>
        <link xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString Property</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> ADSI itself is based on a provider model, so that if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The ADSI provider is free-threaded and Unicode enabled.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">To connect to this provider, set the <legacyBold>Provider</legacyBold> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to the following:</caps:sentence>
          </para>
          <code>ADSDSOObject</code>
          <para>
            <caps:sentence id="src7" class="srcSentence">Reading the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property will return this string as well.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">A typical connection string for this provider is as follows:</caps:sentence>
          </para>
          <code>"Provider=ADSDSOObject;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence id="src10" class="srcSentence">The string consists of the following keywords.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src13" class="srcSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Specifies the OLE DB Provider for Active Directory Service.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src15" class="srcSentence">User ID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Specifies the user name.</caps:sentence>
                    <caps:sentence id="src17" class="srcSentence"> If this keyword is omitted, the current logon is used.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src18" class="srcSentence">Password</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Specifies the user password.</caps:sentence>
                    <caps:sentence id="src20" class="srcSentence"> If this keyword is omitted.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> Then the current logon is used.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence id="src22" class="srcSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <languageKeyword>Trusted_Connection=yes</languageKeyword> or <languageKeyword>Integrated Security = SSPI</languageKeyword> instead of user ID and password information in the connection string.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">Command Text</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src24" class="srcSentence">A four-part command text string is recognized by the provider in the following syntax:</caps:sentence>
          </para>
          <code>"Root; Filter; Attributes[; Scope]"</code>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence id="src27" class="srcSentence">Root</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Indicates the <legacyBold>ADsPath</legacyBold> object from which to start the search (that is, the root of the search).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence id="src29" class="srcSentence">Filter</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Indicates the search filter in the RFC 1960 format.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence id="src31" class="srcSentence">Attributes</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Indicates a comma-delimited list of attributes to be returned.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyItalic>
                      <caps:sentence id="src33" class="srcSentence">Scope</caps:sentence>
                    </legacyItalic>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Optional.</caps:sentence>
                    <caps:sentence id="src35" class="srcSentence"> A <legacyBold>String</legacyBold> that specifies the scope of the search.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> Can be one of the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">Base — Search only the base object (root of the search).</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">OneLevel — Search only one level.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src39" class="srcSentence">Subtree — Search the whole subtree.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src40" class="srcSentence">For example:</caps:sentence>
          </para>
          <code>"&lt;LDAP://DC=ArcadiaBay,DC=COM&gt;;(objectClass=*);sn, givenName; subtree"</code>
          <para>
            <caps:sentence id="src41" class="srcSentence">The provider also supports SQL SELECT for command text.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> For example:</caps:sentence>
          </para>
          <code>"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'"</code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src43" class="srcSentence">The provider does not accept stored procedure calls or simple table names (for example, the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property will always be <legacyBold>adCmdText</legacyBold>).</caps:sentence>
            <caps:sentence id="src44" class="srcSentence"> See the Active Directory Service Interfaces documentation for a more thorough description of the command text elements.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src45" class="srcSentence">Recordset Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src46" class="srcSentence">The following tables list the features available on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object opened by using this provider.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> Only the static cursor type (<legacyBold>adOpenStatic</legacyBold>) is available.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src48" class="srcSentence">For more information about <legacyBold>Recordset</legacyBold> behavior for your provider configuration, run the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method and enumerate the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of the <legacyBold>Recordset</legacyBold> to determine whether provider-specific dynamic properties are present.</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence id="src49" class="srcSentence">Availability of standard ADO Recordset properties:</caps:sentence>
            </embeddedLabel>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Property</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Availability</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">
                      <caps:sentence id="src52" class="srcSentence">AbsolutePage</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">
                      <caps:sentence id="src54" class="srcSentence">AbsolutePosition</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">
                      <caps:sentence id="src56" class="srcSentence">ActiveConnection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">
                      <caps:sentence id="src58" class="srcSentence">BOF</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">
                      <caps:sentence id="src60" class="srcSentence">Bookmark</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">
                      <caps:sentence id="src62" class="srcSentence">CacheSize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">
                      <caps:sentence id="src64" class="srcSentence">CursorLocation</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">always <legacyBold>adUseServer</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">
                      <caps:sentence id="src66" class="srcSentence">CursorType</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">always <legacyBold>adOpenStatic</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">
                      <caps:sentence id="src68" class="srcSentence">EditMode</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">always <legacyBold>adEditNone</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">
                      <caps:sentence id="src70" class="srcSentence">EOF</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">
                      <caps:sentence id="src72" class="srcSentence">Filter</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">
                      <caps:sentence id="src74" class="srcSentence">LockType</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">
                      <caps:sentence id="src76" class="srcSentence">MarshalOptions</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="20c76571-8c9a-482c-a99e-726ab1d93f8b">
                      <caps:sentence id="src78" class="srcSentence">MaxRecords</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">
                      <caps:sentence id="src80" class="srcSentence">PageCount</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">
                      <caps:sentence id="src82" class="srcSentence">PageSize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">
                      <caps:sentence id="src84" class="srcSentence">RecordCount</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">
                      <caps:sentence id="src86" class="srcSentence">Source</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">
                      <caps:sentence id="src88" class="srcSentence">State</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">
                      <caps:sentence id="src90" class="srcSentence">Status</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <embeddedLabel>
              <caps:sentence id="src92" class="srcSentence">Availability of standard ADO Recordset methods:</caps:sentence>
            </embeddedLabel>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">Method</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">Available?</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">
                      <caps:sentence id="src95" class="srcSentence">AddNew</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">
                      <caps:sentence id="src97" class="srcSentence">Cancel</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">
                      <caps:sentence id="src99" class="srcSentence">CancelBatch</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">
                      <caps:sentence id="src101" class="srcSentence">CancelUpdate</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">
                      <caps:sentence id="src103" class="srcSentence">Clone</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">
                      <caps:sentence id="src105" class="srcSentence">Close</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">
                      <caps:sentence id="src107" class="srcSentence">Delete</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="14b92860-4171-47d9-a413-dd60dd6a8880">
                      <caps:sentence id="src109" class="srcSentence">GetRows</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">
                      <caps:sentence id="src111" class="srcSentence">Move</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence id="src113" class="srcSentence">MoveFirst</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence id="src115" class="srcSentence">MoveLast</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence id="src117" class="srcSentence">MoveNext</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence id="src119" class="srcSentence">MovePrevious</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">
                      <caps:sentence id="src121" class="srcSentence">NextRecordset</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src122" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">
                      <caps:sentence id="src123" class="srcSentence">Open</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">
                      <caps:sentence id="src125" class="srcSentence">Requery</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">
                      <caps:sentence id="src127" class="srcSentence">Resync</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">
                      <caps:sentence id="src129" class="srcSentence">Supports</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">
                      <caps:sentence id="src131" class="srcSentence">Update</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">
                      <caps:sentence id="src133" class="srcSentence">UpdateBatch</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src135" class="srcSentence">For more information about ADSI and the specifics of the provider, refer to the Active Directory Service Interfaces documentation or visit the ADSI Web page.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType Property</link>
        <link xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString Property</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
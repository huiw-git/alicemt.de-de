---
title: "Appendix A: Providers"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e2581b47-b11e-4e1e-b96c-d39c77c5b48a
caps.latest.revision: 13
caps.handback.revision: 13
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
# Appendix A: Providers
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="061624f749740a91ce01ac7d49f06b06" id="tgt1" class="tgtSentence">This section addresses three kinds of providers: data providers, service providers, and service components.</caps:sentence>
          <caps:sentence sentenceid="6b718fc66dbe2f73143c8982b7a556fa" id="tgt2" class="tgtSentence"> Providers fall into two categories: those providing data and those providing services.</caps:sentence>
          <caps:sentence sentenceid="3c1ebd8e850dc4505108765f938e2862" id="tgt3" class="tgtSentence"> A <legacyItalic>data provider</legacyItalic> owns its own data and exposes it in tabular form to your application.</caps:sentence>
          <caps:sentence sentenceid="01990f2860e903f3179eafb31ffa86d4" id="tgt4" class="tgtSentence"> A <legacyItalic>service provider</legacyItalic> encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</caps:sentence>
          <caps:sentence sentenceid="f09e23ccab9ca4aebb9e375ad324af58" id="tgt5" class="tgtSentence"> A service provider may also be further defined as a <legacyItalic>service component</legacyItalic>, which must work together with other service providers or components.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="f6f22c14bb05a9db6a0098977b72a3a2" id="tgt6" class="tgtSentence">Data Providers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d2638bda42a636fb755519f765d4bf4b" id="tgt7" class="tgtSentence">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="15ccfd7880f61fcc63429722dda87fbb" id="tgt8" class="tgtSentence">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider.</caps:sentence>
            <caps:sentence sentenceid="6a739385082191b91a2497b963287c9b" id="tgt9" class="tgtSentence"> The differences usually fall into one of three categories:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1e08e819c33d6e2e7e1af931b4b0541f" id="tgt10" class="tgtSentence">Connection parameters in the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="07a1d8db37ffb1baf997548cccaeb81e" id="tgt11" class="tgtSentence">
                  <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object usage.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="35d521471f2adf51b4ff2bf4300fb968" id="tgt12" class="tgtSentence">Provider-specific <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> behavior.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="d0b850071cf69edf1971ad0a9eebae8a" id="tgt13" class="tgtSentence">Details for each of the data providers currently available from Microsoft are listed as follows.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b82677b6c1408df4be21ada9a584fde" id="tgt14" class="tgtSentence">Area</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9d9b68ac2b1de18d3712096354b3c3a5" id="tgt15" class="tgtSentence">Topic</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65723094d75ffce13408b55fe576aab9" id="tgt16" class="tgtSentence">ODBC databases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="25df130e047b7ecdeafa4cb717fb44b6" id="tgt17" class="tgtSentence">
                      <legacyLink xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4f63f99b2df661d544d191fe4ff38d32" id="tgt18" class="tgtSentence">Microsoft Indexing Service</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9604c7858531a263962bc9cef8d6af4" id="tgt19" class="tgtSentence">
                      <legacyLink xlink:href="f86a0598-5097-471b-8318-d2c859d085f2">Microsoft OLE DB Provider for Microsoft Indexing Service</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f7c52518e3ef5de8e0bec07a0cd36c48" id="tgt20" class="tgtSentence">Active Directory Service</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0c177a6a1a71d5a6f74fde1879abb642" id="tgt21" class="tgtSentence">
                      <legacyLink xlink:href="f9e81452-5675-4cfc-9949-cfbd2fe57534">Microsoft OLE DB Provider for Microsoft Active Directory Service</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ca3a8423c52f1d62766e4e1376b6cae2" id="tgt22" class="tgtSentence">Microsoft Jet databases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90bbe9ee9e42ea8a6172385bda0e7431" id="tgt23" class="tgtSentence">
                      <legacyLink xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18037e4d206354c3d91b16055c906b94" id="tgt24" class="tgtSentence">Microsoft SQL Server</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5d46cb26c90374fabf2f819e763037eb" id="tgt25" class="tgtSentence">
                      <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a9fedd8fc34d2124863b105fdf4dfa11" id="tgt26" class="tgtSentence">Oracle databases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="774b3449f549911fc07cd37b78b59fd3" id="tgt27" class="tgtSentence">
                      <legacyLink xlink:href="44fae9dd-5585-4cd6-8bbd-3248a78931b4">Microsoft OLE DB Provider for Oracle</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dfa40981cbeb4b466c96bd3503d7f7fb" id="tgt28" class="tgtSentence">Internet Publishing</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="baf1d750a191e962c1889e7279e00ebc" id="tgt29" class="tgtSentence">
                      <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="afa212eba1381c5c4fad2dcc1e6acc52" id="tgt30" class="tgtSentence">Simple data sources</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4daefee86cbc7ba5536df9f073f659cf" id="tgt31" class="tgtSentence">
                      <legacyLink xlink:href="1e7dc6f0-482c-4103-8187-f890865e40fc">Microsoft OLE DB Simple Provider</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4f127468ab0d929f7a5f3f84af0842eb" id="tgt32" class="tgtSentence">Provider-Specific Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="43a96ecde00072fb5d4bd241bc1f6b9e" id="tgt33" class="tgtSentence">The <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collections of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink>, and <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects include dynamic properties specific to the provider.</caps:sentence>
            <caps:sentence sentenceid="1bf35fee1c80ad4b35d12a99a44d78e0" id="tgt34" class="tgtSentence"> These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c1f52bc63e6697969906161d618ed88d" id="tgt35" class="tgtSentence">After establishing the connection and creating these objects, use the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method on the <legacyBold>Properties</legacyBold> collection of the object to obtain the provider-specific properties.</caps:sentence>
            <caps:sentence sentenceid="f7cd3e844cae195930cd2a6c748aa692" id="tgt36" class="tgtSentence"> Refer to the provider documentation and the <legacyLink xlink:href="3c5e2dd5-35e5-4a93-ac3a-3818bb43bbf8">OLE DB Programmer's Guide</legacyLink> for detailed information about these dynamic properties.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a38c75faa02040d71ea97be41887189c" id="tgt37" class="tgtSentence">Service Providers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="651ce9bca0b387abe579dff1e3554d1d" id="tgt38" class="tgtSentence">To use a service provider, you must supply a keyword.</caps:sentence>
            <caps:sentence sentenceid="97516e0d29a7bfb564252bc74fbba09d" id="tgt39" class="tgtSentence"> You should also be aware of the provider-specific dynamic properties associated with each service provider.</caps:sentence>
            <caps:sentence sentenceid="e7aa167ec43a4c28d0c39259fa70e3bc" id="tgt40" class="tgtSentence"> Provider-specific details are listed for each service provider that is currently available from Microsoft:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="97016a77bb0c67daa51f35423e1702bf" id="tgt41" class="tgtSentence">
                  <legacyLink xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="42551cf6226724a216e61cb6a1bc282f" id="tgt42" class="tgtSentence">
                  <legacyLink xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider</legacyLink>   </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="01fa47ad93ff60cdf3d6daa6fa96c1e5" id="tgt43" class="tgtSentence">
                  <legacyLink xlink:href="a4360ed4-b70f-4734-9041-4025d033346b">Microsoft OLE DB Remoting Provider</legacyLink> </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="28e93bd7a11b21abcee9283c1b65992d" id="tgt44" class="tgtSentence">Service Components</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="fee0e7485d72b8d3fd1aa1e488ad1f83" id="tgt45" class="tgtSentence">The <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Cursor Service for OLE DB</legacyLink> service component supplements the cursor support functions of data providers.</caps:sentence>
            <caps:sentence sentenceid="2933dcee24abb3933943ac8447bce399" id="tgt46" class="tgtSentence"> It also requires a keyword and has dynamic properties.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="acaa77da7259a3d7f092f413ecaa53a3" id="tgt47" class="tgtSentence">For more information about OLE DB Providers, see <externalLink><linkText>Microsoft OLE DB</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms722784.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="af719fc1f99e0095116179cd2e28b9cb" id="tgt48" class="tgtSentence">Provider Commands</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="31c2038e2a4a62161874f03a99b8b212" id="tgt49" class="tgtSentence">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statements, such as <codeInline>DROP TABLE t1</codeInline>, as part of the user input.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</link>
        <link xlink:href="f9e81452-5675-4cfc-9949-cfbd2fe57534">Microsoft OLE DB Provider for Microsoft Active Directory Service</link>
        <link xlink:href="f86a0598-5097-471b-8318-d2c859d085f2">Microsoft OLE DB Provider for Microsoft Indexing Service</link>
        <link xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</link>
        <link xlink:href="44fae9dd-5585-4cd6-8bbd-3248a78931b4">Microsoft OLE DB Provider for Oracle</link>
        <link xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</link>
        <link xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This section addresses three kinds of providers: data providers, service providers, and service components.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Providers fall into two categories: those providing data and those providing services.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> A <legacyItalic>data provider</legacyItalic> owns its own data and exposes it in tabular form to your application.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> A <legacyItalic>service provider</legacyItalic> encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> A service provider may also be further defined as a <legacyItalic>service component</legacyItalic>, which must work together with other service providers or components.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Data Providers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The differences usually fall into one of three categories:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Connection parameters in the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">
                  <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object usage.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">Provider-specific <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> behavior.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src13" class="srcSentence">Details for each of the data providers currently available from Microsoft are listed as follows.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Area</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Topic</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">ODBC databases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">
                      <legacyLink xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Microsoft Indexing Service</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">
                      <legacyLink xlink:href="f86a0598-5097-471b-8318-d2c859d085f2">Microsoft OLE DB Provider for Microsoft Indexing Service</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Active Directory Service</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">
                      <legacyLink xlink:href="f9e81452-5675-4cfc-9949-cfbd2fe57534">Microsoft OLE DB Provider for Microsoft Active Directory Service</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Microsoft Jet databases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">
                      <legacyLink xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Microsoft SQL Server</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">
                      <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Oracle databases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">
                      <legacyLink xlink:href="44fae9dd-5585-4cd6-8bbd-3248a78931b4">Microsoft OLE DB Provider for Oracle</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Internet Publishing</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">
                      <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Simple data sources</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">
                      <legacyLink xlink:href="1e7dc6f0-482c-4103-8187-f890865e40fc">Microsoft OLE DB Simple Provider</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src32" class="srcSentence">Provider-Specific Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src33" class="srcSentence">The <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collections of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink>, and <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects include dynamic properties specific to the provider.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src35" class="srcSentence">After establishing the connection and creating these objects, use the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method on the <legacyBold>Properties</legacyBold> collection of the object to obtain the provider-specific properties.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> Refer to the provider documentation and the <legacyLink xlink:href="3c5e2dd5-35e5-4a93-ac3a-3818bb43bbf8">OLE DB Programmer's Guide</legacyLink> for detailed information about these dynamic properties.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src37" class="srcSentence">Service Providers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src38" class="srcSentence">To use a service provider, you must supply a keyword.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> You should also be aware of the provider-specific dynamic properties associated with each service provider.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> Provider-specific details are listed for each service provider that is currently available from Microsoft:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src41" class="srcSentence">
                  <legacyLink xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src42" class="srcSentence">
                  <legacyLink xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider</legacyLink>   </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src43" class="srcSentence">
                  <legacyLink xlink:href="a4360ed4-b70f-4734-9041-4025d033346b">Microsoft OLE DB Remoting Provider</legacyLink> </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src44" class="srcSentence">Service Components</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src45" class="srcSentence">The <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Cursor Service for OLE DB</legacyLink> service component supplements the cursor support functions of data providers.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> It also requires a keyword and has dynamic properties.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src47" class="srcSentence">For more information about OLE DB Providers, see <externalLink><linkText>Microsoft OLE DB</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms722784.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src48" class="srcSentence">Provider Commands</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src49" class="srcSentence">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statements, such as <codeInline>DROP TABLE t1</codeInline>, as part of the user input.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</link>
        <link xlink:href="f9e81452-5675-4cfc-9949-cfbd2fe57534">Microsoft OLE DB Provider for Microsoft Active Directory Service</link>
        <link xlink:href="f86a0598-5097-471b-8318-d2c859d085f2">Microsoft OLE DB Provider for Microsoft Indexing Service</link>
        <link xlink:href="2dc0372d-e74d-4d0f-9c8c-04e5a168c148">Microsoft OLE DB Provider for ODBC</link>
        <link xlink:href="44fae9dd-5585-4cd6-8bbd-3248a78931b4">Microsoft OLE DB Provider for Oracle</link>
        <link xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</link>
        <link xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
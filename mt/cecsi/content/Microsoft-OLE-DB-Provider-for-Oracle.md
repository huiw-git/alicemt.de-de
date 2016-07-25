---
title: "Microsoft OLE DB Provider for Oracle"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44fae9dd-5585-4cd6-8bbd-3248a78931b4
caps.latest.revision: 15
caps.handback.revision: 15
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
# Microsoft OLE DB Provider for Oracle
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="c11dccd1d3ac27d629272c19f9c6d3c0" id="tgt1" class="tgtSentence">This feature will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt2" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="4d9f5d75f3a0951f4dfbefa140d7fbec" id="tgt3" class="tgtSentence"> Instead, use Oracle’s OLE DB provider.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="226466f80093945dd1e5e194e8853878" id="tgt4" class="tgtSentence">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="df209e37fa6496886af7a164ca15b629" id="tgt5" class="tgtSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="088d725786f170b37d440b6045f0141a" id="tgt6" class="tgtSentence">To connect to this provider, set the <legacyItalic>Provider</legacyItalic> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>MSDAORA</code>
          <para>
            <caps:sentence sentenceid="248709408787db043727f63ce324962e" id="tgt7" class="tgtSentence">Reading the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property will return this string as well.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a35505ce270beffae8d557d969cdada9" id="tgt8" class="tgtSentence">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs.</caps:sentence>
            <caps:sentence sentenceid="dfb70113266d6695d6359fcb6d85e42b" id="tgt9" class="tgtSentence"> Oracle only supports a static read-only cursor.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5cf5a4267aa499f9dca0d6e5a90731cb" id="tgt10" class="tgtSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5c9e747ddd8663400e6e4b231a6386e6" id="tgt11" class="tgtSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=MSDAORA;Data Source=<legacyItalic xmlns="">serverName</legacyItalic>;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>; Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence sentenceid="61333c54636d561759b12d35ff08c05b" id="tgt12" class="tgtSentence">The string consists of these keywords:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7df5b64df1181ef1d62d646a13aa860" id="tgt13" class="tgtSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt14" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9e9f3d70bd8c8957627eada96d967706" id="tgt15" class="tgtSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ed56e09a7e160167082812af7064636f" id="tgt16" class="tgtSentence">Specifies the OLE DB Provider for Oracle.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5f0262ef78817e828a92d75e9749b4f9" id="tgt17" class="tgtSentence">Data Source</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bca77fc94f1fee61d5a14249e9ebb490" id="tgt18" class="tgtSentence">Specifies the name of a server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3bd756a1167a9bff574b512092d53350" id="tgt19" class="tgtSentence">User ID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="894ae1122beff71d90c743328e91d2dd" id="tgt20" class="tgtSentence">Specifies the user name.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5f4dcc3b5aa765d61d8327deb882cf99" id="tgt21" class="tgtSentence">Password</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4df08222df3dae489cac77da63d403c" id="tgt22" class="tgtSentence">Specifies the user password.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d4e879422e89d3713c1c025017b59b61" id="tgt23" class="tgtSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <languageKeyword>Trusted_Connection=yes</languageKeyword> or <languageKeyword>Integrated Security = SSPI</languageKeyword> instead of user ID and password information in the connection string.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b3a258973c03d77c4dc730b82e250514" id="tgt24" class="tgtSentence">Provider-Specific Connection Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b8b3eb1e5b5a0ec3d20283d6a73f91af" id="tgt25" class="tgtSentence">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</caps:sentence>
            <caps:sentence sentenceid="d4a4ec629dce9d7e3c152897f1ea0e4e" id="tgt26" class="tgtSentence"> As with the ADO connection properties, these provider-specific properties can be set via the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> or as part of the <legacyBold>ConnectionString</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4273dda1ba258e764de3118434d66665" id="tgt27" class="tgtSentence">These parameters are fully described in the <legacyLink xlink:href="3c5e2dd5-35e5-4a93-ac3a-3818bb43bbf8">OLE DB Programmer's Reference</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="184e00564ec2cdacc010fe59d0c334ec" id="tgt28" class="tgtSentence"> The <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">ADO Dynamic Property Index</legacyLink> provides a cross-reference between these parameter names and the corresponding OLE DB properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt29" class="tgtSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt30" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="98487bfe9fe529e4a2738b2ad9eacaec" id="tgt31" class="tgtSentence">Window Handle</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dea5530ed03eb847d4f1fddef5f6495f" id="tgt32" class="tgtSentence">Indicates the window handle to use to prompt for additional information.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="2d42b4f73ee8bf025a3c06cfa5499f55" id="tgt33" class="tgtSentence">Locale Identifier</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="421b3bcac8d97af51f2f707299bf306f" id="tgt34" class="tgtSentence">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language.</caps:sentence>
                    <caps:sentence sentenceid="2da29035cacf2460ce63be10248ca3fc" id="tgt35" class="tgtSentence"> These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="b6cc341a84e9a5f17c1bb02869de8f68" id="tgt36" class="tgtSentence">OLE DB Services</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ff8a0e5440f398a1d0affa2486e57995" id="tgt37" class="tgtSentence">Indicates a bitmask that specifies OLE DB services to enable or disable.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="4ae35dbb42614d2429b7d6d181a950bb" id="tgt38" class="tgtSentence">Prompt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="170fecc114504a3a7c9f6d13cc2f082c" id="tgt39" class="tgtSentence">Indicates whether to prompt the user while a connection is being established.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="01a074046ca4de7469fdd27ef0f56b30" id="tgt40" class="tgtSentence">Extended Properties</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ed434176fec6b8d97325e5027bb0fe2e" id="tgt41" class="tgtSentence">A string containing provider-specific, extended connection information.</caps:sentence>
                    <caps:sentence sentenceid="c4a2d87de02d3ffcaf6604bf426f4e3f" id="tgt42" class="tgtSentence"> Use this property only for provider-specific connection information that cannot be described through the property mechanism.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString Property</link>
        <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">This feature will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Instead, use Oracle’s OLE DB provider.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src4" class="srcSentence">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">To connect to this provider, set the <legacyItalic>Provider</legacyItalic> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>MSDAORA</code>
          <para>
            <caps:sentence id="src7" class="srcSentence">Reading the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property will return this string as well.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Oracle only supports a static read-only cursor.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=MSDAORA;Data Source=<legacyItalic xmlns="">serverName</legacyItalic>;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>; Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence id="src12" class="srcSentence">The string consists of these keywords:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src15" class="srcSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Specifies the OLE DB Provider for Oracle.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src17" class="srcSentence">Data Source</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Specifies the name of a server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src19" class="srcSentence">User ID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Specifies the user name.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src21" class="srcSentence">Password</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Specifies the user password.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence id="src23" class="srcSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <languageKeyword>Trusted_Connection=yes</languageKeyword> or <languageKeyword>Integrated Security = SSPI</languageKeyword> instead of user ID and password information in the connection string.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Provider-Specific Connection Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> As with the ADO connection properties, these provider-specific properties can be set via the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> or as part of the <legacyBold>ConnectionString</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">These parameters are fully described in the <legacyLink xlink:href="3c5e2dd5-35e5-4a93-ac3a-3818bb43bbf8">OLE DB Programmer's Reference</legacyLink>.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> The <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">ADO Dynamic Property Index</legacyLink> provides a cross-reference between these parameter names and the corresponding OLE DB properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src31" class="srcSentence">Window Handle</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Indicates the window handle to use to prompt for additional information.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src33" class="srcSentence">Locale Identifier</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language.</caps:sentence>
                    <caps:sentence id="src35" class="srcSentence"> These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src36" class="srcSentence">OLE DB Services</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Indicates a bitmask that specifies OLE DB services to enable or disable.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src38" class="srcSentence">Prompt</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Indicates whether to prompt the user while a connection is being established.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src40" class="srcSentence">Extended Properties</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">A string containing provider-specific, extended connection information.</caps:sentence>
                    <caps:sentence id="src42" class="srcSentence"> Use this property only for provider-specific connection information that cannot be described through the property mechanism.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString Property</link>
        <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ConnectionString Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3be75b75-4d36-4479-ab64-9a456869252a
caps.latest.revision: 17
caps.handback.revision: 17
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
# ConnectionString Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e05f348bd45c86f4a7db4af4fe0a61cb" id="tgt1" class="tgtSentence">Indicates the information used to establish a connection to a data source.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="95c701ec7ef8444399749df7594c0234" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="6d818d435e6e9eeeb1d2b47322fbb2e4" id="tgt4" class="tgtSentence">Use the <legacyBold>ConnectionString</legacyBold> property to specify a data source by passing a detailed connection string containing a series of <legacyItalic>argument</legacyItalic> <legacyItalic>= value</legacyItalic> statements separated by semicolons.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c8ae7cf5abf1e376250788a89f5a108a" id="tgt5" class="tgtSentence">ADO supports five arguments for the <legacyBold>ConnectionString</legacyBold> property; any other arguments pass directly to the provider without any processing by ADO.</caps:sentence>
            <caps:sentence sentenceid="7149094845fbc5bc240f26495a78bef3" id="tgt6" class="tgtSentence"> The arguments ADO supports are as follows.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03cde060e90acdd58ff9f0a4d785d43b" id="tgt7" class="tgtSentence">Argument</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt8" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="68c8f52b93644c080a8c35f5e988083d" id="tgt9" class="tgtSentence">
                      <legacyItalic>Provider=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2d7704648beb665496f61a27facfb14" id="tgt10" class="tgtSentence">Specifies the name of a provider to use for the connection.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0d6d2e931cac31fcf5a4b93c77700b8b" id="tgt11" class="tgtSentence">
                      <legacyItalic>File Name=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a3a212bd1f03eaf7daa1955507182815" id="tgt12" class="tgtSentence">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d3ad0c0f5a625696ec53bcb14de4513" id="tgt13" class="tgtSentence">
                      <legacyItalic>Remote Provider=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="665ec1c0d65eabbeb74cb50fcba38217" id="tgt14" class="tgtSentence">Specifies the name of a provider to use when opening a client-side connection.</caps:sentence>
                    <caps:sentence sentenceid="3a3a994bfe9d2acaa57f71f29e3756ef" id="tgt15" class="tgtSentence"> (Remote Data Service only.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aabad836249cfabc43e5bee653b56c00" id="tgt16" class="tgtSentence">
                      <legacyItalic>Remote Server=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5a13d97ffbc5aa7d4cdb665cd7beb5e8" id="tgt17" class="tgtSentence">Specifies the path name of the server to use when opening a client-side connection.</caps:sentence>
                    <caps:sentence sentenceid="3a3a994bfe9d2acaa57f71f29e3756ef" id="tgt18" class="tgtSentence"> (Remote Data Service only.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="655041e4037ca04d5836fb3a61e22260" id="tgt19" class="tgtSentence">
                      <legacyItalic>URL=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c828997e7783b63901a7412884013a85" id="tgt20" class="tgtSentence">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="987a5b61799f6d1a7c24cb38042bc6ce" id="tgt21" class="tgtSentence">After you set the <legacyBold>ConnectionString</legacyBold> property and open the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their equivalents for the specific provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d6d13345a72373a71931471505df5620" id="tgt22" class="tgtSentence">The <legacyBold>ConnectionString</legacyBold> property automatically inherits the value used for the <legacyItalic>ConnectionString</legacyItalic> argument of the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method, so you can override the current <legacyBold>ConnectionString</legacyBold> property during the <legacyBold>Open</legacyBold> method call.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fc529f0308e4aff942c5123ffc1fc5c0" id="tgt23" class="tgtSentence">Because the <legacyItalic>File Name</legacyItalic> argument causes ADO to load the associated provider, you cannot pass both the <legacyItalic>Provider</legacyItalic> and <legacyItalic>File Name</legacyItalic> arguments.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bd734f89beeb2fffa946ac373e3bec6c" id="tgt24" class="tgtSentence">The <legacyBold>ConnectionString</legacyBold> property is read/write when the connection is closed and read-only when it is open.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7f0a6aac1503ff3600159c5271a85ce2" id="tgt25" class="tgtSentence">Duplicates of an argument in the <legacyBold>ConnectionString</legacyBold> property are ignored.</caps:sentence>
            <caps:sentence sentenceid="6169087a4fe70e9cb4ba519ca1a707e1" id="tgt26" class="tgtSentence"> The last instance of any argument is used.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="75e6c5cb1acd35e355c1b64140de6fef" id="tgt27" class="tgtSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Connection</legacyBold> object, the <legacyBold>ConnectionString</legacyBold> property can include only the <legacyItalic>Remote Provider</legacyItalic> and <legacyItalic>Remote Server</legacyItalic> parameters.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="9df2435c36192fa9135659baad301c66" id="tgt28" class="tgtSentence">The following table lists the default ADO provider for each Windows operating system:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b22e3bc789b58e2c76d9a99e13e596f1" id="tgt29" class="tgtSentence">Default ADO provider</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d134cb2c2493da3dc034e2eb6b9b275e" id="tgt30" class="tgtSentence">Windows operating system </caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2e6003e5d10ea6c705fd469cc9d7f1a5" id="tgt31" class="tgtSentence">MSDASQL</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="2b2f2a19a74c2363327de847d467ef2b" id="tgt32" class="tgtSentence">(To improve the readability of source code, explicitly specify the provider name in the connection string.)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7276357e40b1f22f73760cd94e35425f" id="tgt33" class="tgtSentence">Windows 2000 (32-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="ddf48d5e0da18463cc4e5fab57172b30" id="tgt34" class="tgtSentence">Windows XP (32-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="acf61c9cbe70038d5174a9a1054a4d61" id="tgt35" class="tgtSentence">Windows 2003 Server (32-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="6c10b1c3df234919b6d7b683e388a533" id="tgt36" class="tgtSentence">Windows Vista (32-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="fb0fae5385bb8a33038a10ed5b0959df" id="tgt37" class="tgtSentence">Windows Vista Service Pack 1 or later (32-bit and 64-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="0105da590dd38b21224b2583ef8cbbf5" id="tgt38" class="tgtSentence">Windows versions after Windows Vista (32-bit and 64-bit)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bd4d98cfa45d8840197381bacffe3412" id="tgt39" class="tgtSentence">No default.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="c38bb47c1a0e187ae6e8c251b94d4e77" id="tgt40" class="tgtSentence">When an ADO application runs on the following operating systems and does not specify the provider explicitly, ADO returns the following error: "ADODB.Connection: provider is not specified and there is no designated default provider"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fa5a119f6ede045421a76c0707dcf203" id="tgt41" class="tgtSentence">Windows 2000 (64-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="787ea05ca976c8f403ba700f46690a76" id="tgt42" class="tgtSentence">Windows XP (64-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="94167cdc79a4de24c6db3718ff7df672" id="tgt43" class="tgtSentence">Windows 2003 Server (64-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="48a82408c167de2ab9179fb3d5ffb597" id="tgt44" class="tgtSentence">Windows Vista (64-bit)</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt45" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4de7336a-b5ea-43f1-b750-5fa302b5b756">Visual Basic Example</link>
        <link xlink:href="c6bd2609-4c49-462f-a1aa-7bee0f615adb">Visual C++ Example</link>
        <link xlink:href="4c1e61ed-6569-44a9-b0c8-75b820a64cb6">Visual J++ Example</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the information used to establish a connection to a data source.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>ConnectionString</legacyBold> property to specify a data source by passing a detailed connection string containing a series of <legacyItalic>argument</legacyItalic> <legacyItalic>= value</legacyItalic> statements separated by semicolons.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">ADO supports five arguments for the <legacyBold>ConnectionString</legacyBold> property; any other arguments pass directly to the provider without any processing by ADO.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The arguments ADO supports are as follows.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Argument</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">
                      <legacyItalic>Provider=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Specifies the name of a provider to use for the connection.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">
                      <legacyItalic>File Name=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">
                      <legacyItalic>Remote Provider=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Specifies the name of a provider to use when opening a client-side connection.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> (Remote Data Service only.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">
                      <legacyItalic>Remote Server=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Specifies the path name of the server to use when opening a client-side connection.</caps:sentence>
                    <caps:sentence id="src18" class="srcSentence"> (Remote Data Service only.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">
                      <legacyItalic>URL=</legacyItalic> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src21" class="srcSentence">After you set the <legacyBold>ConnectionString</legacyBold> property and open the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their equivalents for the specific provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">The <legacyBold>ConnectionString</legacyBold> property automatically inherits the value used for the <legacyItalic>ConnectionString</legacyItalic> argument of the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method, so you can override the current <legacyBold>ConnectionString</legacyBold> property during the <legacyBold>Open</legacyBold> method call.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">Because the <legacyItalic>File Name</legacyItalic> argument causes ADO to load the associated provider, you cannot pass both the <legacyItalic>Provider</legacyItalic> and <legacyItalic>File Name</legacyItalic> arguments.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">The <legacyBold>ConnectionString</legacyBold> property is read/write when the connection is closed and read-only when it is open.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">Duplicates of an argument in the <legacyBold>ConnectionString</legacyBold> property are ignored.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> The last instance of any argument is used.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src27" class="srcSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Connection</legacyBold> object, the <legacyBold>ConnectionString</legacyBold> property can include only the <legacyItalic>Remote Provider</legacyItalic> and <legacyItalic>Remote Server</legacyItalic> parameters.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src28" class="srcSentence">The following table lists the default ADO provider for each Windows operating system:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Default ADO provider</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Windows operating system </caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">MSDASQL</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">(To improve the readability of source code, explicitly specify the provider name in the connection string.)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Windows 2000 (32-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Windows XP (32-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Windows 2003 Server (32-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Windows Vista (32-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Windows Vista Service Pack 1 or later (32-bit and 64-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Windows versions after Windows Vista (32-bit and 64-bit)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">No default.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">When an ADO application runs on the following operating systems and does not specify the provider explicitly, ADO returns the following error: "ADODB.Connection: provider is not specified and there is no designated default provider"</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Windows 2000 (64-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Windows XP (64-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Windows 2003 Server (64-bit)</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Windows Vista (64-bit)</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src45" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4de7336a-b5ea-43f1-b750-5fa302b5b756">Visual Basic Example</link>
        <link xlink:href="c6bd2609-4c49-462f-a1aa-7bee0f615adb">Visual C++ Example</link>
        <link xlink:href="4c1e61ed-6569-44a9-b0c8-75b820a64cb6">Visual J++ Example</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
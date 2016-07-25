---
title: "Microsoft OLE DB Provider for Internet Publishing"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 66a208d9-b580-4655-a41e-1d36e5b5bfca
caps.latest.revision: 9
caps.handback.revision: 9
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
# Microsoft OLE DB Provider for Internet Publishing
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4bc16dff8c8080dc14c6e15e841178f9" id="tgt1" class="tgtSentence">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server.</caps:sentence>
          <caps:sentence sentenceid="8d956cad448b4959223bd7bff4a6b57d" id="tgt2" class="tgtSentence"> Resources include web source files such as HTML files, or Windows 2000 web folders.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="df209e37fa6496886af7a164ca15b629" id="tgt3" class="tgtSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="088d725786f170b37d440b6045f0141a" id="tgt4" class="tgtSentence">To connect to this provider, set the <legacyItalic>Provider</legacyItalic> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>MSDAIPP.DSO</code>
          <para>
            <caps:sentence sentenceid="a4158cf50f1c5612aa8cb2bda17ec97e" id="tgt5" class="tgtSentence">This value can also be set or read using the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5cf5a4267aa499f9dca0d6e5a90731cb" id="tgt6" class="tgtSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5c9e747ddd8663400e6e4b231a6386e6" id="tgt7" class="tgtSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=MSDAIPP.DSO;Data Source=<legacyItalic xmlns="">ResourceURL</legacyItalic>;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence sentenceid="3d263eb0233f14872193733387840c80" id="tgt8" class="tgtSentence">-or-</caps:sentence>
          </para>
          <code>"URL=<legacyItalic xmlns="">ResourceURL</legacyItalic>;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence sentenceid="61333c54636d561759b12d35ff08c05b" id="tgt9" class="tgtSentence">The string consists of these keywords:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7df5b64df1181ef1d62d646a13aa860" id="tgt10" class="tgtSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt11" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9e9f3d70bd8c8957627eada96d967706" id="tgt12" class="tgtSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2331c1d04f9019db07b6721c4a4c132c" id="tgt13" class="tgtSentence">Specifies the OLE DB Provider for Internet Publishing.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="96bee283950c28fec464ae0354d4dc75" id="tgt14" class="tgtSentence">
                      <legacyBold>Data Source</legacyBold> -or- <legacyBold>URL</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="762432184d2bf924a85847f927d3516d" id="tgt15" class="tgtSentence">Specifies the URL of a file or directory published in a Web Folder.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3bd756a1167a9bff574b512092d53350" id="tgt16" class="tgtSentence">User ID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="894ae1122beff71d90c743328e91d2dd" id="tgt17" class="tgtSentence">Specifies the user name.</caps:sentence>
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
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d4e879422e89d3713c1c025017b59b61" id="tgt20" class="tgtSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <languageKeyword>Trusted_Connection=yes</languageKeyword> or <languageKeyword>Integrated Security = SSPI</languageKeyword> instead of user ID and password information in the connection string.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="340787249a2b50dcfb258728fd410c45" id="tgt21" class="tgtSentence">If you set the <legacyItalic>ResourceURL</legacyItalic> value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value.</caps:sentence>
            <caps:sentence sentenceid="30ec2f032dac668bfaebcafdfc691935" id="tgt22" class="tgtSentence"> This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="0fb5ef3129b437fc743c2c4c00c05202" id="tgt23" class="tgtSentence">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the <legacyItalic>Provider</legacyItalic> connection string keyword or the <legacyBold>Provider</legacyBold> property, you cannot use "URL=" in the connection string.</caps:sentence>
              <caps:sentence sentenceid="c50fa1c91debfd09ddcb728fab31350a" id="tgt24" class="tgtSentence"> If you do, an error will occur.</caps:sentence>
              <caps:sentence sentenceid="064207f71ff6f6f6865807d7797445fa" id="tgt25" class="tgtSentence"> Instead, simply specify the URL as shown in the topic <legacyLink xlink:href="4869aafa-7401-4ce1-93ce-45406a60274f">Using ADO with the OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</link>
        <link xlink:href="4869aafa-7401-4ce1-93ce-45406a60274f">Using ADO with the OLE DB Provider for Internet Publishing</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Resources include web source files such as HTML files, or Windows 2000 web folders.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">To connect to this provider, set the <legacyItalic>Provider</legacyItalic> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>MSDAIPP.DSO</code>
          <para>
            <caps:sentence id="src5" class="srcSentence">This value can also be set or read using the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=MSDAIPP.DSO;Data Source=<legacyItalic xmlns="">ResourceURL</legacyItalic>;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence id="src8" class="srcSentence">-or-</caps:sentence>
          </para>
          <code>"URL=<legacyItalic xmlns="">ResourceURL</legacyItalic>;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence id="src9" class="srcSentence">The string consists of these keywords:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src12" class="srcSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Specifies the OLE DB Provider for Internet Publishing.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">
                      <legacyBold>Data Source</legacyBold> -or- <legacyBold>URL</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Specifies the URL of a file or directory published in a Web Folder.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src16" class="srcSentence">User ID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Specifies the user name.</caps:sentence>
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
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence id="src20" class="srcSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <languageKeyword>Trusted_Connection=yes</languageKeyword> or <languageKeyword>Integrated Security = SSPI</languageKeyword> instead of user ID and password information in the connection string.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src21" class="srcSentence">If you set the <legacyItalic>ResourceURL</legacyItalic> value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src23" class="srcSentence">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the <legacyItalic>Provider</legacyItalic> connection string keyword or the <legacyBold>Provider</legacyBold> property, you cannot use "URL=" in the connection string.</caps:sentence>
              <caps:sentence id="src24" class="srcSentence"> If you do, an error will occur.</caps:sentence>
              <caps:sentence id="src25" class="srcSentence"> Instead, simply specify the URL as shown in the topic <legacyLink xlink:href="4869aafa-7401-4ce1-93ce-45406a60274f">Using ADO with the OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</link>
        <link xlink:href="4869aafa-7401-4ce1-93ce-45406a60274f">Using ADO with the OLE DB Provider for Internet Publishing</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "CreateObject Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: dec96be6-0b31-4953-9c9a-e962b5afcd18
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
# CreateObject Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3044ca97bc21c354c1fb2ef9d2c100cb" id="tgt1" class="tgtSentence">Creates the proxy for the target business object and returns a pointer to it.</caps:sentence>
          <caps:sentence sentenceid="0b2db67857cb5ba3cf62ffa70277edc4" id="tgt2" class="tgtSentence"> The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet.</caps:sentence>
          <caps:sentence sentenceid="9ae1a6fbdf460c567483a2ef9a82fc85" id="tgt3" class="tgtSentence"> For in-process component objects, no proxies are used, just a pointer to the object is provided.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt4" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt5" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt6" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt7" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt8" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9418e13d3949f3213d10cbf521ce66e5" id="tgt9" class="tgtSentence">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="81788ba0d7d02d81c063dbca621ba11b" id="tgt10" class="tgtSentence">Protocol</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt11" class="tgtSentence">Syntax</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="80791b3ae7002cb88c246876d9faa8f8" id="tgt12" class="tgtSentence">HTTP</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b30268b40cdc7e5c81bfbb90c087e720" id="tgt13" class="tgtSentence">Set object = DataSpace.CreateObject("ProgId", "http://awebsrvr")</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5e056c500a1c4b6a7110b50d807bade5" id="tgt14" class="tgtSentence">HTTPS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="290b2a2217503f956ce04ad323ad7146" id="tgt15" class="tgtSentence">Set object = DataSpace.CreateObject("ProgId", "https://awebsrvr")</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c14f7a73c9cca3dec4ca6c9c3e722f2b" id="tgt16" class="tgtSentence">DCOM</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fa8afbfd01bf45ceb9d8c2c223dda423" id="tgt17" class="tgtSentence">Set object = DataSpace.CreateObject("ProgId", "computername")</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbd0c217f849f5c8cf3333884d9e7779" id="tgt18" class="tgtSentence">In-process</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="33b7def19c7c744e5aaa61d097c5e292" id="tgt19" class="tgtSentence">Set object = DataSpace.CreateObject("ProgId", "")</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt20" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="a8cfde6331bd59eb2ac96f8911c4b666" id="tgt21" class="tgtSentence">Object</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a0dbac9dbfb73a23ede27f5c15258202" id="tgt22" class="tgtSentence">An object variable that evaluates to an object that is the type specified in <legacyItalic>ProgID</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="8e8ff9250223973ebcd4d74cd7df26a7" id="tgt23" class="tgtSentence">DataSpace</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a5832aec1d878c89d8a918ba084eeba6" id="tgt24" class="tgtSentence">An object variable that represents an <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object used to create an instance of the new object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence sentenceid="bddd96a35992af1d958c7afdc4a6f622" id="tgt25" class="tgtSentence">ProgID</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="2cfa2b5cd92784539db004ea403ee642" id="tgt26" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e0b7f94d1adc8e17e25f85644b1b4c96" id="tgt27" class="tgtSentence">
                <legacyItalic>awebsrvr </legacyItalic>or <legacyItalic>computername</legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d413b2e4cd3b3fac7f74946732f3582b" id="tgt28" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that represents a URL identifying the Internet Information Services (IIS) Web server where an instance of the server business object is created.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="5be81db62abc654af5ee20eb26203ca3" id="tgt29" class="tgtSentence">The <legacyItalic>HTTP protocol</legacyItalic> is the standard Web protocol; <legacyItalic>HTTPS</legacyItalic> is a secure Web protocol.</caps:sentence>
            <caps:sentence sentenceid="81baf81a5b70dc366a0c68d33bb61223" id="tgt30" class="tgtSentence"> Use the <legacyItalic>DCOM protocol</legacyItalic> when running a local-area network without HTTP.</caps:sentence>
            <caps:sentence sentenceid="ab98f4da47720b8117315e36599956cd" id="tgt31" class="tgtSentence"> The <legacyItalic>in-process</legacyItalic> protocol is a local dynamic-link library (DLL); it does not use a network.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt32" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b4e2844a-120a-4513-860b-f1b6e4b5dda4">DataFactory Object, Query Method, and CreateObject Method Example (VBScript)</link>
        <link xlink:href="12b0e160-5e5c-441f-bed7-ac0bd061e003">DataSpace Object and CreateObject Method Example (VBScript)</link>
        <link xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Creates the proxy for the target business object and returns a pointer to it.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For in-process component objects, no proxies are used, just a pointer to the object is provided.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src4" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Protocol</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Syntax</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">HTTP</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Set object = DataSpace.CreateObject("ProgId", "http://awebsrvr")</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">HTTPS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Set object = DataSpace.CreateObject("ProgId", "https://awebsrvr")</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">DCOM</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Set object = DataSpace.CreateObject("ProgId", "computername")</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">In-process</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Set object = DataSpace.CreateObject("ProgId", "")</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src21" class="srcSentence">Object</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src22" class="srcSentence">An object variable that evaluates to an object that is the type specified in <legacyItalic>ProgID</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src23" class="srcSentence">DataSpace</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src24" class="srcSentence">An object variable that represents an <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object used to create an instance of the new object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <legacyItalic>
                <caps:sentence id="src25" class="srcSentence">ProgID</caps:sentence>
              </legacyItalic>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src26" class="srcSentence">A <languageKeyword>String</languageKeyword> value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src27" class="srcSentence">
                <legacyItalic>awebsrvr </legacyItalic>or <legacyItalic>computername</legacyItalic></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src28" class="srcSentence">A <languageKeyword>String</languageKeyword> value that represents a URL identifying the Internet Information Services (IIS) Web server where an instance of the server business object is created.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">The <legacyItalic>HTTP protocol</legacyItalic> is the standard Web protocol; <legacyItalic>HTTPS</legacyItalic> is a secure Web protocol.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> Use the <legacyItalic>DCOM protocol</legacyItalic> when running a local-area network without HTTP.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> The <legacyItalic>in-process</legacyItalic> protocol is a local dynamic-link library (DLL); it does not use a network.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src32" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b4e2844a-120a-4513-860b-f1b6e4b5dda4">DataFactory Object, Query Method, and CreateObject Method Example (VBScript)</link>
        <link xlink:href="12b0e160-5e5c-441f-bed7-ac0bd061e003">DataSpace Object and CreateObject Method Example (VBScript)</link>
        <link xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
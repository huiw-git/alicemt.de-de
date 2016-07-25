---
title: "Address Book Data-Binding Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 080c1925-d453-4b89-92ac-c93591490518
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
# Address Book Data-Binding Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8f5e54cd5d30b7e92458f2e6f150e88f" id="tgt1" class="tgtSentence">The Address Book application uses the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page.</caps:sentence>
          <caps:sentence sentenceid="b761c43e535c0e5e50c48f2b6baec763" id="tgt2" class="tgtSentence"> The event-driven VBScript program logic uses the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> to:</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="32942b062f5a8569eb73cb4a8fc853c2" id="tgt7" class="tgtSentence">Query the database, send updates to the database, and refresh the data grid.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="7695828166bc1a769a023e65974049d3" id="tgt8" class="tgtSentence">Allow users to move to the first, next, previous, or last record in the data grid.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="1674e64a6ba8001ec80d8ac33f498df0" id="tgt9" class="tgtSentence">The following code defines the <legacyBold>RDS.DataControl</legacyBold> component:</caps:sentence>
        </para>
        <code>&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"
   ID=DC1 Width=1 Height=1&gt;
   &lt;PARAM NAME="SERVER" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
   &lt;PARAM NAME="CONNECT" VALUE="Provider=sqloledb;
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"&gt;
&lt;/OBJECT&gt;</code>
        <para>
          <caps:sentence sentenceid="ef958a7b615c98b6ed6d67e897aead46" id="tgt10" class="tgtSentence">The OBJECT tag defines the <legacyBold>RDS.DataControl</legacyBold> component in the program.</caps:sentence>
          <caps:sentence sentenceid="c5eb0d879532eceddbbb43cb4370eebe" id="tgt11" class="tgtSentence"> The tag includes two types of parameters:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="7fc5c2e27999d90aabc08cdf0da5dc49" id="tgt12" class="tgtSentence">Those associated with the generic OBJECT tag.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ac46c20854177c391cf6331e9a6db9f8" id="tgt13" class="tgtSentence">Those specific to the <legacyBold>RDS.DataControl</legacyBold> object.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="ec4eb509cebd70248b83eae6d87aee2a" id="tgt14" class="tgtSentence">Generic OBJECT Tag Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ec6be886c88543b22100587891095373" id="tgt15" class="tgtSentence">The following table describes the parameters associated with the OBJECT tag.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt16" class="tgtSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt17" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="07d42fcb59c1774e128a59602aa5937b" id="tgt18" class="tgtSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>CLASSID</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b36f316692f6ab595facecdbe30dd3c7" id="tgt19" class="tgtSentence">A unique, 128-bit number that identifies the type of embedded object to the system.</caps:sentence>
                    <caps:sentence sentenceid="7d6b25246aa0f859278415e02930ee60" id="tgt20" class="tgtSentence"> This identifier is maintained in the local computer's system registry.</caps:sentence>
                    <caps:sentence sentenceid="9bf535a3124b45460b3e47ff018c5cac" id="tgt21" class="tgtSentence"> (For the class IDs of the <legacyBold>RDS.DataControl</legacyBold> object, see <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl Object</legacyLink>.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06f057fd1120d2adc8e6d07b6545d8d4" id="tgt22" class="tgtSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>ID</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="452b2b40f81f373bea0363c37ffca1af" id="tgt23" class="tgtSentence">Defines a document-wide identifier for the embedded object that is used to identify it in code.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="42d089a201263403389e9d30896762ec" id="tgt24" class="tgtSentence">RDS.DataControl Tag Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a80fe4f7384903fc8f321284de083d6d" id="tgt25" class="tgtSentence">The following table describes the parameters specific to the <legacyBold>RDS.DataControl</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="c9996271ca54d79d9f95372b12df7cb7" id="tgt26" class="tgtSentence"> (For a complete list of the <legacyBold>RDS.DataControl</legacyBold> object parameters, and when to implement them, see <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl object</legacyLink>.)</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt27" class="tgtSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt28" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec677d8f10ea6d0af00bc6b162bce9fb" id="tgt29" class="tgtSentence">               <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">SERVER</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f05e4b7852b1464d301732366f6e60d3" id="tgt30" class="tgtSentence">If you are using HTTP, the value is the name of the server computer preceded by <codeInline>http://</codeInline>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f3e71d91ce830b861e3549bab37ac26a" id="tgt31" class="tgtSentence">               <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">CONNECT</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42c481d1cd2acfca00b4419525e4a411" id="tgt32" class="tgtSentence">Provides the necessary connection information for the <legacyBold>RDS.DataControl</legacyBold> to connect to SQL Server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7f3074caf7b55863e5a0ae68c6253649" id="tgt33" class="tgtSentence">               <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62b93ee4e42752634ed53c31a02f4426" id="tgt34" class="tgtSentence">Sets or returns the query string used to retrieve the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Address Book application uses the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The event-driven VBScript program logic uses the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> to:</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Query the database, send updates to the database, and refresh the data grid.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Allow users to move to the first, next, previous, or last record in the data grid.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src9" class="srcSentence">The following code defines the <legacyBold>RDS.DataControl</legacyBold> component:</caps:sentence>
        </para>
        <code>&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"
   ID=DC1 Width=1 Height=1&gt;
   &lt;PARAM NAME="SERVER" VALUE="http://&lt;%=Request.ServerVariables("SERVER_NAME")%&gt;"&gt;
   &lt;PARAM NAME="CONNECT" VALUE="Provider=sqloledb;
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"&gt;
&lt;/OBJECT&gt;</code>
        <para>
          <caps:sentence id="src10" class="srcSentence">The OBJECT tag defines the <legacyBold>RDS.DataControl</legacyBold> component in the program.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> The tag includes two types of parameters:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Those associated with the generic OBJECT tag.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">Those specific to the <legacyBold>RDS.DataControl</legacyBold> object.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Generic OBJECT Tag Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">The following table describes the parameters associated with the OBJECT tag.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>CLASSID</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">A unique, 128-bit number that identifies the type of embedded object to the system.</caps:sentence>
                    <caps:sentence id="src20" class="srcSentence"> This identifier is maintained in the local computer's system registry.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> (For the class IDs of the <legacyBold>RDS.DataControl</legacyBold> object, see <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl Object</legacyLink>.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">               <legacyBold>                 </legacyBold><legacyBold><legacyItalic>ID</legacyItalic></legacyBold><legacyBold>               </legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Defines a document-wide identifier for the embedded object that is used to identify it in code.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">RDS.DataControl Tag Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">The following table describes the parameters specific to the <legacyBold>RDS.DataControl</legacyBold> object.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> (For a complete list of the <legacyBold>RDS.DataControl</legacyBold> object parameters, and when to implement them, see <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl object</legacyLink>.)</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">               <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">SERVER</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">If you are using HTTP, the value is the name of the server computer preceded by <codeInline>http://</codeInline>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">               <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">CONNECT</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Provides the necessary connection information for the <legacyBold>RDS.DataControl</legacyBold> to connect to SQL Server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">               <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Sets or returns the query string used to retrieve the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "DataControl Object (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d85ea4fc-451c-436e-97b8-58f92b149dd0
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
# DataControl Object (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="77b91552962677bfa5fe7b1c5f70f81a" id="tgt1" class="tgtSentence">Binds a data query <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to one or more controls (for example, a text box, grid control, or combo box) to display the <legacyBold>Recordset</legacyBold> data on a Web page.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
   &lt;PARAM NAME="Connect" VALUE="DSN=DSNName;UID=MyUserID;PWD=MyPassword;"&gt;
   &lt;PARAM NAME="Server" VALUE="http://awebsrvr"&gt;
   &lt;PARAM NAME="SQL" VALUE="QueryText"&gt;
&lt;/OBJECT&gt;</legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="2a12fa436569e179cd19021717a24d8e" id="tgt6" class="tgtSentence">The class ID for the <legacyBold>RDS.DataControl</legacyBold> object is BD96C556-65A3-11D0-983A-00C04FC29E33.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="27b1a1d6907b0ad753455dd12e0a2a7a" id="tgt7" class="tgtSentence">If you get an error that an <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> or <legacyBold>RDS.DataControl</legacyBold> object does not load, make sure that you are using the correct class ID.</caps:sentence>
              <caps:sentence sentenceid="e21b99ab805f456b4fce4b09210aa340" id="tgt8" class="tgtSentence"> The class IDs for these objects have changed from version 1.0 and 1.1.</caps:sentence>
              <caps:sentence sentenceid="5e15cf798b5a0e6145a50bb8ac572b60" id="tgt9" class="tgtSentence"> Also, be aware that even nullable columns must be set when you use the <legacyBold>RDS DataControl</legacyBold> object.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="6c43aac2b7fa06d6831b2e3acd1a92e2" id="tgt10" class="tgtSentence">For a basic scenario, you need to set only the <legacyBold>SQL</legacyBold>, <legacyBold>Connect</legacyBold>, and <legacyBold>Server</legacyBold> properties of the <legacyBold>RDS.DataControl</legacyBold> object, which will automatically call the default business object, <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="edcc94ae970ac1940443e9c2c4493910" id="tgt11" class="tgtSentence">All the properties in the <legacyBold>RDS.DataControl</legacyBold> are optional because custom business objects can replace their functionality.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="db9a132592ece3910f03aa7c62a6e303" id="tgt12" class="tgtSentence">If you query for multiple results, only the first <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is returned.</caps:sentence>
              <caps:sentence sentenceid="45ba2b79f7c08cc34aecea28ea81f5a6" id="tgt13" class="tgtSentence"> If multiple result sets are needed, assign each to its own <legacyBold>DataControl</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="1fbeddd5cb1810a5492d23c8f451d8e6" id="tgt14" class="tgtSentence"> An example of a query for multiple results could be the following: <codeInline>"Select * from Authors, Select * from Topics"</codeInline></caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="78686d58448acb3af7b5eabb3a852310" id="tgt15" class="tgtSentence">Adding "DFMode=20;" to your connection string when you use the <legacyBold>RDS.DataControl</legacyBold> object can improve the performance of your server when you update data.</caps:sentence>
            <caps:sentence sentenceid="18b9a197e48e7b61eb5a91ef217de984" id="tgt16" class="tgtSentence"> With this setting, the <legacyBold>RDSServer.DataFactory</legacyBold> object on the server uses a less resource-intensive mode.</caps:sentence>
            <caps:sentence sentenceid="a8d2d8a6036ca2d0e7a5221adf6181a6" id="tgt17" class="tgtSentence"> However, the following features are not available in this configuration:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="5c9f7f3542245e91e0db395d1fdb5eae" id="tgt18" class="tgtSentence">Using parameterized queries.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="117102df81d2bded3a9ae162e62aa6c0" id="tgt19" class="tgtSentence">Getting parameter or column information before calling the <legacyBold>Execute</legacyBold> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="662775dfd4d17f3c9b517912fc8a0c61" id="tgt20" class="tgtSentence">Setting <legacyBold>Transact Updates</legacyBold> to <legacyBold>True</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="031d7d000b8e534eb4018bd110d67344" id="tgt21" class="tgtSentence">Getting row status.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8e4b968f8a83bd47258e567b1198437c" id="tgt22" class="tgtSentence">Calling the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="07b8dc4e43c67f29a027035f45584b37" id="tgt23" class="tgtSentence">Refreshing (explicitly or automatically) via the <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="59c79b8a81beab56a15eb395b8e3a16a" id="tgt24" class="tgtSentence">Setting <legacyBold>Command</legacyBold> or <legacyLink xlink:href="a29e3fb9-306d-497a-9a59-1856a914e5e9">Recordset</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d95b7a520d43039239509737972ee3dd" id="tgt25" class="tgtSentence">Using <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="987aee60cfba622d19c8ebe627bab33c" id="tgt26" class="tgtSentence">The <legacyBold>RDS.DataControl</legacyBold> object runs in asynchronous mode by default.</caps:sentence>
            <caps:sentence sentenceid="b968f400ee9127cda70d4ebbda77f011" id="tgt27" class="tgtSentence"> If you require synchronous execution for your application, set the <legacyLink xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions</legacyLink> parameter equal to <legacyBold>adcExecSync</legacyBold> and the <legacyLink xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions</legacyLink> parameter equal to <legacyBold>adcFetchUpFront</legacyBold>, as shown in the following example.</caps:sentence>
          </para>
          <code>&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
    ID="DataControl"
   &lt;PARAM NAME="Connect" VALUE="DSN=DSNName;UID=MyUserID;PWD=MyPassword;"&gt;
   &lt;PARAM NAME="Server" VALUE="http://awebsrvr"&gt;
   &lt;PARAM NAME="SQL" VALUE="QueryText"&gt;
<codeFeaturedElement xmlns="">   &lt;PARAM NAME="ExecuteOptions" VALUE="1"&gt;   &lt;PARAM NAME="FetchOptions" VALUE="1"&gt;</codeFeaturedElement>
&lt;/OBJECT&gt;</code>
          <para>
            <caps:sentence sentenceid="efd7e00bdfc79f941d116e3605a999fe" id="tgt28" class="tgtSentence">Use one <legacyBold>RDS.DataControl</legacyBold> object to link the results of a single query to one or more visual controls.</caps:sentence>
            <caps:sentence sentenceid="30de94e52c2b57f20c6366c6d86c1306" id="tgt29" class="tgtSentence"> For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status.</caps:sentence>
            <caps:sentence sentenceid="0dc27ddb6d5f01c3291793e839592b27" id="tgt30" class="tgtSentence"> You can use a single <legacyBold>RDS.DataControl</legacyBold> object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8a98481d938d702a55af3abaa01a53fd" id="tgt31" class="tgtSentence">Use different <legacyBold>RDS.DataControl</legacyBold> objects to link the results of multiple queries to different visual controls.</caps:sentence>
            <caps:sentence sentenceid="a2a48b692eeafbb60b890d4020a6c4a5" id="tgt32" class="tgtSentence"> For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased.</caps:sentence>
            <caps:sentence sentenceid="84700c34b0bf369a618405aaf7fa1a44" id="tgt33" class="tgtSentence"> You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control.</caps:sentence>
            <caps:sentence sentenceid="d0fb2a9a166fe6dafa86bd432a54beee" id="tgt34" class="tgtSentence"> If you use the default business object (<legacyBold>RDSServer.DataFactory</legacyBold>), you must do the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="35e623579e1a4c9e7fdc61c3fd37677d" id="tgt35" class="tgtSentence">Add two <legacyBold>RDS.DataControl</legacyBold> objects to your Web page.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="75e35c48b570807e3154e80a0b4b84c0" id="tgt36" class="tgtSentence">Write two queries, one for each <legacyBold>SQL</legacyBold> property of the two <legacyBold>RDS.DataControl</legacyBold> objects.</caps:sentence>
                <caps:sentence sentenceid="db2b6003604295e1aa05823486372a3f" id="tgt37" class="tgtSentence"> One <legacyBold>RDS.DataControl </legacyBold>object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0431bd99bee57cbfe3206ba2fcd67668" id="tgt38" class="tgtSentence">In the OBJECT tags of each bound control, specify the DATAFLD value to set the values for the data that you want to display in each visual control.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="dde740ff6ee8c6db62d973781f8d5fda" id="tgt39" class="tgtSentence">There is no count restriction on the number of <legacyBold>RDS.DataControl</legacyBold> objects that you can embed by using OBJECT tags on a single Web page.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="575f923fbc4f6b48506e677baa872b57" id="tgt40" class="tgtSentence">When you define the <legacyBold>RDS.DataControl</legacyBold> object on a Web page, use nonzero <legacyBold>Height</legacyBold> and <legacyBold>Width</legacyBold> values such as 1 (to avoid the inclusion of extra space).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2215a47c05fffb8810cdf42b863becaf" id="tgt41" class="tgtSentence">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you do not need to include a CODEBASE parameter in your <legacyBold>RDS.DataControl</legacyBold> object tag.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e1dd7165d141efa1eb8d57765b6aab78" id="tgt42" class="tgtSentence">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX® controls only if they are marked as apartment model controls.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="cbfe9d7f321fcc1a071a1413b03042a8" id="tgt43" class="tgtSentence">  <legacyBold>Microsoft Visual Basic Users</legacyBold>   The <legacyBold>RDS.DataControl</legacyBold> is safe for scripting and is used only in Web-based applications.</caps:sentence>
              <caps:sentence sentenceid="96b1ba2ce1eea1f88c1ca7dd692ebd24" id="tgt44" class="tgtSentence"> A Visual Basic client application has no need for it.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt45" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1a27bab5091293bfd3a1c75ca1ac2f73" id="tgt46" class="tgtSentence">
                  <legacyLink xlink:href="9a8f9b0c-8452-4e95-a561-cfc4b7165c5e">DataControl Object (RDS) Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="4f306a51-d5a4-4785-b426-487639cda164">VBScript Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Binds a data query <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to one or more controls (for example, a text box, grid control, or combo box) to display the <legacyBold>Recordset</legacyBold> data on a Web page.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
   &lt;PARAM NAME="Connect" VALUE="DSN=DSNName;UID=MyUserID;PWD=MyPassword;"&gt;
   &lt;PARAM NAME="Server" VALUE="http://awebsrvr"&gt;
   &lt;PARAM NAME="SQL" VALUE="QueryText"&gt;
&lt;/OBJECT&gt;</legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">The class ID for the <legacyBold>RDS.DataControl</legacyBold> object is BD96C556-65A3-11D0-983A-00C04FC29E33.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src7" class="srcSentence">If you get an error that an <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> or <legacyBold>RDS.DataControl</legacyBold> object does not load, make sure that you are using the correct class ID.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> The class IDs for these objects have changed from version 1.0 and 1.1.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> Also, be aware that even nullable columns must be set when you use the <legacyBold>RDS DataControl</legacyBold> object.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src10" class="srcSentence">For a basic scenario, you need to set only the <legacyBold>SQL</legacyBold>, <legacyBold>Connect</legacyBold>, and <legacyBold>Server</legacyBold> properties of the <legacyBold>RDS.DataControl</legacyBold> object, which will automatically call the default business object, <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">All the properties in the <legacyBold>RDS.DataControl</legacyBold> are optional because custom business objects can replace their functionality.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src12" class="srcSentence">If you query for multiple results, only the first <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> is returned.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> If multiple result sets are needed, assign each to its own <legacyBold>DataControl</legacyBold>.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> An example of a query for multiple results could be the following: <codeInline>"Select * from Authors, Select * from Topics"</codeInline></caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src15" class="srcSentence">Adding "DFMode=20;" to your connection string when you use the <legacyBold>RDS.DataControl</legacyBold> object can improve the performance of your server when you update data.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> With this setting, the <legacyBold>RDSServer.DataFactory</legacyBold> object on the server uses a less resource-intensive mode.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> However, the following features are not available in this configuration:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">Using parameterized queries.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">Getting parameter or column information before calling the <legacyBold>Execute</legacyBold> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">Setting <legacyBold>Transact Updates</legacyBold> to <legacyBold>True</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src21" class="srcSentence">Getting row status.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">Calling the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">Refreshing (explicitly or automatically) via the <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src24" class="srcSentence">Setting <legacyBold>Command</legacyBold> or <legacyLink xlink:href="a29e3fb9-306d-497a-9a59-1856a914e5e9">Recordset</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src25" class="srcSentence">Using <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src26" class="srcSentence">The <legacyBold>RDS.DataControl</legacyBold> object runs in asynchronous mode by default.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> If you require synchronous execution for your application, set the <legacyLink xlink:href="62a4fd88-afc3-4f1f-b978-40710a30c4e9">ExecuteOptions</legacyLink> parameter equal to <legacyBold>adcExecSync</legacyBold> and the <legacyLink xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions</legacyLink> parameter equal to <legacyBold>adcFetchUpFront</legacyBold>, as shown in the following example.</caps:sentence>
          </para>
          <code>&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
    ID="DataControl"
   &lt;PARAM NAME="Connect" VALUE="DSN=DSNName;UID=MyUserID;PWD=MyPassword;"&gt;
   &lt;PARAM NAME="Server" VALUE="http://awebsrvr"&gt;
   &lt;PARAM NAME="SQL" VALUE="QueryText"&gt;
<codeFeaturedElement xmlns="">   &lt;PARAM NAME="ExecuteOptions" VALUE="1"&gt;   &lt;PARAM NAME="FetchOptions" VALUE="1"&gt;</codeFeaturedElement>
&lt;/OBJECT&gt;</code>
          <para>
            <caps:sentence id="src28" class="srcSentence">Use one <legacyBold>RDS.DataControl</legacyBold> object to link the results of a single query to one or more visual controls.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> You can use a single <legacyBold>RDS.DataControl</legacyBold> object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src31" class="srcSentence">Use different <legacyBold>RDS.DataControl</legacyBold> objects to link the results of multiple queries to different visual controls.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> If you use the default business object (<legacyBold>RDSServer.DataFactory</legacyBold>), you must do the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">Add two <legacyBold>RDS.DataControl</legacyBold> objects to your Web page.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">Write two queries, one for each <legacyBold>SQL</legacyBold> property of the two <legacyBold>RDS.DataControl</legacyBold> objects.</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> One <legacyBold>RDS.DataControl </legacyBold>object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src38" class="srcSentence">In the OBJECT tags of each bound control, specify the DATAFLD value to set the values for the data that you want to display in each visual control.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src39" class="srcSentence">There is no count restriction on the number of <legacyBold>RDS.DataControl</legacyBold> objects that you can embed by using OBJECT tags on a single Web page.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src40" class="srcSentence">When you define the <legacyBold>RDS.DataControl</legacyBold> object on a Web page, use nonzero <legacyBold>Height</legacyBold> and <legacyBold>Width</legacyBold> values such as 1 (to avoid the inclusion of extra space).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src41" class="srcSentence">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you do not need to include a CODEBASE parameter in your <legacyBold>RDS.DataControl</legacyBold> object tag.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src42" class="srcSentence">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX® controls only if they are marked as apartment model controls.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src43" class="srcSentence">  <legacyBold>Microsoft Visual Basic Users</legacyBold>   The <legacyBold>RDS.DataControl</legacyBold> is safe for scripting and is used only in Web-based applications.</caps:sentence>
              <caps:sentence id="src44" class="srcSentence"> A Visual Basic client application has no need for it.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src45" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src46" class="srcSentence">
                  <legacyLink xlink:href="9a8f9b0c-8452-4e95-a561-cfc4b7165c5e">DataControl Object (RDS) Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="4f306a51-d5a4-4785-b426-487639cda164">VBScript Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
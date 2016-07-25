---
title: "XML Recordset Persistence Scenario"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 353d569a-043a-4397-9ee6-564c4af8d5f6
caps.latest.revision: 3
caps.handback.revision: 3
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
# XML Recordset Persistence Scenario
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="57cdfbcf4900305bab9a6c9c5529528b" id="tgt1" class="tgtSentence">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a Recordset object directly to the ASP Response object.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="9fd18b2cab0bce77eb348dd5b1f46232" id="tgt2" class="tgtSentence">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="c1e8f4632684ae54e59b9c160150a8b5" id="tgt3" class="tgtSentence">The returned Recordset is displayed in Internet Explorer using a <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ab10a49da87594fba9e1e53553c2f7fb" id="tgt4" class="tgtSentence">The following steps are necessary to create this scenario: </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="3d510b0d5b7b324c2b8dd7ff2f11d1ba" id="tgt5" class="tgtSentence">Set Up the Application </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="349c98e4b669f79c58ae1263d1886e36" id="tgt6" class="tgtSentence">Get the Data </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="965123e8f085099c013f1e24c283326a" id="tgt7" class="tgtSentence">Send the Data </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="aa84e34b326d3df6b805b769adaea072" id="tgt8" class="tgtSentence">Receive and Display the Data </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="2d1a4be5aea863de54a984d55e08b0c0" id="tgt9" class="tgtSentence">Step 1: Set Up the Application</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="383f908d5e7c6d052271f8547a5e2d79" id="tgt10" class="tgtSentence">Create an IIS virtual directory named "XMLPersist" with script permissions.</caps:sentence>
            <caps:sentence sentenceid="a77c238bbff94770513f687422f18b81" id="tgt11" class="tgtSentence"> Create two new text files in the folder to which the virtual directory points, one named "XMLResponse.asp," the other named "Default.htm."</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b58e8e9722ef2ca59dfb3dbc720dae41" id="tgt12" class="tgtSentence">Step 2: Get the Data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c57f55ec81bd498462182695ef32a91d" id="tgt13" class="tgtSentence">In this step, you will write the code to open an ADO Recordset and prepare to send it to the client.</caps:sentence>
            <caps:sentence sentenceid="405811a0b57f895999fe422161802ac5" id="tgt14" class="tgtSentence"> Open the file XMLResponse.asp with a text editor, such as Notepad, and insert the following code.</caps:sentence>
          </para>
          <code>&lt;%@ language="VBScript" %&gt;

&lt;!-- #include file='adovbs.inc' --&gt;

&lt;%
  Dim strSQL, strCon
  Dim adoRec 
  Dim adoCon 
  Dim xmlDoc 

  ' You will need to change "MySQLServer" below to the name of the SQL 
  ' server machine to which you want to connect.
  strCon = "Provider=sqloledb;Data Source=MySQLServer;Initial Catalog=Pubs;Integrated Security=SSPI;"
  Set adoCon = server.createObject("ADODB.Connection")
  adoCon.Open strCon

  strSQL = "SELECT Title, Price FROM Titles ORDER BY Price"
  Set adoRec = Server.CreateObject("ADODB.Recordset")
  adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText</code>
          <para>
            <caps:sentence sentenceid="db12d0f7bec7c1fdf4216cafefb3c2c0" id="tgt15" class="tgtSentence">Be sure to change the value of the<codeInline> Data Source </codeInline>parameter in<codeInline> strCon </codeInline>to the name of your Microsoft SQL Server computer.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e472c37de52eaca7885f11ff3dc7d284" id="tgt16" class="tgtSentence">Keep the file open and go on to the next step.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="41deef9d70aadf5328569f6cbb212e03" id="tgt17" class="tgtSentence">Step 3: Send the Data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2ca50ae26943b25a45f317b41b91d193" id="tgt18" class="tgtSentence">Now that you have a Recordset, you must send it to the client by saving it as XML to the ASP Response object.</caps:sentence>
            <caps:sentence sentenceid="50001e2428b648e165b257dcd7daa91f" id="tgt19" class="tgtSentence"> Add the following code to the bottom of XMLResponse.asp.</caps:sentence>
          </para>
          <code>  Response.ContentType = "text/xml"
  Response.Expires = 0
  Response.Buffer = False


  Response.Write "&lt;?xml version='1.0'?&gt;" &amp; vbNewLine
  adoRec.save Response, adPersistXML
  adoRec.Close
  Set adoRec=Nothing
%&gt;</code>
          <para>
            <caps:sentence sentenceid="7c686c884e3ecd4c191634251c4a492b" id="tgt20" class="tgtSentence">Notice that the ASP Response object is specified as the destination for the Recordset <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>.</caps:sentence>
            <caps:sentence sentenceid="37591d3f7bdc7c373882b2228515c8eb" id="tgt21" class="tgtSentence"> The destination of the Save method can be any object that supports the IStream interface, such as an ADO <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object (ADO)</link>, or a file name that includes the complete path to which the Recordset is to be saved.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8540a6877943baddd2be0c42fa90c699" id="tgt22" class="tgtSentence">Save and close XMLResponse.asp before going to the next step.</caps:sentence>
            <caps:sentence sentenceid="864697048c5f9396342ba67fa66e5adb" id="tgt23" class="tgtSentence"> Also copy the adovbs.inc file from the default ADO library installation folder to the same folder where you saved the XMLResponse.asp file.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="50cbe6959e2ec315286e2b57242204b4" id="tgt24" class="tgtSentence">Step 4: Receive and Display the Data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e0740efa00e8121f1cfdc95ae488fec6" id="tgt25" class="tgtSentence">In this step you will create an HTML file with an embedded <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link> object that points at the XMLResponse.asp file to get the Recordset.</caps:sentence>
            <caps:sentence sentenceid="b9d1ae6f177277f02dbb092891ce4a53" id="tgt26" class="tgtSentence"> Open default.htm with a text editor, such as Notepad, and add the following code.</caps:sentence>
            <caps:sentence sentenceid="07dd93e1b9988c6993eea82dcfec3100" id="tgt27" class="tgtSentence"> Replace "sqlserver" in the URL with the name of your server.</caps:sentence>
          </para>
          <code>&lt;HTML&gt;
&lt;HEAD&gt;&lt;TITLE&gt;ADO Recordset Persistence Sample&lt;/TITLE&gt;&lt;/HEAD&gt;
&lt;BODY&gt;

&lt;TABLE DATASRC="#RDC1" border="1"&gt;
  &lt;TR&gt;
&lt;TD&gt;&lt;SPAN DATAFLD="title"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
&lt;TD&gt;&lt;SPAN DATAFLD="price"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TABLE&gt;
&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"&gt;
   &lt;PARAM NAME="URL" VALUE="XMLResponse.asp"&gt;
&lt;/OBJECT&gt;

&lt;/BODY&gt;
&lt;/HTML&gt;</code>
          <para>
            <caps:sentence sentenceid="24f55a95081ebf47d7a4b38111eb8334" id="tgt28" class="tgtSentence">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</caps:sentence>
            <caps:sentence sentenceid="6ab648d8a8abbbc34530418bb376fea5" id="tgt29" class="tgtSentence"> Using Internet Explorer 4.0 or later, open the URL http://<placeholder>sqlserver</placeholder>/XMLPersist/default.htm and observe the results.</caps:sentence>
            <caps:sentence sentenceid="3b9e23ff692a47fb04c280ee30c3acd1" id="tgt30" class="tgtSentence"> The data is displayed in a bound DHTML table.</caps:sentence>
            <caps:sentence sentenceid="a3c5e9e9f2ae57870c3c45d6f67f368e" id="tgt31" class="tgtSentence"> Now open the URL http://<placeholder> sqlserver</placeholder> /XMLPersist/XMLResponse.asp and observe the results.</caps:sentence>
            <caps:sentence sentenceid="e1036f4b5cbf3a0ab62326f4af97c067" id="tgt32" class="tgtSentence"> The XML is displayed.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a Recordset object directly to the ASP Response object.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src2" class="srcSentence">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src3" class="srcSentence">The returned Recordset is displayed in Internet Explorer using a <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">The following steps are necessary to create this scenario: </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Set Up the Application </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Get the Data </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Send the Data </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Receive and Display the Data </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Step 1: Set Up the Application</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">Create an IIS virtual directory named "XMLPersist" with script permissions.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Create two new text files in the folder to which the virtual directory points, one named "XMLResponse.asp," the other named "Default.htm."</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Step 2: Get the Data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">In this step, you will write the code to open an ADO Recordset and prepare to send it to the client.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> Open the file XMLResponse.asp with a text editor, such as Notepad, and insert the following code.</caps:sentence>
          </para>
          <code>&lt;%@ language="VBScript" %&gt;

&lt;!-- #include file='adovbs.inc' --&gt;

&lt;%
  Dim strSQL, strCon
  Dim adoRec 
  Dim adoCon 
  Dim xmlDoc 

  ' You will need to change "MySQLServer" below to the name of the SQL 
  ' server machine to which you want to connect.
  strCon = "Provider=sqloledb;Data Source=MySQLServer;Initial Catalog=Pubs;Integrated Security=SSPI;"
  Set adoCon = server.createObject("ADODB.Connection")
  adoCon.Open strCon

  strSQL = "SELECT Title, Price FROM Titles ORDER BY Price"
  Set adoRec = Server.CreateObject("ADODB.Recordset")
  adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText</code>
          <para>
            <caps:sentence id="src15" class="srcSentence">Be sure to change the value of the<codeInline> Data Source </codeInline>parameter in<codeInline> strCon </codeInline>to the name of your Microsoft SQL Server computer.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">Keep the file open and go on to the next step.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src17" class="srcSentence">Step 3: Send the Data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src18" class="srcSentence">Now that you have a Recordset, you must send it to the client by saving it as XML to the ASP Response object.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> Add the following code to the bottom of XMLResponse.asp.</caps:sentence>
          </para>
          <code>  Response.ContentType = "text/xml"
  Response.Expires = 0
  Response.Buffer = False


  Response.Write "&lt;?xml version='1.0'?&gt;" &amp; vbNewLine
  adoRec.save Response, adPersistXML
  adoRec.Close
  Set adoRec=Nothing
%&gt;</code>
          <para>
            <caps:sentence id="src20" class="srcSentence">Notice that the ASP Response object is specified as the destination for the Recordset <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> The destination of the Save method can be any object that supports the IStream interface, such as an ADO <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object (ADO)</link>, or a file name that includes the complete path to which the Recordset is to be saved.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">Save and close XMLResponse.asp before going to the next step.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> Also copy the adovbs.inc file from the default ADO library installation folder to the same folder where you saved the XMLResponse.asp file.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Step 4: Receive and Display the Data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">In this step you will create an HTML file with an embedded <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link> object that points at the XMLResponse.asp file to get the Recordset.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> Open default.htm with a text editor, such as Notepad, and add the following code.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> Replace "sqlserver" in the URL with the name of your server.</caps:sentence>
          </para>
          <code>&lt;HTML&gt;
&lt;HEAD&gt;&lt;TITLE&gt;ADO Recordset Persistence Sample&lt;/TITLE&gt;&lt;/HEAD&gt;
&lt;BODY&gt;

&lt;TABLE DATASRC="#RDC1" border="1"&gt;
  &lt;TR&gt;
&lt;TD&gt;&lt;SPAN DATAFLD="title"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
&lt;TD&gt;&lt;SPAN DATAFLD="price"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
  &lt;/TR&gt;
&lt;/TABLE&gt;
&lt;OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"&gt;
   &lt;PARAM NAME="URL" VALUE="XMLResponse.asp"&gt;
&lt;/OBJECT&gt;

&lt;/BODY&gt;
&lt;/HTML&gt;</code>
          <para>
            <caps:sentence id="src28" class="srcSentence">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> Using Internet Explorer 4.0 or later, open the URL http://<placeholder>sqlserver</placeholder>/XMLPersist/default.htm and observe the results.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> The data is displayed in a bound DHTML table.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> Now open the URL http://<placeholder> sqlserver</placeholder> /XMLPersist/XMLResponse.asp and observe the results.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> The XML is displayed.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
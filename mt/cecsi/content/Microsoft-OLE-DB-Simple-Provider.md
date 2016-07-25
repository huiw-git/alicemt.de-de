---
title: "Microsoft OLE DB Simple Provider"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1e7dc6f0-482c-4103-8187-f890865e40fc
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
# Microsoft OLE DB Simple Provider
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3149c0614026cb006e4ffcdee90aaefb" id="tgt1" class="tgtSentence">The Microsoft OLE DB Simple Provider (OSP) allows ADO to access any data for which a provider has been written using the <legacyLink xlink:href="6e7b7931-9e4a-4151-ae51-672abd3f84a6">OLE DB Simple Provider (OSP) Toolkit</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="d48cfc524e600d9dcccb8eba01cad678" id="tgt2" class="tgtSentence"> Simple providers are intended to access data sources that require only fundamental OLE DB support, such as in-memory arrays or XML documents.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="df209e37fa6496886af7a164ca15b629" id="tgt3" class="tgtSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="10aeacecf8bd8f4142b26ad476855217" id="tgt4" class="tgtSentence">To connect to the OLE DB Simple Provider DLL, set the <legacyItalic>Provider</legacyItalic> argument to the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>MSDAOSP</code>
          <para>
            <caps:sentence sentenceid="a4158cf50f1c5612aa8cb2bda17ec97e" id="tgt5" class="tgtSentence">This value can also be set or read using the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8a56c95ae66e3182149113abfee2216f" id="tgt6" class="tgtSentence">You can connect to simple providers that have been registered as full OLE DB providers by using the registered provider name, determined by the provider writer.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5cf5a4267aa499f9dca0d6e5a90731cb" id="tgt7" class="tgtSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5c9e747ddd8663400e6e4b231a6386e6" id="tgt8" class="tgtSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=MSDAOSP;Data Source=<legacyItalic xmlns="">serverName</legacyItalic>"</code>
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
                    <caps:sentence sentenceid="b67e7103c22e71aaba94f62e51dd552d" id="tgt13" class="tgtSentence">Specifies the OLE DB provider for SQL Server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5f0262ef78817e828a92d75e9749b4f9" id="tgt14" class="tgtSentence">Data Source</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bca77fc94f1fee61d5a14249e9ebb490" id="tgt15" class="tgtSentence">Specifies the name of a server.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0c09c02023e3001aaf0b529eb28b39a6" id="tgt16" class="tgtSentence">XML Document Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d8e23b65ae298b2ea1063344173c9b01" id="tgt17" class="tgtSentence">The OLE DB Simple Provider (OSP) in MDAC 2.7 or later and Windows Data Access Components (Windows DAC) has been enhanced to support opening hierarchical ADO <legacyBold>Recordsets</legacyBold> over arbitrary XML files.</caps:sentence>
            <caps:sentence sentenceid="30627ce67b8463d0f8bff2c7ba14e9e9" id="tgt18" class="tgtSentence"> These XML files may contain the ADO XML persistence schema, but it is not required.</caps:sentence>
            <caps:sentence sentenceid="2632923785300f4481a6daf5a1ea6469" id="tgt19" class="tgtSentence"> This has been implemented by connecting the OSP to the <legacyBold>MSXML2.DLL</legacyBold>; therefore <legacyBold>MSXML2.DLL</legacyBold> or later is required.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dc2ff75d9fa260d39ca2d69e2abdbd7b" id="tgt20" class="tgtSentence">The <legacyBold>portfolio.xml</legacyBold> file used in the following example contains the following tree:</caps:sentence>
          </para>
          <code>Portfolio
   Stock
      Shares
      Symbol
      Price
      Info
         Company Name
         WebSite</code>
          <para>
            <caps:sentence sentenceid="aa33daa53f2f7a907e6b1f16b89fa5f3" id="tgt21" class="tgtSentence">The XML DSO uses built-in heuristics to convert the nodes in an XML tree to chapters in a hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d0833b2fb0c9bc96780cb7ef5c083930" id="tgt22" class="tgtSentence">Using these built-in heuristics, the XML tree is converted into a two-level hierarchical <legacyBold>Recordset</legacyBold> of the following form:</caps:sentence>
          </para>
          <code>Parent Recordset
Shares, Symbol, Price, $Text
   Child Recordset
      Company Name, WebSite, $Text</code>
          <para>
            <caps:sentence sentenceid="e54df57ad1559cfeaa3ad3b914c5c2c3" id="tgt23" class="tgtSentence">Note that the Portfolio and Info tags are not represented in the hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="e1338a35075be7e453bf9ad8380017fe" id="tgt24" class="tgtSentence"> For an explanation of how the XML DSO converts XML trees to hierarchical <legacyBold>Recordsets</legacyBold>, see the following rules.</caps:sentence>
            <caps:sentence sentenceid="487787288a1d788948aaac0b9ef3a407" id="tgt25" class="tgtSentence"> The $Text column is discussed in the following section.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ac91ac53c89fb9e8104027801c6f439d" id="tgt26" class="tgtSentence">Rules for Assigning XML Elements and Attributes to Columns and Rows</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="136d344752a90f4276feb00bbb4db418" id="tgt27" class="tgtSentence">The XML DSO follows a procedure for assigning elements and attributes to columns and rows in data-bound applications.</caps:sentence>
            <caps:sentence sentenceid="48acaf098de03de35ecafd9d45208e8b" id="tgt28" class="tgtSentence"> XML is modeled as a tree with one tag that contains the entire hierarchy.</caps:sentence>
            <caps:sentence sentenceid="c7a5bda5de7febd694c963f746467352" id="tgt29" class="tgtSentence"> For example, an XML description of a book could contain chapter tags, figure tags, and section tags.</caps:sentence>
            <caps:sentence sentenceid="fe384dc4f8a1d7c40e5d6d6eeb10985e" id="tgt30" class="tgtSentence"> At the highest level would be the book tag, containing the subelements chapter, figure, and section.</caps:sentence>
            <caps:sentence sentenceid="e4084944c04cb7c27ac3140c9ed118dc" id="tgt31" class="tgtSentence"> When the XML DSO maps XML elements to rows and columns, the subelements, not the top level element, are converted.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="66965037300279fd7ae7f21587b5dfe1" id="tgt32" class="tgtSentence">The XML DSO uses this procedure for converting the subelements:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="0c4d62a9cf059d6ec7b6ac01b33f8358" id="tgt33" class="tgtSentence">Each subelement and attribute corresponds to a column in some <legacyBold>Recordset</legacyBold> in the hierarchy.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8b0ab141e4a8728a497a797284924100" id="tgt34" class="tgtSentence">The name of the column is the same as the name of the subelement or attribute, unless the parent element has an attribute and a subelement with the same name, in which case a "!" is prepended to the subelement's column name.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b7905acac6595e9b3f07620d1b6ebf93" id="tgt35" class="tgtSentence">Each column is either a <legacyItalic>simple</legacyItalic> column that contains scalar values (usually strings) or a <legacyBold>Recordset</legacyBold> column that contains child <legacyBold>Recordsets</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7f0ab6ca744ee0dab61861faba57cd5b" id="tgt36" class="tgtSentence">Columns corresponding to attributes are always simple.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="90ca0bca7cc6b9c8d098b465d6a42de9" id="tgt37" class="tgtSentence">Columns corresponding to subelements are <legacyBold>Recordset</legacyBold> columns if either the subelement has its own subelements or attributes (or both), or the subelement's parent has more than one instance of the subelement as a child.</caps:sentence>
                <caps:sentence sentenceid="3eddbfd47770b9093c4353ea1201b94c" id="tgt38" class="tgtSentence"> Otherwise the column is simple.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8ba53d63cb5e0b5c2bcac2ec109afb94" id="tgt39" class="tgtSentence">When there are multiple instances of a subelement (under different parents), its column is a <legacyBold>Recordset</legacyBold> column if <legacyItalic>any</legacyItalic> of the instances imply a <legacyBold>Recordset</legacyBold> column; its column is simple only if <legacyItalic>all</legacyItalic> instances imply a simple column.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="33f0d5a81cfcac1adccea2625f3ab41c" id="tgt40" class="tgtSentence">All <legacyBold>Recordsets</legacyBold> have an additional column named $Text.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ec9cdf1353cf04af34b2104cf408af6c" id="tgt41" class="tgtSentence">The code that is needed to construct a <legacyBold>Recordset</legacyBold> is as follows:</caps:sentence>
          </para>
          <code>   Dim adoConn as ADODB.Connection
   Dim adoRS as ADODB.Recordset

   Set adoRS = New ADODB.Connection
   Set adoRS = New ADODB.Recordset

   adoConn.Open "Provider=MSDAOSP; Data Source=MSXML2.DSOControl.2.6;"
   adoRS.Open "http://WebServer/VRoot/portfolio.xml, adoConn</code>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="04223e7a57bc14bd714cc51257e5350c" id="tgt42" class="tgtSentence">The path of the data file can be specified by using four different naming conventions.</caps:sentence>
            </para>
          </alert>
          <code>   'HTTP://
   adoRS.Open "http://WebServer/VRoot/portfolio.xml", adoConn
   'FILE://
   adoRS.Open "file:/// C:\\Directory\\portfolio.xml", adoConn
   'UNC Path
   adoRS.Open "\\ComputerName\ShareName\portfolio.xml", adoConn
   'Full DOS Path
   adoRS.Open "C:\Directory\portfolio.xml", adoConn</code>
          <para>
            <caps:sentence sentenceid="68408f9dc214e4f157389eb9031e537a" id="tgt43" class="tgtSentence">As soon as the <legacyBold>Recordset</legacyBold> has been opened, the usual ADO <legacyBold>Recordset</legacyBold> navigation commands can be used.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="45c0947f864c5a66c0d6728ab4b24883" id="tgt44" class="tgtSentence">
              <legacyBold>Recordsets</legacyBold> generated by the OSP have a few limitations:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="5729d01fdbe6e6e6376c43ac13683a3c" id="tgt45" class="tgtSentence">Client cursors (<legacyBold>adUseClient</legacyBold>) are not supported.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="590ca76f452667b796b44507687addbb" id="tgt46" class="tgtSentence">Hierarchical <legacyBold>Recordsets</legacyBold> created over arbitrary XML cannot be persisted using <legacyBold>Recordset.Save</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a5090de4856a9c875b60e4d7bd9aad9e" id="tgt47" class="tgtSentence">
                  <legacyBold>Recordsets</legacyBold> created with the OSP are read-only.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b09a2c2b738c86c6d20ed2b013f1394a" id="tgt48" class="tgtSentence">The XMLDSO adds an additional column of Data ($Text) to each <legacyBold>Recordset</legacyBold> in the Hierarchy.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="b4fc21f7170daff22ac0117cf76c5e81" id="tgt49" class="tgtSentence">For more information about the OLE DB Simple Provider, see <legacyLink xlink:href="b31a6cba-58ae-4ee8-9039-700973d354d6">Building a Simple Provider</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ee38d030cb55f8804b04d9303b59184a" id="tgt50" class="tgtSentence">Code Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b6dc9121b39a5989009d8966527d6727" id="tgt51" class="tgtSentence">The following Visual Basic code demonstrates opening an arbitrary XML file, constructing a hierarchical <legacyBold>Recordset</legacyBold>, and recursively writing each record of each <legacyBold>Recordset</legacyBold> to the debug window.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b588b8800377dd4815515aafc8c0e152" id="tgt52" class="tgtSentence">Here is a simple XML file that contains stock quotes.</caps:sentence>
            <caps:sentence sentenceid="e8ceb2c29c422395f78756a750dc9c8e" id="tgt53" class="tgtSentence"> The following code uses this file to construct a two-level hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <code>&lt;portfolio&gt;
   &lt;stock&gt;
      &lt;shares&gt;100&lt;/shares&gt;
      &lt;symbol&gt;MSFT&lt;/symbol&gt;
      &lt;price&gt;$70.00&lt;/price&gt;
      &lt;info&gt;
         &lt;companyname&gt;Microsoft Corporation&lt;/companyname&gt;
         &lt;website&gt;http://www.microsoft.com&lt;/website&gt;
      &lt;/info&gt;
   &lt;/stock&gt;
   &lt;stock&gt;
      &lt;shares&gt;100&lt;/shares&gt;
      &lt;symbol&gt;AAPL&lt;/symbol&gt;
      &lt;price&gt;$107.00&lt;/price&gt;
      &lt;info&gt;
         &lt;companyname&gt;Apple Computer, Inc.&lt;/companyname&gt;
         &lt;website&gt;http://www.apple.com&lt;/website&gt;
      &lt;/info&gt;
   &lt;/stock&gt;
   &lt;stock&gt;
      &lt;shares&gt;100&lt;/shares&gt;
      &lt;symbol&gt;DELL&lt;/symbol&gt;
      &lt;price&gt;$50.00&lt;/price&gt;
      &lt;info&gt;
         &lt;companyname&gt;Dell Corporation&lt;/companyname&gt;
         &lt;website&gt;http://www.dell.com&lt;/website&gt;
      &lt;/info&gt;
    &lt;/stock&gt;
    &lt;stock&gt;
       &lt;shares&gt;100&lt;/shares&gt;
       &lt;symbol&gt;INTC&lt;/symbol&gt;
       &lt;price&gt;$115.00&lt;/price&gt;
       &lt;info&gt;
          &lt;companyname&gt;Intel Corporation&lt;/companyname&gt;
          &lt;website&gt;http://www.intel.com&lt;/website&gt;
       &lt;/info&gt;
   &lt;/stock&gt;
&lt;/portfolio&gt;</code>
          <para>
            <caps:sentence sentenceid="33e0ca5f4651f54b92b8066dff222160" id="tgt54" class="tgtSentence">Following are two Visual Basic sub procedures.</caps:sentence>
            <caps:sentence sentenceid="cafedfd153cf273c768a47252793e56a" id="tgt55" class="tgtSentence"> The first creates the <legacyBold>Recordset</legacyBold> and passes it to the <legacyItalic>WalkHier</legacyItalic> sub procedure, which recursively walks down the hierarchy, writing each <legacyBold>Field</legacyBold> in each record in each <legacyBold>Recordset</legacyBold> to the debug window.</caps:sentence>
          </para>
          <code>Private Sub BrowseHierRecordset()
' Add ADO 2.7 or later to Project/References
' No need to add MSXML2, ADO just passes the ProgID through to the OSP.

    Dim adoConn As ADODB.Connection
    Dim adoRS As ADODB.Recordset
    Dim adoChildRS As ADODB.Recordset
        
    Set adoConn = New ADODB.Connection
    Set adoRS = New ADODB.Recordset
    Set adoChildRS = ADODB.Recordset

    adoConn.Open "Provider=MSDAOSP; Data Source=MSXML2.DSOControl.2.6;"
    adoRS.Open "http://bwillett3/Kowalski/portfolio.xml", adoConn
       
    Dim iLevel As Integer
    iLevel = 0
    WalkHier iLevel, adoRS
                          
End Sub

Sub WalkHier(ByVal iLevel As Integer, ByVal adoRS As ADODB.Recordset)
    iLevel = iLevel + 1
    PriorLevel = iLevel
    While Not adoRS.EOF
        For ndx = 0 To adoRS.Fields.Count - 1
            If adoRS.Fields(ndx).Name &lt;&gt; "$Text" Then
                If adoRS.Fields(ndx).Type = adChapter Then
                    Set adoChildRS = adoRS.Fields(ndx).Value
                    WalkHier iLevel, adoChildRS
                Else
                    Debug.Print iLevel &amp; ": adoRS.Fields(" &amp; ndx &amp; _
                       ") = " &amp; adoRS.Fields(ndx).Name &amp; " = " &amp; _
                       adoRS.Fields(ndx).Value
                End If
            End If
        Next ndx
        adoRS.MoveNext
    Wend
    iLevel = PriorLevel
End Sub</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Microsoft OLE DB Simple Provider (OSP) allows ADO to access any data for which a provider has been written using the <legacyLink xlink:href="6e7b7931-9e4a-4151-ae51-672abd3f84a6">OLE DB Simple Provider (OSP) Toolkit</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Simple providers are intended to access data sources that require only fundamental OLE DB support, such as in-memory arrays or XML documents.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">To connect to the OLE DB Simple Provider DLL, set the <legacyItalic>Provider</legacyItalic> argument to the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>MSDAOSP</code>
          <para>
            <caps:sentence id="src5" class="srcSentence">This value can also be set or read using the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">You can connect to simple providers that have been registered as full OLE DB providers by using the registered provider name, determined by the provider writer.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=MSDAOSP;Data Source=<legacyItalic xmlns="">serverName</legacyItalic>"</code>
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
                    <caps:sentence id="src13" class="srcSentence">Specifies the OLE DB provider for SQL Server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src14" class="srcSentence">Data Source</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Specifies the name of a server.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">XML Document Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">The OLE DB Simple Provider (OSP) in MDAC 2.7 or later and Windows Data Access Components (Windows DAC) has been enhanced to support opening hierarchical ADO <legacyBold>Recordsets</legacyBold> over arbitrary XML files.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> These XML files may contain the ADO XML persistence schema, but it is not required.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> This has been implemented by connecting the OSP to the <legacyBold>MSXML2.DLL</legacyBold>; therefore <legacyBold>MSXML2.DLL</legacyBold> or later is required.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">The <legacyBold>portfolio.xml</legacyBold> file used in the following example contains the following tree:</caps:sentence>
          </para>
          <code>Portfolio
   Stock
      Shares
      Symbol
      Price
      Info
         Company Name
         WebSite</code>
          <para>
            <caps:sentence id="src21" class="srcSentence">The XML DSO uses built-in heuristics to convert the nodes in an XML tree to chapters in a hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">Using these built-in heuristics, the XML tree is converted into a two-level hierarchical <legacyBold>Recordset</legacyBold> of the following form:</caps:sentence>
          </para>
          <code>Parent Recordset
Shares, Symbol, Price, $Text
   Child Recordset
      Company Name, WebSite, $Text</code>
          <para>
            <caps:sentence id="src23" class="srcSentence">Note that the Portfolio and Info tags are not represented in the hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> For an explanation of how the XML DSO converts XML trees to hierarchical <legacyBold>Recordsets</legacyBold>, see the following rules.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> The $Text column is discussed in the following section.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src26" class="srcSentence">Rules for Assigning XML Elements and Attributes to Columns and Rows</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src27" class="srcSentence">The XML DSO follows a procedure for assigning elements and attributes to columns and rows in data-bound applications.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> XML is modeled as a tree with one tag that contains the entire hierarchy.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> For example, an XML description of a book could contain chapter tags, figure tags, and section tags.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> At the highest level would be the book tag, containing the subelements chapter, figure, and section.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> When the XML DSO maps XML elements to rows and columns, the subelements, not the top level element, are converted.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">The XML DSO uses this procedure for converting the subelements:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">Each subelement and attribute corresponds to a column in some <legacyBold>Recordset</legacyBold> in the hierarchy.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">The name of the column is the same as the name of the subelement or attribute, unless the parent element has an attribute and a subelement with the same name, in which case a "!" is prepended to the subelement's column name.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">Each column is either a <legacyItalic>simple</legacyItalic> column that contains scalar values (usually strings) or a <legacyBold>Recordset</legacyBold> column that contains child <legacyBold>Recordsets</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">Columns corresponding to attributes are always simple.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src37" class="srcSentence">Columns corresponding to subelements are <legacyBold>Recordset</legacyBold> columns if either the subelement has its own subelements or attributes (or both), or the subelement's parent has more than one instance of the subelement as a child.</caps:sentence>
                <caps:sentence id="src38" class="srcSentence"> Otherwise the column is simple.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src39" class="srcSentence">When there are multiple instances of a subelement (under different parents), its column is a <legacyBold>Recordset</legacyBold> column if <legacyItalic>any</legacyItalic> of the instances imply a <legacyBold>Recordset</legacyBold> column; its column is simple only if <legacyItalic>all</legacyItalic> instances imply a simple column.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src40" class="srcSentence">All <legacyBold>Recordsets</legacyBold> have an additional column named $Text.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src41" class="srcSentence">The code that is needed to construct a <legacyBold>Recordset</legacyBold> is as follows:</caps:sentence>
          </para>
          <code>   Dim adoConn as ADODB.Connection
   Dim adoRS as ADODB.Recordset

   Set adoRS = New ADODB.Connection
   Set adoRS = New ADODB.Recordset

   adoConn.Open "Provider=MSDAOSP; Data Source=MSXML2.DSOControl.2.6;"
   adoRS.Open "http://WebServer/VRoot/portfolio.xml, adoConn</code>
          <alert class="note">
            <para>
              <caps:sentence id="src42" class="srcSentence">The path of the data file can be specified by using four different naming conventions.</caps:sentence>
            </para>
          </alert>
          <code>   'HTTP://
   adoRS.Open "http://WebServer/VRoot/portfolio.xml", adoConn
   'FILE://
   adoRS.Open "file:/// C:\\Directory\\portfolio.xml", adoConn
   'UNC Path
   adoRS.Open "\\ComputerName\ShareName\portfolio.xml", adoConn
   'Full DOS Path
   adoRS.Open "C:\Directory\portfolio.xml", adoConn</code>
          <para>
            <caps:sentence id="src43" class="srcSentence">As soon as the <legacyBold>Recordset</legacyBold> has been opened, the usual ADO <legacyBold>Recordset</legacyBold> navigation commands can be used.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src44" class="srcSentence">
              <legacyBold>Recordsets</legacyBold> generated by the OSP have a few limitations:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src45" class="srcSentence">Client cursors (<legacyBold>adUseClient</legacyBold>) are not supported.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src46" class="srcSentence">Hierarchical <legacyBold>Recordsets</legacyBold> created over arbitrary XML cannot be persisted using <legacyBold>Recordset.Save</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src47" class="srcSentence">
                  <legacyBold>Recordsets</legacyBold> created with the OSP are read-only.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src48" class="srcSentence">The XMLDSO adds an additional column of Data ($Text) to each <legacyBold>Recordset</legacyBold> in the Hierarchy.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src49" class="srcSentence">For more information about the OLE DB Simple Provider, see <legacyLink xlink:href="b31a6cba-58ae-4ee8-9039-700973d354d6">Building a Simple Provider</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src50" class="srcSentence">Code Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src51" class="srcSentence">The following Visual Basic code demonstrates opening an arbitrary XML file, constructing a hierarchical <legacyBold>Recordset</legacyBold>, and recursively writing each record of each <legacyBold>Recordset</legacyBold> to the debug window.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src52" class="srcSentence">Here is a simple XML file that contains stock quotes.</caps:sentence>
            <caps:sentence id="src53" class="srcSentence"> The following code uses this file to construct a two-level hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <code>&lt;portfolio&gt;
   &lt;stock&gt;
      &lt;shares&gt;100&lt;/shares&gt;
      &lt;symbol&gt;MSFT&lt;/symbol&gt;
      &lt;price&gt;$70.00&lt;/price&gt;
      &lt;info&gt;
         &lt;companyname&gt;Microsoft Corporation&lt;/companyname&gt;
         &lt;website&gt;http://www.microsoft.com&lt;/website&gt;
      &lt;/info&gt;
   &lt;/stock&gt;
   &lt;stock&gt;
      &lt;shares&gt;100&lt;/shares&gt;
      &lt;symbol&gt;AAPL&lt;/symbol&gt;
      &lt;price&gt;$107.00&lt;/price&gt;
      &lt;info&gt;
         &lt;companyname&gt;Apple Computer, Inc.&lt;/companyname&gt;
         &lt;website&gt;http://www.apple.com&lt;/website&gt;
      &lt;/info&gt;
   &lt;/stock&gt;
   &lt;stock&gt;
      &lt;shares&gt;100&lt;/shares&gt;
      &lt;symbol&gt;DELL&lt;/symbol&gt;
      &lt;price&gt;$50.00&lt;/price&gt;
      &lt;info&gt;
         &lt;companyname&gt;Dell Corporation&lt;/companyname&gt;
         &lt;website&gt;http://www.dell.com&lt;/website&gt;
      &lt;/info&gt;
    &lt;/stock&gt;
    &lt;stock&gt;
       &lt;shares&gt;100&lt;/shares&gt;
       &lt;symbol&gt;INTC&lt;/symbol&gt;
       &lt;price&gt;$115.00&lt;/price&gt;
       &lt;info&gt;
          &lt;companyname&gt;Intel Corporation&lt;/companyname&gt;
          &lt;website&gt;http://www.intel.com&lt;/website&gt;
       &lt;/info&gt;
   &lt;/stock&gt;
&lt;/portfolio&gt;</code>
          <para>
            <caps:sentence id="src54" class="srcSentence">Following are two Visual Basic sub procedures.</caps:sentence>
            <caps:sentence id="src55" class="srcSentence"> The first creates the <legacyBold>Recordset</legacyBold> and passes it to the <legacyItalic>WalkHier</legacyItalic> sub procedure, which recursively walks down the hierarchy, writing each <legacyBold>Field</legacyBold> in each record in each <legacyBold>Recordset</legacyBold> to the debug window.</caps:sentence>
          </para>
          <code>Private Sub BrowseHierRecordset()
' Add ADO 2.7 or later to Project/References
' No need to add MSXML2, ADO just passes the ProgID through to the OSP.

    Dim adoConn As ADODB.Connection
    Dim adoRS As ADODB.Recordset
    Dim adoChildRS As ADODB.Recordset
        
    Set adoConn = New ADODB.Connection
    Set adoRS = New ADODB.Recordset
    Set adoChildRS = ADODB.Recordset

    adoConn.Open "Provider=MSDAOSP; Data Source=MSXML2.DSOControl.2.6;"
    adoRS.Open "http://bwillett3/Kowalski/portfolio.xml", adoConn
       
    Dim iLevel As Integer
    iLevel = 0
    WalkHier iLevel, adoRS
                          
End Sub

Sub WalkHier(ByVal iLevel As Integer, ByVal adoRS As ADODB.Recordset)
    iLevel = iLevel + 1
    PriorLevel = iLevel
    While Not adoRS.EOF
        For ndx = 0 To adoRS.Fields.Count - 1
            If adoRS.Fields(ndx).Name &lt;&gt; "$Text" Then
                If adoRS.Fields(ndx).Type = adChapter Then
                    Set adoChildRS = adoRS.Fields(ndx).Value
                    WalkHier iLevel, adoChildRS
                Else
                    Debug.Print iLevel &amp; ": adoRS.Fields(" &amp; ndx &amp; _
                       ") = " &amp; adoRS.Fields(ndx).Name &amp; " = " &amp; _
                       adoRS.Fields(ndx).Value
                End If
            End If
        Next ndx
        adoRS.MoveNext
    Wend
    iLevel = PriorLevel
End Sub</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Microsoft OLE DB Provider for SQL Server"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 99bc40c4-9181-4ca1-a06f-9a1a914a0b7b
caps.latest.revision: 18
caps.handback.revision: 18
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
# Microsoft OLE DB Provider for SQL Server
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="88700e1813f81db3e6a4cee9d4313e68" id="tgt1" class="tgtSentence">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="df209e37fa6496886af7a164ca15b629" id="tgt2" class="tgtSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="dd07dd3bde388a53935bab83143aed20" id="tgt3" class="tgtSentence">To connect to this provider, set the <legacyItalic>Provider</legacyItalic> argument to the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>SQLOLEDB</code>
          <para>
            <caps:sentence sentenceid="a4158cf50f1c5612aa8cb2bda17ec97e" id="tgt4" class="tgtSentence">This value can also be set or read using the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5cf5a4267aa499f9dca0d6e5a90731cb" id="tgt5" class="tgtSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5c9e747ddd8663400e6e4b231a6386e6" id="tgt6" class="tgtSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=SQLOLEDB;Data Source=<legacyItalic xmlns="">serverName</legacyItalic>;"
Initial Catalog=<legacyItalic xmlns="">databaseName</legacyItalic>;
User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence sentenceid="61333c54636d561759b12d35ff08c05b" id="tgt7" class="tgtSentence">The string consists of these keywords:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7df5b64df1181ef1d62d646a13aa860" id="tgt8" class="tgtSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt9" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9e9f3d70bd8c8957627eada96d967706" id="tgt10" class="tgtSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b67e7103c22e71aaba94f62e51dd552d" id="tgt11" class="tgtSentence">Specifies the OLE DB Provider for SQL Server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="086584c8658dc4080c83fc97443c652c" id="tgt12" class="tgtSentence">
                      <legacyBold>Data Source</legacyBold> or <legacyBold>Server</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bca77fc94f1fee61d5a14249e9ebb490" id="tgt13" class="tgtSentence">Specifies the name of a server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0a91c00d92ac82b403e450f139f3aad8" id="tgt14" class="tgtSentence">
                      <legacyBold>Initial Catalog</legacyBold> or <legacyBold>Database</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a3865785b5e5654e7afec41016b72e1c" id="tgt15" class="tgtSentence">Specifies the name of a database on the server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d0cb5a17395c677053e612df040f9105" id="tgt16" class="tgtSentence">
                      <legacyBold>User ID</legacyBold> or <legacyBold>uid</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="153ae02db8f04c4d046884160b6765bd" id="tgt17" class="tgtSentence">Specifies the user name (for SQL Server Authentication).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="560bb3030325a95e5eb185eaacb83b91" id="tgt18" class="tgtSentence">
                      <legacyBold>Password</legacyBold> or <legacyBold>pwd</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="353dbded03f2c73f05e2ba136e2cab86" id="tgt19" class="tgtSentence">Specifies the user password (for SQL Server Authentication).</caps:sentence>
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
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b3a258973c03d77c4dc730b82e250514" id="tgt21" class="tgtSentence">Provider-Specific Connection Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b8b3eb1e5b5a0ec3d20283d6a73f91af" id="tgt22" class="tgtSentence">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</caps:sentence>
            <caps:sentence sentenceid="e3f354abf3db4ecfb4e85dbc5c26865e" id="tgt23" class="tgtSentence"> As with the ADO connection properties, these provider-specific properties can be set via the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> or can be set as part of the <legacyBold>ConnectionString</legacyBold>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt24" class="tgtSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt25" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af080cfa2f50d17838bfc02768188a01" id="tgt26" class="tgtSentence">Trusted_Connection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfb0204948f7e9ef3118f4b7b3dc9e90" id="tgt27" class="tgtSentence">Indicates the user authentication mode.</caps:sentence>
                    <caps:sentence sentenceid="4e9663ecde03f0cab669a23f6931d3cc" id="tgt28" class="tgtSentence"> This can be set to <legacyBold>Yes</legacyBold> or <legacyBold>No</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="fe6c45c65d462beef76ffef94761b773" id="tgt29" class="tgtSentence"> The default value is <legacyBold>No</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="3ffb9e07f9bcc0301ac932b0a8aebb58" id="tgt30" class="tgtSentence"> If this property is set to <legacyBold>Yes</legacyBold>, SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <legacyBold>Location</legacyBold> and <legacyLink xlink:href="300a702a-3544-48c5-b759-83b511fe97e0">Datasource</legacyLink> property values.</caps:sentence>
                    <caps:sentence sentenceid="2e7719617bb3866a07226666195b5937" id="tgt31" class="tgtSentence"> If this property is set to <legacyBold>No</legacyBold>, SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database.</caps:sentence>
                    <caps:sentence sentenceid="051a373ab3c295a6f079902a68e7a58d" id="tgt32" class="tgtSentence"> The SQL Server login and password are specified in the <legacyBold>User Id</legacyBold> and <legacyBold>Password</legacyBold> properties.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e65003e22ba8c684bb914bcb23bf9562" id="tgt33" class="tgtSentence">Current Language</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adf09dd8d78e3ac3e0ce9b5a3e6516f0" id="tgt34" class="tgtSentence">Indicates a SQL Server language name.</caps:sentence>
                    <caps:sentence sentenceid="6cd3b142a96a3bc9f702f85d1e55614b" id="tgt35" class="tgtSentence"> Identifies the language used for system message selection and formatting.</caps:sentence>
                    <caps:sentence sentenceid="cf2c248d2bda0b16e302de71322657e6" id="tgt36" class="tgtSentence"> The language must be installed on the SQL Server, otherwise opening the connection will fail.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e924aba67094eeb9bdf29ccb0847df65" id="tgt37" class="tgtSentence">Network Address</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b3f767cf0737fb51b5d8db968e0aa78" id="tgt38" class="tgtSentence">Indicates the network address of the SQL Server specified by the <legacyBold>Location</legacyBold> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="432a2c941ab752ebe163cc75d996ed1c" id="tgt39" class="tgtSentence">Network Library</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="844207a1c6928babf5e5ef66c8702fea" id="tgt40" class="tgtSentence">Indicates the name of the network library (DLL) used to communicate with the SQL Server.</caps:sentence>
                    <caps:sentence sentenceid="04bbacbe172646baad195226a53f58f6" id="tgt41" class="tgtSentence"> The name should not include the path or the .dll file name extension.</caps:sentence>
                    <caps:sentence sentenceid="c5659ae9142389bc6fbbf0cc5a34fe24" id="tgt42" class="tgtSentence"> The default is provided by the SQL Server client configuration.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1689835d8ca770a8db62f6b9312babc3" id="tgt43" class="tgtSentence">Use Procedure for Prepare</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d41357c4e56dfcec9005289b3f957165" id="tgt44" class="tgtSentence">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <legacyBold>Prepared</legacyBold> property).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1262f52ac9e749cdcfac54e7dca77901" id="tgt45" class="tgtSentence">Auto Translate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16ae7b27301cdccd90da3372802101fa" id="tgt46" class="tgtSentence">Indicates whether OEM/ANSI characters are converted.</caps:sentence>
                    <caps:sentence sentenceid="4e0d8f8d30f2708607bdecb4788ca1a2" id="tgt47" class="tgtSentence"> This property can be set to <legacyBold>True</legacyBold> or <legacyBold>False</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="fbf7504507f27d80e983defad4f9930c" id="tgt48" class="tgtSentence"> The default value is <legacyBold>True</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="7347975debc6bc5af33e4a9202414133" id="tgt49" class="tgtSentence"> If this property is set to <legacyBold>True</legacyBold>, SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server.</caps:sentence>
                    <caps:sentence sentenceid="b524d7bc3eac86188614b9ec9f14baa6" id="tgt50" class="tgtSentence"> If this property is set to <legacyBold>False</legacyBold>, SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="57e495775672b6a544b97df285e507c0" id="tgt51" class="tgtSentence">Packet Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7049621da6d8d6fecd85c85393ad5d96" id="tgt52" class="tgtSentence">Indicates a network packet size in bytes.</caps:sentence>
                    <caps:sentence sentenceid="7b351a7515ee4e1f4aa6735a0e0087b4" id="tgt53" class="tgtSentence"> The packet size property value must be between 512 and 32767.</caps:sentence>
                    <caps:sentence sentenceid="48bdf13d0a66c3db645ecb4c18d1b7f1" id="tgt54" class="tgtSentence"> The default SQLOLEDB network packet size is 4096.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9c4ba7de5291e9bcb2f085edb00cd28f" id="tgt55" class="tgtSentence">Application Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5bfa3b2b01c942fcc6c8c9c1191320f9" id="tgt56" class="tgtSentence">Indicates the client application name.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e739602f14161d4abae8f167ce46fb25" id="tgt57" class="tgtSentence">Workstation ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0830aa0e618c4afca51fe3956227b2e8" id="tgt58" class="tgtSentence">A string identifying the workstation.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="e0f00fb1715bd624b7380c4fbaf0e694" id="tgt59" class="tgtSentence">Command Object Usage</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="942e5cdbf9707bdd38413e553ff3a1e7" id="tgt60" class="tgtSentence">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax.</caps:sentence>
            <caps:sentence sentenceid="8358b810f800901b5eaab671f74c351b" id="tgt61" class="tgtSentence"> For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</caps:sentence>
          </para>
          <code>SELECT customerid={fn LCASE(CustomerID)} FROM Customers
  </code>
          <para>
            <caps:sentence sentenceid="1e38fb3694dc9e38236942b4156d3db8" id="tgt62" class="tgtSentence">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents.</caps:sentence>
            <caps:sentence sentenceid="a84f31b9fb3fba79a3a4d97ebb2dd8b4" id="tgt63" class="tgtSentence"> The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented earlier:</caps:sentence>
          </para>
          <code>SELECT customerid=LOWER(CustomerID) FROM Customers
  </code>
          <para>
            <caps:sentence sentenceid="5581843958828955e173002af1f27bd2" id="tgt64" class="tgtSentence">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="6956f0ba2e2305f6da719c51319830f7" id="tgt65" class="tgtSentence">Stored Procedures</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4304f1aeef7c78492bfdd2e85da933fc" id="tgt66" class="tgtSentence">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text.</caps:sentence>
            <caps:sentence sentenceid="5417c4cb393e6e7d2f21c3537a8653f0" id="tgt67" class="tgtSentence"> SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing.</caps:sentence>
            <caps:sentence sentenceid="6b360fdae054d83e063375b9b8808364" id="tgt68" class="tgtSentence"> For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f52dcc8b11ca579bdc3d6cf7a7a3d520" id="tgt69" class="tgtSentence">ODBC SQL</caps:sentence>
        </title>
        <content>
          <code>{call SalesByCategory('Produce', '1995')}
  </code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="145d441656ead2cd19e2c650f0666a78" id="tgt70" class="tgtSentence">Transact-SQL</caps:sentence>
        </title>
        <content>
          <code>EXECUTE SalesByCategory 'Produce', '1995'
  </code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f2783be7be0a6039473c3a0666584e46" id="tgt71" class="tgtSentence">SQL Server Features</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cfc14d7ba74a205c9870f81378a48c8d" id="tgt72" class="tgtSentence">With SQL Server, ADO can use XML for <legacyBold>Command</legacyBold> input and retrieve results in XML stream format instead of in <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="bbdedf56fcf70d74b662ffded338f6ec" id="tgt73" class="tgtSentence"> For more information, see <legacyLink xlink:href="0ac09dbe-2665-411e-8fbb-d1efe6c777be">Using Streams for Command Input</legacyLink> and <legacyLink xlink:href="996c1321-c926-4f57-8297-85c8c20de974">Retrieving Resultsets Into Streams</legacyLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="80843aadf1ef6acaa13a5a65441e1540" id="tgt74" class="tgtSentence">Accessing sql_variant data using MDAC 2.7, MDAC 2.8, or Windows DAC 6.0</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="87719ee06d488ed384b348847d301ac9" id="tgt75" class="tgtSentence">Microsoft SQL Server has a data type called <legacyBold>sql_variant</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="0a58a53966df92f6b49c1cc70eb57370" id="tgt76" class="tgtSentence"> Similar to OLE DB's <legacyBold>DBTYPE_VARIANT</legacyBold>, the <legacyBold>sql_variant</legacyBold> data type can store data of several different types.</caps:sentence>
                <caps:sentence sentenceid="00d83d3992e8d429fb4a90e99102de09" id="tgt77" class="tgtSentence"> However, there are a few key differences between <legacyBold>DBTYPE_VARIANT</legacyBold> and <legacyBold>sql_variant</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="28896fd73c8e006eb7aa3bf95013c143" id="tgt78" class="tgtSentence"> ADO also handles data stored as a <legacyBold>sql_variant</legacyBold> value differently than how it handles other data types.</caps:sentence>
                <caps:sentence sentenceid="fdf3347e6d8a763eb3f58cbbbac80e5d" id="tgt79" class="tgtSentence"> The following list describes issues to consider when you access SQL Server data stored in columns of type <legacyBold>sql_variant</legacyBold>.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="13286fc8d26788fcefa4668340fdd36a" id="tgt80" class="tgtSentence">In MDAC 2.7, MDAC 2.8, and Windows Data Access Components (Windows DAC) 6.0, the OLE DB Provider for SQL Server supports the <legacyBold>sql_variant</legacyBold> type.</caps:sentence>
                    <caps:sentence sentenceid="eec66622b2743e19460d8d3ee241481b" id="tgt81" class="tgtSentence"> The OLE DB Provider for ODBC does not.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1f15317ad03f23df972841df006b7419" id="tgt82" class="tgtSentence">The <legacyBold>sql_variant</legacyBold> type does not exactly match the <legacyBold>DBTYPE_VARIANT</legacyBold> data type.</caps:sentence>
                    <caps:sentence sentenceid="7687b2ee4baad0a57e9f33e4f8bb59ca" id="tgt83" class="tgtSentence">  The <legacyBold>sql_variant</legacyBold> type supports a few new subtypes not supported by <legacyBold>DBTYPE_VARIANT,</legacyBold> including <legacyBold>GUID</legacyBold>, <legacyBold>ANSI</legacyBold> (non-UNICODE) strings, and <legacyBold>BIGINT</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="c2d1bdd59779f4f4a9c3ea6a312fe3d8" id="tgt84" class="tgtSentence"> Using subtypes other than those listed earlier will work correctly.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6dd442afad5e7d78cd4c77a2808d1f19" id="tgt85" class="tgtSentence">The <legacyBold>sql_variant</legacyBold> subtype <legacyBold>NUMERIC</legacyBold> does not match the <legacyBold>DBTYPE_DECIMAL</legacyBold> in size.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="038799a81de5f18963d568438a5e3a07" id="tgt86" class="tgtSentence">Multiple data type coercions will result in types that do not match.</caps:sentence>
                    <caps:sentence sentenceid="f40ea3a26209806c164ac1a58c4c7a94" id="tgt87" class="tgtSentence"> For example, coercing a <legacyBold>sql_variant</legacyBold> with a subtype of <legacyBold>GUID</legacyBold> to a <legacyBold>DBTYPE_VARIANT</legacyBold> will result in a subtype of <legacyBold>safearray</legacyBold>(bytes).</caps:sentence>
                    <caps:sentence sentenceid="ba94303b908bc796e9183f4d6042ff95" id="tgt88" class="tgtSentence"> Converting this type back to a <legacyBold>sql_variant</legacyBold> will result in a new subtype of <legacyBold>array</legacyBold>(bytes).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a8f3f6865960974bfa6cb20105656fe3" id="tgt89" class="tgtSentence">  <legacyBold>Recordset</legacyBold> fields that contain <legacyBold>sql_variant</legacyBold> data can be remoted (marshaled) or persisted only if the <legacyBold>sql_variant</legacyBold> contains specific subtypes.</caps:sentence>
                    <caps:sentence sentenceid="ba51b88ab98c40170f4399c627d45eee" id="tgt90" class="tgtSentence"> Attempting to remote or persist data with the following unsupported subtypes will cause a run-time error (unsupported conversion) from the Microsoft Persistence Provider (MSPersist): <legacyBold>VT_VARIANT</legacyBold>, <legacyBold>VT_RECORD</legacyBold>, <legacyBold>VT_ILLEGAL</legacyBold>, <legacyBold>VT_UNKNOWN</legacyBold>, <legacyBold>VT_BSTR</legacyBold>, and <legacyBold>VT_DISPATCH.</legacyBold></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="529fc0db9714500ab4d43451041ea755" id="tgt91" class="tgtSentence">The OLE DB Provider for SQL Server in MDAC 2.7, MDAC 2.8, and Windows DAC 6.0 has a dynamic property called <legacyBold>Allow Native Variants</legacyBold> which, as the name implies, allows developers to access the <legacyBold>sql_variant</legacyBold> in its native form as opposed to a <legacyBold>DBTYPE_VARIANT</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="d29a7905bebb6622a8a21b0065ccec41" id="tgt92" class="tgtSentence"> If this property is set, and a <legacyBold>Recordset</legacyBold> is opened with the Client Cursor Engine (<legacyBold>adUseClient</legacyBold>), the <legacyBold>Recordset.Open</legacyBold> call will fail.</caps:sentence>
                    <caps:sentence sentenceid="0f3f77e3d59eecadf4be2d73c63fb498" id="tgt93" class="tgtSentence"> If this property is set and a <legacyBold>Recordset</legacyBold> is opened with server cursors (<legacyBold>adUseServer</legacyBold>), the <legacyBold>Recordset.Open</legacyBold> call will succeed, but accessing columns of type <legacyBold>sql_variant</legacyBold> will produce an error.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ac2bf5e7aa8b599c4020badfedd50688" id="tgt94" class="tgtSentence">In client applications that use MDAC 2.5, <legacyBold>sql_variant </legacyBold>data can be used with queries against Microsoft SQL Server.</caps:sentence>
                    <caps:sentence sentenceid="00531713e48ee462e0463eeb323c2a99" id="tgt95" class="tgtSentence"> However, the values of the <legacyBold>sql_variant</legacyBold> data are treated as strings.</caps:sentence>
                    <caps:sentence sentenceid="74a813014c91d3312e598ae4d063e865" id="tgt96" class="tgtSentence"> Such client applications should be upgraded to MDAC 2.7, MDAC 2.8, or Windows DAC 6.0.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="002c1a21d972a03f6b6e5a266dd56653" id="tgt97" class="tgtSentence">Recordset Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1e81c3529c88b540a2963339e36d9f39" id="tgt98" class="tgtSentence">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands.</caps:sentence>
            <caps:sentence sentenceid="ad86a44f2fad3637da3af84f7c76534a" id="tgt99" class="tgtSentence"> If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="203e0c13105c014db949b91ddc2449bf" id="tgt100" class="tgtSentence">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors.</caps:sentence>
            <caps:sentence sentenceid="ee4aa0c09146a18c8cd1aa46f9edfd08" id="tgt101" class="tgtSentence"> SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database.</caps:sentence>
            <caps:sentence sentenceid="865afc388d8b9e86d26ac9c3cb69490c" id="tgt102" class="tgtSentence"> Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c9cc4b2425ec47fd6141efc88965a1d3" id="tgt103" class="tgtSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="fd5a4f9e6f98315cd87631f3ca965ac8" id="tgt104" class="tgtSentence">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the <legacyBold>Properties</legacyBold> collection of the unopened <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c4d70f669b7e7098098781d22c2f0183" id="tgt105" class="tgtSentence">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</caps:sentence>
            <caps:sentence sentenceid="eef9bb2f9882c6c20042f23692a999c0" id="tgt106" class="tgtSentence"> The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</caps:sentence>
            <caps:sentence sentenceid="5bd6c2a248f991e5772ecf53ac580449" id="tgt107" class="tgtSentence"> You can find more information about these properties in the OLE DB Programmer's Reference.</caps:sentence>
            <caps:sentence sentenceid="dd922c21aeab8495b30148842cb8d125" id="tgt108" class="tgtSentence"> Search for the OLE DB property name in the Index or see <legacyLink xlink:href="deded3ff-f508-4e1b-b2b1-fd9afd3bd292">Appendix C: OLE DB Properties</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="cc03d661ba78db29ad696232fbdfd45d" id="tgt109" class="tgtSentence">Connection Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="66ad75c6de7e35fcc78d16fd0db075f8" id="tgt110" class="tgtSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt111" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt112" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42da7b3adedde15ba58b5e8f720f0729" id="tgt113" class="tgtSentence">Active Sessions</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5db97e3405ada5593894afe7c26e912a" id="tgt114" class="tgtSentence">DBPROP_ACTIVESESSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5fb6f6fbeeed9d35163820f4cad357a5" id="tgt115" class="tgtSentence">Asynchable Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a69ebf5e5b867b80a10c033ec247f235" id="tgt116" class="tgtSentence">DBPROP_ASYNCTXNABORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1553c09566f739d416c34417c3eed8bc" id="tgt117" class="tgtSentence">Asynchable Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8fb4c7f494cd85116f18f4e23dfa3ce2" id="tgt118" class="tgtSentence">DBPROP_ASYNCTNXCOMMIT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ac1b75d9d496be787670b775f6cbc81" id="tgt119" class="tgtSentence">Autocommit Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ed9f459c36be0b771e14849bddd615a" id="tgt120" class="tgtSentence">DBPROP_SESS_AUTOCOMMITISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04e7adcf92320728ff99be4ae9e20b80" id="tgt121" class="tgtSentence">Catalog Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cc7d88f9c70b084ff349547378be6ea7" id="tgt122" class="tgtSentence">DBPROP_CATALOGLOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0d5a9974623ad1d08ec1a87d28e3382b" id="tgt123" class="tgtSentence">Catalog Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5ec52858196e5661e26c0593dc0055f3" id="tgt124" class="tgtSentence">DBPROP_CATALOGTERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ccf0f62c35ce6f4ad47c504191cbc48" id="tgt125" class="tgtSentence">Column Definition</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4036e684cbb10c6c00160fb3f89fec78" id="tgt126" class="tgtSentence">DBPROP_COLUMNDEFINITION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf6acbf359c2d19032f195b15434cbdf" id="tgt127" class="tgtSentence">Connect Timeout</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb371d4f9db6357d81826f393345882e" id="tgt128" class="tgtSentence">DBPROP_INIT_TIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6cf2a5823099e39d4bfcd079068b384d" id="tgt129" class="tgtSentence">Current Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1975407cf7846b03983297436f6feaec" id="tgt130" class="tgtSentence">DBPROP_CURRENTCATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f0262ef78817e828a92d75e9749b4f9" id="tgt131" class="tgtSentence">Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f628f4ca9169da470c6349e4dadfd7b" id="tgt132" class="tgtSentence">DBPROP_INIT_DATASOURCE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4cc4008aeaa109c055aa7289fe8955f6" id="tgt133" class="tgtSentence">Data Source Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f70e2b308e36cc86cb62a25d0cc89d0" id="tgt134" class="tgtSentence">DBPROP_DATASOURCENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0902cf5b7d19a0cc4c0d745125932c99" id="tgt135" class="tgtSentence">Data Source Object Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6168b0502be04b450b621cc21978b79" id="tgt136" class="tgtSentence">DBPROP_DSOTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44576fc26ad5240af73f0f7304ac0161" id="tgt137" class="tgtSentence">DBMS Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8bfb66db9f6b9a9d8249efb32f35bc2" id="tgt138" class="tgtSentence">DBPROP_DBMSNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0865166992725c390cf3955eb7005314" id="tgt139" class="tgtSentence">DBMS Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="91a28922f266288ed023d4fb5e1a9f41" id="tgt140" class="tgtSentence">DBPROP_DBMSVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="01a074046ca4de7469fdd27ef0f56b30" id="tgt141" class="tgtSentence">Extended Properties</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ad981c384f6deb06078fb96a4f6db4af" id="tgt142" class="tgtSentence">DBPROP_INIT_PROVIDERSTRING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fc489b2e87836669c99f48d36447d508" id="tgt143" class="tgtSentence">GROUP BY Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b73b41cab609c063b7570db22674bb0" id="tgt144" class="tgtSentence">DBPROP_GROUPBY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7970e9c2391aaf6904a12c0b64590ee7" id="tgt145" class="tgtSentence">Heterogeneous Table Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8732f1c0c3c20adc7bc8f5f878f4e95f" id="tgt146" class="tgtSentence">DBPROP_HETEROGENEOUSTABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3cc7d428494725fbc1c4117841759a1b" id="tgt147" class="tgtSentence">Identifier Case Sensitivity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f959d99f6f9ff2380e84ed5f89a6545" id="tgt148" class="tgtSentence">DBPROP_IDENTIFIERCASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d61a95016e0ce8932a33ae801954fdbe" id="tgt149" class="tgtSentence">Initial Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="966c4e343eb272d1b5309d5b41dcd77e" id="tgt150" class="tgtSentence">DBPROP_INIT_CATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6d922da801c791516e0fde80744ddda1" id="tgt151" class="tgtSentence">Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b826970c6bc792cec29c7154b97b055f" id="tgt152" class="tgtSentence">DBPROP_SUPPORTEDTXNISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="36d2944c902a8b3bfc937a35534e6d67" id="tgt153" class="tgtSentence">Isolation Retention</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1180eb611191e300302c020a0433017a" id="tgt154" class="tgtSentence">DBPROP_SUPPORTEDTXNISORETAIN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d42b4f73ee8bf025a3c06cfa5499f55" id="tgt155" class="tgtSentence">Locale Identifier</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a119da28f65a0343b705f027db4eb589" id="tgt156" class="tgtSentence">DBPROP_INIT_LCID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d632dbafbc50f25c220bda2bd1d5eb79" id="tgt157" class="tgtSentence">Maximum Index Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0a5f4509b189658a32142048499fb311" id="tgt158" class="tgtSentence">DBPROP_MAXINDEXSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a3cbd82a49b4e695c986f9e21e08bec0" id="tgt159" class="tgtSentence">Maximum Row Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6414b671b9497a028ae03e2ff2baa8a2" id="tgt160" class="tgtSentence">DBPROP_MAXROWSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3fe8d182c92e2a2da388835b24f6a538" id="tgt161" class="tgtSentence">Maximum Row Size Includes BLOB</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82a79937366130603485b2e8243110f3" id="tgt162" class="tgtSentence">DBPROP_MAXROWSIZEINCLUDESBLOB</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="72fa89be4e41d4eec9682e3012510c70" id="tgt163" class="tgtSentence">Maximum Tables in SELECT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12775fa00655f15737d2b126875edf54" id="tgt164" class="tgtSentence">DBPROP_MAXTABLESINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5fa88b3a7f2866a505f6869084d9dbac" id="tgt165" class="tgtSentence">Multiple Parameter Sets</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5b07a57182c870a463947bbe8862f2a" id="tgt166" class="tgtSentence">DBPROP_MULTIPLEPARAMSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34467f0701793e142a97280886a37d11" id="tgt167" class="tgtSentence">Multiple Results</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c6d16a5ed96ee324aaea5d56f93b9ca" id="tgt168" class="tgtSentence">DBPROP_MULTIPLERESULTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94a2500d5a620b62d088ba5e147f9300" id="tgt169" class="tgtSentence">Multiple Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4d0892bbf21bca8cbb05c7688e4481a" id="tgt170" class="tgtSentence">DBPROP_MULTIPLESTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49a7ede339dd477496917e520e53b211" id="tgt171" class="tgtSentence">Multi-Table Update</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45718feaf0858fc05c6e2c5653af9fa5" id="tgt172" class="tgtSentence">DBPROP_MULTITABLEUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="068577c6d2defffb1af7047830fb7e89" id="tgt173" class="tgtSentence">NULL Collation Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="169e04896d93bdec8bd59547b5636cf4" id="tgt174" class="tgtSentence">DBPROP_NULLCOLLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="51a10c8ee8acbdda689781c851e4dbfb" id="tgt175" class="tgtSentence">NULL Concatenation Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="86d53a1e665c382405ca707e70950ee9" id="tgt176" class="tgtSentence">DBPROP_CONCATNULLBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54d02916d0ddd080374282c66901c59c" id="tgt177" class="tgtSentence">OLE DB Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8678185cda69da06b0b18cdede8c9aaf" id="tgt178" class="tgtSentence">DBPROP_PROVIDEROLEDBVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c77b810e588a10689239bf12710a9027" id="tgt179" class="tgtSentence">OLE Object Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9aa0a480916fc5befab6d11935037f12" id="tgt180" class="tgtSentence">DBPROP_OLEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="305717e26f640fcebb5c11bdf62692b0" id="tgt181" class="tgtSentence">Open Rowset Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="467a15dbf1a07da68a090197a6350d8e" id="tgt182" class="tgtSentence">DBPROP_OPENROWSETSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d8d10a19d6045a2990194103e79da9e6" id="tgt183" class="tgtSentence">ORDER BY Columns in Select List</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17519abd080309120a91fbe406545057" id="tgt184" class="tgtSentence">DBPROP_ORDERBYCOLUMNSINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c8bdd56df539c7147de1a6309ccf033" id="tgt185" class="tgtSentence">Output Parameter Availability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b3bb7f1b82d23d1accfa030b4372da90" id="tgt186" class="tgtSentence">DBPROP_OUTPUTPARAMETERAVAILABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ec1f372d153601374fe2b3be37c84a7" id="tgt187" class="tgtSentence">Pass By Ref Accessors</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b063a15f21255c314931eb858f8c898" id="tgt188" class="tgtSentence">DBPROP_BYREFACCESSORS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f4dcc3b5aa765d61d8327deb882cf99" id="tgt189" class="tgtSentence">Password</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a4dad287f50102726dc53803031a610a" id="tgt190" class="tgtSentence">DBPROP_AUTH_PASSWORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="503154ffbc8d4b9909f934dd562a5753" id="tgt191" class="tgtSentence">Persist Security Info</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7902596f88afd8b04b6b61fc09d1a39e" id="tgt192" class="tgtSentence">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d99d60bd887e031a71ff6eff10d6d3d4" id="tgt193" class="tgtSentence">Persistent ID Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ea254ecd2f23ef9f83d15db428137a57" id="tgt194" class="tgtSentence">DBPROP_PERSISTENTIDTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="77b5b43a8424c46e81df1ab0fc6e466d" id="tgt195" class="tgtSentence">Prepare Abort Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c461cd8da2a2986434667ac22d8c4113" id="tgt196" class="tgtSentence">DBPROP_PREPAREABORTBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc732b57d8b179ab01d66f1adcddf935" id="tgt197" class="tgtSentence">Prepare Commit Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5956c34c7c59de311a271e3cc843ced" id="tgt198" class="tgtSentence">DBPROP_PREPARECOMMITBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b307899aa47ab53211ca988c38acf75e" id="tgt199" class="tgtSentence">Procedure Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39fca27d3fe2656d61424456d445849b" id="tgt200" class="tgtSentence">DBPROP_PROCEDURETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ae35dbb42614d2429b7d6d181a950bb" id="tgt201" class="tgtSentence">Prompt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a23c8807135a34f56166fc290ce391c" id="tgt202" class="tgtSentence">DBPROP_INIT_PROMPT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ebbb5df827311326b2ebdcd6cf839f95" id="tgt203" class="tgtSentence">Provider Friendly Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="590bff2f7b8796e1277a936f16a2a7ff" id="tgt204" class="tgtSentence">DBPROP_PROVIDERFRIENDLYNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe158741a51803d31ec342eea567a79" id="tgt205" class="tgtSentence">Provider Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af443c478802f07802f2dc40b36c12b0" id="tgt206" class="tgtSentence">DBPROP_PROVIDERFILENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6ee1f505ae87ddc1ca51166091edec7" id="tgt207" class="tgtSentence">Provider Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d547dd6794dc65d1cbc34bc9a3646cab" id="tgt208" class="tgtSentence">DBPROP_PROVIDERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="14bb11993e3371d739eebc9648db4ec8" id="tgt209" class="tgtSentence">Read-Only Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fbaa45e63afd58892cad4204394e4b4a" id="tgt210" class="tgtSentence">DBPROP_DATASOURCEREADONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b68e1280ee9c56976f9918f1b143ae9b" id="tgt211" class="tgtSentence">Rowset Conversions on Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e9ea492c28f4f9e0ebe6ab7b04499f0a" id="tgt212" class="tgtSentence">DBPROP_ROWSETCONVERSIONSONCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4e214d42f27db2df22d820f4339ab38" id="tgt213" class="tgtSentence">Schema Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="177617f0fc571a0b532c7358fec97041" id="tgt214" class="tgtSentence">DBPROP_SCHEMATERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="996b43fdeae58150436e00ab086e55f9" id="tgt215" class="tgtSentence">Schema Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af6ca7abc5e28a6ba9bc5998e88fc4de" id="tgt216" class="tgtSentence">DBPROP_SCHEMAUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3887b124c8b8b2ac1076ac2fbc50a5a8" id="tgt217" class="tgtSentence">SQL Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67a078a8eabce39c390405b03eaf82df" id="tgt218" class="tgtSentence">DBPROP_SQLSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82b1c99e1276c7b9329843b82cb249a2" id="tgt219" class="tgtSentence">Structured Storage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a912ffa112b5c65343d1368268679294" id="tgt220" class="tgtSentence">DBPROP_STRUCTUREDSTORAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a51c825ecd8a692b685d0736d13a30c8" id="tgt221" class="tgtSentence">Subquery Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2dc44fc06f6f61c8b1e7f8c8b1dc7226" id="tgt222" class="tgtSentence">DBPROP_SUBQUERIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1fa0c9780d8a58f26e201af8cdc9d7d5" id="tgt223" class="tgtSentence">Table Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c25b152bb6a5d33613780d82b09f83f" id="tgt224" class="tgtSentence">DBPROP_TABLETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26e3db30e914b1bf231f1dc48149a6ab" id="tgt225" class="tgtSentence">Transaction DDL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d94fb60768ed9e61630670c5b707db5e" id="tgt226" class="tgtSentence">DBPROP_SUPPORTEDTXNDDL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3bd756a1167a9bff574b512092d53350" id="tgt227" class="tgtSentence">User ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d9c5665b97893aac40b03266365060d" id="tgt228" class="tgtSentence">DBPROP_AUTH_USERID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f28564ce8593a50b9cf507aecccd8cd6" id="tgt229" class="tgtSentence">User Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0673f982c2e13e63312a0a61aed98966" id="tgt230" class="tgtSentence">DBPROP_USERNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98487bfe9fe529e4a2738b2ad9eacaec" id="tgt231" class="tgtSentence">Window Handle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3a92acd985b6ab8b1df6d3cd4df47e83" id="tgt232" class="tgtSentence">DBPROP_INIT_HWND</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0d8dea92a1ae91e40f5bc79d56f722e5" id="tgt233" class="tgtSentence">Recordset Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b6adcadd64667e5ca7f3654365be92fe" id="tgt234" class="tgtSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt235" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt236" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1594fad277e4590ddbbf46e340c4d10c" id="tgt237" class="tgtSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3ae70d0cfd08d73c0e8657de04e3ba3" id="tgt238" class="tgtSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b52683364c551ef6f2a83a9b61aca26" id="tgt239" class="tgtSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7eade57591bcbdf71a01307c5fa55333" id="tgt240" class="tgtSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39674232a2f3f57e87b6f56e9fcd620c" id="tgt241" class="tgtSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c5692554e1273a4cc28709961881f78" id="tgt242" class="tgtSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab13a6b41c0fedc395cff5ae82b531b6" id="tgt243" class="tgtSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt244" class="tgtSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="246a7d96dd79b612bad343d03ea2bec6" id="tgt245" class="tgtSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75cbb9fc61a14afcadf102cfdd0a6733" id="tgt246" class="tgtSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="534d9e8ffeeeff5bf0f381032bbefd20" id="tgt247" class="tgtSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3eac3ca56c13d98b9d1f1d8ef5620027" id="tgt248" class="tgtSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30f3aa8c0ff671730367a69d810898b9" id="tgt249" class="tgtSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32873d7085b6feb780bf00ea59c3a386" id="tgt250" class="tgtSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="68484ede52d011ad20cc9399010ba11a" id="tgt251" class="tgtSentence">Command Time Out</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ff64c42d8e170982b23167bd7148d889" id="tgt252" class="tgtSentence">DBPROP_COMMANDTIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec83d16d5fb11f0a7e532fe6a91dfc36" id="tgt253" class="tgtSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af283d090de02b75e79bf25ce7aa945a" id="tgt254" class="tgtSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c34dec6888b6b898acb79b0597922c27" id="tgt255" class="tgtSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7906ea7eac0a5466ea33c9bf87d083db" id="tgt256" class="tgtSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c24d8cc4559e441d51781708292d746" id="tgt257" class="tgtSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b5c3be77a4c5f0654fd6637b3fd2b44" id="tgt258" class="tgtSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f518893e9bb8f74c9382260d0f79450b" id="tgt259" class="tgtSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2bdf72f0b7184d9ebe2e4086c598ee58" id="tgt260" class="tgtSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d33d5718660dbb261dc40b878ec4b591" id="tgt261" class="tgtSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fcb4539a8be17b29a97aada5fa31577" id="tgt262" class="tgtSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="28dbf41d74f2a648a563b28d2ecef878" id="tgt263" class="tgtSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba30e9909e02f6f6179f9db5cb9852cf" id="tgt264" class="tgtSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6317b9d062ca4ded11773f5df0c39062" id="tgt265" class="tgtSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12f702a41807df637765daa681fed78c" id="tgt266" class="tgtSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63e99e63156fc90f114fa402662387ef" id="tgt267" class="tgtSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="74868f1ee86eb0eaa5fb352a7f6c8f9e" id="tgt268" class="tgtSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="280d1ffb462810568a6fdc7ed49c472c" id="tgt269" class="tgtSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b34e9458e67545a04e915c7ef55719e8" id="tgt270" class="tgtSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="215599a847f963e27588b79210d3ea56" id="tgt271" class="tgtSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be4b610383a4b1af3438c855f29cb110" id="tgt272" class="tgtSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5e86d5adb921fd6e7b7616e2cc6d0b1" id="tgt273" class="tgtSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b8f2d2a246c88031ced7fa4b20e891d" id="tgt274" class="tgtSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5cf35ba4349e6da426be07d34952411e" id="tgt275" class="tgtSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37736c2f13339b1d0f75108bb2e84bd0" id="tgt276" class="tgtSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f7deea1588ac1cc7f77f6df70c1434b" id="tgt277" class="tgtSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f58d445e65ef2cd341481713e2aa6a9" id="tgt278" class="tgtSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1c6d3c5946bb65aba4e55669cac68a" id="tgt279" class="tgtSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8b178f861273bd6fcaa2cd53841838b" id="tgt280" class="tgtSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92f23aaea36b3e3b3f1b4b456d4b0f8a" id="tgt281" class="tgtSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8732f1240c2bdcfd2d50aa877ca7b299" id="tgt282" class="tgtSentence">DBPROP_IRowsestLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82189c22157ca5dbc1566ce5b8fee507" id="tgt283" class="tgtSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>              </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="151e636103f6679064656728e4630284" id="tgt284" class="tgtSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b167241425c6c09726e930d5db411617" id="tgt285" class="tgtSentence">DBPROP_IRowsetScroll</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="869692d9e5c7b7dc7dcfdaf30a7bd348" id="tgt286" class="tgtSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fda716a018fb2c9d85d7f104af6d28fa" id="tgt287" class="tgtSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fd77e41428ef2a86d5994c0a4e658f" id="tgt288" class="tgtSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6fb965f1bd078f921c5a73f084a7d09" id="tgt289" class="tgtSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="130702210bcc45e1afd88b1f2aae1a0b" id="tgt290" class="tgtSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d1813dfdbbaa1c4660b2933198fb3f7" id="tgt291" class="tgtSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34cd68a4ad9a3b16548954ff8184424c" id="tgt292" class="tgtSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbe0ebf1ce342bea12faf4f9960e35db" id="tgt293" class="tgtSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="627482c800288bba5eaa6324bec11b5a" id="tgt294" class="tgtSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8709209928583492b7e8ee9057e1dcd2" id="tgt295" class="tgtSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37f4175871594fd8b8484066ab57df1f" id="tgt296" class="tgtSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="610508ace43dba0c007eb22818d91137" id="tgt297" class="tgtSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09b385ae7a340805af12a182ddf23eb4" id="tgt298" class="tgtSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f76fd118082b0c0ce064d13a83f97d8" id="tgt299" class="tgtSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2a235cb612ded93059abe7d46a49fe3" id="tgt300" class="tgtSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db2433d929e5ee5dac5bf4e762cb10ab" id="tgt301" class="tgtSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9cf646cc11e82fcf71add13e9d665dd" id="tgt302" class="tgtSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17bc94f9006a838977a349a959373da8" id="tgt303" class="tgtSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c018979b39f45a0e004063ce0373c75f" id="tgt304" class="tgtSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00045b5ae2bb643fd385c818dc8e48c6" id="tgt305" class="tgtSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cd5ca965481ad65661cdb310d078fa3" id="tgt306" class="tgtSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7319271b36838a8630e00ceb4554a65" id="tgt307" class="tgtSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf6cb25fea1126c44957f7d00a3a2c4f" id="tgt308" class="tgtSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2e7ff400a4ef4b66e01a7d0219e3d034" id="tgt309" class="tgtSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe7ca5c576c7eb49b58dec45de3b371" id="tgt310" class="tgtSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4267002726b89c5712c11b77ab4b758" id="tgt311" class="tgtSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f08474ed3d97c8e3919ffe184b8cb02e" id="tgt312" class="tgtSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ffd196cae96727a7c58c6701e3c65c1" id="tgt313" class="tgtSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45b7a56f3096b95b93f70ce662332136" id="tgt314" class="tgtSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8d7e45b16c6a09599199e5237263f63" id="tgt315" class="tgtSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="780561121ea65efc60d011b3855083ed" id="tgt316" class="tgtSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8bbf20691fd6dfdc3b55d73bb1b4df42" id="tgt317" class="tgtSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c89b03f5c13331074eed0814571479b" id="tgt318" class="tgtSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1be32916280f74ae0b5b31424efe2e97" id="tgt319" class="tgtSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="360431977c32a0e461c2a887196342cf" id="tgt320" class="tgtSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="015f02a3c579b5978974bb340adbc2ed" id="tgt321" class="tgtSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2fee318949f99eb5f0586e8492ffbaa" id="tgt322" class="tgtSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46634a21ff13d23b96f57f1b7a8e74b3" id="tgt323" class="tgtSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af57e2554f3db187894681afa3ebb162" id="tgt324" class="tgtSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="120451667e76bd8d13d0f0fce84d89e0" id="tgt325" class="tgtSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90f54100a94260ff7c00300f6cfd91d3" id="tgt326" class="tgtSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe1dffe626e729c9881c31329af50b19" id="tgt327" class="tgtSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="993c9b2a5a406fa810a7c0a353c0241d" id="tgt328" class="tgtSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62dbebf39ca99d9e0f7d2548b1a1e897" id="tgt329" class="tgtSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="594965351c01632879dd3120d6bdf6d1" id="tgt330" class="tgtSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dacf8514ed973feacfcb951277d7a7e0" id="tgt331" class="tgtSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26a6a1d6d267ebfa661503a67852b551" id="tgt332" class="tgtSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78e460d27437866f950bef1a322f4fad" id="tgt333" class="tgtSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1082afc70d114a04c5a7c028f54bbef" id="tgt334" class="tgtSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af912945703d4c7e5769a4a5e275c429" id="tgt335" class="tgtSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e89662e8e842b5980db8ce27cddbb136" id="tgt336" class="tgtSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f0866326f49f046b4c2d341fbf8b4a8" id="tgt337" class="tgtSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1a3b43e5bc3c750c8484e75d2dc513" id="tgt338" class="tgtSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d147a76184915ab68be6596b43255f" id="tgt339" class="tgtSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d60a3e481cd7af54f8384abea4e16a7c" id="tgt340" class="tgtSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65b8fe6df5aa2933471401a6b676fba7" id="tgt341" class="tgtSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1198df197cf7df924a1b241c2b2f0043" id="tgt342" class="tgtSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18919c01495e96c385f2eaf5938a7b03" id="tgt343" class="tgtSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdb695a9cc13c0f5e2c73bda79d0aaf" id="tgt344" class="tgtSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a40c17ef17a290d8ff208c5db8518c1" id="tgt345" class="tgtSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78cbcb8d94e6c7daf9e961f93e6b2886" id="tgt346" class="tgtSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d19dc5275a879b3a434a516970425f79" id="tgt347" class="tgtSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5b98c46a74cf81a3a5714e4746025dc3" id="tgt348" class="tgtSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb5fb6c60c1d012edd101ab61e996364" id="tgt349" class="tgtSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8a7611a82fb7d9716f4f12a82fb60754" id="tgt350" class="tgtSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e51a0debee4b6fc0ca6b1e781fc16df7" id="tgt351" class="tgtSentence">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16753e39b4d45199dca719ac2995aeb1" id="tgt352" class="tgtSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="824f2ba91f8243744ab6a8227fbb157f" id="tgt353" class="tgtSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adc2bf5dd51cf373e1aacf17aef14bbd" id="tgt354" class="tgtSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ac6cf4fa0ff0c7b5050593b220d13af2" id="tgt355" class="tgtSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="415a343da7783a4dd06c09c7a67f8825" id="tgt356" class="tgtSentence">Server Cursor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfd7e7c46ce15b85949bbb20dc2eb8f6" id="tgt357" class="tgtSentence">DBPROP_SERVERCURSOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="692ef25d05bb91b856cf5d0564cf74fd" id="tgt358" class="tgtSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87f408e0686b76395d281e685f65bc08" id="tgt359" class="tgtSentence">DBPROP_BOOKMARKSKIPPED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2463d9a101f9c39973277d105f8bf119" id="tgt360" class="tgtSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b4fbfcb976445a344da1d0972764bf0d" id="tgt361" class="tgtSentence">DBPROP_STRONGITDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3d6c9ba3726667cb820e5f392952aca6" id="tgt362" class="tgtSentence">Unique Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fe0a5bebaaa20210a94be8f859bc9b3" id="tgt363" class="tgtSentence">DBPROP_UNIQUEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11c74d1c21dc5dbb8b802a7408596d87" id="tgt364" class="tgtSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2086801d6ac44d08784890faac1a126" id="tgt365" class="tgtSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7a56dd282a8abf8100c423430ec8e4ac" id="tgt366" class="tgtSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd43d482f9e85ec89014c21fbd361a4" id="tgt367" class="tgtSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="af1974d09c74dc4d634c2cdc45a0ab7c" id="tgt368" class="tgtSentence">Command Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ab4280ff216db2e6f6071ba86870ade8" id="tgt369" class="tgtSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt370" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt371" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1594fad277e4590ddbbf46e340c4d10c" id="tgt372" class="tgtSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3ae70d0cfd08d73c0e8657de04e3ba3" id="tgt373" class="tgtSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c073210692669d2119343ffa4a7becd1" id="tgt374" class="tgtSentence">Base Path</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="680a0d094c8d8e9e40abfc5ef3e59488" id="tgt375" class="tgtSentence">SSPROP_STREAM_BASEPATH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b52683364c551ef6f2a83a9b61aca26" id="tgt376" class="tgtSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7eade57591bcbdf71a01307c5fa55333" id="tgt377" class="tgtSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39674232a2f3f57e87b6f56e9fcd620c" id="tgt378" class="tgtSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c5692554e1273a4cc28709961881f78" id="tgt379" class="tgtSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab13a6b41c0fedc395cff5ae82b531b6" id="tgt380" class="tgtSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt381" class="tgtSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="246a7d96dd79b612bad343d03ea2bec6" id="tgt382" class="tgtSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75cbb9fc61a14afcadf102cfdd0a6733" id="tgt383" class="tgtSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="534d9e8ffeeeff5bf0f381032bbefd20" id="tgt384" class="tgtSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3eac3ca56c13d98b9d1f1d8ef5620027" id="tgt385" class="tgtSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30f3aa8c0ff671730367a69d810898b9" id="tgt386" class="tgtSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32873d7085b6feb780bf00ea59c3a386" id="tgt387" class="tgtSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ba981cac505bfc21adfc15465f0dcd7" id="tgt388" class="tgtSentence">Content Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c94e3c1e36511db0fbe1ee4e350f3d46" id="tgt389" class="tgtSentence">SSPROP_STREAM_CONTENTTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2934da01826b91c0cba8d48bb9a076ac" id="tgt390" class="tgtSentence">Cursor Auto Fetch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="41d4c3d7c8251ecefa6633a1b680b14e" id="tgt391" class="tgtSentence">SSPROP_CURSORAUTOFETCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec83d16d5fb11f0a7e532fe6a91dfc36" id="tgt392" class="tgtSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af283d090de02b75e79bf25ce7aa945a" id="tgt393" class="tgtSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1e3694ad03379c1c1a149f8f267c42e0" id="tgt394" class="tgtSentence">Defer Prepare</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1fd0a52aef4af8e86cd3e544b7504c57" id="tgt395" class="tgtSentence">SSPROP_DEFERPREPARE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c34dec6888b6b898acb79b0597922c27" id="tgt396" class="tgtSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7906ea7eac0a5466ea33c9bf87d083db" id="tgt397" class="tgtSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c24d8cc4559e441d51781708292d746" id="tgt398" class="tgtSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b5c3be77a4c5f0654fd6637b3fd2b44" id="tgt399" class="tgtSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f518893e9bb8f74c9382260d0f79450b" id="tgt400" class="tgtSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2bdf72f0b7184d9ebe2e4086c598ee58" id="tgt401" class="tgtSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d33d5718660dbb261dc40b878ec4b591" id="tgt402" class="tgtSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fcb4539a8be17b29a97aada5fa31577" id="tgt403" class="tgtSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="28dbf41d74f2a648a563b28d2ecef878" id="tgt404" class="tgtSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba30e9909e02f6f6179f9db5cb9852cf" id="tgt405" class="tgtSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6317b9d062ca4ded11773f5df0c39062" id="tgt406" class="tgtSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12f702a41807df637765daa681fed78c" id="tgt407" class="tgtSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63e99e63156fc90f114fa402662387ef" id="tgt408" class="tgtSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="74868f1ee86eb0eaa5fb352a7f6c8f9e" id="tgt409" class="tgtSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="280d1ffb462810568a6fdc7ed49c472c" id="tgt410" class="tgtSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b34e9458e67545a04e915c7ef55719e8" id="tgt411" class="tgtSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="215599a847f963e27588b79210d3ea56" id="tgt412" class="tgtSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be4b610383a4b1af3438c855f29cb110" id="tgt413" class="tgtSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5e86d5adb921fd6e7b7616e2cc6d0b1" id="tgt414" class="tgtSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b8f2d2a246c88031ced7fa4b20e891d" id="tgt415" class="tgtSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5cf35ba4349e6da426be07d34952411e" id="tgt416" class="tgtSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37736c2f13339b1d0f75108bb2e84bd0" id="tgt417" class="tgtSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f7deea1588ac1cc7f77f6df70c1434b" id="tgt418" class="tgtSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f58d445e65ef2cd341481713e2aa6a9" id="tgt419" class="tgtSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1c6d3c5946bb65aba4e55669cac68a" id="tgt420" class="tgtSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8b178f861273bd6fcaa2cd53841838b" id="tgt421" class="tgtSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92f23aaea36b3e3b3f1b4b456d4b0f8a" id="tgt422" class="tgtSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt423" class="tgtSentence">DBPROP_IRowsetLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82189c22157ca5dbc1566ce5b8fee507" id="tgt424" class="tgtSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f451196b58bc7c8254dd84ae4b41c41" id="tgt425" class="tgtSentence">DBPROP_IRowsetResynch</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="151e636103f6679064656728e4630284" id="tgt426" class="tgtSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b167241425c6c09726e930d5db411617" id="tgt427" class="tgtSentence">DBPROP_IRowsetScroll</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="869692d9e5c7b7dc7dcfdaf30a7bd348" id="tgt428" class="tgtSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fda716a018fb2c9d85d7f104af6d28fa" id="tgt429" class="tgtSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fd77e41428ef2a86d5994c0a4e658f" id="tgt430" class="tgtSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6fb965f1bd078f921c5a73f084a7d09" id="tgt431" class="tgtSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="130702210bcc45e1afd88b1f2aae1a0b" id="tgt432" class="tgtSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d1813dfdbbaa1c4660b2933198fb3f7" id="tgt433" class="tgtSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34cd68a4ad9a3b16548954ff8184424c" id="tgt434" class="tgtSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbe0ebf1ce342bea12faf4f9960e35db" id="tgt435" class="tgtSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="627482c800288bba5eaa6324bec11b5a" id="tgt436" class="tgtSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8709209928583492b7e8ee9057e1dcd2" id="tgt437" class="tgtSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ac2e31b5fd88afee8c9979f44a49bf9" id="tgt438" class="tgtSentence">Lock Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04b22bfa92a633895f2c4cf0391cd26a" id="tgt439" class="tgtSentence">DBPROP_LOCKMODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37f4175871594fd8b8484066ab57df1f" id="tgt440" class="tgtSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="610508ace43dba0c007eb22818d91137" id="tgt441" class="tgtSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09b385ae7a340805af12a182ddf23eb4" id="tgt442" class="tgtSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f76fd118082b0c0ce064d13a83f97d8" id="tgt443" class="tgtSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2a235cb612ded93059abe7d46a49fe3" id="tgt444" class="tgtSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db2433d929e5ee5dac5bf4e762cb10ab" id="tgt445" class="tgtSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9cf646cc11e82fcf71add13e9d665dd" id="tgt446" class="tgtSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17bc94f9006a838977a349a959373da8" id="tgt447" class="tgtSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c018979b39f45a0e004063ce0373c75f" id="tgt448" class="tgtSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00045b5ae2bb643fd385c818dc8e48c6" id="tgt449" class="tgtSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cd5ca965481ad65661cdb310d078fa3" id="tgt450" class="tgtSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7319271b36838a8630e00ceb4554a65" id="tgt451" class="tgtSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf6cb25fea1126c44957f7d00a3a2c4f" id="tgt452" class="tgtSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2e7ff400a4ef4b66e01a7d0219e3d034" id="tgt453" class="tgtSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe7ca5c576c7eb49b58dec45de3b371" id="tgt454" class="tgtSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4267002726b89c5712c11b77ab4b758" id="tgt455" class="tgtSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="02a903189811423bd175e55d1de4b175" id="tgt456" class="tgtSentence">Output Encoding Property</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="390fde0dcf7b65caddbcde5714d0ebeb" id="tgt457" class="tgtSentence">DBPROP_OUTPUTENCODING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdc84232b59846122e5cd2379cfda80" id="tgt458" class="tgtSentence">Output Stream Property</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2ccbb3a3afd4e387a334103c8cc6f96c" id="tgt459" class="tgtSentence">DBPROP_OUTPUTSTREAM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f08474ed3d97c8e3919ffe184b8cb02e" id="tgt460" class="tgtSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ffd196cae96727a7c58c6701e3c65c1" id="tgt461" class="tgtSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45b7a56f3096b95b93f70ce662332136" id="tgt462" class="tgtSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8d7e45b16c6a09599199e5237263f63" id="tgt463" class="tgtSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="780561121ea65efc60d011b3855083ed" id="tgt464" class="tgtSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8bbf20691fd6dfdc3b55d73bb1b4df42" id="tgt465" class="tgtSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c89b03f5c13331074eed0814571479b" id="tgt466" class="tgtSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1be32916280f74ae0b5b31424efe2e97" id="tgt467" class="tgtSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="360431977c32a0e461c2a887196342cf" id="tgt468" class="tgtSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="015f02a3c579b5978974bb340adbc2ed" id="tgt469" class="tgtSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2fee318949f99eb5f0586e8492ffbaa" id="tgt470" class="tgtSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46634a21ff13d23b96f57f1b7a8e74b3" id="tgt471" class="tgtSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af57e2554f3db187894681afa3ebb162" id="tgt472" class="tgtSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="120451667e76bd8d13d0f0fce84d89e0" id="tgt473" class="tgtSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90f54100a94260ff7c00300f6cfd91d3" id="tgt474" class="tgtSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe1dffe626e729c9881c31329af50b19" id="tgt475" class="tgtSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="993c9b2a5a406fa810a7c0a353c0241d" id="tgt476" class="tgtSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62dbebf39ca99d9e0f7d2548b1a1e897" id="tgt477" class="tgtSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="594965351c01632879dd3120d6bdf6d1" id="tgt478" class="tgtSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dacf8514ed973feacfcb951277d7a7e0" id="tgt479" class="tgtSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26a6a1d6d267ebfa661503a67852b551" id="tgt480" class="tgtSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78e460d27437866f950bef1a322f4fad" id="tgt481" class="tgtSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1082afc70d114a04c5a7c028f54bbef" id="tgt482" class="tgtSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af912945703d4c7e5769a4a5e275c429" id="tgt483" class="tgtSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e89662e8e842b5980db8ce27cddbb136" id="tgt484" class="tgtSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f0866326f49f046b4c2d341fbf8b4a8" id="tgt485" class="tgtSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1a3b43e5bc3c750c8484e75d2dc513" id="tgt486" class="tgtSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d147a76184915ab68be6596b43255f" id="tgt487" class="tgtSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d60a3e481cd7af54f8384abea4e16a7c" id="tgt488" class="tgtSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65b8fe6df5aa2933471401a6b676fba7" id="tgt489" class="tgtSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1198df197cf7df924a1b241c2b2f0043" id="tgt490" class="tgtSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18919c01495e96c385f2eaf5938a7b03" id="tgt491" class="tgtSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdb695a9cc13c0f5e2c73bda79d0aaf" id="tgt492" class="tgtSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a40c17ef17a290d8ff208c5db8518c1" id="tgt493" class="tgtSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78cbcb8d94e6c7daf9e961f93e6b2886" id="tgt494" class="tgtSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d19dc5275a879b3a434a516970425f79" id="tgt495" class="tgtSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5b98c46a74cf81a3a5714e4746025dc3" id="tgt496" class="tgtSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb5fb6c60c1d012edd101ab61e996364" id="tgt497" class="tgtSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8a7611a82fb7d9716f4f12a82fb60754" id="tgt498" class="tgtSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3528ed34871b6b038968af4a908dc081" id="tgt499" class="tgtSentence">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16753e39b4d45199dca719ac2995aeb1" id="tgt500" class="tgtSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="824f2ba91f8243744ab6a8227fbb157f" id="tgt501" class="tgtSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adc2bf5dd51cf373e1aacf17aef14bbd" id="tgt502" class="tgtSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ac6cf4fa0ff0c7b5050593b220d13af2" id="tgt503" class="tgtSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="415a343da7783a4dd06c09c7a67f8825" id="tgt504" class="tgtSentence">Server Cursor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfd7e7c46ce15b85949bbb20dc2eb8f6" id="tgt505" class="tgtSentence">DBPROP_SERVERCURSOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be346cc75b8dd118f2f2af71e8f65a26" id="tgt506" class="tgtSentence">Server Data on Insert</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5024c80fbef16b8c9a3cf58c2ed5e22f" id="tgt507" class="tgtSentence">DBPROP_SERVERDATAONINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="692ef25d05bb91b856cf5d0564cf74fd" id="tgt508" class="tgtSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7bffaed4f81d15733e9f3df7fcdb33a4" id="tgt509" class="tgtSentence">DBPROP_BOOKMARKSKIP</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2463d9a101f9c39973277d105f8bf119" id="tgt510" class="tgtSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f0289c4d7472816b838bf34a3b92d2c" id="tgt511" class="tgtSentence">DBPROP_STRONGIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11c74d1c21dc5dbb8b802a7408596d87" id="tgt512" class="tgtSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2086801d6ac44d08784890faac1a126" id="tgt513" class="tgtSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7a56dd282a8abf8100c423430ec8e4ac" id="tgt514" class="tgtSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd43d482f9e85ec89014c21fbd361a4" id="tgt515" class="tgtSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f6a45ad9ac6e4482de3def9bced6967" id="tgt516" class="tgtSentence">XML Root</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="568cf383f0cb6f2329ac3408d5676247" id="tgt517" class="tgtSentence">SSPROP_STREAM_XMLROOT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4204e4de3fc1f8bffa6f77c383d2d6a0" id="tgt518" class="tgtSentence">XSL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec1db33d65d5b3fd212713f529ada16c" id="tgt519" class="tgtSentence">SSPROP_STREAM_XSL</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="5ac347d9be40408ad1c0e181bfc021fd" id="tgt520" class="tgtSentence">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, see the <legacyLink xlink:href="adf1d6c4-5930-444a-9248-ff1979729635">SQL Server Provider</legacyLink>.</caps:sentence>
          </para>
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
        <para>
          <caps:sentence id="src1" class="srcSentence">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">To connect to this provider, set the <legacyItalic>Provider</legacyItalic> argument to the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>SQLOLEDB</code>
          <para>
            <caps:sentence id="src4" class="srcSentence">This value can also be set or read using the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=SQLOLEDB;Data Source=<legacyItalic xmlns="">serverName</legacyItalic>;"
Initial Catalog=<legacyItalic xmlns="">databaseName</legacyItalic>;
User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence id="src7" class="srcSentence">The string consists of these keywords:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Keyword</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src10" class="srcSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Specifies the OLE DB Provider for SQL Server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">
                      <legacyBold>Data Source</legacyBold> or <legacyBold>Server</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Specifies the name of a server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">
                      <legacyBold>Initial Catalog</legacyBold> or <legacyBold>Database</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Specifies the name of a database on the server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">
                      <legacyBold>User ID</legacyBold> or <legacyBold>uid</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Specifies the user name (for SQL Server Authentication).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">
                      <legacyBold>Password</legacyBold> or <legacyBold>pwd</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Specifies the user password (for SQL Server Authentication).</caps:sentence>
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
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Provider-Specific Connection Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src22" class="srcSentence">The provider supports several provider-specific connection parameters in addition to those defined by ADO.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> As with the ADO connection properties, these provider-specific properties can be set via the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> or can be set as part of the <legacyBold>ConnectionString</legacyBold>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Trusted_Connection</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Indicates the user authentication mode.</caps:sentence>
                    <caps:sentence id="src28" class="srcSentence"> This can be set to <legacyBold>Yes</legacyBold> or <legacyBold>No</legacyBold>.</caps:sentence>
                    <caps:sentence id="src29" class="srcSentence"> The default value is <legacyBold>No</legacyBold>.</caps:sentence>
                    <caps:sentence id="src30" class="srcSentence"> If this property is set to <legacyBold>Yes</legacyBold>, SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <legacyBold>Location</legacyBold> and <legacyLink xlink:href="300a702a-3544-48c5-b759-83b511fe97e0">Datasource</legacyLink> property values.</caps:sentence>
                    <caps:sentence id="src31" class="srcSentence"> If this property is set to <legacyBold>No</legacyBold>, SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database.</caps:sentence>
                    <caps:sentence id="src32" class="srcSentence"> The SQL Server login and password are specified in the <legacyBold>User Id</legacyBold> and <legacyBold>Password</legacyBold> properties.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Current Language</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Indicates a SQL Server language name.</caps:sentence>
                    <caps:sentence id="src35" class="srcSentence"> Identifies the language used for system message selection and formatting.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> The language must be installed on the SQL Server, otherwise opening the connection will fail.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Network Address</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Indicates the network address of the SQL Server specified by the <legacyBold>Location</legacyBold> property.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Network Library</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Indicates the name of the network library (DLL) used to communicate with the SQL Server.</caps:sentence>
                    <caps:sentence id="src41" class="srcSentence"> The name should not include the path or the .dll file name extension.</caps:sentence>
                    <caps:sentence id="src42" class="srcSentence"> The default is provided by the SQL Server client configuration.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Use Procedure for Prepare</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <legacyBold>Prepared</legacyBold> property).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Auto Translate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Indicates whether OEM/ANSI characters are converted.</caps:sentence>
                    <caps:sentence id="src47" class="srcSentence"> This property can be set to <legacyBold>True</legacyBold> or <legacyBold>False</legacyBold>.</caps:sentence>
                    <caps:sentence id="src48" class="srcSentence"> The default value is <legacyBold>True</legacyBold>.</caps:sentence>
                    <caps:sentence id="src49" class="srcSentence"> If this property is set to <legacyBold>True</legacyBold>, SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server.</caps:sentence>
                    <caps:sentence id="src50" class="srcSentence"> If this property is set to <legacyBold>False</legacyBold>, SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Packet Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Indicates a network packet size in bytes.</caps:sentence>
                    <caps:sentence id="src53" class="srcSentence"> The packet size property value must be between 512 and 32767.</caps:sentence>
                    <caps:sentence id="src54" class="srcSentence"> The default SQLOLEDB network packet size is 4096.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Application Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Indicates the client application name.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Workstation ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">A string identifying the workstation.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src59" class="srcSentence">Command Object Usage</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src60" class="srcSentence">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax.</caps:sentence>
            <caps:sentence id="src61" class="srcSentence"> For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</caps:sentence>
          </para>
          <code>SELECT customerid={fn LCASE(CustomerID)} FROM Customers
  </code>
          <para>
            <caps:sentence id="src62" class="srcSentence">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents.</caps:sentence>
            <caps:sentence id="src63" class="srcSentence"> The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented earlier:</caps:sentence>
          </para>
          <code>SELECT customerid=LOWER(CustomerID) FROM Customers
  </code>
          <para>
            <caps:sentence id="src64" class="srcSentence">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src65" class="srcSentence">Stored Procedures</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src66" class="srcSentence">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text.</caps:sentence>
            <caps:sentence id="src67" class="srcSentence"> SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing.</caps:sentence>
            <caps:sentence id="src68" class="srcSentence"> For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src69" class="srcSentence">ODBC SQL</caps:sentence>
        </title>
        <content>
          <code>{call SalesByCategory('Produce', '1995')}
  </code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src70" class="srcSentence">Transact-SQL</caps:sentence>
        </title>
        <content>
          <code>EXECUTE SalesByCategory 'Produce', '1995'
  </code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src71" class="srcSentence">SQL Server Features</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src72" class="srcSentence">With SQL Server, ADO can use XML for <legacyBold>Command</legacyBold> input and retrieve results in XML stream format instead of in <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src73" class="srcSentence"> For more information, see <legacyLink xlink:href="0ac09dbe-2665-411e-8fbb-d1efe6c777be">Using Streams for Command Input</legacyLink> and <legacyLink xlink:href="996c1321-c926-4f57-8297-85c8c20de974">Retrieving Resultsets Into Streams</legacyLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src74" class="srcSentence">Accessing sql_variant data using MDAC 2.7, MDAC 2.8, or Windows DAC 6.0</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src75" class="srcSentence">Microsoft SQL Server has a data type called <legacyBold>sql_variant</legacyBold>.</caps:sentence>
                <caps:sentence id="src76" class="srcSentence"> Similar to OLE DB's <legacyBold>DBTYPE_VARIANT</legacyBold>, the <legacyBold>sql_variant</legacyBold> data type can store data of several different types.</caps:sentence>
                <caps:sentence id="src77" class="srcSentence"> However, there are a few key differences between <legacyBold>DBTYPE_VARIANT</legacyBold> and <legacyBold>sql_variant</legacyBold>.</caps:sentence>
                <caps:sentence id="src78" class="srcSentence"> ADO also handles data stored as a <legacyBold>sql_variant</legacyBold> value differently than how it handles other data types.</caps:sentence>
                <caps:sentence id="src79" class="srcSentence"> The following list describes issues to consider when you access SQL Server data stored in columns of type <legacyBold>sql_variant</legacyBold>.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">In MDAC 2.7, MDAC 2.8, and Windows Data Access Components (Windows DAC) 6.0, the OLE DB Provider for SQL Server supports the <legacyBold>sql_variant</legacyBold> type.</caps:sentence>
                    <caps:sentence id="src81" class="srcSentence"> The OLE DB Provider for ODBC does not.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">The <legacyBold>sql_variant</legacyBold> type does not exactly match the <legacyBold>DBTYPE_VARIANT</legacyBold> data type.</caps:sentence>
                    <caps:sentence id="src83" class="srcSentence">  The <legacyBold>sql_variant</legacyBold> type supports a few new subtypes not supported by <legacyBold>DBTYPE_VARIANT,</legacyBold> including <legacyBold>GUID</legacyBold>, <legacyBold>ANSI</legacyBold> (non-UNICODE) strings, and <legacyBold>BIGINT</legacyBold>.</caps:sentence>
                    <caps:sentence id="src84" class="srcSentence"> Using subtypes other than those listed earlier will work correctly.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">The <legacyBold>sql_variant</legacyBold> subtype <legacyBold>NUMERIC</legacyBold> does not match the <legacyBold>DBTYPE_DECIMAL</legacyBold> in size.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">Multiple data type coercions will result in types that do not match.</caps:sentence>
                    <caps:sentence id="src87" class="srcSentence"> For example, coercing a <legacyBold>sql_variant</legacyBold> with a subtype of <legacyBold>GUID</legacyBold> to a <legacyBold>DBTYPE_VARIANT</legacyBold> will result in a subtype of <legacyBold>safearray</legacyBold>(bytes).</caps:sentence>
                    <caps:sentence id="src88" class="srcSentence"> Converting this type back to a <legacyBold>sql_variant</legacyBold> will result in a new subtype of <legacyBold>array</legacyBold>(bytes).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">  <legacyBold>Recordset</legacyBold> fields that contain <legacyBold>sql_variant</legacyBold> data can be remoted (marshaled) or persisted only if the <legacyBold>sql_variant</legacyBold> contains specific subtypes.</caps:sentence>
                    <caps:sentence id="src90" class="srcSentence"> Attempting to remote or persist data with the following unsupported subtypes will cause a run-time error (unsupported conversion) from the Microsoft Persistence Provider (MSPersist): <legacyBold>VT_VARIANT</legacyBold>, <legacyBold>VT_RECORD</legacyBold>, <legacyBold>VT_ILLEGAL</legacyBold>, <legacyBold>VT_UNKNOWN</legacyBold>, <legacyBold>VT_BSTR</legacyBold>, and <legacyBold>VT_DISPATCH.</legacyBold></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">The OLE DB Provider for SQL Server in MDAC 2.7, MDAC 2.8, and Windows DAC 6.0 has a dynamic property called <legacyBold>Allow Native Variants</legacyBold> which, as the name implies, allows developers to access the <legacyBold>sql_variant</legacyBold> in its native form as opposed to a <legacyBold>DBTYPE_VARIANT</legacyBold>.</caps:sentence>
                    <caps:sentence id="src92" class="srcSentence"> If this property is set, and a <legacyBold>Recordset</legacyBold> is opened with the Client Cursor Engine (<legacyBold>adUseClient</legacyBold>), the <legacyBold>Recordset.Open</legacyBold> call will fail.</caps:sentence>
                    <caps:sentence id="src93" class="srcSentence"> If this property is set and a <legacyBold>Recordset</legacyBold> is opened with server cursors (<legacyBold>adUseServer</legacyBold>), the <legacyBold>Recordset.Open</legacyBold> call will succeed, but accessing columns of type <legacyBold>sql_variant</legacyBold> will produce an error.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">In client applications that use MDAC 2.5, <legacyBold>sql_variant </legacyBold>data can be used with queries against Microsoft SQL Server.</caps:sentence>
                    <caps:sentence id="src95" class="srcSentence"> However, the values of the <legacyBold>sql_variant</legacyBold> data are treated as strings.</caps:sentence>
                    <caps:sentence id="src96" class="srcSentence"> Such client applications should be upgraded to MDAC 2.7, MDAC 2.8, or Windows DAC 6.0.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src97" class="srcSentence">Recordset Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src98" class="srcSentence">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands.</caps:sentence>
            <caps:sentence id="src99" class="srcSentence"> If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src100" class="srcSentence">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors.</caps:sentence>
            <caps:sentence id="src101" class="srcSentence"> SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database.</caps:sentence>
            <caps:sentence id="src102" class="srcSentence"> Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src103" class="srcSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src104" class="srcSentence">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the <legacyBold>Properties</legacyBold> collection of the unopened <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src105" class="srcSentence">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</caps:sentence>
            <caps:sentence id="src106" class="srcSentence"> The OLE DB Programmer's Reference refers to an ADO property name by the term "Description."</caps:sentence>
            <caps:sentence id="src107" class="srcSentence"> You can find more information about these properties in the OLE DB Programmer's Reference.</caps:sentence>
            <caps:sentence id="src108" class="srcSentence"> Search for the OLE DB property name in the Index or see <legacyLink xlink:href="deded3ff-f508-4e1b-b2b1-fd9afd3bd292">Appendix C: OLE DB Properties</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src109" class="srcSentence">Connection Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src110" class="srcSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">Active Sessions</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">DBPROP_ACTIVESESSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">Asynchable Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">DBPROP_ASYNCTXNABORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">Asynchable Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">DBPROP_ASYNCTNXCOMMIT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">Autocommit Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">DBPROP_SESS_AUTOCOMMITISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">Catalog Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src122" class="srcSentence">DBPROP_CATALOGLOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src123" class="srcSentence">Catalog Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">DBPROP_CATALOGTERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">Column Definition</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">DBPROP_COLUMNDEFINITION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">Connect Timeout</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">DBPROP_INIT_TIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">Current Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">DBPROP_CURRENTCATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src131" class="srcSentence">Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">DBPROP_INIT_DATASOURCE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">Data Source Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">DBPROP_DATASOURCENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">Data Source Object Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">DBPROP_DSOTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">DBMS Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">DBPROP_DBMSNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">DBMS Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">DBPROP_DBMSVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">Extended Properties</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">DBPROP_INIT_PROVIDERSTRING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">GROUP BY Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">DBPROP_GROUPBY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">Heterogeneous Table Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">DBPROP_HETEROGENEOUSTABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">Identifier Case Sensitivity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src148" class="srcSentence">DBPROP_IDENTIFIERCASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">Initial Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">DBPROP_INIT_CATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">DBPROP_SUPPORTEDTXNISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">Isolation Retention</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">DBPROP_SUPPORTEDTXNISORETAIN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src155" class="srcSentence">Locale Identifier</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">DBPROP_INIT_LCID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">Maximum Index Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">DBPROP_MAXINDEXSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">Maximum Row Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">DBPROP_MAXROWSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">Maximum Row Size Includes BLOB</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">DBPROP_MAXROWSIZEINCLUDESBLOB</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">Maximum Tables in SELECT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">DBPROP_MAXTABLESINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">Multiple Parameter Sets</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">DBPROP_MULTIPLEPARAMSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">Multiple Results</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">DBPROP_MULTIPLERESULTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">Multiple Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">DBPROP_MULTIPLESTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">Multi-Table Update</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">DBPROP_MULTITABLEUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">NULL Collation Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">DBPROP_NULLCOLLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">NULL Concatenation Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">DBPROP_CONCATNULLBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">OLE DB Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">DBPROP_PROVIDEROLEDBVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">OLE Object Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">DBPROP_OLEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">Open Rowset Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">DBPROP_OPENROWSETSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">ORDER BY Columns in Select List</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">DBPROP_ORDERBYCOLUMNSINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">Output Parameter Availability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">DBPROP_OUTPUTPARAMETERAVAILABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">Pass By Ref Accessors</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">DBPROP_BYREFACCESSORS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">Password</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src190" class="srcSentence">DBPROP_AUTH_PASSWORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">Persist Security Info</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src193" class="srcSentence">Persistent ID Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">DBPROP_PERSISTENTIDTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">Prepare Abort Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">DBPROP_PREPAREABORTBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src197" class="srcSentence">Prepare Commit Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">DBPROP_PREPARECOMMITBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">Procedure Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">DBPROP_PROCEDURETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">Prompt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">DBPROP_INIT_PROMPT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">Provider Friendly Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">DBPROP_PROVIDERFRIENDLYNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">Provider Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src206" class="srcSentence">DBPROP_PROVIDERFILENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">Provider Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src208" class="srcSentence">DBPROP_PROVIDERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">Read-Only Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src210" class="srcSentence">DBPROP_DATASOURCEREADONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src211" class="srcSentence">Rowset Conversions on Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">DBPROP_ROWSETCONVERSIONSONCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">Schema Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">DBPROP_SCHEMATERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src215" class="srcSentence">Schema Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src216" class="srcSentence">DBPROP_SCHEMAUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src217" class="srcSentence">SQL Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src218" class="srcSentence">DBPROP_SQLSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src219" class="srcSentence">Structured Storage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src220" class="srcSentence">DBPROP_STRUCTUREDSTORAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src221" class="srcSentence">Subquery Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src222" class="srcSentence">DBPROP_SUBQUERIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src223" class="srcSentence">Table Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">DBPROP_TABLETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src225" class="srcSentence">Transaction DDL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src226" class="srcSentence">DBPROP_SUPPORTEDTXNDDL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src227" class="srcSentence">User ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src228" class="srcSentence">DBPROP_AUTH_USERID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src229" class="srcSentence">User Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src230" class="srcSentence">DBPROP_USERNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">Window Handle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">DBPROP_INIT_HWND</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src233" class="srcSentence">Recordset Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src234" class="srcSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src235" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src236" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src237" class="srcSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src238" class="srcSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src239" class="srcSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src240" class="srcSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src241" class="srcSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src242" class="srcSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src243" class="srcSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src245" class="srcSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src248" class="srcSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src250" class="srcSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src251" class="srcSentence">Command Time Out</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src252" class="srcSentence">DBPROP_COMMANDTIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src253" class="srcSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src254" class="srcSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src255" class="srcSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src256" class="srcSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src257" class="srcSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src258" class="srcSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src259" class="srcSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src260" class="srcSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src261" class="srcSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src262" class="srcSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src263" class="srcSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src264" class="srcSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src265" class="srcSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src267" class="srcSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src268" class="srcSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src269" class="srcSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src270" class="srcSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src271" class="srcSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src272" class="srcSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src273" class="srcSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src274" class="srcSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src275" class="srcSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src276" class="srcSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src277" class="srcSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src278" class="srcSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src280" class="srcSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src281" class="srcSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src282" class="srcSentence">DBPROP_IRowsestLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src283" class="srcSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>              </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src284" class="srcSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src285" class="srcSentence">DBPROP_IRowsetScroll</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src286" class="srcSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src287" class="srcSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src288" class="srcSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src289" class="srcSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src290" class="srcSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src291" class="srcSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src292" class="srcSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src293" class="srcSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src294" class="srcSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src295" class="srcSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src296" class="srcSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src297" class="srcSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src298" class="srcSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src299" class="srcSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src300" class="srcSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src301" class="srcSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src302" class="srcSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src303" class="srcSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src304" class="srcSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src305" class="srcSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src306" class="srcSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src307" class="srcSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src308" class="srcSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src309" class="srcSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src310" class="srcSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src311" class="srcSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src312" class="srcSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src313" class="srcSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src314" class="srcSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src315" class="srcSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src316" class="srcSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src317" class="srcSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src318" class="srcSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src319" class="srcSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src320" class="srcSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src321" class="srcSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src322" class="srcSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src323" class="srcSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src324" class="srcSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src325" class="srcSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src326" class="srcSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src327" class="srcSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src328" class="srcSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src329" class="srcSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src330" class="srcSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src331" class="srcSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src332" class="srcSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src333" class="srcSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src334" class="srcSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src335" class="srcSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src336" class="srcSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src337" class="srcSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src338" class="srcSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src339" class="srcSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src340" class="srcSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src341" class="srcSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src342" class="srcSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src343" class="srcSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src344" class="srcSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src345" class="srcSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src346" class="srcSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src347" class="srcSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src348" class="srcSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src349" class="srcSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src350" class="srcSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src351" class="srcSentence">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src352" class="srcSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src353" class="srcSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src354" class="srcSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src355" class="srcSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src356" class="srcSentence">Server Cursor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src357" class="srcSentence">DBPROP_SERVERCURSOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src358" class="srcSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src359" class="srcSentence">DBPROP_BOOKMARKSKIPPED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src360" class="srcSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src361" class="srcSentence">DBPROP_STRONGITDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src362" class="srcSentence">Unique Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src363" class="srcSentence">DBPROP_UNIQUEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src364" class="srcSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src365" class="srcSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src366" class="srcSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src367" class="srcSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src368" class="srcSentence">Command Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src369" class="srcSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src370" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src371" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src372" class="srcSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src373" class="srcSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src374" class="srcSentence">Base Path</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src375" class="srcSentence">SSPROP_STREAM_BASEPATH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src376" class="srcSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src377" class="srcSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src378" class="srcSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src379" class="srcSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src380" class="srcSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src381" class="srcSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src382" class="srcSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src383" class="srcSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src384" class="srcSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src385" class="srcSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src386" class="srcSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src387" class="srcSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src388" class="srcSentence">Content Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src389" class="srcSentence">SSPROP_STREAM_CONTENTTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src390" class="srcSentence">Cursor Auto Fetch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src391" class="srcSentence">SSPROP_CURSORAUTOFETCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src392" class="srcSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src393" class="srcSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src394" class="srcSentence">Defer Prepare</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src395" class="srcSentence">SSPROP_DEFERPREPARE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src396" class="srcSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src397" class="srcSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src398" class="srcSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src399" class="srcSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src400" class="srcSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src401" class="srcSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src402" class="srcSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src403" class="srcSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src404" class="srcSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src405" class="srcSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src406" class="srcSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src407" class="srcSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src408" class="srcSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src409" class="srcSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src410" class="srcSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src411" class="srcSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src412" class="srcSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src413" class="srcSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src414" class="srcSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src415" class="srcSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src416" class="srcSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src417" class="srcSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src418" class="srcSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src419" class="srcSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src420" class="srcSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src421" class="srcSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src422" class="srcSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src423" class="srcSentence">DBPROP_IRowsetLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src424" class="srcSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src425" class="srcSentence">DBPROP_IRowsetResynch</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src426" class="srcSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src427" class="srcSentence">DBPROP_IRowsetScroll</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src428" class="srcSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src429" class="srcSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src430" class="srcSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src431" class="srcSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src432" class="srcSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src433" class="srcSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src434" class="srcSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src435" class="srcSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src436" class="srcSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src437" class="srcSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src438" class="srcSentence">Lock Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src439" class="srcSentence">DBPROP_LOCKMODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src440" class="srcSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src441" class="srcSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src442" class="srcSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src443" class="srcSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src444" class="srcSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src445" class="srcSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src446" class="srcSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src447" class="srcSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src448" class="srcSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src449" class="srcSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src450" class="srcSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src451" class="srcSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src452" class="srcSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src453" class="srcSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src454" class="srcSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src455" class="srcSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src456" class="srcSentence">Output Encoding Property</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src457" class="srcSentence">DBPROP_OUTPUTENCODING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src458" class="srcSentence">Output Stream Property</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src459" class="srcSentence">DBPROP_OUTPUTSTREAM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src460" class="srcSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src461" class="srcSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src462" class="srcSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src463" class="srcSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src464" class="srcSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src465" class="srcSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src466" class="srcSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src467" class="srcSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src468" class="srcSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src469" class="srcSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src470" class="srcSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src471" class="srcSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src472" class="srcSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src473" class="srcSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src474" class="srcSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src475" class="srcSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src476" class="srcSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src477" class="srcSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src478" class="srcSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src479" class="srcSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src480" class="srcSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src481" class="srcSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src482" class="srcSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src483" class="srcSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src484" class="srcSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src485" class="srcSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src486" class="srcSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src487" class="srcSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src488" class="srcSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src489" class="srcSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src490" class="srcSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src491" class="srcSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src492" class="srcSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src493" class="srcSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src494" class="srcSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src495" class="srcSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src496" class="srcSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src497" class="srcSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src498" class="srcSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src499" class="srcSentence">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src500" class="srcSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src501" class="srcSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src502" class="srcSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src503" class="srcSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src504" class="srcSentence">Server Cursor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src505" class="srcSentence">DBPROP_SERVERCURSOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src506" class="srcSentence">Server Data on Insert</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src507" class="srcSentence">DBPROP_SERVERDATAONINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src508" class="srcSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src509" class="srcSentence">DBPROP_BOOKMARKSKIP</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src510" class="srcSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src511" class="srcSentence">DBPROP_STRONGIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src512" class="srcSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src513" class="srcSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src514" class="srcSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src515" class="srcSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src516" class="srcSentence">XML Root</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src517" class="srcSentence">SSPROP_STREAM_XMLROOT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src518" class="srcSentence">XSL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src519" class="srcSentence">SSPROP_STREAM_XSL</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src520" class="srcSentence">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, see the <legacyLink xlink:href="adf1d6c4-5930-444a-9248-ff1979729635">SQL Server Provider</legacyLink>.</caps:sentence>
          </para>
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
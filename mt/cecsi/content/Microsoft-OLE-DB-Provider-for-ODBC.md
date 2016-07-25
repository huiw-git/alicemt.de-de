---
title: "Microsoft OLE DB Provider for ODBC"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2dc0372d-e74d-4d0f-9c8c-04e5a168c148
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
# Microsoft OLE DB Provider for ODBC
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="928096f5f40d1d305475340fcbb79cbf" id="tgt1" class="tgtSentence">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</caps:sentence>
          <caps:sentence sentenceid="f16977e8b7178b2e49df3cd9a2140fd2" id="tgt2" class="tgtSentence"> Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</caps:sentence>
          <caps:sentence sentenceid="22828151da58505b9878189433ff0663" id="tgt3" class="tgtSentence"> However, most DBMS systems in use today can be accessed through ODBC.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="148a1e21e647281661a139daf5b7ac09" id="tgt4" class="tgtSentence">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b8aa09f61d7f70f5d3b7923129c09d23" id="tgt5" class="tgtSentence">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</caps:sentence>
          <caps:sentence sentenceid="3a3cd45c40fa616b14fbd71ceb2d569f" id="tgt6" class="tgtSentence"> The provider is free-threaded and Unicode enabled.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="dad07ea8f265d1518693f95098715365" id="tgt7" class="tgtSentence">The provider supports transactions, although different DBMS engines offer different types of transaction support.</caps:sentence>
          <caps:sentence sentenceid="b9e30fc223ed8a8ae52617214be607a4" id="tgt8" class="tgtSentence"> For example, Microsoft Access supports nested transactions up to five levels deep.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fa35bbb009e31aabd4a7e5bbb675e67a" id="tgt9" class="tgtSentence">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="df209e37fa6496886af7a164ca15b629" id="tgt10" class="tgtSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e404ecb428d45872c5f75bc33e2b4c6b" id="tgt11" class="tgtSentence">To connect to this provider, set the <legacyBold>Provider=</legacyBold> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>MSDASQL</code>
          <para>
            <caps:sentence sentenceid="248709408787db043727f63ce324962e" id="tgt12" class="tgtSentence">Reading the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property will return this string as well.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5cf5a4267aa499f9dca0d6e5a90731cb" id="tgt13" class="tgtSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5c9e747ddd8663400e6e4b231a6386e6" id="tgt14" class="tgtSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=MSDASQL;DSN=<legacyItalic xmlns="">dsnName</legacyItalic>;UID=<legacyItalic xmlns="">MyUserID</legacyItalic>;PWD=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence sentenceid="61333c54636d561759b12d35ff08c05b" id="tgt15" class="tgtSentence">The string consists of these keywords:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7df5b64df1181ef1d62d646a13aa860" id="tgt16" class="tgtSentence">Keyword</caps:sentence>
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
                    <legacyBold>
                      <caps:sentence sentenceid="9e9f3d70bd8c8957627eada96d967706" id="tgt18" class="tgtSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf09a00d9a16c5948c3f2f2815dc2697" id="tgt19" class="tgtSentence">Specifies the OLE DB provider for ODBC.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="da532bf806defa26fdbeee5dd2e0d68f" id="tgt20" class="tgtSentence">DSN</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ed1aea55900505af3569df2c6bcc62d1" id="tgt21" class="tgtSentence">Specifies the data source name.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9871d3a2c554b27151cacf1422eec048" id="tgt22" class="tgtSentence">UID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="894ae1122beff71d90c743328e91d2dd" id="tgt23" class="tgtSentence">Specifies the user name.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9003d1df22eb4d3820015070385194c8" id="tgt24" class="tgtSentence">PWD</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4df08222df3dae489cac77da63d403c" id="tgt25" class="tgtSentence">Specifies the user password.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="572d4e421e5e6b9bc11d815e8a027112" id="tgt26" class="tgtSentence">URL</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="762432184d2bf924a85847f927d3516d" id="tgt27" class="tgtSentence">Specifies the URL of a file or directory published in a Web folder.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="379f36146a02a412ad997645b2b1680a" id="tgt28" class="tgtSentence">Because this is the default provider for ADO, if you omit the <legacyBold>Provider=</legacyBold> parameter from the connection string, ADO will try to establish a connection to this provider.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="a955ec3a31d8205c3ae07b07b7fefc6d" id="tgt29" class="tgtSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <system>Trusted_Connection=yes</system> or <system>Integrated Security = SSPI</system> instead of user ID and password information in the connection string.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="963a66486b42c4c56e68855416b45940" id="tgt30" class="tgtSentence">The provider does not support any specific connection parameters in addition to those defined by ADO.</caps:sentence>
            <caps:sentence sentenceid="049927dad8e269a9a1cd28b51e5a2a94" id="tgt31" class="tgtSentence"> However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="eedca7838afdebfd5b1f62f937bc4816" id="tgt32" class="tgtSentence">Because you can omit the <legacyBold>Provider</legacyBold> parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</caps:sentence>
            <caps:sentence sentenceid="43bdf3f09b65d260faa11eec687ce34e" id="tgt33" class="tgtSentence"> Use the same parameter names (<legacyBold>DRIVER=</legacyBold>, <legacyBold>DATABASE=</legacyBold>, <legacyBold>DSN=</legacyBold>, and so on), values, and syntax as you would when composing an ODBC connection string.</caps:sentence>
            <caps:sentence sentenceid="1787b9249b6c10e3e3451c7b3d390981" id="tgt34" class="tgtSentence"> You can connect with or without a predefined data source name (DSN) or FileDSN.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1e98a18c38a0593149bd2b9c4bac9375" id="tgt35" class="tgtSentence">Syntax with a DSN or FileDSN:</caps:sentence>
        </title>
        <content>
          <code>"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; 
[DATABASE=database;] UID=user; PWD=password"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="459028deab45ef409d991db4b1df7794" id="tgt36" class="tgtSentence">Syntax without a DSN (DSN-less connection):</caps:sentence>
        </title>
        <content>
          <code>"[Provider=MSDASQL;] DRIVER=driver; SERVER=server; 
DATABASE=database; UID=MyUserID; PWD=MyPassword"</code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="c95ca6f90190f3e6491f21ff647c72a2" id="tgt37" class="tgtSentence">If you use a <legacyBold>DSN</legacyBold> or <legacyBold>FileDSN</legacyBold>, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</caps:sentence>
            <caps:sentence sentenceid="cd9d703221f12d45e631ea6fe4d2478a" id="tgt38" class="tgtSentence"> In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</caps:sentence>
            <caps:sentence sentenceid="81900bafe098664b5633b95c39e6a671" id="tgt39" class="tgtSentence"> In earlier versions of Windows, the ODBC Administrator icon is named <legacyBold>32-bit ODBC</legacyBold> or just <legacyBold>ODBC</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="30b9262dc50068fc5fd8ff72349fe1e7" id="tgt40" class="tgtSentence">As an alternative to setting a <legacyBold>DSN</legacyBold>, you can specify the ODBC driver (<legacyBold>DRIVER=</legacyBold>), such as "SQL Server;" the server name (<legacyBold>SERVER=</legacyBold>); and the database name (<legacyBold>DATABASE=</legacyBold>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="923f53da4ad05c248a8589ec45763f23" id="tgt41" class="tgtSentence">You can also specify a user account name (<legacyBold>UID=</legacyBold>), and the password for the user account (<legacyBold>PWD=</legacyBold>) in the ODBC-specific parameters or in the standard ADO-defined <legacyItalic>user</legacyItalic> and <legacyItalic>password</legacyItalic> parameters.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c5c7f00e8c134bf17bec54cf07841532" id="tgt42" class="tgtSentence">Although a <legacyBold>DSN</legacyBold> definition already specifies a database, you can specify <legacyItalic>a</legacyItalic> <legacyItalic>database</legacyItalic> parameter in addition to a <legacyBold>DSN</legacyBold> to connect to a different database.</caps:sentence>
            <caps:sentence sentenceid="a063f684626d90b577b4681be498b461" id="tgt43" class="tgtSentence"> It is a good idea to always include <legacyItalic>the</legacyItalic> <legacyItalic>database</legacyItalic> parameter when you use a <legacyBold>DSN</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="48a63ab1b1a3fbcb9604688c0a7ef3e5" id="tgt44" class="tgtSentence"> This will ensure that you connect to the correct database if another user changed the default database parameter since you last checked the <legacyBold>DSN</legacyBold> definition.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="7086452e1a131486319e9280cecf3438" id="tgt45" class="tgtSentence">Provider-Specific Connection Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5613d1be0f2a9b6d13ca0861e77fcdb0" id="tgt46" class="tgtSentence">The OLE DB provider for ODBC adds several properties to the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="3a2851a3ac7cdb40eb399dee52bf53d3" id="tgt47" class="tgtSentence"> The following table lists these properties with the corresponding OLE DB property name in parentheses.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a3d69a40cc5ec31232a11100ae6c951" id="tgt48" class="tgtSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt49" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="962eb1f367ed0db6f11e879f016a3817" id="tgt50" class="tgtSentence">Accessible Procedures (KAGPROP_ACCESSIBLEPROCEDURES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f007b01a6d3fc8a41ae3cb698cc9df29" id="tgt51" class="tgtSentence">Indicates whether the user has access to stored procedures.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45447c4a2aa0717534989eb39d3efe29" id="tgt52" class="tgtSentence">Accessible Tables (KAGPROP_ACCESSIBLETABLES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="68207d7a057c2cdc0fdb7f235a40b9b7" id="tgt53" class="tgtSentence">Indicates whether the user has permission to execute SELECT statements against the database tables.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bb5592e12e79e73bcce62e10a396434b" id="tgt54" class="tgtSentence">Active Statements (KAGPROP_ACTIVESTATEMENTS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7780b94e5d67e55bdbe94e256698423a" id="tgt55" class="tgtSentence">Indicates the number of handles an ODBC driver can support on a connection.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f3c7b6778e7bfae92ff4116ab69648f0" id="tgt56" class="tgtSentence">Driver Name (KAGPROP_DRIVERNAME)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d54d21536a47237adf93fbee0725156" id="tgt57" class="tgtSentence">Indicates the file name of the ODBC driver.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0df5e76b3b1f24dcd8474bfca368f02" id="tgt58" class="tgtSentence">Driver ODBC Version (KAGPROP_DRIVERODBCVER)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e01f15ae62472ca443fec6c158f6e9cb" id="tgt59" class="tgtSentence">Indicates the version of ODBC that this driver supports.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e11f67eb01e18b4d6d2b3765ef1928a3" id="tgt60" class="tgtSentence">File Usage (KAGPROP_FILEUSAGE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f382cb8bd7e8d35558869620a1142cb7" id="tgt61" class="tgtSentence">Indicates how the driver treats a file in a data source; as a table or as a catalog.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a210ef25a4ed8b9801d7227385a2440b" id="tgt62" class="tgtSentence">Like Escape Clause (KAGPROP_LIKEESCAPECLAUSE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ff41c0c2fde21ab9745edbbc5b4e2153" id="tgt63" class="tgtSentence">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e59184f36e0e400e14c6c7c26feb3a5f" id="tgt64" class="tgtSentence">Max Columns in Group By (KAGPROP_MAXCOLUMNSINGROUPBY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="15497e9c2aa7f5fb07012d386f870755" id="tgt65" class="tgtSentence">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="56b01c0a15d4c94299629a6923836764" id="tgt66" class="tgtSentence">Max Columns in Index (KAGPROP_MAXCOLUMNSININDEX)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="113fd44e585cc564cda308bf3e18fb5c" id="tgt67" class="tgtSentence">Indicates the maximum number of columns that can be included in an index.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5576ea696b3644eab15af4e82c7f3009" id="tgt68" class="tgtSentence">Max Columns in Order By (KAGPROP_MAXCOLUMNSINORDERBY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="967986331faa19b2a5fee044910b3c42" id="tgt69" class="tgtSentence">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0be9ab6959300ac420e3c620e0c673f6" id="tgt70" class="tgtSentence">Max Columns in Select (KAGPROP_MAXCOLUMNSINSELECT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8e9547f46b6d2327bbdaba0be63835ba" id="tgt71" class="tgtSentence">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="efd5f26e5778c172babd5df1ba3464c3" id="tgt72" class="tgtSentence">Max Columns in Table (KAGPROP_MAXCOLUMNSINTABLE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="72538b80022d022f462c1149e3fc4e85" id="tgt73" class="tgtSentence">Indicates the maximum number of columns allowed in a table.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0a799d6f3998cc0189766f9f644319bc" id="tgt74" class="tgtSentence">Numeric Functions (KAGPROP_NUMERICFUNCTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c69e6eae976a8867ffce38f6208257fa" id="tgt75" class="tgtSentence">Indicates which numeric functions are supported by the ODBC driver.</caps:sentence>
                    <caps:sentence sentenceid="0f9ae39320fd341493ebe7aa9e9385a4" id="tgt76" class="tgtSentence"> For a listing of function names and the associated values used in this bitmask, see <legacyLink xlink:href="59c7cd5e-32d6-43ab-bac3-7010322d105a">Appendix E: Scalar Functions</legacyLink>, in the ODBC documentation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="57b770f2d51106f6c4e79aedcc2785b2" id="tgt77" class="tgtSentence">Outer Join Capabilities (KAGPROP_OJCAPABILITY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ebc54fff7dccb906160c8fa7b2c327f0" id="tgt78" class="tgtSentence">Indicates the types of OUTER JOINs supported by the provider.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9b0acb2fe63439e54c9d6ccf3b9da174" id="tgt79" class="tgtSentence">Outer Joins (KAGPROP_OUTERJOINS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="055862cbad00058b409ecf897f425c0a" id="tgt80" class="tgtSentence">Indicates whether the provider supports OUTER JOINs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c2f3d7da7a54db45980126fe99543ef" id="tgt81" class="tgtSentence">Special Characters (KAGPROP_SPECIALCHARACTERS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfbd982dc8863b46147eb8602e4a4884" id="tgt82" class="tgtSentence">Indicates which characters have special meaning for the ODBC driver.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9890ff11eaae55453303d32a8528e02c" id="tgt83" class="tgtSentence">Stored Procedures (KAGPROP_PROCEDURES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d67f6b1e83b5bcff178385bf68e3e5d" id="tgt84" class="tgtSentence">Indicates whether stored procedures are available for use with this ODBC driver.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="02a5c7a54b221c4ebd591ca59d065795" id="tgt85" class="tgtSentence">String Functions (KAGPROP_STRINGFUNCTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="603dd77b439f6e710939b2783b780fda" id="tgt86" class="tgtSentence">Indicates which string functions are supported by the ODBC driver.</caps:sentence>
                    <caps:sentence sentenceid="0f9ae39320fd341493ebe7aa9e9385a4" id="tgt87" class="tgtSentence"> For a listing of function names and the associated values used in this bitmask, see <legacyLink xlink:href="59c7cd5e-32d6-43ab-bac3-7010322d105a">Appendix E: Scalar Functions</legacyLink>, in the ODBC documentation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c1cf03c29337076a0c34107699237ede" id="tgt88" class="tgtSentence">System Functions (KAGPROP_SYSTEMFUNCTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b47e4c87a01770d2484bc169146cd5a6" id="tgt89" class="tgtSentence">Indicates which system functions are supported by the ODBC driver.</caps:sentence>
                    <caps:sentence sentenceid="0f9ae39320fd341493ebe7aa9e9385a4" id="tgt90" class="tgtSentence"> For a listing of function names and the associated values used in this bitmask, see <legacyLink xlink:href="59c7cd5e-32d6-43ab-bac3-7010322d105a">Appendix E: Scalar Functions</legacyLink>, in the ODBC documentation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3e5b8b374361d1a4e1f1760674a6ea0c" id="tgt91" class="tgtSentence">Time/Date Functions (KAGPROP_TIMEDATEFUNCTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c197d60aab5779b0cacdcc53b0a92b8e" id="tgt92" class="tgtSentence">Indicates which time and date functions are supported by the ODBC driver.</caps:sentence>
                    <caps:sentence sentenceid="0f9ae39320fd341493ebe7aa9e9385a4" id="tgt93" class="tgtSentence"> For a listing of function names and the associated values used in this bitmask, see <legacyLink xlink:href="59c7cd5e-32d6-43ab-bac3-7010322d105a">Appendix E: Scalar Functions</legacyLink>, in the ODBC documentation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6b1c394f35b89251f6c79de4f2e62567" id="tgt94" class="tgtSentence">SQL Grammar Support (KAGPROP_ODBCSQLCONFORMANCE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2cf9e0fe8514451d101e524aa4a15352" id="tgt95" class="tgtSentence">Indicates the SQL grammar that the ODBC driver supports.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1494887de9c2cae6bece501c37b08e00" id="tgt96" class="tgtSentence">Provider-Specific Recordset and Command Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="30fbedd67faaa652be9ac15a6680e665" id="tgt97" class="tgtSentence">The OLE DB provider for ODBC adds several properties to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> and <legacyBold>Command</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="3a2851a3ac7cdb40eb399dee52bf53d3" id="tgt98" class="tgtSentence"> The following table lists these properties with the corresponding OLE DB property name in parentheses.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a3d69a40cc5ec31232a11100ae6c951" id="tgt99" class="tgtSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt100" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d68657e3174884f1d9bee3f967cd7c68" id="tgt101" class="tgtSentence">Query Based Updates/Deletes/Inserts (KAGPROP_QUERYBASEDUPDATES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="967320ab692a1b80cb15a0e49e83b2eb" id="tgt102" class="tgtSentence">Indicates whether updates, deletions, and insertions can be performed by using SQL queries.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dd8246f7b3ead08c68b4496edca12240" id="tgt103" class="tgtSentence">ODBC Concurrency Type (KAGPROP_CONCURRENCY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d2e6b0f7d539c788a4b5d9aed0b29a23" id="tgt104" class="tgtSentence">Indicates the method used to reduce potential problems caused by two users trying to access the same data from the data source simultaneously.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="356d8e4601299f2e41a61039e813852d" id="tgt105" class="tgtSentence">BLOB accessibility on Forward-Only cursor (KAGPROP_BLOBSONFOCURSOR)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="79c4fc49e41a478985592230a4231ad3" id="tgt106" class="tgtSentence">Indicates whether BLOB <legacyBold>Fields</legacyBold> can be accessed when using a forward-only cursor.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4ef06c655ab75d80fa71d25f9ca87bf" id="tgt107" class="tgtSentence">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses (KAGPROP_INCLUDENONEXACT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f0404794fab14248c0ac01122b49f0b" id="tgt108" class="tgtSentence">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="941bc4996a35c039495bed459604bf33" id="tgt109" class="tgtSentence">Position on the last row after insert (KAGPROP_POSITIONONNEWROW)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="242052b5c85f98958193d1cbeafcfd5f" id="tgt110" class="tgtSentence">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="20184b6bda3a4fb9aa38af82a84d5993" id="tgt111" class="tgtSentence">IRowsetChangeExtInfo (KAGPROP_IROWSETCHANGEEXTINFO)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27e3a653229a6e9b30a76cf24ad9bba" id="tgt112" class="tgtSentence">Indicates whether the <legacyBold>IRowsetChange</legacyBold> interface provides extended information support.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8c73c1cd47bba5c49777f03a17e746a" id="tgt113" class="tgtSentence">ODBC Cursor Type (KAGPROP_CURSOR)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a833cfc850f70bad9b637ce70506017d" id="tgt114" class="tgtSentence">Indicates the type of cursor used by the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5016e90b2753301ae33d08de4f43f9f8" id="tgt115" class="tgtSentence">Generate a Rowset that can be marshaled (KAGPROP_MARSHALLABLE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="455349af352f08d9fb9b12bb8d643f9d" id="tgt116" class="tgtSentence">Indicates that the ODBC driver generates a recordset that can be marshaled</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="6100c52dada9c46bce92964c9f051df5" id="tgt117" class="tgtSentence">Command Text</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ef86bf98cb051ccf8058ef90d90bf983" id="tgt118" class="tgtSentence">How you use the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object largely depends on the data source, and what type of query or command statement it will accept.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c581786f0bbce17555fa9525b5e9a5f8" id="tgt119" class="tgtSentence">ODBC provides a specific syntax for calling stored procedures.</caps:sentence>
            <caps:sentence sentenceid="550746b67e37ad8f90a899404c996c20" id="tgt120" class="tgtSentence"> For the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property of a <legacyBold>Command</legacyBold> object, the <legacyItalic>CommandText </legacyItalic>argument to the <legacyBold>Execute</legacyBold> method on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, or the <legacyItalic>Source</legacyItalic> argument to the <legacyBold>Open</legacyBold> method on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, passes in a string with this syntax:</caps:sentence>
          </para>
          <code>"{ [ ? = ] call procedure [ ( ? [, ? [ , … ]] ) ] }"</code>
          <para>
            <caps:sentence sentenceid="a68368dca51fd432e5277daa20566dfe" id="tgt121" class="tgtSentence">Each <legacyBold>?</legacyBold> references an object in the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
            <caps:sentence sentenceid="464823de757de3792a89aef5268002c7" id="tgt122" class="tgtSentence"> The first <legacyBold>?</legacyBold> references <legacyBold>Parameters</legacyBold>(0), the next <legacyBold>?</legacyBold> references <legacyBold>Parameters</legacyBold>(1), and so on.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fff1bb3ce9f0eb88b2c1bf9b3f610468" id="tgt123" class="tgtSentence">The parameter references are optional and depend on the structure of the stored procedure.</caps:sentence>
            <caps:sentence sentenceid="b004418950128f5327d419b3513b08b1" id="tgt124" class="tgtSentence"> If you want to call a stored procedure that defines no parameters, your string would look like the following:</caps:sentence>
          </para>
          <code>"{ call procedure }"</code>
          <para>
            <caps:sentence sentenceid="3211a3c8a9aad478fdd8d7e8e5704907" id="tgt125" class="tgtSentence">If you have two query parameters, your string would resemble the following:</caps:sentence>
          </para>
          <code>"{ call procedure ( ?, ? ) }"</code>
          <para>
            <caps:sentence sentenceid="0113d8147648c9ddb7b6e524b929b345" id="tgt126" class="tgtSentence">If the stored procedure will return a value, the return value is treated as another parameter.</caps:sentence>
            <caps:sentence sentenceid="d91ccb58a09e138625f33c75cca8579b" id="tgt127" class="tgtSentence"> If you have no query parameters but you do have a return value, your string would resemble the following:</caps:sentence>
          </para>
          <code>"{ ? = call procedure }"</code>
          <para>
            <caps:sentence sentenceid="35f375608a183a38c6fbcf6d8d404aed" id="tgt128" class="tgtSentence">Finally, if you have a return value and two query parameters, your string would resemble the following:</caps:sentence>
          </para>
          <code>"{ ? = call procedure ( ?, ? ) }"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="002c1a21d972a03f6b6e5a266dd56653" id="tgt129" class="tgtSentence">Recordset Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f9c8dde8439e71474ec80afe2b7a9463" id="tgt130" class="tgtSentence">The following tables list the standard ADO methods and properties available on a <legacyBold>Recordset</legacyBold> object opened with this provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="08406b5f8edb6e1d777f9d1c568080a7" id="tgt131" class="tgtSentence">For more detailed information about <legacyBold>Recordset</legacyBold> behavior for your provider configuration, run the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method and enumerate the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> to determine whether provider-specific dynamic properties are present.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="35b5f6c862dc0b3058f55b3e822f9182" id="tgt132" class="tgtSentence">Availability of standard ADO <legacyBold>Recordset</legacyBold> properties:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a8db4c996d8ed8289da5f957879ab94" id="tgt133" class="tgtSentence">Property</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="23805a9b06df2dafee7a3ab65fc437a8" id="tgt134" class="tgtSentence">ForwardOnly</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b72f3bd391ba731a35708bfd8cd8a68f" id="tgt135" class="tgtSentence">Dynamic</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8fde746ce7e917c10595b7d86c6c3ad" id="tgt136" class="tgtSentence">Keyset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a81259cef8e959c624df1d456e5d3297" id="tgt137" class="tgtSentence">Static</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">
                      <caps:sentence sentenceid="2ecac8e7ef8b3884f4acf3190b2f0593" id="tgt138" class="tgtSentence">AbsolutePage</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt139" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt140" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt141" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt142" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">
                      <caps:sentence sentenceid="764a8561e40975325fb7bdcd8e66ce21" id="tgt143" class="tgtSentence">AbsolutePosition</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt144" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt145" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt146" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt147" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">
                      <caps:sentence sentenceid="736b2ee4856989f60b05c8ede807ff4f" id="tgt148" class="tgtSentence">ActiveConnection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt149" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt150" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt151" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt152" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">
                      <caps:sentence sentenceid="c9a3639b57c741dcd0334c28032e4280" id="tgt153" class="tgtSentence">BOF</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt154" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt155" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt156" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt157" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">
                      <caps:sentence sentenceid="fad9383ed4698856ed467fd49ecf4820" id="tgt158" class="tgtSentence">Bookmark</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt159" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt160" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt161" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt162" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">
                      <caps:sentence sentenceid="aee9ee3f775b6b5a790c444f68628b29" id="tgt163" class="tgtSentence">CacheSize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt164" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt165" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt166" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt167" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">
                      <caps:sentence sentenceid="ed2f88c61dd3d03f1ef6781f26d23e41" id="tgt168" class="tgtSentence">CursorLocation</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt169" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt170" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt171" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt172" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">
                      <caps:sentence sentenceid="1cd5476188fe9c7cac9cc2ebcd2fb87a" id="tgt173" class="tgtSentence">CursorType</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt174" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt175" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt176" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt177" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">
                      <caps:sentence sentenceid="c3bd55f87129536ac1698eb00596ceb3" id="tgt178" class="tgtSentence">EditMode</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt179" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt180" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt181" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt182" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">
                      <caps:sentence sentenceid="b2c97ae425dd751b0e48a3acae79cf4a" id="tgt183" class="tgtSentence">Filter</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt184" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt185" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt186" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt187" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">
                      <caps:sentence sentenceid="c2edea50ed670a7360991f97066b85ff" id="tgt188" class="tgtSentence">LockType</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt189" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt190" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt191" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt192" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">
                      <caps:sentence sentenceid="3b38b73230230562600faa0c7a4ae19a" id="tgt193" class="tgtSentence">MarshalOptions</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt194" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt195" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt196" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt197" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="20c76571-8c9a-482c-a99e-726ab1d93f8b">
                      <caps:sentence sentenceid="e8a190f33755a6a8fda424e1fe9f4255" id="tgt198" class="tgtSentence">MaxRecords</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt199" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt200" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt201" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt202" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">
                      <caps:sentence sentenceid="cf65c05c144f7132e7bd231b8a2b5ace" id="tgt203" class="tgtSentence">PageCount</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt204" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt205" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt206" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt207" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">
                      <caps:sentence sentenceid="7525d528a3457f0227997c25239c4507" id="tgt208" class="tgtSentence">PageSize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt209" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt210" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt211" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt212" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">
                      <caps:sentence sentenceid="3d21c0cd334398e6a80b987f79424c5a" id="tgt213" class="tgtSentence">RecordCount</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt214" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2f8489bbd55a4e9b9edbbbfe49edf70" id="tgt215" class="tgtSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt216" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt217" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">
                      <caps:sentence sentenceid="36cd38f49b9afa08222c0dc9ebfe35eb" id="tgt218" class="tgtSentence">Source</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt219" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt220" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt221" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bd48fa1968c1368536ed41090dcbb4" id="tgt222" class="tgtSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">
                      <caps:sentence sentenceid="9ed39e2ea931586b6a985a6942ef573e" id="tgt223" class="tgtSentence">State</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt224" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt225" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt226" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt227" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">
                      <caps:sentence sentenceid="9acb44549b41563697bb490144ec6258" id="tgt228" class="tgtSentence">Status</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt229" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt230" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt231" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7233b8e3eacbd7da2c95f2e581cdbf4e" id="tgt232" class="tgtSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="065b311e741b06165f47164154812706" id="tgt233" class="tgtSentence">The <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink> and <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e78f2d75e7376c614b7972e65313132a" id="tgt234" class="tgtSentence">Availability of standard ADO <legacyBold>Recordset</legacyBold> methods:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ea9f6aca279138c58f705c8d4cb4b8ce" id="tgt235" class="tgtSentence">Method</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="23805a9b06df2dafee7a3ab65fc437a8" id="tgt236" class="tgtSentence">ForwardOnly</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b72f3bd391ba731a35708bfd8cd8a68f" id="tgt237" class="tgtSentence">Dynamic</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8fde746ce7e917c10595b7d86c6c3ad" id="tgt238" class="tgtSentence">Keyset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a81259cef8e959c624df1d456e5d3297" id="tgt239" class="tgtSentence">Static</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">
                      <caps:sentence sentenceid="2a99922bd3fcc215a7b3fcbd9667338a" id="tgt240" class="tgtSentence">AddNew</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt241" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt242" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt243" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt244" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">
                      <caps:sentence sentenceid="10aec35353f9c4096a71c38654c3d402" id="tgt245" class="tgtSentence">Cancel</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt246" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt247" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt248" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt249" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">
                      <caps:sentence sentenceid="ecb488ca7118773aa90cb428ed21379b" id="tgt250" class="tgtSentence">CancelBatch</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt251" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt252" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt253" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt254" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">
                      <caps:sentence sentenceid="07e957a04a9b08eadc8537a17615e387" id="tgt255" class="tgtSentence">CancelUpdate</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt256" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt257" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt258" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt259" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">
                      <caps:sentence sentenceid="d329fd777726c300d7a044e482b967e7" id="tgt260" class="tgtSentence">Clone</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt261" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt262" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt263" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt264" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">
                      <caps:sentence sentenceid="716f6b30598ba30945d84485e61c1027" id="tgt265" class="tgtSentence">Close</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt266" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt267" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt268" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt269" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">
                      <caps:sentence sentenceid="099af53f601532dbd31e0ea99ffdeb64" id="tgt270" class="tgtSentence">Delete</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt271" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt272" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt273" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt274" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="14b92860-4171-47d9-a413-dd60dd6a8880">
                      <caps:sentence sentenceid="d1b51a6e50f7a6a0f9879ebf15f2651d" id="tgt275" class="tgtSentence">GetRows</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt276" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt277" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt278" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt279" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">
                      <caps:sentence sentenceid="3734a903022249b3010be1897042568e" id="tgt280" class="tgtSentence">Move</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt281" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt282" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt283" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt284" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence sentenceid="50f8d4d3e73a87f26463b77a35f46c37" id="tgt285" class="tgtSentence">MoveFirst</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt286" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt287" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt288" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt289" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence sentenceid="aa4486cbb251418b54bf37a38e07877d" id="tgt290" class="tgtSentence">MoveLast</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt291" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt292" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt293" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt294" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence sentenceid="2651169204622cb80ec4b28ac12285ac" id="tgt295" class="tgtSentence">MoveNext</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt296" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt297" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt298" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt299" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence sentenceid="95caad3d8a11cee1b9d2914ef1e9667e" id="tgt300" class="tgtSentence">MovePrevious</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt301" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt302" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt303" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt304" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bb5a5af58a3fc812e2739058dde883f3" id="tgt305" class="tgtSentence">
                      <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>*</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt306" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt307" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt308" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt309" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">
                      <caps:sentence sentenceid="7cef8a734855777c2a9d0caf42666e69" id="tgt310" class="tgtSentence">Open</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt311" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt312" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt313" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt314" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">
                      <caps:sentence sentenceid="65d807e47b5cdafc34fc06e6d25cafd6" id="tgt315" class="tgtSentence">Requery</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt316" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt317" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt318" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt319" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">
                      <caps:sentence sentenceid="e365ce2f3002afe909c5591eb5c69889" id="tgt320" class="tgtSentence">Resync</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt321" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt322" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt323" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt324" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">
                      <caps:sentence sentenceid="72225dfc0ffc1c4e8471c5824c2c63c2" id="tgt325" class="tgtSentence">Supports</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt326" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt327" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt328" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt329" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">
                      <caps:sentence sentenceid="3ac340832f29c11538fbe2d6f75e8bcc" id="tgt330" class="tgtSentence">Update</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt331" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt332" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt333" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt334" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">
                      <caps:sentence sentenceid="f4651adedf889c8f0a0b0e38a2ee96fa" id="tgt335" class="tgtSentence">UpdateBatch</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt336" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt337" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt338" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt339" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="3e7560c80297f7c7ff356913dffc6974" id="tgt340" class="tgtSentence">*Not supported for Microsoft Access databases.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c9cc4b2425ec47fd6141efc88965a1d3" id="tgt341" class="tgtSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="69a25b7b39f16a5683cae874080398a4" id="tgt342" class="tgtSentence">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the <legacyBold>Properties</legacyBold> collection of the unopened <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c4d70f669b7e7098098781d22c2f0183" id="tgt343" class="tgtSentence">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</caps:sentence>
            <caps:sentence sentenceid="c8f596e13cecff8eedb595433f1d524a" id="tgt344" class="tgtSentence"> The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</caps:sentence>
            <caps:sentence sentenceid="5bd6c2a248f991e5772ecf53ac580449" id="tgt345" class="tgtSentence"> You can find more information about these properties in the OLE DB Programmer's Reference.</caps:sentence>
            <caps:sentence sentenceid="dd922c21aeab8495b30148842cb8d125" id="tgt346" class="tgtSentence"> Search for the OLE DB property name in the Index or see <legacyLink xlink:href="deded3ff-f508-4e1b-b2b1-fd9afd3bd292">Appendix C: OLE DB Properties</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="cc03d661ba78db29ad696232fbdfd45d" id="tgt347" class="tgtSentence">Connection Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ce76805809839c98859fe40ab1bc164e" id="tgt348" class="tgtSentence">The following properties are added to the <legacyBold>Connection</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt349" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt350" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42da7b3adedde15ba58b5e8f720f0729" id="tgt351" class="tgtSentence">Active Sessions</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5db97e3405ada5593894afe7c26e912a" id="tgt352" class="tgtSentence">DBPROP_ACTIVESESSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5fb6f6fbeeed9d35163820f4cad357a5" id="tgt353" class="tgtSentence">Asynchable Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a69ebf5e5b867b80a10c033ec247f235" id="tgt354" class="tgtSentence">DBPROP_ASYNCTXNABORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1553c09566f739d416c34417c3eed8bc" id="tgt355" class="tgtSentence">Asynchable Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8fb4c7f494cd85116f18f4e23dfa3ce2" id="tgt356" class="tgtSentence">DBPROP_ASYNCTNXCOMMIT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ac1b75d9d496be787670b775f6cbc81" id="tgt357" class="tgtSentence">Autocommit Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ed9f459c36be0b771e14849bddd615a" id="tgt358" class="tgtSentence">DBPROP_SESS_AUTOCOMMITISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04e7adcf92320728ff99be4ae9e20b80" id="tgt359" class="tgtSentence">Catalog Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cc7d88f9c70b084ff349547378be6ea7" id="tgt360" class="tgtSentence">DBPROP_CATALOGLOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0d5a9974623ad1d08ec1a87d28e3382b" id="tgt361" class="tgtSentence">Catalog Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5ec52858196e5661e26c0593dc0055f3" id="tgt362" class="tgtSentence">DBPROP_CATALOGTERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ccf0f62c35ce6f4ad47c504191cbc48" id="tgt363" class="tgtSentence">Column Definition</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4036e684cbb10c6c00160fb3f89fec78" id="tgt364" class="tgtSentence">DBPROP_COLUMNDEFINITION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf6acbf359c2d19032f195b15434cbdf" id="tgt365" class="tgtSentence">Connect Timeout</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb371d4f9db6357d81826f393345882e" id="tgt366" class="tgtSentence">DBPROP_INIT_TIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6cf2a5823099e39d4bfcd079068b384d" id="tgt367" class="tgtSentence">Current Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1975407cf7846b03983297436f6feaec" id="tgt368" class="tgtSentence">DBPROP_CURRENTCATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f0262ef78817e828a92d75e9749b4f9" id="tgt369" class="tgtSentence">Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f628f4ca9169da470c6349e4dadfd7b" id="tgt370" class="tgtSentence">DBPROP_INIT_DATASOURCE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4cc4008aeaa109c055aa7289fe8955f6" id="tgt371" class="tgtSentence">Data Source Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f70e2b308e36cc86cb62a25d0cc89d0" id="tgt372" class="tgtSentence">DBPROP_DATASOURCENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0902cf5b7d19a0cc4c0d745125932c99" id="tgt373" class="tgtSentence">Data Source Object Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6168b0502be04b450b621cc21978b79" id="tgt374" class="tgtSentence">DBPROP_DSOTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44576fc26ad5240af73f0f7304ac0161" id="tgt375" class="tgtSentence">DBMS Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8bfb66db9f6b9a9d8249efb32f35bc2" id="tgt376" class="tgtSentence">DBPROP_DBMSNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0865166992725c390cf3955eb7005314" id="tgt377" class="tgtSentence">DBMS Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="91a28922f266288ed023d4fb5e1a9f41" id="tgt378" class="tgtSentence">DBPROP_DBMSVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="01a074046ca4de7469fdd27ef0f56b30" id="tgt379" class="tgtSentence">Extended Properties</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ad981c384f6deb06078fb96a4f6db4af" id="tgt380" class="tgtSentence">DBPROP_INIT_PROVIDERSTRING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fc489b2e87836669c99f48d36447d508" id="tgt381" class="tgtSentence">GROUP BY Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b73b41cab609c063b7570db22674bb0" id="tgt382" class="tgtSentence">DBPROP_GROUPBY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7970e9c2391aaf6904a12c0b64590ee7" id="tgt383" class="tgtSentence">Heterogeneous Table Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8732f1c0c3c20adc7bc8f5f878f4e95f" id="tgt384" class="tgtSentence">DBPROP_HETEROGENEOUSTABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3cc7d428494725fbc1c4117841759a1b" id="tgt385" class="tgtSentence">Identifier Case Sensitivity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f959d99f6f9ff2380e84ed5f89a6545" id="tgt386" class="tgtSentence">DBPROP_IDENTIFIERCASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d61a95016e0ce8932a33ae801954fdbe" id="tgt387" class="tgtSentence">Initial Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="966c4e343eb272d1b5309d5b41dcd77e" id="tgt388" class="tgtSentence">DBPROP_INIT_CATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6d922da801c791516e0fde80744ddda1" id="tgt389" class="tgtSentence">Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b826970c6bc792cec29c7154b97b055f" id="tgt390" class="tgtSentence">DBPROP_SUPPORTEDTXNISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="36d2944c902a8b3bfc937a35534e6d67" id="tgt391" class="tgtSentence">Isolation Retention</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1180eb611191e300302c020a0433017a" id="tgt392" class="tgtSentence">DBPROP_SUPPORTEDTXNISORETAIN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d42b4f73ee8bf025a3c06cfa5499f55" id="tgt393" class="tgtSentence">Locale Identifier</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a119da28f65a0343b705f027db4eb589" id="tgt394" class="tgtSentence">DBPROP_INIT_LCID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5189de027922f81005951e6efe0efd5" id="tgt395" class="tgtSentence">Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4c7b060f7306f6b592e88374da28bc30" id="tgt396" class="tgtSentence">DBPROP_INIT_LOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d632dbafbc50f25c220bda2bd1d5eb79" id="tgt397" class="tgtSentence">Maximum Index Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0a5f4509b189658a32142048499fb311" id="tgt398" class="tgtSentence">DBPROP_MAXINDEXSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a3cbd82a49b4e695c986f9e21e08bec0" id="tgt399" class="tgtSentence">Maximum Row Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6414b671b9497a028ae03e2ff2baa8a2" id="tgt400" class="tgtSentence">DBPROP_MAXROWSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3fe8d182c92e2a2da388835b24f6a538" id="tgt401" class="tgtSentence">Maximum Row Size Includes BLOB</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82a79937366130603485b2e8243110f3" id="tgt402" class="tgtSentence">DBPROP_MAXROWSIZEINCLUDESBLOB</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="72fa89be4e41d4eec9682e3012510c70" id="tgt403" class="tgtSentence">Maximum Tables in SELECT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12775fa00655f15737d2b126875edf54" id="tgt404" class="tgtSentence">DBPROP_MAXTABLESINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="15d61712450a686a7f365adf4fef581f" id="tgt405" class="tgtSentence">Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e24a70a829cb0fe614e775e6b781aeef" id="tgt406" class="tgtSentence">DBPROP_INIT_MODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5fa88b3a7f2866a505f6869084d9dbac" id="tgt407" class="tgtSentence">Multiple Parameter Sets</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5b07a57182c870a463947bbe8862f2a" id="tgt408" class="tgtSentence">DBPROP_MULTIPLEPARAMSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34467f0701793e142a97280886a37d11" id="tgt409" class="tgtSentence">Multiple Results</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c6d16a5ed96ee324aaea5d56f93b9ca" id="tgt410" class="tgtSentence">DBPROP_MULTIPLERESULTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94a2500d5a620b62d088ba5e147f9300" id="tgt411" class="tgtSentence">Multiple Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4d0892bbf21bca8cbb05c7688e4481a" id="tgt412" class="tgtSentence">DBPROP_MULTIPLESTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49a7ede339dd477496917e520e53b211" id="tgt413" class="tgtSentence">Multi-Table Update</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45718feaf0858fc05c6e2c5653af9fa5" id="tgt414" class="tgtSentence">DBPROP_MULTITABLEUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="068577c6d2defffb1af7047830fb7e89" id="tgt415" class="tgtSentence">NULL Collation Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="169e04896d93bdec8bd59547b5636cf4" id="tgt416" class="tgtSentence">DBPROP_NULLCOLLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="51a10c8ee8acbdda689781c851e4dbfb" id="tgt417" class="tgtSentence">NULL Concatenation Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="86d53a1e665c382405ca707e70950ee9" id="tgt418" class="tgtSentence">DBPROP_CONCATNULLBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b6cc341a84e9a5f17c1bb02869de8f68" id="tgt419" class="tgtSentence">OLE DB Services</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="20f1f64900731090c77cd859723438e1" id="tgt420" class="tgtSentence">DBPROP_INIT_OLEDBSERVICES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54d02916d0ddd080374282c66901c59c" id="tgt421" class="tgtSentence">OLE DB Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8678185cda69da06b0b18cdede8c9aaf" id="tgt422" class="tgtSentence">DBPROP_PROVIDEROLEDBVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c77b810e588a10689239bf12710a9027" id="tgt423" class="tgtSentence">OLE Object Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9aa0a480916fc5befab6d11935037f12" id="tgt424" class="tgtSentence">DBPROP_OLEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="305717e26f640fcebb5c11bdf62692b0" id="tgt425" class="tgtSentence">Open Rowset Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="467a15dbf1a07da68a090197a6350d8e" id="tgt426" class="tgtSentence">DBPROP_OPENROWSETSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d8d10a19d6045a2990194103e79da9e6" id="tgt427" class="tgtSentence">ORDER BY Columns in Select List</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17519abd080309120a91fbe406545057" id="tgt428" class="tgtSentence">DBPROP_ORDERBYCOLUMNSINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c8bdd56df539c7147de1a6309ccf033" id="tgt429" class="tgtSentence">Output Parameter Availability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b3bb7f1b82d23d1accfa030b4372da90" id="tgt430" class="tgtSentence">DBPROP_OUTPUTPARAMETERAVAILABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f4dcc3b5aa765d61d8327deb882cf99" id="tgt431" class="tgtSentence">Password</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a4dad287f50102726dc53803031a610a" id="tgt432" class="tgtSentence">DBPROP_AUTH_PASSWORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ec1f372d153601374fe2b3be37c84a7" id="tgt433" class="tgtSentence">Pass By Ref Accessors</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b063a15f21255c314931eb858f8c898" id="tgt434" class="tgtSentence">DBPROP_BYREFACCESSORS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="503154ffbc8d4b9909f934dd562a5753" id="tgt435" class="tgtSentence">Persist Security Info</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7902596f88afd8b04b6b61fc09d1a39e" id="tgt436" class="tgtSentence">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d99d60bd887e031a71ff6eff10d6d3d4" id="tgt437" class="tgtSentence">Persistent ID Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ea254ecd2f23ef9f83d15db428137a57" id="tgt438" class="tgtSentence">DBPROP_PERSISTENTIDTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="77b5b43a8424c46e81df1ab0fc6e466d" id="tgt439" class="tgtSentence">Prepare Abort Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c461cd8da2a2986434667ac22d8c4113" id="tgt440" class="tgtSentence">DBPROP_PREPAREABORTBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc732b57d8b179ab01d66f1adcddf935" id="tgt441" class="tgtSentence">Prepare Commit Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5956c34c7c59de311a271e3cc843ced" id="tgt442" class="tgtSentence">DBPROP_PREPARECOMMITBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b307899aa47ab53211ca988c38acf75e" id="tgt443" class="tgtSentence">Procedure Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39fca27d3fe2656d61424456d445849b" id="tgt444" class="tgtSentence">DBPROP_PROCEDURETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ae35dbb42614d2429b7d6d181a950bb" id="tgt445" class="tgtSentence">Prompt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a23c8807135a34f56166fc290ce391c" id="tgt446" class="tgtSentence">DBPROP_INIT_PROMPT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ebbb5df827311326b2ebdcd6cf839f95" id="tgt447" class="tgtSentence">Provider Friendly Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="590bff2f7b8796e1277a936f16a2a7ff" id="tgt448" class="tgtSentence">DBPROP_PROVIDERFRIENDLYNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe158741a51803d31ec342eea567a79" id="tgt449" class="tgtSentence">Provider Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af443c478802f07802f2dc40b36c12b0" id="tgt450" class="tgtSentence">DBPROP_PROVIDERFILENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6ee1f505ae87ddc1ca51166091edec7" id="tgt451" class="tgtSentence">Provider Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d547dd6794dc65d1cbc34bc9a3646cab" id="tgt452" class="tgtSentence">DBPROP_PROVIDERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="14bb11993e3371d739eebc9648db4ec8" id="tgt453" class="tgtSentence">Read-Only Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fbaa45e63afd58892cad4204394e4b4a" id="tgt454" class="tgtSentence">DBPROP_DATASOURCEREADONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b68e1280ee9c56976f9918f1b143ae9b" id="tgt455" class="tgtSentence">Rowset Conversions on Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e9ea492c28f4f9e0ebe6ab7b04499f0a" id="tgt456" class="tgtSentence">DBPROP_ROWSETCONVERSIONSONCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4e214d42f27db2df22d820f4339ab38" id="tgt457" class="tgtSentence">Schema Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="177617f0fc571a0b532c7358fec97041" id="tgt458" class="tgtSentence">DBPROP_SCHEMATERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="996b43fdeae58150436e00ab086e55f9" id="tgt459" class="tgtSentence">Schema Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af6ca7abc5e28a6ba9bc5998e88fc4de" id="tgt460" class="tgtSentence">DBPROP_SCHEMAUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3887b124c8b8b2ac1076ac2fbc50a5a8" id="tgt461" class="tgtSentence">SQL Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67a078a8eabce39c390405b03eaf82df" id="tgt462" class="tgtSentence">DBPROP_SQLSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82b1c99e1276c7b9329843b82cb249a2" id="tgt463" class="tgtSentence">Structured Storage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a912ffa112b5c65343d1368268679294" id="tgt464" class="tgtSentence">DBPROP_STRUCTUREDSTORAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a51c825ecd8a692b685d0736d13a30c8" id="tgt465" class="tgtSentence">Subquery Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2dc44fc06f6f61c8b1e7f8c8b1dc7226" id="tgt466" class="tgtSentence">DBPROP_SUBQUERIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1fa0c9780d8a58f26e201af8cdc9d7d5" id="tgt467" class="tgtSentence">Table Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c25b152bb6a5d33613780d82b09f83f" id="tgt468" class="tgtSentence">DBPROP_TABLETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26e3db30e914b1bf231f1dc48149a6ab" id="tgt469" class="tgtSentence">Transaction DDL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d94fb60768ed9e61630670c5b707db5e" id="tgt470" class="tgtSentence">DBPROP_SUPPORTEDTXNDDL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3bd756a1167a9bff574b512092d53350" id="tgt471" class="tgtSentence">User ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d9c5665b97893aac40b03266365060d" id="tgt472" class="tgtSentence">DBPROP_AUTH_USERID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f28564ce8593a50b9cf507aecccd8cd6" id="tgt473" class="tgtSentence">User Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0673f982c2e13e63312a0a61aed98966" id="tgt474" class="tgtSentence">DBPROP_USERNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98487bfe9fe529e4a2738b2ad9eacaec" id="tgt475" class="tgtSentence">Window Handle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3a92acd985b6ab8b1df6d3cd4df47e83" id="tgt476" class="tgtSentence">DBPROP_INIT_HWND</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0d8dea92a1ae91e40f5bc79d56f722e5" id="tgt477" class="tgtSentence">Recordset Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b0067b1ce963cd0dc9fe2b6e39e482f5" id="tgt478" class="tgtSentence">The following properties are added to the <legacyBold>Recordset</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt479" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt480" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1594fad277e4590ddbbf46e340c4d10c" id="tgt481" class="tgtSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3ae70d0cfd08d73c0e8657de04e3ba3" id="tgt482" class="tgtSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b52683364c551ef6f2a83a9b61aca26" id="tgt483" class="tgtSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7eade57591bcbdf71a01307c5fa55333" id="tgt484" class="tgtSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39674232a2f3f57e87b6f56e9fcd620c" id="tgt485" class="tgtSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c5692554e1273a4cc28709961881f78" id="tgt486" class="tgtSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab13a6b41c0fedc395cff5ae82b531b6" id="tgt487" class="tgtSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt488" class="tgtSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="246a7d96dd79b612bad343d03ea2bec6" id="tgt489" class="tgtSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75cbb9fc61a14afcadf102cfdd0a6733" id="tgt490" class="tgtSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="534d9e8ffeeeff5bf0f381032bbefd20" id="tgt491" class="tgtSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3eac3ca56c13d98b9d1f1d8ef5620027" id="tgt492" class="tgtSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30f3aa8c0ff671730367a69d810898b9" id="tgt493" class="tgtSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32873d7085b6feb780bf00ea59c3a386" id="tgt494" class="tgtSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c34dec6888b6b898acb79b0597922c27" id="tgt495" class="tgtSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7906ea7eac0a5466ea33c9bf87d083db" id="tgt496" class="tgtSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c24d8cc4559e441d51781708292d746" id="tgt497" class="tgtSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b5c3be77a4c5f0654fd6637b3fd2b44" id="tgt498" class="tgtSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f518893e9bb8f74c9382260d0f79450b" id="tgt499" class="tgtSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2bdf72f0b7184d9ebe2e4086c598ee58" id="tgt500" class="tgtSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d33d5718660dbb261dc40b878ec4b591" id="tgt501" class="tgtSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fcb4539a8be17b29a97aada5fa31577" id="tgt502" class="tgtSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="28dbf41d74f2a648a563b28d2ecef878" id="tgt503" class="tgtSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba30e9909e02f6f6179f9db5cb9852cf" id="tgt504" class="tgtSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6317b9d062ca4ded11773f5df0c39062" id="tgt505" class="tgtSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12f702a41807df637765daa681fed78c" id="tgt506" class="tgtSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63e99e63156fc90f114fa402662387ef" id="tgt507" class="tgtSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="74868f1ee86eb0eaa5fb352a7f6c8f9e" id="tgt508" class="tgtSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="280d1ffb462810568a6fdc7ed49c472c" id="tgt509" class="tgtSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b34e9458e67545a04e915c7ef55719e8" id="tgt510" class="tgtSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="215599a847f963e27588b79210d3ea56" id="tgt511" class="tgtSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be4b610383a4b1af3438c855f29cb110" id="tgt512" class="tgtSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5e86d5adb921fd6e7b7616e2cc6d0b1" id="tgt513" class="tgtSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b8f2d2a246c88031ced7fa4b20e891d" id="tgt514" class="tgtSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5cf35ba4349e6da426be07d34952411e" id="tgt515" class="tgtSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37736c2f13339b1d0f75108bb2e84bd0" id="tgt516" class="tgtSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f7deea1588ac1cc7f77f6df70c1434b" id="tgt517" class="tgtSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f58d445e65ef2cd341481713e2aa6a9" id="tgt518" class="tgtSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1c6d3c5946bb65aba4e55669cac68a" id="tgt519" class="tgtSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8b178f861273bd6fcaa2cd53841838b" id="tgt520" class="tgtSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92f23aaea36b3e3b3f1b4b456d4b0f8a" id="tgt521" class="tgtSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt522" class="tgtSentence">DBPROP_IRowsetLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82189c22157ca5dbc1566ce5b8fee507" id="tgt523" class="tgtSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="869692d9e5c7b7dc7dcfdaf30a7bd348" id="tgt524" class="tgtSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fda716a018fb2c9d85d7f104af6d28fa" id="tgt525" class="tgtSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fd77e41428ef2a86d5994c0a4e658f" id="tgt526" class="tgtSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6fb965f1bd078f921c5a73f084a7d09" id="tgt527" class="tgtSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="130702210bcc45e1afd88b1f2aae1a0b" id="tgt528" class="tgtSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d1813dfdbbaa1c4660b2933198fb3f7" id="tgt529" class="tgtSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34cd68a4ad9a3b16548954ff8184424c" id="tgt530" class="tgtSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbe0ebf1ce342bea12faf4f9960e35db" id="tgt531" class="tgtSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="627482c800288bba5eaa6324bec11b5a" id="tgt532" class="tgtSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8709209928583492b7e8ee9057e1dcd2" id="tgt533" class="tgtSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37f4175871594fd8b8484066ab57df1f" id="tgt534" class="tgtSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="610508ace43dba0c007eb22818d91137" id="tgt535" class="tgtSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09b385ae7a340805af12a182ddf23eb4" id="tgt536" class="tgtSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f76fd118082b0c0ce064d13a83f97d8" id="tgt537" class="tgtSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2a235cb612ded93059abe7d46a49fe3" id="tgt538" class="tgtSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db2433d929e5ee5dac5bf4e762cb10ab" id="tgt539" class="tgtSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9cf646cc11e82fcf71add13e9d665dd" id="tgt540" class="tgtSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17bc94f9006a838977a349a959373da8" id="tgt541" class="tgtSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c018979b39f45a0e004063ce0373c75f" id="tgt542" class="tgtSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00045b5ae2bb643fd385c818dc8e48c6" id="tgt543" class="tgtSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cd5ca965481ad65661cdb310d078fa3" id="tgt544" class="tgtSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7319271b36838a8630e00ceb4554a65" id="tgt545" class="tgtSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f08474ed3d97c8e3919ffe184b8cb02e" id="tgt546" class="tgtSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ffd196cae96727a7c58c6701e3c65c1" id="tgt547" class="tgtSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45b7a56f3096b95b93f70ce662332136" id="tgt548" class="tgtSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8d7e45b16c6a09599199e5237263f63" id="tgt549" class="tgtSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="780561121ea65efc60d011b3855083ed" id="tgt550" class="tgtSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8bbf20691fd6dfdc3b55d73bb1b4df42" id="tgt551" class="tgtSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c89b03f5c13331074eed0814571479b" id="tgt552" class="tgtSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1be32916280f74ae0b5b31424efe2e97" id="tgt553" class="tgtSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="360431977c32a0e461c2a887196342cf" id="tgt554" class="tgtSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="015f02a3c579b5978974bb340adbc2ed" id="tgt555" class="tgtSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2fee318949f99eb5f0586e8492ffbaa" id="tgt556" class="tgtSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46634a21ff13d23b96f57f1b7a8e74b3" id="tgt557" class="tgtSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af57e2554f3db187894681afa3ebb162" id="tgt558" class="tgtSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="120451667e76bd8d13d0f0fce84d89e0" id="tgt559" class="tgtSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90f54100a94260ff7c00300f6cfd91d3" id="tgt560" class="tgtSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe1dffe626e729c9881c31329af50b19" id="tgt561" class="tgtSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="993c9b2a5a406fa810a7c0a353c0241d" id="tgt562" class="tgtSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62dbebf39ca99d9e0f7d2548b1a1e897" id="tgt563" class="tgtSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="594965351c01632879dd3120d6bdf6d1" id="tgt564" class="tgtSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dacf8514ed973feacfcb951277d7a7e0" id="tgt565" class="tgtSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26a6a1d6d267ebfa661503a67852b551" id="tgt566" class="tgtSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78e460d27437866f950bef1a322f4fad" id="tgt567" class="tgtSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1082afc70d114a04c5a7c028f54bbef" id="tgt568" class="tgtSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af912945703d4c7e5769a4a5e275c429" id="tgt569" class="tgtSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e89662e8e842b5980db8ce27cddbb136" id="tgt570" class="tgtSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f0866326f49f046b4c2d341fbf8b4a8" id="tgt571" class="tgtSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1a3b43e5bc3c750c8484e75d2dc513" id="tgt572" class="tgtSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d147a76184915ab68be6596b43255f" id="tgt573" class="tgtSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d60a3e481cd7af54f8384abea4e16a7c" id="tgt574" class="tgtSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65b8fe6df5aa2933471401a6b676fba7" id="tgt575" class="tgtSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1198df197cf7df924a1b241c2b2f0043" id="tgt576" class="tgtSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18919c01495e96c385f2eaf5938a7b03" id="tgt577" class="tgtSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdb695a9cc13c0f5e2c73bda79d0aaf" id="tgt578" class="tgtSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a40c17ef17a290d8ff208c5db8518c1" id="tgt579" class="tgtSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78cbcb8d94e6c7daf9e961f93e6b2886" id="tgt580" class="tgtSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d19dc5275a879b3a434a516970425f79" id="tgt581" class="tgtSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5b98c46a74cf81a3a5714e4746025dc3" id="tgt582" class="tgtSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb5fb6c60c1d012edd101ab61e996364" id="tgt583" class="tgtSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8a7611a82fb7d9716f4f12a82fb60754" id="tgt584" class="tgtSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e51a0debee4b6fc0ca6b1e781fc16df7" id="tgt585" class="tgtSentence">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16753e39b4d45199dca719ac2995aeb1" id="tgt586" class="tgtSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="824f2ba91f8243744ab6a8227fbb157f" id="tgt587" class="tgtSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adc2bf5dd51cf373e1aacf17aef14bbd" id="tgt588" class="tgtSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ac6cf4fa0ff0c7b5050593b220d13af2" id="tgt589" class="tgtSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="692ef25d05bb91b856cf5d0564cf74fd" id="tgt590" class="tgtSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87f408e0686b76395d281e685f65bc08" id="tgt591" class="tgtSentence">DBPROP_BOOKMARKSKIPPED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2463d9a101f9c39973277d105f8bf119" id="tgt592" class="tgtSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b4fbfcb976445a344da1d0972764bf0d" id="tgt593" class="tgtSentence">DBPROP_STRONGITDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3d6c9ba3726667cb820e5f392952aca6" id="tgt594" class="tgtSentence">Unique Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fe0a5bebaaa20210a94be8f859bc9b3" id="tgt595" class="tgtSentence">DBPROP_UNIQUEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11c74d1c21dc5dbb8b802a7408596d87" id="tgt596" class="tgtSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2086801d6ac44d08784890faac1a126" id="tgt597" class="tgtSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7a56dd282a8abf8100c423430ec8e4ac" id="tgt598" class="tgtSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd43d482f9e85ec89014c21fbd361a4" id="tgt599" class="tgtSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="af1974d09c74dc4d634c2cdc45a0ab7c" id="tgt600" class="tgtSentence">Command Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="03828b2fe06fc2b202e5fed5623575a6" id="tgt601" class="tgtSentence">The following properties are added to the <legacyBold>Command</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt602" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt603" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1594fad277e4590ddbbf46e340c4d10c" id="tgt604" class="tgtSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3ae70d0cfd08d73c0e8657de04e3ba3" id="tgt605" class="tgtSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b52683364c551ef6f2a83a9b61aca26" id="tgt606" class="tgtSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7eade57591bcbdf71a01307c5fa55333" id="tgt607" class="tgtSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39674232a2f3f57e87b6f56e9fcd620c" id="tgt608" class="tgtSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c5692554e1273a4cc28709961881f78" id="tgt609" class="tgtSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab13a6b41c0fedc395cff5ae82b531b6" id="tgt610" class="tgtSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt611" class="tgtSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="246a7d96dd79b612bad343d03ea2bec6" id="tgt612" class="tgtSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75cbb9fc61a14afcadf102cfdd0a6733" id="tgt613" class="tgtSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="534d9e8ffeeeff5bf0f381032bbefd20" id="tgt614" class="tgtSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3eac3ca56c13d98b9d1f1d8ef5620027" id="tgt615" class="tgtSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30f3aa8c0ff671730367a69d810898b9" id="tgt616" class="tgtSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32873d7085b6feb780bf00ea59c3a386" id="tgt617" class="tgtSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c34dec6888b6b898acb79b0597922c27" id="tgt618" class="tgtSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7906ea7eac0a5466ea33c9bf87d083db" id="tgt619" class="tgtSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c24d8cc4559e441d51781708292d746" id="tgt620" class="tgtSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b5c3be77a4c5f0654fd6637b3fd2b44" id="tgt621" class="tgtSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f518893e9bb8f74c9382260d0f79450b" id="tgt622" class="tgtSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2bdf72f0b7184d9ebe2e4086c598ee58" id="tgt623" class="tgtSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d33d5718660dbb261dc40b878ec4b591" id="tgt624" class="tgtSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fcb4539a8be17b29a97aada5fa31577" id="tgt625" class="tgtSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="28dbf41d74f2a648a563b28d2ecef878" id="tgt626" class="tgtSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba30e9909e02f6f6179f9db5cb9852cf" id="tgt627" class="tgtSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6317b9d062ca4ded11773f5df0c39062" id="tgt628" class="tgtSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12f702a41807df637765daa681fed78c" id="tgt629" class="tgtSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63e99e63156fc90f114fa402662387ef" id="tgt630" class="tgtSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="74868f1ee86eb0eaa5fb352a7f6c8f9e" id="tgt631" class="tgtSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="280d1ffb462810568a6fdc7ed49c472c" id="tgt632" class="tgtSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b34e9458e67545a04e915c7ef55719e8" id="tgt633" class="tgtSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="215599a847f963e27588b79210d3ea56" id="tgt634" class="tgtSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be4b610383a4b1af3438c855f29cb110" id="tgt635" class="tgtSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5e86d5adb921fd6e7b7616e2cc6d0b1" id="tgt636" class="tgtSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b8f2d2a246c88031ced7fa4b20e891d" id="tgt637" class="tgtSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5cf35ba4349e6da426be07d34952411e" id="tgt638" class="tgtSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37736c2f13339b1d0f75108bb2e84bd0" id="tgt639" class="tgtSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f7deea1588ac1cc7f77f6df70c1434b" id="tgt640" class="tgtSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f58d445e65ef2cd341481713e2aa6a9" id="tgt641" class="tgtSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1c6d3c5946bb65aba4e55669cac68a" id="tgt642" class="tgtSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8b178f861273bd6fcaa2cd53841838b" id="tgt643" class="tgtSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92f23aaea36b3e3b3f1b4b456d4b0f8a" id="tgt644" class="tgtSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt645" class="tgtSentence">DBPROP_IRowsetLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82189c22157ca5dbc1566ce5b8fee507" id="tgt646" class="tgtSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="869692d9e5c7b7dc7dcfdaf30a7bd348" id="tgt647" class="tgtSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fda716a018fb2c9d85d7f104af6d28fa" id="tgt648" class="tgtSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fd77e41428ef2a86d5994c0a4e658f" id="tgt649" class="tgtSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6fb965f1bd078f921c5a73f084a7d09" id="tgt650" class="tgtSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="130702210bcc45e1afd88b1f2aae1a0b" id="tgt651" class="tgtSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d1813dfdbbaa1c4660b2933198fb3f7" id="tgt652" class="tgtSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34cd68a4ad9a3b16548954ff8184424c" id="tgt653" class="tgtSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbe0ebf1ce342bea12faf4f9960e35db" id="tgt654" class="tgtSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="627482c800288bba5eaa6324bec11b5a" id="tgt655" class="tgtSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8709209928583492b7e8ee9057e1dcd2" id="tgt656" class="tgtSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37f4175871594fd8b8484066ab57df1f" id="tgt657" class="tgtSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="610508ace43dba0c007eb22818d91137" id="tgt658" class="tgtSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09b385ae7a340805af12a182ddf23eb4" id="tgt659" class="tgtSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f76fd118082b0c0ce064d13a83f97d8" id="tgt660" class="tgtSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2a235cb612ded93059abe7d46a49fe3" id="tgt661" class="tgtSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db2433d929e5ee5dac5bf4e762cb10ab" id="tgt662" class="tgtSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9cf646cc11e82fcf71add13e9d665dd" id="tgt663" class="tgtSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17bc94f9006a838977a349a959373da8" id="tgt664" class="tgtSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c018979b39f45a0e004063ce0373c75f" id="tgt665" class="tgtSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00045b5ae2bb643fd385c818dc8e48c6" id="tgt666" class="tgtSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cd5ca965481ad65661cdb310d078fa3" id="tgt667" class="tgtSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7319271b36838a8630e00ceb4554a65" id="tgt668" class="tgtSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f08474ed3d97c8e3919ffe184b8cb02e" id="tgt669" class="tgtSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ffd196cae96727a7c58c6701e3c65c1" id="tgt670" class="tgtSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45b7a56f3096b95b93f70ce662332136" id="tgt671" class="tgtSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8d7e45b16c6a09599199e5237263f63" id="tgt672" class="tgtSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="780561121ea65efc60d011b3855083ed" id="tgt673" class="tgtSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8bbf20691fd6dfdc3b55d73bb1b4df42" id="tgt674" class="tgtSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c89b03f5c13331074eed0814571479b" id="tgt675" class="tgtSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1be32916280f74ae0b5b31424efe2e97" id="tgt676" class="tgtSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="360431977c32a0e461c2a887196342cf" id="tgt677" class="tgtSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="015f02a3c579b5978974bb340adbc2ed" id="tgt678" class="tgtSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2fee318949f99eb5f0586e8492ffbaa" id="tgt679" class="tgtSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46634a21ff13d23b96f57f1b7a8e74b3" id="tgt680" class="tgtSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af57e2554f3db187894681afa3ebb162" id="tgt681" class="tgtSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="120451667e76bd8d13d0f0fce84d89e0" id="tgt682" class="tgtSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90f54100a94260ff7c00300f6cfd91d3" id="tgt683" class="tgtSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe1dffe626e729c9881c31329af50b19" id="tgt684" class="tgtSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="993c9b2a5a406fa810a7c0a353c0241d" id="tgt685" class="tgtSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62dbebf39ca99d9e0f7d2548b1a1e897" id="tgt686" class="tgtSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="594965351c01632879dd3120d6bdf6d1" id="tgt687" class="tgtSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dacf8514ed973feacfcb951277d7a7e0" id="tgt688" class="tgtSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26a6a1d6d267ebfa661503a67852b551" id="tgt689" class="tgtSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78e460d27437866f950bef1a322f4fad" id="tgt690" class="tgtSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1082afc70d114a04c5a7c028f54bbef" id="tgt691" class="tgtSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af912945703d4c7e5769a4a5e275c429" id="tgt692" class="tgtSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e89662e8e842b5980db8ce27cddbb136" id="tgt693" class="tgtSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f0866326f49f046b4c2d341fbf8b4a8" id="tgt694" class="tgtSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1a3b43e5bc3c750c8484e75d2dc513" id="tgt695" class="tgtSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d147a76184915ab68be6596b43255f" id="tgt696" class="tgtSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d60a3e481cd7af54f8384abea4e16a7c" id="tgt697" class="tgtSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65b8fe6df5aa2933471401a6b676fba7" id="tgt698" class="tgtSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1198df197cf7df924a1b241c2b2f0043" id="tgt699" class="tgtSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18919c01495e96c385f2eaf5938a7b03" id="tgt700" class="tgtSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdb695a9cc13c0f5e2c73bda79d0aaf" id="tgt701" class="tgtSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a40c17ef17a290d8ff208c5db8518c1" id="tgt702" class="tgtSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78cbcb8d94e6c7daf9e961f93e6b2886" id="tgt703" class="tgtSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d19dc5275a879b3a434a516970425f79" id="tgt704" class="tgtSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5b98c46a74cf81a3a5714e4746025dc3" id="tgt705" class="tgtSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb5fb6c60c1d012edd101ab61e996364" id="tgt706" class="tgtSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8a7611a82fb7d9716f4f12a82fb60754" id="tgt707" class="tgtSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3528ed34871b6b038968af4a908dc081" id="tgt708" class="tgtSentence">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16753e39b4d45199dca719ac2995aeb1" id="tgt709" class="tgtSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="824f2ba91f8243744ab6a8227fbb157f" id="tgt710" class="tgtSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adc2bf5dd51cf373e1aacf17aef14bbd" id="tgt711" class="tgtSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ac6cf4fa0ff0c7b5050593b220d13af2" id="tgt712" class="tgtSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="692ef25d05bb91b856cf5d0564cf74fd" id="tgt713" class="tgtSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7bffaed4f81d15733e9f3df7fcdb33a4" id="tgt714" class="tgtSentence">DBPROP_BOOKMARKSKIP</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2463d9a101f9c39973277d105f8bf119" id="tgt715" class="tgtSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f0289c4d7472816b838bf34a3b92d2c" id="tgt716" class="tgtSentence">DBPROP_STRONGIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11c74d1c21dc5dbb8b802a7408596d87" id="tgt717" class="tgtSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2086801d6ac44d08784890faac1a126" id="tgt718" class="tgtSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7a56dd282a8abf8100c423430ec8e4ac" id="tgt719" class="tgtSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd43d482f9e85ec89014c21fbd361a4" id="tgt720" class="tgtSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="5adc4bf6664a2295a3925cb2f1a89dac" id="tgt721" class="tgtSentence">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, see the <legacyLink xlink:href="3c5e2dd5-35e5-4a93-ac3a-3818bb43bbf8">OLE DB Programmer's Reference</legacyLink> or visit the Data Access and Storage Developer Center Web site on MSDN.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString Property</link>
        <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> However, most DBMS systems in use today can be accessed through ODBC.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The provider is free-threaded and Unicode enabled.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">The provider supports transactions, although different DBMS engines offer different types of transaction support.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> For example, Microsoft Access supports nested transactions up to five levels deep.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">To connect to this provider, set the <legacyBold>Provider=</legacyBold> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to:</caps:sentence>
          </para>
          <code>MSDASQL</code>
          <para>
            <caps:sentence id="src12" class="srcSentence">Reading the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property will return this string as well.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Typical Connection String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">A typical connection string for this provider is:</caps:sentence>
          </para>
          <code>"Provider=MSDASQL;DSN=<legacyItalic xmlns="">dsnName</legacyItalic>;UID=<legacyItalic xmlns="">MyUserID</legacyItalic>;PWD=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
          <para>
            <caps:sentence id="src15" class="srcSentence">The string consists of these keywords:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Keyword</caps:sentence>
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
                    <legacyBold>
                      <caps:sentence id="src18" class="srcSentence">Provider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Specifies the OLE DB provider for ODBC.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src20" class="srcSentence">DSN</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Specifies the data source name.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src22" class="srcSentence">UID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Specifies the user name.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src24" class="srcSentence">PWD</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Specifies the user password.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src26" class="srcSentence">URL</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Specifies the URL of a file or directory published in a Web folder.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src28" class="srcSentence">Because this is the default provider for ADO, if you omit the <legacyBold>Provider=</legacyBold> parameter from the connection string, ADO will try to establish a connection to this provider.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src29" class="srcSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <system>Trusted_Connection=yes</system> or <system>Integrated Security = SSPI</system> instead of user ID and password information in the connection string.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src30" class="srcSentence">The provider does not support any specific connection parameters in addition to those defined by ADO.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">Because you can omit the <legacyBold>Provider</legacyBold> parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> Use the same parameter names (<legacyBold>DRIVER=</legacyBold>, <legacyBold>DATABASE=</legacyBold>, <legacyBold>DSN=</legacyBold>, and so on), values, and syntax as you would when composing an ODBC connection string.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> You can connect with or without a predefined data source name (DSN) or FileDSN.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src35" class="srcSentence">Syntax with a DSN or FileDSN:</caps:sentence>
        </title>
        <content>
          <code>"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; 
[DATABASE=database;] UID=user; PWD=password"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src36" class="srcSentence">Syntax without a DSN (DSN-less connection):</caps:sentence>
        </title>
        <content>
          <code>"[Provider=MSDASQL;] DRIVER=driver; SERVER=server; 
DATABASE=database; UID=MyUserID; PWD=MyPassword"</code>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src37" class="srcSentence">If you use a <legacyBold>DSN</legacyBold> or <legacyBold>FileDSN</legacyBold>, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> In earlier versions of Windows, the ODBC Administrator icon is named <legacyBold>32-bit ODBC</legacyBold> or just <legacyBold>ODBC</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src40" class="srcSentence">As an alternative to setting a <legacyBold>DSN</legacyBold>, you can specify the ODBC driver (<legacyBold>DRIVER=</legacyBold>), such as "SQL Server;" the server name (<legacyBold>SERVER=</legacyBold>); and the database name (<legacyBold>DATABASE=</legacyBold>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src41" class="srcSentence">You can also specify a user account name (<legacyBold>UID=</legacyBold>), and the password for the user account (<legacyBold>PWD=</legacyBold>) in the ODBC-specific parameters or in the standard ADO-defined <legacyItalic>user</legacyItalic> and <legacyItalic>password</legacyItalic> parameters.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src42" class="srcSentence">Although a <legacyBold>DSN</legacyBold> definition already specifies a database, you can specify <legacyItalic>a</legacyItalic> <legacyItalic>database</legacyItalic> parameter in addition to a <legacyBold>DSN</legacyBold> to connect to a different database.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> It is a good idea to always include <legacyItalic>the</legacyItalic> <legacyItalic>database</legacyItalic> parameter when you use a <legacyBold>DSN</legacyBold>.</caps:sentence>
            <caps:sentence id="src44" class="srcSentence"> This will ensure that you connect to the correct database if another user changed the default database parameter since you last checked the <legacyBold>DSN</legacyBold> definition.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src45" class="srcSentence">Provider-Specific Connection Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src46" class="srcSentence">The OLE DB provider for ODBC adds several properties to the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> The following table lists these properties with the corresponding OLE DB property name in parentheses.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Accessible Procedures (KAGPROP_ACCESSIBLEPROCEDURES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Indicates whether the user has access to stored procedures.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Accessible Tables (KAGPROP_ACCESSIBLETABLES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Indicates whether the user has permission to execute SELECT statements against the database tables.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Active Statements (KAGPROP_ACTIVESTATEMENTS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Indicates the number of handles an ODBC driver can support on a connection.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Driver Name (KAGPROP_DRIVERNAME)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Indicates the file name of the ODBC driver.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">Driver ODBC Version (KAGPROP_DRIVERODBCVER)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Indicates the version of ODBC that this driver supports.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">File Usage (KAGPROP_FILEUSAGE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">Indicates how the driver treats a file in a data source; as a table or as a catalog.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Like Escape Clause (KAGPROP_LIKEESCAPECLAUSE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">Max Columns in Group By (KAGPROP_MAXCOLUMNSINGROUPBY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">Max Columns in Index (KAGPROP_MAXCOLUMNSININDEX)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">Indicates the maximum number of columns that can be included in an index.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">Max Columns in Order By (KAGPROP_MAXCOLUMNSINORDERBY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">Max Columns in Select (KAGPROP_MAXCOLUMNSINSELECT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Max Columns in Table (KAGPROP_MAXCOLUMNSINTABLE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">Indicates the maximum number of columns allowed in a table.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">Numeric Functions (KAGPROP_NUMERICFUNCTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">Indicates which numeric functions are supported by the ODBC driver.</caps:sentence>
                    <caps:sentence id="src76" class="srcSentence"> For a listing of function names and the associated values used in this bitmask, see <legacyLink xlink:href="59c7cd5e-32d6-43ab-bac3-7010322d105a">Appendix E: Scalar Functions</legacyLink>, in the ODBC documentation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">Outer Join Capabilities (KAGPROP_OJCAPABILITY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">Indicates the types of OUTER JOINs supported by the provider.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">Outer Joins (KAGPROP_OUTERJOINS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">Indicates whether the provider supports OUTER JOINs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">Special Characters (KAGPROP_SPECIALCHARACTERS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">Indicates which characters have special meaning for the ODBC driver.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">Stored Procedures (KAGPROP_PROCEDURES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">Indicates whether stored procedures are available for use with this ODBC driver.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">String Functions (KAGPROP_STRINGFUNCTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">Indicates which string functions are supported by the ODBC driver.</caps:sentence>
                    <caps:sentence id="src87" class="srcSentence"> For a listing of function names and the associated values used in this bitmask, see <legacyLink xlink:href="59c7cd5e-32d6-43ab-bac3-7010322d105a">Appendix E: Scalar Functions</legacyLink>, in the ODBC documentation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">System Functions (KAGPROP_SYSTEMFUNCTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">Indicates which system functions are supported by the ODBC driver.</caps:sentence>
                    <caps:sentence id="src90" class="srcSentence"> For a listing of function names and the associated values used in this bitmask, see <legacyLink xlink:href="59c7cd5e-32d6-43ab-bac3-7010322d105a">Appendix E: Scalar Functions</legacyLink>, in the ODBC documentation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">Time/Date Functions (KAGPROP_TIMEDATEFUNCTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">Indicates which time and date functions are supported by the ODBC driver.</caps:sentence>
                    <caps:sentence id="src93" class="srcSentence"> For a listing of function names and the associated values used in this bitmask, see <legacyLink xlink:href="59c7cd5e-32d6-43ab-bac3-7010322d105a">Appendix E: Scalar Functions</legacyLink>, in the ODBC documentation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">SQL Grammar Support (KAGPROP_ODBCSQLCONFORMANCE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">Indicates the SQL grammar that the ODBC driver supports.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src96" class="srcSentence">Provider-Specific Recordset and Command Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src97" class="srcSentence">The OLE DB provider for ODBC adds several properties to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> and <legacyBold>Command</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src98" class="srcSentence"> The following table lists these properties with the corresponding OLE DB property name in parentheses.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">Query Based Updates/Deletes/Inserts (KAGPROP_QUERYBASEDUPDATES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">Indicates whether updates, deletions, and insertions can be performed by using SQL queries.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src103" class="srcSentence">ODBC Concurrency Type (KAGPROP_CONCURRENCY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">Indicates the method used to reduce potential problems caused by two users trying to access the same data from the data source simultaneously.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">BLOB accessibility on Forward-Only cursor (KAGPROP_BLOBSONFOCURSOR)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">Indicates whether BLOB <legacyBold>Fields</legacyBold> can be accessed when using a forward-only cursor.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses (KAGPROP_INCLUDENONEXACT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">Position on the last row after insert (KAGPROP_POSITIONONNEWROW)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">IRowsetChangeExtInfo (KAGPROP_IROWSETCHANGEEXTINFO)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">Indicates whether the <legacyBold>IRowsetChange</legacyBold> interface provides extended information support.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">ODBC Cursor Type (KAGPROP_CURSOR)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">Indicates the type of cursor used by the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">Generate a Rowset that can be marshaled (KAGPROP_MARSHALLABLE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">Indicates that the ODBC driver generates a recordset that can be marshaled</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src117" class="srcSentence">Command Text</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src118" class="srcSentence">How you use the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object largely depends on the data source, and what type of query or command statement it will accept.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src119" class="srcSentence">ODBC provides a specific syntax for calling stored procedures.</caps:sentence>
            <caps:sentence id="src120" class="srcSentence"> For the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property of a <legacyBold>Command</legacyBold> object, the <legacyItalic>CommandText </legacyItalic>argument to the <legacyBold>Execute</legacyBold> method on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, or the <legacyItalic>Source</legacyItalic> argument to the <legacyBold>Open</legacyBold> method on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, passes in a string with this syntax:</caps:sentence>
          </para>
          <code>"{ [ ? = ] call procedure [ ( ? [, ? [ , … ]] ) ] }"</code>
          <para>
            <caps:sentence id="src121" class="srcSentence">Each <legacyBold>?</legacyBold> references an object in the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
            <caps:sentence id="src122" class="srcSentence"> The first <legacyBold>?</legacyBold> references <legacyBold>Parameters</legacyBold>(0), the next <legacyBold>?</legacyBold> references <legacyBold>Parameters</legacyBold>(1), and so on.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src123" class="srcSentence">The parameter references are optional and depend on the structure of the stored procedure.</caps:sentence>
            <caps:sentence id="src124" class="srcSentence"> If you want to call a stored procedure that defines no parameters, your string would look like the following:</caps:sentence>
          </para>
          <code>"{ call procedure }"</code>
          <para>
            <caps:sentence id="src125" class="srcSentence">If you have two query parameters, your string would resemble the following:</caps:sentence>
          </para>
          <code>"{ call procedure ( ?, ? ) }"</code>
          <para>
            <caps:sentence id="src126" class="srcSentence">If the stored procedure will return a value, the return value is treated as another parameter.</caps:sentence>
            <caps:sentence id="src127" class="srcSentence"> If you have no query parameters but you do have a return value, your string would resemble the following:</caps:sentence>
          </para>
          <code>"{ ? = call procedure }"</code>
          <para>
            <caps:sentence id="src128" class="srcSentence">Finally, if you have a return value and two query parameters, your string would resemble the following:</caps:sentence>
          </para>
          <code>"{ ? = call procedure ( ?, ? ) }"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src129" class="srcSentence">Recordset Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src130" class="srcSentence">The following tables list the standard ADO methods and properties available on a <legacyBold>Recordset</legacyBold> object opened with this provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src131" class="srcSentence">For more detailed information about <legacyBold>Recordset</legacyBold> behavior for your provider configuration, run the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method and enumerate the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> to determine whether provider-specific dynamic properties are present.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src132" class="srcSentence">Availability of standard ADO <legacyBold>Recordset</legacyBold> properties:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">Property</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">ForwardOnly</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">Dynamic</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">Keyset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">Static</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">
                      <caps:sentence id="src138" class="srcSentence">AbsolutePage</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">
                      <caps:sentence id="src143" class="srcSentence">AbsolutePosition</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">
                      <caps:sentence id="src148" class="srcSentence">ActiveConnection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">
                      <caps:sentence id="src153" class="srcSentence">BOF</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src155" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">
                      <caps:sentence id="src158" class="srcSentence">Bookmark</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">
                      <caps:sentence id="src163" class="srcSentence">CacheSize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">
                      <caps:sentence id="src168" class="srcSentence">CursorLocation</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">
                      <caps:sentence id="src173" class="srcSentence">CursorType</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a1b04bb2-8c8b-47f9-8477-bfd0368b6f68">
                      <caps:sentence id="src178" class="srcSentence">EditMode</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">
                      <caps:sentence id="src183" class="srcSentence">Filter</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">
                      <caps:sentence id="src188" class="srcSentence">LockType</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src190" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">
                      <caps:sentence id="src193" class="srcSentence">MarshalOptions</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src197" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="20c76571-8c9a-482c-a99e-726ab1d93f8b">
                      <caps:sentence id="src198" class="srcSentence">MaxRecords</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">
                      <caps:sentence id="src203" class="srcSentence">PageCount</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src206" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="e57930a6-46c4-4a17-a3b6-f79e94d5c9c7">
                      <caps:sentence id="src208" class="srcSentence">PageSize</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src210" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src211" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">
                      <caps:sentence id="src213" class="srcSentence">RecordCount</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src215" class="srcSentence">not available</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src216" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src217" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">
                      <caps:sentence id="src218" class="srcSentence">Source</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src219" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src220" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src221" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src222" class="srcSentence">read/write</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">
                      <caps:sentence id="src223" class="srcSentence">State</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src225" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src226" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src227" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">
                      <caps:sentence id="src228" class="srcSentence">Status</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src229" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src230" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">read-only</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src233" class="srcSentence">The <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink> and <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink> properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src234" class="srcSentence">Availability of standard ADO <legacyBold>Recordset</legacyBold> methods:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src235" class="srcSentence">Method</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src236" class="srcSentence">ForwardOnly</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src237" class="srcSentence">Dynamic</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src238" class="srcSentence">Keyset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src239" class="srcSentence">Static</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">
                      <caps:sentence id="src240" class="srcSentence">AddNew</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src241" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src242" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src243" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">
                      <caps:sentence id="src245" class="srcSentence">Cancel</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src248" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">
                      <caps:sentence id="src250" class="srcSentence">CancelBatch</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src251" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src252" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src253" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src254" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">
                      <caps:sentence id="src255" class="srcSentence">CancelUpdate</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src256" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src257" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src258" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src259" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">
                      <caps:sentence id="src260" class="srcSentence">Clone</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src261" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src262" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src263" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src264" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">
                      <caps:sentence id="src265" class="srcSentence">Close</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src267" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src268" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src269" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">
                      <caps:sentence id="src270" class="srcSentence">Delete</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src271" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src272" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src273" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src274" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="14b92860-4171-47d9-a413-dd60dd6a8880">
                      <caps:sentence id="src275" class="srcSentence">GetRows</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src276" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src277" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src278" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">
                      <caps:sentence id="src280" class="srcSentence">Move</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src281" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src282" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src283" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src284" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence id="src285" class="srcSentence">MoveFirst</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src286" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src287" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src288" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src289" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence id="src290" class="srcSentence">MoveLast</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src291" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src292" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src293" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src294" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence id="src295" class="srcSentence">MoveNext</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src296" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src297" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src298" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src299" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                      <caps:sentence id="src300" class="srcSentence">MovePrevious</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src301" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src302" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src303" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src304" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src305" class="srcSentence">
                      <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">NextRecordset</legacyLink>*</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src306" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src307" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src308" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src309" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">
                      <caps:sentence id="src310" class="srcSentence">Open</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src311" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src312" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src313" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src314" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">
                      <caps:sentence id="src315" class="srcSentence">Requery</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src316" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src317" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src318" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src319" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">
                      <caps:sentence id="src320" class="srcSentence">Resync</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src321" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src322" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src323" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src324" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">
                      <caps:sentence id="src325" class="srcSentence">Supports</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src326" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src327" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src328" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src329" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">
                      <caps:sentence id="src330" class="srcSentence">Update</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src331" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src332" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src333" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src334" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">
                      <caps:sentence id="src335" class="srcSentence">UpdateBatch</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src336" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src337" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src338" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src339" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src340" class="srcSentence">*Not supported for Microsoft Access databases.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src341" class="srcSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src342" class="srcSentence">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the <legacyBold>Properties</legacyBold> collection of the unopened <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src343" class="srcSentence">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</caps:sentence>
            <caps:sentence id="src344" class="srcSentence"> The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</caps:sentence>
            <caps:sentence id="src345" class="srcSentence"> You can find more information about these properties in the OLE DB Programmer's Reference.</caps:sentence>
            <caps:sentence id="src346" class="srcSentence"> Search for the OLE DB property name in the Index or see <legacyLink xlink:href="deded3ff-f508-4e1b-b2b1-fd9afd3bd292">Appendix C: OLE DB Properties</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src347" class="srcSentence">Connection Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src348" class="srcSentence">The following properties are added to the <legacyBold>Connection</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src349" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src350" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src351" class="srcSentence">Active Sessions</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src352" class="srcSentence">DBPROP_ACTIVESESSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src353" class="srcSentence">Asynchable Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src354" class="srcSentence">DBPROP_ASYNCTXNABORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src355" class="srcSentence">Asynchable Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src356" class="srcSentence">DBPROP_ASYNCTNXCOMMIT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src357" class="srcSentence">Autocommit Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src358" class="srcSentence">DBPROP_SESS_AUTOCOMMITISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src359" class="srcSentence">Catalog Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src360" class="srcSentence">DBPROP_CATALOGLOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src361" class="srcSentence">Catalog Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src362" class="srcSentence">DBPROP_CATALOGTERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src363" class="srcSentence">Column Definition</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src364" class="srcSentence">DBPROP_COLUMNDEFINITION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src365" class="srcSentence">Connect Timeout</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src366" class="srcSentence">DBPROP_INIT_TIMEOUT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src367" class="srcSentence">Current Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src368" class="srcSentence">DBPROP_CURRENTCATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src369" class="srcSentence">Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src370" class="srcSentence">DBPROP_INIT_DATASOURCE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src371" class="srcSentence">Data Source Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src372" class="srcSentence">DBPROP_DATASOURCENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src373" class="srcSentence">Data Source Object Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src374" class="srcSentence">DBPROP_DSOTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src375" class="srcSentence">DBMS Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src376" class="srcSentence">DBPROP_DBMSNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src377" class="srcSentence">DBMS Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src378" class="srcSentence">DBPROP_DBMSVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src379" class="srcSentence">Extended Properties</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src380" class="srcSentence">DBPROP_INIT_PROVIDERSTRING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src381" class="srcSentence">GROUP BY Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src382" class="srcSentence">DBPROP_GROUPBY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src383" class="srcSentence">Heterogeneous Table Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src384" class="srcSentence">DBPROP_HETEROGENEOUSTABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src385" class="srcSentence">Identifier Case Sensitivity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src386" class="srcSentence">DBPROP_IDENTIFIERCASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src387" class="srcSentence">Initial Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src388" class="srcSentence">DBPROP_INIT_CATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src389" class="srcSentence">Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src390" class="srcSentence">DBPROP_SUPPORTEDTXNISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src391" class="srcSentence">Isolation Retention</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src392" class="srcSentence">DBPROP_SUPPORTEDTXNISORETAIN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src393" class="srcSentence">Locale Identifier</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src394" class="srcSentence">DBPROP_INIT_LCID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src395" class="srcSentence">Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src396" class="srcSentence">DBPROP_INIT_LOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src397" class="srcSentence">Maximum Index Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src398" class="srcSentence">DBPROP_MAXINDEXSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src399" class="srcSentence">Maximum Row Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src400" class="srcSentence">DBPROP_MAXROWSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src401" class="srcSentence">Maximum Row Size Includes BLOB</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src402" class="srcSentence">DBPROP_MAXROWSIZEINCLUDESBLOB</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src403" class="srcSentence">Maximum Tables in SELECT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src404" class="srcSentence">DBPROP_MAXTABLESINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src405" class="srcSentence">Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src406" class="srcSentence">DBPROP_INIT_MODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src407" class="srcSentence">Multiple Parameter Sets</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src408" class="srcSentence">DBPROP_MULTIPLEPARAMSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src409" class="srcSentence">Multiple Results</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src410" class="srcSentence">DBPROP_MULTIPLERESULTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src411" class="srcSentence">Multiple Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src412" class="srcSentence">DBPROP_MULTIPLESTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src413" class="srcSentence">Multi-Table Update</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src414" class="srcSentence">DBPROP_MULTITABLEUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src415" class="srcSentence">NULL Collation Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src416" class="srcSentence">DBPROP_NULLCOLLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src417" class="srcSentence">NULL Concatenation Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src418" class="srcSentence">DBPROP_CONCATNULLBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src419" class="srcSentence">OLE DB Services</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src420" class="srcSentence">DBPROP_INIT_OLEDBSERVICES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src421" class="srcSentence">OLE DB Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src422" class="srcSentence">DBPROP_PROVIDEROLEDBVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src423" class="srcSentence">OLE Object Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src424" class="srcSentence">DBPROP_OLEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src425" class="srcSentence">Open Rowset Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src426" class="srcSentence">DBPROP_OPENROWSETSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src427" class="srcSentence">ORDER BY Columns in Select List</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src428" class="srcSentence">DBPROP_ORDERBYCOLUMNSINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src429" class="srcSentence">Output Parameter Availability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src430" class="srcSentence">DBPROP_OUTPUTPARAMETERAVAILABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src431" class="srcSentence">Password</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src432" class="srcSentence">DBPROP_AUTH_PASSWORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src433" class="srcSentence">Pass By Ref Accessors</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src434" class="srcSentence">DBPROP_BYREFACCESSORS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src435" class="srcSentence">Persist Security Info</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src436" class="srcSentence">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src437" class="srcSentence">Persistent ID Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src438" class="srcSentence">DBPROP_PERSISTENTIDTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src439" class="srcSentence">Prepare Abort Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src440" class="srcSentence">DBPROP_PREPAREABORTBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src441" class="srcSentence">Prepare Commit Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src442" class="srcSentence">DBPROP_PREPARECOMMITBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src443" class="srcSentence">Procedure Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src444" class="srcSentence">DBPROP_PROCEDURETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src445" class="srcSentence">Prompt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src446" class="srcSentence">DBPROP_INIT_PROMPT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src447" class="srcSentence">Provider Friendly Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src448" class="srcSentence">DBPROP_PROVIDERFRIENDLYNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src449" class="srcSentence">Provider Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src450" class="srcSentence">DBPROP_PROVIDERFILENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src451" class="srcSentence">Provider Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src452" class="srcSentence">DBPROP_PROVIDERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src453" class="srcSentence">Read-Only Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src454" class="srcSentence">DBPROP_DATASOURCEREADONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src455" class="srcSentence">Rowset Conversions on Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src456" class="srcSentence">DBPROP_ROWSETCONVERSIONSONCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src457" class="srcSentence">Schema Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src458" class="srcSentence">DBPROP_SCHEMATERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src459" class="srcSentence">Schema Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src460" class="srcSentence">DBPROP_SCHEMAUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src461" class="srcSentence">SQL Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src462" class="srcSentence">DBPROP_SQLSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src463" class="srcSentence">Structured Storage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src464" class="srcSentence">DBPROP_STRUCTUREDSTORAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src465" class="srcSentence">Subquery Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src466" class="srcSentence">DBPROP_SUBQUERIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src467" class="srcSentence">Table Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src468" class="srcSentence">DBPROP_TABLETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src469" class="srcSentence">Transaction DDL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src470" class="srcSentence">DBPROP_SUPPORTEDTXNDDL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src471" class="srcSentence">User ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src472" class="srcSentence">DBPROP_AUTH_USERID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src473" class="srcSentence">User Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src474" class="srcSentence">DBPROP_USERNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src475" class="srcSentence">Window Handle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src476" class="srcSentence">DBPROP_INIT_HWND</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src477" class="srcSentence">Recordset Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src478" class="srcSentence">The following properties are added to the <legacyBold>Recordset</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src479" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src480" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src481" class="srcSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src482" class="srcSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src483" class="srcSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src484" class="srcSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src485" class="srcSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src486" class="srcSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src487" class="srcSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src488" class="srcSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src489" class="srcSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src490" class="srcSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src491" class="srcSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src492" class="srcSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src493" class="srcSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src494" class="srcSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src495" class="srcSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src496" class="srcSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src497" class="srcSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src498" class="srcSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src499" class="srcSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src500" class="srcSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src501" class="srcSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src502" class="srcSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src503" class="srcSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src504" class="srcSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src505" class="srcSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src506" class="srcSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src507" class="srcSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src508" class="srcSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src509" class="srcSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src510" class="srcSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src511" class="srcSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src512" class="srcSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src513" class="srcSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src514" class="srcSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src515" class="srcSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src516" class="srcSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src517" class="srcSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src518" class="srcSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src519" class="srcSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src520" class="srcSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src521" class="srcSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src522" class="srcSentence">DBPROP_IRowsetLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src523" class="srcSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src524" class="srcSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src525" class="srcSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src526" class="srcSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src527" class="srcSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src528" class="srcSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src529" class="srcSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src530" class="srcSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src531" class="srcSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src532" class="srcSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src533" class="srcSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src534" class="srcSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src535" class="srcSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src536" class="srcSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src537" class="srcSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src538" class="srcSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src539" class="srcSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src540" class="srcSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src541" class="srcSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src542" class="srcSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src543" class="srcSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src544" class="srcSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src545" class="srcSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src546" class="srcSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src547" class="srcSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src548" class="srcSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src549" class="srcSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src550" class="srcSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src551" class="srcSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src552" class="srcSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src553" class="srcSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src554" class="srcSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src555" class="srcSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src556" class="srcSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src557" class="srcSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src558" class="srcSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src559" class="srcSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src560" class="srcSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src561" class="srcSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src562" class="srcSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src563" class="srcSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src564" class="srcSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src565" class="srcSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src566" class="srcSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src567" class="srcSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src568" class="srcSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src569" class="srcSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src570" class="srcSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src571" class="srcSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src572" class="srcSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src573" class="srcSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src574" class="srcSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src575" class="srcSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src576" class="srcSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src577" class="srcSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src578" class="srcSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src579" class="srcSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src580" class="srcSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src581" class="srcSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src582" class="srcSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src583" class="srcSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src584" class="srcSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src585" class="srcSentence">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src586" class="srcSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src587" class="srcSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src588" class="srcSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src589" class="srcSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src590" class="srcSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src591" class="srcSentence">DBPROP_BOOKMARKSKIPPED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src592" class="srcSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src593" class="srcSentence">DBPROP_STRONGITDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src594" class="srcSentence">Unique Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src595" class="srcSentence">DBPROP_UNIQUEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src596" class="srcSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src597" class="srcSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src598" class="srcSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src599" class="srcSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src600" class="srcSentence">Command Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src601" class="srcSentence">The following properties are added to the <legacyBold>Command</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src602" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src603" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src604" class="srcSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src605" class="srcSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src606" class="srcSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src607" class="srcSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src608" class="srcSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src609" class="srcSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src610" class="srcSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src611" class="srcSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src612" class="srcSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src613" class="srcSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src614" class="srcSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src615" class="srcSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src616" class="srcSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src617" class="srcSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src618" class="srcSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src619" class="srcSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src620" class="srcSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src621" class="srcSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src622" class="srcSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src623" class="srcSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src624" class="srcSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src625" class="srcSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src626" class="srcSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src627" class="srcSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src628" class="srcSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src629" class="srcSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src630" class="srcSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src631" class="srcSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src632" class="srcSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src633" class="srcSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src634" class="srcSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src635" class="srcSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src636" class="srcSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src637" class="srcSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src638" class="srcSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src639" class="srcSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src640" class="srcSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src641" class="srcSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src642" class="srcSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src643" class="srcSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src644" class="srcSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src645" class="srcSentence">DBPROP_IRowsetLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src646" class="srcSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src647" class="srcSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src648" class="srcSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src649" class="srcSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src650" class="srcSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src651" class="srcSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src652" class="srcSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src653" class="srcSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src654" class="srcSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src655" class="srcSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src656" class="srcSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src657" class="srcSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src658" class="srcSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src659" class="srcSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src660" class="srcSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src661" class="srcSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src662" class="srcSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src663" class="srcSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src664" class="srcSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src665" class="srcSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src666" class="srcSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src667" class="srcSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src668" class="srcSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src669" class="srcSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src670" class="srcSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src671" class="srcSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src672" class="srcSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src673" class="srcSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src674" class="srcSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src675" class="srcSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src676" class="srcSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src677" class="srcSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src678" class="srcSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src679" class="srcSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src680" class="srcSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src681" class="srcSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src682" class="srcSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src683" class="srcSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src684" class="srcSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src685" class="srcSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src686" class="srcSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src687" class="srcSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src688" class="srcSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src689" class="srcSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src690" class="srcSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src691" class="srcSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src692" class="srcSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src693" class="srcSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src694" class="srcSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src695" class="srcSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src696" class="srcSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src697" class="srcSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src698" class="srcSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src699" class="srcSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src700" class="srcSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src701" class="srcSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src702" class="srcSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src703" class="srcSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src704" class="srcSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src705" class="srcSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src706" class="srcSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src707" class="srcSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src708" class="srcSentence">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src709" class="srcSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src710" class="srcSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src711" class="srcSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src712" class="srcSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src713" class="srcSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src714" class="srcSentence">DBPROP_BOOKMARKSKIP</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src715" class="srcSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src716" class="srcSentence">DBPROP_STRONGIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src717" class="srcSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src718" class="srcSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src719" class="srcSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src720" class="srcSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src721" class="srcSentence">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, see the <legacyLink xlink:href="3c5e2dd5-35e5-4a93-ac3a-3818bb43bbf8">OLE DB Programmer's Reference</legacyLink> or visit the Data Access and Storage Developer Center Web site on MSDN.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString Property</link>
        <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
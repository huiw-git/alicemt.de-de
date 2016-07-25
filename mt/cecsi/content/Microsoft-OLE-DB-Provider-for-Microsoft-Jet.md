---
title: "Microsoft OLE DB Provider for Microsoft Jet"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fd956da1-5203-40af-aa7e-fc13a6c6581f
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
# Microsoft OLE DB Provider for Microsoft Jet
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7303c08cc90537720db820e456c88202" id="tgt1" class="tgtSentence">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="df209e37fa6496886af7a164ca15b629" id="tgt2" class="tgtSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f785aefc737eabc5212c97ea5d915748" id="tgt3" class="tgtSentence">To connect to this provider, set the <legacyItalic>Provider</legacyItalic> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to the following:</caps:sentence>
          </para>
          <code>Microsoft.Jet.OLEDB.4.0</code>
          <para>
            <caps:sentence sentenceid="00a3db676c5b0b62adb741e71fae2e09" id="tgt4" class="tgtSentence">Reading the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property will also return this string.</caps:sentence>
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
          <code>"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=<legacyItalic xmlns="">databaseName</legacyItalic>;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
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
                    <caps:sentence sentenceid="f6e486531e9d59738c961e53d6f2cc1d" id="tgt11" class="tgtSentence">Specifies the OLE DB Provider for Microsoft Jet.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5f0262ef78817e828a92d75e9749b4f9" id="tgt12" class="tgtSentence">Data Source</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8a5fbd8b0f93758a1c3021cf4b7affb" id="tgt13" class="tgtSentence">Specifies the database path and file name (for example, <codeInline>c:\Northwind.mdb</codeInline>).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3bd756a1167a9bff574b512092d53350" id="tgt14" class="tgtSentence">User ID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="894ae1122beff71d90c743328e91d2dd" id="tgt15" class="tgtSentence">Specifies the user name.</caps:sentence>
                    <caps:sentence sentenceid="9e37aaf8653328ec673b452396eff111" id="tgt16" class="tgtSentence"> If this keyword is not specified, the string, "<codeInline>admin</codeInline>", is used by default.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5f4dcc3b5aa765d61d8327deb882cf99" id="tgt17" class="tgtSentence">Password</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4df08222df3dae489cac77da63d403c" id="tgt18" class="tgtSentence">Specifies the user password.</caps:sentence>
                    <caps:sentence sentenceid="7cd483681425d037c82de76aeea09bdf" id="tgt19" class="tgtSentence"> If this keyword is not specified, the empty string (""), is used by default.</caps:sentence>
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
            <caps:sentence sentenceid="cf087b04e6589b0fb9d64f848c87b848" id="tgt22" class="tgtSentence">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those that are defined by ADO.</caps:sentence>
            <caps:sentence sentenceid="25711c3d3a4022c15ca4ba2d8c7c2ba8" id="tgt23" class="tgtSentence"> As with all other <legacyBold>Connection</legacyBold> parameters, they can be set by using the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Connection</legacyBold> object or as part of the connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5d975fe5948b643dfa4bd288abb4943f" id="tgt24" class="tgtSentence">The following table lists these properties together with the corresponding OLE DB property name in parentheses.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt25" class="tgtSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt26" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b0fa2596ebac600f0cc59a9b45ac37a" id="tgt27" class="tgtSentence">Jet OLEDB:Compact Reclaimed Space Amount (DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42300905d77ab1e234dbdcbb269064a7" id="tgt28" class="tgtSentence">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database.</caps:sentence>
                    <caps:sentence sentenceid="8e79157a656d8862dfcd00e75f2c69af" id="tgt29" class="tgtSentence"> This value is only valid after a database connection has been established.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ac777a542864b1e5ffd85dd9d6fd5ec" id="tgt30" class="tgtSentence">Jet OLEDB:Connection Control (DBPROP_JETOLEDB_CONNECTIONCONTROL)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ecb73b11691d00b216f9021696fa88d" id="tgt31" class="tgtSentence">Indicates whether users can connect to the database.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78a55a1da3577431d63e0036424cfa51" id="tgt32" class="tgtSentence">Jet OLEDB:Create System Database (DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fb398514786fafd83bbf1c0d7e16ccce" id="tgt33" class="tgtSentence">Indicates whether a system database should be created when creating a new data source.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="50ebf15b48bf3a1e5e3564fb39f8cbc4" id="tgt34" class="tgtSentence">Jet OLEDB:Database Locking Mode (DBPROP_JETOLEDB_DATABASELOCKMODE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="453c7909715498d3bbb62e030eed7e59" id="tgt35" class="tgtSentence">Indicates the locking mode for this database.</caps:sentence>
                    <caps:sentence sentenceid="5a627b8992c3230f1464dacb2acd3f3b" id="tgt36" class="tgtSentence"> The first user to open the database determines the mode used while the database is open.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bbbeea98468b9f9723953f99d954ecb2" id="tgt37" class="tgtSentence">Jet OLEDB:Database Password (DBPROP_JETOLEDB_DATABASEPASSWORD)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f154610d19e3a5108752479b97ca488d" id="tgt38" class="tgtSentence">Indicates the database password.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f340d9a6d75c87af5aa4f6814e874657" id="tgt39" class="tgtSentence">Jet OLEDB:Don't Copy Locale on Compact (DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c34ed0580670461f0d89a61d43825c96" id="tgt40" class="tgtSentence">Indicates whether Jet should copy locale information when compacting a database.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7677b9b01acb9b44cae79c87e458046f" id="tgt41" class="tgtSentence">Jet OLEDB:Encrypt Database (DBPROP_JETOLEDB_ENCRYPTDATABASE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7378fbfb718156533863de36a5f46926" id="tgt42" class="tgtSentence">Indicates whether a compacted database should be encrypted.</caps:sentence>
                    <caps:sentence sentenceid="836b030c6ec669b4c0e0652f898485f7" id="tgt43" class="tgtSentence"> If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eacc01a17e255c4485fd3597b9dc5f92" id="tgt44" class="tgtSentence">Jet OLEDB:Engine Type (DBPROP_JETOLEDB_ENGINE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4349d148d75c0b1beb929292b65ec61e" id="tgt45" class="tgtSentence">Indicates the storage engine used to access the current data store.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="93a16e52c7525a9a5e951b9b349f0281" id="tgt46" class="tgtSentence">Jet OLEDB:Exclusive Async Delay (DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="585129cd3f248def48f6a9990fb8293c" id="tgt47" class="tgtSentence">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f1d6f0be916f2b6136c2839f5fdc919a" id="tgt48" class="tgtSentence">This property is ignored unless <legacyBold>Jet OLEDB:Flush Transaction Timeout</legacyBold> is set to 0.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9c184b0398322ae23c865fbc0664d68e" id="tgt49" class="tgtSentence">Jet OLEDB:Flush Transaction Timeout (DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cd80702e51e4c33139a6541736df0c95" id="tgt50" class="tgtSentence">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk.</caps:sentence>
                    <caps:sentence sentenceid="925afe25ddf209dd2623f2f65f19f75a" id="tgt51" class="tgtSentence"> This setting overrides the values for <legacyBold>Jet OLEDB:Shared Async Delay</legacyBold> and <legacyBold>Jet OLEDB:Exclusive Async Delay</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="85abc3c490cd78450f8e34590ce5b01e" id="tgt52" class="tgtSentence">Jet OLEDB:Global Bulk Transactions (DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2f16ced308c86e33505cfb4bec100d4b" id="tgt53" class="tgtSentence">Indicates whether SQL bulk transactions are transacted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3dc41a4a87b9e4c6bf1a307cddd7d132" id="tgt54" class="tgtSentence">Jet OLEDB:Global Partial Bulk Ops (DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb3a92ffa03d283365af2a49cd1800a5" id="tgt55" class="tgtSentence">Indicates the password used to open the database.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7bdc5bf2c95467fdf097685d1e1c8a18" id="tgt56" class="tgtSentence">Jet OLEDB:Implicit Commit Sync (DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ec7da6ab49e08aacf4289f3c16ec722" id="tgt57" class="tgtSentence">Indicates whether changes that were made in internal implicit transactions are written in synchronous or asynchronous mode.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44e51cd4ba61cb94be5dd37f51d2850f" id="tgt58" class="tgtSentence">Jet OLEDB:Lock Delay (DBPROP_JETOLEDB_LOCKDELAY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fb28ce92d50bba601829b60105c57725" id="tgt59" class="tgtSentence">Indicates the number of milliseconds to wait before trying to acquire a lock after a previous attempt has failed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ce27224cfa810c4b05c5653a52e048" id="tgt60" class="tgtSentence">Jet OLEDB:Lock Retry (DBPROP_JETOLEDB_LOCKRETRY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bc4c0fd1242ad5776ba92ec359c2ccd6" id="tgt61" class="tgtSentence">Indicates how many times an attempt to access a locked page is repeated.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b3598dbd1002dbc5b6dd33278068bbcb" id="tgt62" class="tgtSentence">Jet OLEDB:Max Buffer Size (DBPROP_JETOLEDB_MAXBUFFERSIZE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1e555cf6996434bc2ea8023cfe228954" id="tgt63" class="tgtSentence">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0560f869e1a9737dc1c91eb23f9618b4" id="tgt64" class="tgtSentence">Jet OLEDB:Max Locks Per File (DBPROP_JETOLEDB_MAXLOCKSPERFILE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b94e37e6a2681efae52d135dc640e265" id="tgt65" class="tgtSentence">Indicates the maximum number of locks Jet can place on a database.</caps:sentence>
                    <caps:sentence sentenceid="6321d6400e45ace1a7855eb4f4281b76" id="tgt66" class="tgtSentence"> The default value is 9500.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b5317da139660f3399f1e19dc1d47da2" id="tgt67" class="tgtSentence">Jet OLEDB:New Database Password (DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c0d1ad1fa6686beda6a87b0c1b853d2" id="tgt68" class="tgtSentence">Indicates the new password to be set for this database.</caps:sentence>
                    <caps:sentence sentenceid="af2cb6e01916a53e54bc578bd9f90ee5" id="tgt69" class="tgtSentence"> The old password is stored in <legacyBold>Jet OLEDB:Database Password</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fd83b0b1e8c55b7d56744da799296477" id="tgt70" class="tgtSentence">Jet OLEDB:ODBC Command Time Out (DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34609572f84612f7b4ac16c13c53e09e" id="tgt71" class="tgtSentence">Indicates the number of milliseconds before a remote ODBC query from Jet will time out.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="43bf7d7a35b6f50278d96eeebc5d8f46" id="tgt72" class="tgtSentence">Jet OLEDB:Page Locks to Table Lock (DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="51f78efdf49c38ffc9a34c6319c4a53f" id="tgt73" class="tgtSentence">Indicates how many pages must be locked within a transaction before Jet tries to promote the lock to a table lock.</caps:sentence>
                    <caps:sentence sentenceid="ef5d082044b475e08928d0ac3693f0fc" id="tgt74" class="tgtSentence"> If this value is 0, the lock is never promoted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bb3b50f16c72b4923eb4a5257a2ed56b" id="tgt75" class="tgtSentence">Jet OLEDB:Page Timeout (DBPROP_JETOLEDB_PAGETIMEOUT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d32454aedab7a9457e0127df501af36c" id="tgt76" class="tgtSentence">Indicates the number of milliseconds Jet will wait before checking to see whether its cache is out of date with the database file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b4d180b4a5801bf63d9c8e951117eb58" id="tgt77" class="tgtSentence">Jet OLEDB:Recycle Long-Valued Pages (DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fa85c71819646f34643295e353012f07" id="tgt78" class="tgtSentence">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fb7295c52513e2b8c2769612c32a257" id="tgt79" class="tgtSentence">Jet OLEDB:Registry Path (DBPROP_JETOLEDB_REGPATH)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="109d238f309df103f8f4855ff23968d3" id="tgt80" class="tgtSentence">Indicates the Windows registry key that contains values for the Jet database engine.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e95d9faa1812fdba58404ba0f179117a" id="tgt81" class="tgtSentence">Jet OLEDB:Reset ISAM Stats (DBPROP_JETOLEDB_RESETISAMSTATS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b905eca52e128621097ccdda5b9a44bf" id="tgt82" class="tgtSentence">Indicates whether the schema <legacyBold>Recordset</legacyBold> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after it returns performance information.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5937266f2c10a4ccafed43f44ea424d8" id="tgt83" class="tgtSentence">Jet OLEDB:Shared Async Delay (DBPROP_JETOLEDB_SHAREDASYNCDELAY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3a403079ae72f610034f3f46c1ed63e3" id="tgt84" class="tgtSentence">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multiuser mode.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6432ebe7cbda1f666230b1777308e271" id="tgt85" class="tgtSentence">Jet OLEDB:System Database (DBPROP_JETOLEDB_SYSDBPATH)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="07c8d3fbb6309f8339165fd70f589237" id="tgt86" class="tgtSentence">Indicates the path and file name for the workgroup information file (system database).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e070b91c21e71180a8620cb252b504f2" id="tgt87" class="tgtSentence">Jet OLEDB:Transaction Commit Mode (DBPROP_JETOLEDB_TXNCOMMITMODE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c0ba1522f17a3fe126d50118110e4d81" id="tgt88" class="tgtSentence">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9d3f0cfe0dd57314e2e58197cbfdf71c" id="tgt89" class="tgtSentence">Jet OLEDB:User Commit Sync (DBPROP_JETOLEDB_USERCOMMITSYNC)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="66db43a0dce268503d7e6ccba1d1713c" id="tgt90" class="tgtSentence">Indicates whether changes that were made in transactions are written in synchronous or asynchronous mode.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1494887de9c2cae6bece501c37b08e00" id="tgt91" class="tgtSentence">Provider-Specific Recordset and Command Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="edb183f7f79f2a5122e4b750eb782930" id="tgt92" class="tgtSentence">The Jet provider also supports several provider-specific <legacyBold>Recordset</legacyBold> and <legacyBold>Command</legacyBold> properties.</caps:sentence>
            <caps:sentence sentenceid="9e7bc93910646df35eef85985957d79d" id="tgt93" class="tgtSentence"> These properties are accessed and set through the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> or <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="6750373ddacd30ea46844010045557e1" id="tgt94" class="tgtSentence"> The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a3d69a40cc5ec31232a11100ae6c951" id="tgt95" class="tgtSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt96" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f330156417c31c761253193d30465e86" id="tgt97" class="tgtSentence">Jet OLEDB:Bulk Transactions (DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8fea410518751952734bdd36cab9b40d" id="tgt98" class="tgtSentence">Indicates whether SQL bulk operations are transacted.</caps:sentence>
                    <caps:sentence sentenceid="3f0f92a3a0099d50f68cb2d3565c59fb" id="tgt99" class="tgtSentence"> Large bulk operations might fail when transacted, because of resource delays.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="321cf743dc3361665c89ce62b68de3fb" id="tgt100" class="tgtSentence">Jet OLEDB:Enable Fat Cursors (DBPROP_JETOLEDB_ENABLEFATCURSOR)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="185c1fa4ccd3e5c5527af3ded9e3840d" id="tgt101" class="tgtSentence">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e09dba875a929e5d4ec34cf3e53fa74b" id="tgt102" class="tgtSentence">Jet OLEDB:Fat Cursor Cache Size (DBPROP_JETOLEDB_FATCURSORMAXROWS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cf441d8d7d6db1a145322852e0e66666" id="tgt103" class="tgtSentence">Indicates the number of rows to cache when using remote data store row caching.</caps:sentence>
                    <caps:sentence sentenceid="12b5fc001c35990cd1dfb88b32611ce0" id="tgt104" class="tgtSentence"> This value is ignored unless <legacyBold>Jet OLEDB:Enable Fat Cursors</legacyBold> is True.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="70bc3d9b470f111ddc7fe1a87967d0e3" id="tgt105" class="tgtSentence">Jet OLEDB:Inconsistent (DBPROP_JETOLEDB_INCONSISTENT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94531eb0fa4b091ffae3bbacdff32ff7" id="tgt106" class="tgtSentence">Indicates whether query results allow inconsistent updates.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6bea48be203197d87c449a011c036df1" id="tgt107" class="tgtSentence">Jet OLEDB:Locking Granularity (DBPROP_JETOLEDB_LOCKGRANULARITY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a2f379ccbfcc86000eb578009996f8da" id="tgt108" class="tgtSentence">Indicates whether a table is opened using row-level locking.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="521cbed0b2e2707b634ff70f4150cb0e" id="tgt109" class="tgtSentence">Jet OLEDB:ODBC Pass-Through Statement (DBPROP_JETOLEDB_ODBCPASSTHROUGH)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="733c4602ab141736c588274aba3af42a" id="tgt110" class="tgtSentence">Indicates that Jet should pass the SQL text in a <legacyBold>Command</legacyBold> object to the back end unaltered.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12c28f228d2713e156a50025822780e3" id="tgt111" class="tgtSentence">Jet OLEDB:Partial Bulk Ops (DBPROP_JETOLEDB_BULKPARTIAL)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6b3e91a5a917ac6eaa24c50a4e58df6" id="tgt112" class="tgtSentence">Indicates Jet's behavior when SQL DML operations fail.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="71b206a82cd4b7224d2cd0fdd97144f6" id="tgt113" class="tgtSentence">Jet OLEDB:Pass Through Query Bulk-Op (DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="38bc69ee58827da01d5bfeadd65ed28e" id="tgt114" class="tgtSentence">Indicates whether queries that do not return a <legacyBold>Recordset</legacyBold> are passed unaltered to the data source.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="de2b8be64fa20fa5f504fa0b9f8c1561" id="tgt115" class="tgtSentence">Jet OLEDB:Pass Through Query Connect String (DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49bbb9be5f48238a352c8df6926a7ef8" id="tgt116" class="tgtSentence">Indicates the Jet connect string used to connect to a remote data store.</caps:sentence>
                    <caps:sentence sentenceid="f5e41bb928cd1eebb509e51aa9e32255" id="tgt117" class="tgtSentence"> This value is ignored unless <legacyBold>Jet OLEDB:ODBC Pass-Through Statement</legacyBold> is True.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="28a5f704446cb57e7395277595eac456" id="tgt118" class="tgtSentence">Jet OLEDB:Stored Query (DBPROP_JETOLEDB_STOREDQUERY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="69823023c5039ccaca225b339200335c" id="tgt119" class="tgtSentence">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bb796333dc88c5bff9113cbf18ba4140" id="tgt120" class="tgtSentence">Jet OLEDB:Validate Rules On Set (DBPROP_JETOLEDB_VALIDATEONSET)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="29a7568408d2fb550da88db01c4a6e14" id="tgt121" class="tgtSentence">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="5fb0ac0a4c2398c41a21cec6c2b761df" id="tgt122" class="tgtSentence">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode.</caps:sentence>
            <caps:sentence sentenceid="5919722ddf4b9ab34735802e95b006b4" id="tgt123" class="tgtSentence"> To open a database in read-only mode, set the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property on the ADO <legacyBold>Connection</legacyBold> object to <legacyBold>adModeRead</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="e0f00fb1715bd624b7380c4fbaf0e694" id="tgt124" class="tgtSentence">Command Object Usage</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bf4a9a9dda550f4f9d739f5c3da48632" id="tgt125" class="tgtSentence">Command text in the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object uses the Microsoft Jet SQL dialect.</caps:sentence>
            <caps:sentence sentenceid="002275bc349c772f7d922fdb9ee41733" id="tgt126" class="tgtSentence"> You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="002c1a21d972a03f6b6e5a266dd56653" id="tgt127" class="tgtSentence">Recordset Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8b6c4ec1f1657dab5e6eb4754cb4b94b" id="tgt128" class="tgtSentence">The Microsoft Jet database engine does not support dynamic cursors.</caps:sentence>
            <caps:sentence sentenceid="a35c7dc90f67660168713d5ed8ae7959" id="tgt129" class="tgtSentence"> Therefore, the OLE DB Provider for Microsoft Jet does not support the <legacyBold>adLockDynamic</legacyBold> cursor type.</caps:sentence>
            <caps:sentence sentenceid="509a0e83882a8fe86c281e653055eb56" id="tgt130" class="tgtSentence"> When a dynamic cursor is requested, the provider will return a keyset cursor and reset the <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink> property to indicate the type of <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> returned.</caps:sentence>
            <caps:sentence sentenceid="e896a76c6e082602afa762730a92af00" id="tgt131" class="tgtSentence"> Further, if an updatable <legacyBold>Recordset</legacyBold> is requested (<legacyBold>LockType</legacyBold> is <legacyBold>adLockOptimistic</legacyBold>, <legacyBold>adLockBatchOptimistic</legacyBold>, or <legacyBold>adLockPessimistic</legacyBold>) the provider will also return a keyset cursor and reset the <legacyBold>CursorType</legacyBold> property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c9cc4b2425ec47fd6141efc88965a1d3" id="tgt132" class="tgtSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="58614adf8173d10346fea739a693c2b8" id="tgt133" class="tgtSentence">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the <legacyBold>Properties</legacyBold> collection of the unopened <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c4d70f669b7e7098098781d22c2f0183" id="tgt134" class="tgtSentence">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</caps:sentence>
            <caps:sentence sentenceid="c8f596e13cecff8eedb595433f1d524a" id="tgt135" class="tgtSentence"> The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</caps:sentence>
            <caps:sentence sentenceid="5bd6c2a248f991e5772ecf53ac580449" id="tgt136" class="tgtSentence"> You can find more information about these properties in the OLE DB Programmer's Reference.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="cc03d661ba78db29ad696232fbdfd45d" id="tgt137" class="tgtSentence">Connection Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="66ad75c6de7e35fcc78d16fd0db075f8" id="tgt138" class="tgtSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt139" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt140" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="42da7b3adedde15ba58b5e8f720f0729" id="tgt141" class="tgtSentence">Active Sessions</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5db97e3405ada5593894afe7c26e912a" id="tgt142" class="tgtSentence">DBPROP_ACTIVESESSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5fb6f6fbeeed9d35163820f4cad357a5" id="tgt143" class="tgtSentence">Asynchable Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a69ebf5e5b867b80a10c033ec247f235" id="tgt144" class="tgtSentence">DBPROP_ASYNCTXNABORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1553c09566f739d416c34417c3eed8bc" id="tgt145" class="tgtSentence">Asynchable Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8fb4c7f494cd85116f18f4e23dfa3ce2" id="tgt146" class="tgtSentence">DBPROP_ASYNCTNXCOMMIT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ac1b75d9d496be787670b775f6cbc81" id="tgt147" class="tgtSentence">Autocommit Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ed9f459c36be0b771e14849bddd615a" id="tgt148" class="tgtSentence">DBPROP_SESS_AUTOCOMMITISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04e7adcf92320728ff99be4ae9e20b80" id="tgt149" class="tgtSentence">Catalog Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cc7d88f9c70b084ff349547378be6ea7" id="tgt150" class="tgtSentence">DBPROP_CATALOGLOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0d5a9974623ad1d08ec1a87d28e3382b" id="tgt151" class="tgtSentence">Catalog Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5ec52858196e5661e26c0593dc0055f3" id="tgt152" class="tgtSentence">DBPROP_CATALOGTERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ccf0f62c35ce6f4ad47c504191cbc48" id="tgt153" class="tgtSentence">Column Definition</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4036e684cbb10c6c00160fb3f89fec78" id="tgt154" class="tgtSentence">DBPROP_COLUMNDEFINITION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6cf2a5823099e39d4bfcd079068b384d" id="tgt155" class="tgtSentence">Current Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1975407cf7846b03983297436f6feaec" id="tgt156" class="tgtSentence">DBPROP_CURRENTCATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f0262ef78817e828a92d75e9749b4f9" id="tgt157" class="tgtSentence">Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f628f4ca9169da470c6349e4dadfd7b" id="tgt158" class="tgtSentence">DBPROP_INIT_DATASOURCE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4cc4008aeaa109c055aa7289fe8955f6" id="tgt159" class="tgtSentence">Data Source Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f70e2b308e36cc86cb62a25d0cc89d0" id="tgt160" class="tgtSentence">DBPROP_DATASOURCENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0902cf5b7d19a0cc4c0d745125932c99" id="tgt161" class="tgtSentence">Data Source Object Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6168b0502be04b450b621cc21978b79" id="tgt162" class="tgtSentence">DBPROP_DSOTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="44576fc26ad5240af73f0f7304ac0161" id="tgt163" class="tgtSentence">DBMS Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8bfb66db9f6b9a9d8249efb32f35bc2" id="tgt164" class="tgtSentence">DBPROP_DBMSNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0865166992725c390cf3955eb7005314" id="tgt165" class="tgtSentence">DBMS Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="91a28922f266288ed023d4fb5e1a9f41" id="tgt166" class="tgtSentence">DBPROP_DBMSVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fc489b2e87836669c99f48d36447d508" id="tgt167" class="tgtSentence">GROUP BY Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b73b41cab609c063b7570db22674bb0" id="tgt168" class="tgtSentence">DBPROP_GROUPBY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7970e9c2391aaf6904a12c0b64590ee7" id="tgt169" class="tgtSentence">Heterogeneous Table Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8732f1c0c3c20adc7bc8f5f878f4e95f" id="tgt170" class="tgtSentence">DBPROP_HETEROGENEOUSTABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3cc7d428494725fbc1c4117841759a1b" id="tgt171" class="tgtSentence">Identifier Case Sensitivity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f959d99f6f9ff2380e84ed5f89a6545" id="tgt172" class="tgtSentence">DBPROP_IDENTIFIERCASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6d922da801c791516e0fde80744ddda1" id="tgt173" class="tgtSentence">Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b826970c6bc792cec29c7154b97b055f" id="tgt174" class="tgtSentence">DBPROP_SUPPORTEDTXNISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="36d2944c902a8b3bfc937a35534e6d67" id="tgt175" class="tgtSentence">Isolation Retention</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1180eb611191e300302c020a0433017a" id="tgt176" class="tgtSentence">DBPROP_SUPPORTEDTXNISORETAIN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2d42b4f73ee8bf025a3c06cfa5499f55" id="tgt177" class="tgtSentence">Locale Identifier</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a119da28f65a0343b705f027db4eb589" id="tgt178" class="tgtSentence">DBPROP_INIT_LCID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d632dbafbc50f25c220bda2bd1d5eb79" id="tgt179" class="tgtSentence">Maximum Index Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0a5f4509b189658a32142048499fb311" id="tgt180" class="tgtSentence">DBPROP_MAXINDEXSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a3cbd82a49b4e695c986f9e21e08bec0" id="tgt181" class="tgtSentence">Maximum Row Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6414b671b9497a028ae03e2ff2baa8a2" id="tgt182" class="tgtSentence">DBPROP_MAXROWSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3fe8d182c92e2a2da388835b24f6a538" id="tgt183" class="tgtSentence">Maximum Row Size Includes BLOB</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82a79937366130603485b2e8243110f3" id="tgt184" class="tgtSentence">DBPROP_MAXROWSIZEINCLUDESBLOB</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="72fa89be4e41d4eec9682e3012510c70" id="tgt185" class="tgtSentence">Maximum Tables in SELECT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12775fa00655f15737d2b126875edf54" id="tgt186" class="tgtSentence">DBPROP_MAXTABLESINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="15d61712450a686a7f365adf4fef581f" id="tgt187" class="tgtSentence">Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e24a70a829cb0fe614e775e6b781aeef" id="tgt188" class="tgtSentence">DBPROP_INIT_MODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5fa88b3a7f2866a505f6869084d9dbac" id="tgt189" class="tgtSentence">Multiple Parameter Sets</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5b07a57182c870a463947bbe8862f2a" id="tgt190" class="tgtSentence">DBPROP_MULTIPLEPARAMSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34467f0701793e142a97280886a37d11" id="tgt191" class="tgtSentence">Multiple Results</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c6d16a5ed96ee324aaea5d56f93b9ca" id="tgt192" class="tgtSentence">DBPROP_MULTIPLERESULTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94a2500d5a620b62d088ba5e147f9300" id="tgt193" class="tgtSentence">Multiple Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4d0892bbf21bca8cbb05c7688e4481a" id="tgt194" class="tgtSentence">DBPROP_MULTIPLESTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49a7ede339dd477496917e520e53b211" id="tgt195" class="tgtSentence">Multi-Table Update</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45718feaf0858fc05c6e2c5653af9fa5" id="tgt196" class="tgtSentence">DBPROP_MULTITABLEUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="068577c6d2defffb1af7047830fb7e89" id="tgt197" class="tgtSentence">NULL Collation Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="169e04896d93bdec8bd59547b5636cf4" id="tgt198" class="tgtSentence">DBPROP_NULLCOLLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="51a10c8ee8acbdda689781c851e4dbfb" id="tgt199" class="tgtSentence">NULL Concatenation Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="86d53a1e665c382405ca707e70950ee9" id="tgt200" class="tgtSentence">DBPROP_CONCATNULLBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="54d02916d0ddd080374282c66901c59c" id="tgt201" class="tgtSentence">OLE DB Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8678185cda69da06b0b18cdede8c9aaf" id="tgt202" class="tgtSentence">DBPROP_PROVIDEROLEDBVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c77b810e588a10689239bf12710a9027" id="tgt203" class="tgtSentence">OLE Object Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9aa0a480916fc5befab6d11935037f12" id="tgt204" class="tgtSentence">DBPROP_OLEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="305717e26f640fcebb5c11bdf62692b0" id="tgt205" class="tgtSentence">Open Rowset Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="467a15dbf1a07da68a090197a6350d8e" id="tgt206" class="tgtSentence">DBPROP_OPENROWSETSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d8d10a19d6045a2990194103e79da9e6" id="tgt207" class="tgtSentence">ORDER BY Columns in Select List</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17519abd080309120a91fbe406545057" id="tgt208" class="tgtSentence">DBPROP_ORDERBYCOLUMNSINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6c8bdd56df539c7147de1a6309ccf033" id="tgt209" class="tgtSentence">Output Parameter Availability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b3bb7f1b82d23d1accfa030b4372da90" id="tgt210" class="tgtSentence">DBPROP_OUTPUTPARAMETERAVAILABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ec1f372d153601374fe2b3be37c84a7" id="tgt211" class="tgtSentence">Pass By Ref Accessors</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b063a15f21255c314931eb858f8c898" id="tgt212" class="tgtSentence">DBPROP_BYREFACCESSORS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f4dcc3b5aa765d61d8327deb882cf99" id="tgt213" class="tgtSentence">Password</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a4dad287f50102726dc53803031a610a" id="tgt214" class="tgtSentence">DBPROP_AUTH_PASSWORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d99d60bd887e031a71ff6eff10d6d3d4" id="tgt215" class="tgtSentence">Persistent ID Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ea254ecd2f23ef9f83d15db428137a57" id="tgt216" class="tgtSentence">DBPROP_PERSISTENTIDTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="77b5b43a8424c46e81df1ab0fc6e466d" id="tgt217" class="tgtSentence">Prepare Abort Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c461cd8da2a2986434667ac22d8c4113" id="tgt218" class="tgtSentence">DBPROP_PREPAREABORTBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dc732b57d8b179ab01d66f1adcddf935" id="tgt219" class="tgtSentence">Prepare Commit Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e5956c34c7c59de311a271e3cc843ced" id="tgt220" class="tgtSentence">DBPROP_PREPARECOMMITBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b307899aa47ab53211ca988c38acf75e" id="tgt221" class="tgtSentence">Procedure Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39fca27d3fe2656d61424456d445849b" id="tgt222" class="tgtSentence">DBPROP_PROCEDURETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4ae35dbb42614d2429b7d6d181a950bb" id="tgt223" class="tgtSentence">Prompt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a23c8807135a34f56166fc290ce391c" id="tgt224" class="tgtSentence">DBPROP_INIT_PROMPT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ebbb5df827311326b2ebdcd6cf839f95" id="tgt225" class="tgtSentence">Provider Friendly Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="590bff2f7b8796e1277a936f16a2a7ff" id="tgt226" class="tgtSentence">DBPROP_PROVIDERFRIENDLYNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe158741a51803d31ec342eea567a79" id="tgt227" class="tgtSentence">Provider Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af443c478802f07802f2dc40b36c12b0" id="tgt228" class="tgtSentence">DBPROP_PROVIDERFILENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6ee1f505ae87ddc1ca51166091edec7" id="tgt229" class="tgtSentence">Provider Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d547dd6794dc65d1cbc34bc9a3646cab" id="tgt230" class="tgtSentence">DBPROP_PROVIDERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="14bb11993e3371d739eebc9648db4ec8" id="tgt231" class="tgtSentence">Read-Only Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fbaa45e63afd58892cad4204394e4b4a" id="tgt232" class="tgtSentence">DBPROP_DATASOURCEREADONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b68e1280ee9c56976f9918f1b143ae9b" id="tgt233" class="tgtSentence">Rowset Conversions on Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e9ea492c28f4f9e0ebe6ab7b04499f0a" id="tgt234" class="tgtSentence">DBPROP_ROWSETCONVERSIONSONCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4e214d42f27db2df22d820f4339ab38" id="tgt235" class="tgtSentence">Schema Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="177617f0fc571a0b532c7358fec97041" id="tgt236" class="tgtSentence">DBPROP_SCHEMATERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="996b43fdeae58150436e00ab086e55f9" id="tgt237" class="tgtSentence">Schema Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af6ca7abc5e28a6ba9bc5998e88fc4de" id="tgt238" class="tgtSentence">DBPROP_SCHEMAUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3887b124c8b8b2ac1076ac2fbc50a5a8" id="tgt239" class="tgtSentence">SQL Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67a078a8eabce39c390405b03eaf82df" id="tgt240" class="tgtSentence">DBPROP_SQLSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82b1c99e1276c7b9329843b82cb249a2" id="tgt241" class="tgtSentence">Structured Storage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a912ffa112b5c65343d1368268679294" id="tgt242" class="tgtSentence">DBPROP_STRUCTUREDSTORAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a51c825ecd8a692b685d0736d13a30c8" id="tgt243" class="tgtSentence">Subquery Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2dc44fc06f6f61c8b1e7f8c8b1dc7226" id="tgt244" class="tgtSentence">DBPROP_SUBQUERIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1fa0c9780d8a58f26e201af8cdc9d7d5" id="tgt245" class="tgtSentence">Table Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c25b152bb6a5d33613780d82b09f83f" id="tgt246" class="tgtSentence">DBPROP_TABLETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26e3db30e914b1bf231f1dc48149a6ab" id="tgt247" class="tgtSentence">Transaction DDL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d94fb60768ed9e61630670c5b707db5e" id="tgt248" class="tgtSentence">DBPROP_SUPPORTEDTXNDDL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3bd756a1167a9bff574b512092d53350" id="tgt249" class="tgtSentence">User ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1d9c5665b97893aac40b03266365060d" id="tgt250" class="tgtSentence">DBPROP_AUTH_USERID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f28564ce8593a50b9cf507aecccd8cd6" id="tgt251" class="tgtSentence">User Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0673f982c2e13e63312a0a61aed98966" id="tgt252" class="tgtSentence">DBPROP_USERNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98487bfe9fe529e4a2738b2ad9eacaec" id="tgt253" class="tgtSentence">Window Handle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3a92acd985b6ab8b1df6d3cd4df47e83" id="tgt254" class="tgtSentence">DBPROP_INIT_HWND</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0d8dea92a1ae91e40f5bc79d56f722e5" id="tgt255" class="tgtSentence">Recordset Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b6adcadd64667e5ca7f3654365be92fe" id="tgt256" class="tgtSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt257" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt258" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1594fad277e4590ddbbf46e340c4d10c" id="tgt259" class="tgtSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3ae70d0cfd08d73c0e8657de04e3ba3" id="tgt260" class="tgtSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7bc03dfea4165f8cc7279ecbcee1f41e" id="tgt261" class="tgtSentence">Append-Only Rowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="323934bf263c92d3fce05577ebb64799" id="tgt262" class="tgtSentence">DBPROP_APPENDONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b52683364c551ef6f2a83a9b61aca26" id="tgt263" class="tgtSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7eade57591bcbdf71a01307c5fa55333" id="tgt264" class="tgtSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39674232a2f3f57e87b6f56e9fcd620c" id="tgt265" class="tgtSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c5692554e1273a4cc28709961881f78" id="tgt266" class="tgtSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab13a6b41c0fedc395cff5ae82b531b6" id="tgt267" class="tgtSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt268" class="tgtSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="422691e4a2607d6fbf9785c231c0ea8a" id="tgt269" class="tgtSentence">Bookmarks Ordered</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa7751ca5633df65e31f1c633c547600" id="tgt270" class="tgtSentence">DBPROP_ORDEREDBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="187e822fb45791582a5f5e12e783c1c0" id="tgt271" class="tgtSentence">Cache Deferred Columns</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8683aa6604e702bc21392138b519177" id="tgt272" class="tgtSentence">DBPROP_CACHEDEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="246a7d96dd79b612bad343d03ea2bec6" id="tgt273" class="tgtSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75cbb9fc61a14afcadf102cfdd0a6733" id="tgt274" class="tgtSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="534d9e8ffeeeff5bf0f381032bbefd20" id="tgt275" class="tgtSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3eac3ca56c13d98b9d1f1d8ef5620027" id="tgt276" class="tgtSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30f3aa8c0ff671730367a69d810898b9" id="tgt277" class="tgtSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32873d7085b6feb780bf00ea59c3a386" id="tgt278" class="tgtSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ece0c04224a4c71df58445121e0aa118" id="tgt279" class="tgtSentence">Column Writable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fe0ab4d24b04b7f23827a14cb6c9ea2" id="tgt280" class="tgtSentence">DBPROP_MAYWRITECOLUMN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec83d16d5fb11f0a7e532fe6a91dfc36" id="tgt281" class="tgtSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af283d090de02b75e79bf25ce7aa945a" id="tgt282" class="tgtSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c34dec6888b6b898acb79b0597922c27" id="tgt283" class="tgtSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7906ea7eac0a5466ea33c9bf87d083db" id="tgt284" class="tgtSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c24d8cc4559e441d51781708292d746" id="tgt285" class="tgtSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b5c3be77a4c5f0654fd6637b3fd2b44" id="tgt286" class="tgtSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f518893e9bb8f74c9382260d0f79450b" id="tgt287" class="tgtSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2bdf72f0b7184d9ebe2e4086c598ee58" id="tgt288" class="tgtSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d33d5718660dbb261dc40b878ec4b591" id="tgt289" class="tgtSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fcb4539a8be17b29a97aada5fa31577" id="tgt290" class="tgtSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="28dbf41d74f2a648a563b28d2ecef878" id="tgt291" class="tgtSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba30e9909e02f6f6179f9db5cb9852cf" id="tgt292" class="tgtSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6317b9d062ca4ded11773f5df0c39062" id="tgt293" class="tgtSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12f702a41807df637765daa681fed78c" id="tgt294" class="tgtSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63e99e63156fc90f114fa402662387ef" id="tgt295" class="tgtSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="74868f1ee86eb0eaa5fb352a7f6c8f9e" id="tgt296" class="tgtSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="280d1ffb462810568a6fdc7ed49c472c" id="tgt297" class="tgtSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b34e9458e67545a04e915c7ef55719e8" id="tgt298" class="tgtSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45afed999f9128204c1b1e5adf7405f8" id="tgt299" class="tgtSentence">ILockBytes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c90d9924ae74cab935b46bc666cb4203" id="tgt300" class="tgtSentence">DBPROP_ILockBytes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="215599a847f963e27588b79210d3ea56" id="tgt301" class="tgtSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be4b610383a4b1af3438c855f29cb110" id="tgt302" class="tgtSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5e86d5adb921fd6e7b7616e2cc6d0b1" id="tgt303" class="tgtSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b8f2d2a246c88031ced7fa4b20e891d" id="tgt304" class="tgtSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5cf35ba4349e6da426be07d34952411e" id="tgt305" class="tgtSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37736c2f13339b1d0f75108bb2e84bd0" id="tgt306" class="tgtSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f7deea1588ac1cc7f77f6df70c1434b" id="tgt307" class="tgtSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f58d445e65ef2cd341481713e2aa6a9" id="tgt308" class="tgtSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e3f7c5b1879950f9342e7cced01273f3" id="tgt309" class="tgtSentence">IRowsetIndex</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6042e3b382f503197951508039d93710" id="tgt310" class="tgtSentence">DBPROP_IRowsetIndex</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1c6d3c5946bb65aba4e55669cac68a" id="tgt311" class="tgtSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8b178f861273bd6fcaa2cd53841838b" id="tgt312" class="tgtSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92f23aaea36b3e3b3f1b4b456d4b0f8a" id="tgt313" class="tgtSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8732f1240c2bdcfd2d50aa877ca7b299" id="tgt314" class="tgtSentence">DBPROP_IRowsestLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82189c22157ca5dbc1566ce5b8fee507" id="tgt315" class="tgtSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="151e636103f6679064656728e4630284" id="tgt316" class="tgtSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b167241425c6c09726e930d5db411617" id="tgt317" class="tgtSentence">DBPROP_IRowsetScroll</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="869692d9e5c7b7dc7dcfdaf30a7bd348" id="tgt318" class="tgtSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fda716a018fb2c9d85d7f104af6d28fa" id="tgt319" class="tgtSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fd77e41428ef2a86d5994c0a4e658f" id="tgt320" class="tgtSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6fb965f1bd078f921c5a73f084a7d09" id="tgt321" class="tgtSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="40f5759c2cdc1f9b68e6b0c162714753" id="tgt322" class="tgtSentence">IStorage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b61424aa1f6bd9fb838069f140834e40" id="tgt323" class="tgtSentence">DBPROP_IStorage</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2d5d0d1cb71d3cef4032b3cad9fcb77" id="tgt324" class="tgtSentence">IStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="da8994beee477ef4fd5cf9143e4c26ad" id="tgt325" class="tgtSentence">DBPROP_IStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="130702210bcc45e1afd88b1f2aae1a0b" id="tgt326" class="tgtSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d1813dfdbbaa1c4660b2933198fb3f7" id="tgt327" class="tgtSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34cd68a4ad9a3b16548954ff8184424c" id="tgt328" class="tgtSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbe0ebf1ce342bea12faf4f9960e35db" id="tgt329" class="tgtSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="627482c800288bba5eaa6324bec11b5a" id="tgt330" class="tgtSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8709209928583492b7e8ee9057e1dcd2" id="tgt331" class="tgtSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37f4175871594fd8b8484066ab57df1f" id="tgt332" class="tgtSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="610508ace43dba0c007eb22818d91137" id="tgt333" class="tgtSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09b385ae7a340805af12a182ddf23eb4" id="tgt334" class="tgtSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f76fd118082b0c0ce064d13a83f97d8" id="tgt335" class="tgtSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2a235cb612ded93059abe7d46a49fe3" id="tgt336" class="tgtSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db2433d929e5ee5dac5bf4e762cb10ab" id="tgt337" class="tgtSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8112db23cce9278ba61947c470e76c84" id="tgt338" class="tgtSentence">Memory Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab00228ad48e6044d3e6fa7f306b6984" id="tgt339" class="tgtSentence">DBPROP_MEMORYUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9cf646cc11e82fcf71add13e9d665dd" id="tgt340" class="tgtSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17bc94f9006a838977a349a959373da8" id="tgt341" class="tgtSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c018979b39f45a0e004063ce0373c75f" id="tgt342" class="tgtSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00045b5ae2bb643fd385c818dc8e48c6" id="tgt343" class="tgtSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cd5ca965481ad65661cdb310d078fa3" id="tgt344" class="tgtSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7319271b36838a8630e00ceb4554a65" id="tgt345" class="tgtSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf6cb25fea1126c44957f7d00a3a2c4f" id="tgt346" class="tgtSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2e7ff400a4ef4b66e01a7d0219e3d034" id="tgt347" class="tgtSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe7ca5c576c7eb49b58dec45de3b371" id="tgt348" class="tgtSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4267002726b89c5712c11b77ab4b758" id="tgt349" class="tgtSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f08474ed3d97c8e3919ffe184b8cb02e" id="tgt350" class="tgtSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ffd196cae96727a7c58c6701e3c65c1" id="tgt351" class="tgtSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45b7a56f3096b95b93f70ce662332136" id="tgt352" class="tgtSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8d7e45b16c6a09599199e5237263f63" id="tgt353" class="tgtSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="780561121ea65efc60d011b3855083ed" id="tgt354" class="tgtSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8bbf20691fd6dfdc3b55d73bb1b4df42" id="tgt355" class="tgtSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c89b03f5c13331074eed0814571479b" id="tgt356" class="tgtSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1be32916280f74ae0b5b31424efe2e97" id="tgt357" class="tgtSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="360431977c32a0e461c2a887196342cf" id="tgt358" class="tgtSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="015f02a3c579b5978974bb340adbc2ed" id="tgt359" class="tgtSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2fee318949f99eb5f0586e8492ffbaa" id="tgt360" class="tgtSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46634a21ff13d23b96f57f1b7a8e74b3" id="tgt361" class="tgtSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af57e2554f3db187894681afa3ebb162" id="tgt362" class="tgtSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="120451667e76bd8d13d0f0fce84d89e0" id="tgt363" class="tgtSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90f54100a94260ff7c00300f6cfd91d3" id="tgt364" class="tgtSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe1dffe626e729c9881c31329af50b19" id="tgt365" class="tgtSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="993c9b2a5a406fa810a7c0a353c0241d" id="tgt366" class="tgtSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62dbebf39ca99d9e0f7d2548b1a1e897" id="tgt367" class="tgtSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="594965351c01632879dd3120d6bdf6d1" id="tgt368" class="tgtSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dacf8514ed973feacfcb951277d7a7e0" id="tgt369" class="tgtSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26a6a1d6d267ebfa661503a67852b551" id="tgt370" class="tgtSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78e460d27437866f950bef1a322f4fad" id="tgt371" class="tgtSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1082afc70d114a04c5a7c028f54bbef" id="tgt372" class="tgtSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af912945703d4c7e5769a4a5e275c429" id="tgt373" class="tgtSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e89662e8e842b5980db8ce27cddbb136" id="tgt374" class="tgtSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f0866326f49f046b4c2d341fbf8b4a8" id="tgt375" class="tgtSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1a3b43e5bc3c750c8484e75d2dc513" id="tgt376" class="tgtSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d147a76184915ab68be6596b43255f" id="tgt377" class="tgtSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d60a3e481cd7af54f8384abea4e16a7c" id="tgt378" class="tgtSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65b8fe6df5aa2933471401a6b676fba7" id="tgt379" class="tgtSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1198df197cf7df924a1b241c2b2f0043" id="tgt380" class="tgtSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18919c01495e96c385f2eaf5938a7b03" id="tgt381" class="tgtSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdb695a9cc13c0f5e2c73bda79d0aaf" id="tgt382" class="tgtSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a40c17ef17a290d8ff208c5db8518c1" id="tgt383" class="tgtSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78cbcb8d94e6c7daf9e961f93e6b2886" id="tgt384" class="tgtSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d19dc5275a879b3a434a516970425f79" id="tgt385" class="tgtSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5b98c46a74cf81a3a5714e4746025dc3" id="tgt386" class="tgtSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb5fb6c60c1d012edd101ab61e996364" id="tgt387" class="tgtSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8a7611a82fb7d9716f4f12a82fb60754" id="tgt388" class="tgtSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e51a0debee4b6fc0ca6b1e781fc16df7" id="tgt389" class="tgtSentence">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16753e39b4d45199dca719ac2995aeb1" id="tgt390" class="tgtSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="824f2ba91f8243744ab6a8227fbb157f" id="tgt391" class="tgtSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adc2bf5dd51cf373e1aacf17aef14bbd" id="tgt392" class="tgtSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ac6cf4fa0ff0c7b5050593b220d13af2" id="tgt393" class="tgtSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="692ef25d05bb91b856cf5d0564cf74fd" id="tgt394" class="tgtSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87f408e0686b76395d281e685f65bc08" id="tgt395" class="tgtSentence">DBPROP_BOOKMARKSKIPPED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2463d9a101f9c39973277d105f8bf119" id="tgt396" class="tgtSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b4fbfcb976445a344da1d0972764bf0d" id="tgt397" class="tgtSentence">DBPROP_STRONGITDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11c74d1c21dc5dbb8b802a7408596d87" id="tgt398" class="tgtSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2086801d6ac44d08784890faac1a126" id="tgt399" class="tgtSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7a56dd282a8abf8100c423430ec8e4ac" id="tgt400" class="tgtSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd43d482f9e85ec89014c21fbd361a4" id="tgt401" class="tgtSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="af1974d09c74dc4d634c2cdc45a0ab7c" id="tgt402" class="tgtSentence">Command Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ab4280ff216db2e6f6071ba86870ade8" id="tgt403" class="tgtSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d27c70c8521c8760a817c283e11ab448" id="tgt404" class="tgtSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fca0865baf7e3ec879b19df286a8a77" id="tgt405" class="tgtSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1594fad277e4590ddbbf46e340c4d10c" id="tgt406" class="tgtSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3ae70d0cfd08d73c0e8657de04e3ba3" id="tgt407" class="tgtSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7bc03dfea4165f8cc7279ecbcee1f41e" id="tgt408" class="tgtSentence">Append-Only Rowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="323934bf263c92d3fce05577ebb64799" id="tgt409" class="tgtSentence">DBPROP_APPENDONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b52683364c551ef6f2a83a9b61aca26" id="tgt410" class="tgtSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7eade57591bcbdf71a01307c5fa55333" id="tgt411" class="tgtSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="39674232a2f3f57e87b6f56e9fcd620c" id="tgt412" class="tgtSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c5692554e1273a4cc28709961881f78" id="tgt413" class="tgtSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab13a6b41c0fedc395cff5ae82b531b6" id="tgt414" class="tgtSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt415" class="tgtSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="246a7d96dd79b612bad343d03ea2bec6" id="tgt416" class="tgtSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="75cbb9fc61a14afcadf102cfdd0a6733" id="tgt417" class="tgtSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="534d9e8ffeeeff5bf0f381032bbefd20" id="tgt418" class="tgtSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3eac3ca56c13d98b9d1f1d8ef5620027" id="tgt419" class="tgtSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="30f3aa8c0ff671730367a69d810898b9" id="tgt420" class="tgtSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="32873d7085b6feb780bf00ea59c3a386" id="tgt421" class="tgtSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec83d16d5fb11f0a7e532fe6a91dfc36" id="tgt422" class="tgtSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af283d090de02b75e79bf25ce7aa945a" id="tgt423" class="tgtSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c34dec6888b6b898acb79b0597922c27" id="tgt424" class="tgtSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7906ea7eac0a5466ea33c9bf87d083db" id="tgt425" class="tgtSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c24d8cc4559e441d51781708292d746" id="tgt426" class="tgtSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b5c3be77a4c5f0654fd6637b3fd2b44" id="tgt427" class="tgtSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f518893e9bb8f74c9382260d0f79450b" id="tgt428" class="tgtSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2bdf72f0b7184d9ebe2e4086c598ee58" id="tgt429" class="tgtSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d33d5718660dbb261dc40b878ec4b591" id="tgt430" class="tgtSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4fcb4539a8be17b29a97aada5fa31577" id="tgt431" class="tgtSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="28dbf41d74f2a648a563b28d2ecef878" id="tgt432" class="tgtSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba30e9909e02f6f6179f9db5cb9852cf" id="tgt433" class="tgtSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6317b9d062ca4ded11773f5df0c39062" id="tgt434" class="tgtSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12f702a41807df637765daa681fed78c" id="tgt435" class="tgtSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63e99e63156fc90f114fa402662387ef" id="tgt436" class="tgtSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="74868f1ee86eb0eaa5fb352a7f6c8f9e" id="tgt437" class="tgtSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="280d1ffb462810568a6fdc7ed49c472c" id="tgt438" class="tgtSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b34e9458e67545a04e915c7ef55719e8" id="tgt439" class="tgtSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45afed999f9128204c1b1e5adf7405f8" id="tgt440" class="tgtSentence">ILockBytes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c90d9924ae74cab935b46bc666cb4203" id="tgt441" class="tgtSentence">DBPROP_ILockBytes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="215599a847f963e27588b79210d3ea56" id="tgt442" class="tgtSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be4b610383a4b1af3438c855f29cb110" id="tgt443" class="tgtSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5e86d5adb921fd6e7b7616e2cc6d0b1" id="tgt444" class="tgtSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b8f2d2a246c88031ced7fa4b20e891d" id="tgt445" class="tgtSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5cf35ba4349e6da426be07d34952411e" id="tgt446" class="tgtSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37736c2f13339b1d0f75108bb2e84bd0" id="tgt447" class="tgtSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6f7deea1588ac1cc7f77f6df70c1434b" id="tgt448" class="tgtSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f58d445e65ef2cd341481713e2aa6a9" id="tgt449" class="tgtSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e3f7c5b1879950f9342e7cced01273f3" id="tgt450" class="tgtSentence">IRowsetIndex</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6042e3b382f503197951508039d93710" id="tgt451" class="tgtSentence">DBPROP_IRowsetIndex</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1c6d3c5946bb65aba4e55669cac68a" id="tgt452" class="tgtSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8b178f861273bd6fcaa2cd53841838b" id="tgt453" class="tgtSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92f23aaea36b3e3b3f1b4b456d4b0f8a" id="tgt454" class="tgtSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8ec2465ef542faa46a5d8e47da92cca3" id="tgt455" class="tgtSentence">DBPROP_IRowsetLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="82189c22157ca5dbc1566ce5b8fee507" id="tgt456" class="tgtSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="151e636103f6679064656728e4630284" id="tgt457" class="tgtSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b167241425c6c09726e930d5db411617" id="tgt458" class="tgtSentence">DBPROP_IRowsetScroll</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="869692d9e5c7b7dc7dcfdaf30a7bd348" id="tgt459" class="tgtSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fda716a018fb2c9d85d7f104af6d28fa" id="tgt460" class="tgtSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0fd77e41428ef2a86d5994c0a4e658f" id="tgt461" class="tgtSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6fb965f1bd078f921c5a73f084a7d09" id="tgt462" class="tgtSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="40f5759c2cdc1f9b68e6b0c162714753" id="tgt463" class="tgtSentence">IStorage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b61424aa1f6bd9fb838069f140834e40" id="tgt464" class="tgtSentence">DBPROP_IStorage</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2d5d0d1cb71d3cef4032b3cad9fcb77" id="tgt465" class="tgtSentence">IStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="da8994beee477ef4fd5cf9143e4c26ad" id="tgt466" class="tgtSentence">DBPROP_IStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="130702210bcc45e1afd88b1f2aae1a0b" id="tgt467" class="tgtSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d1813dfdbbaa1c4660b2933198fb3f7" id="tgt468" class="tgtSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34cd68a4ad9a3b16548954ff8184424c" id="tgt469" class="tgtSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbe0ebf1ce342bea12faf4f9960e35db" id="tgt470" class="tgtSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="627482c800288bba5eaa6324bec11b5a" id="tgt471" class="tgtSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8709209928583492b7e8ee9057e1dcd2" id="tgt472" class="tgtSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ac2e31b5fd88afee8c9979f44a49bf9" id="tgt473" class="tgtSentence">Lock Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="04b22bfa92a633895f2c4cf0391cd26a" id="tgt474" class="tgtSentence">DBPROP_LOCKMODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37f4175871594fd8b8484066ab57df1f" id="tgt475" class="tgtSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="610508ace43dba0c007eb22818d91137" id="tgt476" class="tgtSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09b385ae7a340805af12a182ddf23eb4" id="tgt477" class="tgtSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f76fd118082b0c0ce064d13a83f97d8" id="tgt478" class="tgtSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2a235cb612ded93059abe7d46a49fe3" id="tgt479" class="tgtSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db2433d929e5ee5dac5bf4e762cb10ab" id="tgt480" class="tgtSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d9cf646cc11e82fcf71add13e9d665dd" id="tgt481" class="tgtSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17bc94f9006a838977a349a959373da8" id="tgt482" class="tgtSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c018979b39f45a0e004063ce0373c75f" id="tgt483" class="tgtSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00045b5ae2bb643fd385c818dc8e48c6" id="tgt484" class="tgtSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9cd5ca965481ad65661cdb310d078fa3" id="tgt485" class="tgtSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7319271b36838a8630e00ceb4554a65" id="tgt486" class="tgtSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf6cb25fea1126c44957f7d00a3a2c4f" id="tgt487" class="tgtSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2e7ff400a4ef4b66e01a7d0219e3d034" id="tgt488" class="tgtSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fe7ca5c576c7eb49b58dec45de3b371" id="tgt489" class="tgtSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4267002726b89c5712c11b77ab4b758" id="tgt490" class="tgtSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f08474ed3d97c8e3919ffe184b8cb02e" id="tgt491" class="tgtSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ffd196cae96727a7c58c6701e3c65c1" id="tgt492" class="tgtSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45b7a56f3096b95b93f70ce662332136" id="tgt493" class="tgtSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8d7e45b16c6a09599199e5237263f63" id="tgt494" class="tgtSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="780561121ea65efc60d011b3855083ed" id="tgt495" class="tgtSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8bbf20691fd6dfdc3b55d73bb1b4df42" id="tgt496" class="tgtSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2c89b03f5c13331074eed0814571479b" id="tgt497" class="tgtSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1be32916280f74ae0b5b31424efe2e97" id="tgt498" class="tgtSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="360431977c32a0e461c2a887196342cf" id="tgt499" class="tgtSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="015f02a3c579b5978974bb340adbc2ed" id="tgt500" class="tgtSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2fee318949f99eb5f0586e8492ffbaa" id="tgt501" class="tgtSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46634a21ff13d23b96f57f1b7a8e74b3" id="tgt502" class="tgtSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af57e2554f3db187894681afa3ebb162" id="tgt503" class="tgtSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="120451667e76bd8d13d0f0fce84d89e0" id="tgt504" class="tgtSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90f54100a94260ff7c00300f6cfd91d3" id="tgt505" class="tgtSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe1dffe626e729c9881c31329af50b19" id="tgt506" class="tgtSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="993c9b2a5a406fa810a7c0a353c0241d" id="tgt507" class="tgtSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62dbebf39ca99d9e0f7d2548b1a1e897" id="tgt508" class="tgtSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="594965351c01632879dd3120d6bdf6d1" id="tgt509" class="tgtSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dacf8514ed973feacfcb951277d7a7e0" id="tgt510" class="tgtSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26a6a1d6d267ebfa661503a67852b551" id="tgt511" class="tgtSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78e460d27437866f950bef1a322f4fad" id="tgt512" class="tgtSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d1082afc70d114a04c5a7c028f54bbef" id="tgt513" class="tgtSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af912945703d4c7e5769a4a5e275c429" id="tgt514" class="tgtSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e89662e8e842b5980db8ce27cddbb136" id="tgt515" class="tgtSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f0866326f49f046b4c2d341fbf8b4a8" id="tgt516" class="tgtSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b1a3b43e5bc3c750c8484e75d2dc513" id="tgt517" class="tgtSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="06d147a76184915ab68be6596b43255f" id="tgt518" class="tgtSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d60a3e481cd7af54f8384abea4e16a7c" id="tgt519" class="tgtSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65b8fe6df5aa2933471401a6b676fba7" id="tgt520" class="tgtSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1198df197cf7df924a1b241c2b2f0043" id="tgt521" class="tgtSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18919c01495e96c385f2eaf5938a7b03" id="tgt522" class="tgtSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbdb695a9cc13c0f5e2c73bda79d0aaf" id="tgt523" class="tgtSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4a40c17ef17a290d8ff208c5db8518c1" id="tgt524" class="tgtSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="78cbcb8d94e6c7daf9e961f93e6b2886" id="tgt525" class="tgtSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d19dc5275a879b3a434a516970425f79" id="tgt526" class="tgtSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5b98c46a74cf81a3a5714e4746025dc3" id="tgt527" class="tgtSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb5fb6c60c1d012edd101ab61e996364" id="tgt528" class="tgtSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8a7611a82fb7d9716f4f12a82fb60754" id="tgt529" class="tgtSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3528ed34871b6b038968af4a908dc081" id="tgt530" class="tgtSentence">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16753e39b4d45199dca719ac2995aeb1" id="tgt531" class="tgtSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="824f2ba91f8243744ab6a8227fbb157f" id="tgt532" class="tgtSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="adc2bf5dd51cf373e1aacf17aef14bbd" id="tgt533" class="tgtSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ac6cf4fa0ff0c7b5050593b220d13af2" id="tgt534" class="tgtSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="be346cc75b8dd118f2f2af71e8f65a26" id="tgt535" class="tgtSentence">Server Data on Insert</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5024c80fbef16b8c9a3cf58c2ed5e22f" id="tgt536" class="tgtSentence">DBPROP_SERVERDATAONINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="692ef25d05bb91b856cf5d0564cf74fd" id="tgt537" class="tgtSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7bffaed4f81d15733e9f3df7fcdb33a4" id="tgt538" class="tgtSentence">DBPROP_BOOKMARKSKIP</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2463d9a101f9c39973277d105f8bf119" id="tgt539" class="tgtSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f0289c4d7472816b838bf34a3b92d2c" id="tgt540" class="tgtSentence">DBPROP_STRONGIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11c74d1c21dc5dbb8b802a7408596d87" id="tgt541" class="tgtSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2086801d6ac44d08784890faac1a126" id="tgt542" class="tgtSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7a56dd282a8abf8100c423430ec8e4ac" id="tgt543" class="tgtSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd43d482f9e85ec89014c21fbd361a4" id="tgt544" class="tgtSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="a1cc159e3f19aaf7c317ee90ae24b1cb" id="tgt545" class="tgtSentence">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, see <externalLink><linkText>Jet Provider</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms722791.aspx</linkUri></externalLink> in the OLE DB documentation.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Connection String Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">To connect to this provider, set the <legacyItalic>Provider</legacyItalic> argument of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property to the following:</caps:sentence>
          </para>
          <code>Microsoft.Jet.OLEDB.4.0</code>
          <para>
            <caps:sentence id="src4" class="srcSentence">Reading the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property will also return this string.</caps:sentence>
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
          <code>"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=<legacyItalic xmlns="">databaseName</legacyItalic>;User ID=<legacyItalic xmlns="">MyUserID</legacyItalic>;Password=<legacyItalic xmlns="">MyPassword</legacyItalic>;"</code>
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
                    <caps:sentence id="src11" class="srcSentence">Specifies the OLE DB Provider for Microsoft Jet.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src12" class="srcSentence">Data Source</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Specifies the database path and file name (for example, <codeInline>c:\Northwind.mdb</codeInline>).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src14" class="srcSentence">User ID</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Specifies the user name.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> If this keyword is not specified, the string, "<codeInline>admin</codeInline>", is used by default.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src17" class="srcSentence">Password</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Specifies the user password.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> If this keyword is not specified, the empty string (""), is used by default.</caps:sentence>
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
            <caps:sentence id="src22" class="srcSentence">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those that are defined by ADO.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> As with all other <legacyBold>Connection</legacyBold> parameters, they can be set by using the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Connection</legacyBold> object or as part of the connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">The following table lists these properties together with the corresponding OLE DB property name in parentheses.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Parameter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Jet OLEDB:Compact Reclaimed Space Amount (DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database.</caps:sentence>
                    <caps:sentence id="src29" class="srcSentence"> This value is only valid after a database connection has been established.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Jet OLEDB:Connection Control (DBPROP_JETOLEDB_CONNECTIONCONTROL)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Indicates whether users can connect to the database.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Jet OLEDB:Create System Database (DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Indicates whether a system database should be created when creating a new data source.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Jet OLEDB:Database Locking Mode (DBPROP_JETOLEDB_DATABASELOCKMODE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Indicates the locking mode for this database.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> The first user to open the database determines the mode used while the database is open.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Jet OLEDB:Database Password (DBPROP_JETOLEDB_DATABASEPASSWORD)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Indicates the database password.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Jet OLEDB:Don't Copy Locale on Compact (DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Indicates whether Jet should copy locale information when compacting a database.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Jet OLEDB:Encrypt Database (DBPROP_JETOLEDB_ENCRYPTDATABASE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Indicates whether a compacted database should be encrypted.</caps:sentence>
                    <caps:sentence id="src43" class="srcSentence"> If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Jet OLEDB:Engine Type (DBPROP_JETOLEDB_ENGINE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Indicates the storage engine used to access the current data store.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Jet OLEDB:Exclusive Async Delay (DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">This property is ignored unless <legacyBold>Jet OLEDB:Flush Transaction Timeout</legacyBold> is set to 0.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Jet OLEDB:Flush Transaction Timeout (DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk.</caps:sentence>
                    <caps:sentence id="src51" class="srcSentence"> This setting overrides the values for <legacyBold>Jet OLEDB:Shared Async Delay</legacyBold> and <legacyBold>Jet OLEDB:Exclusive Async Delay</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Jet OLEDB:Global Bulk Transactions (DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Indicates whether SQL bulk transactions are transacted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Jet OLEDB:Global Partial Bulk Ops (DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Indicates the password used to open the database.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Jet OLEDB:Implicit Commit Sync (DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Indicates whether changes that were made in internal implicit transactions are written in synchronous or asynchronous mode.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">Jet OLEDB:Lock Delay (DBPROP_JETOLEDB_LOCKDELAY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Indicates the number of milliseconds to wait before trying to acquire a lock after a previous attempt has failed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">Jet OLEDB:Lock Retry (DBPROP_JETOLEDB_LOCKRETRY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">Indicates how many times an attempt to access a locked page is repeated.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Jet OLEDB:Max Buffer Size (DBPROP_JETOLEDB_MAXBUFFERSIZE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">Jet OLEDB:Max Locks Per File (DBPROP_JETOLEDB_MAXLOCKSPERFILE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">Indicates the maximum number of locks Jet can place on a database.</caps:sentence>
                    <caps:sentence id="src66" class="srcSentence"> The default value is 9500.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">Jet OLEDB:New Database Password (DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">Indicates the new password to be set for this database.</caps:sentence>
                    <caps:sentence id="src69" class="srcSentence"> The old password is stored in <legacyBold>Jet OLEDB:Database Password</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">Jet OLEDB:ODBC Command Time Out (DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">Indicates the number of milliseconds before a remote ODBC query from Jet will time out.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Jet OLEDB:Page Locks to Table Lock (DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">Indicates how many pages must be locked within a transaction before Jet tries to promote the lock to a table lock.</caps:sentence>
                    <caps:sentence id="src74" class="srcSentence"> If this value is 0, the lock is never promoted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">Jet OLEDB:Page Timeout (DBPROP_JETOLEDB_PAGETIMEOUT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">Indicates the number of milliseconds Jet will wait before checking to see whether its cache is out of date with the database file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">Jet OLEDB:Recycle Long-Valued Pages (DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">Jet OLEDB:Registry Path (DBPROP_JETOLEDB_REGPATH)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">Indicates the Windows registry key that contains values for the Jet database engine.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">Jet OLEDB:Reset ISAM Stats (DBPROP_JETOLEDB_RESETISAMSTATS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">Indicates whether the schema <legacyBold>Recordset</legacyBold> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after it returns performance information.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">Jet OLEDB:Shared Async Delay (DBPROP_JETOLEDB_SHAREDASYNCDELAY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multiuser mode.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">Jet OLEDB:System Database (DBPROP_JETOLEDB_SYSDBPATH)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">Indicates the path and file name for the workgroup information file (system database).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">Jet OLEDB:Transaction Commit Mode (DBPROP_JETOLEDB_TXNCOMMITMODE)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">Jet OLEDB:User Commit Sync (DBPROP_JETOLEDB_USERCOMMITSYNC)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">Indicates whether changes that were made in transactions are written in synchronous or asynchronous mode.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src91" class="srcSentence">Provider-Specific Recordset and Command Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src92" class="srcSentence">The Jet provider also supports several provider-specific <legacyBold>Recordset</legacyBold> and <legacyBold>Command</legacyBold> properties.</caps:sentence>
            <caps:sentence id="src93" class="srcSentence"> These properties are accessed and set through the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> or <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence id="src94" class="srcSentence"> The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src97" class="srcSentence">Jet OLEDB:Bulk Transactions (DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">Indicates whether SQL bulk operations are transacted.</caps:sentence>
                    <caps:sentence id="src99" class="srcSentence"> Large bulk operations might fail when transacted, because of resource delays.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Jet OLEDB:Enable Fat Cursors (DBPROP_JETOLEDB_ENABLEFATCURSOR)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">Jet OLEDB:Fat Cursor Cache Size (DBPROP_JETOLEDB_FATCURSORMAXROWS)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src103" class="srcSentence">Indicates the number of rows to cache when using remote data store row caching.</caps:sentence>
                    <caps:sentence id="src104" class="srcSentence"> This value is ignored unless <legacyBold>Jet OLEDB:Enable Fat Cursors</legacyBold> is True.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">Jet OLEDB:Inconsistent (DBPROP_JETOLEDB_INCONSISTENT)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">Indicates whether query results allow inconsistent updates.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">Jet OLEDB:Locking Granularity (DBPROP_JETOLEDB_LOCKGRANULARITY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">Indicates whether a table is opened using row-level locking.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">Jet OLEDB:ODBC Pass-Through Statement (DBPROP_JETOLEDB_ODBCPASSTHROUGH)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Indicates that Jet should pass the SQL text in a <legacyBold>Command</legacyBold> object to the back end unaltered.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">Jet OLEDB:Partial Bulk Ops (DBPROP_JETOLEDB_BULKPARTIAL)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">Indicates Jet's behavior when SQL DML operations fail.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">Jet OLEDB:Pass Through Query Bulk-Op (DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">Indicates whether queries that do not return a <legacyBold>Recordset</legacyBold> are passed unaltered to the data source.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">Jet OLEDB:Pass Through Query Connect String (DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">Indicates the Jet connect string used to connect to a remote data store.</caps:sentence>
                    <caps:sentence id="src117" class="srcSentence"> This value is ignored unless <legacyBold>Jet OLEDB:ODBC Pass-Through Statement</legacyBold> is True.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">Jet OLEDB:Stored Query (DBPROP_JETOLEDB_STOREDQUERY)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">Jet OLEDB:Validate Rules On Set (DBPROP_JETOLEDB_VALIDATEONSET)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src122" class="srcSentence">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode.</caps:sentence>
            <caps:sentence id="src123" class="srcSentence"> To open a database in read-only mode, set the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property on the ADO <legacyBold>Connection</legacyBold> object to <legacyBold>adModeRead</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src124" class="srcSentence">Command Object Usage</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src125" class="srcSentence">Command text in the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object uses the Microsoft Jet SQL dialect.</caps:sentence>
            <caps:sentence id="src126" class="srcSentence"> You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src127" class="srcSentence">Recordset Behavior</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src128" class="srcSentence">The Microsoft Jet database engine does not support dynamic cursors.</caps:sentence>
            <caps:sentence id="src129" class="srcSentence"> Therefore, the OLE DB Provider for Microsoft Jet does not support the <legacyBold>adLockDynamic</legacyBold> cursor type.</caps:sentence>
            <caps:sentence id="src130" class="srcSentence"> When a dynamic cursor is requested, the provider will return a keyset cursor and reset the <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink> property to indicate the type of <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> returned.</caps:sentence>
            <caps:sentence id="src131" class="srcSentence"> Further, if an updatable <legacyBold>Recordset</legacyBold> is requested (<legacyBold>LockType</legacyBold> is <legacyBold>adLockOptimistic</legacyBold>, <legacyBold>adLockBatchOptimistic</legacyBold>, or <legacyBold>adLockPessimistic</legacyBold>) the provider will also return a keyset cursor and reset the <legacyBold>CursorType</legacyBold> property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src132" class="srcSentence">Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src133" class="srcSentence">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the <legacyBold>Properties</legacyBold> collection of the unopened <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src134" class="srcSentence">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property.</caps:sentence>
            <caps:sentence id="src135" class="srcSentence"> The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description."</caps:sentence>
            <caps:sentence id="src136" class="srcSentence"> You can find more information about these properties in the OLE DB Programmer's Reference.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src137" class="srcSentence">Connection Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src138" class="srcSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">Active Sessions</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">DBPROP_ACTIVESESSIONS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">Asynchable Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">DBPROP_ASYNCTXNABORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">Asynchable Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">DBPROP_ASYNCTNXCOMMIT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">Autocommit Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src148" class="srcSentence">DBPROP_SESS_AUTOCOMMITISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">Catalog Location</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">DBPROP_CATALOGLOCATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">Catalog Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">DBPROP_CATALOGTERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">Column Definition</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">DBPROP_COLUMNDEFINITION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src155" class="srcSentence">Current Catalog</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">DBPROP_CURRENTCATALOG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">DBPROP_INIT_DATASOURCE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">Data Source Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">DBPROP_DATASOURCENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">Data Source Object Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">DBPROP_DSOTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">DBMS Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">DBPROP_DBMSNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">DBMS Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">DBPROP_DBMSVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">GROUP BY Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">DBPROP_GROUPBY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">Heterogeneous Table Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">DBPROP_HETEROGENEOUSTABLES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">Identifier Case Sensitivity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">DBPROP_IDENTIFIERCASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">Isolation Levels</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">DBPROP_SUPPORTEDTXNISOLEVELS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">Isolation Retention</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">DBPROP_SUPPORTEDTXNISORETAIN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">Locale Identifier</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">DBPROP_INIT_LCID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">Maximum Index Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">DBPROP_MAXINDEXSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">Maximum Row Size</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">DBPROP_MAXROWSIZE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">Maximum Row Size Includes BLOB</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">DBPROP_MAXROWSIZEINCLUDESBLOB</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">Maximum Tables in SELECT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">DBPROP_MAXTABLESINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">DBPROP_INIT_MODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">Multiple Parameter Sets</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src190" class="srcSentence">DBPROP_MULTIPLEPARAMSETS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">Multiple Results</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">DBPROP_MULTIPLERESULTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src193" class="srcSentence">Multiple Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">DBPROP_MULTIPLESTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">Multi-Table Update</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">DBPROP_MULTITABLEUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src197" class="srcSentence">NULL Collation Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">DBPROP_NULLCOLLATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">NULL Concatenation Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">DBPROP_CONCATNULLBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">OLE DB Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">DBPROP_PROVIDEROLEDBVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">OLE Object Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">DBPROP_OLEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">Open Rowset Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src206" class="srcSentence">DBPROP_OPENROWSETSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">ORDER BY Columns in Select List</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src208" class="srcSentence">DBPROP_ORDERBYCOLUMNSINSELECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">Output Parameter Availability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src210" class="srcSentence">DBPROP_OUTPUTPARAMETERAVAILABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src211" class="srcSentence">Pass By Ref Accessors</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">DBPROP_BYREFACCESSORS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">Password</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">DBPROP_AUTH_PASSWORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src215" class="srcSentence">Persistent ID Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src216" class="srcSentence">DBPROP_PERSISTENTIDTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src217" class="srcSentence">Prepare Abort Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src218" class="srcSentence">DBPROP_PREPAREABORTBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src219" class="srcSentence">Prepare Commit Behavior</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src220" class="srcSentence">DBPROP_PREPARECOMMITBEHAVIOR</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src221" class="srcSentence">Procedure Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src222" class="srcSentence">DBPROP_PROCEDURETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src223" class="srcSentence">Prompt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">DBPROP_INIT_PROMPT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src225" class="srcSentence">Provider Friendly Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src226" class="srcSentence">DBPROP_PROVIDERFRIENDLYNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src227" class="srcSentence">Provider Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src228" class="srcSentence">DBPROP_PROVIDERFILENAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src229" class="srcSentence">Provider Version</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src230" class="srcSentence">DBPROP_PROVIDERVER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">Read-Only Data Source</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">DBPROP_DATASOURCEREADONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src233" class="srcSentence">Rowset Conversions on Command</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src234" class="srcSentence">DBPROP_ROWSETCONVERSIONSONCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src235" class="srcSentence">Schema Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src236" class="srcSentence">DBPROP_SCHEMATERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src237" class="srcSentence">Schema Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src238" class="srcSentence">DBPROP_SCHEMAUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src239" class="srcSentence">SQL Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src240" class="srcSentence">DBPROP_SQLSUPPORT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src241" class="srcSentence">Structured Storage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src242" class="srcSentence">DBPROP_STRUCTUREDSTORAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src243" class="srcSentence">Subquery Support</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">DBPROP_SUBQUERIES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src245" class="srcSentence">Table Term</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">DBPROP_TABLETERM</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">Transaction DDL</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src248" class="srcSentence">DBPROP_SUPPORTEDTXNDDL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">User ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src250" class="srcSentence">DBPROP_AUTH_USERID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src251" class="srcSentence">User Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src252" class="srcSentence">DBPROP_USERNAME</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src253" class="srcSentence">Window Handle</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src254" class="srcSentence">DBPROP_INIT_HWND</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src255" class="srcSentence">Recordset Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src256" class="srcSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src257" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src258" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src259" class="srcSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src260" class="srcSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src261" class="srcSentence">Append-Only Rowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src262" class="srcSentence">DBPROP_APPENDONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src263" class="srcSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src264" class="srcSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src265" class="srcSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src267" class="srcSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src268" class="srcSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src269" class="srcSentence">Bookmarks Ordered</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src270" class="srcSentence">DBPROP_ORDEREDBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src271" class="srcSentence">Cache Deferred Columns</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src272" class="srcSentence">DBPROP_CACHEDEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src273" class="srcSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src274" class="srcSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src275" class="srcSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src276" class="srcSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src277" class="srcSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src278" class="srcSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">Column Writable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src280" class="srcSentence">DBPROP_MAYWRITECOLUMN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src281" class="srcSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src282" class="srcSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src283" class="srcSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src284" class="srcSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src285" class="srcSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src286" class="srcSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src287" class="srcSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src288" class="srcSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src289" class="srcSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src290" class="srcSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src291" class="srcSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src292" class="srcSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src293" class="srcSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src294" class="srcSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src295" class="srcSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src296" class="srcSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src297" class="srcSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src298" class="srcSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src299" class="srcSentence">ILockBytes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src300" class="srcSentence">DBPROP_ILockBytes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src301" class="srcSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src302" class="srcSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src303" class="srcSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src304" class="srcSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src305" class="srcSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src306" class="srcSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src307" class="srcSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src308" class="srcSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src309" class="srcSentence">IRowsetIndex</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src310" class="srcSentence">DBPROP_IRowsetIndex</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src311" class="srcSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src312" class="srcSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src313" class="srcSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src314" class="srcSentence">DBPROP_IRowsestLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src315" class="srcSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src316" class="srcSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src317" class="srcSentence">DBPROP_IRowsetScroll</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src318" class="srcSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src319" class="srcSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src320" class="srcSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src321" class="srcSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src322" class="srcSentence">IStorage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src323" class="srcSentence">DBPROP_IStorage</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src324" class="srcSentence">IStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src325" class="srcSentence">DBPROP_IStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src326" class="srcSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src327" class="srcSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src328" class="srcSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src329" class="srcSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src330" class="srcSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src331" class="srcSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src332" class="srcSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src333" class="srcSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src334" class="srcSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src335" class="srcSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src336" class="srcSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src337" class="srcSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src338" class="srcSentence">Memory Usage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src339" class="srcSentence">DBPROP_MEMORYUSAGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src340" class="srcSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src341" class="srcSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src342" class="srcSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src343" class="srcSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src344" class="srcSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src345" class="srcSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src346" class="srcSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src347" class="srcSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src348" class="srcSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src349" class="srcSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src350" class="srcSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src351" class="srcSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src352" class="srcSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src353" class="srcSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src354" class="srcSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src355" class="srcSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src356" class="srcSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src357" class="srcSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src358" class="srcSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src359" class="srcSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src360" class="srcSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src361" class="srcSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src362" class="srcSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src363" class="srcSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src364" class="srcSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src365" class="srcSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src366" class="srcSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src367" class="srcSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src368" class="srcSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src369" class="srcSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src370" class="srcSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src371" class="srcSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src372" class="srcSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src373" class="srcSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src374" class="srcSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src375" class="srcSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src376" class="srcSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src377" class="srcSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src378" class="srcSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src379" class="srcSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src380" class="srcSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src381" class="srcSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src382" class="srcSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src383" class="srcSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src384" class="srcSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src385" class="srcSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src386" class="srcSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src387" class="srcSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src388" class="srcSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src389" class="srcSentence">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src390" class="srcSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src391" class="srcSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src392" class="srcSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src393" class="srcSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src394" class="srcSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src395" class="srcSentence">DBPROP_BOOKMARKSKIPPED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src396" class="srcSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src397" class="srcSentence">DBPROP_STRONGITDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src398" class="srcSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src399" class="srcSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src400" class="srcSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src401" class="srcSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src402" class="srcSentence">Command Dynamic Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src403" class="srcSentence">The following properties are added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Command</legacyBold> object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src404" class="srcSentence">ADO Property Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src405" class="srcSentence">OLE DB Property Name</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src406" class="srcSentence">Access Order</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src407" class="srcSentence">DBPROP_ACCESSORDER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src408" class="srcSentence">Append-Only Rowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src409" class="srcSentence">DBPROP_APPENDONLY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src410" class="srcSentence">Blocking Storage Objects</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src411" class="srcSentence">DBPROP_BLOCKINGSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src412" class="srcSentence">Bookmark Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src413" class="srcSentence">DBPROP_BOOKMARKTYPE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src414" class="srcSentence">Bookmarkable</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src415" class="srcSentence">DBPROP_IROWSETLOCATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src416" class="srcSentence">Change Inserted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src417" class="srcSentence">DBPROP_CHANGEINSERTEDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src418" class="srcSentence">Column Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src419" class="srcSentence">DBPROP_COLUMNRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src420" class="srcSentence">Column Set Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src421" class="srcSentence">DBPROP_NOTIFYCOLUMNSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src422" class="srcSentence">Defer Column</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src423" class="srcSentence">DBPROP_DEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src424" class="srcSentence">Delay Storage Object Updates</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src425" class="srcSentence">DBPROP_DELAYSTORAGEOBJECTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src426" class="srcSentence">Fetch Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src427" class="srcSentence">DBPROP_CANFETCHBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src428" class="srcSentence">Hold Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src429" class="srcSentence">DBPROP_CANHOLDROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src430" class="srcSentence">IAccessor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src431" class="srcSentence">DBPROP_IAccessor</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src432" class="srcSentence">IColumnsInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src433" class="srcSentence">DBPROP_IColumnsInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src434" class="srcSentence">IColumnsRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src435" class="srcSentence">DBPROP_IColumnsRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src436" class="srcSentence">IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src437" class="srcSentence">DBPROP_IConnectionPointContainer</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src438" class="srcSentence">IConvertType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src439" class="srcSentence">DBPROP_IConvertType</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src440" class="srcSentence">ILockBytes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src441" class="srcSentence">DBPROP_ILockBytes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src442" class="srcSentence">Immobile Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src443" class="srcSentence">DBPROP_IMMOBILEROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src444" class="srcSentence">IRowset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src445" class="srcSentence">DBPROP_IRowset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src446" class="srcSentence">IRowsetChange</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src447" class="srcSentence">DBPROP_IRowsetChange</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src448" class="srcSentence">IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src449" class="srcSentence">DBPROP_IRowsetIdentity</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src450" class="srcSentence">IRowsetIndex</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src451" class="srcSentence">DBPROP_IRowsetIndex</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src452" class="srcSentence">IRowsetInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src453" class="srcSentence">DBPROP_IRowsetInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src454" class="srcSentence">IRowsetLocate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src455" class="srcSentence">DBPROP_IRowsetLocate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src456" class="srcSentence">IRowsetResynch</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src457" class="srcSentence">IRowsetScroll</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src458" class="srcSentence">DBPROP_IRowsetScroll</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src459" class="srcSentence">IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src460" class="srcSentence">DBPROP_IRowsetUpdate</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src461" class="srcSentence">ISequentialStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src462" class="srcSentence">DBPROP_ISequentialStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src463" class="srcSentence">IStorage</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src464" class="srcSentence">DBPROP_IStorage</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src465" class="srcSentence">IStream</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src466" class="srcSentence">DBPROP_IStream</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src467" class="srcSentence">ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src468" class="srcSentence">DBPROP_ISupportErrorInfo</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src469" class="srcSentence">Literal Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src470" class="srcSentence">DBPROP_LITERALBOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src471" class="srcSentence">Literal Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src472" class="srcSentence">DBPROP_LITERALIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src473" class="srcSentence">Lock Mode</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src474" class="srcSentence">DBPROP_LOCKMODE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src475" class="srcSentence">Maximum Open Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src476" class="srcSentence">DBPROP_MAXOPENROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src477" class="srcSentence">Maximum Pending Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src478" class="srcSentence">DBPROP_MAXPENDINGROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src479" class="srcSentence">Maximum Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src480" class="srcSentence">DBPROP_MAXROWS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src481" class="srcSentence">Notification Granularity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src482" class="srcSentence">DBPROP_NOTIFICATIONGRANULARITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src483" class="srcSentence">Notification Phases</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src484" class="srcSentence">DBPROP_NOTIFICATIONPHASES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src485" class="srcSentence">Objects Transacted</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src486" class="srcSentence">DBPROP_TRANSACTEDOBJECT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src487" class="srcSentence">Others' Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src488" class="srcSentence">DBPROP_OTHERUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src489" class="srcSentence">Others' Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src490" class="srcSentence">DBPROP_OTHERINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src491" class="srcSentence">Own Changes Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src492" class="srcSentence">DBPROP_OWNUPDATEDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src493" class="srcSentence">Own Inserts Visible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src494" class="srcSentence">DBPROP_OWNINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src495" class="srcSentence">Preserve on Abort</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src496" class="srcSentence">DBPROP_ABORTPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src497" class="srcSentence">Preserve on Commit</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src498" class="srcSentence">DBPROP_COMMITPRESERVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src499" class="srcSentence">Quick Restart</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src500" class="srcSentence">DBPROP_QUICKRESTART</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src501" class="srcSentence">Reentrant Events</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src502" class="srcSentence">DBPROP_REENTRANTEVENTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src503" class="srcSentence">Remove Deleted Rows</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src504" class="srcSentence">DBPROP_REMOVEDELETED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src505" class="srcSentence">Report Multiple Changes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src506" class="srcSentence">DBPROP_REPORTMULTIPLECHANGES</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src507" class="srcSentence">Return Pending Inserts</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src508" class="srcSentence">DBPROP_RETURNPENDINGINSERTS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src509" class="srcSentence">Row Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src510" class="srcSentence">DBPROP_NOTIFYROWDELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src511" class="srcSentence">Row First Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src512" class="srcSentence">DBPROP_NOTIFYROWFIRSTCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src513" class="srcSentence">Row Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src514" class="srcSentence">DBPROP_NOTIFYROWINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src515" class="srcSentence">Row Privileges</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src516" class="srcSentence">DBPROP_ROWRESTRICT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src517" class="srcSentence">Row Resynchronization Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src518" class="srcSentence">DBPROP_NOTIFYROWRESYNCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src519" class="srcSentence">Row Threading Model</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src520" class="srcSentence">DBPROP_ROWTHREADMODEL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src521" class="srcSentence">Row Undo Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src522" class="srcSentence">DBPROP_NOTIFYROWUNDOCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src523" class="srcSentence">Row Undo Delete Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src524" class="srcSentence">DBPROP_NOTIFYROWUNDODELETE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src525" class="srcSentence">Row Undo Insert Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src526" class="srcSentence">DBPROP_NOTIFYROWUNDOINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src527" class="srcSentence">Row Update Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src528" class="srcSentence">DBPROP_NOTIFYROWUPDATE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src529" class="srcSentence">Rowset Fetch Position Change Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src530" class="srcSentence">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src531" class="srcSentence">Rowset Release Notification</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src532" class="srcSentence">DBPROP_NOTIFYROWSETRELEASE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src533" class="srcSentence">Scroll Backwards</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src534" class="srcSentence">DBPROP_CANSCROLLBACKWARDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src535" class="srcSentence">Server Data on Insert</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src536" class="srcSentence">DBPROP_SERVERDATAONINSERT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src537" class="srcSentence">Skip Deleted Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src538" class="srcSentence">DBPROP_BOOKMARKSKIP</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src539" class="srcSentence">Strong Row Identity</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src540" class="srcSentence">DBPROP_STRONGIDENTITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src541" class="srcSentence">Updatability</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src542" class="srcSentence">DBPROP_UPDATABILITY</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src543" class="srcSentence">Use Bookmarks</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src544" class="srcSentence">DBPROP_BOOKMARKS</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src545" class="srcSentence">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, see <externalLink><linkText>Jet Provider</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms722791.aspx</linkUri></externalLink> in the OLE DB documentation.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Using RDS with ODBC Connection Pooling"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e8b912c1-da5b-4e85-a000-1e6648a94237
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
# Using RDS with ODBC Connection Pooling
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4c03e5e777bc765e8b2a37519363dbfd" id="tgt1" class="tgtSentence">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load.</caps:sentence>
          <caps:sentence sentenceid="a3929e3c0111edb93f262d46e7df9b99" id="tgt2" class="tgtSentence"> Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="743222246316b7da4dad65d3168fcaa0" id="tgt7" class="tgtSentence">To enable connection pooling, refer to the Internet Information Services documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a17617e2cdb6024a994f672729c26d04" id="tgt8" class="tgtSentence">Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8161cb7751acdbf657fe00a397c390d8" id="tgt9" class="tgtSentence">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3a1f8941e36ca15b65e4b9f868f17327" id="tgt10" class="tgtSentence">To do this, you need to: </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="7472a61f657a2340043ad3143d0bb083" id="tgt11" class="tgtSentence">Configure the SQL Server computer to use TCP/IP Sockets.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="eef24d996a58ac37bfdb166aafad8a73" id="tgt12" class="tgtSentence">Configure the Web server to use TCP/IP Sockets.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="8cf2730eb26e9f6615d6e110f209e0e5" id="tgt13" class="tgtSentence">Configuring the SQL Server Computer to Use TCP/IP Sockets</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="3622ccdcfdfb5f6518773e19a5e251fe" id="tgt14" class="tgtSentence">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="2f59d3b58c45846fd18ac9723e8ef0a3" id="tgt15" class="tgtSentence">To specify the TCP/IP Socket network library on the SQL Server computer</caps:sentence>
            </title>
            <content></content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="66dbaed0de60a32c6108e1b0417b21c2" id="tgt16" class="tgtSentence">In Microsoft SQL Server 6.5:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0a89b62f575645bf1ecdf89f0a745ae2" id="tgt17" class="tgtSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 6.5, and then click SQL Setup.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="544ef359878e2214d7d62ae6398984ab" id="tgt18" class="tgtSentence">Click Continue twice.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cb6e5a7d3f473c28ebcfc8ec46a0ff84" id="tgt19" class="tgtSentence">In the Microsoft SQL Server —Options dialog box, select Change Network Support, and then click Continue.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2aa1db2581930d2db78e204f1769aff1" id="tgt20" class="tgtSentence">Make sure the TCP/IP Sockets check box is selected, and click OK.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="efe855bff47e6b007540594fd1f07924" id="tgt21" class="tgtSentence">Click Continue to finish, and exit setup.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="afbee553bbbf8e1e874e6ed66d1e2890" id="tgt22" class="tgtSentence">In Microsoft SQL Server 7.0:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ae3e8813121363b3c4dda081e22926ec" id="tgt23" class="tgtSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 7.0, and then click Server Network Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5ebcc99c1f7019f6abee1eb61d38ad46" id="tgt24" class="tgtSentence">On the General tab of the dialog box, click Add.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="02146dde8932f971edb88f0b59cc0365" id="tgt25" class="tgtSentence">In the Add Network Library Configuration dialog box, click TCP/IP.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3220fded4f80b343af283a3318db87aa" id="tgt26" class="tgtSentence">In the Port number and Proxy address boxes, enter the port number and proxy address provided by your network administrator.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cea12d54b93f3835a90c0bba1e1ed802" id="tgt27" class="tgtSentence">Click OK to finish, and exit setup.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0befbde72baca1b601bd07fcede668fa" id="tgt28" class="tgtSentence">Configuring the Web Server to Use TCP/IP Sockets</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="44d5f2bf712d848deb2c2539bed764db" id="tgt29" class="tgtSentence">There are two options for configuring the Web server to use TCP/IP Sockets.</caps:sentence>
            <caps:sentence sentenceid="2521162effea6e8d91a3a6bd5591aaeb" id="tgt30" class="tgtSentence"> What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="75f0e5debf64630dd9ff3cf4f32e0343" id="tgt31" class="tgtSentence">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</caps:sentence>
            <caps:sentence sentenceid="c6185465abcf484d8a63a4c12b569850" id="tgt32" class="tgtSentence"> The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="4c787f02c6992e41b87fae5637848ca2" id="tgt33" class="tgtSentence">To configure the Web server (all SQL Servers)</caps:sentence>
            </title>
            <content></content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="ddd5a5f8e926c2051e09da2fa0531efb" id="tgt34" class="tgtSentence">For Microsoft SQL Server 6.5:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="24ca421c2a5b4ed93baf922c9a7474db" id="tgt35" class="tgtSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 6.5 , and then click SQL Client Configuration Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6895777b70b7032740a4622bd6553019" id="tgt36" class="tgtSentence">Click the Net Library tab.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="01810c3a19e1089b9ca73f02409196c8" id="tgt37" class="tgtSentence">In the Default Network box, select TCP/IP Sockets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="65c2377ba31064ddbdcd42a3c8c5362d" id="tgt38" class="tgtSentence">Click Done to save changes and exit the utility.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="85761596e372135d319eb986f8c0d74c" id="tgt39" class="tgtSentence">For Microsoft SQL Server 7.0:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e83138c9b9e9acdf548342d241298a3b" id="tgt40" class="tgtSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 7.0 , and then click Client Network Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="74ab1e739c78baa8b29fa0c2cac513b1" id="tgt41" class="tgtSentence">Click the General tab.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="25ae410dffe0c7a66f632fc355fda93c" id="tgt42" class="tgtSentence">In the Default network library box, click TCP/IP.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f6c40d5fd72dbcdeea85a8577061d2f7" id="tgt43" class="tgtSentence">Click OK to save changes and exit the utility.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="838acbc62d4f5401bb4500e72a8a263e" id="tgt44" class="tgtSentence">If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</caps:sentence>
                <caps:sentence sentenceid="f9a981f88b42f70921802cb53c7a12ee" id="tgt45" class="tgtSentence"> To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="a34d1e275fa4465db3e18449730e89c3" id="tgt46" class="tgtSentence">To configure the Web server (a specific SQL Server)</caps:sentence>
            </title>
            <content></content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="ddd5a5f8e926c2051e09da2fa0531efb" id="tgt47" class="tgtSentence">For Microsoft SQL Server 6.5:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="786a7841561ca8f872975da101ecd0a3" id="tgt48" class="tgtSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 6.5, and then click SQL Client Configuration Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="773fb947fad59bb6159e7c720a7b7c43" id="tgt49" class="tgtSentence">Click the Advanced tab.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="dff582f3cfa450d71a54c413924cbba5" id="tgt50" class="tgtSentence">In the Server box, type the name of the server to connect to using TCP/IP Sockets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d61ba7afe480974ccd4396a3b6a85d9e" id="tgt51" class="tgtSentence">In the DLL Name box, select TCP/IP Sockets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="35531baae1e80d0008a2c177759ffd5d" id="tgt52" class="tgtSentence">Click Add/Modify.</caps:sentence>
                    <caps:sentence sentenceid="369ad06548b4bb0a09aef04096506491" id="tgt53" class="tgtSentence"> All data sources pointing to this server will now use TCP/IP Sockets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="539822edd1c06156bfec0579d0be6aaa" id="tgt54" class="tgtSentence">Click Done.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="85761596e372135d319eb986f8c0d74c" id="tgt55" class="tgtSentence">For Microsoft SQL Server 7.0:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="46e0b3dafc10964635f351cb5605b127" id="tgt56" class="tgtSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 7.0, and then click Client Configuration Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="74ab1e739c78baa8b29fa0c2cac513b1" id="tgt57" class="tgtSentence">Click the General tab.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4d9b54c82eefaf659904ac3bc922376f" id="tgt58" class="tgtSentence">Click Add.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="dd18a00a7a58a2b2494a6995cb96e2ba" id="tgt59" class="tgtSentence">Enter the alias of the server in the Server alias box.</caps:sentence>
                    <caps:sentence sentenceid="ac92ea5aee39d1d59219d2e1d49d6c3b" id="tgt60" class="tgtSentence"> In the Network libraries box, click TCP/IP.</caps:sentence>
                    <caps:sentence sentenceid="0d8fe38d66e90e7ff4bd8938717054e3" id="tgt61" class="tgtSentence"> In the Computer name box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</caps:sentence>
                    <caps:sentence sentenceid="ca3986b2b49ed3f0ccc8ba3550ba42da" id="tgt62" class="tgtSentence"> In the Port number box, enter the port on which the SQL Server listens.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="544ded95c4eff042b33962b8d0427575" id="tgt63" class="tgtSentence">Click OK, and then OK again to exit the utility.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src7" class="srcSentence">To enable connection pooling, refer to the Internet Information Services documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">To do this, you need to: </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Configure the SQL Server computer to use TCP/IP Sockets.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Configure the Web server to use TCP/IP Sockets.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Configuring the SQL Server Computer to Use TCP/IP Sockets</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src15" class="srcSentence">To specify the TCP/IP Socket network library on the SQL Server computer</caps:sentence>
            </title>
            <content></content>
          </section>
          <section>
            <title>
              <caps:sentence id="src16" class="srcSentence">In Microsoft SQL Server 6.5:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 6.5, and then click SQL Setup.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Click Continue twice.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">In the Microsoft SQL Server —Options dialog box, select Change Network Support, and then click Continue.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Make sure the TCP/IP Sockets check box is selected, and click OK.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Click Continue to finish, and exit setup.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src22" class="srcSentence">In Microsoft SQL Server 7.0:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 7.0, and then click Server Network Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">On the General tab of the dialog box, click Add.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">In the Add Network Library Configuration dialog box, click TCP/IP.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">In the Port number and Proxy address boxes, enter the port number and proxy address provided by your network administrator.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Click OK to finish, and exit setup.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">Configuring the Web Server to Use TCP/IP Sockets</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">There are two options for configuring the Web server to use TCP/IP Sockets.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src31" class="srcSentence">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src33" class="srcSentence">To configure the Web server (all SQL Servers)</caps:sentence>
            </title>
            <content></content>
          </section>
          <section>
            <title>
              <caps:sentence id="src34" class="srcSentence">For Microsoft SQL Server 6.5:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 6.5 , and then click SQL Client Configuration Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Click the Net Library tab.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">In the Default Network box, select TCP/IP Sockets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Click Done to save changes and exit the utility.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src39" class="srcSentence">For Microsoft SQL Server 7.0:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 7.0 , and then click Client Network Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Click the General tab.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">In the Default network library box, click TCP/IP.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Click OK to save changes and exit the utility.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src44" class="srcSentence">If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</caps:sentence>
                <caps:sentence id="src45" class="srcSentence"> To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src46" class="srcSentence">To configure the Web server (a specific SQL Server)</caps:sentence>
            </title>
            <content></content>
          </section>
          <section>
            <title>
              <caps:sentence id="src47" class="srcSentence">For Microsoft SQL Server 6.5:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 6.5, and then click SQL Client Configuration Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Click the Advanced tab.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">In the Server box, type the name of the server to connect to using TCP/IP Sockets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">In the DLL Name box, select TCP/IP Sockets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Click Add/Modify.</caps:sentence>
                    <caps:sentence id="src53" class="srcSentence"> All data sources pointing to this server will now use TCP/IP Sockets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Click Done.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src55" class="srcSentence">For Microsoft SQL Server 7.0:</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">From the Start menu, point to Programs, point to Microsoft SQL Server 7.0, and then click Client Configuration Utility.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Click the General tab.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">Click Add.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Enter the alias of the server in the Server alias box.</caps:sentence>
                    <caps:sentence id="src60" class="srcSentence"> In the Network libraries box, click TCP/IP.</caps:sentence>
                    <caps:sentence id="src61" class="srcSentence"> In the Computer name box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</caps:sentence>
                    <caps:sentence id="src62" class="srcSentence"> In the Port number box, enter the port on which the SQL Server listens.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Click OK, and then OK again to exit the utility.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "SQL Server-Treiber"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a5a9e591-4236-4105-9464-70cd36eeeb51
caps.latest.revision: 11
caps.handback.revision: 7
manager: jhubbard
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
# SQL Server-Treiber
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="e86731e68deaf7f4d03e2d4734865cc6" id="tgt1" class="tgtSentence">SQL Server unterstützt eine Vielzahl von Treibern, die von Clientanwendungen oder Diensten verwendet werden, um Verbindungen herzustellen und Daten abzufragen.</caps:sentence>
          <caps:sentence sentenceid="c0c71800c5dbaed9c638a733f1658e31" id="tgt2" class="tgtSentence">  Nachstehen finden Sie eine Zusammenfassung der verschiedenen Treiber (aktuelle und ältere).</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="d832943dc2afe2c6aca4f08e71e1748d" id="tgt3" class="tgtSentence">Aktuelle SQL-Treiber</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="757a9699a73a11492c7fd6f642b60dbe" id="tgt4" class="tgtSentence">Folgende SQL-Treiber werden aktiv weiterentwickelt.</caps:sentence>
            <caps:sentence sentenceid="17b047438af04a2aa49fbaaa4a92b259" id="tgt5" class="tgtSentence"> Jeder Treiber verfügt über eine Support-Anweisung. Diese finden Sie durch Klicken auf die Links.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="57ff1386625f3de00347b8825535d10c" id="tgt6" class="tgtSentence">ADO.NET</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="dd9e3092c50bdb6beb5c4e4a40979739" id="tgt7" class="tgtSentence">       
							ADO.NET ist eine Standardbibliothek des .Net Framework.</caps:sentence>
                <caps:sentence sentenceid="321debe2ec625f793f642c547c926b19" id="tgt8" class="tgtSentence">  Sie ist eine C#-Implementierung des TDS-Protokolls, das von allen modernen SQL Server-Versionen unterstützt wird.</caps:sentence>
                <caps:sentence sentenceid="b2aa0efec0bc063e3fa6ae792588efc1" id="tgt9" class="tgtSentence"> Dieser Treiber wird von Microsoft entwickelt, getestet und supported.</caps:sentence>
              </para>
              <para>
                <link xlink:href="5e467fce-7237-4678-bafa-a16f32323d0c">Microsoft ADO.NET for SQL Server</link>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="84beffd3a0d49636a58ce6080caa87c7" id="tgt10" class="tgtSentence">JDBC</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f4bc2120ce46b00b3b39317772a168d3" id="tgt11" class="tgtSentence">Der JDBC SQL-Treiber ist eine Java-Implementierung des TDS-Protokolls, das von allen modernen SQL Server-Versionen unterstützt wird.</caps:sentence>
                <caps:sentence sentenceid="9e8eb9d69ad9f3e433f8fe2d1879dd6d" id="tgt12" class="tgtSentence">  Dieser Treiber wird von Microsoft entwickelt, getestet und supported.</caps:sentence>
              </para>
              <para>
                <link xlink:href="baf420ab-c058-4cec-a673-d7cb6397210e">Microsoft JDBC Driver for SQL Server</link>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="ce84a752147653739c63cd1d8c03f927" id="tgt13" class="tgtSentence">ODBC</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cc7a29d418576d8f3209efad5799a06d" id="tgt14" class="tgtSentence">Der ODBC SQL-Treiber ist eine Java-Implementierung des TDS-Protokolls,das von allen modernen SQL Server-Versionen unterstützt wird.</caps:sentence>
                <caps:sentence sentenceid="9e8eb9d69ad9f3e433f8fe2d1879dd6d" id="tgt15" class="tgtSentence">  Dieser Treiber wird von Microsoft entwickelt, getestet und supported.</caps:sentence>
              </para>
              <para>
                <link xlink:href="9f2ae91b-06af-4c9a-9d24-062df7bc4662">Microsoft ODBC Driver for SQL Server</link>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="e1bfd762321e409cee4ac0b6e841963c" id="tgt16" class="tgtSentence">PHP</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ee5b34efc1f5da81a7e69e2bd2d14887" id="tgt17" class="tgtSentence">Der PHP SQL-Treiber benötigt den Microsoft SQL Server ODBC-Treiber zum Verarbeiten der Low-Level-Kommunikation mit SQL Server.</caps:sentence>
                <caps:sentence sentenceid="9e8eb9d69ad9f3e433f8fe2d1879dd6d" id="tgt18" class="tgtSentence">  Dieser Treiber wird von Microsoft entwickelt, getestet und supported.</caps:sentence>
              </para>
              <para>
                <link xlink:href="9e78bbf3-9e9a-426d-99d3-6fa2cb33ff6b">Microsoft Drivers for PHP for SQL Server</link>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="28a3689be95c88dd5e7a37db516ab084" id="tgt19" class="tgtSentence">Node.js</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="185f385b20da17727ef29db363419d85" id="tgt20" class="tgtSentence">Der Node.js SQL-Treiber wird von der Node.js Foundation gehostet und unterstützt, einem Gemeinschaftsprojekt der Linux Foundation.</caps:sentence>
              </para>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="28a3689be95c88dd5e7a37db516ab084" id="tgt21" class="tgtSentence">Node.js</caps:sentence>
                  </linkText>
                  <linkUri>https://nodejs.org</linkUri>
                </externalLink>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="23eeeb4347bdd26bfc6b7ee9a3b755dd" id="tgt22" class="tgtSentence">Python</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e1744a771ff45f71ffad2fd29707f0d6" id="tgt23" class="tgtSentence">Der Python SQL-Treiber wird von der Python Software Foundation gehostet und unterstützt.</caps:sentence>
              </para>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="23eeeb4347bdd26bfc6b7ee9a3b755dd" id="tgt24" class="tgtSentence">Python</caps:sentence>
                  </linkText>
                  <linkUri>https://www.python.org/</linkUri>
                </externalLink>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="58e53d1324eef6265fdb97b08ed9aadf" id="tgt25" class="tgtSentence">Ruby</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="792bc8f62e1cb958e53588e5c4f72be3" id="tgt26" class="tgtSentence">Der Ruby SQL-Treiber wird am folgenden Speicherort gehostet.</caps:sentence>
              </para>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="58e53d1324eef6265fdb97b08ed9aadf" id="tgt27" class="tgtSentence">Ruby</caps:sentence>
                  </linkText>
                  <linkUri>https://www.ruby-lang.org/</linkUri>
                </externalLink>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2eb2c78c94a44412025ebb96d005d567" id="tgt28" class="tgtSentence"> Ältere SQL-Treiber</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="411ee0769b75d8016112a3988823bbc0" id="tgt29" class="tgtSentence">Die folgenden SQL-Treiber wurden von Microsoft entwickelt und getestet, aber werden für neue Entwicklungen nicht empfohlen.</caps:sentence>
            <caps:sentence sentenceid="17b047438af04a2aa49fbaaa4a92b259" id="tgt30" class="tgtSentence"> Jeder Treiber verfügt über eine Support-Anweisung. Diese finden Sie durch Klicken auf die Links.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="d5e036daaa738915e9bbf07b775a9365" id="tgt31" class="tgtSentence">OLEDB</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ec4a521904808fc77295d68b8e64773a" id="tgt32" class="tgtSentence">       
						Der OLE DB-Anbieter wird in den Nachfolgern von SQL Server 2012 nicht mehr enthalten sein.</caps:sentence>
              </para>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence sentenceid="436303ae62d1cbd8e4d7c9d810652edd" id="tgt33" class="tgtSentence">Microsoft OLE DB</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/ms722784.aspx</linkUri>
                </externalLink>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="421359a899e6aeb972c11a26fb52ad15" id="tgt34" class="tgtSentence">ADO</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="8009346f14703621687c9b50b26335a7" id="tgt35" class="tgtSentence">       
						Der ADO SQL-Treiber ist direkt vom OLE DB-Anbieter abhängig.</caps:sentence>
                <caps:sentence sentenceid="6dfb77eec960bbac560504e8247d3e7d" id="tgt36" class="tgtSentence">  Daher wird er in den Nachfolgern von SQL Server 2012 nicht mehr unterstützt.</caps:sentence>
              </para>
              <para>
                <link xlink:href="8e9d52da-342d-46b5-8535-c57f07711db0">ActiveX Data Objects (ADO)</link>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">SQL Server supports a wide variety of drivers, which are used by client applications or services to connect and query for data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence">  Please see below for a summary of the different drivers, both current and legacy.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Current SQL Drivers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The following SQL Drivers are actively developed.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Each driver has a support statement that can be found by following the links.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src6" class="srcSentence">ADO.NET</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src7" class="srcSentence">       
							ADO.NET is a library that is a standard part of the .Net framework.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence">  It is a C# implementation of the TDS protocol, which is supported by all modern versions of SQL Server.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> This driver is developed, tested, and supported by Microsoft.</caps:sentence>
              </para>
              <para>
                <link xlink:href="5e467fce-7237-4678-bafa-a16f32323d0c">Microsoft ADO.NET for SQL Server</link>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src10" class="srcSentence">JDBC</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src11" class="srcSentence">The JDBC SQL driver is a Java implementation of the TDS protocol, which is supported by all modern versions of SQL Server.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence">  This driver is developed, tested, and supported by Microsoft.</caps:sentence>
              </para>
              <para>
                <link xlink:href="baf420ab-c058-4cec-a673-d7cb6397210e">Microsoft JDBC Driver for SQL Server</link>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src13" class="srcSentence">ODBC</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src14" class="srcSentence">The ODBC SQL driver is a C++ implementation of the TDS protocol, which is supported by all modern versions of SQL Server.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence">  This driver is developed, tested, and supported by Microsoft.</caps:sentence>
              </para>
              <para>
                <link xlink:href="9f2ae91b-06af-4c9a-9d24-062df7bc4662">Microsoft ODBC Driver for SQL Server</link>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src16" class="srcSentence">PHP</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src17" class="srcSentence">The PHP SQL driver relies on the Microsoft SQL Server ODBC Driver to handle the low-level communication with SQL Server.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence">  This driver is developed, tested, and supported by Microsoft.</caps:sentence>
              </para>
              <para>
                <link xlink:href="9e78bbf3-9e9a-426d-99d3-6fa2cb33ff6b">Microsoft Drivers for PHP for SQL Server</link>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src19" class="srcSentence">Node.js</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src20" class="srcSentence">The Node.js SQL driver is hosted and supported by the Node.js Foundation, a collaborative project at the Linux Foundation.</caps:sentence>
              </para>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src21" class="srcSentence">Node.js</caps:sentence>
                  </linkText>
                  <linkUri>https://nodejs.org</linkUri>
                </externalLink>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src22" class="srcSentence">Python</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src23" class="srcSentence">The Python SQL driver is hosted and supported by the Python Software Foundation.</caps:sentence>
              </para>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src24" class="srcSentence">Python</caps:sentence>
                  </linkText>
                  <linkUri>https://www.python.org/</linkUri>
                </externalLink>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src25" class="srcSentence">Ruby</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src26" class="srcSentence">The Ruby SQL driver is hosted at the following location.</caps:sentence>
              </para>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src27" class="srcSentence">Ruby</caps:sentence>
                  </linkText>
                  <linkUri>https://www.ruby-lang.org/</linkUri>
                </externalLink>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence"> Legacy SQL Drivers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">The following SQL Drivers were developed and tested by Microsoft, but are not recommended to be used for new development.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> Each driver has a support statement that can be found by following the links.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src31" class="srcSentence">OLEDB</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src32" class="srcSentence">       
						The OLE DB provider will not be included after SQL Server 2012.</caps:sentence>
              </para>
              <para>
                <externalLink>
                  <linkText>
                    <caps:sentence id="src33" class="srcSentence">Microsoft OLE DB</caps:sentence>
                  </linkText>
                  <linkUri>https://msdn.microsoft.com/library/ms722784.aspx</linkUri>
                </externalLink>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src34" class="srcSentence">ADO</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src35" class="srcSentence">       
						The ADO SQL driver has a direct dependency on the OLE DB provider.</caps:sentence>
                <caps:sentence id="src36" class="srcSentence">  As such, it will not be supported after SQL Server 2012.</caps:sentence>
              </para>
              <para>
                <link xlink:href="8e9d52da-342d-46b5-8535-c57f07711db0">ActiveX Data Objects (ADO)</link>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
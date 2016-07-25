---
title: "Using ADO with Scripting Languages"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76fc4d00-0c9f-422b-af5c-af6ed8fb29d8
caps.latest.revision: 11
caps.handback.revision: 11
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
# Using ADO with Scripting Languages
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ac5bd4a992e366f608ac7d29b2a96397" id="tgt1" class="tgtSentence">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</caps:sentence>
          <caps:sentence sentenceid="a4efef274c51658a4c8dd2090c94afbf" id="tgt2" class="tgtSentence"> In this scenario, ADO, the underlying OLE DB provider that it uses, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</caps:sentence>
          <caps:sentence sentenceid="ccbdb40d9d302cb2fd02d50ee0f6ef1f" id="tgt3" class="tgtSentence"> Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</caps:sentence>
          <caps:sentence sentenceid="37d5a1e02c7f46e159d1d2521cb19b6a" id="tgt4" class="tgtSentence"> This HTML content can be passed via HTTP to a client Web browser.</caps:sentence>
          <caps:sentence sentenceid="8b3baf2f849970d9ce6bc7532b7853e2" id="tgt5" class="tgtSentence"> By using scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5410a0745826ad2653de0766f7a6cc6e" id="tgt6" class="tgtSentence">Before you use an ActiveX object in a Web page, it is important to know whether the object is safe for scripting.</caps:sentence>
          <caps:sentence sentenceid="ab44a7224755633253c0ea5370ab270e" id="tgt7" class="tgtSentence"> When an object is considered safe for scripting, it means that the control cannot take any harmful action on the user's computer and therefore can be executed without requesting the user's approval.</caps:sentence>
          <caps:sentence sentenceid="3df6a140765fd08661b0161988d65ac2" id="tgt8" class="tgtSentence"> The following table lists the ADO objects and indicates whether they are safe for scripting.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a8cfde6331bd59eb2ac96f8911c4b666" id="tgt9" class="tgtSentence">Object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cb2a3f271e3236c40504684eda987d6c" id="tgt10" class="tgtSentence">Safe for Scripting?</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="75e8df85551ea3732d306a02951f51e1" id="tgt11" class="tgtSentence">ADO Connection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt12" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="bdb9815dc1ea0a8d3289a47f5ea5195d" id="tgt13" class="tgtSentence">ADO Command</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt14" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a286c4ee5e3765b1f58b386c5d6f7089" id="tgt15" class="tgtSentence">ADO Parameter</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt16" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3fdc2f8d60d4afbb8bcd2ce0470ffa35" id="tgt17" class="tgtSentence">ADO Recordset</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt18" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="62e983930abb09e46209d56a330011e7" id="tgt19" class="tgtSentence">ADO Record</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt20" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8d5cc1fe6344156dba60359301c1b317" id="tgt21" class="tgtSentence">ADO Stream</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt22" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0e645c38e729f971c98a786eccda8d28" id="tgt23" class="tgtSentence">ADO Error</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt24" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6c3ce3046a12f1e35d99b81ae93a86bb" id="tgt25" class="tgtSentence">ADOX Catalog</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt26" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="785b47a7623461bde7a81dd99e473cb8" id="tgt27" class="tgtSentence">ADOX CellSet</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt28" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d835ae238dde4e3e16da9a1d7d1269d9" id="tgt29" class="tgtSentence">RDS DataControl</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt30" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="42bdb6a14c91430948172535c6f337b1" id="tgt31" class="tgtSentence">RDS DataSpace</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt32" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ff6002bbb136495086e3620a9e635fbf" id="tgt33" class="tgtSentence">RDS DataFactory</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt34" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="b2ef68de4937e39561dc7c54b9311635" id="tgt35" class="tgtSentence">The following table lists the providers included with Windows DAC/MDAC, and indicates whether they are safe for scripting.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9e9f3d70bd8c8957627eada96d967706" id="tgt36" class="tgtSentence">Provider</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cb2a3f271e3236c40504684eda987d6c" id="tgt37" class="tgtSentence">Safe for Scripting?</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8c73a98a300905900337f535531dfca6" id="tgt38" class="tgtSentence">Shape</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt39" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="5ca4b722707013b233e526659583df95" id="tgt40" class="tgtSentence">Persist</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt41" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2c18e486683a3db1e645ad8523223b72" id="tgt42" class="tgtSentence">Remote</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt43" class="tgtSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="babee36d5c4377fe655c76afc44612bc" id="tgt44" class="tgtSentence">OLE DB Provider for SQL Server (SQLOLEDB)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt45" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8dd956f37e72576068810e9269c3a633" id="tgt46" class="tgtSentence">OLE DB Provider for ODBC (MSDASQL)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt47" class="tgtSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="2bc3d2cd7848bf9d36d8bb3aafebf914" id="tgt48" class="tgtSentence">ODBC Data Sources</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b1c15444860a78ba8ff864f55bafdcbf" id="tgt49" class="tgtSentence">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used.</caps:sentence>
            <caps:sentence sentenceid="3f647f7623387890f4cb66ea890a72c6" id="tgt50" class="tgtSentence"> For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator.</caps:sentence>
            <caps:sentence sentenceid="1ba2f0f93a4416e06b632c149992dd2d" id="tgt51" class="tgtSentence"> For scripts that are running under IIS, you must create a System DSN; otherwise your scripts will not recognize the data source you created.</caps:sentence>
            <caps:sentence sentenceid="ef6425070e432d604094bcb42e5371fa" id="tgt52" class="tgtSentence"> This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2b467330ef7e831da2e6c776f98ba250" id="tgt53" class="tgtSentence">Referencing the ADO Library</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7195ba82f7af9c562a838b0c560b78ff" id="tgt54" class="tgtSentence">Not applicable with scripting languages.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="aa3ecfd7bf94dd3cc62f2d8ff235c31f" id="tgt55" class="tgtSentence">Handling events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7195ba82f7af9c562a838b0c560b78ff" id="tgt56" class="tgtSentence">Not applicable with scripting languages.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2434abc8699cab1975d81c958d0e11be" id="tgt57" class="tgtSentence">The following topics contain more specific information about using ADO with scripting languages:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="ada4a40ea70b89e9958ba1eafbea83be" id="tgt58" class="tgtSentence">             <legacyLink xlink:href="6aaaf6d0-1376-4473-bea6-b81f2645a9ac">VBScript ADO Programming</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c8a07f755a74307c6c21c13ed93dc85e" id="tgt59" class="tgtSentence">             <legacyLink xlink:href="62273658-0fe7-4aac-b4d8-f725e6baf043">JScript ADO Programming</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="9dfb6784-037d-4f9d-bb7f-b506b4498573">Using ADO with Microsoft Visual Basic</link>
        <link xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">Using ADO with Microsoft Visual C++</link>
        <link xlink:href="15542c35-3bf7-4d5f-a3b2-3a5cff286987">Using ADO with Microsoft Visual J++</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> In this scenario, ADO, the underlying OLE DB provider that it uses, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> This HTML content can be passed via HTTP to a client Web browser.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> By using scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">Before you use an ActiveX object in a Web page, it is important to know whether the object is safe for scripting.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> When an object is considered safe for scripting, it means that the control cannot take any harmful action on the user's computer and therefore can be executed without requesting the user's approval.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The following table lists the ADO objects and indicates whether they are safe for scripting.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Object</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Safe for Scripting?</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">ADO Connection</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">ADO Command</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">ADO Parameter</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">ADO Recordset</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">ADO Record</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">ADO Stream</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">ADO Error</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">ADOX Catalog</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">ADOX CellSet</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">RDS DataControl</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">RDS DataSpace</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">RDS DataFactory</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src35" class="srcSentence">The following table lists the providers included with Windows DAC/MDAC, and indicates whether they are safe for scripting.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">Provider</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Safe for Scripting?</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">Shape</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">Persist</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">Remote</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">Yes</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src44" class="srcSentence">OLE DB Provider for SQL Server (SQLOLEDB)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">OLE DB Provider for ODBC (MSDASQL)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">No</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src48" class="srcSentence">ODBC Data Sources</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src49" class="srcSentence">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used.</caps:sentence>
            <caps:sentence id="src50" class="srcSentence"> For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator.</caps:sentence>
            <caps:sentence id="src51" class="srcSentence"> For scripts that are running under IIS, you must create a System DSN; otherwise your scripts will not recognize the data source you created.</caps:sentence>
            <caps:sentence id="src52" class="srcSentence"> This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src53" class="srcSentence">Referencing the ADO Library</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src54" class="srcSentence">Not applicable with scripting languages.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src55" class="srcSentence">Handling events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src56" class="srcSentence">Not applicable with scripting languages.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src57" class="srcSentence">The following topics contain more specific information about using ADO with scripting languages:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src58" class="srcSentence">             <legacyLink xlink:href="6aaaf6d0-1376-4473-bea6-b81f2645a9ac">VBScript ADO Programming</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src59" class="srcSentence">             <legacyLink xlink:href="62273658-0fe7-4aac-b4d8-f725e6baf043">JScript ADO Programming</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="9dfb6784-037d-4f9d-bb7f-b506b4498573">Using ADO with Microsoft Visual Basic</link>
        <link xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">Using ADO with Microsoft Visual C++</link>
        <link xlink:href="15542c35-3bf7-4d5f-a3b2-3a5cff286987">Using ADO with Microsoft Visual J++</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
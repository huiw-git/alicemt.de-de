---
title: "ADO History"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 667673f2-3151-432b-894a-3fc60b704ea4
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
# ADO History
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9363126f2d03927a0b54a37c0c80ec37" id="tgt1" class="tgtSentence">This topic lists the new features introduced by each release of ADO, ADO MD, and ADOX.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="95d74b1a3f013bb42d11c0ee81c9d692" id="tgt2" class="tgtSentence">ADO 6.0</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="79161bea87d6b279bb077bd9506e5a7f" id="tgt3" class="tgtSentence">ADO 6.0 is included in Windows Vista, as a part of the Windows Data Access Components (Windows DAC) 6.0.</caps:sentence>
            <caps:sentence sentenceid="13307a3647995aceaf64fe4df2e7fee5" id="tgt4" class="tgtSentence"> ADO 6.0 is functionally equivalent to ADO 2.8.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="7d87aa27dcccb3023302989f5fefe74f" id="tgt5" class="tgtSentence">ADO 2.8</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a740c2279e82de69838aa1e95b4f6c42" id="tgt6" class="tgtSentence">ADO 2.8 was included in Windows XP and Windows Server 2003, as part of the Microsoft Data Access Components (MDAC) 2.8.</caps:sentence>
            <caps:sentence sentenceid="12049751025754d06047ba343b913bc2" id="tgt7" class="tgtSentence"> A redistributable version of MDAC 2.8 is also available; note that this redistributable version should only be installed on Windows 2000.</caps:sentence>
            <caps:sentence sentenceid="19f66d70c99d0fdee8e0ec2ae366981d" id="tgt8" class="tgtSentence"> ADO 2.8 addresses several security-related concerns:</caps:sentence>
          </para>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d84cd0691ba5174c4e07a0d25463d5f0" id="tgt9" class="tgtSentence"> <legacyItalic>Hard drive access is not allowed outside a trusted zone.</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="644b26bb54302de0c0e0399cbe79d888" id="tgt10" class="tgtSentence">In cross-domain scripting involving nontrusted sites, the following operations are disabled: <legacyBold>Stream.SaveToFile</legacyBold>, <legacyBold>Stream.LoadFromFile</legacyBold>, <legacyBold>Recordset.Save</legacyBold>, and <legacyBold>Recordset.Open</legacyBold>, used in conjunction with the <legacyBold>adCmdFile</legacyBold> flag or with the Microsoft OLE DB Persistence Provider (MSPersist).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="614b17bf4511d76db45303af326b9c8c" id="tgt11" class="tgtSentence">
                <legacyBold>Recordset.Open</legacyBold>
                <legacyItalic>, </legacyItalic>
                <legacyBold>Recordset.Save</legacyBold>
                <legacyItalic>, </legacyItalic>
                <legacyBold>Stream.SaveToFile</legacyBold>
                <legacyItalic>, and </legacyItalic>
                <legacyBold>Stream.LoadFromFile</legacyBold>
                <legacyItalic> operate on physical files only.</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="fe420a88a65503a5ff6836230de02cbd" id="tgt12" class="tgtSentence">These methods now verify that file handles point to physical files only.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="38a697b08dadee42bebfb275a5662d96" id="tgt13" class="tgtSentence">
                <legacyBold>Recordset.ActiveCommand</legacyBold>
                <legacyItalic> returns an error when invoked from an HTML/ASP page.</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="352360a4abdde2425438a281340367a1" id="tgt14" class="tgtSentence">This prevents the <legacyBold>Command</legacyBold> object from being misused.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="7b75213b41d869a6e6ac48caf5039b2a" id="tgt15" class="tgtSentence"> <legacyItalic>The number of </legacyItalic><legacyBold>Recordsets</legacyBold><legacyItalic> returned by a nested </legacyItalic><legacyBold>Shape</legacyBold><legacyItalic> command has an upper bound.</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="83af3d55bc71a32d0902a9e74d962d2d" id="tgt16" class="tgtSentence">A nested shape command now returns a maximum of 512 <legacyBold>Recordsets</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="0c498cf554bb738262edab330bea66fa" id="tgt17" class="tgtSentence"> This means that a <legacyBold>Shape</legacyBold> command can no longer be nested at any depth.</caps:sentence>
                <caps:sentence sentenceid="18df030c1dcb700b28eaa7dfd7f184bd" id="tgt18" class="tgtSentence"> Instead, the maximum level depth is 512, if each command results in a single (child) <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="b8dfeba33e41e54d2ad4823c03f120ea" id="tgt19" class="tgtSentence"> If, at any level, a <legacyBold>Shape</legacyBold> command returns multiple <legacyBold>Recordsets</legacyBold>, the maximum level of depth will be less than 512.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ec4422a7755dae6b680fab9b25c02f40" id="tgt20" class="tgtSentence">ADO 2.7</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="baab6b8477af8912e364a39e9175c9a9" id="tgt21" class="tgtSentence"> <legacyItalic>64-bit platform support</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e356bfd5a569f05eeadb3c7f4dc72a12" id="tgt22" class="tgtSentence">ADO 2.7 introduces support for 64-bit processors.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="89e77e031c72187cbca8b35448e4cc53" id="tgt23" class="tgtSentence">ADO 2.6</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="39bef2b34d554f0335b85711181d9e41" id="tgt24" class="tgtSentence">
                <legacyBold>CubDef.GetSchemaObject</legacyBold>
                <legacyItalic> Method</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="8703ea5a05b241ee614d62dcf474c970" id="tgt25" class="tgtSentence">Starting with ADO 2.6, ADO MD objects can be retrieved using unique names, as specified by the <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName property (ADO MD)</legacyLink>.</caps:sentence>
                <caps:sentence sentenceid="322413018f46d3d01cbfcf918b9b2cca" id="tgt26" class="tgtSentence"> The names of parent objects do not need to be known, and parent collections do not need to be populated to retrieve a schema object.</caps:sentence>
                <caps:sentence sentenceid="ec8695ede3480ac39e6317275ad57ae3" id="tgt27" class="tgtSentence"> See <legacyLink xlink:href="36b754b4-6b17-4dd1-a925-bca46938b7c4">GetSchemaObject method (ADO MD)</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="69fe6215dc2aa031239a7eb20ecdbf38" id="tgt28" class="tgtSentence"> <legacyItalic>Command streams</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="819a858098450a62fbd07ae0b84c5efe" id="tgt29" class="tgtSentence">The <legacyBold>Command</legacyBold> object supports commands in stream format as an alternative to using the <legacyBold>CommandText</legacyBold> property.</caps:sentence>
                <caps:sentence sentenceid="b8a37ce527be896ba8e09fa0ebe57e68" id="tgt30" class="tgtSentence"> The <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream property (ADO)</legacyLink> can be used to specify XML Templates or updategrams as the <legacyBold>Command</legacyBold> input with the Microsoft OLE DB Provider for SQL Server.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="6c95ba4688562028957e114ce241cd82" id="tgt31" class="tgtSentence">
                <legacyBold>Dialect</legacyBold>
                <legacyItalic> property</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="85392d69b4505b4d5deebcf23f409510" id="tgt32" class="tgtSentence">
                  <legacyLink xlink:href="329c3a71-ba88-4009-b04f-2f52195a5957">Dialect</legacyLink> is a new property that defines the syntax and general rules that the provider uses to parse the string or stream.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="1e2dc6ebb33e5bb8ab69446b78ed92fb" id="tgt33" class="tgtSentence">
                <legacyBold>Command.Execute</legacyBold>
                <legacyItalic> method</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="20ff1aabdb87ed0c2fd64d4547299723" id="tgt34" class="tgtSentence">The <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute method</legacyLink> of the ADO <legacyBold>Command</legacyBold> object has been enhanced to use streams for input and output.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="1fbe38bead601d9b3ac1710b55b08df9" id="tgt35" class="tgtSentence"> <legacyItalic>Field statusvalues</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0211e425ecb0199fc0be7ce1ff8404a5" id="tgt36" class="tgtSentence">If the user encounters a DB_E_ERRORSOCCURRED error when modifying a <legacyBold>Field</legacyBold> of a <legacyBold>Recordset</legacyBold>, ADO will now fill the <legacyBold>Field.Status</legacyBold> property with the appropriate status information so that the user will have more information about what went wrong.</caps:sentence>
                <caps:sentence sentenceid="0d7d8074e683d81702550bd82f3e9e8c" id="tgt37" class="tgtSentence"> See <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status Property (ADO Field)</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="0094ff4463219c4687ccda6443a8c456" id="tgt38" class="tgtSentence">
                <legacyBold>NamedParameters</legacyBold>
                <legacyItalic> property</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="183bda7f77bfcabce5724dae2057464c" id="tgt39" class="tgtSentence">
                  <legacyLink xlink:href="42409387-026c-435f-a9b1-bf4167095875">NamedParameters</legacyLink> is a new property of the <legacyBold>Command</legacyBold> object that indicates that the provider should use named parameters.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a81f0584a8a28d1dc1567baa1d138b1d" id="tgt40" class="tgtSentence"> <legacyItalic>Resultsets in streams</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="1c83b43b376e5aedc4173c21c188e3d9" id="tgt41" class="tgtSentence">ADO can return resultsets from a data source in a <legacyBold>Stream</legacyBold>, rather than a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="48cda8f3aa2cd7e157d43e00b581b2be" id="tgt42" class="tgtSentence"> Using the latest version of the Microsoft OLE DB Provider for SQL Server, you can get XML results from the provider by executing a "For XML" query.</caps:sentence>
                <caps:sentence sentenceid="04203a62ee80427edb76fcdd935ac4a0" id="tgt43" class="tgtSentence"> A <legacyBold>Stream </legacyBold>that receives the resultset can be opened with a "For XML" command as the source.</caps:sentence>
                <caps:sentence sentenceid="bb01208f0643ca9e36230fc4ce2ae161" id="tgt44" class="tgtSentence"> See <legacyLink xlink:href="996c1321-c926-4f57-8297-85c8c20de974">Retrieving Resultsets into Streams</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8a41b602d5a508924d5d1fcd6accdf27" id="tgt45" class="tgtSentence"> <legacyItalic>Single row resultset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="aa7a021931fc8a941d03e999533fdc56" id="tgt46" class="tgtSentence">The ADO <legacyBold>Record</legacyBold> object can now be opened on a command string or <legacyBold>Command</legacyBold> object that returns one row of data from the provider.</caps:sentence>
                <caps:sentence sentenceid="a2acd381d7e09e0943dd6f90e2e75c86" id="tgt47" class="tgtSentence"> This results in improved performance with MDAC 2.6 providers.</caps:sentence>
                <caps:sentence sentenceid="b8e5bea3be2143c68f98561bc8c38d5e" id="tgt48" class="tgtSentence"> See <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</legacyLink>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="7f2473d2b2e9682340e252bfa77fa3ea" id="tgt49" class="tgtSentence">ADO 2.5</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="fc2a54207fc17897a1e3b60f880828df" id="tgt50" class="tgtSentence"> <legacyBold>Record</legacyBold> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="6c437f9ee683c65652970b3839d93d38" id="tgt51" class="tgtSentence">ADO 2.5 introduces the <legacyBold>Record</legacyBold> object to represent and manage a row from a <legacyBold>Recordset</legacyBold> or a data provider, or an object encapsulating a semi-structured data, such as a file or directory.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="eca5c51f42384dcae3d0b95d5c9e0e15" id="tgt52" class="tgtSentence"> <legacyBold>Stream</legacyBold> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e4f8959484ce0a3d140e13008da8aa6a" id="tgt53" class="tgtSentence">ADO 2.5 also introduces the <legacyBold>Stream</legacyBold> object to represent a stream of binary or text data.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="b2242a69b43a180ea86590469b907853" id="tgt54" class="tgtSentence"> <legacyItalic>URL binding</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="915df833cb743bc3f92b76c3f4504b6b" id="tgt55" class="tgtSentence">ADO 2.5 introduces the use of a URL, as an alternative to a connection string and command text, to name data store objects.</caps:sentence>
                <caps:sentence sentenceid="e1530f2c48667020b29e84ee811a3e9e" id="tgt56" class="tgtSentence"> A URL can be used with the existing <legacyBold>Connection</legacyBold> and <legacyBold>Recordset</legacyBold> objects, as well as with the new <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="76268455d6fe3cf41ebb329a2021f8bd" id="tgt57" class="tgtSentence"> <legacyItalic>Data providers supporting URL binding</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b946a5a8d001627f5a522cea6c414dd6" id="tgt58" class="tgtSentence">ADO 2.5 supports OLE DB providers that recognize the URL schemes.</caps:sentence>
                <caps:sentence sentenceid="224b0f85533414bb82713668c84e0d2f" id="tgt59" class="tgtSentence"> This includes OLE DB Provider for Internet Publishing, which accesses the Windows 2000 file system and recognizes the existing HTTP scheme.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This topic lists the new features introduced by each release of ADO, ADO MD, and ADOX.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">ADO 6.0</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">ADO 6.0 is included in Windows Vista, as a part of the Windows Data Access Components (Windows DAC) 6.0.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> ADO 6.0 is functionally equivalent to ADO 2.8.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">ADO 2.8</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">ADO 2.8 was included in Windows XP and Windows Server 2003, as part of the Microsoft Data Access Components (MDAC) 2.8.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> A redistributable version of MDAC 2.8 is also available; note that this redistributable version should only be installed on Windows 2000.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> ADO 2.8 addresses several security-related concerns:</caps:sentence>
          </para>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>Hard drive access is not allowed outside a trusted zone.</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">In cross-domain scripting involving nontrusted sites, the following operations are disabled: <legacyBold>Stream.SaveToFile</legacyBold>, <legacyBold>Stream.LoadFromFile</legacyBold>, <legacyBold>Recordset.Save</legacyBold>, and <legacyBold>Recordset.Open</legacyBold>, used in conjunction with the <legacyBold>adCmdFile</legacyBold> flag or with the Microsoft OLE DB Persistence Provider (MSPersist).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src11" class="srcSentence">
                <legacyBold>Recordset.Open</legacyBold>
                <legacyItalic>, </legacyItalic>
                <legacyBold>Recordset.Save</legacyBold>
                <legacyItalic>, </legacyItalic>
                <legacyBold>Stream.SaveToFile</legacyBold>
                <legacyItalic>, and </legacyItalic>
                <legacyBold>Stream.LoadFromFile</legacyBold>
                <legacyItalic> operate on physical files only.</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src12" class="srcSentence">These methods now verify that file handles point to physical files only.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src13" class="srcSentence">
                <legacyBold>Recordset.ActiveCommand</legacyBold>
                <legacyItalic> returns an error when invoked from an HTML/ASP page.</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src14" class="srcSentence">This prevents the <legacyBold>Command</legacyBold> object from being misused.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src15" class="srcSentence"> <legacyItalic>The number of </legacyItalic><legacyBold>Recordsets</legacyBold><legacyItalic> returned by a nested </legacyItalic><legacyBold>Shape</legacyBold><legacyItalic> command has an upper bound.</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src16" class="srcSentence">A nested shape command now returns a maximum of 512 <legacyBold>Recordsets</legacyBold>.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> This means that a <legacyBold>Shape</legacyBold> command can no longer be nested at any depth.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> Instead, the maximum level depth is 512, if each command results in a single (child) <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> If, at any level, a <legacyBold>Shape</legacyBold> command returns multiple <legacyBold>Recordsets</legacyBold>, the maximum level of depth will be less than 512.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">ADO 2.7</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src21" class="srcSentence"> <legacyItalic>64-bit platform support</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src22" class="srcSentence">ADO 2.7 introduces support for 64-bit processors.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">ADO 2.6</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src24" class="srcSentence">
                <legacyBold>CubDef.GetSchemaObject</legacyBold>
                <legacyItalic> Method</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src25" class="srcSentence">Starting with ADO 2.6, ADO MD objects can be retrieved using unique names, as specified by the <legacyLink xlink:href="5b977956-e252-4861-8425-f1aaf6b80130">UniqueName property (ADO MD)</legacyLink>.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> The names of parent objects do not need to be known, and parent collections do not need to be populated to retrieve a schema object.</caps:sentence>
                <caps:sentence id="src27" class="srcSentence"> See <legacyLink xlink:href="36b754b4-6b17-4dd1-a925-bca46938b7c4">GetSchemaObject method (ADO MD)</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src28" class="srcSentence"> <legacyItalic>Command streams</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src29" class="srcSentence">The <legacyBold>Command</legacyBold> object supports commands in stream format as an alternative to using the <legacyBold>CommandText</legacyBold> property.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> The <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStream property (ADO)</legacyLink> can be used to specify XML Templates or updategrams as the <legacyBold>Command</legacyBold> input with the Microsoft OLE DB Provider for SQL Server.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src31" class="srcSentence">
                <legacyBold>Dialect</legacyBold>
                <legacyItalic> property</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src32" class="srcSentence">
                  <legacyLink xlink:href="329c3a71-ba88-4009-b04f-2f52195a5957">Dialect</legacyLink> is a new property that defines the syntax and general rules that the provider uses to parse the string or stream.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src33" class="srcSentence">
                <legacyBold>Command.Execute</legacyBold>
                <legacyItalic> method</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src34" class="srcSentence">The <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute method</legacyLink> of the ADO <legacyBold>Command</legacyBold> object has been enhanced to use streams for input and output.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src35" class="srcSentence"> <legacyItalic>Field statusvalues</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src36" class="srcSentence">If the user encounters a DB_E_ERRORSOCCURRED error when modifying a <legacyBold>Field</legacyBold> of a <legacyBold>Recordset</legacyBold>, ADO will now fill the <legacyBold>Field.Status</legacyBold> property with the appropriate status information so that the user will have more information about what went wrong.</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> See <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status Property (ADO Field)</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src38" class="srcSentence">
                <legacyBold>NamedParameters</legacyBold>
                <legacyItalic> property</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src39" class="srcSentence">
                  <legacyLink xlink:href="42409387-026c-435f-a9b1-bf4167095875">NamedParameters</legacyLink> is a new property of the <legacyBold>Command</legacyBold> object that indicates that the provider should use named parameters.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src40" class="srcSentence"> <legacyItalic>Resultsets in streams</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src41" class="srcSentence">ADO can return resultsets from a data source in a <legacyBold>Stream</legacyBold>, rather than a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence id="src42" class="srcSentence"> Using the latest version of the Microsoft OLE DB Provider for SQL Server, you can get XML results from the provider by executing a "For XML" query.</caps:sentence>
                <caps:sentence id="src43" class="srcSentence"> A <legacyBold>Stream </legacyBold>that receives the resultset can be opened with a "For XML" command as the source.</caps:sentence>
                <caps:sentence id="src44" class="srcSentence"> See <legacyLink xlink:href="996c1321-c926-4f57-8297-85c8c20de974">Retrieving Resultsets into Streams</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src45" class="srcSentence"> <legacyItalic>Single row resultset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src46" class="srcSentence">The ADO <legacyBold>Record</legacyBold> object can now be opened on a command string or <legacyBold>Command</legacyBold> object that returns one row of data from the provider.</caps:sentence>
                <caps:sentence id="src47" class="srcSentence"> This results in improved performance with MDAC 2.6 providers.</caps:sentence>
                <caps:sentence id="src48" class="srcSentence"> See <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</legacyLink>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src49" class="srcSentence">ADO 2.5</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src50" class="srcSentence"> <legacyBold>Record</legacyBold> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src51" class="srcSentence">ADO 2.5 introduces the <legacyBold>Record</legacyBold> object to represent and manage a row from a <legacyBold>Recordset</legacyBold> or a data provider, or an object encapsulating a semi-structured data, such as a file or directory.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src52" class="srcSentence"> <legacyBold>Stream</legacyBold> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src53" class="srcSentence">ADO 2.5 also introduces the <legacyBold>Stream</legacyBold> object to represent a stream of binary or text data.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src54" class="srcSentence"> <legacyItalic>URL binding</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src55" class="srcSentence">ADO 2.5 introduces the use of a URL, as an alternative to a connection string and command text, to name data store objects.</caps:sentence>
                <caps:sentence id="src56" class="srcSentence"> A URL can be used with the existing <legacyBold>Connection</legacyBold> and <legacyBold>Recordset</legacyBold> objects, as well as with the new <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src57" class="srcSentence"> <legacyItalic>Data providers supporting URL binding</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src58" class="srcSentence">ADO 2.5 supports OLE DB providers that recognize the URL schemes.</caps:sentence>
                <caps:sentence id="src59" class="srcSentence"> This includes OLE DB Provider for Internet Publishing, which accesses the Windows 2000 file system and recognizes the existing HTTP scheme.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
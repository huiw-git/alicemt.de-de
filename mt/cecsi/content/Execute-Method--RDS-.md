---
title: "Execute Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 2d9c30e9-ab5b-4920-91b8-48454c2fb5d8
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
# Execute Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="84a43c17cd2c1182df7a69d75eb975ff" id="tgt1" class="tgtSentence">Executes the request and creates an ADO recordset for use in ADO 2.5 and later.</caps:sentence>
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
          <parameterReference>object</parameterReference>.<legacyBold>Execute(</legacyBold><parameterReference>ConnectionString As String, HandlerString As String, QueryString As String, lFetchOptions As Long, Properties, TableId, lExecuteOptions As Long, pParameters, [lcid As Long], [pInformation]</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>ConnectionString </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d167bf9f6c65ad13d7002282107f146d" id="tgt6" class="tgtSentence">A string used to connect to the OLE DB provider where the request will be sent for execution.</caps:sentence>
                <caps:sentence sentenceid="68c9b70b4c90cee081c458dfae47e4d0" id="tgt7" class="tgtSentence"> If a handler is specified by using <parameterReference>HandlerString</parameterReference> it can edit or replace the connection string.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>HandlerString </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ac4ef201b0e5b303aeb2a2d56bbb015d" id="tgt8" class="tgtSentence">A two-part string that identifies the handler to be used with this execution.</caps:sentence>
                <caps:sentence sentenceid="6668483370ae31fe7b096614686b0984" id="tgt9" class="tgtSentence"> The string contains two parts.</caps:sentence>
                <caps:sentence sentenceid="0e5078cf2aec59c27cceceba97b93520" id="tgt10" class="tgtSentence"> The first part contains the name (ProgID) of the handler to be used.</caps:sentence>
                <caps:sentence sentenceid="c0df359eb6cdeeefcef5beeb6b13f2e6" id="tgt11" class="tgtSentence"> The second part contains arguments to be passed to the handler.</caps:sentence>
                <caps:sentence sentenceid="38dfad5ea853d40bd872058627fe34e6" id="tgt12" class="tgtSentence"> The details of how the arguments string is interpreted are specific to each handler.</caps:sentence>
                <caps:sentence sentenceid="c1df87b4d129918da5e80b5307a41833" id="tgt13" class="tgtSentence"> The two parts are separated by the first instance of a comma in the string.</caps:sentence>
                <caps:sentence sentenceid="04dfa2df059f0c9e325c457d1839ae35" id="tgt14" class="tgtSentence"> The arguments string can contain additional commas.</caps:sentence>
                <caps:sentence sentenceid="eb7bd88bd784064af19f6909107892ae" id="tgt15" class="tgtSentence"> The arguments are optional.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>QueryString </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="39bab05395d611f647d57ef3aefb8dab" id="tgt16" class="tgtSentence">A command in the command language supported by the OLE DB provider identified in the connection string.</caps:sentence>
                <caps:sentence sentenceid="cad718203ddeb5aa30a3c7bb017dcdf5" id="tgt17" class="tgtSentence"> For SQL-based providers, <parameterReference>QueryString</parameterReference> might contain a Transact-SQL command statement, but for non-SQL providers (for example, MSDataShape) this may not be a <token>tsql</token> query statement.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5d1d76f86c5d6bd842ed5c1051232fdc" id="tgt18" class="tgtSentence">If a handler is being used, the handler can alter or replace the value specified here.</caps:sentence>
                <caps:sentence sentenceid="a756304c0e46519033f59ae87f575d08" id="tgt19" class="tgtSentence"> For example, the handler typically replaces <parameterReference>QueryString</parameterReference> with a query string from its .ini file.</caps:sentence>
                <caps:sentence sentenceid="e0c027a6ed36a55be3e825cb479b3317" id="tgt20" class="tgtSentence"> By default, the Msdfmap.ini file is used.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>lFetchOptions </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b5fe9c28d1d773e1ea267b403c271900" id="tgt21" class="tgtSentence">Indicates the type of asynchronous fetching.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="55822da6064720a7912a9bd5c4e1ded7" id="tgt22" class="tgtSentence">For more information, see <link xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions Property (RDS)</link>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>TableID </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="df6e82dc84fa2ac8643c5a6c580e5d2c" id="tgt23" class="tgtSentence">A <languageKeyword>Variant</languageKeyword> of type either VT_EMPTY or VT_BSTR.</caps:sentence>
                <caps:sentence sentenceid="728053d04e4968a702285bb6db82f17d" id="tgt24" class="tgtSentence"> If this value is of type VT_EMPTY, it is ignored.</caps:sentence>
                <caps:sentence sentenceid="6cad9374e7c311128e0cce3ff0bfc7e7" id="tgt25" class="tgtSentence"> If it is of type VT_BSTR, the recordset is created by using <legacyBold>adCmdTableDirect</legacyBold> and the value specified here and the <parameterReference>QueryString</parameterReference> parameter is ignored.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>lExecuteOptions </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d132506887ed0ee93fceeee9ac2f6b26" id="tgt26" class="tgtSentence">A bit mask of execution options:</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="eb93d3ccc7cfbd58d672063dcac9923f" id="tgt27" class="tgtSentence">1=<parameterReference>ReadOnly</parameterReference>   The recordset will be opened by using <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b7cbb9bc324bd6492062b58e7b7e3702" id="tgt28" class="tgtSentence">2=<parameterReference>NoBatch</parameterReference>     The recordset will be opened by using <legacyBold>adLockOptimistic</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="00ea5ec1ddb7207a046a057626bada14" id="tgt29" class="tgtSentence">4=<parameterReference>AllParamInfoSupplied</parameterReference>     The caller guarantees that parameter information for all parameters is supplied in <parameterReference>pParameters</parameterReference>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="073e0d77db5c689a11addcdf297b83ae" id="tgt30" class="tgtSentence">8=<parameterReference>GetInfo</parameterReference>     Parameter information for the query will be obtained from the OLE DB provider and returned in the <parameterReference>pParameters</parameterReference> parameter.</caps:sentence>
                <caps:sentence sentenceid="6bcf752a911478f8c83861b65485967b" id="tgt31" class="tgtSentence"> The query is not executed and no recordset is returned.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b089701713ff66f595a87b68c818da2f" id="tgt32" class="tgtSentence">16=<parameterReference>GetHiddenColumns</parameterReference>     The recordset will be opened by using <legacyBold>adLockBatchOptimistic</legacyBold> and any hidden columns will be included in the recordset.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="13f696ccf3e0cc3b30b65c1c2d5b82b4" id="tgt33" class="tgtSentence">
                  <parameterReference>ReadOnly</parameterReference>, <parameterReference>NoBatch</parameterReference> and <parameterReference>GetHiddenColumns</parameterReference> are mutually exclusive options; however, it does not generate an error to set more than one of them.</caps:sentence>
                <caps:sentence sentenceid="c278c49bab0b5b923cd9597763967e65" id="tgt34" class="tgtSentence"> If multiple options are set, <parameterReference>GetHiddenColumns</parameterReference> takes precedence over all others, followed by <parameterReference>ReadOnly</parameterReference>.</caps:sentence>
                <caps:sentence sentenceid="190191a65454f572de8ec7fbb89ddab6" id="tgt35" class="tgtSentence"> If no options are specified, by default, the recordset is opened by using <legacyBold>adLockBatchOptimistic</legacyBold> and hidden columns are not included in the recordset.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c43b1f6434843c06eb3ee34cbc3e3940" id="tgt36" class="tgtSentence"> <parameterReference>pParameters </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="884549b19a624b7d121ada23cd7790b8" id="tgt37" class="tgtSentence">A <languageKeyword>Variant</languageKeyword> that contains a safe array of parameter definitions.</caps:sentence>
                <caps:sentence sentenceid="2e01e01f110d4b95fce73d22d7b1ca75" id="tgt38" class="tgtSentence"> If the <parameterReference>GetInfo</parameterReference> option was specified in <parameterReference>lExecuteOptions</parameterReference>, this parameter is used to return the parameter definitions obtained from the OLE DB provider.</caps:sentence>
                <caps:sentence sentenceid="ed6ffce31317bf4836d52f6c6b57f673" id="tgt39" class="tgtSentence"> Otherwise, this parameter can be empty.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="7dfc8e339f58a60f6fa014c1092fafbc" id="tgt40" class="tgtSentence"> <parameterReference>lcid </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="39389ae3e0eeaacd37e91b84b388635d" id="tgt41" class="tgtSentence">The LCID used to build any errors that are returned in <parameterReference>pInformation</parameterReference>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="433716f42f8ccbc61f486955df7f2639" id="tgt42" class="tgtSentence"> <parameterReference>pInformation </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d236e0849208f5be90606a96e4a9ad05" id="tgt43" class="tgtSentence">A pointer to information error returned by Execute.</caps:sentence>
                <caps:sentence sentenceid="dd9f35542fec75a884d4b34270b84417" id="tgt44" class="tgtSentence"> If NULL, no error information is returned.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="3569fdb4eb5ded62bb9095ee0f03d153" id="tgt45" class="tgtSentence">The <parameterReference>HandlerString</parameterReference> parameter may be null.</caps:sentence>
            <caps:sentence sentenceid="1b4c660a3a602cd739f685a819be7264" id="tgt46" class="tgtSentence"> What happens in this case depends on how the RDS server is configured.</caps:sentence>
            <caps:sentence sentenceid="dc86db3c777e821e0f1e8862f2dbea9d" id="tgt47" class="tgtSentence"> A handler string of "MSDFMAP.handler" indicates that the Microsoft supplied handler (Msdfmap.dll) should be used.</caps:sentence>
            <caps:sentence sentenceid="dca3b0f47a2bb9ac97fdc3da8755c3cd" id="tgt48" class="tgtSentence"> A handler string of "MASDFMAP.handler,sample.ini" indicates that the Msdfmap.dll handler should be used and that the argument "sample.ini" should be passed to the handler.</caps:sentence>
            <caps:sentence sentenceid="5d8810a5f13357a7a6a18c20ed4acda9" id="tgt49" class="tgtSentence"> MSDFMAP.dll will interpret the argument as a direction to use the sample.ini to check the connection and query strings.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt50" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Executes the request and creates an ADO recordset for use in ADO 2.5 and later.</caps:sentence>
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
          <parameterReference>object</parameterReference>.<legacyBold>Execute(</legacyBold><parameterReference>ConnectionString As String, HandlerString As String, QueryString As String, lFetchOptions As Long, Properties, TableId, lExecuteOptions As Long, pParameters, [lcid As Long], [pInformation]</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <parameterReference>ConnectionString </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A string used to connect to the OLE DB provider where the request will be sent for execution.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> If a handler is specified by using <parameterReference>HandlerString</parameterReference> it can edit or replace the connection string.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>HandlerString </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">A two-part string that identifies the handler to be used with this execution.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> The string contains two parts.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> The first part contains the name (ProgID) of the handler to be used.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> The second part contains arguments to be passed to the handler.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> The details of how the arguments string is interpreted are specific to each handler.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> The two parts are separated by the first instance of a comma in the string.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> The arguments string can contain additional commas.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> The arguments are optional.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>QueryString </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src16" class="srcSentence">A command in the command language supported by the OLE DB provider identified in the connection string.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> For SQL-based providers, <parameterReference>QueryString</parameterReference> might contain a Transact-SQL command statement, but for non-SQL providers (for example, MSDataShape) this may not be a <token>tsql</token> query statement.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src18" class="srcSentence">If a handler is being used, the handler can alter or replace the value specified here.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> For example, the handler typically replaces <parameterReference>QueryString</parameterReference> with a query string from its .ini file.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> By default, the Msdfmap.ini file is used.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>lFetchOptions </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src21" class="srcSentence">Indicates the type of asynchronous fetching.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src22" class="srcSentence">For more information, see <link xlink:href="7b2e254a-9354-4541-bc98-bb185276388f">FetchOptions Property (RDS)</link>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>TableID </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src23" class="srcSentence">A <languageKeyword>Variant</languageKeyword> of type either VT_EMPTY or VT_BSTR.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> If this value is of type VT_EMPTY, it is ignored.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> If it is of type VT_BSTR, the recordset is created by using <legacyBold>adCmdTableDirect</legacyBold> and the value specified here and the <parameterReference>QueryString</parameterReference> parameter is ignored.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <parameterReference>lExecuteOptions </parameterReference>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src26" class="srcSentence">A bit mask of execution options:</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src27" class="srcSentence">1=<parameterReference>ReadOnly</parameterReference>   The recordset will be opened by using <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src28" class="srcSentence">2=<parameterReference>NoBatch</parameterReference>     The recordset will be opened by using <legacyBold>adLockOptimistic</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src29" class="srcSentence">4=<parameterReference>AllParamInfoSupplied</parameterReference>     The caller guarantees that parameter information for all parameters is supplied in <parameterReference>pParameters</parameterReference>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src30" class="srcSentence">8=<parameterReference>GetInfo</parameterReference>     Parameter information for the query will be obtained from the OLE DB provider and returned in the <parameterReference>pParameters</parameterReference> parameter.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> The query is not executed and no recordset is returned.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src32" class="srcSentence">16=<parameterReference>GetHiddenColumns</parameterReference>     The recordset will be opened by using <legacyBold>adLockBatchOptimistic</legacyBold> and any hidden columns will be included in the recordset.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src33" class="srcSentence">
                  <parameterReference>ReadOnly</parameterReference>, <parameterReference>NoBatch</parameterReference> and <parameterReference>GetHiddenColumns</parameterReference> are mutually exclusive options; however, it does not generate an error to set more than one of them.</caps:sentence>
                <caps:sentence id="src34" class="srcSentence"> If multiple options are set, <parameterReference>GetHiddenColumns</parameterReference> takes precedence over all others, followed by <parameterReference>ReadOnly</parameterReference>.</caps:sentence>
                <caps:sentence id="src35" class="srcSentence"> If no options are specified, by default, the recordset is opened by using <legacyBold>adLockBatchOptimistic</legacyBold> and hidden columns are not included in the recordset.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src36" class="srcSentence"> <parameterReference>pParameters </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src37" class="srcSentence">A <languageKeyword>Variant</languageKeyword> that contains a safe array of parameter definitions.</caps:sentence>
                <caps:sentence id="src38" class="srcSentence"> If the <parameterReference>GetInfo</parameterReference> option was specified in <parameterReference>lExecuteOptions</parameterReference>, this parameter is used to return the parameter definitions obtained from the OLE DB provider.</caps:sentence>
                <caps:sentence id="src39" class="srcSentence"> Otherwise, this parameter can be empty.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src40" class="srcSentence"> <parameterReference>lcid </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src41" class="srcSentence">The LCID used to build any errors that are returned in <parameterReference>pInformation</parameterReference>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src42" class="srcSentence"> <parameterReference>pInformation </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src43" class="srcSentence">A pointer to information error returned by Execute.</caps:sentence>
                <caps:sentence id="src44" class="srcSentence"> If NULL, no error information is returned.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src45" class="srcSentence">The <parameterReference>HandlerString</parameterReference> parameter may be null.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> What happens in this case depends on how the RDS server is configured.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> A handler string of "MSDFMAP.handler" indicates that the Microsoft supplied handler (Msdfmap.dll) should be used.</caps:sentence>
            <caps:sentence id="src48" class="srcSentence"> A handler string of "MASDFMAP.handler,sample.ini" indicates that the Msdfmap.dll handler should be used and that the argument "sample.ini" should be passed to the handler.</caps:sentence>
            <caps:sentence id="src49" class="srcSentence"> MSDFMAP.dll will interpret the argument as a direction to use the sample.ini to check the connection and query strings.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src50" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
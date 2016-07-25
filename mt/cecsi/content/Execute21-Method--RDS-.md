---
title: "Execute21 Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 9f131c8d-1497-416d-8209-abb481c38f7b
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
# Execute21 Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7e224ec1e9335b1c6472782f496e85ea" id="tgt1" class="tgtSentence">Executes the request and creates an ADO recordset for use in ADO 2.1.</caps:sentence>
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
          <parameterReference>object</parameterReference>.<legacyBold>Execute21(</legacyBold><parameterReference>ConnectionString As String, HandlerString As String, QueryString As String, lMarshalOptions As Long, Properties, TableId, lExecuteOptions As Long, pParameters</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d78656013dfd2e3c848a339806ae4610" id="tgt6" class="tgtSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d167bf9f6c65ad13d7002282107f146d" id="tgt7" class="tgtSentence">A string used to connect to the OLE DB provider where the request will be sent for execution.</caps:sentence>
                <caps:sentence sentenceid="78e00d8ae12e8854ac8ad99d5d507ae7" id="tgt8" class="tgtSentence"> If a handler is specified by using <legacyItalic>HandlerString</legacyItalic>, it can edit or replace the connection string.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e574ae256511d7881774708955260d6a" id="tgt9" class="tgtSentence"> <legacyItalic>HandlerString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="508e53f45c1b8e7e8ff025d7e5e6f54e" id="tgt10" class="tgtSentence">The string identifies the handler to be used with this execution.</caps:sentence>
                <caps:sentence sentenceid="6668483370ae31fe7b096614686b0984" id="tgt11" class="tgtSentence"> The string contains two parts.</caps:sentence>
                <caps:sentence sentenceid="0e5078cf2aec59c27cceceba97b93520" id="tgt12" class="tgtSentence"> The first part contains the name (ProgID) of the handler to be used.</caps:sentence>
                <caps:sentence sentenceid="be6d3a3634225e9b7f8ef8a0dfdab8b6" id="tgt13" class="tgtSentence"> The second part of the string contains arguments to be passed to the handler.</caps:sentence>
                <caps:sentence sentenceid="a2577b29f52b029ecf3a3384804d0b3a" id="tgt14" class="tgtSentence"> How the arguments string is interpreted is handler specific.</caps:sentence>
                <caps:sentence sentenceid="1d968146aa350e170efc926d37e0517f" id="tgt15" class="tgtSentence"> The two parts are separated by the first instance of a comma in the string (although the arguments string can contain additional commas).</caps:sentence>
                <caps:sentence sentenceid="eb7bd88bd784064af19f6909107892ae" id="tgt16" class="tgtSentence"> The arguments are optional.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="37e5c165259d70bf8ff4aecb3c54ab2a" id="tgt17" class="tgtSentence"> <legacyItalic>QueryString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="39bab05395d611f647d57ef3aefb8dab" id="tgt18" class="tgtSentence">A command in the command language supported by the OLE DB provider identified in the connection string.</caps:sentence>
                <caps:sentence sentenceid="8f07d34e81d4c844db0be7046154b4d0" id="tgt19" class="tgtSentence"> For SQL-based providers, it might contain a <token>tsql</token> command statement, but for non-SQL providers (for example, MSDataShape) this may not be a <token>tsql</token> query statement.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ecac794ddec35665d018474a7f2aeb9d" id="tgt20" class="tgtSentence">Also, if a handler is being used (and it is highly recommended that a handler be used), the handler can alter or replace the value specified here.</caps:sentence>
                <caps:sentence sentenceid="011fd95066d210d8f823de15a3fdf8eb" id="tgt21" class="tgtSentence"> For example, the handler typically replaces <legacyItalic>QueryString</legacyItalic> with a query string from its .ini file.</caps:sentence>
                <caps:sentence sentenceid="e0c027a6ed36a55be3e825cb479b3317" id="tgt22" class="tgtSentence"> By default, the Msdfmap.ini file is used.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="55755c7ca7f18d71f70cef1e3ef16b4a" id="tgt23" class="tgtSentence"> <legacyItalic>lMarshalOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0a6889d68e43bad407ee550f454e0513" id="tgt24" class="tgtSentence">Used to set the marshaling options on the rowset/recordset being returned.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="020134c7e6821cb2af8753b6ed8fa182" id="tgt25" class="tgtSentence"> <legacyItalic>TableID</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="c45f0025adad9279b46448cb22bc333b" id="tgt26" class="tgtSentence">A variant of type either VT_EMPTY or VT_BSTR.</caps:sentence>
                <caps:sentence sentenceid="728053d04e4968a702285bb6db82f17d" id="tgt27" class="tgtSentence"> If this value is of type VT_EMPTY, it is ignored.</caps:sentence>
                <caps:sentence sentenceid="97214bea8da86a379988959c0fca67e7" id="tgt28" class="tgtSentence"> If it is of type VT_BSTR, the recordset is created by using <legacyBold>adCmdTableDirect</legacyBold> using the value specified here and the <legacyItalic>QueryString</legacyItalic> parameter is ignored.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="309f923783d19106d458870b9e75e798" id="tgt29" class="tgtSentence"> <legacyItalic>lExecuteOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="c92517539291311b90a80b3505923987" id="tgt30" class="tgtSentence">A bitmask of execution options:</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c2c798769349698621deb8445c732d9c" id="tgt31" class="tgtSentence">1=<legacyItalic>ReadOnly</legacyItalic>     The recordset will be opened by using <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="0d90b9251003e2982cd09105fbbb6a77" id="tgt32" class="tgtSentence">2=<legacyItalic>NoBatch</legacyItalic>     The recordset will be opened by using <legacyBold>adLockOptimistic</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="48a332d11f34d21aef6fec4a4b414da6" id="tgt33" class="tgtSentence">4=<legacyItalic>AllParamInfoSupplied</legacyItalic>     The caller guarantees that parameter information for all parameters is supplied in <legacyItalic>pParameters</legacyItalic>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="85a18752117cf39b25a17730ccca37d0" id="tgt34" class="tgtSentence">8=<legacyItalic>GetInfo</legacyItalic>     Parameter information for the query will be obtained from the OLE DB provider and returned in the <legacyItalic>pParameters</legacyItalic> parameter.</caps:sentence>
                <caps:sentence sentenceid="6bcf752a911478f8c83861b65485967b" id="tgt35" class="tgtSentence"> The query is not executed and no recordset is returned.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="37bff1af67a6f26892b97b27d5cc1f99" id="tgt36" class="tgtSentence">16=GetHiddenColumns     The recordset will be opened by using <legacyBold>adLockBatchOptimistic</legacyBold> and any hidden columns will be included in the recordset.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e06cb10246de1e9cfe1ffff8aed0ad3b" id="tgt37" class="tgtSentence">Although <legacyItalic>ReadOnly</legacyItalic>, <legacyItalic>NoBatch</legacyItalic> and <legacyItalic>GetHiddenColumns</legacyItalic> are mutually exclusive options, it is not an error to set more than one of them.</caps:sentence>
                <caps:sentence sentenceid="16be79c3148210c991c292222c3c7af9" id="tgt38" class="tgtSentence"> If multiple options are set, <legacyItalic>GetHiddenColumns</legacyItalic> takes precedence over all other options, followed by <legacyItalic>ReadOnly</legacyItalic>.</caps:sentence>
                <caps:sentence sentenceid="29223732f2b01ac871bc88b27ba31e5e" id="tgt39" class="tgtSentence"> If no options are specified, by default, the recordset is opened by using <legacyBold>adLockBatchOptimistic</legacyBold> but hidden columns are not included in the recordset.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="3ef305448ede56f850ff8c3076f174d5" id="tgt40" class="tgtSentence"> <legacyItalic>pParameters</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="141f73a982f2773e235c6fdfc034702a" id="tgt41" class="tgtSentence">A variant that contains a safe array of parameter definitions.</caps:sentence>
                <caps:sentence sentenceid="c056728fa64c8bb5d114ea134907ee77" id="tgt42" class="tgtSentence"> If the <legacyItalic>GetInfo</legacyItalic> option was specified in <legacyItalic>lExecuteOptions</legacyItalic>, this parameter is used to return the parameter definitions obtained from the OLE DB provider.</caps:sentence>
                <caps:sentence sentenceid="227a68193ad2b424c425c9e335150489" id="tgt43" class="tgtSentence"> Otherwise, this parameter may be empty.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1a2cfafaeb8866689d41715c096f38ba" id="tgt44" class="tgtSentence">The <legacyItalic>HandlerString</legacyItalic> parameter may be null.</caps:sentence>
            <caps:sentence sentenceid="1996ef0e2221f44b176ee3eef69a4e3e" id="tgt45" class="tgtSentence"> What occurs in this case depends on how the RDS server is configured.</caps:sentence>
            <caps:sentence sentenceid="dc86db3c777e821e0f1e8862f2dbea9d" id="tgt46" class="tgtSentence"> A handler string of "MSDFMAP.handler" indicates that the Microsoft supplied handler (Msdfmap.dll) should be used.</caps:sentence>
            <caps:sentence sentenceid="dca3b0f47a2bb9ac97fdc3da8755c3cd" id="tgt47" class="tgtSentence"> A handler string of "MASDFMAP.handler,sample.ini" indicates that the Msdfmap.dll handler should be used and that the argument "sample.ini" should be passed to the handler.</caps:sentence>
            <caps:sentence sentenceid="5d8810a5f13357a7a6a18c20ed4acda9" id="tgt48" class="tgtSentence"> MSDFMAP.dll will interpret the argument as a direction to use the sample.ini to check the connection and query strings.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="60993b72a053f0d79236198807f3f3ce" id="tgt49" class="tgtSentence">The <legacyBold>Execute21</legacyBold> method is a version of the <legacyLink xlink:href="2d9c30e9-ab5b-4920-91b8-48454c2fb5d8">Execute method (RDS)</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="b43b3fc164082b9a36b6338d79b863f6" id="tgt50" class="tgtSentence"> Where you need to use the <legacyBold>Execute</legacyBold> method to communicate with ADO 2.1, the <legacyBold>Execute21</legacyBold> method can be called instead.</caps:sentence>
              <caps:sentence sentenceid="81004b7a9e19a551679414aa9f5a163b" id="tgt51" class="tgtSentence"> The capabilities of the <legacyBold>Execute</legacyBold> method in ADO 2.5 and later are a superset of the capabilities provided for the same method in ADO 2.1.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt52" class="tgtSentence">Applies To</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Executes the request and creates an ADO recordset for use in ADO 2.1.</caps:sentence>
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
          <parameterReference>object</parameterReference>.<legacyBold>Execute21(</legacyBold><parameterReference>ConnectionString As String, HandlerString As String, QueryString As String, lMarshalOptions As Long, Properties, TableId, lExecuteOptions As Long, pParameters</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">A string used to connect to the OLE DB provider where the request will be sent for execution.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> If a handler is specified by using <legacyItalic>HandlerString</legacyItalic>, it can edit or replace the connection string.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>HandlerString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">The string identifies the handler to be used with this execution.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> The string contains two parts.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> The first part contains the name (ProgID) of the handler to be used.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> The second part of the string contains arguments to be passed to the handler.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> How the arguments string is interpreted is handler specific.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> The two parts are separated by the first instance of a comma in the string (although the arguments string can contain additional commas).</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> The arguments are optional.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src17" class="srcSentence"> <legacyItalic>QueryString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src18" class="srcSentence">A command in the command language supported by the OLE DB provider identified in the connection string.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> For SQL-based providers, it might contain a <token>tsql</token> command statement, but for non-SQL providers (for example, MSDataShape) this may not be a <token>tsql</token> query statement.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src20" class="srcSentence">Also, if a handler is being used (and it is highly recommended that a handler be used), the handler can alter or replace the value specified here.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> For example, the handler typically replaces <legacyItalic>QueryString</legacyItalic> with a query string from its .ini file.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> By default, the Msdfmap.ini file is used.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src23" class="srcSentence"> <legacyItalic>lMarshalOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src24" class="srcSentence">Used to set the marshaling options on the rowset/recordset being returned.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src25" class="srcSentence"> <legacyItalic>TableID</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src26" class="srcSentence">A variant of type either VT_EMPTY or VT_BSTR.</caps:sentence>
                <caps:sentence id="src27" class="srcSentence"> If this value is of type VT_EMPTY, it is ignored.</caps:sentence>
                <caps:sentence id="src28" class="srcSentence"> If it is of type VT_BSTR, the recordset is created by using <legacyBold>adCmdTableDirect</legacyBold> using the value specified here and the <legacyItalic>QueryString</legacyItalic> parameter is ignored.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src29" class="srcSentence"> <legacyItalic>lExecuteOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src30" class="srcSentence">A bitmask of execution options:</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src31" class="srcSentence">1=<legacyItalic>ReadOnly</legacyItalic>     The recordset will be opened by using <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src32" class="srcSentence">2=<legacyItalic>NoBatch</legacyItalic>     The recordset will be opened by using <legacyBold>adLockOptimistic</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src33" class="srcSentence">4=<legacyItalic>AllParamInfoSupplied</legacyItalic>     The caller guarantees that parameter information for all parameters is supplied in <legacyItalic>pParameters</legacyItalic>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src34" class="srcSentence">8=<legacyItalic>GetInfo</legacyItalic>     Parameter information for the query will be obtained from the OLE DB provider and returned in the <legacyItalic>pParameters</legacyItalic> parameter.</caps:sentence>
                <caps:sentence id="src35" class="srcSentence"> The query is not executed and no recordset is returned.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src36" class="srcSentence">16=GetHiddenColumns     The recordset will be opened by using <legacyBold>adLockBatchOptimistic</legacyBold> and any hidden columns will be included in the recordset.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src37" class="srcSentence">Although <legacyItalic>ReadOnly</legacyItalic>, <legacyItalic>NoBatch</legacyItalic> and <legacyItalic>GetHiddenColumns</legacyItalic> are mutually exclusive options, it is not an error to set more than one of them.</caps:sentence>
                <caps:sentence id="src38" class="srcSentence"> If multiple options are set, <legacyItalic>GetHiddenColumns</legacyItalic> takes precedence over all other options, followed by <legacyItalic>ReadOnly</legacyItalic>.</caps:sentence>
                <caps:sentence id="src39" class="srcSentence"> If no options are specified, by default, the recordset is opened by using <legacyBold>adLockBatchOptimistic</legacyBold> but hidden columns are not included in the recordset.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src40" class="srcSentence"> <legacyItalic>pParameters</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src41" class="srcSentence">A variant that contains a safe array of parameter definitions.</caps:sentence>
                <caps:sentence id="src42" class="srcSentence"> If the <legacyItalic>GetInfo</legacyItalic> option was specified in <legacyItalic>lExecuteOptions</legacyItalic>, this parameter is used to return the parameter definitions obtained from the OLE DB provider.</caps:sentence>
                <caps:sentence id="src43" class="srcSentence"> Otherwise, this parameter may be empty.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src44" class="srcSentence">The <legacyItalic>HandlerString</legacyItalic> parameter may be null.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> What occurs in this case depends on how the RDS server is configured.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> A handler string of "MSDFMAP.handler" indicates that the Microsoft supplied handler (Msdfmap.dll) should be used.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> A handler string of "MASDFMAP.handler,sample.ini" indicates that the Msdfmap.dll handler should be used and that the argument "sample.ini" should be passed to the handler.</caps:sentence>
            <caps:sentence id="src48" class="srcSentence"> MSDFMAP.dll will interpret the argument as a direction to use the sample.ini to check the connection and query strings.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src49" class="srcSentence">The <legacyBold>Execute21</legacyBold> method is a version of the <legacyLink xlink:href="2d9c30e9-ab5b-4920-91b8-48454c2fb5d8">Execute method (RDS)</legacyLink>.</caps:sentence>
              <caps:sentence id="src50" class="srcSentence"> Where you need to use the <legacyBold>Execute</legacyBold> method to communicate with ADO 2.1, the <legacyBold>Execute21</legacyBold> method can be called instead.</caps:sentence>
              <caps:sentence id="src51" class="srcSentence"> The capabilities of the <legacyBold>Execute</legacyBold> method in ADO 2.5 and later are a superset of the capabilities provided for the same method in ADO 2.1.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src52" class="srcSentence">Applies To</caps:sentence>
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
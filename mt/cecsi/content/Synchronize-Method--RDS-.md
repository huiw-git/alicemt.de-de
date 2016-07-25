---
title: "Synchronize Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 7af42866-7db2-4174-8251-388a2cf741f2
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
# Synchronize Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ff22839ddb0a93a0d0401948a1c27e80" id="tgt1" class="tgtSentence">Synchronize the given Recordset with the database specified by the connection string for use in ADO 2.5 and later.</caps:sentence>
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
          <parameterReference>object</parameterReference>.<legacyBold>Synchronize(</legacyBold><parameterReference>ConnectionString As String, HandlerString As String, lSynchronizeOptions As Long, ppRecordset As Object, pStatusArray, [lcid As Long], [pInformation</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d78656013dfd2e3c848a339806ae4610" id="tgt6" class="tgtSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0ab61cfc06503edbd72d1f5890fd811e" id="tgt7" class="tgtSentence">A string used to connect to the OLE DB provider where the request will be sent.</caps:sentence>
                <caps:sentence sentenceid="019736972a61e417ae1958e91993de08" id="tgt8" class="tgtSentence"> If a handler is used, the handler may edit or replace the connection string.</caps:sentence>
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
                <caps:sentence sentenceid="20be080b85ace641fa5181f3c22323d5" id="tgt15" class="tgtSentence"> The two parts are separated by the first instance of a comma in the string (although the arguments string may contain additional commas).</caps:sentence>
                <caps:sentence sentenceid="eb7bd88bd784064af19f6909107892ae" id="tgt16" class="tgtSentence"> The arguments are optional.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="9d812ebb2585ca0dc451ddda3392dbad" id="tgt17" class="tgtSentence"> <legacyItalic>lSynchronizeOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7636fea187878b41840cbedcb34aadec" id="tgt18" class="tgtSentence">A bit mask of synchronization options.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a156726b11fd82cff3b36ca3ad9fcc1b" id="tgt19" class="tgtSentence">1=<legacyItalic>UpdateTransact</legacyItalic>     Updates to the database are wrapped in a transaction.</caps:sentence>
                <caps:sentence sentenceid="b302f55e2bf1378db7a472a2f72a765e" id="tgt20" class="tgtSentence"> The transaction is aborted if any of the updates fail.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="25776f8b1831ee1a4d4593866c27823b" id="tgt21" class="tgtSentence">2=<legacyItalic>RefreshWithUpdate</legacyItalic>     Causes row statuses to be returned when neither <legacyItalic>Refresh</legacyItalic> nor <legacyItalic>RefreshConflicts</legacyItalic> is set.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="f7d1b8b75711d33e7319e0a8598467c5" id="tgt22" class="tgtSentence">4=<legacyItalic>Refresh</legacyItalic>     The recordset is refreshed with current data from the database.</caps:sentence>
                <caps:sentence sentenceid="40fb7ee42856ac0c9439bd2353ce0e58" id="tgt23" class="tgtSentence"> Pending updates are not pushed to the database.</caps:sentence>
                <caps:sentence sentenceid="62b307d980b7665baebf24dbf6d5b201" id="tgt24" class="tgtSentence"> If this bit is not set, the recordset is not refreshed, and any pending updates are pushed to the database.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="46a77a2201a659f8bed95f6a994f67cd" id="tgt25" class="tgtSentence">8=<legacyItalic>RefreshConflicts</legacyItalic>     Any rows with pending changes fail to update.</caps:sentence>
                <caps:sentence sentenceid="2c79324b77fe66cd2431f6f1a36064ff" id="tgt26" class="tgtSentence"> The rows which failed to update are refreshed with current data from the database.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="209325ca5a48a859611ebe9a60466689" id="tgt27" class="tgtSentence"> <legacyItalic>ppRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="4873a1d0bd18b110e2e1fe68101e9bce" id="tgt28" class="tgtSentence">A pointer to the recordset to be synchronized.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d83cf6c7c445b2482b2abe740ecdf797" id="tgt29" class="tgtSentence"> <legacyItalic>pStatusArray</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="26e31859b34c57f7318a2162e0888b60" id="tgt30" class="tgtSentence">A variant used to return a safe array of row statuses for the rows affected by synchronize.</caps:sentence>
                <caps:sentence sentenceid="18279b9721e549f8176b4930b5feb130" id="tgt31" class="tgtSentence"> Not set if none of the following synchronization options are set: <legacyItalic>RefreshWithUpdate</legacyItalic>, <legacyItalic>Refresh</legacyItalic> and <legacyItalic>RefreshConflicts</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d58409f5726000eb418150424d009359" id="tgt32" class="tgtSentence"> <legacyItalic>lcid</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="9361cf052fbc0227ad507410428b55b2" id="tgt33" class="tgtSentence">The LCID used to build any errors that are returned in <legacyItalic>pInformation</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="50523b68ba4a98c90f725945e7c18b5a" id="tgt34" class="tgtSentence"> <legacyItalic>pInformation</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b88bb3ec50a15ed13b23aee7a9dd0344" id="tgt35" class="tgtSentence">A pointer to information error returned by <unmanagedCodeEntityReference>Execute</unmanagedCodeEntityReference>.</caps:sentence>
                <caps:sentence sentenceid="dd9f35542fec75a884d4b34270b84417" id="tgt36" class="tgtSentence"> If NULL, no error information is returned.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1a2cfafaeb8866689d41715c096f38ba" id="tgt37" class="tgtSentence">The <legacyItalic>HandlerString</legacyItalic> parameter may be null.</caps:sentence>
            <caps:sentence sentenceid="1b4c660a3a602cd739f685a819be7264" id="tgt38" class="tgtSentence"> What happens in this case depends on how the RDS server is configured.</caps:sentence>
            <caps:sentence sentenceid="dc86db3c777e821e0f1e8862f2dbea9d" id="tgt39" class="tgtSentence"> A handler string of "MSDFMAP.handler" indicates that the Microsoft supplied handler (Msdfmap.dll) should be used.</caps:sentence>
            <caps:sentence sentenceid="dca3b0f47a2bb9ac97fdc3da8755c3cd" id="tgt40" class="tgtSentence"> A handler string of "MASDFMAP.handler,sample.ini" indicates that the Msdfmap.dll handler should be used and that the argument "sample.ini" should be passed to the handler.</caps:sentence>
            <caps:sentence sentenceid="a9c9e84f5bc1ca37a99b1699737473b6" id="tgt41" class="tgtSentence"> Msdfmap.dll will then interpret the argument as a direction to use the sample.ini to check the connection and query strings.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt42" class="tgtSentence">Applies To</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Synchronize the given Recordset with the database specified by the connection string for use in ADO 2.5 and later.</caps:sentence>
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
          <parameterReference>object</parameterReference>.<legacyBold>Synchronize(</legacyBold><parameterReference>ConnectionString As String, HandlerString As String, lSynchronizeOptions As Long, ppRecordset As Object, pStatusArray, [lcid As Long], [pInformation</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>ConnectionString</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">A string used to connect to the OLE DB provider where the request will be sent.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> If a handler is used, the handler may edit or replace the connection string.</caps:sentence>
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
                <caps:sentence id="src15" class="srcSentence"> The two parts are separated by the first instance of a comma in the string (although the arguments string may contain additional commas).</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> The arguments are optional.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src17" class="srcSentence"> <legacyItalic>lSynchronizeOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src18" class="srcSentence">A bit mask of synchronization options.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src19" class="srcSentence">1=<legacyItalic>UpdateTransact</legacyItalic>     Updates to the database are wrapped in a transaction.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> The transaction is aborted if any of the updates fail.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src21" class="srcSentence">2=<legacyItalic>RefreshWithUpdate</legacyItalic>     Causes row statuses to be returned when neither <legacyItalic>Refresh</legacyItalic> nor <legacyItalic>RefreshConflicts</legacyItalic> is set.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src22" class="srcSentence">4=<legacyItalic>Refresh</legacyItalic>     The recordset is refreshed with current data from the database.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> Pending updates are not pushed to the database.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> If this bit is not set, the recordset is not refreshed, and any pending updates are pushed to the database.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src25" class="srcSentence">8=<legacyItalic>RefreshConflicts</legacyItalic>     Any rows with pending changes fail to update.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> The rows which failed to update are refreshed with current data from the database.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src27" class="srcSentence"> <legacyItalic>ppRecordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src28" class="srcSentence">A pointer to the recordset to be synchronized.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src29" class="srcSentence"> <legacyItalic>pStatusArray</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src30" class="srcSentence">A variant used to return a safe array of row statuses for the rows affected by synchronize.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> Not set if none of the following synchronization options are set: <legacyItalic>RefreshWithUpdate</legacyItalic>, <legacyItalic>Refresh</legacyItalic> and <legacyItalic>RefreshConflicts</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src32" class="srcSentence"> <legacyItalic>lcid</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src33" class="srcSentence">The LCID used to build any errors that are returned in <legacyItalic>pInformation</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src34" class="srcSentence"> <legacyItalic>pInformation</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src35" class="srcSentence">A pointer to information error returned by <unmanagedCodeEntityReference>Execute</unmanagedCodeEntityReference>.</caps:sentence>
                <caps:sentence id="src36" class="srcSentence"> If NULL, no error information is returned.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src37" class="srcSentence">The <legacyItalic>HandlerString</legacyItalic> parameter may be null.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> What happens in this case depends on how the RDS server is configured.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> A handler string of "MSDFMAP.handler" indicates that the Microsoft supplied handler (Msdfmap.dll) should be used.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> A handler string of "MASDFMAP.handler,sample.ini" indicates that the Msdfmap.dll handler should be used and that the argument "sample.ini" should be passed to the handler.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> Msdfmap.dll will then interpret the argument as a direction to use the sample.ini to check the connection and query strings.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src42" class="srcSentence">Applies To</caps:sentence>
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
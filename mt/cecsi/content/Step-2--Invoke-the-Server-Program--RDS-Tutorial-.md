---
title: "Step 2: Invoke the Server Program (RDS Tutorial)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5e74c2da-65ee-4de4-8b41-6eac45c3632e
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
# Step 2: Invoke the Server Program (RDS Tutorial)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="219201f12de5158cc5be575ed8877663" id="tgt1" class="tgtSentence">When you invoke a method on the client <legacyItalic>proxy</legacyItalic>, the actual program on the server executes the method.</caps:sentence>
          <caps:sentence sentenceid="b01c7f1c9f2409bcb805913a46dc140b" id="tgt2" class="tgtSentence"> In this step, you'll execute a query on the server.</caps:sentence>
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
          <caps:sentence sentenceid="81ab003fcd654be0fd83ffc95fab9051" id="tgt7" class="tgtSentence">
            <legacyBold>Part A</legacyBold>   If you weren't using <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> in this tutorial, the most convenient way to perform this step would be to use the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="6a00230886f286ebc63fa8e9e1363a33" id="tgt8" class="tgtSentence"> The <legacyBold>RDS.DataControl</legacyBold> combines the previous step of creating a proxy, with this step, issuing the query.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1b2e659a5389c0f81380c3139ae650e2" id="tgt9" class="tgtSentence">Set the <legacyBold>RDS.DataControl</legacyBold> object <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server</legacyLink> property to identify where the server program should be instantiated; the <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property to specify the connect string to access the data source; and the <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> property to specify the query command text.</caps:sentence>
          <caps:sentence sentenceid="b4d9c983f041f33fa8128709eeb18486" id="tgt10" class="tgtSentence"> Then issue the <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh</legacyLink> method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a <legacyBold>Recordset</legacyBold> object to the client.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="d911ba8196c685eac5abf051362c52a5" id="tgt11" class="tgtSentence">This tutorial does not use the <legacyBold>RDS.DataControl</legacyBold>, but this is how it would look if it did:</caps:sentence>
        </para>
        <code>Sub RDSTutorial2A()
   Dim DC as New RDS.DataControl
   DC.<codeFeaturedElement xmlns="">Server</codeFeaturedElement> = "http://yourServer"
   DC.<codeFeaturedElement xmlns="">Connect</codeFeaturedElement> = "DSN=Pubs"
   DC.<codeFeaturedElement xmlns="">SQL</codeFeaturedElement> = "SELECT * FROM Authors"
   DC.<codeFeaturedElement xmlns="">Refresh</codeFeaturedElement>
...</code>
        <para>
          <caps:sentence sentenceid="305531b4758602db234d845253e47455" id="tgt12" class="tgtSentence">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</caps:sentence>
        </para>
        <code>Dim rs as New ADODB.Recordset
rs.Open "SELECT * FROM Authors","<codeFeaturedElement xmlns="">Provider</codeFeaturedElement>=MS Remote;<codeFeaturedElement xmlns="">Data Source</codeFeaturedElement>=Pubs;" &amp; _
        "<codeFeaturedElement xmlns="">Remote Server</codeFeaturedElement>=http://yourServer;<codeFeaturedElement xmlns="">Remote Provider</codeFeaturedElement>=SQLOLEDB;"</code>
        <para>
          <caps:sentence sentenceid="4f7a6865132f1e3b93bfe814196433d9" id="tgt13" class="tgtSentence">         <legacyBold>Part B</legacyBold>   The general method of performing this step is to invoke the <legacyBold>RDSServer.DataFactory</legacyBold> object <legacyLink xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query</legacyLink> method.</caps:sentence>
          <caps:sentence sentenceid="2a960b5cd39979e8c366759c8ebf67f3" id="tgt14" class="tgtSentence"> That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0875799050bfa0088067133e9a991924" id="tgt15" class="tgtSentence">This tutorial uses the <legacyBold>DataFactory</legacyBold> object <legacyBold>Query</legacyBold> method:</caps:sentence>
        </para>
        <code>Sub RDSTutorial2B()
   Dim DS as New RDS.DataSpace
   Dim DF
   Dim RS as ADODB.Recordset
   Set DF = DS.<codeFeaturedElement xmlns="">CreateObject</codeFeaturedElement>("RDSServer.DataFactory", "http://yourServer")
   Set RS = DF.<codeFeaturedElement xmlns="">Query</codeFeaturedElement> ("DSN=Pubs", "SELECT * FROM Authors")
...</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="9c6779c9-1208-4696-ac51-c39f3a6d9240">Step 3: Server Obtains a Recordset (RDS Tutorial)</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">When you invoke a method on the client <legacyItalic>proxy</legacyItalic>, the actual program on the server executes the method.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> In this step, you'll execute a query on the server.</caps:sentence>
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
          <caps:sentence id="src7" class="srcSentence">
            <legacyBold>Part A</legacyBold>   If you weren't using <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> in this tutorial, the most convenient way to perform this step would be to use the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The <legacyBold>RDS.DataControl</legacyBold> combines the previous step of creating a proxy, with this step, issuing the query.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">Set the <legacyBold>RDS.DataControl</legacyBold> object <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server</legacyLink> property to identify where the server program should be instantiated; the <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property to specify the connect string to access the data source; and the <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> property to specify the query command text.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> Then issue the <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh</legacyLink> method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a <legacyBold>Recordset</legacyBold> object to the client.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">This tutorial does not use the <legacyBold>RDS.DataControl</legacyBold>, but this is how it would look if it did:</caps:sentence>
        </para>
        <code>Sub RDSTutorial2A()
   Dim DC as New RDS.DataControl
   DC.<codeFeaturedElement xmlns="">Server</codeFeaturedElement> = "http://yourServer"
   DC.<codeFeaturedElement xmlns="">Connect</codeFeaturedElement> = "DSN=Pubs"
   DC.<codeFeaturedElement xmlns="">SQL</codeFeaturedElement> = "SELECT * FROM Authors"
   DC.<codeFeaturedElement xmlns="">Refresh</codeFeaturedElement>
...</code>
        <para>
          <caps:sentence id="src12" class="srcSentence">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</caps:sentence>
        </para>
        <code>Dim rs as New ADODB.Recordset
rs.Open "SELECT * FROM Authors","<codeFeaturedElement xmlns="">Provider</codeFeaturedElement>=MS Remote;<codeFeaturedElement xmlns="">Data Source</codeFeaturedElement>=Pubs;" &amp; _
        "<codeFeaturedElement xmlns="">Remote Server</codeFeaturedElement>=http://yourServer;<codeFeaturedElement xmlns="">Remote Provider</codeFeaturedElement>=SQLOLEDB;"</code>
        <para>
          <caps:sentence id="src13" class="srcSentence">         <legacyBold>Part B</legacyBold>   The general method of performing this step is to invoke the <legacyBold>RDSServer.DataFactory</legacyBold> object <legacyLink xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query</legacyLink> method.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src15" class="srcSentence">This tutorial uses the <legacyBold>DataFactory</legacyBold> object <legacyBold>Query</legacyBold> method:</caps:sentence>
        </para>
        <code>Sub RDSTutorial2B()
   Dim DS as New RDS.DataSpace
   Dim DF
   Dim RS as ADODB.Recordset
   Set DF = DS.<codeFeaturedElement xmlns="">CreateObject</codeFeaturedElement>("RDSServer.DataFactory", "http://yourServer")
   Set RS = DF.<codeFeaturedElement xmlns="">Query</codeFeaturedElement> ("DSN=Pubs", "SELECT * FROM Authors")
...</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="9c6779c9-1208-4696-ac51-c39f3a6d9240">Step 3: Server Obtains a Recordset (RDS Tutorial)</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
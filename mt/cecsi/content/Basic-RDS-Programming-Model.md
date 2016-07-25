---
title: "Basic RDS Programming Model"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0bdd236b-edff-4aac-94c3-93e1465ca6c5
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
# Basic RDS Programming Model
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt1" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt2" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt3" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt4" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="2574872c0e34610f5339dfe7ee8861e8" id="tgt5" class="tgtSentence">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information.</caps:sentence>
          <caps:sentence sentenceid="fcdf0050957e747348c3b9c6dd721ee8" id="tgt6" class="tgtSentence"> The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use.</caps:sentence>
          <caps:sentence sentenceid="5cb0b8dea3ebc18a05f63a41a2ccace2" id="tgt7" class="tgtSentence"> RDS provides the means for you to perform the following sequence of actions:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="b68aae75d47c6896891dee35bd03a6b7" id="tgt8" class="tgtSentence">Specify the program to be invoked on the server, and obtain a way to refer to it from the client.</caps:sentence>
              <caps:sentence sentenceid="e8409ac00b9eb405094c4cfbccccc810" id="tgt9" class="tgtSentence"> (This reference is sometimes called a <legacyItalic>proxy</legacyItalic>.</caps:sentence>
              <caps:sentence sentenceid="fe084204857aca22b345340f64db3017" id="tgt10" class="tgtSentence"> It represents the remote server program.</caps:sentence>
              <caps:sentence sentenceid="f192cafa26f40b60c8882235c3b5764a" id="tgt11" class="tgtSentence"> The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="83f2b4f3d98548dba9b841e8d943777d" id="tgt12" class="tgtSentence">Invoke the server program.</caps:sentence>
              <caps:sentence sentenceid="44bf8fe386659be2b426e1d64f67e40b" id="tgt13" class="tgtSentence"> Pass parameters to the server program that identify the data source and the command to issue.</caps:sentence>
              <caps:sentence sentenceid="77cf3918848639bdc58ed351a11aa5cd" id="tgt14" class="tgtSentence"> (The server program actually uses ADO to gain access to the data source.</caps:sentence>
              <caps:sentence sentenceid="93a1e1d334d1e4c0ca8592e0ed1cc6ce" id="tgt15" class="tgtSentence"> ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e1edfb90500e0b5f04453e962722099e" id="tgt16" class="tgtSentence">The server program obtains a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object from the data source.</caps:sentence>
              <caps:sentence sentenceid="80b526a6b97214c09e6ad55e88561d3e" id="tgt17" class="tgtSentence"> Optionally, the <legacyBold>Recordset</legacyBold> object is processed on the server.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="da8c00386481dccbfb215d2b73c38227" id="tgt18" class="tgtSentence">The server program returns the final <legacyBold>Recordset</legacyBold> object to the client application.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a63c71c6f576be03b7473d4a38ebbdb9" id="tgt19" class="tgtSentence">On the client, the <legacyBold>Recordset</legacyBold> object is put into a form that can be easily used by visual controls.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c507ba09b1e82fc53564b7f6ab2b2518" id="tgt20" class="tgtSentence">Any modifications to the <legacyBold>Recordset</legacyBold> object are sent back to the server program, which uses them to update the data source.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="b5af3361a659da5f48fa6c0d1bec7ea4" id="tgt21" class="tgtSentence">This programming model contains certain convenience features.</caps:sentence>
          <caps:sentence sentenceid="d5dcad3c511b0587123f4720602eb232" id="tgt22" class="tgtSentence"> If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="87b5bf2db3ed4514d20c5c60eb37e969" id="tgt23" class="tgtSentence">If you need more complex processing, you can specify your own custom server program.</caps:sentence>
          <caps:sentence sentenceid="7ea25e426872a95a6c0ac4f5f3b46871" id="tgt24" class="tgtSentence"> For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7f83bfdd1c1a838adefeb856ca9f1d3a" id="tgt25" class="tgtSentence">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="3e57af8d-519b-4467-a0bd-af468534cefd">RDS Programming Model in Detail</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src5" class="srcSentence">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> RDS provides the means for you to perform the following sequence of actions:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Specify the program to be invoked on the server, and obtain a way to refer to it from the client.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> (This reference is sometimes called a <legacyItalic>proxy</legacyItalic>.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> It represents the remote server program.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Invoke the server program.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> Pass parameters to the server program that identify the data source and the command to issue.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> (The server program actually uses ADO to gain access to the data source.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">The server program obtains a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object from the data source.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> Optionally, the <legacyBold>Recordset</legacyBold> object is processed on the server.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">The server program returns the final <legacyBold>Recordset</legacyBold> object to the client application.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src19" class="srcSentence">On the client, the <legacyBold>Recordset</legacyBold> object is put into a form that can be easily used by visual controls.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src20" class="srcSentence">Any modifications to the <legacyBold>Recordset</legacyBold> object are sent back to the server program, which uses them to update the data source.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src21" class="srcSentence">This programming model contains certain convenience features.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src23" class="srcSentence">If you need more complex processing, you can specify your own custom server program.</caps:sentence>
          <caps:sentence id="src24" class="srcSentence"> For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src25" class="srcSentence">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="3e57af8d-519b-4467-a0bd-af468534cefd">RDS Programming Model in Detail</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "RDS Programming Model in Detail"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e57af8d-519b-4467-a0bd-af468534cefd
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
# RDS Programming Model in Detail
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8c7f6b0dab2cb0a9ef5cd7f4c1ce41d3" id="tgt1" class="tgtSentence">The following are key elements of the RDS programming model:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="913f713b9550959b8840b896ece5b6ed" id="tgt2" class="tgtSentence">RDS.DataSpace</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5e7fada676510aef896ebc0796b97301" id="tgt3" class="tgtSentence">RDSServer.DataFactory</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="fb777eae6d9020c4e101e50148a3a639" id="tgt4" class="tgtSentence">RDS.DataControl</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4119639092e62c55ea8be348e4d9260d" id="tgt5" class="tgtSentence">Event</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt6" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt7" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt8" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt9" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="913f713b9550959b8840b896ece5b6ed" id="tgt10" class="tgtSentence">RDS.DataSpace</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b9f998f040509d60d115359bee2d320e" id="tgt11" class="tgtSentence">Your client application must specify the server and the server program to invoke.</caps:sentence>
            <caps:sentence sentenceid="2802342f50cf59260da4b501a43c2bb5" id="tgt12" class="tgtSentence"> In return, your application receives a reference to the server program and can treat the reference as if it were the server program itself.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e3f11793d269bd870d9cd618fd76b518" id="tgt13" class="tgtSentence">The RDS object model embodies this functionality with the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="339259e2b774f157833d64cc69ae5348" id="tgt14" class="tgtSentence">The server program is specified with a program identifier, or <legacyItalic>ProgID</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="64205baf7772acb8b903ec250c5d14e2" id="tgt15" class="tgtSentence"> The server uses the <legacyItalic>ProgID</legacyItalic> and the server machine's registry to locate information about the actual program to initiate.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cf3c713b5913d0afe9f1025a44724ab9" id="tgt16" class="tgtSentence">RDS makes a distinction internally depending on whether the server program is on a remote server across the Internet or an intranet; a server on a local area network; or not on a server at all, but instead on a local dynamic-link library (DLL).</caps:sentence>
            <caps:sentence sentenceid="daacfebb5131b242568cba4d0502b081" id="tgt17" class="tgtSentence"> This distinction determines how information is exchanged between the client and the server, and makes a tangible difference in the type of reference returned to your client application.</caps:sentence>
            <caps:sentence sentenceid="4af676776cd54d2fd0a9dd9d3bda1219" id="tgt18" class="tgtSentence"> However, from your point of view, this distinction has no special meaning.</caps:sentence>
            <caps:sentence sentenceid="6b3800ff3e3ab7838f39aa21268a4c88" id="tgt19" class="tgtSentence"> All that matters is that you receive a usable program reference.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5e7fada676510aef896ebc0796b97301" id="tgt20" class="tgtSentence">RDSServer.DataFactory</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9aea8f2cbe54975135cf5eaae2bc8da4" id="tgt21" class="tgtSentence">RDS provides a default server program that can either perform a SQL query against the data source and return a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object or take a <legacyBold>Recordset</legacyBold> object and update the data source.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f3abb60d23adb89793f5fb663320036e" id="tgt22" class="tgtSentence">The RDS object model embodies this functionality with the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6f1253df60cfe1be3ffdb94407df20a6" id="tgt23" class="tgtSentence">In addition, this object has a method for creating an empty <legacyBold>Recordset</legacyBold> object that you can fill programmatically (<legacyLink xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset</legacyLink>), and another method for converting a <legacyBold>Recordset</legacyBold> object into a text string to build a Web page (<legacyLink xlink:href="b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe">ConvertToString</legacyLink>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d39b4eed0fadb7c376d72401cf42cff3" id="tgt24" class="tgtSentence">With ADO, you can override some of the standard connection and command behavior of the <legacyBold>RDSServer.DataFactory</legacyBold> with a <legacyBold>DataFactory</legacyBold> handler and a customization file that contains connection, command, and security parameters.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f170099d18ad612ad34fe3efb35f8c80" id="tgt25" class="tgtSentence">The server program is sometimes called a <legacyItalic>business object</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="9c3fbfe5af3b00765bab18343683d620" id="tgt26" class="tgtSentence"> You can write your own custom business object that can perform complicated data access, validity checks, and so on.</caps:sentence>
            <caps:sentence sentenceid="d3850d7bf5f8f2895e3ab9e7927ede53" id="tgt27" class="tgtSentence"> Even when writing a custom business object, you can create an instance of an <legacyBold>RDSServer.DataFactory</legacyBold> object and use some of its methods to accomplish your own tasks.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="fb777eae6d9020c4e101e50148a3a639" id="tgt28" class="tgtSentence">RDS.DataControl</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="51661291fd04e94d10ab33bfa625150e" id="tgt29" class="tgtSentence">RDS provides a means to combine the functionality of the <legacyBold>RDS.DataSpace</legacyBold> and <legacyBold>RDSServer.DataFactory</legacyBold>, and also enable visual controls to easily use the <legacyBold>Recordset</legacyBold> object returned by a query from a data source.</caps:sentence>
            <caps:sentence sentenceid="0dc1e5d8b34d59badcdf9cf8b64e9fcf" id="tgt30" class="tgtSentence"> RDS attempts, for the most common case, to do as much as possible to automatically gain access to information on a server and display it in a visual control.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f3fce4339d5d33269917626357a7ab84" id="tgt31" class="tgtSentence">The RDS object model embodies this functionality with the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e00d7143ed117221c9ea52ce1747d3fc" id="tgt32" class="tgtSentence">The <legacyBold>RDS.DataControl</legacyBold> has two aspects.</caps:sentence>
            <caps:sentence sentenceid="e621193e9f5bd4b1c61d0fa6f187521f" id="tgt33" class="tgtSentence"> One aspect pertains to the data source.</caps:sentence>
            <caps:sentence sentenceid="551ee1ddc579460f39cf9019a961ed63" id="tgt34" class="tgtSentence"> If you set the command and connection information using the <legacyBold>Connect</legacyBold> and <legacyBold>SQL</legacyBold> properties of the <legacyBold>RDS.DataControl</legacyBold>, it will automatically use the <legacyBold>RDS.DataSpace</legacyBold> to create a reference to the default <legacyBold>RDSServer.DataFactory</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="ceb58390bcd24e73f5dd29e1ca04ea9e" id="tgt35" class="tgtSentence"> Then the <legacyBold>RDSServer.DataFactory</legacyBold> will use the <legacyBold>Connect</legacyBold> property value to connect to the data source, use the <legacyBold>SQL</legacyBold> property value to obtain a <legacyBold>Recordset</legacyBold> from the data source, and return the <legacyBold>Recordset</legacyBold> object to the <legacyBold>RDS.DataControl</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7f7e732bf6c5086822fd713c6558be7a" id="tgt36" class="tgtSentence">The second aspect pertains to the display of returned <legacyBold>Recordset</legacyBold> information in a visual control.</caps:sentence>
            <caps:sentence sentenceid="691656c705db475d04f3f68bc9e4b2aa" id="tgt37" class="tgtSentence"> You can associate a visual control with the <legacyBold>RDS.DataControl</legacyBold> (in a process called binding) and gain access to the information in the associated <legacyBold>Recordset</legacyBold> object, displaying query results on a Web page in Microsoft® Internet Explorer.</caps:sentence>
            <caps:sentence sentenceid="c90b386da5d7b047d2ac5d2efd9c0746" id="tgt38" class="tgtSentence"> Each <legacyBold>RDS.DataControl</legacyBold> object binds one <legacyBold>Recordset</legacyBold> object, representing the results of a single query, to one or more visual controls (for example, a text box, combo box, grid control, and so forth).</caps:sentence>
            <caps:sentence sentenceid="f51ab7374e45d3eebda18958fe6f4de6" id="tgt39" class="tgtSentence"> There may be more than one <legacyBold>RDS.DataControl</legacyBold> object on each page.</caps:sentence>
            <caps:sentence sentenceid="1e262dbdb8f5342c66bbd9d660e383d3" id="tgt40" class="tgtSentence"> Each <legacyBold>RDS.DataControl</legacyBold> object can be connected to a different data source and contain the results of a separate query.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ae0b5d9e20abd99797d2605bc28743c9" id="tgt41" class="tgtSentence">The <legacyBold>RDS.DataControl</legacyBold> object also has its own methods for navigating, sorting, and filtering the rows of the associated <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="19f6382ad1d4ebec49d4c4de3edac42a" id="tgt42" class="tgtSentence"> These methods are similar, but not the same as the methods on the ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt43" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c2912beca8565117449171f4c943a04a" id="tgt44" class="tgtSentence">RDS supports two of its own events, which are independent of the ADO event model.</caps:sentence>
            <caps:sentence sentenceid="52cd4f109cb43e49d8b70aa39b32595c" id="tgt45" class="tgtSentence"> The <legacyLink xlink:href="bf2ae3ac-bfe4-4709-b50a-ea7c282c3164">onReadyStateChange</legacyLink> event is called whenever the <legacyBold>RDS.DataControl</legacyBold> <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState</legacyLink> property changes, thus notifying you when an asynchronous operation has successfully completed, terminated, or experienced an error.</caps:sentence>
            <caps:sentence sentenceid="2d449b734b03aedcb9738b27dfcd064f" id="tgt46" class="tgtSentence"> The <legacyLink xlink:href="b01cbc62-fbd7-4068-b16c-8b0f80a05887">onError</legacyLink> event is called whenever an error occurs, even if the error occurs during an asynchronous operation.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="b4e8e11e0b4789c09b78b65dcd6f7224" id="tgt47" class="tgtSentence">Microsoft Internet Explorer provides two additional events to RDS: <legacyBold>onDataSetChanged</legacyBold>, which indicates that the <legacyBold>Recordset</legacyBold> is functional but still retrieving rows, and <legacyBold>onDataSetComplete</legacyBold>, which indicates that the <legacyBold>Recordset</legacyBold> has finished retrieving rows.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="07ce0ef0-72f1-48f4-823d-1b65d28c0926">RDS Programming Model with Objects</link>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following are key elements of the RDS programming model:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">RDS.DataSpace</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">RDSServer.DataFactory</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">RDS.DataControl</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Event</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence id="src6" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">RDS.DataSpace</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">Your client application must specify the server and the server program to invoke.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> In return, your application receives a reference to the server program and can treat the reference as if it were the server program itself.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">The RDS object model embodies this functionality with the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">The server program is specified with a program identifier, or <legacyItalic>ProgID</legacyItalic>.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The server uses the <legacyItalic>ProgID</legacyItalic> and the server machine's registry to locate information about the actual program to initiate.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">RDS makes a distinction internally depending on whether the server program is on a remote server across the Internet or an intranet; a server on a local area network; or not on a server at all, but instead on a local dynamic-link library (DLL).</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> This distinction determines how information is exchanged between the client and the server, and makes a tangible difference in the type of reference returned to your client application.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> However, from your point of view, this distinction has no special meaning.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> All that matters is that you receive a usable program reference.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">RDSServer.DataFactory</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">RDS provides a default server program that can either perform a SQL query against the data source and return a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object or take a <legacyBold>Recordset</legacyBold> object and update the data source.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">The RDS object model embodies this functionality with the <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">In addition, this object has a method for creating an empty <legacyBold>Recordset</legacyBold> object that you can fill programmatically (<legacyLink xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset</legacyLink>), and another method for converting a <legacyBold>Recordset</legacyBold> object into a text string to build a Web page (<legacyLink xlink:href="b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe">ConvertToString</legacyLink>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">With ADO, you can override some of the standard connection and command behavior of the <legacyBold>RDSServer.DataFactory</legacyBold> with a <legacyBold>DataFactory</legacyBold> handler and a customization file that contains connection, command, and security parameters.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">The server program is sometimes called a <legacyItalic>business object</legacyItalic>.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> You can write your own custom business object that can perform complicated data access, validity checks, and so on.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> Even when writing a custom business object, you can create an instance of an <legacyBold>RDSServer.DataFactory</legacyBold> object and use some of its methods to accomplish your own tasks.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">RDS.DataControl</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">RDS provides a means to combine the functionality of the <legacyBold>RDS.DataSpace</legacyBold> and <legacyBold>RDSServer.DataFactory</legacyBold>, and also enable visual controls to easily use the <legacyBold>Recordset</legacyBold> object returned by a query from a data source.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> RDS attempts, for the most common case, to do as much as possible to automatically gain access to information on a server and display it in a visual control.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src31" class="srcSentence">The RDS object model embodies this functionality with the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">The <legacyBold>RDS.DataControl</legacyBold> has two aspects.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> One aspect pertains to the data source.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> If you set the command and connection information using the <legacyBold>Connect</legacyBold> and <legacyBold>SQL</legacyBold> properties of the <legacyBold>RDS.DataControl</legacyBold>, it will automatically use the <legacyBold>RDS.DataSpace</legacyBold> to create a reference to the default <legacyBold>RDSServer.DataFactory</legacyBold> object.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> Then the <legacyBold>RDSServer.DataFactory</legacyBold> will use the <legacyBold>Connect</legacyBold> property value to connect to the data source, use the <legacyBold>SQL</legacyBold> property value to obtain a <legacyBold>Recordset</legacyBold> from the data source, and return the <legacyBold>Recordset</legacyBold> object to the <legacyBold>RDS.DataControl</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src36" class="srcSentence">The second aspect pertains to the display of returned <legacyBold>Recordset</legacyBold> information in a visual control.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> You can associate a visual control with the <legacyBold>RDS.DataControl</legacyBold> (in a process called binding) and gain access to the information in the associated <legacyBold>Recordset</legacyBold> object, displaying query results on a Web page in Microsoft® Internet Explorer.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> Each <legacyBold>RDS.DataControl</legacyBold> object binds one <legacyBold>Recordset</legacyBold> object, representing the results of a single query, to one or more visual controls (for example, a text box, combo box, grid control, and so forth).</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> There may be more than one <legacyBold>RDS.DataControl</legacyBold> object on each page.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> Each <legacyBold>RDS.DataControl</legacyBold> object can be connected to a different data source and contain the results of a separate query.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src41" class="srcSentence">The <legacyBold>RDS.DataControl</legacyBold> object also has its own methods for navigating, sorting, and filtering the rows of the associated <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> These methods are similar, but not the same as the methods on the ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src43" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src44" class="srcSentence">RDS supports two of its own events, which are independent of the ADO event model.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> The <legacyLink xlink:href="bf2ae3ac-bfe4-4709-b50a-ea7c282c3164">onReadyStateChange</legacyLink> event is called whenever the <legacyBold>RDS.DataControl</legacyBold> <legacyLink xlink:href="5be75bc7-1171-4440-a37e-c8cc6b5cd865">ReadyState</legacyLink> property changes, thus notifying you when an asynchronous operation has successfully completed, terminated, or experienced an error.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> The <legacyLink xlink:href="b01cbc62-fbd7-4068-b16c-8b0f80a05887">onError</legacyLink> event is called whenever an error occurs, even if the error occurs during an asynchronous operation.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src47" class="srcSentence">Microsoft Internet Explorer provides two additional events to RDS: <legacyBold>onDataSetChanged</legacyBold>, which indicates that the <legacyBold>Recordset</legacyBold> is functional but still retrieving rows, and <legacyBold>onDataSetComplete</legacyBold>, which indicates that the <legacyBold>Recordset</legacyBold> has finished retrieving rows.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="07ce0ef0-72f1-48f4-823d-1b65d28c0926">RDS Programming Model with Objects</link>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
        <link xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace Object (RDS)</link>
        <link xlink:href="a7dcad87-aaf0-4b02-9660-472f8469761c">RDS Scenario</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="b8ac3739-05d3-4818-8201-a763795fb8b4">Using RDS</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
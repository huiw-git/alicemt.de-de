---
title: "Absolute and Relative URLs"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf
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
# Absolute and Relative URLs
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d0e2092f7ea356323f27d7c25a9240de" id="tgt1" class="tgtSentence">A URL specifies the location of a target stored on a local or networked computer.</caps:sentence>
          <caps:sentence sentenceid="4f061fb19e95524634e58e855e0007a4" id="tgt2" class="tgtSentence"> The target can be a file, directory, HTML page, image, program, and so on<legacyItalic>.</legacyItalic></caps:sentence> </para>
        <para>
          <caps:sentence sentenceid="c08c0e0398c9cc77c809f135a611da95" id="tgt3" class="tgtSentence">An <legacyItalic>absolute URL</legacyItalic> contains all the information necessary to locate a resource.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b037e2c8b0eab2c78e7336da1483e51e" id="tgt4" class="tgtSentence">A <legacyItalic>relative URL</legacyItalic> locates a resource using an absolute URL as a starting point.</caps:sentence>
          <caps:sentence sentenceid="44bbb962ea467f657675eda7b946040c" id="tgt5" class="tgtSentence"> In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e405be16676b30e05d72d289a8a3b008" id="tgt6" class="tgtSentence">An <legacyItalic>absolute URL</legacyItalic> uses the following format: <legacyItalic>scheme://server/path/resource</legacyItalic></caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f4dc1dfff6a5d05afdbbb0ca04d2ebbf" id="tgt7" class="tgtSentence">A relative URL typically consists only of the <legacyItalic>path</legacyItalic>, and optionally, the <legacyItalic>resource</legacyItalic>, but no <legacyItalic>scheme</legacyItalic> or <legacyItalic>server</legacyItalic>.</caps:sentence>
          <caps:sentence sentenceid="1906e41595aee14438c93e241220fd71" id="tgt8" class="tgtSentence"> The following tables define the individual parts of the complete URL format.</caps:sentence>
        </para>
        <definitionTable>
          <definedTerm>
            <caps:sentence sentenceid="0649af320abf81c4aa18221c2950b16c" id="tgt9" class="tgtSentence"> <legacyItalic>scheme</legacyItalic> </caps:sentence>
          </definedTerm>
          <definition>
            <para>
              <caps:sentence sentenceid="83d44c3587dae47fc0dba79043b78045" id="tgt10" class="tgtSentence">Specifies how the <legacyItalic>resource</legacyItalic> is to be accessed.</caps:sentence>
            </para>
          </definition>
          <definedTerm>
            <caps:sentence sentenceid="40a6d661d5720c00fb2c4db928148127" id="tgt11" class="tgtSentence"> <legacyItalic>server</legacyItalic> </caps:sentence>
          </definedTerm>
          <definition>
            <para>
              <caps:sentence sentenceid="386471b77d831f0441fa7f9285928586" id="tgt12" class="tgtSentence">Specifies the name of the computer where the <legacyItalic>resource</legacyItalic> is located.</caps:sentence>
            </para>
          </definition>
          <definedTerm>
            <caps:sentence sentenceid="e06b226c8ed8386843878479e2981bce" id="tgt13" class="tgtSentence"> <legacyItalic>path</legacyItalic> </caps:sentence>
          </definedTerm>
          <definition>
            <para>
              <caps:sentence sentenceid="30e2c6f0499f72ad4a63ba9ac63ef5cb" id="tgt14" class="tgtSentence">Specifies the sequence of directories leading to the target.</caps:sentence>
              <caps:sentence sentenceid="de2bb94651c960289dc129774d4499f5" id="tgt15" class="tgtSentence"> If <legacyItalic>resource</legacyItalic> is omitted, the target is the last directory in <legacyItalic>path</legacyItalic>.</caps:sentence>
            </para>
          </definition>
          <definedTerm>
            <caps:sentence sentenceid="7f7079d8ffcc13cf84ab12754dde2ec2" id="tgt16" class="tgtSentence"> <legacyItalic>resource</legacyItalic> </caps:sentence>
          </definedTerm>
          <definition>
            <para>
              <caps:sentence sentenceid="1ef2da10c0710dcb4199bb19f21a0363" id="tgt17" class="tgtSentence">If included, <legacyItalic>resource</legacyItalic> is the target, and is typically the name of a file.</caps:sentence>
              <caps:sentence sentenceid="9d06e0dd7d692155e33e90a3ba4937f3" id="tgt18" class="tgtSentence"> It may be a <legacyItalic>simple file,</legacyItalic> containing a single binary stream of bytes, or a <legacyItalic>structured document,</legacyItalic> containing one or more storages and binary streams of bytes.</caps:sentence>
            </para>
          </definition>
        </definitionTable>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="24dc1a7d7288e3387e7f7a0b8924c676" id="tgt19" class="tgtSentence">URL Scheme Registration</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ad2816d2f99469745228923939bcd1a8" id="tgt20" class="tgtSentence">If a provider supports URLs, the provider will register one or more URL schemes.</caps:sentence>
            <caps:sentence sentenceid="2208f1f43c3fba857299be36e95b1347" id="tgt21" class="tgtSentence"> Registration means that any URLs using the scheme will automatically invoke the registered provider.</caps:sentence>
            <caps:sentence sentenceid="6958bcd242a1db6ddb029e27a8c5045f" id="tgt22" class="tgtSentence"> For example, the <legacyItalic>http</legacyItalic> scheme is registered to the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="178038f452c8556254a8da80b638e702" id="tgt23" class="tgtSentence"> ADO assumes all URLs prefixed with "http" represent Web folders or files to be used with the Internet Publishing Provider.</caps:sentence>
            <caps:sentence sentenceid="f427800fa1ed2a6e0e5acb8da4024b38" id="tgt24" class="tgtSentence"> For information about the schemes registered by your provider, see your provider documentation.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="75505923690af308be4c5e97cf770b61" id="tgt25" class="tgtSentence">Defining Context with a URL</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="dd427078580d253f799a3db6b0dd2039" id="tgt26" class="tgtSentence">One function of an open connection, represented by a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, is to restrict subsequent operations to the data source represented by that connection.</caps:sentence>
            <caps:sentence sentenceid="682f264c250086b1e76f22ed7393b498" id="tgt27" class="tgtSentence"> That is, the connection defines the context for subsequent operations.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6db61213a155fa724aa12416b792b511" id="tgt28" class="tgtSentence">With ADO 2.7 or later, an absolute URL can also define a context.</caps:sentence>
            <caps:sentence sentenceid="1c238e634bb793d9f470ec50afa08035" id="tgt29" class="tgtSentence"> For example, when a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object is opened with an absolute URL, a <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object is implicitly created to represent the resource specified by the URL.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8455dcafd89622b90d24bad9241a56a6" id="tgt30" class="tgtSentence">An absolute URL that defines a context can be specified in the <parameterReference>ActiveConnection</parameterReference> parameter of the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="02b6ddfad6a6ffd3afdc9e7eb53cfb92" id="tgt31" class="tgtSentence"> An absolute URL can also be specified as the value of the "URL<legacyBold>=</legacyBold>" keyword in the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method <parameterReference>ConnectionString</parameterReference> parameter, and the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method <legacyItalic>ActiveConnection</legacyItalic> parameter.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="05f8ac7a65e551b1d7fa66bae2f693c7" id="tgt32" class="tgtSentence">Context can also be defined by opening a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object that represents a directory, because these objects already have an implicitly or explicitly declared <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object that specifies context.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="80134f13d02561ee7d49c9ae5012d5e6" id="tgt33" class="tgtSentence">Scoped Operations</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8e0ca6c118e8194077ae8c1fc37d4dbf" id="tgt34" class="tgtSentence">The context also defines scope—that is, the directory and its subdirectories that can participate in subsequent operations.</caps:sentence>
            <caps:sentence sentenceid="fcab670c725d2bb9fb577117e34eca6b" id="tgt35" class="tgtSentence"> The <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object has several scoped methods that operate on a directory and all its subdirectories.</caps:sentence>
            <caps:sentence sentenceid="e2ad3a3ebecf93b339eef1dfcac4c9ef" id="tgt36" class="tgtSentence"> These methods include <legacyLink xlink:href="b9bcf272-3c74-479f-95dd-0229a32e98fc">CopyRecord</legacyLink>, <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord</legacyLink>, and <legacyLink xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5475edf57f3ad8bfd7f1f9c70c1a24d9" id="tgt37" class="tgtSentence">Relative URLs as Command Text</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="500f0f466a03624b6cd7b1a440f64e79" id="tgt38" class="tgtSentence">You can specify a command to be executed on the data source by typing a string in the <legacyItalic>CommandText</legacyItalic> parameter of the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method, and in the <parameterReference>Source</parameterReference> parameter of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object's <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9b803dd1634473d9d2117925ab05db02" id="tgt39" class="tgtSentence">A relative URL can be specified in the <parameterReference>CommandText</parameterReference> or <parameterReference>Source</parameterReference> parameter.</caps:sentence>
            <caps:sentence sentenceid="7bbc408991631868829ad626487c6e0d" id="tgt40" class="tgtSentence"> The relative URL does not actually represent a command, such as an SQL command; it merely specifies the parameters.</caps:sentence>
            <caps:sentence sentenceid="a6b52919df82a6cc06ee6504b8981311" id="tgt41" class="tgtSentence"> The context of the active connection must be an absolute URL, and the <parameterReference>Option</parameterReference> parameter must be set to <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e3576a1402267ca2388f826e76d99d1e" id="tgt42" class="tgtSentence">For example, the following code sample shows how to open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> on the Readme25.txt file of the Winnt/system32 directory:</caps:sentence>
          </para>
          <code>recordset.Open "system32/Readme25.txt", "URL=http://YourServer/Winnt/",,,adCmdTableDirect</code>
          <para>
            <caps:sentence sentenceid="6eb776e410e0b9419a51cd68f9458803" id="tgt43" class="tgtSentence">The absolute URL in the connection string specifies the server (<codeInline>YourServer</codeInline>) and the path (<codeInline>Winnt</codeInline>).</caps:sentence>
            <caps:sentence sentenceid="01aa0fefa2d55e0104d399a4cabd3c07" id="tgt44" class="tgtSentence"> This URL also defines the context.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bf8556f8db1c8ee3e40db33b62a967f8" id="tgt45" class="tgtSentence">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (<codeInline>system32</codeInline>) and the file to open (<codeInline>Readme25.txt</codeInline>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="23fe2ff9b3a8adfbabcac4e5e686ec46" id="tgt46" class="tgtSentence">The options field (<codeInline>adCmdTableDirect</codeInline>) indicates that the command type is a relative URL.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="12ca36d22023d6702da5914dc418b30c" id="tgt47" class="tgtSentence">As another example, the following code will open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> on the contents of the <codeInline>Winnt</codeInline> directory:</caps:sentence>
          </para>
          <code>recordset.Open "", "URL=http://YourServer/Winnt/",,,adCmdTableDirect</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="db0c09cac2c879dc46fc8e161760246e" id="tgt48" class="tgtSentence">OLE DB Provider-Supplied URL Schemes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cb68a1ac2420e84968dfeb9ce7eea39b" id="tgt49" class="tgtSentence">The leading part of a fully-qualified URL is the <newTerm>scheme</newTerm> that is used to access the resource identified by the remainder of the URL.</caps:sentence>
            <caps:sentence sentenceid="b88034e57d4e358db401f7bafd5a9cd9" id="tgt50" class="tgtSentence"> Examples are HTTP (Hypertext Transfer Protocol) and FTP (File Transfer Protocol).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8190d7526a4cc8a6b668ba177515067e" id="tgt51" class="tgtSentence">ADO supports OLE DB providers that recognize their own URL schemes.</caps:sentence>
            <caps:sentence sentenceid="9fcc019327fbbee7ab525d064c5e4217" id="tgt52" class="tgtSentence"> For example, the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink><legacyItalic>,</legacyItalic> which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">A URL specifies the location of a target stored on a local or networked computer.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The target can be a file, directory, HTML page, image, program, and so on<legacyItalic>.</legacyItalic></caps:sentence> </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">An <legacyItalic>absolute URL</legacyItalic> contains all the information necessary to locate a resource.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">A <legacyItalic>relative URL</legacyItalic> locates a resource using an absolute URL as a starting point.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">An <legacyItalic>absolute URL</legacyItalic> uses the following format: <legacyItalic>scheme://server/path/resource</legacyItalic></caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">A relative URL typically consists only of the <legacyItalic>path</legacyItalic>, and optionally, the <legacyItalic>resource</legacyItalic>, but no <legacyItalic>scheme</legacyItalic> or <legacyItalic>server</legacyItalic>.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The following tables define the individual parts of the complete URL format.</caps:sentence>
        </para>
        <definitionTable>
          <definedTerm>
            <caps:sentence id="src9" class="srcSentence"> <legacyItalic>scheme</legacyItalic> </caps:sentence>
          </definedTerm>
          <definition>
            <para>
              <caps:sentence id="src10" class="srcSentence">Specifies how the <legacyItalic>resource</legacyItalic> is to be accessed.</caps:sentence>
            </para>
          </definition>
          <definedTerm>
            <caps:sentence id="src11" class="srcSentence"> <legacyItalic>server</legacyItalic> </caps:sentence>
          </definedTerm>
          <definition>
            <para>
              <caps:sentence id="src12" class="srcSentence">Specifies the name of the computer where the <legacyItalic>resource</legacyItalic> is located.</caps:sentence>
            </para>
          </definition>
          <definedTerm>
            <caps:sentence id="src13" class="srcSentence"> <legacyItalic>path</legacyItalic> </caps:sentence>
          </definedTerm>
          <definition>
            <para>
              <caps:sentence id="src14" class="srcSentence">Specifies the sequence of directories leading to the target.</caps:sentence>
              <caps:sentence id="src15" class="srcSentence"> If <legacyItalic>resource</legacyItalic> is omitted, the target is the last directory in <legacyItalic>path</legacyItalic>.</caps:sentence>
            </para>
          </definition>
          <definedTerm>
            <caps:sentence id="src16" class="srcSentence"> <legacyItalic>resource</legacyItalic> </caps:sentence>
          </definedTerm>
          <definition>
            <para>
              <caps:sentence id="src17" class="srcSentence">If included, <legacyItalic>resource</legacyItalic> is the target, and is typically the name of a file.</caps:sentence>
              <caps:sentence id="src18" class="srcSentence"> It may be a <legacyItalic>simple file,</legacyItalic> containing a single binary stream of bytes, or a <legacyItalic>structured document,</legacyItalic> containing one or more storages and binary streams of bytes.</caps:sentence>
            </para>
          </definition>
        </definitionTable>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src19" class="srcSentence">URL Scheme Registration</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src20" class="srcSentence">If a provider supports URLs, the provider will register one or more URL schemes.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> Registration means that any URLs using the scheme will automatically invoke the registered provider.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> For example, the <legacyItalic>http</legacyItalic> scheme is registered to the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> ADO assumes all URLs prefixed with "http" represent Web folders or files to be used with the Internet Publishing Provider.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> For information about the schemes registered by your provider, see your provider documentation.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src25" class="srcSentence">Defining Context with a URL</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src26" class="srcSentence">One function of an open connection, represented by a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, is to restrict subsequent operations to the data source represented by that connection.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> That is, the connection defines the context for subsequent operations.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">With ADO 2.7 or later, an absolute URL can also define a context.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> For example, when a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object is opened with an absolute URL, a <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object is implicitly created to represent the resource specified by the URL.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src30" class="srcSentence">An absolute URL that defines a context can be specified in the <parameterReference>ActiveConnection</parameterReference> parameter of the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> An absolute URL can also be specified as the value of the "URL<legacyBold>=</legacyBold>" keyword in the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method <parameterReference>ConnectionString</parameterReference> parameter, and the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method <legacyItalic>ActiveConnection</legacyItalic> parameter.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">Context can also be defined by opening a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object that represents a directory, because these objects already have an implicitly or explicitly declared <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object that specifies context.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src33" class="srcSentence">Scoped Operations</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src34" class="srcSentence">The context also defines scope—that is, the directory and its subdirectories that can participate in subsequent operations.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> The <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object has several scoped methods that operate on a directory and all its subdirectories.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> These methods include <legacyLink xlink:href="b9bcf272-3c74-479f-95dd-0229a32e98fc">CopyRecord</legacyLink>, <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord</legacyLink>, and <legacyLink xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src37" class="srcSentence">Relative URLs as Command Text</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src38" class="srcSentence">You can specify a command to be executed on the data source by typing a string in the <legacyItalic>CommandText</legacyItalic> parameter of the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method, and in the <parameterReference>Source</parameterReference> parameter of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object's <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src39" class="srcSentence">A relative URL can be specified in the <parameterReference>CommandText</parameterReference> or <parameterReference>Source</parameterReference> parameter.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> The relative URL does not actually represent a command, such as an SQL command; it merely specifies the parameters.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> The context of the active connection must be an absolute URL, and the <parameterReference>Option</parameterReference> parameter must be set to <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src42" class="srcSentence">For example, the following code sample shows how to open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> on the Readme25.txt file of the Winnt/system32 directory:</caps:sentence>
          </para>
          <code>recordset.Open "system32/Readme25.txt", "URL=http://YourServer/Winnt/",,,adCmdTableDirect</code>
          <para>
            <caps:sentence id="src43" class="srcSentence">The absolute URL in the connection string specifies the server (<codeInline>YourServer</codeInline>) and the path (<codeInline>Winnt</codeInline>).</caps:sentence>
            <caps:sentence id="src44" class="srcSentence"> This URL also defines the context.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src45" class="srcSentence">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (<codeInline>system32</codeInline>) and the file to open (<codeInline>Readme25.txt</codeInline>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src46" class="srcSentence">The options field (<codeInline>adCmdTableDirect</codeInline>) indicates that the command type is a relative URL.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src47" class="srcSentence">As another example, the following code will open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> on the contents of the <codeInline>Winnt</codeInline> directory:</caps:sentence>
          </para>
          <code>recordset.Open "", "URL=http://YourServer/Winnt/",,,adCmdTableDirect</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src48" class="srcSentence">OLE DB Provider-Supplied URL Schemes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src49" class="srcSentence">The leading part of a fully-qualified URL is the <newTerm>scheme</newTerm> that is used to access the resource identified by the remainder of the URL.</caps:sentence>
            <caps:sentence id="src50" class="srcSentence"> Examples are HTTP (Hypertext Transfer Protocol) and FTP (File Transfer Protocol).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src51" class="srcSentence">ADO supports OLE DB providers that recognize their own URL schemes.</caps:sentence>
            <caps:sentence id="src52" class="srcSentence"> For example, the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink><legacyItalic>,</legacyItalic> which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
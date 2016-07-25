---
title: "Records and Streams"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4d68868e-2611-4b5c-9a89-7caa5f753151
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
# Records and Streams
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="288c08736ee75b172b035c0ff4fbb185" id="tgt1" class="tgtSentence">ADO currently provides the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object as the primary means of accessing information in data sources, such as relational databases.</caps:sentence>
          <caps:sentence sentenceid="ae4cdcf560d83755b4a874fc1b9e96f3" id="tgt2" class="tgtSentence"> However, some providers support the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> and <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects as alternative or complementary objects with which data from providers can be manipulated.</caps:sentence>
          <caps:sentence sentenceid="facdc448b7c53649debb000b2e5c5671" id="tgt3" class="tgtSentence"> For specifics on <legacyBold>Record</legacyBold> behavior, see your provider's documentation.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6e52c40bb8fc91ff39ee5c79b4211f67" id="tgt4" class="tgtSentence">Records</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b6ce6ea1b61768d0776a2b1de0fea063" id="tgt5" class="tgtSentence">
              <legacyBold>Record</legacyBold> objects essentially function as one-row <legacyBold>Recordset</legacyBold>s.</caps:sentence>
            <caps:sentence sentenceid="c8805da8848649d803971a3d439a27df" id="tgt6" class="tgtSentence"> However, <legacyBold>Records</legacyBold> have limited functionality compared to <legacyBold>Recordsets</legacyBold> and they have different properties and methods.The source for the data in a <legacyBold>Record</legacyBold> object can be a command which returns one row of data from the provider.</caps:sentence>
            <caps:sentence sentenceid="e6ebdd97b31820fc9087a51512792b0e" id="tgt7" class="tgtSentence"> Using <legacyBold>Record</legacyBold> objects rather than <legacyBold>Recordset</legacyBold> objects to receive the results from a query that returns one row of data eliminates the overhead of instantiating the more complex <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2ae5996ed9cab007ab382021f7662dde" id="tgt8" class="tgtSentence">
              <legacyBold>Record</legacyBold> objects can serve another purpose, particularly with providers for data sources other than traditional relational databases, such as the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="be540be5303fbcfb72b16cc867ab8021" id="tgt9" class="tgtSentence"> Much of the information that must be processed exists, not as tables in databases, but as messages in electronic mail systems and files in modern file systems.</caps:sentence>
            <caps:sentence sentenceid="730a8e9de1cf06f539d4c1206f42acb2" id="tgt10" class="tgtSentence"> The <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects facilitate access to information stored in sources other than relational databases.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1bdea690a03c4f364cbaa9be29c78c10" id="tgt11" class="tgtSentence">The <legacyBold>Record</legacyBold> object can represent and manage data such as directories and files in a file system or folders and messages in an e-mail system.</caps:sentence>
            <caps:sentence sentenceid="29e6d46a2b7359ff5e9602b5ff9574ae" id="tgt12" class="tgtSentence"> For these purposes, the source for the <legacyBold>Record</legacyBold> can be the current row of an open <legacyBold>Recordset</legacyBold>, an absolute URL, or a relative URL in conjunction with an open <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8ea1967ccbfecb82ced8f1cf25666afa" id="tgt13" class="tgtSentence">Typically, a <legacyBold>Recordset</legacyBold> can be used to represent a container or parent in a hierarchy such as a folder or directory.</caps:sentence>
            <caps:sentence sentenceid="e40b069f365cb3e3ca090093b007118b" id="tgt14" class="tgtSentence"> A <legacyBold>Record</legacyBold> can be used to return specific information about one node in the parent container, such as a file or document.</caps:sentence>
            <caps:sentence sentenceid="f69660f5c0f563be249d2dffcb6af29e" id="tgt15" class="tgtSentence"> The primary reason <legacyBold>Records</legacyBold> are used to represent this type of information is that these sources of data are heterogeneous.</caps:sentence>
            <caps:sentence sentenceid="0900e84c38fc728df54a9b76bf6b8290" id="tgt16" class="tgtSentence"> This means that each <legacyBold>Record</legacyBold> may have a different set and number of fields.</caps:sentence>
            <caps:sentence sentenceid="38865bff2a6b38a1d45870bb7847a6b0" id="tgt17" class="tgtSentence"> Traditional <legacyBold>Recordsets</legacyBold> containing rows from a database are homogenous, which means that each row has the same number and type of fields.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8d3b313179bfb10271aee34c6f122fc8" id="tgt18" class="tgtSentence">For more information about using the <legacyBold>Record</legacyBold> object for processing this heterogeneous data from providers such as the Internet Publishing Provider, see <legacyLink xlink:href="d399fce4-b70b-418f-8110-3deb3448863c">Using ADO for Internet Publishing</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f6f4768f1c2d7c8f1f54823723f1a70" id="tgt19" class="tgtSentence">Streams</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2f0a9de77a4b11f4515c145227d136ca" id="tgt20" class="tgtSentence">The <legacyBold>Stream</legacyBold> object provides the means to read, write, and manage a stream of bytes.</caps:sentence>
            <caps:sentence sentenceid="e0af183b6b858711cbeb4718f94f82ae" id="tgt21" class="tgtSentence"> This byte stream may be text or binary and is limited in size only by system resources.</caps:sentence>
            <caps:sentence sentenceid="3763a4370892987d38738f6bd2ca415b" id="tgt22" class="tgtSentence"> Typically, ADO <legacyBold>Stream</legacyBold> objects are used for the following purposes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="ad74c8bda24ad1e0727b6275a9cb14b0" id="tgt23" class="tgtSentence">To contain the data of a <legacyBold>Recordset</legacyBold> saved in XML format.</caps:sentence>
                <caps:sentence sentenceid="ba1345397228f370d98272eded7c907a" id="tgt24" class="tgtSentence"> These XML streams from saved <legacyBold>Recordset</legacyBold>s can be used as the source when opening a new <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="1469bee53c301c20db8776d97d3e9c84" id="tgt25" class="tgtSentence"> For more information, see <legacyLink xlink:href="ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea">Streams and Persistence</legacyLink>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5bf93fe97f1add0a2b1b4fd1abf9ffae" id="tgt26" class="tgtSentence">To contain <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStreams</legacyLink> to be executed against the provider as an alternative to <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink>.</caps:sentence>
                <caps:sentence sentenceid="48521d95af794149360572490c6a65ed" id="tgt27" class="tgtSentence"> For example, XML UpdateGrams can be used as the source for a command against the Microsoft OLE DB Provider for SQL Server.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="69cb1e176e2fd22e77dbafc792f988a0" id="tgt28" class="tgtSentence">To receive results from the provider in a format other than a <legacyBold>Recordset</legacyBold>, such as XML results from the Microsoft OLE DB Provider for SQL Server.</caps:sentence>
                <caps:sentence sentenceid="9a23a3853853451b48dbfda25b65a1b8" id="tgt29" class="tgtSentence"> For more information, see <legacyLink xlink:href="996c1321-c926-4f57-8297-85c8c20de974">Retrieving Resultsets into Streams</legacyLink>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4ca05d20fa211821f9a7bf3e1d6d903b" id="tgt30" class="tgtSentence">To contain the text or bytes that comprise a file or message, typically used with providers such as the Microsoft OLE DB Provider for Internet Publishing.</caps:sentence>
                <caps:sentence sentenceid="ac8d47dfe949e324b3851945ad69958a" id="tgt31" class="tgtSentence"> For more information about this use of <legacyBold>Stream</legacyBold> objects, see <legacyLink xlink:href="d399fce4-b70b-418f-8110-3deb3448863c">Using ADO for Internet Publishing</legacyLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="b72fca29fc319a64fb2b2dc412a34d6a" id="tgt32" class="tgtSentence">A <legacyBold>Stream</legacyBold> object can be opened on:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="46d7dde0660be417ae71cc57ca302947" id="tgt33" class="tgtSentence">A simple file specified with a URL.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="74bea895b3c5941a146ced8e2ab06437" id="tgt34" class="tgtSentence">A field of a <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> containing a <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="71bb007eaf17e89f8e538e01da8c6d9f" id="tgt35" class="tgtSentence">The default stream of a <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> object representing a directory or compound file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4dd8044d9057ced10e349e52d9660216" id="tgt36" class="tgtSentence">A resource field containing the URL of a simple file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="afcfc6fb8f0f74c2a53318daf65e1b29" id="tgt37" class="tgtSentence">No particular source at all.</caps:sentence>
                <caps:sentence sentenceid="524754354b1cd5962eee0cbff18fc323" id="tgt38" class="tgtSentence"> In this case, a <legacyBold>Stream</legacyBold> object is opened in memory.</caps:sentence>
                <caps:sentence sentenceid="731475b6f63557051a742aab7f1e397b" id="tgt39" class="tgtSentence"> Data can be written to it and then saved in another <legacyBold>Stream</legacyBold> or file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="45125ef3b2e4b0f77bb3f00956417fa8" id="tgt40" class="tgtSentence">A BLOB field in a <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt41" class="tgtSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea">
                  <caps:sentence sentenceid="2f162ac8ecfdc246e2b8c92c3a353242" id="tgt42" class="tgtSentence">Streams and Persistence</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="0ac09dbe-2665-411e-8fbb-d1efe6c777be">
                  <caps:sentence sentenceid="6b4bb8f4cc66f53238288b015efb3533" id="tgt43" class="tgtSentence">Command Streams</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="996c1321-c926-4f57-8297-85c8c20de974">
                  <caps:sentence sentenceid="c8e599416a6b0d3474faa03fc2db149f" id="tgt44" class="tgtSentence">Retrieving Resultsets into Streams</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="d399fce4-b70b-418f-8110-3deb3448863c">
                  <caps:sentence sentenceid="667ff9b76449540cefc57852923a2c26" id="tgt45" class="tgtSentence">Using ADO for Internet Publishing</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO currently provides the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object as the primary means of accessing information in data sources, such as relational databases.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> However, some providers support the <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> and <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects as alternative or complementary objects with which data from providers can be manipulated.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For specifics on <legacyBold>Record</legacyBold> behavior, see your provider's documentation.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Records</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">
              <legacyBold>Record</legacyBold> objects essentially function as one-row <legacyBold>Recordset</legacyBold>s.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> However, <legacyBold>Records</legacyBold> have limited functionality compared to <legacyBold>Recordsets</legacyBold> and they have different properties and methods.The source for the data in a <legacyBold>Record</legacyBold> object can be a command which returns one row of data from the provider.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Using <legacyBold>Record</legacyBold> objects rather than <legacyBold>Recordset</legacyBold> objects to receive the results from a query that returns one row of data eliminates the overhead of instantiating the more complex <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">
              <legacyBold>Record</legacyBold> objects can serve another purpose, particularly with providers for data sources other than traditional relational databases, such as the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Much of the information that must be processed exists, not as tables in databases, but as messages in electronic mail systems and files in modern file systems.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects facilitate access to information stored in sources other than relational databases.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">The <legacyBold>Record</legacyBold> object can represent and manage data such as directories and files in a file system or folders and messages in an e-mail system.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> For these purposes, the source for the <legacyBold>Record</legacyBold> can be the current row of an open <legacyBold>Recordset</legacyBold>, an absolute URL, or a relative URL in conjunction with an open <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">Typically, a <legacyBold>Recordset</legacyBold> can be used to represent a container or parent in a hierarchy such as a folder or directory.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> A <legacyBold>Record</legacyBold> can be used to return specific information about one node in the parent container, such as a file or document.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The primary reason <legacyBold>Records</legacyBold> are used to represent this type of information is that these sources of data are heterogeneous.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> This means that each <legacyBold>Record</legacyBold> may have a different set and number of fields.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Traditional <legacyBold>Recordsets</legacyBold> containing rows from a database are homogenous, which means that each row has the same number and type of fields.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">For more information about using the <legacyBold>Record</legacyBold> object for processing this heterogeneous data from providers such as the Internet Publishing Provider, see <legacyLink xlink:href="d399fce4-b70b-418f-8110-3deb3448863c">Using ADO for Internet Publishing</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src19" class="srcSentence">Streams</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src20" class="srcSentence">The <legacyBold>Stream</legacyBold> object provides the means to read, write, and manage a stream of bytes.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> This byte stream may be text or binary and is limited in size only by system resources.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Typically, ADO <legacyBold>Stream</legacyBold> objects are used for the following purposes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">To contain the data of a <legacyBold>Recordset</legacyBold> saved in XML format.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> These XML streams from saved <legacyBold>Recordset</legacyBold>s can be used as the source when opening a new <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> For more information, see <legacyLink xlink:href="ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea">Streams and Persistence</legacyLink>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src26" class="srcSentence">To contain <legacyLink xlink:href="f78f61b6-87e0-48dc-961e-83d0e20da58e">CommandStreams</legacyLink> to be executed against the provider as an alternative to <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink>.</caps:sentence>
                <caps:sentence id="src27" class="srcSentence"> For example, XML UpdateGrams can be used as the source for a command against the Microsoft OLE DB Provider for SQL Server.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src28" class="srcSentence">To receive results from the provider in a format other than a <legacyBold>Recordset</legacyBold>, such as XML results from the Microsoft OLE DB Provider for SQL Server.</caps:sentence>
                <caps:sentence id="src29" class="srcSentence"> For more information, see <legacyLink xlink:href="996c1321-c926-4f57-8297-85c8c20de974">Retrieving Resultsets into Streams</legacyLink>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">To contain the text or bytes that comprise a file or message, typically used with providers such as the Microsoft OLE DB Provider for Internet Publishing.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> For more information about this use of <legacyBold>Stream</legacyBold> objects, see <legacyLink xlink:href="d399fce4-b70b-418f-8110-3deb3448863c">Using ADO for Internet Publishing</legacyLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src32" class="srcSentence">A <legacyBold>Stream</legacyBold> object can be opened on:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">A simple file specified with a URL.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">A field of a <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> containing a <legacyBold>Stream</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">The default stream of a <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> object representing a directory or compound file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">A resource field containing the URL of a simple file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src37" class="srcSentence">No particular source at all.</caps:sentence>
                <caps:sentence id="src38" class="srcSentence"> In this case, a <legacyBold>Stream</legacyBold> object is opened in memory.</caps:sentence>
                <caps:sentence id="src39" class="srcSentence"> Data can be written to it and then saved in another <legacyBold>Stream</legacyBold> or file.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src40" class="srcSentence">A BLOB field in a <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src41" class="srcSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea">
                  <caps:sentence id="src42" class="srcSentence">Streams and Persistence</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="0ac09dbe-2665-411e-8fbb-d1efe6c777be">
                  <caps:sentence id="src43" class="srcSentence">Command Streams</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="996c1321-c926-4f57-8297-85c8c20de974">
                  <caps:sentence id="src44" class="srcSentence">Retrieving Resultsets into Streams</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="d399fce4-b70b-418f-8110-3deb3448863c">
                  <caps:sentence id="src45" class="srcSentence">Using ADO for Internet Publishing</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
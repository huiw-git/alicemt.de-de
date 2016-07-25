---
title: "Record Object (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: db83ed2c-a8e3-460c-8682-64667e4d5d01
caps.latest.revision: 5
caps.handback.revision: 5
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
# Record Object (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c389d9e042e1672d0f3c812e10e6f5de" id="tgt1" class="tgtSentence">Represents a row from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> or the data provider, or an object returned by a semi-structured data provider, such as a file or directory.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1db26d8b18072e8d937cf33256b938e1" id="tgt2" class="tgtSentence">A <legacyBold>Record</legacyBold> object represents one row of data, and has some conceptual similarities with a one-row <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="a14932c532e429a5fe6bcfb522d03321" id="tgt3" class="tgtSentence"> Depending on the capabilities of your provider, <legacyBold>Record</legacyBold> objects may be returned directly from your provider instead of a one-row <legacyBold>Recordset</legacyBold>, for example when an SQL query that selects only one row is executed.</caps:sentence>
            <caps:sentence sentenceid="46256d421fa933e1232e10e3f8c9416c" id="tgt4" class="tgtSentence"> Or, a <legacyBold>Record</legacyBold> object can be obtained directly from a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="58a4e78ec9f708a932bcb9bace3e7010" id="tgt5" class="tgtSentence"> Or, a <legacyBold>Record</legacyBold> can be returned directly from a provider to semi-structured data, such as the Microsoft Exchange OLE DB provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="311fb8080dd2421f98304aae86663646" id="tgt6" class="tgtSentence">You can view the fields associated with the <legacyBold>Record</legacyBold> object by way of the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection on the <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="ce6ca785d97d91be4aa98bd69f8d977e" id="tgt7" class="tgtSentence"> ADO allows object-valued columns including <legacyBold>Recordset</legacyBold>, <legacyBold>SafeArray</legacyBold>, and scalar values in the <legacyBold>Fields</legacyBold> collection of <legacyBold>Record</legacyBold> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="87ab7044b66c2972fd86fc5cbbfda157" id="tgt8" class="tgtSentence">If the <legacyBold>Record</legacyBold> object represents a row in a <legacyBold>Recordset</legacyBold>, it is possible to return to that original <legacyBold>Recordset</legacyBold> with the <legacyLink xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2528e5ec0d43144bec5845dea1642781" id="tgt9" class="tgtSentence">The <legacyBold>Record</legacyBold> object can also be used by semi-structured data providers such as the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>, to model tree-structured namespaces.</caps:sentence>
            <caps:sentence sentenceid="5c5330c81b138a3ef0f9d9971e07f78f" id="tgt10" class="tgtSentence"> Each node in the tree is a <legacyBold>Record</legacyBold> object with associated columns.</caps:sentence>
            <caps:sentence sentenceid="1da64dd2aec63f8bc1786c7f52ea1d54" id="tgt11" class="tgtSentence"> The columns can represent the attributes of that node and other relevant information.</caps:sentence>
            <caps:sentence sentenceid="13e33856d91682051fe5c6d0a9a63136" id="tgt12" class="tgtSentence"> The <legacyBold>Record</legacyBold> object can represent both a leaf node and a non-leaf node in the tree structure.</caps:sentence>
            <caps:sentence sentenceid="955189d1f2c9db48fde59145d72ba9c0" id="tgt13" class="tgtSentence"> Non-leaf nodes have other nodes as their contents, but leaf nodes do not have such contents.</caps:sentence>
            <caps:sentence sentenceid="212901e506828a4d104702a285974b44" id="tgt14" class="tgtSentence"> Leaf nodes typically contain binary streams of data and non-leaf nodes may also have a default binary stream associated with them.</caps:sentence>
            <caps:sentence sentenceid="01c2576d61556ac4b5baf7bfd7db024f" id="tgt15" class="tgtSentence"> Properties on the <legacyBold>Record</legacyBold> object identify the type of node.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="47fb79b4b2e55490036a248fef7de16f" id="tgt16" class="tgtSentence">The <legacyBold>Record</legacyBold> object also represents an alternative way for navigating hierarchically organized data.</caps:sentence>
            <caps:sentence sentenceid="2a73cf6d60cd77d2ca5440b67648a208" id="tgt17" class="tgtSentence"> A <legacyBold>Record</legacyBold> object may be created to represent the root of a specific sub-tree in a large tree structure and new <legacyBold>Record</legacyBold> objects may be opened to represent child nodes.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7cf11478fdd48d3419d4ac568bb38b04" id="tgt18" class="tgtSentence">A resource (for example, a file or directory) can be uniquely identified by an absolute URL.</caps:sentence>
            <caps:sentence sentenceid="15675600348eb4f7941bb0ba3444ea65" id="tgt19" class="tgtSentence"> A <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object is implicitly created and set to the <legacyBold>Record</legacyBold> object when the <legacyBold>Record</legacyBold> is opened by using an absolute URL.</caps:sentence>
            <caps:sentence sentenceid="173b6aa7d79172e63a1c19473655f812" id="tgt20" class="tgtSentence"> A <legacyBold>Connection</legacyBold> object may explicitly be set to the <legacyBold>Record</legacyBold> object via the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property.</caps:sentence>
            <caps:sentence sentenceid="fdca42c38ff2457fdd998e3301c1379e" id="tgt21" class="tgtSentence"> The files and directories that can be accessed by using the <legacyBold>Connection</legacyBold> object define the <legacyItalic>context</legacyItalic> in which <legacyBold>Record</legacyBold> operations may occur.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d6ba001132b5d0a0b72705328bb141ff" id="tgt22" class="tgtSentence">Data modification and navigation methods on the <legacyBold>Record</legacyBold> object also accept a relative URL, which locates a resource using an absolute URL or the <legacyBold>Connection</legacyBold> object context as a starting point.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt23" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt24" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="6ca032d9308085ecc68c0af3fc0ac83c" id="tgt25" class="tgtSentence">A <legacyBold>Connection</legacyBold> object is associated with each <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="ca61ced9ac21b44d4eeb4ef13e371099" id="tgt26" class="tgtSentence"> Therefore, <legacyBold>Record</legacyBold> object operations can be part of a transaction by invoking <legacyBold>Connection</legacyBold> object transaction methods.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="23dcfb87fbff8cdc944e21b90ef56554" id="tgt27" class="tgtSentence">The <legacyBold>Record</legacyBold> object does not support ADO events, and therefore will not respond to notifications.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4a333e0abb5536bea7e1b366a636d906" id="tgt28" class="tgtSentence">With the methods and properties of a <legacyBold>Record</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="b7cc8ddfb06459b79eb21006620592c5" id="tgt29" class="tgtSentence">Set or return the associated <legacyBold>Connection</legacyBold> object with the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="97125c4ae499d88883dcac335b54b0cb" id="tgt30" class="tgtSentence">Indicate access permissions with the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="efdb5c4a9e1d8a1b34abc07d560a692f" id="tgt31" class="tgtSentence">Return the URL of the directory, if any, that contains the resource represented by the <legacyBold>Record</legacyBold> with the <legacyLink xlink:href="65120ce6-3900-4cd4-b322-3b9816d74737">ParentURL</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1708bb6758030778bce9eb9d4400bbac" id="tgt32" class="tgtSentence">Indicate the absolute URL, relative URL, or <legacyBold>Recordset</legacyBold> from which the <legacyBold>Record</legacyBold> is derived with the <legacyLink xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d073a42aae6983b32688a88f7edcc7b7" id="tgt33" class="tgtSentence">Indicate the current status of the <legacyBold>Record</legacyBold> with the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="347e1fd58bf29f5ec3d654e0c798ea39" id="tgt34" class="tgtSentence">Indicate the type of <legacyBold>Record</legacyBold> — <legacyItalic>simple</legacyItalic>, <legacyItalic>collection</legacyItalic>, or <legacyItalic>structured document</legacyItalic> — with the <legacyLink xlink:href="790e46a2-13d2-451e-a8be-130bd9a206a4">RecordType</legacyLink>property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fbc371776ace246253f666b04a2ae2fb" id="tgt35" class="tgtSentence">Stop execution of an asynchronous operation with the <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5096551890adc879040185aa892988ee" id="tgt36" class="tgtSentence">Disassociate the <legacyBold>Record</legacyBold> from a data source with the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="991c6b223540ee5380873e940bc0c3af" id="tgt37" class="tgtSentence">Copy the file or directory represented by a <legacyBold>Record</legacyBold> to another location with the <legacyLink xlink:href="b9bcf272-3c74-479f-95dd-0229a32e98fc">CopyRecord</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9973724ffa2db04c03ab5c7461289934" id="tgt38" class="tgtSentence">Delete the file, or directory and subdirectories, represented by a <legacyBold>Record</legacyBold> with the <legacyLink xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7152a61db24c6c84b80a1e1ef8e714d9" id="tgt39" class="tgtSentence">Open a <legacyBold>Recordset</legacyBold> that contains rows that represent the subdirectories and files of the entity represented by the <legacyBold>Record</legacyBold> with the <legacyLink xlink:href="b3f09bac-4f66-49f6-aa5a-6fbb4fb28338">GetChildren</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1cb564ffb59ea420c9f9ea9a6a2107c0" id="tgt40" class="tgtSentence">Move (rename) the file, or directory and subdirectories, represented by a <legacyBold>Record</legacyBold> to another location with the <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="56edb44a24f4e1fc0ffd940e25c1a1aa" id="tgt41" class="tgtSentence">Associate the <legacyBold>Record</legacyBold> with an existing data source, or create a new file or directory with the <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="d8696bd6fd7bec6baf7de168da0bac15" id="tgt42" class="tgtSentence">The <legacyBold>Record</legacyBold> object is safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt43" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="cbf6f6fd88090991aeae18b345514efb" id="tgt44" class="tgtSentence">             <legacyLink xlink:href="dadde268-bd0f-4ba0-8775-83a5cd3e258a">Record Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">Records and Streams</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a row from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> or the data provider, or an object returned by a semi-structured data provider, such as a file or directory.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <legacyBold>Record</legacyBold> object represents one row of data, and has some conceptual similarities with a one-row <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Depending on the capabilities of your provider, <legacyBold>Record</legacyBold> objects may be returned directly from your provider instead of a one-row <legacyBold>Recordset</legacyBold>, for example when an SQL query that selects only one row is executed.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Or, a <legacyBold>Record</legacyBold> object can be obtained directly from a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Or, a <legacyBold>Record</legacyBold> can be returned directly from a provider to semi-structured data, such as the Microsoft Exchange OLE DB provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">You can view the fields associated with the <legacyBold>Record</legacyBold> object by way of the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection on the <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> ADO allows object-valued columns including <legacyBold>Recordset</legacyBold>, <legacyBold>SafeArray</legacyBold>, and scalar values in the <legacyBold>Fields</legacyBold> collection of <legacyBold>Record</legacyBold> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">If the <legacyBold>Record</legacyBold> object represents a row in a <legacyBold>Recordset</legacyBold>, it is possible to return to that original <legacyBold>Recordset</legacyBold> with the <legacyLink xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <legacyBold>Record</legacyBold> object can also be used by semi-structured data providers such as the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>, to model tree-structured namespaces.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Each node in the tree is a <legacyBold>Record</legacyBold> object with associated columns.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The columns can represent the attributes of that node and other relevant information.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The <legacyBold>Record</legacyBold> object can represent both a leaf node and a non-leaf node in the tree structure.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Non-leaf nodes have other nodes as their contents, but leaf nodes do not have such contents.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> Leaf nodes typically contain binary streams of data and non-leaf nodes may also have a default binary stream associated with them.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Properties on the <legacyBold>Record</legacyBold> object identify the type of node.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">The <legacyBold>Record</legacyBold> object also represents an alternative way for navigating hierarchically organized data.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> A <legacyBold>Record</legacyBold> object may be created to represent the root of a specific sub-tree in a large tree structure and new <legacyBold>Record</legacyBold> objects may be opened to represent child nodes.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">A resource (for example, a file or directory) can be uniquely identified by an absolute URL.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> A <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object is implicitly created and set to the <legacyBold>Record</legacyBold> object when the <legacyBold>Record</legacyBold> is opened by using an absolute URL.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> A <legacyBold>Connection</legacyBold> object may explicitly be set to the <legacyBold>Record</legacyBold> object via the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> The files and directories that can be accessed by using the <legacyBold>Connection</legacyBold> object define the <legacyItalic>context</legacyItalic> in which <legacyBold>Record</legacyBold> operations may occur.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">Data modification and navigation methods on the <legacyBold>Record</legacyBold> object also accept a relative URL, which locates a resource using an absolute URL or the <legacyBold>Connection</legacyBold> object context as a starting point.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src23" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src24" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src25" class="srcSentence">A <legacyBold>Connection</legacyBold> object is associated with each <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> Therefore, <legacyBold>Record</legacyBold> object operations can be part of a transaction by invoking <legacyBold>Connection</legacyBold> object transaction methods.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">The <legacyBold>Record</legacyBold> object does not support ADO events, and therefore will not respond to notifications.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">With the methods and properties of a <legacyBold>Record</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src29" class="srcSentence">Set or return the associated <legacyBold>Connection</legacyBold> object with the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">Indicate access permissions with the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src31" class="srcSentence">Return the URL of the directory, if any, that contains the resource represented by the <legacyBold>Record</legacyBold> with the <legacyLink xlink:href="65120ce6-3900-4cd4-b322-3b9816d74737">ParentURL</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src32" class="srcSentence">Indicate the absolute URL, relative URL, or <legacyBold>Recordset</legacyBold> from which the <legacyBold>Record</legacyBold> is derived with the <legacyLink xlink:href="2c18279e-6f35-4af0-b12e-8f1543d9ed20">Source</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">Indicate the current status of the <legacyBold>Record</legacyBold> with the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">Indicate the type of <legacyBold>Record</legacyBold> — <legacyItalic>simple</legacyItalic>, <legacyItalic>collection</legacyItalic>, or <legacyItalic>structured document</legacyItalic> — with the <legacyLink xlink:href="790e46a2-13d2-451e-a8be-130bd9a206a4">RecordType</legacyLink>property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">Stop execution of an asynchronous operation with the <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">Disassociate the <legacyBold>Record</legacyBold> from a data source with the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src37" class="srcSentence">Copy the file or directory represented by a <legacyBold>Record</legacyBold> to another location with the <legacyLink xlink:href="b9bcf272-3c74-479f-95dd-0229a32e98fc">CopyRecord</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src38" class="srcSentence">Delete the file, or directory and subdirectories, represented by a <legacyBold>Record</legacyBold> with the <legacyLink xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src39" class="srcSentence">Open a <legacyBold>Recordset</legacyBold> that contains rows that represent the subdirectories and files of the entity represented by the <legacyBold>Record</legacyBold> with the <legacyLink xlink:href="b3f09bac-4f66-49f6-aa5a-6fbb4fb28338">GetChildren</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src40" class="srcSentence">Move (rename) the file, or directory and subdirectories, represented by a <legacyBold>Record</legacyBold> to another location with the <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src41" class="srcSentence">Associate the <legacyBold>Record</legacyBold> with an existing data source, or create a new file or directory with the <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src42" class="srcSentence">The <legacyBold>Record</legacyBold> object is safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src43" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src44" class="srcSentence">             <legacyLink xlink:href="dadde268-bd0f-4ba0-8775-83a5cd3e258a">Record Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">Records and Streams</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Stream Object (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 0514531f-009d-4519-abc3-d727014a39f1
caps.latest.revision: 6
caps.handback.revision: 6
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
# Stream Object (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="56691c904f1b7e7cd7b7c6e13ac0f8ab" id="tgt1" class="tgtSentence">Represents a stream of binary data or text.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9f19f57c25e6ea5edab677f2a57c1981" id="tgt2" class="tgtSentence">In tree-structured hierarchies such as a file system or an e-mail system, a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> may have a default binary stream of bits associated with it that contains the contents of the file or the e-mail.</caps:sentence>
          <caps:sentence sentenceid="e6d94527352eff2e6be01860163f1360" id="tgt3" class="tgtSentence"> A <legacyBold>Stream</legacyBold> object can be used to manipulate fields or records containing these streams of data.</caps:sentence>
          <caps:sentence sentenceid="2e69d2899d1b14c984104b38c0fcfcd0" id="tgt4" class="tgtSentence"> A <legacyBold>Stream</legacyBold> object can be obtained in these ways:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="eaaf1743713265e0f12acc38a407f87c" id="tgt5" class="tgtSentence">From a URL pointing to an object (typically a file) containing binary or text data.</caps:sentence>
              <caps:sentence sentenceid="c7ddc4f1c0d2eaa5aa2589010f9e8e22" id="tgt6" class="tgtSentence"> This object can be a simple document, a <legacyBold>Record</legacyBold> object representing a structured document, or a folder.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="aed78a029c0632f9d4bc74154cbe0997" id="tgt7" class="tgtSentence">By opening the default <legacyBold>Stream</legacyBold> object associated with a <legacyBold>Record</legacyBold> object.</caps:sentence>
              <caps:sentence sentenceid="00322f985755bc0f79d9cae3ea9ecaad" id="tgt8" class="tgtSentence"> You can obtain the default stream associated with a <legacyBold>Record</legacyBold> object when the <legacyBold>Record</legacyBold> is opened, to eliminate a round-trip just to open the stream.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="176f225b7c27664edc12fbfbc50e7829" id="tgt9" class="tgtSentence">By instantiating a <legacyBold>Stream</legacyBold> object.</caps:sentence>
              <caps:sentence sentenceid="a094fbc5ed30d7d652391bbb4e69d48e" id="tgt10" class="tgtSentence"> These <legacyBold>Stream</legacyBold> objects can be used to store data for the purposes of your application.</caps:sentence>
              <caps:sentence sentenceid="fe465e312fc02a23c1a54b62aae98c90" id="tgt11" class="tgtSentence"> Unlike a <legacyBold>Stream</legacyBold> associated with a URL, or the default <legacyBold>Stream</legacyBold> of a <legacyBold>Record</legacyBold>, an instantiated <legacyBold>Stream</legacyBold> has no association with an underlying source by default.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="6407af362b15503a824918d43dfeafd1" id="tgt12" class="tgtSentence">With the methods and properties of a <legacyBold>Stream</legacyBold> object, you can do the following:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="210fd04f0f0d8df63f91387b02ce64d4" id="tgt13" class="tgtSentence">Open a <legacyBold>Stream</legacyBold> object from a <legacyBold>Record</legacyBold> or URL with the <legacyLink xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a66017ef5bfd613c5eff4ec8514b7811" id="tgt14" class="tgtSentence">Close a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a443f7010797b36fd231ae771584f6bf" id="tgt15" class="tgtSentence">Input bytes or text to a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink> and <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink> methods.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="fe6046e70a778fb28145e22f5d028a66" id="tgt16" class="tgtSentence">Read bytes from the <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">Read</legacyLink> and <legacyLink xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">ReadText</legacyLink> methods.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4700cae8fdd3be233d067d4d5e67993d" id="tgt17" class="tgtSentence">Write any <legacyBold>Stream</legacyBold> data still in the ADO buffer to the underlying object with the <legacyLink xlink:href="938522b4-f836-4c80-8d27-a598a000f0ee">Flush</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4e45194cefd6218c5dab9a88630e3f94" id="tgt18" class="tgtSentence">Copy the contents of a <legacyBold>Stream</legacyBold> to another <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="b4aa5714-916b-48b8-8b09-cc2708379602">CopyTo</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="20836ff505b3f6cea5f7cfeb3dd36f4b" id="tgt19" class="tgtSentence">Control how lines are read from the source file with the <legacyLink xlink:href="0abc00fe-ee09-4c8e-b1f2-48ee9c5f3329">SkipLine</legacyLink>method and the <legacyLink xlink:href="0b20fbb8-6b83-48ec-b442-f96c8a4bafbb">LineSeparator</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c30d677d4c8cf8a2528c66be5d90f3de" id="tgt20" class="tgtSentence">Determine the end of stream position with the <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink>property and <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="eb7ebb401888ef3f371721fe8c0cf86d" id="tgt21" class="tgtSentence">Save and restore data in files with the <legacyLink xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile</legacyLink>and <legacyLink xlink:href="b18d8d38-7354-4a94-b637-6ac035faa433">LoadFromFile</legacyLink> methods.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9f9369e2b6ded16b4b0464224d716a08" id="tgt22" class="tgtSentence">Specify the character set used for storing the <legacyBold>Stream </legacyBold>with the <legacyLink xlink:href="e42507cb-9b46-4ce4-8191-2948eaf14ca2">Charset</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9d5c11e268d2127555d365e7eec37a61" id="tgt23" class="tgtSentence">Halt an asynchronous <legacyBold>Stream</legacyBold> operation with the <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="726f5bca7f9905d18b7b0dbec90b0f7c" id="tgt24" class="tgtSentence">Determine the number of bytes in a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a6c5a5da738ab08be663e33ff8abf61e" id="tgt25" class="tgtSentence">Control the current position within a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="fbde63856ba62e542cda9ffb0d11249f" id="tgt26" class="tgtSentence">Determine the type of data in a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0db081727ef533c3ad0d0e6eff74d3a6" id="tgt27" class="tgtSentence">Determine the current state of the <legacyBold>Stream</legacyBold> (closed, open, or executing) with the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6587a7d9a9448039eeff5a011cb5d050" id="tgt28" class="tgtSentence">Specify the access mode for the <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt29" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt30" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="8328bff31fc84c52214307bad4e48361" id="tgt31" class="tgtSentence">The <legacyBold>Stream</legacyBold> object is safe for scripting.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt32" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="de8343cbe9c05f6630f9e3ce546041e0" id="tgt33" class="tgtSentence">
                <legacyLink xlink:href="9b0eed90-c38c-4aa6-9040-5827f8c46b94">Stream Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">Records and Streams</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a stream of binary data or text.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">In tree-structured hierarchies such as a file system or an e-mail system, a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> may have a default binary stream of bits associated with it that contains the contents of the file or the e-mail.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> A <legacyBold>Stream</legacyBold> object can be used to manipulate fields or records containing these streams of data.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> A <legacyBold>Stream</legacyBold> object can be obtained in these ways:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">From a URL pointing to an object (typically a file) containing binary or text data.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> This object can be a simple document, a <legacyBold>Record</legacyBold> object representing a structured document, or a folder.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">By opening the default <legacyBold>Stream</legacyBold> object associated with a <legacyBold>Record</legacyBold> object.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> You can obtain the default stream associated with a <legacyBold>Record</legacyBold> object when the <legacyBold>Record</legacyBold> is opened, to eliminate a round-trip just to open the stream.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">By instantiating a <legacyBold>Stream</legacyBold> object.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> These <legacyBold>Stream</legacyBold> objects can be used to store data for the purposes of your application.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> Unlike a <legacyBold>Stream</legacyBold> associated with a URL, or the default <legacyBold>Stream</legacyBold> of a <legacyBold>Record</legacyBold>, an instantiated <legacyBold>Stream</legacyBold> has no association with an underlying source by default.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src12" class="srcSentence">With the methods and properties of a <legacyBold>Stream</legacyBold> object, you can do the following:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">Open a <legacyBold>Stream</legacyBold> object from a <legacyBold>Record</legacyBold> or URL with the <legacyLink xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">Close a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">Input bytes or text to a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">Write</legacyLink> and <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">WriteText</legacyLink> methods.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">Read bytes from the <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">Read</legacyLink> and <legacyLink xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">ReadText</legacyLink> methods.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">Write any <legacyBold>Stream</legacyBold> data still in the ADO buffer to the underlying object with the <legacyLink xlink:href="938522b4-f836-4c80-8d27-a598a000f0ee">Flush</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">Copy the contents of a <legacyBold>Stream</legacyBold> to another <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="b4aa5714-916b-48b8-8b09-cc2708379602">CopyTo</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src19" class="srcSentence">Control how lines are read from the source file with the <legacyLink xlink:href="0abc00fe-ee09-4c8e-b1f2-48ee9c5f3329">SkipLine</legacyLink>method and the <legacyLink xlink:href="0b20fbb8-6b83-48ec-b442-f96c8a4bafbb">LineSeparator</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src20" class="srcSentence">Determine the end of stream position with the <legacyLink xlink:href="57e08c5f-f3ed-4ecd-8c66-50b83b1031d1">EOS</legacyLink>property and <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">SetEOS</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src21" class="srcSentence">Save and restore data in files with the <legacyLink xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile</legacyLink>and <legacyLink xlink:href="b18d8d38-7354-4a94-b637-6ac035faa433">LoadFromFile</legacyLink> methods.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src22" class="srcSentence">Specify the character set used for storing the <legacyBold>Stream </legacyBold>with the <legacyLink xlink:href="e42507cb-9b46-4ce4-8191-2948eaf14ca2">Charset</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src23" class="srcSentence">Halt an asynchronous <legacyBold>Stream</legacyBold> operation with the <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">Cancel</legacyLink> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src24" class="srcSentence">Determine the number of bytes in a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="a487c241-d953-4c31-ae7e-6358d5cf6733">Size</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src25" class="srcSentence">Control the current position within a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src26" class="srcSentence">Determine the type of data in a <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src27" class="srcSentence">Determine the current state of the <legacyBold>Stream</legacyBold> (closed, open, or executing) with the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src28" class="srcSentence">Specify the access mode for the <legacyBold>Stream</legacyBold> with the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src29" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src31" class="srcSentence">The <legacyBold>Stream</legacyBold> object is safe for scripting.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src32" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src33" class="srcSentence">
                <legacyLink xlink:href="9b0eed90-c38c-4aa6-9040-5827f8c46b94">Stream Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">Records and Streams</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
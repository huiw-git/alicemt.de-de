---
title: "Tables Collection (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 38d750e7-f3fb-426e-b4b4-55eea4f1a654
caps.latest.revision: 10
caps.handback.revision: 10
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
# Tables Collection (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="dfe444a8a021cac22b1178519c68501c" id="tgt1" class="tgtSentence">Contains all <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink> objects of a catalog.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="f54d2f572ad3d6e8fffc6d5701be8408" id="tgt2" class="tgtSentence">The <legacyLink xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append</legacyLink> method for a <legacyBold>Tables</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt3" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1d413b90024a801f6be7601866ca8822" id="tgt4" class="tgtSentence">Add a new table to the collection with the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ed0be1c652e041a462a56d678a7a9845" id="tgt5" class="tgtSentence">The remaining properties and methods are standard to ADO collections.</caps:sentence>
            <caps:sentence sentenceid="ebc26c505b434e3b0709cbb029c75188" id="tgt6" class="tgtSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="4859211f2765a6c14ae1afcc95d9b21c" id="tgt7" class="tgtSentence">Access a table in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8111180f3b78369815bb77c8e5bbd695" id="tgt8" class="tgtSentence">Return the number of tables contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="09d86474f9aa137cac651785122da870" id="tgt9" class="tgtSentence">Remove a table from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="918e7bfcf1fb8892b265d13bf57519fd" id="tgt10" class="tgtSentence">Update the objects in the collection to reflect the current database schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="801df7d297c36497153daa7a22ff9c1f" id="tgt11" class="tgtSentence">Some providers may return other schema objects, such as a view, in the <unmanagedCodeEntityReference>Tables</unmanagedCodeEntityReference> collection.</caps:sentence>
            <caps:sentence sentenceid="04ec5e02ce1399772bbd18b15e3ce812" id="tgt12" class="tgtSentence"> Therefore, some ADOX collections may contain multiple references to the same object.</caps:sentence>
            <caps:sentence sentenceid="52fdde4dc23bc7ef0eca731e340d68a0" id="tgt13" class="tgtSentence"> Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method is called on the collection.</caps:sentence>
            <caps:sentence sentenceid="09f685b9ea08e5331a9c6cf649e8aa15" id="tgt14" class="tgtSentence"> For example, with the OLE DB Provider for Microsoft Jet, views are returned with the <unmanagedCodeEntityReference>Tables</unmanagedCodeEntityReference> collection.</caps:sentence>
            <caps:sentence sentenceid="18f124df053c6a3a7b13a0a692e1958d" id="tgt15" class="tgtSentence"> If you drop a view, you must refresh the <unmanagedCodeEntityReference>Tables</unmanagedCodeEntityReference> collection before the collection will reflect the change.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt16" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="98101a52-53a6-4287-a8d9-2a7c76c3e0b9">
                  <caps:sentence sentenceid="3e317702d9ebffdc3c7e4263de833bb4" id="tgt17" class="tgtSentence">Tables Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink> objects of a catalog.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <legacyLink xlink:href="a362ed51-314c-4783-9598-538dbf755f3d">Append</legacyLink> method for a <legacyBold>Tables</legacyBold> collection is unique for ADOX.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Add a new table to the collection with the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src5" class="srcSentence">The remaining properties and methods are standard to ADO collections.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> You can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Access a table in the collection with the <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Return the number of tables contained in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">Remove a table from the collection with the <legacyLink xlink:href="e6b6e3a4-8952-4d79-81f4-51019c338374">Delete</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Update the objects in the collection to reflect the current database schema with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src11" class="srcSentence">Some providers may return other schema objects, such as a view, in the <unmanagedCodeEntityReference>Tables</unmanagedCodeEntityReference> collection.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Therefore, some ADOX collections may contain multiple references to the same object.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method is called on the collection.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> For example, with the OLE DB Provider for Microsoft Jet, views are returned with the <unmanagedCodeEntityReference>Tables</unmanagedCodeEntityReference> collection.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> If you drop a view, you must refresh the <unmanagedCodeEntityReference>Tables</unmanagedCodeEntityReference> collection before the collection will reflect the change.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="98101a52-53a6-4287-a8d9-2a7c76c3e0b9">
                  <caps:sentence id="src17" class="srcSentence">Tables Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
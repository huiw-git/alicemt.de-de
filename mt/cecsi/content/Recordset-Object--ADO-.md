---
title: "Recordset Object (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ede1415f-c3df-4cc5-a05b-2576b2b84b60
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
# Recordset Object (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c8539f3ead60efbc64bb1fe5e92cf1e8" id="tgt1" class="tgtSentence">Represents the entire set of records from a base table or the results of an executed command.</caps:sentence>
          <caps:sentence sentenceid="897ca532fd939b8ba420b3045f063105" id="tgt2" class="tgtSentence"> At any time, the <legacyBold>Recordset</legacyBold> object refers to only a single record within the set as the current record.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9698f5e060dc9e353f1f3aabf068ed38" id="tgt3" class="tgtSentence">You use <legacyBold>Recordset</legacyBold> objects to manipulate data from a provider.</caps:sentence>
            <caps:sentence sentenceid="ef199940722867103bb5c07499834de6" id="tgt4" class="tgtSentence"> When you use ADO, you manipulate data almost entirely using <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="d6466e3858ae41d65ba9dea975bdc2c1" id="tgt5" class="tgtSentence"> All <legacyBold>Recordset</legacyBold> objects consist of records (rows) and fields (columns).</caps:sentence>
            <caps:sentence sentenceid="44e85359d68056da1d48044d94a61d11" id="tgt6" class="tgtSentence"> Depending on the functionality supported by the provider, some <legacyBold>Recordset</legacyBold> methods or properties may not be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2ab1214b6d251c111755caccdbccd3c9" id="tgt7" class="tgtSentence">ADODB.Recordset is the ProgID that should be used to create a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="4e81b1b82d430e813c61a3d2514635b1" id="tgt8" class="tgtSentence"> Existing applications that reference the outdated ADOR.Recordset ProgID will continue to work without recompiling, but new development should reference ADODB.Recordset.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e9448e35ba41d0c3223ba1ae56dfff2d" id="tgt9" class="tgtSentence">There are four different cursor types defined in ADO:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="60d3c72c1529188c48092289d64cb4fb" id="tgt10" class="tgtSentence">
                  <legacyBold>Dynamic cursor</legacyBold>     Allows you to view additions, changes, and deletions by other users; allows all types of movement through the <legacyBold>Recordset</legacyBold> that doesn't rely on bookmarks; and allows bookmarks if the provider supports them.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b3a37b4484dbc760b35e1ebfb67b7565" id="tgt11" class="tgtSentence">
                  <legacyBold>Keyset cursor</legacyBold>     Behaves like a dynamic cursor, except that it prevents you from seeing records that other users add, and prevents access to records that other users delete.</caps:sentence>
                <caps:sentence sentenceid="3994a5b4d7928d96d093e9bf94f275db" id="tgt12" class="tgtSentence"> Data changes by other users will still be visible.</caps:sentence>
                <caps:sentence sentenceid="53eab8d576dada1d71afaaab9cc552b4" id="tgt13" class="tgtSentence"> It always supports bookmarks and therefore allows all types of movement through the <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="00f82e9daff840cbf1d616aca3534fff" id="tgt14" class="tgtSentence">
                  <legacyBold>Static cursor</legacyBold>     Provides a static copy of a set of records for you to use to find data or generate reports; always allows bookmarks and therefore allows all types of movement through the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="737e1c0ba77f64011ff0ffa919c6731b" id="tgt15" class="tgtSentence"> Additions, changes, or deletions by other users will not be visible.</caps:sentence>
                <caps:sentence sentenceid="220593667265574bdca46a9b08783e2f" id="tgt16" class="tgtSentence"> This is the only type of cursor allowed when you open a client-side <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7e2e27dd74667ed8e22bb06fb052e70b" id="tgt17" class="tgtSentence">
                  <legacyBold>Forward-only cursor</legacyBold>     Allows you to only scroll forward through the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="737e1c0ba77f64011ff0ffa919c6731b" id="tgt18" class="tgtSentence"> Additions, changes, or deletions by other users will not be visible.</caps:sentence>
                <caps:sentence sentenceid="44ecca9731bac242e609b981fe270249" id="tgt19" class="tgtSentence"> This improves performance in situations where you need to make only a single pass through a <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="37d1bd8da4397164b322fe320f71a630" id="tgt20" class="tgtSentence">Set the <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink> property prior to opening the <legacyBold>Recordset</legacyBold> to choose the cursor type, or pass a <legacyItalic>CursorType</legacyItalic> argument with the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="70774427c076a4ef880a3dc2d1596a26" id="tgt21" class="tgtSentence"> Some providers don't support all cursor types.</caps:sentence>
            <caps:sentence sentenceid="800858675058d2242bebc38367517fe4" id="tgt22" class="tgtSentence"> Check the documentation for the provider.</caps:sentence>
            <caps:sentence sentenceid="9b1d7f78cdface9c14764ed7fdd635cc" id="tgt23" class="tgtSentence"> If you don't specify a cursor type, ADO opens a forward-only cursor by default.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="10fd18c6230bbb368db11bb13cede7ba" id="tgt24" class="tgtSentence">If the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold> to open a <legacyBold>Recordset</legacyBold>, the <legacyBold>UnderlyingValue</legacyBold> property on <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects is not available in the returned <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="0cbb5d522ff9ea104ad013b951f21596" id="tgt25" class="tgtSentence"> When used with some providers (such as the Microsoft ODBC Provider for OLE DB in conjunction with Microsoft SQL Server), you can create <legacyBold>Recordset</legacyBold> objects independently of a previously defined <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object by passing a connection string with the <legacyBold>Open</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="38395a6352ece2f6fe6be36761bb7d89" id="tgt26" class="tgtSentence"> ADO still creates a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, but it doesn't assign that object to an object variable.</caps:sentence>
            <caps:sentence sentenceid="a497ddd67ee01726f19e08c711cddf1b" id="tgt27" class="tgtSentence"> However, if you are opening multiple <legacyBold>Recordset</legacyBold> objects over the same connection, you should explicitly create and open a <legacyBold>Connection</legacyBold> object; this assigns the <legacyBold>Connection</legacyBold> object to an object variable.</caps:sentence>
            <caps:sentence sentenceid="1f2abdb5b2219bedcc9c3f1e231dd0c9" id="tgt28" class="tgtSentence"> If you do not use this object variable when opening your <legacyBold>Recordset</legacyBold> objects, ADO creates a new <legacyBold>Connection</legacyBold> object for each new <legacyBold>Recordset</legacyBold>, even if you pass the same connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="75b255a0b94723057f06437f4eb5d083" id="tgt29" class="tgtSentence">You can create as many <legacyBold>Recordset</legacyBold> objects as needed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e2d3e8f0b83c63da09be73c6a86c8888" id="tgt30" class="tgtSentence">When you open a <legacyBold>Recordset</legacyBold>, the current record is positioned to the first record (if any) and the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> and <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> properties are set to <legacyBold>False</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="f082606e848febec5ef2252e1ae18c41" id="tgt31" class="tgtSentence"> If there are no records, the <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> property settings are <legacyBold>True</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7bb017eed858b687c96c5e87c30c6716" id="tgt32" class="tgtSentence">You can use the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink>, <legacyBold>MoveLast</legacyBold>, <legacyBold>MoveNext</legacyBold>, and <legacyBold>MovePrevious</legacyBold> methods; the <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink> method; and the <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink>, <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink>, and <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> properties to reposition the current record, assuming the provider supports the relevant functionality.</caps:sentence>
            <caps:sentence sentenceid="8fbcff266c3a973c17918a94c3bdb111" id="tgt33" class="tgtSentence"> Forward-only <legacyBold>Recordset</legacyBold> objects support only the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveNext</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="5567ed3a1e24e529b9dc4d13e04087cb" id="tgt34" class="tgtSentence"> When you use the <legacyBold>Move</legacyBold> methods to visit each record (or enumerate the <legacyBold>Recordset</legacyBold>), you can use the <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> properties to determine if you've moved beyond the beginning or end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="14a3b051da22266442dd326711115c51" id="tgt35" class="tgtSentence">Before using any functionality of a <legacyBold>Recordset</legacyBold> object, you must call the <legacyBold>Supports</legacyBold> method on the object to verify that the functionality is supported or available.</caps:sentence>
            <caps:sentence sentenceid="0ac0981355b474a0223eb02a06868cb4" id="tgt36" class="tgtSentence"> You must not use the functionality when the <legacyBold>Supports</legacyBold> method returns false.</caps:sentence>
            <caps:sentence sentenceid="9a6d6edb99ecff04c9204589ac2945f3" id="tgt37" class="tgtSentence"> For example, you can use the <legacyBold>MovePrevious</legacyBold> method only if <codeInline>Recordset.Supports(adMovePrevious)</codeInline> returns <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence sentenceid="5f0b76513019bb595be4db975f586173" id="tgt38" class="tgtSentence"> Otherwise, you will get an error, because the <legacyBold>Recordset</legacyBold> object might have been closed and the functionality rendered unavailable on the instance.</caps:sentence>
            <caps:sentence sentenceid="c03682c8e19f20bfa4988dd912d06354" id="tgt39" class="tgtSentence"> If a feature you are interested in is not supported, <legacyBold>Supports</legacyBold> will return false as well.</caps:sentence>
            <caps:sentence sentenceid="cbb1c829bb609f7bce324dfc5afad3a0" id="tgt40" class="tgtSentence"> In this case, you should avoid calling the corresponding property or method on the <legacyBold>Recrodset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f320edbca23ab074a89bc9c6a621e3b8" id="tgt41" class="tgtSentence">
              <legacyBold>Recordset</legacyBold> objects can support two types of updating: immediate and batched.</caps:sentence>
            <caps:sentence sentenceid="5f840d9850d7bce3b0fa5c5f8bc97c67" id="tgt42" class="tgtSentence"> In immediate updating, all changes to data are written immediately to the underlying data source once you call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="be2d35abc51b9358a8355017f6d29c44" id="tgt43" class="tgtSentence"> You can also pass arrays of values as parameters with the <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink> and <legacyBold>Update</legacyBold> methods and simultaneously update several fields in a record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5af1c54746f01ab51453bd6b19f6dc59" id="tgt44" class="tgtSentence">If a provider supports batch updating, you can have the provider cache changes to more than one record and then transmit them in a single call to the database with the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="e635a36ee4803308b54d59d6b7cc6c1d" id="tgt45" class="tgtSentence"> This applies to changes made with the <legacyBold>AddNew</legacyBold>, <legacyBold>Update</legacyBold>, and <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink> methods.</caps:sentence>
            <caps:sentence sentenceid="2990684d76b323483105e3c33621c0b3" id="tgt46" class="tgtSentence"> After you call the <legacyBold>UpdateBatch</legacyBold> method, you can use the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property to check for any data conflicts in order to resolve them.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="636553b8df25551b6fe93c5f67f0c95f" id="tgt47" class="tgtSentence">To execute a query without using a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object, pass a query string to the <legacyBold>Open</legacyBold> method of a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              <caps:sentence sentenceid="5a6bc7413de18737e3bd6d36cf514725" id="tgt48" class="tgtSentence"> However, a <legacyBold>Command</legacyBold> object is required when you want to persist the command text and re-execute it, or use query parameters.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="a6ef8572ed9213c7e525947e175d5067" id="tgt49" class="tgtSentence">The <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property governs access permissions.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2eebdab72a98993b78bff68d2a11b8d4" id="tgt50" class="tgtSentence">The <legacyBold>Fields</legacyBold> collection is the default member of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="eedc8983db3e1e2c44d428cf0eced41d" id="tgt51" class="tgtSentence"> As a result, the following two code statements are equivalent.</caps:sentence>
          </para>
          <code>Debug.Print objRs.Fields.Item(0)  ' Both statements print 
Debug.Print objRs(0)              '  the Value of Item(0).</code>
          <para>
            <caps:sentence sentenceid="fe819fbab68e64c99bf0711671dd7173" id="tgt52" class="tgtSentence">When a <legacyBold>Recordset</legacyBold> object is passed across processes, only the <legacyBold>rowset</legacyBold> values are marshalled, and the properties of the <legacyBold>Recordset</legacyBold> object are ignored.</caps:sentence>
            <caps:sentence sentenceid="85d465f74a56da34ea873360e4d35904" id="tgt53" class="tgtSentence"> During unmarshalling, the <legacyBold>rowset</legacyBold> is unpacked into a newly created <legacyBold>Recordset</legacyBold> object, which also sets its properties to the default values.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c955fbb5152fc75c6a8825ffc712d0a3" id="tgt54" class="tgtSentence">The <legacyBold>Recordset</legacyBold> object is safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt55" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="fe16f574a2791602146f68d640a9b184" id="tgt56" class="tgtSentence">
                  <legacyLink xlink:href="4295a6e5-112d-4595-b18a-57728893ac2d">Recordset Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents the entire set of records from a base table or the results of an executed command.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> At any time, the <legacyBold>Recordset</legacyBold> object refers to only a single record within the set as the current record.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">You use <legacyBold>Recordset</legacyBold> objects to manipulate data from a provider.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> When you use ADO, you manipulate data almost entirely using <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> All <legacyBold>Recordset</legacyBold> objects consist of records (rows) and fields (columns).</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Depending on the functionality supported by the provider, some <legacyBold>Recordset</legacyBold> methods or properties may not be available.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">ADODB.Recordset is the ProgID that should be used to create a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Existing applications that reference the outdated ADOR.Recordset ProgID will continue to work without recompiling, but new development should reference ADODB.Recordset.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">There are four different cursor types defined in ADO:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">
                  <legacyBold>Dynamic cursor</legacyBold>     Allows you to view additions, changes, and deletions by other users; allows all types of movement through the <legacyBold>Recordset</legacyBold> that doesn't rely on bookmarks; and allows bookmarks if the provider supports them.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">
                  <legacyBold>Keyset cursor</legacyBold>     Behaves like a dynamic cursor, except that it prevents you from seeing records that other users add, and prevents access to records that other users delete.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> Data changes by other users will still be visible.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> It always supports bookmarks and therefore allows all types of movement through the <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">
                  <legacyBold>Static cursor</legacyBold>     Provides a static copy of a set of records for you to use to find data or generate reports; always allows bookmarks and therefore allows all types of movement through the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> Additions, changes, or deletions by other users will not be visible.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> This is the only type of cursor allowed when you open a client-side <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">
                  <legacyBold>Forward-only cursor</legacyBold>     Allows you to only scroll forward through the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> Additions, changes, or deletions by other users will not be visible.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> This improves performance in situations where you need to make only a single pass through a <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src20" class="srcSentence">Set the <legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink> property prior to opening the <legacyBold>Recordset</legacyBold> to choose the cursor type, or pass a <legacyItalic>CursorType</legacyItalic> argument with the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> Some providers don't support all cursor types.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Check the documentation for the provider.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> If you don't specify a cursor type, ADO opens a forward-only cursor by default.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">If the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold> to open a <legacyBold>Recordset</legacyBold>, the <legacyBold>UnderlyingValue</legacyBold> property on <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects is not available in the returned <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> When used with some providers (such as the Microsoft ODBC Provider for OLE DB in conjunction with Microsoft SQL Server), you can create <legacyBold>Recordset</legacyBold> objects independently of a previously defined <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object by passing a connection string with the <legacyBold>Open</legacyBold> method.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> ADO still creates a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, but it doesn't assign that object to an object variable.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> However, if you are opening multiple <legacyBold>Recordset</legacyBold> objects over the same connection, you should explicitly create and open a <legacyBold>Connection</legacyBold> object; this assigns the <legacyBold>Connection</legacyBold> object to an object variable.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> If you do not use this object variable when opening your <legacyBold>Recordset</legacyBold> objects, ADO creates a new <legacyBold>Connection</legacyBold> object for each new <legacyBold>Recordset</legacyBold>, even if you pass the same connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">You can create as many <legacyBold>Recordset</legacyBold> objects as needed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src30" class="srcSentence">When you open a <legacyBold>Recordset</legacyBold>, the current record is positioned to the first record (if any) and the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> and <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> properties are set to <legacyBold>False</legacyBold>.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> If there are no records, the <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> property settings are <legacyBold>True</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">You can use the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink>, <legacyBold>MoveLast</legacyBold>, <legacyBold>MoveNext</legacyBold>, and <legacyBold>MovePrevious</legacyBold> methods; the <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink> method; and the <legacyLink xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition</legacyLink>, <legacyLink xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage</legacyLink>, and <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> properties to reposition the current record, assuming the provider supports the relevant functionality.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> Forward-only <legacyBold>Recordset</legacyBold> objects support only the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveNext</legacyLink> method.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> When you use the <legacyBold>Move</legacyBold> methods to visit each record (or enumerate the <legacyBold>Recordset</legacyBold>), you can use the <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> properties to determine if you've moved beyond the beginning or end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src35" class="srcSentence">Before using any functionality of a <legacyBold>Recordset</legacyBold> object, you must call the <legacyBold>Supports</legacyBold> method on the object to verify that the functionality is supported or available.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> You must not use the functionality when the <legacyBold>Supports</legacyBold> method returns false.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> For example, you can use the <legacyBold>MovePrevious</legacyBold> method only if <codeInline>Recordset.Supports(adMovePrevious)</codeInline> returns <languageKeyword>True</languageKeyword>.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> Otherwise, you will get an error, because the <legacyBold>Recordset</legacyBold> object might have been closed and the functionality rendered unavailable on the instance.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> If a feature you are interested in is not supported, <legacyBold>Supports</legacyBold> will return false as well.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> In this case, you should avoid calling the corresponding property or method on the <legacyBold>Recrodset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src41" class="srcSentence">
              <legacyBold>Recordset</legacyBold> objects can support two types of updating: immediate and batched.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> In immediate updating, all changes to data are written immediately to the underlying data source once you call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> You can also pass arrays of values as parameters with the <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink> and <legacyBold>Update</legacyBold> methods and simultaneously update several fields in a record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src44" class="srcSentence">If a provider supports batch updating, you can have the provider cache changes to more than one record and then transmit them in a single call to the database with the <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> method.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> This applies to changes made with the <legacyBold>AddNew</legacyBold>, <legacyBold>Update</legacyBold>, and <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink> methods.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> After you call the <legacyBold>UpdateBatch</legacyBold> method, you can use the <legacyLink xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status</legacyLink> property to check for any data conflicts in order to resolve them.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src47" class="srcSentence">To execute a query without using a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object, pass a query string to the <legacyBold>Open</legacyBold> method of a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              <caps:sentence id="src48" class="srcSentence"> However, a <legacyBold>Command</legacyBold> object is required when you want to persist the command text and re-execute it, or use query parameters.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src49" class="srcSentence">The <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property governs access permissions.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src50" class="srcSentence">The <legacyBold>Fields</legacyBold> collection is the default member of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src51" class="srcSentence"> As a result, the following two code statements are equivalent.</caps:sentence>
          </para>
          <code>Debug.Print objRs.Fields.Item(0)  ' Both statements print 
Debug.Print objRs(0)              '  the Value of Item(0).</code>
          <para>
            <caps:sentence id="src52" class="srcSentence">When a <legacyBold>Recordset</legacyBold> object is passed across processes, only the <legacyBold>rowset</legacyBold> values are marshalled, and the properties of the <legacyBold>Recordset</legacyBold> object are ignored.</caps:sentence>
            <caps:sentence id="src53" class="srcSentence"> During unmarshalling, the <legacyBold>rowset</legacyBold> is unpacked into a newly created <legacyBold>Recordset</legacyBold> object, which also sets its properties to the default values.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src54" class="srcSentence">The <legacyBold>Recordset</legacyBold> object is safe for scripting.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src55" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src56" class="srcSentence">
                  <legacyLink xlink:href="4295a6e5-112d-4595-b18a-57728893ac2d">Recordset Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
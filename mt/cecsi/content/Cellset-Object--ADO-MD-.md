---
title: "Cellset Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 5e2452c0-cac0-49b2-8099-836c35794d50
caps.latest.revision: 9
caps.handback.revision: 9
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
# Cellset Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3e014c42ab8d3b3e5e05bc8df5e61857" id="tgt1" class="tgtSentence">Represents the results of a multidimensional query.</caps:sentence>
          <caps:sentence sentenceid="7dbc5d3d8438b2573e631affbe48aebb" id="tgt2" class="tgtSentence"> It is a collection of cells selected from cubes or other cellsets.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="baca1b3afc28c1b043ecc399bd21f54f" id="tgt3" class="tgtSentence">Data within a <legacyBold>Cellset</legacyBold> is retrieved using direct, array-like access.</caps:sentence>
            <caps:sentence sentenceid="7c4bf8fce7938e47f14d7a7872b6de43" id="tgt4" class="tgtSentence"> You can drill down to a specific member to obtain data about that member.</caps:sentence>
            <caps:sentence sentenceid="e17779fac60799ed905e105fc2e530f4" id="tgt5" class="tgtSentence"> For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named <codeInline>cst</codeInline>:</caps:sentence>
          </para>
          <code>cst.Axes(0).Positions(0).Members(0).Caption</code>
        </content>
      </languageReferenceRemarks>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="fc03c76918309ceae8a397996f4696d8" id="tgt6" class="tgtSentence">There is no notion of a current cell within a cellset.</caps:sentence>
            <caps:sentence sentenceid="edc11d0324c54ffd9c98eaf6da6845b5" id="tgt7" class="tgtSentence"> Instead, the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property retrieves a specific <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink> object from the cellset.</caps:sentence>
            <caps:sentence sentenceid="7f1d8da636d7ff3d262a4bfb28b03a66" id="tgt8" class="tgtSentence"> The arguments of the <legacyBold>Item</legacyBold> property determine which cell is retrieved.</caps:sentence>
            <caps:sentence sentenceid="40f74e44836eea12f5a9b986f1760167" id="tgt9" class="tgtSentence"> You can specify the unique ordinal value of a cell.</caps:sentence>
            <caps:sentence sentenceid="eae69efbb9d73850d06958fb5bab2cf8" id="tgt10" class="tgtSentence"> You can also retrieve cells by using their position numbers along each axis of the cellset.</caps:sentence>
            <caps:sentence sentenceid="ca9db0b52b8036587ba3135b36a68bf1" id="tgt11" class="tgtSentence"> For more information about retrieving cells, see the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a07894dd4d4605bb7a3f57b2c1dc416a" id="tgt12" class="tgtSentence">With the collections, methods, and properties of a <legacyBold>Cellset</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="75b420b51209e8dd28abf41a743cb7b8" id="tgt13" class="tgtSentence">Associate an open connection with a <legacyBold>Cellset</legacyBold> object by setting its <legacyLink xlink:href="2509b32c-a995-4364-9152-d8c83129bdd8">ActiveConnection</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="673c20979028dc8c38fe42da7ae76070" id="tgt14" class="tgtSentence">Execute and retrieve the results of a multidimensional query with the <legacyLink xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="449a4a1cdcc436cac764990585d8b605" id="tgt15" class="tgtSentence">Retrieve a <legacyBold>Cell</legacyBold> from the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="67d1ee8cfee8d54d389e5d9d1cb4b44e" id="tgt16" class="tgtSentence">Return the <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink> objects that define the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b37aabc4a7d11c42c4b243c435927ae6" id="tgt17" class="tgtSentence">Retrieve information about the dimensions used to filter the data in the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="9c656963-531e-4cd1-b698-d5f42a9b7ba3">FilterAxis</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="07b188d7250e19cbabaad1ee17e3ed7d" id="tgt18" class="tgtSentence">Return or specify the query used to define the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="875a99ea-7f1a-4570-87b1-5ecbebbcf845">Source</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="cffaac3734fdfd8090dea10670702038" id="tgt19" class="tgtSentence">Return the current state of the <legacyBold>Cellset</legacyBold> (open, closed, executing, or connecting) with the <legacyLink xlink:href="06d480ca-9eb6-4570-a45d-a73539bddd32">State</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ef3ea94697eb7674c55a94de2e688a1b" id="tgt20" class="tgtSentence">Close an open <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="a3aa594d-f9d4-4654-8625-ec20153ff5d9">Close</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6092f5bc161c78a3cbfdd9265fbd6ae2" id="tgt21" class="tgtSentence">Retrieve provider-specific information about the <legacyBold>Cellset</legacyBold> with the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt22" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f1738027f5ba19ede4b08530628161a8" id="tgt23" class="tgtSentence">
                  <legacyLink xlink:href="fb303e33-5a85-4e4e-81db-acaaa6f53799">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes Collection</link>
        <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents the results of a multidimensional query.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It is a collection of cells selected from cubes or other cellsets.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Data within a <legacyBold>Cellset</legacyBold> is retrieved using direct, array-like access.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> You can drill down to a specific member to obtain data about that member.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named <codeInline>cst</codeInline>:</caps:sentence>
          </para>
          <code>cst.Axes(0).Positions(0).Members(0).Caption</code>
        </content>
      </languageReferenceRemarks>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">There is no notion of a current cell within a cellset.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Instead, the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property retrieves a specific <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink> object from the cellset.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The arguments of the <legacyBold>Item</legacyBold> property determine which cell is retrieved.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> You can specify the unique ordinal value of a cell.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> You can also retrieve cells by using their position numbers along each axis of the cellset.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> For more information about retrieving cells, see the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">With the collections, methods, and properties of a <legacyBold>Cellset</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Associate an open connection with a <legacyBold>Cellset</legacyBold> object by setting its <legacyLink xlink:href="2509b32c-a995-4364-9152-d8c83129bdd8">ActiveConnection</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">Execute and retrieve the results of a multidimensional query with the <legacyLink xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">Retrieve a <legacyBold>Cell</legacyBold> from the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">Return the <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink> objects that define the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">Retrieve information about the dimensions used to filter the data in the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="9c656963-531e-4cd1-b698-d5f42a9b7ba3">FilterAxis</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">Return or specify the query used to define the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="875a99ea-7f1a-4570-87b1-5ecbebbcf845">Source</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">Return the current state of the <legacyBold>Cellset</legacyBold> (open, closed, executing, or connecting) with the <legacyLink xlink:href="06d480ca-9eb6-4570-a45d-a73539bddd32">State</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">Close an open <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="a3aa594d-f9d4-4654-8625-ec20153ff5d9">Close</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src21" class="srcSentence">Retrieve provider-specific information about the <legacyBold>Cellset</legacyBold> with the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src22" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">
                  <legacyLink xlink:href="fb303e33-5a85-4e4e-81db-acaaa6f53799">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes Collection</link>
        <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
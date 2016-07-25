---
title: "Overview of Multidimensional Schemas and Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ce37fa06-c581-4d80-9a9b-c3aa66408909
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
# Overview of Multidimensional Schemas and Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="1d1ae36fd871893652f8e5155bf91539" id="tgt1" class="tgtSentence">Understanding Multidimensional Schemas</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e0ff44a35fddedd43b5114623836de70" id="tgt2" class="tgtSentence">The central metadata object in ADO MD is the <legacyItalic>cube</legacyItalic>, which consists of a structured set of related dimensions, hierarchies, levels, and members.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3361c9dd985a9b37eca5c2ed99d9d884" id="tgt3" class="tgtSentence">A <legacyItalic>dimension</legacyItalic> is an independent category of data from your multidimensional database, derived from your business entities.</caps:sentence>
            <caps:sentence sentenceid="6569029313f94dd9f0b3b5f57eebd3e0" id="tgt4" class="tgtSentence"> A dimension typically contains items to be used as query criteria for the measures of the database.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c86886a7ea80200c6550def2495773ca" id="tgt5" class="tgtSentence">A <legacyItalic>hierarchy</legacyItalic> is a path of aggregation of a dimension.</caps:sentence>
            <caps:sentence sentenceid="111846d2d0a5a76006ff66b13fd351a3" id="tgt6" class="tgtSentence"> A dimension may have multiple levels of granularity, which have parent-child relationships.</caps:sentence>
            <caps:sentence sentenceid="01a3af3cc2dc1d2a05c7d70311a45282" id="tgt7" class="tgtSentence"> A hierarchy defines how these levels are related.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a9d8c70bd3ebf22830c6e06a1195c4c0" id="tgt8" class="tgtSentence">A <legacyItalic>level</legacyItalic> is a step of aggregation in a hierarchy.</caps:sentence>
            <caps:sentence sentenceid="a5b298a2ea16aa263e174bfc2eacb7a2" id="tgt9" class="tgtSentence"> For dimensions with multiple layers of information, each layer is a level.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e1fd72333a7247ed0350c5a368f94716" id="tgt10" class="tgtSentence">A <legacyItalic>member</legacyItalic> is a data item in a dimension.</caps:sentence>
            <caps:sentence sentenceid="a240ffa9ecdc376bcfd125e73521830e" id="tgt11" class="tgtSentence"> Typically, you create a caption or describe a measure of the database using members.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d306437adf8406aef1b9ab28a1d9d817" id="tgt12" class="tgtSentence">Cubes are represented by <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> objects in ADO MD.</caps:sentence>
            <caps:sentence sentenceid="d0175258eee4e5ba5d81efee3387e473" id="tgt13" class="tgtSentence"> Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension</legacyLink>, <legacyLink xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy</legacyLink>, <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink>, and <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="f412b80e160b69732c123964aae04302" id="tgt14" class="tgtSentence">Dimensions</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="805dcad6e95f455f365db78b7383fc04" id="tgt15" class="tgtSentence">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</caps:sentence>
                <caps:sentence sentenceid="ecdd12133e15929478c84efbddb0bcf2" id="tgt16" class="tgtSentence"> Typically, each dimension is an independent entry point or mechanism for selecting data.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="91cc9cc07bb4cc389f3db8738a4d6626" id="tgt17" class="tgtSentence">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</caps:sentence>
                <caps:sentence sentenceid="f003bc71823a513db8d3030f340b0ede" id="tgt18" class="tgtSentence"> The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6e85a79e8a55a4658913ddb0fa7f36a9" id="tgt19" class="tgtSentence">The Geography dimension has the following set of members:</caps:sentence>
              </para>
              <code>{All, North America, Europe, Canada, USA, UK, Germany, Canada-West,
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland, 
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto, 
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, 
Shreveport, Miami, Boston, New York, London, Dover, Glasgow, 
Edinburgh, Cardiff, Pembroke, Belfast, Derry, Berlin, 
Hamburg, Munich, Stuttgart}</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="363a3f0eb8ee21c582e96e99979801de" id="tgt20" class="tgtSentence">Hierarchies</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="322367baa7e1da28420d7cb6d522738b" id="tgt21" class="tgtSentence">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</caps:sentence>
                <caps:sentence sentenceid="38251a965de01d7aeb02aca6304f84d6" id="tgt22" class="tgtSentence"> A dimension can have more than one hierarchy.</caps:sentence>
                <caps:sentence sentenceid="d251f6dc375bc9f6630a50ca9a0b156e" id="tgt23" class="tgtSentence"> A natural hierarchy exists in the Geography dimension:</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="836eb5e382b5d9f430df48883fca918e" id="tgt24" class="tgtSentence">Levels</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="71f6d9afddbbd19430c4d7e8d3653a9e" id="tgt25" class="tgtSentence">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="42bb5cccdcb7071ed069a9eefea51549" id="tgt26" class="tgtSentence">Each level has a set of members, as follows:  </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e3604ace05f776b78eb43dc3886c519b" id="tgt27" class="tgtSentence">The World<codeInline> = {All}</codeInline></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="93843ade12dd3dbb8a192e17d0ec3674" id="tgt28" class="tgtSentence">Continents<codeInline> = {North America, Europe}</codeInline></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="92d96f113a137e7fc7539cd325c84ca8" id="tgt29" class="tgtSentence">Countries<codeInline> = {Canada, USA, UK, Germany}</codeInline></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9914c4682c5131fe7dc99a8049fe668b" id="tgt30" class="tgtSentence">Regions<codeInline> = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</codeInline></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e393aa43634a75bb07e7dd7f4bef272a" id="tgt31" class="tgtSentence">Cities<codeInline> = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Derry, Berlin, Hamburg, Munich, Stuttgart}</codeInline></caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="d2e3083420929d8bfae81f58fa4594cb" id="tgt32" class="tgtSentence">Members</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9b46c59b760e457bd833ba3be87bf368" id="tgt33" class="tgtSentence">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</caps:sentence>
                <caps:sentence sentenceid="63200ff92cad05045fc9911849dc9e0f" id="tgt34" class="tgtSentence"> All other members have at least one parent and at least one child.</caps:sentence>
                <caps:sentence sentenceid="93dc34fac13ecc1e33fe05fbfa56532f" id="tgt35" class="tgtSentence"> For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8412bfeba42c1f936decb95bbc7e523d" id="tgt36" class="tgtSentence">                 <codeInline>{All} (parent of) {Europe, North America}</codeInline>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="085a5a3fd874da907eef7db227770bc0" id="tgt37" class="tgtSentence">                 <codeInline>{North America} (parent of) {Canada, USA}</codeInline>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a5f25dc41ac3e0fe21d0db3fad280ab9" id="tgt38" class="tgtSentence">                 <codeInline>{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</codeInline>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bc158943c3ea6c0dc668c47cbb6593d0" id="tgt39" class="tgtSentence">                 <codeInline>{USA-NW} (parent of) {Boise, Seattle}</codeInline>               </caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="2244fe978ba0d158357914f7459d59ee" id="tgt40" class="tgtSentence">Members can be consolidated along one or more hierarchies per dimension.</caps:sentence>
                <caps:sentence sentenceid="c2a38777eabfd95b4a4c3da86e41f212" id="tgt41" class="tgtSentence"> Consider a Time dimension where there are two ways to roll up to the Year level from the Days level:</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4e079e806466c1709e182cd5144016c8" id="tgt42" class="tgtSentence">This example also illustrates another characteristic: Some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</caps:sentence>
                <caps:sentence sentenceid="1edd792e972aa214433f04c9c5aca63a" id="tgt43" class="tgtSentence"> Thus, a hierarchy need not include all members of a dimension.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">Microsoft ADO MD Programmer's Reference</link>
        <link xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</link>
        <link xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</link>
        <link xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Understanding Multidimensional Schemas</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The central metadata object in ADO MD is the <legacyItalic>cube</legacyItalic>, which consists of a structured set of related dimensions, hierarchies, levels, and members.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">A <legacyItalic>dimension</legacyItalic> is an independent category of data from your multidimensional database, derived from your business entities.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> A dimension typically contains items to be used as query criteria for the measures of the database.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">A <legacyItalic>hierarchy</legacyItalic> is a path of aggregation of a dimension.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> A dimension may have multiple levels of granularity, which have parent-child relationships.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> A hierarchy defines how these levels are related.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">A <legacyItalic>level</legacyItalic> is a step of aggregation in a hierarchy.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> For dimensions with multiple layers of information, each layer is a level.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">A <legacyItalic>member</legacyItalic> is a data item in a dimension.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Typically, you create a caption or describe a measure of the database using members.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">Cubes are represented by <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> objects in ADO MD.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension</legacyLink>, <legacyLink xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy</legacyLink>, <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink>, and <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src14" class="srcSentence">Dimensions</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src15" class="srcSentence">The dimensions of a cube depend on your business entities and types of data to be modeled in the database.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> Typically, each dimension is an independent entry point or mechanism for selecting data.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src17" class="srcSentence">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src19" class="srcSentence">The Geography dimension has the following set of members:</caps:sentence>
              </para>
              <code>{All, North America, Europe, Canada, USA, UK, Germany, Canada-West,
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland, 
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto, 
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, 
Shreveport, Miami, Boston, New York, London, Dover, Glasgow, 
Edinburgh, Cardiff, Pembroke, Belfast, Derry, Berlin, 
Hamburg, Munich, Stuttgart}</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src20" class="srcSentence">Hierarchies</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src21" class="srcSentence">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> A dimension can have more than one hierarchy.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> A natural hierarchy exists in the Geography dimension:</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src24" class="srcSentence">Levels</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src25" class="srcSentence">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src26" class="srcSentence">Each level has a set of members, as follows:  </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">The World<codeInline> = {All}</codeInline></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Continents<codeInline> = {North America, Europe}</codeInline></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Countries<codeInline> = {Canada, USA, UK, Germany}</codeInline></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Regions<codeInline> = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</codeInline></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Cities<codeInline> = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Derry, Berlin, Hamburg, Munich, Stuttgart}</codeInline></caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src32" class="srcSentence">Members</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src33" class="srcSentence">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent.</caps:sentence>
                <caps:sentence id="src34" class="srcSentence"> All other members have at least one parent and at least one child.</caps:sentence>
                <caps:sentence id="src35" class="srcSentence"> For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">                 <codeInline>{All} (parent of) {Europe, North America}</codeInline>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">                 <codeInline>{North America} (parent of) {Canada, USA}</codeInline>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">                 <codeInline>{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</codeInline>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">                 <codeInline>{USA-NW} (parent of) {Boise, Seattle}</codeInline>               </caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src40" class="srcSentence">Members can be consolidated along one or more hierarchies per dimension.</caps:sentence>
                <caps:sentence id="src41" class="srcSentence"> Consider a Time dimension where there are two ways to roll up to the Year level from the Days level:</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src42" class="srcSentence">This example also illustrates another characteristic: Some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</caps:sentence>
                <caps:sentence id="src43" class="srcSentence"> Thus, a hierarchy need not include all members of a dimension.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">Microsoft ADO MD Programmer's Reference</link>
        <link xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</link>
        <link xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</link>
        <link xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
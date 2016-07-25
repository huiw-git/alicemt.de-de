---
title: "Working with Multidimensional Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 84387746-aa3e-44fd-ad6c-a8214a6966dc
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
# Working with Multidimensional Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="fde925003d6711db93f32b29fe6eda03" id="tgt1" class="tgtSentence">A <legacyItalic>cellset</legacyItalic> is the result of a query on multidimensional data.</caps:sentence>
          <caps:sentence sentenceid="523698b0ecba51a8050ab991f58729ab" id="tgt2" class="tgtSentence"> It consists of a collection of axes, usually no more than four axes and typically only two or three.</caps:sentence>
          <caps:sentence sentenceid="8714a8438143206bce3b2b76a7f7f0d8" id="tgt3" class="tgtSentence"> An <legacyItalic>axis</legacyItalic> is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="10c0f380fa35e50474b10ab1f21d4323" id="tgt4" class="tgtSentence">A <legacyItalic>position</legacyItalic> is a point along an axis.</caps:sentence>
          <caps:sentence sentenceid="06b77abaa81e87eb5ff3ba21ffd06266" id="tgt5" class="tgtSentence"> For an axis consisting of a single dimension, these positions are a subset of the dimension members.</caps:sentence>
          <caps:sentence sentenceid="95b85abab3ab5dd6dbd6155ba8cb0ab4" id="tgt6" class="tgtSentence"> If an axis consists of more than one dimension, then each position is a compound entity, which has <legacyItalic>n</legacyItalic> parts where <legacyItalic>n</legacyItalic> is the number of dimensions oriented along that axis.</caps:sentence>
          <caps:sentence sentenceid="d90221f6ab01d6b5738ccd4b71775113" id="tgt7" class="tgtSentence"> Each part of the position is a member from one constituent dimension.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4f1bb0b0e11ba5451da5b05c5123e041" id="tgt8" class="tgtSentence">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers."</caps:sentence>
          <caps:sentence sentenceid="5557358924c16d5fdd194c6cfe493c6f" id="tgt9" class="tgtSentence"> In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4a7a74102f866aa99bbc9862c3f59031" id="tgt10" class="tgtSentence">A <legacyItalic>cell</legacyItalic> is an object positioned at the intersection of axis coordinates.</caps:sentence>
          <caps:sentence sentenceid="b2ed9ec2d30bdd50496a3c0143a1d9a4" id="tgt11" class="tgtSentence"> Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value.</caps:sentence>
          <caps:sentence sentenceid="f5914b2f16ee06ec0bebb55cd2d0f39e" id="tgt12" class="tgtSentence"> (Each cell is a unique ordinal value in the cellset.</caps:sentence>
          <caps:sentence sentenceid="2baf3b4252d301c98210c2c51ea1dc10" id="tgt13" class="tgtSentence"> The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="eca3c15673ec7cbc258a24e14d107dc9" id="tgt14" class="tgtSentence">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in <legacyLink xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</legacyLink>):  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="b2e790a52146d5ec2f635c6bc699da91" id="tgt15" class="tgtSentence">Salesperson</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1707b7e41e69191222e31d92ddf7ba70" id="tgt16" class="tgtSentence">Geography (natural hierarchy) — Continents, Countries, States, and so on</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d5ff3806150df085704530a00340d832" id="tgt17" class="tgtSentence">Quarters — Quarters, Months, Days</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="75aeb98e5241592ad6a6c2c4c78a16ef" id="tgt18" class="tgtSentence">Years</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="31e5d419892ec083e00bde66eb3513b6" id="tgt19" class="tgtSentence">Measures — Sales, PercentChange, BudgetedSales</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="86024cad1e83101d97359d7351051156" id="tgt20" class="tgtSentence">Products</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="615ae5a46e9e699162437d73a0f1f8e7" id="tgt21" class="tgtSentence">The following cellset represents sales for 1991 for all products:</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="fddfbd91fa4178c0b1230d2aac5f9c52" id="tgt22" class="tgtSentence">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="6599bc1915b9a72219ad4890c4efe2a0" id="tgt23" class="tgtSentence">The characteristics of this cellset are as follows:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="d724158bad1889e06dbe86c1833bfdfb" id="tgt24" class="tgtSentence">Axis dimensions: Quarters, Salesperson, Geography</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3ca6ce4003ef14947889b2be77ab6738" id="tgt25" class="tgtSentence">Filter dimensions: Measures, Years, Products</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="09464a4e717857d27ed0401b4879e240" id="tgt26" class="tgtSentence">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="bf5f0099b779f2054e8a8145757b3f9f" id="tgt27" class="tgtSentence">x-axis: two nested dimensions, Salesperson and Geography</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9830db03fa57b6d89d81ec0c099eb9d1" id="tgt28" class="tgtSentence">y-axis: Quarters dimension</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="b19769b2c19ce34f8bfa69c0d1d37c18" id="tgt29" class="tgtSentence">The x-axis has two nested dimensions: Salesperson and Geography.</caps:sentence>
          <caps:sentence sentenceid="6ad97316f0243f4d3dc715db391b7880" id="tgt30" class="tgtSentence"> From Geography, four members are selected: Seattle, Boston, USA-South, and Japan.</caps:sentence>
          <caps:sentence sentenceid="e85b19e0cbc8e2fefca2f773d248a3fc" id="tgt31" class="tgtSentence"> Two members are selected from Salesperson: Valentine and Nash.</caps:sentence>
          <caps:sentence sentenceid="33fe622bbe3bf1c2ddcd133aa3020b86" id="tgt32" class="tgtSentence"> This yields a total of eight positions on this axis (8 = 4*2).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f43699d9c65401ffaa0835ccfc482444" id="tgt33" class="tgtSentence">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</caps:sentence>
        </para>
        <code>(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North),
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North),
(Nash, Japan)</code>
        <para>
          <caps:sentence sentenceid="aea21bd7852de9cdca71e6c630e611e4" id="tgt34" class="tgtSentence">The y-axis has only one dimension, containing the following eight positions:</caps:sentence>
        </para>
        <code>Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec</code>
        <para>
          <caps:sentence sentenceid="aa5c071c74e36092226b40b7ae7b0434" id="tgt35" class="tgtSentence">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink>, <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink>, <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink>, and <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">Microsoft ADO MD Programmer's Reference</link>
        <link xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</link>
        <link xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</link>
        <link xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">A <legacyItalic>cellset</legacyItalic> is the result of a query on multidimensional data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It consists of a collection of axes, usually no more than four axes and typically only two or three.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> An <legacyItalic>axis</legacyItalic> is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">A <legacyItalic>position</legacyItalic> is a point along an axis.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> For an axis consisting of a single dimension, these positions are a subset of the dimension members.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> If an axis consists of more than one dimension, then each position is a compound entity, which has <legacyItalic>n</legacyItalic> parts where <legacyItalic>n</legacyItalic> is the number of dimensions oriented along that axis.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Each part of the position is a member from one constituent dimension.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers."</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">A <legacyItalic>cell</legacyItalic> is an object positioned at the intersection of axis coordinates.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> (Each cell is a unique ordinal value in the cellset.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in <legacyLink xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</legacyLink>):  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">Salesperson</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">Geography (natural hierarchy) — Continents, Countries, States, and so on</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">Quarters — Quarters, Months, Days</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">Years</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src19" class="srcSentence">Measures — Sales, PercentChange, BudgetedSales</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src20" class="srcSentence">Products</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src21" class="srcSentence">The following cellset represents sales for 1991 for all products:</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src22" class="srcSentence">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src23" class="srcSentence">The characteristics of this cellset are as follows:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src24" class="srcSentence">Axis dimensions: Quarters, Salesperson, Geography</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src25" class="srcSentence">Filter dimensions: Measures, Years, Products</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src26" class="srcSentence">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src27" class="srcSentence">x-axis: two nested dimensions, Salesperson and Geography</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src28" class="srcSentence">y-axis: Quarters dimension</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src29" class="srcSentence">The x-axis has two nested dimensions: Salesperson and Geography.</caps:sentence>
          <caps:sentence id="src30" class="srcSentence"> From Geography, four members are selected: Seattle, Boston, USA-South, and Japan.</caps:sentence>
          <caps:sentence id="src31" class="srcSentence"> Two members are selected from Salesperson: Valentine and Nash.</caps:sentence>
          <caps:sentence id="src32" class="srcSentence"> This yields a total of eight positions on this axis (8 = 4*2).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src33" class="srcSentence">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</caps:sentence>
        </para>
        <code>(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North),
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North),
(Nash, Japan)</code>
        <para>
          <caps:sentence id="src34" class="srcSentence">The y-axis has only one dimension, containing the following eight positions:</caps:sentence>
        </para>
        <code>Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec</code>
        <para>
          <caps:sentence id="src35" class="srcSentence">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink>, <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink>, <legacyLink xlink:href="5f498c9a-b1e7-4e6e-9ae6-71eadaf9aada">Axis</legacyLink>, and <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="6242b374-091b-406f-827a-c0dcd3e1967a">ADO MD Object Model</link>
        <link xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">Microsoft ADO MD Programmer's Reference</link>
        <link xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</link>
        <link xlink:href="c826b9b5-0d78-43a2-8174-5844db62a93c">Programming with ADO MD</link>
        <link xlink:href="cfae435e-2ac3-4312-8c1e-9ca4a74cd875">Using ADO with ADO MD</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Item Property (ADO MD Cellset)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 0e93d79b-b12e-4e98-889e-c2dfcca20fd0
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
# Item Property (ADO MD Cellset)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b2282e28230335fc3b5ded237d389d7d" id="tgt1" class="tgtSentence">Retrieves a cell from a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">cellset</legacyLink> using its coordinates.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt2" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>
            <codeFeaturedElement>Set</codeFeaturedElement>
            <legacyItalic>Cell</legacyItalic> = <legacyItalic>Cellset</legacyItalic>.<codeFeaturedElement>Item ( </codeFeaturedElement><legacyItalic>Positions</legacyItalic><codeFeaturedElement>)</codeFeaturedElement></code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt3" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="b60b37aa698f4d2649aad54bc1e1dd3d" id="tgt4" class="tgtSentence"> <legacyItalic>Positions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ae8893264992aa5fe80c21df52782e31" id="tgt5" class="tgtSentence">A <languageKeyword>VariantArray</languageKeyword> of values that uniquely specify a cell.</caps:sentence>
                <caps:sentence sentenceid="94fb9c877f27f5558018abf7aac4f6d3" id="tgt6" class="tgtSentence">
                  <legacyItalic>Positions</legacyItalic> can be one of the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="74a39ecd797948ea143604dfd882daa3" id="tgt7" class="tgtSentence">An array of position numbers</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2461353233d645b1baad8ac45b92434c" id="tgt8" class="tgtSentence">An array of member names</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="04b5a51966cafa1e0e11fb38408bd020" id="tgt9" class="tgtSentence">The ordinal position</caps:sentence>
                  </para>
                </listItem>
              </list>
            </definition>
          </definitionTable>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b9b0e3fa5205c568c85dc7608dcfb3bd" id="tgt10" class="tgtSentence">Use the <unmanagedCodeEntityReference>Item</unmanagedCodeEntityReference> property to return a <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink> object within a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="ea734b5ac9f3fa98fda6223ddb1aa219" id="tgt11" class="tgtSentence"> If the <unmanagedCodeEntityReference>Item</unmanagedCodeEntityReference> property cannot find the cell corresponding to the <legacyItalic>Positions</legacyItalic> argument, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b46853bdd1aaae31fbad0240d9d0cdbd" id="tgt12" class="tgtSentence">The <unmanagedCodeEntityReference>Item</unmanagedCodeEntityReference> property is the default property for the <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="1fc9b6a66a933c9db21e1ebe7affbcf0" id="tgt13" class="tgtSentence"> The following syntax forms are interchangeable:</caps:sentence>
          </para>
          <code>
            <legacyItalic>Cellset</legacyItalic>.Item ( <legacyItalic>Positions</legacyItalic> )<legacyItalic>Cellset</legacyItalic> ( <legacyItalic>Positions</legacyItalic> )</code>
        </content>
      </languageReferenceRemarks>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="2d88edf698a65571ccae97e9dc4b7e9f" id="tgt14" class="tgtSentence">The <legacyItalic>Positions </legacyItalic>argument specifies which cell to return.</caps:sentence>
            <caps:sentence sentenceid="fdd229797abc229b0424fdd0b1dacc6a" id="tgt15" class="tgtSentence"> You can specify the cell by ordinal position or by the position along each axis.</caps:sentence>
            <caps:sentence sentenceid="39b0ede73c84be1c2b71f3887659f1b8" id="tgt16" class="tgtSentence"> When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e285f1f618a95b8acba2ca60c6623aa8" id="tgt17" class="tgtSentence">The ordinal position is a number that uniquely identifies one cell within the <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="4be5d2affaa10824c65c24d05f177f4f" id="tgt18" class="tgtSentence"> Conceptually, cells are numbered in a <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference> as if the <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference> were a <legacyItalic>p</legacyItalic>-dimensional array, where <legacyItalic>p</legacyItalic> is the number of axes.</caps:sentence>
            <caps:sentence sentenceid="3743d55c3088b4cd6526d524d8ae373f" id="tgt19" class="tgtSentence"> Cells are addressed in row-major order.</caps:sentence>
            <caps:sentence sentenceid="acd3b572894aff1a8c841f796b0451aa" id="tgt20" class="tgtSentence"> Below is the formula for calculating the ordinal number of a cell:</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e6446ab3fffd44da6d5c7703533fcec3" id="tgt21" class="tgtSentence">If member names are passed as strings to <unmanagedCodeEntityReference>Item</unmanagedCodeEntityReference>, the members must be listed in increasing order of the numeric axis identifiers.</caps:sentence>
            <caps:sentence sentenceid="2f5206f8701aa140625c219dc4648b1d" id="tgt22" class="tgtSentence"> Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions.</caps:sentence>
            <caps:sentence sentenceid="95f775a474ca8aeb79b9112dc5887f6b" id="tgt23" class="tgtSentence"> Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="5c5b457859bd051c55a22345ac84b75e" id="tgt24" class="tgtSentence">Retrieving cells by member name may not be supported by your data provider.</caps:sentence>
              <caps:sentence sentenceid="d6fcebf315a70e0352f701647709f00e" id="tgt25" class="tgtSentence"> See the documentation for your provider for more information.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt26" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object</link>
        <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Retrieves a cell from a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">cellset</legacyLink> using its coordinates.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <code>
            <codeFeaturedElement>Set</codeFeaturedElement>
            <legacyItalic>Cell</legacyItalic> = <legacyItalic>Cellset</legacyItalic>.<codeFeaturedElement>Item ( </codeFeaturedElement><legacyItalic>Positions</legacyItalic><codeFeaturedElement>)</codeFeaturedElement></code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>Positions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">A <languageKeyword>VariantArray</languageKeyword> of values that uniquely specify a cell.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence">
                  <legacyItalic>Positions</legacyItalic> can be one of the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">An array of position numbers</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">An array of member names</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">The ordinal position</caps:sentence>
                  </para>
                </listItem>
              </list>
            </definition>
          </definitionTable>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">Use the <unmanagedCodeEntityReference>Item</unmanagedCodeEntityReference> property to return a <legacyLink xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell</legacyLink> object within a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> If the <unmanagedCodeEntityReference>Item</unmanagedCodeEntityReference> property cannot find the cell corresponding to the <legacyItalic>Positions</legacyItalic> argument, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">The <unmanagedCodeEntityReference>Item</unmanagedCodeEntityReference> property is the default property for the <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> The following syntax forms are interchangeable:</caps:sentence>
          </para>
          <code>
            <legacyItalic>Cellset</legacyItalic>.Item ( <legacyItalic>Positions</legacyItalic> )<legacyItalic>Cellset</legacyItalic> ( <legacyItalic>Positions</legacyItalic> )</code>
        </content>
      </languageReferenceRemarks>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">The <legacyItalic>Positions </legacyItalic>argument specifies which cell to return.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> You can specify the cell by ordinal position or by the position along each axis.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">The ordinal position is a number that uniquely identifies one cell within the <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Conceptually, cells are numbered in a <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference> as if the <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference> were a <legacyItalic>p</legacyItalic>-dimensional array, where <legacyItalic>p</legacyItalic> is the number of axes.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> Cells are addressed in row-major order.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Below is the formula for calculating the ordinal number of a cell:</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">If member names are passed as strings to <unmanagedCodeEntityReference>Item</unmanagedCodeEntityReference>, the members must be listed in increasing order of the numeric axis identifiers.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src24" class="srcSentence">Retrieving cells by member name may not be supported by your data provider.</caps:sentence>
              <caps:sentence id="src25" class="srcSentence"> See the documentation for your provider for more information.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src26" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object (ADO MD)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dcc2f044-b785-4a29-9bc5-b673f66eedf9">Cell Object</link>
        <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
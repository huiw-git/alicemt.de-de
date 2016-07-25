---
title: "Cell Object (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: dcc2f044-b785-4a29-9bc5-b673f66eedf9
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
# Cell Object (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="47b5bb3e3f751e42526578ed8c8538de" id="tgt1" class="tgtSentence">Represents the data at the intersection of axis coordinates contained in a cellset.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="a8cc5c293e558a1b749c526fb526820b" id="tgt2" class="tgtSentence">A <legacyBold>Cell</legacyBold> object is returned by the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property of a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a6fb4994b2737a1a9e4a257f77d4ec6f" id="tgt3" class="tgtSentence">With the collections and properties of a <legacyBold>Cell</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="25daecbcffd5c1132a3177af9ad13b7d" id="tgt4" class="tgtSentence">Return the data in the <legacyBold>Cell</legacyBold> with the <legacyLink xlink:href="70dc5cff-0b05-456d-b86b-2686fe4e7ce6">Value</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="91b039faeb49a255b3f10723f1e18e04" id="tgt5" class="tgtSentence">Return the string representing the formatted display of the <legacyBold>Value</legacyBold> property with the <legacyLink xlink:href="5c06451e-06ec-4da6-9a87-2d043469248a">FormattedValue</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="13d7aa8939b6ed9912eaba2a7bc1f12d" id="tgt6" class="tgtSentence">Return the ordinal value of the <legacyBold>Cell</legacyBold> within the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="a6001168-b954-47f0-ba0d-c05c4cc40c58">Ordinal</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="77d3685df86b737e2679e2b75e006bf3" id="tgt7" class="tgtSentence">Determine the position of the <legacyBold>Cell</legacyBold> within the <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> with the <legacyLink xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5669252378d7a85b0130011277e848ef" id="tgt8" class="tgtSentence">Retrieve other information about the <legacyBold>Cell</legacyBold> with the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="39452e7aa7674a533008488280c4b581" id="tgt9" class="tgtSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence sentenceid="4be124b7b0fe47f8aff65d60ff33d8e3" id="tgt10" class="tgtSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence sentenceid="8cf7e6aaac62008f842531d45619b20d" id="tgt11" class="tgtSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence sentenceid="d4f2c74aa9a9fd8ed47f1fcb6abfc159" id="tgt12" class="tgtSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt13" class="tgtSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt14" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fca76d73dd201a2af0c6908be2240261" id="tgt15" class="tgtSentence">BackColor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="02d5f8dd0a8fb47c9b98ec62b7cff8d9" id="tgt16" class="tgtSentence">Background color used when displaying the cell.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b46f741fc295d5790d4d1fd8f27529d7" id="tgt17" class="tgtSentence">FontFlags</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7e8852f782923f032860fdeb0c5314a" id="tgt18" class="tgtSentence">Bitmask detailing effects on the font.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b6ecc3f0f6032d8fe82a25872e35c21" id="tgt19" class="tgtSentence">FontName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ada791e84fe4006069807ee9b0546e64" id="tgt20" class="tgtSentence">Font used to display the cell value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b64d06b5495a47cc736c3f7f24594e3" id="tgt21" class="tgtSentence">FontSize</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5be4068be4b8853a8f797fd53dfd7919" id="tgt22" class="tgtSentence">Font size used to display the cell value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1756e3531d013c98e058a73e9d7485ab" id="tgt23" class="tgtSentence">ForeColor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ca46c132602c70717656792d0d519d6b" id="tgt24" class="tgtSentence">Foreground color used when displaying the cell.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e699ab6243b50d1b5366f847b0bc3770" id="tgt25" class="tgtSentence">FormatString</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="854eabfa4d89ab75f5f3f85b69300b89" id="tgt26" class="tgtSentence">Value in a formatted string.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt27" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3b3565f049f2884cae5659fea11e36c2" id="tgt28" class="tgtSentence">
                  <legacyLink xlink:href="c45d795b-3272-4df4-a54c-7cd4fcb187fd">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b4647211-2566-4657-ae7b-3dd761457d7b">VBScript Example</link>
        <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object</link>
        <link xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents the data at the intersection of axis coordinates contained in a cellset.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <legacyBold>Cell</legacyBold> object is returned by the <legacyLink xlink:href="0e93d79b-b12e-4e98-889e-c2dfcca20fd0">Item</legacyLink> property of a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">With the collections and properties of a <legacyBold>Cell</legacyBold> object, you can do the following:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">Return the data in the <legacyBold>Cell</legacyBold> with the <legacyLink xlink:href="70dc5cff-0b05-456d-b86b-2686fe4e7ce6">Value</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Return the string representing the formatted display of the <legacyBold>Value</legacyBold> property with the <legacyLink xlink:href="5c06451e-06ec-4da6-9a87-2d043469248a">FormattedValue</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Return the ordinal value of the <legacyBold>Cell</legacyBold> within the <legacyBold>Cellset</legacyBold> with the <legacyLink xlink:href="a6001168-b954-47f0-ba0d-c05c4cc40c58">Ordinal</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Determine the position of the <legacyBold>Cell</legacyBold> within the <legacyLink xlink:href="feb2581c-fc41-471c-bb69-29f8a55fda70">CubeDef</legacyLink> with the <legacyLink xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">Retrieve other information about the <legacyBold>Cell</legacyBold> with the standard ADO <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <legacyBold>Properties</legacyBold> collection contains provider-supplied properties.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The following table lists properties that might be available.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The actual property list may differ depending upon the implementation of the provider.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> See the documentation for your provider for a more complete list of available properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">BackColor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Background color used when displaying the cell.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">FontFlags</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Bitmask detailing effects on the font.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">FontName</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Font used to display the cell value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">FontSize</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Font size used to display the cell value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">ForeColor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Foreground color used when displaying the cell.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">FormatString</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Value in a formatted string.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src27" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src28" class="srcSentence">
                  <legacyLink xlink:href="c45d795b-3272-4df4-a54c-7cd4fcb187fd">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b4647211-2566-4657-ae7b-3dd761457d7b">VBScript Example</link>
        <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object</link>
        <link xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
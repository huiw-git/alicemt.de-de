---
title: "Count Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: da9ccd1f-d402-41a2-940c-45556fc5340d
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
# Count Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="191c0353791a4ad37eb0bb09e360a689" id="tgt1" class="tgtSentence">Indicates the number of objects in a collection.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="43757cdb8ce2f43bcf7e4c8c37c24040" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="85ca2296a78e5210205719c74ecd2e71" id="tgt4" class="tgtSentence">Use the <legacyBold>Count</legacyBold> property to determine how many objects are in a given collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="156f7b13ac4fc9d177503260643bbc83" id="tgt5" class="tgtSentence">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the <legacyBold>Count</legacyBold> property minus 1.</caps:sentence>
            <caps:sentence sentenceid="49b9a08247d21e1253c732bd51da85b6" id="tgt6" class="tgtSentence"> If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the <legacyBold>Count</legacyBold> property, use the <legacyBold>For</legacyBold> <legacyBold>Each...Next</legacyBold> command.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="94b10d742468366063cd5f943209d201" id="tgt7" class="tgtSentence">If the <legacyBold>Count</legacyBold> property is zero, there are no objects in the collection.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="eaf6f4e7-2ea0-49a3-89ee-e219e025257c">Dimensions Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="bef0fcb1-8060-4faa-84f0-3d52e9c4526f">Hierarchies Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">Levels Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="35033910-623b-449a-a57d-baff3ed5ab8f">Visual Basic Example</link>
        <link xlink:href="54dfb1dd-636c-4560-8a3f-32b1f6aa07d7">Visual C++ Example</link>
        <link xlink:href="68cc1395-2433-4000-98dc-9e860170cd59">Visual J++ Example</link>
        <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the number of objects in a collection.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Count</legacyBold> property to determine how many objects are in a given collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the <legacyBold>Count</legacyBold> property minus 1.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the <legacyBold>Count</legacyBold> property, use the <legacyBold>For</legacyBold> <legacyBold>Each...Next</legacyBold> command.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If the <legacyBold>Count</legacyBold> property is zero, there are no objects in the collection.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">Axes Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">Columns Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="eaf6f4e7-2ea0-49a3-89ee-e219e025257c">Dimensions Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">Groups Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="bef0fcb1-8060-4faa-84f0-3d52e9c4526f">Hierarchies Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">Indexes Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">Keys Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">Levels Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">Members Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">Positions Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">Users Collection</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="35033910-623b-449a-a57d-baff3ed5ab8f">Visual Basic Example</link>
        <link xlink:href="54dfb1dd-636c-4560-8a3f-32b1f6aa07d7">Visual C++ Example</link>
        <link xlink:href="68cc1395-2433-4000-98dc-9e860170cd59">Visual J++ Example</link>
        <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ADOX Enumerated Constants"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d91f511-d46f-44ef-97ef-77bf93836186
caps.latest.revision: 8
caps.handback.revision: 8
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
# ADOX Enumerated Constants
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="91489b544e8f7d33c0f53cf8e689b9a9" id="tgt1" class="tgtSentence">To assist debugging, the ADOX enumerated constants list a value for each constant.</caps:sentence>
          <caps:sentence sentenceid="7b374a131de6ba64b3dd2c955d84efd0" id="tgt2" class="tgtSentence"> However, this value is purely advisory, and may change from one release of ADOX to another.</caps:sentence>
          <caps:sentence sentenceid="ef6b6ef3a7fb6485f14faa59eb623c9a" id="tgt3" class="tgtSentence"> Your code should only depend on the name, not the actual value, of enumerated constants.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <para>
            <caps:sentence sentenceid="5a7c064cf19d3c9df109f8767e63e17e" id="tgt4" class="tgtSentence">The following enumerated constants are defined.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f49fe61d5812612c53377049e3c86d6" id="tgt5" class="tgtSentence">Enumeration</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt6" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="f948febd-c885-4621-823b-421e116fec4e">
                      <caps:sentence sentenceid="a248a0a2d9c383ba093130a46ee01daa" id="tgt7" class="tgtSentence">ActionEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="77bc76d7a0c97fc88fa7e69ccece1003" id="tgt8" class="tgtSentence">Specifies the type of action to be performed when <legacyBold>SetPermissions</legacyBold> is called.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="6acf3689-1a7f-4379-9d7f-df452ccbac27">
                      <caps:sentence sentenceid="28573c998d342319a22273a3204a0d85" id="tgt9" class="tgtSentence">AllowNullsEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4d2edf2643491122f2f406870000d959" id="tgt10" class="tgtSentence">Specifies whether records with null values are indexed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="cd0db27a-1080-40af-a491-3893e7bef9cd">
                      <caps:sentence sentenceid="c22a243c7e8999ce56fb482c8c227bdf" id="tgt11" class="tgtSentence">ColumnAttributesEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f4c0017c7cde3f5e32e8472574eead72" id="tgt12" class="tgtSentence">Specifies characteristics of a <legacyBold>Column</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">
                      <caps:sentence sentenceid="6d319c4fef32e6f68dce9829ae8c2cf4" id="tgt13" class="tgtSentence">DataTypeEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="96a3e63d0f65ad96ade45b9240dbdb20" id="tgt14" class="tgtSentence">Specifies the data type of a <legacyBold>Field</legacyBold>, <legacyBold>Parameter</legacyBold>, or <legacyBold>Property</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="c2f6ce79-c4b3-4d40-ac95-21025208f991">
                      <caps:sentence sentenceid="7b20393867037bdb1d4883e245f94bdb" id="tgt15" class="tgtSentence">InheritTypeEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d5e68716b89e07a671dbab95ad073127" id="tgt16" class="tgtSentence">Specifies how objects will inherit permissions set with <legacyBold>SetPermissions</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3e597c52-caf4-4341-8471-d1ade563dbf7">
                      <caps:sentence sentenceid="ad8368093a82a106408b02b167162936" id="tgt17" class="tgtSentence">KeyTypeEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="041b284c88c82fb21b4faeaaefbc4522" id="tgt18" class="tgtSentence">Specifies the type of <legacyBold>Key</legacyBold>: primary, foreign, or unique.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">
                      <caps:sentence sentenceid="41acc235e210dbbb0f3a4669c184d5db" id="tgt19" class="tgtSentence">ObjectTypeEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7d64bd61740b8ce0a42b9603e06a2b90" id="tgt20" class="tgtSentence">Specifies the type of database object for which to set permissions or ownership.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="55ee67c7-a583-42aa-849a-78264b4cb614">
                      <caps:sentence sentenceid="1fecd764a9c012a80c24b7d23a5c544e" id="tgt21" class="tgtSentence">RightsEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4e1bf689d17ba58905f47f888441fc37" id="tgt22" class="tgtSentence">Specifies the rights or permissions for a group or user on an object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="738fd3ff-3daf-483d-a0b9-88bef1be54c1">
                      <caps:sentence sentenceid="907a45ef8d7256a894e056c0c6821477" id="tgt23" class="tgtSentence">RuleEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8607d889c3a2dc5c1ff212ca29d9482" id="tgt24" class="tgtSentence">Specifies the rule to follow when a <legacyBold>Key</legacyBold> is deleted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="0b9d46e7-29d9-4ca1-a23a-056403106a71">
                      <caps:sentence sentenceid="23076ff15173677935e46abefd9539ed" id="tgt25" class="tgtSentence">SortOrderEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4f7bc6e5b8f3e5388cdf583b4d0a6941" id="tgt26" class="tgtSentence">Specifies the sort sequence for an indexed column.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ef700465-2e97-46e8-8213-2d662501e540">ADOX API Reference</link>
        <link xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">Microsoft ADOX Programmer's Reference</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To assist debugging, the ADOX enumerated constants list a value for each constant.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> However, this value is purely advisory, and may change from one release of ADOX to another.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Your code should only depend on the name, not the actual value, of enumerated constants.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The following enumerated constants are defined.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Enumeration</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="f948febd-c885-4621-823b-421e116fec4e">
                      <caps:sentence id="src7" class="srcSentence">ActionEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Specifies the type of action to be performed when <legacyBold>SetPermissions</legacyBold> is called.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="6acf3689-1a7f-4379-9d7f-df452ccbac27">
                      <caps:sentence id="src9" class="srcSentence">AllowNullsEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Specifies whether records with null values are indexed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="cd0db27a-1080-40af-a491-3893e7bef9cd">
                      <caps:sentence id="src11" class="srcSentence">ColumnAttributesEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Specifies characteristics of a <legacyBold>Column</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">
                      <caps:sentence id="src13" class="srcSentence">DataTypeEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Specifies the data type of a <legacyBold>Field</legacyBold>, <legacyBold>Parameter</legacyBold>, or <legacyBold>Property</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="c2f6ce79-c4b3-4d40-ac95-21025208f991">
                      <caps:sentence id="src15" class="srcSentence">InheritTypeEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Specifies how objects will inherit permissions set with <legacyBold>SetPermissions</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3e597c52-caf4-4341-8471-d1ade563dbf7">
                      <caps:sentence id="src17" class="srcSentence">KeyTypeEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Specifies the type of <legacyBold>Key</legacyBold>: primary, foreign, or unique.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">
                      <caps:sentence id="src19" class="srcSentence">ObjectTypeEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Specifies the type of database object for which to set permissions or ownership.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="55ee67c7-a583-42aa-849a-78264b4cb614">
                      <caps:sentence id="src21" class="srcSentence">RightsEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Specifies the rights or permissions for a group or user on an object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="738fd3ff-3daf-483d-a0b9-88bef1be54c1">
                      <caps:sentence id="src23" class="srcSentence">RuleEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Specifies the rule to follow when a <legacyBold>Key</legacyBold> is deleted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="0b9d46e7-29d9-4ca1-a23a-056403106a71">
                      <caps:sentence id="src25" class="srcSentence">SortOrderEnum</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Specifies the sort sequence for an indexed column.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ef700465-2e97-46e8-8213-2d662501e540">ADOX API Reference</link>
        <link xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">Microsoft ADOX Programmer's Reference</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
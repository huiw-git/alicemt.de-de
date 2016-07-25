---
title: "AllowNullsEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6acf3689-1a7f-4379-9d7f-df452ccbac27
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
# AllowNullsEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4d2edf2643491122f2f406870000d959" id="tgt1" class="tgtSentence">Specifies whether records with null values are indexed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt2" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt3" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt4" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8e67c141ec5fc8ee25dbed3df4d33fe1" id="tgt5" class="tgtSentence">
                      <legacyBold>adIndexNullsAllow</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt6" class="tgtSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="57eb342cf70b0ac1dd202ff3b85c7e0f" id="tgt7" class="tgtSentence">The index does allow entries in which the key columns are null.</caps:sentence>
                    <caps:sentence sentenceid="b6179781cdeb017ece58807707e35d98" id="tgt8" class="tgtSentence"> If a null value is entered in a key column, the entry is inserted into the index.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="037920aada2fbf1dd2930479b0d61002" id="tgt9" class="tgtSentence">
                      <legacyBold>adIndexNullsDisallow</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt10" class="tgtSentence">1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt11" class="tgtSentence">Default.</caps:sentence>
                    <caps:sentence sentenceid="1af612cb866df5a737abec114e0458e2" id="tgt12" class="tgtSentence"> The index does not allow entries in which the key columns are null.</caps:sentence>
                    <caps:sentence sentenceid="e65d8aaafc077684dc68b6ca4f102e5e" id="tgt13" class="tgtSentence"> If a null value is entered in a key column, an error will occur.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2933b1b1c885c16bed15818a6ee626ad" id="tgt14" class="tgtSentence">
                      <legacyBold>adIndexNullsIgnore</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt15" class="tgtSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9954cf0ec269288df6b7cbff18b344c0" id="tgt16" class="tgtSentence">The index does not insert entries containing null keys.</caps:sentence>
                    <caps:sentence sentenceid="ac88037f617883ad37fdc13054d3fefc" id="tgt17" class="tgtSentence"> If a null value is entered in a key column, the entry is ignored and no error occurs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2a8d7c89918ca6920dfb5da6ff70c39" id="tgt18" class="tgtSentence">
                      <legacyBold>adIndexNullsIgnoreAny</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt19" class="tgtSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b19a2165e4466ef179d4784f3a8bd0e0" id="tgt20" class="tgtSentence">The index does not insert entries where some key column has a null value.</caps:sentence>
                    <caps:sentence sentenceid="24ee1123a8706b03c57707738caaa259" id="tgt21" class="tgtSentence"> For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt22" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="313b0bf7-3f37-4823-8fca-bd9c80e078a7">IndexNulls Property (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies whether records with null values are indexed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src2" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src3" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">
                      <legacyBold>adIndexNullsAllow</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">The index does allow entries in which the key columns are null.</caps:sentence>
                    <caps:sentence id="src8" class="srcSentence"> If a null value is entered in a key column, the entry is inserted into the index.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">
                      <legacyBold>adIndexNullsDisallow</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Default.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> The index does not allow entries in which the key columns are null.</caps:sentence>
                    <caps:sentence id="src13" class="srcSentence"> If a null value is entered in a key column, an error will occur.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">
                      <legacyBold>adIndexNullsIgnore</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">The index does not insert entries containing null keys.</caps:sentence>
                    <caps:sentence id="src17" class="srcSentence"> If a null value is entered in a key column, the entry is ignored and no error occurs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">
                      <legacyBold>adIndexNullsIgnoreAny</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">The index does not insert entries where some key column has a null value.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="313b0bf7-3f37-4823-8fca-bd9c80e078a7">IndexNulls Property (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
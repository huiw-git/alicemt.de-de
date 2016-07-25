---
title: "SaveOptionsEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 59339100-6e29-48d1-aea3-6873796d186b
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
# SaveOptionsEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="201482d6ac436c330f02ff6ffd8b676d" id="tgt1" class="tgtSentence">Specifies whether a file should be created or overwritten when saving from a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="495ef368103f079ec60b2728595bb551" id="tgt2" class="tgtSentence"> The values can be <legacyBold>adSaveCreateNotExist</legacyBold> or <legacyBold>adSaveCreateOverWrite</legacyBold>..</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt3" class="tgtSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt4" class="tgtSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt5" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="17c821061cebdc04933f75dac78ff658" id="tgt6" class="tgtSentence">adSaveCreateNotExist</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt7" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt8" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="167a41b2758c0f2beea54272da5fff15" id="tgt9" class="tgtSentence"> Creates a new file if the file specified by the <legacyItalic>FileName</legacyItalic> parameter does not already exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3c88cf1d8339d3a52e269706095fe59e" id="tgt10" class="tgtSentence">adSaveCreateOverWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt11" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="551db1199470e506500993c86a6f5b22" id="tgt12" class="tgtSentence">Overwrites the file with the data from the currently open <legacyBold>Stream</legacyBold> object, if the file specified by the <legacyItalic>Filename</legacyItalic> parameter already exists.</caps:sentence>
                  <caps:sentence sentenceid="bf841aa9aa4774972c0c2df424a0d594" id="tgt13" class="tgtSentence"> If the file specified by the <parameterReference>Filename</parameterReference> parameter does not exist, a new file is created.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt14" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2feceb55ab2f12074bf5420d2fcd6fc5" id="tgt15" class="tgtSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt16" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile Method</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies whether a file should be created or overwritten when saving from a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The values can be <legacyBold>adSaveCreateNotExist</legacyBold> or <legacyBold>adSaveCreateOverWrite</legacyBold>..</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src6" class="srcSentence">adSaveCreateNotExist</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> Creates a new file if the file specified by the <legacyItalic>FileName</legacyItalic> parameter does not already exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src10" class="srcSentence">adSaveCreateOverWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Overwrites the file with the data from the currently open <legacyBold>Stream</legacyBold> object, if the file specified by the <legacyItalic>Filename</legacyItalic> parameter already exists.</caps:sentence>
                  <caps:sentence id="src13" class="srcSentence"> If the file specified by the <parameterReference>Filename</parameterReference> parameter does not exist, a new file is created.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile Method</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
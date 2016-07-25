---
title: "InheritTypeEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: c2f6ce79-c4b3-4d40-ac95-21025208f991
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
# InheritTypeEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1b6d137da88cb848480e55960a7b4db5" id="tgt1" class="tgtSentence">Specifies how objects will inherit permissions set with <legacyLink xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions</legacyLink>.</caps:sentence>
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
                    <caps:sentence sentenceid="3dcab155a96913d4b18495728db968e8" id="tgt5" class="tgtSentence">
                      <legacyBold>adInheritBoth</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt6" class="tgtSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b139ebde200c7588f13b277a2d74bbf1" id="tgt7" class="tgtSentence">Both objects and other containers contained by the primary object inherit the entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f59d99c2fb4e5dea216dd8b29dbb5cba" id="tgt8" class="tgtSentence">
                      <legacyBold>adInheritContainers</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt9" class="tgtSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="14c554958200f1248f84bb858a688d12" id="tgt10" class="tgtSentence">Other containers that are contained by the primary object inherit the entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="58041f45b53fa6268eedb20e7f0d94fc" id="tgt11" class="tgtSentence">
                      <legacyBold>adInheritNone</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt12" class="tgtSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt13" class="tgtSentence">Default.</caps:sentence>
                    <caps:sentence sentenceid="f4035b8b537182ff14db731c8e498cd8" id="tgt14" class="tgtSentence"> No inheritance occurs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e48278b6b17ad18140b9d13b17227d30" id="tgt15" class="tgtSentence">
                      <legacyBold>adInheritNoPropagate</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt16" class="tgtSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="07ce612f86a520a6487945934dbac8d6" id="tgt17" class="tgtSentence">The <legacyBold>adInheritObjects</legacyBold> and <legacyBold>adInheritContainers</legacyBold> flags are not propagated to an inherited entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c09f01c761e6946047ef421adf5fdf7b" id="tgt18" class="tgtSentence">
                      <legacyBold>adInheritObjects</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt19" class="tgtSentence">1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e7c0db59f92ddfb399bb98f454765ff8" id="tgt20" class="tgtSentence">Non-container objects in the container inherit the permissions.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt21" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions Method (ADOX)</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies how objects will inherit permissions set with <legacyLink xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions</legacyLink>.</caps:sentence>
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
                      <legacyBold>adInheritBoth</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Both objects and other containers contained by the primary object inherit the entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">
                      <legacyBold>adInheritContainers</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Other containers that are contained by the primary object inherit the entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">
                      <legacyBold>adInheritNone</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Default.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> No inheritance occurs.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">
                      <legacyBold>adInheritNoPropagate</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">The <legacyBold>adInheritObjects</legacyBold> and <legacyBold>adInheritContainers</legacyBold> flags are not propagated to an inherited entry.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">
                      <legacyBold>adInheritObjects</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Non-container objects in the container inherit the permissions.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions Method (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ObjectProxy (ADO/WFC Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f68f58bc-ad28-46cc-9fb3-099e1a678397
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
# ObjectProxy (ADO/WFC Syntax)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="23abb3b3750806dcbe39028cec5f027d" id="tgt1" class="tgtSentence">An <legacyBold>ObjectProxy</legacyBold> object represents a server, and is returned by the <legacyBold>createObject</legacyBold> method of the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="35ea690f2b7d63137ef7f7c590022c52" id="tgt2" class="tgtSentence"> The ObjectProxy class has one method, <legacyBold>call</legacyBold>, which can invoke a method on the server and return an object resulting from that invocation.</caps:sentence>
        </para>
        <para>
          <legacyBold>
            <caps:sentence sentenceid="bf01303ec05e42a8b2352d82e9a911f6" id="tgt3" class="tgtSentence">package com.ms.wfc.data</caps:sentence>
          </legacyBold>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt4" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="3affd4a460a5eda57f563c6c85811dd2" id="tgt5" class="tgtSentence">Call Method (ADO/WFC Syntax)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="7ea6513455803c1aef463a798e8d284d" id="tgt6" class="tgtSentence">Invokes a method on the server represented by the ObjectProxy.</caps:sentence>
                <caps:sentence sentenceid="e4e7c71ce10bb7a5beeb1c2e3bccb8ed" id="tgt7" class="tgtSentence"> Optionally, method arguments may be passed as an array of objects.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt8" class="tgtSentence">Syntax</caps:sentence>
                </title>
                <content>
                  <code>public Object <legacyItalic xmlns="">ObjectProxy</legacyItalic>.( String <legacyItalic xmlns="">method</legacyItalic> )
public Object <legacyItalic xmlns="">ObjectProxy</legacyItalic>.( String <legacyItalic xmlns="">method</legacyItalic>, Object[] <legacyItalic xmlns="">args</legacyItalic>)</code>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="7fff84525c6516919851a9005373f87e" id="tgt9" class="tgtSentence">Returns</caps:sentence>
                </title>
                <content>
                  <definitionTable>
                    <definedTerm>
                      <caps:sentence sentenceid="75df90dfe0a1dbc61cc89f9a6e6f77e9" id="tgt10" class="tgtSentence">Object </caps:sentence>
                    </definedTerm>
                    <definition>
                      <para>
                        <caps:sentence sentenceid="008c3fb36c2487b38275e881e16c1fe8" id="tgt11" class="tgtSentence">An object resulting from invoking the method.</caps:sentence>
                      </para>
                    </definition>
                  </definitionTable>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt12" class="tgtSentence">Parameters</caps:sentence>
                </title>
                <content>
                  <definitionTable>
                    <definedTerm>
                      <caps:sentence sentenceid="4eb56ff53bdc540c2562c098b1fdd244" id="tgt13" class="tgtSentence"> <legacyItalic>ObjectProxy</legacyItalic> </caps:sentence>
                    </definedTerm>
                    <definition>
                      <para>
                        <caps:sentence sentenceid="41d6dc8465b75534e327d3e8f064b77f" id="tgt14" class="tgtSentence">An <legacyBold>ObjectProxy</legacyBold> object that represents the server.</caps:sentence>
                      </para>
                    </definition>
                    <definedTerm>
                      <caps:sentence sentenceid="b35828c5ca5bea87cff83a1cbe81373f" id="tgt15" class="tgtSentence"> <legacyItalic>method</legacyItalic> </caps:sentence>
                    </definedTerm>
                    <definition>
                      <para>
                        <caps:sentence sentenceid="254d551828c1f83716830dc82ab36001" id="tgt16" class="tgtSentence">A String, containing the name of the method to invoke on the server.</caps:sentence>
                      </para>
                    </definition>
                    <definedTerm>
                      <caps:sentence sentenceid="83cc79cf7bc14222ca9e15a321515c3c" id="tgt17" class="tgtSentence"> <legacyItalic>args</legacyItalic> </caps:sentence>
                    </definedTerm>
                    <definition>
                      <para>
                        <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt18" class="tgtSentence">Optional.</caps:sentence>
                        <caps:sentence sentenceid="fdd76ce3c4914b7d8852a5691d354c68" id="tgt19" class="tgtSentence"> An array of objects that are arguments to the method on the server.</caps:sentence>
                        <caps:sentence sentenceid="e82387c2f6f6bceb1adfa00dfcfdf864" id="tgt20" class="tgtSentence"> Java data types are automatically converted to data types suitable for use on the server.</caps:sentence>
                      </para>
                    </definition>
                  </definitionTable>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">An <legacyBold>ObjectProxy</legacyBold> object represents a server, and is returned by the <legacyBold>createObject</legacyBold> method of the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">DataSpace</legacyLink> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The ObjectProxy class has one method, <legacyBold>call</legacyBold>, which can invoke a method on the server and return an object resulting from that invocation.</caps:sentence>
        </para>
        <para>
          <legacyBold>
            <caps:sentence id="src3" class="srcSentence">package com.ms.wfc.data</caps:sentence>
          </legacyBold>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src5" class="srcSentence">Call Method (ADO/WFC Syntax)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src6" class="srcSentence">Invokes a method on the server represented by the ObjectProxy.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> Optionally, method arguments may be passed as an array of objects.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src8" class="srcSentence">Syntax</caps:sentence>
                </title>
                <content>
                  <code>public Object <legacyItalic xmlns="">ObjectProxy</legacyItalic>.( String <legacyItalic xmlns="">method</legacyItalic> )
public Object <legacyItalic xmlns="">ObjectProxy</legacyItalic>.( String <legacyItalic xmlns="">method</legacyItalic>, Object[] <legacyItalic xmlns="">args</legacyItalic>)</code>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src9" class="srcSentence">Returns</caps:sentence>
                </title>
                <content>
                  <definitionTable>
                    <definedTerm>
                      <caps:sentence id="src10" class="srcSentence">Object </caps:sentence>
                    </definedTerm>
                    <definition>
                      <para>
                        <caps:sentence id="src11" class="srcSentence">An object resulting from invoking the method.</caps:sentence>
                      </para>
                    </definition>
                  </definitionTable>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src12" class="srcSentence">Parameters</caps:sentence>
                </title>
                <content>
                  <definitionTable>
                    <definedTerm>
                      <caps:sentence id="src13" class="srcSentence"> <legacyItalic>ObjectProxy</legacyItalic> </caps:sentence>
                    </definedTerm>
                    <definition>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">An <legacyBold>ObjectProxy</legacyBold> object that represents the server.</caps:sentence>
                      </para>
                    </definition>
                    <definedTerm>
                      <caps:sentence id="src15" class="srcSentence"> <legacyItalic>method</legacyItalic> </caps:sentence>
                    </definedTerm>
                    <definition>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">A String, containing the name of the method to invoke on the server.</caps:sentence>
                      </para>
                    </definition>
                    <definedTerm>
                      <caps:sentence id="src17" class="srcSentence"> <legacyItalic>args</legacyItalic> </caps:sentence>
                    </definedTerm>
                    <definition>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">Optional.</caps:sentence>
                        <caps:sentence id="src19" class="srcSentence"> An array of objects that are arguments to the method on the server.</caps:sentence>
                        <caps:sentence id="src20" class="srcSentence"> Java data types are automatically converted to data types suitable for use on the server.</caps:sentence>
                      </para>
                    </definition>
                  </definitionTable>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
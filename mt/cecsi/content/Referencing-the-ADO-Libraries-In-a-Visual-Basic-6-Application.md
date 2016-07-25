---
title: "Referencing the ADO Libraries In a Visual Basic 6 Application"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cfd37a82-aad2-41cd-8d13-1566c43d95f0
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
# Referencing the ADO Libraries In a Visual Basic 6 Application
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="01446219206dbadd9aad7ed8691ae681" id="tgt1" class="tgtSentence">To import the ADO libraries into a Microsoft Visual Basic 6 application, you must set a reference in the Visual Basic project.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence sentenceid="df8d99f6e36aaf69a0c5227956264d72" id="tgt2" class="tgtSentence">To set a reference to the ADO libraries in a Visual Basic project</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="3cef692190a2e6b7683f8f1f61f77f35" id="tgt3" class="tgtSentence">Create a new or open an existing Visual Basic project.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="241413af88e81d6629f81baef0b9742c" id="tgt4" class="tgtSentence">Click the <legacyBold>Project </legacyBold>menu item and then select <legacyBold>References...</legacyBold> from the drop-down menu panel.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="d3f751e32f77021a2c68757027218890" id="tgt5" class="tgtSentence">From <legacyBold>Available References</legacyBold>, check the box for <legacyBold>Microsoft ActiveX Data Objects </legacyBold><legacyBold><legacyItalic>n.n</legacyItalic></legacyBold><legacyBold> Library</legacyBold>, where <legacyBold><legacyItalic>n.n</legacyItalic></legacyBold> represents the latest version number.</caps:sentence>
                  <caps:sentence sentenceid="e855567657376c5860d9c1a480848d7e" id="tgt6" class="tgtSentence"> The <legacyBold>Location</legacyBold> field below should identify your choice as <legacyItalic>$installDir\msado15.dll</legacyItalic>, where <legacyItalic>$installDir </legacyItalic>represents the path of the directory in which the ADO library has been installed.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="df91d10ad705f8574dc6fa4237eca6ef" id="tgt7" class="tgtSentence">If you intend to use ADO MD, repeat step 3 to select <legacyBold>Microsoft ActiveX Data Objects (Multi-dimensional) </legacyBold><legacyBold><legacyItalic>n.n</legacyItalic></legacyBold><legacyBold> Library</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="d13ecc2518dc6d45dc6692110dff6f25" id="tgt8" class="tgtSentence"> The <legacyBold>Location</legacyBold> field should identify this choice as <legacyItalic>$installDir\msadomd.dll</legacyItalic>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="544433da8ccaafe7d15429045740d75e" id="tgt9" class="tgtSentence">If you intend to use ADOX, repeat step 3 to select <legacyBold>Microsoft ADO Ext. </legacyBold><legacyBold><legacyItalic>n.n</legacyItalic></legacyBold><legacyBold> for DDL and Security</legacyBold>. The <legacyBold>Location</legacyBold> field should identify this choice as <legacyItalic>$installDir\msadox.dll</legacyItalic>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="2a410eafca0827d999fb050d79facdb3" id="tgt10" class="tgtSentence">Click <legacyBold>OK</legacyBold> to finish setting the references.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="60cca08b90e3076e13f8a399bbb8cffc" id="tgt11" class="tgtSentence">Backward Compatibility</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9c8028f9eb4c47858d16509beb328cde" id="tgt12" class="tgtSentence">Installing ADO also copies the following type libraries of earlier versions:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="61f489e264f31b52236a5192b5fafbc6" id="tgt13" class="tgtSentence">
                  <legacyItalic>msado27.tlb</legacyItalic>, ADO 2.7 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="82ecd45805ed7a364ee334ad2dcc54cc" id="tgt14" class="tgtSentence">
                  <legacyItalic>msado26.tlb</legacyItalic>, ADO 2.6 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="65f2004806127e12f67880727bed8468" id="tgt15" class="tgtSentence">
                  <legacyItalic>msado25.tlb</legacyItalic>, ADO 2.5 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f34847fc095d36a4d1e00f6b0b7c4d6c" id="tgt16" class="tgtSentence">
                  <legacyItalic>msado21.tlb</legacyItalic>, ADO 2.1 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a05402ee375ec5df76e99e80614cd876" id="tgt17" class="tgtSentence">
                  <legacyItalic>msado20.tlb</legacyItalic>, ADO 2.0 Type Library</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="eb94af11752880002cc85473496d89b8" id="tgt18" class="tgtSentence">If your application must use any of these ADO libraries for reasons of backward compatibility, you need to import the appropriate version of the type library.</caps:sentence>
            <caps:sentence sentenceid="956b1ba98bb351632154836bdfd57b4d" id="tgt19" class="tgtSentence"> To do this, follow the procedures in the previous section, replacing <legacyItalic>msado15.dll</legacyItalic> by <legacyItalic>msadoXX.tlb</legacyItalic>, where <legacyItalic>XX</legacyItalic> represents the version number you need to import.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To import the ADO libraries into a Microsoft Visual Basic 6 application, you must set a reference in the Visual Basic project.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence id="src2" class="srcSentence">To set a reference to the ADO libraries in a Visual Basic project</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Create a new or open an existing Visual Basic project.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Click the <legacyBold>Project </legacyBold>menu item and then select <legacyBold>References...</legacyBold> from the drop-down menu panel.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src5" class="srcSentence">From <legacyBold>Available References</legacyBold>, check the box for <legacyBold>Microsoft ActiveX Data Objects </legacyBold><legacyBold><legacyItalic>n.n</legacyItalic></legacyBold><legacyBold> Library</legacyBold>, where <legacyBold><legacyItalic>n.n</legacyItalic></legacyBold> represents the latest version number.</caps:sentence>
                  <caps:sentence id="src6" class="srcSentence"> The <legacyBold>Location</legacyBold> field below should identify your choice as <legacyItalic>$installDir\msado15.dll</legacyItalic>, where <legacyItalic>$installDir </legacyItalic>represents the path of the directory in which the ADO library has been installed.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src7" class="srcSentence">If you intend to use ADO MD, repeat step 3 to select <legacyBold>Microsoft ActiveX Data Objects (Multi-dimensional) </legacyBold><legacyBold><legacyItalic>n.n</legacyItalic></legacyBold><legacyBold> Library</legacyBold>.</caps:sentence>
                  <caps:sentence id="src8" class="srcSentence"> The <legacyBold>Location</legacyBold> field should identify this choice as <legacyItalic>$installDir\msadomd.dll</legacyItalic>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src9" class="srcSentence">If you intend to use ADOX, repeat step 3 to select <legacyBold>Microsoft ADO Ext. </legacyBold><legacyBold><legacyItalic>n.n</legacyItalic></legacyBold><legacyBold> for DDL and Security</legacyBold>. The <legacyBold>Location</legacyBold> field should identify this choice as <legacyItalic>$installDir\msadox.dll</legacyItalic>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Click <legacyBold>OK</legacyBold> to finish setting the references.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Backward Compatibility</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Installing ADO also copies the following type libraries of earlier versions:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">
                  <legacyItalic>msado27.tlb</legacyItalic>, ADO 2.7 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">
                  <legacyItalic>msado26.tlb</legacyItalic>, ADO 2.6 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">
                  <legacyItalic>msado25.tlb</legacyItalic>, ADO 2.5 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">
                  <legacyItalic>msado21.tlb</legacyItalic>, ADO 2.1 Type Library</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">
                  <legacyItalic>msado20.tlb</legacyItalic>, ADO 2.0 Type Library</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src18" class="srcSentence">If your application must use any of these ADO libraries for reasons of backward compatibility, you need to import the appropriate version of the type library.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> To do this, follow the procedures in the previous section, replacing <legacyItalic>msado15.dll</legacyItalic> by <legacyItalic>msadoXX.tlb</legacyItalic>, where <legacyItalic>XX</legacyItalic> represents the version number you need to import.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
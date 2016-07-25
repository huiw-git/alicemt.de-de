---
title: "Using ADO with Microsoft Visual Basic"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9dfb6784-037d-4f9d-bb7f-b506b4498573
caps.latest.revision: 10
caps.handback.revision: 10
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
# Using ADO with Microsoft Visual Basic
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4d7c8f9ed19965239eb76b39f9f2c6a1" id="tgt1" class="tgtSentence">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications.</caps:sentence>
          <caps:sentence sentenceid="70c6f468d23941cc9e9d35481542e8c4" id="tgt2" class="tgtSentence"> This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="2b467330ef7e831da2e6c776f98ba250" id="tgt3" class="tgtSentence">Referencing the ADO Library</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cd4b603ed150441d286b1aab8d731f27" id="tgt4" class="tgtSentence">The ADO library must be referenced by your project.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="5e6af0612a44f15bf82af5fd9bc3c086" id="tgt5" class="tgtSentence">To reference ADO from Microsoft Visual Basic</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e52f9caf5bb9827ff334efa74e4118e8" id="tgt6" class="tgtSentence">In Visual Basic, from the <legacyBold>Project</legacyBold> menu, select <legacyBold>References...</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="21e6815ce3f677b4c700f792163b8c67" id="tgt7" class="tgtSentence">Select <legacyBold>Microsoft ActiveX Data Objects x.x Library</legacyBold> from the list.</caps:sentence>
                    <caps:sentence sentenceid="7e1da16884450f967e5bfe25cf9174f6" id="tgt8" class="tgtSentence"> Verify that at least the following libraries are also selected:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8e915b410f8e33b053de9034e305f761" id="tgt9" class="tgtSentence">Visual Basic for Applications</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ce507321d06199e96cbfa0643ef0c23e" id="tgt10" class="tgtSentence">Visual Basic runtime objects and procedures</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1a047bd525127e4db3cf38b5ae44bfc4" id="tgt11" class="tgtSentence">Visual Basic objects and procedures</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d7f12225373c0ba306a4644d26e07b1f" id="tgt12" class="tgtSentence">OLE Automation</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fb580b3510ed12de7ded60dc5ad40eeb" id="tgt13" class="tgtSentence">Click <legacyBold>OK</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence sentenceid="70867a1838ecda9cfd380397bed91a59" id="tgt14" class="tgtSentence">You can use ADO just as easily with Visual Basic for Applications, by using Microsoft Access, for example.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="3863c1f94ecf62d14191773a7341f21f" id="tgt15" class="tgtSentence">To reference ADO from Microsoft Access</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9d90d953eaca3ff9ef4179e231095914" id="tgt16" class="tgtSentence">In Microsoft Access, select or create a module from the <legacyBold>Modules</legacyBold> tab in the <legacyBold>Database</legacyBold> window.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d694d95deec1f2286e416fc55d9d7a08" id="tgt17" class="tgtSentence">On the <legacyBold>Tools</legacyBold> menu, select <legacyBold>References...</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="21e6815ce3f677b4c700f792163b8c67" id="tgt18" class="tgtSentence">Select <legacyBold>Microsoft ActiveX Data Objects x.x Library</legacyBold> from the list.</caps:sentence>
                    <caps:sentence sentenceid="7e1da16884450f967e5bfe25cf9174f6" id="tgt19" class="tgtSentence"> Verify that at least the following libraries are also selected:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8e915b410f8e33b053de9034e305f761" id="tgt20" class="tgtSentence">Visual Basic for Applications</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="84a3659f172184f364c4ce4e96231d5f" id="tgt21" class="tgtSentence">Microsoft Access 8.0 Object Library (or later)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3e36b3441fcbc7187f68171b08abcbd5" id="tgt22" class="tgtSentence">Microsoft DAO 3.5 Object Library (or later)</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fb580b3510ed12de7ded60dc5ad40eeb" id="tgt23" class="tgtSentence">Click <legacyBold>OK</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c6862346ab5c2a65fc50a8959314235c" id="tgt24" class="tgtSentence">Creating ADO Objects in Visual Basic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="28f13dd66cb555cf838cdbc68f1f193d" id="tgt25" class="tgtSentence">To create an automation variable and an instance of an object for that variable, you can use two methods: <legacyBold>Dim</legacyBold> or <legacyBold>CreateObject</legacyBold>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="563728df0fdd90631ac1e51258e2857d" id="tgt26" class="tgtSentence">Dim</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9b931aeb5619d581088da71ba934479a" id="tgt27" class="tgtSentence">You can use the <legacyBold>New</legacyBold> keyword with <legacyBold>Dim</legacyBold> to declare and create instances of ADO objects in one step:</caps:sentence>
              </para>
              <code>Dim conn As New ADODB.Connection</code>
              <para>
                <caps:sentence sentenceid="6e3861c93a8499c0809f9e66475f1826" id="tgt28" class="tgtSentence">Alternatively, the <legacyBold>Dim </legacyBold>statement declaration and object instantiation can also be two steps:</caps:sentence>
              </para>
              <code>Dim conn As ADODB.Connection
Set conn = New ADODB.Connection</code>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="ecd03ad3f1324291f9b355a5304aa3aa" id="tgt29" class="tgtSentence">It is not required to explicitly use the <codeInline>ADODB</codeInline> progid with the <legacyBold>Dim</legacyBold> statement, assuming you have correctly referenced the ADO library in your project.</caps:sentence>
                  <caps:sentence sentenceid="9254010a5cf4237f9712ab5ef39eaf14" id="tgt30" class="tgtSentence"> However, using it ensures that you will not have naming conflicts with other libraries.</caps:sentence>
                </para>
              </alert>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="cdb44c412edaed8b1a838df5404c7f98" id="tgt31" class="tgtSentence">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating <legacyBold>Recordset</legacyBold> objects, as in the following code:</caps:sentence>
                </para>
              </alert>
              <code>Dim adoRS As ADODB.Recordset
Dim daoRS As DAO.Recordset</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="840bbd01aee8ad9cc55bf9f358e451d3" id="tgt32" class="tgtSentence">CreateObject</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="addd80cd3f81220c74b3a082627e9371" id="tgt33" class="tgtSentence">With the <legacyBold>CreateObject</legacyBold> method, the declaration and object instantiation must be two discrete steps:</caps:sentence>
              </para>
              <code>Dim conn1
Set conn1 = CreateObject("ADODB.Connection") As Object</code>
              <para>
                <caps:sentence sentenceid="0d4af6d9b33dab21a91385006eed171d" id="tgt34" class="tgtSentence">Objects instantiated with <legacyBold>CreateObject</legacyBold> are late-bound, which means that they are not strongly typed and command-line completion is disabled.</caps:sentence>
                <caps:sentence sentenceid="79d870debc04ddba3441eb9e737cc992" id="tgt35" class="tgtSentence"> However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects.</caps:sentence>
                <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt36" class="tgtSentence"> For example:</caps:sentence>
              </para>
              <code>Set conn1 = CreateObject("ADODB.Connection.2.0") As Object</code>
              <para>
                <caps:sentence sentenceid="8cceb23bb3a678f2465d168e6f644abb" id="tgt37" class="tgtSentence">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="09e70454d2e223629e3311a46ba14d9a" id="tgt38" class="tgtSentence">Instantiating objects by using the <legacyBold>CreateObject</legacyBold> method is typically slower than using the <legacyBold>Dim</legacyBold> statement.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="aa3ecfd7bf94dd3cc62f2d8ff235c31f" id="tgt39" class="tgtSentence">Handling Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="93a2507b62990793d67154bda2d96dea" id="tgt40" class="tgtSentence">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the <legacyBold>WithEvents</legacyBold> keyword.</caps:sentence>
            <caps:sentence sentenceid="f193139996e25ab6c063b708c94010eb" id="tgt41" class="tgtSentence"> The variable can be declared only as part of a class module and must be declared at the module level.</caps:sentence>
            <caps:sentence sentenceid="b91199041f7854ffd8dd575d28fd2092" id="tgt42" class="tgtSentence"> For a more thorough discussion of handling ADO events, see <legacyLink xlink:href="e9003457-0762-48b3-942f-0820266b158f">Handling ADO Events</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="e16dc19c4a59be8f0da8bc1cd82acf3f" id="tgt43" class="tgtSentence">Visual Basic Examples</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="023db38ee0adb82f62323fd197c2a845" id="tgt44" class="tgtSentence">Many Visual Basic examples are included with the ADO documentation.</caps:sentence>
            <caps:sentence sentenceid="4ff799afa7a37b208a3330a1e78f61c1" id="tgt45" class="tgtSentence"> For more information, see <legacyLink xlink:href="1152893e-b617-40f1-88b6-81e82e2234f1">ADO Code Examples in Microsoft Visual Basic</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">Using ADO with Microsoft Visual C++</link>
        <link xlink:href="15542c35-3bf7-4d5f-a3b2-3a5cff286987">Using ADO with Microsoft Visual J++</link>
        <link xlink:href="76fc4d00-0c9f-422b-af5c-af6ed8fb29d8">Using ADO with Scripting Languages</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Referencing the ADO Library</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The ADO library must be referenced by your project.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src5" class="srcSentence">To reference ADO from Microsoft Visual Basic</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">In Visual Basic, from the <legacyBold>Project</legacyBold> menu, select <legacyBold>References...</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Select <legacyBold>Microsoft ActiveX Data Objects x.x Library</legacyBold> from the list.</caps:sentence>
                    <caps:sentence id="src8" class="srcSentence"> Verify that at least the following libraries are also selected:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src9" class="srcSentence">Visual Basic for Applications</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src10" class="srcSentence">Visual Basic runtime objects and procedures</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src11" class="srcSentence">Visual Basic objects and procedures</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src12" class="srcSentence">OLE Automation</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Click <legacyBold>OK</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence id="src14" class="srcSentence">You can use ADO just as easily with Visual Basic for Applications, by using Microsoft Access, for example.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src15" class="srcSentence">To reference ADO from Microsoft Access</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">In Microsoft Access, select or create a module from the <legacyBold>Modules</legacyBold> tab in the <legacyBold>Database</legacyBold> window.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">On the <legacyBold>Tools</legacyBold> menu, select <legacyBold>References...</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Select <legacyBold>Microsoft ActiveX Data Objects x.x Library</legacyBold> from the list.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> Verify that at least the following libraries are also selected:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">Visual Basic for Applications</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">Microsoft Access 8.0 Object Library (or later)</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">Microsoft DAO 3.5 Object Library (or later)</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Click <legacyBold>OK</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Creating ADO Objects in Visual Basic</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">To create an automation variable and an instance of an object for that variable, you can use two methods: <legacyBold>Dim</legacyBold> or <legacyBold>CreateObject</legacyBold>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src26" class="srcSentence">Dim</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src27" class="srcSentence">You can use the <legacyBold>New</legacyBold> keyword with <legacyBold>Dim</legacyBold> to declare and create instances of ADO objects in one step:</caps:sentence>
              </para>
              <code>Dim conn As New ADODB.Connection</code>
              <para>
                <caps:sentence id="src28" class="srcSentence">Alternatively, the <legacyBold>Dim </legacyBold>statement declaration and object instantiation can also be two steps:</caps:sentence>
              </para>
              <code>Dim conn As ADODB.Connection
Set conn = New ADODB.Connection</code>
              <alert class="note">
                <para>
                  <caps:sentence id="src29" class="srcSentence">It is not required to explicitly use the <codeInline>ADODB</codeInline> progid with the <legacyBold>Dim</legacyBold> statement, assuming you have correctly referenced the ADO library in your project.</caps:sentence>
                  <caps:sentence id="src30" class="srcSentence"> However, using it ensures that you will not have naming conflicts with other libraries.</caps:sentence>
                </para>
              </alert>
              <alert class="note">
                <para>
                  <caps:sentence id="src31" class="srcSentence">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating <legacyBold>Recordset</legacyBold> objects, as in the following code:</caps:sentence>
                </para>
              </alert>
              <code>Dim adoRS As ADODB.Recordset
Dim daoRS As DAO.Recordset</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src32" class="srcSentence">CreateObject</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src33" class="srcSentence">With the <legacyBold>CreateObject</legacyBold> method, the declaration and object instantiation must be two discrete steps:</caps:sentence>
              </para>
              <code>Dim conn1
Set conn1 = CreateObject("ADODB.Connection") As Object</code>
              <para>
                <caps:sentence id="src34" class="srcSentence">Objects instantiated with <legacyBold>CreateObject</legacyBold> are late-bound, which means that they are not strongly typed and command-line completion is disabled.</caps:sentence>
                <caps:sentence id="src35" class="srcSentence"> However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects.</caps:sentence>
                <caps:sentence id="src36" class="srcSentence"> For example:</caps:sentence>
              </para>
              <code>Set conn1 = CreateObject("ADODB.Connection.2.0") As Object</code>
              <para>
                <caps:sentence id="src37" class="srcSentence">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src38" class="srcSentence">Instantiating objects by using the <legacyBold>CreateObject</legacyBold> method is typically slower than using the <legacyBold>Dim</legacyBold> statement.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src39" class="srcSentence">Handling Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src40" class="srcSentence">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the <legacyBold>WithEvents</legacyBold> keyword.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> The variable can be declared only as part of a class module and must be declared at the module level.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> For a more thorough discussion of handling ADO events, see <legacyLink xlink:href="e9003457-0762-48b3-942f-0820266b158f">Handling ADO Events</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src43" class="srcSentence">Visual Basic Examples</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src44" class="srcSentence">Many Visual Basic examples are included with the ADO documentation.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> For more information, see <legacyLink xlink:href="1152893e-b617-40f1-88b6-81e82e2234f1">ADO Code Examples in Microsoft Visual Basic</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">Using ADO with Microsoft Visual C++</link>
        <link xlink:href="15542c35-3bf7-4d5f-a3b2-3a5cff286987">Using ADO with Microsoft Visual J++</link>
        <link xlink:href="76fc4d00-0c9f-422b-af5c-af6ed8fb29d8">Using ADO with Scripting Languages</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
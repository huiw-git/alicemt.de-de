---
title: "RDS Tutorial"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6e3305a0-7bc7-40d1-9122-235c15d23ab2
caps.latest.revision: 14
caps.handback.revision: 14
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
# RDS Tutorial
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="791d6e7b491c69b27971993f015eacbf" id="tgt1" class="tgtSentence">This tutorial illustrates using the RDS programming model to query and update a data source.</caps:sentence>
          <caps:sentence sentenceid="6b7b824e2e0c25d762faff7996a597cc" id="tgt2" class="tgtSentence"> First, it describes the steps necessary to accomplish this task.</caps:sentence>
          <caps:sentence sentenceid="689ec13bb8e8e7a787d04cd8d6093e49" id="tgt3" class="tgtSentence"> Then the tutorial is repeated in Microsoft® Visual Basic Scripting Edition and Microsoft® Visual J++®, featuring ADO for Windows Foundation Classes (ADO/WFC).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="151dd7d8b4a8c256c99f725bb1161d50" id="tgt4" class="tgtSentence">This tutorial is coded in different languages for two reasons:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="91681b065ff0e5ef43b3a1a0b5bf9f64" id="tgt5" class="tgtSentence">The documentation for RDS assumes the reader codes in Visual Basic.</caps:sentence>
              <caps:sentence sentenceid="b7f5ac3c101dc0a146c5269b2461c6a7" id="tgt6" class="tgtSentence"> This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="23a0488a4e110f2c0119a1dc619d6c87" id="tgt7" class="tgtSentence">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt8" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt9" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt10" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt11" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="f68ff53e7b52b76a797a35c5fde432b5" id="tgt12" class="tgtSentence">How the Tutorial is Presented</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="03922e7c2ddf03a65a6da31d5e948b6a" id="tgt13" class="tgtSentence">This tutorial is based on the RDS programming model.</caps:sentence>
            <caps:sentence sentenceid="0ee2a8e8d2f7c9dbb7de84b3172513e8" id="tgt14" class="tgtSentence"> It discusses each step of the programming model individually.</caps:sentence>
            <caps:sentence sentenceid="32383618714abd4544e2bfe80e054b8c" id="tgt15" class="tgtSentence"> In addition, it illustrates each step with a fragment of Visual Basic code.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a138704ba8344716bbb255e9884aca0a" id="tgt16" class="tgtSentence">The code example is repeated in other languages with minimal discussion.</caps:sentence>
            <caps:sentence sentenceid="f6654f15079972bda773d27c6c7993f2" id="tgt17" class="tgtSentence"> Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial.</caps:sentence>
            <caps:sentence sentenceid="f8e2aed646d591cc5d9fb759e461c9c5" id="tgt18" class="tgtSentence"> Use the number of the step to refer to the discussion in the descriptive tutorial.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="107e0620b25cad8f1bab2dfe091cab98" id="tgt19" class="tgtSentence">The RDS programming model is stated in the following section.</caps:sentence>
            <caps:sentence sentenceid="829054354de696393b140ae95c773e53" id="tgt20" class="tgtSentence"> Use it as a roadmap as you proceed through the tutorial.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="35683e2bdee02394050066d41498063f" id="tgt21" class="tgtSentence">RDS Programming Model with Objects</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="470c3b90b74b65e599f5503964c17bbc" id="tgt22" class="tgtSentence">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="83f2b4f3d98548dba9b841e8d943777d" id="tgt23" class="tgtSentence">Invoke the server program.</caps:sentence>
                <caps:sentence sentenceid="1009e5af227d76b862e4ca8d30f37061" id="tgt24" class="tgtSentence"> Pass parameters to the server program that identifies the data source and the command to issue.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="22dc421d101c5632a3c5054488d92d73" id="tgt25" class="tgtSentence">The server program obtains a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object from the data source, typically by using ADO.</caps:sentence>
                <caps:sentence sentenceid="80b526a6b97214c09e6ad55e88561d3e" id="tgt26" class="tgtSentence"> Optionally, the <legacyBold>Recordset</legacyBold> object is processed on the server.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="da8c00386481dccbfb215d2b73c38227" id="tgt27" class="tgtSentence">The server program returns the final <legacyBold>Recordset</legacyBold> object to the client application.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b379bcd42be6600d18136692d12203c0" id="tgt28" class="tgtSentence">On the client, the <legacyBold>Recordset</legacyBold> object is optionally put into a form that can be easily used by visual controls.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="67650438e4d4154e3ed7291c0055f1ae" id="tgt29" class="tgtSentence">Changes to the <legacyBold>Recordset</legacyBold> object are sent back to the server and used to update the data source.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="b56c634b44809acab4cdd095c0e5015c" id="tgt30" class="tgtSentence">This tutorial contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="c1be9c8d875e55c26f6f89c3a810bcc5" id="tgt31" class="tgtSentence">
                  <legacyLink xlink:href="d8bb35b1-c02a-4231-8d55-016e56e53b95">Step 1: Specify a Server Program (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="62cba145ec01ba62fb0ba09cbd31ea3a" id="tgt32" class="tgtSentence">
                  <legacyLink xlink:href="5e74c2da-65ee-4de4-8b41-6eac45c3632e">Step 2: Invoke the Server Program (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8464c8123214cda7dabcae556d0903d4" id="tgt33" class="tgtSentence">
                  <legacyLink xlink:href="9c6779c9-1208-4696-ac51-c39f3a6d9240">Step 3: Server Obtains a Recordset (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8fd3ca9ed2023f6d7a38c8f19c7eaf5d" id="tgt34" class="tgtSentence">
                  <legacyLink xlink:href="3d1855c4-419c-4810-b5ea-6c874b5e2905">Step 4: Server Returns the Recordset (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="98a8f732679fab40a7e1a8d58d57e714" id="tgt35" class="tgtSentence">
                  <legacyLink xlink:href="ed5c4a24-9804-4c85-817e-317652acb9b4">Step 5: DataControl is Made Usable (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2a3186882ee88b2238fa352b9c877c56" id="tgt36" class="tgtSentence">
                  <legacyLink xlink:href="b1e927d6-7d50-4978-9eef-045043cdce7a">Step 6: Changes are Sent to the Server (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1543a1d9d9998dd7e93124413fd3849b" id="tgt37" class="tgtSentence">
                  <legacyLink xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2077b4680a8dbcf6d1c4746e049a15a6" id="tgt38" class="tgtSentence">
                  <legacyLink xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d8bb35b1-c02a-4231-8d55-016e56e53b95">Step 1: Specify a Server Program (RDS Tutorial)</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This tutorial illustrates using the RDS programming model to query and update a data source.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> First, it describes the steps necessary to accomplish this task.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Then the tutorial is repeated in Microsoft® Visual Basic Scripting Edition and Microsoft® Visual J++®, featuring ADO for Windows Foundation Classes (ADO/WFC).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">This tutorial is coded in different languages for two reasons:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">The documentation for RDS assumes the reader codes in Visual Basic.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence id="src8" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">How the Tutorial is Presented</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">This tutorial is based on the RDS programming model.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> It discusses each step of the programming model individually.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> In addition, it illustrates each step with a fragment of Visual Basic code.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">The code example is repeated in other languages with minimal discussion.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Use the number of the step to refer to the discussion in the descriptive tutorial.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">The RDS programming model is stated in the following section.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Use it as a roadmap as you proceed through the tutorial.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">RDS Programming Model with Objects</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">Invoke the server program.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> Pass parameters to the server program that identifies the data source and the command to issue.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src25" class="srcSentence">The server program obtains a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object from the data source, typically by using ADO.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> Optionally, the <legacyBold>Recordset</legacyBold> object is processed on the server.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src27" class="srcSentence">The server program returns the final <legacyBold>Recordset</legacyBold> object to the client application.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src28" class="srcSentence">On the client, the <legacyBold>Recordset</legacyBold> object is optionally put into a form that can be easily used by visual controls.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src29" class="srcSentence">Changes to the <legacyBold>Recordset</legacyBold> object are sent back to the server and used to update the data source.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src30" class="srcSentence">This tutorial contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src31" class="srcSentence">
                  <legacyLink xlink:href="d8bb35b1-c02a-4231-8d55-016e56e53b95">Step 1: Specify a Server Program (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src32" class="srcSentence">
                  <legacyLink xlink:href="5e74c2da-65ee-4de4-8b41-6eac45c3632e">Step 2: Invoke the Server Program (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">
                  <legacyLink xlink:href="9c6779c9-1208-4696-ac51-c39f3a6d9240">Step 3: Server Obtains a Recordset (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">
                  <legacyLink xlink:href="3d1855c4-419c-4810-b5ea-6c874b5e2905">Step 4: Server Returns the Recordset (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">
                  <legacyLink xlink:href="ed5c4a24-9804-4c85-817e-317652acb9b4">Step 5: DataControl is Made Usable (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">
                  <legacyLink xlink:href="b1e927d6-7d50-4978-9eef-045043cdce7a">Step 6: Changes are Sent to the Server (RDS Tutorial)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src37" class="srcSentence">
                  <legacyLink xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src38" class="srcSentence">
                  <legacyLink xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d8bb35b1-c02a-4231-8d55-016e56e53b95">Step 1: Specify a Server Program (RDS Tutorial)</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
        <link xlink:href="d0d735e0-669a-41e7-ada2-8dd80924e349">RDS Tutorial (Visual J++)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
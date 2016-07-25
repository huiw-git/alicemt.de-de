---
title: "SubmitChanges Method (RDS)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 250062a4-13c4-4bed-807d-8b9ad81536d4
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
# SubmitChanges Method (RDS)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="778d871cfcc0ce1b32f926135c311e4e" id="tgt1" class="tgtSentence">Submits pending changes of the locally cached and updatable <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to the data source specified in the <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property or the <legacyLink xlink:href="8c56b233-1be8-442c-8d0e-a4c96465bc99">URL</legacyLink> property.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>DataControl.</parameterReference>
          <legacyBold>SubmitChanges </legacyBold>
          <parameterReference>DataFactory</parameterReference>.<legacyBold>SubmitChanges </legacyBold><parameterReference>Connection, Recordset</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="033f425d12dfef3857c30172a3b63457" id="tgt6" class="tgtSentence"> <legacyItalic>DataControl</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0f504ae70ec16a59af2497e524453cfb" id="tgt7" class="tgtSentence">An object variable that represents an <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="41531125f69098131facc32b1b8f2d1d" id="tgt8" class="tgtSentence"> <legacyItalic>DataFactory</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="35dd05598ab8303c73bc9037d548f6b2" id="tgt9" class="tgtSentence">An object variable that represents an <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="18940e08e082b35b38fb8cfe58b0bed5" id="tgt10" class="tgtSentence"> <legacyItalic>Connection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="8171b8494c1a11c66d7e80a20ef300d0" id="tgt11" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that represents the connection created with the <unmanagedCodeEntityReference>RDS.DataControl</unmanagedCodeEntityReference> object's <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f12c824c1f08397ff9ad9725419e444a" id="tgt12" class="tgtSentence"> <legacyItalic>Recordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b960ef4e9b331de17c921bc5c68a4a1b" id="tgt13" class="tgtSentence">An object variable that represents a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="a30bd08ef156327babdc6569b562a40e" id="tgt14" class="tgtSentence">The <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink>, <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server</legacyLink>, and <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> properties must be set before you can use the <unmanagedCodeEntityReference>SubmitChanges</unmanagedCodeEntityReference> method with the <unmanagedCodeEntityReference>RDS.DataControl</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="32b58cbd562c4e3fca3f2888b717249b" id="tgt15" class="tgtSentence">If you call the <legacyLink xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate</legacyLink> method after you have called <unmanagedCodeEntityReference>SubmitChanges</unmanagedCodeEntityReference> for the same <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, the <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> call fails because the changes have already been committed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8e0aed6b121707bd9ef1cbe110416864" id="tgt16" class="tgtSentence">Only the changed records are sent for modification, and either all of the changes succeed or all the changes fail together.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5a9d6eec8446f0b3b5375ef197771856" id="tgt17" class="tgtSentence">You can use <unmanagedCodeEntityReference>SubmitChanges</unmanagedCodeEntityReference> only with the default <unmanagedCodeEntityReference>RDSServer.DataFactory</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="ccc0331194ea62aa21aced289504cee9" id="tgt18" class="tgtSentence"> Custom business objects cannot use this method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e6ba783cee176dab695e30e3fdd7bcdb" id="tgt19" class="tgtSentence">If the <unmanagedCodeEntityReference>URL</unmanagedCodeEntityReference> property has been set, <unmanagedCodeEntityReference>SubmitChanges</unmanagedCodeEntityReference> will submit changes to the location specified by the URL.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt20" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="619bc7fd-ad0a-44ea-9678-ad40a662c258">VBScript Example</link>
        <link xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Submits pending changes of the locally cached and updatable <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to the data source specified in the <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property or the <legacyLink xlink:href="8c56b233-1be8-442c-8d0e-a4c96465bc99">URL</legacyLink> property.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>DataControl.</parameterReference>
          <legacyBold>SubmitChanges </legacyBold>
          <parameterReference>DataFactory</parameterReference>.<legacyBold>SubmitChanges </legacyBold><parameterReference>Connection, Recordset</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>DataControl</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An object variable that represents an <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>DataFactory</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">An object variable that represents an <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">RDSServer.DataFactory</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>Connection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">A <languageKeyword>String</languageKeyword> value that represents the connection created with the <unmanagedCodeEntityReference>RDS.DataControl</unmanagedCodeEntityReference> object's <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink> property.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>Recordset</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">An object variable that represents a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">The <legacyLink xlink:href="dbad5e77-b213-4eb8-aecf-d60f203fdb59">Connect</legacyLink>, <legacyLink xlink:href="d2727ce7-da9f-4271-ae3c-9334ef477c14">Server</legacyLink>, and <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> properties must be set before you can use the <unmanagedCodeEntityReference>SubmitChanges</unmanagedCodeEntityReference> method with the <unmanagedCodeEntityReference>RDS.DataControl</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">If you call the <legacyLink xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate</legacyLink> method after you have called <unmanagedCodeEntityReference>SubmitChanges</unmanagedCodeEntityReference> for the same <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, the <unmanagedCodeEntityReference>CancelUpdate</unmanagedCodeEntityReference> call fails because the changes have already been committed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">Only the changed records are sent for modification, and either all of the changes succeed or all the changes fail together.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">You can use <unmanagedCodeEntityReference>SubmitChanges</unmanagedCodeEntityReference> only with the default <unmanagedCodeEntityReference>RDSServer.DataFactory</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Custom business objects cannot use this method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">If the <unmanagedCodeEntityReference>URL</unmanagedCodeEntityReference> property has been set, <unmanagedCodeEntityReference>SubmitChanges</unmanagedCodeEntityReference> will submit changes to the location specified by the URL.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="619bc7fd-ad0a-44ea-9678-ad40a662c258">VBScript Example</link>
        <link xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
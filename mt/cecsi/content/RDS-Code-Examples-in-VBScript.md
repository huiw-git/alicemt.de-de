---
title: "RDS Code Examples in VBScript"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 22f23c30-7c21-4fe3-8e76-36cea6448819
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
# RDS Code Examples in VBScript
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt1" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt2" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt3" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt4" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="43baec504f87d34ffd5de890980214c4" id="tgt5" class="tgtSentence">Use the following code examples to learn how to use the RDS objects, methods, and properties when writing in Microsoft Visual Basic Scripting Edition (VBScript).</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="60112f1437485d0ce0860afad2afc9f3" id="tgt6" class="tgtSentence">Paste the entire code example into your code editor.</caps:sentence>
            <caps:sentence sentenceid="d0af02b2a7f5e8d60d6ca45d510c2f3c" id="tgt7" class="tgtSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="5891da2d64975cae48d175d1e001f5da" id="tgt8" class="tgtSentence">Objects</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="4f306a51-d5a4-4785-b426-487639cda164">
                  <caps:sentence sentenceid="2e8e1caa6dc1f2cdc8ae00a4dd761db2" id="tgt9" class="tgtSentence">DataControl Object Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="12b0e160-5e5c-441f-bed7-ac0bd061e003">
                  <caps:sentence sentenceid="82083029cd7eaf5eb4ec8bbcda0ca735" id="tgt10" class="tgtSentence">DataSpace Object Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="b4e2844a-120a-4513-860b-f1b6e4b5dda4">
                  <caps:sentence sentenceid="240e7dcad88c9d41712a161d85227cdf" id="tgt11" class="tgtSentence">DataFactory Object Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt12" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="4ade106d-063d-486e-bc4d-a1a6b6e0bea9">
                  <caps:sentence sentenceid="7b55194e72a2f0feb64fb925b2e48bbc" id="tgt13" class="tgtSentence">Cancel Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="c23912f0-1288-4727-8fb4-f643b8811cf7">
                  <caps:sentence sentenceid="982e7110e8728e7a2202a8b2885ff9e4" id="tgt14" class="tgtSentence">CancelUpdate Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="edd0a01c-1a1b-4b91-9966-2529e244abae">
                  <caps:sentence sentenceid="3cd0da21f753140e99de8fd3653ae734" id="tgt15" class="tgtSentence">ConvertToString Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="12b0e160-5e5c-441f-bed7-ac0bd061e003">
                  <caps:sentence sentenceid="2641d4c5806c30dba63c5771d8446d95" id="tgt16" class="tgtSentence">CreateObject Method</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="cce0d8b5-e87b-4f7b-a8a0-37d5025a1f5d">
                  <caps:sentence sentenceid="48e8473951a30da79f3d4d8f8880d9d6" id="tgt17" class="tgtSentence">CreateRecordset Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="b4e2844a-120a-4513-860b-f1b6e4b5dda4">
                  <caps:sentence sentenceid="2709b257a98a225920b0b6d436f0a87f" id="tgt18" class="tgtSentence">Query Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="f2926578-bc60-464b-916e-ddfdb8014253">
                  <caps:sentence sentenceid="780aef6f1380f3a9e9ccfd5e71065b5d" id="tgt19" class="tgtSentence">Refresh Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="8a74802f-34d6-4676-bf94-07df5f8bff66">
                  <caps:sentence sentenceid="ccdec0c8a87f85386bec72ee7b07efd5" id="tgt20" class="tgtSentence">Reset Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="619bc7fd-ad0a-44ea-9678-ad40a662c258">
                  <caps:sentence sentenceid="004010c3f50d76a6bc7e6b476cbe0cfc" id="tgt21" class="tgtSentence">SubmitChanges Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt22" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="06297993-fe72-4446-aa76-3b8bc25444f6">
                  <caps:sentence sentenceid="686fcd42e6015971a86a7aac06252d8c" id="tgt23" class="tgtSentence">Connect Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="753a4a3d-0fba-40b8-86e7-50b34182ca69">
                  <caps:sentence sentenceid="a0a4593c7d7544249c9302f245baa04b" id="tgt24" class="tgtSentence">ExecuteOptions and FetchOptions Properties Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="8a74802f-34d6-4676-bf94-07df5f8bff66">
                  <caps:sentence sentenceid="ff07261f676d13914a6d3ed17b1d6cc7" id="tgt25" class="tgtSentence">FilterColumn, FilterCriterion, FilterValue, SortColumn, and SortDirection Properties Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="e3e18da4-0511-4ece-a35d-699978bc28c6">
                  <caps:sentence sentenceid="bd27386a0a32b4e2dac0d2b509eab5e9" id="tgt26" class="tgtSentence">ReadyState Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="95175316-cd10-4cf7-96ba-2a226fd97701">
                  <caps:sentence sentenceid="b9d1da6188404fc3fcd5c740f94829a6" id="tgt27" class="tgtSentence">Recordset and SourceRecordset Properties Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="0fe57af9-a4d0-4986-a2e3-beaa4d26ed58">
                  <caps:sentence sentenceid="59b215b9983dedfc5dd4b74aefe6922a" id="tgt28" class="tgtSentence">Server Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="32c33bcf-3320-4836-9e2e-99c8978ce581">
                  <caps:sentence sentenceid="52a5c6f1e99ad81b3d24c60c813fa861" id="tgt29" class="tgtSentence">SQL Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="6ae5ac50-c88c-4262-b7ab-f2b3de382a0b">
                  <caps:sentence sentenceid="4abec7a2cd34df2cf9021d1c4b672785" id="tgt30" class="tgtSentence">URL Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src5" class="srcSentence">Use the following code examples to learn how to use the RDS objects, methods, and properties when writing in Microsoft Visual Basic Scripting Edition (VBScript).</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src6" class="srcSentence">Paste the entire code example into your code editor.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Objects</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="4f306a51-d5a4-4785-b426-487639cda164">
                  <caps:sentence id="src9" class="srcSentence">DataControl Object Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="12b0e160-5e5c-441f-bed7-ac0bd061e003">
                  <caps:sentence id="src10" class="srcSentence">DataSpace Object Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="b4e2844a-120a-4513-860b-f1b6e4b5dda4">
                  <caps:sentence id="src11" class="srcSentence">DataFactory Object Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="4ade106d-063d-486e-bc4d-a1a6b6e0bea9">
                  <caps:sentence id="src13" class="srcSentence">Cancel Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="c23912f0-1288-4727-8fb4-f643b8811cf7">
                  <caps:sentence id="src14" class="srcSentence">CancelUpdate Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="edd0a01c-1a1b-4b91-9966-2529e244abae">
                  <caps:sentence id="src15" class="srcSentence">ConvertToString Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="12b0e160-5e5c-441f-bed7-ac0bd061e003">
                  <caps:sentence id="src16" class="srcSentence">CreateObject Method</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="cce0d8b5-e87b-4f7b-a8a0-37d5025a1f5d">
                  <caps:sentence id="src17" class="srcSentence">CreateRecordset Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="b4e2844a-120a-4513-860b-f1b6e4b5dda4">
                  <caps:sentence id="src18" class="srcSentence">Query Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="f2926578-bc60-464b-916e-ddfdb8014253">
                  <caps:sentence id="src19" class="srcSentence">Refresh Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="8a74802f-34d6-4676-bf94-07df5f8bff66">
                  <caps:sentence id="src20" class="srcSentence">Reset Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="619bc7fd-ad0a-44ea-9678-ad40a662c258">
                  <caps:sentence id="src21" class="srcSentence">SubmitChanges Method Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="06297993-fe72-4446-aa76-3b8bc25444f6">
                  <caps:sentence id="src23" class="srcSentence">Connect Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="753a4a3d-0fba-40b8-86e7-50b34182ca69">
                  <caps:sentence id="src24" class="srcSentence">ExecuteOptions and FetchOptions Properties Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="8a74802f-34d6-4676-bf94-07df5f8bff66">
                  <caps:sentence id="src25" class="srcSentence">FilterColumn, FilterCriterion, FilterValue, SortColumn, and SortDirection Properties Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="e3e18da4-0511-4ece-a35d-699978bc28c6">
                  <caps:sentence id="src26" class="srcSentence">ReadyState Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="95175316-cd10-4cf7-96ba-2a226fd97701">
                  <caps:sentence id="src27" class="srcSentence">Recordset and SourceRecordset Properties Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="0fe57af9-a4d0-4986-a2e3-beaa4d26ed58">
                  <caps:sentence id="src28" class="srcSentence">Server Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="32c33bcf-3320-4836-9e2e-99c8978ce581">
                  <caps:sentence id="src29" class="srcSentence">SQL Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="6ae5ac50-c88c-4262-b7ab-f2b3de382a0b">
                  <caps:sentence id="src30" class="srcSentence">URL Property Example</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
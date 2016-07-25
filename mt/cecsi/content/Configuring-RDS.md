---
title: "Configuring RDS"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5dd48483-858a-48c2-98ce-f2359abe1f59
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
# Configuring RDS
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
          <caps:sentence sentenceid="5c4d5bc47234efe8a5bb266b016c9b57" id="tgt5" class="tgtSentence">To implement RDS efficiently, be sure you are familiar with the various configurations available to you.</caps:sentence>
          <caps:sentence sentenceid="faeb2f8cefa744eb899fedbefc3bd381" id="tgt6" class="tgtSentence"> This section includes important information about security and scalability in your implementation of RDS.</caps:sentence>
          <caps:sentence sentenceid="9a85b9db7cdba5c4c040837e4206e572" id="tgt7" class="tgtSentence"> See the following topics for information about configuring your computers to use RDS.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="ead1bac49139f3583bc84851e3b2715d" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="e851a22d-01bc-4eb0-bc42-92b8f65d1c63">Granting Guest Privileges to a Web Server Computer</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ecafa4f6caf1ba5e1919c69bfeda920f" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="e9032ad8-d14c-42e3-ba13-cb5f00084a79">Registering a Custom Business Object</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8332bc6938c5d1ff84fb1e5ac948efab" id="tgt10" class="tgtSentence">             <legacyLink xlink:href="0be98d1a-ab3d-4dce-a166-dacda10d154a">Marking Business Objects as Safe for Scripting</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c0c0177b1fb86943e084b5ab3ae377fe" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="75a21910-607f-463a-ae18-a17130dafb7e">Registering Business Objects on the Client for Use with DCOM</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="54cd5ff0fc5f73021fb8b18d5f0d885c" id="tgt12" class="tgtSentence">             <legacyLink xlink:href="46664ac5-d6e6-4457-8bae-3a98300f2a41">Setting DCOM Stream Marshaling Format</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a2d7e511e0b2e310f9bae45e465cba56" id="tgt13" class="tgtSentence">             <legacyLink xlink:href="5f1c2205-191c-4fb4-9bd9-84c878ea46ed">Enabling a DLL to Run on DCOM</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e68015e956b8af1889c2e0f913fca5fa" id="tgt14" class="tgtSentence">             <legacyLink xlink:href="2b4786c6-40c4-4ce1-9ad4-03df436e0aff">Configuring Virtual Servers on IIS</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5be506aae832aaf8d161990a97705fe6" id="tgt15" class="tgtSentence">             <legacyLink xlink:href="82fb1330-d6c6-4c17-ad3e-d417ff822b25">Securing RDS Applications</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="46660bcbf4fb0a894eb15521d39c5346" id="tgt16" class="tgtSentence">             <legacyLink xlink:href="8ff24805-dc7a-42ae-b600-5bad0e3f51b8">Configuring DataFactory for Safe or Unrestricted Modes</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a98a7245-06a7-455c-82ef-950807b9f1e7">Using Related Technologies with RDS</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="92905044-579f-4c38-bca6-f8bd5b239c20">Troubleshooting RDS</link>
      </relatedTopics>
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
          <caps:sentence id="src5" class="srcSentence">To implement RDS efficiently, be sure you are familiar with the various configurations available to you.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> This section includes important information about security and scalability in your implementation of RDS.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> See the following topics for information about configuring your computers to use RDS.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="e851a22d-01bc-4eb0-bc42-92b8f65d1c63">Granting Guest Privileges to a Web Server Computer</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="e9032ad8-d14c-42e3-ba13-cb5f00084a79">Registering a Custom Business Object</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">             <legacyLink xlink:href="0be98d1a-ab3d-4dce-a166-dacda10d154a">Marking Business Objects as Safe for Scripting</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="75a21910-607f-463a-ae18-a17130dafb7e">Registering Business Objects on the Client for Use with DCOM</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">             <legacyLink xlink:href="46664ac5-d6e6-4457-8bae-3a98300f2a41">Setting DCOM Stream Marshaling Format</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">             <legacyLink xlink:href="5f1c2205-191c-4fb4-9bd9-84c878ea46ed">Enabling a DLL to Run on DCOM</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">             <legacyLink xlink:href="2b4786c6-40c4-4ce1-9ad4-03df436e0aff">Configuring Virtual Servers on IIS</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">             <legacyLink xlink:href="82fb1330-d6c6-4c17-ad3e-d417ff822b25">Securing RDS Applications</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">             <legacyLink xlink:href="8ff24805-dc7a-42ae-b600-5bad0e3f51b8">Configuring DataFactory for Safe or Unrestricted Modes</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a98a7245-06a7-455c-82ef-950807b9f1e7">Using Related Technologies with RDS</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="92905044-579f-4c38-bca6-f8bd5b239c20">Troubleshooting RDS</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
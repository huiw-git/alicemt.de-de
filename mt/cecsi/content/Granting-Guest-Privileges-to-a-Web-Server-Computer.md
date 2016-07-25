---
title: "Granting Guest Privileges to a Web Server Computer"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e851a22d-01bc-4eb0-bc42-92b8f65d1c63
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
# Granting Guest Privileges to a Web Server Computer
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7e0fbb45059ca5dc3d45ebbd17df2663" id="tgt1" class="tgtSentence">The anonymous Web server account (IUSR_<legacyItalic>ComputerName</legacyItalic>) must be added to the Guests local group on the Web server computer to use RDS.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt2" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt3" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt4" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt5" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence sentenceid="621e5a144f5c6d2eeb2e20c09ad5bec5" id="tgt6" class="tgtSentence">To grant guest privileges to a Web server computer</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="aa40f2822f071e61babad1fb6bd8575b" id="tgt7" class="tgtSentence">On your Microsoft Windows 2000 Server computer, click <legacyBold>Start</legacyBold>, point to <legacyBold>Programs</legacyBold>, point to <legacyBold>Administrative Tools</legacyBold>, and then click <legacyBold>Computer Management</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="eebda95e6ea70293eaf11db37453cfc6" id="tgt8" class="tgtSentence">In the console tree, in <legacyBold>Local Users and Groups</legacyBold>, click <legacyBold>Groups</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="aee496065938618f6a4f124f1b857cbf" id="tgt9" class="tgtSentence">Select the <legacyBold>Guests</legacyBold> local group.</caps:sentence>
                  <caps:sentence sentenceid="051a5f6d852fadeffb8defb4b15092f5" id="tgt10" class="tgtSentence"> From the <legacyBold>Action</legacyBold> menu, choose <legacyBold>Properties</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="2cdcc44af701b92d48657b396bb3b35b" id="tgt11" class="tgtSentence">In the <legacyBold>Guests Properties</legacyBold> dialog box, click <legacyBold>Add</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="e775832150536ad09c31d35e0b7baab9" id="tgt12" class="tgtSentence">If the anonymous Web server account does not appear in the list in the <legacyBold>Select Users or Groups</legacyBold> dialog box, type its name (IUSR_<legacyItalic>ComputerName</legacyItalic>) into the bottom blank box, and then click <legacyBold>Add</legacyBold>.</caps:sentence>
                </para>
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
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The anonymous Web server account (IUSR_<legacyItalic>ComputerName</legacyItalic>) must be added to the Guests local group on the Web server computer to use RDS.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src2" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence id="src6" class="srcSentence">To grant guest privileges to a Web server computer</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src7" class="srcSentence">On your Microsoft Windows 2000 Server computer, click <legacyBold>Start</legacyBold>, point to <legacyBold>Programs</legacyBold>, point to <legacyBold>Administrative Tools</legacyBold>, and then click <legacyBold>Computer Management</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src8" class="srcSentence">In the console tree, in <legacyBold>Local Users and Groups</legacyBold>, click <legacyBold>Groups</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Select the <legacyBold>Guests</legacyBold> local group.</caps:sentence>
                  <caps:sentence id="src10" class="srcSentence"> From the <legacyBold>Action</legacyBold> menu, choose <legacyBold>Properties</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src11" class="srcSentence">In the <legacyBold>Guests Properties</legacyBold> dialog box, click <legacyBold>Add</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src12" class="srcSentence">If the anonymous Web server account does not appear in the list in the <legacyBold>Select Users or Groups</legacyBold> dialog box, type its name (IUSR_<legacyItalic>ComputerName</legacyItalic>) into the bottom blank box, and then click <legacyBold>Add</legacyBold>.</caps:sentence>
                </para>
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
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
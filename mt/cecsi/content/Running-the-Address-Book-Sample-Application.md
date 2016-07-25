---
title: "Running the Address Book Sample Application"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a2644e9-d634-4ae6-a5b7-13fb7b317ec7
caps.latest.revision: 13
caps.handback.revision: 13
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
# Running the Address Book Sample Application
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
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
          <caps:sentence sentenceid="25e1e576691c967fef60b4ffa09481c8" id="tgt5" class="tgtSentence">To run the Address Book application, follow this procedure.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt6" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt7" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt8" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt9" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence sentenceid="57fc0bf690fc0099d640db38ce3df079" id="tgt10" class="tgtSentence">To run this application</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="e9f0c1f6023ac73940ccee0468b57721" id="tgt11" class="tgtSentence">Make sure that Microsoft SQL Server is running.</caps:sentence>
                  <caps:sentence sentenceid="9ad286597f897fdc724bd27857d0d2c1" id="tgt12" class="tgtSentence"> Click <legacyBold>Start</legacyBold>, point to <legacyBold>Programs</legacyBold>, point to <legacyBold>Microsoft SQL Server 7.0</legacyBold>, and then click <legacyBold>Service Manager</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="2d841ed4f863e9f61d2bb7e417341128" id="tgt13" class="tgtSentence"> If there is a green arrow in the white circle, then SQL Server is running.</caps:sentence>
                  <caps:sentence sentenceid="cdcfec6cb62aefe1acc3f159ef0e4e72" id="tgt14" class="tgtSentence"> If it is not (there will be a red square in the white circle), click <legacyBold>Start/Continue</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="44c0c98a984dd717d8b3bd6eaa10934c" id="tgt15" class="tgtSentence">In Microsoft Internet Explorer 4.0 or later, type the following address: </caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="6033d25395b3b4c9fd346c468b8df61e" id="tgt16" class="tgtSentence">                 <legacyBold>http://</legacyBold>                 <legacyItalic>webserver</legacyItalic>                 <legacyBold>/RDS/AddressBook/AddrBook.asp</legacyBold>               </caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="839483dfe3e4255d45139d9201d266bc" id="tgt17" class="tgtSentence">where <legacyItalic>webserver</legacyItalic> is the name of the Web server where the RDS server components are installed.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="a98cac2a4903e5ac6a78ebf0ff6cc6fe" id="tgt18" class="tgtSentence">You can then try various scenarios in the Address Book sample application, such as searching for a person based on his or her e-mail name, listing all people with the title "Program Manager," or editing existing records.</caps:sentence>
                  <caps:sentence sentenceid="74102e45d0f04a5e995b8fcf255a81eb" id="tgt19" class="tgtSentence"> Click <legacyBold>Find</legacyBold> to fill the data grid with all the available names.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <relatedTopics>
        <link xlink:href="080c1925-d453-4b89-92ac-c93591490518">Address Book Data-Binding Object</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
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
          <caps:sentence id="src5" class="srcSentence">To run the Address Book application, follow this procedure.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src6" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <procedure>
          <title>
            <caps:sentence id="src10" class="srcSentence">To run this application</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Make sure that Microsoft SQL Server is running.</caps:sentence>
                  <caps:sentence id="src12" class="srcSentence"> Click <legacyBold>Start</legacyBold>, point to <legacyBold>Programs</legacyBold>, point to <legacyBold>Microsoft SQL Server 7.0</legacyBold>, and then click <legacyBold>Service Manager</legacyBold>.</caps:sentence>
                  <caps:sentence id="src13" class="srcSentence"> If there is a green arrow in the white circle, then SQL Server is running.</caps:sentence>
                  <caps:sentence id="src14" class="srcSentence"> If it is not (there will be a red square in the white circle), click <legacyBold>Start/Continue</legacyBold>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src15" class="srcSentence">In Microsoft Internet Explorer 4.0 or later, type the following address: </caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src16" class="srcSentence">                 <legacyBold>http://</legacyBold>                 <legacyItalic>webserver</legacyItalic>                 <legacyBold>/RDS/AddressBook/AddrBook.asp</legacyBold>               </caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src17" class="srcSentence">where <legacyItalic>webserver</legacyItalic> is the name of the Web server where the RDS server components are installed.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src18" class="srcSentence">You can then try various scenarios in the Address Book sample application, such as searching for a person based on his or her e-mail name, listing all people with the title "Program Manager," or editing existing records.</caps:sentence>
                  <caps:sentence id="src19" class="srcSentence"> Click <legacyBold>Find</legacyBold> to fill the data grid with all the available names.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
        </procedure>
      </introduction>
      <relatedTopics>
        <link xlink:href="080c1925-d453-4b89-92ac-c93591490518">Address Book Data-Binding Object</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
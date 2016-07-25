---
title: "Marking Business Objects as Safe for Scripting"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0be98d1a-ab3d-4dce-a166-dacda10d154a
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
# Marking Business Objects as Safe for Scripting
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
          <caps:sentence sentenceid="9bf1e32ddd767e9b2f379819ba6ebdbe" id="tgt5" class="tgtSentence">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object's <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method as "safe for scripting."</caps:sentence>
          <caps:sentence sentenceid="e93465774b02426196c0432abad8d90e" id="tgt6" class="tgtSentence"> You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="6a710f2a5fc88a5fcc9e104b07f9073e" id="tgt7" class="tgtSentence">Business objects marked as "safe for scripting" or safe for initialization can be instantiated and initialized by anyone over the network.</caps:sentence>
            <caps:sentence sentenceid="ca50aaaa824c530d0317f397f2c097df" id="tgt8" class="tgtSentence"> Marking a business object "safe for scripting" does not make it safe.</caps:sentence>
            <caps:sentence sentenceid="207d15ce6b4418d7fdfc1544c17cdf8e" id="tgt9" class="tgtSentence"> It is vitally important to make sure business objects are coded with the highest security to ensure that such objects do not present an unprotected access point for sensitive data.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="16aeaaa3409dc1cc3894664b772fcc9d" id="tgt10" class="tgtSentence">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text.</caps:sentence>
          <caps:sentence sentenceid="91aa4aa7d544683fc840a119a93a8a8f" id="tgt11" class="tgtSentence"> In this example, &lt;<legacyItalic>MyActiveXGUID</legacyItalic>&gt; is the hexadecimal GUID number of your business object.</caps:sentence>
          <caps:sentence sentenceid="d5bafaa5be8736ad2b6e17ec718ad559" id="tgt12" class="tgtSentence"> The following two numbers enable the safe-for-scripting feature:</caps:sentence>
        </para>
        <code>[HKEY_CLASSES_ROOT\CLSID\&lt;<legacyItalic xmlns="">MyActiveXGUID</legacyItalic>&gt;\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}]
[HKEY_CLASSES_ROOT\CLSID\&lt;<legacyItalic xmlns="">MyActiveXGUID</legacyItalic>&gt;\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}]</code>
        <para>
          <caps:sentence sentenceid="a4c9fbc6d2aca5540888e646665d50fe" id="tgt13" class="tgtSentence">Save the file and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4edc3812fd5cfc15d84259e29a7f73b2" id="tgt14" class="tgtSentence">Business objects created in Microsoft Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</caps:sentence>
          <caps:sentence sentenceid="23136cb40fc23bf5893549b9befdedb4" id="tgt15" class="tgtSentence"> When the wizard asks you to specify safety settings, select <legacyBold>Safe for initialization </legacyBold>and <legacyBold>Safe for scripting</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="14a0c70c719a4a5d3de6d4cc7883289c" id="tgt16" class="tgtSentence">On the last step, the Application Setup Wizard creates an .htm and a .cab file.</caps:sentence>
          <caps:sentence sentenceid="074e59dc5a49f0c417d1458c2dabf6f1" id="tgt17" class="tgtSentence"> You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b58fec7c0e78843ab5a4b8cbe14ce0f5" id="tgt18" class="tgtSentence">Because the business object will be installed in the Windows\System32\Occache directory by default, move it to the Windows\System32 directory and change the <legacyBold>HKEY_CLASSES_ROOT\CLSID\</legacyBold>&lt;<legacyItalic>MyActiveXGUID</legacyItalic>&gt;\<legacyBold>InprocServer32 </legacyBold>registry key to match the correct path.</caps:sentence>
        </para>
      </introduction>
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
          <caps:sentence id="src5" class="srcSentence">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object's <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method as "safe for scripting."</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src7" class="srcSentence">Business objects marked as "safe for scripting" or safe for initialization can be instantiated and initialized by anyone over the network.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Marking a business object "safe for scripting" does not make it safe.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> It is vitally important to make sure business objects are coded with the highest security to ensure that such objects do not present an unprotected access point for sensitive data.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src10" class="srcSentence">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> In this example, &lt;<legacyItalic>MyActiveXGUID</legacyItalic>&gt; is the hexadecimal GUID number of your business object.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> The following two numbers enable the safe-for-scripting feature:</caps:sentence>
        </para>
        <code>[HKEY_CLASSES_ROOT\CLSID\&lt;<legacyItalic xmlns="">MyActiveXGUID</legacyItalic>&gt;\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}]
[HKEY_CLASSES_ROOT\CLSID\&lt;<legacyItalic xmlns="">MyActiveXGUID</legacyItalic>&gt;\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}]</code>
        <para>
          <caps:sentence id="src13" class="srcSentence">Save the file and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">Business objects created in Microsoft Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> When the wizard asks you to specify safety settings, select <legacyBold>Safe for initialization </legacyBold>and <legacyBold>Safe for scripting</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src16" class="srcSentence">On the last step, the Application Setup Wizard creates an .htm and a .cab file.</caps:sentence>
          <caps:sentence id="src17" class="srcSentence"> You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src18" class="srcSentence">Because the business object will be installed in the Windows\System32\Occache directory by default, move it to the Windows\System32 directory and change the <legacyBold>HKEY_CLASSES_ROOT\CLSID\</legacyBold>&lt;<legacyItalic>MyActiveXGUID</legacyItalic>&gt;\<legacyBold>InprocServer32 </legacyBold>registry key to match the correct path.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
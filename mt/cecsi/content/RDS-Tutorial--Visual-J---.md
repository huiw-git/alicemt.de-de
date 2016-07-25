---
title: "RDS Tutorial (Visual J++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d0d735e0-669a-41e7-ada2-8dd80924e349
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
# RDS Tutorial (Visual J++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="bc9b096d2c4d7c44bb35e27e936c9e97" id="tgt1" class="tgtSentence">ADO/WFC does not completely follow the RDS object model in that it does not implement the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="b8f79f03196069d0566bb0742b9a7065" id="tgt2" class="tgtSentence"> ADO/WFC implements only the client-side class, <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="d524c5b6246844f7b1375ef23e7be47f" id="tgt7" class="tgtSentence">The <legacyBold>DataSpace</legacyBold> class implements one method, <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink>, which returns an <legacyLink xlink:href="f68f58bc-ad28-46cc-9fb3-099e1a678397">ObjectProxy</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="e4998ca68bc832b0af83dd6f74357e06" id="tgt8" class="tgtSentence"> The <legacyBold>DataSpace</legacyBold> class also implements the <legacyLink xlink:href="4d1c8892-4bbc-4e71-bf4b-ba52c0ea9549">InternetTimeout</legacyLink> property.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7f8b5fd9b73b43729a5ce0f0dfb796de" id="tgt9" class="tgtSentence">The <legacyBold>ObjectProxy</legacyBold> class implements one method, call, which can invoke any server-side business object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="bfd88beecc815fa3304af3c4425aea0f" id="tgt10" class="tgtSentence">         <legacyBold>This is the beginning of the tutorial.</legacyBold>       </caps:sentence>
        </para>
        <code>import com.ms.wfc.data.*;
public class RDSTutorial 
{
   public void tutorial()
   {
// Step 1: Specify a server program.
      ObjectProxy obj = 
         DataSpace.createObject(
            "RDSServer.DataFactory", 
            "http://YourServer");

// Step 2: Server returns a Recordset. 
      Recordset rs = (Recordset) obj.call(
            "Query", 
            new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"});

// Step 3: Changes are sent to the server. 
      ...                        // Edit Recordset.
      obj.call(
            "SubmitChanges", 
            new Object[] {"DSN=Pubs;", rs});   
      return;
   }
}</code>
        <para>
          <caps:sentence sentenceid="933e817b96a7a9248336f20d9e222414" id="tgt11" class="tgtSentence">         <legacyBold>This is the end of the tutorial.</legacyBold>       </caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO/WFC does not completely follow the RDS object model in that it does not implement the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> ADO/WFC implements only the client-side class, <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src7" class="srcSentence">The <legacyBold>DataSpace</legacyBold> class implements one method, <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink>, which returns an <legacyLink xlink:href="f68f58bc-ad28-46cc-9fb3-099e1a678397">ObjectProxy</legacyLink> object.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The <legacyBold>DataSpace</legacyBold> class also implements the <legacyLink xlink:href="4d1c8892-4bbc-4e71-bf4b-ba52c0ea9549">InternetTimeout</legacyLink> property.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">The <legacyBold>ObjectProxy</legacyBold> class implements one method, call, which can invoke any server-side business object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">         <legacyBold>This is the beginning of the tutorial.</legacyBold>       </caps:sentence>
        </para>
        <code>import com.ms.wfc.data.*;
public class RDSTutorial 
{
   public void tutorial()
   {
// Step 1: Specify a server program.
      ObjectProxy obj = 
         DataSpace.createObject(
            "RDSServer.DataFactory", 
            "http://YourServer");

// Step 2: Server returns a Recordset. 
      Recordset rs = (Recordset) obj.call(
            "Query", 
            new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"});

// Step 3: Changes are sent to the server. 
      ...                        // Edit Recordset.
      obj.call(
            "SubmitChanges", 
            new Object[] {"DSN=Pubs;", rs});   
      return;
   }
}</code>
        <para>
          <caps:sentence id="src11" class="srcSentence">         <legacyBold>This is the end of the tutorial.</legacyBold>       </caps:sentence>
        </para>
      </introduction>
      <relatedTopics>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
        <link xlink:href="e2a48c4d-88b1-43ff-a202-9cdec54997d2">RDS Tutorial (VBScript)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
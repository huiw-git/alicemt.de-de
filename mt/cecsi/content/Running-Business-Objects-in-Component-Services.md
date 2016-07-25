---
title: "Running Business Objects in Component Services"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3077d0b6-42d6-4f10-8e5d-42e6204f1109
caps.latest.revision: 15
caps.handback.revision: 15
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
# Running Business Objects in Component Services
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
          <caps:sentence sentenceid="8b615e1113fbd7cf25161046d71c3655" id="tgt5" class="tgtSentence">Business objects can be executable files (.exe) or dynamic-link libraries (.dll).</caps:sentence>
          <caps:sentence sentenceid="e5ad86d95320dffc0eba0a4ee1ce3198" id="tgt6" class="tgtSentence"> The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="cf77a0ca39eb3075896a0b6c985024f9" id="tgt7" class="tgtSentence">Business objects created as .exe files can be called through DCOM.</caps:sentence>
              <caps:sentence sentenceid="e76c49aefa3c8d6c8498ca3efe06ce4e" id="tgt8" class="tgtSentence"> If these business objects are used through Internet Information Services (IIS), they are subject to additional marshaling of data, which will slow client performance.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9a9af75389fcf9fa20e23def6882ce6c" id="tgt9" class="tgtSentence">Business objects created as .dll files can be used through IIS, and therefore also by HTTP.</caps:sentence>
              <caps:sentence sentenceid="b113ae23b69641db2de700018b588277" id="tgt10" class="tgtSentence"> They can also be used over DCOM only through Component Services, or through Microsoft Transaction Server, if you are using Windows NT.</caps:sentence>
              <caps:sentence sentenceid="0dff957ba3155df7e0a4e0cf9fbcf290" id="tgt11" class="tgtSentence"> Business object DLLs will need to be registered on the IIS server computer to access them through  IIS.</caps:sentence>
              <caps:sentence sentenceid="64cfe6737aaeccacae3356cf18d06adc" id="tgt12" class="tgtSentence"> For information about how to configure a DLL to run on DCOM, see the section, <legacyLink xlink:href="5f1c2205-191c-4fb4-9bd9-84c878ea46ed">Enabling a DLL to Run on DCOM</legacyLink>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="dc5a136bb14548ea4349aea889e65a51" id="tgt13" class="tgtSentence">When business objects on the middle tier are implemented as Component Services components by using <legacyBold>GetObjectContext</legacyBold>, <legacyBold>SetComplete</legacyBold>, and <legacyBold>SetAbort</legacyBold>, the business objects can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</caps:sentence>
            <caps:sentence sentenceid="eee301e11cedf992dd61b4c0bb73d93f" id="tgt14" class="tgtSentence"> This scenario is possible with DCOM, which is typically implemented between trusted clients and servers in an intranet.</caps:sentence>
            <caps:sentence sentenceid="9eadaa0fdc09a44befbb889d7956d1f2" id="tgt15" class="tgtSentence"> In this case, the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object and <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method on the client side are replaced by the transaction context object and <legacyBold>CreateInstance</legacyBold> method, which are provided by the <legacyBold>ITransactionContext </legacyBold>interface and implemented by Component Services.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
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
          <caps:sentence id="src5" class="srcSentence">Business objects can be executable files (.exe) or dynamic-link libraries (.dll).</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Business objects created as .exe files can be called through DCOM.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> If these business objects are used through Internet Information Services (IIS), they are subject to additional marshaling of data, which will slow client performance.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Business objects created as .dll files can be used through IIS, and therefore also by HTTP.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> They can also be used over DCOM only through Component Services, or through Microsoft Transaction Server, if you are using Windows NT.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> Business object DLLs will need to be registered on the IIS server computer to access them through  IIS.</caps:sentence>
              <caps:sentence id="src12" class="srcSentence"> For information about how to configure a DLL to run on DCOM, see the section, <legacyLink xlink:href="5f1c2205-191c-4fb4-9bd9-84c878ea46ed">Enabling a DLL to Run on DCOM</legacyLink>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src13" class="srcSentence">When business objects on the middle tier are implemented as Component Services components by using <legacyBold>GetObjectContext</legacyBold>, <legacyBold>SetComplete</legacyBold>, and <legacyBold>SetAbort</legacyBold>, the business objects can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> This scenario is possible with DCOM, which is typically implemented between trusted clients and servers in an intranet.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> In this case, the <legacyLink xlink:href="9194bffa-5bdf-4dff-af86-f7158c23bfa7">RDS.DataSpace</legacyLink> object and <legacyLink xlink:href="dec96be6-0b31-4953-9c9a-e962b5afcd18">CreateObject</legacyLink> method on the client side are replaced by the transaction context object and <legacyBold>CreateInstance</legacyBold> method, which are provided by the <legacyBold>ITransactionContext </legacyBold>interface and implemented by Component Services.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <relatedTopics>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
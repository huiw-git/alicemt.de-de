---
title: "The OLE DB Provider for Internet Publishing"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4869aafa-7401-4ce1-93ce-45406a60274f
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
# The OLE DB Provider for Internet Publishing
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="595f0f33ae2d2b309135cd1df1482f37" id="tgt1" class="tgtSentence">The ADO <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> and <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as Web folders or files served by Microsoft FrontPage.</caps:sentence>
          <caps:sentence sentenceid="05115217a43d7cd7b46d4d03a9ed946f" id="tgt2" class="tgtSentence"> With ADO, you can specify the source of a <legacyBold>Record</legacyBold>, <legacyBold>Stream</legacyBold>, or <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to be a URL.</caps:sentence>
          <caps:sentence sentenceid="ab4f0d6fa5d441b7e3d62bcc6578301c" id="tgt3" class="tgtSentence"> You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f2df170cb94ac945c26a3999f35f7d6c" id="tgt4" class="tgtSentence">For example code that uses <legacyBold>Records</legacyBold> and <legacyBold>Streams</legacyBold> with the Internet Publishing Provider, see the <legacyLink xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8f579669bd9baf18bb12bbfcc0a133b4" id="tgt5" class="tgtSentence">The Internet Publishing Provider is installed with Microsoft Windows 2000.</caps:sentence>
          <caps:sentence sentenceid="cc205f19622f04923ffd9a560113353c" id="tgt6" class="tgtSentence"> Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="77678b0a4cecaba7fc3ec32dfc8ceae9" id="tgt7" class="tgtSentence">There are three ways to connect ADO to the Internet Publishing Provider:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="2f4c307029a044aff994922b283e85eb" id="tgt8" class="tgtSentence">Specify "URL=" in the connection string.</caps:sentence>
              <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt9" class="tgtSentence"> For example:</caps:sentence>
            </para>
            <code>objConn.Open "URL=http://servername"</code>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="758cee36d3835e41233785f281b4de07" id="tgt10" class="tgtSentence">Specify Msdaipp.dso for the <legacyItalic>Provider</legacyItalic> keyword of the connection string.</caps:sentence>
              <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt11" class="tgtSentence"> For example:</caps:sentence>
            </para>
            <code>objConn.Open "provider=MSDAIPP.DSO;data source=http://servername"</code>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="294b2ac0eb8cc0809e1b98ecf034f05f" id="tgt12" class="tgtSentence">Specify Msdaipp.dso for the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
              <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt13" class="tgtSentence"> For example:</caps:sentence>
            </para>
            <code>objConn.Provider = "MSDAIPP.DSO"
objConn.Open "http://servername"</code>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="0fb5ef3129b437fc743c2c4c00c05202" id="tgt14" class="tgtSentence">If Msdaipp.dso is explicitly specified as the value of the provider, either with the <legacyItalic>Provider</legacyItalic> connection string keyword or the <legacyBold>Provider</legacyBold> property, you cannot use "URL=" in the connection string.</caps:sentence>
            <caps:sentence sentenceid="c50fa1c91debfd09ddcb728fab31350a" id="tgt15" class="tgtSentence"> If you do, an error will occur.</caps:sentence>
            <caps:sentence sentenceid="eb4c99b4569ca00aaf4b7ee465ac3eb4" id="tgt16" class="tgtSentence"> Instead, simply specify the URL as shown earlier.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="bde31aa67dba30300ab4deb51805fd69" id="tgt17" class="tgtSentence">For more specific information about the Internet Publishing Provider, see <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>, or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The ADO <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> and <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as Web folders or files served by Microsoft FrontPage.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> With ADO, you can specify the source of a <legacyBold>Record</legacyBold>, <legacyBold>Stream</legacyBold>, or <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to be a URL.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">For example code that uses <legacyBold>Records</legacyBold> and <legacyBold>Streams</legacyBold> with the Internet Publishing Provider, see the <legacyLink xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The Internet Publishing Provider is installed with Microsoft Windows 2000.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">There are three ways to connect ADO to the Internet Publishing Provider:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Specify "URL=" in the connection string.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> For example:</caps:sentence>
            </para>
            <code>objConn.Open "URL=http://servername"</code>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Specify Msdaipp.dso for the <legacyItalic>Provider</legacyItalic> keyword of the connection string.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence"> For example:</caps:sentence>
            </para>
            <code>objConn.Open "provider=MSDAIPP.DSO;data source=http://servername"</code>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Specify Msdaipp.dso for the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> For example:</caps:sentence>
            </para>
            <code>objConn.Provider = "MSDAIPP.DSO"
objConn.Open "http://servername"</code>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src14" class="srcSentence">If Msdaipp.dso is explicitly specified as the value of the provider, either with the <legacyItalic>Provider</legacyItalic> connection string keyword or the <legacyBold>Provider</legacyBold> property, you cannot use "URL=" in the connection string.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> If you do, an error will occur.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Instead, simply specify the URL as shown earlier.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src17" class="srcSentence">For more specific information about the Internet Publishing Provider, see <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>, or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
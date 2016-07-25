---
title: "Microsoft ActiveX Data Objects (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2fa6237b-44b8-4b6c-9952-5acd80a54e20
caps.latest.revision: 18
caps.handback.revision: 18
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
# Microsoft ActiveX Data Objects (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d4986d35cc2d2c9b145a39466b4b2192" id="tgt1" class="tgtSentence">ActiveX Data Objects (ADO) consists of the following components:</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="421359a899e6aeb972c11a26fb52ad15" id="tgt2" class="tgtSentence">ADO</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="390e819bd3cd616f86f62ac61beca0c0" id="tgt3" class="tgtSentence">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a variety of sources through an OLE DB provider.</caps:sentence>
            <caps:sentence sentenceid="93a8c0c590e763860dbac2825774b486" id="tgt4" class="tgtSentence"> Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint.</caps:sentence>
            <caps:sentence sentenceid="45c9c8786719f49cbd2aee5dcbf939d3" id="tgt5" class="tgtSentence"> ADO supports key features for building client/server and Web-based applications.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="347a683cedfa4b901d918ff90ad32f5b" id="tgt6" class="tgtSentence">ADO MD</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e02da6b71873d83b56e37eebfb4fd12d" id="tgt7" class="tgtSentence">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</caps:sentence>
            <caps:sentence sentenceid="f9d264f88a475dd46a2bd6635cb11a33" id="tgt8" class="tgtSentence"> ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects.</caps:sentence>
            <caps:sentence sentenceid="116f1b45d36eda66d7c4d0b8fff295a4" id="tgt9" class="tgtSentence"> With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cd160290e1d32ffaa8b313de55f9d429" id="tgt10" class="tgtSentence">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</caps:sentence>
            <caps:sentence sentenceid="3d97df013f6032d94e0405de28f29948" id="tgt11" class="tgtSentence"> To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</caps:sentence>
            <caps:sentence sentenceid="5bbe22578975ee4235f0bac11462feb9" id="tgt12" class="tgtSentence"> MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</caps:sentence>
            <caps:sentence sentenceid="6c55bb13a5386f556ece6b1a7f867b6e" id="tgt13" class="tgtSentence"> Refer to the documentation for your OLAP OLE DB provider for more detailed information about the specific syntax and behaviors supported by your provider.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1d374ed2a6bcf601d7bfd4fc3dfd3b5d" id="tgt14" class="tgtSentence">RDS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6cd8ae097806e00ce911977af8ffb665" id="tgt15" class="tgtSentence">Remote Data Service (RDS) is a feature of ADO, with which you can move data from a server to a client application or Web page, manipulate the data on the client, and return updates to the server in a single round trip.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt16" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
              <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt17" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
              <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt18" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
              <caps:sentence sentenceid="20827e3adfa88537ab8adfa70f7ffa15" id="tgt19" class="tgtSentence"> Applications that use RDS should migrate to  <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a7e6aa49b4687d53060358087b3cd761" id="tgt20" class="tgtSentence">ADOX</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6e1d6b4543209f8b3fae3a096de1de1f" id="tgt21" class="tgtSentence">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</caps:sentence>
            <caps:sentence sentenceid="fb8b5ff2afe9f40e1a9c3bf4f68dc52e" id="tgt22" class="tgtSentence"> ADOX includes objects for schema creation and modification, as well as security.</caps:sentence>
            <caps:sentence sentenceid="bf0f8b8c0d669a79fded3b9a7cd52793" id="tgt23" class="tgtSentence"> Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1b2d4a4a53332b3c7868ff2b3e8e5c09" id="tgt24" class="tgtSentence">ADOX is a companion library to the core ADO objects.</caps:sentence>
            <caps:sentence sentenceid="c7150e95af7e5973d1e41aa27115331b" id="tgt25" class="tgtSentence"> It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</caps:sentence>
            <caps:sentence sentenceid="51f7d916a04de7548d5d0e92367b2f45" id="tgt26" class="tgtSentence"> It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="55876228853abf632dec9346a4f372ec" id="tgt27" class="tgtSentence">Documentation</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="86b83a38-efdf-4831-a6d5-7e470d517d1c">ADO 2.8 Security Design Issues and Changes</link>
          </para>
          <para>
            <link xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">Programmer's Guide</link>
          </para>
          <para>
            <caps:sentence sentenceid="fc45f58d69af9212ee6614fa58ccb7ed" id="tgt28" class="tgtSentence">An introduction to using ADO, RDS, ADO MD, and ADOX.</caps:sentence>
          </para>
          <para>
            <link xlink:href="6dc27c85-84e1-472a-b057-d1854b8c98a3">Programmer's Reference</link>
          </para>
          <para>
            <caps:sentence sentenceid="0f1ffdc55e879a60cc9cd3c1d130be28" id="tgt29" class="tgtSentence">This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</caps:sentence>
          </para>
          <para>
            <link xlink:href="b0478836-4123-4357-969a-c5784fc28be5">ADO Glossary</link>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="434990c8a25d2be94863561ae98bd682" id="tgt30" class="tgtSentence">Support</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="aa63d40fc53dc6e2e0da171b69eff6c0" id="tgt31" class="tgtSentence">For free help with ADO issues, try posting to the ADO public newsgroup.</caps:sentence>
            <caps:sentence sentenceid="b35b1b55ecc3270907c3c5e94c71f889" id="tgt32" class="tgtSentence"> This newsgroup is monitored by Microsoft Product Support Services (PSS) support professionals who cover ADO, and by other experienced ADO developers.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="57a8bcd8f5587a7e3e85db1f5c10c97a" id="tgt33" class="tgtSentence">Further information about support options can be found on the Microsoft Help and Support Web site.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ActiveX Data Objects (ADO) consists of the following components:</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">ADO</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a variety of sources through an OLE DB provider.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> ADO supports key features for building client/server and Web-based applications.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">ADO MD</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Refer to the documentation for your OLAP OLE DB provider for more detailed information about the specific syntax and behaviors supported by your provider.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">RDS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">Remote Data Service (RDS) is a feature of ADO, with which you can move data from a server to a client application or Web page, manipulate the data on the client, and return updates to the server in a single round trip.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src16" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
              <caps:sentence id="src18" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
              <caps:sentence id="src19" class="srcSentence"> Applications that use RDS should migrate to  <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">ADOX</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> ADOX includes objects for schema creation and modification, as well as security.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">ADOX is a companion library to the core ADO objects.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">Documentation</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="86b83a38-efdf-4831-a6d5-7e470d517d1c">ADO 2.8 Security Design Issues and Changes</link>
          </para>
          <para>
            <link xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">Programmer's Guide</link>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">An introduction to using ADO, RDS, ADO MD, and ADOX.</caps:sentence>
          </para>
          <para>
            <link xlink:href="6dc27c85-84e1-472a-b057-d1854b8c98a3">Programmer's Reference</link>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</caps:sentence>
          </para>
          <para>
            <link xlink:href="b0478836-4123-4357-969a-c5784fc28be5">ADO Glossary</link>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src30" class="srcSentence">Support</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src31" class="srcSentence">For free help with ADO issues, try posting to the ADO public newsgroup.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> This newsgroup is monitored by Microsoft Product Support Services (PSS) support professionals who cover ADO, and by other experienced ADO developers.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src33" class="srcSentence">Further information about support options can be found on the Microsoft Help and Support Web site.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
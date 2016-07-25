---
title: "ADOX Fundamentals"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 954476fc-5f72-4ada-ace5-d9acb27d18f8
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
# ADOX Fundamentals
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="cdc78106aa11167024b8c7970e4903bc" id="tgt1" class="tgtSentence">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</caps:sentence>
          <caps:sentence sentenceid="fb8b5ff2afe9f40e1a9c3bf4f68dc52e" id="tgt2" class="tgtSentence"> ADOX includes objects for schema creation and modification, as well as security.</caps:sentence>
          <caps:sentence sentenceid="bf0f8b8c0d669a79fded3b9a7cd52793" id="tgt3" class="tgtSentence"> Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1b2d4a4a53332b3c7868ff2b3e8e5c09" id="tgt4" class="tgtSentence">ADOX is a companion library to the core ADO objects.</caps:sentence>
          <caps:sentence sentenceid="c7150e95af7e5973d1e41aa27115331b" id="tgt5" class="tgtSentence"> It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</caps:sentence>
          <caps:sentence sentenceid="51f7d916a04de7548d5d0e92367b2f45" id="tgt6" class="tgtSentence"> It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8d819dc5d83aa2ab0b3750faf9ea5522" id="tgt7" class="tgtSentence">To use ADOX with your development tool, you should establish a reference to the ADOX type library.</caps:sentence>
          <caps:sentence sentenceid="1680b8086d680dd124eda6e7922e1f09" id="tgt8" class="tgtSentence"> The description of the ADOX library is "Microsoft ADO Ext.</caps:sentence>
          <caps:sentence sentenceid="438f87701e06f59350d68bbba7f999fe" id="tgt9" class="tgtSentence"> for DDL and Security."</caps:sentence>
          <caps:sentence sentenceid="fca4b5184e343429d68da5951927c9fd" id="tgt10" class="tgtSentence"> The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX".</caps:sentence>
          <caps:sentence sentenceid="9079b29a32f4aee706e97da5ee401373" id="tgt11" class="tgtSentence"> For more information about establishing references to libraries, see the documentation of your development tool.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5ae6ae18a8c0026914b34d2484217785" id="tgt12" class="tgtSentence">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX.</caps:sentence>
          <caps:sentence sentenceid="314b7ddf374bf859abea7c5206fab4f2" id="tgt13" class="tgtSentence"> Certain features of ADOX may not be supported, depending on your data provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="448fe58f5aec2994c8b1b9b7fc5273d8" id="tgt14" class="tgtSentence">This document assumes a working knowledge of the Microsoft® Visual Basic® programming language and a general knowledge of ADO.</caps:sentence>
          <caps:sentence sentenceid="04b39d2564515e57337e243f0198c6b5" id="tgt15" class="tgtSentence"> For more information about ADO, see the <legacyLink xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">ADO Programmer's Guide</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="558321f5195493ed6e7c2cdee015490e" id="tgt16" class="tgtSentence"> For more overview information about ADOX, see the following topics:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="31c0781c-96c8-4460-90ea-134066154fc7">
                <caps:sentence sentenceid="be510399d40dff9f33ebe3ec2d27772e" id="tgt17" class="tgtSentence">ADOX Object Model</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="3f5287e9-f62c-40c4-bb59-985102be956e">
                <caps:sentence sentenceid="c55585ac275818d237128ee04ce79407" id="tgt18" class="tgtSentence">ADOX Objects</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="c0c90ba9-0471-4381-96f1-376de22fa2ee">
                <caps:sentence sentenceid="8ebab0ff0852318736740f557a5eeb17" id="tgt19" class="tgtSentence">ADOX Collections</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="2ddf19e4-312e-4d21-8053-a6fc4b738ad4">
                <caps:sentence sentenceid="cc663e29b23903008cc97ae3ad0edd29" id="tgt20" class="tgtSentence">ADOX Properties</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="8de11ef7-034c-4613-91df-2244171f0b9a">
                <caps:sentence sentenceid="797d4315a15dee6c35855ee234cadf06" id="tgt21" class="tgtSentence">ADOX Methods</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="438e4369-f7e8-4dca-a709-dd501a3ca83f">
                <caps:sentence sentenceid="7aae09b4f359c16eeaab1da8773a2d6a" id="tgt22" class="tgtSentence">ADOX Examples</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef700465-2e97-46e8-8213-2d662501e540">ADOX API Reference</link>
        <link xlink:href="438e4369-f7e8-4dca-a709-dd501a3ca83f">ADOX Code Examples</link>
        <link xlink:href="c0c90ba9-0471-4381-96f1-376de22fa2ee">ADOX Collections</link>
        <link xlink:href="9d91f511-d46f-44ef-97ef-77bf93836186">ADOX Enumerated Constants</link>
        <link xlink:href="8de11ef7-034c-4613-91df-2244171f0b9a">ADOX Methods</link>
        <link xlink:href="31c0781c-96c8-4460-90ea-134066154fc7">ADOX Object Model</link>
        <link xlink:href="3f5287e9-f62c-40c4-bb59-985102be956e">ADOX Objects</link>
        <link xlink:href="2ddf19e4-312e-4d21-8053-a6fc4b738ad4">ADOX Properties</link>
        <link xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">Microsoft ADO MD Programmer's Reference</link>
        <link xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">ADO Programmer's Guide</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> ADOX includes objects for schema creation and modification, as well as security.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">ADOX is a companion library to the core ADO objects.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">To use ADOX with your development tool, you should establish a reference to the ADOX type library.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The description of the ADOX library is "Microsoft ADO Ext.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> for DDL and Security."</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX".</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> For more information about establishing references to libraries, see the documentation of your development tool.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> Certain features of ADOX may not be supported, depending on your data provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src14" class="srcSentence">This document assumes a working knowledge of the Microsoft® Visual Basic® programming language and a general knowledge of ADO.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> For more information about ADO, see the <legacyLink xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">ADO Programmer's Guide</legacyLink>.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> For more overview information about ADOX, see the following topics:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="31c0781c-96c8-4460-90ea-134066154fc7">
                <caps:sentence id="src17" class="srcSentence">ADOX Object Model</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="3f5287e9-f62c-40c4-bb59-985102be956e">
                <caps:sentence id="src18" class="srcSentence">ADOX Objects</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="c0c90ba9-0471-4381-96f1-376de22fa2ee">
                <caps:sentence id="src19" class="srcSentence">ADOX Collections</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="2ddf19e4-312e-4d21-8053-a6fc4b738ad4">
                <caps:sentence id="src20" class="srcSentence">ADOX Properties</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="8de11ef7-034c-4613-91df-2244171f0b9a">
                <caps:sentence id="src21" class="srcSentence">ADOX Methods</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="438e4369-f7e8-4dca-a709-dd501a3ca83f">
                <caps:sentence id="src22" class="srcSentence">ADOX Examples</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef700465-2e97-46e8-8213-2d662501e540">ADOX API Reference</link>
        <link xlink:href="438e4369-f7e8-4dca-a709-dd501a3ca83f">ADOX Code Examples</link>
        <link xlink:href="c0c90ba9-0471-4381-96f1-376de22fa2ee">ADOX Collections</link>
        <link xlink:href="9d91f511-d46f-44ef-97ef-77bf93836186">ADOX Enumerated Constants</link>
        <link xlink:href="8de11ef7-034c-4613-91df-2244171f0b9a">ADOX Methods</link>
        <link xlink:href="31c0781c-96c8-4460-90ea-134066154fc7">ADOX Object Model</link>
        <link xlink:href="3f5287e9-f62c-40c4-bb59-985102be956e">ADOX Objects</link>
        <link xlink:href="2ddf19e4-312e-4d21-8053-a6fc4b738ad4">ADOX Properties</link>
        <link xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">Microsoft ADO MD Programmer's Reference</link>
        <link xlink:href="e3c50eee-964a-4abd-810d-1bd51978e814">ADO Programmer's Guide</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
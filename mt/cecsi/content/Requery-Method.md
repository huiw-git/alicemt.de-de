---
title: "Requery Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1
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
# Requery Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7e791dd0e5309ce5cf4ae65d9e580daf" id="tgt1" class="tgtSentence">Updates the data in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object by re-executing the query on which the object is based.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>.<legacyBold>Requery </legacyBold><parameterReference>Options</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt2" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="9adedc557e8e216fcb31a9234d327e38" id="tgt4" class="tgtSentence"> A bitmask that contains <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> and <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> values affecting this operation.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="033a5ef5a6404119a950a91c158920e6" id="tgt5" class="tgtSentence">If <legacyItalic>Options</legacyItalic> is set to <legacyBold>adAsyncExecute</legacyBold>, this operation will execute asynchronously and a <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">RecordsetChangeComplete</legacyLink> event will be issued when it concludes.</caps:sentence>
              <caps:sentence sentenceid="fa9d5785f63a1f7707459b3ba677fe74" id="tgt6" class="tgtSentence"> The <legacyBold>ExecuteOpenEnum</legacyBold> values of <legacyBold>adExecuteNoRecords</legacyBold> or <legacyBold>adExecuteStream</legacyBold> should not be used with <legacyBold>Requery</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="811e9a2f4d3b4cd7d6db4244aa7050c1" id="tgt7" class="tgtSentence">Use the <legacyBold>Requery</legacyBold> method to refresh the entire contents of a <legacyBold>Recordset</legacyBold> object from the data source by reissuing the original command and retrieving the data a second time.</caps:sentence>
            <caps:sentence sentenceid="b843e81d176589f5b5afd872e376ee43" id="tgt8" class="tgtSentence"> Calling this method is equivalent to calling the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> and <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> methods in succession.</caps:sentence>
            <caps:sentence sentenceid="6bb3951027847596deb28e982ca15b05" id="tgt9" class="tgtSentence"> If you are editing the current record or adding a new record, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="36ceb46aa3b80a9632e26240a314abb8" id="tgt10" class="tgtSentence">While the <legacyBold>Recordset</legacyBold> object is open, the properties that define the nature of the cursor (<legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink>, <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType</legacyLink>, <legacyLink xlink:href="20c76571-8c9a-482c-a99e-726ab1d93f8b">MaxRecords</legacyLink>, and so forth) are read-only.</caps:sentence>
            <caps:sentence sentenceid="25fbc11303a32b5c4a94a5bf289681d3" id="tgt11" class="tgtSentence"> Thus, the <legacyBold>Requery</legacyBold> method can only refresh the current cursor.</caps:sentence>
            <caps:sentence sentenceid="5b6ad6b695213b8dc68bc78175c69379" id="tgt12" class="tgtSentence"> To change any of the cursor properties and view the results, you must use the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method so that the properties become read/write again.</caps:sentence>
            <caps:sentence sentenceid="2e6b852501ef1a47cb65b1da8aab0781" id="tgt13" class="tgtSentence"> You can then change the property settings and call the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method to reopen the cursor.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ed5e1b60-3769-4b26-a253-1d721e37941d">Visual Basic Example</link>
        <link xlink:href="3a7bbf07-2fca-4892-95f4-eec93f2d5e91">VBScript Example</link>
        <link xlink:href="ada6acc1-82eb-4cfa-8f2f-617a916ffd8d">Visual C++ Example</link>
        <link xlink:href="3c92cb19-c13b-4bb3-b4cd-75dc8f42057c">Visual J++ Example</link>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Updates the data in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object by re-executing the query on which the object is based.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>.<legacyBold>Requery </legacyBold><parameterReference>Options</parameterReference></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A bitmask that contains <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink> and <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> values affecting this operation.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence id="src5" class="srcSentence">If <legacyItalic>Options</legacyItalic> is set to <legacyBold>adAsyncExecute</legacyBold>, this operation will execute asynchronously and a <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">RecordsetChangeComplete</legacyLink> event will be issued when it concludes.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> The <legacyBold>ExecuteOpenEnum</legacyBold> values of <legacyBold>adExecuteNoRecords</legacyBold> or <legacyBold>adExecuteStream</legacyBold> should not be used with <legacyBold>Requery</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">Use the <legacyBold>Requery</legacyBold> method to refresh the entire contents of a <legacyBold>Recordset</legacyBold> object from the data source by reissuing the original command and retrieving the data a second time.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Calling this method is equivalent to calling the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> and <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> methods in succession.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If you are editing the current record or adding a new record, an error occurs.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">While the <legacyBold>Recordset</legacyBold> object is open, the properties that define the nature of the cursor (<legacyLink xlink:href="b62c66ca-58d5-430e-9257-eb38c65e48c2">CursorType</legacyLink>, <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType</legacyLink>, <legacyLink xlink:href="20c76571-8c9a-482c-a99e-726ab1d93f8b">MaxRecords</legacyLink>, and so forth) are read-only.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Thus, the <legacyBold>Requery</legacyBold> method can only refresh the current cursor.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> To change any of the cursor properties and view the results, you must use the <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">Close</legacyLink> method so that the properties become read/write again.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> You can then change the property settings and call the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method to reopen the cursor.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ed5e1b60-3769-4b26-a253-1d721e37941d">Visual Basic Example</link>
        <link xlink:href="3a7bbf07-2fca-4892-95f4-eec93f2d5e91">VBScript Example</link>
        <link xlink:href="ada6acc1-82eb-4cfa-8f2f-617a916ffd8d">Visual C++ Example</link>
        <link xlink:href="3c92cb19-c13b-4bb3-b4cd-75dc8f42057c">Visual J++ Example</link>
        <link xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
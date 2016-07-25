---
title: "Preparing and Executing Commands"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7448d9ee-7f4b-47e3-be54-2df8c9bbac32
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
# Preparing and Executing Commands
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="74de42946e3196a77b3819a6c22d2fde" id="tgt1" class="tgtSentence">Commands are instructions issued to a provider to perform some operations against the underlying data source.</caps:sentence>
          <caps:sentence sentenceid="5fcb12871c4a76c7774f450d676a6fca" id="tgt2" class="tgtSentence"> An SQL statement, for example, is a command to the Microsoft SQL Data Provider.</caps:sentence>
          <caps:sentence sentenceid="0772b041e911109f91895fc71a01ddad" id="tgt3" class="tgtSentence"> In ADO, commands are typically represented by <legacyBold>Command</legacyBold> objects, although simple commands can also be issued through <legacyBold>Connection</legacyBold> or <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1aaa58a4b3fc996e795fb03d6dcc8fa4" id="tgt4" class="tgtSentence">You can use the <legacyBold>Command</legacyBold> object to request any supported type of operation from the provider, assuming that the provider can interpret the command string properly.</caps:sentence>
          <caps:sentence sentenceid="04ada1077f892cbd821d97ccd41fda7c" id="tgt5" class="tgtSentence"> A common operation for data providers is to query a database and return records in a <legacyBold>Recordset</legacyBold> object, which that can be thought of as a container to hold the result and a tool to view the result.</caps:sentence>
          <caps:sentence sentenceid="9d3fa4668518588843a21e7a662f832d" id="tgt6" class="tgtSentence"> As with many ADO objects, some <legacyBold>Command</legacyBold> object collections, methods, or properties might generate errors when referenced, depending on the functionality of the provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b9d8a8b3a2bf03bc021c124311cd93f4" id="tgt7" class="tgtSentence">In addition to using <legacyBold>Command</legacyBold> objects, you can use the <legacyBold>Execute</legacyBold> method on the <legacyBold>Connection</legacyBold> object or the <legacyBold>Open</legacyBold> method on the <legacyBold>Recordset</legacyBold> object to issue a command and have it executed.</caps:sentence>
          <caps:sentence sentenceid="ddc07c8bc479cc40d21f7825f2aa11c0" id="tgt8" class="tgtSentence"> However, you should use a <legacyBold>Command</legacyBold> object if you need to reuse a command in your code, or if you need to pass detailed parameter information with your command.</caps:sentence>
          <caps:sentence sentenceid="5a997e43a2f682ac1e6e0e55688a9661" id="tgt9" class="tgtSentence"> These scenarios are covered in more detail later in this section.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="35de959c6551d2f97ad9cdfd30417bf5" id="tgt10" class="tgtSentence">Certain <legacyBold>Command</legacyBold>s can return a result set as a binary stream or as a single <legacyBold>Record</legacyBold> rather than as a <legacyBold>Recordset</legacyBold>, if this is supported by the provider.</caps:sentence>
            <caps:sentence sentenceid="d4da616283b72a460328f24bc6d9163f" id="tgt11" class="tgtSentence"> Also, some <legacyBold>Command</legacyBold>s are not intended to return any result set at all (for example, a SQL Update query).</caps:sentence>
            <caps:sentence sentenceid="7392483b7c37c684ddf2450770eb8f84" id="tgt12" class="tgtSentence"> This section will cover the most typical scenario, however: executing <legacyBold>Command</legacyBold>s that return results as a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="6468773e06c5e9b42c694436b982a34e" id="tgt13" class="tgtSentence"> For more information about returning results into <legacyBold>Record</legacyBold>s or <legacyBold>Stream</legacyBold>s, see <legacyLink xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">Records and Streams</legacyLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt14" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="36cc51f9e8d394c21b762802d7395b45" id="tgt15" class="tgtSentence">             <legacyLink xlink:href="e84a14b1-3c2a-4f7d-a966-9e08a93948df">Command Object Overview</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3d687821c9b83625e2341df44d4bc397" id="tgt16" class="tgtSentence">             <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Creating and Executing a Simple Command</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="7005088deca8ede8b95584b294f31af4" id="tgt17" class="tgtSentence">             <legacyLink xlink:href="10e7ef4a-78bf-4e91-931e-cbc6c065dd4c">Command Object Parameters</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1a2acaec66094be73095bad48d83427c" id="tgt18" class="tgtSentence">             <legacyLink xlink:href="685f7652-2271-4ede-b552-2eeb8c756b4c">Calling a Stored Procedure with a Command</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ffbefcede51bbe61819eaf3802c5dea0" id="tgt19" class="tgtSentence">             <legacyLink xlink:href="35ffdb79-a931-4271-a3bb-0cd804cf173e">Calling a Stored Procedure as a Method on a Connection Object</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d7ec1858f3ef931c884161a04ada5aed" id="tgt20" class="tgtSentence">             <legacyLink xlink:href="5a0ec8f9-5ba3-4f9f-b80d-2073aa049586">Named Commands</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="cfce8cb7e4d1d4e7ebba1e7fbd02d993" id="tgt21" class="tgtSentence">             <legacyLink xlink:href="36e0cdbe-7f50-40f5-af0d-700f5d8dc75a">Passing Parameters to a Named Command</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Commands are instructions issued to a provider to perform some operations against the underlying data source.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> An SQL statement, for example, is a command to the Microsoft SQL Data Provider.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> In ADO, commands are typically represented by <legacyBold>Command</legacyBold> objects, although simple commands can also be issued through <legacyBold>Connection</legacyBold> or <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">You can use the <legacyBold>Command</legacyBold> object to request any supported type of operation from the provider, assuming that the provider can interpret the command string properly.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> A common operation for data providers is to query a database and return records in a <legacyBold>Recordset</legacyBold> object, which that can be thought of as a container to hold the result and a tool to view the result.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> As with many ADO objects, some <legacyBold>Command</legacyBold> object collections, methods, or properties might generate errors when referenced, depending on the functionality of the provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">In addition to using <legacyBold>Command</legacyBold> objects, you can use the <legacyBold>Execute</legacyBold> method on the <legacyBold>Connection</legacyBold> object or the <legacyBold>Open</legacyBold> method on the <legacyBold>Recordset</legacyBold> object to issue a command and have it executed.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> However, you should use a <legacyBold>Command</legacyBold> object if you need to reuse a command in your code, or if you need to pass detailed parameter information with your command.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> These scenarios are covered in more detail later in this section.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src10" class="srcSentence">Certain <legacyBold>Command</legacyBold>s can return a result set as a binary stream or as a single <legacyBold>Record</legacyBold> rather than as a <legacyBold>Recordset</legacyBold>, if this is supported by the provider.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Also, some <legacyBold>Command</legacyBold>s are not intended to return any result set at all (for example, a SQL Update query).</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> This section will cover the most typical scenario, however: executing <legacyBold>Command</legacyBold>s that return results as a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> For more information about returning results into <legacyBold>Record</legacyBold>s or <legacyBold>Stream</legacyBold>s, see <legacyLink xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">Records and Streams</legacyLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src14" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">             <legacyLink xlink:href="e84a14b1-3c2a-4f7d-a966-9e08a93948df">Command Object Overview</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">             <legacyLink xlink:href="0b81af6f-b9ae-4f7c-b59b-b5bdd775036f">Creating and Executing a Simple Command</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">             <legacyLink xlink:href="10e7ef4a-78bf-4e91-931e-cbc6c065dd4c">Command Object Parameters</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">             <legacyLink xlink:href="685f7652-2271-4ede-b552-2eeb8c756b4c">Calling a Stored Procedure with a Command</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src19" class="srcSentence">             <legacyLink xlink:href="35ffdb79-a931-4271-a3bb-0cd804cf173e">Calling a Stored Procedure as a Method on a Connection Object</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src20" class="srcSentence">             <legacyLink xlink:href="5a0ec8f9-5ba3-4f9f-b80d-2073aa049586">Named Commands</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src21" class="srcSentence">             <legacyLink xlink:href="36e0cdbe-7f50-40f5-af0d-700f5d8dc75a">Passing Parameters to a Named Command</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Refresh Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 089b7ca7-684f-4259-8032-5bd1ecc54426
caps.latest.revision: 11
caps.handback.revision: 11
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
# Refresh Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="227051afa8c902ab4368237f19c7718c" id="tgt1" class="tgtSentence">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>collection</parameterReference>.<legacyBold>Refresh</legacyBold></legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="9d536ff6d0b07da4873837ab155f0174" id="tgt2" class="tgtSentence">The <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method accomplishes different tasks depending on the collection from which you call it.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <content></content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt3" class="tgtSentence">Parameters</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="1a5e9d9be151c8d0df8c0799c5061a27" id="tgt4" class="tgtSentence">Using the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method on the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object retrieves provider-side parameter information for the stored procedure or parameterized query specified in the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object.</caps:sentence>
                    <caps:sentence sentenceid="d961448e2e4ce68b0f41e88bbbfe55b3" id="tgt5" class="tgtSentence"> The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="341b521b346411ac86ff821582b84644" id="tgt6" class="tgtSentence">You should set the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property of the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object to a valid <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property to a valid command, and the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property to <legacyBold>adCmdStoredProc</legacyBold> before calling the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="15ed09cd60dfadc1a162ffd0ab7b0d87" id="tgt7" class="tgtSentence">If you access the <unmanagedCodeEntityReference>Parameters</unmanagedCodeEntityReference> collection before calling the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method, ADO will automatically call the method and populate the collection for you.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="f0ed9b3de09b9481545175a504c38e8c" id="tgt8" class="tgtSentence">If you use the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method to obtain parameter information from the provider and it returns one or more variable-length data type <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution.</caps:sentence>
                      <caps:sentence sentenceid="429c00e375b3e91c9e6502e8ee95115a" id="tgt9" class="tgtSentence"> You should explicitly set the <legacyLink xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size</legacyLink> property for these parameters before calling the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method to prevent errors.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="d05b6ed7d2345020440df396d6da7f73" id="tgt10" class="tgtSentence">Fields</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="6ef9709d16e62b70c68d76ae319e9a8a" id="tgt11" class="tgtSentence">Using the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method on the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection has no visible effect.</caps:sentence>
                    <caps:sentence sentenceid="43451a5089d625631925d65a5d355eef" id="tgt12" class="tgtSentence"> To retrieve changes from the underlying database structure, you must use either the <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> method or, if the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object does not support bookmarks, the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink> method.</caps:sentence>
                  </para>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt13" class="tgtSentence">Properties</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="98a73b042472f58fdb9d94e17960d9e5" id="tgt14" class="tgtSentence">Using the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method on a <unmanagedCodeEntityReference>Properties</unmanagedCodeEntityReference> collection of some objects populates the collection with the dynamic properties that the provider exposes.</caps:sentence>
                    <caps:sentence sentenceid="f7dab2583b3037bdbcf53ab6898778cf" id="tgt15" class="tgtSentence"> These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt16" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">
                      <caps:sentence sentenceid="cbf5e06eb1c706e1519c0f509e6e26b8" id="tgt17" class="tgtSentence">Axes Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">
                      <caps:sentence sentenceid="99fbddbd2624687698880c0d9f5fdf87" id="tgt18" class="tgtSentence">Columns Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">
                      <caps:sentence sentenceid="422f64c140f37984ffcb1c120148909c" id="tgt19" class="tgtSentence">CubeDefs Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="eaf6f4e7-2ea0-49a3-89ee-e219e025257c">
                      <caps:sentence sentenceid="168338dfa85821b835b23cd5878cc6f4" id="tgt20" class="tgtSentence">Dimensions Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">
                      <caps:sentence sentenceid="3c69e3f80ec3f7e1f6d12d9e4a0cea6d" id="tgt21" class="tgtSentence">Errors Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">
                      <caps:sentence sentenceid="674ea0184650cb95a2fb260332db2e00" id="tgt22" class="tgtSentence">Fields Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">
                      <caps:sentence sentenceid="c9eb156f404c779d36bd5c9d49c8dd0e" id="tgt23" class="tgtSentence">Groups Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="bef0fcb1-8060-4faa-84f0-3d52e9c4526f">
                      <caps:sentence sentenceid="412915da09c444068dd6d57b9171835c" id="tgt24" class="tgtSentence">Hierarchies Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">
                      <caps:sentence sentenceid="3ec8f48378a449dc4727a819e79807ee" id="tgt25" class="tgtSentence">Indexes Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">
                      <caps:sentence sentenceid="1ff95ae0349f00cab4e3f99ebf4d5c7b" id="tgt26" class="tgtSentence">Keys Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">
                      <caps:sentence sentenceid="b9680c82c535b26b76eaeeb708ce1342" id="tgt27" class="tgtSentence">Levels Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">
                      <caps:sentence sentenceid="04c396696736b58abf3bf0ac9dd32386" id="tgt28" class="tgtSentence">Members Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">
                      <caps:sentence sentenceid="7de80a224c6430583d8aa944e23154fb" id="tgt29" class="tgtSentence">Parameters Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">
                      <caps:sentence sentenceid="6cd207228ed31ea5de7a469254a17678" id="tgt30" class="tgtSentence">Positions Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">
                      <caps:sentence sentenceid="0ed99f9ee0743c01afa5028a0ead7085" id="tgt31" class="tgtSentence">Procedures Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">
                      <caps:sentence sentenceid="7439ef29259e7f6c884c602c322db7d4" id="tgt32" class="tgtSentence">Properties Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">
                      <caps:sentence sentenceid="4edaeeaf83e6078c1df9f2957d17b416" id="tgt33" class="tgtSentence">Tables Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">
                      <caps:sentence sentenceid="81cc4ec10bc4a5663d52f8158760cccc" id="tgt34" class="tgtSentence">Users Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">
                      <caps:sentence sentenceid="a84f59d49eaef56320c3dbce95952fb2" id="tgt35" class="tgtSentence">Views Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f5375fa1-4711-4f7e-9ba4-54c427f71325">Visual Basic Example</link>
        <link xlink:href="3dc3443b-a1b0-4fbd-908a-6e274dec981c">Visual C++ Example</link>
        <link xlink:href="c0fbf728-0ccb-468d-be1e-c09dad9ffddb">Visual VJ++ Example</link>
        <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>collection</parameterReference>.<legacyBold>Refresh</legacyBold></legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method accomplishes different tasks depending on the collection from which you call it.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <content></content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src3" class="srcSentence">Parameters</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">Using the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method on the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object retrieves provider-side parameter information for the stored procedure or parameterized query specified in the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object.</caps:sentence>
                    <caps:sentence id="src5" class="srcSentence"> The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">You should set the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property of the <unmanagedCodeEntityReference>Command</unmanagedCodeEntityReference> object to a valid <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object, the <legacyLink xlink:href="4dd7e82a-8da5-4a4e-b439-11a29286fa0e">CommandText</legacyLink> property to a valid command, and the <legacyLink xlink:href="ca44809c-8647-48b6-a7fb-0be70a02f53e">CommandType</legacyLink> property to <legacyBold>adCmdStoredProc</legacyBold> before calling the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">If you access the <unmanagedCodeEntityReference>Parameters</unmanagedCodeEntityReference> collection before calling the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method, ADO will automatically call the method and populate the collection for you.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src8" class="srcSentence">If you use the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method to obtain parameter information from the provider and it returns one or more variable-length data type <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution.</caps:sentence>
                      <caps:sentence id="src9" class="srcSentence"> You should explicitly set the <legacyLink xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size</legacyLink> property for these parameters before calling the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method to prevent errors.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src10" class="srcSentence">Fields</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Using the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method on the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection has no visible effect.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> To retrieve changes from the underlying database structure, you must use either the <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> method or, if the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object does not support bookmarks, the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink> method.</caps:sentence>
                  </para>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src13" class="srcSentence">Properties</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Using the <unmanagedCodeEntityReference>Refresh</unmanagedCodeEntityReference> method on a <unmanagedCodeEntityReference>Properties</unmanagedCodeEntityReference> collection of some objects populates the collection with the dynamic properties that the provider exposes.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="072fb21a-ec0f-4b02-9022-1cef3ad4bfff">
                      <caps:sentence id="src17" class="srcSentence">Axes Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="23b9fea8-4f76-4a51-95ce-1a6ce4560b34">
                      <caps:sentence id="src18" class="srcSentence">Columns Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">
                      <caps:sentence id="src19" class="srcSentence">CubeDefs Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="eaf6f4e7-2ea0-49a3-89ee-e219e025257c">
                      <caps:sentence id="src20" class="srcSentence">Dimensions Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">
                      <caps:sentence id="src21" class="srcSentence">Errors Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">
                      <caps:sentence id="src22" class="srcSentence">Fields Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="09aa7b0a-69d5-4564-80a7-20ad8189670f">
                      <caps:sentence id="src23" class="srcSentence">Groups Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="bef0fcb1-8060-4faa-84f0-3d52e9c4526f">
                      <caps:sentence id="src24" class="srcSentence">Hierarchies Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="184cf536-455c-42be-bf1c-a5c25bade961">
                      <caps:sentence id="src25" class="srcSentence">Indexes Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="cdb31c76-e559-475c-b33a-aac24f73e70e">
                      <caps:sentence id="src26" class="srcSentence">Keys Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="fed8684a-b428-4ee4-8f8d-928abe4ad9ad">
                      <caps:sentence id="src27" class="srcSentence">Levels Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="3a647cde-efdc-4394-b1b9-8cbb1b9d689f">
                      <caps:sentence id="src28" class="srcSentence">Members Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">
                      <caps:sentence id="src29" class="srcSentence">Parameters Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="5b9e7545-cf30-464d-80ef-5c99c8306bab">
                      <caps:sentence id="src30" class="srcSentence">Positions Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">
                      <caps:sentence id="src31" class="srcSentence">Procedures Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">
                      <caps:sentence id="src32" class="srcSentence">Properties Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">
                      <caps:sentence id="src33" class="srcSentence">Tables Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyLink xlink:href="0a30fa74-6f10-4410-bd70-882e7c43cd46">
                      <caps:sentence id="src34" class="srcSentence">Users Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">
                      <caps:sentence id="src35" class="srcSentence">Views Collection</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f5375fa1-4711-4f7e-9ba4-54c427f71325">Visual Basic Example</link>
        <link xlink:href="3dc3443b-a1b0-4fbd-908a-6e274dec981c">Visual C++ Example</link>
        <link xlink:href="c0fbf728-0ccb-468d-be1e-c09dad9ffddb">Visual VJ++ Example</link>
        <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property</link>
        <link xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh Method (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
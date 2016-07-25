---
title: "NextRecordset Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ab1fa449-a695-4987-b1ee-bc68f89418dd
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
# NextRecordset Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="931576974bf09203d4a7c165063ddc8b" id="tgt1" class="tgtSentence">Clears the current <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object and returns the next <legacyBold>Recordset</legacyBold> by advancing through a series of commands.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>recordset2</parameterReference> = <parameterReference>recordset1</parameterReference><legacyBold>.NextRecordset(</legacyBold><parameterReference>RecordsAffected </parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="b775937c62b6d63604df3ba677af31a8" id="tgt2" class="tgtSentence">Returns a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="c97e7c959379b1b519d87257ed091a9f" id="tgt3" class="tgtSentence"> In the syntax model, <legacyItalic>recordset1</legacyItalic> and <legacyItalic>recordset2</legacyItalic> can be the same <legacyBold>Recordset</legacyBold> object, or you can use separate objects.</caps:sentence>
            <caps:sentence sentenceid="2e4c071ff8ad88200a020ceeb0883810" id="tgt4" class="tgtSentence"> When using separate <legacyBold>Recordset</legacyBold> objects, resetting the <legacyBold>ActiveConnection</legacyBold> property on the original <legacyBold>Recordset</legacyBold> (<legacyItalic>recordset1</legacyItalic>) after <legacyBold>NextRecordset</legacyBold> has been called will generate an error.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7818b1bda08fe42f7ac5dcd9cc7471dc" id="tgt5" class="tgtSentence"> <legacyItalic>RecordsAffected</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt6" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="9180d7326b6d1f8130a89febed7965c1" id="tgt7" class="tgtSentence"> A <languageKeyword>Long</languageKeyword> variable to which the provider returns the number of records that the current operation affected.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="28dd9a4859a4c55a701835a8dfad611c" id="tgt8" class="tgtSentence">This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="8eb0905aed783fea6d77ad9fb8f80304" id="tgt9" class="tgtSentence">Use the <legacyBold>NextRecordset</legacyBold> method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results.</caps:sentence>
            <caps:sentence sentenceid="d0323970415dd8112081e85d38f54a06" id="tgt10" class="tgtSentence"> If you open a <legacyBold>Recordset</legacyBold> object based on a compound command statement (for example, "SELECT * FROM table1;SELECT * FROM table2") using the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method on a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> or the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method on a <legacyBold>Recordset</legacyBold>, ADO executes only the first command and returns the results to <legacyItalic>recordset</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="d9d252a1a555d1a13a67a9af5841ba87" id="tgt11" class="tgtSentence"> To access the results of subsequent commands in the statement, call the <legacyBold>NextRecordset</legacyBold> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="91da5e296a3e8abad5c73b35c1c5fa47" id="tgt12" class="tgtSentence">As long as there are additional results and the <legacyBold>Recordset</legacyBold> containing the compound statements is not disconnected or marshaled across process boundaries, the <legacyBold>NextRecordset</legacyBold> method will continue to return <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="d43ca9ded9b12f0b04000381640fd8b0" id="tgt13" class="tgtSentence"> If a row-returning command executes successfully but returns no records, the returned <legacyBold>Recordset</legacyBold> object will be open but empty.</caps:sentence>
            <caps:sentence sentenceid="cade1c4aa206ad9272f919638e0ffb86" id="tgt14" class="tgtSentence"> Test for this case by verifying that the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> and <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> properties are both <legacyBold>True</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="4403ff52ad3204c3a80cd8feb7b9adba" id="tgt15" class="tgtSentence"> If a non–row-returning command executes successfully, the returned <legacyBold>Recordset</legacyBold> object will be closed, which you can verify by testing the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property on the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="da9f2a4273b10de44026a9059167b07e" id="tgt16" class="tgtSentence"> When there are no more results, <legacyItalic>recordset</legacyItalic> will be set to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cd725b2e9865807bcc7121f9403877cd" id="tgt17" class="tgtSentence">The <legacyBold>NextRecordset</legacyBold> method is not available on a disconnected <legacyBold>Recordset</legacyBold> object, where <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> has been set to <legacyBold>Nothing</legacyBold> (in Microsoft Visual Basic) or NULL (in other languages).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="df95bae4a93d18270a1db52aa61438f5" id="tgt18" class="tgtSentence">If an edit is in progress while in immediate update mode, calling the <legacyBold>NextRecordset</legacyBold> method generates an error; call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> or <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method first.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="acc8beaccfeea83040bc3b8946767ea7" id="tgt19" class="tgtSentence">To pass parameters for more than one command in the compound statement by filling the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection, or by passing an array with the original <legacyBold>Open</legacyBold> or <legacyBold>Execute</legacyBold> call, the parameters must be in the same order in the collection or array as their respective commands in the command series.</caps:sentence>
            <caps:sentence sentenceid="19b050ab52fdcc90783ba0a1d6841948" id="tgt20" class="tgtSentence"> You must finish reading all the results before reading output parameter values.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="274c27da80e0e3c5675e358048a873f5" id="tgt21" class="tgtSentence">Your OLE DB provider determines when each command command in a compound statement is executed.</caps:sentence>
            <caps:sentence sentenceid="e2bd1799ec4ffadd05fa4daab3053dd8" id="tgt22" class="tgtSentence"> The <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink>, for example, executes all commands in a batch upon receiving the compound statement.</caps:sentence>
            <caps:sentence sentenceid="c9616736af8e91c05e635f40d27188fe" id="tgt23" class="tgtSentence"> The resulting <legacyBold>Recordsets</legacyBold> are simply returned when you call <legacyBold>NextRecordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cc900f12f2c7f737af8f7a382080734a" id="tgt24" class="tgtSentence">However, other providers may execute the next command in a statement only after NextRecordset is called.</caps:sentence>
            <caps:sentence sentenceid="c2d584595a5098e4c739a01c650fa12d" id="tgt25" class="tgtSentence"> For these providers, if you explicitly close the <legacyBold>Recordset</legacyBold> object before stepping through the entire command statement, ADO never executes the remaining commands.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt26" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b14806da-80d9-4da4-bb87-f558b36a6ac0">Visual Basic Example</link>
        <link xlink:href="8bb72817-0cf5-4ce9-9fb8-043c89da941c">Visual C++ Example</link>
        <link xlink:href="7948eefb-f5cc-4e74-b2f4-39033b46243d">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Clears the current <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object and returns the next <legacyBold>Recordset</legacyBold> by advancing through a series of commands.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>recordset2</parameterReference> = <parameterReference>recordset1</parameterReference><legacyBold>.NextRecordset(</legacyBold><parameterReference>RecordsAffected </parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> In the syntax model, <legacyItalic>recordset1</legacyItalic> and <legacyItalic>recordset2</legacyItalic> can be the same <legacyBold>Recordset</legacyBold> object, or you can use separate objects.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> When using separate <legacyBold>Recordset</legacyBold> objects, resetting the <legacyBold>ActiveConnection</legacyBold> property on the original <legacyBold>Recordset</legacyBold> (<legacyItalic>recordset1</legacyItalic>) after <legacyBold>NextRecordset</legacyBold> has been called will generate an error.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>RecordsAffected</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> A <languageKeyword>Long</languageKeyword> variable to which the provider returns the number of records that the current operation affected.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <alert class="note">
            <para>
              <caps:sentence id="src8" class="srcSentence">This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">Use the <legacyBold>NextRecordset</legacyBold> method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> If you open a <legacyBold>Recordset</legacyBold> object based on a compound command statement (for example, "SELECT * FROM table1;SELECT * FROM table2") using the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method on a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> or the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method on a <legacyBold>Recordset</legacyBold>, ADO executes only the first command and returns the results to <legacyItalic>recordset</legacyItalic>.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> To access the results of subsequent commands in the statement, call the <legacyBold>NextRecordset</legacyBold> method.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">As long as there are additional results and the <legacyBold>Recordset</legacyBold> containing the compound statements is not disconnected or marshaled across process boundaries, the <legacyBold>NextRecordset</legacyBold> method will continue to return <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> If a row-returning command executes successfully but returns no records, the returned <legacyBold>Recordset</legacyBold> object will be open but empty.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> Test for this case by verifying that the <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> and <legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> properties are both <legacyBold>True</legacyBold>.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> If a non–row-returning command executes successfully, the returned <legacyBold>Recordset</legacyBold> object will be closed, which you can verify by testing the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property on the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> When there are no more results, <legacyItalic>recordset</legacyItalic> will be set to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">The <legacyBold>NextRecordset</legacyBold> method is not available on a disconnected <legacyBold>Recordset</legacyBold> object, where <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> has been set to <legacyBold>Nothing</legacyBold> (in Microsoft Visual Basic) or NULL (in other languages).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If an edit is in progress while in immediate update mode, calling the <legacyBold>NextRecordset</legacyBold> method generates an error; call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> or <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method first.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">To pass parameters for more than one command in the compound statement by filling the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection, or by passing an array with the original <legacyBold>Open</legacyBold> or <legacyBold>Execute</legacyBold> call, the parameters must be in the same order in the collection or array as their respective commands in the command series.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> You must finish reading all the results before reading output parameter values.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">Your OLE DB provider determines when each command command in a compound statement is executed.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> The <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink>, for example, executes all commands in a batch upon receiving the compound statement.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> The resulting <legacyBold>Recordsets</legacyBold> are simply returned when you call <legacyBold>NextRecordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">However, other providers may execute the next command in a statement only after NextRecordset is called.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> For these providers, if you explicitly close the <legacyBold>Recordset</legacyBold> object before stepping through the entire command statement, ADO never executes the remaining commands.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src26" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b14806da-80d9-4da4-bb87-f558b36a6ac0">Visual Basic Example</link>
        <link xlink:href="8bb72817-0cf5-4ce9-9fb8-043c89da941c">Visual C++ Example</link>
        <link xlink:href="7948eefb-f5cc-4e74-b2f4-39033b46243d">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
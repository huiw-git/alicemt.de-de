---
title: "Transaction Processing"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 74ab6706-e2dc-42cb-af77-dbc58a9cf4ce
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
# Transaction Processing
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ed40868d8f48b07cf37a8c1af08627ea" id="tgt1" class="tgtSentence">A <legacyItalic>transaction </legacyItalic>delimits the beginning and end of a series of data access operations executed across a connection.</caps:sentence>
          <caps:sentence sentenceid="4cc79883cc1bd64b660610f2755c51ff" id="tgt2" class="tgtSentence"> Subject to the transactional capabilities of your data source, the <legacyBold>Connection</legacyBold> object also allows you to create and manage transactions.</caps:sentence>
          <caps:sentence sentenceid="e13083b4d16691a42b097706ce164ccc" id="tgt3" class="tgtSentence"> For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server, you can create multiple nested transactions for the commands you execute.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="46dace4a3f9a27b8ab5d097fe4212c7d" id="tgt4" class="tgtSentence">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9646074e97c7f0a2255d3a96b39ec9d1" id="tgt5" class="tgtSentence">If you cancel the transaction, or if one of its operations fails, the result will be as if none of the operations in the transaction occurred.</caps:sentence>
          <caps:sentence sentenceid="247bcd0db934ac4c3afb9300b5ca243b" id="tgt6" class="tgtSentence"> The data source will remain as it was before the transaction began.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f9968232aac8265783ff1bb691cc2405" id="tgt7" class="tgtSentence">ADO provides the following methods for controlling transactions: <legacyBold>BeginTrans</legacyBold>, <legacyBold>CommitTrans</legacyBold>, and <legacyBold>RollbackTrans</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="95bdf931c530c0ae5e50f8b69375f9b6" id="tgt8" class="tgtSentence"> Use these methods with a <legacyBold>Connection</legacyBold> object when you want to save or cancel a series of changes made to the source data as a single unit.</caps:sentence>
          <caps:sentence sentenceid="714627ee173a35a32a033a0f0128d068" id="tgt9" class="tgtSentence"> For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other.</caps:sentence>
          <caps:sentence sentenceid="7e3bfbbf8152e76331fc522e7c8abb83" id="tgt10" class="tgtSentence"> If either update fails, the accounts no longer balance.</caps:sentence>
          <caps:sentence sentenceid="ea49e751e5c279a6d7af39ad1a778f84" id="tgt11" class="tgtSentence"> Making these changes within an open transaction ensures that either all or none of the changes go through.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="5744353ad26597c7b64a08d78bbadb21" id="tgt12" class="tgtSentence">Not all providers support transactions.</caps:sentence>
            <caps:sentence sentenceid="bd67fe472e4810706ad4bc406cded4fb" id="tgt13" class="tgtSentence"> Verify that the provider-defined property "<legacyBold>Transaction DDL</legacyBold>" appears in the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection, indicating that the provider supports transactions.</caps:sentence>
            <caps:sentence sentenceid="8caff03787457e405f97339d2d52a152" id="tgt14" class="tgtSentence"> If the provider does not support transactions, calling one of these methods will return an error.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="0d9a40b5cde8308108d35262fc79ccea" id="tgt15" class="tgtSentence">After you call the <legacyBold>BeginTrans</legacyBold> method, the provider will no longer instantaneously commit changes you make until you call <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> to end the transaction.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="be3f1d19505c4af3a2ba3687e95bc694" id="tgt16" class="tgtSentence">Calling the <legacyBold>CommitTrans</legacyBold> method saves changes made within an open transaction on the connection and ends the transaction.</caps:sentence>
          <caps:sentence sentenceid="59517ec8c64cd18c273a94cd36d7b639" id="tgt17" class="tgtSentence"> Calling the <legacyBold>RollbackTrans</legacyBold> method reverses any changes made within an open transaction and ends the transaction.</caps:sentence>
          <caps:sentence sentenceid="00c67f059f2d5c56fb3cf6f4f30580ad" id="tgt18" class="tgtSentence"> Calling either method when there is no open transaction generates an error.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="62e72bd1564986b4b15e161ad133638b" id="tgt19" class="tgtSentence">Depending on the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property, calling either the <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> method may automatically start a new transaction.</caps:sentence>
          <caps:sentence sentenceid="d59ad127df76bca23876cd943bf4c7d1" id="tgt20" class="tgtSentence"> If the <legacyBold>Attributes</legacyBold> property is set to <legacyBold>adXactCommitRetaining</legacyBold>, the provider automatically starts a new transaction after a <legacyBold>CommitTrans</legacyBold> call.</caps:sentence>
          <caps:sentence sentenceid="c46a640f26f33eb49b76b805925990a3" id="tgt21" class="tgtSentence"> If the <legacyBold>Attributes</legacyBold> property is set to <legacyBold>adXactAbortRetaining</legacyBold>, the provider automatically starts a new transaction after a <legacyBold>RollbackTrans</legacyBold> call.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="023c5839bc7a84967758ae4e736d5402" id="tgt22" class="tgtSentence">Transaction Isolation Level</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="54e6e4a26eafec813a143abe62e36d01" id="tgt23" class="tgtSentence">Use the <legacyBold>IsolationLevel</legacyBold> property to set the isolation level of a transaction on a <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="f1eb267b0b438ca140725e2f74957737" id="tgt24" class="tgtSentence"> The setting does not take effect until the next time you call the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="80e27d84b6a6164850a218b8fa06a3ec" id="tgt25" class="tgtSentence"> If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</caps:sentence>
            <caps:sentence sentenceid="38012bc793960943990f7cb90ef42945" id="tgt26" class="tgtSentence"> Refer to the <legacyBold>IsolationLevel</legacyBold> property in the ADO Programmer's Reference for more details on valid values.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="927bf11aa5a703b7c83de7f9833983b3" id="tgt27" class="tgtSentence">Nested Transactions</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5da5a3404ed9f161a62edffbd207971e" id="tgt28" class="tgtSentence">For providers that support nested transactions, calling the <legacyBold>BeginTrans</legacyBold> method within an open transaction starts a new, nested transaction.</caps:sentence>
            <caps:sentence sentenceid="5bf7b055459411b901af733687a98f99" id="tgt29" class="tgtSentence"> The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth.</caps:sentence>
            <caps:sentence sentenceid="b91bf2c4c8c9f388cb401f0029a8011a" id="tgt30" class="tgtSentence"> Calling <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">A <legacyItalic>transaction </legacyItalic>delimits the beginning and end of a series of data access operations executed across a connection.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Subject to the transactional capabilities of your data source, the <legacyBold>Connection</legacyBold> object also allows you to create and manage transactions.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server, you can create multiple nested transactions for the commands you execute.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">If you cancel the transaction, or if one of its operations fails, the result will be as if none of the operations in the transaction occurred.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The data source will remain as it was before the transaction began.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">ADO provides the following methods for controlling transactions: <legacyBold>BeginTrans</legacyBold>, <legacyBold>CommitTrans</legacyBold>, and <legacyBold>RollbackTrans</legacyBold>.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Use these methods with a <legacyBold>Connection</legacyBold> object when you want to save or cancel a series of changes made to the source data as a single unit.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> If either update fails, the accounts no longer balance.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> Making these changes within an open transaction ensures that either all or none of the changes go through.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src12" class="srcSentence">Not all providers support transactions.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Verify that the provider-defined property "<legacyBold>Transaction DDL</legacyBold>" appears in the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection, indicating that the provider supports transactions.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> If the provider does not support transactions, calling one of these methods will return an error.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src15" class="srcSentence">After you call the <legacyBold>BeginTrans</legacyBold> method, the provider will no longer instantaneously commit changes you make until you call <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> to end the transaction.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src16" class="srcSentence">Calling the <legacyBold>CommitTrans</legacyBold> method saves changes made within an open transaction on the connection and ends the transaction.</caps:sentence>
          <caps:sentence id="src17" class="srcSentence"> Calling the <legacyBold>RollbackTrans</legacyBold> method reverses any changes made within an open transaction and ends the transaction.</caps:sentence>
          <caps:sentence id="src18" class="srcSentence"> Calling either method when there is no open transaction generates an error.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src19" class="srcSentence">Depending on the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property, calling either the <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> method may automatically start a new transaction.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> If the <legacyBold>Attributes</legacyBold> property is set to <legacyBold>adXactCommitRetaining</legacyBold>, the provider automatically starts a new transaction after a <legacyBold>CommitTrans</legacyBold> call.</caps:sentence>
          <caps:sentence id="src21" class="srcSentence"> If the <legacyBold>Attributes</legacyBold> property is set to <legacyBold>adXactAbortRetaining</legacyBold>, the provider automatically starts a new transaction after a <legacyBold>RollbackTrans</legacyBold> call.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Transaction Isolation Level</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src23" class="srcSentence">Use the <legacyBold>IsolationLevel</legacyBold> property to set the isolation level of a transaction on a <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> The setting does not take effect until the next time you call the <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">BeginTrans</legacyLink> method.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> Refer to the <legacyBold>IsolationLevel</legacyBold> property in the ADO Programmer's Reference for more details on valid values.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">Nested Transactions</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src28" class="srcSentence">For providers that support nested transactions, calling the <legacyBold>BeginTrans</legacyBold> method within an open transaction starts a new, nested transaction.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> Calling <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
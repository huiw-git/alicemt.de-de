---
title: "BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d4683472-4120-4236-8640-fa9ae289e23e
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
# BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="588ec7f32aeee59bd5d389952454c07e" id="tgt1" class="tgtSentence">These transaction methods manage transaction processing within a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object as follows:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="929f15c3c86730ad3b514d64c849ba29" id="tgt2" class="tgtSentence">
                <legacyBold>BeginTrans</legacyBold>     Begins a new transaction.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e14261daadd537aa8309e0509c8f0b5f" id="tgt3" class="tgtSentence">
                <legacyBold>CommitTrans</legacyBold>     Saves any changes and ends the current transaction.</caps:sentence>
              <caps:sentence sentenceid="0d170df5fe4be946ab147e1ba485f7df" id="tgt4" class="tgtSentence"> It may also start a new transaction.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="70b667f1fa7b10d7b825264db8069479" id="tgt5" class="tgtSentence">
                <legacyBold>RollbackTrans</legacyBold>      Cancels any changes made during the current transaction and ends the transaction.</caps:sentence>
              <caps:sentence sentenceid="0d170df5fe4be946ab147e1ba485f7df" id="tgt6" class="tgtSentence"> It may also start a new transaction.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <syntaxSection>
        <legacySyntax>
level = object.BeginTrans()
object.BeginTrans
object.CommitTrans
object.RollbackTrans</legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="1e3e76db15423624f7e020b6f1a9c50e" id="tgt7" class="tgtSentence">
              <legacyBold>BeginTrans</legacyBold> can be called as a function that returns a <languageKeyword>Long</languageKeyword> variable indicating the nesting level of the transaction.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7dac69667e814ea09c728e6d30f5074d" id="tgt8" class="tgtSentence"> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="89b6703484f3b19e301c9eec6a7e8208" id="tgt9" class="tgtSentence">A <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="4717d53ebfdfea8477f780ec66151dcb" id="tgt10" class="tgtSentence">Connection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f7b05438e8aa5456a7f30be5542da16a" id="tgt11" class="tgtSentence">Use these methods with a <legacyBold>Connection</legacyBold> object when you want to save or cancel a series of changes made to the source data as a single unit.</caps:sentence>
                <caps:sentence sentenceid="714627ee173a35a32a033a0f0128d068" id="tgt12" class="tgtSentence"> For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other.</caps:sentence>
                <caps:sentence sentenceid="7e3bfbbf8152e76331fc522e7c8abb83" id="tgt13" class="tgtSentence"> If either update fails, the accounts no longer balance.</caps:sentence>
                <caps:sentence sentenceid="ea49e751e5c279a6d7af39ad1a778f84" id="tgt14" class="tgtSentence"> Making these changes within an open transaction ensures that either all or none of the changes go through.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="5744353ad26597c7b64a08d78bbadb21" id="tgt15" class="tgtSentence">Not all providers support transactions.</caps:sentence>
                  <caps:sentence sentenceid="bd67fe472e4810706ad4bc406cded4fb" id="tgt16" class="tgtSentence"> Verify that the provider-defined property "<legacyBold>Transaction DDL</legacyBold>" appears in the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection, indicating that the provider supports transactions.</caps:sentence>
                  <caps:sentence sentenceid="8caff03787457e405f97339d2d52a152" id="tgt17" class="tgtSentence"> If the provider does not support transactions, calling one of these methods will return an error.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="0d9a40b5cde8308108d35262fc79ccea" id="tgt18" class="tgtSentence">After you call the <legacyBold>BeginTrans</legacyBold> method, the provider will no longer instantaneously commit changes you make until you call <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> to end the transaction.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5da5a3404ed9f161a62edffbd207971e" id="tgt19" class="tgtSentence">For providers that support nested transactions, calling the <legacyBold>BeginTrans</legacyBold> method within an open transaction starts a new, nested transaction.</caps:sentence>
                <caps:sentence sentenceid="5bf7b055459411b901af733687a98f99" id="tgt20" class="tgtSentence"> The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth.</caps:sentence>
                <caps:sentence sentenceid="b91bf2c4c8c9f388cb401f0029a8011a" id="tgt21" class="tgtSentence"> Calling <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="be3f1d19505c4af3a2ba3687e95bc694" id="tgt22" class="tgtSentence">Calling the <legacyBold>CommitTrans</legacyBold> method saves changes made within an open transaction on the connection and ends the transaction.</caps:sentence>
                <caps:sentence sentenceid="59517ec8c64cd18c273a94cd36d7b639" id="tgt23" class="tgtSentence"> Calling the <legacyBold>RollbackTrans</legacyBold> method reverses any changes made within an open transaction and ends the transaction.</caps:sentence>
                <caps:sentence sentenceid="00c67f059f2d5c56fb3cf6f4f30580ad" id="tgt24" class="tgtSentence"> Calling either method when there is no open transaction generates an error.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c0f063801657acea67247752e940e442" id="tgt25" class="tgtSentence">Depending on the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property, calling either the <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> methods may automatically start a new transaction.</caps:sentence>
                <caps:sentence sentenceid="d59ad127df76bca23876cd943bf4c7d1" id="tgt26" class="tgtSentence"> If the <legacyBold>Attributes</legacyBold> property is set to <legacyBold>adXactCommitRetaining</legacyBold>, the provider automatically starts a new transaction after a <legacyBold>CommitTrans</legacyBold> call.</caps:sentence>
                <caps:sentence sentenceid="c46a640f26f33eb49b76b805925990a3" id="tgt27" class="tgtSentence"> If the <legacyBold>Attributes</legacyBold> property is set to <legacyBold>adXactAbortRetaining</legacyBold>, the provider automatically starts a new transaction after a <legacyBold>RollbackTrans</legacyBold> call.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="63c94bdfa1808c56c20d49ee0e33e436" id="tgt28" class="tgtSentence">Remote Data Service</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cd22e37b9c70f21f0ce6a21b4c2169b2" id="tgt29" class="tgtSentence">The <legacyBold>BeginTrans</legacyBold>, <legacyBold>CommitTrans</legacyBold>, and <legacyBold>RollbackTrans</legacyBold> methods are not available on a client-side <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </parameters>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt30" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="aa7de324-cd71-4bd0-8043-24229f4a785e">Visual Basic Example</link>
        <link xlink:href="4ac19647-73e7-4edf-9913-25c8fd927e36">Visual C++ Example</link>
        <link xlink:href="27f502f8-d66a-4b44-9071-a05993d3fabb">Visual J++ Example</link>
        <link xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">These transaction methods manage transaction processing within a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object as follows:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">
                <legacyBold>BeginTrans</legacyBold>     Begins a new transaction.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">
                <legacyBold>CommitTrans</legacyBold>     Saves any changes and ends the current transaction.</caps:sentence>
              <caps:sentence id="src4" class="srcSentence"> It may also start a new transaction.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">
                <legacyBold>RollbackTrans</legacyBold>      Cancels any changes made during the current transaction and ends the transaction.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> It may also start a new transaction.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <syntaxSection>
        <legacySyntax>
level = object.BeginTrans()
object.BeginTrans
object.CommitTrans
object.RollbackTrans</legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">
              <legacyBold>BeginTrans</legacyBold> can be called as a function that returns a <languageKeyword>Long</languageKeyword> variable indicating the nesting level of the transaction.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">A <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src10" class="srcSentence">Connection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src11" class="srcSentence">Use these methods with a <legacyBold>Connection</legacyBold> object when you want to save or cancel a series of changes made to the source data as a single unit.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> If either update fails, the accounts no longer balance.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> Making these changes within an open transaction ensures that either all or none of the changes go through.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src15" class="srcSentence">Not all providers support transactions.</caps:sentence>
                  <caps:sentence id="src16" class="srcSentence"> Verify that the provider-defined property "<legacyBold>Transaction DDL</legacyBold>" appears in the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection, indicating that the provider supports transactions.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> If the provider does not support transactions, calling one of these methods will return an error.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src18" class="srcSentence">After you call the <legacyBold>BeginTrans</legacyBold> method, the provider will no longer instantaneously commit changes you make until you call <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> to end the transaction.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src19" class="srcSentence">For providers that support nested transactions, calling the <legacyBold>BeginTrans</legacyBold> method within an open transaction starts a new, nested transaction.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> Calling <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src22" class="srcSentence">Calling the <legacyBold>CommitTrans</legacyBold> method saves changes made within an open transaction on the connection and ends the transaction.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> Calling the <legacyBold>RollbackTrans</legacyBold> method reverses any changes made within an open transaction and ends the transaction.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> Calling either method when there is no open transaction generates an error.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src25" class="srcSentence">Depending on the <legacyBold>Connection</legacyBold> object's <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property, calling either the <legacyBold>CommitTrans</legacyBold> or <legacyBold>RollbackTrans</legacyBold> methods may automatically start a new transaction.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> If the <legacyBold>Attributes</legacyBold> property is set to <legacyBold>adXactCommitRetaining</legacyBold>, the provider automatically starts a new transaction after a <legacyBold>CommitTrans</legacyBold> call.</caps:sentence>
                <caps:sentence id="src27" class="srcSentence"> If the <legacyBold>Attributes</legacyBold> property is set to <legacyBold>adXactAbortRetaining</legacyBold>, the provider automatically starts a new transaction after a <legacyBold>RollbackTrans</legacyBold> call.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src28" class="srcSentence">Remote Data Service</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src29" class="srcSentence">The <legacyBold>BeginTrans</legacyBold>, <legacyBold>CommitTrans</legacyBold>, and <legacyBold>RollbackTrans</legacyBold> methods are not available on a client-side <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </parameters>
      <section>
        <title>
          <caps:sentence id="src30" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="aa7de324-cd71-4bd0-8043-24229f4a785e">Visual Basic Example</link>
        <link xlink:href="4ac19647-73e7-4edf-9913-25c8fd927e36">Visual C++ Example</link>
        <link xlink:href="27f502f8-d66a-4b44-9071-a05993d3fabb">Visual J++ Example</link>
        <link xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
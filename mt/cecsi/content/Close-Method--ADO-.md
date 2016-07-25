---
title: "Close Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3cdf27d1-a180-4cff-8e42-95dec5fb1b55
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
# Close Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="00ce5bb31e4d14be6b806e2b19829049" id="tgt1" class="tgtSentence">Closes an open object and any dependent objects.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>object</parameterReference>.<legacyBold>Close</legacyBold></legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="bacb29d561f062a0ae977ba0389333f7" id="tgt2" class="tgtSentence">Use the <legacyBold>Close</legacyBold> method to close a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, or a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object to free any associated system resources.</caps:sentence>
            <caps:sentence sentenceid="8783c1fd24e7d1bd27aae0815f0c28e3" id="tgt3" class="tgtSentence"> Closing an object does not remove it from memory; you can change its property settings and open it again later.</caps:sentence>
            <caps:sentence sentenceid="6ac4b18c6f07f7198b6520fcc3a0bb06" id="tgt4" class="tgtSentence"> To completely eliminate an object from memory, close the object and then set the object variable to <legacyItalic>Nothing</legacyItalic> (in Visual Basic).</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="4717d53ebfdfea8477f780ec66151dcb" id="tgt5" class="tgtSentence">Connection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="16d532a25583e13e1771478330e89ac3" id="tgt6" class="tgtSentence">Using the <legacyBold>Close</legacyBold> method to close a <legacyBold>Connection</legacyBold> object also closes any active <legacyBold>Recordset</legacyBold> objects associated with the connection.</caps:sentence>
                <caps:sentence sentenceid="9da7cdbcc0da717b80adbd215c5e36cc" id="tgt7" class="tgtSentence"> A <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object associated with the <legacyBold>Connection</legacyBold> object you are closing will persist, but it will no longer be associated with a <legacyBold>Connection</legacyBold> object; that is, its <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property will be set to <legacyBold>Nothing</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="8ea3f1d1d7b071dae31db3f90afde2bd" id="tgt8" class="tgtSentence"> Also, the <legacyBold>Command</legacyBold> object's <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection will be cleared of any provider-defined parameters.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="81b24d561c25f1e9ded7eabdf6fd1094" id="tgt9" class="tgtSentence">You can later call the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method to re-establish the connection to the same, or another, data source.</caps:sentence>
                <caps:sentence sentenceid="fbe33335e87ea52a38b1f7c4a71ba606" id="tgt10" class="tgtSentence"> While the <legacyBold>Connection</legacyBold> object is closed, calling any methods that require an open connection to the data source generates an error.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8fa838dac47a5348b5f4b276c803ad59" id="tgt11" class="tgtSentence">Closing a <legacyBold>Connection</legacyBold> object while there are open <legacyBold>Recordset</legacyBold> objects on the connection rolls back any pending changes in all of the <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
                <caps:sentence sentenceid="1e8782f78bf6e952188635758799bde4" id="tgt12" class="tgtSentence"> Explicitly closing a <legacyBold>Connection</legacyBold> object (calling the <legacyBold>Close</legacyBold> method) while a transaction is in progress generates an error.</caps:sentence>
                <caps:sentence sentenceid="954f21b43d10b10f986432aeabcea1b8" id="tgt13" class="tgtSentence"> If a <legacyBold>Connection</legacyBold> object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="390134123ca48b11e003e44c16a864c6" id="tgt14" class="tgtSentence">Recordset, Record, Stream</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="536dfc7777d64bf72a360bbff9a18a19" id="tgt15" class="tgtSentence">Using the <legacyBold>Close</legacyBold> method to close a <legacyBold>Recordset</legacyBold>, <legacyBold>Record</legacyBold>, or <legacyBold>Stream</legacyBold> object releases the associated data and any exclusive access you may have had to the data through this particular object.</caps:sentence>
                <caps:sentence sentenceid="8fdf3b4a5b6d250f4e4eee17a45f3b9d" id="tgt16" class="tgtSentence"> You can later call the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method to reopen the object with the same, or modified, attributes.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a7416cc92af42933c41afdafcd3e1038" id="tgt17" class="tgtSentence">While a <legacyBold>Recordset</legacyBold> object is closed, calling any methods that require a live cursor generates an error.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c4485686d4b5bfda724d80d796891bd8" id="tgt18" class="tgtSentence">If an edit is in progress while in immediate update mode, calling the <legacyBold>Close</legacyBold> method generates an error; instead, call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> or <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method first.</caps:sentence>
                <caps:sentence sentenceid="e5ad551452c0cc0f86a85b56ca2d847a" id="tgt19" class="tgtSentence"> If you close the <legacyBold>Recordset</legacyBold> object while in batch update mode, all changes since the last <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> call are lost.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c16d97e69c6f955c9f7ecdbb9749c565" id="tgt20" class="tgtSentence">If you use the <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">Clone</legacyLink> method to create copies of an open <legacyBold>Recordset</legacyBold> object, closing the original or a clone does not affect any of the other copies.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt21" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1311d561-0e86-40f5-8cbc-ad8f13e626d1">Visual Basic Example</link>
        <link xlink:href="66eca011-e258-4d8f-bd67-e017bcf0871b">VBScript Example</link>
        <link xlink:href="f74a81fd-cbcc-4143-b9f8-774c88dd4fad">Visual C++ Example</link>
        <link xlink:href="0b7dd9f8-4751-48fb-a75d-c6f75d80d928">Visual J++ Example</link>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Closes an open object and any dependent objects.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>object</parameterReference>.<legacyBold>Close</legacyBold></legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Use the <legacyBold>Close</legacyBold> method to close a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, or a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object to free any associated system resources.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Closing an object does not remove it from memory; you can change its property settings and open it again later.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> To completely eliminate an object from memory, close the object and then set the object variable to <legacyItalic>Nothing</legacyItalic> (in Visual Basic).</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src5" class="srcSentence">Connection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src6" class="srcSentence">Using the <legacyBold>Close</legacyBold> method to close a <legacyBold>Connection</legacyBold> object also closes any active <legacyBold>Recordset</legacyBold> objects associated with the connection.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> A <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object associated with the <legacyBold>Connection</legacyBold> object you are closing will persist, but it will no longer be associated with a <legacyBold>Connection</legacyBold> object; that is, its <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property will be set to <legacyBold>Nothing</legacyBold>.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> Also, the <legacyBold>Command</legacyBold> object's <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection will be cleared of any provider-defined parameters.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src9" class="srcSentence">You can later call the <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink> method to re-establish the connection to the same, or another, data source.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> While the <legacyBold>Connection</legacyBold> object is closed, calling any methods that require an open connection to the data source generates an error.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src11" class="srcSentence">Closing a <legacyBold>Connection</legacyBold> object while there are open <legacyBold>Recordset</legacyBold> objects on the connection rolls back any pending changes in all of the <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> Explicitly closing a <legacyBold>Connection</legacyBold> object (calling the <legacyBold>Close</legacyBold> method) while a transaction is in progress generates an error.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> If a <legacyBold>Connection</legacyBold> object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src14" class="srcSentence">Recordset, Record, Stream</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src15" class="srcSentence">Using the <legacyBold>Close</legacyBold> method to close a <legacyBold>Recordset</legacyBold>, <legacyBold>Record</legacyBold>, or <legacyBold>Stream</legacyBold> object releases the associated data and any exclusive access you may have had to the data through this particular object.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> You can later call the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method to reopen the object with the same, or modified, attributes.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src17" class="srcSentence">While a <legacyBold>Recordset</legacyBold> object is closed, calling any methods that require a live cursor generates an error.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src18" class="srcSentence">If an edit is in progress while in immediate update mode, calling the <legacyBold>Close</legacyBold> method generates an error; instead, call the <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> or <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate</legacyLink> method first.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> If you close the <legacyBold>Recordset</legacyBold> object while in batch update mode, all changes since the last <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink> call are lost.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src20" class="srcSentence">If you use the <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">Clone</legacyLink> method to create copies of an open <legacyBold>Recordset</legacyBold> object, closing the original or a clone does not affect any of the other copies.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1311d561-0e86-40f5-8cbc-ad8f13e626d1">Visual Basic Example</link>
        <link xlink:href="66eca011-e258-4d8f-bd67-e017bcf0871b">VBScript Example</link>
        <link xlink:href="f74a81fd-cbcc-4143-b9f8-774c88dd4fad">Visual C++ Example</link>
        <link xlink:href="0b7dd9f8-4751-48fb-a75d-c6f75d80d928">Visual J++ Example</link>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
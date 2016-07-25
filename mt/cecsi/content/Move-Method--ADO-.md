---
title: "Move Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 13fe9381-d00b-4f4a-9162-83c3f21b3837
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
# Move Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3ed7d36b2fa1c27b3bc70498f2e99582" id="tgt1" class="tgtSentence">Moves the position of the current record in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.Move</legacyBold>
          <parameterReference>NumRecords</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Start</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="c4818e3a4bc7732470a81f2c6c9d7bf2" id="tgt2" class="tgtSentence"> <legacyItalic>NumRecords</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="4dcf10b8d0f738f89d54207d2af57d40" id="tgt3" class="tgtSentence">A signed <languageKeyword>Long</languageKeyword> expression that specifies the number of records that the current record position moves.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="922ed5a49d50fca828b4bba43d2f705e" id="tgt4" class="tgtSentence"> <legacyItalic>Start</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt5" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="23a4c5d83d088d0cf210732bd114b1a2" id="tgt6" class="tgtSentence"> A <languageKeyword>String</languageKeyword> value or <languageKeyword>Variant</languageKeyword> that evaluates to a bookmark.</caps:sentence>
                <caps:sentence sentenceid="80aa3459d9b3cadc111520375fbb4ef6" id="tgt7" class="tgtSentence"> You can also use a <legacyLink xlink:href="55d273c4-ccee-48ef-ba90-8893d04313c8">BookmarkEnum</legacyLink> value.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="028e2e11b4b7d9bebb5d384c62910c2c" id="tgt8" class="tgtSentence">The <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> method is supported on all <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fcd559925b20ccf194848897d3f918b8" id="tgt9" class="tgtSentence">If the <legacyItalic>NumRecords</legacyItalic> argument is greater than zero, the current record position moves forward (toward the end of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>).</caps:sentence>
            <caps:sentence sentenceid="60356919523ec7338d449aabf22efa3b" id="tgt10" class="tgtSentence"> If <legacyItalic>NumRecords</legacyItalic> is less than zero, the current record position moves backward (toward the beginning of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0aae500cdf339351d03f135e50390f73" id="tgt11" class="tgtSentence">If the <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset (<legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> is <languageKeyword>True</languageKeyword>).</caps:sentence>
            <caps:sentence sentenceid="6c098f56defa6a7b2eae851f9160bccf" id="tgt12" class="tgtSentence"> An attempt to move backward when the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> property is already <languageKeyword>True</languageKeyword> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="01cf2791b1c901572be1f7efa92dffe3" id="tgt13" class="tgtSentence">If the <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset (<legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> is <languageKeyword>True</languageKeyword>).</caps:sentence>
            <caps:sentence sentenceid="ec844e3b588e1fa2c27852c5ca24a2a0" id="tgt14" class="tgtSentence"> An attempt to move forward when the <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> property is already <languageKeyword>True</languageKeyword> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f958fbf93a310cfbfacc45e8d2dc12f6" id="tgt15" class="tgtSentence">Calling the <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> method from an empty <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2ae6aa73b10604bc7d0ca2977e153455" id="tgt16" class="tgtSentence">If you pass the <legacyItalic>Start</legacyItalic> argument, the move is relative to the record with this bookmark, assuming the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports bookmarks.</caps:sentence>
            <caps:sentence sentenceid="b2d25f66d32d22ed9015297a9115fd76" id="tgt17" class="tgtSentence"> If not specified, the move is relative to the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0da6e49faa9cbdc9ec7c6b5e5a0ed71b" id="tgt18" class="tgtSentence">If you are using the <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">CacheSize</legacyLink> property to locally cache records from the provider, passing a <legacyItalic>NumRecords</legacyItalic> argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</caps:sentence>
            <caps:sentence sentenceid="4f55c66009f12c0a34272b8757ba88f3" id="tgt19" class="tgtSentence"> The <unmanagedCodeEntityReference>CacheSize</unmanagedCodeEntityReference> property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="957f19604533c9e9da8316d4f5a27733" id="tgt20" class="tgtSentence">If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is forward only, a user can still pass a <legacyItalic>NumRecords</legacyItalic> argument less than zero, provided the destination is within the current set of cached records.</caps:sentence>
            <caps:sentence sentenceid="216772a11363ca8038e7946c05d28b22" id="tgt21" class="tgtSentence"> If the <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> call would move the current record position to a record before the first cached record, an error will occur.</caps:sentence>
            <caps:sentence sentenceid="4b51b7d5581869fa19e7881d935f10da" id="tgt22" class="tgtSentence"> Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</caps:sentence>
            <caps:sentence sentenceid="d2ac213cf10f4843a425b61353d18f30" id="tgt23" class="tgtSentence"> Because cached records are loaded into memory, you should avoid caching more records than are necessary.</caps:sentence>
            <caps:sentence sentenceid="a3805a7def28ca787227ca763bd1833f" id="tgt24" class="tgtSentence"> Even if a forward-only <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports backward moves in this way, calling the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MovePrevious</legacyLink> method on any forward-only <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object will still generate an error.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="6f9b820d159dc19d7bafe5d50a5b2df7" id="tgt25" class="tgtSentence">Support for moving backwards in a forward-only <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is not predictable, depending upon your provider.</caps:sentence>
              <caps:sentence sentenceid="16c71dea13319c5b148fd06f0b1b3eb6" id="tgt26" class="tgtSentence"> If the current record has been positioned after the last record in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> backwards may not result in the correct current position.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt27" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="55eb797a-0205-40d2-a797-55b216d1d3bb">Visual Basic Example</link>
        <link xlink:href="29ec4b95-8986-4970-943f-3da3ecb207a2">VBScript Example</link>
        <link xlink:href="0e08af60-f668-4092-8b6a-9e8b6db90448">Visual C++ Example</link>
        <link xlink:href="b29ddb8c-ceb3-4aad-a240-8030462fceba">Visual J++ Example</link>
        <link xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods</link>
        <link xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</link>
        <link xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Moves the position of the current record in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.Move</legacyBold>
          <parameterReference>NumRecords</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Start</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>NumRecords</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A signed <languageKeyword>Long</languageKeyword> expression that specifies the number of records that the current record position moves.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>Start</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> A <languageKeyword>String</languageKeyword> value or <languageKeyword>Variant</languageKeyword> that evaluates to a bookmark.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> You can also use a <legacyLink xlink:href="55d273c4-ccee-48ef-ba90-8893d04313c8">BookmarkEnum</legacyLink> value.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> method is supported on all <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">If the <legacyItalic>NumRecords</legacyItalic> argument is greater than zero, the current record position moves forward (toward the end of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>).</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> If <legacyItalic>NumRecords</legacyItalic> is less than zero, the current record position moves backward (toward the beginning of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If the <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset (<legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> is <languageKeyword>True</languageKeyword>).</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> An attempt to move backward when the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> property is already <languageKeyword>True</languageKeyword> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">If the <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset (<legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> is <languageKeyword>True</languageKeyword>).</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> An attempt to move forward when the <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> property is already <languageKeyword>True</languageKeyword> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">Calling the <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> method from an empty <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">If you pass the <legacyItalic>Start</legacyItalic> argument, the move is relative to the record with this bookmark, assuming the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports bookmarks.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> If not specified, the move is relative to the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If you are using the <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">CacheSize</legacyLink> property to locally cache records from the provider, passing a <legacyItalic>NumRecords</legacyItalic> argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> The <unmanagedCodeEntityReference>CacheSize</unmanagedCodeEntityReference> property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">If the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is forward only, a user can still pass a <legacyItalic>NumRecords</legacyItalic> argument less than zero, provided the destination is within the current set of cached records.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> If the <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> call would move the current record position to a record before the first cached record, an error will occur.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> Because cached records are loaded into memory, you should avoid caching more records than are necessary.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> Even if a forward-only <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object supports backward moves in this way, calling the <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MovePrevious</legacyLink> method on any forward-only <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object will still generate an error.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src25" class="srcSentence">Support for moving backwards in a forward-only <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is not predictable, depending upon your provider.</caps:sentence>
              <caps:sentence id="src26" class="srcSentence"> If the current record has been positioned after the last record in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, <unmanagedCodeEntityReference>Move</unmanagedCodeEntityReference> backwards may not result in the correct current position.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="55eb797a-0205-40d2-a797-55b216d1d3bb">Visual Basic Example</link>
        <link xlink:href="29ec4b95-8986-4970-943f-3da3ecb207a2">VBScript Example</link>
        <link xlink:href="0e08af60-f668-4092-8b6a-9e8b6db90448">Visual C++ Example</link>
        <link xlink:href="b29ddb8c-ceb3-4aad-a240-8030462fceba">Visual J++ Example</link>
        <link xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods</link>
        <link xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</link>
        <link xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
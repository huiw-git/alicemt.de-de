---
title: "MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a61a01a7-5b33-4150-9126-21dfa63654cb
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
# MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="44b289b800843f6e6c4367da32cb1835" id="tgt1" class="tgtSentence">Moves to the first, last, next, or previous record in a specified <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object and makes that record the current record.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.</legacyBold>{<legacyBold>MoveFirst</legacyBold> | <legacyBold>MoveLast</legacyBold> | <legacyBold>MoveNext</legacyBold> | <legacyBold>MovePrevious</legacyBold>}</legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e8f1f135466300077e0b586e2052a1e6" id="tgt2" class="tgtSentence">Use the <legacyBold>MoveFirst</legacyBold> method to move the current record position to the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b6171d82ff609e023cf042339e0ae79a" id="tgt3" class="tgtSentence">Use the <legacyBold>MoveLast</legacyBold> method to move the current record position to the last record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="fdfd2d7966ea04ba71e4bea9f85e4ae7" id="tgt4" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c08061a469f8c5c30ffa515def791a6e" id="tgt5" class="tgtSentence">A call to either <legacyBold>MoveFirst</legacyBold> or <legacyBold>MoveLast</legacyBold> when the <legacyBold>Recordset</legacyBold> is empty (both <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> are True) generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="94d9d3b7b57079a78a670992a2460cf8" id="tgt6" class="tgtSentence">Use the <legacyBold>MoveNext</legacyBold> method to move the current record position one record forward (toward the bottom of the <legacyBold>Recordset</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="f7d83e826c327c50fc0be3844029d42e" id="tgt7" class="tgtSentence"> If the last record is the current record and you call the <legacyBold>MoveNext</legacyBold> method, ADO sets the current record to the position after the last record in the <legacyBold>Recordset</legacyBold> (<legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> is <legacyBold>True</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="4697085a8b6f42204605523e9c0413dc" id="tgt8" class="tgtSentence"> An attempt to move forward when the <legacyBold>EOF</legacyBold> property is already <legacyBold>True</legacyBold> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="74b4493e6df8c0b22380734fd7614046" id="tgt9" class="tgtSentence">In ADO 2.5 and later, when the <legacyBold>Recordset</legacyBold> has been filtered or sorted and the data of the current record is changed, calling the <legacyBold>MoveNext</legacyBold> method moves the cursor two records forward from the current record.</caps:sentence>
            <caps:sentence sentenceid="79386649c0ae6cdfc9bf51ee08d26926" id="tgt10" class="tgtSentence"> This is because when the current record is changed, the next record becomes the new current record.</caps:sentence>
            <caps:sentence sentenceid="614ff569c4a005e646e958f8123cc65a" id="tgt11" class="tgtSentence"> Calling <legacyBold>MoveNext</legacyBold> after the change moves the cursor one record forward from the new current record.</caps:sentence>
            <caps:sentence sentenceid="b87f17fbb7ef1400f1aa442b6dfc6983" id="tgt12" class="tgtSentence"> This is different from the behavior in ADO 2.1 and earlier.</caps:sentence>
            <caps:sentence sentenceid="9dfd00323dfa1b2dc3d6f9d167e9c5cc" id="tgt13" class="tgtSentence"> In these earlier versions, changing the data of a current record in the sorted or filtered <legacyBold>Recordset</legacyBold> does not change the position of the current record, and <legacyBold>MoveNext</legacyBold> moves the cursor to the next record immediately after the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0a75b20b17a67ee7be1c00d8632b79bc" id="tgt14" class="tgtSentence">Use the <legacyBold>MovePrevious</legacyBold> method to move the current record position one record backward (toward the top of the <legacyBold>Recordset</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="fdfd2d7966ea04ba71e4bea9f85e4ae7" id="tgt15" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error.</caps:sentence>
            <caps:sentence sentenceid="a15b633e9eca79a8d1d427473775a84e" id="tgt16" class="tgtSentence"> If the first record is the current record and you call the <legacyBold>MovePrevious</legacyBold> method, ADO sets the current record to the position before the first record in the <legacyBold>Recordset</legacyBold> (<legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> is <legacyBold>True</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="4c99003d94608e41b79194d45c6be9df" id="tgt17" class="tgtSentence"> An attempt to move backward when the <legacyBold>BOF</legacyBold> property is already <legacyBold>True</legacyBold> generates an error.</caps:sentence>
            <caps:sentence sentenceid="4a725741b3f51d01f3e4c0ca8b3d075d" id="tgt18" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> object does not support either bookmarks or backward cursor movement, the <legacyBold>MovePrevious</legacyBold> method will generate an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="75d8ec5dd73f930cf0b7dc318f058373" id="tgt19" class="tgtSentence">If the <legacyBold>Recordset</legacyBold> is forward only and you want to support both forward and backward scrolling, you can use the <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">CacheSize</legacyLink> property to create a record cache that will support backward cursor movement through the <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="d2edfef6bf14d6f610c637bab115db9c" id="tgt20" class="tgtSentence"> Because cached records are loaded into memory, you should avoid caching more records than is necessary.</caps:sentence>
            <caps:sentence sentenceid="e5bf2c0e9d58678bf1241673f8be9ea8" id="tgt21" class="tgtSentence"> You can call the <legacyBold>MoveFirst</legacyBold> method in a forward-only <legacyBold>Recordset</legacyBold> object; doing so may cause the provider to re-execute the command that generated the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt22" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="31d3b083-c677-423e-8d26-a212eaeea281">Visual Basic Example</link>
        <link xlink:href="911aa1dd-2786-4f34-992c-bb2fbdabcbdf">VBScript Example</link>
        <link xlink:href="7f8aea7b-9183-4b29-8ac0-a393ed2e8bd5">Visual C++ Example</link>
        <link xlink:href="d2db8a95-3072-4007-a127-44376405a67e">Visual J++ Example</link>
        <link xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move Method</link>
        <link xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</link>
        <link xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Moves to the first, last, next, or previous record in a specified <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object and makes that record the current record.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>recordset</parameterReference>
          <legacyBold>.</legacyBold>{<legacyBold>MoveFirst</legacyBold> | <legacyBold>MoveLast</legacyBold> | <legacyBold>MoveNext</legacyBold> | <legacyBold>MovePrevious</legacyBold>}</legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Use the <legacyBold>MoveFirst</legacyBold> method to move the current record position to the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">Use the <legacyBold>MoveLast</legacyBold> method to move the current record position to the last record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The <legacyBold>Recordset</legacyBold> object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">A call to either <legacyBold>MoveFirst</legacyBold> or <legacyBold>MoveLast</legacyBold> when the <legacyBold>Recordset</legacyBold> is empty (both <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> are True) generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">Use the <legacyBold>MoveNext</legacyBold> method to move the current record position one record forward (toward the bottom of the <legacyBold>Recordset</legacyBold>).</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If the last record is the current record and you call the <legacyBold>MoveNext</legacyBold> method, ADO sets the current record to the position after the last record in the <legacyBold>Recordset</legacyBold> (<legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">EOF</legacyLink> is <legacyBold>True</legacyBold>).</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> An attempt to move forward when the <legacyBold>EOF</legacyBold> property is already <legacyBold>True</legacyBold> generates an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">In ADO 2.5 and later, when the <legacyBold>Recordset</legacyBold> has been filtered or sorted and the data of the current record is changed, calling the <legacyBold>MoveNext</legacyBold> method moves the cursor two records forward from the current record.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> This is because when the current record is changed, the next record becomes the new current record.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Calling <legacyBold>MoveNext</legacyBold> after the change moves the cursor one record forward from the new current record.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> This is different from the behavior in ADO 2.1 and earlier.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> In these earlier versions, changing the data of a current record in the sorted or filtered <legacyBold>Recordset</legacyBold> does not change the position of the current record, and <legacyBold>MoveNext</legacyBold> moves the cursor to the next record immediately after the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">Use the <legacyBold>MovePrevious</legacyBold> method to move the current record position one record backward (toward the top of the <legacyBold>Recordset</legacyBold>).</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The <legacyBold>Recordset</legacyBold> object must support bookmarks or backward cursor movement; otherwise, the method call will generate an error.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> If the first record is the current record and you call the <legacyBold>MovePrevious</legacyBold> method, ADO sets the current record to the position before the first record in the <legacyBold>Recordset</legacyBold> (<legacyLink xlink:href="36c31ab2-f3b6-4281-89b6-db7e04e38fd2">BOF</legacyLink> is <legacyBold>True</legacyBold>).</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> An attempt to move backward when the <legacyBold>BOF</legacyBold> property is already <legacyBold>True</legacyBold> generates an error.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> object does not support either bookmarks or backward cursor movement, the <legacyBold>MovePrevious</legacyBold> method will generate an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">If the <legacyBold>Recordset</legacyBold> is forward only and you want to support both forward and backward scrolling, you can use the <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">CacheSize</legacyLink> property to create a record cache that will support backward cursor movement through the <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink> method.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Because cached records are loaded into memory, you should avoid caching more records than is necessary.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> You can call the <legacyBold>MoveFirst</legacyBold> method in a forward-only <legacyBold>Recordset</legacyBold> object; doing so may cause the provider to re-execute the command that generated the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="31d3b083-c677-423e-8d26-a212eaeea281">Visual Basic Example</link>
        <link xlink:href="911aa1dd-2786-4f34-992c-bb2fbdabcbdf">VBScript Example</link>
        <link xlink:href="7f8aea7b-9183-4b29-8ac0-a393ed2e8bd5">Visual C++ Example</link>
        <link xlink:href="d2db8a95-3072-4007-a127-44376405a67e">Visual J++ Example</link>
        <link xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move Method</link>
        <link xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</link>
        <link xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
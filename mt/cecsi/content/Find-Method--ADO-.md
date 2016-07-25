---
title: "Find Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 55c9810a-d8ca-46c2-a9dc-80e7ee7aa188
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
# Find Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="818417306646dd1403fd8468b1fd3df5" id="tgt1" class="tgtSentence">Searches a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> for the row that satisfies the specified criteria.</caps:sentence>
          <caps:sentence sentenceid="596d9d87a90aef36eb7c571dd456a94e" id="tgt2" class="tgtSentence"> Optionally, the direction of the search, starting row, and offset from the starting row may be specified.</caps:sentence>
          <caps:sentence sentenceid="6ad3488429c8a73626f9d7bbc849524e" id="tgt3" class="tgtSentence"> If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Find</legacyBold>
          <parameterReference>(Criteria, SkipRows, SearchDirection, Start)</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="70c4c79eb47166c6d9b4f3150baa354e" id="tgt4" class="tgtSentence"> <legacyItalic>Criteria</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d7652184b84ae8d4d51a6c3993911079" id="tgt5" class="tgtSentence">A <legacyBold>String</legacyBold> value that contains a statement specifying the column name, comparison operator, and value to use in the search.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="221f96f094dedb86e84ddf8b3271f5b0" id="tgt6" class="tgtSentence"> <legacyItalic>SkipRows</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="9a157059e69cf7f5c9d4f555eda7e20a" id="tgt7" class="tgtSentence">Optional<legacyItalic>. </legacyItalic>A <legacyBold>Long</legacyBold> value, whose default value is zero, that specifies the row offset from the current row or <legacyItalic>Start </legacyItalic>bookmark to begin the search. By default, the search will start on the current row.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e5d624141fa61ef6a826bc0328257df0" id="tgt8" class="tgtSentence"> <legacyItalic>SearchDirection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d6f44e127157bf13cb095b98c048f3a0" id="tgt9" class="tgtSentence">Optional<legacyItalic>. </legacyItalic>A <legacyLink xlink:href="81272ae3-2165-4f4e-adfe-9ede0368cb17">SearchDirectionEnum</legacyLink> value that specifies whether the search should begin on the current row or the next available row in the direction of the search. An unsuccessful search stops at the end of the <legacyBold>Recordset</legacyBold> if the value is <legacyBold>adSearchForward</legacyBold>. An unsuccessful search stops at the start of the <legacyBold>Recordset</legacyBold> if the value is <legacyBold>adSearchBackward</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="922ed5a49d50fca828b4bba43d2f705e" id="tgt10" class="tgtSentence"> <legacyItalic>Start</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt11" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="1479a071880a2265ee540e5f899b5310" id="tgt12" class="tgtSentence"> A <legacyBold>Variant</legacyBold> bookmark that functions as the starting position for the search.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4a0292c8d2183132e0f95c27886708cf" id="tgt13" class="tgtSentence">Only a single-column name may be specified in <legacyItalic>criteria</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="fcb682b5d35dcfdde0d987d0794c063b" id="tgt14" class="tgtSentence"> This method does not support multi-column searches.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b89659f50abe5a1de4af8eda71971900" id="tgt15" class="tgtSentence">The comparison operator in <legacyItalic>Criteria</legacyItalic> may be "<legacyBold>&gt;</legacyBold>" (greater than), "<legacyBold>&lt;</legacyBold>" (less than), "=" (equal), "&gt;=" (greater than or equal), "&lt;=" (less than or equal), "&lt;&gt;" (not equal), or "like" (pattern matching).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="90060cd1c0be8d5bc51c7a1c55b9be7d" id="tgt16" class="tgtSentence">The value in <legacyItalic>Criteria</legacyItalic> may be a string, floating-point number, or date.</caps:sentence>
            <caps:sentence sentenceid="dbf5216b1f0dbeecc5e4dcb2d3136edc" id="tgt17" class="tgtSentence"> String values are delimited with single quotes or "#" (number sign) marks (for example, "state = 'WA'" or "state = #WA#").</caps:sentence>
            <caps:sentence sentenceid="eb47660444f80cceb50be5df8cc295b2" id="tgt18" class="tgtSentence"> Date values are delimited with "#" (number sign) marks (for example, "start_date &gt; #7/22/97#").</caps:sentence>
            <caps:sentence sentenceid="e16b33a5335c0fd89737c7637541290b" id="tgt19" class="tgtSentence"> These values can contain hours, minutes, and seconds to indicate time stamps, but should not contain milliseconds or errors will occur.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="784d61198b66f34701851ece7f2900b5" id="tgt20" class="tgtSentence">If the comparison operator is "like", the string value may contain an asterisk (*) to find one or more occurrences of any character or substring.</caps:sentence>
            <caps:sentence sentenceid="f368dbfb28ddbc5b723265343fd93cdd" id="tgt21" class="tgtSentence"> For example, "state like 'M*'" matches Maine and Massachusetts.</caps:sentence>
            <caps:sentence sentenceid="5318841a1848b5bd416d44f70ea55770" id="tgt22" class="tgtSentence"> You can also use leading and trailing asterisks to find a substring contained within the values.</caps:sentence>
            <caps:sentence sentenceid="3d7489f29b82cc819812b22e8aceb8ce" id="tgt23" class="tgtSentence"> For example, "state like '*as*'" matches Alaska, Arkansas, and Massachusetts.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bb3afff2d8f145d3f27180e5e6b77aa4" id="tgt24" class="tgtSentence">Asterisks can be used only at the end of a criteria string, or at both the beginning and end of a criteria string, as shown above.</caps:sentence>
            <caps:sentence sentenceid="86303dd2b1a30c8c8f362fbf45521699" id="tgt25" class="tgtSentence"> You cannot use the asterisk as a leading wildcard ('*str'), or as an embedded wildcard ('s*r').</caps:sentence>
            <caps:sentence sentenceid="e1cd53259983321ab04abc08895a8830" id="tgt26" class="tgtSentence"> This will cause an error.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="6c5b6901c0ebf8b6a634c36db80c518f" id="tgt27" class="tgtSentence">An error will occur if a current row position is not set before calling <legacyBold>Find</legacyBold>.</caps:sentence>
              <caps:sentence sentenceid="3187dbdba1d87460588f6fbeae648868" id="tgt28" class="tgtSentence"> Any method that sets row position, such as <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink>, should be called before calling <legacyBold>Find</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="846ac4663dcb434e117afb502b668c58" id="tgt29" class="tgtSentence">If you call the <legacyBold>Find</legacyBold> method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything.</caps:sentence>
              <caps:sentence sentenceid="422232fd632b616c59b19b7e2ce21ca5" id="tgt30" class="tgtSentence"> You need to call the <legacyBold>MoveFirst</legacyBold> method to set the current position/cursor to the beginning of the recordset.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt31" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bbf27dcc-9815-4e2f-8ea8-b8c9fe6dedd6">Visual Basic Example</link>
        <link xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index Property</link>
        <link xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize Property — Dynamic (ADO)</link>
        <link xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Searches a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> for the row that satisfies the specified criteria.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Optionally, the direction of the search, starting row, and offset from the starting row may be specified.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Find</legacyBold>
          <parameterReference>(Criteria, SkipRows, SearchDirection, Start)</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>Criteria</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">A <legacyBold>String</legacyBold> value that contains a statement specifying the column name, comparison operator, and value to use in the search.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>SkipRows</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Optional<legacyItalic>. </legacyItalic>A <legacyBold>Long</legacyBold> value, whose default value is zero, that specifies the row offset from the current row or <legacyItalic>Start </legacyItalic>bookmark to begin the search. By default, the search will start on the current row.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>SearchDirection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">Optional<legacyItalic>. </legacyItalic>A <legacyLink xlink:href="81272ae3-2165-4f4e-adfe-9ede0368cb17">SearchDirectionEnum</legacyLink> value that specifies whether the search should begin on the current row or the next available row in the direction of the search. An unsuccessful search stops at the end of the <legacyBold>Recordset</legacyBold> if the value is <legacyBold>adSearchForward</legacyBold>. An unsuccessful search stops at the start of the <legacyBold>Recordset</legacyBold> if the value is <legacyBold>adSearchBackward</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>Start</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> A <legacyBold>Variant</legacyBold> bookmark that functions as the starting position for the search.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">Only a single-column name may be specified in <legacyItalic>criteria</legacyItalic>.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> This method does not support multi-column searches.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">The comparison operator in <legacyItalic>Criteria</legacyItalic> may be "<legacyBold>&gt;</legacyBold>" (greater than), "<legacyBold>&lt;</legacyBold>" (less than), "=" (equal), "&gt;=" (greater than or equal), "&lt;=" (less than or equal), "&lt;&gt;" (not equal), or "like" (pattern matching).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">The value in <legacyItalic>Criteria</legacyItalic> may be a string, floating-point number, or date.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> String values are delimited with single quotes or "#" (number sign) marks (for example, "state = 'WA'" or "state = #WA#").</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Date values are delimited with "#" (number sign) marks (for example, "start_date &gt; #7/22/97#").</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> These values can contain hours, minutes, and seconds to indicate time stamps, but should not contain milliseconds or errors will occur.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">If the comparison operator is "like", the string value may contain an asterisk (*) to find one or more occurrences of any character or substring.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> For example, "state like 'M*'" matches Maine and Massachusetts.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> You can also use leading and trailing asterisks to find a substring contained within the values.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> For example, "state like '*as*'" matches Alaska, Arkansas, and Massachusetts.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">Asterisks can be used only at the end of a criteria string, or at both the beginning and end of a criteria string, as shown above.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> You cannot use the asterisk as a leading wildcard ('*str'), or as an embedded wildcard ('s*r').</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> This will cause an error.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src27" class="srcSentence">An error will occur if a current row position is not set before calling <legacyBold>Find</legacyBold>.</caps:sentence>
              <caps:sentence id="src28" class="srcSentence"> Any method that sets row position, such as <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst</legacyLink>, should be called before calling <legacyBold>Find</legacyBold>.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src29" class="srcSentence">If you call the <legacyBold>Find</legacyBold> method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything.</caps:sentence>
              <caps:sentence id="src30" class="srcSentence"> You need to call the <legacyBold>MoveFirst</legacyBold> method to set the current position/cursor to the beginning of the recordset.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src31" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bbf27dcc-9815-4e2f-8ea8-b8c9fe6dedd6">Visual Basic Example</link>
        <link xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index Property</link>
        <link xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize Property — Dynamic (ADO)</link>
        <link xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
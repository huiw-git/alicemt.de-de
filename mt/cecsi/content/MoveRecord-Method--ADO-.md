---
title: "MoveRecord Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6d2807b0-b861-4583-bcaf-fb0b82e0f2d0
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
# MoveRecord Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d3418868964b90f6777531cac0e86f1b" id="tgt1" class="tgtSentence">Moves the entity represented by a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> to another location.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Record</parameterReference>.<legacyBold>MoveRecord (</legacyBold><parameterReference>Source</parameterReference><legacyBold>, </legacyBold><parameterReference>Destination</parameterReference><legacyBold>, </legacyBold><parameterReference>UserName</parameterReference><legacyBold>, </legacyBold><parameterReference>Password</parameterReference><legacyBold>, </legacyBold><parameterReference>Options</parameterReference><legacyBold>, </legacyBold><parameterReference>Async</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="b86002c905ed82eb6c9ab27bfdb86afd" id="tgt2" class="tgtSentence"> <legacyItalic>Source</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt3" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="57ab9772939fd1024dc3b9c3b4a72130" id="tgt4" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains a URL identifying the <legacyBold>Record</legacyBold> to be moved.</caps:sentence>
                <caps:sentence sentenceid="6bf22e9a8b1cd89b269d48c7830194a1" id="tgt5" class="tgtSentence"> If <legacyItalic>Source </legacyItalic>is omitted or specifies an empty string, the object represented by this <legacyBold>Record</legacyBold> is moved.</caps:sentence>
                <caps:sentence sentenceid="92fc55fef3378b017145585bd4a80a2e" id="tgt6" class="tgtSentence"> For example, if the <legacyBold>Record</legacyBold> represents a file, the contents of the file are moved to the location specified by <legacyItalic>Destination</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="004d43c096763731c9a280248b72895c" id="tgt7" class="tgtSentence"> <legacyItalic>Destination</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="1bc40a340537cee092a3b59cb49780fd" id="tgt9" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains a URL specifying the location where <legacyItalic>Source</legacyItalic> will be moved.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="230b2555855f31ab54ada86334bb7da2" id="tgt10" class="tgtSentence"> <legacyItalic>UserName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt11" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="feb7c60176a2ad48990f805bd0ee8ea3" id="tgt12" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains the user ID that, if needed, authorizes access to <legacyItalic>Destination</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d83fe9057df78601fffb657095e0114f" id="tgt13" class="tgtSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt14" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="a9d01054c788afb35e138a873679adc1" id="tgt15" class="tgtSentence"> A <legacyBold>String</legacyBold> that contains the password that, if needed, verifies <legacyItalic>UserName</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt16" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt17" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="f2576463de71446e8faed2cd1c6a3d02" id="tgt18" class="tgtSentence"> A <legacyLink xlink:href="f53c2ce4-1021-4a45-92b8-775e8bebad99">MoveRecordOptionsEnum</legacyLink> value whose default value is <legacyBold>adMoveUnspecified</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="563bbfa209a2d8fcf4551a667bec9a36" id="tgt19" class="tgtSentence"> Specifies the behavior of this method.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="4f96059e85234f10011f72092bee6b67" id="tgt20" class="tgtSentence"> <legacyItalic>Async</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt21" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="3b7f8c47c765af094394e6455c31b6ca" id="tgt22" class="tgtSentence"> A <legacyBold>Boolean</legacyBold> value that, when <legacyBold>True</legacyBold>, specifies this operation should be asynchronous.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="0ff1bb4544124fbe06745ad7ef5c4f8e" id="tgt23" class="tgtSentence">A <legacyBold>String</legacyBold> value.</caps:sentence>
            <caps:sentence sentenceid="aa1100ef07a706408b20375941b8c6d6" id="tgt24" class="tgtSentence"> Typically, the value of <legacyItalic>Destination</legacyItalic> is returned.</caps:sentence>
            <caps:sentence sentenceid="ba90443fac67a179ba91323ae8b4fb20" id="tgt25" class="tgtSentence"> However, the exact value returned is provider-dependent.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="dd1a5589e8502518b3f410088c740dbf" id="tgt26" class="tgtSentence">The values of <legacyItalic>Source</legacyItalic> and <legacyItalic>Destination</legacyItalic> must not be identical; otherwise, a run-time error occurs.</caps:sentence>
            <caps:sentence sentenceid="550d7230d5a1998624d13415c32ddd95" id="tgt27" class="tgtSentence"> At least the server, path, and resource names must differ.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="578001625c5a164978e474ea2365c4bb" id="tgt28" class="tgtSentence">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by <legacyItalic>Options</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="daa2f58ec27d594dc64b0237b33d29b3" id="tgt29" class="tgtSentence"> This method fails if <legacyItalic>Destination</legacyItalic> identifies an existing object (for example, a file or directory), unless <legacyBold>adMoveOverWrite</legacyBold> is specified.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="7ae56ca660503d975e88913a4b95e1f6" id="tgt30" class="tgtSentence">Use the <legacyBold>adMoveOverWrite</legacyBold> option judiciously.</caps:sentence>
              <caps:sentence sentenceid="467763c40a8fe6fbe698c8a62edafdab" id="tgt31" class="tgtSentence"> For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="2077b394c4459f1cb382130ebd120ede" id="tgt32" class="tgtSentence">Certain attributes of the <legacyBold>Record</legacyBold> object, such as the <legacyLink xlink:href="65120ce6-3900-4cd4-b322-3b9816d74737">ParentURL</legacyLink> property, will not be updated after this operation completes.</caps:sentence>
            <caps:sentence sentenceid="3117c6ae6b4551911ba77ab413b4ea16" id="tgt33" class="tgtSentence"> Refresh the <legacyBold>Record</legacyBold> object's properties by closing the <legacyBold>Record</legacyBold>, then re-opening it with the URL of the location where the file or directory was moved.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b8d6affa2eac083ae9c13609a7d9cdad" id="tgt34" class="tgtSentence">If this <legacyBold>Record</legacyBold> was obtained from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, the new location of the moved file or directory will not be reflected immediately in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="3feae0f6053f731a01da6223af215355" id="tgt35" class="tgtSentence"> Refresh the <legacyBold>Recordset</legacyBold> by closing and re-opening it.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt36" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt37" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt38" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move Method</link>
        <link xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods</link>
        <link xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Moves the entity represented by a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> to another location.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Record</parameterReference>.<legacyBold>MoveRecord (</legacyBold><parameterReference>Source</parameterReference><legacyBold>, </legacyBold><parameterReference>Destination</parameterReference><legacyBold>, </legacyBold><parameterReference>UserName</parameterReference><legacyBold>, </legacyBold><parameterReference>Password</parameterReference><legacyBold>, </legacyBold><parameterReference>Options</parameterReference><legacyBold>, </legacyBold><parameterReference>Async</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <legacyItalic>Source</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains a URL identifying the <legacyBold>Record</legacyBold> to be moved.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> If <legacyItalic>Source </legacyItalic>is omitted or specifies an empty string, the object represented by this <legacyBold>Record</legacyBold> is moved.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> For example, if the <legacyBold>Record</legacyBold> represents a file, the contents of the file are moved to the location specified by <legacyItalic>Destination</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>Destination</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains a URL specifying the location where <legacyItalic>Source</legacyItalic> will be moved.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <legacyItalic>UserName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains the user ID that, if needed, authorizes access to <legacyItalic>Destination</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src13" class="srcSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src14" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> A <legacyBold>String</legacyBold> that contains the password that, if needed, verifies <legacyItalic>UserName</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src16" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src17" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> A <legacyLink xlink:href="f53c2ce4-1021-4a45-92b8-775e8bebad99">MoveRecordOptionsEnum</legacyLink> value whose default value is <legacyBold>adMoveUnspecified</legacyBold>.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> Specifies the behavior of this method.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src20" class="srcSentence"> <legacyItalic>Async</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src21" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> A <legacyBold>Boolean</legacyBold> value that, when <legacyBold>True</legacyBold>, specifies this operation should be asynchronous.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src23" class="srcSentence">A <legacyBold>String</legacyBold> value.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> Typically, the value of <legacyItalic>Destination</legacyItalic> is returned.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> However, the exact value returned is provider-dependent.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src26" class="srcSentence">The values of <legacyItalic>Source</legacyItalic> and <legacyItalic>Destination</legacyItalic> must not be identical; otherwise, a run-time error occurs.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> At least the server, path, and resource names must differ.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by <legacyItalic>Options</legacyItalic>.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> This method fails if <legacyItalic>Destination</legacyItalic> identifies an existing object (for example, a file or directory), unless <legacyBold>adMoveOverWrite</legacyBold> is specified.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src30" class="srcSentence">Use the <legacyBold>adMoveOverWrite</legacyBold> option judiciously.</caps:sentence>
              <caps:sentence id="src31" class="srcSentence"> For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src32" class="srcSentence">Certain attributes of the <legacyBold>Record</legacyBold> object, such as the <legacyLink xlink:href="65120ce6-3900-4cd4-b322-3b9816d74737">ParentURL</legacyLink> property, will not be updated after this operation completes.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> Refresh the <legacyBold>Record</legacyBold> object's properties by closing the <legacyBold>Record</legacyBold>, then re-opening it with the URL of the location where the file or directory was moved.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src34" class="srcSentence">If this <legacyBold>Record</legacyBold> was obtained from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, the new location of the moved file or directory will not be reflected immediately in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> Refresh the <legacyBold>Recordset</legacyBold> by closing and re-opening it.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src36" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src37" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src38" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move Method</link>
        <link xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods</link>
        <link xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
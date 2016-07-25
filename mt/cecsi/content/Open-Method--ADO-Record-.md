---
title: "Open Method (ADO Record)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ab79a623-88a9-40b6-a017-a658bf19b778
caps.latest.revision: 14
caps.handback.revision: 14
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
# Open Method (ADO Record)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ee37e1a15b585785b697ad43625d92e9" id="tgt1" class="tgtSentence">Opens an existing <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, or creates a new item represented by the <legacyBold>Record</legacyBold>, such as a file or directory.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Open </legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>ActiveConnection</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Mode</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>CreateOptions</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Options</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>UserName</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Password</parameterReference>
        </legacySyntax>
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
                <caps:sentence sentenceid="cbb5b3ce4142041464da4ca8566805e5" id="tgt4" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> that may represent the URL of the entity to be represented by this <legacyBold>Record</legacyBold> object, a <legacyBold>Command</legacyBold>, an open <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> or another <legacyBold>Record</legacyBold> object, a string that contains an SQL SELECT statement or a table name.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="b998383d7912d34117ef4638f8034b42" id="tgt5" class="tgtSentence"> <legacyItalic>ActiveConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt6" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="7a787929a36bfa250ebf09e2046b43a7" id="tgt7" class="tgtSentence"> A <legacyBold>Variant</legacyBold> that represents the connect string or open <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a34287bbfa1f581118264867ed0b3373" id="tgt8" class="tgtSentence"> <legacyItalic>Mode</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt9" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="aca336f430489124702edf39bf7368fa" id="tgt10" class="tgtSentence"> A <legacyLink xlink:href="3792c294-5161-4538-a908-22a5fc50b85f">ConnectModeEnum</legacyLink> value that specifies the access mode for the resultant <legacyBold>Record</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="85e1927a94753c75b24ec89ac05ac5b9" id="tgt11" class="tgtSentence"> Default value is <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="445c5ecbb1647dc258bdc3f91a9d57dc" id="tgt12" class="tgtSentence"> <legacyItalic>CreateOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt13" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="fd8d1c9f878866c221478c24e4915389" id="tgt14" class="tgtSentence"> A <legacyLink xlink:href="6d746670-0850-4065-9cd4-168dea1d3ea9">RecordCreateOptionsEnum</legacyLink> value that specifies whether an existing file or directory should be opened, or a new file or directory should be created.</caps:sentence>
                <caps:sentence sentenceid="64ad5c2560b06d00339c1906f19b1720" id="tgt15" class="tgtSentence"> Default value is <legacyBold>adFailIfNotExists</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="d75bce11e77f2aac24b93c3a1694effa" id="tgt16" class="tgtSentence"> If set to the default value, the access mode is obtained from the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property.</caps:sentence>
                <caps:sentence sentenceid="cff0956481bda2d391377d92d5ed363d" id="tgt17" class="tgtSentence"> This parameter is ignored when the <legacyItalic>Source</legacyItalic> parameter does not contain a URL.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="abeb0f120929e9691849f837060ffe89" id="tgt18" class="tgtSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt19" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="35b28038460208699efc140e0be107d0" id="tgt20" class="tgtSentence"> A <legacyLink xlink:href="9028aba4-90fc-4dfc-88e4-fa8a7b6fedee">RecordOpenOptionsEnum</legacyLink> value that specifies options for opening the <legacyBold>Record</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="0de671e2389e9461982bf443ecefe048" id="tgt21" class="tgtSentence"> Default value is <legacyBold>adOpenRecordUnspecified</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="2fe35eb5cca11ed1387f2becd4b19dd4" id="tgt22" class="tgtSentence"> These values can be combined.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="230b2555855f31ab54ada86334bb7da2" id="tgt23" class="tgtSentence"> <legacyItalic>UserName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt24" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="ba50ff08b2f6b95182fe822deb7deec1" id="tgt25" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains the user ID that, if it is required, authorizes access to <legacyItalic>Source</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d83fe9057df78601fffb657095e0114f" id="tgt26" class="tgtSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt27" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="023355c94a701e3742f1075fa514db6c" id="tgt28" class="tgtSentence"> A <legacyBold>String</legacyBold> value that contains the password that, if it is required, verifies <legacyItalic>UserName</legacyItalic>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="2abeea2317527e23de8986e58a746ce5" id="tgt29" class="tgtSentence">
              <legacyItalic>Source</legacyItalic> may be:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1fb3acf70063860b86f2b2354f25763f" id="tgt30" class="tgtSentence">A URL.</caps:sentence>
                <caps:sentence sentenceid="dd9cc045e00aa07fced805bcb6a35695" id="tgt31" class="tgtSentence"> If the protocol for the URL is http, the Internet Provider will be invoked by default.</caps:sentence>
                <caps:sentence sentenceid="b4b5805204e7ef5b36b11ef3a8fc7c97" id="tgt32" class="tgtSentence"> If the URL points to a node that contains an executable script (such as an .ASP page), a <legacyBold>Record</legacyBold> that contains the source instead of the executed contents is opened by default.</caps:sentence>
                <caps:sentence sentenceid="6a742779f965a029e017a25bd7e22b0c" id="tgt33" class="tgtSentence"> Use the <legacyItalic>Options</legacyItalic> argument to modify this behavior.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="78a26f3cbc66ace93a2d22c8d3907573" id="tgt34" class="tgtSentence">A <legacyBold>Record</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="20bc014e765600a374bd77500326bf07" id="tgt35" class="tgtSentence"> A <legacyBold>Record</legacyBold> object opened from another <legacyBold>Record</legacyBold> will clone the original <legacyBold>Record</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ff8ccbb47e25e28bc7fa388cb36623d7" id="tgt36" class="tgtSentence">A <legacyBold>Command</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="5127707bb94e8dc875dacaa6c3120c3d" id="tgt37" class="tgtSentence"> The opened <legacyBold>Record</legacyBold> object represents the single row returned by executing the <legacyBold>Command</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="7a119d401f879e16268331c80ced0bc2" id="tgt38" class="tgtSentence"> If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1c3bbb748cbef711e21666e6d0a21fe6" id="tgt39" class="tgtSentence">An SQL SELECT statement.</caps:sentence>
                <caps:sentence sentenceid="052677c2f7c2ceb0dc9c62d9c0fb56f0" id="tgt40" class="tgtSentence"> The opened <legacyBold>Record</legacyBold> object represents the single row returned by executing the contents of the string.</caps:sentence>
                <caps:sentence sentenceid="7a119d401f879e16268331c80ced0bc2" id="tgt41" class="tgtSentence"> If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8b9752f2715b03c6b6cb008dc4af4f99" id="tgt42" class="tgtSentence">A table name.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="3e9b3f2569b9281ddc76d542b538955a" id="tgt43" class="tgtSentence">If the <legacyBold>Record</legacyBold> object represents an entity that cannot be accessed with a URL (for example, a row of a <legacyBold>Recordset</legacyBold> derived from a database), the values of both the <legacyLink xlink:href="65120ce6-3900-4cd4-b322-3b9816d74737">ParentURL</legacyLink> property and the field accessed with the <legacyBold>adRecordURL</legacyBold> constant are null.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt44" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt45" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt46" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Opens an existing <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, or creates a new item represented by the <legacyBold>Record</legacyBold>, such as a file or directory.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Open </legacyBold>
          <parameterReference>Source</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>ActiveConnection</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Mode</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>CreateOptions</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Options</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>UserName</parameterReference>
          <legacyBold>, </legacyBold>
          <parameterReference>Password</parameterReference>
        </legacySyntax>
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
                <caps:sentence id="src4" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> that may represent the URL of the entity to be represented by this <legacyBold>Record</legacyBold> object, a <legacyBold>Command</legacyBold>, an open <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> or another <legacyBold>Record</legacyBold> object, a string that contains an SQL SELECT statement or a table name.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>ActiveConnection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> A <legacyBold>Variant</legacyBold> that represents the connect string or open <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>Mode</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> A <legacyLink xlink:href="3792c294-5161-4538-a908-22a5fc50b85f">ConnectModeEnum</legacyLink> value that specifies the access mode for the resultant <legacyBold>Record</legacyBold> object.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> Default value is <legacyBold>adModeUnknown</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src12" class="srcSentence"> <legacyItalic>CreateOptions</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src13" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> A <legacyLink xlink:href="6d746670-0850-4065-9cd4-168dea1d3ea9">RecordCreateOptionsEnum</legacyLink> value that specifies whether an existing file or directory should be opened, or a new file or directory should be created.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> Default value is <legacyBold>adFailIfNotExists</legacyBold>.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> If set to the default value, the access mode is obtained from the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> This parameter is ignored when the <legacyItalic>Source</legacyItalic> parameter does not contain a URL.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src18" class="srcSentence"> <legacyItalic>Options</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src19" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> A <legacyLink xlink:href="9028aba4-90fc-4dfc-88e4-fa8a7b6fedee">RecordOpenOptionsEnum</legacyLink> value that specifies options for opening the <legacyBold>Record</legacyBold>.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> Default value is <legacyBold>adOpenRecordUnspecified</legacyBold>.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> These values can be combined.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src23" class="srcSentence"> <legacyItalic>UserName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src24" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains the user ID that, if it is required, authorizes access to <legacyItalic>Source</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src26" class="srcSentence"> <legacyItalic>Password</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src27" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src28" class="srcSentence"> A <legacyBold>String</legacyBold> value that contains the password that, if it is required, verifies <legacyItalic>UserName</legacyItalic>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">
              <legacyItalic>Source</legacyItalic> may be:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">A URL.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> If the protocol for the URL is http, the Internet Provider will be invoked by default.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> If the URL points to a node that contains an executable script (such as an .ASP page), a <legacyBold>Record</legacyBold> that contains the source instead of the executed contents is opened by default.</caps:sentence>
                <caps:sentence id="src33" class="srcSentence"> Use the <legacyItalic>Options</legacyItalic> argument to modify this behavior.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">A <legacyBold>Record</legacyBold> object.</caps:sentence>
                <caps:sentence id="src35" class="srcSentence"> A <legacyBold>Record</legacyBold> object opened from another <legacyBold>Record</legacyBold> will clone the original <legacyBold>Record</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">A <legacyBold>Command</legacyBold> object.</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> The opened <legacyBold>Record</legacyBold> object represents the single row returned by executing the <legacyBold>Command</legacyBold>.</caps:sentence>
                <caps:sentence id="src38" class="srcSentence"> If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src39" class="srcSentence">An SQL SELECT statement.</caps:sentence>
                <caps:sentence id="src40" class="srcSentence"> The opened <legacyBold>Record</legacyBold> object represents the single row returned by executing the contents of the string.</caps:sentence>
                <caps:sentence id="src41" class="srcSentence"> If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src42" class="srcSentence">A table name.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src43" class="srcSentence">If the <legacyBold>Record</legacyBold> object represents an entity that cannot be accessed with a URL (for example, a row of a <legacyBold>Recordset</legacyBold> derived from a database), the values of both the <legacyLink xlink:href="65120ce6-3900-4cd4-b322-3b9816d74737">ParentURL</legacyLink> property and the field accessed with the <legacyBold>adRecordURL</legacyBold> constant are null.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src44" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src45" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src46" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
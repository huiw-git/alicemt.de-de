---
title: "ParentURL Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 65120ce6-3900-4cd4-b322-3b9816d74737
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
# ParentURL Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="61e4bdeb9d30d33bd416c6311b5208fd" id="tgt1" class="tgtSentence">Indicates an absolute URL string that points to the parent <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> of the current <legacyBold>Record</legacyBold> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="62ab56e2a6b4ce8c4ba2f72de92a2183" id="tgt3" class="tgtSentence">Returns a <legacyBold>String</legacyBold> value that indicates the URL of the parent <legacyBold>Record</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="55ba8e83baf9e49d9431acd85242d5f4" id="tgt4" class="tgtSentence">The <legacyBold>ParentURL</legacyBold> property depends on the source used to open the <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="66f587067d6c7860a065b49d6d33c8c2" id="tgt5" class="tgtSentence"> For example, the <legacyBold>Record</legacyBold> can be opened with a source that contains a relative path name of a directory referenced by the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6228bb27f9bcd3d176737d3237c24f93" id="tgt6" class="tgtSentence">Suppose "second" is a folder contained under "first".</caps:sentence>
            <caps:sentence sentenceid="e0d6d333c116f698b6a06a2a41a89094" id="tgt7" class="tgtSentence"> Open the <legacyBold>Record</legacyBold> object by using the following syntax:</caps:sentence>
          </para>
          <code>record.ActiveConnection = "http://first"
record.Open "second"</code>
          <para>
            <caps:sentence sentenceid="a5a220aaacad38cb20bef4c91d684e52" id="tgt8" class="tgtSentence">Now, the value of <codeInline>the </codeInline><legacyBold>ParentURL</legacyBold> property is <codeInline>"http://first"</codeInline>, the same as <legacyBold>ActiveConnection</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b857efa020543b15411fbfef0e39cb48" id="tgt9" class="tgtSentence">The source can also be an absolute URL such as, <codeInline>"http://first/second"</codeInline>.</caps:sentence>
            <caps:sentence sentenceid="91642da4f4c40aaad60ebb30983a5c92" id="tgt10" class="tgtSentence"> The <legacyBold>ParentURL</legacyBold> property is then <codeInline>"http://first"</codeInline>, the level above <codeInline>"second"</codeInline>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a8015397cc4885b7090be1c8da4a1d91" id="tgt11" class="tgtSentence">This property may be a null value if:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="72b8e39504a7e0e1ff5a6bb43d65c095" id="tgt12" class="tgtSentence">There is no parent for the current object; for example, if the <legacyBold>Record</legacyBold> object represents the root of a directory.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a280c0e7df71c9600e211260a875799f" id="tgt13" class="tgtSentence">The <legacyBold>Record</legacyBold> object represents an entity that cannot be specified with a URL.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="8367eab0183b970bbe7f7545cd0002bb" id="tgt14" class="tgtSentence">This property is read-only.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="b7c75807a8157a18f68d5ce180454ab9" id="tgt15" class="tgtSentence">This property is only supported by document source providers, such as the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="91d31f2948dddee19c829ee6ef8a5849" id="tgt16" class="tgtSentence"> For more information, see <legacyLink xlink:href="77f95e0a-0cf2-411a-a792-593f77330fbd">Records and Provider-Supplied Fields</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt17" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt18" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="0c825cf3b3a64bab164a8f1e388f2a01" id="tgt19" class="tgtSentence">If the current record contains a data record from an ADO <legacyBold>Recordset</legacyBold>, accessing the <legacyBold>ParentURL</legacyBold> property causes a run-time error, indicating that no URL is possible.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt20" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates an absolute URL string that points to the parent <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> of the current <legacyBold>Record</legacyBold> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyBold>String</legacyBold> value that indicates the URL of the parent <legacyBold>Record</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <legacyBold>ParentURL</legacyBold> property depends on the source used to open the <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> For example, the <legacyBold>Record</legacyBold> can be opened with a source that contains a relative path name of a directory referenced by the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">Suppose "second" is a folder contained under "first".</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Open the <legacyBold>Record</legacyBold> object by using the following syntax:</caps:sentence>
          </para>
          <code>record.ActiveConnection = "http://first"
record.Open "second"</code>
          <para>
            <caps:sentence id="src8" class="srcSentence">Now, the value of <codeInline>the </codeInline><legacyBold>ParentURL</legacyBold> property is <codeInline>"http://first"</codeInline>, the same as <legacyBold>ActiveConnection</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The source can also be an absolute URL such as, <codeInline>"http://first/second"</codeInline>.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The <legacyBold>ParentURL</legacyBold> property is then <codeInline>"http://first"</codeInline>, the level above <codeInline>"second"</codeInline>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">This property may be a null value if:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">There is no parent for the current object; for example, if the <legacyBold>Record</legacyBold> object represents the root of a directory.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">The <legacyBold>Record</legacyBold> object represents an entity that cannot be specified with a URL.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src14" class="srcSentence">This property is read-only.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src15" class="srcSentence">This property is only supported by document source providers, such as the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src16" class="srcSentence"> For more information, see <legacyLink xlink:href="77f95e0a-0cf2-411a-a792-593f77330fbd">Records and Provider-Supplied Fields</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src17" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
              <caps:sentence id="src18" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
            </para>
          </alert>
          <alert class="note">
            <para>
              <caps:sentence id="src19" class="srcSentence">If the current record contains a data record from an ADO <legacyBold>Recordset</legacyBold>, accessing the <legacyBold>ParentURL</legacyBold> property causes a run-time error, indicating that no URL is possible.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
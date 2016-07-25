---
title: "Using ADO for Internet Publishing"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d399fce4-b70b-418f-8110-3deb3448863c
caps.latest.revision: 9
caps.handback.revision: 9
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
# Using ADO for Internet Publishing
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f260b2dc62308e7e558ac94dbbd253ed" id="tgt1" class="tgtSentence">       <legacyLink xlink:href="4869aafa-7401-4ce1-93ce-45406a60274f">The OLE DB Provider for Internet Publishing</legacyLink> shows a specific example of accessing heterogeneous data with ADO.</caps:sentence>
          <caps:sentence sentenceid="ed105df24156b2eaf8d3f174a55d794f" id="tgt2" class="tgtSentence"> Although the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an e-mail store.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="45a82579528dcdc6535fdcb693a36170" id="tgt3" class="tgtSentence">URLs</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8b7c7df3e6357e92525e6c034c1c3b29" id="tgt4" class="tgtSentence">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories.</caps:sentence>
            <caps:sentence sentenceid="d13ae282d27034b7c407ce31b07f1b94" id="tgt5" class="tgtSentence"> You can use URLs with the existing <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> and <legacyBold>Recordset</legacyBold> objects and with the <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c76170fc178f01171b048258d7aa55d8" id="tgt6" class="tgtSentence">For more information about how to use URLs, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="dcb43e8b340ce6e241e4b1b220866ed9" id="tgt7" class="tgtSentence">Record Fields</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c22e104f2c43a645ef7cf2fe1c66349c" id="tgt8" class="tgtSentence">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or <legacyBold>Record</legacyBold>, can have a different set of columns, or <legacyBold>Fields</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="aabf8bed0e139451dbf35fc20d708216" id="tgt9" class="tgtSentence"> For homogeneous data, each row has the same set of columns.</caps:sentence>
            <caps:sentence sentenceid="74a083cf65fb967ad06f635dc7772665" id="tgt10" class="tgtSentence"> For more information about the fields specific to the Internet Publishing Provider, see <legacyLink xlink:href="77f95e0a-0cf2-411a-a792-593f77330fbd">Records and Provider-Supplied Extra Fields</legacyLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="5ebb3692887d93bd27925a25ed0594fc" id="tgt11" class="tgtSentence">Appending New Fields</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9dad1751cc478107a050e52afa0a3073" id="tgt12" class="tgtSentence">Several ADO objects have been enhanced to work together with <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e321ff7e11b2f2cbd1c460ca49366179" id="tgt13" class="tgtSentence">The <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method, which creates and adds a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object to the collection, can also specify the value of the <legacyBold>Field</legacyBold>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c8bc20959c275364e27840b38886da64" id="tgt14" class="tgtSentence">The <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method finalizes the addition or deletion of fields to the collection.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="903d12699f361f2ec8214d979292fe86" id="tgt15" class="tgtSentence">As a shortcut and alternative to the <legacyBold>Append</legacyBold> method, you can create fields by assigning a value to an undefined or previously deleted field.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt16" class="tgtSentence">This section contains the following topics.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4e1028ff7e66226232dcd860a33b1472" id="tgt17" class="tgtSentence">                 <legacyLink xlink:href="4869aafa-7401-4ce1-93ce-45406a60274f">The OLE DB Provider for Internet Publishing</legacyLink>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="892cd35c22b97a5087f079a0c3bbeb4e" id="tgt18" class="tgtSentence">                 <legacyLink xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</legacyLink>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cc50aa748716540f24d4cb2e2c1280f1" id="tgt19" class="tgtSentence">                 <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0366f1b02165a8b78c4b94e1670269ef" id="tgt20" class="tgtSentence">                 <legacyLink xlink:href="77f95e0a-0cf2-411a-a792-593f77330fbd">Records and Provider-Supplied Fields</legacyLink>               </caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
        <link xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">What's New in ADO</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">       <legacyLink xlink:href="4869aafa-7401-4ce1-93ce-45406a60274f">The OLE DB Provider for Internet Publishing</legacyLink> shows a specific example of accessing heterogeneous data with ADO.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Although the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an e-mail store.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">URLs</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> You can use URLs with the existing <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> and <legacyBold>Recordset</legacyBold> objects and with the <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">For more information about how to use URLs, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Record Fields</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or <legacyBold>Record</legacyBold>, can have a different set of columns, or <legacyBold>Fields</legacyBold>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> For homogeneous data, each row has the same set of columns.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> For more information about the fields specific to the Internet Publishing Provider, see <legacyLink xlink:href="77f95e0a-0cf2-411a-a792-593f77330fbd">Records and Provider-Supplied Extra Fields</legacyLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src11" class="srcSentence">Appending New Fields</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src12" class="srcSentence">Several ADO objects have been enhanced to work together with <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">The <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method, which creates and adds a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object to the collection, can also specify the value of the <legacyBold>Field</legacyBold>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">The <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method finalizes the addition or deletion of fields to the collection.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">As a shortcut and alternative to the <legacyBold>Append</legacyBold> method, you can create fields by assigning a value to an undefined or previously deleted field.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src16" class="srcSentence">This section contains the following topics.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">                 <legacyLink xlink:href="4869aafa-7401-4ce1-93ce-45406a60274f">The OLE DB Provider for Internet Publishing</legacyLink>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">                 <legacyLink xlink:href="2f551969-0fd9-41ee-b81d-100975a4bdc2">Internet Publishing Scenario</legacyLink>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">                 <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>               </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">                 <legacyLink xlink:href="77f95e0a-0cf2-411a-a792-593f77330fbd">Records and Provider-Supplied Fields</legacyLink>               </caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
        <link xlink:href="667673f2-3151-432b-894a-3fc60b704ea4">What's New in ADO</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "RecordOpenOptionsEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 9028aba4-90fc-4dfc-88e4-fa8a7b6fedee
caps.latest.revision: 10
caps.handback.revision: 10
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
# RecordOpenOptionsEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c7d913aeb1a1b78da99e4e3dab5d5efc" id="tgt1" class="tgtSentence">Specifies options for opening a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="58d7a0373787916b38d805d015c4167a" id="tgt2" class="tgtSentence"> These values may be combined by using OR.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt3" class="tgtSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt4" class="tgtSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt5" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="7a9412deafc7e5519e72413622ddbf5e" id="tgt6" class="tgtSentence">adDelayFetchFields</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2c19da7a85d14d73f4f3c32213fb3ce4" id="tgt7" class="tgtSentence">0x8000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5f8e477c1ce6681f049efa204996c593" id="tgt8" class="tgtSentence">Indicates to the provider that the fields associated with the <legacyBold>Record</legacyBold> need not be retrieved initially, but can be retrieved at the first attempt to access the field.</caps:sentence>
                  <caps:sentence sentenceid="79a0d44a7755a016b4e1ed54a4df33b4" id="tgt9" class="tgtSentence"> The default behavior, indicated by the absence of this flag, is to retrieve all the <legacyBold>Record</legacyBold> object fields.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="043eb96d32e59fd86a70f5fc825fb1ff" id="tgt10" class="tgtSentence">adDelayFetchStream</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="53097f7414e99594ac5b8a15c3fc2fff" id="tgt11" class="tgtSentence">0x4000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f008c537c9b802be8c4a0ed04399ac40" id="tgt12" class="tgtSentence">Indicates to the provider that the default stream associated with the <legacyBold>Record</legacyBold> need not be retrieved initially.</caps:sentence>
                  <caps:sentence sentenceid="5283f2a2fac4f83b7f41bd6eabfdc912" id="tgt13" class="tgtSentence"> The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="61f9fc97ae22355800a363714410b45e" id="tgt14" class="tgtSentence">adOpenAsync</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="77176f38a4aeb7cbc5591c30e3536bc2" id="tgt15" class="tgtSentence">0x1000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c0824537aa74536b7c8bd4ebcaab817c" id="tgt16" class="tgtSentence">Indicates that the <legacyBold>Record</legacyBold> object is opened in asynchronous mode.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="ad5a273b64c703e45414e7fc652ae483" id="tgt17" class="tgtSentence">adOpenExecuteCommand</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d391cf999fd4648a0975af64a61802d" id="tgt18" class="tgtSentence">0x10000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3bb5dfad208c4d35f07dd2c7dab2dc0a" id="tgt19" class="tgtSentence">Indicates that the Source string contains command text that should be executed.</caps:sentence>
                  <caps:sentence sentenceid="b8ff895f682da19c657352df623a96a4" id="tgt20" class="tgtSentence"> This value is equivalent to the <legacyBold>adCmdText</legacyBold> option on <legacyBold>Recordset.Open</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="f9694b16b8dcb9a8c372ef852f213da9" id="tgt21" class="tgtSentence">adOpenRecordUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt22" class="tgtSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt23" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="3f0d016534faf9b866f8598a79d263ff" id="tgt24" class="tgtSentence"> Indicates no options are specified.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="729b5c6b2adae9190b141a150ff71257" id="tgt25" class="tgtSentence">adOpenOutput</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="56cbd6e2f68ae6b54cc912a342e23117" id="tgt26" class="tgtSentence">0x800000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3391938b8ddae7f06fd33ebe87453e1e" id="tgt27" class="tgtSentence">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <legacyBold>Record</legacyBold> will contain the results of the executed script.</caps:sentence>
                  <caps:sentence sentenceid="edbc668dcc87f02318f97088ec778a18" id="tgt28" class="tgtSentence"> This value is only valid with non-collection records.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt29" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2feceb55ab2f12074bf5420d2fcd6fc5" id="tgt30" class="tgtSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt31" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies options for opening a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These values may be combined by using OR.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src6" class="srcSentence">adDelayFetchFields</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">0x8000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Indicates to the provider that the fields associated with the <legacyBold>Record</legacyBold> need not be retrieved initially, but can be retrieved at the first attempt to access the field.</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> The default behavior, indicated by the absence of this flag, is to retrieve all the <legacyBold>Record</legacyBold> object fields.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src10" class="srcSentence">adDelayFetchStream</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">0x4000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Indicates to the provider that the default stream associated with the <legacyBold>Record</legacyBold> need not be retrieved initially.</caps:sentence>
                  <caps:sentence id="src13" class="srcSentence"> The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src14" class="srcSentence">adOpenAsync</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">0x1000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Indicates that the <legacyBold>Record</legacyBold> object is opened in asynchronous mode.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src17" class="srcSentence">adOpenExecuteCommand</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">0x10000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Indicates that the Source string contains command text that should be executed.</caps:sentence>
                  <caps:sentence id="src20" class="srcSentence"> This value is equivalent to the <legacyBold>adCmdText</legacyBold> option on <legacyBold>Recordset.Open</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src21" class="srcSentence">adOpenRecordUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src24" class="srcSentence"> Indicates no options are specified.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src25" class="srcSentence">adOpenOutput</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">0x800000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <legacyBold>Record</legacyBold> will contain the results of the executed script.</caps:sentence>
                  <caps:sentence id="src28" class="srcSentence"> This value is only valid with non-collection records.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src29" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src30" class="srcSentence">These constants do not have ADO/WFC equivalents.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src31" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
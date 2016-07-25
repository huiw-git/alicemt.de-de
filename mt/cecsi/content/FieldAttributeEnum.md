---
title: "FieldAttributeEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6e34d886-005a-40dc-bd5c-6adcbf81e5cd
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
# FieldAttributeEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f465c36a29e0d36cf288ae71fa20bfd3" id="tgt1" class="tgtSentence">Specifies one or more attributes of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt2" class="tgtSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt3" class="tgtSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt4" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e432d82b6798eb8e79d2dd25b3c6c757" id="tgt5" class="tgtSentence">adFldCacheDeferred</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="77176f38a4aeb7cbc5591c30e3536bc2" id="tgt6" class="tgtSentence">0x1000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6c15c8383fc268aafb8fced8a6020ab5" id="tgt7" class="tgtSentence">Indicates that the provider caches field values and that subsequent reads are done from the cache.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="70f6b9fff8a958114bdabd67d0dbe6c4" id="tgt8" class="tgtSentence">adFldFixed</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7f6a417be70d8c2743207d53badb5c83" id="tgt9" class="tgtSentence">0x10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="aaad21b48168b4a79a579aea2e1b905c" id="tgt10" class="tgtSentence">Indicates that the field contains fixed-length data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="01edc66fda137f173a9f8ac23eda7da7" id="tgt11" class="tgtSentence">adFldIsChapter</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f41b03f46687b6430a40b0d6624a472f" id="tgt12" class="tgtSentence">0x2000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="91f12b1d3d68a06af54c358dc286c9e3" id="tgt13" class="tgtSentence">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field.</caps:sentence>
                  <caps:sentence sentenceid="88a108801c00defe15f83a6c5441dd62" id="tgt14" class="tgtSentence"> Typically chapter fields are used with data shaping or filters.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="11b7a627920a729714830e15f067f82d" id="tgt15" class="tgtSentence">adFldIsCollection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="efd66904e73acaef7840c416afe41725" id="tgt16" class="tgtSentence">0x40000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f95f114c97ac9c7cd6c3277af853d75b" id="tgt17" class="tgtSentence">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="77f2c78de0e8dedb3f9c96794c2443d7" id="tgt18" class="tgtSentence">adFldKeyColumn</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2c19da7a85d14d73f4f3c32213fb3ce4" id="tgt19" class="tgtSentence">0x8000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f15932ccc68b3211ec4ee45bfef0715e" id="tgt20" class="tgtSentence">Indicates that the field specifies all or part of the column's primary key.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2aa63de5abc715bd2a4316c2c0c85397" id="tgt21" class="tgtSentence">adFldIsDefaultStream</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5a03448e3c97608b71324f913efa7b86" id="tgt22" class="tgtSentence">0x20000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="efafb2e66f57570425abb5aadb3a26e7" id="tgt23" class="tgtSentence">Indicates that the field contains the default stream for the resource represented by the record.</caps:sentence>
                  <caps:sentence sentenceid="b6b445664f19f38e6b8dd276003896ff" id="tgt24" class="tgtSentence"> For example, the default stream can be the HTML content of a root folder on a Web site, which is automatically served when the root URL is specified.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8270c098a3b9926d64204f4acfb62ab6" id="tgt25" class="tgtSentence">adFldIsNullable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9cb7196b9376491fb16d0db6de086efb" id="tgt26" class="tgtSentence">0x20</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="52fe653972053ff1ebdf77ef9400fb10" id="tgt27" class="tgtSentence">Indicates that the field accepts null values.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="233a38b67402c146132832325fa40e40" id="tgt28" class="tgtSentence">adFldIsRowURL</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d391cf999fd4648a0975af64a61802d" id="tgt29" class="tgtSentence">0x10000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1b78d62440ce8e8d01d03381c7799563" id="tgt30" class="tgtSentence">Indicates that the field contains the URL that names the resource from the data store represented by the record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2235d5158a4f1f14db3d49c244a247a4" id="tgt31" class="tgtSentence">adFldLong</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="86339579fe78c05cb63c5eefc948bd77" id="tgt32" class="tgtSentence">0x80</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f407feabb23416c9ce2da33b981ceb21" id="tgt33" class="tgtSentence">Indicates that the field is a long binary field.</caps:sentence>
                  <caps:sentence sentenceid="1d0a12b5f9a42ec00bc6699e4fa0d8a4" id="tgt34" class="tgtSentence"> Also indicates that you can use the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk</legacyLink> and <legacyLink xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk</legacyLink> methods.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="4c85e8a275c781fbb83d88818239a4b2" id="tgt35" class="tgtSentence">adFldMayBeNull</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b0723edc0cca12c5fa732c5e2df9cd90" id="tgt36" class="tgtSentence">0x40</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="178f4e67be937121f9fa32eb39d5f77e" id="tgt37" class="tgtSentence">Indicates that you can read null values from the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="907cc692d38108b2a149c64472dd9daf" id="tgt38" class="tgtSentence">adFldMayDefer</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="70f97d5da645a10e3dc2b005a86d2cd7" id="tgt39" class="tgtSentence">0x2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="369e8a3e11aec63dd3f48800fef73a7c" id="tgt40" class="tgtSentence">Indicates that the field is deferred—that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="b9439ef44cb6f11b76b4da5503503226" id="tgt41" class="tgtSentence">adFldNegativeScale</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="53097f7414e99594ac5b8a15c3fc2fff" id="tgt42" class="tgtSentence">0x4000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="64a18b7666d17ce5c7f0ff5a48f25b5f" id="tgt43" class="tgtSentence">Indicates that the field represents a numeric value from a column that supports negative scale values.</caps:sentence>
                  <caps:sentence sentenceid="ec45df5ab0a6aca803f4261cd37e690a" id="tgt44" class="tgtSentence"> The scale is specified by the <legacyLink xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale</legacyLink> property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="6c6e8f28963146cd393cb9b98b8855be" id="tgt45" class="tgtSentence">adFldRowID</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c31ff34c5741f41aaab689b057de2aed" id="tgt46" class="tgtSentence">0x100</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="860d14f8ec9692a5499b41ae3d3f17c2" id="tgt47" class="tgtSentence">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8f90097a5cef22a950a08a75769b8331" id="tgt48" class="tgtSentence">adFldRowVersion</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="417312c0143ef2ee3cb46ab39385be0e" id="tgt49" class="tgtSentence">0x200</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d748e80682c717f74490eb3f8781e253" id="tgt50" class="tgtSentence">Indicates that the field contains some kind of time or date stamp used to track updates.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8bad3b048a67d8399b8e741931843bd3" id="tgt51" class="tgtSentence">adFldUnknownUpdatable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b045dea7dac3110bf77b78932b0849ff" id="tgt52" class="tgtSentence">0x8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="41315d3092134c7c3fb4d121de079a72" id="tgt53" class="tgtSentence">Indicates that the provider cannot determine if you can write to the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="471149453640a0acfefbcb490fa3837e" id="tgt54" class="tgtSentence">adFldUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="aaae9096f95564e43b5c57ebb7f02091" id="tgt55" class="tgtSentence">-1 0xFFFFFFFF</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a2dcc4be678c655e53de7182b20e1bc8" id="tgt56" class="tgtSentence">Indicates that the provider does not specify the field attributes.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3d76c5019af722fd70e38eccf9a7fd72" id="tgt57" class="tgtSentence">adFldUpdatable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c59fa8ebbc79e63a41006d9cb98e468d" id="tgt58" class="tgtSentence">0x4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c6dc7db35b1c302dd0e74e45b05692fa" id="tgt59" class="tgtSentence">Indicates that you can write to the field.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt60" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt61" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt62" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7137a064858c670904cd63799ff14f2b" id="tgt63" class="tgtSentence">AdoEnums.FieldAttribute.CACHEDEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe4ebacf6e7e2ea00bd45bae5b18315c" id="tgt64" class="tgtSentence">AdoEnums.FieldAttribute.FIXED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="70279d5bd6510f84ab2bcf31fd09095f" id="tgt65" class="tgtSentence">AdoEnums.FieldAttribute.ISNULLABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b1ddb750b5df58512827f19b88b21a2" id="tgt66" class="tgtSentence">AdoEnums.FieldAttribute.LONG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ef87e773fca3f39bd42e3a2545928e92" id="tgt67" class="tgtSentence">AdoEnums.FieldAttribute.MAYBENULL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="633dba07d56683212144219fa9409c13" id="tgt68" class="tgtSentence">AdoEnums.FieldAttribute.MAYDEFER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="600b29577cc6f92a7548a0d97cda937c" id="tgt69" class="tgtSentence">AdoEnums.FieldAttribute.NEGATIVESCALE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ee57e771cc420865b555fc7ec0667973" id="tgt70" class="tgtSentence">AdoEnums.FieldAttribute.ROWID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b350447a951ecd4097814c319ae31923" id="tgt71" class="tgtSentence">AdoEnums.FieldAttribute.ROWVERSION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7e4d9653c21b261ac35b1b6b35fceb2a" id="tgt72" class="tgtSentence">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b81d67a0d30e17b5f670bcc77290699b" id="tgt73" class="tgtSentence">AdoEnums.FieldAttribute.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eb71acaee961b2d9fb5835b887dc7c65" id="tgt74" class="tgtSentence">AdoEnums.FieldAttribute.UPDATABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt75" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes Property</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies one or more attributes of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src5" class="srcSentence">adFldCacheDeferred</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">0x1000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Indicates that the provider caches field values and that subsequent reads are done from the cache.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src8" class="srcSentence">adFldFixed</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">0x10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Indicates that the field contains fixed-length data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src11" class="srcSentence">adFldIsChapter</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">0x2000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field.</caps:sentence>
                  <caps:sentence id="src14" class="srcSentence"> Typically chapter fields are used with data shaping or filters.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src15" class="srcSentence">adFldIsCollection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">0x40000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src18" class="srcSentence">adFldKeyColumn</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">0x8000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Indicates that the field specifies all or part of the column's primary key.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src21" class="srcSentence">adFldIsDefaultStream</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">0x20000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Indicates that the field contains the default stream for the resource represented by the record.</caps:sentence>
                  <caps:sentence id="src24" class="srcSentence"> For example, the default stream can be the HTML content of a root folder on a Web site, which is automatically served when the root URL is specified.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src25" class="srcSentence">adFldIsNullable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">0x20</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Indicates that the field accepts null values.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src28" class="srcSentence">adFldIsRowURL</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">0x10000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Indicates that the field contains the URL that names the resource from the data store represented by the record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src31" class="srcSentence">adFldLong</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">0x80</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Indicates that the field is a long binary field.</caps:sentence>
                  <caps:sentence id="src34" class="srcSentence"> Also indicates that you can use the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk</legacyLink> and <legacyLink xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk</legacyLink> methods.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src35" class="srcSentence">adFldMayBeNull</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">0x40</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Indicates that you can read null values from the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src38" class="srcSentence">adFldMayDefer</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">0x2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">Indicates that the field is deferred—that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src41" class="srcSentence">adFldNegativeScale</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">0x4000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">Indicates that the field represents a numeric value from a column that supports negative scale values.</caps:sentence>
                  <caps:sentence id="src44" class="srcSentence"> The scale is specified by the <legacyLink xlink:href="29a02992-64be-4fcd-be13-445cba205893">NumericScale</legacyLink> property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src45" class="srcSentence">adFldRowID</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">0x100</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src48" class="srcSentence">adFldRowVersion</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">0x200</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src50" class="srcSentence">Indicates that the field contains some kind of time or date stamp used to track updates.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src51" class="srcSentence">adFldUnknownUpdatable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">0x8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">Indicates that the provider cannot determine if you can write to the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src54" class="srcSentence">adFldUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">-1 0xFFFFFFFF</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">Indicates that the provider does not specify the field attributes.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src57" class="srcSentence">adFldUpdatable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src58" class="srcSentence">0x4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">Indicates that you can write to the field.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src60" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src61" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">AdoEnums.FieldAttribute.CACHEDEFERRED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">AdoEnums.FieldAttribute.FIXED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">AdoEnums.FieldAttribute.ISNULLABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">AdoEnums.FieldAttribute.LONG</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">AdoEnums.FieldAttribute.MAYBENULL</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">AdoEnums.FieldAttribute.MAYDEFER</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">AdoEnums.FieldAttribute.NEGATIVESCALE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">AdoEnums.FieldAttribute.ROWID</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">AdoEnums.FieldAttribute.ROWVERSION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">AdoEnums.FieldAttribute.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">AdoEnums.FieldAttribute.UPDATABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src75" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes Property</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
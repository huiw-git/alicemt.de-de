---
title: "ExecuteOptionEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 68bfa83a-5df4-4bef-8736-0f88ae8c29ea
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
# ExecuteOptionEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a9dbee9ac2dc031fbbfc6d8c0ca879cd" id="tgt1" class="tgtSentence">Specifies how a provider should execute a command.</caps:sentence>
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
                    <caps:sentence sentenceid="d5f8a5ef80d4ac5a0ecb5e5e66d01f88" id="tgt5" class="tgtSentence">adAsyncExecute</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7f6a417be70d8c2743207d53badb5c83" id="tgt6" class="tgtSentence">0x10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6f87fbe669e665bf579ce9e8f1ba97b9" id="tgt7" class="tgtSentence">Indicates that the command should execute asynchronously.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="f3b57394f30bb8ddc1884831d251e8c7" id="tgt8" class="tgtSentence">This value cannot be combined with the <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> value <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="666a6465ff9db41598a340becc408605" id="tgt9" class="tgtSentence">adAsyncFetch</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9cb7196b9376491fb16d0db6de086efb" id="tgt10" class="tgtSentence">0x20</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5c3e803e5078de4f509833d768b8f1e7" id="tgt11" class="tgtSentence">Indicates that the remaining rows after the initial quantity specified in the <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">CacheSize</legacyLink> property should be retrieved asynchronously.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="910e3793f5f4486c33a407d835086336" id="tgt12" class="tgtSentence">adAsyncFetchNonBlocking</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b0723edc0cca12c5fa732c5e2df9cd90" id="tgt13" class="tgtSentence">0x40</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b48b2fe2e208dd6d3aa15a79a5ef17b9" id="tgt14" class="tgtSentence">Indicates that the main thread never blocks while retrieving.</caps:sentence>
                  <caps:sentence sentenceid="1963da6262704f3493bff2a5e1141321" id="tgt15" class="tgtSentence"> If the requested row has not been retrieved, the current row automatically moves to the end of the file.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="176422506be6fdc415bf47476b1ffff2" id="tgt16" class="tgtSentence">If you open a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> from a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> containing a persistently stored <legacyBold>Recordset</legacyBold>, <legacyBold>adAsyncFetchNonBlocking</legacyBold> will not have an effect; the operation will be synchronous and blocking.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="e0b8537fe2444b08678df2918fcd0d78" id="tgt17" class="tgtSentence">
                    <legacyBold>adAsynchFetchNonBlocking</legacyBold> has no effect when the <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">adCmdTableDirect</legacyLink> option is used to open the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="220ac15c6fab1ca379bc3604151bb0e5" id="tgt18" class="tgtSentence">adExecuteNoRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="86339579fe78c05cb63c5eefc948bd77" id="tgt19" class="tgtSentence">0x80</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3bd784ec4932f5da2d2329cd4b6b6b78" id="tgt20" class="tgtSentence">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</caps:sentence>
                  <caps:sentence sentenceid="366d652919b11c4313c63823a17e2ec7" id="tgt21" class="tgtSentence"> If any rows are retrieved, they are discarded and not returned.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="16b2c8b3a2d0b5c40362ec2d32d788a3" id="tgt22" class="tgtSentence">
                    <legacyBold>adExecuteNoRecords</legacyBold> can only be passed as an optional parameter to the <legacyBold>Command</legacyBold> or <legacyBold>Connection</legacyBold> <legacyBold>Execute</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="724fb42998ed319f164ddf73180d825a" id="tgt23" class="tgtSentence">adExecuteStream</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9c40b1bf1523fa0d7eb38ed802bb6d11" id="tgt24" class="tgtSentence">0x400</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="23c25a84a64cb1b691d2f844e3ac0cc1" id="tgt25" class="tgtSentence">Indicates that the results of a command execution should be returned as a stream.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="23a6c83e4b8e52c751e3b4af9b22a097" id="tgt26" class="tgtSentence">
                    <legacyBold>adExecuteStream</legacyBold> can only be passed as an optional parameter to the <legacyBold>Command</legacyBold> <legacyBold>Execute</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="b2e6344eae02de8d1f693e2aca088f93" id="tgt27" class="tgtSentence">adExecuteRecord</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="756855b20e4bc19d4db76c9f02357504" id="tgt28" class="tgtSentence">Indicates that the <legacyBold>CommandText</legacyBold> is a command or stored procedure that returns a single row which should be returned as a <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2bf84c0a397b333220cce8763b7ab690" id="tgt29" class="tgtSentence">adOptionUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6bb61e3b7bce0931da574d19d1d82c88" id="tgt30" class="tgtSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="15ec3d2f8a6a1a471b14e366e43cc69c" id="tgt31" class="tgtSentence">Indicates that the command is unspecified.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt32" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt33" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt34" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fa288ab05751adeefe54d4adee010629" id="tgt35" class="tgtSentence">AdoEnums.ExecuteOption.ASYNCEXECUTE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1c9c9e128c97dca7d784b186969d0136" id="tgt36" class="tgtSentence">AdoEnums.ExecuteOption.ASYNCFETCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03394748d1760fd6b2fa6bcf1a5933d0" id="tgt37" class="tgtSentence">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="458957db3b8df35914bc6c604b83686a" id="tgt38" class="tgtSentence">AdoEnums.ExecuteOption.NORECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5e23db39346012c23577f26f6e76cddb" id="tgt39" class="tgtSentence">AdoEnums.ExecuteOption.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt40" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link>
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
          <caps:sentence id="src1" class="srcSentence">Specifies how a provider should execute a command.</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">adAsyncExecute</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">0x10</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Indicates that the command should execute asynchronously.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src8" class="srcSentence">This value cannot be combined with the <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> value <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src9" class="srcSentence">adAsyncFetch</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">0x20</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Indicates that the remaining rows after the initial quantity specified in the <legacyLink xlink:href="49dc9a49-af7b-433b-be36-7a14ca984fb7">CacheSize</legacyLink> property should be retrieved asynchronously.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src12" class="srcSentence">adAsyncFetchNonBlocking</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">0x40</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Indicates that the main thread never blocks while retrieving.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> If the requested row has not been retrieved, the current row automatically moves to the end of the file.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src16" class="srcSentence">If you open a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> from a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> containing a persistently stored <legacyBold>Recordset</legacyBold>, <legacyBold>adAsyncFetchNonBlocking</legacyBold> will not have an effect; the operation will be synchronous and blocking.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src17" class="srcSentence">
                    <legacyBold>adAsynchFetchNonBlocking</legacyBold> has no effect when the <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">adCmdTableDirect</legacyLink> option is used to open the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src18" class="srcSentence">adExecuteNoRecords</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">0x80</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</caps:sentence>
                  <caps:sentence id="src21" class="srcSentence"> If any rows are retrieved, they are discarded and not returned.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src22" class="srcSentence">
                    <legacyBold>adExecuteNoRecords</legacyBold> can only be passed as an optional parameter to the <legacyBold>Command</legacyBold> or <legacyBold>Connection</legacyBold> <legacyBold>Execute</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src23" class="srcSentence">adExecuteStream</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">0x400</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Indicates that the results of a command execution should be returned as a stream.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src26" class="srcSentence">
                    <legacyBold>adExecuteStream</legacyBold> can only be passed as an optional parameter to the <legacyBold>Command</legacyBold> <legacyBold>Execute</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src27" class="srcSentence">adExecuteRecord</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">Indicates that the <legacyBold>CommandText</legacyBold> is a command or stored procedure that returns a single row which should be returned as a <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src29" class="srcSentence">adOptionUnspecified</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">-1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Indicates that the command is unspecified.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src32" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src33" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">AdoEnums.ExecuteOption.ASYNCEXECUTE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">AdoEnums.ExecuteOption.ASYNCFETCH</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">AdoEnums.ExecuteOption.NORECORDS</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">AdoEnums.ExecuteOption.UNSPECIFIED</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src40" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery Method</link>
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
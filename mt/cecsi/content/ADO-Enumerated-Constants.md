---
title: "ADO Enumerated Constants"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c97ed131-1a93-463c-9e61-22f029b0c474
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
# ADO Enumerated Constants
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2a1d3acc2474ddef230ef44f5e66fa34" id="tgt1" class="tgtSentence">To assist in debugging, the ADO enumerations list a value for each constant.</caps:sentence>
          <caps:sentence sentenceid="5b14793b70332bbd5d42b23e8a024b62" id="tgt2" class="tgtSentence"> However, this value is purely advisory, and may change from one release of ADO to another.</caps:sentence>
          <caps:sentence sentenceid="349eed5691c39a8f3258ae589df6d018" id="tgt3" class="tgtSentence"> Your code should only depend on the name, not the actual value, of each enumerated constant.</caps:sentence>
        </para>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e79a6a32e6fb4a07f9f278d820952a05" id="tgt4" class="tgtSentence">               <legacyLink xlink:href="f0965617-17d8-41e0-98d0-f824274735a6">ADCPROP_ASYNCTHREADPRIORITY_ENUM</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0a62dc428f0edfdf6e2fed7650075dd9" id="tgt5" class="tgtSentence">For an RDS <legacyBold>Recordset</legacyBold> object, specifies the execution priority of the asynchronous thread that retrieves data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="1dbfb7f6203e83328ba0f4e66b53ebc9" id="tgt6" class="tgtSentence">               <legacyLink xlink:href="ded4f087-87b9-4efa-8026-bde53d3e9e8a">ADCPROP_AUTORECALC_ENUM</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d964f1d9a13ba66f2f93bbba14c9a79c" id="tgt7" class="tgtSentence">Specifies when the <legacyBold>MSDataShape</legacyBold> provider re-calculates aggregate and calculated columns in a hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e64049cd63ee91d7ffa318a75aa1ecd7" id="tgt8" class="tgtSentence">               <legacyLink xlink:href="33fd7b65-2ec8-4f62-91a7-630b5dab1aa2">ADCPROP_UPDATECRITERIA_ENUM</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="39b8d503edd3b693d5008ab7d6d12f85" id="tgt9" class="tgtSentence">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="353a4e4ee82658017109bbb94d2782aa" id="tgt10" class="tgtSentence">               <legacyLink xlink:href="bc9e1a37-e969-47e9-8382-0bbfffa2034f">ADCPROP_UPDATERESYNC_ENUM</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="599c0b02253e6896fbd814ff813e1291" id="tgt11" class="tgtSentence">Specifies whether the <legacyBold>UpdateBatch</legacyBold> method is followed by an implicit <legacyBold>Resync</legacyBold> method operation and if so, the scope of that operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="817bbfb4e8eb091380e60681c3f75b60" id="tgt12" class="tgtSentence">               <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="06f399c4af59d53b225101fe022d0288" id="tgt13" class="tgtSentence">Specifies which records are affected by an operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d8febb259ce39f8dc20a52725ebe13ab" id="tgt14" class="tgtSentence">               <legacyLink xlink:href="55d273c4-ccee-48ef-ba90-8893d04313c8">BookmarkEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3c2198cc5d4bfb4b6d342ba2346b768a" id="tgt15" class="tgtSentence">Specifies a bookmark that indicates where the operation should begin.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e46fe90b0ab5caa13ee18d73e6eff4b3" id="tgt16" class="tgtSentence">               <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4bcbba0bc95b2cb08e67ec1c2657ed0d" id="tgt17" class="tgtSentence">Specifies how a command argument should be interpreted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="16ef0d35e29dad07750c82cc8d4b7513" id="tgt18" class="tgtSentence">               <legacyLink xlink:href="bc8f710d-0621-4673-8d8e-0361e44abed0">CompareEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="20e01a7e28e1edf479c5aee2ee5d833e" id="tgt19" class="tgtSentence">Specifies the relative position of two records represented by their bookmarks.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="696c22d6f8ae25ae3b70cbfa3079e0b6" id="tgt20" class="tgtSentence">               <legacyLink xlink:href="3792c294-5161-4538-a908-22a5fc50b85f">ConnectModeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="530103e1dffb4c27b73774e1d5c65bcc" id="tgt21" class="tgtSentence">Specifies the available permissions for modifying data in a <legacyBold>Connection</legacyBold>, opening a <legacyBold>Record</legacyBold>, or specifying values for the <legacyBold>Mode</legacyBold> property of the<legacyBold> Record</legacyBold> and <legacyBold>Stream</legacyBold> objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="fd329774a08979a101f711692e23b551" id="tgt22" class="tgtSentence">               <legacyLink xlink:href="bff07eeb-dee3-4e4e-9b2d-d56061ea744d">ConnectOptionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="34d26cca13d92ac01a693f4ae2b1e510" id="tgt23" class="tgtSentence">Specifies whether the <legacyBold>Open</legacyBold> method of a <legacyBold>Connection</legacyBold> object should return after (synchronously) or before (asynchronously) the connection is established.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="28ffdc995f4557dd668fea17e80c1df7" id="tgt24" class="tgtSentence">               <legacyLink xlink:href="21026e24-62b7-4cc9-8aef-62c1fc6cba75">ConnectPromptEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="161697df3a46022c66df289d784f1add" id="tgt25" class="tgtSentence">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8af3c885ab98701f3fa8d5350d5f969c" id="tgt26" class="tgtSentence">               <legacyLink xlink:href="2fa4eec5-d50b-4fd3-8ae7-40af441ba12b">CopyRecordOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ba5efb42c7d59a9c40cfbe4da29fb9fc" id="tgt27" class="tgtSentence">Specifies the behavior of the <legacyBold>CopyRecord</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="77847fab71522270a8d3ea5431e50749" id="tgt28" class="tgtSentence">               <legacyLink xlink:href="acb255ff-1734-4b70-89bb-aef862b4c63b">CursorLocationEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="32ce6aab2f822cc752855b6dcbad6849" id="tgt29" class="tgtSentence">Specifies the location of the cursor engine.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="729992ca4b1ee092b403fd1e657decfe" id="tgt30" class="tgtSentence">               <legacyLink xlink:href="4e10cda7-ce81-4466-94c2-844d38191cf1">CursorOptionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="58aae9e52ebf7b390723ae8dd1c5a2d8" id="tgt31" class="tgtSentence">Specifies what functionality the <legacyBold>Supports</legacyBold> method should test for.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="14b4e8791e38e83bb548a627f0ae269c" id="tgt32" class="tgtSentence">               <legacyLink xlink:href="ffc6e245-4471-42ae-84dd-e85bddfce983">CursorTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5c9d911c277212390d44e0b8462e5e08" id="tgt33" class="tgtSentence">Specifies the type of cursor used in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="357996911f8c6250b93052f6f8243929" id="tgt34" class="tgtSentence">               <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="96a3e63d0f65ad96ade45b9240dbdb20" id="tgt35" class="tgtSentence">Specifies the data type of a <legacyBold>Field</legacyBold>, <legacyBold>Parameter</legacyBold>, or <legacyBold>Property</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="39b06ee30d7e6e775738fa932dfb190d" id="tgt36" class="tgtSentence">               <legacyLink xlink:href="45d54b6e-db2c-4553-9fd0-528147d6da2f">EditModeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a34f1dec13defd432d3cf22111ac09fa" id="tgt37" class="tgtSentence">Specifies the editing status of a record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7228c57c7f9bf09025b491238f58183b" id="tgt38" class="tgtSentence">               <legacyLink xlink:href="9469ba3a-5e4f-4a10-bbb8-a51a6c9660ea">ErrorValueEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7e43dc4473ea0423a133a6bbcec6ebf8" id="tgt39" class="tgtSentence">Specifies the type of ADO run-time error.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="5cce2b412a7a9bc0e84e215a61bf88df" id="tgt40" class="tgtSentence">               <legacyLink xlink:href="7d4a5496-ec2d-4936-b36a-7049a82be4b4">EventReasonEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4871e8cdfeb62b5d82debd9a34a6b1c5" id="tgt41" class="tgtSentence">Specifies the reason that caused an event to occur.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="5cb45a70cae3fcbd06443b43f49040bc" id="tgt42" class="tgtSentence">               <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="207994c22dec15814b7ee4f04edfd92f" id="tgt43" class="tgtSentence">Specifies the current status of the execution of an event.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e170de2906b6f6b8bb6624d4b1b22203" id="tgt44" class="tgtSentence">               <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a9dbee9ac2dc031fbbfc6d8c0ca879cd" id="tgt45" class="tgtSentence">Specifies how a provider should execute a command.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="dab5b662d127af0aaac8759218f356e5" id="tgt46" class="tgtSentence">               <legacyLink xlink:href="be4eda13-d4e4-4d6b-bb0d-3310b0a96fc2">FieldEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="10da588e6b8f58bfeb1bc6ba44dc9d1a" id="tgt47" class="tgtSentence">Specifies the special fields referenced in the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ab95e4b74cb6a6957a8360184fb36bfa" id="tgt48" class="tgtSentence">               <legacyLink xlink:href="6e34d886-005a-40dc-bd5c-6adcbf81e5cd">FieldAttributeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="33f4016e23e4a06e6fe133383bbeaf4f" id="tgt49" class="tgtSentence">Specifies one or more attributes of a <legacyBold>Field</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e1cc1a20fa51d0a0af7b3ab04bad6ada" id="tgt50" class="tgtSentence">               <legacyLink xlink:href="e06da1e2-303f-41b2-a3b0-61e233da152c">FieldStatusEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="db0be838d698f59b3ced694afe3ec31a" id="tgt51" class="tgtSentence">Specifies the status of a <legacyBold>Field</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4558942c1977d6c923c213474061381f" id="tgt52" class="tgtSentence">               <legacyLink xlink:href="b22e725e-84bd-4286-a070-290c278c3783">FilterGroupEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8e63d73cb9c8c7f9ac72e8c6fb052ee3" id="tgt53" class="tgtSentence">Specifies the group of records to be filtered from a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="723dcf1cdd4e049fc02335a64bd1758d" id="tgt54" class="tgtSentence">               <legacyLink xlink:href="adc109b9-79f4-4946-a5eb-658e22e9a8a5">GetRowsOptionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="59ff6da1fc7bfc7ebd5b1ee26ce2df6e" id="tgt55" class="tgtSentence">Specifies how many records to retrieve from a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="08337a8f68963d644027a3460e497a53" id="tgt56" class="tgtSentence">               <legacyLink xlink:href="8e17a7bc-b8a3-4ae2-b6c9-ce088ad31fdf">IsolationLevelEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="845f5a68c4263f6cdfb1850482371677" id="tgt57" class="tgtSentence">Specifies the level of transaction isolation for a <legacyBold>Connection</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="08f2cd06d7834bb694c289a94cd47c1f" id="tgt58" class="tgtSentence">               <legacyLink xlink:href="0440b793-99c7-49a2-b3e2-ec5b1a7e3e60">LineSeparatorsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9c93641ed8b7d88e03d518d944c17838" id="tgt59" class="tgtSentence">Specifies the character used as a line separator in text <legacyBold>Stream</legacyBold> objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="633d8f40c930d6d52ec8cf4051e2252a" id="tgt60" class="tgtSentence">               <legacyLink xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d4b92b624c18277feccbee3b6c726492" id="tgt61" class="tgtSentence">Specifies the type of lock placed on records during editing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f4f4f3b221968c5e93c24df6f9f5aed3" id="tgt62" class="tgtSentence">               <legacyLink xlink:href="4013075d-dbea-4bbc-a6f4-c345a55c5633">MarshalOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3df9f8fa7460dc19d6ed56989b420cf9" id="tgt63" class="tgtSentence">Specifies which records should be returned to the server.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="01d836e1b17fd51efbe80b47b0f71edd" id="tgt64" class="tgtSentence">               <legacyLink xlink:href="f53c2ce4-1021-4a45-92b8-775e8bebad99">MoveRecordOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7c4cc7c2c05bcf2328185797b5adc98c" id="tgt65" class="tgtSentence">Specifies the behavior of the <legacyBold>Record</legacyBold> object <legacyBold>MoveRecord</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="5da042bb9970af0cfbf2766d5472edfb" id="tgt66" class="tgtSentence">               <legacyLink xlink:href="32746558-097b-4749-989e-519aadf7e3f4">ObjectStateEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a4eec36a37a01a0b92f026eb93b6613b" id="tgt67" class="tgtSentence">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4560fabab8a82a7236f319d73a930eff" id="tgt68" class="tgtSentence">               <legacyLink xlink:href="7ef6c728-5eda-4bde-8052-02d2db1d2cfe">ParameterAttributesEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5257f4bbb1f109cdb4c21916a4fe830b" id="tgt69" class="tgtSentence">Specifies the attributes of a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c66091ab1c682b25a87a19a5884d70a5" id="tgt70" class="tgtSentence">               <legacyLink xlink:href="c66aa6e6-d4f0-4f0f-9640-e08ae6cfdef3">ParameterDirectionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f8f4fffe8328d5e01ab5c4225592c3b5" id="tgt71" class="tgtSentence">Specifies whether the <legacyBold>Parameter</legacyBold> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="436c9c238ae45603a1507ec0abc6ebf0" id="tgt72" class="tgtSentence">               <legacyLink xlink:href="ebe1a2ab-e9f1-43a2-8f94-b190c9613d70">PersistFormatEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2bb5b8c3eff31ff98e48ab71e3217a97" id="tgt73" class="tgtSentence">Specifies the format in which to save a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2528be19f0c55c6a3adbd5b1a433102d" id="tgt74" class="tgtSentence">               <legacyLink xlink:href="e69af0a5-3405-4b72-9c6e-6b188ff746fd">PositionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2e09435d4e20bb725c72a5ad9cfb671a" id="tgt75" class="tgtSentence">Specifies the current position of the record pointer within a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="11fe2a999d17995dcfd092873d90c384" id="tgt76" class="tgtSentence">               <legacyLink xlink:href="96a01955-a6b4-4cbf-9c73-52bcd1e9fb25">PropertyAttributesEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3e1c7b93a25e4e2e999ac9cd39b5bf3b" id="tgt77" class="tgtSentence">Specifies the attributes of a <legacyBold>Property</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="fd30efaad8bbe155131b0421ce8f341e" id="tgt78" class="tgtSentence">               <legacyLink xlink:href="6d746670-0850-4065-9cd4-168dea1d3ea9">RecordCreateOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4e67158c81ed30427f19e59e26999f18" id="tgt79" class="tgtSentence">Specifies for the <legacyBold>Record</legacyBold> object <legacyBold>Open</legacyBold> method whether an existing <legacyBold>Record</legacyBold> should be opened, or a new <legacyBold>Record</legacyBold> should be created.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6e41fb54217757f748e99aac15d225f7" id="tgt80" class="tgtSentence">               <legacyLink xlink:href="9028aba4-90fc-4dfc-88e4-fa8a7b6fedee">RecordOpenOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1f0059d0a5b750947fa8f967e0b2d561" id="tgt81" class="tgtSentence">Specifies options for opening a <legacyBold>Record</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="e6a39be0fcec986e995e6f3acf0270bc" id="tgt82" class="tgtSentence"> These values may be combined by using an OR operator.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9cef71da36bcf80d7cadf892964e47ec" id="tgt83" class="tgtSentence">               <legacyLink xlink:href="506fdd70-4452-4e83-95d5-c94311988dfa">RecordStatusEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="565f72928566c539e120143603bbbaa1" id="tgt84" class="tgtSentence">Specifies the status of a record with regard to batch updates and other bulk operations.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="409aebd5a885a4808800be382b9fd2a6" id="tgt85" class="tgtSentence">               <legacyLink xlink:href="f557e537-015d-4ba7-8a41-a6f00b366a91">RecordTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d2e3c78c181c451afb0e187c987014b6" id="tgt86" class="tgtSentence">Specifies the type of <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3e6b69081a2f26e8c9a7353bacbbcad8" id="tgt87" class="tgtSentence">               <legacyLink xlink:href="d3df2c90-e570-4c40-a79a-25b3448a009c">ResyncEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eac050a7153980e828060c18e8f91d40" id="tgt88" class="tgtSentence">Specifies whether underlying values are overwritten by a call to <legacyBold>Resync</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c8096759c08b516b5ca072d539b34664" id="tgt89" class="tgtSentence">               <legacyLink xlink:href="59339100-6e29-48d1-aea3-6873796d186b">SaveOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f7e9cf98443de40d4fbc5459729930c7" id="tgt90" class="tgtSentence">Specifies whether a file should be created or overwritten when saving from a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence sentenceid="4614f350c587bea521f4503285b7ba9d" id="tgt91" class="tgtSentence"> The values can be combined with an AND operator.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2c6554ad46fb6d5c2b141d633759bc98" id="tgt92" class="tgtSentence">               <legacyLink xlink:href="21c97651-297f-469f-b5b5-c48af72b62a8">SchemaEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f4c49fa45e8d8aa4e2fd3a9bcaec00ea" id="tgt93" class="tgtSentence">Specifies the type of schema <legacyBold>Recordset</legacyBold> that the <legacyBold>OpenSchema</legacyBold> method retrieves.</caps:sentence>
                  <caps:sentence sentenceid="9533ff6b772a47c44587982246763fa2" id="tgt94" class="tgtSentence"> Specifies the direction of a record search within a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="325c6f9fcd04c0136e8e30708bba0b6f" id="tgt95" class="tgtSentence">               <legacyLink xlink:href="81272ae3-2165-4f4e-adfe-9ede0368cb17">SearchDirectionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1feed00f94994b62b1d06a747103d779" id="tgt96" class="tgtSentence">Specifies the direction of a record search within a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="7efb375d1f251cc109fae49c3cf78315" id="tgt97" class="tgtSentence"> Specifies the type of <legacyBold>Seek</legacyBold> to execute.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ef96847dc2dba4df27bb6f9acde62aa8" id="tgt98" class="tgtSentence">               <legacyLink xlink:href="f0ec0c92-8253-47c6-9a14-e5dbccbad219">SeekEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fcfaacaad1d6863cc2fc42fbfa60a56c" id="tgt99" class="tgtSentence">Specifies the type of <legacyBold>Seek</legacyBold> to execute.</caps:sentence>
                  <caps:sentence sentenceid="e29f18b437581cb4b57dc86f9bb607ae" id="tgt100" class="tgtSentence"> Specifies options for opening a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence sentenceid="4614f350c587bea521f4503285b7ba9d" id="tgt101" class="tgtSentence"> The values can be combined with an AND operator.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="07d17fc736da7858ee1b151e9525fed6" id="tgt102" class="tgtSentence">               <legacyLink xlink:href="85b6c57f-47ed-46ba-bd92-07882ae9e9d2">StreamOpenOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7b6a00f1993979e35c11430b3439ec8d" id="tgt103" class="tgtSentence">Specifies options for opening a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence sentenceid="4614f350c587bea521f4503285b7ba9d" id="tgt104" class="tgtSentence"> The values can be combined with an AND operator.</caps:sentence>
                  <caps:sentence sentenceid="684bc4aabcbd282d734b9625f491feec" id="tgt105" class="tgtSentence"> Specifies whether the whole stream or the next line should be read from a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="089c9d257489b50e5233cb4110dac788" id="tgt106" class="tgtSentence">               <legacyLink xlink:href="cfa1b416-003a-436f-a21b-bd2397e54db3">StreamReadEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bcafd018c850608d2a592bd1145e1b13" id="tgt107" class="tgtSentence">Specifies whether the whole stream or the next line should be read from a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence sentenceid="00d68b0b302feda6526a60915bb29cda" id="tgt108" class="tgtSentence"> Specifies the type of data stored in a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9712701cf054337bc8fb617bed1c1920" id="tgt109" class="tgtSentence">               <legacyLink xlink:href="220fe51d-4889-4020-a099-2ec9c7485503">StreamTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bd2884c40007202001a74100b68f35ae" id="tgt110" class="tgtSentence">Specifies the type of data stored in a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence sentenceid="5ff960641e60a544e5f58fdcd94bed31" id="tgt111" class="tgtSentence"> Specifies whether a line separator is appended to the string written to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="25e05a63e65a48cceea8e8d311e18997" id="tgt112" class="tgtSentence">               <legacyLink xlink:href="bdbf3405-a0bd-4f02-85d4-e3fe8da3f3f7">StreamWriteEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1d016d98df746d716f1d501fa2912168" id="tgt113" class="tgtSentence">Specifies whether a line separator is appended to the string written to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence sentenceid="c8640a2c0867132871a47c0ede296469" id="tgt114" class="tgtSentence"> Specifies the format when retrieving a <legacyBold>Recordset</legacyBold> as a string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="25ddb0959a8161c15d47c2da3c0e6385" id="tgt115" class="tgtSentence">               <legacyLink xlink:href="28f7d1ec-092b-4323-a39d-d3f882c6c81a">StringFormatEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="db959a0a51ed3634e1bd21b128a0b8c3" id="tgt116" class="tgtSentence">Specifies the format when retrieving a <legacyBold>Recordset</legacyBold> as a string.</caps:sentence>
                  <caps:sentence sentenceid="fcccbfd0cc0dd4ef2d75cd5b263ce84a" id="tgt117" class="tgtSentence"> Specifies the transaction attributes of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="78049fede747a1d7ffaf2acaee335b45" id="tgt118" class="tgtSentence">               <legacyLink xlink:href="e7dcecd3-7dc7-445c-b922-f700c3067fbc">XactAttributeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7ae1e65bf8f9b6da22553ebd1a17e5e9" id="tgt119" class="tgtSentence">Specifies the transaction attributes of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</link>
        <link xlink:href="d7b06d72-f792-4328-93a2-5006b9e2c581">ADO Dynamic Properties</link>
        <link xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">ADO Errors</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">To assist in debugging, the ADO enumerations list a value for each constant.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> However, this value is purely advisory, and may change from one release of ADO to another.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Your code should only depend on the name, not the actual value, of each enumerated constant.</caps:sentence>
        </para>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">               <legacyLink xlink:href="f0965617-17d8-41e0-98d0-f824274735a6">ADCPROP_ASYNCTHREADPRIORITY_ENUM</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">For an RDS <legacyBold>Recordset</legacyBold> object, specifies the execution priority of the asynchronous thread that retrieves data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">               <legacyLink xlink:href="ded4f087-87b9-4efa-8026-bde53d3e9e8a">ADCPROP_AUTORECALC_ENUM</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Specifies when the <legacyBold>MSDataShape</legacyBold> provider re-calculates aggregate and calculated columns in a hierarchical <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">               <legacyLink xlink:href="33fd7b65-2ec8-4f62-91a7-630b5dab1aa2">ADCPROP_UPDATECRITERIA_ENUM</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">               <legacyLink xlink:href="bc9e1a37-e969-47e9-8382-0bbfffa2034f">ADCPROP_UPDATERESYNC_ENUM</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Specifies whether the <legacyBold>UpdateBatch</legacyBold> method is followed by an implicit <legacyBold>Resync</legacyBold> method operation and if so, the scope of that operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">               <legacyLink xlink:href="1ab921a0-6c57-43b4-9291-701b2599f3e8">AffectEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Specifies which records are affected by an operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">               <legacyLink xlink:href="55d273c4-ccee-48ef-ba90-8893d04313c8">BookmarkEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Specifies a bookmark that indicates where the operation should begin.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">               <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Specifies how a command argument should be interpreted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">               <legacyLink xlink:href="bc8f710d-0621-4673-8d8e-0361e44abed0">CompareEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Specifies the relative position of two records represented by their bookmarks.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">               <legacyLink xlink:href="3792c294-5161-4538-a908-22a5fc50b85f">ConnectModeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Specifies the available permissions for modifying data in a <legacyBold>Connection</legacyBold>, opening a <legacyBold>Record</legacyBold>, or specifying values for the <legacyBold>Mode</legacyBold> property of the<legacyBold> Record</legacyBold> and <legacyBold>Stream</legacyBold> objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">               <legacyLink xlink:href="bff07eeb-dee3-4e4e-9b2d-d56061ea744d">ConnectOptionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Specifies whether the <legacyBold>Open</legacyBold> method of a <legacyBold>Connection</legacyBold> object should return after (synchronously) or before (asynchronously) the connection is established.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">               <legacyLink xlink:href="21026e24-62b7-4cc9-8aef-62c1fc6cba75">ConnectPromptEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">               <legacyLink xlink:href="2fa4eec5-d50b-4fd3-8ae7-40af441ba12b">CopyRecordOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Specifies the behavior of the <legacyBold>CopyRecord</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">               <legacyLink xlink:href="acb255ff-1734-4b70-89bb-aef862b4c63b">CursorLocationEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">Specifies the location of the cursor engine.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">               <legacyLink xlink:href="4e10cda7-ce81-4466-94c2-844d38191cf1">CursorOptionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Specifies what functionality the <legacyBold>Supports</legacyBold> method should test for.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">               <legacyLink xlink:href="ffc6e245-4471-42ae-84dd-e85bddfce983">CursorTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Specifies the type of cursor used in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">               <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">Specifies the data type of a <legacyBold>Field</legacyBold>, <legacyBold>Parameter</legacyBold>, or <legacyBold>Property</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">               <legacyLink xlink:href="45d54b6e-db2c-4553-9fd0-528147d6da2f">EditModeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Specifies the editing status of a record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">               <legacyLink xlink:href="9469ba3a-5e4f-4a10-bbb8-a51a6c9660ea">ErrorValueEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">Specifies the type of ADO run-time error.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">               <legacyLink xlink:href="7d4a5496-ec2d-4936-b36a-7049a82be4b4">EventReasonEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">Specifies the reason that caused an event to occur.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">               <legacyLink xlink:href="ebfd4cda-4017-4873-9d28-38b1c7db12a8">EventStatusEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">Specifies the current status of the execution of an event.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src44" class="srcSentence">               <legacyLink xlink:href="68bfa83a-5df4-4bef-8736-0f88ae8c29ea">ExecuteOptionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">Specifies how a provider should execute a command.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">               <legacyLink xlink:href="be4eda13-d4e4-4d6b-bb0d-3310b0a96fc2">FieldEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">Specifies the special fields referenced in the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src48" class="srcSentence">               <legacyLink xlink:href="6e34d886-005a-40dc-bd5c-6adcbf81e5cd">FieldAttributeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">Specifies one or more attributes of a <legacyBold>Field</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src50" class="srcSentence">               <legacyLink xlink:href="e06da1e2-303f-41b2-a3b0-61e233da152c">FieldStatusEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src51" class="srcSentence">Specifies the status of a <legacyBold>Field</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">               <legacyLink xlink:href="b22e725e-84bd-4286-a070-290c278c3783">FilterGroupEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">Specifies the group of records to be filtered from a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">               <legacyLink xlink:href="adc109b9-79f4-4946-a5eb-658e22e9a8a5">GetRowsOptionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">Specifies how many records to retrieve from a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">               <legacyLink xlink:href="8e17a7bc-b8a3-4ae2-b6c9-ce088ad31fdf">IsolationLevelEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">Specifies the level of transaction isolation for a <legacyBold>Connection</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src58" class="srcSentence">               <legacyLink xlink:href="0440b793-99c7-49a2-b3e2-ec5b1a7e3e60">LineSeparatorsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">Specifies the character used as a line separator in text <legacyBold>Stream</legacyBold> objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src60" class="srcSentence">               <legacyLink xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src61" class="srcSentence">Specifies the type of lock placed on records during editing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src62" class="srcSentence">               <legacyLink xlink:href="4013075d-dbea-4bbc-a6f4-c345a55c5633">MarshalOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src63" class="srcSentence">Specifies which records should be returned to the server.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src64" class="srcSentence">               <legacyLink xlink:href="f53c2ce4-1021-4a45-92b8-775e8bebad99">MoveRecordOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src65" class="srcSentence">Specifies the behavior of the <legacyBold>Record</legacyBold> object <legacyBold>MoveRecord</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src66" class="srcSentence">               <legacyLink xlink:href="32746558-097b-4749-989e-519aadf7e3f4">ObjectStateEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src67" class="srcSentence">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src68" class="srcSentence">               <legacyLink xlink:href="7ef6c728-5eda-4bde-8052-02d2db1d2cfe">ParameterAttributesEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src69" class="srcSentence">Specifies the attributes of a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src70" class="srcSentence">               <legacyLink xlink:href="c66aa6e6-d4f0-4f0f-9640-e08ae6cfdef3">ParameterDirectionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src71" class="srcSentence">Specifies whether the <legacyBold>Parameter</legacyBold> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src72" class="srcSentence">               <legacyLink xlink:href="ebe1a2ab-e9f1-43a2-8f94-b190c9613d70">PersistFormatEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src73" class="srcSentence">Specifies the format in which to save a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src74" class="srcSentence">               <legacyLink xlink:href="e69af0a5-3405-4b72-9c6e-6b188ff746fd">PositionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src75" class="srcSentence">Specifies the current position of the record pointer within a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src76" class="srcSentence">               <legacyLink xlink:href="96a01955-a6b4-4cbf-9c73-52bcd1e9fb25">PropertyAttributesEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src77" class="srcSentence">Specifies the attributes of a <legacyBold>Property</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src78" class="srcSentence">               <legacyLink xlink:href="6d746670-0850-4065-9cd4-168dea1d3ea9">RecordCreateOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src79" class="srcSentence">Specifies for the <legacyBold>Record</legacyBold> object <legacyBold>Open</legacyBold> method whether an existing <legacyBold>Record</legacyBold> should be opened, or a new <legacyBold>Record</legacyBold> should be created.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src80" class="srcSentence">               <legacyLink xlink:href="9028aba4-90fc-4dfc-88e4-fa8a7b6fedee">RecordOpenOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src81" class="srcSentence">Specifies options for opening a <legacyBold>Record</legacyBold>.</caps:sentence>
                  <caps:sentence id="src82" class="srcSentence"> These values may be combined by using an OR operator.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src83" class="srcSentence">               <legacyLink xlink:href="506fdd70-4452-4e83-95d5-c94311988dfa">RecordStatusEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src84" class="srcSentence">Specifies the status of a record with regard to batch updates and other bulk operations.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src85" class="srcSentence">               <legacyLink xlink:href="f557e537-015d-4ba7-8a41-a6f00b366a91">RecordTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src86" class="srcSentence">Specifies the type of <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src87" class="srcSentence">               <legacyLink xlink:href="d3df2c90-e570-4c40-a79a-25b3448a009c">ResyncEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src88" class="srcSentence">Specifies whether underlying values are overwritten by a call to <legacyBold>Resync</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src89" class="srcSentence">               <legacyLink xlink:href="59339100-6e29-48d1-aea3-6873796d186b">SaveOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src90" class="srcSentence">Specifies whether a file should be created or overwritten when saving from a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence id="src91" class="srcSentence"> The values can be combined with an AND operator.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src92" class="srcSentence">               <legacyLink xlink:href="21c97651-297f-469f-b5b5-c48af72b62a8">SchemaEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src93" class="srcSentence">Specifies the type of schema <legacyBold>Recordset</legacyBold> that the <legacyBold>OpenSchema</legacyBold> method retrieves.</caps:sentence>
                  <caps:sentence id="src94" class="srcSentence"> Specifies the direction of a record search within a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src95" class="srcSentence">               <legacyLink xlink:href="81272ae3-2165-4f4e-adfe-9ede0368cb17">SearchDirectionEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src96" class="srcSentence">Specifies the direction of a record search within a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence id="src97" class="srcSentence"> Specifies the type of <legacyBold>Seek</legacyBold> to execute.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src98" class="srcSentence">               <legacyLink xlink:href="f0ec0c92-8253-47c6-9a14-e5dbccbad219">SeekEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src99" class="srcSentence">Specifies the type of <legacyBold>Seek</legacyBold> to execute.</caps:sentence>
                  <caps:sentence id="src100" class="srcSentence"> Specifies options for opening a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence id="src101" class="srcSentence"> The values can be combined with an AND operator.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src102" class="srcSentence">               <legacyLink xlink:href="85b6c57f-47ed-46ba-bd92-07882ae9e9d2">StreamOpenOptionsEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src103" class="srcSentence">Specifies options for opening a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence id="src104" class="srcSentence"> The values can be combined with an AND operator.</caps:sentence>
                  <caps:sentence id="src105" class="srcSentence"> Specifies whether the whole stream or the next line should be read from a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src106" class="srcSentence">               <legacyLink xlink:href="cfa1b416-003a-436f-a21b-bd2397e54db3">StreamReadEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src107" class="srcSentence">Specifies whether the whole stream or the next line should be read from a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence id="src108" class="srcSentence"> Specifies the type of data stored in a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src109" class="srcSentence">               <legacyLink xlink:href="220fe51d-4889-4020-a099-2ec9c7485503">StreamTypeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src110" class="srcSentence">Specifies the type of data stored in a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence id="src111" class="srcSentence"> Specifies whether a line separator is appended to the string written to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src112" class="srcSentence">               <legacyLink xlink:href="bdbf3405-a0bd-4f02-85d4-e3fe8da3f3f7">StreamWriteEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src113" class="srcSentence">Specifies whether a line separator is appended to the string written to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  <caps:sentence id="src114" class="srcSentence"> Specifies the format when retrieving a <legacyBold>Recordset</legacyBold> as a string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src115" class="srcSentence">               <legacyLink xlink:href="28f7d1ec-092b-4323-a39d-d3f882c6c81a">StringFormatEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src116" class="srcSentence">Specifies the format when retrieving a <legacyBold>Recordset</legacyBold> as a string.</caps:sentence>
                  <caps:sentence id="src117" class="srcSentence"> Specifies the transaction attributes of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src118" class="srcSentence">               <legacyLink xlink:href="e7dcecd3-7dc7-445c-b922-f700c3067fbc">XactAttributeEnum</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src119" class="srcSentence">Specifies the transaction attributes of a <legacyBold>Connection</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</link>
        <link xlink:href="d7b06d72-f792-4328-93a2-5006b9e2c581">ADO Dynamic Properties</link>
        <link xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">ADO Errors</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
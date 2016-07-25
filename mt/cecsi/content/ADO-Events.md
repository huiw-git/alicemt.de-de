---
title: "ADO Events"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0ded5ad9-8f83-4224-95af-38512783b972
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
# ADO Events
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerOrientationDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="cbfadf7c452f5ef70a362225b934871b" id="tgt1" class="tgtSentence">             <legacyLink xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">BeginTransComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="49fe524369d5e6ad406d47212c38dab3" id="tgt2" class="tgtSentence">Called after the <legacyBold>BeginTrans</legacyBold> operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0b6d729adf5e13d6e3ab650fb6bbc039" id="tgt3" class="tgtSentence">             <legacyLink xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">CommitTransComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="37343c21ffd1a101b0783b9f80f4bc58" id="tgt4" class="tgtSentence">Called after the <legacyBold>CommitTrans</legacyBold> operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="79a6e5376632c090c0bfc402cc4223bf" id="tgt5" class="tgtSentence">             <legacyLink xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">ConnectComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3b2b6e31f8e93a953cd01f49022ff21c" id="tgt6" class="tgtSentence">Called after a connection starts.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2e7d5ef016efcf0a77b492fccc54feac" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">Disconnect</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="753ac45de5a402a947fde0dcd60f4a7f" id="tgt8" class="tgtSentence">Called after a connection ends.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="612e985233b41dd477291c9d9aad55ba" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="475de5e2-f634-4954-9edf-0027a6ba38d6">EndOfRecordset</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="933608c51cdf13557a3415e1658e26a1" id="tgt10" class="tgtSentence">Called when there is an attempt to move to a row past the end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="69110863807642633417acc2d3e28312" id="tgt11" class="tgtSentence">             <legacyLink xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e4db13fde771d11fe75efcdeb3bf7160" id="tgt12" class="tgtSentence">Called after a command has finished executing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a1af21cda81a99f5c8bf890055d890ad" id="tgt13" class="tgtSentence">             <legacyLink xlink:href="a28d3858-566c-468d-b070-d1de4339fbea">FetchComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cdf24c07330a2f045b0b61eecda82e1e" id="tgt14" class="tgtSentence">Called after all the records in a lengthy asynchronous operation have been retrieved into the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9cf25145e0959d20ff90b4a333bab49b" id="tgt15" class="tgtSentence">             <legacyLink xlink:href="301716fd-81fc-40eb-8a04-221ef7ab410e">FetchProgress</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8b5af7009e585387337a82015559d5a7" id="tgt16" class="tgtSentence">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8d94c4298d83199d22b86fdae3a0a45f" id="tgt17" class="tgtSentence">             <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">FieldChangeComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a82cf83d8d30e97470b2766ccfd91229" id="tgt18" class="tgtSentence">Called after the value of one or more <legacyBold>Field</legacyBold> objects has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="20a01a0fc4b720f05e0c843e484a3489" id="tgt19" class="tgtSentence">             <legacyLink xlink:href="468c87dd-e3bc-4084-9941-94d10743d4e9">InfoMessage</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="159b2c02084121aded7ebc0408f9744f" id="tgt20" class="tgtSentence">Called whenever a warning occurs during a <legacyBold>ConnectionEvent</legacyBold> operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a0557fd732e2ce3e5f3f77014fa7c171" id="tgt21" class="tgtSentence">             <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">MoveComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b4bbda76e9b5813aa33287a4dba1248b" id="tgt22" class="tgtSentence">Called after the current position in the <legacyBold>Recordset</legacyBold> changes.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0fd5c8716104c048692051c5edd508e6" id="tgt23" class="tgtSentence">             <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">RecordChangeComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="82c67327e8ecbbd0373cc91eab4a911b" id="tgt24" class="tgtSentence">Called after one or more records change.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="5c0d4152efcd52d4222beb6881fbf11f" id="tgt25" class="tgtSentence">             <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">RecordsetChangeComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ce82080eb6b3b93230a9c711ab0e53b8" id="tgt26" class="tgtSentence">Called after the <legacyBold>Recordset</legacyBold> has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="950b1a6dea33bd43c6a6234a5bf8d525" id="tgt27" class="tgtSentence">             <legacyLink xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">RollbackTransComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9fe086e6153bd574a5a226dcf5d7ce75" id="tgt28" class="tgtSentence">Called after the <legacyBold>RollbackTrans</legacyBold> operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="27ba23ba717b9c5e3bc3a7c8f3d9c8fe" id="tgt29" class="tgtSentence">             <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="575101351474f5bdc9f5cb5861e40f80" id="tgt30" class="tgtSentence">Called before a pending operation changes the value of one or more <legacyBold>Field</legacyBold> objects in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="397971f88d3fe5a558b0059010cfbae2" id="tgt31" class="tgtSentence">             <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">WillChangeRecord</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f314e2874d3540f139763eb13acea700" id="tgt32" class="tgtSentence">Called before one or more records (rows) in the <legacyBold>Recordset</legacyBold> change.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a0b0f90636f24ff35e0d6d9afca58dee" id="tgt33" class="tgtSentence">             <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8b2fe994ee39e102d3eda3dd052bef76" id="tgt34" class="tgtSentence">Called before a pending operation changes the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="fb996b7292b3e2a551e499d23d20ec79" id="tgt35" class="tgtSentence">             <legacyLink xlink:href="da561d58-eb58-446c-a4fd-1838c76073c0">WillConnect</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="341ef5176439d8f153e030e9548774dd" id="tgt36" class="tgtSentence">Called before a connection starts.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f5fcd816490f4bbf864976f2d1f32416" id="tgt37" class="tgtSentence">             <legacyLink xlink:href="dd755e46-f589-48a3-93a9-51ff998d44b5">WillExecute</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9e9cc48777b391deeef8d2fba817c548" id="tgt38" class="tgtSentence">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="304caeffa14a664c405d182caa3ebb69" id="tgt39" class="tgtSentence">             <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cbeba26a6efb8cd956e7846c884f5c3a" id="tgt40" class="tgtSentence">The <legacyBold>WillMove</legacyBold> event is called <legacyItalic>before</legacyItalic> a pending operation changes the current position in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
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
        <link xlink:href="c97ed131-1a93-463c-9e61-22f029b0c474">ADO Enumerated Constants</link>
        <link xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">ADO Errors</link>
        <link xlink:href="e9003457-0762-48b3-942f-0820266b158f">ADO Event Model, Synchronous and Asynchronous Operations</link>
        <link xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerOrientationDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerOrientationDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src1" class="srcSentence">             <legacyLink xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">BeginTransComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Called after the <legacyBold>BeginTrans</legacyBold> operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">             <legacyLink xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">CommitTransComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Called after the <legacyBold>CommitTrans</legacyBold> operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">             <legacyLink xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">ConnectComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Called after a connection starts.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">Disconnect</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Called after a connection ends.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="475de5e2-f634-4954-9edf-0027a6ba38d6">EndOfRecordset</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Called when there is an attempt to move to a row past the end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">             <legacyLink xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Called after a command has finished executing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">             <legacyLink xlink:href="a28d3858-566c-468d-b070-d1de4339fbea">FetchComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Called after all the records in a lengthy asynchronous operation have been retrieved into the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">             <legacyLink xlink:href="301716fd-81fc-40eb-8a04-221ef7ab410e">FetchProgress</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">             <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">FieldChangeComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Called after the value of one or more <legacyBold>Field</legacyBold> objects has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">             <legacyLink xlink:href="468c87dd-e3bc-4084-9941-94d10743d4e9">InfoMessage</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Called whenever a warning occurs during a <legacyBold>ConnectionEvent</legacyBold> operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">             <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">MoveComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Called after the current position in the <legacyBold>Recordset</legacyBold> changes.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">             <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">RecordChangeComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Called after one or more records change.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">             <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">RecordsetChangeComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">Called after the <legacyBold>Recordset</legacyBold> has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">             <legacyLink xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">RollbackTransComplete</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">Called after the <legacyBold>RollbackTrans</legacyBold> operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">             <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Called before a pending operation changes the value of one or more <legacyBold>Field</legacyBold> objects in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">             <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">WillChangeRecord</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Called before one or more records (rows) in the <legacyBold>Recordset</legacyBold> change.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">             <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">Called before a pending operation changes the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">             <legacyLink xlink:href="da561d58-eb58-446c-a4fd-1838c76073c0">WillConnect</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">Called before a connection starts.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">             <legacyLink xlink:href="dd755e46-f589-48a3-93a9-51ff998d44b5">WillExecute</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">             <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove</legacyLink>           </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">The <legacyBold>WillMove</legacyBold> event is called <legacyItalic>before</legacyItalic> a pending operation changes the current position in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
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
        <link xlink:href="c97ed131-1a93-463c-9e61-22f029b0c474">ADO Enumerated Constants</link>
        <link xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">ADO Errors</link>
        <link xlink:href="e9003457-0762-48b3-942f-0820266b158f">ADO Event Model, Synchronous and Asynchronous Operations</link>
        <link xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerOrientationDocument>
  </caps:SxSSource>
</caps:SxS>
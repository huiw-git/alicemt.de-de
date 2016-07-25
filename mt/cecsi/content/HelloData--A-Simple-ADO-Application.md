---
title: "HelloData: A Simple ADO Application"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de4bcd56-dac2-45e6-95ab-9fd7f25878fc
caps.latest.revision: 15
caps.handback.revision: 15
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
# HelloData: A Simple ADO Application
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e6a3520657c7e773e78e93e5dd9f159c" id="tgt1" class="tgtSentence">This simple application steps through each of the four major ADO operations: getting, examining, editing, and updating data.</caps:sentence>
          <caps:sentence sentenceid="9f12ca3cfc31e3ff0828c7a94bd42a8c" id="tgt2" class="tgtSentence"> These operations are performed against the Northwind sample database included with Microsoft® SQL Server.</caps:sentence>
          <caps:sentence sentenceid="393f022ff34aebd6fd4a933c140513f9" id="tgt3" class="tgtSentence"> To focus on the fundamentals of ADO and to prevent code clutter, error handling in the example is minimal.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence sentenceid="0d761ecc0ff5b18507d0e4d6dd0a09b1" id="tgt4" class="tgtSentence">To run HelloData</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="b73dacae3fc32bbd07cfa5a775b4fc80" id="tgt5" class="tgtSentence">Create a new Standard EXE Visual Basic project that references the ADO library.</caps:sentence>
                  <caps:sentence sentenceid="1f3a557d4382bb730dd9b008e46fb1c3" id="tgt6" class="tgtSentence"> For more information, see <legacyLink xlink:href="573f8f27-babd-4e2f-bf9a-270ee7024975">Referencing the ADO Libraries</legacyLink>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="e89dd0dbada96ea193d254a4ce396691" id="tgt7" class="tgtSentence">Create four command buttons at the top of the form, setting the <legacyBold>Name</legacyBold> and <legacyBold>Caption</legacyBold> properties to the values shown in the table at the end of this topic.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="f4eeedb525fbcc3058b9b11f4f143189" id="tgt8" class="tgtSentence">Below the buttons, add a <legacyBold>Microsoft DataGrid Control</legacyBold> (Msdatgrd.ocx).</caps:sentence>
                  <caps:sentence sentenceid="fa6da51a8ffa0a879305045a6d48cf62" id="tgt9" class="tgtSentence"> The Msdatgrd.ocx file is included with Visual Basic and is located in your \windows\system32 or \winnt\system32 directory.</caps:sentence>
                  <caps:sentence sentenceid="346f82a2570d0f0d1e709e0551b6ace0" id="tgt10" class="tgtSentence"> To add the DataGrid control to your Visual Basic toolbox pane, select <legacyBold>Components...</legacyBold> from the <legacyBold>Project</legacyBold> menu.</caps:sentence>
                  <caps:sentence sentenceid="8d1b8be4eab395f3ba8c3bbab25d7d55" id="tgt11" class="tgtSentence"> Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and then click <legacyBold>OK</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="40abfefae2329a033f36d70b254df9d8" id="tgt12" class="tgtSentence"> To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="0affeea4ab5cb9cfb8de2edf42145988" id="tgt13" class="tgtSentence">Create a <legacyBold>TextBox</legacyBold> on the form below the grid and set its properties as shown in the table.</caps:sentence>
                  <caps:sentence sentenceid="5f7b91f516e429d2c347dfbeb36407b6" id="tgt14" class="tgtSentence"> The form should resemble the following figure when you are finished.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence sentenceid="73a3034b06ea9380c57fd4b307c01015" id="tgt15" class="tgtSentence">Finally, copy the code listed in <legacyLink xlink:href="6da136c5-fa93-4fe6-9bf5-90f4d92441fb">HelloData Code</legacyLink>, and paste it into the code editor window of the form.</caps:sentence>
                  <caps:sentence sentenceid="5af02b91a6d15a89d18fc8179038d189" id="tgt16" class="tgtSentence"> Press <legacyBold>F5</legacyBold> to run the code.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
          <conclusion>
            <content>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="ad6f091bac794b58988e621d8d4f9333" id="tgt17" class="tgtSentence">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</caps:sentence>
                  <caps:sentence sentenceid="a9f981a0cef12512ac41efc0d7840403" id="tgt18" class="tgtSentence"> You should substitute these values with valid logon credentials for your server.</caps:sentence>
                  <caps:sentence sentenceid="580b17e063706a1f576897fdbc2860cb" id="tgt19" class="tgtSentence"> Also, substitute the "MySQLServer" value with the name of your server.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="d674c1e15a5f7f81ff83fc463ebbb7e1" id="tgt20" class="tgtSentence">For a detailed description of the code, see <legacyLink xlink:href="a2831d77-7040-4b73-bbae-fe0bf78107ed">Comments on HelloData</legacyLink>.</caps:sentence>
              </para>
            </content>
          </conclusion>
        </procedure>
        <mediaLink>
          <image xlink:href="7053f5d1-7f7b-495f-9dbc-591e9bbf15a8"></image>
        </mediaLink>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="5018d8a031f77f1125b5c315e71aa4d9" id="tgt21" class="tgtSentence">Control Type</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1a8db4c996d8ed8289da5f957879ab94" id="tgt22" class="tgtSentence">Property</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt23" class="tgtSentence">Value</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3fcdb73d36d54f2cc22d0f68e6b6e182" id="tgt24" class="tgtSentence">Form</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt25" class="tgtSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="60c0b53095f81a7bf551b30c93fd20dd" id="tgt26" class="tgtSentence">Form1</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b435e227d5dd201e1768b2bcb2e0aa81" id="tgt27" class="tgtSentence">Height</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1e0f65eb20acbfb27ee05ddc000b50ec" id="tgt28" class="tgtSentence">6500</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eaae26a6fb20ed3ef54fb23bfa0b1fcc" id="tgt29" class="tgtSentence">Width</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1e0f65eb20acbfb27ee05ddc000b50ec" id="tgt30" class="tgtSentence">6500</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="dfcae9e45ed1d78fa0d7a4e985ff5bb9" id="tgt31" class="tgtSentence">MS DataGrid</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt32" class="tgtSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2c1449332f21f93249e0b29bb2236ca8" id="tgt33" class="tgtSentence">grdDisplay1</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="5174307b9097d47b1a506bc8171c2bb3" id="tgt34" class="tgtSentence">TextBox</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt35" class="tgtSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="be5f6df3c31c4e7a7b0b7c8596d6655a" id="tgt36" class="tgtSentence">txtDisplay1</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="dfbce84c747c2c9d2627445fa0d8fa3b" id="tgt37" class="tgtSentence">Multiline</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b326b5062b2f0e69046810717534cb09" id="tgt38" class="tgtSentence">true</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="09b8d9b3f39ed04699f3fc327827aa86" id="tgt39" class="tgtSentence">Command Button</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt40" class="tgtSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a6d93286d7f117a64defea5e709423c2" id="tgt41" class="tgtSentence">cmdGetData</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7a7dc1cda8a5f2b4be2dcb815907d56e" id="tgt42" class="tgtSentence">Caption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8803c95c008a415d65ace7dc9988a974" id="tgt43" class="tgtSentence">Get Data</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="09b8d9b3f39ed04699f3fc327827aa86" id="tgt44" class="tgtSentence">Command Button</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt45" class="tgtSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4546ad0e008aadf385dc869a27b73c81" id="tgt46" class="tgtSentence">cmdExamineData</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7a7dc1cda8a5f2b4be2dcb815907d56e" id="tgt47" class="tgtSentence">Caption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="55dd7d018484861093cdc07936a60862" id="tgt48" class="tgtSentence">Examine Data</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="09b8d9b3f39ed04699f3fc327827aa86" id="tgt49" class="tgtSentence">Command Button</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt50" class="tgtSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="dde21365d8c58b52deb5ad36262d70b9" id="tgt51" class="tgtSentence">cmdEditData</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7a7dc1cda8a5f2b4be2dcb815907d56e" id="tgt52" class="tgtSentence">Caption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d03cfa3a71c444dbf87a40200ef4508e" id="tgt53" class="tgtSentence">Edit Data</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="09b8d9b3f39ed04699f3fc327827aa86" id="tgt54" class="tgtSentence">Command Button</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt55" class="tgtSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2445fa9453f25c72791d9678a2845333" id="tgt56" class="tgtSentence">cmdUpdateData</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7a7dc1cda8a5f2b4be2dcb815907d56e" id="tgt57" class="tgtSentence">Caption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="362edf8290fbfc2e51d4eafdca814d99" id="tgt58" class="tgtSentence">Update Data</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This simple application steps through each of the four major ADO operations: getting, examining, editing, and updating data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These operations are performed against the Northwind sample database included with Microsoft® SQL Server.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> To focus on the fundamentals of ADO and to prevent code clutter, error handling in the example is minimal.</caps:sentence>
        </para>
        <procedure>
          <title>
            <caps:sentence id="src4" class="srcSentence">To run HelloData</caps:sentence>
          </title>
          <steps class="ordered">
            <step>
              <content>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Create a new Standard EXE Visual Basic project that references the ADO library.</caps:sentence>
                  <caps:sentence id="src6" class="srcSentence"> For more information, see <legacyLink xlink:href="573f8f27-babd-4e2f-bf9a-270ee7024975">Referencing the ADO Libraries</legacyLink>.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Create four command buttons at the top of the form, setting the <legacyBold>Name</legacyBold> and <legacyBold>Caption</legacyBold> properties to the values shown in the table at the end of this topic.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Below the buttons, add a <legacyBold>Microsoft DataGrid Control</legacyBold> (Msdatgrd.ocx).</caps:sentence>
                  <caps:sentence id="src9" class="srcSentence"> The Msdatgrd.ocx file is included with Visual Basic and is located in your \windows\system32 or \winnt\system32 directory.</caps:sentence>
                  <caps:sentence id="src10" class="srcSentence"> To add the DataGrid control to your Visual Basic toolbox pane, select <legacyBold>Components...</legacyBold> from the <legacyBold>Project</legacyBold> menu.</caps:sentence>
                  <caps:sentence id="src11" class="srcSentence"> Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and then click <legacyBold>OK</legacyBold>.</caps:sentence>
                  <caps:sentence id="src12" class="srcSentence"> To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Create a <legacyBold>TextBox</legacyBold> on the form below the grid and set its properties as shown in the table.</caps:sentence>
                  <caps:sentence id="src14" class="srcSentence"> The form should resemble the following figure when you are finished.</caps:sentence>
                </para>
              </content>
            </step>
            <step>
              <content>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Finally, copy the code listed in <legacyLink xlink:href="6da136c5-fa93-4fe6-9bf5-90f4d92441fb">HelloData Code</legacyLink>, and paste it into the code editor window of the form.</caps:sentence>
                  <caps:sentence id="src16" class="srcSentence"> Press <legacyBold>F5</legacyBold> to run the code.</caps:sentence>
                </para>
              </content>
            </step>
          </steps>
          <conclusion>
            <content>
              <alert class="note">
                <para>
                  <caps:sentence id="src17" class="srcSentence">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</caps:sentence>
                  <caps:sentence id="src18" class="srcSentence"> You should substitute these values with valid logon credentials for your server.</caps:sentence>
                  <caps:sentence id="src19" class="srcSentence"> Also, substitute the "MySQLServer" value with the name of your server.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src20" class="srcSentence">For a detailed description of the code, see <legacyLink xlink:href="a2831d77-7040-4b73-bbae-fe0bf78107ed">Comments on HelloData</legacyLink>.</caps:sentence>
              </para>
            </content>
          </conclusion>
        </procedure>
        <mediaLink>
          <image xlink:href="7053f5d1-7f7b-495f-9dbc-591e9bbf15a8"></image>
        </mediaLink>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Control Type</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Property</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Value</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Form</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">Form1</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Height</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">6500</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">Width</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">6500</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">MS DataGrid</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">grdDisplay1</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">TextBox</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">txtDisplay1</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Multiline</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">true</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">Command Button</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">cmdGetData</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">Caption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">Get Data</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src44" class="srcSentence">Command Button</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">cmdExamineData</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">Caption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src48" class="srcSentence">Examine Data</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">Command Button</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src50" class="srcSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src51" class="srcSentence">cmdEditData</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">Caption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">Edit Data</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">Command Button</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">Name</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">cmdUpdateData</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">Caption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src58" class="srcSentence">Update Data</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
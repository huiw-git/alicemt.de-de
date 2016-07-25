---
title: "Comments on HelloData"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a2831d77-7040-4b73-bbae-fe0bf78107ed
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
# Comments on HelloData
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d2dc0f46813219df445eb1c88a8d29a3" id="tgt1" class="tgtSentence">The HelloData application steps through the basic operations of a typical ADO application: getting, examining, editing, and updating data.</caps:sentence>
          <caps:sentence sentenceid="f9c9fc6aaa534c9069b5423f720154df" id="tgt2" class="tgtSentence"> When you start the application, click the first button, <legacyBold>Get Data</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="a6762ec40c64a0c11779a1af28e9c4e1" id="tgt3" class="tgtSentence"> This will run the <legacyBold>GetData</legacyBold> subroutine.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="b0a72918ae398652fac8e07449bcce8c" id="tgt4" class="tgtSentence">GetData</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="006937217dc5850695d915ebcd3612bd" id="tgt5" class="tgtSentence">
              <legacyBold>GetData</legacyBold> places a valid connection string into a module-level variable, <legacyItalic>m_sConnStr</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="64a41fb6ec7bc6dd9c688c5b10be6cda" id="tgt6" class="tgtSentence"> For more information about connection strings, see <legacyLink xlink:href="14eae122-2d1e-40c8-b88e-b7cb8dfbc93b">Creating the Connection String</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="88d0e6af972edab3bf72b96065074c8b" id="tgt7" class="tgtSentence">Assign an error handler using a Visual Basic <legacyBold>OnError</legacyBold> statement.</caps:sentence>
            <caps:sentence sentenceid="4a570e4d77a0464d5d5783c9ffff8b52" id="tgt8" class="tgtSentence"> For more information about error handling in ADO, see <legacyLink xlink:href="4909e413-f3b0-4183-8ad3-67b1434df742">Error Handling</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="c94fe8afe101b87d7e323a3cf782c0ea" id="tgt9" class="tgtSentence"> A new <legacyBold>Connection</legacyBold> object is created, and the <legacyBold>CursorLocation</legacyBold> property is set to <legacyBold>adUseClient</legacyBold> because the HelloData example creates a <legacyItalic>disconnected Recordset</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="8f6ef2329bf184f0d264c9e65afc90df" id="tgt10" class="tgtSentence"> This means that as soon as the data has been fetched from the data source, the physical connection with the data source is broken, but you can still work with the data that is cached locally in your <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b50f43182e3d82a1994fd7df9b2a8cc4" id="tgt11" class="tgtSentence">After the connection has been opened, assign an SQL string to a variable (sSQL).</caps:sentence>
            <caps:sentence sentenceid="2ed8bdc8a8d45a075e18d1f9d5e2ec93" id="tgt12" class="tgtSentence"> Then create an instance of a new <legacyBold>Recordset</legacyBold> object, <codeInline>m_oRecordset1</codeInline>.</caps:sentence>
            <caps:sentence sentenceid="32639470f6932ed0cd8a3866f2b5a0f5" id="tgt13" class="tgtSentence"> In the next line of code, open the <legacyBold>Recordset</legacyBold> over the existing <legacyBold>Connection</legacyBold>, passing in <codeInline>sSQL</codeInline> as the source of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="a4f1106885b234276042f8887288a14c" id="tgt14" class="tgtSentence"> You help ADO in making the determination that the SQL string you have passed as the source for the <legacyBold>Recordset</legacyBold> is a textual definition of a command by passing <legacyBold>adCmdText</legacyBold> in the final argument to the <legacyBold>Recordset</legacyBold> <legacyBold>Open</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="aedee920c226b9a002a9a42a86cc65d5" id="tgt15" class="tgtSentence"> This line also sets the <legacyBold>LockType</legacyBold> and <legacyBold>CursorType</legacyBold> associated with the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d3c740aa3831d4d1218cf5fecf8d1dd5" id="tgt16" class="tgtSentence">The next line of code sets the <legacyBold>MarshalOptions</legacyBold> property equal to <legacyBold>adMarshalModifiedOnly</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="610d0d3a30549113aa8d8e84915b9ddb" id="tgt17" class="tgtSentence">
              <legacyBold>MarshalOptions</legacyBold> indicates which records should be marshaled to the middle tier (or Web server).</caps:sentence>
            <caps:sentence sentenceid="734d7d50da6dcae4ec2c7b12bdd155d6" id="tgt18" class="tgtSentence"> For more information about marshaling, see the COM documentation.</caps:sentence>
            <caps:sentence sentenceid="d6867507ae3776faf562a5cc97348d3d" id="tgt19" class="tgtSentence"> When you use <legacyBold>adMarshalModifiedOnly</legacyBold> with a client-side cursor (<legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> = <legacyBold>adUseClient</legacyBold>), only records that have been modified on the client are written back to the middle tier.</caps:sentence>
            <caps:sentence sentenceid="c08b1ecc0ba32042a4f13ef2468c38c4" id="tgt20" class="tgtSentence"> Setting <legacyBold>MarshalOptions</legacyBold> to <legacyBold>adMarshalModifiedOnly</legacyBold> can improve performance because fewer rows are marshaled.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="72f1f86ea315a55e7bcc87698f0b723b" id="tgt21" class="tgtSentence">Next, disconnect the <legacyBold>Recordset</legacyBold> by setting its <legacyBold>ActiveConnection</legacyBold> property equal to <legacyBold>Nothing</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="0fe36c5fe6da2527b169ee6c909a5b7a" id="tgt22" class="tgtSentence"> For more information, see the section "Disconnecting and Reconnecting the Recordset" in <link xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1589365713421b5ae3a94259e5a5c1df" id="tgt23" class="tgtSentence">Close the connection to the data source and destroy the existing <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="9ecc4c8ee9ddaddf2e850f39d3255386" id="tgt24" class="tgtSentence"> This releases the resources that it consumed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d685a665b64fa897b4084247b78a07bd" id="tgt25" class="tgtSentence">The final step is to set the <legacyBold>Recordset</legacyBold> as the <legacyBold>DataSource</legacyBold> for the Microsoft DataGrid Control on the form so that you can easily display the data from the <legacyBold>Recordset</legacyBold> on the form.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="17c1b21c427e56d59f68cb8cc231f3ec" id="tgt26" class="tgtSentence">Click the second button, <legacyBold>Examine Data</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="86568f0e6bffef92a3f9f75e5b7507f2" id="tgt27" class="tgtSentence"> This runs the <legacyBold>ExamineData</legacyBold> subroutine.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="24d522a9b15f362750df77ffbe0389e9" id="tgt28" class="tgtSentence">ExamineData</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7ce4dca9e749635904d70d9b3275643d" id="tgt29" class="tgtSentence">ExamineData uses various methods and properties of the <legacyBold>Recordset</legacyBold> object to display information about the data in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="15d8ab7f86302f5ec66158209eb790ad" id="tgt30" class="tgtSentence"> It reports the number of records by using the <legacyBold>RecordCount</legacyBold> property.</caps:sentence>
            <caps:sentence sentenceid="27cd91cd901bf088673adc95a48698f6" id="tgt31" class="tgtSentence"> It loops through the <legacyBold>Recordset</legacyBold> and prints the value of the <legacyBold>AbsolutePosition</legacyBold> property in the display text box on the form.</caps:sentence>
            <caps:sentence sentenceid="ae4e15a07529fc6db9645d7fb7858f91" id="tgt32" class="tgtSentence"> Also while in the loop, the value of the <legacyBold>Bookmark</legacyBold> property for the third record is placed into a variant variable, <legacyItalic>vBookmark</legacyItalic>, for later use.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1568e78be240eb41cb99a23839dc2c33" id="tgt33" class="tgtSentence">The routine navigates directly back to the third record using the bookmark variable that it stored earlier.</caps:sentence>
            <caps:sentence sentenceid="5862ac5b17c00a529ac4458029cc48ba" id="tgt34" class="tgtSentence"> The routine calls the <legacyBold>WalkFields</legacyBold> subroutine, which loops through the <legacyBold>Fields</legacyBold> collection of the <legacyBold>Recordset</legacyBold> and displays details about each <legacyBold>Field</legacyBold> in the collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8f9b1c3f26242cd76b9d5078ff07d80b" id="tgt35" class="tgtSentence">Finally, <legacyBold>ExamineData</legacyBold> uses the <legacyBold>Filter</legacyBold> property of the <legacyBold>Recordset</legacyBold> to screen for only those records with a <legacyBold>CategoryId</legacyBold> equal to 2.</caps:sentence>
            <caps:sentence sentenceid="2d192348fa85904d30119080a83b82da" id="tgt36" class="tgtSentence"> The result of applying this filter is immediately visible in the display grid on the form.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="15b24b1e14374f99c88080f3b8fb7c00" id="tgt37" class="tgtSentence">For more information about the functionality shown in the <legacyBold>ExamineData</legacyBold> subroutine, see <legacyLink xlink:href="de1d74af-89b6-4f3f-a8c9-07c3e2b3c9a5">Examining Data</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a86ca05aeb5b6c125546960f0f658beb" id="tgt38" class="tgtSentence">Next, click the third button, <legacyBold>Edit Data</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="f3f6ce285d9c6a10a223e271de52b2e2" id="tgt39" class="tgtSentence"> This will run the <legacyBold>EditData</legacyBold> subroutine.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a6e275da3f1161e4504e6dbbb2f81fd1" id="tgt40" class="tgtSentence">EditData</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="73c1932c747772d8c6fb409a01b4990f" id="tgt41" class="tgtSentence">When the code enters the <legacyBold>EditData</legacyBold> subroutine, the <legacyBold>Recordset</legacyBold> is still filtered on <legacyBold>CategoryId</legacyBold> equal to 2, so that only those items that meet the filter criteria are visible.</caps:sentence>
            <caps:sentence sentenceid="cc92058aacdd25a66e2f57dd6341d10d" id="tgt42" class="tgtSentence"> It first loops through the <legacyBold>Recordset</legacyBold> and increases the price of each visible item in the <legacyBold>Recordset</legacyBold> by 10 percent.</caps:sentence>
            <caps:sentence sentenceid="623c2886f7dfb25c06e5339f1e1a690c" id="tgt43" class="tgtSentence"> The value of the <legacyBold>Price</legacyBold> field is changed by setting the <legacyBold>Value</legacyBold> property for that field equal to a new, valid amount.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="312040396f539b7e569091b2f46f2cd5" id="tgt44" class="tgtSentence">Remember that the <legacyBold>Recordset</legacyBold> is disconnected from the data source.</caps:sentence>
            <caps:sentence sentenceid="a65aef698658e779e12cb34e893b0edc" id="tgt45" class="tgtSentence"> The changes that were made in <legacyBold>EditData</legacyBold> are made only to the locally cached copy of the data.</caps:sentence>
            <caps:sentence sentenceid="fd013a048e445079797c2cd47f4957df" id="tgt46" class="tgtSentence"> For more information, see <legacyLink xlink:href="ef514f85-c446-4f05-824e-c9313b2ffae1">Editing Data</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d2c48898fab5ac9f692d7a708e9ec5df" id="tgt47" class="tgtSentence">The changes will not be made on the data source until you click the fourth button, <legacyBold>Update Data</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="3e27e6bf451e902772911b27b554e008" id="tgt48" class="tgtSentence"> This will run the <legacyBold>UpdateData</legacyBold> subroutine.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="59691edb6e8b83def0f05a4b1297ea9c" id="tgt49" class="tgtSentence">UpdateData</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="46ec9f1b1db0087259d1e0d178a5b6a1" id="tgt50" class="tgtSentence">UpdateData first removes the filter that has been applied to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="32f65ba8b263b0364bb4fd86ca1b9f6f" id="tgt51" class="tgtSentence"> The code removes and resets <codeInline>m_oRecordset1</codeInline> as the <legacyBold>DataSource</legacyBold> for the Microsoft Bound DataGrid on the form so that the unfiltered <legacyBold>Recordset</legacyBold> appears in the grid.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="54b257bbdb1f7cd7538e77ea4d40e1d5" id="tgt52" class="tgtSentence">The code then checks to see whether you can move backward in the <legacyBold>Recordset</legacyBold> by using the <legacyBold>Supports</legacyBold> method with the <legacyBold>adMovePrevious</legacyBold> argument.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="60964c5124f9ec5b3317f7fb2e8eb370" id="tgt53" class="tgtSentence">The routine moves to the first record using the <legacyBold>MoveFirst</legacyBold> method and displays the field's original and current values, by using the <legacyBold>OriginalValue</legacyBold> and <legacyBold>Value</legacyBold> properties of the <legacyBold>Field</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="ccd9052bac2413ec519856204511a465" id="tgt54" class="tgtSentence"> These properties, together with the <legacyBold>UnderlyingValue</legacyBold> property (not used here), are discussed in <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="be0bfe52e2b752237c3c8aa13673f090" id="tgt55" class="tgtSentence">Next, a new <legacyBold>Connection</legacyBold> object is created and used to reestablish a connection to the data source.</caps:sentence>
            <caps:sentence sentenceid="32b999fcf242996656389828c80e9ba3" id="tgt56" class="tgtSentence"> You reconnect the <legacyBold>Recordset</legacyBold> to the data source by setting the new <legacyBold>Connection</legacyBold> as the <legacyBold>ActiveConnection</legacyBold> for the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="568c7b785853721abdd7464a15e2833f" id="tgt57" class="tgtSentence"> To send the updates to the server, the code calls <legacyBold>UpdateBatch</legacyBold> on the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="09780502fd5383a9604f13619e2dcd82" id="tgt58" class="tgtSentence">If the batch update succeeds, a module-level flag variable, <codeInline>m_flgPriceUpdated</codeInline>, is set to True.</caps:sentence>
            <caps:sentence sentenceid="0f66d2bf41ec04406364885da817a709" id="tgt59" class="tgtSentence"> This will remind you later to clean up all the changes that were made to the database.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="03f03115cee6108ea05caed3eeb83ff8" id="tgt60" class="tgtSentence">Finally, the code moves back to the first record in the <legacyBold>Recordset</legacyBold> and displays the original and current values.</caps:sentence>
            <caps:sentence sentenceid="b8ab5fd2fd8038fd8bf79c4d8361c827" id="tgt61" class="tgtSentence"> The values are the same after the call to <legacyBold>UpdateBatch</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5d4faa011eb5f810a6cf33d149e25a4a" id="tgt62" class="tgtSentence">For detailed information about how to update data, including what to do when data on the server changes while your <legacyBold>Recordset</legacyBold> is disconnected, see <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="49d7c91c7d0aede58f0da3259597646c" id="tgt63" class="tgtSentence">Form_Unload</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d8d8e86f09ff81a21a3f7c07fbf1cf39" id="tgt64" class="tgtSentence">The <legacyBold>Form_Unload</legacyBold> subroutine is important for several reasons.</caps:sentence>
            <caps:sentence sentenceid="eb8cdcc077e19322a4287642fee1e7ec" id="tgt65" class="tgtSentence"> First, because this is a sample application, Form_Unload cleans up the changes that were made to the database before the application exits.</caps:sentence>
            <caps:sentence sentenceid="8be032eb20fe6853fe064871f3ef4b54" id="tgt66" class="tgtSentence"> Second, the code shows how a command can be executed directly from an open <legacyBold>Connection</legacyBold> object by using the <legacyBold>Execute</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="6780cb76ee53eb1e7774f4a744be836f" id="tgt67" class="tgtSentence"> Finally, it shows an example of executing a non-row–returning query (an UPDATE query) against the data source.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The HelloData application steps through the basic operations of a typical ADO application: getting, examining, editing, and updating data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When you start the application, click the first button, <legacyBold>Get Data</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This will run the <legacyBold>GetData</legacyBold> subroutine.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">GetData</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">
              <legacyBold>GetData</legacyBold> places a valid connection string into a module-level variable, <legacyItalic>m_sConnStr</legacyItalic>.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For more information about connection strings, see <legacyLink xlink:href="14eae122-2d1e-40c8-b88e-b7cb8dfbc93b">Creating the Connection String</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">Assign an error handler using a Visual Basic <legacyBold>OnError</legacyBold> statement.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> For more information about error handling in ADO, see <legacyLink xlink:href="4909e413-f3b0-4183-8ad3-67b1434df742">Error Handling</legacyLink>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> A new <legacyBold>Connection</legacyBold> object is created, and the <legacyBold>CursorLocation</legacyBold> property is set to <legacyBold>adUseClient</legacyBold> because the HelloData example creates a <legacyItalic>disconnected Recordset</legacyItalic>.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> This means that as soon as the data has been fetched from the data source, the physical connection with the data source is broken, but you can still work with the data that is cached locally in your <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">After the connection has been opened, assign an SQL string to a variable (sSQL).</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Then create an instance of a new <legacyBold>Recordset</legacyBold> object, <codeInline>m_oRecordset1</codeInline>.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> In the next line of code, open the <legacyBold>Recordset</legacyBold> over the existing <legacyBold>Connection</legacyBold>, passing in <codeInline>sSQL</codeInline> as the source of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> You help ADO in making the determination that the SQL string you have passed as the source for the <legacyBold>Recordset</legacyBold> is a textual definition of a command by passing <legacyBold>adCmdText</legacyBold> in the final argument to the <legacyBold>Recordset</legacyBold> <legacyBold>Open</legacyBold> method.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> This line also sets the <legacyBold>LockType</legacyBold> and <legacyBold>CursorType</legacyBold> associated with the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">The next line of code sets the <legacyBold>MarshalOptions</legacyBold> property equal to <legacyBold>adMarshalModifiedOnly</legacyBold>.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence">
              <legacyBold>MarshalOptions</legacyBold> indicates which records should be marshaled to the middle tier (or Web server).</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> For more information about marshaling, see the COM documentation.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> When you use <legacyBold>adMarshalModifiedOnly</legacyBold> with a client-side cursor (<legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> = <legacyBold>adUseClient</legacyBold>), only records that have been modified on the client are written back to the middle tier.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Setting <legacyBold>MarshalOptions</legacyBold> to <legacyBold>adMarshalModifiedOnly</legacyBold> can improve performance because fewer rows are marshaled.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">Next, disconnect the <legacyBold>Recordset</legacyBold> by setting its <legacyBold>ActiveConnection</legacyBold> property equal to <legacyBold>Nothing</legacyBold>.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> For more information, see the section "Disconnecting and Reconnecting the Recordset" in <link xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">Close the connection to the data source and destroy the existing <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> This releases the resources that it consumed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">The final step is to set the <legacyBold>Recordset</legacyBold> as the <legacyBold>DataSource</legacyBold> for the Microsoft DataGrid Control on the form so that you can easily display the data from the <legacyBold>Recordset</legacyBold> on the form.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src26" class="srcSentence">Click the second button, <legacyBold>Examine Data</legacyBold>.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> This runs the <legacyBold>ExamineData</legacyBold> subroutine.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">ExamineData</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">ExamineData uses various methods and properties of the <legacyBold>Recordset</legacyBold> object to display information about the data in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> It reports the number of records by using the <legacyBold>RecordCount</legacyBold> property.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> It loops through the <legacyBold>Recordset</legacyBold> and prints the value of the <legacyBold>AbsolutePosition</legacyBold> property in the display text box on the form.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> Also while in the loop, the value of the <legacyBold>Bookmark</legacyBold> property for the third record is placed into a variant variable, <legacyItalic>vBookmark</legacyItalic>, for later use.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src33" class="srcSentence">The routine navigates directly back to the third record using the bookmark variable that it stored earlier.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> The routine calls the <legacyBold>WalkFields</legacyBold> subroutine, which loops through the <legacyBold>Fields</legacyBold> collection of the <legacyBold>Recordset</legacyBold> and displays details about each <legacyBold>Field</legacyBold> in the collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src35" class="srcSentence">Finally, <legacyBold>ExamineData</legacyBold> uses the <legacyBold>Filter</legacyBold> property of the <legacyBold>Recordset</legacyBold> to screen for only those records with a <legacyBold>CategoryId</legacyBold> equal to 2.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> The result of applying this filter is immediately visible in the display grid on the form.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src37" class="srcSentence">For more information about the functionality shown in the <legacyBold>ExamineData</legacyBold> subroutine, see <legacyLink xlink:href="de1d74af-89b6-4f3f-a8c9-07c3e2b3c9a5">Examining Data</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src38" class="srcSentence">Next, click the third button, <legacyBold>Edit Data</legacyBold>.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> This will run the <legacyBold>EditData</legacyBold> subroutine.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src40" class="srcSentence">EditData</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src41" class="srcSentence">When the code enters the <legacyBold>EditData</legacyBold> subroutine, the <legacyBold>Recordset</legacyBold> is still filtered on <legacyBold>CategoryId</legacyBold> equal to 2, so that only those items that meet the filter criteria are visible.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> It first loops through the <legacyBold>Recordset</legacyBold> and increases the price of each visible item in the <legacyBold>Recordset</legacyBold> by 10 percent.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> The value of the <legacyBold>Price</legacyBold> field is changed by setting the <legacyBold>Value</legacyBold> property for that field equal to a new, valid amount.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src44" class="srcSentence">Remember that the <legacyBold>Recordset</legacyBold> is disconnected from the data source.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> The changes that were made in <legacyBold>EditData</legacyBold> are made only to the locally cached copy of the data.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> For more information, see <legacyLink xlink:href="ef514f85-c446-4f05-824e-c9313b2ffae1">Editing Data</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src47" class="srcSentence">The changes will not be made on the data source until you click the fourth button, <legacyBold>Update Data</legacyBold>.</caps:sentence>
            <caps:sentence id="src48" class="srcSentence"> This will run the <legacyBold>UpdateData</legacyBold> subroutine.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src49" class="srcSentence">UpdateData</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src50" class="srcSentence">UpdateData first removes the filter that has been applied to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src51" class="srcSentence"> The code removes and resets <codeInline>m_oRecordset1</codeInline> as the <legacyBold>DataSource</legacyBold> for the Microsoft Bound DataGrid on the form so that the unfiltered <legacyBold>Recordset</legacyBold> appears in the grid.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src52" class="srcSentence">The code then checks to see whether you can move backward in the <legacyBold>Recordset</legacyBold> by using the <legacyBold>Supports</legacyBold> method with the <legacyBold>adMovePrevious</legacyBold> argument.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src53" class="srcSentence">The routine moves to the first record using the <legacyBold>MoveFirst</legacyBold> method and displays the field's original and current values, by using the <legacyBold>OriginalValue</legacyBold> and <legacyBold>Value</legacyBold> properties of the <legacyBold>Field</legacyBold> object.</caps:sentence>
            <caps:sentence id="src54" class="srcSentence"> These properties, together with the <legacyBold>UnderlyingValue</legacyBold> property (not used here), are discussed in <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src55" class="srcSentence">Next, a new <legacyBold>Connection</legacyBold> object is created and used to reestablish a connection to the data source.</caps:sentence>
            <caps:sentence id="src56" class="srcSentence"> You reconnect the <legacyBold>Recordset</legacyBold> to the data source by setting the new <legacyBold>Connection</legacyBold> as the <legacyBold>ActiveConnection</legacyBold> for the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src57" class="srcSentence"> To send the updates to the server, the code calls <legacyBold>UpdateBatch</legacyBold> on the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src58" class="srcSentence">If the batch update succeeds, a module-level flag variable, <codeInline>m_flgPriceUpdated</codeInline>, is set to True.</caps:sentence>
            <caps:sentence id="src59" class="srcSentence"> This will remind you later to clean up all the changes that were made to the database.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src60" class="srcSentence">Finally, the code moves back to the first record in the <legacyBold>Recordset</legacyBold> and displays the original and current values.</caps:sentence>
            <caps:sentence id="src61" class="srcSentence"> The values are the same after the call to <legacyBold>UpdateBatch</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src62" class="srcSentence">For detailed information about how to update data, including what to do when data on the server changes while your <legacyBold>Recordset</legacyBold> is disconnected, see <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src63" class="srcSentence">Form_Unload</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src64" class="srcSentence">The <legacyBold>Form_Unload</legacyBold> subroutine is important for several reasons.</caps:sentence>
            <caps:sentence id="src65" class="srcSentence"> First, because this is a sample application, Form_Unload cleans up the changes that were made to the database before the application exits.</caps:sentence>
            <caps:sentence id="src66" class="srcSentence"> Second, the code shows how a command can be executed directly from an open <legacyBold>Connection</legacyBold> object by using the <legacyBold>Execute</legacyBold> method.</caps:sentence>
            <caps:sentence id="src67" class="srcSentence"> Finally, it shows an example of executing a non-row–returning query (an UPDATE query) against the data source.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
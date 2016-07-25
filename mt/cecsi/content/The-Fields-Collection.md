---
title: "The Fields Collection"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 574cf36e-e5f5-403b-983c-749ef93c108f
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
# The Fields Collection
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="12871468c17bce86708dc4ac41e133c6" id="tgt1" class="tgtSentence">The <legacyBold>Fields</legacyBold> collection is one of ADO's intrinsic collections.</caps:sentence>
          <caps:sentence sentenceid="cab2228676374dc246b6486fe97bbbe3" id="tgt2" class="tgtSentence"> A collection is an ordered set of items that can be referred to as a unit.</caps:sentence>
          <caps:sentence sentenceid="d425f612882bcc4788a7f771eb10082c" id="tgt3" class="tgtSentence"> For more information about ADO collections, see <legacyLink xlink:href="7a745aae-9372-49b6-8dae-b9c93e5f3216">The ADO Object Model</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3e9773472439dd902e5c5bc4a7706458" id="tgt4" class="tgtSentence">The <legacyBold>Fields</legacyBold> collection contains a <legacyBold>Field</legacyBold> object for every field (column) in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="7135d198370854cf23a1ac4cc638aacc" id="tgt5" class="tgtSentence"> Like all ADO collections, it has <legacyBold>Count</legacyBold> and <legacyBold>Item</legacyBold> properties, as well as <legacyBold>Append</legacyBold> and <legacyBold>Refresh</legacyBold> methods.</caps:sentence>
          <caps:sentence sentenceid="8eeeabdb082335f5c8754c7b732cc8ee" id="tgt6" class="tgtSentence"> It also has <legacyBold>CancelUpdate</legacyBold>, <legacyBold>Delete</legacyBold>, <legacyBold>Resync</legacyBold>, and <legacyBold>Update</legacyBold> methods, which are not available to other ADO collections.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="e4f6778cf7023f5e02e7b8722c9a6c94" id="tgt7" class="tgtSentence">Examining the Fields Collection</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="38186839792c89c8f604b2386141fbb0" id="tgt8" class="tgtSentence">Consider the <legacyBold>Fields</legacyBold> collection of the sample <legacyBold>Recordset</legacyBold> introduced in this section.</caps:sentence>
            <caps:sentence sentenceid="806ac6b1b5867a6602f12de4a5c8b608" id="tgt9" class="tgtSentence"> The sample <legacyBold>Recordset</legacyBold> was derived from the SQL statement</caps:sentence>
          </para>
          <code>SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7</code>
          <para>
            <caps:sentence sentenceid="e67846254f75c356c5df57aa57322fe7" id="tgt10" class="tgtSentence">Thus, you should find that the <legacyBold>Recordset</legacyBold> <legacyBold>Fields</legacyBold> collection contains three fields.</caps:sentence>
          </para>
          <code>'BeginWalkFields
    Dim objFields As ADODB.Fields
    Dim intLoop As Integer
    
    objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText
    
    Set objFields = objRs.Fields
    
    For intLoop = 0 To (objFields.Count - 1)
        Debug.Print objFields.Item(intLoop).Name
    Next
'EndWalkFields</code>
          <para>
            <caps:sentence sentenceid="bcc5a0cffb17cdb32e43b0536d77410a" id="tgt11" class="tgtSentence">This code simply determines the number of <legacyBold>Field</legacyBold> objects in the <legacyBold>Fields</legacyBold> collection using the <legacyBold>Count</legacyBold> property and loops through the collection, returning the value of the <legacyBold>Name</legacyBold> property for each <legacyBold>Field</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="db5c9af6cc89284eaceb4c4ba0e819a7" id="tgt12" class="tgtSentence"> You can use many more <legacyBold>Field</legacyBold> properties to get information about a field.</caps:sentence>
            <caps:sentence sentenceid="262c95b150226c00d1bd23d8f0f6137d" id="tgt13" class="tgtSentence"> For more information about querying a <legacyBold>Field</legacyBold>, see <legacyLink xlink:href="7d1c4ad5-4be3-42ab-b516-e7133ca300bc">The Field Object</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5cc4f1d11f1480738168e4d08273bdf4" id="tgt14" class="tgtSentence">Counting Columns</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c9655c33d78b473fbe11fb8ccb49ecc5" id="tgt15" class="tgtSentence">As you might expect, the <legacyBold>Count</legacyBold> property returns the actual number of <legacyBold>Field</legacyBold> objects in the <legacyBold>Fields</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="a4e982e86d525af23f0aa738e0a53215" id="tgt16" class="tgtSentence"> Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the <legacyBold>Count</legacyBold> property minus 1.</caps:sentence>
            <caps:sentence sentenceid="49b9a08247d21e1253c732bd51da85b6" id="tgt17" class="tgtSentence"> If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the <legacyBold>Count</legacyBold> property, use the <legacyBold>For</legacyBold> <legacyBold>Each...Next</legacyBold> command.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="94b10d742468366063cd5f943209d201" id="tgt18" class="tgtSentence">If the <legacyBold>Count</legacyBold> property is zero, there are no objects in the collection.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ccf415a8762b8d23b65db1e057b1cab9" id="tgt19" class="tgtSentence">Getting to the Field</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="887e09b3f2ec97664663d44e22d8336f" id="tgt20" class="tgtSentence">As with any ADO collection, the <legacyBold>Item</legacyBold> property is the default property of the collection.</caps:sentence>
            <caps:sentence sentenceid="c2e3b6c95f4a1e85f392fd8da17cc871" id="tgt21" class="tgtSentence"> It returns the individual <legacyBold>Field</legacyBold> object specified by the name or index passed to it.</caps:sentence>
            <caps:sentence sentenceid="f54ee776d326fe1d8cba3ac0f2a056c0" id="tgt22" class="tgtSentence"> Therefore, the following statements are equivalent for the sample <legacyBold>Recordset</legacyBold>:</caps:sentence>
          </para>
          <code>objField = objRecordset.Fields.Item("ProductID")
objField = objRecordset.Fields("ProductID")
objField = objRecordset.Fields.Item(0)
objField = objRecordset.Fields(0)</code>
          <para>
            <caps:sentence sentenceid="709eef23f248f318f1ffaa0f9c0bb289" id="tgt23" class="tgtSentence">If these methods are equivalent, which is best?</caps:sentence>
            <caps:sentence sentenceid="b39c2091bb55e3bf397eafac88d9987d" id="tgt24" class="tgtSentence"> It depends.</caps:sentence>
            <caps:sentence sentenceid="d2708168e541de5b123082e53ecd8310" id="tgt25" class="tgtSentence"> Using an index to retrieve a <legacyBold>Field</legacyBold> from the collection is faster because it accesses the <legacyBold>Field</legacyBold> directly without having to perform a string lookup.</caps:sentence>
            <caps:sentence sentenceid="36ee5f7beda9e5952c56c80b8d09dc9a" id="tgt26" class="tgtSentence"> On the other hand, the order of <legacyBold>Fields</legacyBold> within the collection must be known, and if the order changes, the reference to the <legacyBold>Field's</legacyBold> index will have to be changed wherever it occurs.</caps:sentence>
            <caps:sentence sentenceid="e90d1953c071e95762985880f14712cb" id="tgt27" class="tgtSentence"> Although slightly slower, using the name of the <legacyBold>Field</legacyBold> is more flexible because it doesn't depend on the order of the <legacyBold>Fields</legacyBold> in the collection.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="11a807d4a9e4d8c49b9439983d4b587b" id="tgt28" class="tgtSentence">Using the Refresh Method</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1a8178f2c484e3a642adcaa87c240e06" id="tgt29" class="tgtSentence">Unlike some other ADO collections, using the <legacyBold>Refresh</legacyBold> method on the <legacyBold>Fields</legacyBold> collection has no visible effect.</caps:sentence>
            <caps:sentence sentenceid="9402a7fafb188cd8750c1a584e8e6c19" id="tgt30" class="tgtSentence"> To retrieve changes from the underlying database structure, you must use either the <legacyBold>Requery</legacyBold> method, or if the <legacyBold>Recordset</legacyBold> object does not support bookmarks, the <legacyBold>MoveFirst</legacyBold> method, which will cause the command to be executed against the provider again.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d0eba4e879984cc68452dcd0b4d1aef1" id="tgt31" class="tgtSentence">Adding Fields to a Recordset</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8f360547dd53dc0287a5c035ad3df271" id="tgt32" class="tgtSentence">The <legacyBold>Append</legacyBold> method is used to add fields to a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="307b5065f6e969fb83975b12544a64c4" id="tgt33" class="tgtSentence">You can use the <legacyBold>Append</legacyBold> method to fabricate a <legacyBold>Recordset</legacyBold> programmatically without opening a connection to a data source.</caps:sentence>
            <caps:sentence sentenceid="ae13c590c975da13547fd6a4527cd867" id="tgt34" class="tgtSentence"> A run-time error will occur if the <legacyBold>Append</legacyBold> method is called on the <legacyBold>Fields</legacyBold> collection of an open <legacyBold>Recordset</legacyBold> or on a <legacyBold>Recordset</legacyBold> where the <legacyBold>ActiveConnection</legacyBold> property has been set.</caps:sentence>
            <caps:sentence sentenceid="8f2bb05654c90cddfefaac775eba1e56" id="tgt35" class="tgtSentence"> You can append fields only to a <legacyBold>Recordset</legacyBold> that is not open and has not yet been connected to a data source.</caps:sentence>
            <caps:sentence sentenceid="ee0a7e884bd926f84e6098fc4391faba" id="tgt36" class="tgtSentence"> However, to specify values for the newly appended <legacyBold>Fields</legacyBold>, the <legacyBold>Recordset</legacyBold> must first be opened.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="19c99032a5363e5749eca3f0cf02f437" id="tgt37" class="tgtSentence">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface.</caps:sentence>
            <caps:sentence sentenceid="e56ffecd3efbd9193e562f850a3e6d82" id="tgt38" class="tgtSentence"> ADO (in conjunction with the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink>) enables the developer to build an empty <legacyBold>Recordset</legacyBold> object by specifying column information and calling <legacyBold>Open</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="729196838d70e9bcd0bb241d031281b5" id="tgt39" class="tgtSentence"> In the following example, three new fields are appended to a new <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="b356fb311b50c110bd3fbf800ffbaa41" id="tgt40" class="tgtSentence"> Then the <legacyBold>Recordset</legacyBold> is opened, two new records are added, and the <legacyBold>Recordset</legacyBold> is persisted to a file.</caps:sentence>
            <caps:sentence sentenceid="261d5f5096c5cabb41bc1d3e85f8ff65" id="tgt41" class="tgtSentence"> (For more information about <legacyBold>Recordset</legacyBold> persistence, see <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.)</caps:sentence>
          </para>
          <code>'BeginFabricate
    Dim objRs As ADODB.Recordset
    Set objRs = New ADODB.Recordset
    
    With objRs.Fields
        .Append "StudentID", adChar, 11, adFldUpdatable
        .Append "FullName", adVarChar, 50, adFldUpdatable
        .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable
    End With
    
    With objRs
        .Open
        
        .AddNew
        .Fields(0) = "123-45-6789"
        .Fields(1) = "John Doe"
        .Fields(2) = "(425) 555-5555"
        .Update
        
        .AddNew
        .Fields(0) = "123-45-6780"
        .Fields(1) = "Jane Doe"
        .Fields(2) = "(615) 555-1212"
        .Update
    End With
            
    objRs.Save App.Path &amp; "FabriTest.adtg", adPersistADTG
    
    objRs.Close
'EndFabricate</code>
          <para>
            <caps:sentence sentenceid="742f1c5ef7d8b844bcfd68c1386ce8bc" id="tgt42" class="tgtSentence">The usage of the <legacyBold>Fields</legacyBold> <legacyBold>Append</legacyBold> method differs between the <legacyBold>Recordset</legacyBold> object and the <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="3cb1d90bf62402eaf5abb706a2b34a5f" id="tgt43" class="tgtSentence"> For more information about the <legacyBold>Record</legacyBold> object, see <legacyLink xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">Records and Streams</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a584e642-a4a3-418e-bc20-3aff81a5625a">Fabricating Hierarchical Recordsets</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>Fields</legacyBold> collection is one of ADO's intrinsic collections.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A collection is an ordered set of items that can be referred to as a unit.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For more information about ADO collections, see <legacyLink xlink:href="7a745aae-9372-49b6-8dae-b9c93e5f3216">The ADO Object Model</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">The <legacyBold>Fields</legacyBold> collection contains a <legacyBold>Field</legacyBold> object for every field (column) in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Like all ADO collections, it has <legacyBold>Count</legacyBold> and <legacyBold>Item</legacyBold> properties, as well as <legacyBold>Append</legacyBold> and <legacyBold>Refresh</legacyBold> methods.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> It also has <legacyBold>CancelUpdate</legacyBold>, <legacyBold>Delete</legacyBold>, <legacyBold>Resync</legacyBold>, and <legacyBold>Update</legacyBold> methods, which are not available to other ADO collections.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Examining the Fields Collection</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">Consider the <legacyBold>Fields</legacyBold> collection of the sample <legacyBold>Recordset</legacyBold> introduced in this section.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The sample <legacyBold>Recordset</legacyBold> was derived from the SQL statement</caps:sentence>
          </para>
          <code>SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7</code>
          <para>
            <caps:sentence id="src10" class="srcSentence">Thus, you should find that the <legacyBold>Recordset</legacyBold> <legacyBold>Fields</legacyBold> collection contains three fields.</caps:sentence>
          </para>
          <code>'BeginWalkFields
    Dim objFields As ADODB.Fields
    Dim intLoop As Integer
    
    objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText
    
    Set objFields = objRs.Fields
    
    For intLoop = 0 To (objFields.Count - 1)
        Debug.Print objFields.Item(intLoop).Name
    Next
'EndWalkFields</code>
          <para>
            <caps:sentence id="src11" class="srcSentence">This code simply determines the number of <legacyBold>Field</legacyBold> objects in the <legacyBold>Fields</legacyBold> collection using the <legacyBold>Count</legacyBold> property and loops through the collection, returning the value of the <legacyBold>Name</legacyBold> property for each <legacyBold>Field</legacyBold> object.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> You can use many more <legacyBold>Field</legacyBold> properties to get information about a field.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> For more information about querying a <legacyBold>Field</legacyBold>, see <legacyLink xlink:href="7d1c4ad5-4be3-42ab-b516-e7133ca300bc">The Field Object</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Counting Columns</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">As you might expect, the <legacyBold>Count</legacyBold> property returns the actual number of <legacyBold>Field</legacyBold> objects in the <legacyBold>Fields</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the <legacyBold>Count</legacyBold> property minus 1.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the <legacyBold>Count</legacyBold> property, use the <legacyBold>For</legacyBold> <legacyBold>Each...Next</legacyBold> command.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">If the <legacyBold>Count</legacyBold> property is zero, there are no objects in the collection.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src19" class="srcSentence">Getting to the Field</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src20" class="srcSentence">As with any ADO collection, the <legacyBold>Item</legacyBold> property is the default property of the collection.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> It returns the individual <legacyBold>Field</legacyBold> object specified by the name or index passed to it.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Therefore, the following statements are equivalent for the sample <legacyBold>Recordset</legacyBold>:</caps:sentence>
          </para>
          <code>objField = objRecordset.Fields.Item("ProductID")
objField = objRecordset.Fields("ProductID")
objField = objRecordset.Fields.Item(0)
objField = objRecordset.Fields(0)</code>
          <para>
            <caps:sentence id="src23" class="srcSentence">If these methods are equivalent, which is best?</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> It depends.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> Using an index to retrieve a <legacyBold>Field</legacyBold> from the collection is faster because it accesses the <legacyBold>Field</legacyBold> directly without having to perform a string lookup.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> On the other hand, the order of <legacyBold>Fields</legacyBold> within the collection must be known, and if the order changes, the reference to the <legacyBold>Field's</legacyBold> index will have to be changed wherever it occurs.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> Although slightly slower, using the name of the <legacyBold>Field</legacyBold> is more flexible because it doesn't depend on the order of the <legacyBold>Fields</legacyBold> in the collection.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">Using the Refresh Method</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">Unlike some other ADO collections, using the <legacyBold>Refresh</legacyBold> method on the <legacyBold>Fields</legacyBold> collection has no visible effect.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> To retrieve changes from the underlying database structure, you must use either the <legacyBold>Requery</legacyBold> method, or if the <legacyBold>Recordset</legacyBold> object does not support bookmarks, the <legacyBold>MoveFirst</legacyBold> method, which will cause the command to be executed against the provider again.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src31" class="srcSentence">Adding Fields to a Recordset</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src32" class="srcSentence">The <legacyBold>Append</legacyBold> method is used to add fields to a <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src33" class="srcSentence">You can use the <legacyBold>Append</legacyBold> method to fabricate a <legacyBold>Recordset</legacyBold> programmatically without opening a connection to a data source.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> A run-time error will occur if the <legacyBold>Append</legacyBold> method is called on the <legacyBold>Fields</legacyBold> collection of an open <legacyBold>Recordset</legacyBold> or on a <legacyBold>Recordset</legacyBold> where the <legacyBold>ActiveConnection</legacyBold> property has been set.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> You can append fields only to a <legacyBold>Recordset</legacyBold> that is not open and has not yet been connected to a data source.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> However, to specify values for the newly appended <legacyBold>Fields</legacyBold>, the <legacyBold>Recordset</legacyBold> must first be opened.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src37" class="srcSentence">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> ADO (in conjunction with the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink>) enables the developer to build an empty <legacyBold>Recordset</legacyBold> object by specifying column information and calling <legacyBold>Open</legacyBold>.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> In the following example, three new fields are appended to a new <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> Then the <legacyBold>Recordset</legacyBold> is opened, two new records are added, and the <legacyBold>Recordset</legacyBold> is persisted to a file.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> (For more information about <legacyBold>Recordset</legacyBold> persistence, see <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">Updating and Persisting Data</legacyLink>.)</caps:sentence>
          </para>
          <code>'BeginFabricate
    Dim objRs As ADODB.Recordset
    Set objRs = New ADODB.Recordset
    
    With objRs.Fields
        .Append "StudentID", adChar, 11, adFldUpdatable
        .Append "FullName", adVarChar, 50, adFldUpdatable
        .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable
    End With
    
    With objRs
        .Open
        
        .AddNew
        .Fields(0) = "123-45-6789"
        .Fields(1) = "John Doe"
        .Fields(2) = "(425) 555-5555"
        .Update
        
        .AddNew
        .Fields(0) = "123-45-6780"
        .Fields(1) = "Jane Doe"
        .Fields(2) = "(615) 555-1212"
        .Update
    End With
            
    objRs.Save App.Path &amp; "FabriTest.adtg", adPersistADTG
    
    objRs.Close
'EndFabricate</code>
          <para>
            <caps:sentence id="src42" class="srcSentence">The usage of the <legacyBold>Fields</legacyBold> <legacyBold>Append</legacyBold> method differs between the <legacyBold>Recordset</legacyBold> object and the <legacyBold>Record</legacyBold> object.</caps:sentence>
            <caps:sentence id="src43" class="srcSentence"> For more information about the <legacyBold>Record</legacyBold> object, see <legacyLink xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">Records and Streams</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="a584e642-a4a3-418e-bc20-3aff81a5625a">Fabricating Hierarchical Recordsets</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
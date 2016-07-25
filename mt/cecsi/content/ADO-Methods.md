---
title: "ADO Methods"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a38c5670-ba28-44f3-bd5b-fcb46880e904
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
# ADO Methods
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
                  <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">
                    <caps:sentence sentenceid="2a99922bd3fcc215a7b3fcbd9667338a" id="tgt1" class="tgtSentence">AddNew</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="49dff47457e3cc10a14b4b72c8d30b8c" id="tgt2" class="tgtSentence">Creates a new record for an updatable <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">
                    <caps:sentence sentenceid="9516dfb15f51c7ee19a4d46b8c0dbe1d" id="tgt3" class="tgtSentence">Append</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3ac349617bf6819d445c640413bb207f" id="tgt4" class="tgtSentence">Appends an object to a collection.</caps:sentence>
                  <caps:sentence sentenceid="58db7e1bf8bb46a7ad97c44150787395" id="tgt5" class="tgtSentence"> If the collection is <legacyBold>Fields</legacyBold>, a new <legacyBold>Field</legacyBold> object may be created before it is appended to the collection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">
                    <caps:sentence sentenceid="ad8d53c3bd11f643cf69c18100bbff5a" id="tgt6" class="tgtSentence">AppendChunk</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d83a7fb9c0e8e930f9812ce6782c3fa7" id="tgt7" class="tgtSentence">Appends data to a large text or binary data <legacyBold>Field</legacyBold>, or to a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">
                    <caps:sentence sentenceid="781e110f75ef7d93d48dd8d2d8db8493" id="tgt8" class="tgtSentence">BeginTrans, CommitTrans, and RollbackTrans</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="64721cfcb24256332b6b51bfec7232c4" id="tgt9" class="tgtSentence">Manages transaction processing within a <legacyBold>Connection</legacyBold> object as follows:</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="996e0d982096be7395a4e56ccc5b2b44" id="tgt10" class="tgtSentence">
                    <legacyBold>BeginTrans</legacyBold> — Begins a new transaction.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="e522e999bbf55168e13065795276484e" id="tgt11" class="tgtSentence">
                    <legacyBold>CommitTrans</legacyBold> — Saves any changes and ends the current transaction.</caps:sentence>
                  <caps:sentence sentenceid="0d170df5fe4be946ab147e1ba485f7df" id="tgt12" class="tgtSentence"> It may also start a new transaction.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="46485e8844668db8915adc1bb4676469" id="tgt13" class="tgtSentence">
                    <legacyBold>RollbackTrans</legacyBold> — Cancels any changes and ends the current transaction.</caps:sentence>
                  <caps:sentence sentenceid="0d170df5fe4be946ab147e1ba485f7df" id="tgt14" class="tgtSentence"> It may also start a new transaction.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">
                    <caps:sentence sentenceid="10aec35353f9c4096a71c38654c3d402" id="tgt15" class="tgtSentence">Cancel</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="77dac816e9afab97779cda8a243c6ef3" id="tgt16" class="tgtSentence">Cancels execution of a pending, asynchronous method call.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">
                    <caps:sentence sentenceid="ecb488ca7118773aa90cb428ed21379b" id="tgt17" class="tgtSentence">CancelBatch</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a65d233746333e6dbd5df56e7ee2fd9b" id="tgt18" class="tgtSentence">Cancels a pending batch update.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">
                    <caps:sentence sentenceid="07e957a04a9b08eadc8537a17615e387" id="tgt19" class="tgtSentence">CancelUpdate</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6896233e4f67b5a09065ff73ff6d817c" id="tgt20" class="tgtSentence">Cancels any changes that were made to the current or new row of a <legacyBold>Recordset</legacyBold> object, or the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object, before calling the <legacyBold>Update</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">
                    <caps:sentence sentenceid="01bc6f8efa4202821e95f4fdf6298b30" id="tgt21" class="tgtSentence">Clear</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="848ad50b4ca1bb4811639225a2b3034b" id="tgt22" class="tgtSentence">Removes all the <legacyBold>Error</legacyBold> objects from the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">
                    <caps:sentence sentenceid="d329fd777726c300d7a044e482b967e7" id="tgt23" class="tgtSentence">Clone</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9d4de33cec9bcc7fa2801172a609d2ff" id="tgt24" class="tgtSentence">Creates a duplicate <legacyBold>Recordset </legacyBold>object from an existing <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                  <caps:sentence sentenceid="e05a271f17e9dbf9e8a3efed4c3cf96c" id="tgt25" class="tgtSentence"> Optionally, specifies that the clone be read-only.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">
                    <caps:sentence sentenceid="716f6b30598ba30945d84485e61c1027" id="tgt26" class="tgtSentence">Close</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="00ce5bb31e4d14be6b806e2b19829049" id="tgt27" class="tgtSentence">Closes an open object and any dependent objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d0b64286-2cc4-4a22-8f1d-9aefeebbcbc6">
                    <caps:sentence sentenceid="c42346ac5a17b515602ff6ee767469fa" id="tgt28" class="tgtSentence">CompareBookmarks</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a7d8935330860954f167f6cd9ee4d3c3" id="tgt29" class="tgtSentence">Compares two bookmarks and returns an indication of their relative values.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b9bcf272-3c74-479f-95dd-0229a32e98fc">
                    <caps:sentence sentenceid="bcced5c25d72aa2a157bf7725c0d1101" id="tgt30" class="tgtSentence">CopyRecord</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e1a4164360b5447e842c6b7d6e096377" id="tgt31" class="tgtSentence">Copies a file or directory, and its contents, to another location.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b4aa5714-916b-48b8-8b09-cc2708379602">
                    <caps:sentence sentenceid="14ee76d3a6e860b3a0f29ab303dbb272" id="tgt32" class="tgtSentence">CopyTo</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="788846142d0c5e8ebfa0118b48a2318c" id="tgt33" class="tgtSentence">Copies the specified number of characters or bytes (depending on <legacyBold>Type</legacyBold>) in the <legacyBold>Stream</legacyBold> to another <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">
                    <caps:sentence sentenceid="4dcdea2a87e268e1df46458c0b8af74c" id="tgt34" class="tgtSentence">CreateParameter</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4760c04eb1951c030cc65f247a701605" id="tgt35" class="tgtSentence">Creates a new <legacyBold>Parameter</legacyBold> object that has the specified properties.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">
                    <caps:sentence sentenceid="18716f1b35d9c6c4a6c42844f15158aa" id="tgt36" class="tgtSentence">Delete (ADO Parameters Collection)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="aeab6b032aff7b072a2660c54b04551e" id="tgt37" class="tgtSentence">Deletes an object from the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">
                    <caps:sentence sentenceid="7be2d4fb6dd0c6ec4df30492a8ac0af3" id="tgt38" class="tgtSentence">Delete (ADO Fields Collection)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8476489577df40cac9a9cea698d2dc48" id="tgt39" class="tgtSentence">Deletes an object from the <legacyBold>Fields</legacyBold> collection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">
                    <caps:sentence sentenceid="170a966c1191d8dfeabef470ff50516f" id="tgt40" class="tgtSentence">Delete (ADO Recordset)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c3482f6e47cc7207c6bf21a13b228a8f" id="tgt41" class="tgtSentence">Deletes the current record or a group of records.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">
                    <caps:sentence sentenceid="46cab06323efb09f89376bb1fe69e8c2" id="tgt42" class="tgtSentence">DeleteRecord</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fdaf029e4983931b24e8010384658f87" id="tgt43" class="tgtSentence">Deletes a file or directory, and all its subdirectories.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">
                    <caps:sentence sentenceid="46ee0c8a62cbba510ac6b6d9040c34a3" id="tgt44" class="tgtSentence">Execute (ADO Command)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bb914bdd2538663506f5c91afbb176c3" id="tgt45" class="tgtSentence">Executes the query, SQL statement, or stored procedure specified in the <legacyBold>CommandText</legacyBold> property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">
                    <caps:sentence sentenceid="c17738f6de6f5ca3eca07ed8b32a68ae" id="tgt46" class="tgtSentence">Execute (ADO Connection)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a98ac61157e1ba1b52017824b3b84379" id="tgt47" class="tgtSentence">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">
                    <caps:sentence sentenceid="ea170e2cafb1337755c8b3d5ae4437f4" id="tgt48" class="tgtSentence">Find</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ab701b5de3bab8374806f35566baed73" id="tgt49" class="tgtSentence">Searches a <legacyBold>Recordset</legacyBold> for the row that satisfies the specified criteria.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="938522b4-f836-4c80-8d27-a598a000f0ee">
                    <caps:sentence sentenceid="86f354b8575a1a736775ae003fa344e5" id="tgt50" class="tgtSentence">Flush</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9df50f53cca8eef44cecb6bc565dd378" id="tgt51" class="tgtSentence">Forces the contents of the <legacyBold>Stream</legacyBold> remaining in the ADO buffer to the underlying object with which the <legacyBold>Stream</legacyBold> is associated.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="23d551f5-3d5b-434b-ade6-fef15f1710e7">get_OLEDBCommand</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e42bc12f442e7f113f9c50a880ad01f6" id="tgt52" class="tgtSentence">Returns the underlying OLEDB Command, first propagating any parameter information set on the ADO Command to the OLEDB command.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b3f09bac-4f66-49f6-aa5a-6fbb4fb28338">
                    <caps:sentence sentenceid="5693dc3e49735415007b453885b834fc" id="tgt53" class="tgtSentence">GetChildren</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4046ceb1411a1fd87de41701ab998bff" id="tgt54" class="tgtSentence">Returns a <legacyBold>Recordset</legacyBold> whose rows represent the files and subdirectories in the directory represented by this <legacyBold>Record</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">
                    <caps:sentence sentenceid="4793f48c200809291817fe7a00fec97c" id="tgt55" class="tgtSentence">GetChunk</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1dc29d8643895e803d3a3c6e4bc10252" id="tgt56" class="tgtSentence">Returns all, or a portion of, the contents of a large text or binary data <legacyBold>Field</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="5a4c6bd5-0c79-4f81-a977-0561392d8d50">GetDataProviderDSO</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f5f36f0bfe57318d38f058a43e4100c1" id="tgt57" class="tgtSentence">Retrieves the underlying OLEDB Data Source object from the Shape provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="14b92860-4171-47d9-a413-dd60dd6a8880">
                    <caps:sentence sentenceid="d1b51a6e50f7a6a0f9879ebf15f2651d" id="tgt58" class="tgtSentence">GetRows</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bbdda64ec6348d67f85c1b5875999fde" id="tgt59" class="tgtSentence">Retrieves multiple records of a <legacyBold>Recordset</legacyBold> object into an array.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="92452940-b2a7-456e-94fc-3780c71da33c">
                    <caps:sentence sentenceid="689c28a24832ccb66e5f8ef4a05dc6f4" id="tgt60" class="tgtSentence">GetString</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d47f6a984112db9a19d0ef107eca3f2f" id="tgt61" class="tgtSentence">Returns the <legacyBold>Recordset</legacyBold> as a string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b18d8d38-7354-4a94-b637-6ac035faa433">
                    <caps:sentence sentenceid="773633cf8b11e688d2bae7fccd96cb5f" id="tgt62" class="tgtSentence">LoadFromFile</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="47712c73bb0bf2e9cbef27bc33e354d7" id="tgt63" class="tgtSentence">Loads the contents of an existing file into a <legacyBold>Stream</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">
                    <caps:sentence sentenceid="3734a903022249b3010be1897042568e" id="tgt64" class="tgtSentence">Move</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1cc43db5c211801b9d0beaa55cf2ed3a" id="tgt65" class="tgtSentence">Moves the position of the current record in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                    <caps:sentence sentenceid="81d56325b25f86ad77011a497bffa3a2" id="tgt66" class="tgtSentence">MoveFirst, MoveLast, MoveNext, and MovePrevious</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5b1c6c8a062493ffef308e74d404d37a" id="tgt67" class="tgtSentence">Moves to the first, last, next, or previous record in a specified <legacyBold>Recordset</legacyBold> object and makes that record the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">
                    <caps:sentence sentenceid="c4ac997b6503e3989ee873b65afe54ff" id="tgt68" class="tgtSentence">MoveRecord</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="806cb4040caa969a9bc93147af495e05" id="tgt69" class="tgtSentence">Moves a file, or a directory and its contents, to another location.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">
                    <caps:sentence sentenceid="1e8095fae1cbe555ea131424ef67f608" id="tgt70" class="tgtSentence">NextRecordset</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8441e9f75e4dbd312d6df94be6c9034b" id="tgt71" class="tgtSentence">Clears the current <legacyBold>Recordset</legacyBold> object and returns the next <legacyBold>Recordset</legacyBold> by advancing through a series of commands.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">
                    <caps:sentence sentenceid="f9d4c80126e0d81f9e4483ea325a5389" id="tgt72" class="tgtSentence">Open (ADO Connection)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="dbc01469e8610f34f53bb155be4d9319" id="tgt73" class="tgtSentence">Opens a connection to a data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">
                    <caps:sentence sentenceid="76cb8b2042081b59a44432bbf9961a7d" id="tgt74" class="tgtSentence">Open (ADO Record)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2b9fca1cce63b8e456d626465c7e9d72" id="tgt75" class="tgtSentence">Opens an existing <legacyBold>Record</legacyBold> object, or creates a new file or directory.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">
                    <caps:sentence sentenceid="a1f45ff297350c0bd7560343406d2982" id="tgt76" class="tgtSentence">Open (ADO Recordset)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d05cdc3818e3084183ebda9dfa894d59" id="tgt77" class="tgtSentence">Opens a cursor.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">
                    <caps:sentence sentenceid="3899265b2bf8a9a9f7b05d4ac97773b4" id="tgt78" class="tgtSentence">Open (ADO Stream)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7b5b135bef11cedde2b26e95bf20f3ee" id="tgt79" class="tgtSentence">Opens a <legacyBold>Stream</legacyBold> object to manipulate streams of binary or text data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">
                    <caps:sentence sentenceid="8c2d4dc5eac8af32d9f7633873a11f20" id="tgt80" class="tgtSentence">OpenSchema</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="04d9fa93dcd673016cb8daafcc94a69d" id="tgt81" class="tgtSentence">Obtains database schema information from the provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="ca6a5804-bf5c-4afc-99db-22904bc0b33d">put_OLEDBCommand</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="54e50f235c2744dcd87560be72921fc1" id="tgt82" class="tgtSentence">This method performs no operation - it always returns S_OK.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">
                    <caps:sentence sentenceid="ecae13117d6f0584c25a9da6c8f8415e" id="tgt83" class="tgtSentence">Read</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8f061f3534679392a500f59a9232ca6b" id="tgt84" class="tgtSentence">Reads a specified number of bytes from a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">
                    <caps:sentence sentenceid="6bd31e723b9f3f03f4ef2dd91cd40975" id="tgt85" class="tgtSentence">ReadText</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="98aeb7094cf9faa89deb0a9b2262db76" id="tgt86" class="tgtSentence">Reads a specified number of characters from a text <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">
                    <caps:sentence sentenceid="03b62516184fb6ef591f45bd4974b753" id="tgt87" class="tgtSentence">Refresh</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="227051afa8c902ab4368237f19c7718c" id="tgt88" class="tgtSentence">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">
                    <caps:sentence sentenceid="65d807e47b5cdafc34fc06e6d25cafd6" id="tgt89" class="tgtSentence">Requery</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5a8b6b86f8a6cdbb028ff05b4f5b5dc4" id="tgt90" class="tgtSentence">Updates the data in a <legacyBold>Recordset</legacyBold> object by re-executing the query on which the object is based.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">
                    <caps:sentence sentenceid="e365ce2f3002afe909c5591eb5c69889" id="tgt91" class="tgtSentence">Resync</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6b8e1adc00520feea78b1e17574bd127" id="tgt92" class="tgtSentence">Refreshes the data in the current <legacyBold>Recordset</legacyBold> object, or <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object, from the underlying database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">
                    <caps:sentence sentenceid="43781db5c40ecc39fd718685594f0956" id="tgt93" class="tgtSentence">Save</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8717345a96f891ee2ac410a23ed2d099" id="tgt94" class="tgtSentence">Saves the <legacyBold>Recordset</legacyBold> in a file or <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">
                    <caps:sentence sentenceid="0657fe5bb80e57aa98825267fa847cba" id="tgt95" class="tgtSentence">SaveToFile</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5b85fc1ef374f03211490d58479b4690" id="tgt96" class="tgtSentence">Saves the binary contents of a <legacyBold>Stream</legacyBold> to a file.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">
                    <caps:sentence sentenceid="e6f6362248805a36c61d205dbc6f4076" id="tgt97" class="tgtSentence">Seek</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f1f266a34fc61fd038702ad8659a5d4e" id="tgt98" class="tgtSentence">Searches the index of a <legacyBold>Recordset</legacyBold> to quickly locate the row that matches the specified values, and changes the current row position to that row.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">
                    <caps:sentence sentenceid="9af0e7cb6e9875260996a9a8f184cbb6" id="tgt99" class="tgtSentence">SetEOS</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="269857b16ce62889b25b604290b3b204" id="tgt100" class="tgtSentence">Sets the position that is the end of the stream.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="0abc00fe-ee09-4c8e-b1f2-48ee9c5f3329">
                    <caps:sentence sentenceid="e780b01c3cf3c0285dc5889e209a757a" id="tgt101" class="tgtSentence">SkipLine</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d0ff70c03af4f3fa01b65f0cf5570f25" id="tgt102" class="tgtSentence">Skips one entire line when reading a text stream.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="99a2b2d4-e6b1-4205-b011-72d024ea7240">
                    <caps:sentence sentenceid="77ddcb5f19832f4145345889013ab3a4" id="tgt103" class="tgtSentence">Stat</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d5ca6bab1e6f9c4ff1d4a5c52f74f1f9" id="tgt104" class="tgtSentence">Gets statistical information about an open stream.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">
                    <caps:sentence sentenceid="72225dfc0ffc1c4e8471c5824c2c63c2" id="tgt105" class="tgtSentence">Supports</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="39047ebd27619bef11cfbe9293886ed4" id="tgt106" class="tgtSentence">Determines whether a specified <legacyBold>Recordset</legacyBold> object supports a particular type of functionality.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">
                    <caps:sentence sentenceid="3ac340832f29c11538fbe2d6f75e8bcc" id="tgt107" class="tgtSentence">Update</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eab2cc68458ddfe2f7f8d9647f8c1dcd" id="tgt108" class="tgtSentence">Saves any changes you make to the current row of a <legacyBold>Recordset</legacyBold> object, or the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">
                    <caps:sentence sentenceid="f4651adedf889c8f0a0b0e38a2ee96fa" id="tgt109" class="tgtSentence">UpdateBatch</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a493d8b88708449aab867bbb27b84fc6" id="tgt110" class="tgtSentence">Writes all pending batch updates to disk.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">
                    <caps:sentence sentenceid="efb2a684e4afb7d55e6147fbe5a332ee" id="tgt111" class="tgtSentence">Write</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="66febdebc5a6eac6c40d5a89952f8e46" id="tgt112" class="tgtSentence">Writes binary data to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">
                    <caps:sentence sentenceid="1be5c0acb97efd370a7684b2b553efeb" id="tgt113" class="tgtSentence">WriteText</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1faf691ca977694f72a84561f2f73179" id="tgt114" class="tgtSentence">Writes a specified text string to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
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
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
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
                  <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">
                    <caps:sentence id="src1" class="srcSentence">AddNew</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Creates a new record for an updatable <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">
                    <caps:sentence id="src3" class="srcSentence">Append</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Appends an object to a collection.</caps:sentence>
                  <caps:sentence id="src5" class="srcSentence"> If the collection is <legacyBold>Fields</legacyBold>, a new <legacyBold>Field</legacyBold> object may be created before it is appended to the collection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">
                    <caps:sentence id="src6" class="srcSentence">AppendChunk</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Appends data to a large text or binary data <legacyBold>Field</legacyBold>, or to a <legacyBold>Parameter</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d4683472-4120-4236-8640-fa9ae289e23e">
                    <caps:sentence id="src8" class="srcSentence">BeginTrans, CommitTrans, and RollbackTrans</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Manages transaction processing within a <legacyBold>Connection</legacyBold> object as follows:</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src10" class="srcSentence">
                    <legacyBold>BeginTrans</legacyBold> — Begins a new transaction.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src11" class="srcSentence">
                    <legacyBold>CommitTrans</legacyBold> — Saves any changes and ends the current transaction.</caps:sentence>
                  <caps:sentence id="src12" class="srcSentence"> It may also start a new transaction.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src13" class="srcSentence">
                    <legacyBold>RollbackTrans</legacyBold> — Cancels any changes and ends the current transaction.</caps:sentence>
                  <caps:sentence id="src14" class="srcSentence"> It may also start a new transaction.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="e0db4e15-6787-41e2-8f13-9e9b524d620a">
                    <caps:sentence id="src15" class="srcSentence">Cancel</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Cancels execution of a pending, asynchronous method call.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">
                    <caps:sentence id="src17" class="srcSentence">CancelBatch</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Cancels a pending batch update.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="eaa856cc-c786-462e-890c-c896261b1741">
                    <caps:sentence id="src19" class="srcSentence">CancelUpdate</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Cancels any changes that were made to the current or new row of a <legacyBold>Recordset</legacyBold> object, or the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object, before calling the <legacyBold>Update</legacyBold> method.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">
                    <caps:sentence id="src21" class="srcSentence">Clear</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Removes all the <legacyBold>Error</legacyBold> objects from the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">
                    <caps:sentence id="src23" class="srcSentence">Clone</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Creates a duplicate <legacyBold>Recordset </legacyBold>object from an existing <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                  <caps:sentence id="src25" class="srcSentence"> Optionally, specifies that the clone be read-only.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="3cdf27d1-a180-4cff-8e42-95dec5fb1b55">
                    <caps:sentence id="src26" class="srcSentence">Close</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Closes an open object and any dependent objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d0b64286-2cc4-4a22-8f1d-9aefeebbcbc6">
                    <caps:sentence id="src28" class="srcSentence">CompareBookmarks</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">Compares two bookmarks and returns an indication of their relative values.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b9bcf272-3c74-479f-95dd-0229a32e98fc">
                    <caps:sentence id="src30" class="srcSentence">CopyRecord</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Copies a file or directory, and its contents, to another location.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b4aa5714-916b-48b8-8b09-cc2708379602">
                    <caps:sentence id="src32" class="srcSentence">CopyTo</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Copies the specified number of characters or bytes (depending on <legacyBold>Type</legacyBold>) in the <legacyBold>Stream</legacyBold> to another <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">
                    <caps:sentence id="src34" class="srcSentence">CreateParameter</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">Creates a new <legacyBold>Parameter</legacyBold> object that has the specified properties.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">
                    <caps:sentence id="src36" class="srcSentence">Delete (ADO Parameters Collection)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Deletes an object from the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">
                    <caps:sentence id="src38" class="srcSentence">Delete (ADO Fields Collection)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">Deletes an object from the <legacyBold>Fields</legacyBold> collection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">
                    <caps:sentence id="src40" class="srcSentence">Delete (ADO Recordset)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">Deletes the current record or a group of records.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">
                    <caps:sentence id="src42" class="srcSentence">DeleteRecord</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">Deletes a file or directory, and all its subdirectories.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">
                    <caps:sentence id="src44" class="srcSentence">Execute (ADO Command)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">Executes the query, SQL statement, or stored procedure specified in the <legacyBold>CommandText</legacyBold> property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">
                    <caps:sentence id="src46" class="srcSentence">Execute (ADO Connection)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">
                    <caps:sentence id="src48" class="srcSentence">Find</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">Searches a <legacyBold>Recordset</legacyBold> for the row that satisfies the specified criteria.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="938522b4-f836-4c80-8d27-a598a000f0ee">
                    <caps:sentence id="src50" class="srcSentence">Flush</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src51" class="srcSentence">Forces the contents of the <legacyBold>Stream</legacyBold> remaining in the ADO buffer to the underlying object with which the <legacyBold>Stream</legacyBold> is associated.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="23d551f5-3d5b-434b-ade6-fef15f1710e7">get_OLEDBCommand</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">Returns the underlying OLEDB Command, first propagating any parameter information set on the ADO Command to the OLEDB command.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b3f09bac-4f66-49f6-aa5a-6fbb4fb28338">
                    <caps:sentence id="src53" class="srcSentence">GetChildren</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">Returns a <legacyBold>Recordset</legacyBold> whose rows represent the files and subdirectories in the directory represented by this <legacyBold>Record</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">
                    <caps:sentence id="src55" class="srcSentence">GetChunk</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">Returns all, or a portion of, the contents of a large text or binary data <legacyBold>Field</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="5a4c6bd5-0c79-4f81-a977-0561392d8d50">GetDataProviderDSO</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">Retrieves the underlying OLEDB Data Source object from the Shape provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="14b92860-4171-47d9-a413-dd60dd6a8880">
                    <caps:sentence id="src58" class="srcSentence">GetRows</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">Retrieves multiple records of a <legacyBold>Recordset</legacyBold> object into an array.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="92452940-b2a7-456e-94fc-3780c71da33c">
                    <caps:sentence id="src60" class="srcSentence">GetString</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src61" class="srcSentence">Returns the <legacyBold>Recordset</legacyBold> as a string.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b18d8d38-7354-4a94-b637-6ac035faa433">
                    <caps:sentence id="src62" class="srcSentence">LoadFromFile</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src63" class="srcSentence">Loads the contents of an existing file into a <legacyBold>Stream</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">
                    <caps:sentence id="src64" class="srcSentence">Move</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src65" class="srcSentence">Moves the position of the current record in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="a61a01a7-5b33-4150-9126-21dfa63654cb">
                    <caps:sentence id="src66" class="srcSentence">MoveFirst, MoveLast, MoveNext, and MovePrevious</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src67" class="srcSentence">Moves to the first, last, next, or previous record in a specified <legacyBold>Recordset</legacyBold> object and makes that record the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">
                    <caps:sentence id="src68" class="srcSentence">MoveRecord</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src69" class="srcSentence">Moves a file, or a directory and its contents, to another location.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ab1fa449-a695-4987-b1ee-bc68f89418dd">
                    <caps:sentence id="src70" class="srcSentence">NextRecordset</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src71" class="srcSentence">Clears the current <legacyBold>Recordset</legacyBold> object and returns the next <legacyBold>Recordset</legacyBold> by advancing through a series of commands.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">
                    <caps:sentence id="src72" class="srcSentence">Open (ADO Connection)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src73" class="srcSentence">Opens a connection to a data source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">
                    <caps:sentence id="src74" class="srcSentence">Open (ADO Record)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src75" class="srcSentence">Opens an existing <legacyBold>Record</legacyBold> object, or creates a new file or directory.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">
                    <caps:sentence id="src76" class="srcSentence">Open (ADO Recordset)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src77" class="srcSentence">Opens a cursor.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">
                    <caps:sentence id="src78" class="srcSentence">Open (ADO Stream)</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src79" class="srcSentence">Opens a <legacyBold>Stream</legacyBold> object to manipulate streams of binary or text data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">
                    <caps:sentence id="src80" class="srcSentence">OpenSchema</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src81" class="srcSentence">Obtains database schema information from the provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="ca6a5804-bf5c-4afc-99db-22904bc0b33d">put_OLEDBCommand</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src82" class="srcSentence">This method performs no operation - it always returns S_OK.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="838502de-80f1-4eeb-8838-dd3d9403e567">
                    <caps:sentence id="src83" class="srcSentence">Read</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src84" class="srcSentence">Reads a specified number of bytes from a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="be5a409e-cf87-4859-9ea5-713401755a77">
                    <caps:sentence id="src85" class="srcSentence">ReadText</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src86" class="srcSentence">Reads a specified number of characters from a text <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">
                    <caps:sentence id="src87" class="srcSentence">Refresh</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src88" class="srcSentence">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">
                    <caps:sentence id="src89" class="srcSentence">Requery</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src90" class="srcSentence">Updates the data in a <legacyBold>Recordset</legacyBold> object by re-executing the query on which the object is based.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">
                    <caps:sentence id="src91" class="srcSentence">Resync</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src92" class="srcSentence">Refreshes the data in the current <legacyBold>Recordset</legacyBold> object, or <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object, from the underlying database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">
                    <caps:sentence id="src93" class="srcSentence">Save</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src94" class="srcSentence">Saves the <legacyBold>Recordset</legacyBold> in a file or <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">
                    <caps:sentence id="src95" class="srcSentence">SaveToFile</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src96" class="srcSentence">Saves the binary contents of a <legacyBold>Stream</legacyBold> to a file.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">
                    <caps:sentence id="src97" class="srcSentence">Seek</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src98" class="srcSentence">Searches the index of a <legacyBold>Recordset</legacyBold> to quickly locate the row that matches the specified values, and changes the current row position to that row.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="707c18ca-6a56-4970-bbd6-ae1fb86a0b8a">
                    <caps:sentence id="src99" class="srcSentence">SetEOS</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src100" class="srcSentence">Sets the position that is the end of the stream.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="0abc00fe-ee09-4c8e-b1f2-48ee9c5f3329">
                    <caps:sentence id="src101" class="srcSentence">SkipLine</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src102" class="srcSentence">Skips one entire line when reading a text stream.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="99a2b2d4-e6b1-4205-b011-72d024ea7240">
                    <caps:sentence id="src103" class="srcSentence">Stat</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src104" class="srcSentence">Gets statistical information about an open stream.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">
                    <caps:sentence id="src105" class="srcSentence">Supports</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src106" class="srcSentence">Determines whether a specified <legacyBold>Recordset</legacyBold> object supports a particular type of functionality.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">
                    <caps:sentence id="src107" class="srcSentence">Update</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src108" class="srcSentence">Saves any changes you make to the current row of a <legacyBold>Recordset</legacyBold> object, or the <legacyBold>Fields</legacyBold> collection of a <legacyBold>Record</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">
                    <caps:sentence id="src109" class="srcSentence">UpdateBatch</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src110" class="srcSentence">Writes all pending batch updates to disk.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="02982e6a-ac5f-4af2-b82e-ce12534b84b2">
                    <caps:sentence id="src111" class="srcSentence">Write</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src112" class="srcSentence">Writes binary data to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="7a669048-13f4-4574-a2b1-985e089729d5">
                    <caps:sentence id="src113" class="srcSentence">WriteText</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src114" class="srcSentence">Writes a specified text string to a <legacyBold>Stream</legacyBold> object.</caps:sentence>
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
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerOrientationDocument>
  </caps:SxSSource>
</caps:SxS>
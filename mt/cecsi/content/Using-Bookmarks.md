---
title: "Using Bookmarks"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cca244e6-84f8-4394-bca9-f7a819b8f4df
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
# Using Bookmarks
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="cc2536dacefa8abe2ac2841b7fabe2d9" id="tgt1" class="tgtSentence">It is often useful to return directly to a specific record after having moved around in the <legacyBold>Recordset</legacyBold> without having to scroll through every record and compare values.</caps:sentence>
          <caps:sentence sentenceid="87509f3062a27ec28db3317aa9e8f8ca" id="tgt2" class="tgtSentence"> For example, if you attempt to search for a record using the <legacyBold>Find</legacyBold> method but the search returns no records, you are automatically placed at either end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="d95c179090772f011dab0182b4645f2c" id="tgt3" class="tgtSentence"> If your provider supports them, bookmarks can be used to mark your place before using the <legacyBold>Find</legacyBold> method so you can return to your location.</caps:sentence>
          <caps:sentence sentenceid="b650654f300bd7ef0cb5b33d51756189" id="tgt4" class="tgtSentence"> A bookmark is a <legacyBold>Variant</legacyBold> type value that uniquely identifies a record in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="041af7947c9a722d1be742b3f4dddf90" id="tgt5" class="tgtSentence">You can also use a variant array of bookmarks with the <legacyBold>Recordset</legacyBold> <legacyBold>Filter</legacyBold> method to filter on a selected set of records.</caps:sentence>
          <caps:sentence sentenceid="9aea3fcc3445e5a1905ae8b843d84615" id="tgt6" class="tgtSentence"> For details about this technique, see Filtering the Results in the topic, <legacyLink xlink:href="bdf9a56a-de4a-44de-9111-2f11ab7b16ea">Working with Recordsets</legacyLink>, later in this section.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1d61b969ed5351e4bde911036901fdc2" id="tgt7" class="tgtSentence">You can use the <legacyBold>Bookmark</legacyBold> property to get a bookmark for a record, or set the current record in a <legacyBold>Recordset</legacyBold> object to the record identified by a valid bookmark.</caps:sentence>
          <caps:sentence sentenceid="4bd1e9752c55feef085b15e99e9d7674" id="tgt8" class="tgtSentence"> The following code uses the <legacyBold>Bookmark</legacyBold> property to set a bookmark and then return to the bookmarked record after moving on to other records.</caps:sentence>
          <caps:sentence sentenceid="9cf000bf6abe86b588242048a87139a1" id="tgt9" class="tgtSentence"> To determine if your <legacyBold>Recordset</legacyBold> supports bookmarks, use the <legacyBold>Supports</legacyBold> method.</caps:sentence>
        </para>
        <code>    'BeginBookmarkEg
    Dim varBookmark As Variant
    Dim blnCanBkmrk As Boolean
    
    objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText
    
    If objRs.RecordCount &gt; 4 Then
        objRs.Move 4                       ' move to the fifth record
        blnCanBkmrk = objRs.Supports(adBookmark)
        If blnCanBkmrk = True Then
            varBookmark = objRs.Bookmark   ' record the bookmark
            objRs.MoveLast                 ' move to a different record
            objRs.Bookmark = varBookmark   ' return to the bookmarked (sixth) record
        End If
    End If
    'EndBookmarkEg</code>
        <para>
          <caps:sentence sentenceid="acaa520c96c11dbfa0be540bd27379ed" id="tgt10" class="tgtSentence">The <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method is covered in more detail later.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="46cad0c54570bfd14eb3d3e089820257" id="tgt11" class="tgtSentence">Except for the case of cloned <legacyBold>Recordsets</legacyBold>, bookmarks are unique to the <legacyBold>Recordset</legacyBold> in which they were created, even if the same command is used.</caps:sentence>
          <caps:sentence sentenceid="c7544b57371200418115e20d02ee8014" id="tgt12" class="tgtSentence"> This means that you cannot use a <legacyBold>Bookmark</legacyBold> obtained from one <legacyBold>Recordset</legacyBold> to move to the same record in a second <legacyBold>Recordset</legacyBold> opened with the same command.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">It is often useful to return directly to a specific record after having moved around in the <legacyBold>Recordset</legacyBold> without having to scroll through every record and compare values.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For example, if you attempt to search for a record using the <legacyBold>Find</legacyBold> method but the search returns no records, you are automatically placed at either end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> If your provider supports them, bookmarks can be used to mark your place before using the <legacyBold>Find</legacyBold> method so you can return to your location.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> A bookmark is a <legacyBold>Variant</legacyBold> type value that uniquely identifies a record in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">You can also use a variant array of bookmarks with the <legacyBold>Recordset</legacyBold> <legacyBold>Filter</legacyBold> method to filter on a selected set of records.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> For details about this technique, see Filtering the Results in the topic, <legacyLink xlink:href="bdf9a56a-de4a-44de-9111-2f11ab7b16ea">Working with Recordsets</legacyLink>, later in this section.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">You can use the <legacyBold>Bookmark</legacyBold> property to get a bookmark for a record, or set the current record in a <legacyBold>Recordset</legacyBold> object to the record identified by a valid bookmark.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The following code uses the <legacyBold>Bookmark</legacyBold> property to set a bookmark and then return to the bookmarked record after moving on to other records.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> To determine if your <legacyBold>Recordset</legacyBold> supports bookmarks, use the <legacyBold>Supports</legacyBold> method.</caps:sentence>
        </para>
        <code>    'BeginBookmarkEg
    Dim varBookmark As Variant
    Dim blnCanBkmrk As Boolean
    
    objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText
    
    If objRs.RecordCount &gt; 4 Then
        objRs.Move 4                       ' move to the fifth record
        blnCanBkmrk = objRs.Supports(adBookmark)
        If blnCanBkmrk = True Then
            varBookmark = objRs.Bookmark   ' record the bookmark
            objRs.MoveLast                 ' move to a different record
            objRs.Bookmark = varBookmark   ' return to the bookmarked (sixth) record
        End If
    End If
    'EndBookmarkEg</code>
        <para>
          <caps:sentence id="src10" class="srcSentence">The <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method is covered in more detail later.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">Except for the case of cloned <legacyBold>Recordsets</legacyBold>, bookmarks are unique to the <legacyBold>Recordset</legacyBold> in which they were created, even if the same command is used.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> This means that you cannot use a <legacyBold>Bookmark</legacyBold> obtained from one <legacyBold>Recordset</legacyBold> to move to the same record in a second <legacyBold>Recordset</legacyBold> opened with the same command.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
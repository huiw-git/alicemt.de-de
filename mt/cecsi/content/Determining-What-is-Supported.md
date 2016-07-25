---
title: "Determining What is Supported"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 65090cba-6d46-4775-8d61-f6838e7752a6
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
# Determining What is Supported
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e4bc13d48dc0659d9056f8d55b0eb2d4" id="tgt1" class="tgtSentence">The <legacyBold>Supports</legacyBold> method is used to determine whether a specified <legacyBold>Recordset</legacyBold> object supports a particular type of functionality.</caps:sentence>
          <caps:sentence sentenceid="d8c17bdbf4a10e9b93ff0edb74ed51ca" id="tgt2" class="tgtSentence"> It has the following syntax:</caps:sentence>
        </para>
        <code>
        boolean = recordset.Supports(CursorOptions )</code>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="37d6b02a1148bbf5d1e278598ff251f6" id="tgt3" class="tgtSentence">The <legacyBold>Supports</legacyBold> method returns a Boolean value that indicates whether the provider supports all of the features identified by the CursorOptions argument.</caps:sentence>
            <caps:sentence sentenceid="311415955b405bad2183e9dd717284aa" id="tgt4" class="tgtSentence"> You can use the <legacyBold>Supports</legacyBold> method to determine what types of functionality a <legacyBold>Recordset</legacyBold> object supports.</caps:sentence>
            <caps:sentence sentenceid="7b7fe15a737fc18199c5df9b4c2ee6ee" id="tgt5" class="tgtSentence"> If the <legacyBold>Recordset</legacyBold> object supports the features whose corresponding constants are in <legacyItalic>CursorOptions</legacyItalic>, the <legacyBold>Supports</legacyBold> method returns <legacyBold>True</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="c1148c61b69984c413f5a16b6b93c7c2" id="tgt6" class="tgtSentence"> Otherwise, it returns <legacyBold>False</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b22d8da84bcac0a6eeb47bbdbdc4eef7" id="tgt7" class="tgtSentence">Using the <legacyBold>Supports</legacyBold> method, you can check for the ability of the <legacyBold>Recordset</legacyBold> object to add new records, use bookmarks, use the <legacyBold>Find</legacyBold> method, use scrolling, use the <legacyBold>Index</legacyBold> property, and to perform batch updates.</caps:sentence>
            <caps:sentence sentenceid="10bf0d6bdae6dfe6cc69589517729db6" id="tgt8" class="tgtSentence"> For a complete list of constants and their meanings, see <legacyLink xlink:href="4e10cda7-ce81-4466-94c2-844d38191cf1">CursorOptionEnum</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b0685071478da30c1f90aa1a957c8fc4" id="tgt9" class="tgtSentence">Although the <legacyBold>Supports</legacyBold> method may return <legacyBold>True</legacyBold> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</caps:sentence>
            <caps:sentence sentenceid="c11d4d26da22374454cc8057a2f9d0f3" id="tgt10" class="tgtSentence"> The <legacyBold>Supports</legacyBold> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</caps:sentence>
            <caps:sentence sentenceid="516aa5cf46074cb3e1c091091f90ff82" id="tgt11" class="tgtSentence"> For example, the <legacyBold>Supports</legacyBold> method may indicate that a <legacyBold>Recordset</legacyBold> object supports updates, even though the cursor is based on a multiple table join — some columns of which are not updateable.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>Supports</legacyBold> method is used to determine whether a specified <legacyBold>Recordset</legacyBold> object supports a particular type of functionality.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It has the following syntax:</caps:sentence>
        </para>
        <code>
        boolean = recordset.Supports(CursorOptions )</code>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">The <legacyBold>Supports</legacyBold> method returns a Boolean value that indicates whether the provider supports all of the features identified by the CursorOptions argument.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> You can use the <legacyBold>Supports</legacyBold> method to determine what types of functionality a <legacyBold>Recordset</legacyBold> object supports.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> If the <legacyBold>Recordset</legacyBold> object supports the features whose corresponding constants are in <legacyItalic>CursorOptions</legacyItalic>, the <legacyBold>Supports</legacyBold> method returns <legacyBold>True</legacyBold>.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Otherwise, it returns <legacyBold>False</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">Using the <legacyBold>Supports</legacyBold> method, you can check for the ability of the <legacyBold>Recordset</legacyBold> object to add new records, use bookmarks, use the <legacyBold>Find</legacyBold> method, use scrolling, use the <legacyBold>Index</legacyBold> property, and to perform batch updates.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> For a complete list of constants and their meanings, see <legacyLink xlink:href="4e10cda7-ce81-4466-94c2-844d38191cf1">CursorOptionEnum</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">Although the <legacyBold>Supports</legacyBold> method may return <legacyBold>True</legacyBold> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The <legacyBold>Supports</legacyBold> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> For example, the <legacyBold>Supports</legacyBold> method may indicate that a <legacyBold>Recordset</legacyBold> object supports updates, even though the cursor is based on a multiple table join — some columns of which are not updateable.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Bookmark Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 481dcc93-487b-490e-ac58-a1e9b2ebfd43
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
# Bookmark Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7d7595006aebab060685591790db073b" id="tgt1" class="tgtSentence">Indicates a bookmark that uniquely identifies the current record in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object or sets the current record in a <legacyBold>Recordset</legacyBold> object to the record identified by a valid bookmark.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9e3903f501b662d895e33216524bedc3" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Variant</languageKeyword> expression that evaluates to a valid bookmark.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="f30b7207bfb9b19528eff34062df875a" id="tgt4" class="tgtSentence">Use the <legacyBold>Bookmark</legacyBold> property to save the position of the current record and return to that record at any time.</caps:sentence>
            <caps:sentence sentenceid="b09a2f6c4e8650bd7cde4b96de560198" id="tgt5" class="tgtSentence"> Bookmarks are available only in <legacyBold>Recordset</legacyBold> objects that support bookmark functionality.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="62ef2ef321660f7fd2bf2d43a56bf7bc" id="tgt6" class="tgtSentence">When you open a <legacyBold>Recordset</legacyBold> object, each of its records has a unique bookmark.</caps:sentence>
            <caps:sentence sentenceid="d00c521dfc05900392d1d2d365aa9612" id="tgt7" class="tgtSentence"> To save the bookmark for the current record, assign the value of the <legacyBold>Bookmark</legacyBold> property to a variable.</caps:sentence>
            <caps:sentence sentenceid="e583ced6a5fd226e975bd0065baa6e36" id="tgt8" class="tgtSentence"> To quickly return to that record at any time after moving to a different record, set the <legacyBold>Recordset</legacyBold> object's <legacyBold>Bookmark</legacyBold> property to the value of that variable.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="02826d078e5407b7a971a6aa2434ddfd" id="tgt9" class="tgtSentence">The user may not be able to view the value of the bookmark.</caps:sentence>
            <caps:sentence sentenceid="daba2b5052d9a6282797321f16adf083" id="tgt10" class="tgtSentence"> Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="db29c131b21a0ac26c8f76dd54b2eb96" id="tgt11" class="tgtSentence">If you use the <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">Clone</legacyLink> method to create a copy of a <legacyBold>Recordset</legacyBold> object, the <legacyBold>Bookmark</legacyBold> property settings for the original and the duplicate <legacyBold>Recordset</legacyBold> objects are identical and you can use them interchangeably.</caps:sentence>
            <caps:sentence sentenceid="bc7eaf34a8127ed08717ba815aee80ea" id="tgt12" class="tgtSentence"> However, you cannot use bookmarks from different <legacyBold>Recordset</legacyBold> objects interchangeably, even if they were created from the same source or command.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="d3c0be4d41256a532ab48228ef9c684b" id="tgt13" class="tgtSentence">
                <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> object, the <legacyBold>Bookmark</legacyBold> property is always available.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt14" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b6573c6e-fee8-4267-a722-fadaec6eafe6">Visual Basic Example</link>
        <link xlink:href="bd2b9d85-e75e-4fc8-a392-076582019caa">Visual C++ Example</link>
        <link xlink:href="eecd75a8-3e4f-4a18-b1c1-4c053dd7833f">Visual J++ Example</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates a bookmark that uniquely identifies the current record in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object or sets the current record in a <legacyBold>Recordset</legacyBold> object to the record identified by a valid bookmark.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Variant</languageKeyword> expression that evaluates to a valid bookmark.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Bookmark</legacyBold> property to save the position of the current record and return to that record at any time.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Bookmarks are available only in <legacyBold>Recordset</legacyBold> objects that support bookmark functionality.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">When you open a <legacyBold>Recordset</legacyBold> object, each of its records has a unique bookmark.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> To save the bookmark for the current record, assign the value of the <legacyBold>Bookmark</legacyBold> property to a variable.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> To quickly return to that record at any time after moving to a different record, set the <legacyBold>Recordset</legacyBold> object's <legacyBold>Bookmark</legacyBold> property to the value of that variable.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The user may not be able to view the value of the bookmark.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If you use the <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">Clone</legacyLink> method to create a copy of a <legacyBold>Recordset</legacyBold> object, the <legacyBold>Bookmark</legacyBold> property settings for the original and the duplicate <legacyBold>Recordset</legacyBold> objects are identical and you can use them interchangeably.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> However, you cannot use bookmarks from different <legacyBold>Recordset</legacyBold> objects interchangeably, even if they were created from the same source or command.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src13" class="srcSentence">
                <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> object, the <legacyBold>Bookmark</legacyBold> property is always available.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b6573c6e-fee8-4267-a722-fadaec6eafe6">Visual Basic Example</link>
        <link xlink:href="bd2b9d85-e75e-4fc8-a392-076582019caa">Visual C++ Example</link>
        <link xlink:href="eecd75a8-3e4f-4a18-b1c1-4c053dd7833f">Visual J++ Example</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Accessing Rows in a Hierarchical Recordset"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 25f1d2a1-6d5e-4457-aa07-5db5c75dee18
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
# Accessing Rows in a Hierarchical Recordset
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b2fa8a12ac167fa527a3f93e5eda4366" id="tgt1" class="tgtSentence">The following example shows the steps necessary to access rows in a hierarchical <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>:  </caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence sentenceid="c11178c1c8774002b05fecc725b64b45" id="tgt2" class="tgtSentence">
                <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects from the <legacyBold>authors</legacyBold> and <legacyBold>titleauthor</legacyBold> tables are related by author ID.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="34474ac273b9767b4dc9f30402b022ca" id="tgt3" class="tgtSentence">The outer loop displays each author's first and last name, state, and identification.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4c3bfb609429ccb2d607e0d087b984c7" id="tgt4" class="tgtSentence">The appended <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> for each row is retrieved from the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection and assigned to <legacyItalic>rstTitleAuthor</legacyItalic>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0a2edddd0519de61a079fe154e330213" id="tgt5" class="tgtSentence">The inner loop displays four fields from each row in the appended <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="7d44972159e6608697a3f7fa6e3b64bc" id="tgt6" class="tgtSentence">The <legacyLink xlink:href="502d69b5-dc9a-455d-b115-a03bd39a552b">StayInSync</legacyLink> property is set to <languageKeyword>false</languageKeyword> for purposes of illustration, so that you can see the chapter change explicitly in each iteration of the outer loop.</caps:sentence>
          <caps:sentence sentenceid="efe6870cb782f7a7e9e5f058a9c92f23" id="tgt7" class="tgtSentence"> To make the code example more efficient, you can move the assignment in step 3 before the first line in step 2, so that the assignment is performed only once.</caps:sentence>
          <caps:sentence sentenceid="1a9d925576995c80dcec86ecd4a6f761" id="tgt8" class="tgtSentence"> Then set the <legacyLink xlink:href="502d69b5-dc9a-455d-b115-a03bd39a552b">StayInSync</legacyLink> property to <languageKeyword>true</languageKeyword>, so that <legacyItalic>rstTitleAuthor</legacyItalic> will implicitly and automatically change to the corresponding chapter whenever <legacyItalic>rst</legacyItalic> moves to a new row.</caps:sentence>
        </para>
      </introduction>
      <codeExample>
        <code>Sub datashape()
   Dim cnn As New ADODB.Connection
   Dim rst As New ADODB.Recordset
   Dim rstTitleAuthor As New ADODB.Recordset

   cnn.Provider = "MSDataShape"
   cnn.Open    "Data Provider=MSDASQL;" &amp; _
               "Data Source=SRV;Integrated Security=SSPI;Database=Pubs"
' STEP 1
   rst.StayInSync = FALSE
   rst.Open    "SHAPE  {select * from authors} "  &amp; _ 
               "APPEND ({select * from titleauthor} " &amp; _
               "RELATE au_id TO au_id) AS chapTitleAuthor", _
               cnn
' STEP 2
   While Not rst.EOF
      Debug.Print    rst("au_fname"), rst("au_lname"), _
                     rst("state"), rst("au_id")
' STEP 3
      Set rstTitleAuthor = rst("chapTitleAuthor").Value
' STEP 4
      While Not rstTitleAuthor.EOF
         Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _
                     rstTitleAuthor(2), rstTitleAuthor(3)
         rstTitleAuthor.MoveNext
      Wend
      rst.MoveNext
   Wend
End Sub</code>
      </codeExample>
      <relatedTopics>
        <link xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">Data Shaping Summary</link>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</link>
        <link xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">Shape APPEND Clause</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
        <link xlink:href="3fdfead2-b5ab-4163-9b1d-3d2143a5db8c">Shape COMPUTE Clause</link>
        <link xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications Functions</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following example shows the steps necessary to access rows in a hierarchical <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>:  </caps:sentence>
        </para>
        <list class="ordered">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">
                <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects from the <legacyBold>authors</legacyBold> and <legacyBold>titleauthor</legacyBold> tables are related by author ID.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">The outer loop displays each author's first and last name, state, and identification.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">The appended <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> for each row is retrieved from the <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection and assigned to <legacyItalic>rstTitleAuthor</legacyItalic>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">The inner loop displays four fields from each row in the appended <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src6" class="srcSentence">The <legacyLink xlink:href="502d69b5-dc9a-455d-b115-a03bd39a552b">StayInSync</legacyLink> property is set to <languageKeyword>false</languageKeyword> for purposes of illustration, so that you can see the chapter change explicitly in each iteration of the outer loop.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> To make the code example more efficient, you can move the assignment in step 3 before the first line in step 2, so that the assignment is performed only once.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> Then set the <legacyLink xlink:href="502d69b5-dc9a-455d-b115-a03bd39a552b">StayInSync</legacyLink> property to <languageKeyword>true</languageKeyword>, so that <legacyItalic>rstTitleAuthor</legacyItalic> will implicitly and automatically change to the corresponding chapter whenever <legacyItalic>rst</legacyItalic> moves to a new row.</caps:sentence>
        </para>
      </introduction>
      <codeExample>
        <code>Sub datashape()
   Dim cnn As New ADODB.Connection
   Dim rst As New ADODB.Recordset
   Dim rstTitleAuthor As New ADODB.Recordset

   cnn.Provider = "MSDataShape"
   cnn.Open    "Data Provider=MSDASQL;" &amp; _
               "Data Source=SRV;Integrated Security=SSPI;Database=Pubs"
' STEP 1
   rst.StayInSync = FALSE
   rst.Open    "SHAPE  {select * from authors} "  &amp; _ 
               "APPEND ({select * from titleauthor} " &amp; _
               "RELATE au_id TO au_id) AS chapTitleAuthor", _
               cnn
' STEP 2
   While Not rst.EOF
      Debug.Print    rst("au_fname"), rst("au_lname"), _
                     rst("state"), rst("au_id")
' STEP 3
      Set rstTitleAuthor = rst("chapTitleAuthor").Value
' STEP 4
      While Not rstTitleAuthor.EOF
         Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _
                     rstTitleAuthor(2), rstTitleAuthor(3)
         rstTitleAuthor.MoveNext
      Wend
      rst.MoveNext
   Wend
End Sub</code>
      </codeExample>
      <relatedTopics>
        <link xlink:href="4cb5fd29-4e56-46ac-ae48-a6771c321c0c">Data Shaping Summary</link>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="ea691475-0f03-4abe-a785-b77e77712d1d">Formal Shape Grammar</link>
        <link xlink:href="523009ce-e01b-4e2d-a7df-816d7688aff0">Microsoft Data Shaping Service for OLE DB</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="d49d48d2-ac2d-4c11-895c-5a149b444620">Required Providers for Data Shaping</link>
        <link xlink:href="f90fcf55-6b24-401d-94e1-d65bd24bd342">Shape APPEND Clause</link>
        <link xlink:href="1fac7831-a187-4b15-9b43-aad380c5556c">Shape Commands in General</link>
        <link xlink:href="3fdfead2-b5ab-4163-9b1d-3d2143a5db8c">Shape COMPUTE Clause</link>
        <link xlink:href="ccbdea9d-f9cf-4b0c-ade2-2d65311e12dc">Visual Basic for Applications Functions</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
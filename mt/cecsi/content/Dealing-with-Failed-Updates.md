---
title: "Dealing with Failed Updates"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 299c37bd-19ff-4261-8571-b9665687e075
caps.latest.revision: 2
caps.handback.revision: 2
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
# Dealing with Failed Updates
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9d09a7f99f11d991e2f1512e96c4ade4" id="tgt1" class="tgtSentence">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application.</caps:sentence>
          <caps:sentence sentenceid="df59ee59118e58d6c6edb110ead1488b" id="tgt2" class="tgtSentence"> However, if the database is shared with other users, a typical error is that someone else modifies the field before you do.</caps:sentence>
          <caps:sentence sentenceid="cf31ad34833f75cb1a78d1f3643f06fe" id="tgt3" class="tgtSentence"> This type of error is called a conflict.</caps:sentence>
          <caps:sentence sentenceid="f1ca835d5ad9d8eee72a91e011f2dc6b" id="tgt4" class="tgtSentence"> ADO detects this situation and reports an error.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt5" class="tgtSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="df6114e6f82e40e2acf3d04f30afd00d" id="tgt6" class="tgtSentence">If there are update errors, they will be trapped in an error-handling routine.</caps:sentence>
            <caps:sentence sentenceid="5ba282fdc2e466ed94fbc2447a5f26ec" id="tgt7" class="tgtSentence"> Filter the Recordset with the adFilterConflictingRecords constant so that only the conflicting rows are visible.</caps:sentence>
            <caps:sentence sentenceid="ff8cd1679251a30387169465ec191e9a" id="tgt8" class="tgtSentence"> In this example, the error-resolution strategy is merely to print the author's first and last names (au_fname and au_lname).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="10d62d8d07e6150841e23453dfa5fc31" id="tgt9" class="tgtSentence">The code to alert the user to the update conflict looks like this:</caps:sentence>
          </para>
          <code>objRs.Filter = adFilterConflictingRecords
objRs.MoveFirst
Do While Not objRst.EOF
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname
   objRs.MoveNext
Loop</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> However, if the database is shared with other users, a typical error is that someone else modifies the field before you do.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This type of error is called a conflict.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> ADO detects this situation and reports an error.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">If there are update errors, they will be trapped in an error-handling routine.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Filter the Recordset with the adFilterConflictingRecords constant so that only the conflicting rows are visible.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> In this example, the error-resolution strategy is merely to print the author's first and last names (au_fname and au_lname).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The code to alert the user to the update conflict looks like this:</caps:sentence>
          </para>
          <code>objRs.Filter = adFilterConflictingRecords
objRs.MoveFirst
Do While Not objRst.EOF
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname
   objRs.MoveNext
Loop</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="0cb548e0-fcb4-4c49-98c8-be287911f826">Batch Mode</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
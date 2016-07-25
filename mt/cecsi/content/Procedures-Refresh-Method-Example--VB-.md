---
title: "Procedures Refresh Method Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 499679bd-287b-487d-bdfb-3803abffec1c
caps.latest.revision: 8
caps.handback.revision: 8
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
# Procedures Refresh Method Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9bc54b0314f9478544729269136e8750" id="tgt1" class="tgtSentence">The following code shows how to refresh the <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="18151bc84aace693268796b1cb9b0796" id="tgt2" class="tgtSentence"> This is required before <legacyLink xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure</legacyLink> objects from the <legacyBold>Catalog</legacyBold> can be accessed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginProceduresRefreshVB
Sub Main()
    On Error GoTo ProcedureRefreshError

    Dim cat As New ADOX.Catalog
    
    ' Open the Catalog
    cat.ActiveConnection = _
        "Provider='Microsoft.Jet.OLEDB.4.0';" &amp; _
        "Data Source='Northwind.mdb';"
    
    ' Refresh the Procedures collection
    cat.Procedures.Refresh

    'Clean up
    Set cat.ActiveConnection = Nothing
    Set cat = Nothing
    Exit Sub
    
ProcedureRefreshError:
    Set cat = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
' EndProceduresRefreshVB</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
        <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following code shows how to refresh the <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This is required before <legacyLink xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure</legacyLink> objects from the <legacyBold>Catalog</legacyBold> can be accessed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginProceduresRefreshVB
Sub Main()
    On Error GoTo ProcedureRefreshError

    Dim cat As New ADOX.Catalog
    
    ' Open the Catalog
    cat.ActiveConnection = _
        "Provider='Microsoft.Jet.OLEDB.4.0';" &amp; _
        "Data Source='Northwind.mdb';"
    
    ' Refresh the Procedures collection
    cat.Procedures.Refresh

    'Clean up
    Set cat.ActiveConnection = Nothing
    Set cat = Nothing
    Exit Sub
    
ProcedureRefreshError:
    Set cat = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
' EndProceduresRefreshVB</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
        <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
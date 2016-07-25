---
title: "Views Refresh Method Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cdad2d66-6ade-40dc-9e74-e40cfa9bc127
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
# Views Refresh Method Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6af9af7623ff56e05c8eec8649ca1f4e" id="tgt1" class="tgtSentence">The following code shows how to refresh the <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="4fa109505ea1036aa6299e22a1349e26" id="tgt2" class="tgtSentence"> This is required before <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> objects from the <legacyBold>Catalog</legacyBold> can be accessed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginViewsRefreshVB
Sub Main()
    On Error GoTo ProcedureViewsRefreshError

    Dim cat As New ADOX.Catalog
    
    ' Open the catalog.
    cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" &amp; _
        "Data Source='Northwind.mdb';"
    
    ' Refresh the Procedures collection.
    cat.Views.Refresh
    
    'Clean up
    Set cat = Nothing
    Exit Sub
    
ProcedureViewsRefreshError:

    If Not cat Is Nothing Then
        Set cat = Nothing
    End If
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
' EndViewsRefreshVB</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method</link>
        <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following code shows how to refresh the <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink> collection of a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This is required before <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> objects from the <legacyBold>Catalog</legacyBold> can be accessed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginViewsRefreshVB
Sub Main()
    On Error GoTo ProcedureViewsRefreshError

    Dim cat As New ADOX.Catalog
    
    ' Open the catalog.
    cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" &amp; _
        "Data Source='Northwind.mdb';"
    
    ' Refresh the Procedures collection.
    cat.Views.Refresh
    
    'Clean up
    Set cat = Nothing
    Exit Sub
    
ProcedureViewsRefreshError:

    If Not cat Is Nothing Then
        Set cat = Nothing
    End If
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
' EndViewsRefreshVB</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method</link>
        <link xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
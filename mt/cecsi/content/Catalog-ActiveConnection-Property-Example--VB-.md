---
title: "Catalog ActiveConnection Property Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bb3274b1-764d-43a7-a49f-ef55680ecd26
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
# Catalog ActiveConnection Property Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a4b5d562b4593ebafd6dc840bb2609b2" id="tgt1" class="tgtSentence">Setting the <legacyLink xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection</legacyLink> property to a valid, open connection "opens" the catalog.</caps:sentence>
          <caps:sentence sentenceid="3beb957b5afb4aa0e1956476f4e4f25b" id="tgt2" class="tgtSentence"> From an open catalog, you can access the schema objects contained within that catalog.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginOpenConnectionVB
Sub Main()
    On Error GoTo OpenConnectionError
    
    Dim cnn As New ADODB.Connection
    Dim cat As New ADOX.Catalog
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" &amp; _
        "Data Source= 'Northwind.mdb';"
    Set cat.ActiveConnection = cnn
    Debug.Print cat.Tables(0).Type
    
    'Clean up
    cnn.Close
    Set cat = Nothing
    Set cnn = Nothing
    Exit Sub
    
OpenConnectionError:
    
    Set cat = Nothing

    If Not cnn Is Nothing Then
        If cnn.State = adStateOpen Then cnn.Close
    End If
    Set cnn = Nothing

    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
' EndOpenConnectionVB</code>
          <para>
            <caps:sentence sentenceid="e8c4cf8507d6c7087b62ae11fb621199" id="tgt3" class="tgtSentence">Setting the <legacyBold>ActiveConnection</legacyBold> property to a valid connection string also "opens" the catalog.</caps:sentence>
          </para>
          <code>Attribute VB_Name = "Catalog"</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection Property</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
        <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection</link>
        <link xlink:href="7b6e14bb-fb69-4d74-aaca-f5d380f4d887">Type Property (Table)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Setting the <legacyLink xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection</legacyLink> property to a valid, open connection "opens" the catalog.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> From an open catalog, you can access the schema objects contained within that catalog.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginOpenConnectionVB
Sub Main()
    On Error GoTo OpenConnectionError
    
    Dim cnn As New ADODB.Connection
    Dim cat As New ADOX.Catalog
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" &amp; _
        "Data Source= 'Northwind.mdb';"
    Set cat.ActiveConnection = cnn
    Debug.Print cat.Tables(0).Type
    
    'Clean up
    cnn.Close
    Set cat = Nothing
    Set cnn = Nothing
    Exit Sub
    
OpenConnectionError:
    
    Set cat = Nothing

    If Not cnn Is Nothing Then
        If cnn.State = adStateOpen Then cnn.Close
    End If
    Set cnn = Nothing

    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
' EndOpenConnectionVB</code>
          <para>
            <caps:sentence id="src3" class="srcSentence">Setting the <legacyBold>ActiveConnection</legacyBold> property to a valid connection string also "opens" the catalog.</caps:sentence>
          </para>
          <code>Attribute VB_Name = "Catalog"</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection Property</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
        <link xlink:href="38d750e7-f3fb-426e-b4b4-55eea4f1a654">Tables Collection</link>
        <link xlink:href="7b6e14bb-fb69-4d74-aaca-f5d380f4d887">Type Property (Table)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Parameters Collection, Command Property Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7df1089e-69b7-476e-9244-19947c087351
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
# Parameters Collection, Command Property Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c4e4b685c0dfeb672237ab4f34141f6e" id="tgt1" class="tgtSentence">The following code demonstrates how to use the <legacyLink xlink:href="bcc9146f-586f-4e69-9c10-863440c9cffa">Command</legacyLink> property with the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object to retrieve parameter information for the procedure.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginParametersVB
Sub Main()
    On Error GoTo ProcedureParametersError

    Dim cnn As New ADODB.Connection
    Dim cmd As ADODB.Command
    Dim prm As ADODB.Parameter
    Dim cat As New ADOX.Catalog
    
    ' Open the Connection
    cnn.Open _
        "Provider='Microsoft.Jet.OLEDB.4.0';" &amp; _
        "Data Source='Northwind.mdb';"
    
    ' Open the catalog
    Set cat.ActiveConnection = cnn
    
    ' Get the command object
    Set cmd = cat.Procedures("CustomerById").Command
    
    ' Retrieve Parameter information
    cmd.Parameters.Refresh
    For Each prm In cmd.Parameters
        Debug.Print prm.Name &amp; ":" &amp; prm.Type
    Next
   
    'Clean up
    cnn.Close
    Set cat = Nothing
    Set cmd = Nothing
    Set cnn = Nothing
    Exit Sub
    
ProcedureParametersError:

    Set cat = Nothing
    Set cmd = Nothing
    
    If Not cnn Is Nothing Then
        If cnn.State = adStateOpen Then cnn.Close
    End If
    Set cnn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
' EndParametersVB</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection Property</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="bcc9146f-586f-4e69-9c10-863440c9cffa">Command Property</link>
        <link xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure Object</link>
        <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following code demonstrates how to use the <legacyLink xlink:href="bcc9146f-586f-4e69-9c10-863440c9cffa">Command</legacyLink> property with the <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object to retrieve parameter information for the procedure.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginParametersVB
Sub Main()
    On Error GoTo ProcedureParametersError

    Dim cnn As New ADODB.Connection
    Dim cmd As ADODB.Command
    Dim prm As ADODB.Parameter
    Dim cat As New ADOX.Catalog
    
    ' Open the Connection
    cnn.Open _
        "Provider='Microsoft.Jet.OLEDB.4.0';" &amp; _
        "Data Source='Northwind.mdb';"
    
    ' Open the catalog
    Set cat.ActiveConnection = cnn
    
    ' Get the command object
    Set cmd = cat.Procedures("CustomerById").Command
    
    ' Retrieve Parameter information
    cmd.Parameters.Refresh
    For Each prm In cmd.Parameters
        Debug.Print prm.Name &amp; ":" &amp; prm.Type
    Next
   
    'Clean up
    cnn.Close
    Set cat = Nothing
    Set cmd = Nothing
    Set cnn = Nothing
    Exit Sub
    
ProcedureParametersError:

    Set cat = Nothing
    Set cmd = Nothing
    
    If Not cnn Is Nothing Then
        If cnn.State = adStateOpen Then cnn.Close
    End If
    Set cnn = Nothing
    
    If Err &lt;&gt; 0 Then
        MsgBox Err.Source &amp; "--&gt;" &amp; Err.Description, , "Error"
    End If
End Sub
' EndParametersVB</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="25fff69b-7556-4a28-b6f5-600a4bb0f607">ActiveConnection Property</link>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="bcc9146f-586f-4e69-9c10-863440c9cffa">Command Property</link>
        <link xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure Object</link>
        <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
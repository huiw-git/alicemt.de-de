---
title: "GetObjectOwner and SetObjectOwner Methods Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e44ec3d4-42ae-447d-aaed-bdea53cb0cca
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
# GetObjectOwner and SetObjectOwner Methods Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8c028ea16ca017b4f81a99893c057f04" id="tgt1" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="8965adf0-9075-4125-8142-73eb700029c3">GetObjectOwner</legacyLink> and <legacyLink xlink:href="e5170a37-9d6e-43db-bfb6-9b6631fa3048">SetObjectOwner</legacyLink> methods.</caps:sentence>
          <caps:sentence sentenceid="40df0ef09d45354abe0bdb5d102b86eb" id="tgt2" class="tgtSentence"> This code assumes the existence of the group Accounting (see the <legacyLink xlink:href="c9426757-9cdd-4a95-b506-d3d011569109">Groups and Users Append, ChangePassword Methods Example (VB)</legacyLink> to see how to add this group to the system).</caps:sentence>
          <caps:sentence sentenceid="6c5b873bd53b37b48d1f1b4ee85c5f53" id="tgt3" class="tgtSentence"> The owner of the Categories table is set to Accounting.</caps:sentence>
        </para>
        <code>' BeginOwnersVB
Sub OwnersX()

    Dim tblLoop As New ADOX.Table
    Dim cat As New ADOX.Catalog
    Dim strOwner As String

    ' Open the Catalog.
    cat.ActiveConnection = "Provider=Microsoft.Jet.OLEDB.4.0;" &amp; _
        "Data Source=c:\Program Files\" &amp; _
        "Microsoft Office\Office\Samples\Northwind.mdb;" &amp; _
        "jet oledb:system database=" &amp; _
        "c:\Program Files\Microsoft Office\Office\system.mdw"

    ' Print the original owner of Categories
    strOwner = cat.GetObjectOwner("Categories", adPermObjTable)
    Debug.Print "Owner of Categories: " &amp; strOwner

    ' Set the owner of Categories to Accounting
    cat.SetObjectOwner "Categories", adPermObjTable, "Accounting"

    ' List the owners of all tables and columns in the catalog.
    For Each tblLoop In cat.Tables
        Debug.Print "Table: " &amp; tblLoop.Name
        Debug.Print "   Owner: " &amp; _
            cat.GetObjectOwner(tblLoop.Name, adPermObjTable)
    Next tblLoop
    
    ' Restore the original owner of Categories
    cat.SetObjectOwner "Categories", adPermObjTable, strOwner

End Sub
' EndOwnersVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="8965adf0-9075-4125-8142-73eb700029c3">GetObjectOwner Method</link>
        <link xlink:href="e5170a37-9d6e-43db-bfb6-9b6631fa3048">SetObjectOwner Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example demonstrates the <legacyLink xlink:href="8965adf0-9075-4125-8142-73eb700029c3">GetObjectOwner</legacyLink> and <legacyLink xlink:href="e5170a37-9d6e-43db-bfb6-9b6631fa3048">SetObjectOwner</legacyLink> methods.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This code assumes the existence of the group Accounting (see the <legacyLink xlink:href="c9426757-9cdd-4a95-b506-d3d011569109">Groups and Users Append, ChangePassword Methods Example (VB)</legacyLink> to see how to add this group to the system).</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The owner of the Categories table is set to Accounting.</caps:sentence>
        </para>
        <code>' BeginOwnersVB
Sub OwnersX()

    Dim tblLoop As New ADOX.Table
    Dim cat As New ADOX.Catalog
    Dim strOwner As String

    ' Open the Catalog.
    cat.ActiveConnection = "Provider=Microsoft.Jet.OLEDB.4.0;" &amp; _
        "Data Source=c:\Program Files\" &amp; _
        "Microsoft Office\Office\Samples\Northwind.mdb;" &amp; _
        "jet oledb:system database=" &amp; _
        "c:\Program Files\Microsoft Office\Office\system.mdw"

    ' Print the original owner of Categories
    strOwner = cat.GetObjectOwner("Categories", adPermObjTable)
    Debug.Print "Owner of Categories: " &amp; strOwner

    ' Set the owner of Categories to Accounting
    cat.SetObjectOwner "Categories", adPermObjTable, "Accounting"

    ' List the owners of all tables and columns in the catalog.
    For Each tblLoop In cat.Tables
        Debug.Print "Table: " &amp; tblLoop.Name
        Debug.Print "   Owner: " &amp; _
            cat.GetObjectOwner(tblLoop.Name, adPermObjTable)
    Next tblLoop
    
    ' Restore the original owner of Categories
    cat.SetObjectOwner "Categories", adPermObjTable, strOwner

End Sub
' EndOwnersVB</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object</link>
        <link xlink:href="8965adf0-9075-4125-8142-73eb700029c3">GetObjectOwner Method</link>
        <link xlink:href="e5170a37-9d6e-43db-bfb6-9b6631fa3048">SetObjectOwner Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
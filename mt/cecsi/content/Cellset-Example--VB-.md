---
title: "Cellset Example (VB)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2666ad1c-b48e-4b2c-b269-5a9f4e4a7810
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
# Cellset Example (VB)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="44affe04e87a04179d5e5661de2f5dbb" id="tgt1" class="tgtSentence">This Visual Basic project demonstrates the basics of using ADO MD to access cube data.</caps:sentence>
          <caps:sentence sentenceid="8490d5b11621351c80e21b76e45ca57e" id="tgt2" class="tgtSentence"> It displays member captions for column and row headers, then displays formatted values of specific cells within the cellset.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>Private Sub cmdCellSettoDebugWindow_Click()
Dim cat As New ADOMD.<codeFeaturedElement xmlns="">Catalog</codeFeaturedElement>
Dim cst As New ADOMD.<codeFeaturedElement xmlns="">Cellset</codeFeaturedElement>
Dim i As Integer
Dim j As Integer
Dim strServer As String
Dim strSource As String
Dim strColumnHeader As String
Dim strRowText As String

On Error GoTo Error_cmdCellSettoDebugWindow_Click
Screen.MousePointer = vbHourglass
'*-----------------------------------------------------------------------
'* Set Server to Local Host
'*-----------------------------------------------------------------------
    strServer = "LOCALHOST"

'*-----------------------------------------------------------------------
'* Set MDX query string Source
'*-----------------------------------------------------------------------
    strSource = strSource &amp; "SELECT "
    strSource = strSource &amp; "{[Measures].members} ON COLUMNS,"
    strSource = strSource &amp; _
        "NON EMPTY [Store].[Store City].members ON ROWS"
    strSource = strSource &amp; " FROM Sales"

'*-----------------------------------------------------------------------
'* Set Active Connection
'*-----------------------------------------------------------------------
        cat.ActiveConnection = "Data Source=" &amp; strServer &amp; _
            ";Provider=msolap;"

'*-----------------------------------------------------------------------
'* Set Cell Set source to MDX query string
'*-----------------------------------------------------------------------
        cst.<codeFeaturedElement xmlns="">Source</codeFeaturedElement> = strSource

'*-----------------------------------------------------------------------
'* Set Cell Sets active connection to current connection
'*-----------------------------------------------------------------------
    Set cst.<codeFeaturedElement xmlns="">ActiveConnection</codeFeaturedElement> = cat.<codeFeaturedElement xmlns="">ActiveConnection</codeFeaturedElement>

'*-----------------------------------------------------------------------
'* Open Cell Set
'*-----------------------------------------------------------------------
    cst.<codeFeaturedElement xmlns="">Open</codeFeaturedElement>

'*-----------------------------------------------------------------------
'* Allow space for Row Header Text
'*-----------------------------------------------------------------------
strColumnHeader = vbTab &amp; vbTab &amp; vbTab &amp; vbTab &amp; vbTab &amp; vbTab

'*-----------------------------------------------------------------------
'* Loop through Column Headers
'*-----------------------------------------------------------------------
       For i = 0 To cst.<codeFeaturedElement xmlns="">Axes</codeFeaturedElement>(0).<codeFeaturedElement xmlns="">Positions</codeFeaturedElement>.Count - 1
            strColumnHeader = strColumnHeader &amp; _
                cst.Axes(0).Positions(i).<codeFeaturedElement xmlns="">Members</codeFeaturedElement>(0).<codeFeaturedElement xmlns="">Caption</codeFeaturedElement> &amp; vbTab &amp; _
                    vbTab &amp; vbTab &amp; vbTab
       Next
       Debug.Print vbTab &amp; strColumnHeader &amp; vbCrLf

'*-----------------------------------------------------------------------
'* Loop through Row Headers and Provide data for each row
'*-----------------------------------------------------------------------
        strRowText = ""
        For j = 0 To cst.<codeFeaturedElement xmlns="">Axes</codeFeaturedElement>(1).<codeFeaturedElement xmlns="">Positions</codeFeaturedElement>.Count - 1
            strRowText = strRowText &amp; _
                cst.Axes(1).Positions(j).<codeFeaturedElement xmlns="">Members</codeFeaturedElement>(0).<codeFeaturedElement xmlns="">Caption</codeFeaturedElement> &amp; vbTab &amp; _
                    vbTab &amp; vbTab &amp; vbTab
            For k = 0 To cst.<codeFeaturedElement xmlns="">Axes</codeFeaturedElement>(0).<codeFeaturedElement xmlns="">Positions</codeFeaturedElement>.Count - 1
                strRowText = strRowText &amp; cst(k, j).<codeFeaturedElement xmlns="">FormattedValue</codeFeaturedElement> &amp; _
                    vbTab &amp; vbTab &amp; vbTab &amp; vbTab
            Next
            Debug.Print strRowText &amp; vbCrLf
            strRowText = ""
        Next

    Screen.MousePointer = vbDefault
Exit Sub

Error_cmdCellSettoDebugWindow_Click:
   Beep
   Screen.MousePointer = vbDefault
   MsgBox "The Following Error has occurred:" &amp; vbCrLf &amp; _
      Err.Description, vbCritical, " Error!"
   Exit Sub
End Sub</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This Visual Basic project demonstrates the basics of using ADO MD to access cube data.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It displays member captions for column and row headers, then displays formatted values of specific cells within the cellset.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>Private Sub cmdCellSettoDebugWindow_Click()
Dim cat As New ADOMD.<codeFeaturedElement xmlns="">Catalog</codeFeaturedElement>
Dim cst As New ADOMD.<codeFeaturedElement xmlns="">Cellset</codeFeaturedElement>
Dim i As Integer
Dim j As Integer
Dim strServer As String
Dim strSource As String
Dim strColumnHeader As String
Dim strRowText As String

On Error GoTo Error_cmdCellSettoDebugWindow_Click
Screen.MousePointer = vbHourglass
'*-----------------------------------------------------------------------
'* Set Server to Local Host
'*-----------------------------------------------------------------------
    strServer = "LOCALHOST"

'*-----------------------------------------------------------------------
'* Set MDX query string Source
'*-----------------------------------------------------------------------
    strSource = strSource &amp; "SELECT "
    strSource = strSource &amp; "{[Measures].members} ON COLUMNS,"
    strSource = strSource &amp; _
        "NON EMPTY [Store].[Store City].members ON ROWS"
    strSource = strSource &amp; " FROM Sales"

'*-----------------------------------------------------------------------
'* Set Active Connection
'*-----------------------------------------------------------------------
        cat.ActiveConnection = "Data Source=" &amp; strServer &amp; _
            ";Provider=msolap;"

'*-----------------------------------------------------------------------
'* Set Cell Set source to MDX query string
'*-----------------------------------------------------------------------
        cst.<codeFeaturedElement xmlns="">Source</codeFeaturedElement> = strSource

'*-----------------------------------------------------------------------
'* Set Cell Sets active connection to current connection
'*-----------------------------------------------------------------------
    Set cst.<codeFeaturedElement xmlns="">ActiveConnection</codeFeaturedElement> = cat.<codeFeaturedElement xmlns="">ActiveConnection</codeFeaturedElement>

'*-----------------------------------------------------------------------
'* Open Cell Set
'*-----------------------------------------------------------------------
    cst.<codeFeaturedElement xmlns="">Open</codeFeaturedElement>

'*-----------------------------------------------------------------------
'* Allow space for Row Header Text
'*-----------------------------------------------------------------------
strColumnHeader = vbTab &amp; vbTab &amp; vbTab &amp; vbTab &amp; vbTab &amp; vbTab

'*-----------------------------------------------------------------------
'* Loop through Column Headers
'*-----------------------------------------------------------------------
       For i = 0 To cst.<codeFeaturedElement xmlns="">Axes</codeFeaturedElement>(0).<codeFeaturedElement xmlns="">Positions</codeFeaturedElement>.Count - 1
            strColumnHeader = strColumnHeader &amp; _
                cst.Axes(0).Positions(i).<codeFeaturedElement xmlns="">Members</codeFeaturedElement>(0).<codeFeaturedElement xmlns="">Caption</codeFeaturedElement> &amp; vbTab &amp; _
                    vbTab &amp; vbTab &amp; vbTab
       Next
       Debug.Print vbTab &amp; strColumnHeader &amp; vbCrLf

'*-----------------------------------------------------------------------
'* Loop through Row Headers and Provide data for each row
'*-----------------------------------------------------------------------
        strRowText = ""
        For j = 0 To cst.<codeFeaturedElement xmlns="">Axes</codeFeaturedElement>(1).<codeFeaturedElement xmlns="">Positions</codeFeaturedElement>.Count - 1
            strRowText = strRowText &amp; _
                cst.Axes(1).Positions(j).<codeFeaturedElement xmlns="">Members</codeFeaturedElement>(0).<codeFeaturedElement xmlns="">Caption</codeFeaturedElement> &amp; vbTab &amp; _
                    vbTab &amp; vbTab &amp; vbTab
            For k = 0 To cst.<codeFeaturedElement xmlns="">Axes</codeFeaturedElement>(0).<codeFeaturedElement xmlns="">Positions</codeFeaturedElement>.Count - 1
                strRowText = strRowText &amp; cst(k, j).<codeFeaturedElement xmlns="">FormattedValue</codeFeaturedElement> &amp; _
                    vbTab &amp; vbTab &amp; vbTab &amp; vbTab
            Next
            Debug.Print strRowText &amp; vbCrLf
            strRowText = ""
        Next

    Screen.MousePointer = vbDefault
Exit Sub

Error_cmdCellSettoDebugWindow_Click:
   Beep
   Screen.MousePointer = vbDefault
   MsgBox "The Following Error has occurred:" &amp; vbCrLf &amp; _
      Err.Description, vbCritical, " Error!"
   Exit Sub
End Sub</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
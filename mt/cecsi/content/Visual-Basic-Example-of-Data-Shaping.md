---
title: "Visual Basic Example of Data Shaping"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d95dd499-19e2-4ce7-b16e-f56a04a9519c
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
# Visual Basic Example of Data Shaping
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <code>' This application makes use of Microsoft Hierarchical FlexGrid
' Control, which is named as MSHFLexGrid.
Const SHAPER = "MSDataShape"
Const DP = "SQLOLEDB"
Const DS = "MySQLServer"
Const DB = "Northwind"

Private Sub Form_Load()
    FirstExample
End Sub

Private Sub Form_Resize()
    MSHFlexGrid.Top = 0
    MSHFlexGrid.Left = 0
    MSHFlexGrid.Width = Me.ScaleWidth
    MSHFlexGrid.Height = Me.ScaleHeight
End Sub

Private Sub FirstExample()
    Dim con As ADODB.Connection
    Dim rst As ADODB.Recordset
    Dim sCmd As String
    
    Set con = New ADODB.Connection
    Set rst = New ADODB.Recordset
    
    con.ConnectionString = ConnectionString(SHAPER, DP, DS, DB)
    con.Open
    
    sCmd = "SHAPE {SELECT CustomerID, ContactName FROM Customers} " _
        &amp; "APPEND ({SELECT OrderID, OrderDate, CustomerID FROM Orders} " _
        &amp; "AS chapOrders " _
        &amp; "RELATE customerID TO customerID)"

    rst.Open sCmd, con, adOpenStatic, 2
    Set MSHFlexGrid.Recordset = rst
    
    rst.Close
    Set rst = Nothing
    
    con.Close
    Set con = Nothing
    
End Sub

Private Function ConnectionString(pr As String, _
                                  dpr As String, _
                                  dsr As String, _
                                  dbs As String)
    Dim s As String
    If pr = "" Then
        s = "Provider=" &amp; dpr &amp; _
          ";Data Source=" &amp; dsr &amp; _
          ";Initial Catalog=" &amp; dbs &amp; _
          ";Integrated Security=SSPI;"
    Else
        s = "Provider=" &amp; pr &amp; _
          ";Data Provider=" &amp; dpr &amp; _
          ";Data Source=" &amp; dsr &amp; _
          ";Initial Catalog=" &amp; dbs &amp; _
          ";Integrated Security=SSPI;"
    End If
    ConnectionString = s
End Function
                                  </code>
      </introduction>
      <section>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="eab739b3bf4161ac88e7077cd075b8e8" id="tgt1" class="tgtSentence">Try It!</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="86d9db8183570c860d3c2447f50b5f69" id="tgt2" class="tgtSentence">Create a Visual Basic Standard EXE application project</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="4fb29d074d50565c24ab46abe08014fd" id="tgt3" class="tgtSentence">Select <legacyBold>Components</legacyBold> from the <legacyBold>Project</legacyBold> menu in Visual Studio</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="f6131f497308e5ffde3a80cfc1ed4182" id="tgt4" class="tgtSentence">Select "Microsoft Hierarchical FlexGrid Control 6.0 (OLEDB)" from the <legacyBold>Components</legacyBold> popup window and then click <legacyBold>Save</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a2eae50cdf5ae51bdacc717918c15611" id="tgt5" class="tgtSentence">Double-click the FlexGrid Control from the ToolBox pane in the Visual Basic workspace.</caps:sentence>
                    <caps:sentence sentenceid="e7f2ae2f10dc99e494c66e0e187c7c60" id="tgt6" class="tgtSentence"> Change the name of this instance to MSHFLEXGRID.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="0407bfe39f78d9bf0d052c549fe625af" id="tgt7" class="tgtSentence">Copy the preceding code and paste it into the <legacyBold>Code</legacyBold> page to replace any existing code.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fca2be630e2d1042ee6a1525bb379cc8" id="tgt8" class="tgtSentence">Select <legacyBold>Start</legacyBold> from the <legacyBold>Run</legacyBold> menu to execute the application.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <code>' This application makes use of Microsoft Hierarchical FlexGrid
' Control, which is named as MSHFLexGrid.
Const SHAPER = "MSDataShape"
Const DP = "SQLOLEDB"
Const DS = "MySQLServer"
Const DB = "Northwind"

Private Sub Form_Load()
    FirstExample
End Sub

Private Sub Form_Resize()
    MSHFlexGrid.Top = 0
    MSHFlexGrid.Left = 0
    MSHFlexGrid.Width = Me.ScaleWidth
    MSHFlexGrid.Height = Me.ScaleHeight
End Sub

Private Sub FirstExample()
    Dim con As ADODB.Connection
    Dim rst As ADODB.Recordset
    Dim sCmd As String
    
    Set con = New ADODB.Connection
    Set rst = New ADODB.Recordset
    
    con.ConnectionString = ConnectionString(SHAPER, DP, DS, DB)
    con.Open
    
    sCmd = "SHAPE {SELECT CustomerID, ContactName FROM Customers} " _
        &amp; "APPEND ({SELECT OrderID, OrderDate, CustomerID FROM Orders} " _
        &amp; "AS chapOrders " _
        &amp; "RELATE customerID TO customerID)"

    rst.Open sCmd, con, adOpenStatic, 2
    Set MSHFlexGrid.Recordset = rst
    
    rst.Close
    Set rst = Nothing
    
    con.Close
    Set con = Nothing
    
End Sub

Private Function ConnectionString(pr As String, _
                                  dpr As String, _
                                  dsr As String, _
                                  dbs As String)
    Dim s As String
    If pr = "" Then
        s = "Provider=" &amp; dpr &amp; _
          ";Data Source=" &amp; dsr &amp; _
          ";Initial Catalog=" &amp; dbs &amp; _
          ";Integrated Security=SSPI;"
    Else
        s = "Provider=" &amp; pr &amp; _
          ";Data Provider=" &amp; dpr &amp; _
          ";Data Source=" &amp; dsr &amp; _
          ";Initial Catalog=" &amp; dbs &amp; _
          ";Integrated Security=SSPI;"
    End If
    ConnectionString = s
End Function
                                  </code>
      </introduction>
      <section>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src1" class="srcSentence">Try It!</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src2" class="srcSentence">Create a Visual Basic Standard EXE application project</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src3" class="srcSentence">Select <legacyBold>Components</legacyBold> from the <legacyBold>Project</legacyBold> menu in Visual Studio</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">Select "Microsoft Hierarchical FlexGrid Control 6.0 (OLEDB)" from the <legacyBold>Components</legacyBold> popup window and then click <legacyBold>Save</legacyBold>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Double-click the FlexGrid Control from the ToolBox pane in the Visual Basic workspace.</caps:sentence>
                    <caps:sentence id="src6" class="srcSentence"> Change the name of this instance to MSHFLEXGRID.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Copy the preceding code and paste it into the <legacyBold>Code</legacyBold> page to replace any existing code.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Select <legacyBold>Start</legacyBold> from the <legacyBold>Run</legacyBold> menu to execute the application.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
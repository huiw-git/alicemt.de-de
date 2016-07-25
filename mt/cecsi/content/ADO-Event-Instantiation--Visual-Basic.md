---
title: "ADO Event Instantiation: Visual Basic"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dce0a2a3-326f-4aaf-a822-6c5549833afa
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
# ADO Event Instantiation: Visual Basic
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b113a0d29b7786df7491a70522e9c0c2" id="tgt1" class="tgtSentence">In order to handle ADO events in Microsoft® Visual Basic®, you must declare a module-level variable using the <legacyBold>WithEvents</legacyBold> keyword.</caps:sentence>
          <caps:sentence sentenceid="f193139996e25ab6c063b708c94010eb" id="tgt2" class="tgtSentence"> The variable can be declared only as part of a class module and must be declared at the module level.</caps:sentence>
          <caps:sentence sentenceid="5a158f03cd3f1d9b9675880357117a2f" id="tgt3" class="tgtSentence"> This is not as restrictive as it seems, however, because Visual Basic <legacyBold>Form</legacyBold> objects are also classes.</caps:sentence>
          <caps:sentence sentenceid="038ce18f50bc3efbeb5c4edd234c9448" id="tgt4" class="tgtSentence"> The simplest way to handle ADO events is to declare a variable using <legacyBold>WithEvents</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="ef489dcc2329fe830b44fcc08fdb3572" id="tgt5" class="tgtSentence"> The following example handles the <legacyBold>ConnectComplete</legacyBold> event for a <legacyBold>Connection</legacyBold> object:</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginEventExampleVB02
Dim WithEvents connEvent As Connection
Attribute connEvent.VB_VarHelpID = -1

Private Sub Form_Load()
Dim strConn As String

   ' Create a new object with event
   ' handling enabled.
   strConn = "Provider=sqloledb;" &amp; _
      "Data Source=MyServer;" &amp; _
      "Initial Catalog=Northwind;" &amp; _
      "Integrated Security=SSPI;"
   Set connEvent = New ADODB.Connection
   connEvent.Open strConn
End Sub

Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _
    adStatus As ADODB.EventStatusEnum, _
    ByVal pConnection As ADODB.Connection)
Dim strMsg As String

   If adStatus = adStatusErrorsOccurred Then
      Select Case pError.Number
         Case adErrOperationCancelled
            ' The operation was cancelled in the
            ' Will event. Notify the user and exit.
            strMsg = "I'm sorry you can't connect right now." &amp; vbCrLf
            strMsg = strMsg &amp; "Click OK to exit."
            Unload Me
         Case Else
            strMsg = "Error " &amp; Format(pError.Number) &amp; vbCrLf
            strMsg = strMsg &amp; pError.Description
            strMsg = strMsg &amp; "Click OK to exit."
            Unload Me
      End Select
   End If
   frmWait.btnOK.Enabled = True
End Sub
' EndEventExampleVB02</code>
          <para>
            <caps:sentence sentenceid="20cdc3dbeb7470fa59ca314751bca202" id="tgt6" class="tgtSentence">The <legacyBold>Connection</legacyBold> object is declared at the <legacyBold>Form</legacyBold> level using the <legacyBold>WithEvents</legacyBold> keyword to enable event handling.</caps:sentence>
            <caps:sentence sentenceid="547a17c9175496a214ca90fe064c14e2" id="tgt7" class="tgtSentence"> The Form_Load event handler actually creates the object by assigning a new <legacyBold>Connection</legacyBold> object to <legacyItalic>connEvent</legacyItalic> and then opens the connection.</caps:sentence>
            <caps:sentence sentenceid="be8bdaf920d17f18ffa44c84acf51ba4" id="tgt8" class="tgtSentence"> Of course, a real application would do more processing in the Form_Load event handler than is shown here.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">In order to handle ADO events in Microsoft® Visual Basic®, you must declare a module-level variable using the <legacyBold>WithEvents</legacyBold> keyword.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The variable can be declared only as part of a class module and must be declared at the module level.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This is not as restrictive as it seems, however, because Visual Basic <legacyBold>Form</legacyBold> objects are also classes.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The simplest way to handle ADO events is to declare a variable using <legacyBold>WithEvents</legacyBold>.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> The following example handles the <legacyBold>ConnectComplete</legacyBold> event for a <legacyBold>Connection</legacyBold> object:</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>' BeginEventExampleVB02
Dim WithEvents connEvent As Connection
Attribute connEvent.VB_VarHelpID = -1

Private Sub Form_Load()
Dim strConn As String

   ' Create a new object with event
   ' handling enabled.
   strConn = "Provider=sqloledb;" &amp; _
      "Data Source=MyServer;" &amp; _
      "Initial Catalog=Northwind;" &amp; _
      "Integrated Security=SSPI;"
   Set connEvent = New ADODB.Connection
   connEvent.Open strConn
End Sub

Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _
    adStatus As ADODB.EventStatusEnum, _
    ByVal pConnection As ADODB.Connection)
Dim strMsg As String

   If adStatus = adStatusErrorsOccurred Then
      Select Case pError.Number
         Case adErrOperationCancelled
            ' The operation was cancelled in the
            ' Will event. Notify the user and exit.
            strMsg = "I'm sorry you can't connect right now." &amp; vbCrLf
            strMsg = strMsg &amp; "Click OK to exit."
            Unload Me
         Case Else
            strMsg = "Error " &amp; Format(pError.Number) &amp; vbCrLf
            strMsg = strMsg &amp; pError.Description
            strMsg = strMsg &amp; "Click OK to exit."
            Unload Me
      End Select
   End If
   frmWait.btnOK.Enabled = True
End Sub
' EndEventExampleVB02</code>
          <para>
            <caps:sentence id="src6" class="srcSentence">The <legacyBold>Connection</legacyBold> object is declared at the <legacyBold>Form</legacyBold> level using the <legacyBold>WithEvents</legacyBold> keyword to enable event handling.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The Form_Load event handler actually creates the object by assigning a new <legacyBold>Connection</legacyBold> object to <legacyItalic>connEvent</legacyItalic> and then opens the connection.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Of course, a real application would do more processing in the Form_Load event handler than is shown here.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
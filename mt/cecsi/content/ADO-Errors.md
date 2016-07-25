---
title: "ADO Errors"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9bb84114-a1df-4122-a1b8-ad98dcd85cc3
caps.latest.revision: 7
caps.handback.revision: 7
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
# ADO Errors
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3981e005bf20fbd74aa1a619f16ac204" id="tgt1" class="tgtSentence">ADO errors are reported to your program as run-time errors.</caps:sentence>
          <caps:sentence sentenceid="013cab50390c28a1227430bfb5aa579b" id="tgt2" class="tgtSentence"> You can use the error-trapping mechanism of your programming language to trap and handle them.</caps:sentence>
          <caps:sentence sentenceid="ca24368357a03712d1740687a5717f6a" id="tgt3" class="tgtSentence"> For example, in Visual Basic, use the <legacyBold>On Error</legacyBold> statement.</caps:sentence>
          <caps:sentence sentenceid="d10d7d769c62a709e0f98239949c3edb" id="tgt4" class="tgtSentence"> In Visual J++, use a <legacyBold>try-catch</legacyBold> block.</caps:sentence>
          <caps:sentence sentenceid="1d74fde29bd75bb90a75798f6d6b947b" id="tgt5" class="tgtSentence"> In Visual C++, it depends on the method you are using to access the ADO libraries.</caps:sentence>
          <caps:sentence sentenceid="114e354958b780a06a1efb786b8615ed" id="tgt6" class="tgtSentence"> With #import, use a <legacyBold>try-catch</legacyBold> block.</caps:sentence>
          <caps:sentence sentenceid="2b884c74755ceeeca107ceca8a11bde1" id="tgt7" class="tgtSentence"> Otherwise, C++ programmers need to explicitly retrieve the error object by calling <legacyBold>GetErrorInfo</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="df8ba8f8d557adab3c53da55a1bf269e" id="tgt8" class="tgtSentence"> The following Visual Basic sub procedure demonstrates trapping an ADO error:</caps:sentence>
        </para>
        <code>' BeginErrorHandlingVB01
Private Sub Form_Load()
' Turn on error handling
On Error GoTo FormLoadError

'Open the database and the recordset for processing.
'
Dim strCnn As String
strCnn = "Provider=sqloledb;" &amp; _
    "Data Source=a-iresmi2000;" &amp; _
    "Initial Catalog=Northwind;Integrated Security=SSPI"

' cnn is a Public Connection Object because
' it was defined WithEvents
Set cnn = New ADODB.Connection
cnn.Open strCnn

' The next line of code intentionally causes
' an error by trying to open a connection
' that has already been opened.
cnn.Open strCnn

' rst is a Public Recordset because it
' was defined WithEvents
Set rst = New ADODB.Recordset
rst.Open "Customers", cnn

Exit Sub

' Error handler
FormLoadError:
    Dim strErr As String
    Select Case Err
        Case adErrObjectOpen
            strErr = "Error #" &amp; Err.Number &amp; ": " &amp; Err.Description &amp; vbCrLf
            strErr = strErr &amp; "Error reported by: " &amp; Err.Source &amp; vbCrLf
            strErr = strErr &amp; "Help File: " &amp; Err.HelpFile &amp; vbCrLf
            strErr = strErr &amp; "Topic ID: " &amp; Err.HelpContext
            MsgBox strErr
            Debug.Print strErr
            Err.Clear
            Resume Next
        ' If some other error occurs that
        ' has nothing to do with ADO, show
        ' the number and description and exit.
        Case Else
            strErr = "Error #" &amp; Err.Number &amp; ": " &amp; Err.Description &amp; vbCrLf
            MsgBox strErr
            Debug.Print strErr
            Unload Me
    End Select
End Sub
' EndErrorHandlingVB01</code>
        <para>
          <caps:sentence sentenceid="892ae7032fcf1e28bfbc8d3d9b635aff" id="tgt9" class="tgtSentence">This <legacyBold>Form_Load</legacyBold> event procedure intentionally creates an error by trying to open the same <legacyBold>Connection</legacyBold> object twice.</caps:sentence>
          <caps:sentence sentenceid="2e134f27da83eeaf9cb561ae7a7a1ff8" id="tgt10" class="tgtSentence"> The second time the <legacyBold>Open</legacyBold> method is called, the error handler is activated.</caps:sentence>
          <caps:sentence sentenceid="b172c09e4582170ee246d77d49f399d5" id="tgt11" class="tgtSentence"> In this case the error is of type <legacyBold>adErrObjectOpen</legacyBold>, so the error handler displays the following message before resuming program execution:</caps:sentence>
        </para>
        <code>Error #3705: Operation is not allowed when the object is open.
Error reported by: ADODB.Connection
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705</code>
        <para>
          <caps:sentence sentenceid="36df912152705d10f9e0b11431d6c833" id="tgt12" class="tgtSentence">The error message includes each piece of information provided by the Visual Basic <legacyBold>Err</legacyBold> object except for the <legacyBold>LastDLLError</legacyBold> value, which does not apply here.</caps:sentence>
          <caps:sentence sentenceid="a6e23f09b9baf134d7f7d37808458fec" id="tgt13" class="tgtSentence"> The error number tells you which error has occurred.</caps:sentence>
          <caps:sentence sentenceid="4381f78715839f37ce1daad5c70f3873" id="tgt14" class="tgtSentence"> The description is useful in cases in which you do not want to handle the error yourself.</caps:sentence>
          <caps:sentence sentenceid="c182138a80d7bf46440ac2dbe060fa3c" id="tgt15" class="tgtSentence"> You can simply pass it along to the user.</caps:sentence>
          <caps:sentence sentenceid="af254952458f62c87c07b1507aea63d5" id="tgt16" class="tgtSentence"> Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong.</caps:sentence>
          <caps:sentence sentenceid="29ef02a716d66272a38e801be1e6ce5c" id="tgt17" class="tgtSentence"> In the sample code, the error was reported by the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="bcf0597c8617bd1f1d2e145b7f06ef68" id="tgt18" class="tgtSentence"> You will see the object's type or programmatic ID here — not a variable name.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="0f621a8282aba59dc138cf705ff6c67f" id="tgt19" class="tgtSentence">The Visual Basic <legacyBold>Err</legacyBold> object only contains information about the most recent error.</caps:sentence>
            <caps:sentence sentenceid="784bf72319e641ffe5fb110291e0aaff" id="tgt20" class="tgtSentence"> The ADO <legacyBold>Errors</legacyBold> collection of the <legacyBold>Connection </legacyBold>object contains one <legacyBold>Error</legacyBold> object for each error raised by the most recent ADO operation.</caps:sentence>
            <caps:sentence sentenceid="f6c14f1b394dcbd6813716ba525ee219" id="tgt21" class="tgtSentence"> Use the <legacyBold>Errors</legacyBold> collection rather than the <legacyBold>Err </legacyBold>object to handle multiple errors.</caps:sentence>
            <caps:sentence sentenceid="7edf51dc734275450144eb0b3f15ba08" id="tgt22" class="tgtSentence"> For more information about the <legacyBold>Errors</legacyBold> collection, see <legacyLink xlink:href="cc7d6ff9-2034-45c6-9d61-90b177010054">Provider Errors</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="6e697a7ddfb32f1982f45f1146b78e49" id="tgt23" class="tgtSentence"> However, if there is no valid <legacyBold>Connection</legacyBold> object, the <legacyBold>Err</legacyBold> object is the only source for information about ADO errors.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="9cf8b860873c2ac40e78fb566b5e5fa8" id="tgt24" class="tgtSentence">What kinds of operations are likely to cause ADO errors?</caps:sentence>
          <caps:sentence sentenceid="6ee51bb9a5e5c2f06954fd7fd5f0839c" id="tgt25" class="tgtSentence"> Common ADO errors can involve opening an object such as a <legacyBold>Connection</legacyBold> or <legacyBold>Recordset</legacyBold>, attempting to update data, or calling a method or property that is not supported by your provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="b804359e15c1732067c5947a003001b4" id="tgt26" class="tgtSentence">OLE DB errors can also be passed to your application as run-time errors in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fde3d67872e53c5a8bfa353ac92b4436" id="tgt27" class="tgtSentence">The following topic provides more information about ADO errors.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="edcd22a15ca9389630a9270802667647" id="tgt28" class="tgtSentence">
                <legacyLink xlink:href="f653393e-d4b0-4c34-ad5f-2bdf56bc1305">ADO Error Reference</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO errors are reported to your program as run-time errors.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can use the error-trapping mechanism of your programming language to trap and handle them.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For example, in Visual Basic, use the <legacyBold>On Error</legacyBold> statement.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> In Visual J++, use a <legacyBold>try-catch</legacyBold> block.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> In Visual C++, it depends on the method you are using to access the ADO libraries.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> With #import, use a <legacyBold>try-catch</legacyBold> block.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Otherwise, C++ programmers need to explicitly retrieve the error object by calling <legacyBold>GetErrorInfo</legacyBold>.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The following Visual Basic sub procedure demonstrates trapping an ADO error:</caps:sentence>
        </para>
        <code>' BeginErrorHandlingVB01
Private Sub Form_Load()
' Turn on error handling
On Error GoTo FormLoadError

'Open the database and the recordset for processing.
'
Dim strCnn As String
strCnn = "Provider=sqloledb;" &amp; _
    "Data Source=a-iresmi2000;" &amp; _
    "Initial Catalog=Northwind;Integrated Security=SSPI"

' cnn is a Public Connection Object because
' it was defined WithEvents
Set cnn = New ADODB.Connection
cnn.Open strCnn

' The next line of code intentionally causes
' an error by trying to open a connection
' that has already been opened.
cnn.Open strCnn

' rst is a Public Recordset because it
' was defined WithEvents
Set rst = New ADODB.Recordset
rst.Open "Customers", cnn

Exit Sub

' Error handler
FormLoadError:
    Dim strErr As String
    Select Case Err
        Case adErrObjectOpen
            strErr = "Error #" &amp; Err.Number &amp; ": " &amp; Err.Description &amp; vbCrLf
            strErr = strErr &amp; "Error reported by: " &amp; Err.Source &amp; vbCrLf
            strErr = strErr &amp; "Help File: " &amp; Err.HelpFile &amp; vbCrLf
            strErr = strErr &amp; "Topic ID: " &amp; Err.HelpContext
            MsgBox strErr
            Debug.Print strErr
            Err.Clear
            Resume Next
        ' If some other error occurs that
        ' has nothing to do with ADO, show
        ' the number and description and exit.
        Case Else
            strErr = "Error #" &amp; Err.Number &amp; ": " &amp; Err.Description &amp; vbCrLf
            MsgBox strErr
            Debug.Print strErr
            Unload Me
    End Select
End Sub
' EndErrorHandlingVB01</code>
        <para>
          <caps:sentence id="src9" class="srcSentence">This <legacyBold>Form_Load</legacyBold> event procedure intentionally creates an error by trying to open the same <legacyBold>Connection</legacyBold> object twice.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> The second time the <legacyBold>Open</legacyBold> method is called, the error handler is activated.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> In this case the error is of type <legacyBold>adErrObjectOpen</legacyBold>, so the error handler displays the following message before resuming program execution:</caps:sentence>
        </para>
        <code>Error #3705: Operation is not allowed when the object is open.
Error reported by: ADODB.Connection
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705</code>
        <para>
          <caps:sentence id="src12" class="srcSentence">The error message includes each piece of information provided by the Visual Basic <legacyBold>Err</legacyBold> object except for the <legacyBold>LastDLLError</legacyBold> value, which does not apply here.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> The error number tells you which error has occurred.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> The description is useful in cases in which you do not want to handle the error yourself.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> You can simply pass it along to the user.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong.</caps:sentence>
          <caps:sentence id="src17" class="srcSentence"> In the sample code, the error was reported by the <legacyBold>Connection</legacyBold> object.</caps:sentence>
          <caps:sentence id="src18" class="srcSentence"> You will see the object's type or programmatic ID here — not a variable name.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src19" class="srcSentence">The Visual Basic <legacyBold>Err</legacyBold> object only contains information about the most recent error.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> The ADO <legacyBold>Errors</legacyBold> collection of the <legacyBold>Connection </legacyBold>object contains one <legacyBold>Error</legacyBold> object for each error raised by the most recent ADO operation.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> Use the <legacyBold>Errors</legacyBold> collection rather than the <legacyBold>Err </legacyBold>object to handle multiple errors.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> For more information about the <legacyBold>Errors</legacyBold> collection, see <legacyLink xlink:href="cc7d6ff9-2034-45c6-9d61-90b177010054">Provider Errors</legacyLink>.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> However, if there is no valid <legacyBold>Connection</legacyBold> object, the <legacyBold>Err</legacyBold> object is the only source for information about ADO errors.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src24" class="srcSentence">What kinds of operations are likely to cause ADO errors?</caps:sentence>
          <caps:sentence id="src25" class="srcSentence"> Common ADO errors can involve opening an object such as a <legacyBold>Connection</legacyBold> or <legacyBold>Recordset</legacyBold>, attempting to update data, or calling a method or property that is not supported by your provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src26" class="srcSentence">OLE DB errors can also be passed to your application as run-time errors in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src27" class="srcSentence">The following topic provides more information about ADO errors.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src28" class="srcSentence">
                <legacyLink xlink:href="f653393e-d4b0-4c34-ad5f-2bdf56bc1305">ADO Error Reference</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
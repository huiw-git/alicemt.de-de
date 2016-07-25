---
title: "Provider Errors"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cc7d6ff9-2034-45c6-9d61-90b177010054
caps.latest.revision: 4
caps.handback.revision: 4
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
# Provider Errors
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="dc04b44cfd6177dfccb9651c55f149d8" id="tgt1" class="tgtSentence">When a provider error occurs, a run-time error of -2147467259 is returned.</caps:sentence>
          <caps:sentence sentenceid="543ffe0a5e2fea17bea78428f1cdb0f8" id="tgt2" class="tgtSentence"> When you receive this error, check the <legacyBold>Errors</legacyBold> collection of the active <legacyBold>Connection</legacyBold> object, which will contain one or more errors describing what occurred.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="e9fbdbfebbe5c421041aca8cce185e3e" id="tgt3" class="tgtSentence">The ADO Errors Collection</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="90610e66ce44a711804ed9d9a187ce87" id="tgt4" class="tgtSentence">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="db551487d9cf58eadaeba518ec60fb2f" id="tgt5" class="tgtSentence"> This collection contains no objects if an operation concludes successfully and contains one or more <legacyBold>Error</legacyBold> objects if something went wrong and the provider raised one or more errors.</caps:sentence>
            <caps:sentence sentenceid="09c48dcffcf92fb7b891e746991cd671" id="tgt6" class="tgtSentence"> Examine each error object to determine the exact cause of the error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="54598b27a5f0b9e9cf2d4bd6ea15426d" id="tgt7" class="tgtSentence">As soon as you have finished handling any errors that have occurred, you can clear the collection by calling the <legacyBold>Clear</legacyBold> method.</caps:sentence>
            <caps:sentence sentenceid="1d005cf6c5626c1b797d6b287def774c" id="tgt8" class="tgtSentence"> It is especially important to explicitly clear the <legacyBold>Errors</legacyBold> collection before you call the <legacyBold>Resync</legacyBold>, <legacyBold>UpdateBatch</legacyBold>, or <legacyBold>CancelBatch</legacyBold> method on a <legacyBold>Recordset</legacyBold> object, the <legacyBold>Open</legacyBold> method on a <legacyBold>Connection</legacyBold> object, or set the <legacyBold>Filter</legacyBold> property on a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="7fac62ac039a68e3596cca42471dfe3f" id="tgt9" class="tgtSentence"> By clearing the collection explicitly, you can be certain that any <legacyBold>Error</legacyBold> objects in the collection are not left over from a previous operation.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fcad604aaa52534d5e3a8688140342c1" id="tgt10" class="tgtSentence">Some operations can generate warnings in addition to errors.</caps:sentence>
            <caps:sentence sentenceid="d4f8ed2bfce0da0df24a4ecdf8459514" id="tgt11" class="tgtSentence"> Warnings are also represented by <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="15ed0e4d356ec8d75bd91c0568558ec4" id="tgt12" class="tgtSentence"> When a provider adds a warning to the collection, it does not generate a run-time error.</caps:sentence>
            <caps:sentence sentenceid="13cd39d3c135e7e639ffa0c9e29e722f" id="tgt13" class="tgtSentence"> Check the <legacyBold>Count</legacyBold> property of the <legacyBold>Errors</legacyBold> collection to determine whether a warning was produced by a particular operation.</caps:sentence>
            <caps:sentence sentenceid="030d08cbfa6f5b2c669835f289f6342d" id="tgt14" class="tgtSentence"> If the count is one or greater, an <legacyBold>Error</legacyBold> object has been added to the collection.</caps:sentence>
            <caps:sentence sentenceid="4816557b69dce56660edcc7713d5a69d" id="tgt15" class="tgtSentence"> As soon as you have determined that the <legacyBold>Errors</legacyBold> collection contains errors or warnings, you can iterate through the collection and retrieve information about each <legacyBold>Error</legacyBold> object that it contains.</caps:sentence>
            <caps:sentence sentenceid="451f85e3356622f225df0abcbb5e429d" id="tgt16" class="tgtSentence"> The following short Visual Basic example demonstrates this:</caps:sentence>
          </para>
          <code>' BeginErrorHandlingVB02
Private Function DeleteCustomer(ByVal CompanyName As String) As Long
    On Error GoTo DeleteCustomerError
    
    rst.Find "CompanyName='" &amp; CompanyName &amp; "'"
DeleteCustomerError:
Dim objError As ADODB.Error
Dim strError As String

    If cnn.Errors.Count &gt; 0 Then
        For Each objError In cnn.Errors
            strError = strError &amp; "Error #" &amp; objError.Number &amp; _
                " " &amp; objError.Description &amp; vbCrLf &amp; _
                "NativeError: " &amp; objError.NativeError &amp; vbCrLf &amp; _
                "SQLState: " &amp; objError.SQLState &amp; vbCrLf &amp; _
                "Reported by: " &amp; objError.Source &amp; vbCrLf &amp; _
                "Help file: " &amp; objError.HelpFile &amp; vbCrLf &amp; _
                "Help Context ID: " &amp; objError.HelpContext
        Next
        MsgBox strError
    End If
End Function
' EndErrorHandlingVB02</code>
          <para>
            <caps:sentence sentenceid="776cc05b55c06824c96c0f088cf5d73c" id="tgt17" class="tgtSentence">The error-handling routine includes a <legacyBold>For Each</legacyBold> loop that examines each object in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="57dfbfdc7c3021071c09eb57e14d4458" id="tgt18" class="tgtSentence"> In this example, it accumulates a message for display.</caps:sentence>
            <caps:sentence sentenceid="5a3801ecd4460dfad564778d6e0903bc" id="tgt19" class="tgtSentence"> In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly manner.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="dc1e835f93073bc4104041061f95f196" id="tgt20" class="tgtSentence">The Error Object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="92c02f5f8a58e6284e70e60c57b74a03" id="tgt21" class="tgtSentence">By examining an <legacyBold>Error</legacyBold> object you can determine what error occurred, and more important, what application or what object caused the error.</caps:sentence>
            <caps:sentence sentenceid="2ee3f0573a090cdf01223e55b103b07c" id="tgt22" class="tgtSentence"> The <legacyBold>Error</legacyBold> object has the following properties:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a3d69a40cc5ec31232a11100ae6c951" id="tgt23" class="tgtSentence">Property name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt24" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0a325a4b647152aa2f7199eddbd5cd23" id="tgt25" class="tgtSentence">               <legacyBold>Description</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="91512ef2509cf8e06ac1ce1e0ca91f22" id="tgt26" class="tgtSentence">A text description of the error that occurred.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="142cd5768b05ae3e3bb7b8c19a02c6e9" id="tgt27" class="tgtSentence">               <legacyBold>HelpContext, HelpFile</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90d4dcfd7376e483602e62ccec09bd6b" id="tgt28" class="tgtSentence">Refers to the Help topic and Help file that contain a description of the error that occurred.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f40091a35cf04d824208d8bddab317e" id="tgt29" class="tgtSentence">               <legacyBold>NativeError</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fc810341fb9f3b51603e2a9322a8a27b" id="tgt30" class="tgtSentence">The provider-specific error number.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18f509bb6276508293185ccd5f68eb96" id="tgt31" class="tgtSentence">               <legacyBold>Number</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cd04f3f0174ae680f92a7b87fd744a8b" id="tgt32" class="tgtSentence">A Long Integer that represents the number (listed in the <legacyBold>ErrorValueEnum</legacyBold>) of the error that occurred.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c3a6f6c76a78d9586a3f68e240bffca" id="tgt33" class="tgtSentence">               <legacyBold>Source</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="93b0a74276c2f2b065d4304cc523623c" id="tgt34" class="tgtSentence">Indicates the name of the object or application that generated an error.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0fe4be8cf94a655ad0b98e3033e49d13" id="tgt35" class="tgtSentence">               <legacyBold>SQLState</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="40aaf8d43620952f9000d4759d627226" id="tgt36" class="tgtSentence">A five-character error code that the provider returns during the process of an SQL statement.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="6f416b928b0a70e98f691aee2ae98cde" id="tgt37" class="tgtSentence">The ADO <legacyBold>Error</legacyBold> object is very similar to the standard Visual Basic <legacyBold>Err</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="e0f0e631f7a78f0613c6351f5f098e80" id="tgt38" class="tgtSentence"> Its properties describe the error that occurred.</caps:sentence>
            <caps:sentence sentenceid="838f8dcc8c7e35b7b8d245a048a7ff5b" id="tgt39" class="tgtSentence"> In addition to the number of the error, you also receive two related pieces of information.</caps:sentence>
            <caps:sentence sentenceid="5be1bb9c1d186c1fc1d896da3af15eb3" id="tgt40" class="tgtSentence"> The <legacyBold>NativeError</legacyBold> property contains an error number specific to the provider you are using.</caps:sentence>
            <caps:sentence sentenceid="3bad1ddc494534b60af1b616ea03f08c" id="tgt41" class="tgtSentence"> In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so <legacyBold>NativeError</legacyBold> will contain errors specific to SQL Server.</caps:sentence>
            <caps:sentence sentenceid="a4bf33c97835c641a20fe6b0c3b9f66e" id="tgt42" class="tgtSentence"> The <legacyBold>SQLState</legacyBold> property has a five-letter code that describes an error in an SQL statement.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="178ca13e8f8813dcd73746aa98159b76" id="tgt43" class="tgtSentence">Event-Related Errors</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f0712b6d80254a4207ba9e30d9ae946c" id="tgt44" class="tgtSentence">The <legacyBold>Error</legacyBold> object is also used when event-related errors occur.</caps:sentence>
            <caps:sentence sentenceid="8634c92c3d182dea0cdbbb6a643fec37" id="tgt45" class="tgtSentence"> You can determine whether an error occurred in the process that raised an ADO event by checking the <legacyBold>Error</legacyBold> object passed as an event parameter.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b9d92157f1bbe197526095cea318563f" id="tgt46" class="tgtSentence">If the operation that causes an event is concluded successfully, the <legacyItalic>adStatus</legacyItalic> parameter of the event handler will be set to <legacyItalic>adStatusOK</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="7dca6aba2165ef8ebf525096ada27895" id="tgt47" class="tgtSentence"> On the other hand, if the operation that raised the event was unsuccessful, the <legacyItalic>adStatus</legacyItalic> parameter is set to <legacyItalic>adStatusErrorsOccurred</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="4475d93d5aaddbb42f3e1cf26d383541" id="tgt48" class="tgtSentence"> In that case, the <legacyItalic>pError</legacyItalic> parameter will contain an <legacyBold>Error</legacyBold> object that describes the error.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">When a provider error occurs, a run-time error of -2147467259 is returned.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When you receive this error, check the <legacyBold>Errors</legacyBold> collection of the active <legacyBold>Connection</legacyBold> object, which will contain one or more errors describing what occurred.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">The ADO Errors Collection</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the <legacyBold>Connection</legacyBold> object.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> This collection contains no objects if an operation concludes successfully and contains one or more <legacyBold>Error</legacyBold> objects if something went wrong and the provider raised one or more errors.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Examine each error object to determine the exact cause of the error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">As soon as you have finished handling any errors that have occurred, you can clear the collection by calling the <legacyBold>Clear</legacyBold> method.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> It is especially important to explicitly clear the <legacyBold>Errors</legacyBold> collection before you call the <legacyBold>Resync</legacyBold>, <legacyBold>UpdateBatch</legacyBold>, or <legacyBold>CancelBatch</legacyBold> method on a <legacyBold>Recordset</legacyBold> object, the <legacyBold>Open</legacyBold> method on a <legacyBold>Connection</legacyBold> object, or set the <legacyBold>Filter</legacyBold> property on a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> By clearing the collection explicitly, you can be certain that any <legacyBold>Error</legacyBold> objects in the collection are not left over from a previous operation.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">Some operations can generate warnings in addition to errors.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Warnings are also represented by <legacyBold>Error</legacyBold> objects in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> When a provider adds a warning to the collection, it does not generate a run-time error.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Check the <legacyBold>Count</legacyBold> property of the <legacyBold>Errors</legacyBold> collection to determine whether a warning was produced by a particular operation.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> If the count is one or greater, an <legacyBold>Error</legacyBold> object has been added to the collection.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> As soon as you have determined that the <legacyBold>Errors</legacyBold> collection contains errors or warnings, you can iterate through the collection and retrieve information about each <legacyBold>Error</legacyBold> object that it contains.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> The following short Visual Basic example demonstrates this:</caps:sentence>
          </para>
          <code>' BeginErrorHandlingVB02
Private Function DeleteCustomer(ByVal CompanyName As String) As Long
    On Error GoTo DeleteCustomerError
    
    rst.Find "CompanyName='" &amp; CompanyName &amp; "'"
DeleteCustomerError:
Dim objError As ADODB.Error
Dim strError As String

    If cnn.Errors.Count &gt; 0 Then
        For Each objError In cnn.Errors
            strError = strError &amp; "Error #" &amp; objError.Number &amp; _
                " " &amp; objError.Description &amp; vbCrLf &amp; _
                "NativeError: " &amp; objError.NativeError &amp; vbCrLf &amp; _
                "SQLState: " &amp; objError.SQLState &amp; vbCrLf &amp; _
                "Reported by: " &amp; objError.Source &amp; vbCrLf &amp; _
                "Help file: " &amp; objError.HelpFile &amp; vbCrLf &amp; _
                "Help Context ID: " &amp; objError.HelpContext
        Next
        MsgBox strError
    End If
End Function
' EndErrorHandlingVB02</code>
          <para>
            <caps:sentence id="src17" class="srcSentence">The error-handling routine includes a <legacyBold>For Each</legacyBold> loop that examines each object in the <legacyBold>Errors</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> In this example, it accumulates a message for display.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly manner.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">The Error Object</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">By examining an <legacyBold>Error</legacyBold> object you can determine what error occurred, and more important, what application or what object caused the error.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> The <legacyBold>Error</legacyBold> object has the following properties:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Property name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">               <legacyBold>Description</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">A text description of the error that occurred.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">               <legacyBold>HelpContext, HelpFile</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Refers to the Help topic and Help file that contain a description of the error that occurred.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">               <legacyBold>NativeError</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">The provider-specific error number.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">               <legacyBold>Number</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">A Long Integer that represents the number (listed in the <legacyBold>ErrorValueEnum</legacyBold>) of the error that occurred.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">               <legacyBold>Source</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Indicates the name of the object or application that generated an error.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">               <legacyBold>SQLState</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">A five-character error code that the provider returns during the process of an SQL statement.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src37" class="srcSentence">The ADO <legacyBold>Error</legacyBold> object is very similar to the standard Visual Basic <legacyBold>Err</legacyBold> object.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> Its properties describe the error that occurred.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> In addition to the number of the error, you also receive two related pieces of information.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> The <legacyBold>NativeError</legacyBold> property contains an error number specific to the provider you are using.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so <legacyBold>NativeError</legacyBold> will contain errors specific to SQL Server.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> The <legacyBold>SQLState</legacyBold> property has a five-letter code that describes an error in an SQL statement.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src43" class="srcSentence">Event-Related Errors</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src44" class="srcSentence">The <legacyBold>Error</legacyBold> object is also used when event-related errors occur.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> You can determine whether an error occurred in the process that raised an ADO event by checking the <legacyBold>Error</legacyBold> object passed as an event parameter.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src46" class="srcSentence">If the operation that causes an event is concluded successfully, the <legacyItalic>adStatus</legacyItalic> parameter of the event handler will be set to <legacyItalic>adStatusOK</legacyItalic>.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> On the other hand, if the operation that raised the event was unsuccessful, the <legacyItalic>adStatus</legacyItalic> parameter is set to <legacyItalic>adStatusErrorsOccurred</legacyItalic>.</caps:sentence>
            <caps:sentence id="src48" class="srcSentence"> In that case, the <legacyItalic>pError</legacyItalic> parameter will contain an <legacyBold>Error</legacyBold> object that describes the error.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
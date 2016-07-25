---
title: "Delete Method Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 78935d6d-1c1a-4306-a83a-1763210c69f9
caps.latest.revision: 11
caps.handback.revision: 11
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
# Delete Method Example (VBScript)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c64d14bd4879cc4de57a1ee0e0764f78" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink> method to remove a specified record from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="632368375da61dbecc72fc82386f66b3" id="tgt2" class="tgtSentence">Use the following example in an Active Server Page (ASP).</caps:sentence>
          <caps:sentence sentenceid="1d199c67f06a4a4dee8575a4ac2cc61a" id="tgt3" class="tgtSentence"> To view this fully functional example, you must either have the data source AdvWorks.mdb (installed with the SDK) located at C:\Program Files\Microsoft Platform SDK\Samples\DataAccess\Rds\RDSTest\advworks.mdb or edit the path in the example code to reflect the actual location of this file.</caps:sentence>
          <caps:sentence sentenceid="232d857b786c203e8e1bd7fab0aeaf14" id="tgt4" class="tgtSentence"> This is a Microsoft Access database file.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e4feba9e18b9fbe62851f0fed87383be" id="tgt5" class="tgtSentence">Use <legacyBold>Find</legacyBold> to locate the file Adovbs.inc and place it in the directory you plan to use.</caps:sentence>
          <caps:sentence sentenceid="58ff04839e7526b1c36aaffb2b83f953" id="tgt6" class="tgtSentence"> Cut and paste the following code into Notepad or another text editor, and save it as <legacyBold>DeleteVBS.asp</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="2ec2928247650e1340e8f032c91c1be4" id="tgt7" class="tgtSentence"> You can view the result in any client browser.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="85b1b4c599399993f938cfdda2d23dc6" id="tgt8" class="tgtSentence">To exercise the example, try using the <legacyLink xlink:href="dcdcaf0a-b9b0-4d81-8728-43c38c4c853b">AddNew</legacyLink> example first to add some records.</caps:sentence>
          <caps:sentence sentenceid="529dec629a0faea0a4742d11ec21e149" id="tgt9" class="tgtSentence"> Then you can try to delete them.</caps:sentence>
          <caps:sentence sentenceid="b7c89b36ff503a5e3f6ce1c5d762c3dc" id="tgt10" class="tgtSentence"> View the result in any client browser.</caps:sentence>
        </para>
        <code>&lt;!-- BeginDeleteVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;% ' use this meta tag instead of ADOVBS.inc%&gt;
&lt;!-- METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4"  --&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;ADO Delete Method&lt;/TITLE&gt;
&lt;/HEAD&gt;
&lt;STYLE&gt;
&lt;!--
TH {
   background-color: #008080; 
   font-family: 'Arial Narrow','Arial',sans-serif; 
   font-size: xx-small;
   color: white;
   }
TD { 
   text-align: center;
   background-color: #f7efde;
   font-family: 'Arial Narrow','Arial',sans-serif; 
   font-size: xx-small;
    }
--&gt;
&lt;/STYLE&gt;

&lt;BODY&gt; 
&lt;H3&gt;ADO Delete Method&lt;/H3&gt;

&lt;%
    ' to integrate this code replace the DataSource value in the connection string

    ' connection and recordset variables
   Dim Cnxn, strCnxn
   Dim rsCustomers, strSQLCustomers

    ' create and open connection
   Set Cnxn = Server.CreateObject("ADODB.Connection") 
   strCnxn="Provider='sqloledb';Data Source=" &amp; _
            Request.ServerVariables("SERVER_NAME") &amp; ";" &amp; _
            "Integrated Security='SSPI';Initial Catalog='Northwind';"
   Cnxn.Open  strCnxn
    ' create and open recordset
   Set rsCustomers = Server.CreateObject("ADODB.Recordset")
   strSQLCustomers = "Customers"
   rsCustomers.Open strSQLCustomers, Cnxn, adOpenKeyset, adLockOptimistic, adCmdTable
   
   ' Move to designated record and delete it
   If Not IsEmpty(Request.Form("WhichRecord")) Then
      'Get value to move from Form Post method
      Moves = Request.Form("WhichRecord")

      rsCustomers.Move CInt(Moves)
      If Not rsCustomers.EOF or rsCustomers.BOF Then
          ' handle any db errors
         On Error Resume Next
         rsCustomers.Delete 1
         If Cnxn.Errors.Count &lt;&gt; 0 Then
            Response.Write "Cannot delete since there are related records in other tables."
            Response.End
         End If
         rsCustomers.MoveFirst
         On Error GoTo 0
      Else
         Response.Write "Not a Valid Record Number"
         rsCustomers.MoveFirst
      End If
   End If
%&gt;

&lt;!-- BEGIN column header row for Customer Table--&gt;
&lt;TABLE COLSPAN=8 CELLPADDING=5 BORDER=0&gt;
&lt;TR&gt;
   &lt;TH&gt;Rec. #&lt;/TH&gt;
   &lt;TH&gt;Company Name&lt;/TH&gt;
   &lt;TH&gt;Contact Name&lt;/TH&gt;
   &lt;TH&gt;City&lt;/TH&gt;
&lt;/TR&gt;

   &lt;% 
   ' Display ADO Data from Customer Table 
   ' Loop through Recordset adding one row to HTML Table each pass
   Dim iCount
   iCount = 0
   Do Until rsCustomers.EOF %&gt;
   &lt;TR&gt;
     &lt;TD&gt; &lt;%= CStr(iCount) %&gt;
     &lt;TD&gt; &lt;%= rsCustomers("CompanyName")%&gt; &lt;/TD&gt;
     &lt;TD&gt; &lt;%= rsCustomers("ContactName")%&gt; &lt;/TD&gt;
     &lt;TD&gt; &lt;%= rsCustomers("City")%&gt; &lt;/TD&gt;
   &lt;/TR&gt;
   &lt;% 
     iCount = iCount + 1
     rsCustomers.MoveNext 
   Loop 
   %&gt;
&lt;/TABLE&gt;

&lt;!-- Do Client side Input Data Validation Move to named record and Delete it --&gt;
&lt;Center&gt;
&lt;H4&gt;Clicking Button Will Remove Designated Record&lt;/H4&gt;
&lt;H5&gt;There are &lt;%=rsCustomers.RecordCount%&gt; Records in this Set&lt;/H5&gt;

&lt;Form Method=Post Action="Deletevbs.asp" Name=Form&gt;
   &lt;Input Type=Text Name="WhichRecord" Size=3&gt; 
   &lt;Input Type=Button Name=cmdDelete Value="Delete Record"&gt;
&lt;/Form&gt;

&lt;/BODY&gt;

&lt;Script Language = "VBScript"&gt;
Sub cmdDelete_OnClick
   If IsNumeric(Document.Form.WhichRecord.Value) Then
      Document.Form.WhichRecord.Value = CInt(Document.Form.WhichRecord.Value)
      Dim Response
      Response = MsgBox("Are You Sure About Deleting This Record?", vbYesNo,  "ADO-ASP Example")

      If Response = vbYes Then
         Document.Form.Submit
      End If
   Else
      MsgBox "You Must Enter a Valid Record Number",,"ADO-ASP Example"
   End If
End Sub
&lt;/Script&gt;

&lt;%
    ' clean up
    If rsCustomers.State = adStateOpen then
        rsCustomers.Close
    End If
    If Cnxn.State = adStateOpen then
        Cnxn.Close
    End If
%&gt;
&lt;/HTML&gt;
&lt;!-- EndDeleteVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete</legacyLink> method to remove a specified record from a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Use the following example in an Active Server Page (ASP).</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> To view this fully functional example, you must either have the data source AdvWorks.mdb (installed with the SDK) located at C:\Program Files\Microsoft Platform SDK\Samples\DataAccess\Rds\RDSTest\advworks.mdb or edit the path in the example code to reflect the actual location of this file.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> This is a Microsoft Access database file.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">Use <legacyBold>Find</legacyBold> to locate the file Adovbs.inc and place it in the directory you plan to use.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Cut and paste the following code into Notepad or another text editor, and save it as <legacyBold>DeleteVBS.asp</legacyBold>.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> You can view the result in any client browser.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">To exercise the example, try using the <legacyLink xlink:href="dcdcaf0a-b9b0-4d81-8728-43c38c4c853b">AddNew</legacyLink> example first to add some records.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> Then you can try to delete them.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> View the result in any client browser.</caps:sentence>
        </para>
        <code>&lt;!-- BeginDeleteVBS --&gt;
&lt;%@ Language=VBScript %&gt;
&lt;% ' use this meta tag instead of ADOVBS.inc%&gt;
&lt;!-- METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4"  --&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;ADO Delete Method&lt;/TITLE&gt;
&lt;/HEAD&gt;
&lt;STYLE&gt;
&lt;!--
TH {
   background-color: #008080; 
   font-family: 'Arial Narrow','Arial',sans-serif; 
   font-size: xx-small;
   color: white;
   }
TD { 
   text-align: center;
   background-color: #f7efde;
   font-family: 'Arial Narrow','Arial',sans-serif; 
   font-size: xx-small;
    }
--&gt;
&lt;/STYLE&gt;

&lt;BODY&gt; 
&lt;H3&gt;ADO Delete Method&lt;/H3&gt;

&lt;%
    ' to integrate this code replace the DataSource value in the connection string

    ' connection and recordset variables
   Dim Cnxn, strCnxn
   Dim rsCustomers, strSQLCustomers

    ' create and open connection
   Set Cnxn = Server.CreateObject("ADODB.Connection") 
   strCnxn="Provider='sqloledb';Data Source=" &amp; _
            Request.ServerVariables("SERVER_NAME") &amp; ";" &amp; _
            "Integrated Security='SSPI';Initial Catalog='Northwind';"
   Cnxn.Open  strCnxn
    ' create and open recordset
   Set rsCustomers = Server.CreateObject("ADODB.Recordset")
   strSQLCustomers = "Customers"
   rsCustomers.Open strSQLCustomers, Cnxn, adOpenKeyset, adLockOptimistic, adCmdTable
   
   ' Move to designated record and delete it
   If Not IsEmpty(Request.Form("WhichRecord")) Then
      'Get value to move from Form Post method
      Moves = Request.Form("WhichRecord")

      rsCustomers.Move CInt(Moves)
      If Not rsCustomers.EOF or rsCustomers.BOF Then
          ' handle any db errors
         On Error Resume Next
         rsCustomers.Delete 1
         If Cnxn.Errors.Count &lt;&gt; 0 Then
            Response.Write "Cannot delete since there are related records in other tables."
            Response.End
         End If
         rsCustomers.MoveFirst
         On Error GoTo 0
      Else
         Response.Write "Not a Valid Record Number"
         rsCustomers.MoveFirst
      End If
   End If
%&gt;

&lt;!-- BEGIN column header row for Customer Table--&gt;
&lt;TABLE COLSPAN=8 CELLPADDING=5 BORDER=0&gt;
&lt;TR&gt;
   &lt;TH&gt;Rec. #&lt;/TH&gt;
   &lt;TH&gt;Company Name&lt;/TH&gt;
   &lt;TH&gt;Contact Name&lt;/TH&gt;
   &lt;TH&gt;City&lt;/TH&gt;
&lt;/TR&gt;

   &lt;% 
   ' Display ADO Data from Customer Table 
   ' Loop through Recordset adding one row to HTML Table each pass
   Dim iCount
   iCount = 0
   Do Until rsCustomers.EOF %&gt;
   &lt;TR&gt;
     &lt;TD&gt; &lt;%= CStr(iCount) %&gt;
     &lt;TD&gt; &lt;%= rsCustomers("CompanyName")%&gt; &lt;/TD&gt;
     &lt;TD&gt; &lt;%= rsCustomers("ContactName")%&gt; &lt;/TD&gt;
     &lt;TD&gt; &lt;%= rsCustomers("City")%&gt; &lt;/TD&gt;
   &lt;/TR&gt;
   &lt;% 
     iCount = iCount + 1
     rsCustomers.MoveNext 
   Loop 
   %&gt;
&lt;/TABLE&gt;

&lt;!-- Do Client side Input Data Validation Move to named record and Delete it --&gt;
&lt;Center&gt;
&lt;H4&gt;Clicking Button Will Remove Designated Record&lt;/H4&gt;
&lt;H5&gt;There are &lt;%=rsCustomers.RecordCount%&gt; Records in this Set&lt;/H5&gt;

&lt;Form Method=Post Action="Deletevbs.asp" Name=Form&gt;
   &lt;Input Type=Text Name="WhichRecord" Size=3&gt; 
   &lt;Input Type=Button Name=cmdDelete Value="Delete Record"&gt;
&lt;/Form&gt;

&lt;/BODY&gt;

&lt;Script Language = "VBScript"&gt;
Sub cmdDelete_OnClick
   If IsNumeric(Document.Form.WhichRecord.Value) Then
      Document.Form.WhichRecord.Value = CInt(Document.Form.WhichRecord.Value)
      Dim Response
      Response = MsgBox("Are You Sure About Deleting This Record?", vbYesNo,  "ADO-ASP Example")

      If Response = vbYes Then
         Document.Form.Submit
      End If
   Else
      MsgBox "You Must Enter a Valid Record Number",,"ADO-ASP Example"
   End If
End Sub
&lt;/Script&gt;

&lt;%
    ' clean up
    If rsCustomers.State = adStateOpen then
        rsCustomers.Close
    End If
    If Cnxn.State = adStateOpen then
        Cnxn.Close
    End If
%&gt;
&lt;/HTML&gt;
&lt;!-- EndDeleteVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
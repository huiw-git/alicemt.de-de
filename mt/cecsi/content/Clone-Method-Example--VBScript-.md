---
title: "Clone Method Example (VBScript)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 36b96e3d-8cb0-4b79-bd93-ea5e0eb5679f
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
# Clone Method Example (VBScript)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7ade7c7d9f3422660dfa01764396b6bb" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">Clone</legacyLink> method to create copies of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> and then lets the user position the record pointer of each copy independently.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="632368375da61dbecc72fc82386f66b3" id="tgt2" class="tgtSentence">Use the following example in an Active Server Page (ASP).</caps:sentence>
          <caps:sentence sentenceid="6a5566326d32990bfaf851274042b79b" id="tgt3" class="tgtSentence"> This example uses the <legacyBold>Northwind</legacyBold> database distributed with Microsoft Access.</caps:sentence>
          <caps:sentence sentenceid="fc97c9710cbe05e153dec742ed5b10d7" id="tgt4" class="tgtSentence"> Cut and paste the following code to Notepad or another text editor and save it as CloneVBS.asp.</caps:sentence>
          <caps:sentence sentenceid="2ec2928247650e1340e8f032c91c1be4" id="tgt5" class="tgtSentence"> You can view the result in any client browser.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5f04eb2c3446fb61bcf47690beb9b04c" id="tgt6" class="tgtSentence">To exercise the example, change the line <codeInline>RsCustomerList.Source = "Customers"</codeInline> to <codeInline>RsCustomerList.Source = "Products"</codeInline> to count a larger table.</caps:sentence>
        </para>
        <code>&lt;!-- BeginCloneVBS --&gt;
&lt;% Language = VBScript %&gt;
&lt;%' use this meta tag instead of adovbs.inc%&gt;
&lt;!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;ADO Clone Method&lt;/TITLE&gt;
&lt;/HEAD&gt;

&lt;BODY&gt;

&lt;H1 align="center"&gt;ADO Clone Method&lt;/H1&gt;
&lt;HR&gt;
&lt;% ' to integrate/test this code replace the 
   ' Data Source value in the Connection string%&gt;
&lt;% 
    ' connection and recordset variables
    Dim Cnxn, strCnxn
    Dim rsCustomers, strSQLCustomers
    Dim rsFirst, rsLast, rsCount
    Dim rsClone
    Dim CloneFirst, CloneLast, CloneCount

    ' open connection
    Set Cnxn = Server.CreateObject("ADODB.Connection")
    strCnxn = "Provider='sqloledb';Data Source=" &amp; _
            Request.ServerVariables("SERVER_NAME") &amp; ";" &amp; _
            "Integrated Security='SSPI';Initial Catalog='Northwind';"
    Cnxn.Open strCnxn
        
    ' create and open Recordset using object refs
    Set rsCustomers = Server.CreateObject("ADODB.Recordset")
    strSQLCustomers = "Customers"
    
    rsCustomers.ActiveConnection = Cnxn
    rsCustomers.CursorLocation = adUseClient
    rsCustomers.CursorType = adOpenKeyset
    rsCustomers.LockType = adLockOptimistic
    rsCustomers.Source = strSQLCustomers
    rsCustomers.Open

    rsCustomers.MoveFirst
    rsCount = rsCustomers.RecordCount
    rsFirst = rsCustomers("CompanyName")
    rsCustomers.MoveLast
    rsLast = rsCustomers("CompanyName")

    ' create clone
    Set rsClone = rsCustomers.Clone
    rsClone.MoveFirst
    CloneCount = rsClone.RecordCount
    CloneFirst = rsClone("CompanyName")
    rsClone.MoveLast
    CloneLast = rsClone("CompanyName")
%&gt;

&lt;!-- Display Results --&gt;
&lt;H3&gt;There Are &lt;%=rsCount%&gt; Records in the original recordset&lt;/H3&gt;
&lt;H3&gt;The first record is &lt;%=rsFirst%&gt; and the last record is &lt;%=rsLast%&gt;&lt;/H3&gt;
&lt;BR&gt;&lt;HR&gt;
&lt;H3&gt;There Are &lt;%=CloneCount%&gt; Records in the original recordset&lt;/H3&gt;
&lt;H3&gt;The first record is &lt;%=CloneFirst%&gt; and the last record is &lt;%=CloneLast%&gt;&lt;/H3&gt;
&lt;BR&gt;&lt;HR&gt;
&lt;H4&gt;Location of OLEDB Database&lt;/H4&gt;

&lt;%
    ' Show location of DSN data source
    Response.Write(Cnxn)

    ' Clean up
    If rsCustomers.State = adStateOpen then
       rsCustomers.Close
    End If
    If rsClone.State = adStateOpen then
       rsClone.Close
    End If
    If Cnxn.State = adStateOpen then
       Cnxn.Close
    End If
    Set rsCustomers = Nothing
    Set rsClone = Nothing
    Set Cnxn = Nothing
%&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndCloneVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">Clone Method</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">Clone</legacyLink> method to create copies of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> and then lets the user position the record pointer of each copy independently.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Use the following example in an Active Server Page (ASP).</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This example uses the <legacyBold>Northwind</legacyBold> database distributed with Microsoft Access.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Cut and paste the following code to Notepad or another text editor and save it as CloneVBS.asp.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> You can view the result in any client browser.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">To exercise the example, change the line <codeInline>RsCustomerList.Source = "Customers"</codeInline> to <codeInline>RsCustomerList.Source = "Products"</codeInline> to count a larger table.</caps:sentence>
        </para>
        <code>&lt;!-- BeginCloneVBS --&gt;
&lt;% Language = VBScript %&gt;
&lt;%' use this meta tag instead of adovbs.inc%&gt;
&lt;!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;ADO Clone Method&lt;/TITLE&gt;
&lt;/HEAD&gt;

&lt;BODY&gt;

&lt;H1 align="center"&gt;ADO Clone Method&lt;/H1&gt;
&lt;HR&gt;
&lt;% ' to integrate/test this code replace the 
   ' Data Source value in the Connection string%&gt;
&lt;% 
    ' connection and recordset variables
    Dim Cnxn, strCnxn
    Dim rsCustomers, strSQLCustomers
    Dim rsFirst, rsLast, rsCount
    Dim rsClone
    Dim CloneFirst, CloneLast, CloneCount

    ' open connection
    Set Cnxn = Server.CreateObject("ADODB.Connection")
    strCnxn = "Provider='sqloledb';Data Source=" &amp; _
            Request.ServerVariables("SERVER_NAME") &amp; ";" &amp; _
            "Integrated Security='SSPI';Initial Catalog='Northwind';"
    Cnxn.Open strCnxn
        
    ' create and open Recordset using object refs
    Set rsCustomers = Server.CreateObject("ADODB.Recordset")
    strSQLCustomers = "Customers"
    
    rsCustomers.ActiveConnection = Cnxn
    rsCustomers.CursorLocation = adUseClient
    rsCustomers.CursorType = adOpenKeyset
    rsCustomers.LockType = adLockOptimistic
    rsCustomers.Source = strSQLCustomers
    rsCustomers.Open

    rsCustomers.MoveFirst
    rsCount = rsCustomers.RecordCount
    rsFirst = rsCustomers("CompanyName")
    rsCustomers.MoveLast
    rsLast = rsCustomers("CompanyName")

    ' create clone
    Set rsClone = rsCustomers.Clone
    rsClone.MoveFirst
    CloneCount = rsClone.RecordCount
    CloneFirst = rsClone("CompanyName")
    rsClone.MoveLast
    CloneLast = rsClone("CompanyName")
%&gt;

&lt;!-- Display Results --&gt;
&lt;H3&gt;There Are &lt;%=rsCount%&gt; Records in the original recordset&lt;/H3&gt;
&lt;H3&gt;The first record is &lt;%=rsFirst%&gt; and the last record is &lt;%=rsLast%&gt;&lt;/H3&gt;
&lt;BR&gt;&lt;HR&gt;
&lt;H3&gt;There Are &lt;%=CloneCount%&gt; Records in the original recordset&lt;/H3&gt;
&lt;H3&gt;The first record is &lt;%=CloneFirst%&gt; and the last record is &lt;%=CloneLast%&gt;&lt;/H3&gt;
&lt;BR&gt;&lt;HR&gt;
&lt;H4&gt;Location of OLEDB Database&lt;/H4&gt;

&lt;%
    ' Show location of DSN data source
    Response.Write(Cnxn)

    ' Clean up
    If rsCustomers.State = adStateOpen then
       rsCustomers.Close
    End If
    If rsClone.State = adStateOpen then
       rsClone.Close
    End If
    If Cnxn.State = adStateOpen then
       Cnxn.Close
    End If
    Set rsCustomers = Nothing
    Set rsClone = Nothing
    Set Cnxn = Nothing
%&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndCloneVBS --&gt;</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">Clone Method</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
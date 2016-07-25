---
title: "Address Book Navigation Buttons"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f0dd84c6-5c33-4ab9-82b4-4c42dfdd2277
caps.latest.revision: 12
caps.handback.revision: 12
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
# Address Book Navigation Buttons
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b7f4116ea9abbb574d3d49013a2c060a" id="tgt1" class="tgtSentence">The Address Book application displays the navigation buttons at the bottom of the Web page.</caps:sentence>
          <caps:sentence sentenceid="18b40607197215631707e09b22f64298" id="tgt2" class="tgtSentence"> You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="0f4126468de5bdfa3736431ad22f5a4e" id="tgt7" class="tgtSentence">Navigation Sub Procedures</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a3862b8110ea0abee53c10a517664bdb" id="tgt8" class="tgtSentence">The Address Book application contains several procedures that allow users to click the <legacyBold>First</legacyBold>, <legacyBold>Next</legacyBold>, <legacyBold>Previous</legacyBold>, and <legacyBold>Last</legacyBold> buttons to move around the data.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0d7d12a1de602ba5ad027eea74945008" id="tgt9" class="tgtSentence">For example, clicking the <legacyBold>First</legacyBold> button activates the VBScript First_OnClick Sub procedure.</caps:sentence>
            <caps:sentence sentenceid="f48f64fe060908c4ec828bc4fb533b4c" id="tgt10" class="tgtSentence"> The procedure executes a <legacyLink xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst</legacyLink> method, which makes the first row of data the current selection.</caps:sentence>
            <caps:sentence sentenceid="531ae413ddbcff7706ada1c0b4bceec1" id="tgt11" class="tgtSentence"> Clicking the <legacyBold>Last</legacyBold> button activates the Last_OnClick Sub procedure, which invokes the <legacyLink xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveLast</legacyLink> method, making the last row of data the current selection.</caps:sentence>
            <caps:sentence sentenceid="e553b1ef0b06f7feb43945fc6964312f" id="tgt12" class="tgtSentence"> The remaining navigation buttons work in a similar fashion.</caps:sentence>
          </para>
          <code>' Move to the first record in the bound Recordset.
Sub First_OnClick
   DC1.Recordset.MoveFirst
End Sub

' Move to the next record from the current position 
' in the bound Recordset.
Sub Next_OnClick
   If Not DC1.Recordset.EOF Then    ' Cannot move beyond bottom record.
      DC1.Recordset.MoveNext
      Exit Sub
   End If   
End Sub

' Move to the previous record from the current position in the bound 
' Recordset.
Sub Prev_OnClick
   If Not DC1.Recordset.BOF Then    ' Cannot move beyond top record.
      DC1.Recordset.MovePrevious
      Exit Sub
   End If
End Sub

' Move to the last record in the bound Recordset.
Sub Last_OnClick
   DC1.Recordset.MoveLast
End Sub</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Address Book application displays the navigation buttons at the bottom of the Web page.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Navigation Sub Procedures</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">The Address Book application contains several procedures that allow users to click the <legacyBold>First</legacyBold>, <legacyBold>Next</legacyBold>, <legacyBold>Previous</legacyBold>, and <legacyBold>Last</legacyBold> buttons to move around the data.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">For example, clicking the <legacyBold>First</legacyBold> button activates the VBScript First_OnClick Sub procedure.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The procedure executes a <legacyLink xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst</legacyLink> method, which makes the first row of data the current selection.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Clicking the <legacyBold>Last</legacyBold> button activates the Last_OnClick Sub procedure, which invokes the <legacyLink xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveLast</legacyLink> method, making the last row of data the current selection.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The remaining navigation buttons work in a similar fashion.</caps:sentence>
          </para>
          <code>' Move to the first record in the bound Recordset.
Sub First_OnClick
   DC1.Recordset.MoveFirst
End Sub

' Move to the next record from the current position 
' in the bound Recordset.
Sub Next_OnClick
   If Not DC1.Recordset.EOF Then    ' Cannot move beyond bottom record.
      DC1.Recordset.MoveNext
      Exit Sub
   End If   
End Sub

' Move to the previous record from the current position in the bound 
' Recordset.
Sub Prev_OnClick
   If Not DC1.Recordset.BOF Then    ' Cannot move beyond top record.
      DC1.Recordset.MovePrevious
      Exit Sub
   End If
End Sub

' Move to the last record in the bound Recordset.
Sub Last_OnClick
   DC1.Recordset.MoveLast
End Sub</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
        <link xlink:href="45c80bb5-136f-4204-9df2-78740fa55574">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
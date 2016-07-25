---
title: "Required Client Settings"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833
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
# Required Client Settings
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt1" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt2" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt3" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt4" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="9e9126219d92cb84d640ea38f3bc55c2" id="tgt5" class="tgtSentence">Specify the following settings to use a custom <legacyBold>DataFactory</legacyBold> handler.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="870fdfab1e339df37d34e179ae3ee555" id="tgt6" class="tgtSentence">Specify "Provider=MS Remote" in the <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object_ADO</link> object <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property (ADO)</link> property or the <legacyBold>Connection</legacyBold> object connection string "<legacyBold>Provider</legacyBold>=" keyword.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="06baddec05b59b1979f527ef9ce211b0" id="tgt7" class="tgtSentence">Set the <link xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation Property (ADO)</link> property to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="602e48991b52c5b6f95dbe5780adc79e" id="tgt8" class="tgtSentence">Specify the name of the handler to use in the <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link> object's <legacyBold>Handler</legacyBold> property, or the <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link> object's connection string "<legacyBold>Handler</legacyBold>=" keyword.</caps:sentence>
              <caps:sentence sentenceid="0e1945ce0cd13684a2a12aae3ac69f5e" id="tgt9" class="tgtSentence"> (You cannot set the handler in the <legacyBold>Connection</legacyBold> object connect string.)</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="d96344908dae6d0f21a89bc9de374dff" id="tgt10" class="tgtSentence">RDS provides a default handler on the server named <legacyBold>MSDFMAP.Handler</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="3eec6441a7cb6336a4183d1055eb200e" id="tgt11" class="tgtSentence"> (The default customization file is named MSDFMAP.INI.)</caps:sentence>
        </para>
        <para>
          <legacyBold>
            <caps:sentence sentenceid="1a79a4d60de6718e8e5b326e338ae533" id="tgt12" class="tgtSentence">Example</caps:sentence>
          </legacyBold>
        </para>
        <para>
          <caps:sentence sentenceid="7db873ed54dd20320f62030423870fa1" id="tgt13" class="tgtSentence">Assume that the following sections in <legacyBold>MSDFMAP.INI</legacyBold> and the data source name, AdvWorks, have been previously defined:</caps:sentence>
        </para>
        <code>[connect CustomerDataBase]
Access=ReadWrite
Connect="DSN=AdvWorks"

[sql CustomerById]
SQL="SELECT * FROM Customers WHERE CustomerID = ?"</code>
        <para>
          <caps:sentence sentenceid="d1eac49244d510820450339433c0d725" id="tgt14" class="tgtSentence">The following code snippets are written in Visual Basic:</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="83322b0924fbbacc55b7a1dfc4899e61" id="tgt15" class="tgtSentence">RDS.DataControl Version</caps:sentence>
        </title>
        <content>
          <code>Dim dc as New RDS.DataControl
Set dc.Handler = "MSDFMAP.Handler"
Set dc.Server = "http://yourServer"
Set dc.Connect = "Data Source=CustomerDatabase"
Set dc.SQL = "CustomerById(4)"
dc.Refresh</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="3f5050cf8ff838a1f3bb8eceea812d51" id="tgt16" class="tgtSentence">Recordset Version</caps:sentence>
        </title>
        <content>
          <code>Dim rs as New ADODB.Recordset
rs.CursorLocation = adUseClient</code>
          <para>
            <caps:sentence sentenceid="f591c79c15146476a0c96699d5e2f3db" id="tgt17" class="tgtSentence">Specify either the <link xlink:href="fdc34362-6d47-4727-b171-8d033159408e">Handler Property (RDS)</link> property or keyword; the <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property (ADO)</link> property or keyword; and the <legacyItalic>CustomerById</legacyItalic> and <legacyItalic>CustomerDatabase</legacyItalic> identifiers.</caps:sentence>
            <caps:sentence sentenceid="2267af2a90664866b98370d5501b7e71" id="tgt18" class="tgtSentence"> Then open the <legacyBold>Recordset</legacyBold> object</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f8070ff1585b1b1e98e3d1fcac1c19f7" id="tgt19" class="tgtSentence">rs.Open "CustomerById(4)", "Handler=MSDFMAP.Handler;" &amp; _</caps:sentence>
          </para>
          <code>   "Provider=MS Remote;Data Source=CustomerDatabase;" &amp; _
   "Remote Server=http://yourServer"</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</link>
        <link xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src5" class="srcSentence">Specify the following settings to use a custom <legacyBold>DataFactory</legacyBold> handler.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Specify "Provider=MS Remote" in the <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object_ADO</link> object <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property (ADO)</link> property or the <legacyBold>Connection</legacyBold> object connection string "<legacyBold>Provider</legacyBold>=" keyword.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Set the <link xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation Property (ADO)</link> property to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Specify the name of the handler to use in the <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link> object's <legacyBold>Handler</legacyBold> property, or the <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link> object's connection string "<legacyBold>Handler</legacyBold>=" keyword.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> (You cannot set the handler in the <legacyBold>Connection</legacyBold> object connect string.)</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src10" class="srcSentence">RDS provides a default handler on the server named <legacyBold>MSDFMAP.Handler</legacyBold>.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> (The default customization file is named MSDFMAP.INI.)</caps:sentence>
        </para>
        <para>
          <legacyBold>
            <caps:sentence id="src12" class="srcSentence">Example</caps:sentence>
          </legacyBold>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">Assume that the following sections in <legacyBold>MSDFMAP.INI</legacyBold> and the data source name, AdvWorks, have been previously defined:</caps:sentence>
        </para>
        <code>[connect CustomerDataBase]
Access=ReadWrite
Connect="DSN=AdvWorks"

[sql CustomerById]
SQL="SELECT * FROM Customers WHERE CustomerID = ?"</code>
        <para>
          <caps:sentence id="src14" class="srcSentence">The following code snippets are written in Visual Basic:</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">RDS.DataControl Version</caps:sentence>
        </title>
        <content>
          <code>Dim dc as New RDS.DataControl
Set dc.Handler = "MSDFMAP.Handler"
Set dc.Server = "http://yourServer"
Set dc.Connect = "Data Source=CustomerDatabase"
Set dc.SQL = "CustomerById(4)"
dc.Refresh</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Recordset Version</caps:sentence>
        </title>
        <content>
          <code>Dim rs as New ADODB.Recordset
rs.CursorLocation = adUseClient</code>
          <para>
            <caps:sentence id="src17" class="srcSentence">Specify either the <link xlink:href="fdc34362-6d47-4727-b171-8d033159408e">Handler Property (RDS)</link> property or keyword; the <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property (ADO)</link> property or keyword; and the <legacyItalic>CustomerById</legacyItalic> and <legacyItalic>CustomerDatabase</legacyItalic> identifiers.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Then open the <legacyBold>Recordset</legacyBold> object</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">rs.Open "CustomerById(4)", "Handler=MSDFMAP.Handler;" &amp; _</caps:sentence>
          </para>
          <code>   "Provider=MS Remote;Data Source=CustomerDatabase;" &amp; _
   "Remote Server=http://yourServer"</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</link>
        <link xlink:href="d447712a-e123-47b5-a3a4-5d366cfe8d72">Writing Your Own Customized Handler</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
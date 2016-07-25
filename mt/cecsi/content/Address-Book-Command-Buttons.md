---
title: "Address Book Command Buttons"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 80676831-6488-4dad-a558-c47c52256a22
caps.latest.revision: 14
caps.handback.revision: 14
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
# Address Book Command Buttons
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9292f6469d07efc9587de61abce38065" id="tgt1" class="tgtSentence">The Address Book application includes the following command buttons:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="6492fa568c77ae28f5a9ac5b70034740" id="tgt2" class="tgtSentence">A <ui>Find</ui> button to submit a query to the database.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ef3291d02f9d76a6f3194ec70cef5dd4" id="tgt3" class="tgtSentence">A <ui>Clear</ui> button to clear the text boxes before starting a new search.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0306be15b28ceec3c8ae9ae63ae8b232" id="tgt4" class="tgtSentence">An <ui>Update Profile</ui> button to save changes to an employee record.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="36a99736bd8eb28995fab18d39b79cfa" id="tgt5" class="tgtSentence">A <ui>Cancel Changes</ui> button to discard changes.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt6" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt7" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt8" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt9" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="ce48af4735f0f551f5fbb9f7ae3a0f1d" id="tgt10" class="tgtSentence">Find Button</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d30161780c9ab3cf6bb7f49b590c2c23" id="tgt11" class="tgtSentence">Clicking the <ui>Find</ui> button activates the VBScript Find_OnClick Sub procedure, which builds and sends the SQL query.</caps:sentence>
            <caps:sentence sentenceid="2747ac81c1d64a97b103f77edcc99e44" id="tgt12" class="tgtSentence"> Clicking this button populates the data grid.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5b1d724aaca3fc2f7634e50e6da7cc68" id="tgt13" class="tgtSentence">Building the SQL Query</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="466e835139554b6eec4069943096a0b9" id="tgt14" class="tgtSentence">The first part of the Find_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</caps:sentence>
            <caps:sentence sentenceid="f46fa8ca38360411f27292c9f9430b12" id="tgt15" class="tgtSentence"> It begins by setting the variable <codeInline>myQuery</codeInline> to a SQL SELECT statement that requests all rows of data from the data source table.</caps:sentence>
            <caps:sentence sentenceid="f62f62f30eb72484f82b4f42e1a1c178" id="tgt16" class="tgtSentence"> Next, the Sub procedure scans each of the four input boxes on the page.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="625ed0457b8bfcc7f6a118e19c2150d0" id="tgt17" class="tgtSentence">Because the program uses the word <codeInline>like</codeInline> in building the SQL statements, the queries are substring searches rather than exact matches.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1f213e9d9dea0a7f27c82146e01fdbd3" id="tgt18" class="tgtSentence">For example, if the <legacyBold>Last Name</legacyBold> box contained the entry "Berge" and the <legacyBold>Title</legacyBold> box contained the entry "Program Manager", the SQL statement (value of <codeInline>myQuery</codeInline>) would read:</caps:sentence>
          </para>
          <code>Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%'</code>
          <para>
            <caps:sentence sentenceid="3903fabc80285c7d82b89ce2625bd9fa" id="tgt19" class="tgtSentence">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="03f68f74f4a66946a3f450cc620355d3" id="tgt20" class="tgtSentence">Preparing and Sending the Query</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ff70c5c86bdcea6e8e046b2e44eb92af" id="tgt21" class="tgtSentence">The last part of the Find_OnClick Sub procedure consists of two statements.</caps:sentence>
            <caps:sentence sentenceid="21688b463ca2ca6d46b63850eb9d5230" id="tgt22" class="tgtSentence"> The first statement assigns the <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> property of the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object equal to the dynamically built SQL query.</caps:sentence>
            <caps:sentence sentenceid="4e8b684ee44987e82cb36e5e9d0a3d8c" id="tgt23" class="tgtSentence"> The second statement causes the <legacyBold>RDS.DataControl</legacyBold> object (<codeInline>DC1</codeInline>) to query the database, and then display the new results of the query in the grid.</caps:sentence>
          </para>
          <code>Sub Find_OnClick
   '...
   DC1.SQL = myQuery
   DC1.Refresh
End Sub</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1d01386cbad048042c15c153c5f46233" id="tgt24" class="tgtSentence">Update Profile Button</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b3c114c41d539e4c905c0928da141be2" id="tgt25" class="tgtSentence">Clicking the <legacyBold>Update Profile</legacyBold> button activates the VBScript Update_OnClick Sub procedure, which executes the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's (<codeInline>DC1</codeInline>) <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges</legacyLink> and <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh</legacyLink> methods.</caps:sentence>
          </para>
          <code>Sub Update_OnClick
   DC1.SubmitChanges
   DC1.Refresh
End Sub</code>
          <para>
            <caps:sentence sentenceid="ccd4e157b0cec0bbe5ce63fb24b629fd" id="tgt26" class="tgtSentence">When <codeInline>DC1.SubmitChanges</codeInline> executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</caps:sentence>
            <caps:sentence sentenceid="f4cd2ab31960940e5ee3bb86aa644700" id="tgt27" class="tgtSentence"> The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</caps:sentence>
            <caps:sentence sentenceid="9b0b43ccd32dce0e23ceeda7c3e5f174" id="tgt28" class="tgtSentence">
              <codeInline>DC1.Refresh </codeInline>isn't necessary after <legacyBold>SubmitChanges</legacyBold> with Remote Data Service, but it ensures fresh data.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1c9a57f89401eb2334ac38065ddb5622" id="tgt29" class="tgtSentence">Cancel Changes Button</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e4d72bc29574d7ff138d7019706aeda5" id="tgt30" class="tgtSentence">Clicking <legacyBold>Cancel Changes</legacyBold> activates the VBScript Cancel_OnClick Sub procedure, which executes the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's (<codeInline>DC1)</codeInline> <legacyLink xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate</legacyLink> method.</caps:sentence>
          </para>
          <code>Sub Cancel_OnClick
   DC1.CancelUpdate
End Sub</code>
          <para>
            <caps:sentence sentenceid="fe4a61fda7297ee3752dfd37bbc97c5b" id="tgt31" class="tgtSentence">When<codeInline> DC1.CancelUpdate</codeInline> executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</caps:sentence>
            <caps:sentence sentenceid="1f858308cf587bdbe16fc94cf699a9d5" id="tgt32" class="tgtSentence"> It restores the original values.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f0dd84c6-5c33-4ab9-82b4-4c42dfdd2277">Address Book Navigation Buttons</link>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Address Book application includes the following command buttons:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">A <ui>Find</ui> button to submit a query to the database.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">A <ui>Clear</ui> button to clear the text boxes before starting a new search.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">An <ui>Update Profile</ui> button to save changes to an employee record.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">A <ui>Cancel Changes</ui> button to discard changes.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence id="src6" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Find Button</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">Clicking the <ui>Find</ui> button activates the VBScript Find_OnClick Sub procedure, which builds and sends the SQL query.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Clicking this button populates the data grid.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Building the SQL Query</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">The first part of the Find_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> It begins by setting the variable <codeInline>myQuery</codeInline> to a SQL SELECT statement that requests all rows of data from the data source table.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Next, the Sub procedure scans each of the four input boxes on the page.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">Because the program uses the word <codeInline>like</codeInline> in building the SQL statements, the queries are substring searches rather than exact matches.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">For example, if the <legacyBold>Last Name</legacyBold> box contained the entry "Berge" and the <legacyBold>Title</legacyBold> box contained the entry "Program Manager", the SQL statement (value of <codeInline>myQuery</codeInline>) would read:</caps:sentence>
          </para>
          <code>Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%'</code>
          <para>
            <caps:sentence id="src19" class="srcSentence">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Preparing and Sending the Query</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">The last part of the Find_OnClick Sub procedure consists of two statements.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> The first statement assigns the <legacyLink xlink:href="e0dabf23-a159-4fe5-a962-3df544a21f5c">SQL</legacyLink> property of the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object equal to the dynamically built SQL query.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> The second statement causes the <legacyBold>RDS.DataControl</legacyBold> object (<codeInline>DC1</codeInline>) to query the database, and then display the new results of the query in the grid.</caps:sentence>
          </para>
          <code>Sub Find_OnClick
   '...
   DC1.SQL = myQuery
   DC1.Refresh
End Sub</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src24" class="srcSentence">Update Profile Button</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src25" class="srcSentence">Clicking the <legacyBold>Update Profile</legacyBold> button activates the VBScript Update_OnClick Sub procedure, which executes the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's (<codeInline>DC1</codeInline>) <legacyLink xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges</legacyLink> and <legacyLink xlink:href="c90a8050-0ff4-4c83-9925-261f2f2ccfe9">Refresh</legacyLink> methods.</caps:sentence>
          </para>
          <code>Sub Update_OnClick
   DC1.SubmitChanges
   DC1.Refresh
End Sub</code>
          <para>
            <caps:sentence id="src26" class="srcSentence">When <codeInline>DC1.SubmitChanges</codeInline> executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence">
              <codeInline>DC1.Refresh </codeInline>isn't necessary after <legacyBold>SubmitChanges</legacyBold> with Remote Data Service, but it ensures fresh data.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src29" class="srcSentence">Cancel Changes Button</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src30" class="srcSentence">Clicking <legacyBold>Cancel Changes</legacyBold> activates the VBScript Cancel_OnClick Sub procedure, which executes the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object's (<codeInline>DC1)</codeInline> <legacyLink xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate</legacyLink> method.</caps:sentence>
          </para>
          <code>Sub Cancel_OnClick
   DC1.CancelUpdate
End Sub</code>
          <para>
            <caps:sentence id="src31" class="srcSentence">When<codeInline> DC1.CancelUpdate</codeInline> executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> It restores the original values.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f0dd84c6-5c33-4ab9-82b4-4c42dfdd2277">Address Book Navigation Buttons</link>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "RDS Scenario"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a7dcad87-aaf0-4b02-9660-472f8469761c
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
# RDS Scenario
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
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
          <caps:sentence sentenceid="c800ff26f4280a274ed852a02c544a5f" id="tgt5" class="tgtSentence">The Address Book application is a scenario that shows you how to use Remote Data Service (RDS) to build a simple, data-aware Web application — an online corporate address book.</caps:sentence>
          <caps:sentence sentenceid="ef67dc7e6e7147a2dc11756e3e0a2621" id="tgt6" class="tgtSentence"> This scenario is useful for Microsoft Visual Basic Scripting Edition (VBScript) and COM programmers who want to learn how to use data-aware ActiveX Controls with RDS, and for more experienced software developers who want to build data-centric Web applications.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="83b267f2d91759fa0835c55069607d21" id="tgt7" class="tgtSentence">This scenario assumes that you know how to use basic HTML layout tags, use DHTML data binding techniques, and program with ActiveX Controls.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="dd5c3c114b8b3f3bad2d2c947e3128fb" id="tgt8" class="tgtSentence">If you have installed the SDK, the complete source code for the Address Book sample application can be found in the SDK directory at samples\dataaccess\rds\AddressBook\AddressBook.asp.</caps:sentence>
          <caps:sentence sentenceid="63a1e01f83ed191dd1f6179e8989b03e" id="tgt9" class="tgtSentence"> To view the Address Book scenario, in Internet Explorer 4.0 or later, type <legacyBold>http://</legacyBold><legacyBold><legacyItalic>webserver</legacyItalic></legacyBold><legacyBold>/RDS/AddressBook/AddressBook.asp</legacyBold> where <legacyItalic>webserver</legacyItalic> is the name given to your Windows NT 4.0 or Windows 2000 Web server computer that is running Internet Information Services (IIS) and ASP.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="9bf61bad9cea54d382e91d1a7e40b240" id="tgt10" class="tgtSentence">Introduction to Address Book</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b2f7aa0cc488d955ae20e7225b8eea90" id="tgt11" class="tgtSentence">The Address Book sample application provides a simple online address book that you can use to publish a searchable directory over an intranet.</caps:sentence>
            <caps:sentence sentenceid="4e4ce3e7068ce78a48e131cf69e9fb00" id="tgt12" class="tgtSentence"> The address book is designed so that a user can enter a search string in one or more fields to request information about employees.</caps:sentence>
            <caps:sentence sentenceid="66e33fc60cc822cba8e10d8fd392140b" id="tgt13" class="tgtSentence"> To show you the basic features of Remote Data Service, the sample application is intentionally kept small, with a minimum number of objects and search fields.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="981f81e23ced01b964f9762dd683bf6e" id="tgt14" class="tgtSentence">The application interface consists of the following parts:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="9fa6ece5e5b1bc205ee95ded3bb99113" id="tgt15" class="tgtSentence">A non-visual <legacyBold>RDS.DataControl</legacyBold> data-binding object that is used by the client to connect to the database.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dffa14954461e0d313aec9bef4e06b46" id="tgt16" class="tgtSentence">HTML text boxes that act as input fields for employee attribute search criteria.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="840bcb562fe34f5dc97451626349ac5a" id="tgt17" class="tgtSentence">HTML command buttons to build queries, clear search fields, update the database with employee information, cancel pending changes, and navigate the rows of data displayed in the grid.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4109c6b9c6d0f5c9067975a2ab5ef8e9" id="tgt18" class="tgtSentence">DHTML data binding to display data returned from queries against a back-end database (through the <legacyBold>RDS.DataControl</legacyBold> data-binding object) in a table.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3db942142ca270a5150d90759ca55a77" id="tgt19" class="tgtSentence">VBScript routines that connect each of the elements that were previously mentioned and allow them to interact.</caps:sentence>
                <caps:sentence sentenceid="bbefe8a8cc81d3043ec3518802d5dc15" id="tgt20" class="tgtSentence"> VBScript code is also used to initialize the <legacyBold>RDS.DataControl</legacyBold> object and dynamically create the column headings in the HTML table from the names of the <legacyBold>RDS.DataControl</legacyBold> recordset fields.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="1630928d30f2fffa0204903ef2d52fb0" id="tgt21" class="tgtSentence">Follow the links from step to step to set up and run the scenario and to learn more about how the scenario works.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1e85059cc108e781f232de883af7d976" id="tgt22" class="tgtSentence">This scenario contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="e3b1a399f504cda35d2dbf2c9b697a05" id="tgt23" class="tgtSentence">
                  <legacyLink xlink:href="da385405-1c9a-478b-9bf6-fba70015324c">System Requirements for the Address Book Application</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5dbf43f51a70a8dcbe895b0499b694ff" id="tgt24" class="tgtSentence">
                  <legacyLink xlink:href="409b3f8b-0ced-4867-acbe-b245dcdf6702">Running the Address Book SQL Script</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3cc5cd381946691dff45422a0171776f" id="tgt25" class="tgtSentence">
                  <legacyLink xlink:href="3a2644e9-d634-4ae6-a5b7-13fb7b317ec7">Running the Address Book Sample Application</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b88ed4f8c86efd1bc7be2d8c1c965322" id="tgt26" class="tgtSentence">
                  <legacyLink xlink:href="080c1925-d453-4b89-92ac-c93591490518">Address Book Data-Binding Object</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f843f2c618a33f14da483ec66b1daa99" id="tgt27" class="tgtSentence">
                  <legacyLink xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="37f0be79a7e928105d9ff57bc4a0a773" id="tgt28" class="tgtSentence">
                  <legacyLink xlink:href="f0dd84c6-5c33-4ab9-82b4-4c42dfdd2277">Address Book Navigation Buttons</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="da385405-1c9a-478b-9bf6-fba70015324c">System Requirements for the Address Book Application</link>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
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
          <caps:sentence id="src5" class="srcSentence">The Address Book application is a scenario that shows you how to use Remote Data Service (RDS) to build a simple, data-aware Web application — an online corporate address book.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> This scenario is useful for Microsoft Visual Basic Scripting Edition (VBScript) and COM programmers who want to learn how to use data-aware ActiveX Controls with RDS, and for more experienced software developers who want to build data-centric Web applications.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">This scenario assumes that you know how to use basic HTML layout tags, use DHTML data binding techniques, and program with ActiveX Controls.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">If you have installed the SDK, the complete source code for the Address Book sample application can be found in the SDK directory at samples\dataaccess\rds\AddressBook\AddressBook.asp.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> To view the Address Book scenario, in Internet Explorer 4.0 or later, type <legacyBold>http://</legacyBold><legacyBold><legacyItalic>webserver</legacyItalic></legacyBold><legacyBold>/RDS/AddressBook/AddressBook.asp</legacyBold> where <legacyItalic>webserver</legacyItalic> is the name given to your Windows NT 4.0 or Windows 2000 Web server computer that is running Internet Information Services (IIS) and ASP.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Introduction to Address Book</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">The Address Book sample application provides a simple online address book that you can use to publish a searchable directory over an intranet.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The address book is designed so that a user can enter a search string in one or more fields to request information about employees.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> To show you the basic features of Remote Data Service, the sample application is intentionally kept small, with a minimum number of objects and search fields.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">The application interface consists of the following parts:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">A non-visual <legacyBold>RDS.DataControl</legacyBold> data-binding object that is used by the client to connect to the database.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">HTML text boxes that act as input fields for employee attribute search criteria.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">HTML command buttons to build queries, clear search fields, update the database with employee information, cancel pending changes, and navigate the rows of data displayed in the grid.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">DHTML data binding to display data returned from queries against a back-end database (through the <legacyBold>RDS.DataControl</legacyBold> data-binding object) in a table.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">VBScript routines that connect each of the elements that were previously mentioned and allow them to interact.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> VBScript code is also used to initialize the <legacyBold>RDS.DataControl</legacyBold> object and dynamically create the column headings in the HTML table from the names of the <legacyBold>RDS.DataControl</legacyBold> recordset fields.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src21" class="srcSentence">Follow the links from step to step to set up and run the scenario and to learn more about how the scenario works.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">This scenario contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">
                  <legacyLink xlink:href="da385405-1c9a-478b-9bf6-fba70015324c">System Requirements for the Address Book Application</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src24" class="srcSentence">
                  <legacyLink xlink:href="409b3f8b-0ced-4867-acbe-b245dcdf6702">Running the Address Book SQL Script</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src25" class="srcSentence">
                  <legacyLink xlink:href="3a2644e9-d634-4ae6-a5b7-13fb7b317ec7">Running the Address Book Sample Application</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src26" class="srcSentence">
                  <legacyLink xlink:href="080c1925-d453-4b89-92ac-c93591490518">Address Book Data-Binding Object</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src27" class="srcSentence">
                  <legacyLink xlink:href="80676831-6488-4dad-a558-c47c52256a22">Address Book Command Buttons</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src28" class="srcSentence">
                  <legacyLink xlink:href="f0dd84c6-5c33-4ab9-82b4-4c42dfdd2277">Address Book Navigation Buttons</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="da385405-1c9a-478b-9bf6-fba70015324c">System Requirements for the Address Book Application</link>
        <link xlink:href="2fa6237b-44b8-4b6c-9952-5acd80a54e20">ActiveX Data Objects Start Page</link>
        <link xlink:href="a676f0a7-7d17-45db-87c1-3fc78627465f">RDS Fundamentals</link>
        <link xlink:href="6e3305a0-7bc7-40d1-9122-235c15d23ab2">RDS Tutorial</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
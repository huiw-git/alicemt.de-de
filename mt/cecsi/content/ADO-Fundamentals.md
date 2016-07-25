---
title: "ADO Fundamentals"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6a66928-e68f-4c38-b87a-838c5de50a28
caps.latest.revision: 9
caps.handback.revision: 9
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
# ADO Fundamentals
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3bd196c69acaecdec6fb4b4216e22a22" id="tgt1" class="tgtSentence">ADO gives developers a powerful, logical object model for programmatically accessing, editing, and updating data from a wide variety of data sources through OLE DB system interfaces.</caps:sentence>
          <caps:sentence sentenceid="74c9ef2a5fd187e1c797be7940d577d1" id="tgt2" class="tgtSentence"> The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps let users make and save changes to the data.</caps:sentence>
          <caps:sentence sentenceid="21785464d338bc9e5a2902f34e7f19ce" id="tgt3" class="tgtSentence"> Other tasks include the following:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="9182db92a8dd7b18721827eed52a791c" id="tgt4" class="tgtSentence">Querying a database using SQL and displaying the results.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a1f615a8edf840a4afbc08deb806d7e3" id="tgt5" class="tgtSentence">Accessing information in a file store over the Internet.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a0db5673e4ed78f7cea5ac47abf70b6e" id="tgt6" class="tgtSentence">Manipulating messages and folders in an e-mail system.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="19d05ed82b7907cd7c6eb8b82cbffafb" id="tgt7" class="tgtSentence">Saving data from a database into an XML file.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6b17f6944f51a8d218b4f1de05062b26" id="tgt8" class="tgtSentence">Executing commands described with XML and retrieving an XML stream.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ac677243d84c9b02e106c8615e66efd2" id="tgt9" class="tgtSentence">Saving data into a binary or XML stream.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="69ea32b90c79efd4d942a3c330b06cce" id="tgt10" class="tgtSentence">Allowing a user to review and change data in database tables.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a510a037dc216b8750c476ee6b8010ed" id="tgt11" class="tgtSentence">Creating and reusing parameterized database commands.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8adf07b751eb121f7406e48c9a36238b" id="tgt12" class="tgtSentence">Executing stored procedures.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b09f6fc1fe0b31aedbc3cb27ca7bacee" id="tgt13" class="tgtSentence">Dynamically creating a flexible structure, which is named a <legacyBold>Recordset</legacyBold>, to hold, navigate, and manipulate data.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b2b8f50fbfe801c58b7d1228a3fc98c1" id="tgt14" class="tgtSentence">Performing transactional database operations.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e6dc8a8e696880cbdacf0a815bb6e530" id="tgt15" class="tgtSentence">Filtering and sorting local copies of database information based on run-time criteria.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4228d47be5d60f2f6c053fa11dadf993" id="tgt16" class="tgtSentence">Creating and manipulating hierarchical results from databases.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="bc469bd50a051eefbe6c0c23a6366da7" id="tgt17" class="tgtSentence">Binding database fields to data-aware components.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f3a54a1c7ab42230d6e439be3fbd9cae" id="tgt18" class="tgtSentence">Creating remote, disconnected <legacyBold>Recordsets</legacyBold>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="0452616497942bf347e46c5779d7545e" id="tgt19" class="tgtSentence">ADO exposes a wide variety of options and settings to provide such flexibility.</caps:sentence>
          <caps:sentence sentenceid="52c3d4aacc13548d449184fc0a37b73c" id="tgt20" class="tgtSentence"> Therefore, it is important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="46a7f52f270df257e766cc19734d7646" id="tgt21" class="tgtSentence">Four primary operations are involved in most applications that use ADO: getting data, examining data, editing data, and updating data.</caps:sentence>
          <caps:sentence sentenceid="c5570f4ba43234c8fd6ae38070930534" id="tgt22" class="tgtSentence"> These operations are examined in more detail later in this section.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="d285653e958535a453efe757123390d0" id="tgt23" class="tgtSentence">However, before we discuss these details, we will present an overview of the ADO object model and a simple ADO application, which is written in Microsoft® Visual Basic® and performs each of the four primary ADO operations:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="fb2ec7c2ea6a69a4fcca0338bd6d46e0" id="tgt24" class="tgtSentence">             <legacyLink xlink:href="7a745aae-9372-49b6-8dae-b9c93e5f3216">ADO Objects and Collections</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="64fad1c46553a3682847168c57b5d9eb" id="tgt25" class="tgtSentence">             <legacyLink xlink:href="de4bcd56-dac2-45e6-95ab-9fd7f25878fc">HelloData: A Simple ADO Application</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a381fb22c08f1329c018715bead37097" id="tgt26" class="tgtSentence">             <legacyLink xlink:href="6e0488c3-934d-4976-99dc-65c580dc7a3c">OLE DB Providers</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="875912320d2a9b47135e5e843bf10f99" id="tgt27" class="tgtSentence">             <legacyLink xlink:href="8ae6611b-3069-4155-b014-c0c9da37be39">Errors</legacyLink>           </caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">ADO gives developers a powerful, logical object model for programmatically accessing, editing, and updating data from a wide variety of data sources through OLE DB system interfaces.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps let users make and save changes to the data.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Other tasks include the following:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Querying a database using SQL and displaying the results.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Accessing information in a file store over the Internet.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Manipulating messages and folders in an e-mail system.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Saving data from a database into an XML file.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Executing commands described with XML and retrieving an XML stream.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Saving data into a binary or XML stream.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Allowing a user to review and change data in database tables.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Creating and reusing parameterized database commands.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Executing stored procedures.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">Dynamically creating a flexible structure, which is named a <legacyBold>Recordset</legacyBold>, to hold, navigate, and manipulate data.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">Performing transactional database operations.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">Filtering and sorting local copies of database information based on run-time criteria.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">Creating and manipulating hierarchical results from databases.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">Binding database fields to data-aware components.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">Creating remote, disconnected <legacyBold>Recordsets</legacyBold>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src19" class="srcSentence">ADO exposes a wide variety of options and settings to provide such flexibility.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> Therefore, it is important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src21" class="srcSentence">Four primary operations are involved in most applications that use ADO: getting data, examining data, editing data, and updating data.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> These operations are examined in more detail later in this section.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src23" class="srcSentence">However, before we discuss these details, we will present an overview of the ADO object model and a simple ADO application, which is written in Microsoft® Visual Basic® and performs each of the four primary ADO operations:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src24" class="srcSentence">             <legacyLink xlink:href="7a745aae-9372-49b6-8dae-b9c93e5f3216">ADO Objects and Collections</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src25" class="srcSentence">             <legacyLink xlink:href="de4bcd56-dac2-45e6-95ab-9fd7f25878fc">HelloData: A Simple ADO Application</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src26" class="srcSentence">             <legacyLink xlink:href="6e0488c3-934d-4976-99dc-65c580dc7a3c">OLE DB Providers</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src27" class="srcSentence">             <legacyLink xlink:href="8ae6611b-3069-4155-b014-c0c9da37be39">Errors</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
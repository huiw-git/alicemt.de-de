---
title: "DataFactory Object (RDSServer) Properties, Methods, and Events"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 36a1f49b-91f4-44f4-b6e2-52fc7ed06d7e
caps.latest.revision: 13
caps.handback.revision: 13
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
# DataFactory Object (RDSServer) Properties, Methods, and Events
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
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt5" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt6" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt7" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe">ConvertToString Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9069410b328b8f1fc71da540ccc19371" id="tgt8" class="tgtSentence">Converts a recordset into a MIME64 string.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d638423986deb6ea4f841ec6187b4682" id="tgt9" class="tgtSentence">Creates and returns an empty recordset.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="2d9c30e9-ab5b-4920-91b8-48454c2fb5d8">Execute Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="81df981db0eb7707f822e2444931015b" id="tgt10" class="tgtSentence">Execute the request and create an advanced data rowset (for use with ADO 2.5 or later).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="9f131c8d-1497-416d-8209-abb481c38f7b">Execute21 Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c2c67f08cb46e6d877cc1e361cf9aedf" id="tgt11" class="tgtSentence">Execute the request and create an advanced data rowset (for use with ADO 2.1).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="404b336a09e00dd4afc135b8823e3698" id="tgt12" class="tgtSentence">Execute the request and create an advanced data rowset.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="79eaa385d36a51b19cad1f0726047949" id="tgt13" class="tgtSentence">Given a recordset with pending changes, this method submits them to the database identified in the connection string.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="7af42866-7db2-4174-8251-388a2cf741f2">Synchronize Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2bca2687830a72ad50a26f95f5230e0a" id="tgt14" class="tgtSentence">Synchronize the given recordset with the database specified by the connection string (for use with ADO 2.5 or later).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="6b35f136-9d9a-4bdd-8144-67decfd3c4e9">Synchronize21 Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="62a93a8e3e6ee068a2788ee01b958928" id="tgt15" class="tgtSentence">Synchronize the given recordset with the database specified by the connection string (for use with ADO 2.1).</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt16" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt17" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
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
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="b3f36bc8-6f69-49b0-83cd-2ccd3afebfbe">ConvertToString Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Converts a recordset into a MIME64 string.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Creates and returns an empty recordset.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="2d9c30e9-ab5b-4920-91b8-48454c2fb5d8">Execute Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Execute the request and create an advanced data rowset (for use with ADO 2.5 or later).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="9f131c8d-1497-416d-8209-abb481c38f7b">Execute21 Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Execute the request and create an advanced data rowset (for use with ADO 2.1).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="20f2480f-3758-405d-a379-05a0dce74796">Query Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Execute the request and create an advanced data rowset.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="250062a4-13c4-4bed-807d-8b9ad81536d4">SubmitChanges Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Given a recordset with pending changes, this method submits them to the database identified in the connection string.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="7af42866-7db2-4174-8251-388a2cf741f2">Synchronize Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Synchronize the given recordset with the database specified by the connection string (for use with ADO 2.5 or later).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="6b35f136-9d9a-4bdd-8144-67decfd3c4e9">Synchronize21 Method (RDS)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Synchronize the given recordset with the database specified by the connection string (for use with ADO 2.1).</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory Object (RDSServer)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
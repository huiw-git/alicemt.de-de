---
title: "Namespaces"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: efff5569-db52-451d-a039-2e74870534da
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
# Namespaces
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6907ee96a603b77f9eb5caa0a37c6b07" id="tgt1" class="tgtSentence">The XML persistence format in ADO uses the following four namespaces.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt2" class="tgtSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6907ee96a603b77f9eb5caa0a37c6b07" id="tgt3" class="tgtSentence">The XML persistence format in ADO uses the following four namespaces.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="851f5ac9941d720844d143ed9cfcf60a" id="tgt4" class="tgtSentence">Prefix</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt5" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03c7c0ace395d80182db07ae2c30f034" id="tgt6" class="tgtSentence">s</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5e3197fa361ad24d587ae4555c1af867" id="tgt7" class="tgtSentence">Refers to the "XML-Data" namespace containing the elements and attributes that define the schema of the current Recordset.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3017d911efceb27d1de6a92b70979795" id="tgt8" class="tgtSentence">dt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6c468be2bab02197b2adaf50de78155" id="tgt9" class="tgtSentence">Refers to the data type definitions specification.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3a2d7564baee79182ebc7b65084aabd1" id="tgt10" class="tgtSentence">rs</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f4bcad8d899dae48051cc086e9782f8d" id="tgt11" class="tgtSentence">Refers to the namespace containing elements and attributes specific to ADO Recordset properties and attributes.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fbade9e36a3f36d3d676c1b808451dd7" id="tgt12" class="tgtSentence">z</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="212ba141f17e340dbc842831d277b702" id="tgt13" class="tgtSentence">Refers to the schema of the current rowset.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="011e90b471da0cf2048111842457fae8" id="tgt14" class="tgtSentence">A client should not add its own tags to these namespaces, as defined by the specification.</caps:sentence>
            <caps:sentence sentenceid="c1ea3b22ed618db86383c05bec7c7341" id="tgt15" class="tgtSentence"> For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</caps:sentence>
            <caps:sentence sentenceid="b3a7ec5f56b0ed048d192968f22f5147" id="tgt16" class="tgtSentence"> To learn more about namespaces, see the <externalLink><linkText>W3C Namespaces in XML Recommendation</linkText><linkUri>http://www.w3.org/TR/REC-xml-names/</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="663fa292e41301d3a9f4c0ff86dcf9d1" id="tgt17" class="tgtSentence">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="917585b5e9878123bcecf9cf0d524b59" id="tgt18" class="tgtSentence">Note that the prefix of the namespace — the part between the colon and the equal sign — is arbitrary.</caps:sentence>
          </para>
          <code>xmlns:rs="urn:schemas-microsoft-com:rowset"</code>
          <para>
            <caps:sentence sentenceid="af08cd196e1f7088461f6d808c9d5979" id="tgt19" class="tgtSentence">The user can define this to be any name as long as this name is consistently used throughout the XML document.</caps:sentence>
            <caps:sentence sentenceid="0c7910f4c7aa402b0d7fae87e05f625e" id="tgt20" class="tgtSentence"> ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The XML persistence format in ADO uses the following four namespaces.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">The XML persistence format in ADO uses the following four namespaces.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">Prefix</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">s</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Refers to the "XML-Data" namespace containing the elements and attributes that define the schema of the current Recordset.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">dt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Refers to the data type definitions specification.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">rs</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Refers to the namespace containing elements and attributes specific to ADO Recordset properties and attributes.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">z</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Refers to the schema of the current rowset.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src14" class="srcSentence">A client should not add its own tags to these namespaces, as defined by the specification.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> To learn more about namespaces, see the <externalLink><linkText>W3C Namespaces in XML Recommendation</linkText><linkUri>http://www.w3.org/TR/REC-xml-names/</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src17" class="srcSentence">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src18" class="srcSentence">Note that the prefix of the namespace — the part between the colon and the equal sign — is arbitrary.</caps:sentence>
          </para>
          <code>xmlns:rs="urn:schemas-microsoft-com:rowset"</code>
          <para>
            <caps:sentence id="src19" class="srcSentence">The user can define this to be any name as long as this name is consistently used throughout the XML document.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "XML Persistence Format"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6e146738-ac4d-47bb-b6cd-d87b2260aead
caps.latest.revision: 5
caps.handback.revision: 5
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
# XML Persistence Format
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="28daf5d7f0b0bc0f4c32cbf726ad7c56" id="tgt1" class="tgtSentence">ADO uses UTF-8 encoding for the XML stream it persists.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2e4892005497108ed85a919888d1f9a0" id="tgt2" class="tgtSentence">The ADO XML format is broken into two sections, a schema section followed by the data section.</caps:sentence>
          <caps:sentence sentenceid="ecdf955895fcd9061ce67952f0305fb3" id="tgt3" class="tgtSentence"> The following is an example XML file for the Shippers table from the Northwind database.</caps:sentence>
          <caps:sentence sentenceid="1b4b4a53497165941c1a676184fbfe4b" id="tgt4" class="tgtSentence"> Various parts of the XML are discussed following the example.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt5" class="tgtSentence">Remarks</caps:sentence>
        </title>
        <content>
          <code>&lt;xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882" 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
xmlns:z="#RowsetSchema"&gt; 
  &lt;s:Schema id="RowsetSchema"&gt; 
    &lt;s:ElementType name="row" content="eltOnly" rs:updatable="true"&gt; 
      &lt;s:AttributeType name="ShipperID" rs:number="1" 
        rs:basetable="shippers" rs:basecolumn="ShipperID"
        rs:keycolumn="true"&gt; 
        &lt;s:datatype dt:type="int" dt:maxLength="4" rs:precision="10" 
          rs:fixedlength="true" rs:maybenull="false"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:AttributeType name="CompanyName" rs:number="2" 
        rs:nullable="true" rs:write="true" rs:basetable="shippers" 
        rs:basecolumn="CompanyName"&gt; 
        &lt;s:datatype dt:type="string" dt:maxLength="40" /&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:AttributeType name="Phone" rs:number="3" rs:nullable="true" 
        rs:write="true" rs:basetable="shippers" 
        rs:basecolumn="Phone"&gt; 
        &lt;s:datatype dt:type="string" dt:maxLength="24"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:extends type="rs:rowbase"/&gt; 
    &lt;/s:ElementType&gt; 
  &lt;/s:Schema&gt; 

  &lt;rs:data&gt; 
    &lt;z:row ShipperID="1" CompanyName="Speedy Express" 
      Phone="(503) 555-9831"/&gt; 
    &lt;z:row ShipperID="2" CompanyName="United Package" 
      Phone="(503) 555-3199"/&gt; 
    &lt;z:row ShipperID="3" CompanyName="Federal Shipping" 
      Phone="(503) 555-9931"/&gt; 
  &lt;/rs:data&gt; 
&lt;/xml&gt;</code>
          <para>
            <caps:sentence sentenceid="cafbbf34502f30807b5fd34dcd0b66ab" id="tgt6" class="tgtSentence">The schema shows the declarations of namespaces, the schema section, and the data section.</caps:sentence>
            <caps:sentence sentenceid="41c39b12a4a83eea080c0c73ed84ecb2" id="tgt7" class="tgtSentence"> The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6032379d986842c76042fabf4ea7dd4e" id="tgt8" class="tgtSentence">Schema definitions conform to the <externalLink><linkText>W3C XML-Data specification</linkText><linkUri>http://www.w3.org/TR/1998/NOTE-XML-data/</linkUri></externalLink> and can be fully validated (though validation will not occur in Internet Explorer 5).</caps:sentence>
            <caps:sentence sentenceid="b06dea2150989c5eaa4a42abaa1ec488" id="tgt9" class="tgtSentence"> XML-Data is currently the only supported schema format for Recordset persistence.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d30bda5cf79063dd5e9a9f0fbca7b39c" id="tgt10" class="tgtSentence">The data section has three rows containing information about shippers.</caps:sentence>
            <caps:sentence sentenceid="9df9c9e9d57bd6d47b0597df35cfc7c5" id="tgt11" class="tgtSentence"> For an empty rowset, the data section may be empty, but the &lt;rs:data&gt; tags must be present.</caps:sentence>
            <caps:sentence sentenceid="600f1ed4fc349f1124cf525adf594635" id="tgt12" class="tgtSentence"> With no data, you could write the tag shorthand as simply &lt;rs:data/&gt;.</caps:sentence>
            <caps:sentence sentenceid="a3e1e6fa705ac81c0185dd41eab98326" id="tgt13" class="tgtSentence"> Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">ADO uses UTF-8 encoding for the XML stream it persists.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">The ADO XML format is broken into two sections, a schema section followed by the data section.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The following is an example XML file for the Shippers table from the Northwind database.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Various parts of the XML are discussed following the example.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Remarks</caps:sentence>
        </title>
        <content>
          <code>&lt;xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882" 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
xmlns:z="#RowsetSchema"&gt; 
  &lt;s:Schema id="RowsetSchema"&gt; 
    &lt;s:ElementType name="row" content="eltOnly" rs:updatable="true"&gt; 
      &lt;s:AttributeType name="ShipperID" rs:number="1" 
        rs:basetable="shippers" rs:basecolumn="ShipperID"
        rs:keycolumn="true"&gt; 
        &lt;s:datatype dt:type="int" dt:maxLength="4" rs:precision="10" 
          rs:fixedlength="true" rs:maybenull="false"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:AttributeType name="CompanyName" rs:number="2" 
        rs:nullable="true" rs:write="true" rs:basetable="shippers" 
        rs:basecolumn="CompanyName"&gt; 
        &lt;s:datatype dt:type="string" dt:maxLength="40" /&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:AttributeType name="Phone" rs:number="3" rs:nullable="true" 
        rs:write="true" rs:basetable="shippers" 
        rs:basecolumn="Phone"&gt; 
        &lt;s:datatype dt:type="string" dt:maxLength="24"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:extends type="rs:rowbase"/&gt; 
    &lt;/s:ElementType&gt; 
  &lt;/s:Schema&gt; 

  &lt;rs:data&gt; 
    &lt;z:row ShipperID="1" CompanyName="Speedy Express" 
      Phone="(503) 555-9831"/&gt; 
    &lt;z:row ShipperID="2" CompanyName="United Package" 
      Phone="(503) 555-3199"/&gt; 
    &lt;z:row ShipperID="3" CompanyName="Federal Shipping" 
      Phone="(503) 555-9931"/&gt; 
  &lt;/rs:data&gt; 
&lt;/xml&gt;</code>
          <para>
            <caps:sentence id="src6" class="srcSentence">The schema shows the declarations of namespaces, the schema section, and the data section.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">Schema definitions conform to the <externalLink><linkText>W3C XML-Data specification</linkText><linkUri>http://www.w3.org/TR/1998/NOTE-XML-data/</linkUri></externalLink> and can be fully validated (though validation will not occur in Internet Explorer 5).</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> XML-Data is currently the only supported schema format for Recordset persistence.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">The data section has three rows containing information about shippers.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> For an empty rowset, the data section may be empty, but the &lt;rs:data&gt; tags must be present.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> With no data, you could write the tag shorthand as simply &lt;rs:data/&gt;.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
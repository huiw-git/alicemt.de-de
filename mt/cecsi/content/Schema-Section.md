---
title: "Schema Section"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4ac6e524-2c92-48e8-b871-0a4b5c8fda18
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
# Schema Section
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ec00c20534dc91f294e24ca4161b2124" id="tgt1" class="tgtSentence">The schema section is required.</caps:sentence>
          <caps:sentence sentenceid="fcf8bacdd110d0422091589ea2b6c707" id="tgt2" class="tgtSentence"> As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating.</caps:sentence>
          <caps:sentence sentenceid="0c5281c267c808b60c4fd4d08d9a797a" id="tgt3" class="tgtSentence"> However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong.</caps:sentence>
          <caps:sentence sentenceid="f232fc966884e8ac70beed28095ac194" id="tgt4" class="tgtSentence"> Here is an example of a minimal schema:</caps:sentence>
        </para>
        <code>&lt;xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"
    xmlns:rs="urn:schemas-microsoft-com:rowset"
    xmlns:z="#RowsetSchema"&gt;
  &lt;s:Schema id="RowsetSchema"&gt;
    &lt;s:ElementType name="row" content="eltOnly"&gt;
      &lt;s:AttributeType name="ShipperID"/&gt;
      &lt;s:AttributeType name="CompanyName"/&gt;
      &lt;s:AttributeType name="Phone"/&gt;
      &lt;s:Extends type="rs:rowbase"/&gt;
    &lt;/s:ElementType&gt;
  &lt;/s:Schema&gt;
  &lt;rs:data&gt;
...
  &lt;/rs:data&gt;
&lt;/xml&gt;</code>
        <para>
          <caps:sentence sentenceid="08302ecd4af35c27eec2c1ad3bba7bee" id="tgt5" class="tgtSentence">In the previous example, ADO will treat the data as variable length strings because no type information is included in the schema.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="1b83b92e317199db2a1ab684c6dd37d8" id="tgt6" class="tgtSentence">Creating Aliases for Column Names</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f441298005ea8543e6447b6d44eddd12" id="tgt7" class="tgtSentence">The rs:name attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section.</caps:sentence>
            <caps:sentence sentenceid="b49d2ddca09d4c1aefb35a66fc8aeafd" id="tgt8" class="tgtSentence"> For example, the previous schema could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</caps:sentence>
          </para>
          <code>&lt;s:Schema id="RowsetSchema"&gt; 
&lt;s:ElementType name="row" content="eltOnly" rs:updatable="true"&gt; 
&lt;s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...&gt; 
...
&lt;/s:AttributeType&gt; 
&lt;s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...&gt; 
...
&lt;/s:AttributeType&gt; 
&lt;s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...&gt; 
...
&lt;/s:AttributeType&gt; 
...
&lt;/s:ElementType&gt; 
&lt;/s:Schema&gt;</code>
          <para>
            <caps:sentence sentenceid="88d135e306cec7e7661ca7b08b84e053" id="tgt9" class="tgtSentence">Then, in the data section, the row would use the name attribute (not rs:name) to refer to that column:</caps:sentence>
          </para>
          <code>"&lt;row s1="1" s2="Speedy Express" s3="(503) 555-9831"/&gt;</code>
          <para>
            <caps:sentence sentenceid="6fdcbf27e582bd081cc3d08e5bca3ea4" id="tgt10" class="tgtSentence">Creating aliases for column names is required whenever a column name is not a valid attribute or tag name in XML.</caps:sentence>
            <caps:sentence sentenceid="b0bff6c131ba7a2302e90b6578d5d809" id="tgt11" class="tgtSentence"> For example, "LastName" must have an alias because names with embedded spaces are invalid attributes.</caps:sentence>
            <caps:sentence sentenceid="bae3693ae0652362c3a60814ec29f6f5" id="tgt12" class="tgtSentence"> The following line will not be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space.</caps:sentence>
          </para>
          <code>&lt;row last name="Jones"/&gt;</code>
          <para>
            <caps:sentence sentenceid="3d5ffedf89a16fd27af1b8b59d3dfd79" id="tgt13" class="tgtSentence">Whatever value you use for the name attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document.</caps:sentence>
            <caps:sentence sentenceid="1c46f63bc08c45acd5960435c6b39494" id="tgt14" class="tgtSentence"> The following example shows the consistent use of s1:</caps:sentence>
          </para>
          <code>&lt;s:Schema id="RowsetSchema"&gt;
  &lt;s:ElementType name="row" content="eltOnly"&gt;
    &lt;s:attribute type="s1"/&gt;
    &lt;s:attribute type="CompanyName"/&gt;
    &lt;s:attribute type="s3"/&gt;
    &lt;s:extends type="rs:rowbase"/&gt;
  &lt;/s:ElementType&gt;
  &lt;s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" 
    rs:maydefer="true" rs:writeunknown="true"&gt;
    &lt;s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10" 
      rs:fixedlength="true" rs:maybenull="true"/&gt;
  &lt;/s:AttributeType&gt;
&lt;/s:Schema&gt;
&lt;rs:data&gt;
  &lt;z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/&gt;
&lt;/rs:data&gt;</code>
          <para>
            <caps:sentence sentenceid="9d6484effd651546f7861b2131b12265" id="tgt15" class="tgtSentence">Similarly, because there is no alias defined for<codeInline> CompanyName </codeInline>in the previous example,<codeInline> CompanyName </codeInline>must be used consistently throughout the document.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f1b81df45c748eff5d4cb40e7d8a2c56" id="tgt16" class="tgtSentence">Data Types</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="175aec815c89948a25f98a299d14e780" id="tgt17" class="tgtSentence">You can apply a data type to a column with the dt:type attribute.</caps:sentence>
            <caps:sentence sentenceid="bbfd586cb6b69d3955d56aededcce079" id="tgt18" class="tgtSentence"> For the definitive guide to allowed XML types, see the Data Types section of the <externalLink><linkText>W3C XML-Data specification</linkText><linkUri>http://www.w3.org/TR/1998/NOTE-XML-data/</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="4ad3462f0be9cc7bed08e3d2efc08912" id="tgt19" class="tgtSentence"> You can specify a data type in two ways: either specify the dt:type attribute directly on the column definition itself or use the s:datatype construct as a nested element of the column definition.</caps:sentence>
            <caps:sentence sentenceid="2c802c1c3cc7a4e8d0693decfaa19694" id="tgt20" class="tgtSentence"> For example,</caps:sentence>
          </para>
          <code>&lt;s:AttributeType name="Phone" &gt;
  &lt;s:datatype dt:type="string"/&gt;
&lt;/s:AttributeType&gt;</code>
          <para>
            <caps:sentence sentenceid="a5e51c500779fb15f6c4851ad084a586" id="tgt21" class="tgtSentence">is equivalent to</caps:sentence>
          </para>
          <code>&lt;s:AttributeType name="Phone" dt:type="string"/&gt;</code>
          <para>
            <caps:sentence sentenceid="341fc37c4085db5fa220dd2c8dd5dca6" id="tgt22" class="tgtSentence">If you omit the dt:type attribute entirely from the row definition, by default, the column's type will be a variable length string.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dba72c2a88b129af899282e065805b37" id="tgt23" class="tgtSentence">If you have more type information than simply the type name (for example, dt:maxLength), it makes it more readable to use the s:datatype child element.</caps:sentence>
            <caps:sentence sentenceid="2623f98ee5b1ba6b1eae680ed89f2918" id="tgt24" class="tgtSentence"> This is merely a convention, however, and not a requirement.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="369c1d8de5f10f76874a591e979a5700" id="tgt25" class="tgtSentence">The following examples show further how to include type information in your schema.</caps:sentence>
          </para>
          <code>&lt;!-- 1. String with no max length --&gt;
&lt;s:AttributeType name="title_id"/&gt;
&lt;!—or --&gt;
&lt;s:AttributeType name="title_id" dt:type="string"/&gt;

&lt;!—- 2. Fixed length string with max length of 6 --&gt;
&lt;s:AttributeType name="title_id"&gt;
    &lt;s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /&gt;
&lt;/s:AttributeType&gt;

&lt;!—- 3. Variable length string with max length of 6 --&gt;
&lt;s:AttributeType name="title_id"&gt;
    &lt;s:datatype dt:type="string" dt:maxLength="6" /&gt;
&lt;/s:AttributeType&gt;

&lt;!—- 4. Integer --&gt;
&lt;s:AttributeType name="title_id" dt:type="int"/&gt;</code>
          <para>
            <caps:sentence sentenceid="27fa8639e7d3a5e849941a1272ac7860" id="tgt26" class="tgtSentence">There is a subtle use of the rs:fixedlength attribute in the second example.</caps:sentence>
            <caps:sentence sentenceid="542812fc0b3acb9fc12dca11741f2f79" id="tgt27" class="tgtSentence"> A column with the rs:fixedlength attribute set to true means that the data must have the length defined in the schema.</caps:sentence>
            <caps:sentence sentenceid="fb0a8d8098fae5643482ec03e7885c0d" id="tgt28" class="tgtSentence"> In this case, a valid value for title_id is "123456," as is "123   ."</caps:sentence>
            <caps:sentence sentenceid="7207b1bb08786d0e17f19d8a03f481ff" id="tgt29" class="tgtSentence"> However, "123" would not be valid because its length is 3, not 6.</caps:sentence>
            <caps:sentence sentenceid="c89ed87c9545e0c9df33e65d1ea36a1d" id="tgt30" class="tgtSentence"> See the OLE DB Programmer's Guide for a more complete description of the fixedlength property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="14b0942ea255caac3d692d1be85dd7bf" id="tgt31" class="tgtSentence">Handling Nulls</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f57c42069e86849d6ec8fc701ffdd692" id="tgt32" class="tgtSentence">Null values are handled by the rs:maybenull attribute.</caps:sentence>
            <caps:sentence sentenceid="2ca3e829a034fae80fb75123535bb231" id="tgt33" class="tgtSentence"> If this attribute is set to true, the contents of the column can contain a null value.</caps:sentence>
            <caps:sentence sentenceid="d6f93ae40536921fb87aab428748508c" id="tgt34" class="tgtSentence"> Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from IRowset::GetData().</caps:sentence>
            <caps:sentence sentenceid="03349b483955d74fa9a7690d3e0a93d0" id="tgt35" class="tgtSentence"> Consider the following column definitions from the Shippers table.</caps:sentence>
          </para>
          <code>&lt;s:AttributeType name="ShipperID"&gt;
  &lt;s:datatype dt:type="int" dt:maxLength="4"/&gt;
&lt;/s:AttributeType&gt;
&lt;s:AttributeType name="CompanyName"&gt;
  &lt;s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/&gt;
&lt;/s:AttributeType&gt;</code>
          <para>
            <caps:sentence sentenceid="ea147406ad7b4b45522f1ea826a1c555" id="tgt36" class="tgtSentence">The definition allows<codeInline> CompanyName </codeInline>to be null, but<codeInline> ShipperID </codeInline>cannot contain a null value.</caps:sentence>
            <caps:sentence sentenceid="7e5c9f112d2af0ba1f800452e51417e2" id="tgt37" class="tgtSentence"> If the data section contained the following row, the Persistence Provider would set the status of the data for the<codeInline> CompanyName </codeInline>column to the OLE DB status constant DBSTATUS_S_ISNULL:</caps:sentence>
          </para>
          <code>&lt;z:row ShipperID="1"/&gt;</code>
          <para>
            <caps:sentence sentenceid="1305fb194893832c8d36266827dc6231" id="tgt38" class="tgtSentence">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS_E_UNAVAILABLE for<codeInline> ShipperID </codeInline>and DBSTATUS_S_ISNULL for CompanyName.</caps:sentence>
          </para>
          <code>&lt;z:row/&gt; </code>
          <para>
            <caps:sentence sentenceid="1c509649e5f277610eaad34c8751a430" id="tgt39" class="tgtSentence">Note that a zero-length string is not the same as null.</caps:sentence>
          </para>
          <code>&lt;z:row ShipperID="1" CompanyName=""/&gt;</code>
          <para>
            <caps:sentence sentenceid="38cee80695b9db61aa4545469545e808" id="tgt40" class="tgtSentence">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS_S_OK for both columns.</caps:sentence>
            <caps:sentence sentenceid="04d25ae0bc227244136f71fef36ae5f4" id="tgt41" class="tgtSentence"> The<codeInline> CompanyName </codeInline>in this case is simply "" (a zero-length string).</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f19074272723ef32600c726a38ac5906" id="tgt42" class="tgtSentence">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The schema section is required.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Here is an example of a minimal schema:</caps:sentence>
        </para>
        <code>&lt;xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"
    xmlns:rs="urn:schemas-microsoft-com:rowset"
    xmlns:z="#RowsetSchema"&gt;
  &lt;s:Schema id="RowsetSchema"&gt;
    &lt;s:ElementType name="row" content="eltOnly"&gt;
      &lt;s:AttributeType name="ShipperID"/&gt;
      &lt;s:AttributeType name="CompanyName"/&gt;
      &lt;s:AttributeType name="Phone"/&gt;
      &lt;s:Extends type="rs:rowbase"/&gt;
    &lt;/s:ElementType&gt;
  &lt;/s:Schema&gt;
  &lt;rs:data&gt;
...
  &lt;/rs:data&gt;
&lt;/xml&gt;</code>
        <para>
          <caps:sentence id="src5" class="srcSentence">In the previous example, ADO will treat the data as variable length strings because no type information is included in the schema.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Creating Aliases for Column Names</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">The rs:name attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> For example, the previous schema could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</caps:sentence>
          </para>
          <code>&lt;s:Schema id="RowsetSchema"&gt; 
&lt;s:ElementType name="row" content="eltOnly" rs:updatable="true"&gt; 
&lt;s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...&gt; 
...
&lt;/s:AttributeType&gt; 
&lt;s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...&gt; 
...
&lt;/s:AttributeType&gt; 
&lt;s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...&gt; 
...
&lt;/s:AttributeType&gt; 
...
&lt;/s:ElementType&gt; 
&lt;/s:Schema&gt;</code>
          <para>
            <caps:sentence id="src9" class="srcSentence">Then, in the data section, the row would use the name attribute (not rs:name) to refer to that column:</caps:sentence>
          </para>
          <code>"&lt;row s1="1" s2="Speedy Express" s3="(503) 555-9831"/&gt;</code>
          <para>
            <caps:sentence id="src10" class="srcSentence">Creating aliases for column names is required whenever a column name is not a valid attribute or tag name in XML.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> For example, "LastName" must have an alias because names with embedded spaces are invalid attributes.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The following line will not be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space.</caps:sentence>
          </para>
          <code>&lt;row last name="Jones"/&gt;</code>
          <para>
            <caps:sentence id="src13" class="srcSentence">Whatever value you use for the name attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The following example shows the consistent use of s1:</caps:sentence>
          </para>
          <code>&lt;s:Schema id="RowsetSchema"&gt;
  &lt;s:ElementType name="row" content="eltOnly"&gt;
    &lt;s:attribute type="s1"/&gt;
    &lt;s:attribute type="CompanyName"/&gt;
    &lt;s:attribute type="s3"/&gt;
    &lt;s:extends type="rs:rowbase"/&gt;
  &lt;/s:ElementType&gt;
  &lt;s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" 
    rs:maydefer="true" rs:writeunknown="true"&gt;
    &lt;s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10" 
      rs:fixedlength="true" rs:maybenull="true"/&gt;
  &lt;/s:AttributeType&gt;
&lt;/s:Schema&gt;
&lt;rs:data&gt;
  &lt;z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/&gt;
&lt;/rs:data&gt;</code>
          <para>
            <caps:sentence id="src15" class="srcSentence">Similarly, because there is no alias defined for<codeInline> CompanyName </codeInline>in the previous example,<codeInline> CompanyName </codeInline>must be used consistently throughout the document.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Data Types</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">You can apply a data type to a column with the dt:type attribute.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> For the definitive guide to allowed XML types, see the Data Types section of the <externalLink><linkText>W3C XML-Data specification</linkText><linkUri>http://www.w3.org/TR/1998/NOTE-XML-data/</linkUri></externalLink>.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> You can specify a data type in two ways: either specify the dt:type attribute directly on the column definition itself or use the s:datatype construct as a nested element of the column definition.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> For example,</caps:sentence>
          </para>
          <code>&lt;s:AttributeType name="Phone" &gt;
  &lt;s:datatype dt:type="string"/&gt;
&lt;/s:AttributeType&gt;</code>
          <para>
            <caps:sentence id="src21" class="srcSentence">is equivalent to</caps:sentence>
          </para>
          <code>&lt;s:AttributeType name="Phone" dt:type="string"/&gt;</code>
          <para>
            <caps:sentence id="src22" class="srcSentence">If you omit the dt:type attribute entirely from the row definition, by default, the column's type will be a variable length string.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">If you have more type information than simply the type name (for example, dt:maxLength), it makes it more readable to use the s:datatype child element.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> This is merely a convention, however, and not a requirement.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">The following examples show further how to include type information in your schema.</caps:sentence>
          </para>
          <code>&lt;!-- 1. String with no max length --&gt;
&lt;s:AttributeType name="title_id"/&gt;
&lt;!—or --&gt;
&lt;s:AttributeType name="title_id" dt:type="string"/&gt;

&lt;!—- 2. Fixed length string with max length of 6 --&gt;
&lt;s:AttributeType name="title_id"&gt;
    &lt;s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /&gt;
&lt;/s:AttributeType&gt;

&lt;!—- 3. Variable length string with max length of 6 --&gt;
&lt;s:AttributeType name="title_id"&gt;
    &lt;s:datatype dt:type="string" dt:maxLength="6" /&gt;
&lt;/s:AttributeType&gt;

&lt;!—- 4. Integer --&gt;
&lt;s:AttributeType name="title_id" dt:type="int"/&gt;</code>
          <para>
            <caps:sentence id="src26" class="srcSentence">There is a subtle use of the rs:fixedlength attribute in the second example.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> A column with the rs:fixedlength attribute set to true means that the data must have the length defined in the schema.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> In this case, a valid value for title_id is "123456," as is "123   ."</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> However, "123" would not be valid because its length is 3, not 6.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> See the OLE DB Programmer's Guide for a more complete description of the fixedlength property.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src31" class="srcSentence">Handling Nulls</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src32" class="srcSentence">Null values are handled by the rs:maybenull attribute.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> If this attribute is set to true, the contents of the column can contain a null value.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from IRowset::GetData().</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> Consider the following column definitions from the Shippers table.</caps:sentence>
          </para>
          <code>&lt;s:AttributeType name="ShipperID"&gt;
  &lt;s:datatype dt:type="int" dt:maxLength="4"/&gt;
&lt;/s:AttributeType&gt;
&lt;s:AttributeType name="CompanyName"&gt;
  &lt;s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/&gt;
&lt;/s:AttributeType&gt;</code>
          <para>
            <caps:sentence id="src36" class="srcSentence">The definition allows<codeInline> CompanyName </codeInline>to be null, but<codeInline> ShipperID </codeInline>cannot contain a null value.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> If the data section contained the following row, the Persistence Provider would set the status of the data for the<codeInline> CompanyName </codeInline>column to the OLE DB status constant DBSTATUS_S_ISNULL:</caps:sentence>
          </para>
          <code>&lt;z:row ShipperID="1"/&gt;</code>
          <para>
            <caps:sentence id="src38" class="srcSentence">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS_E_UNAVAILABLE for<codeInline> ShipperID </codeInline>and DBSTATUS_S_ISNULL for CompanyName.</caps:sentence>
          </para>
          <code>&lt;z:row/&gt; </code>
          <para>
            <caps:sentence id="src39" class="srcSentence">Note that a zero-length string is not the same as null.</caps:sentence>
          </para>
          <code>&lt;z:row ShipperID="1" CompanyName=""/&gt;</code>
          <para>
            <caps:sentence id="src40" class="srcSentence">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS_S_OK for both columns.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> The<codeInline> CompanyName </codeInline>in this case is simply "" (a zero-length string).</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src42" class="srcSentence">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
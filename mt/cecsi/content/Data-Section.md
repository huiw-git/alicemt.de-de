---
title: "Data Section"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 43dc42a8-7057-48e6-93d6-880d5c5c51a4
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
# Data Section
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3e440c6fa40c260d5abbfe85fb1c77a8" id="tgt1" class="tgtSentence">The data section defines the data of the rowset along with any pending updates, insertions, or deletions.</caps:sentence>
          <caps:sentence sentenceid="7f3663afc99b99ac01c0cc72b95632ef" id="tgt2" class="tgtSentence"> The data section can contain zero or more rows.</caps:sentence>
          <caps:sentence sentenceid="ca532db45e2758884dfaa21268b74706" id="tgt3" class="tgtSentence"> It can only contain data from one rowset where the row is defined by the schema.</caps:sentence>
          <caps:sentence sentenceid="73d12b645c0fa9a716a4404fe7729a98" id="tgt4" class="tgtSentence"> Also, as noted before, columns without any data can be omitted.</caps:sentence>
          <caps:sentence sentenceid="dda9ca168a6558c9a4c3304b0051fc17" id="tgt5" class="tgtSentence"> If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt6" class="tgtSentence">String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f6b945888560749a34ec49fc5f0717bf" id="tgt7" class="tgtSentence">Reserved XML characters in text data must be replaced with appropriate character entities.</caps:sentence>
            <caps:sentence sentenceid="ca6145f967f5c0798c2ee06592be4de1" id="tgt8" class="tgtSentence"> For example, in the company name "Joe's Garage," the single quotation mark must be replaced by an entity.</caps:sentence>
            <caps:sentence sentenceid="61445382d8bf6a1d52bd0a102fa8a1ed" id="tgt9" class="tgtSentence"> The actual row would resemble the following:</caps:sentence>
          </para>
          <code>&lt;z:row CompanyName="Joe&amp;apos;s Garage"/&gt;</code>
          <para>
            <caps:sentence sentenceid="a61ac5a749f4c50ff550a6b85cc4055f" id="tgt10" class="tgtSentence">The following characters are reserved in XML and must be replaced by character entities: {',",&amp;,&lt;,&gt;}.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="9d7183f16acce70658f686ae7f1a4d20" id="tgt11" class="tgtSentence">Binary</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b734b427d5cb896340520c482994e01a" id="tgt12" class="tgtSentence">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="dfeaaeb4316477bd556ea5e8c3295887" id="tgt13" class="tgtSentence">DateTime</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a9b1e2181feb31be3fd8bd568fe0237d" id="tgt14" class="tgtSentence">The variant VT_DATE format is not directly supported by XML-Data data types.</caps:sentence>
            <caps:sentence sentenceid="d337f4be216818847a5bc54d2fae6ea8" id="tgt15" class="tgtSentence"> The correct format for dates with both a data and time component is yyyy-mm-ddThh:mm:ss.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="32c4d7961e6c85133d9f570af5916aa9" id="tgt16" class="tgtSentence">For more information about date formats specified by XML, see the <externalLink><linkText>W3C XML-Data specification</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=5692</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ac537ea2409793ea26eeac88aeb5a903" id="tgt17" class="tgtSentence">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="e3fa6b3699323de15abed08d52cc636d" id="tgt18" class="tgtSentence">Managing Pending Changes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e8fc45487efbbb83668a487004dd2c88" id="tgt19" class="tgtSentence">A Recordset can be opened in immediate or batch update mode.</caps:sentence>
            <caps:sentence sentenceid="c1faf15b6b747fbf484125e8445105b4" id="tgt20" class="tgtSentence"> When they are opened in batch update mode with client-side cursors, all changes made to the Recordset are in a pending state until the UpdateBatch method is called.</caps:sentence>
            <caps:sentence sentenceid="779fe20c9c5f5e985d59a4871ba435eb" id="tgt21" class="tgtSentence"> Pending changes are also persisted when the Recordset is saved.</caps:sentence>
            <caps:sentence sentenceid="b203c4714cb79d94b9be599a9eba9a84" id="tgt22" class="tgtSentence"> In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset.</caps:sentence>
            <caps:sentence sentenceid="5171a29f3011b9b86f2bfa3e403558a0" id="tgt23" class="tgtSentence"> In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row.</caps:sentence>
            <caps:sentence sentenceid="c8692aef729b28e280e730bbe334a537" id="tgt24" class="tgtSentence"> For example, to define that the Shippers table contains pending changes, the row definition would look resemble following.</caps:sentence>
          </para>
          <code>&lt;s:ElementType name="row" content="eltOnly" updatable="true"&gt;
  &lt;s:attribute type="ShipperID"/&gt;
  &lt;s:attribute type="CompanyName"/&gt;
  &lt;s:attribute type="Phone"/&gt;
  &lt;s:extends type="rs:rowbase"/&gt;
&lt;/s:ElementType&gt;</code>
          <para>
            <caps:sentence sentenceid="cb116115189ed5cbbf83bb8ba1582cff" id="tgt25" class="tgtSentence">This tells the Persistence Provider to surface data so that ADO can construct an updatable Recordset object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="73b4beb8dedc900a4fde8368d056aafe" id="tgt26" class="tgtSentence">The following sample data shows how insertions, changes, and deletions look in the persisted file.</caps:sentence>
          </para>
          <code>&lt;rs:data&gt;
  &lt;z:row ShipperID="2" CompanyName="United Package" 
    Phone="(503) 555-3199"/&gt;
&lt;rs:update&gt;
  &lt;rs:original&gt;
    &lt;z:row ShipperID="3" CompanyName="Federal Shipping" 
      Phone="(503) 555-9931"/&gt;
  &lt;/rs:original&gt;
  &lt;z:row Phone="(503) 552-7134"/&gt;
&lt;/rs:update&gt;
&lt;rs:insert&gt;
  &lt;z:row ShipperID="12" CompanyName="Lightning Shipping" 
    Phone="(505) 111-2222"/&gt;
  &lt;z:row ShipperID="13" CompanyName="Thunder Overnight" 
    Phone="(505) 111-2222"/&gt;
  &lt;z:row ShipperID="14" CompanyName="Blue Angel Air Delivery" 
    Phone="(505) 111-2222"/&gt;
&lt;/rs:insert&gt;
&lt;rs:delete&gt;
  &lt;z:row ShipperID="1" CompanyName="Speedy Express" Phone="(503) 555-9831"/&gt;
&lt;/rs:delete&gt;
&lt;/rs:data&gt;</code>
          <para>
            <caps:sentence sentenceid="510f60c10bbb36913c5e3fc3e39126a4" id="tgt27" class="tgtSentence">An update always contains the entire original row data followed by the changed row data.</caps:sentence>
            <caps:sentence sentenceid="81ebaf761417762c9d221d99e466f716" id="tgt28" class="tgtSentence"> The changed row may contain all the columns or only those columns that have actually changed.</caps:sentence>
            <caps:sentence sentenceid="2f3d0167a1f684d24a1e04c54cb70aa4" id="tgt29" class="tgtSentence"> In the previous example, the row for Shipper 2 is not changed, and only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row.</caps:sentence>
            <caps:sentence sentenceid="602b5aeb5cf31b8fe456e218b16f6154" id="tgt30" class="tgtSentence"> The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag.</caps:sentence>
            <caps:sentence sentenceid="cd17827415e5f2356627d4fcc072456a" id="tgt31" class="tgtSentence"> Note that deleted rows can also be batched together, although this is not shown in the previous example.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">The data section defines the data of the rowset along with any pending updates, insertions, or deletions.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The data section can contain zero or more rows.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> It can only contain data from one rowset where the row is defined by the schema.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Also, as noted before, columns without any data can be omitted.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">String</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">Reserved XML characters in text data must be replaced with appropriate character entities.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> For example, in the company name "Joe's Garage," the single quotation mark must be replaced by an entity.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The actual row would resemble the following:</caps:sentence>
          </para>
          <code>&lt;z:row CompanyName="Joe&amp;apos;s Garage"/&gt;</code>
          <para>
            <caps:sentence id="src10" class="srcSentence">The following characters are reserved in XML and must be replaced by character entities: {',",&amp;,&lt;,&gt;}.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Binary</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">DateTime</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">The variant VT_DATE format is not directly supported by XML-Data data types.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The correct format for dates with both a data and time component is yyyy-mm-ddThh:mm:ss.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">For more information about date formats specified by XML, see the <externalLink><linkText>W3C XML-Data specification</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=5692</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src18" class="srcSentence">Managing Pending Changes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src19" class="srcSentence">A Recordset can be opened in immediate or batch update mode.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> When they are opened in batch update mode with client-side cursors, all changes made to the Recordset are in a pending state until the UpdateBatch method is called.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> Pending changes are also persisted when the Recordset is saved.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> For example, to define that the Shippers table contains pending changes, the row definition would look resemble following.</caps:sentence>
          </para>
          <code>&lt;s:ElementType name="row" content="eltOnly" updatable="true"&gt;
  &lt;s:attribute type="ShipperID"/&gt;
  &lt;s:attribute type="CompanyName"/&gt;
  &lt;s:attribute type="Phone"/&gt;
  &lt;s:extends type="rs:rowbase"/&gt;
&lt;/s:ElementType&gt;</code>
          <para>
            <caps:sentence id="src25" class="srcSentence">This tells the Persistence Provider to surface data so that ADO can construct an updatable Recordset object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src26" class="srcSentence">The following sample data shows how insertions, changes, and deletions look in the persisted file.</caps:sentence>
          </para>
          <code>&lt;rs:data&gt;
  &lt;z:row ShipperID="2" CompanyName="United Package" 
    Phone="(503) 555-3199"/&gt;
&lt;rs:update&gt;
  &lt;rs:original&gt;
    &lt;z:row ShipperID="3" CompanyName="Federal Shipping" 
      Phone="(503) 555-9931"/&gt;
  &lt;/rs:original&gt;
  &lt;z:row Phone="(503) 552-7134"/&gt;
&lt;/rs:update&gt;
&lt;rs:insert&gt;
  &lt;z:row ShipperID="12" CompanyName="Lightning Shipping" 
    Phone="(505) 111-2222"/&gt;
  &lt;z:row ShipperID="13" CompanyName="Thunder Overnight" 
    Phone="(505) 111-2222"/&gt;
  &lt;z:row ShipperID="14" CompanyName="Blue Angel Air Delivery" 
    Phone="(505) 111-2222"/&gt;
&lt;/rs:insert&gt;
&lt;rs:delete&gt;
  &lt;z:row ShipperID="1" CompanyName="Speedy Express" Phone="(503) 555-9831"/&gt;
&lt;/rs:delete&gt;
&lt;/rs:data&gt;</code>
          <para>
            <caps:sentence id="src27" class="srcSentence">An update always contains the entire original row data followed by the changed row data.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> The changed row may contain all the columns or only those columns that have actually changed.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> In the previous example, the row for Shipper 2 is not changed, and only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> Note that deleted rows can also be batched together, although this is not shown in the previous example.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
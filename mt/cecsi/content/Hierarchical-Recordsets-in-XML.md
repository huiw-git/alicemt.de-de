---
title: "Hierarchical Recordsets in XML"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5d4b11c4-c94f-4910-b99b-5b9abc50d791
caps.latest.revision: 3
caps.handback.revision: 3
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
# Hierarchical Recordsets in XML
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2de9f37e7cbaf08645a86ad99a412037" id="tgt1" class="tgtSentence">ADO allows persistence of hierarchical Recordset objects into XML.</caps:sentence>
          <caps:sentence sentenceid="9065b44ec4117c462d07074658e63907" id="tgt2" class="tgtSentence"> With hierarchical Recordset objects, the value of a field in the parent Recordset is another Recordset.</caps:sentence>
          <caps:sentence sentenceid="bf745c3a5fcf63acd2387e1f87c09761" id="tgt3" class="tgtSentence"> Such fields are represented as child elements in the XML stream rather than an attribute.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt4" class="tgtSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7cd488f8d295f48e1f501a8a88d530a0" id="tgt5" class="tgtSentence">The following example demonstrates this case:</caps:sentence>
          </para>
          <code>Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;Integrated Security=SSPI;"</code>
          <para>
            <caps:sentence sentenceid="0e1ef1552c8b1d8bad39e3cef4a08e8b" id="tgt6" class="tgtSentence">The following is the XML format of the persisted Recordset:</caps:sentence>
          </para>
          <code>&lt;xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"&gt; 
  &lt;s:Schema id="RowsetSchema"&gt; 
    &lt;s:ElementType name="row" content="eltOnly" rs:updatable="true"&gt; 
      &lt;s:AttributeType name="stor_id" rs:number="1" 
        rs:writeunknown="true"&gt; 
        &lt;s:datatype dt:type="string" dt:maxLength="4" 
          rs:fixedlength="true" rs:maybenull="false"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:AttributeType name="stor_name" rs:number="2" rs:nullable="true" 
        rs:writeunknown="true"&gt; 
          &lt;s:datatype dt:type="string" dt:maxLength="40"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:AttributeType name="state" rs:number="3" rs:nullable="true" 
        rs:writeunknown="true"&gt; 
        &lt;s:datatype dt:type="string" dt:maxLength="2" 
          rs:fixedlength="true"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:ElementType name="rsSales" content="eltOnly" 
        rs:updatable="true" rs:relation="010000000100000000000000"&gt; 
        &lt;s:AttributeType name="stor_id" rs:number="1" 
          rs:writeunknown="true"&gt; 
          &lt;s:datatype dt:type="string" dt:maxLength="4" 
            rs:fixedlength="true" rs:maybenull="false"/&gt; 
        &lt;/s:AttributeType&gt; 
        &lt;s:AttributeType name="ord_num" rs:number="2" 
          rs:writeunknown="true"&gt; 
          &lt;s:datatype dt:type="string" dt:maxLength="20" 
            rs:maybenull="false"/&gt; 
        &lt;/s:AttributeType&gt; 
        &lt;s:AttributeType name="ord_date" rs:number="3" 
          rs:writeunknown="true"&gt; 
            &lt;s:datatype dt:type="dateTime" dt:maxLength="16" 
              rs:scale="3" rs:precision="23" rs:fixedlength="true" 
              rs:maybenull="false"/&gt; 
        &lt;/s:AttributeType&gt; 
        &lt;s:AttributeType name="qty" rs:number="4" rs:writeunknown="true"&gt; 
          &lt;s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5" 
            rs:fixedlength="true" rs:maybenull="false"/&gt; 
        &lt;/s:AttributeType&gt; 
        &lt;s:extends type="rs:rowbase"/&gt; 
      &lt;/s:ElementType&gt; 
      &lt;s:extends type="rs:rowbase"/&gt; 
    &lt;/s:ElementType&gt; 
  &lt;/s:Schema&gt; 
  &lt;rs:data&gt; 
    &lt;z:row stor_id="6380" stor_name="Eric the Read Books" state="WA"&gt; 
      &lt;rsSales stor_id="6380" ord_num="6871" 
        ord_date="1994-09-14T00:00:00" qty="5"/&gt; 
      &lt;rsSales stor_id="6380" ord_num="722a" 
        ord_date="1994-09-13T00:00:00" qty="3"/&gt; 
    &lt;/z:row&gt; 
    &lt;z:row stor_id="7066" stor_name="Barnum's" state="CA"&gt; 
      &lt;rsSales stor_id="7066" ord_num="A2976" 
        ord_date="1993-05-24T00:00:00" qty="50"/&gt; 
      &lt;rsSales stor_id="7066" ord_num="QA7442.3" 
        ord_date="1994-09-13T00:00:00" qty="75"/&gt; 
    &lt;/z:row&gt; 
    &lt;z:row stor_id="7067" stor_name="News &amp; Brews" state="CA"&gt; 
      &lt;rsSales stor_id="7067" ord_num="D4482" 
        ord_date="1994-09-14T00:00:00" qty="10"/&gt; 
      &lt;rsSales stor_id="7067" ord_num="P2121" 
        ord_date="1992-06-15T00:00:00" qty="40"/&gt; 
      &lt;rsSales stor_id="7067" ord_num="P2121" 
        ord_date="1992-06-15T00:00:00" qty="20"/&gt; 
      &lt;rsSales stor_id="7067" ord_num="P2121" 
        ord_date="1992-06-15T00:00:00" qty="20"/&gt; 
    &lt;/z:row&gt; 
  &lt;/rs:data&gt; 
&lt;/xml&gt; </code>
          <para>
            <caps:sentence sentenceid="190849eccf27ce833ad143963c586b05" id="tgt7" class="tgtSentence">The exact order of the columns in the parent Recordset is not obvious when it is persisted in this manner.</caps:sentence>
            <caps:sentence sentenceid="1b4d1ff734b65afa1c77746db11dbc15" id="tgt8" class="tgtSentence"> Any field in the parent may contain a child Recordset.</caps:sentence>
            <caps:sentence sentenceid="89c79e711057f1670edbddb7595f53f4" id="tgt9" class="tgtSentence"> The Persistence Provider persists out all scalar columns first as attributes and then persists out all child Recordset "columns" as child elements of the parent row.</caps:sentence>
            <caps:sentence sentenceid="6f69686a3abb19b234640fdc6c4498db" id="tgt10" class="tgtSentence"> The ordinal position of the field in the parent Recordset can be obtained by looking at the schema definition of the Recordset.</caps:sentence>
            <caps:sentence sentenceid="3288bf0090f1a5f0dfb32d46fb9d750f" id="tgt11" class="tgtSentence"> Every field has an OLE DB property, rs:number, defined in the Recordset schema namespace that contains the ordinal number for that field.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="838fb223574bffa9fb705279940fac82" id="tgt12" class="tgtSentence">The names of all fields in the child Recordset are concatenated with the name of the field in the parent Recordset that contains this child.</caps:sentence>
            <caps:sentence sentenceid="790b80a073be653b9414c8da7d05724a" id="tgt13" class="tgtSentence"> This is to ensure that there are no name collisions in cases where parent and child Recordsets both contain a field that is obtained from two different tables but is named singularly.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3c41d8ad2c4de0b4666c53e1e5700372" id="tgt14" class="tgtSentence">When saving hierarchical Recordsets into XML, you should be aware of the following restrictions in ADO: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="88b2ce67e2795b4c9409d7f66a74e08f" id="tgt15" class="tgtSentence">A hierarchical Recordset with pending updates cannot be persisted into XML.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="85b2a1df4db9bf588642aaaf158b36b3" id="tgt16" class="tgtSentence">A hierarchical Recordset created with a parameterized shape command cannot be persisted (in either XML or ADTG format).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6e793a9ce3fcbcc80b198abbb94d6cf1" id="tgt17" class="tgtSentence">ADO currently saves the relationship between the parent and the child Recordsets as a binary large object (BLOB).</caps:sentence>
                <caps:sentence sentenceid="72e535f1bae1fb83c79dfb1eca2249ba" id="tgt18" class="tgtSentence"> XML tags to describe this relationship have not yet been defined in the rowset schema namespace.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b4722928703dbd933ca97717b95a474e" id="tgt19" class="tgtSentence">When a hierarchical Recordset is saved, all child Recordsets are saved along with it.</caps:sentence>
                <caps:sentence sentenceid="291a5d3c0da115dc9d9aba3aa6b8b39e" id="tgt20" class="tgtSentence"> If the current Recordset is a child of another Recordset, its parent is not saved.</caps:sentence>
                <caps:sentence sentenceid="7749ec0724c83c3f6e0114f82ef5bb80" id="tgt21" class="tgtSentence"> All child Recordsets that form the subtree of the current Recordset are saved.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="0cb2abfcb1d591498d054072340dcba0" id="tgt22" class="tgtSentence">When a hierarchical Recordset is reopened from its XML-persisted format, you must be aware of the following limitations: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="70f0b4967b1c136fd7ef8d0da0f8047b" id="tgt23" class="tgtSentence">If the child record contains records for which there are no corresponding parent records, these rows are not written out in the XML representation of the hierarchical Recordset.</caps:sentence>
                <caps:sentence sentenceid="5b8c0044d8fa12555a31375a04af9637" id="tgt24" class="tgtSentence"> Thus, these rows will be lost when the Recordset is reopened from its persisted location.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="89d882909ea00f967df838f46ad8d1fd" id="tgt25" class="tgtSentence">If a child record has references to more than one parent record, then on reopening the Recordset, the child Recordset may contain duplicate records.</caps:sentence>
                <caps:sentence sentenceid="831d33c024abd08e168e323d2a129750" id="tgt26" class="tgtSentence"> However, these duplicates will only be visible if the user works directly with the underlying child rowset.</caps:sentence>
                <caps:sentence sentenceid="97d2b63d3015f2324d7ff7d95a40a827" id="tgt27" class="tgtSentence"> If a chapter is used to navigate the child Recordset (that is the only way to navigate through ADO), the duplicates are not visible.</caps:sentence>
              </para>
            </listItem>
          </list>
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
          <caps:sentence id="src1" class="srcSentence">ADO allows persistence of hierarchical Recordset objects into XML.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> With hierarchical Recordset objects, the value of a field in the parent Recordset is another Recordset.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Such fields are represented as child elements in the XML stream rather than an attribute.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The following example demonstrates this case:</caps:sentence>
          </para>
          <code>Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;Integrated Security=SSPI;"</code>
          <para>
            <caps:sentence id="src6" class="srcSentence">The following is the XML format of the persisted Recordset:</caps:sentence>
          </para>
          <code>&lt;xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"&gt; 
  &lt;s:Schema id="RowsetSchema"&gt; 
    &lt;s:ElementType name="row" content="eltOnly" rs:updatable="true"&gt; 
      &lt;s:AttributeType name="stor_id" rs:number="1" 
        rs:writeunknown="true"&gt; 
        &lt;s:datatype dt:type="string" dt:maxLength="4" 
          rs:fixedlength="true" rs:maybenull="false"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:AttributeType name="stor_name" rs:number="2" rs:nullable="true" 
        rs:writeunknown="true"&gt; 
          &lt;s:datatype dt:type="string" dt:maxLength="40"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:AttributeType name="state" rs:number="3" rs:nullable="true" 
        rs:writeunknown="true"&gt; 
        &lt;s:datatype dt:type="string" dt:maxLength="2" 
          rs:fixedlength="true"/&gt; 
      &lt;/s:AttributeType&gt; 
      &lt;s:ElementType name="rsSales" content="eltOnly" 
        rs:updatable="true" rs:relation="010000000100000000000000"&gt; 
        &lt;s:AttributeType name="stor_id" rs:number="1" 
          rs:writeunknown="true"&gt; 
          &lt;s:datatype dt:type="string" dt:maxLength="4" 
            rs:fixedlength="true" rs:maybenull="false"/&gt; 
        &lt;/s:AttributeType&gt; 
        &lt;s:AttributeType name="ord_num" rs:number="2" 
          rs:writeunknown="true"&gt; 
          &lt;s:datatype dt:type="string" dt:maxLength="20" 
            rs:maybenull="false"/&gt; 
        &lt;/s:AttributeType&gt; 
        &lt;s:AttributeType name="ord_date" rs:number="3" 
          rs:writeunknown="true"&gt; 
            &lt;s:datatype dt:type="dateTime" dt:maxLength="16" 
              rs:scale="3" rs:precision="23" rs:fixedlength="true" 
              rs:maybenull="false"/&gt; 
        &lt;/s:AttributeType&gt; 
        &lt;s:AttributeType name="qty" rs:number="4" rs:writeunknown="true"&gt; 
          &lt;s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5" 
            rs:fixedlength="true" rs:maybenull="false"/&gt; 
        &lt;/s:AttributeType&gt; 
        &lt;s:extends type="rs:rowbase"/&gt; 
      &lt;/s:ElementType&gt; 
      &lt;s:extends type="rs:rowbase"/&gt; 
    &lt;/s:ElementType&gt; 
  &lt;/s:Schema&gt; 
  &lt;rs:data&gt; 
    &lt;z:row stor_id="6380" stor_name="Eric the Read Books" state="WA"&gt; 
      &lt;rsSales stor_id="6380" ord_num="6871" 
        ord_date="1994-09-14T00:00:00" qty="5"/&gt; 
      &lt;rsSales stor_id="6380" ord_num="722a" 
        ord_date="1994-09-13T00:00:00" qty="3"/&gt; 
    &lt;/z:row&gt; 
    &lt;z:row stor_id="7066" stor_name="Barnum's" state="CA"&gt; 
      &lt;rsSales stor_id="7066" ord_num="A2976" 
        ord_date="1993-05-24T00:00:00" qty="50"/&gt; 
      &lt;rsSales stor_id="7066" ord_num="QA7442.3" 
        ord_date="1994-09-13T00:00:00" qty="75"/&gt; 
    &lt;/z:row&gt; 
    &lt;z:row stor_id="7067" stor_name="News &amp; Brews" state="CA"&gt; 
      &lt;rsSales stor_id="7067" ord_num="D4482" 
        ord_date="1994-09-14T00:00:00" qty="10"/&gt; 
      &lt;rsSales stor_id="7067" ord_num="P2121" 
        ord_date="1992-06-15T00:00:00" qty="40"/&gt; 
      &lt;rsSales stor_id="7067" ord_num="P2121" 
        ord_date="1992-06-15T00:00:00" qty="20"/&gt; 
      &lt;rsSales stor_id="7067" ord_num="P2121" 
        ord_date="1992-06-15T00:00:00" qty="20"/&gt; 
    &lt;/z:row&gt; 
  &lt;/rs:data&gt; 
&lt;/xml&gt; </code>
          <para>
            <caps:sentence id="src7" class="srcSentence">The exact order of the columns in the parent Recordset is not obvious when it is persisted in this manner.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Any field in the parent may contain a child Recordset.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The Persistence Provider persists out all scalar columns first as attributes and then persists out all child Recordset "columns" as child elements of the parent row.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The ordinal position of the field in the parent Recordset can be obtained by looking at the schema definition of the Recordset.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Every field has an OLE DB property, rs:number, defined in the Recordset schema namespace that contains the ordinal number for that field.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">The names of all fields in the child Recordset are concatenated with the name of the field in the parent Recordset that contains this child.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> This is to ensure that there are no name collisions in cases where parent and child Recordsets both contain a field that is obtained from two different tables but is named singularly.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">When saving hierarchical Recordsets into XML, you should be aware of the following restrictions in ADO: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">A hierarchical Recordset with pending updates cannot be persisted into XML.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">A hierarchical Recordset created with a parameterized shape command cannot be persisted (in either XML or ADTG format).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">ADO currently saves the relationship between the parent and the child Recordsets as a binary large object (BLOB).</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> XML tags to describe this relationship have not yet been defined in the rowset schema namespace.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">When a hierarchical Recordset is saved, all child Recordsets are saved along with it.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> If the current Recordset is a child of another Recordset, its parent is not saved.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> All child Recordsets that form the subtree of the current Recordset are saved.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src22" class="srcSentence">When a hierarchical Recordset is reopened from its XML-persisted format, you must be aware of the following limitations: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">If the child record contains records for which there are no corresponding parent records, these rows are not written out in the XML representation of the hierarchical Recordset.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> Thus, these rows will be lost when the Recordset is reopened from its persisted location.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src25" class="srcSentence">If a child record has references to more than one parent record, then on reopening the Recordset, the child Recordset may contain duplicate records.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> However, these duplicates will only be visible if the user works directly with the underlying child rowset.</caps:sentence>
                <caps:sentence id="src27" class="srcSentence"> If a chapter is used to navigate the child Recordset (that is the only way to navigate through ADO), the duplicates are not visible.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
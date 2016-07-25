---
title: "The Field Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7d1c4ad5-4be3-42ab-b516-e7133ca300bc
caps.latest.revision: 10
caps.handback.revision: 10
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
# The Field Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="02e571a8f8c16059e20c15d54e39c141" id="tgt1" class="tgtSentence">Each <legacyBold>Field</legacyBold> object usually corresponds to a column in a database table.</caps:sentence>
          <caps:sentence sentenceid="17664d98eb12b199e59173a5e4cd1f4d" id="tgt2" class="tgtSentence"> However, a <legacyBold>Field</legacyBold> can also represent a pointer to another <legacyBold>Recordset</legacyBold>, called a chapter.</caps:sentence>
          <caps:sentence sentenceid="d10e8ddfa944f14c3c17328df1550080" id="tgt3" class="tgtSentence"> Exceptions, such as chapter columns, will be covered later in this guide.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fc1b285c71bcd085fabf97ea7dd221a7" id="tgt4" class="tgtSentence">Use the <legacyBold>Value</legacyBold> property of <legacyBold>Field</legacyBold> objects to set or return data for the current record.</caps:sentence>
          <caps:sentence sentenceid="cea30ca340c7dbfaa14105c4c8348231" id="tgt5" class="tgtSentence"> Depending on the functionality the provider exposes, some collections, methods, or properties of a <legacyBold>Field</legacyBold> object may not be available.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="daa0ba3f25ebe97dd0e80c7f17e10704" id="tgt6" class="tgtSentence">With the collections, methods, and properties of a <legacyBold>Field</legacyBold> object, you can do the following:   </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="b17a87064af357be4ad7f3b40c07a2cc" id="tgt7" class="tgtSentence">Return the name of a field by using the <legacyBold>Name</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a67747728110b2d163e0508f326ab0ee" id="tgt8" class="tgtSentence">View or change the data in the field by using the <legacyBold>Value</legacyBold> property.</caps:sentence>
              <caps:sentence sentenceid="5f63de41a9838d59dd6fbe9a4eb96584" id="tgt9" class="tgtSentence">
                <legacyBold>Value </legacyBold>is the default property of the <legacyBold>Field</legacyBold> object.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="340027f527addbaed760029feb69b3df" id="tgt10" class="tgtSentence">Return the basic characteristics of a field by using the <legacyBold>Type</legacyBold>, <legacyBold>Precision</legacyBold>, and <legacyBold>NumericScale</legacyBold> properties.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="dff538cfecd8cb63d182e98485b6c0e9" id="tgt11" class="tgtSentence">Return the declared size of a field by using the <legacyBold>DefinedSize</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="018f1b0e58949cff75d0fcf15d11894d" id="tgt12" class="tgtSentence">Return the actual size of the data in a given field by using the <legacyBold>ActualSize</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="85b6a149cad4ce546c9051d68f94a8ac" id="tgt13" class="tgtSentence">Determine what types of functionality are supported for a given field by using the <legacyBold>Attributes</legacyBold> property and <legacyBold>Properties</legacyBold> collection.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="2f6caac09ed5f16a6dff4819fbe7e905" id="tgt14" class="tgtSentence">Manipulate the values of fields containing long binary or long character data by using the <legacyBold>AppendChunk</legacyBold> and <legacyBold>GetChunk</legacyBold> methods.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="14f7bf914464a7594fed07a8f9c3cf15" id="tgt15" class="tgtSentence">Resolve discrepancies in field values during batch updating by using the <legacyBold>OriginalValue</legacyBold> and <legacyBold>UnderlyingValue</legacyBold> properties, if the provider supports batch updates.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="37398d51f5d900d40b9696778179e493" id="tgt16" class="tgtSentence">Describing a Field</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7ca58d41b74be6a235a9372ea38f9c49" id="tgt17" class="tgtSentence">The topics that follow will discuss properties of the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object that represent information that describes the <legacyBold>Field</legacyBold> object itself — that is, metadata about the field.</caps:sentence>
            <caps:sentence sentenceid="0abc7f89974731af0ba5a76a5fa09870" id="tgt18" class="tgtSentence"> This information can be used to determine much about the schema of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="5d9166a0b94f4c2dca45f60fc2a84820" id="tgt19" class="tgtSentence"> These properties include <legacyBold>Type</legacyBold>, <legacyBold>DefinedSize</legacyBold> and <legacyBold>ActualSize</legacyBold>, <legacyBold>Name</legacyBold>, and <legacyBold>NumericScale</legacyBold> and <legacyBold>Precision</legacyBold>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="070a317b735730f973f2d86e80db1fea" id="tgt20" class="tgtSentence">Discovering the Data Type</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4b008ff81abe93f84a6f42b8b0907a94" id="tgt21" class="tgtSentence">The <legacyBold>Type</legacyBold> property indicates the data type of the field.</caps:sentence>
                <caps:sentence sentenceid="7fed94cc193840e265e3794c1b1a5a45" id="tgt22" class="tgtSentence"> The data type enumerated constants that are supported by ADO are described in <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> in the <legacyItalic>ADO Programmer's Reference</legacyItalic>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1d9f15332c5a1e86d95ae6a9fd520d67" id="tgt23" class="tgtSentence">For floating point numeric types such <legacyBold>adNumeric</legacyBold>, you can obtain more information.</caps:sentence>
                <caps:sentence sentenceid="24ceb41781fe2b7c2d7d4d870c13c7eb" id="tgt24" class="tgtSentence"> The <legacyBold>NumericScale</legacyBold> property indicates how many digits to the right of the decimal point will be used to represent values for the <legacyBold>Field</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="6bebc5cce37108889a049cfd7d830aa7" id="tgt25" class="tgtSentence"> The <legacyBold>Precision</legacyBold> property specifies the maximum number of digits used to represent values for the <legacyBold>Field</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="b36c30fcd6d10ddac34bbaf7d58ddacd" id="tgt26" class="tgtSentence">Determining Field Size</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="1553a9ef2a3b1a9808b9dee0ccd01e7a" id="tgt27" class="tgtSentence">Use the <legacyBold>DefinedSize</legacyBold> property to determine the data capacity of a <legacyBold>Field</legacyBold> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6afad7d449af1a2f59fdeb621de80980" id="tgt28" class="tgtSentence">Use the <legacyBold>ActualSize</legacyBold> property to return the actual length of a <legacyBold>Field</legacyBold> object's value.</caps:sentence>
                <caps:sentence sentenceid="53564252c1c08e7f138fab1e8bb68bc5" id="tgt29" class="tgtSentence"> For all fields, the <legacyBold>ActualSize</legacyBold> property is read-only.</caps:sentence>
                <caps:sentence sentenceid="79acffd43cc12809fad5b9d3cc4908db" id="tgt30" class="tgtSentence"> If ADO cannot determine the length of the <legacyBold>Field</legacyBold> object's value, the <legacyBold>ActualSize</legacyBold> property returns <legacyBold>adUnknown</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8c4e29e985fb55b9f481943ea0b6014b" id="tgt31" class="tgtSentence">The <legacyBold>DefinedSize</legacyBold> and <legacyBold>ActualSize</legacyBold> properties have different purposes.</caps:sentence>
                <caps:sentence sentenceid="6f8e8c8a23d66628ad06a306c54f5f08" id="tgt32" class="tgtSentence"> For example, consider a <legacyBold>Field</legacyBold> object with a declared type of <legacyBold>adVarChar</legacyBold> and a <legacyBold>DefinedSize</legacyBold> property value of 50, containing a single character.</caps:sentence>
                <caps:sentence sentenceid="a668c4e94d5d93752769725252c1fe10" id="tgt33" class="tgtSentence"> The <legacyBold>ActualSize</legacyBold> property value it returns is the length in bytes of the single character.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="3707293e602b74958528050c79392cad" id="tgt34" class="tgtSentence">Determining Field Contents</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2d9279ae8bd06600228cbad7f64ce896" id="tgt35" class="tgtSentence">The identifier of the column from the data source is represented by the <legacyBold>Name</legacyBold> property of the <legacyBold>Field</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="0e8f640110fa1d4d7c036499f584326a" id="tgt36" class="tgtSentence"> The <legacyBold>Value</legacyBold> property of the <legacyBold>Field</legacyBold> object returns or sets the actual data content of the field.</caps:sentence>
                <caps:sentence sentenceid="73020ad75e8fc55a59e4deb3d75f570d" id="tgt37" class="tgtSentence"> This is the default property.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="fb8f354a6e8090471311e6d6b84cad9c" id="tgt38" class="tgtSentence">To change the data in a field, set the <legacyBold>Value</legacyBold> property equal to a new value of the correct type.</caps:sentence>
                <caps:sentence sentenceid="bae6a992ce665b6e186d791639f7b2e0" id="tgt39" class="tgtSentence"> Your cursor type must support updates to change the contents of a field.</caps:sentence>
                <caps:sentence sentenceid="54965075a0d443f49e1a0c29de26e760" id="tgt40" class="tgtSentence"> Database validation is not done here in batch mode, so you will need to check for errors when you call <legacyBold>UpdateBatch</legacyBold> in such a case.</caps:sentence>
                <caps:sentence sentenceid="ca4b0d1b8ca159fcf06c183a86abd29e" id="tgt41" class="tgtSentence"> Some providers also support the ADO <legacyBold>Field</legacyBold> object's <legacyBold>UnderlyingValue</legacyBold> and <legacyBold>OriginalValue</legacyBold> properties to assist you with resolving conflicts when you attempt to perform batch updates.</caps:sentence>
                <caps:sentence sentenceid="d58e6ef84624b0e443edc1a8cabb6316" id="tgt42" class="tgtSentence"> For details about how to resolve such conflicts, see <legacyLink xlink:href="ef514f85-c446-4f05-824e-c9313b2ffae1">Editing Data</legacyLink>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="ac71756af10cc074a5547817eac86e6c" id="tgt43" class="tgtSentence">               <legacyBold>Recordset Field</legacyBold> values cannot be set when appending new <legacyBold>Fields</legacyBold> to a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="b2a6290220e3b07a6a8a2876a6a6be8b" id="tgt44" class="tgtSentence"> Rather, new <legacyBold>Fields</legacyBold> can be appended to a closed <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="d50f8a641053dbbdd821a7b4325cd21f" id="tgt45" class="tgtSentence"> Then the <legacyBold>Recordset</legacyBold> must be opened, and only then can values be assigned to these <legacyBold>Fields</legacyBold>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="e6322ba01bda59143d2c2db77e24f13b" id="tgt46" class="tgtSentence">Getting More Field Information</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9691608e01c3641684541802db4843fd" id="tgt47" class="tgtSentence">ADO objects have two types of properties: built-in and dynamic.</caps:sentence>
                <caps:sentence sentenceid="90a84249ed443d6cfbd8f391af613214" id="tgt48" class="tgtSentence"> To this point, only the built-in properties of the <legacyBold>Field</legacyBold> object have been discussed.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="34660eaf25649fab722283c2e26ac948" id="tgt49" class="tgtSentence">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the <codeInline>MyObject.Property</codeInline> syntax.</caps:sentence>
                <caps:sentence sentenceid="d93222387e6aac7438805a628b8c0324" id="tgt50" class="tgtSentence"> They do not appear as <legacyBold>Property</legacyBold> objects in an object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c6a5a17c8ed0eea2c0dfc3cb5a55fb16" id="tgt51" class="tgtSentence">Dynamic properties are defined by the underlying data provider, and appear in the <legacyBold>Properties</legacyBold> collection for the appropriate ADO object.</caps:sentence>
                <caps:sentence sentenceid="5b6748f6dc89f399723d61609965cdde" id="tgt52" class="tgtSentence"> For example, a property specific to the provider may indicate if a <legacyBold>Recordset</legacyBold> object supports transactions or updating.</caps:sentence>
                <caps:sentence sentenceid="3de59f7c76ea0128dfe3142d0b0fbe67" id="tgt53" class="tgtSentence"> These additional properties will appear as <legacyBold>Property</legacyBold> objects in that <legacyBold>Recordset</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
                <caps:sentence sentenceid="cfe98f4340bdecd020ef8b8e14b071d9" id="tgt54" class="tgtSentence"> Dynamic properties can be referenced only through the collection, using the syntax <codeInline>MyObject.Properties(0)</codeInline> or <codeInline>MyObject.Properties("Name")</codeInline>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1c08354a2624dc3b87b7587e5140890f" id="tgt55" class="tgtSentence">You cannot delete either kind of property.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="9f79968efba8f5645cc7369c2b8c2a2b" id="tgt56" class="tgtSentence">A dynamic <legacyBold>Property</legacyBold> object has four built-in properties of its own:   </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0100008be4965c99b977ee6a586d1544" id="tgt57" class="tgtSentence">The <legacyBold>Name</legacyBold> property is a string that identifies the property.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a4a0df0e9dd0983942bdf533df8140fa" id="tgt58" class="tgtSentence">The <legacyBold>Type</legacyBold> property is an integer that specifies the property data type.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="13d6f57816feaea1877d03d9adecd15d" id="tgt59" class="tgtSentence">The <legacyBold>Value</legacyBold> property is a variant that contains the property setting.</caps:sentence>
                    <caps:sentence sentenceid="fb7ddeaca01dd43d87d9fa5d494c6252" id="tgt60" class="tgtSentence">
                      <legacyBold>Value</legacyBold> is the default property for a <legacyBold>Property</legacyBold> object.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5cbbf3e06d111431ab8ebd1c4a3faddc" id="tgt61" class="tgtSentence">The <legacyBold>Attributes</legacyBold> property is a <legacyBold>Long</legacyBold> value that indicates characteristics of the property specific to the provider.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="d91dd8507ac8b1101d6dafce3f3692d7" id="tgt62" class="tgtSentence">The <legacyBold>Properties</legacyBold> collection for the <legacyBold>Field</legacyBold> object contains additional metadata about the field.</caps:sentence>
                <caps:sentence sentenceid="361846cb5bd887af5ec25e8aa72c7615" id="tgt63" class="tgtSentence"> The contents of this collection vary depending upon the provider.</caps:sentence>
                <caps:sentence sentenceid="66899a1ef29d7802da54c2ea0370d51b" id="tgt64" class="tgtSentence"> The following code example examines the <legacyBold>Properties</legacyBold> collection of the sample <legacyBold>Recordset</legacyBold> introduced at the beginning of this section.</caps:sentence>
                <caps:sentence sentenceid="f096e78e6fbbf3633c1f54be43899738" id="tgt65" class="tgtSentence"> It first looks at the contents of the collection.</caps:sentence>
                <caps:sentence sentenceid="017f116be8edf308b3ea1844fe3d740c" id="tgt66" class="tgtSentence"> This code uses the <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">OLE DB Provider for SQL Server</legacyLink>, so the <legacyBold>Properties</legacyBold> collection contains information relevant to that provider.</caps:sentence>
              </para>
              <code>'BeginFieldProps
    Dim objProp As ADODB.Property
        
    For intLoop = 0 To (objFields.Count - 1)
        Debug.Print objFields.Item(intLoop).Name
        
        For Each objProp In objFields(intLoop).Properties
            Debug.Print vbTab &amp; objProp.Name &amp; " = " &amp; objProp.Value
        Next objProp
    Next intLoop
'EndFieldProps</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="a6f1fa07defb0c2142035a6bb23bcd22" id="tgt67" class="tgtSentence">Dealing with Binary Data</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="922abc77546fb749343494e2ef1678da" id="tgt68" class="tgtSentence">Use the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk</legacyLink> method on a <legacyBold>Field</legacyBold> object to fill it with long binary or character data.</caps:sentence>
                <caps:sentence sentenceid="2fbfef4e15ec9f750332e8005a8dc252" id="tgt69" class="tgtSentence"> In situations where system memory is limited, you can use the <legacyBold>AppendChunk</legacyBold> method to manipulate long values in portions rather than in their entirety.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ee24646127cafaec5b2f9a4e4d39347e" id="tgt70" class="tgtSentence">If the <legacyBold>adFldLong</legacyBold> bit in the <legacyBold>Attributes</legacyBold> property of a <legacyBold>Field</legacyBold> object is set to <legacyBold>True</legacyBold>, you can use the <legacyBold>AppendChunk</legacyBold> method for that field.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="769ad6d156564a9e36ff2e274572b28b" id="tgt71" class="tgtSentence">The first <legacyBold>AppendChunk</legacyBold> call on a <legacyBold>Field</legacyBold> object writes data to the field, overwriting any existing data.</caps:sentence>
                <caps:sentence sentenceid="3e130bfb278cd230be5cb76246b8b5b1" id="tgt72" class="tgtSentence"> Subsequent <legacyBold>AppendChunk</legacyBold> calls add to existing data.</caps:sentence>
                <caps:sentence sentenceid="edf8d2ffe9dec91a719ecdac4374cd34" id="tgt73" class="tgtSentence"> If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field.</caps:sentence>
                <caps:sentence sentenceid="d42dd8e6b4f9eb8817236483d7146ab6" id="tgt74" class="tgtSentence"> If you call the <legacyBold>AppendChunk</legacyBold> method on the first field again, ADO interprets the call as a new <legacyBold>AppendChunk</legacyBold> operation and overwrites the existing data.</caps:sentence>
                <caps:sentence sentenceid="a8fc7283a222c1608b03530394fd932c" id="tgt75" class="tgtSentence"> Accessing fields in other <legacyBold>Recordset</legacyBold> objects that are not clones of the first <legacyBold>Recordset</legacyBold> object will not disrupt <legacyBold>AppendChunk</legacyBold> operations.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d13a151ae504adcaf03f47a66e098b26" id="tgt76" class="tgtSentence">Use the <legacyBold>GetChunk</legacyBold> method on a <legacyBold>Field</legacyBold> object to retrieve part or all of its long binary or character data.</caps:sentence>
                <caps:sentence sentenceid="c2cec76508ba4838295bbe3699ef99e5" id="tgt77" class="tgtSentence"> In situations where system memory is limited, you can use the <legacyBold>GetChunk</legacyBold> method to manipulate long values in portions, rather than in their entirety.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7b5bf03eb6b230837f8a7003148c36bf" id="tgt78" class="tgtSentence">The data that a <legacyBold>GetChunk</legacyBold> call returns is assigned to <legacyItalic>variable</legacyItalic>.</caps:sentence>
                <caps:sentence sentenceid="87c821fbfbed6d43eb38f1c1e26d5d91" id="tgt79" class="tgtSentence"> If <legacyItalic>Size</legacyItalic> is greater than the remaining data, the <legacyBold>GetChunk</legacyBold> method returns only the remaining data without padding <legacyItalic>variable</legacyItalic> with empty spaces.</caps:sentence>
                <caps:sentence sentenceid="1c42673677bcea79eea46cd595c540d4" id="tgt80" class="tgtSentence"> If the field is empty, the <legacyBold>GetChunk</legacyBold> method returns a null value.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="584c0f9e3872d656053a985a573b60b0" id="tgt81" class="tgtSentence">Each subsequent <legacyBold>GetChunk</legacyBold> call retrieves data starting from where the previous <legacyBold>GetChunk</legacyBold> call left off.</caps:sentence>
                <caps:sentence sentenceid="38a95dd2077194bee14142fbc7a88a40" id="tgt82" class="tgtSentence"> However, if you are retrieving data from one field and then set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</caps:sentence>
                <caps:sentence sentenceid="50355b5b661ddc153bd9e3999dde1685" id="tgt83" class="tgtSentence"> If you call the <legacyBold>GetChunk</legacyBold> method on the first field again, ADO interprets the call as a new <legacyBold>GetChunk</legacyBold> operation and starts reading from the beginning of the data.</caps:sentence>
                <caps:sentence sentenceid="294e8bbcd3430f81bd5a3902a00f3460" id="tgt84" class="tgtSentence"> Accessing fields in other <legacyBold>Recordset</legacyBold> objects that are not clones of the first <legacyBold>Recordset</legacyBold> object will not disrupt <legacyBold>GetChunk</legacyBold> operations.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="238f813f8250969f6d5caaccda236fb7" id="tgt85" class="tgtSentence">If the <legacyBold>adFldLong</legacyBold> bit in the <legacyBold>Attributes</legacyBold> property of a <legacyBold>Field</legacyBold> object is set to <legacyBold>True</legacyBold>, you can use the <legacyBold>GetChunk</legacyBold> method for that field.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7959697d5b765066171494b4075251a0" id="tgt86" class="tgtSentence">If there is no current record when you use the <legacyBold>GetChunk</legacyBold> or <legacyBold>AppendChunk</legacyBold> method on a <legacyBold>Field</legacyBold> object, error 3021 (no current record) occurs.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c006383b1acfcf50f63bb0fd923704f7" id="tgt87" class="tgtSentence">For an example of using these methods to manipulate binary data, see the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk Method</legacyLink> and <legacyLink xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk Method</legacyLink> examples in the <legacyItalic>ADO Programmer's Reference</legacyItalic>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Each <legacyBold>Field</legacyBold> object usually corresponds to a column in a database table.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> However, a <legacyBold>Field</legacyBold> can also represent a pointer to another <legacyBold>Recordset</legacyBold>, called a chapter.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Exceptions, such as chapter columns, will be covered later in this guide.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Value</legacyBold> property of <legacyBold>Field</legacyBold> objects to set or return data for the current record.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> Depending on the functionality the provider exposes, some collections, methods, or properties of a <legacyBold>Field</legacyBold> object may not be available.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">With the collections, methods, and properties of a <legacyBold>Field</legacyBold> object, you can do the following:   </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Return the name of a field by using the <legacyBold>Name</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">View or change the data in the field by using the <legacyBold>Value</legacyBold> property.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence">
                <legacyBold>Value </legacyBold>is the default property of the <legacyBold>Field</legacyBold> object.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Return the basic characteristics of a field by using the <legacyBold>Type</legacyBold>, <legacyBold>Precision</legacyBold>, and <legacyBold>NumericScale</legacyBold> properties.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Return the declared size of a field by using the <legacyBold>DefinedSize</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Return the actual size of the data in a given field by using the <legacyBold>ActualSize</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">Determine what types of functionality are supported for a given field by using the <legacyBold>Attributes</legacyBold> property and <legacyBold>Properties</legacyBold> collection.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">Manipulate the values of fields containing long binary or long character data by using the <legacyBold>AppendChunk</legacyBold> and <legacyBold>GetChunk</legacyBold> methods.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src15" class="srcSentence">Resolve discrepancies in field values during batch updating by using the <legacyBold>OriginalValue</legacyBold> and <legacyBold>UnderlyingValue</legacyBold> properties, if the provider supports batch updates.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Describing a Field</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">The topics that follow will discuss properties of the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object that represent information that describes the <legacyBold>Field</legacyBold> object itself — that is, metadata about the field.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> This information can be used to determine much about the schema of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> These properties include <legacyBold>Type</legacyBold>, <legacyBold>DefinedSize</legacyBold> and <legacyBold>ActualSize</legacyBold>, <legacyBold>Name</legacyBold>, and <legacyBold>NumericScale</legacyBold> and <legacyBold>Precision</legacyBold>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src20" class="srcSentence">Discovering the Data Type</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src21" class="srcSentence">The <legacyBold>Type</legacyBold> property indicates the data type of the field.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> The data type enumerated constants that are supported by ADO are described in <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> in the <legacyItalic>ADO Programmer's Reference</legacyItalic>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src23" class="srcSentence">For floating point numeric types such <legacyBold>adNumeric</legacyBold>, you can obtain more information.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> The <legacyBold>NumericScale</legacyBold> property indicates how many digits to the right of the decimal point will be used to represent values for the <legacyBold>Field</legacyBold>.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> The <legacyBold>Precision</legacyBold> property specifies the maximum number of digits used to represent values for the <legacyBold>Field</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src26" class="srcSentence">Determining Field Size</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src27" class="srcSentence">Use the <legacyBold>DefinedSize</legacyBold> property to determine the data capacity of a <legacyBold>Field</legacyBold> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src28" class="srcSentence">Use the <legacyBold>ActualSize</legacyBold> property to return the actual length of a <legacyBold>Field</legacyBold> object's value.</caps:sentence>
                <caps:sentence id="src29" class="srcSentence"> For all fields, the <legacyBold>ActualSize</legacyBold> property is read-only.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> If ADO cannot determine the length of the <legacyBold>Field</legacyBold> object's value, the <legacyBold>ActualSize</legacyBold> property returns <legacyBold>adUnknown</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src31" class="srcSentence">The <legacyBold>DefinedSize</legacyBold> and <legacyBold>ActualSize</legacyBold> properties have different purposes.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> For example, consider a <legacyBold>Field</legacyBold> object with a declared type of <legacyBold>adVarChar</legacyBold> and a <legacyBold>DefinedSize</legacyBold> property value of 50, containing a single character.</caps:sentence>
                <caps:sentence id="src33" class="srcSentence"> The <legacyBold>ActualSize</legacyBold> property value it returns is the length in bytes of the single character.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src34" class="srcSentence">Determining Field Contents</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src35" class="srcSentence">The identifier of the column from the data source is represented by the <legacyBold>Name</legacyBold> property of the <legacyBold>Field</legacyBold>.</caps:sentence>
                <caps:sentence id="src36" class="srcSentence"> The <legacyBold>Value</legacyBold> property of the <legacyBold>Field</legacyBold> object returns or sets the actual data content of the field.</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> This is the default property.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src38" class="srcSentence">To change the data in a field, set the <legacyBold>Value</legacyBold> property equal to a new value of the correct type.</caps:sentence>
                <caps:sentence id="src39" class="srcSentence"> Your cursor type must support updates to change the contents of a field.</caps:sentence>
                <caps:sentence id="src40" class="srcSentence"> Database validation is not done here in batch mode, so you will need to check for errors when you call <legacyBold>UpdateBatch</legacyBold> in such a case.</caps:sentence>
                <caps:sentence id="src41" class="srcSentence"> Some providers also support the ADO <legacyBold>Field</legacyBold> object's <legacyBold>UnderlyingValue</legacyBold> and <legacyBold>OriginalValue</legacyBold> properties to assist you with resolving conflicts when you attempt to perform batch updates.</caps:sentence>
                <caps:sentence id="src42" class="srcSentence"> For details about how to resolve such conflicts, see <legacyLink xlink:href="ef514f85-c446-4f05-824e-c9313b2ffae1">Editing Data</legacyLink>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src43" class="srcSentence">               <legacyBold>Recordset Field</legacyBold> values cannot be set when appending new <legacyBold>Fields</legacyBold> to a <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence id="src44" class="srcSentence"> Rather, new <legacyBold>Fields</legacyBold> can be appended to a closed <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  <caps:sentence id="src45" class="srcSentence"> Then the <legacyBold>Recordset</legacyBold> must be opened, and only then can values be assigned to these <legacyBold>Fields</legacyBold>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src46" class="srcSentence">Getting More Field Information</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src47" class="srcSentence">ADO objects have two types of properties: built-in and dynamic.</caps:sentence>
                <caps:sentence id="src48" class="srcSentence"> To this point, only the built-in properties of the <legacyBold>Field</legacyBold> object have been discussed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src49" class="srcSentence">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the <codeInline>MyObject.Property</codeInline> syntax.</caps:sentence>
                <caps:sentence id="src50" class="srcSentence"> They do not appear as <legacyBold>Property</legacyBold> objects in an object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src51" class="srcSentence">Dynamic properties are defined by the underlying data provider, and appear in the <legacyBold>Properties</legacyBold> collection for the appropriate ADO object.</caps:sentence>
                <caps:sentence id="src52" class="srcSentence"> For example, a property specific to the provider may indicate if a <legacyBold>Recordset</legacyBold> object supports transactions or updating.</caps:sentence>
                <caps:sentence id="src53" class="srcSentence"> These additional properties will appear as <legacyBold>Property</legacyBold> objects in that <legacyBold>Recordset</legacyBold> object's <legacyBold>Properties</legacyBold> collection.</caps:sentence>
                <caps:sentence id="src54" class="srcSentence"> Dynamic properties can be referenced only through the collection, using the syntax <codeInline>MyObject.Properties(0)</codeInline> or <codeInline>MyObject.Properties("Name")</codeInline>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src55" class="srcSentence">You cannot delete either kind of property.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src56" class="srcSentence">A dynamic <legacyBold>Property</legacyBold> object has four built-in properties of its own:   </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">The <legacyBold>Name</legacyBold> property is a string that identifies the property.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">The <legacyBold>Type</legacyBold> property is an integer that specifies the property data type.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">The <legacyBold>Value</legacyBold> property is a variant that contains the property setting.</caps:sentence>
                    <caps:sentence id="src60" class="srcSentence">
                      <legacyBold>Value</legacyBold> is the default property for a <legacyBold>Property</legacyBold> object.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">The <legacyBold>Attributes</legacyBold> property is a <legacyBold>Long</legacyBold> value that indicates characteristics of the property specific to the provider.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src62" class="srcSentence">The <legacyBold>Properties</legacyBold> collection for the <legacyBold>Field</legacyBold> object contains additional metadata about the field.</caps:sentence>
                <caps:sentence id="src63" class="srcSentence"> The contents of this collection vary depending upon the provider.</caps:sentence>
                <caps:sentence id="src64" class="srcSentence"> The following code example examines the <legacyBold>Properties</legacyBold> collection of the sample <legacyBold>Recordset</legacyBold> introduced at the beginning of this section.</caps:sentence>
                <caps:sentence id="src65" class="srcSentence"> It first looks at the contents of the collection.</caps:sentence>
                <caps:sentence id="src66" class="srcSentence"> This code uses the <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">OLE DB Provider for SQL Server</legacyLink>, so the <legacyBold>Properties</legacyBold> collection contains information relevant to that provider.</caps:sentence>
              </para>
              <code>'BeginFieldProps
    Dim objProp As ADODB.Property
        
    For intLoop = 0 To (objFields.Count - 1)
        Debug.Print objFields.Item(intLoop).Name
        
        For Each objProp In objFields(intLoop).Properties
            Debug.Print vbTab &amp; objProp.Name &amp; " = " &amp; objProp.Value
        Next objProp
    Next intLoop
'EndFieldProps</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src67" class="srcSentence">Dealing with Binary Data</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src68" class="srcSentence">Use the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk</legacyLink> method on a <legacyBold>Field</legacyBold> object to fill it with long binary or character data.</caps:sentence>
                <caps:sentence id="src69" class="srcSentence"> In situations where system memory is limited, you can use the <legacyBold>AppendChunk</legacyBold> method to manipulate long values in portions rather than in their entirety.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src70" class="srcSentence">If the <legacyBold>adFldLong</legacyBold> bit in the <legacyBold>Attributes</legacyBold> property of a <legacyBold>Field</legacyBold> object is set to <legacyBold>True</legacyBold>, you can use the <legacyBold>AppendChunk</legacyBold> method for that field.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src71" class="srcSentence">The first <legacyBold>AppendChunk</legacyBold> call on a <legacyBold>Field</legacyBold> object writes data to the field, overwriting any existing data.</caps:sentence>
                <caps:sentence id="src72" class="srcSentence"> Subsequent <legacyBold>AppendChunk</legacyBold> calls add to existing data.</caps:sentence>
                <caps:sentence id="src73" class="srcSentence"> If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field.</caps:sentence>
                <caps:sentence id="src74" class="srcSentence"> If you call the <legacyBold>AppendChunk</legacyBold> method on the first field again, ADO interprets the call as a new <legacyBold>AppendChunk</legacyBold> operation and overwrites the existing data.</caps:sentence>
                <caps:sentence id="src75" class="srcSentence"> Accessing fields in other <legacyBold>Recordset</legacyBold> objects that are not clones of the first <legacyBold>Recordset</legacyBold> object will not disrupt <legacyBold>AppendChunk</legacyBold> operations.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src76" class="srcSentence">Use the <legacyBold>GetChunk</legacyBold> method on a <legacyBold>Field</legacyBold> object to retrieve part or all of its long binary or character data.</caps:sentence>
                <caps:sentence id="src77" class="srcSentence"> In situations where system memory is limited, you can use the <legacyBold>GetChunk</legacyBold> method to manipulate long values in portions, rather than in their entirety.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src78" class="srcSentence">The data that a <legacyBold>GetChunk</legacyBold> call returns is assigned to <legacyItalic>variable</legacyItalic>.</caps:sentence>
                <caps:sentence id="src79" class="srcSentence"> If <legacyItalic>Size</legacyItalic> is greater than the remaining data, the <legacyBold>GetChunk</legacyBold> method returns only the remaining data without padding <legacyItalic>variable</legacyItalic> with empty spaces.</caps:sentence>
                <caps:sentence id="src80" class="srcSentence"> If the field is empty, the <legacyBold>GetChunk</legacyBold> method returns a null value.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src81" class="srcSentence">Each subsequent <legacyBold>GetChunk</legacyBold> call retrieves data starting from where the previous <legacyBold>GetChunk</legacyBold> call left off.</caps:sentence>
                <caps:sentence id="src82" class="srcSentence"> However, if you are retrieving data from one field and then set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</caps:sentence>
                <caps:sentence id="src83" class="srcSentence"> If you call the <legacyBold>GetChunk</legacyBold> method on the first field again, ADO interprets the call as a new <legacyBold>GetChunk</legacyBold> operation and starts reading from the beginning of the data.</caps:sentence>
                <caps:sentence id="src84" class="srcSentence"> Accessing fields in other <legacyBold>Recordset</legacyBold> objects that are not clones of the first <legacyBold>Recordset</legacyBold> object will not disrupt <legacyBold>GetChunk</legacyBold> operations.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src85" class="srcSentence">If the <legacyBold>adFldLong</legacyBold> bit in the <legacyBold>Attributes</legacyBold> property of a <legacyBold>Field</legacyBold> object is set to <legacyBold>True</legacyBold>, you can use the <legacyBold>GetChunk</legacyBold> method for that field.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src86" class="srcSentence">If there is no current record when you use the <legacyBold>GetChunk</legacyBold> or <legacyBold>AppendChunk</legacyBold> method on a <legacyBold>Field</legacyBold> object, error 3021 (no current record) occurs.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src87" class="srcSentence">For an example of using these methods to manipulate binary data, see the <legacyLink xlink:href="c648b5a8-d4f1-4d16-836e-3957feb03617">AppendChunk Method</legacyLink> and <legacyLink xlink:href="fc268e22-205b-44a3-9038-ffed51e23e10">GetChunk Method</legacyLink> examples in the <legacyItalic>ADO Programmer's Reference</legacyItalic>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Append Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: f8a9bbed-ba9c-4698-945d-317ad22d2e92
caps.latest.revision: 17
caps.handback.revision: 17
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
# Append Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="3ac349617bf6819d445c640413bb207f" id="tgt1" class="tgtSentence">Appends an object to a collection.</caps:sentence>
          <caps:sentence sentenceid="5ccbdcbea8d96abac2c8ffa7353faf74" id="tgt2" class="tgtSentence"> If the collection is <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink>, a new <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object can be created before it is appended to the collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
collection.Append object
fields.Append Name, Type, DefinedSize, Attrib, FieldValue</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="09ce078fb8e1b16f9dece31d57a0594d" id="tgt3" class="tgtSentence"> <legacyItalic>collection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="078e215cd2eb4b244f496a2d8d22b4c4" id="tgt4" class="tgtSentence">A collection object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8bddbd1d644449f57c976b7c137a00a3" id="tgt5" class="tgtSentence"> <legacyItalic>fields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="6ea063ff9a99e2c56626ea3366c6573c" id="tgt6" class="tgtSentence">A <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="7dac69667e814ea09c728e6d30f5074d" id="tgt7" class="tgtSentence"> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7609bf4e201a9aaada72b7eb2fd2afce" id="tgt8" class="tgtSentence">An object variable that represents the object to be appended.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="126d3eb305aa375299a9b5255f84a45f" id="tgt9" class="tgtSentence"> <legacyItalic>Name</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="1e900cc204336d7a246bb1846bfb8b0a" id="tgt10" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that contains the name of the new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object, and must not be the same name as any other object in <legacyItalic>fields</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="3d5db6fea3d2a41199d7bdbdc219501c" id="tgt11" class="tgtSentence"> <legacyItalic>Type</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="502125fdf5affad02ae221dec526156d" id="tgt12" class="tgtSentence">A <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> value, whose default value is <legacyBold>adEmpty</legacyBold>, that specifies the data type of the new field.</caps:sentence>
                <caps:sentence sentenceid="4d0f901423e83db20ff4abcb603e96d4" id="tgt13" class="tgtSentence"> The following data types are not supported by ADO, and should not be used when appending new fields to a <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object (ADO)</link>: <legacyBold>adIDispatch</legacyBold>, <legacyBold>adIUnknown</legacyBold>, <legacyBold>adVariant</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="272f969b8fb8cc4ebce4294679e5cb2f" id="tgt14" class="tgtSentence"> <legacyItalic>DefinedSize</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt15" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="d66f33785770605287114ea335c0d0dc" id="tgt16" class="tgtSentence"> A <languageKeyword>Long</languageKeyword> value that represents the defined size, in characters or bytes, of the new field.</caps:sentence>
                <caps:sentence sentenceid="1ae88eaab6652e7efe9a478042236768" id="tgt17" class="tgtSentence"> The default value for this parameter is derived from <parameterReference>Type</parameterReference>.</caps:sentence>
                <caps:sentence sentenceid="5c073caeea5baa9ca795fa9ac367abb9" id="tgt18" class="tgtSentence"> Fields that have a <parameterReference>DefinedSize</parameterReference> greater than 255 bytes are treated as variable length columns.</caps:sentence>
                <caps:sentence sentenceid="c66ff110864c560154efb3d8190e9ac5" id="tgt19" class="tgtSentence"> The default for <parameterReference>DefinedSize</parameterReference> is unspecified.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="02302442e30742710778cbc6720fc809" id="tgt20" class="tgtSentence"> <legacyItalic>Attrib</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt21" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="93e82bd83bd9c6e62d4f855641b2d1ab" id="tgt22" class="tgtSentence"> A <legacyLink xlink:href="6e34d886-005a-40dc-bd5c-6adcbf81e5cd">FieldAttributeEnum</legacyLink> value, whose default value is <legacyBold>adFldDefault</legacyBold>, that specifies attributes for the new field.</caps:sentence>
                <caps:sentence sentenceid="e2258b8cc49615afb62a000e78abcbcc" id="tgt23" class="tgtSentence"> If this value is not specified, the field will contain attributes derived from <parameterReference>Type</parameterReference>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="46185ae857261bc72c412a4589fde4aa" id="tgt24" class="tgtSentence"> <legacyItalic>FieldValue</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt25" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="7c6454a2f0ca9d84a9b4ceff265ca1b6" id="tgt26" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> that represents the value for the new field.</caps:sentence>
                <caps:sentence sentenceid="ec44f4de6f5696cb17e88799e6f7bf5b" id="tgt27" class="tgtSentence"> If not specified, the field is appended with a null value.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="7de80a224c6430583d8aa944e23154fb" id="tgt28" class="tgtSentence">Parameters Collection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="61ca891331e52f968e4d8b95e0176540" id="tgt29" class="tgtSentence">You must set the <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> property of a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object before appending it to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
                <caps:sentence sentenceid="cdb7da19e146349ca07188cb26068b4e" id="tgt30" class="tgtSentence"> If you select a variable-length data type, you must also set the <legacyLink xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size</legacyLink> property to a value greater than zero.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="29396ec8856165243786e461ff5d4797" id="tgt31" class="tgtSentence">Describing parameters yourself minimizes calls to the provider and therefore improves performance when you use stored procedures or parameterized queries.</caps:sentence>
                <caps:sentence sentenceid="93fff6f834c9aa1b4cffdf49fbc63ce5" id="tgt32" class="tgtSentence"> However, you must know the properties of the parameters associated with the stored procedure or parameterized query that you want to call.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="cd92b68b1eb3e5a479c02899ffc13ecd" id="tgt33" class="tgtSentence">Use the <legacyLink xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter</legacyLink> method to create <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> objects with the appropriate property settings and use the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method to add them to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
                <caps:sentence sentenceid="9bb341e4987a64222a1328d5860eead3" id="tgt34" class="tgtSentence"> This lets you set and return parameter values without having to call the provider for the parameter information.</caps:sentence>
                <caps:sentence sentenceid="c14c59e77d0776eb9203039f72b1f919" id="tgt35" class="tgtSentence"> If you are writing to a provider that does not supply parameter information, you must use this method to manually populate the <unmanagedCodeEntityReference>Parameters</unmanagedCodeEntityReference> collection in order to use parameters at all.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="674ea0184650cb95a2fb260332db2e00" id="tgt36" class="tgtSentence">Fields Collection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="09dca03584313327df9e47f31920449c" id="tgt37" class="tgtSentence">The <legacyItalic>FieldValue</legacyItalic> parameter is only valid when adding a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object to a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, not to a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
                <caps:sentence sentenceid="383bade8f2923ac4d18561b58253f04e" id="tgt38" class="tgtSentence"> With a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object, you can append fields and provide values at the same time.</caps:sentence>
                <caps:sentence sentenceid="5721ee0349159f3948fc8481b559ef29" id="tgt39" class="tgtSentence"> With a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, you must create fields while the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is closed, and then open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> and assign values to the fields.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="0ed7414580d26e483bf8c6f7d1d333bb" id="tgt40" class="tgtSentence">For new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects that have been appended to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object, the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property must be set before any other <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> properties can be specified.</caps:sentence>
                  <caps:sentence sentenceid="418b7b05c5a0d2fea9db660057e96537" id="tgt41" class="tgtSentence"> First, a specific value for the <unmanagedCodeEntityReference>Value</unmanagedCodeEntityReference> property must have been assigned and <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> on the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection called.</caps:sentence>
                  <caps:sentence sentenceid="7de5d83ef3be56f8b1667f4cd105e1ba" id="tgt42" class="tgtSentence"> Then, other properties such as <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> or <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> can be accessed.</caps:sentence>
                  <caps:sentence sentenceid="f0d509d742fa1d567c5cb0f25ab467dd" id="tgt43" class="tgtSentence">
                    <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects of the following data types (<legacyBold>DataTypeEnum</legacyBold>) cannot be appended to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection and will cause an error to occur: <legacyBold>adArray</legacyBold>, <legacyBold>adChapter</legacyBold>, <legacyBold>adEmpty</legacyBold>, <legacyBold>adPropVariant</legacyBold>, and <legacyBold>adUserDefined</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="ccf8efda0c50d704545f9f63544fc485" id="tgt44" class="tgtSentence"> Also, the following data types are not supported by ADO: <legacyBold>adIDispatch</legacyBold>, <legacyBold>adIUnknown</legacyBold>, and <legacyBold>adIVariant</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="951bfe17050e94e19728dee5dff7e34c" id="tgt45" class="tgtSentence"> For these types, no error will occur when appended, but usage can produce unpredictable results including memory leaks.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="c1e71ce69bff36c1582c5f180ea9a4ff" id="tgt46" class="tgtSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ec912175cfd476de9e64ecca03789cdf" id="tgt47" class="tgtSentence">If you do not set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property before calling the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method, <unmanagedCodeEntityReference>CursorLocation</unmanagedCodeEntityReference> will be set to <legacyBold>adUseClient</legacyBold> (a <legacyLink xlink:href="acb255ff-1734-4b70-89bb-aef862b4c63b">CursorLocationEnum</legacyLink> value) automatically when the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object is called.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4231d62d12aa963039a1696c8f5bfaa3" id="tgt48" class="tgtSentence">A run-time error will occur if the <unmanagedCodeEntityReference>Append </unmanagedCodeEntityReference>method is called on the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of an open <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, or on a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> where the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property has been set.</caps:sentence>
                <caps:sentence sentenceid="e215c3a9e82867717e44e50c46e3b489" id="tgt49" class="tgtSentence"> You can only append fields to a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> that is not open and has not yet been connected to a data source.</caps:sentence>
                <caps:sentence sentenceid="80fff89d6e7241e7de7ad65b17fa2718" id="tgt50" class="tgtSentence"> This is typically the case when a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is fabricated with the <legacyLink xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset</legacyLink> method or assigned to an object variable.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="de17f0f24b49f8364187891f8550ffbb" id="tgt51" class="tgtSentence">Record</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9c29188a7370297ea55e481299a49629" id="tgt52" class="tgtSentence">A run-time error will not occur if the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method is called on the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of an open <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference>.</caps:sentence>
                <caps:sentence sentenceid="f91a0f4b8cf2ccbdb1962c84aebfa619" id="tgt53" class="tgtSentence"> The new field will be added to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object.</caps:sentence>
                <caps:sentence sentenceid="a48d2e0299a53c102de429147fc4fe21" id="tgt54" class="tgtSentence"> If the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> was derived from a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, the new field will not appear in the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5bf48df1105cc27d80925757f45c6c8e" id="tgt55" class="tgtSentence">A non-existent field can be created and appended to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection by assigning a value to the field object as if it already existed in the collection.</caps:sentence>
                <caps:sentence sentenceid="f92f618e7a75525f01c77d7d8eb9ed6f" id="tgt56" class="tgtSentence"> The assignment will trigger the automatic creation and appending of the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object, and then the assignment will be completed.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="f5f5c346d0bbf7ad9aa0f167a23ca764" id="tgt57" class="tgtSentence">After appending a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object, call the <unmanagedCodeEntityReference>Update</unmanagedCodeEntityReference> method of the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection to save the change.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt58" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="46908cbd-434f-43e7-a794-ed0be0e0c0a7">Visual Basic Example</link>
        <link xlink:href="b57d144c-0a34-49c8-94cf-e5981edfcca6">Visual C++ Example</link>
        <link xlink:href="9673f232-fa58-4439-995a-b4066db628aa">Visual J++ Example</link>
        <link xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter Method</link>
        <link xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">Delete Method (ADO Fields Collection)</link>
        <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Appends an object to a collection.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> If the collection is <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink>, a new <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object can be created before it is appended to the collection.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
collection.Append object
fields.Append Name, Type, DefinedSize, Attrib, FieldValue</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>collection</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A collection object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>fields</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>object</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">An object variable that represents the object to be appended.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <legacyItalic>Name</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">A <languageKeyword>String</languageKeyword> value that contains the name of the new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object, and must not be the same name as any other object in <legacyItalic>fields</legacyItalic>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src11" class="srcSentence"> <legacyItalic>Type</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src12" class="srcSentence">A <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> value, whose default value is <legacyBold>adEmpty</legacyBold>, that specifies the data type of the new field.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> The following data types are not supported by ADO, and should not be used when appending new fields to a <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object (ADO)</link>: <legacyBold>adIDispatch</legacyBold>, <legacyBold>adIUnknown</legacyBold>, <legacyBold>adVariant</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src14" class="srcSentence"> <legacyItalic>DefinedSize</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src15" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> A <languageKeyword>Long</languageKeyword> value that represents the defined size, in characters or bytes, of the new field.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> The default value for this parameter is derived from <parameterReference>Type</parameterReference>.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> Fields that have a <parameterReference>DefinedSize</parameterReference> greater than 255 bytes are treated as variable length columns.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> The default for <parameterReference>DefinedSize</parameterReference> is unspecified.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src20" class="srcSentence"> <legacyItalic>Attrib</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src21" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> A <legacyLink xlink:href="6e34d886-005a-40dc-bd5c-6adcbf81e5cd">FieldAttributeEnum</legacyLink> value, whose default value is <legacyBold>adFldDefault</legacyBold>, that specifies attributes for the new field.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> If this value is not specified, the field will contain attributes derived from <parameterReference>Type</parameterReference>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src24" class="srcSentence"> <legacyItalic>FieldValue</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src25" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> that represents the value for the new field.</caps:sentence>
                <caps:sentence id="src27" class="srcSentence"> If not specified, the field is appended with a null value.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src28" class="srcSentence">Parameters Collection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src29" class="srcSentence">You must set the <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> property of a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object before appending it to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> If you select a variable-length data type, you must also set the <legacyLink xlink:href="e6bad449-ebdb-4dd3-886a-9e6f1e7ee5d2">Size</legacyLink> property to a value greater than zero.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src31" class="srcSentence">Describing parameters yourself minimizes calls to the provider and therefore improves performance when you use stored procedures or parameterized queries.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> However, you must know the properties of the parameters associated with the stored procedure or parameterized query that you want to call.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src33" class="srcSentence">Use the <legacyLink xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter</legacyLink> method to create <unmanagedCodeEntityReference>Parameter</unmanagedCodeEntityReference> objects with the appropriate property settings and use the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method to add them to the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection.</caps:sentence>
                <caps:sentence id="src34" class="srcSentence"> This lets you set and return parameter values without having to call the provider for the parameter information.</caps:sentence>
                <caps:sentence id="src35" class="srcSentence"> If you are writing to a provider that does not supply parameter information, you must use this method to manually populate the <unmanagedCodeEntityReference>Parameters</unmanagedCodeEntityReference> collection in order to use parameters at all.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src36" class="srcSentence">Fields Collection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src37" class="srcSentence">The <legacyItalic>FieldValue</legacyItalic> parameter is only valid when adding a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object to a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object, not to a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
                <caps:sentence id="src38" class="srcSentence"> With a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object, you can append fields and provide values at the same time.</caps:sentence>
                <caps:sentence id="src39" class="srcSentence"> With a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, you must create fields while the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> is closed, and then open the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> and assign values to the fields.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src40" class="srcSentence">For new <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects that have been appended to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object, the <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property must be set before any other <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> properties can be specified.</caps:sentence>
                  <caps:sentence id="src41" class="srcSentence"> First, a specific value for the <unmanagedCodeEntityReference>Value</unmanagedCodeEntityReference> property must have been assigned and <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> on the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection called.</caps:sentence>
                  <caps:sentence id="src42" class="srcSentence"> Then, other properties such as <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> or <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> can be accessed.</caps:sentence>
                  <caps:sentence id="src43" class="srcSentence">
                    <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> objects of the following data types (<legacyBold>DataTypeEnum</legacyBold>) cannot be appended to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection and will cause an error to occur: <legacyBold>adArray</legacyBold>, <legacyBold>adChapter</legacyBold>, <legacyBold>adEmpty</legacyBold>, <legacyBold>adPropVariant</legacyBold>, and <legacyBold>adUserDefined</legacyBold>.</caps:sentence>
                  <caps:sentence id="src44" class="srcSentence"> Also, the following data types are not supported by ADO: <legacyBold>adIDispatch</legacyBold>, <legacyBold>adIUnknown</legacyBold>, and <legacyBold>adIVariant</legacyBold>.</caps:sentence>
                  <caps:sentence id="src45" class="srcSentence"> For these types, no error will occur when appended, but usage can produce unpredictable results including memory leaks.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src46" class="srcSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src47" class="srcSentence">If you do not set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property before calling the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method, <unmanagedCodeEntityReference>CursorLocation</unmanagedCodeEntityReference> will be set to <legacyBold>adUseClient</legacyBold> (a <legacyLink xlink:href="acb255ff-1734-4b70-89bb-aef862b4c63b">CursorLocationEnum</legacyLink> value) automatically when the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method of the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object is called.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src48" class="srcSentence">A run-time error will occur if the <unmanagedCodeEntityReference>Append </unmanagedCodeEntityReference>method is called on the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of an open <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, or on a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> where the <legacyLink xlink:href="52d0a96c-14fb-4ad9-b004-4d821bc0a6db">ActiveConnection</legacyLink> property has been set.</caps:sentence>
                <caps:sentence id="src49" class="srcSentence"> You can only append fields to a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> that is not open and has not yet been connected to a data source.</caps:sentence>
                <caps:sentence id="src50" class="srcSentence"> This is typically the case when a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object is fabricated with the <legacyLink xlink:href="6840b1e5-c04d-4d3e-9dcc-42128c83492f">CreateRecordset</legacyLink> method or assigned to an object variable.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src51" class="srcSentence">Record</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src52" class="srcSentence">A run-time error will not occur if the <unmanagedCodeEntityReference>Append</unmanagedCodeEntityReference> method is called on the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of an open <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference>.</caps:sentence>
                <caps:sentence id="src53" class="srcSentence"> The new field will be added to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object.</caps:sentence>
                <caps:sentence id="src54" class="srcSentence"> If the <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> was derived from a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>, the new field will not appear in the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src55" class="srcSentence">A non-existent field can be created and appended to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection by assigning a value to the field object as if it already existed in the collection.</caps:sentence>
                <caps:sentence id="src56" class="srcSentence"> The assignment will trigger the automatic creation and appending of the <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> object, and then the assignment will be completed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src57" class="srcSentence">After appending a <unmanagedCodeEntityReference>Field</unmanagedCodeEntityReference> to the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection of a <unmanagedCodeEntityReference>Record</unmanagedCodeEntityReference> object, call the <unmanagedCodeEntityReference>Update</unmanagedCodeEntityReference> method of the <unmanagedCodeEntityReference>Fields</unmanagedCodeEntityReference> collection to save the change.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src58" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="46908cbd-434f-43e7-a794-ed0be0e0c0a7">Visual Basic Example</link>
        <link xlink:href="b57d144c-0a34-49c8-94cf-e5981edfcca6">Visual C++ Example</link>
        <link xlink:href="9673f232-fa58-4439-995a-b4066db628aa">Visual J++ Example</link>
        <link xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter Method</link>
        <link xlink:href="25bedc25-c51c-4cab-96ce-930b959965d9">Delete Method (ADO Fields Collection)</link>
        <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
        <link xlink:href="1eb9209c-602c-4507-b0c2-6527a599b67d">Delete Method (ADO Recordset)</link>
        <link xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
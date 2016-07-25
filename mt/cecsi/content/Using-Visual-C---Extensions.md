---
title: "Using Visual C++ Extensions"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ff759185-df41-4507-8d12-0921894ffbd9
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
# Using Visual C++ Extensions
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="81a8f45e7af3403d7a1a22bd6e72a035" id="tgt1" class="tgtSentence">The IADORecordBinding Interface</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f5fc96459be4cdce87971d85f3a1cc98" id="tgt2" class="tgtSentence">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object to C/C++ variables.</caps:sentence>
            <caps:sentence sentenceid="4027a0c34edd7fd05e75d3f52692d999" id="tgt3" class="tgtSentence"> Whenever the current row of the bound <legacyBold>Recordset</legacyBold> changes, all the bound fields in the <legacyBold>Recordset</legacyBold> are copied to the C/C++ variables.</caps:sentence>
            <caps:sentence sentenceid="6b2ddb1d06b5226c9241d95cfe4ec1c9" id="tgt4" class="tgtSentence"> If necessary, the copied data is converted to the declared data type of the C/C++ variable.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c9b1a37c152f62eb3b6b07bd87dc272e" id="tgt5" class="tgtSentence">The <legacyBold>BindToRecordset</legacyBold> method of the <legacyBold>IADORecordBinding</legacyBold> interface binds fields to C/C++ variables.</caps:sentence>
            <caps:sentence sentenceid="4607594e27e6cdb4e8a144422fc3b1c0" id="tgt6" class="tgtSentence"> The <legacyBold>AddNew</legacyBold> method adds a new row to the bound <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="f6fa6cea45b1130c168ac63795511e05" id="tgt7" class="tgtSentence"> The <legacyBold>Update</legacyBold> method populates fields in new rows of the <legacyBold>Recordset</legacyBold>, or updates fields in existing rows, with the value of the C/C++ variables.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f12440910ef530ac677be477daefa52b" id="tgt8" class="tgtSentence">The <legacyBold>IADORecordBinding</legacyBold> interface is implemented by the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="059f1e858a2b682718a1235b64d79c5c" id="tgt9" class="tgtSentence"> You do not code the implementation yourself.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c452f811f8a5d3b29a59a8776000d493" id="tgt10" class="tgtSentence">Binding Entries</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bfa7db0dd6e3c56c451065cd45d4dd35" id="tgt11" class="tgtSentence">The Visual C++ Extensions for ADO map fields of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object to C/C++ variables.</caps:sentence>
            <caps:sentence sentenceid="fe15306579babce8b4debbcfeeb31606" id="tgt12" class="tgtSentence"> The definition of a mapping between a field and a variable is called a <legacyItalic>binding entry</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="a31ed13ba14069e119c58f02178fd22d" id="tgt13" class="tgtSentence"> Macros provide binding entries for numeric, fixed-length, and variable-length data.</caps:sentence>
            <caps:sentence sentenceid="07a0b747358f0cdac4b7b5f638f94af6" id="tgt14" class="tgtSentence"> The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, <legacyBold>CADORecordBinding</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="c0ab0ae7da03c590fa4ba2b785b32f0b" id="tgt15" class="tgtSentence"> The <legacyBold>CADORecordBinding</legacyBold> class is defined internally by the binding entry macros.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ce1b402c684ef280dc9cd269e36bd222" id="tgt16" class="tgtSentence">ADO internally maps the parameters in these macros to an OLE DB <legacyBold>DBBINDING</legacyBold> structure and creates an OLE DB <legacyBold>Accessor</legacyBold> object to manage the movement and conversion of data between fields and variables.</caps:sentence>
            <caps:sentence sentenceid="f7b3d76a91bc1712e39f29b6dfda2997" id="tgt17" class="tgtSentence"> OLE DB defines data as consisting of three parts: A <legacyItalic>buffer</legacyItalic> where the data is stored; a <legacyItalic>status</legacyItalic> that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the <legacyItalic>length</legacyItalic> of the data.</caps:sentence>
            <caps:sentence sentenceid="1e4d49944257d472be1a42fe8a2af004" id="tgt18" class="tgtSentence"> (See <legacyLink xlink:href="4369708b-c9fb-4d48-a321-bf949b41a369">Getting and Setting Data (OLE DB)</legacyLink>in the OLE DB Programmer's Reference, for more information.)</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="577de499e6963e09b276a49bb8642708" id="tgt19" class="tgtSentence">Header File</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="fbc6773a8e971570a188e9b9d39038ef" id="tgt20" class="tgtSentence">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</caps:sentence>
          </para>
          <code>#include &lt;icrsint.h&gt;</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="6f7b29e0582ab7097731151cc299bd65" id="tgt21" class="tgtSentence">Binding Recordset Fields</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="523fbb2ea8069ccd60d4319f81446ea1" id="tgt22" class="tgtSentence">To Bind Recordset Fields to C/C++ Variables</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="2d9e1a3e16beeea8098243a9d85f22af" id="tgt23" class="tgtSentence">Create a class derived from the <legacyBold>CADORecordBinding</legacyBold> class.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="aa7ae4e3eec9da59fc927584b910c101" id="tgt24" class="tgtSentence">Specify binding entries and corresponding C/C++ variables in the derived class.</caps:sentence>
                    <caps:sentence sentenceid="2e9aa07af8c193e60c7d38ee84cf2835" id="tgt25" class="tgtSentence"> Bracket the binding entries between <legacyBold>BEGIN_ADO_BINDING</legacyBold> and <legacyBold>END_ADO_BINDING</legacyBold> macros.</caps:sentence>
                    <caps:sentence sentenceid="334d30610c8d469a330ab4de9a46a575" id="tgt26" class="tgtSentence"> Do not terminate the macros with commas or semicolons.</caps:sentence>
                    <caps:sentence sentenceid="961a3f494e0e0d7e45b17fe57f20cf53" id="tgt27" class="tgtSentence"> Appropriate delimiters are specified automatically by each macro.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="5c6e5b404c43c6bc6e78523a91450d50" id="tgt28" class="tgtSentence">Specify one binding entry for each field to be mapped to a C/C++ variable.</caps:sentence>
                    <caps:sentence sentenceid="4a2e053856e5e2ff478af10fe8fd67b0" id="tgt29" class="tgtSentence"> Use an appropriate member from the <legacyBold>ADO_FIXED_LENGTH_ENTRY</legacyBold>, <legacyBold>ADO_NUMERIC_ENTRY</legacyBold>, or <legacyBold>ADO_VARIABLE_LENGTH_ENTRY</legacyBold> family of macros.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9da2cda2ce16389ca11059cf7dc013f6" id="tgt30" class="tgtSentence">In your application, create an instance of the class derived from <legacyBold>CADORecordBinding</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="51cca0e2b7721f7f019313f637f48374" id="tgt31" class="tgtSentence"> Get the <legacyBold>IADORecordBinding</legacyBold> interface from the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="515e27377e1351e428e96e60d6178df4" id="tgt32" class="tgtSentence"> Then call the <legacyBold>BindToRecordset</legacyBold> method to bind the <legacyBold>Recordset</legacyBold> fields to the C/C++ variables.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence sentenceid="5c612215661daaf0ef4c08493bdc6470" id="tgt33" class="tgtSentence">For more information, see the <legacyLink xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">Visual C++ Extensions Example</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b2778e072d730c6b1517899319979e4a" id="tgt34" class="tgtSentence">Interface Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="73f481024d48fc62331201efe5e79e2d" id="tgt35" class="tgtSentence">The <legacyBold>IADORecordBinding</legacyBold> interface has three methods: <legacyBold>BindToRecordset</legacyBold>, <legacyBold>AddNew</legacyBold>, and <legacyBold>Update</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="a53e7788c0668d4b5d5919d4f307457b" id="tgt36" class="tgtSentence"> The sole argument to each method is a pointer to an instance of the class derived from <legacyBold>CADORecordBinding</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="e6c60f31cc67564c0237bc2dbd6c58cf" id="tgt37" class="tgtSentence"> Therefore, the <legacyBold>AddNew</legacyBold> and <legacyBold>Update</legacyBold> methods cannot specify any of the parameters of their ADO method namesakes.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="55152fd428afc5d73e8878d27d0b09c3" id="tgt38" class="tgtSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ddda92ee9475fc1f822cb1d9be38f8f2" id="tgt39" class="tgtSentence">The <legacyBold>BindToRecordset</legacyBold> method associates the <legacyBold>Recordset</legacyBold> fields with C/C++ variables.</caps:sentence>
          </para>
          <code>BindToRecordset(CADORecordBinding <legacyItalic xmlns="">*binding</legacyItalic>)</code>
          <para>
            <caps:sentence sentenceid="733415c0c7583030b9ab005647e114a4" id="tgt40" class="tgtSentence">The <legacyBold>AddNew</legacyBold> method invokes its namesake, the ADO <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink> method, to add a new row to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <code>AddNew(CADORecordBinding <legacyItalic xmlns="">*binding</legacyItalic>)</code>
          <para>
            <caps:sentence sentenceid="6783afafe55bc377558671a3b0927a91" id="tgt41" class="tgtSentence">The <legacyBold>Update</legacyBold> method invokes its namesake, the ADO <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method, to update the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <code>Update(CADORecordBinding <legacyItalic xmlns="">*binding</legacyItalic>)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="21d66cf3807b69ad37bd5b71b485990c" id="tgt42" class="tgtSentence">Binding Entry Macros</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2415b7f974913215cd1cf44dbb1e307d" id="tgt43" class="tgtSentence">Binding entry macros define the association of a <legacyBold>Recordset</legacyBold> field and a variable.</caps:sentence>
            <caps:sentence sentenceid="270b0ca87b0af5bcf4575f12917da4cd" id="tgt44" class="tgtSentence"> A beginning and ending macro delimits the set of binding entries.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c62b245d2b5d45c0df7061bc29ba5a8a" id="tgt45" class="tgtSentence">Families of macros are provided for fixed-length data, such as <legacyBold>adDate</legacyBold> or <legacyBold>adBoolean</legacyBold>; numeric data, such as <legacyBold>adTinyInt</legacyBold>, <legacyBold>adInteger</legacyBold>, or <legacyBold>adDouble</legacyBold>; and variable-length data, such as <legacyBold>adChar</legacyBold>, <legacyBold>adVarChar</legacyBold> or <legacyBold>adVarBinary</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="679635be349f801918e77fe9f69b0ebb" id="tgt46" class="tgtSentence"> All numeric types, except for <legacyBold>adVarNumeric</legacyBold>, are also fixed-length types.</caps:sentence>
            <caps:sentence sentenceid="5103d25ae5aec153ae43915d6884b626" id="tgt47" class="tgtSentence"> Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dc10de7a9a1c2c732360ed936502e168" id="tgt48" class="tgtSentence">For more information, see <legacyLink xlink:href="e3a0533a-2196-4eb0-a31e-92fe9556ada6">Appendix A: Data Types</legacyLink>, of the OLE DB Programmer's Reference.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="f4d6e2da796c7d1d59bcfe0546f2f1a5" id="tgt49" class="tgtSentence">Begin Binding Entries</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cf46f0bd6d772fab25a0ebc9da5c52db" id="tgt50" class="tgtSentence">
                  <legacyBold>BEGIN_ADO_BINDING</legacyBold>(<legacyItalic>Class</legacyItalic>)</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="0c43b7ef32e64e5b7ec7bd7eb0b4153b" id="tgt51" class="tgtSentence">Fixed-Length Data</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="fd11d9dbbdd7c66e5b2255ce056ea49b" id="tgt52" class="tgtSentence">
                  <legacyBold>ADO_FIXED_LENGTH_ENTRY</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Status, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="258524e34975ea15ab68b23ebf9d99ad" id="tgt53" class="tgtSentence">
                  <legacyBold>ADO_FIXED_LENGTH_ENTRY2</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Modify</legacyItalic>)</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="cdbf1ae34cc0ecd492760731dba150a2" id="tgt54" class="tgtSentence">Numeric Data</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f4319145e7fb3c62771258d2933994d6" id="tgt55" class="tgtSentence">
                  <legacyBold>ADO_NUMERIC_ENTRY</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Precision, Scale, Status, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5292fcbcf834f515d042f9fbda8a0d51" id="tgt56" class="tgtSentence">
                  <legacyBold>ADO_NUMERIC_ENTRY2</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Precision, Scale, Modify</legacyItalic>)</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="bc9ec32e4d6a386216d6a8d927907388" id="tgt57" class="tgtSentence">Variable-Length Data</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="912c1c9f2f73cd3b7cadbdf858f8908e" id="tgt58" class="tgtSentence">
                  <legacyBold>ADO_VARIABLE_LENGTH_ENTRY</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Size, Status, Length, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="05ab89cac500314a9a3285912e031328" id="tgt59" class="tgtSentence">
                  <legacyBold>ADO_VARIABLE_LENGTH_ENTRY2</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Size, Status, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="474d95e949685dbab248733501356e61" id="tgt60" class="tgtSentence">
                  <legacyBold>ADO_VARIABLE_LENGTH_ENTRY3</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Size, Length, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="78de0f6096d508c4584d9808f3c06792" id="tgt61" class="tgtSentence">
                  <legacyBold>ADO_VARIABLE_LENGTH_ENTRY4</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Size, Modify</legacyItalic>)</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="05e90918ce9ca2d52673ba7fbb5c7a1f" id="tgt62" class="tgtSentence">End Binding Entries</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="8d710128fc52adb580f4b4c9a37e6e3b" id="tgt63" class="tgtSentence">
                  <legacyBold>END_ADO_BINDING</legacyBold>()</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt64" class="tgtSentence">Parameter</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt65" class="tgtSentence">Description</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="a2f2ed4f8ebc2cbb4c21a29dc40ab61d" id="tgt66" class="tgtSentence">Class</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4ebba48e49a65e9ae55586c536df1771" id="tgt67" class="tgtSentence">Class in which the binding entries and C/C++ variables are defined.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="281858037f7dcf7ed49271bb92c60526" id="tgt68" class="tgtSentence">Ordinal</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3f2e99c895bdf03994966d780fa35d4d" id="tgt69" class="tgtSentence">Ordinal number, counting from one, of the <legacyBold>Recordset</legacyBold> field corresponding to your C/C++ variable.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="3931108d1662baf3d3b7a912ca3c43fd" id="tgt70" class="tgtSentence">DataType</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="420f053f91e91e8f685b6a6ec3f7cb1b" id="tgt71" class="tgtSentence">Equivalent ADO data type of the C/C++ variable (see <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> for a list of valid data types).</caps:sentence>
                        <caps:sentence sentenceid="26e8e86223913c436e417be7b17d5a68" id="tgt72" class="tgtSentence"> The value of the <legacyBold>Recordset</legacyBold> field will be converted to this data type if necessary.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="7f2db423a49b305459147332fb01cf87" id="tgt73" class="tgtSentence">Buffer</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fff85af6ab8d67e730cc6eae1682e0c0" id="tgt74" class="tgtSentence">Name of the C/C++ variable where the <legacyBold>Recordset</legacyBold> field will be stored.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="f7bd60b75b29d79b660a2859395c1a24" id="tgt75" class="tgtSentence">Size</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="db06c5182c36008961ab5750d9a55196" id="tgt76" class="tgtSentence">Maximum size in bytes of <legacyItalic>Buffer</legacyItalic>.</caps:sentence>
                        <caps:sentence sentenceid="2283c226572dc376fde47c1f4f250141" id="tgt77" class="tgtSentence"> If <legacyItalic>Buffer </legacyItalic>will contain a variable-length string, allow room for a terminating zero.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="9acb44549b41563697bb490144ec6258" id="tgt78" class="tgtSentence">Status</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fefe612e12528769c12abd1789148c25" id="tgt79" class="tgtSentence">Name of a variable that will indicate whether the contents of <legacyItalic>Buffer </legacyItalic>are valid, and whether the conversion of the field to <legacyItalic>DataType </legacyItalic>was successful.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="e4adc53f113ff8831c0e30ec339939d3" id="tgt80" class="tgtSentence">The two most important values for this variable are <legacyBold>adFldOK</legacyBold>, which means the conversion was successful; and <legacyBold>adFldNull</legacyBold>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="83430a0c35860b4ee981cb5bf47e1d19" id="tgt81" class="tgtSentence">Possible values for <legacyItalic>Status </legacyItalic>are listed in the next table, "Status Values."</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="8f45a2644508b5282f57fe129f62d19a" id="tgt82" class="tgtSentence">Modify</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="80b05285d0c63b6321964486488d9550" id="tgt83" class="tgtSentence">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <legacyBold>Recordset</legacyBold> field with the value contained in <legacyItalic>Buffer</legacyItalic>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="d035399ea1a61bf5f88637379258fbbf" id="tgt84" class="tgtSentence">Set the Boolean <legacyItalic>modify</legacyItalic> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="e2794d8f12719281eff5601251c8a680" id="tgt85" class="tgtSentence">Precision</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ef1d9b273128707bc1421eaef46b0c1e" id="tgt86" class="tgtSentence">Number of digits that can be represented in a numeric variable.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="0cb47aeb6e5f9323f0969e628c4e59f5" id="tgt87" class="tgtSentence">Scale</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="dd6fdb53480c6089fd3c99b2abfd622b" id="tgt88" class="tgtSentence">Number of decimal places in a numeric variable.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="2fa47f7c65fec19cc163b195725e3844" id="tgt89" class="tgtSentence">Length</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6c8856e886540c5204010393c33b4576" id="tgt90" class="tgtSentence">Name of a four-byte variable that will contain the actual length of the data in <legacyItalic>Buffer</legacyItalic>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="37302dafd6c8af6fb1518635d958a521" id="tgt91" class="tgtSentence">Status Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f8f2c90521154cd7baffdf67f9bfffc3" id="tgt92" class="tgtSentence">The value of the <legacyItalic>Status</legacyItalic> variable indicates whether a field was successfully copied to a variable.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="239b63e83e349e318bf22bd8d1f1de6a" id="tgt93" class="tgtSentence">When setting data, <legacyItalic>Status </legacyItalic>may be set to <legacyBold>adFldNull</legacyBold> to indicate the <legacyBold>Recordset</legacyBold> field should be set to null.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt94" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt95" class="tgtSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt96" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="61140b179dcadd7df3cbc2605178a18e" id="tgt97" class="tgtSentence">adFldOK</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt98" class="tgtSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ac5401f0974080151b7b0df704f924e" id="tgt99" class="tgtSentence">A non-null field value was returned.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a274627c9890a9b1246f644699e52db4" id="tgt100" class="tgtSentence">adFldBadAccessor</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt101" class="tgtSentence">1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fdebff8705b55bebc68266f175e5012" id="tgt102" class="tgtSentence">Binding was invalid.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a97ce2edf4ba74757239d0b44215cb50" id="tgt103" class="tgtSentence">adFldCantConvertValue</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt104" class="tgtSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dad000e3e11bef96c276736b5e3f4eb9" id="tgt105" class="tgtSentence">Value couldn't be converted for reasons other than sign mismatch or data overflow.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d8722d92ff44d8db1c4e450794555634" id="tgt106" class="tgtSentence">adFldNull</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt107" class="tgtSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c27d03ef166a2e8433030332e8d96e4e" id="tgt108" class="tgtSentence">When getting a field, indicates a null value was returned.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="6caac7ebf0823fcbb17d3c0df4ccdd8d" id="tgt109" class="tgtSentence">When setting a field, indicates the field should be set to <legacyBold>NULL</legacyBold> when the field cannot encode <legacyBold>NULL</legacyBold> itself (for example, a character array or an integer).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="afcfb258dc3140de381b9572f9c263bc" id="tgt110" class="tgtSentence">adFldTruncated</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt111" class="tgtSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f81219fcf70373569666358f05603290" id="tgt112" class="tgtSentence">Variable-length data or numeric digits were truncated.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="ae1a8d27ba45ab3eec7b9e241cabaf0b" id="tgt113" class="tgtSentence">adFldSignMismatch</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e4da3b7fbbce2345d7772b0674a318d5" id="tgt114" class="tgtSentence">5</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1e7d651e5ac1086431e484eaf80e195a" id="tgt115" class="tgtSentence">Value is signed and variable data type is unsigned.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="641b42893f28409d73c4912e832736db" id="tgt116" class="tgtSentence">adFldDataOverFlow</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1679091c5a880faf6fb5e6087eb1b2dc" id="tgt117" class="tgtSentence">6</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="93a31aaabb4099ee1dbb0d01ad84edb4" id="tgt118" class="tgtSentence">Value is larger than could be stored in the variable data type.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d6f2f3d77d0722058bc235a7d8794b8d" id="tgt119" class="tgtSentence">adFldCantCreate</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8f14e45fceea167a5a36dedd4bea2543" id="tgt120" class="tgtSentence">7</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46eee0ebf462f408ca20710730547e5c" id="tgt121" class="tgtSentence">Unknown column type and field already open.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="df3e58164f8d4a9b91b6fd1047211170" id="tgt122" class="tgtSentence">adFldUnavailable</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c9f0f895fb98ab9159f51fd0297e236d" id="tgt123" class="tgtSentence">8</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db7fe4df448f86784ff959545c658276" id="tgt124" class="tgtSentence">Field value could not be determined—for example, on a new, unassigned field with no default value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="c90ef8ff8daeb7b824a947dfdac31bf6" id="tgt125" class="tgtSentence">adFldPermissionDenied</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45c48cce2e2d7fbdea1afc51c7c6ad26" id="tgt126" class="tgtSentence">9</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="527b712948e7fedc45870785edd37c91" id="tgt127" class="tgtSentence">When updating, no permission to write data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="89b3bbad18fb969d82e42492a19a4912" id="tgt128" class="tgtSentence">adFldIntegrityViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d3d9446802a44259755d38e6d163e820" id="tgt129" class="tgtSentence">10</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cc540537eecb2eea396326d47b9c2d2d" id="tgt130" class="tgtSentence">When updating, field value would violate column integrity.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="09997a1cd6d24a29f5d905f3f7bce209" id="tgt131" class="tgtSentence">adFldSchemaViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6512bd43d9caa6e02c990b0a82652dca" id="tgt132" class="tgtSentence">11</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ffac4aab6201446dae852479800c5bb9" id="tgt133" class="tgtSentence">When updating, field value would violate column schema.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="f9c6a6ffd04e2b0deb5c38bb1f245914" id="tgt134" class="tgtSentence">adFldBadStatus</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c20ad4d76fe97759aa27a0c99bff6710" id="tgt135" class="tgtSentence">12</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9143c7c60a58495125088d790e8c1d60" id="tgt136" class="tgtSentence">When updating, invalid status parameter.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="138967d01c415f1decf8dbc45e7b4f77" id="tgt137" class="tgtSentence">adFldDefault</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c51ce410c124a10e0db5e4b97fc2af39" id="tgt138" class="tgtSentence">13</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="11e7fa853ce66e1bb718538ece885734" id="tgt139" class="tgtSentence">When updating, a default value was used.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">ADO with Visual C++ Extensions Example</link>
        <link xlink:href="e492d307-24cb-489c-a5b0-99cdc09b07da">Visual C++ Extensions Header</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">The IADORecordBinding Interface</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object to C/C++ variables.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Whenever the current row of the bound <legacyBold>Recordset</legacyBold> changes, all the bound fields in the <legacyBold>Recordset</legacyBold> are copied to the C/C++ variables.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> If necessary, the copied data is converted to the declared data type of the C/C++ variable.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">The <legacyBold>BindToRecordset</legacyBold> method of the <legacyBold>IADORecordBinding</legacyBold> interface binds fields to C/C++ variables.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The <legacyBold>AddNew</legacyBold> method adds a new row to the bound <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The <legacyBold>Update</legacyBold> method populates fields in new rows of the <legacyBold>Recordset</legacyBold>, or updates fields in existing rows, with the value of the C/C++ variables.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <legacyBold>IADORecordBinding</legacyBold> interface is implemented by the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> You do not code the implementation yourself.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Binding Entries</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">The Visual C++ Extensions for ADO map fields of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object to C/C++ variables.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> The definition of a mapping between a field and a variable is called a <legacyItalic>binding entry</legacyItalic>.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Macros provide binding entries for numeric, fixed-length, and variable-length data.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, <legacyBold>CADORecordBinding</legacyBold>.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> The <legacyBold>CADORecordBinding</legacyBold> class is defined internally by the binding entry macros.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">ADO internally maps the parameters in these macros to an OLE DB <legacyBold>DBBINDING</legacyBold> structure and creates an OLE DB <legacyBold>Accessor</legacyBold> object to manage the movement and conversion of data between fields and variables.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> OLE DB defines data as consisting of three parts: A <legacyItalic>buffer</legacyItalic> where the data is stored; a <legacyItalic>status</legacyItalic> that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the <legacyItalic>length</legacyItalic> of the data.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> (See <legacyLink xlink:href="4369708b-c9fb-4d48-a321-bf949b41a369">Getting and Setting Data (OLE DB)</legacyLink>in the OLE DB Programmer's Reference, for more information.)</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src19" class="srcSentence">Header File</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src20" class="srcSentence">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</caps:sentence>
          </para>
          <code>#include &lt;icrsint.h&gt;</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Binding Recordset Fields</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src22" class="srcSentence">To Bind Recordset Fields to C/C++ Variables</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Create a class derived from the <legacyBold>CADORecordBinding</legacyBold> class.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Specify binding entries and corresponding C/C++ variables in the derived class.</caps:sentence>
                    <caps:sentence id="src25" class="srcSentence"> Bracket the binding entries between <legacyBold>BEGIN_ADO_BINDING</legacyBold> and <legacyBold>END_ADO_BINDING</legacyBold> macros.</caps:sentence>
                    <caps:sentence id="src26" class="srcSentence"> Do not terminate the macros with commas or semicolons.</caps:sentence>
                    <caps:sentence id="src27" class="srcSentence"> Appropriate delimiters are specified automatically by each macro.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Specify one binding entry for each field to be mapped to a C/C++ variable.</caps:sentence>
                    <caps:sentence id="src29" class="srcSentence"> Use an appropriate member from the <legacyBold>ADO_FIXED_LENGTH_ENTRY</legacyBold>, <legacyBold>ADO_NUMERIC_ENTRY</legacyBold>, or <legacyBold>ADO_VARIABLE_LENGTH_ENTRY</legacyBold> family of macros.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">In your application, create an instance of the class derived from <legacyBold>CADORecordBinding</legacyBold>.</caps:sentence>
                    <caps:sentence id="src31" class="srcSentence"> Get the <legacyBold>IADORecordBinding</legacyBold> interface from the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                    <caps:sentence id="src32" class="srcSentence"> Then call the <legacyBold>BindToRecordset</legacyBold> method to bind the <legacyBold>Recordset</legacyBold> fields to the C/C++ variables.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence id="src33" class="srcSentence">For more information, see the <legacyLink xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">Visual C++ Extensions Example</legacyLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src34" class="srcSentence">Interface Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src35" class="srcSentence">The <legacyBold>IADORecordBinding</legacyBold> interface has three methods: <legacyBold>BindToRecordset</legacyBold>, <legacyBold>AddNew</legacyBold>, and <legacyBold>Update</legacyBold>.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> The sole argument to each method is a pointer to an instance of the class derived from <legacyBold>CADORecordBinding</legacyBold>.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> Therefore, the <legacyBold>AddNew</legacyBold> and <legacyBold>Update</legacyBold> methods cannot specify any of the parameters of their ADO method namesakes.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src38" class="srcSentence">Syntax</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src39" class="srcSentence">The <legacyBold>BindToRecordset</legacyBold> method associates the <legacyBold>Recordset</legacyBold> fields with C/C++ variables.</caps:sentence>
          </para>
          <code>BindToRecordset(CADORecordBinding <legacyItalic xmlns="">*binding</legacyItalic>)</code>
          <para>
            <caps:sentence id="src40" class="srcSentence">The <legacyBold>AddNew</legacyBold> method invokes its namesake, the ADO <legacyLink xlink:href="a9f54be9-5763-45d0-a6eb-09981b03bc08">AddNew</legacyLink> method, to add a new row to the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <code>AddNew(CADORecordBinding <legacyItalic xmlns="">*binding</legacyItalic>)</code>
          <para>
            <caps:sentence id="src41" class="srcSentence">The <legacyBold>Update</legacyBold> method invokes its namesake, the ADO <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink> method, to update the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <code>Update(CADORecordBinding <legacyItalic xmlns="">*binding</legacyItalic>)</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src42" class="srcSentence">Binding Entry Macros</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src43" class="srcSentence">Binding entry macros define the association of a <legacyBold>Recordset</legacyBold> field and a variable.</caps:sentence>
            <caps:sentence id="src44" class="srcSentence"> A beginning and ending macro delimits the set of binding entries.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src45" class="srcSentence">Families of macros are provided for fixed-length data, such as <legacyBold>adDate</legacyBold> or <legacyBold>adBoolean</legacyBold>; numeric data, such as <legacyBold>adTinyInt</legacyBold>, <legacyBold>adInteger</legacyBold>, or <legacyBold>adDouble</legacyBold>; and variable-length data, such as <legacyBold>adChar</legacyBold>, <legacyBold>adVarChar</legacyBold> or <legacyBold>adVarBinary</legacyBold>.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> All numeric types, except for <legacyBold>adVarNumeric</legacyBold>, are also fixed-length types.</caps:sentence>
            <caps:sentence id="src47" class="srcSentence"> Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src48" class="srcSentence">For more information, see <legacyLink xlink:href="e3a0533a-2196-4eb0-a31e-92fe9556ada6">Appendix A: Data Types</legacyLink>, of the OLE DB Programmer's Reference.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src49" class="srcSentence">Begin Binding Entries</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src50" class="srcSentence">
                  <legacyBold>BEGIN_ADO_BINDING</legacyBold>(<legacyItalic>Class</legacyItalic>)</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src51" class="srcSentence">Fixed-Length Data</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src52" class="srcSentence">
                  <legacyBold>ADO_FIXED_LENGTH_ENTRY</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Status, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src53" class="srcSentence">
                  <legacyBold>ADO_FIXED_LENGTH_ENTRY2</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Modify</legacyItalic>)</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src54" class="srcSentence">Numeric Data</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src55" class="srcSentence">
                  <legacyBold>ADO_NUMERIC_ENTRY</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Precision, Scale, Status, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src56" class="srcSentence">
                  <legacyBold>ADO_NUMERIC_ENTRY2</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Precision, Scale, Modify</legacyItalic>)</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src57" class="srcSentence">Variable-Length Data</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src58" class="srcSentence">
                  <legacyBold>ADO_VARIABLE_LENGTH_ENTRY</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Size, Status, Length, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src59" class="srcSentence">
                  <legacyBold>ADO_VARIABLE_LENGTH_ENTRY2</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Size, Status, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src60" class="srcSentence">
                  <legacyBold>ADO_VARIABLE_LENGTH_ENTRY3</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Size, Length, Modify</legacyItalic>)</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src61" class="srcSentence">
                  <legacyBold>ADO_VARIABLE_LENGTH_ENTRY4</legacyBold>(<legacyItalic>Ordinal, DataType, Buffer, Size, Modify</legacyItalic>)</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src62" class="srcSentence">End Binding Entries</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src63" class="srcSentence">
                  <legacyBold>END_ADO_BINDING</legacyBold>()</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">Parameter</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">Description</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src66" class="srcSentence">Class</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">Class in which the binding entries and C/C++ variables are defined.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src68" class="srcSentence">Ordinal</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">Ordinal number, counting from one, of the <legacyBold>Recordset</legacyBold> field corresponding to your C/C++ variable.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src70" class="srcSentence">DataType</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Equivalent ADO data type of the C/C++ variable (see <legacyLink xlink:href="2c57eca6-9336-4b06-ba10-9fef5926b1d0">DataTypeEnum</legacyLink> for a list of valid data types).</caps:sentence>
                        <caps:sentence id="src72" class="srcSentence"> The value of the <legacyBold>Recordset</legacyBold> field will be converted to this data type if necessary.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src73" class="srcSentence">Buffer</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">Name of the C/C++ variable where the <legacyBold>Recordset</legacyBold> field will be stored.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src75" class="srcSentence">Size</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src76" class="srcSentence">Maximum size in bytes of <legacyItalic>Buffer</legacyItalic>.</caps:sentence>
                        <caps:sentence id="src77" class="srcSentence"> If <legacyItalic>Buffer </legacyItalic>will contain a variable-length string, allow room for a terminating zero.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src78" class="srcSentence">Status</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">Name of a variable that will indicate whether the contents of <legacyItalic>Buffer </legacyItalic>are valid, and whether the conversion of the field to <legacyItalic>DataType </legacyItalic>was successful.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">The two most important values for this variable are <legacyBold>adFldOK</legacyBold>, which means the conversion was successful; and <legacyBold>adFldNull</legacyBold>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">Possible values for <legacyItalic>Status </legacyItalic>are listed in the next table, "Status Values."</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src82" class="srcSentence">Modify</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <legacyBold>Recordset</legacyBold> field with the value contained in <legacyItalic>Buffer</legacyItalic>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">Set the Boolean <legacyItalic>modify</legacyItalic> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src85" class="srcSentence">Precision</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">Number of digits that can be represented in a numeric variable.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src87" class="srcSentence">Scale</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">Number of decimal places in a numeric variable.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src89" class="srcSentence">Length</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">Name of a four-byte variable that will contain the actual length of the data in <legacyItalic>Buffer</legacyItalic>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src91" class="srcSentence">Status Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src92" class="srcSentence">The value of the <legacyItalic>Status</legacyItalic> variable indicates whether a field was successfully copied to a variable.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src93" class="srcSentence">When setting data, <legacyItalic>Status </legacyItalic>may be set to <legacyBold>adFldNull</legacyBold> to indicate the <legacyBold>Recordset</legacyBold> field should be set to null.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">Value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src97" class="srcSentence">adFldOK</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">A non-null field value was returned.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src100" class="srcSentence">adFldBadAccessor</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">Binding was invalid.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src103" class="srcSentence">adFldCantConvertValue</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">2</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">Value couldn't be converted for reasons other than sign mismatch or data overflow.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src106" class="srcSentence">adFldNull</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">3</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">When getting a field, indicates a null value was returned.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">When setting a field, indicates the field should be set to <legacyBold>NULL</legacyBold> when the field cannot encode <legacyBold>NULL</legacyBold> itself (for example, a character array or an integer).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src110" class="srcSentence">adFldTruncated</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">4</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">Variable-length data or numeric digits were truncated.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src113" class="srcSentence">adFldSignMismatch</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">5</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">Value is signed and variable data type is unsigned.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src116" class="srcSentence">adFldDataOverFlow</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">6</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">Value is larger than could be stored in the variable data type.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src119" class="srcSentence">adFldCantCreate</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">7</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">Unknown column type and field already open.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src122" class="srcSentence">adFldUnavailable</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src123" class="srcSentence">8</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">Field value could not be determined—for example, on a new, unassigned field with no default value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src125" class="srcSentence">adFldPermissionDenied</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">9</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">When updating, no permission to write data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src128" class="srcSentence">adFldIntegrityViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">10</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">When updating, field value would violate column integrity.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src131" class="srcSentence">adFldSchemaViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">11</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">When updating, field value would violate column schema.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src134" class="srcSentence">adFldBadStatus</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">12</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">When updating, invalid status parameter.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src137" class="srcSentence">adFldDefault</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">13</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">When updating, a default value was used.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">ADO with Visual C++ Extensions Example</link>
        <link xlink:href="e492d307-24cb-489c-a5b0-99cdc09b07da">Visual C++ Extensions Header</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
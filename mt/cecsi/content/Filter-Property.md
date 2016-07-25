---
title: "Filter Property"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 80263a7a-5d21-45d1-84fc-34b7a9be4c22
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
# Filter Property
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7c265ea51c3a1ca23f7d70fe5d0ef5a8" id="tgt1" class="tgtSentence">Indicates a filter for data in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0e5342a8527c2bff35bb52947027b0d6" id="tgt3" class="tgtSentence">Sets or returns a <legacyBold>Variant</legacyBold> value, which can contain one of the following: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="dd8dc904af9cd4725cd7795a5feedfe6" id="tgt4" class="tgtSentence">
                  <legacyBold>Criteria string</legacyBold> — a string made up of one or more individual clauses concatenated with <legacyBold>AND</legacyBold> or <legacyBold>OR</legacyBold> operators.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="cac1e1d8ce26161d7d1e94d944616988" id="tgt5" class="tgtSentence">
                  <legacyBold>Array of bookmarks</legacyBold> — an array of unique bookmark values that point to records in the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="53be18cad652265a543aa9b28d84b215" id="tgt6" class="tgtSentence">A <link xlink:href="b22e725e-84bd-4286-a070-290c278c3783">FilterGroupEnum</link> value.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="de267f336de69e2ebae4799ec79b2fdf" id="tgt7" class="tgtSentence">Use the <legacyBold>Filter</legacyBold> property to selectively screen out records in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="5ab43d3c28575d1184100c00bb42703d" id="tgt8" class="tgtSentence"> The filtered <legacyBold>Recordset</legacyBold> becomes the current cursor.</caps:sentence>
            <caps:sentence sentenceid="f0314eeeceac282346dd19d4151a53a9" id="tgt9" class="tgtSentence"> Other properties that return values based on the current <legacyBold>cursor</legacyBold> are affected, such as <link xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition Property (ADO)</link>, <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property (ADO)</link>, <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property (ADO)</link>, and <link xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount Property (ADO)</link>.</caps:sentence>
            <caps:sentence sentenceid="55845f031ad22cbd51a6d2d49c590b1b" id="tgt10" class="tgtSentence"> This is because setting the <legacyBold>Filter</legacyBold> property to a specific value will move the current record to the first record that satisfies the new value.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d04f40d2426ef61d30359960de6a00b4" id="tgt11" class="tgtSentence">The criteria string is made up of clauses in the form <legacyItalic>FieldName-Operator-Value</legacyItalic> (for example, <codeInline>"LastName = 'Smith'"</codeInline>).</caps:sentence>
            <caps:sentence sentenceid="eb5f8f38a70f0a59fdc73f4ba7c8c3a3" id="tgt12" class="tgtSentence"> You can create compound clauses by concatenating individual clauses with <legacyBold>AND</legacyBold> (for example, <codeInline>"LastName = 'Smith' AND FirstName = 'John'"</codeInline>) or <legacyBold>OR</legacyBold> (for example, <codeInline>"LastName = 'Smith' OR LastName = 'Jones'"</codeInline>).</caps:sentence>
            <caps:sentence sentenceid="d560792cbf3de4464c07b312f6b0696a" id="tgt13" class="tgtSentence"> Use the following guidelines for criteria strings:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="c879d47a224889b57428f5af8bd66ca3" id="tgt14" class="tgtSentence">
                  <legacyItalic>FieldName</legacyItalic> must be a valid field name from the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="9e1c645376798c904c75488b09352567" id="tgt15" class="tgtSentence"> If the field name contains spaces, you must enclose the name in square brackets.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c3238dc3ecdc6087089c632442cc32f5" id="tgt16" class="tgtSentence">Operator must be one of the following: &lt;, &gt;, &lt;=, &gt;=, &lt;&gt;, =, or <legacyBold>LIKE</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fae8646b16c60205d985a4b7053d03ad" id="tgt17" class="tgtSentence">Value is the value with which you will compare the field values (for example, 'Smith', #8/24/95#, 12.345, or $50.00).</caps:sentence>
                <caps:sentence sentenceid="c616e2807fbb853bf469eb7705108249" id="tgt18" class="tgtSentence"> Use single quotes with strings and pound signs (#) with dates.</caps:sentence>
                <caps:sentence sentenceid="af3da72ab39086363b0390de7fd48a79" id="tgt19" class="tgtSentence"> For numbers, you can use decimal points, dollar signs, and scientific notation.</caps:sentence>
                <caps:sentence sentenceid="1b9ecdfb785b5a68cbd2f550c16c5824" id="tgt20" class="tgtSentence"> If Operator is <legacyBold>LIKE</legacyBold>, Value can use wildcards.</caps:sentence>
                <caps:sentence sentenceid="a1775953a471ddcb8ed07946ff7fd139" id="tgt21" class="tgtSentence"> Only the asterisk (*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</caps:sentence>
                <caps:sentence sentenceid="376e6a3eb2daf98f6558ec2cf82ad89e" id="tgt22" class="tgtSentence"> Value cannot be null.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="193dae26f8b28e976344b3318220f07c" id="tgt23" class="tgtSentence">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one.</caps:sentence>
              <caps:sentence sentenceid="69b3e5fd0c41b827e22adff5069a4218" id="tgt24" class="tgtSentence"> For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'".</caps:sentence>
              <caps:sentence sentenceid="2a1330c01dab22215f18124e97ac370d" id="tgt25" class="tgtSentence"> To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#).</caps:sentence>
              <caps:sentence sentenceid="a1c57851ddbf3e5357f23cc4e6474881" id="tgt26" class="tgtSentence"> For example, to filter on '1', the criteria string should be "col1 = #'1'#".</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="13f1cff744d12b69a9817ba3c3d94734" id="tgt27" class="tgtSentence">There is no precedence between AND and OR.</caps:sentence>
                <caps:sentence sentenceid="f1d9c46cdcfd93850b33eb92610d1bde" id="tgt28" class="tgtSentence"> Clauses can be grouped within parentheses.</caps:sentence>
                <caps:sentence sentenceid="89179a0cc13d750379cbbb1c39f1c076" id="tgt29" class="tgtSentence"> However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this: <codeInline>(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'</codeInline></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="79490630700671b057fc01fd2d33b04a" id="tgt30" class="tgtSentence">Instead, you would construct this filter as <codeInline>(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')</codeInline></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1959c2be2cc63a9f562783301fb65ce2" id="tgt31" class="tgtSentence">In a <legacyBold>LIKE</legacyBold> clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '*mit*'), or only at the end of the pattern (for example, LastName Like 'Smit*').</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="81d981eaff31404fa2455659d283d536" id="tgt32" class="tgtSentence">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link> method call.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="acc5e37e87116a7d0b82261012300955" id="tgt33" class="tgtSentence">Setting the Filter property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user).</caps:sentence>
            <caps:sentence sentenceid="c94ba90762ba15e8fb279615635e652e" id="tgt34" class="tgtSentence"> In such a case, the provider returns warnings to the <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection (ADO)</link> collection but does not halt program execution.</caps:sentence>
            <caps:sentence sentenceid="4c7f463f068ed0b730457239bf177224" id="tgt35" class="tgtSentence"> A run-time error occurs only if there are conflicts on all the requested records.</caps:sentence>
            <caps:sentence sentenceid="8787d37feb2823d3690ae2b974b87917" id="tgt36" class="tgtSentence"> Use the <link xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status Property (ADO Recordset)</link> property to locate records with conflicts.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b8673e001f5ff144d6926c732b399436" id="tgt37" class="tgtSentence">Setting the <legacyBold>Filter</legacyBold> property to a zero-length string ("") has the same effect as using the <legacyBold>adFilterNone</legacyBold> constant.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b48c2448c03a6f9fa2a2cd5a4c1377ee" id="tgt38" class="tgtSentence">Whenever the <legacyBold>Filter</legacyBold> property is set, the current record position moves to the first record in the filtered subset of records in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="417195e63b6243fbed91403f34ecbb7f" id="tgt39" class="tgtSentence"> Similarly, when the <legacyBold>Filter</legacyBold> property is cleared, the current record position moves to the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3ad69892ae52eb4d5cbec0407ab551d2" id="tgt40" class="tgtSentence">When a <legacyBold>Recordset</legacyBold> is filtered based on a field of some variant type (e.g., sql_variant), an error (DISP_E_TYPEMISMATCH or 80020005) will result if the subtypes of the field and filter values used in the criteria string do not match.</caps:sentence>
            <caps:sentence sentenceid="f24a143e0c7f6d59edb226e8e98a72cc" id="tgt41" class="tgtSentence"> For example, if a <legacyBold>Recordset</legacyBold> object (rs) contains a column (C) of the sql_variant type and a field of this column has been assigned a value of 1 of the I4 type, setting the criteria string of rs.Filter = "C='A'" on the field will produce the error at run time.</caps:sentence>
            <caps:sentence sentenceid="71acce61764f1d821e9a5923b051c26f" id="tgt42" class="tgtSentence"> However, rs.Filter = "C=2" applied on the same field will not produce any error although the field will be filtered out of the current record set.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6e74ee3a22156d637ba77bc30874e288" id="tgt43" class="tgtSentence">See the <link xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark Property (ADO)</link> property for an explanation of bookmark values from which you can build an array to use with the Filter property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d132af0ac02b67da8e206eb32da85994" id="tgt44" class="tgtSentence">Only Filters in the form of Criteria Strings (e.g. OrderDate &gt; '12/31/1999') affect the contents of a persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="f682b816f8f953f1a20ed65a084d7a0a" id="tgt45" class="tgtSentence"> Filters created with an Array of Bookmarks or using a value from the FilterGroupEnum will not affect the contents of the persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="946eb4b859c5c07463e38d0d4849b2f1" id="tgt46" class="tgtSentence"> These rules apply to Recordsets created with either client-side or server-side cursors.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="f92ed32e9d7642d5546fb5754a21d63f" id="tgt47" class="tgtSentence">When you apply the adFilterPendingRecords flag to a filtered and modified <legacyBold>Recordset</legacyBold> in the batch update mode, the resultant <legacyBold>Recordset</legacyBold> is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values.</caps:sentence>
              <caps:sentence sentenceid="c3a96a30d5602b79bb86925383ef6e52" id="tgt48" class="tgtSentence"> The resultant <legacyBold>Recordset</legacyBold> will be non-empty if one of the following is true:</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="2eb84ee8b321b4f0948738621c772f81" id="tgt49" class="tgtSentence">The filtering was based on non-key fields in a single-keyed table.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5c6d251f845fc200bd019a7eb1c4675d" id="tgt50" class="tgtSentence">The filtering was based on any fields in a multiple-keyed table.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4c94c63ed1f6a1e41e9cc81bfbaf6bb1" id="tgt51" class="tgtSentence">Modifications were made on non-key fields in a single-keyed table.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9a0d21666575982b7b543ac1b4bb24ff" id="tgt52" class="tgtSentence">Modifications were made on any fields in a multiple-keyed table.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="b046d81a5f431604faebe151d0d16bd6" id="tgt53" class="tgtSentence">The following table summarizes the effects of <legacyBold>adFilterPendingRecords</legacyBold> in different combinations of filtering and modifications.</caps:sentence>
            <caps:sentence sentenceid="b74342841e267b5a34d434e4b00d39be" id="tgt54" class="tgtSentence"> The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table.</caps:sentence>
            <caps:sentence sentenceid="ee28816744bc7cf3b3e2b6c5d12ac706" id="tgt55" class="tgtSentence"> The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table.</caps:sentence>
            <caps:sentence sentenceid="cd40c1cee2aa82b408f63f7297ee54f7" id="tgt56" class="tgtSentence"> The intersecting cells show the results: + means that applying <legacyBold>adFilterPendingRecords</legacyBold> results in a non-empty <legacyBold>Recordset</legacyBold>; - means an empty <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para> </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="64d371d934d4a2bbb074264cf065fe54" id="tgt57" class="tgtSentence">Non keys</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b2af4de9cec99ed69831679f1ef3a599" id="tgt58" class="tgtSentence">Single Key</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a4c40a8f0f591db6ebdcf7bde0442855" id="tgt59" class="tgtSentence">Multiple Keys</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="64d371d934d4a2bbb074264cf065fe54" id="tgt60" class="tgtSentence">Non keys</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26b17225b626fb9238849fd60eabdf60" id="tgt61" class="tgtSentence">+</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26b17225b626fb9238849fd60eabdf60" id="tgt62" class="tgtSentence">+</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26b17225b626fb9238849fd60eabdf60" id="tgt63" class="tgtSentence">+</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="b2af4de9cec99ed69831679f1ef3a599" id="tgt64" class="tgtSentence">Single Key</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26b17225b626fb9238849fd60eabdf60" id="tgt65" class="tgtSentence">+</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="336d5ebc5436534e61d16e63ddfca327" id="tgt66" class="tgtSentence">-</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt67" class="tgtSentence">N/A</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a4c40a8f0f591db6ebdcf7bde0442855" id="tgt68" class="tgtSentence">Multiple Keys</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26b17225b626fb9238849fd60eabdf60" id="tgt69" class="tgtSentence">+</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt70" class="tgtSentence">N/A</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26b17225b626fb9238849fd60eabdf60" id="tgt71" class="tgtSentence">+</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt72" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e8bc63c7-8967-438a-9a49-512478a87a15">Filter and RecordCount Properties Example (VB)</link>
        <link xlink:href="b71346cb-3b09-4b8c-a600-976171a1c336">Filter and RecordCount Properties Example (VC++)</link>
        <link xlink:href="16d5d896-9905-4f75-973b-e1e696cd169f">Filter and RecordCount Properties Example (VJ++)</link>
        <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method (ADO)</link>
        <link xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize Property-Dynamic (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates a filter for data in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyBold>Variant</legacyBold> value, which can contain one of the following: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src4" class="srcSentence">
                  <legacyBold>Criteria string</legacyBold> — a string made up of one or more individual clauses concatenated with <legacyBold>AND</legacyBold> or <legacyBold>OR</legacyBold> operators.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">
                  <legacyBold>Array of bookmarks</legacyBold> — an array of unique bookmark values that point to records in the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">A <link xlink:href="b22e725e-84bd-4286-a070-290c278c3783">FilterGroupEnum</link> value.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">Use the <legacyBold>Filter</legacyBold> property to selectively screen out records in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The filtered <legacyBold>Recordset</legacyBold> becomes the current cursor.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Other properties that return values based on the current <legacyBold>cursor</legacyBold> are affected, such as <link xlink:href="79f8ee5e-fc70-46d8-8c29-ebf943c66592">AbsolutePosition Property (ADO)</link>, <link xlink:href="ddb58a35-ec3a-423c-a504-3c65e62c23d4">AbsolutePage Property (ADO)</link>, <link xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount Property (ADO)</link>, and <link xlink:href="b601b56c-0ac4-44ee-bc91-c3d2d104f00a">PageCount Property (ADO)</link>.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> This is because setting the <legacyBold>Filter</legacyBold> property to a specific value will move the current record to the first record that satisfies the new value.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">The criteria string is made up of clauses in the form <legacyItalic>FieldName-Operator-Value</legacyItalic> (for example, <codeInline>"LastName = 'Smith'"</codeInline>).</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> You can create compound clauses by concatenating individual clauses with <legacyBold>AND</legacyBold> (for example, <codeInline>"LastName = 'Smith' AND FirstName = 'John'"</codeInline>) or <legacyBold>OR</legacyBold> (for example, <codeInline>"LastName = 'Smith' OR LastName = 'Jones'"</codeInline>).</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Use the following guidelines for criteria strings:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">
                  <legacyItalic>FieldName</legacyItalic> must be a valid field name from the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> If the field name contains spaces, you must enclose the name in square brackets.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">Operator must be one of the following: &lt;, &gt;, &lt;=, &gt;=, &lt;&gt;, =, or <legacyBold>LIKE</legacyBold>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">Value is the value with which you will compare the field values (for example, 'Smith', #8/24/95#, 12.345, or $50.00).</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> Use single quotes with strings and pound signs (#) with dates.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> For numbers, you can use decimal points, dollar signs, and scientific notation.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> If Operator is <legacyBold>LIKE</legacyBold>, Value can use wildcards.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> Only the asterisk (*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> Value cannot be null.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src23" class="srcSentence">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one.</caps:sentence>
              <caps:sentence id="src24" class="srcSentence"> For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'".</caps:sentence>
              <caps:sentence id="src25" class="srcSentence"> To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#).</caps:sentence>
              <caps:sentence id="src26" class="srcSentence"> For example, to filter on '1', the criteria string should be "col1 = #'1'#".</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src27" class="srcSentence">There is no precedence between AND and OR.</caps:sentence>
                <caps:sentence id="src28" class="srcSentence"> Clauses can be grouped within parentheses.</caps:sentence>
                <caps:sentence id="src29" class="srcSentence"> However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this: <codeInline>(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'</codeInline></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">Instead, you would construct this filter as <codeInline>(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')</codeInline></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src31" class="srcSentence">In a <legacyBold>LIKE</legacyBold> clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '*mit*'), or only at the end of the pattern (for example, LastName Like 'Smit*').</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src32" class="srcSentence">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last <link xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch Method</link> method call.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src33" class="srcSentence">Setting the Filter property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user).</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> In such a case, the provider returns warnings to the <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection (ADO)</link> collection but does not halt program execution.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> A run-time error occurs only if there are conflicts on all the requested records.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> Use the <link xlink:href="41d70d89-880f-4850-9d17-19d9790cc8eb">Status Property (ADO Recordset)</link> property to locate records with conflicts.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src37" class="srcSentence">Setting the <legacyBold>Filter</legacyBold> property to a zero-length string ("") has the same effect as using the <legacyBold>adFilterNone</legacyBold> constant.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src38" class="srcSentence">Whenever the <legacyBold>Filter</legacyBold> property is set, the current record position moves to the first record in the filtered subset of records in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> Similarly, when the <legacyBold>Filter</legacyBold> property is cleared, the current record position moves to the first record in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src40" class="srcSentence">When a <legacyBold>Recordset</legacyBold> is filtered based on a field of some variant type (e.g., sql_variant), an error (DISP_E_TYPEMISMATCH or 80020005) will result if the subtypes of the field and filter values used in the criteria string do not match.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> For example, if a <legacyBold>Recordset</legacyBold> object (rs) contains a column (C) of the sql_variant type and a field of this column has been assigned a value of 1 of the I4 type, setting the criteria string of rs.Filter = "C='A'" on the field will produce the error at run time.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> However, rs.Filter = "C=2" applied on the same field will not produce any error although the field will be filtered out of the current record set.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src43" class="srcSentence">See the <link xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark Property (ADO)</link> property for an explanation of bookmark values from which you can build an array to use with the Filter property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src44" class="srcSentence">Only Filters in the form of Criteria Strings (e.g. OrderDate &gt; '12/31/1999') affect the contents of a persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> Filters created with an Array of Bookmarks or using a value from the FilterGroupEnum will not affect the contents of the persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> These rules apply to Recordsets created with either client-side or server-side cursors.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src47" class="srcSentence">When you apply the adFilterPendingRecords flag to a filtered and modified <legacyBold>Recordset</legacyBold> in the batch update mode, the resultant <legacyBold>Recordset</legacyBold> is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values.</caps:sentence>
              <caps:sentence id="src48" class="srcSentence"> The resultant <legacyBold>Recordset</legacyBold> will be non-empty if one of the following is true:</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src49" class="srcSentence">The filtering was based on non-key fields in a single-keyed table.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src50" class="srcSentence">The filtering was based on any fields in a multiple-keyed table.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src51" class="srcSentence">Modifications were made on non-key fields in a single-keyed table.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src52" class="srcSentence">Modifications were made on any fields in a multiple-keyed table.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src53" class="srcSentence">The following table summarizes the effects of <legacyBold>adFilterPendingRecords</legacyBold> in different combinations of filtering and modifications.</caps:sentence>
            <caps:sentence id="src54" class="srcSentence"> The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table.</caps:sentence>
            <caps:sentence id="src55" class="srcSentence"> The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table.</caps:sentence>
            <caps:sentence id="src56" class="srcSentence"> The intersecting cells show the results: + means that applying <legacyBold>adFilterPendingRecords</legacyBold> results in a non-empty <legacyBold>Recordset</legacyBold>; - means an empty <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para> </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Non keys</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">Single Key</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Multiple Keys</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src60" class="srcSentence">Non keys</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">+</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">+</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">+</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src64" class="srcSentence">Single Key</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">+</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">-</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">N/A</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src68" class="srcSentence">Multiple Keys</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">+</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">N/A</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">+</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src72" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object_ADO</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e8bc63c7-8967-438a-9a49-512478a87a15">Filter and RecordCount Properties Example (VB)</link>
        <link xlink:href="b71346cb-3b09-4b8c-a600-976171a1c336">Filter and RecordCount Properties Example (VC++)</link>
        <link xlink:href="16d5d896-9905-4f75-973b-e1e696cd169f">Filter and RecordCount Properties Example (VJ++)</link>
        <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method (ADO)</link>
        <link xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize Property-Dynamic (ADO)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Working with Recordsets"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bdf9a56a-de4a-44de-9111-2f11ab7b16ea
caps.latest.revision: 12
caps.handback.revision: 12
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
# Working with Recordsets
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8d44660e3686ac7101e76bc0a3e5f3cd" id="tgt1" class="tgtSentence">The <legacyBold>Recordset</legacyBold> object has built-in features that let you rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes.</caps:sentence>
          <caps:sentence sentenceid="9c32ee8c07fecbee83f47f1f3e5a7c2b" id="tgt2" class="tgtSentence"> Whether these features are available for use depends on the provider and in some cases — such as that of the <legacyLink xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index</legacyLink> property — the structure of the data source itself.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a427d7017d8c3edf02c47aa600219d48" id="tgt3" class="tgtSentence">Arranging Data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1141547199a57d74d271b5b78abd7fc2" id="tgt4" class="tgtSentence">Frequently, the most efficient way to order the data in your <legacyBold>Recordset</legacyBold> is by specifying an ORDER BY clause in the SQL command used to return results to it.</caps:sentence>
            <caps:sentence sentenceid="970af6d99c87389fc47504191e26eb07" id="tgt5" class="tgtSentence"> However, you might have to change the order of the data in a <legacyBold>Recordset</legacyBold> that has already been created.</caps:sentence>
            <caps:sentence sentenceid="6d6afaa458ebae74969cc143ce742153" id="tgt6" class="tgtSentence"> You can use the <legacyBold>Sort</legacyBold> property to establish the order in which rows of a <legacyBold>Recordset</legacyBold> are traversed.</caps:sentence>
            <caps:sentence sentenceid="9cf214f8c6911b9d908ea4eff82c29b6" id="tgt7" class="tgtSentence"> Additionally, the <legacyBold>Filter</legacyBold> property determines which rows are can be accessed when traversing rows.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0c779a217ade22de34379567965b38ce" id="tgt8" class="tgtSentence">The <legacyBold>Sort</legacyBold> property sets or returns a <legacyBold>String</legacyBold> value that indicates the field names in the <legacyBold>Recordset</legacyBold> on which to sort.</caps:sentence>
            <caps:sentence sentenceid="fca77d57fc727fcbd90f9af9ca980efb" id="tgt9" class="tgtSentence"> Each name is separated by a comma and is optionally followed by a space and the keyword <legacyBold>ASC</legacyBold> (which sorts the field in ascending order) or <legacyBold>DESC</legacyBold> (which sorts the field in descending order).</caps:sentence>
            <caps:sentence sentenceid="d38e14e58622062acad1659334d1ef9b" id="tgt10" class="tgtSentence"> By default, if no keyword is specified, the field is sorted in ascending order.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="998c9219b1d99a2fac022d1dad19dd6f" id="tgt11" class="tgtSentence">The sort operation is efficient because data is not physically rearranged but is accessed in the order specified by an index.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bba19566d78a420f218ef88212e0e53f" id="tgt12" class="tgtSentence">The <legacyBold>Sort</legacyBold> property requires the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to be set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="30465918a14a5f3b49c20656d0718b40" id="tgt13" class="tgtSentence"> A temporary index will be created for each field specified in the <legacyBold>Sort</legacyBold> property if an index does not already exist.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="91ae62640afcf79e497388393cbb03b1" id="tgt14" class="tgtSentence">Setting the <legacyBold>Sort</legacyBold> property to an empty string will reset the rows to their original order and delete temporary indexes.</caps:sentence>
            <caps:sentence sentenceid="f50be024f80b7867ced581d002816f22" id="tgt15" class="tgtSentence"> Existing indexes will not be deleted.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b3427e54779c913dee9afb9ef04339c1" id="tgt16" class="tgtSentence">Suppose a <legacyBold>Recordset</legacyBold> contains three fields named <legacyItalic>firstName</legacyItalic>, <legacyItalic>middleInitial</legacyItalic>, and <legacyItalic>lastName</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="e60f6afad9cf48f8c482767e52b3319c" id="tgt17" class="tgtSentence"> Set the <legacyBold>Sort</legacyBold> property to the string "<codeInline>lastName DESC, firstName ASC</codeInline>", which will order the <legacyBold>Recordset</legacyBold> by last name in descending order and then by first name in ascending order.</caps:sentence>
            <caps:sentence sentenceid="3a43ba2e847c8bd0a870ab39157c5a54" id="tgt18" class="tgtSentence"> The middle initial is ignored.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4a2051941ca98ee850998b2d327bca54" id="tgt19" class="tgtSentence">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords <legacyBold>ASC</legacyBold> and <legacyBold>DESC</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="a25cf24ccaab49b143dc966aead936d4" id="tgt20" class="tgtSentence"> Give a field that has a conflicting name an alias by using the <legacyBold>AS</legacyBold> keyword in the query that returns the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="df87bb7aba23aaf497a014efc93e41cd" id="tgt21" class="tgtSentence">For more information about <legacyBold>Recordset</legacyBold> filtering, see "Filtering the Results" later in this topic.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="31a6b1c5e4a3e866c9bd7305e607ed64" id="tgt22" class="tgtSentence">Finding a Specific Record</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="baa04dd8210cba783e1386de4f6cc971" id="tgt23" class="tgtSentence">ADO provides the <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find</legacyLink> and <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek</legacyLink> methods for locating a particular record in a <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="0da8dfffd38b960c89fd059a51ddbf87" id="tgt24" class="tgtSentence"> The <legacyBold>Find</legacyBold> method is supported by a variety of providers but is limited to a single search criterion.</caps:sentence>
            <caps:sentence sentenceid="1d28c6d87891d3b784119d1b821807ae" id="tgt25" class="tgtSentence"> The <legacyBold>Seek</legacyBold> method supports searching on multiple criteria, but is not supported by many providers.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c437e21933ba7b398da30f659f3b10fe" id="tgt26" class="tgtSentence">Indexes on fields can greatly enhance the performance of the <legacyBold>Find</legacyBold> method and <legacyBold>Sort</legacyBold> and <legacyBold>Filter</legacyBold> properties of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="50097b0711670bb315f8a6a44d34d6f4" id="tgt27" class="tgtSentence"> You can create an internal index for a <legacyBold>Field</legacyBold> object by setting its dynamic <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> property.</caps:sentence>
            <caps:sentence sentenceid="c2114d634250770f7eab7a69d7847342" id="tgt28" class="tgtSentence"> This dynamic property is added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Field</legacyBold> object when you set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="c5edb01d64279a105186123bdbafa9e9" id="tgt29" class="tgtSentence"> Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose.</caps:sentence>
            <caps:sentence sentenceid="695ea588d486808400b17206c45cf8eb" id="tgt30" class="tgtSentence"> Also, this index is distinct from the <legacyLink xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index</legacyLink> property of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4b1c9f150ba8cdad71c9ca072fbf43db" id="tgt31" class="tgtSentence">The <legacyBold>Find</legacyBold> method quickly locates a value within a column (field) of a <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="4ada5394d1b2007c4ef5395d98eff91a" id="tgt32" class="tgtSentence"> You can frequently improve the speed of the <legacyBold>Find</legacyBold> method on a column by using the <legacyBold>Optimize</legacyBold> property to create an index on it.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d2f21db26264a168cf85ddb84a3cdd84" id="tgt33" class="tgtSentence">The <legacyBold>Find</legacyBold> method limits your search to the contents of one field.</caps:sentence>
            <caps:sentence sentenceid="9e9ee6771f333045b171a3a02fb48698" id="tgt34" class="tgtSentence"> The <legacyBold>Seek</legacyBold> method requires that you have an index and has other limitations as well.</caps:sentence>
            <caps:sentence sentenceid="109740ec72221d4a7ceb1f77c88ff328" id="tgt35" class="tgtSentence"> If you must search on multiple fields that are not the basis of an index, or if your provider does not support indexes, you can limit your results by using the <legacyBold>Filter</legacyBold> property of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="ea170e2cafb1337755c8b3d5ae4437f4" id="tgt36" class="tgtSentence">Find</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a47bce07fa06046b2453fd357dde41c4" id="tgt37" class="tgtSentence">The <legacyBold>Find</legacyBold> method searches a <legacyBold>Recordset</legacyBold> for the row that satisfies a specified criterion.</caps:sentence>
                <caps:sentence sentenceid="596d9d87a90aef36eb7c571dd456a94e" id="tgt38" class="tgtSentence"> Optionally, the direction of the search, starting row, and offset from the starting row may be specified.</caps:sentence>
                <caps:sentence sentenceid="4cceec91a90333bf6580a6560ddac49f" id="tgt39" class="tgtSentence"> If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the <legacyBold>Recordset</legacyBold>, depending on search direction.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="910456c7c4654673c6bac1e9675e1611" id="tgt40" class="tgtSentence">Only a single-column name can be specified for the criterion.</caps:sentence>
                <caps:sentence sentenceid="c31bda0dd7fb496602daec32bff868b0" id="tgt41" class="tgtSentence"> In other words, this method does not support multicolumn searches.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="80424e9f3270be7ccc4e88fcef1f8d1d" id="tgt42" class="tgtSentence">The comparison operator for the criterion can be "<legacyBold>&gt;</legacyBold>" (greater than), "<legacyBold>&lt;</legacyBold>" (less than), "=" (equal), "&gt;=" (greater than or equal), "&lt;=" (less than or equal), "&lt;&gt;" (not equal), or "LIKE" (pattern matching).</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b52214a6204935c6ecda5bf08e9b9b34" id="tgt43" class="tgtSentence">The criterion value can be a string, floating-point number, or date.</caps:sentence>
                <caps:sentence sentenceid="300cdff672757be5ac905d78eb3d17d4" id="tgt44" class="tgtSentence"> String values are delimited with single quotation marks or "#" (number sign) marks (for example, "state = 'WA'" or "state = #WA#").</caps:sentence>
                <caps:sentence sentenceid="eb47660444f80cceb50be5df8cc295b2" id="tgt45" class="tgtSentence"> Date values are delimited with "#" (number sign) marks (for example, "start_date &gt; #7/22/97#").</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="967080a1d93fe6d1e62b42fefaba8aa8" id="tgt46" class="tgtSentence">If the comparison operator is "like", the string value can contain an asterisk (*) to find one or more occurrences of any character or substring.</caps:sentence>
                <caps:sentence sentenceid="f368dbfb28ddbc5b723265343fd93cdd" id="tgt47" class="tgtSentence"> For example, "state like 'M*'" matches Maine and Massachusetts.</caps:sentence>
                <caps:sentence sentenceid="a4c1b8b3df03224f51337c2a82be6aa9" id="tgt48" class="tgtSentence"> You can also use leading and trailing asterisks to find a substring that is contained within the values.</caps:sentence>
                <caps:sentence sentenceid="3d7489f29b82cc819812b22e8aceb8ce" id="tgt49" class="tgtSentence"> For example, "state like '*as*'" matches Alaska, Arkansas, and Massachusetts.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="568351b838cd508754383b41ad8df472" id="tgt50" class="tgtSentence">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown earlier.</caps:sentence>
                <caps:sentence sentenceid="4661ae46ce87cbef4025ed1e809679e9" id="tgt51" class="tgtSentence"> You cannot use the asterisk as a leading wildcard ('*str') or embedded wildcard ('s*r').</caps:sentence>
                <caps:sentence sentenceid="e1cd53259983321ab04abc08895a8830" id="tgt52" class="tgtSentence"> This will cause an error.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="edad124fe3b3b56b8e799ccdbd324429" id="tgt53" class="tgtSentence">Seek and Index</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9dad0e423e6a16a08b65899f0eb09b8c" id="tgt54" class="tgtSentence">Use the <legacyBold>Seek</legacyBold> method together with the <legacyBold>Index</legacyBold> property if the underlying provider supports indexes on the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="c2da0c3ca8006a421b6f1cd456542e28" id="tgt55" class="tgtSentence"> Use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink><legacyBold>(adSeek)</legacyBold> method to determine whether the underlying provider supports <legacyBold>Seek</legacyBold>, and the <legacyBold>Supports(adIndex)</legacyBold> method to determine whether the provider supports indexes.</caps:sentence>
                <caps:sentence sentenceid="9e755ccd5c458438fdd5d9baf53faeb2" id="tgt56" class="tgtSentence"> (For example, the <legacyLink xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</legacyLink> supports <legacyBold>Seek</legacyBold> and <legacyBold>Index</legacyBold>.)</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7451c97d2e16828ae1822334a254a26c" id="tgt57" class="tgtSentence">If <legacyBold>Seek</legacyBold> does not find the desired row, no error occurs, and the row is positioned at the end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="d8410c03b7daa8c87ef63bb0d4d2e3c2" id="tgt58" class="tgtSentence"> Set the <legacyBold>Index</legacyBold> property to the desired index before executing this method.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="3184107b314be3e45bcc6ccd5ab61425" id="tgt59" class="tgtSentence">This method is supported only with server-side cursors.</caps:sentence>
                <caps:sentence sentenceid="f41e0fd5813dda8d431658bd54b356f5" id="tgt60" class="tgtSentence"> Seek is not supported when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property value of the <legacyBold>Recordset</legacyBold> object is <legacyBold>adUseClient</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2cb13ce583a81a06dffd0d84cca737bb" id="tgt61" class="tgtSentence">This method can be used only when the <legacyBold>Recordset</legacyBold> object has been opened with a <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> value of <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0ce70f2e7ebd0f90007328253de986f6" id="tgt62" class="tgtSentence">Filtering the Results</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d2f21db26264a168cf85ddb84a3cdd84" id="tgt63" class="tgtSentence">The <legacyBold>Find</legacyBold> method limits your search to the contents of one field.</caps:sentence>
            <caps:sentence sentenceid="9e9ee6771f333045b171a3a02fb48698" id="tgt64" class="tgtSentence"> The <legacyBold>Seek</legacyBold> method requires that you have an index and has other limitations as well.</caps:sentence>
            <caps:sentence sentenceid="0c485dc16a059a916b06788c79e5a30b" id="tgt65" class="tgtSentence"> If you must search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results by using the <legacyBold>Filter</legacyBold> property of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="de267f336de69e2ebae4799ec79b2fdf" id="tgt66" class="tgtSentence">Use the <legacyBold>Filter</legacyBold> property to selectively screen out records in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="84a5013321f9d1460366a1439ca5b958" id="tgt67" class="tgtSentence"> The filtered <legacyBold>Recordset</legacyBold> becomes the current cursor, which means that records that do not satisfy the <legacyBold>Filter</legacyBold> criteria are not available in the <legacyBold>Recordset</legacyBold> until the <legacyBold>Filter</legacyBold> is removed.</caps:sentence>
            <caps:sentence sentenceid="56dcf183ec561c3832b533c2449e55cf" id="tgt68" class="tgtSentence"> Other properties that return values based on the current cursor are affected, such as <legacyBold>AbsolutePosition</legacyBold>, <legacyBold>AbsolutePage</legacyBold>, <legacyBold>RecordCount</legacyBold>, and <legacyBold>PageCount</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="55845f031ad22cbd51a6d2d49c590b1b" id="tgt69" class="tgtSentence"> This is because setting the <legacyBold>Filter</legacyBold> property to a specific value will move the current record to the first record that satisfies the new value.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cb06e15201c02eb98cf7b353d6caf4bb" id="tgt70" class="tgtSentence">The <legacyBold>Filter</legacyBold> property takes a variant argument.</caps:sentence>
            <caps:sentence sentenceid="ad951687ef9c9cfcdb1284d0c1c99647" id="tgt71" class="tgtSentence"> This value represents one of three methods for using the <legacyBold>Filter</legacyBold> property: a criteria string, a <legacyBold>FilterGroupEnum</legacyBold> constant, or an array of bookmarks.</caps:sentence>
            <caps:sentence sentenceid="eb92796da139d0fc86c12739e1966659" id="tgt72" class="tgtSentence"> For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="0d8d5566e08f116ea385b14bf9601551" id="tgt73" class="tgtSentence">When you know the data that you want to select, it is usually more efficient to open a <legacyBold>Recordset</legacyBold> with an SQL statement that effectively filters the result set, instead of relying on the <legacyBold>Filter</legacyBold> property.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="480bf83e8208c5b8b503ba80a1a72d9c" id="tgt74" class="tgtSentence">To remove a filter from a <legacyBold>Recordset</legacyBold>, use the <legacyBold>adFilterNone</legacyBold> constant.</caps:sentence>
            <caps:sentence sentenceid="720fad4896ecf777a033de12e62e4f1b" id="tgt75" class="tgtSentence"> Setting the <legacyBold>Filter</legacyBold> property to a zero-length string ("") has the same effect as using the <legacyBold>adFilterNone</legacyBold> constant.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="1557015f4db11b6b8cd99f17c3fc126c" id="tgt76" class="tgtSentence">Filtering with a Criteria String</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="eec8ccbf592c2d3453f9c8f3c803aa1c" id="tgt77" class="tgtSentence">The criteria string consists of clauses in the form <legacyItalic>FieldName Operator Value</legacyItalic> (for example, <codeInline>"LastName = 'Smith'"</codeInline>).</caps:sentence>
                <caps:sentence sentenceid="edb6e7b35bac391cfa744db641ae5926" id="tgt78" class="tgtSentence"> You can create compound clauses by concatenating individual clauses with <languageKeyword>AND</languageKeyword> (for example, <codeInline>"LastName = 'Smith' AND FirstName = 'John'"</codeInline>) and<languageKeyword> OR </languageKeyword>(for example, <codeInline>"LastName = 'Smith' OR LastName = 'Jones'"</codeInline>).</caps:sentence>
                <caps:sentence sentenceid="d560792cbf3de4464c07b312f6b0696a" id="tgt79" class="tgtSentence"> Use the following guidelines for criteria strings:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c879d47a224889b57428f5af8bd66ca3" id="tgt80" class="tgtSentence">
                      <legacyItalic>FieldName</legacyItalic> must be a valid field name from the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="9e1c645376798c904c75488b09352567" id="tgt81" class="tgtSentence"> If the field name contains spaces, you must enclose the name in square brackets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2af31bfacf45dc724ac393315ed945b9" id="tgt82" class="tgtSentence">
                      <legacyItalic>Operator</legacyItalic> must be one of the following: <languageKeyword>&lt;</languageKeyword>, <languageKeyword>&gt;</languageKeyword>, <languageKeyword>&lt;=</languageKeyword>, <languageKeyword>&gt;=</languageKeyword>, <languageKeyword>&lt;&gt;</languageKeyword>, <languageKeyword>=</languageKeyword>, or <languageKeyword>LIKE</languageKeyword>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="037c701026d06f6b5cffe8e037056b6d" id="tgt83" class="tgtSentence">
                      <legacyItalic>Value</legacyItalic> is the value with which you will compare the field values (for example, <codeInline>'Smith'</codeInline>, <codeInline>#8/24/95#</codeInline>, <codeInline>12.345</codeInline>, or <codeInline>$50.00</codeInline>).</caps:sentence>
                    <caps:sentence sentenceid="ae6c7f85264c7213ac2bcb878d3780a8" id="tgt84" class="tgtSentence"> Use single quotation marks (') with strings and pound signs (<codeInline>#</codeInline>) with dates.</caps:sentence>
                    <caps:sentence sentenceid="af3da72ab39086363b0390de7fd48a79" id="tgt85" class="tgtSentence"> For numbers, you can use decimal points, dollar signs, and scientific notation.</caps:sentence>
                    <caps:sentence sentenceid="b3bbe68868a6554b21fc984e5a01c975" id="tgt86" class="tgtSentence"> If <legacyItalic>Operator</legacyItalic> is <languageKeyword>LIKE</languageKeyword>, <legacyItalic>Value</legacyItalic> can use wildcard characters.</caps:sentence>
                    <caps:sentence sentenceid="52d6e29972348968208984c0c146c65c" id="tgt87" class="tgtSentence"> Only the asterisk (*) and percent sign (%) wildcard characters are allowed, and they must be the last character in the string.</caps:sentence>
                    <caps:sentence sentenceid="654f272a59a3c54b488f60ceedc61d35" id="tgt88" class="tgtSentence">
                      <legacyItalic>Value</legacyItalic> cannot be null.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="101dfd6941567a780ea0697702432f19" id="tgt89" class="tgtSentence">To include single quotation marks (') in the filter <legacyItalic>Value</legacyItalic>, use two single quotation marks to represent one.</caps:sentence>
                      <caps:sentence sentenceid="9ef01afd6812b1330a4e5f09720b4f23" id="tgt90" class="tgtSentence"> For example, to filter on <legacyItalic>O'Malley</legacyItalic>, the criteria string should be <codeInline>"col1 = 'O''Malley'"</codeInline>.</caps:sentence>
                      <caps:sentence sentenceid="d23edcd1f78a169d0760dc628eead09e" id="tgt91" class="tgtSentence"> To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</caps:sentence>
                      <caps:sentence sentenceid="aea0e500fcfe56ab780ebed8bf9ddbbd" id="tgt92" class="tgtSentence"> For example, to filter on <legacyItalic>'1'</legacyItalic>, the criteria string should be <codeInline>"col1 = #'1'#"</codeInline>.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="052d97bd44538e90ae5842a6f9939ca8" id="tgt93" class="tgtSentence">There is no precedence between <languageKeyword>AND</languageKeyword> and <languageKeyword>OR</languageKeyword>.</caps:sentence>
                <caps:sentence sentenceid="f1d9c46cdcfd93850b33eb92610d1bde" id="tgt94" class="tgtSentence"> Clauses can be grouped within parentheses.</caps:sentence>
                <caps:sentence sentenceid="7f93dd23f1cf324ef08718f5d42cd8ed" id="tgt95" class="tgtSentence"> However, you cannot group clauses joined by an <languageKeyword>OR</languageKeyword> and then join the group to another clause with an AND, as follows.</caps:sentence>
              </para>
              <code>(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'</code>
              <para>
                <caps:sentence sentenceid="01a59563008a83faf53869853e3b99de" id="tgt96" class="tgtSentence">Instead, you would construct this filter as follows.</caps:sentence>
              </para>
              <code>(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')</code>
              <para>
                <caps:sentence sentenceid="f373e701a1ba6c456a4332efe4cd96c7" id="tgt97" class="tgtSentence">In a <languageKeyword>LIKE</languageKeyword> clause, you can use a wildcard at the beginning and end of the pattern (for example,<codeInline> LastName Like '*mit*'</codeInline>) or only at the end of the pattern (for example, <codeInline>LastName Like 'Smit*'</codeInline>).</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="5c29b43c1d56cf4cc4dd1fe11358b2b8" id="tgt98" class="tgtSentence">Filtering with a Constant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="58089835f83931a27c538c71838ca1a0" id="tgt99" class="tgtSentence">The following constants are available for filtering <legacyBold>Recordsets</legacyBold>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt100" class="tgtSentence">Constant</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt101" class="tgtSentence">Description</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b8d539c28e1829648a808816f84d19c6" id="tgt102" class="tgtSentence">
                          <legacyBold>adFilterAffectedRecords</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3b381e279c5af5fdb4f5a5d5b801797a" id="tgt103" class="tgtSentence">Filters for viewing only records affected by the last <legacyBold>Delete</legacyBold>, <legacyBold>Resync</legacyBold>, <legacyBold>UpdateBatch</legacyBold>, or <legacyBold>CancelBatch</legacyBold> call.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4bc1adc9b7a6744f3f8e64254da7d0e1" id="tgt104" class="tgtSentence">
                          <legacyBold>adFilterConflictingRecords</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="83e8e3cc58970e86f91b20cd0093682b" id="tgt105" class="tgtSentence">Filters for viewing the records that failed the last batch update.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="adafb4e096b7e53eb4864cbd8a515b6a" id="tgt106" class="tgtSentence">
                          <legacyBold>adFilterFetchedRecords</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9f2c9a1206064309fc69f281655c620b" id="tgt107" class="tgtSentence">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fb01b22c911fe16b75ab3c575323b6bb" id="tgt108" class="tgtSentence">
                          <legacyBold>adFilterNone</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="81d05a51f063816f8ccc4b006352c420" id="tgt109" class="tgtSentence">Removes the current filter and restores all records for viewing.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="af5911e37491558df034653b0a10ce4b" id="tgt110" class="tgtSentence">
                          <legacyBold>adFilterPendingRecords</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="aeb1fdc1f9791a49499ab760b28ebfcd" id="tgt111" class="tgtSentence">Filters for viewing only records that have changed but have not yet been sent to the server.</caps:sentence>
                        <caps:sentence sentenceid="6431ab163aa327a213f2bf0178c11263" id="tgt112" class="tgtSentence"> Applicable only for batch update mode.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="876b7d4fd8b3d02d976790ac6dea319d" id="tgt113" class="tgtSentence">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last <legacyBold>UpdateBatch</legacyBold> method call, as shown in the following example.</caps:sentence>
              </para>
              <para>
                <codeInline>Attribute VB_Name = "modExaminingData"</codeInline>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="1b0a7379a138820bb2f5edadfec48dd3" id="tgt114" class="tgtSentence">Filtering with Bookmarks</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e406dd20ec148067696c3f65329827a5" id="tgt115" class="tgtSentence">Finally, you can pass a variant array of bookmarks to the <legacyBold>Filter</legacyBold> property.</caps:sentence>
                <caps:sentence sentenceid="4670c0c95c03d13b41670abcb5130fbf" id="tgt116" class="tgtSentence"> The resulting cursor will contain only those records whose bookmark was passed in to the property.</caps:sentence>
                <caps:sentence sentenceid="731671faa1dbac15e1708fc7305631b5" id="tgt117" class="tgtSentence"> The following code example creates an array of bookmarks from the records in a <legacyBold>Recordset</legacyBold> which have a "B" in the <legacyItalic>ProductName</legacyItalic> field.</caps:sentence>
                <caps:sentence sentenceid="fb19a06f51d3405e15163caaf55d1f51" id="tgt118" class="tgtSentence"> It then passes the array to the <legacyBold>Filter</legacyBold> property and displays information about the resulting filtered <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
              <code>    'BeginFilterBkmk
    Dim vBkmkArray() As Variant
    Dim i As Integer

    'Recordset created using "SELECT * FROM Products" as command.
    'So, we will check to see if ProductName has a capital B, and
    'if so, add to the array.
    i = 0
    Do While Not objRs.EOF
        If InStr(1, objRs("ProductName"), "B") Then
            ReDim Preserve vBkmkArray(i)
            vBkmkArray(i) = objRs.Bookmark
            i = i + 1
            Debug.Print objRs("ProductName")
        End If
        objRs.MoveNext
    Loop
    
    'Filter using the array of bookmarks.
    objRs.Filter = vBkmkArray
    
    objRs.MoveFirst
    Do While Not objRs.EOF
        Debug.Print objRs("ProductName")
        objRs.MoveNext
    Loop
    'EndFilterBkmk</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="84fc1b99c5392f1d7c712750a0e14cf1" id="tgt119" class="tgtSentence">Creating a Clone of a Recordset</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="55806e3581713e1e5f8c53306e79d20e" id="tgt120" class="tgtSentence">Use the <legacyBold>Clone</legacyBold> method to create multiple, duplicate <legacyBold>Recordset</legacyBold> objects, especially if you want to maintain more than one current record in a given set of records.</caps:sentence>
            <caps:sentence sentenceid="5908c75efe02db75cc8069f235591021" id="tgt121" class="tgtSentence"> Using the <legacyBold>Clone</legacyBold> method is more efficient than creating and opening a new <legacyBold>Recordset</legacyBold> object with the same definition as the original.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="16d6346514553e24e7f942d7ee83e1a5" id="tgt122" class="tgtSentence">The current record of a newly created clone is originally set to the first record.</caps:sentence>
            <caps:sentence sentenceid="7559a7bb81dbb132d79cb9121220e24b" id="tgt123" class="tgtSentence"> The current record pointer in a cloned <legacyBold>Recordset</legacyBold> is not synchronized with the original or vice versa.</caps:sentence>
            <caps:sentence sentenceid="4af8b42e47bdb0fa314d5a7aec17875e" id="tgt124" class="tgtSentence"> You can navigate independently in each <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2d043c07712a0ebc40313ab9daf051db" id="tgt125" class="tgtSentence">Changes you make to one <legacyBold>Recordset</legacyBold> object are visible in all of its clones regardless of cursor type.</caps:sentence>
            <caps:sentence sentenceid="ebdff9f9c2970e70a975021aed19d0ba" id="tgt126" class="tgtSentence"> However, after you execute <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> on the original <legacyBold>Recordset</legacyBold>, the clones will no longer be synchronized to the original.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="27401fb381692f47fbb70743909c05b6" id="tgt127" class="tgtSentence">Closing the original <legacyBold>Recordset</legacyBold> does not close its copies, nor does closing a copy close the original or any of the other copies.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4d4be11f2965cda273b1e6bafc171efb" id="tgt128" class="tgtSentence">You can clone a <legacyBold>Recordset</legacyBold> object only if it supports bookmarks.</caps:sentence>
            <caps:sentence sentenceid="49bc06483929df883e64b4208205ab13" id="tgt129" class="tgtSentence"> Bookmark values are interchangeable; that is, a bookmark reference from one <legacyBold>Recordset</legacyBold> object refers to the same record in any of its clones.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>Recordset</legacyBold> object has built-in features that let you rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Whether these features are available for use depends on the provider and in some cases — such as that of the <legacyLink xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index</legacyLink> property — the structure of the data source itself.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Arranging Data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Frequently, the most efficient way to order the data in your <legacyBold>Recordset</legacyBold> is by specifying an ORDER BY clause in the SQL command used to return results to it.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> However, you might have to change the order of the data in a <legacyBold>Recordset</legacyBold> that has already been created.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> You can use the <legacyBold>Sort</legacyBold> property to establish the order in which rows of a <legacyBold>Recordset</legacyBold> are traversed.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Additionally, the <legacyBold>Filter</legacyBold> property determines which rows are can be accessed when traversing rows.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">The <legacyBold>Sort</legacyBold> property sets or returns a <legacyBold>String</legacyBold> value that indicates the field names in the <legacyBold>Recordset</legacyBold> on which to sort.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Each name is separated by a comma and is optionally followed by a space and the keyword <legacyBold>ASC</legacyBold> (which sorts the field in ascending order) or <legacyBold>DESC</legacyBold> (which sorts the field in descending order).</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> By default, if no keyword is specified, the field is sorted in ascending order.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">The sort operation is efficient because data is not physically rearranged but is accessed in the order specified by an index.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">The <legacyBold>Sort</legacyBold> property requires the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to be set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> A temporary index will be created for each field specified in the <legacyBold>Sort</legacyBold> property if an index does not already exist.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">Setting the <legacyBold>Sort</legacyBold> property to an empty string will reset the rows to their original order and delete temporary indexes.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Existing indexes will not be deleted.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">Suppose a <legacyBold>Recordset</legacyBold> contains three fields named <legacyItalic>firstName</legacyItalic>, <legacyItalic>middleInitial</legacyItalic>, and <legacyItalic>lastName</legacyItalic>.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Set the <legacyBold>Sort</legacyBold> property to the string "<codeInline>lastName DESC, firstName ASC</codeInline>", which will order the <legacyBold>Recordset</legacyBold> by last name in descending order and then by first name in ascending order.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> The middle initial is ignored.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords <legacyBold>ASC</legacyBold> and <legacyBold>DESC</legacyBold>.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Give a field that has a conflicting name an alias by using the <legacyBold>AS</legacyBold> keyword in the query that returns the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">For more information about <legacyBold>Recordset</legacyBold> filtering, see "Filtering the Results" later in this topic.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Finding a Specific Record</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src23" class="srcSentence">ADO provides the <legacyLink xlink:href="55c9810a-d8ca-46c2-a9dc-80e7ee7aa188">Find</legacyLink> and <legacyLink xlink:href="129293d2-19d3-4940-bf64-483ee72fb4a1">Seek</legacyLink> methods for locating a particular record in a <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> The <legacyBold>Find</legacyBold> method is supported by a variety of providers but is limited to a single search criterion.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> The <legacyBold>Seek</legacyBold> method supports searching on multiple criteria, but is not supported by many providers.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src26" class="srcSentence">Indexes on fields can greatly enhance the performance of the <legacyBold>Find</legacyBold> method and <legacyBold>Sort</legacyBold> and <legacyBold>Filter</legacyBold> properties of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> You can create an internal index for a <legacyBold>Field</legacyBold> object by setting its dynamic <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink> property.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> This dynamic property is added to the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Field</legacyBold> object when you set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence id="src29" class="srcSentence"> Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> Also, this index is distinct from the <legacyLink xlink:href="1c79e271-21ec-41a8-8163-c5e89f0001a7">Index</legacyLink> property of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src31" class="srcSentence">The <legacyBold>Find</legacyBold> method quickly locates a value within a column (field) of a <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence"> You can frequently improve the speed of the <legacyBold>Find</legacyBold> method on a column by using the <legacyBold>Optimize</legacyBold> property to create an index on it.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src33" class="srcSentence">The <legacyBold>Find</legacyBold> method limits your search to the contents of one field.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> The <legacyBold>Seek</legacyBold> method requires that you have an index and has other limitations as well.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> If you must search on multiple fields that are not the basis of an index, or if your provider does not support indexes, you can limit your results by using the <legacyBold>Filter</legacyBold> property of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src36" class="srcSentence">Find</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src37" class="srcSentence">The <legacyBold>Find</legacyBold> method searches a <legacyBold>Recordset</legacyBold> for the row that satisfies a specified criterion.</caps:sentence>
                <caps:sentence id="src38" class="srcSentence"> Optionally, the direction of the search, starting row, and offset from the starting row may be specified.</caps:sentence>
                <caps:sentence id="src39" class="srcSentence"> If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the <legacyBold>Recordset</legacyBold>, depending on search direction.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src40" class="srcSentence">Only a single-column name can be specified for the criterion.</caps:sentence>
                <caps:sentence id="src41" class="srcSentence"> In other words, this method does not support multicolumn searches.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src42" class="srcSentence">The comparison operator for the criterion can be "<legacyBold>&gt;</legacyBold>" (greater than), "<legacyBold>&lt;</legacyBold>" (less than), "=" (equal), "&gt;=" (greater than or equal), "&lt;=" (less than or equal), "&lt;&gt;" (not equal), or "LIKE" (pattern matching).</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src43" class="srcSentence">The criterion value can be a string, floating-point number, or date.</caps:sentence>
                <caps:sentence id="src44" class="srcSentence"> String values are delimited with single quotation marks or "#" (number sign) marks (for example, "state = 'WA'" or "state = #WA#").</caps:sentence>
                <caps:sentence id="src45" class="srcSentence"> Date values are delimited with "#" (number sign) marks (for example, "start_date &gt; #7/22/97#").</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src46" class="srcSentence">If the comparison operator is "like", the string value can contain an asterisk (*) to find one or more occurrences of any character or substring.</caps:sentence>
                <caps:sentence id="src47" class="srcSentence"> For example, "state like 'M*'" matches Maine and Massachusetts.</caps:sentence>
                <caps:sentence id="src48" class="srcSentence"> You can also use leading and trailing asterisks to find a substring that is contained within the values.</caps:sentence>
                <caps:sentence id="src49" class="srcSentence"> For example, "state like '*as*'" matches Alaska, Arkansas, and Massachusetts.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src50" class="srcSentence">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown earlier.</caps:sentence>
                <caps:sentence id="src51" class="srcSentence"> You cannot use the asterisk as a leading wildcard ('*str') or embedded wildcard ('s*r').</caps:sentence>
                <caps:sentence id="src52" class="srcSentence"> This will cause an error.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src53" class="srcSentence">Seek and Index</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src54" class="srcSentence">Use the <legacyBold>Seek</legacyBold> method together with the <legacyBold>Index</legacyBold> property if the underlying provider supports indexes on the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence id="src55" class="srcSentence"> Use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink><legacyBold>(adSeek)</legacyBold> method to determine whether the underlying provider supports <legacyBold>Seek</legacyBold>, and the <legacyBold>Supports(adIndex)</legacyBold> method to determine whether the provider supports indexes.</caps:sentence>
                <caps:sentence id="src56" class="srcSentence"> (For example, the <legacyLink xlink:href="fd956da1-5203-40af-aa7e-fc13a6c6581f">OLE DB Provider for Microsoft Jet</legacyLink> supports <legacyBold>Seek</legacyBold> and <legacyBold>Index</legacyBold>.)</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src57" class="srcSentence">If <legacyBold>Seek</legacyBold> does not find the desired row, no error occurs, and the row is positioned at the end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src58" class="srcSentence"> Set the <legacyBold>Index</legacyBold> property to the desired index before executing this method.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src59" class="srcSentence">This method is supported only with server-side cursors.</caps:sentence>
                <caps:sentence id="src60" class="srcSentence"> Seek is not supported when the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property value of the <legacyBold>Recordset</legacyBold> object is <legacyBold>adUseClient</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src61" class="srcSentence">This method can be used only when the <legacyBold>Recordset</legacyBold> object has been opened with a <legacyLink xlink:href="4b1feb9c-a855-40fe-a906-efe688687e9f">CommandTypeEnum</legacyLink> value of <legacyBold>adCmdTableDirect</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src62" class="srcSentence">Filtering the Results</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src63" class="srcSentence">The <legacyBold>Find</legacyBold> method limits your search to the contents of one field.</caps:sentence>
            <caps:sentence id="src64" class="srcSentence"> The <legacyBold>Seek</legacyBold> method requires that you have an index and has other limitations as well.</caps:sentence>
            <caps:sentence id="src65" class="srcSentence"> If you must search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results by using the <legacyBold>Filter</legacyBold> property of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src66" class="srcSentence">Use the <legacyBold>Filter</legacyBold> property to selectively screen out records in a <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src67" class="srcSentence"> The filtered <legacyBold>Recordset</legacyBold> becomes the current cursor, which means that records that do not satisfy the <legacyBold>Filter</legacyBold> criteria are not available in the <legacyBold>Recordset</legacyBold> until the <legacyBold>Filter</legacyBold> is removed.</caps:sentence>
            <caps:sentence id="src68" class="srcSentence"> Other properties that return values based on the current cursor are affected, such as <legacyBold>AbsolutePosition</legacyBold>, <legacyBold>AbsolutePage</legacyBold>, <legacyBold>RecordCount</legacyBold>, and <legacyBold>PageCount</legacyBold>.</caps:sentence>
            <caps:sentence id="src69" class="srcSentence"> This is because setting the <legacyBold>Filter</legacyBold> property to a specific value will move the current record to the first record that satisfies the new value.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src70" class="srcSentence">The <legacyBold>Filter</legacyBold> property takes a variant argument.</caps:sentence>
            <caps:sentence id="src71" class="srcSentence"> This value represents one of three methods for using the <legacyBold>Filter</legacyBold> property: a criteria string, a <legacyBold>FilterGroupEnum</legacyBold> constant, or an array of bookmarks.</caps:sentence>
            <caps:sentence id="src72" class="srcSentence"> For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src73" class="srcSentence">When you know the data that you want to select, it is usually more efficient to open a <legacyBold>Recordset</legacyBold> with an SQL statement that effectively filters the result set, instead of relying on the <legacyBold>Filter</legacyBold> property.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src74" class="srcSentence">To remove a filter from a <legacyBold>Recordset</legacyBold>, use the <legacyBold>adFilterNone</legacyBold> constant.</caps:sentence>
            <caps:sentence id="src75" class="srcSentence"> Setting the <legacyBold>Filter</legacyBold> property to a zero-length string ("") has the same effect as using the <legacyBold>adFilterNone</legacyBold> constant.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src76" class="srcSentence">Filtering with a Criteria String</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src77" class="srcSentence">The criteria string consists of clauses in the form <legacyItalic>FieldName Operator Value</legacyItalic> (for example, <codeInline>"LastName = 'Smith'"</codeInline>).</caps:sentence>
                <caps:sentence id="src78" class="srcSentence"> You can create compound clauses by concatenating individual clauses with <languageKeyword>AND</languageKeyword> (for example, <codeInline>"LastName = 'Smith' AND FirstName = 'John'"</codeInline>) and<languageKeyword> OR </languageKeyword>(for example, <codeInline>"LastName = 'Smith' OR LastName = 'Jones'"</codeInline>).</caps:sentence>
                <caps:sentence id="src79" class="srcSentence"> Use the following guidelines for criteria strings:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">
                      <legacyItalic>FieldName</legacyItalic> must be a valid field name from the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                    <caps:sentence id="src81" class="srcSentence"> If the field name contains spaces, you must enclose the name in square brackets.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">
                      <legacyItalic>Operator</legacyItalic> must be one of the following: <languageKeyword>&lt;</languageKeyword>, <languageKeyword>&gt;</languageKeyword>, <languageKeyword>&lt;=</languageKeyword>, <languageKeyword>&gt;=</languageKeyword>, <languageKeyword>&lt;&gt;</languageKeyword>, <languageKeyword>=</languageKeyword>, or <languageKeyword>LIKE</languageKeyword>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">
                      <legacyItalic>Value</legacyItalic> is the value with which you will compare the field values (for example, <codeInline>'Smith'</codeInline>, <codeInline>#8/24/95#</codeInline>, <codeInline>12.345</codeInline>, or <codeInline>$50.00</codeInline>).</caps:sentence>
                    <caps:sentence id="src84" class="srcSentence"> Use single quotation marks (') with strings and pound signs (<codeInline>#</codeInline>) with dates.</caps:sentence>
                    <caps:sentence id="src85" class="srcSentence"> For numbers, you can use decimal points, dollar signs, and scientific notation.</caps:sentence>
                    <caps:sentence id="src86" class="srcSentence"> If <legacyItalic>Operator</legacyItalic> is <languageKeyword>LIKE</languageKeyword>, <legacyItalic>Value</legacyItalic> can use wildcard characters.</caps:sentence>
                    <caps:sentence id="src87" class="srcSentence"> Only the asterisk (*) and percent sign (%) wildcard characters are allowed, and they must be the last character in the string.</caps:sentence>
                    <caps:sentence id="src88" class="srcSentence">
                      <legacyItalic>Value</legacyItalic> cannot be null.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src89" class="srcSentence">To include single quotation marks (') in the filter <legacyItalic>Value</legacyItalic>, use two single quotation marks to represent one.</caps:sentence>
                      <caps:sentence id="src90" class="srcSentence"> For example, to filter on <legacyItalic>O'Malley</legacyItalic>, the criteria string should be <codeInline>"col1 = 'O''Malley'"</codeInline>.</caps:sentence>
                      <caps:sentence id="src91" class="srcSentence"> To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</caps:sentence>
                      <caps:sentence id="src92" class="srcSentence"> For example, to filter on <legacyItalic>'1'</legacyItalic>, the criteria string should be <codeInline>"col1 = #'1'#"</codeInline>.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src93" class="srcSentence">There is no precedence between <languageKeyword>AND</languageKeyword> and <languageKeyword>OR</languageKeyword>.</caps:sentence>
                <caps:sentence id="src94" class="srcSentence"> Clauses can be grouped within parentheses.</caps:sentence>
                <caps:sentence id="src95" class="srcSentence"> However, you cannot group clauses joined by an <languageKeyword>OR</languageKeyword> and then join the group to another clause with an AND, as follows.</caps:sentence>
              </para>
              <code>(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'</code>
              <para>
                <caps:sentence id="src96" class="srcSentence">Instead, you would construct this filter as follows.</caps:sentence>
              </para>
              <code>(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')</code>
              <para>
                <caps:sentence id="src97" class="srcSentence">In a <languageKeyword>LIKE</languageKeyword> clause, you can use a wildcard at the beginning and end of the pattern (for example,<codeInline> LastName Like '*mit*'</codeInline>) or only at the end of the pattern (for example, <codeInline>LastName Like 'Smit*'</codeInline>).</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src98" class="srcSentence">Filtering with a Constant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src99" class="srcSentence">The following constants are available for filtering <legacyBold>Recordsets</legacyBold>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">Constant</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">Description</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">
                          <legacyBold>adFilterAffectedRecords</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src103" class="srcSentence">Filters for viewing only records affected by the last <legacyBold>Delete</legacyBold>, <legacyBold>Resync</legacyBold>, <legacyBold>UpdateBatch</legacyBold>, or <legacyBold>CancelBatch</legacyBold> call.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">
                          <legacyBold>adFilterConflictingRecords</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">Filters for viewing the records that failed the last batch update.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">
                          <legacyBold>adFilterFetchedRecords</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src108" class="srcSentence">
                          <legacyBold>adFilterNone</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src109" class="srcSentence">Removes the current filter and restores all records for viewing.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">
                          <legacyBold>adFilterPendingRecords</legacyBold>                 </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src111" class="srcSentence">Filters for viewing only records that have changed but have not yet been sent to the server.</caps:sentence>
                        <caps:sentence id="src112" class="srcSentence"> Applicable only for batch update mode.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src113" class="srcSentence">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last <legacyBold>UpdateBatch</legacyBold> method call, as shown in the following example.</caps:sentence>
              </para>
              <para>
                <codeInline>Attribute VB_Name = "modExaminingData"</codeInline>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src114" class="srcSentence">Filtering with Bookmarks</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src115" class="srcSentence">Finally, you can pass a variant array of bookmarks to the <legacyBold>Filter</legacyBold> property.</caps:sentence>
                <caps:sentence id="src116" class="srcSentence"> The resulting cursor will contain only those records whose bookmark was passed in to the property.</caps:sentence>
                <caps:sentence id="src117" class="srcSentence"> The following code example creates an array of bookmarks from the records in a <legacyBold>Recordset</legacyBold> which have a "B" in the <legacyItalic>ProductName</legacyItalic> field.</caps:sentence>
                <caps:sentence id="src118" class="srcSentence"> It then passes the array to the <legacyBold>Filter</legacyBold> property and displays information about the resulting filtered <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
              <code>    'BeginFilterBkmk
    Dim vBkmkArray() As Variant
    Dim i As Integer

    'Recordset created using "SELECT * FROM Products" as command.
    'So, we will check to see if ProductName has a capital B, and
    'if so, add to the array.
    i = 0
    Do While Not objRs.EOF
        If InStr(1, objRs("ProductName"), "B") Then
            ReDim Preserve vBkmkArray(i)
            vBkmkArray(i) = objRs.Bookmark
            i = i + 1
            Debug.Print objRs("ProductName")
        End If
        objRs.MoveNext
    Loop
    
    'Filter using the array of bookmarks.
    objRs.Filter = vBkmkArray
    
    objRs.MoveFirst
    Do While Not objRs.EOF
        Debug.Print objRs("ProductName")
        objRs.MoveNext
    Loop
    'EndFilterBkmk</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src119" class="srcSentence">Creating a Clone of a Recordset</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src120" class="srcSentence">Use the <legacyBold>Clone</legacyBold> method to create multiple, duplicate <legacyBold>Recordset</legacyBold> objects, especially if you want to maintain more than one current record in a given set of records.</caps:sentence>
            <caps:sentence id="src121" class="srcSentence"> Using the <legacyBold>Clone</legacyBold> method is more efficient than creating and opening a new <legacyBold>Recordset</legacyBold> object with the same definition as the original.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src122" class="srcSentence">The current record of a newly created clone is originally set to the first record.</caps:sentence>
            <caps:sentence id="src123" class="srcSentence"> The current record pointer in a cloned <legacyBold>Recordset</legacyBold> is not synchronized with the original or vice versa.</caps:sentence>
            <caps:sentence id="src124" class="srcSentence"> You can navigate independently in each <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src125" class="srcSentence">Changes you make to one <legacyBold>Recordset</legacyBold> object are visible in all of its clones regardless of cursor type.</caps:sentence>
            <caps:sentence id="src126" class="srcSentence"> However, after you execute <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> on the original <legacyBold>Recordset</legacyBold>, the clones will no longer be synchronized to the original.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src127" class="srcSentence">Closing the original <legacyBold>Recordset</legacyBold> does not close its copies, nor does closing a copy close the original or any of the other copies.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src128" class="srcSentence">You can clone a <legacyBold>Recordset</legacyBold> object only if it supports bookmarks.</caps:sentence>
            <caps:sentence id="src129" class="srcSentence"> Bookmark values are interchangeable; that is, a bookmark reference from one <legacyBold>Recordset</legacyBold> object refers to the same record in any of its clones.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
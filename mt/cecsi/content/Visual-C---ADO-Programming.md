---
title: "Visual C++ ADO Programming"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 11233b96-e05c-4221-9aed-5f20944b0f1c
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
# Visual C++ ADO Programming
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9b96c2b5e528ae05c4bc46a1f3a7e41a" id="tgt1" class="tgtSentence">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</caps:sentence>
          <caps:sentence sentenceid="c8477bfbd7b25c398fb6ac02f54227ef" id="tgt2" class="tgtSentence"> Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the <legacyBold>#import</legacyBold> directive), and Visual J++ (with the ADO/WFC class package).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0d1a88e3cab1d528f2b3104bcb420aaa" id="tgt3" class="tgtSentence">To accommodate this diversity, the <legacyLink xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">ADO for Visual C++ Syntax Indexes</legacyLink> provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e088a0975cc749c0ff0dab1b28e8b448" id="tgt4" class="tgtSentence">ADO is implemented with COM (Component Object Model) interfaces.</caps:sentence>
          <caps:sentence sentenceid="d31ec01abc7ac12a82b0173b21dcf37e" id="tgt5" class="tgtSentence"> However, it is easier for programmers to work with COM in certain programming languages than others.</caps:sentence>
          <caps:sentence sentenceid="c427c47345acc1b77c7c05d9ddfe01d4" id="tgt6" class="tgtSentence"> For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1dd1a07dec1077ab5dff1dea97eac38b" id="tgt7" class="tgtSentence">The following sections summarize details for C and C++ programmers using ADO and the <legacyBold>#import</legacyBold> directive.</caps:sentence>
          <caps:sentence sentenceid="77fa7dc8b8e1a2a39cb1a79a1312e835" id="tgt8" class="tgtSentence"> It focuses on data types specific to COM (<legacyBold>Variant</legacyBold>, <legacyBold>BSTR</legacyBold>, and <legacyBold>SafeArray</legacyBold>), and error handling (_com_error).</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="e454308352b1877a9793913c26a08446" id="tgt9" class="tgtSentence">Using the #import Compiler Directive</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="af463472556c3a781b2b2601c4202d56" id="tgt10" class="tgtSentence">The <legacyBold>#import</legacyBold> Visual C++ compiler directive simplifies working with the ADO methods and properties.</caps:sentence>
            <caps:sentence sentenceid="9dbebb161bdd25aee967362406763736" id="tgt11" class="tgtSentence"> The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</caps:sentence>
            <caps:sentence sentenceid="a025efa983be076c4f1be78559d2314b" id="tgt12" class="tgtSentence"> Each interface is encapsulated, or wrapped, in a class.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4656536c4fb941ad3af103bcfab7c400" id="tgt13" class="tgtSentence">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully.</caps:sentence>
            <caps:sentence sentenceid="5e2e27ed7450f18786d9ff13ca63a289" id="tgt14" class="tgtSentence"> If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="17f9909d9dd59968f39de8fe5f0e15f0" id="tgt15" class="tgtSentence">Operations that retrieve the value of a property have names of the form, <legacyBold>Get</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="7c746cc4ff204735cf9093c6f125287b" id="tgt16" class="tgtSentence"> Operations that set the value of a property have names of the form, <legacyBold>Put</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="6a5891855412840f8eb0d58e444966ee" id="tgt17" class="tgtSentence"> Operations that set the value of a property with a pointer to an ADO object have names of the form, <legacyBold>PutRef</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="712bca900ea23f94e08068fcc26c1a91" id="tgt18" class="tgtSentence">You can get or set a property with calls of these forms:</caps:sentence>
          </para>
          <code>variable = objectPtr-&gt;Get<legacyItalic xmlns="">Property</legacyItalic>(); // get property value 
objectPtr-&gt;Put<legacyItalic xmlns="">Property</legacyItalic>(<legacyItalic xmlns="">value</legacyItalic>);       // set property value
objectPtr-&gt;PutRef<legacyItalic xmlns="">Property</legacyItalic>(&amp;<legacyItalic xmlns="">value</legacyItalic>);   // set property with object pointer</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ef92834b2d9da85b95fcc3e5db4f6c43" id="tgt19" class="tgtSentence">Using Property Directives</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="75a90012431a44c3c1f3ca15f97621d5" id="tgt20" class="tgtSentence">The <legacyBold>__declspec(property...)</legacyBold> compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</caps:sentence>
            <caps:sentence sentenceid="d574614872a147c44e1eff20c82eadc6" id="tgt21" class="tgtSentence"> As a result, you can set or get values of a property in a way similar to Visual Basic.</caps:sentence>
            <caps:sentence sentenceid="ea112c641e2d65125ba2ee1eb448bb5d" id="tgt22" class="tgtSentence"> For example, you can set and get a property this way:</caps:sentence>
          </para>
          <code>objectPtr-&gt;<legacyItalic xmlns="">property</legacyItalic> = <legacyItalic xmlns="">value</legacyItalic>;        // set property value
variable = objectPtr-&gt;<legacyItalic xmlns="">property</legacyItalic>;     // get property value</code>
          <para>
            <caps:sentence sentenceid="de81797f01ac6f200a0cbf2decce853d" id="tgt23" class="tgtSentence">Notice you do not have to code:</caps:sentence>
          </para>
          <code>objectPtr-&gt;Put<legacyItalic xmlns="">Property</legacyItalic>(<legacyItalic xmlns="">value</legacyItalic>);      // set property value
variable = objectPtr-&gt;Get<legacyItalic xmlns="">Property</legacyItalic>;  // get property value</code>
          <para>
            <caps:sentence sentenceid="cae7a765ff1712735567fcd8e6cbf0c8" id="tgt24" class="tgtSentence">The compiler will generate the appropriate <legacyBold>Get</legacyBold><legacyItalic>-</legacyItalic>, <legacyBold>Put</legacyBold>-, or <legacyBold>PutRef</legacyBold><legacyItalic>Property</legacyItalic> call based on what alternative syntax is declared and whether the property is being read or written.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bf38aa9e5ba21662616b31445b66250c" id="tgt25" class="tgtSentence">The <legacyBold>__declspec(property...)</legacyBold> compiler directive can only declare <legacyBold>get</legacyBold>, <legacyBold>put</legacyBold>, or <legacyBold>get</legacyBold> and <legacyBold>put</legacyBold> alternative syntax for a function.</caps:sentence>
            <caps:sentence sentenceid="2a6a88d39743e4051fe9a7424d1af7dd" id="tgt26" class="tgtSentence"> Read-only operations only have a <legacyBold>get</legacyBold> declaration; write-only operations only have a <legacyBold>put</legacyBold> declaration; operations that are both read and write have both <legacyBold>get</legacyBold> and <legacyBold>put</legacyBold> declarations.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bbd64a3f6b014561996e58d987720bf0" id="tgt27" class="tgtSentence">Only two declarations are possible with this directive; however, each property may have three property functions: <legacyBold>Get</legacyBold><legacyItalic>Property</legacyItalic>, <legacyBold>Put</legacyBold><legacyItalic>Property</legacyItalic>, and <legacyBold>PutRef</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="66c0681408b429c93719c7ad8c4f6cb0" id="tgt28" class="tgtSentence"> In that case, only two forms of the property have the alternative syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="045db50c32eb62c191ed3ca714626de3" id="tgt29" class="tgtSentence">For example, the <legacyBold>Command</legacyBold> object <legacyBold>ActiveConnection</legacyBold> property is declared with an alternative syntax for <legacyBold>Get</legacyBold><legacyItalic>ActiveConnection</legacyItalic> and <legacyBold>PutRef</legacyBold><legacyItalic>ActiveConnection</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="66dd00828014d4aed694a20b747b531e" id="tgt30" class="tgtSentence"> The <legacyBold>PutRef</legacyBold>- syntax is a good choice because in practice, you will typically want to put an open <legacyBold>Connection</legacyBold> object (that is, a <legacyBold>Connection</legacyBold> object pointer) in this property.</caps:sentence>
            <caps:sentence sentenceid="7d656045ec204f75d046dadfe668f125" id="tgt31" class="tgtSentence"> On the other hand, the <legacyBold>Recordset</legacyBold> object has <legacyBold>Get</legacyBold>-, <legacyBold>Put</legacyBold>-, and <legacyBold>PutRef</legacyBold><legacyItalic>ActiveConnection</legacyItalic> operations, but no alternative syntax.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2820c5fd6f22ce5e443d0f05072e171c" id="tgt32" class="tgtSentence">Collections, the GetItem Method, and the Item Property</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5a74c6ffb4eabd8d46859ebe6205e87d" id="tgt33" class="tgtSentence">ADO defines several collections, including <legacyBold>Fields</legacyBold>, <legacyBold>Parameters</legacyBold>, <legacyBold>Properties</legacyBold>, and <legacyBold>Errors</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="f65832f1d4a19ce9e54d1c6534564c76" id="tgt34" class="tgtSentence"> In Visual C++, the <legacyBold>GetItem(</legacyBold><legacyItalic>index</legacyItalic><legacyBold>)</legacyBold> method returns a member of the collection.</caps:sentence>
            <caps:sentence sentenceid="2a4c5ece4ebea9ec9b29618a5c31f7a2" id="tgt35" class="tgtSentence">
              <legacyItalic>Index</legacyItalic> is a <legacyBold>Variant</legacyBold>, the value of which is either a numeric index of the member in the collection, or a string containing the name of the member.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3dd8a6fa4bf7cb2920d030a44a19cf9b" id="tgt36" class="tgtSentence">The <legacyBold>__declspec(property...)</legacyBold> compiler directive declares the <legacyBold>Item</legacyBold> property as an alternative syntax to each collection's fundamental <legacyBold>GetItem() </legacyBold>method.</caps:sentence>
            <caps:sentence sentenceid="6bf4edf633e460b3ee5d822f47d45095" id="tgt37" class="tgtSentence"> The alternative syntax uses square brackets and looks similar to an array reference.</caps:sentence>
            <caps:sentence sentenceid="50dd2716fc84e887f15c9f535d50b9df" id="tgt38" class="tgtSentence"> In general, the two forms look like the following:</caps:sentence>
          </para>
          <code>
            <legacyItalic>collectionPtr-&gt;</legacyItalic>GetItem(index);
<legacyItalic>collectionPtr</legacyItalic>-&gt;Item[index];</code>
          <para>
            <caps:sentence sentenceid="ac99c9af3cb0c5ba52ec087063e611a9" id="tgt39" class="tgtSentence">For example, assign a value to a field of a <legacyBold>Recordset</legacyBold> object, named <legacyBold><legacyItalic>rs</legacyItalic></legacyBold>, derived from the <legacyBold>authors</legacyBold> table of the <legacyBold>pubs</legacyBold> database.</caps:sentence>
            <caps:sentence sentenceid="2d3b84f8ed199a636a2e605bcce037bc" id="tgt40" class="tgtSentence"> Use the <legacyBold>Item()</legacyBold> property to access the third <legacyBold>Field</legacyBold> of the <legacyBold>Recordset</legacyBold> object <legacyBold>Fields</legacyBold> collection (collections are indexed from zero; assume the third field is named <legacyBold><legacyItalic>au_fname</legacyItalic></legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="7e417e04d4e023916c772ffd1a0bfbce" id="tgt41" class="tgtSentence"> Then call the <legacyBold>Value()</legacyBold> method on the <legacyBold>Field</legacyBold> object to assign a string value.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3e77e7f23c758d2fc74525903429b72a" id="tgt42" class="tgtSentence">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</caps:sentence>
          </para>
          <code>rs.Fields.Item(2).Value = "<legacyItalic xmlns="">value</legacyItalic>"
rs.Fields.Item("au_fname").Value = "<legacyItalic xmlns="">value</legacyItalic>"
rs(2) = "<legacyItalic xmlns="">value</legacyItalic>"
rs!au_fname = "<legacyItalic xmlns="">value</legacyItalic>"</code>
          <para>
            <caps:sentence sentenceid="03b01c25be1aa743cf86a64456889b86" id="tgt43" class="tgtSentence">The equivalent in Visual C++ to the first two forms above is:</caps:sentence>
          </para>
          <code>rs-&gt;Fields-&gt;GetItem(long(2))-&gt;PutValue("<legacyItalic xmlns="">value</legacyItalic>"); 
rs-&gt;Fields-&gt;GetItem("au_fname")-&gt;PutValue("<legacyItalic xmlns="">value</legacyItalic>");</code>
          <para>
            <caps:sentence sentenceid="4e417fdffab97302c02faec2232abffc" id="tgt44" class="tgtSentence">-or- (the alternative syntax for the <legacyBold>Value</legacyBold> property is also shown)</caps:sentence>
          </para>
          <code>rs-&gt;Fields-&gt;Item[long(2)]-&gt;Value = "<legacyItalic xmlns="">value</legacyItalic>";
rs-&gt;Fields-&gt;Item["au_fname"]-&gt;Value = "<legacyItalic xmlns="">value</legacyItalic>";</code>
          <para>
            <caps:sentence sentenceid="16548617fb090b5963f98f4ee9b25640" id="tgt45" class="tgtSentence">For examples of iterating through a collection, see the "ADO Collections" section of "ADO Reference".</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f26e1fcc785c11525f755f82d825efb1" id="tgt46" class="tgtSentence">COM-Specific Data Types</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1ad64b2fd885252176067f6a3b964333" id="tgt47" class="tgtSentence">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent.</caps:sentence>
            <caps:sentence sentenceid="909348c9eb216d3ef3a650b12524f02d" id="tgt48" class="tgtSentence"> These include standard data types such as <legacyBold>unsigned char</legacyBold> for a Visual Basic <legacyBold>Byte</legacyBold>, <legacyBold>short</legacyBold> for <legacyBold>Integer</legacyBold>, and <legacyBold>long </legacyBold>for <legacyBold>Long</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="99cacf9f6fda22e74a349b8e82771073" id="tgt49" class="tgtSentence"> Look in the Syntax Indexesto see exactly what is required for the operands of a given method or property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ac3b23d04244f4e522eefe474775d21a" id="tgt50" class="tgtSentence">The exceptions to this rule are the data types specific to COM: <legacyBold>Variant</legacyBold>, <legacyBold>BSTR</legacyBold>, and <legacyBold>SafeArray</legacyBold>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="aa7ac8cd5e0a6993a177746279cc00d2" id="tgt51" class="tgtSentence">Variant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="69b5506d80ff0e626980570dbeb61838" id="tgt52" class="tgtSentence">A <legacyBold>Variant</legacyBold> is a structured data type that contains a value member and a data type member.</caps:sentence>
                <caps:sentence sentenceid="ce690938717b3a0162fac51305d28485" id="tgt53" class="tgtSentence"> A <legacyBold>Variant</legacyBold> may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on.</caps:sentence>
                <caps:sentence sentenceid="648c2233b187bd81cd12dfbfe581b5b5" id="tgt54" class="tgtSentence"> COM also provides methods that make it easy to convert one data type to another.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="047b50c4bc59d64cb9d2e093ebace5a5" id="tgt55" class="tgtSentence">The <legacyBold>_variant_t</legacyBold> class encapsulates and manages the <legacyBold>Variant</legacyBold> data type.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d8f2f44508573cc96d621e9248c7bbe0" id="tgt56" class="tgtSentence">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a <legacyBold>_variant_t</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b8ea8a489a89b75c4436e458c8e4d4b2" id="tgt57" class="tgtSentence">This rule is explicitly true when the <legacyBold>Parameters</legacyBold> section in the topics of the ADO API Reference says an operand is a <legacyBold>Variant</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="ba8821dcf97a3430b6eb9d33d8ca5af5" id="tgt58" class="tgtSentence"> One exception is when the documentation explicitly says the operand takes a standard data type, such as <legacyBold>Long</legacyBold> or <legacyBold>Byte</legacyBold>, or an enumeration.</caps:sentence>
                <caps:sentence sentenceid="760e98af345323e337e6281145ae4996" id="tgt59" class="tgtSentence"> Another exception is when the operand takes a <legacyBold>String</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="4cab53ffca49159385612f2870f0037d" id="tgt60" class="tgtSentence">BSTR</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3c00e24214c692296733a63cd6d478de" id="tgt61" class="tgtSentence">A <legacyBold>BSTR</legacyBold> (<legacyBold>B</legacyBold>asic <legacyBold>STR</legacyBold>ing) is a structured data type that contains a character string and the string's length.</caps:sentence>
                <caps:sentence sentenceid="9308d97577bf11abcc39b8382255822f" id="tgt62" class="tgtSentence"> COM provides methods to allocate, manipulate, and free a <legacyBold>BSTR</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1f7ed7d9b14948f8e7e3b55875aa86ee" id="tgt63" class="tgtSentence">The <legacyBold>_bstr_t</legacyBold> class encapsulates and manages the <legacyBold>BSTR</legacyBold> data type.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5817226150aac658218fc570286f5f11" id="tgt64" class="tgtSentence">When the ADO API Reference says a method or property takes a <legacyBold>String</legacyBold> value, it means the value is in the form of a <legacyBold>_bstr_t</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="7e6fcf436574d995fc930a2391eee3dd" id="tgt65" class="tgtSentence">Casting _variant_t and _bstr_t Classes</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2d779b2ad46f4209e73149eb412f18de" id="tgt66" class="tgtSentence">Often it is not necessary to explicitly code a <legacyBold>_variant_t</legacyBold> or <legacyBold>_bstr_t</legacyBold> in an argument to an operation.</caps:sentence>
                <caps:sentence sentenceid="e9ac728a67b83b147b6cfdc3d8ec4229" id="tgt67" class="tgtSentence"> If the <legacyBold>_variant_t</legacyBold> or <legacyBold>_bstr_t</legacyBold> class has a constructor that matches the data type of the argument, the compiler will generate the appropriate <legacyBold>_variant_t</legacyBold> or <legacyBold>_bstr_t</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d1a49dbcbd54efaba205c77b55d18679" id="tgt68" class="tgtSentence">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5efc2679bd4acc3b6f7a3e5f1a490f0d" id="tgt69" class="tgtSentence">For example, the declaration for the <legacyBold>Recordset::Open</legacyBold> method is:</caps:sentence>
              </para>
              <code>    HRESULT Open (
        const _variant_t &amp; Source,
        const _variant_t &amp; ActiveConnection,
        enum CursorTypeEnum CursorType,
        enum LockTypeEnum LockType,
        long Options );</code>
              <para>
                <caps:sentence sentenceid="c51565bca828afc2fb2a190202ee5305" id="tgt70" class="tgtSentence">The <codeInline>ActiveConnection </codeInline>argument takes a reference to a <legacyBold>_variant_t</legacyBold>, which you may code as a connection string or a pointer to an open <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="be4d734899f214e956d744fbef7e21fe" id="tgt71" class="tgtSentence">The correct <legacyBold>_variant_t</legacyBold> will be constructed implicitly if you pass a string such as "<codeInline>DSN=pubs;uid=MyUserName;pwd=MyPassword;</codeInline>", or a pointer such as "<codeInline>(IDispatch *) pConn</codeInline>".</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="a955ec3a31d8205c3ae07b07b7fefc6d" id="tgt72" class="tgtSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <system>Trusted_Connection=yes</system> or <system>Integrated Security = SSPI</system> instead of user ID and password information in the connection string.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="60cd4df907c86ffd4b0891a6c7567778" id="tgt73" class="tgtSentence">Or you may explicitly code a <legacyBold>_variant_t</legacyBold> containing a pointer such as "<codeInline>_variant_t((IDispatch *) pConn, true)</codeInline>".</caps:sentence>
                <caps:sentence sentenceid="e3397fca6c1b8ddbdd8ec7a2cf882342" id="tgt74" class="tgtSentence"> The cast, <codeInline>(IDispatch *)</codeInline>, resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="fb10b2d7082cb7dc2e844630fd157f23" id="tgt75" class="tgtSentence">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface.</caps:sentence>
                <caps:sentence sentenceid="2a23bb9246f9f6beb53820f262c2645f" id="tgt76" class="tgtSentence"> Whenever a pointer to an ADO object must be passed as a <legacyBold>Variant</legacyBold>, that pointer must be cast as a pointer to an IDispatch interface.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="97f93d53cd56378fbf479da46289aced" id="tgt77" class="tgtSentence">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of <codeInline>true</codeInline>.</caps:sentence>
                <caps:sentence sentenceid="f826875617d74a0f449c857c431adee7" id="tgt78" class="tgtSentence"> This argument causes the <legacyBold>Variant</legacyBold> constructor to call its <legacyBold>AddRef</legacyBold>() method, which compensates for ADO automatically calling the <legacyBold>_variant_t::Release</legacyBold>() method when the ADO method or property call completes.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="7626d85603963ac6dff312385027b538" id="tgt79" class="tgtSentence">SafeArray</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2b54ec6defd59a55ba5dbea0c0343154" id="tgt80" class="tgtSentence">A <legacyBold>SafeArray</legacyBold> is a structured data type that contains an array of other data types.</caps:sentence>
                <caps:sentence sentenceid="6199ac5361215bfa2d8287cd818debe8" id="tgt81" class="tgtSentence"> A <legacyBold>SafeArray</legacyBold> is called <legacyItalic>safe</legacyItalic> because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e3680725d6b65a99c99ce4cf6503f24d" id="tgt82" class="tgtSentence">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a <legacyBold>SafeArray</legacyBold>, not a native C/C++ array.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="f35db5d9bcb12b7254b08d0ee7f77464" id="tgt83" class="tgtSentence">For example, the second parameter of the <legacyBold>Connection</legacyBold> object <legacyBold>OpenSchema</legacyBold> method requires an array of <legacyBold>Variant</legacyBold> values.</caps:sentence>
                <caps:sentence sentenceid="bbb854d91c9cd5d26f1fd8b455a2f99c" id="tgt84" class="tgtSentence"> Those <legacyBold>Variant</legacyBold> values must be passed as elements of a <legacyBold>SafeArray</legacyBold>, and that <legacyBold>SafeArray</legacyBold> must be set as the value of another <legacyBold>Variant</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="77fc2eef2196f381f5ea084345724902" id="tgt85" class="tgtSentence"> It is that other <legacyBold>Variant</legacyBold> that is passed as the second argument of <legacyBold>OpenSchema</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="08178055dfc5e1f2e75f402aaef2aa95" id="tgt86" class="tgtSentence">As further examples, the first argument of the <legacyBold>Find</legacyBold> method is a <legacyBold>Variant</legacyBold> whose value is a one-dimensional <legacyBold>SafeArray</legacyBold>; each of the optional first and second arguments of <legacyBold>AddNew</legacyBold> is a one-dimensional <legacyBold>SafeArray</legacyBold>; and the return value of the <legacyBold>GetRows</legacyBold> method is a <legacyBold>Variant</legacyBold> whose value is a two-dimensional <legacyBold>SafeArray</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="300bd366fdac177e62d409c784147e75" id="tgt87" class="tgtSentence">Missing and Default Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6f1fe550bc54b881a4c84acbdfcee1d5" id="tgt88" class="tgtSentence">Visual Basic allows missing parameters in methods.</caps:sentence>
            <caps:sentence sentenceid="8b3ff5e7f428bbd85a9834981a8a4eb4" id="tgt89" class="tgtSentence"> For example, the <legacyBold>Recordset</legacyBold> object <legacyBold>Open</legacyBold> method has five parameters, but you can skip intermediate parameters and leave off trailing parameters.</caps:sentence>
            <caps:sentence sentenceid="ec92bd550007d6667dd69d0d0b3ca222" id="tgt90" class="tgtSentence"> A default <legacyBold>BSTR</legacyBold> or <legacyBold>Variant</legacyBold> will be substituted depending on the data type of the missing operand.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d60a2ff4f98732ce7be84c0709dd55dc" id="tgt91" class="tgtSentence">In C/C++, all operands must be specified.</caps:sentence>
            <caps:sentence sentenceid="89a1eb3595f9896d06d28fa43f294283" id="tgt92" class="tgtSentence"> If you want to specify a missing parameter whose data type is a string, specify a <legacyBold>_bstr_t</legacyBold> containing a null string.</caps:sentence>
            <caps:sentence sentenceid="945b892eb3dd7ffa395a6f670482154d" id="tgt93" class="tgtSentence"> If you want to specify a missing parameter whose data type is a <legacyBold>Variant</legacyBold>, specify a <legacyBold>_variant_t</legacyBold> with a value of DISP_E_PARAMNOTFOUND and a type of VT_ERROR.</caps:sentence>
            <caps:sentence sentenceid="8706ed9082cbd57956091e68b69f1ca5" id="tgt94" class="tgtSentence"> Alternatively, specify the equivalent <legacyBold>_variant_t</legacyBold> constant, <legacyBold>vtMissing</legacyBold>, which is supplied by the <legacyBold>#import</legacyBold> directive.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="06773cbbfce8260a251132a7bb6c8533" id="tgt95" class="tgtSentence">Three methods are exceptions to the typical use of <legacyBold>vtMissing</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="bf04a0cf91dd0a16f95964070d9af59b" id="tgt96" class="tgtSentence"> These are the <legacyBold>Execute</legacyBold> methods of the <legacyBold>Connection</legacyBold> and <legacyBold>Command</legacyBold> objects, and the <legacyBold>NextRecordset</legacyBold> method of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="ca2af74d78994784b066db41b2f206b4" id="tgt97" class="tgtSentence"> The following are their signatures:</caps:sentence>
          </para>
          <code>_RecordsetPtr &lt;A HREF="mdmthcnnexecute.htm"&gt;Execute&lt;/A&gt;( _bstr_t <legacyItalic xmlns="">CommandText</legacyItalic>, VARIANT * <legacyItalic xmlns="">RecordsAffected</legacyItalic>, 
        long<legacyItalic xmlns=""> Options </legacyItalic>);  // Connection
_RecordsetPtr &lt;A HREF="mdmthcmdexecute.htm"&gt;Execute&lt;/A&gt;( VARIANT * <legacyItalic xmlns="">RecordsAffected</legacyItalic>, VARIANT * <legacyItalic xmlns="">Parameters</legacyItalic>, 
        long<legacyItalic xmlns=""> Options </legacyItalic>);  // Command
_RecordsetPtr &lt;A HREF="mdmthnextrec.htm"&gt;NextRecordset&lt;/A&gt;( VARIANT *<legacyItalic xmlns=""> RecordsAffected </legacyItalic>);  // Recordset</code>
          <para>
            <caps:sentence sentenceid="6a0210e793a671679187d0ba26d87ba3" id="tgt98" class="tgtSentence">The parameters, <legacyItalic>RecordsAffected</legacyItalic> and <legacyItalic>Parameters</legacyItalic>, are pointers to a <legacyBold>Variant</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="30f2cd61d93d0606f7c85123a8c65aaa" id="tgt99" class="tgtSentence">
              <legacyItalic>Parameters</legacyItalic> is an input parameter which specifies the address of a <legacyBold>Variant</legacyBold> containing a single parameter, or array of parameters, that will modify the command being executed.</caps:sentence>
            <caps:sentence sentenceid="a9b5465b72d132c8f8dc7906f4dcb0be" id="tgt100" class="tgtSentence">
              <legacyItalic>RecordsAffected </legacyItalic>is an output parameter that specifies the address of a <legacyBold>Variant</legacyBold>, where the number of rows affected by the method is returned.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b01da8bce6d7bfd90e922acac8bba39f" id="tgt101" class="tgtSentence">In the <legacyBold>Command</legacyBold> object <legacyBold>Execute</legacyBold> method, indicate that no parameters are specified by setting <legacyItalic>Parameters</legacyItalic> to either <codeInline>&amp;vtMissing</codeInline> (which is recommended) or to the null pointer (that is, <legacyBold>NULL</legacyBold> or zero (0)).</caps:sentence>
            <caps:sentence sentenceid="8fa697f50f84b667db83be512c501186" id="tgt102" class="tgtSentence"> If <legacyItalic>Parameters</legacyItalic> is set to the null pointer, the method internally substitutes the equivalent of <legacyBold>vtMissing</legacyBold>, and then completes the operation.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5cc8a1d9a9eb3f0261f7329514565a2d" id="tgt103" class="tgtSentence">In all the methods, indicate that the number of records affected should not be returned by setting <legacyItalic>RecordsAffected </legacyItalic>to the null pointer.</caps:sentence>
            <caps:sentence sentenceid="b4295519e6cd62a9a5351178c71792b4" id="tgt104" class="tgtSentence"> In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1c7963959338b62f5211fa2ffc8a3a35" id="tgt105" class="tgtSentence">Thus, for these three methods, it is valid to code something such as:</caps:sentence>
          </para>
          <code>pConnection-&gt;Execute("<legacyItalic xmlns="">commandText</legacyItalic>", NULL, adCmdText); 
pCommand-&gt;Execute(NULL, NULL, adCmdText);
pRecordset-&gt;NextRecordset(NULL);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="db0b59b9623daf50a80d69cd1518a7d2" id="tgt106" class="tgtSentence">Error Handling</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0155031c9ca858577fe652e05954149c" id="tgt107" class="tgtSentence">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</caps:sentence>
            <caps:sentence sentenceid="1cefb3f5e272ef1e577e4e90705a39fe" id="tgt108" class="tgtSentence"> The <legacyBold>#import</legacyBold> directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</caps:sentence>
            <caps:sentence sentenceid="ca49b10f2f78cb6798ce4f791c575399" id="tgt109" class="tgtSentence"> If the HRESULT indicates failure, the wrapper code throws a COM error by calling _com_issue_errorex() with the HRESULT return code as an argument.</caps:sentence>
            <caps:sentence sentenceid="7fcbfd06c23e74a67c20b4bf9d3b441f" id="tgt110" class="tgtSentence"> COM error objects can be caught in a <legacyBold>try</legacyBold>-<legacyBold>catch</legacyBold> block.</caps:sentence>
            <caps:sentence sentenceid="fe7a0a8ad50076e913201553ef200327" id="tgt111" class="tgtSentence"> (For efficiency's sake, catch a reference to a <legacyBold>_com_error</legacyBold> object.)</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="7f22d5d63bd849bc1746a6342266957c" id="tgt112" class="tgtSentence">Remember, these are ADO errors: they result from the ADO operation failing.</caps:sentence>
            <caps:sentence sentenceid="27c6ccb96e14e3504a40f31eaeb9f99a" id="tgt113" class="tgtSentence"> Errors returned by the underlying provider appear as <legacyBold>Error</legacyBold> objects in the <legacyBold>Connection</legacyBold> object <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c4ed7d0a51e0f99b2aced178ec7ee3e5" id="tgt114" class="tgtSentence">The <legacyBold>#import</legacyBold> directive creates only error handling routines for methods and properties declared in the ADO .dll.</caps:sentence>
            <caps:sentence sentenceid="7d5409a8538ac326a52a98f5c35df249" id="tgt115" class="tgtSentence"> However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</caps:sentence>
            <caps:sentence sentenceid="0b36a150147ba9658cf2ab09e22788c1" id="tgt116" class="tgtSentence"> See the topic, <legacyLink xlink:href="2952ece0-7217-4448-bb09-f6b64f43b7e2">Visual C++ Extensions</legacyLink>, or the code in the following sections for examples.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="e1839fb9b5a25a10c450220b1881196e" id="tgt117" class="tgtSentence">Visual C++ Equivalents of Visual Basic Conventions</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2ed5fff00d656f381cb5d77db81991be" id="tgt118" class="tgtSentence">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="6fcdf8fdd679d35b742800517380f041" id="tgt119" class="tgtSentence">Declaring an ADO Object</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9b46c203856546ec4e69faf9e849de4a" id="tgt120" class="tgtSentence">In Visual Basic, an ADO object variable (in this case for a <legacyBold>Recordset</legacyBold> object) is declared as follows:</caps:sentence>
              </para>
              <code>Dim rst As ADODB.Recordset</code>
              <para>
                <caps:sentence sentenceid="d82d802aee057654f77756238ba37445" id="tgt121" class="tgtSentence">The clause, "<codeInline>ADODB.Recordset</codeInline>", is the ProgID of the <legacyBold>Recordset</legacyBold> object as defined in the registry.</caps:sentence>
                <caps:sentence sentenceid="e73125047309708930241626328e63e9" id="tgt122" class="tgtSentence"> A new instance of a <legacyBold>Record</legacyBold> object is declared as follows:</caps:sentence>
              </para>
              <code>Dim rst As New ADODB.Recordset</code>
              <para>
                <caps:sentence sentenceid="3d263eb0233f14872193733387840c80" id="tgt123" class="tgtSentence">-or-</caps:sentence>
              </para>
              <code>Dim rst As ADODB.Recordset
Set rst = New ADODB.Recordset</code>
              <para>
                <caps:sentence sentenceid="426101afcbf884a08144906b5fe85661" id="tgt124" class="tgtSentence">In Visual C++, the <legacyBold>#import </legacyBold>directive generates smart pointer-type declarations for all the ADO objects.</caps:sentence>
                <caps:sentence sentenceid="24548bb21e9a635a431872658c25e03d" id="tgt125" class="tgtSentence"> For example, a variable that points to a <legacyBold>_Recordset</legacyBold> object is of type <legacyBold>_RecordsetPtr</legacyBold>, and is declared as follows:</caps:sentence>
              </para>
              <code>_RecordsetPtr  rs;</code>
              <para>
                <caps:sentence sentenceid="5dd25441a71d8d4d7b65ffef143a250f" id="tgt126" class="tgtSentence">A variable that points to a new instance of a <legacyBold>_Recordset</legacyBold> object is declared as follows:</caps:sentence>
              </para>
              <code>_RecordsetPtr  rs("ADODB.Recordset");</code>
              <para>
                <caps:sentence sentenceid="3d263eb0233f14872193733387840c80" id="tgt127" class="tgtSentence">-or-</caps:sentence>
              </para>
              <code>_RecordsetPtr  rs;
rs.CreateInstance("ADODB.Recordset");</code>
              <para>
                <caps:sentence sentenceid="3d263eb0233f14872193733387840c80" id="tgt128" class="tgtSentence">-or-</caps:sentence>
              </para>
              <code>_RecordsetPtr  rs;
rs.CreateInstance(__uuidof(_Recordset));</code>
              <para>
                <caps:sentence sentenceid="6f7023ec144c551061502a5b4ce79447" id="tgt129" class="tgtSentence">After the <legacyBold>CreateInstance</legacyBold> method is called, the variable can be used as follows:</caps:sentence>
              </para>
              <code>rs-&gt;Open(...);</code>
              <para>
                <caps:sentence sentenceid="866d210f352884959990959947ac684c" id="tgt130" class="tgtSentence">Notice that in one case, the "<codeInline>.</codeInline>" operator is used as if the variable were an instance of a class (<codeInline>rs.CreateInstance</codeInline>), and in another case, the "<codeInline>-&gt;</codeInline>" operator is used as if the variable were a pointer to an interface (<codeInline>rs-&gt;Open</codeInline>).</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c1ff2105cb0efc4ebc9a37156d89bb64" id="tgt131" class="tgtSentence">One variable can be used in two ways because the "<codeInline>-&gt;</codeInline>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</caps:sentence>
                <caps:sentence sentenceid="1041d1f99f844922be251906dc6bcc85" id="tgt132" class="tgtSentence"> A private class member of the instance variable contains a pointer to the <legacyBold>_Recordset</legacyBold> interface; the "<codeInline>-&gt;</codeInline>" operator returns that pointer; and the returned pointer accesses the members of the <legacyBold>_Recordset</legacyBold> object.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="327d40a298636df245bb2df59b4ea044" id="tgt133" class="tgtSentence">Coding a Missing Parameter — String</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3f4b9950a82b9362074438af87fab1a2" id="tgt134" class="tgtSentence">When you need to code a missing <legacyBold>String</legacyBold> operand in Visual Basic, you merely omit the operand.</caps:sentence>
                <caps:sentence sentenceid="79fa0c18ce9bee3156e430a88c4cb0f2" id="tgt135" class="tgtSentence"> You must specify the operand in Visual C++.</caps:sentence>
                <caps:sentence sentenceid="7c7068d1bedb1fd457fc5bbd8ff28d77" id="tgt136" class="tgtSentence"> Code a <legacyBold>_bstr_t</legacyBold> that has an empty string as a value.</caps:sentence>
              </para>
              <code>_bstr_t strMissing(L"");</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="6e753e8e38ce8f2173831d571320328c" id="tgt137" class="tgtSentence">Coding a Missing Parameter — Variant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="fcea483f6f8038928ba0cbeae17790af" id="tgt138" class="tgtSentence">When you need to code a missing <legacyBold>Variant</legacyBold> operand in Visual Basic, you merely omit the operand.</caps:sentence>
                <caps:sentence sentenceid="4b3f5dad418063d1aa672dd897e3d8d5" id="tgt139" class="tgtSentence"> You must specify all operands in Visual C++.</caps:sentence>
                <caps:sentence sentenceid="5bfb3e574a89b96b090c3fd1bd46c79f" id="tgt140" class="tgtSentence"> Code a missing <legacyBold>Variant</legacyBold> parameter with a <legacyBold>_variant_t</legacyBold> set to the special value, DISP_E_PARAMNOTFOUND, and type, VT_ERROR.</caps:sentence>
                <caps:sentence sentenceid="26db8a5a13f3474851d20cc1bd63dce0" id="tgt141" class="tgtSentence"> Alternatively, specify <legacyBold>vtMissing</legacyBold>, which is an equivalent predefined constant supplied by the <legacyBold>#import</legacyBold> directive.</caps:sentence>
              </para>
              <code>_variant_t  vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); </code>
              <para>
                <caps:sentence sentenceid="fae92e1d4386d4a350df74495ebd8a0a" id="tgt142" class="tgtSentence">-or use -</caps:sentence>
              </para>
              <code>...vtMissing...;</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="b97b2b112358288ddeaec62bb656b5e6" id="tgt143" class="tgtSentence">Declaring a Variant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="5fd0759a0088b727e9352f306e5658b6" id="tgt144" class="tgtSentence">In Visual Basic, a <legacyBold>Variant</legacyBold> is declared with the <legacyBold>Dim</legacyBold> statement as follows:</caps:sentence>
              </para>
              <code>Dim <legacyItalic xmlns="">VariableName</legacyItalic> As Variant</code>
              <para>
                <caps:sentence sentenceid="80a4f5ed72b39f4e3b5bc4fa95cd9780" id="tgt145" class="tgtSentence">In Visual C++, declare a variable as type <legacyBold>_variant_t</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="ee2e1a1e84346598813e00b808ebb82b" id="tgt146" class="tgtSentence"> A few schematic <legacyBold>_variant_t </legacyBold>declarations are shown below.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="884333305dbfa95358e66e78e93648b3" id="tgt147" class="tgtSentence">These declarations merely give a rough idea of what you would code in your own program.</caps:sentence>
                  <caps:sentence sentenceid="c3a556dc06d26571c5ecd03e04961c0b" id="tgt148" class="tgtSentence"> For more information, see the examples below, and the Visual C++documentation.</caps:sentence>
                </para>
              </alert>
              <code>_variant_t  VariableName(<legacyItalic xmlns="">value</legacyItalic>);
_variant_t  VariableName((<legacyItalic xmlns="">data type cast</legacyItalic>) <legacyItalic xmlns="">value</legacyItalic>);
_variant_t  VariableName(<legacyItalic xmlns="">value, </legacyItalic>VT<legacyItalic xmlns="">_DATATYPE</legacyItalic>);
_variant_t  VariableName(interface * <legacyItalic xmlns="">value, </legacyItalic>bool fAddRef = true);</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="1ab4b9686ceb876c4434b622381c5555" id="tgt149" class="tgtSentence">Using Arrays of Variants</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="98a65e2ccd20d293caa4679f7f65a7ca" id="tgt150" class="tgtSentence">In Visual Basic, arrays of <legacyBold>Variants</legacyBold> can be coded with the <legacyBold>Dim</legacyBold> statement, or you may use the <legacyBold>Array</legacyBold> function, as demonstrated in the following example code:</caps:sentence>
              </para>
              <code>Public Sub ArrayOfVariants
Dim cn As ADODB.Connection
Dim rs As ADODB.Recordset
Dim fld As ADODB.Field

    cn.Open "DSN=pubs"
    rs = cn.OpenSchema(adSchemaColumns, _
        Array(Empty, Empty, "authors", Empty))
    For Each fld in rs.Fields
        Debug.Print "Name = "; fld.Name
    Next fld
    rs.Close
    cn.Close
End Sub</code>
              <para>
                <caps:sentence sentenceid="31092272832a084f951a8a3ceb0ad135" id="tgt151" class="tgtSentence">The following Visual C++ example demonstrates using a <legacyBold>SafeArray</legacyBold> used with a <legacyBold>_variant_t</legacyBold>.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="4358b5009c67d0e31d7fbf1663fcd3bf" id="tgt152" class="tgtSentence">Notes</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="9481ffed6108072c3d116dcec35d592f" id="tgt153" class="tgtSentence">The following notes correspond to commented sections in the code example.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5cc9a64b855abe0db1b3f9dbe880b0de" id="tgt154" class="tgtSentence">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="31d57446758ba3fb0b10277d85423fa7" id="tgt155" class="tgtSentence">You only need a one-dimensional array, so you can use <legacyBold>SafeArrayCreateVector</legacyBold>, instead of the general purpose <legacyBold>SAFEARRAYBOUND</legacyBold> declaration and <legacyBold>SafeArrayCreate</legacyBold> function.</caps:sentence>
                        <caps:sentence sentenceid="28a9dc9ee4417f97434ba556a941cc28" id="tgt156" class="tgtSentence"> The following is what that code would look like using <legacyBold>SafeArrayCreate</legacyBold>:</caps:sentence>
                      </para>
                      <code>   SAFEARRAYBOUND   sabound[1];
   sabound[0].lLbound = 0;
   sabound[0].cElements = 4;
   pSa = SafeArrayCreate(VT_VARIANT, 1, sabound);</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="e0b7b00cef38198888688314cb92074f" id="tgt157" class="tgtSentence">The schema identified by the enumerated constant, <legacyBold>adSchemaColumns</legacyBold>, is associated with four constraint columns: TABLE_CATALOG, TABLE_SCHEMA, TABLE_NAME, and COLUMN_NAME.</caps:sentence>
                        <caps:sentence sentenceid="3fcd68ce2c140aac4df4c152aca80a27" id="tgt158" class="tgtSentence"> Therefore, an array of <legacyBold>Variant</legacyBold> values with four elements is created.</caps:sentence>
                        <caps:sentence sentenceid="3963771ebc55a643592b2cd213a18c21" id="tgt159" class="tgtSentence"> Then a constraint value that corresponds to the third column, TABLE_NAME, is specified.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="cd2ed60b8d18708236892b4a1b0826f2" id="tgt160" class="tgtSentence">The <legacyBold>Recordset</legacyBold> that is returned consists of several columns, a subset of which is the constraint columns.</caps:sentence>
                        <caps:sentence sentenceid="8112405dbc5dc831921eebc3bca9137a" id="tgt161" class="tgtSentence"> The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2143a09ae4e08aee835575dda5e35a93" id="tgt162" class="tgtSentence">Those familiar with <legacyBold>SafeArrays </legacyBold>may be surprised that <legacyBold>SafeArrayDestroy</legacyBold>() is not called before the exit.</caps:sentence>
                        <caps:sentence sentenceid="62c298980c51d18c0981aa4ffc9a93b0" id="tgt163" class="tgtSentence"> In fact, calling <legacyBold>SafeArrayDestroy</legacyBold>() in this case will cause a run-time exception.</caps:sentence>
                        <caps:sentence sentenceid="e1063112d5446f9ff0718a3541571f47" id="tgt164" class="tgtSentence"> The reason is that the destructor for <codeInline>vtCriteria</codeInline> will call <legacyBold>VariantClear</legacyBold>() when the <legacyBold>_variant_t </legacyBold>goes out of scope, which will free the <legacyBold>SafeArray</legacyBold>.</caps:sentence>
                        <caps:sentence sentenceid="c6ec4e36eec94f8a5167d2633ac80ba1" id="tgt165" class="tgtSentence"> Calling <legacyBold>SafeArrayDestroy</legacyBold>, without manually clearing the <legacyBold>_variant_t</legacyBold>, would cause the destructor to try to clear an invalid <legacyBold>SafeArray</legacyBold> pointer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="4e86c371cdf651f8f2bf51a752d46a66" id="tgt166" class="tgtSentence">If <legacyBold>SafeArrayDestroy</legacyBold> were called, the code would look like this:</caps:sentence>
                      </para>
                      <code>      TESTHR(SafeArrayDestroy(pSa));
   vtCriteria.vt = VT_EMPTY;
      vtCriteria.parray = NULL;</code>
                      <para>
                        <caps:sentence sentenceid="c1786385696b3d52e8c467eb5a6c9a72" id="tgt167" class="tgtSentence">However, it is much simpler to let the <legacyBold>_variant_t</legacyBold> manage the <legacyBold>SafeArray</legacyBold>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <code>// Visual_CPP_ADO_Prog_1.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

// Note 1
inline void TESTHR( HRESULT _hr ) { 
   if FAILED(_hr) 
      _com_issue_error(_hr); 
}

int main() {
   CoInitialize(NULL);
   try {
      _RecordsetPtr pRs("ADODB.Recordset");
      _ConnectionPtr pCn("ADODB.Connection");
      _variant_t vtTableName("authors"), vtCriteria;
      long ix[1];
      SAFEARRAY *pSa = NULL;

      pCn-&gt;Provider = "sqloledb";
      pCn-&gt;Open("Data Source='(local)';Initial Catalog='pubs';Integrated Security=SSPI", "", "", adConnectUnspecified);
      // Note 2, Note 3
      pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4);
      if (!pSa) 
         _com_issue_error(E_OUTOFMEMORY);

      // Specify TABLE_NAME in the third array element (index of 2). 
      ix[0] = 2;      
      TESTHR(SafeArrayPutElement(pSa, ix, &amp;vtTableName));

      // There is no Variant constructor for a SafeArray, so manually set the 
      // type (SafeArray of Variant) and value (pointer to a SafeArray).

      vtCriteria.vt = VT_ARRAY | VT_VARIANT;
      vtCriteria.parray = pSa;

      pRs = pCn-&gt;OpenSchema(adSchemaColumns, vtCriteria, vtMissing);

      long limit = pRs-&gt;GetFields()-&gt;Count;
      for ( long x = 0 ; x &lt; limit ; x++ )
         printf( "%d: %s\n", x + 1, ((char*) pRs-&gt;GetFields()-&gt;Item[x]-&gt;Name) );
      // Note 4
      pRs-&gt;Close();
      pCn-&gt;Close();
   }
   catch (_com_error &amp;e) {
      printf("Error:\n");
      printf("Code = %08lx\n", e.Error());
      printf("Code meaning = %s\n", (char*) e.ErrorMessage());
      printf("Source = %s\n", (char*) e.Source());
      printf("Description = %s\n", (char*) e.Description());
   }
   CoUninitialize();
}</code>
                </content>
              </section>
            </sections>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="c2956fa9f4ef91b9cfb79d9c850ba59d" id="tgt168" class="tgtSentence">Using Property Get/Put/PutRef</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="de8c12d2138f43b78b761abe7d0cc72d" id="tgt169" class="tgtSentence">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</caps:sentence>
              </para>
              <code>Public Sub GetPutPutRef
Dim rs As New ADODB.Recordset
Dim cn As New ADODB.Connection
Dim sz as Integer
cn.Open "Provider=sqloledb;Data Source=yourserver;" &amp; _
         "Initial Catalog=pubs;Integrated Security=SSPI;"
rs.PageSize = 10
sz = rs.PageSize
rs.ActiveConnection = cn
rs.Open "authors",,adOpenStatic
' ...
rs.Close
cn.Close
End Sub</code>
              <para>
                <caps:sentence sentenceid="668d7bd5c4bee0e0ccf70e59825efbb0" id="tgt170" class="tgtSentence">This Visual C++ example demonstrates the <legacyBold>Get</legacyBold>/<legacyBold>Put</legacyBold>/<legacyBold>PutRef</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="4358b5009c67d0e31d7fbf1663fcd3bf" id="tgt171" class="tgtSentence">Notes</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="9481ffed6108072c3d116dcec35d592f" id="tgt172" class="tgtSentence">The following notes correspond to commented sections in the code example.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7a753bf8ae92032cd4dc3f690dee5526" id="tgt173" class="tgtSentence">This example uses two forms of a missing string argument: an explicit constant, <legacyBold>strMissing</legacyBold>, and a string that the compiler will use to create a temporary <legacyBold>_bstr_t</legacyBold> that will exist for the scope of the <legacyBold>Open</legacyBold> method.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1003df7ab30feaf13dacf66cb3f2ca08" id="tgt174" class="tgtSentence">It is not necessary to cast the operand of <codeInline>rs-&gt;PutRefActiveConnection(cn)</codeInline> to <codeInline>(IDispatch *)</codeInline> because the type of the operand is already <codeInline>(IDispatch *)</codeInline>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <code>// Visual_CPP_ado_prog_2.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

int main() {
   CoInitialize(NULL);
   try {
      _ConnectionPtr cn("ADODB.Connection");
      _RecordsetPtr rs("ADODB.Recordset");
      _bstr_t strMissing(L"");
      long oldPgSz = 0, newPgSz = 5;

      // Note 1
      cn-&gt;Provider = "sqloledb";
      cn-&gt;Open("Data Source='(local)';Initial Catalog=pubs;Integrated Security=SSPI;", strMissing, "", adConnectUnspecified);

      oldPgSz = rs-&gt;GetPageSize();
      // -or-
      // oldPgSz = rs-&gt;PageSize;

      rs-&gt;PutPageSize(newPgSz);
      // -or-
      // rs-&gt;PageSize = newPgSz;

      // Note 2
      rs-&gt;PutRefActiveConnection( cn );
      rs-&gt;Open("authors", vtMissing, adOpenStatic, adLockReadOnly, adCmdTable);
      printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, rs-&gt;GetPageSize());
      rs-&gt;Close();
      cn-&gt;Close();
      
   }
   catch (_com_error &amp;e) {
      printf("Description = %s\n", (char*) e.Description());
   }
   ::CoUninitialize();
}</code>
                </content>
              </section>
            </sections>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="0f5da5f4075002d43339c0add8202ee3" id="tgt175" class="tgtSentence">Using GetItem(x) and Item[x]</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="1b3ebdf4a337d03306d6d97cecac0a72" id="tgt176" class="tgtSentence">This Visual Basic example demonstrates the standard and alternative syntax for <legacyBold>Item</legacyBold>().</caps:sentence>
              </para>
              <code>Public Sub GetItemItem
Dim rs As New ADODB.Recordset
Dim name as String
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _
         adLockBatchOptimistic, adTable
name = rs(0)
' -or-
name = rs.Fields.Item(0)
rs(0) = "Test"
rs.UpdateBatch
' Restore name
rs(0) = name
rs.UpdateBatch
rs.Close
End Sub</code>
              <para>
                <caps:sentence sentenceid="a774cfd59e50ab2d63ef94a473963208" id="tgt177" class="tgtSentence">This Visual C++ example demonstrates <legacyBold>Item</legacyBold>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="bd425d1615e808ca407b91edfa964e96" id="tgt178" class="tgtSentence">The following note corresponds to commented sections in the code example:  When the collection is accessed with <legacyBold>Item</legacyBold>, the index, <legacyBold>2</legacyBold>, must be cast to <legacyBold>long</legacyBold> so an appropriate constructor will be invoked.</caps:sentence>
                </para>
              </alert>
              <code>// Visual_CPP_ado_prog_3.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

void main() {
   CoInitialize(NULL);
   try {
      _ConnectionPtr cn("ADODB.Connection");
      _RecordsetPtr rs("ADODB.Recordset");
      _variant_t vtFirstName;

      cn-&gt;Provider = "sqloledb";
      cn-&gt;Open("Data Source='(local)';Initial Catalog=pubs;Integrated Security=SSPI;", "", "", adConnectUnspecified);

      rs-&gt;PutRefActiveConnection( cn );
      rs-&gt;Open("authors", vtMissing, adOpenStatic, adLockOptimistic, adCmdTable);
      rs-&gt;MoveFirst();

      // Note 1. Get a field.
      vtFirstName = rs-&gt;Fields-&gt;GetItem((long)2)-&gt;GetValue();
      // -or-
      vtFirstName = rs-&gt;Fields-&gt;Item[(long)2]-&gt;Value;

      printf( "First name = '%s'\n", (char*)( (_bstr_t)vtFirstName) );

      rs-&gt;Fields-&gt;GetItem((long)2)-&gt;Value = L"TEST";
      rs-&gt;Update(vtMissing, vtMissing);

      // Restore name
      rs-&gt;Fields-&gt;GetItem((long)2)-&gt;PutValue(vtFirstName);
      // -or-
      rs-&gt;Fields-&gt;GetItem((long)2)-&gt;Value = vtFirstName;
      rs-&gt;Update(vtMissing, vtMissing);
      rs-&gt;Close();
   }
   catch (_com_error &amp;e) {
      printf("Description = '%s'\n", (char*) e.Description());
   }
   ::CoUninitialize();
}</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="d8933b4174e1360e7d4d59be47e8e0eb" id="tgt179" class="tgtSentence">Casting ADO object pointers with (IDispatch *)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e14b664498e814573466ab2e8140b3ed" id="tgt180" class="tgtSentence">The following Visual C++ example demonstrates using (IDispatch *) to cast ADO object pointers.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="4358b5009c67d0e31d7fbf1663fcd3bf" id="tgt181" class="tgtSentence">Notes</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="9481ffed6108072c3d116dcec35d592f" id="tgt182" class="tgtSentence">The following notes correspond to commented sections in the code example.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="502a4981857ae2e4dd314f76afa1a349" id="tgt183" class="tgtSentence">Specify an open <legacyBold>Connection</legacyBold> object in an explicitly coded <legacyBold>Variant</legacyBold>.</caps:sentence>
                        <caps:sentence sentenceid="d77ea07a504f5a5a2b131101053fba4e" id="tgt184" class="tgtSentence"> Cast it with (IDispatch *) so the correct constructor will be invoked.</caps:sentence>
                        <caps:sentence sentenceid="6fe1f8103a62846144a62ff0d93c57e4" id="tgt185" class="tgtSentence"> Also, explicitly set the second <legacyBold>_variant_t</legacyBold> parameter to the default value of <legacyBold>true</legacyBold>, so the object reference count will be correct when the <legacyBold>Recordset::Open</legacyBold> operation ends.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6bbb1e6c15722bef515bf72edd3d887c" id="tgt186" class="tgtSentence">The expression, <codeInline>(_bstr_t)</codeInline>, is not a cast, but a <legacyBold>_variant_t</legacyBold> operator that extracts a <legacyBold>_bstr_t </legacyBold>string from the <legacyBold>Variant</legacyBold> returned by <legacyBold>Value</legacyBold>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="201f7a527f6e4eedf75f19a4a4acdc3c" id="tgt187" class="tgtSentence">The expression, <codeInline>(char*)</codeInline>, is not a cast, but a <legacyBold>_bstr_t</legacyBold> operator that extracts a pointer to the encapsulated string in a <legacyBold>_bstr_t</legacyBold> object.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="3591884019683c9ed4568ef500ee61e0" id="tgt188" class="tgtSentence">This section of code demonstrates some of the useful behaviors of <legacyBold>_variant_t</legacyBold> and <legacyBold>_bstr_t</legacyBold> operators.</caps:sentence>
                  </para>
                  <code>// Visual_CPP_ado_prog_4.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

int main() {
   CoInitialize(NULL);
   try {
      _ConnectionPtr pConn("ADODB.Connection");
      _RecordsetPtr pRst("ADODB.Recordset");

      pConn-&gt;Provider = "sqloledb";
      pConn-&gt;Open("Data Source='(local)';Initial Catalog='pubs';Integrated Security=SSPI", "", "", adConnectUnspecified);

      // Note 1.
      pRst-&gt;Open("authors", _variant_t((IDispatch *) pConn, true), adOpenStatic, adLockReadOnly, adCmdTable);
      pRst-&gt;MoveLast();

      // Note 2.
      printf("Last name is '%s %s'\n", 
         (char*) ((_bstr_t) pRst-&gt;GetFields()-&gt;GetItem("au_fname")-&gt;GetValue()),
         (char*) ((_bstr_t) pRst-&gt;Fields-&gt;Item["au_lname"]-&gt;Value));

      pRst-&gt;Close();
      pConn-&gt;Close();
   }
   catch (_com_error &amp;e) {
      printf("Description = '%s'\n", (char*) e.Description());
   }   
   ::CoUninitialize();
}</code>
                </content>
              </section>
            </sections>
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
          <caps:sentence id="src1" class="srcSentence">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the <legacyBold>#import</legacyBold> directive), and Visual J++ (with the ADO/WFC class package).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">To accommodate this diversity, the <legacyLink xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">ADO for Visual C++ Syntax Indexes</legacyLink> provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">ADO is implemented with COM (Component Object Model) interfaces.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> However, it is easier for programmers to work with COM in certain programming languages than others.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src7" class="srcSentence">The following sections summarize details for C and C++ programmers using ADO and the <legacyBold>#import</legacyBold> directive.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> It focuses on data types specific to COM (<legacyBold>Variant</legacyBold>, <legacyBold>BSTR</legacyBold>, and <legacyBold>SafeArray</legacyBold>), and error handling (_com_error).</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Using the #import Compiler Directive</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">The <legacyBold>#import</legacyBold> Visual C++ compiler directive simplifies working with the ADO methods and properties.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Each interface is encapsulated, or wrapped, in a class.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">Operations that retrieve the value of a property have names of the form, <legacyBold>Get</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> Operations that set the value of a property have names of the form, <legacyBold>Put</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Operations that set the value of a property with a pointer to an ADO object have names of the form, <legacyBold>PutRef</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">You can get or set a property with calls of these forms:</caps:sentence>
          </para>
          <code>variable = objectPtr-&gt;Get<legacyItalic xmlns="">Property</legacyItalic>(); // get property value 
objectPtr-&gt;Put<legacyItalic xmlns="">Property</legacyItalic>(<legacyItalic xmlns="">value</legacyItalic>);       // set property value
objectPtr-&gt;PutRef<legacyItalic xmlns="">Property</legacyItalic>(&amp;<legacyItalic xmlns="">value</legacyItalic>);   // set property with object pointer</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src19" class="srcSentence">Using Property Directives</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src20" class="srcSentence">The <legacyBold>__declspec(property...)</legacyBold> compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> As a result, you can set or get values of a property in a way similar to Visual Basic.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> For example, you can set and get a property this way:</caps:sentence>
          </para>
          <code>objectPtr-&gt;<legacyItalic xmlns="">property</legacyItalic> = <legacyItalic xmlns="">value</legacyItalic>;        // set property value
variable = objectPtr-&gt;<legacyItalic xmlns="">property</legacyItalic>;     // get property value</code>
          <para>
            <caps:sentence id="src23" class="srcSentence">Notice you do not have to code:</caps:sentence>
          </para>
          <code>objectPtr-&gt;Put<legacyItalic xmlns="">Property</legacyItalic>(<legacyItalic xmlns="">value</legacyItalic>);      // set property value
variable = objectPtr-&gt;Get<legacyItalic xmlns="">Property</legacyItalic>;  // get property value</code>
          <para>
            <caps:sentence id="src24" class="srcSentence">The compiler will generate the appropriate <legacyBold>Get</legacyBold><legacyItalic>-</legacyItalic>, <legacyBold>Put</legacyBold>-, or <legacyBold>PutRef</legacyBold><legacyItalic>Property</legacyItalic> call based on what alternative syntax is declared and whether the property is being read or written.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">The <legacyBold>__declspec(property...)</legacyBold> compiler directive can only declare <legacyBold>get</legacyBold>, <legacyBold>put</legacyBold>, or <legacyBold>get</legacyBold> and <legacyBold>put</legacyBold> alternative syntax for a function.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> Read-only operations only have a <legacyBold>get</legacyBold> declaration; write-only operations only have a <legacyBold>put</legacyBold> declaration; operations that are both read and write have both <legacyBold>get</legacyBold> and <legacyBold>put</legacyBold> declarations.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">Only two declarations are possible with this directive; however, each property may have three property functions: <legacyBold>Get</legacyBold><legacyItalic>Property</legacyItalic>, <legacyBold>Put</legacyBold><legacyItalic>Property</legacyItalic>, and <legacyBold>PutRef</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> In that case, only two forms of the property have the alternative syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">For example, the <legacyBold>Command</legacyBold> object <legacyBold>ActiveConnection</legacyBold> property is declared with an alternative syntax for <legacyBold>Get</legacyBold><legacyItalic>ActiveConnection</legacyItalic> and <legacyBold>PutRef</legacyBold><legacyItalic>ActiveConnection</legacyItalic>.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> The <legacyBold>PutRef</legacyBold>- syntax is a good choice because in practice, you will typically want to put an open <legacyBold>Connection</legacyBold> object (that is, a <legacyBold>Connection</legacyBold> object pointer) in this property.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> On the other hand, the <legacyBold>Recordset</legacyBold> object has <legacyBold>Get</legacyBold>-, <legacyBold>Put</legacyBold>-, and <legacyBold>PutRef</legacyBold><legacyItalic>ActiveConnection</legacyItalic> operations, but no alternative syntax.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src32" class="srcSentence">Collections, the GetItem Method, and the Item Property</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src33" class="srcSentence">ADO defines several collections, including <legacyBold>Fields</legacyBold>, <legacyBold>Parameters</legacyBold>, <legacyBold>Properties</legacyBold>, and <legacyBold>Errors</legacyBold>.</caps:sentence>
            <caps:sentence id="src34" class="srcSentence"> In Visual C++, the <legacyBold>GetItem(</legacyBold><legacyItalic>index</legacyItalic><legacyBold>)</legacyBold> method returns a member of the collection.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence">
              <legacyItalic>Index</legacyItalic> is a <legacyBold>Variant</legacyBold>, the value of which is either a numeric index of the member in the collection, or a string containing the name of the member.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src36" class="srcSentence">The <legacyBold>__declspec(property...)</legacyBold> compiler directive declares the <legacyBold>Item</legacyBold> property as an alternative syntax to each collection's fundamental <legacyBold>GetItem() </legacyBold>method.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> The alternative syntax uses square brackets and looks similar to an array reference.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> In general, the two forms look like the following:</caps:sentence>
          </para>
          <code>
            <legacyItalic>collectionPtr-&gt;</legacyItalic>GetItem(index);
<legacyItalic>collectionPtr</legacyItalic>-&gt;Item[index];</code>
          <para>
            <caps:sentence id="src39" class="srcSentence">For example, assign a value to a field of a <legacyBold>Recordset</legacyBold> object, named <legacyBold><legacyItalic>rs</legacyItalic></legacyBold>, derived from the <legacyBold>authors</legacyBold> table of the <legacyBold>pubs</legacyBold> database.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> Use the <legacyBold>Item()</legacyBold> property to access the third <legacyBold>Field</legacyBold> of the <legacyBold>Recordset</legacyBold> object <legacyBold>Fields</legacyBold> collection (collections are indexed from zero; assume the third field is named <legacyBold><legacyItalic>au_fname</legacyItalic></legacyBold>).</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> Then call the <legacyBold>Value()</legacyBold> method on the <legacyBold>Field</legacyBold> object to assign a string value.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src42" class="srcSentence">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</caps:sentence>
          </para>
          <code>rs.Fields.Item(2).Value = "<legacyItalic xmlns="">value</legacyItalic>"
rs.Fields.Item("au_fname").Value = "<legacyItalic xmlns="">value</legacyItalic>"
rs(2) = "<legacyItalic xmlns="">value</legacyItalic>"
rs!au_fname = "<legacyItalic xmlns="">value</legacyItalic>"</code>
          <para>
            <caps:sentence id="src43" class="srcSentence">The equivalent in Visual C++ to the first two forms above is:</caps:sentence>
          </para>
          <code>rs-&gt;Fields-&gt;GetItem(long(2))-&gt;PutValue("<legacyItalic xmlns="">value</legacyItalic>"); 
rs-&gt;Fields-&gt;GetItem("au_fname")-&gt;PutValue("<legacyItalic xmlns="">value</legacyItalic>");</code>
          <para>
            <caps:sentence id="src44" class="srcSentence">-or- (the alternative syntax for the <legacyBold>Value</legacyBold> property is also shown)</caps:sentence>
          </para>
          <code>rs-&gt;Fields-&gt;Item[long(2)]-&gt;Value = "<legacyItalic xmlns="">value</legacyItalic>";
rs-&gt;Fields-&gt;Item["au_fname"]-&gt;Value = "<legacyItalic xmlns="">value</legacyItalic>";</code>
          <para>
            <caps:sentence id="src45" class="srcSentence">For examples of iterating through a collection, see the "ADO Collections" section of "ADO Reference".</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src46" class="srcSentence">COM-Specific Data Types</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src47" class="srcSentence">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent.</caps:sentence>
            <caps:sentence id="src48" class="srcSentence"> These include standard data types such as <legacyBold>unsigned char</legacyBold> for a Visual Basic <legacyBold>Byte</legacyBold>, <legacyBold>short</legacyBold> for <legacyBold>Integer</legacyBold>, and <legacyBold>long </legacyBold>for <legacyBold>Long</legacyBold>.</caps:sentence>
            <caps:sentence id="src49" class="srcSentence"> Look in the Syntax Indexesto see exactly what is required for the operands of a given method or property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src50" class="srcSentence">The exceptions to this rule are the data types specific to COM: <legacyBold>Variant</legacyBold>, <legacyBold>BSTR</legacyBold>, and <legacyBold>SafeArray</legacyBold>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src51" class="srcSentence">Variant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src52" class="srcSentence">A <legacyBold>Variant</legacyBold> is a structured data type that contains a value member and a data type member.</caps:sentence>
                <caps:sentence id="src53" class="srcSentence"> A <legacyBold>Variant</legacyBold> may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on.</caps:sentence>
                <caps:sentence id="src54" class="srcSentence"> COM also provides methods that make it easy to convert one data type to another.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src55" class="srcSentence">The <legacyBold>_variant_t</legacyBold> class encapsulates and manages the <legacyBold>Variant</legacyBold> data type.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src56" class="srcSentence">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a <legacyBold>_variant_t</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src57" class="srcSentence">This rule is explicitly true when the <legacyBold>Parameters</legacyBold> section in the topics of the ADO API Reference says an operand is a <legacyBold>Variant</legacyBold>.</caps:sentence>
                <caps:sentence id="src58" class="srcSentence"> One exception is when the documentation explicitly says the operand takes a standard data type, such as <legacyBold>Long</legacyBold> or <legacyBold>Byte</legacyBold>, or an enumeration.</caps:sentence>
                <caps:sentence id="src59" class="srcSentence"> Another exception is when the operand takes a <legacyBold>String</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src60" class="srcSentence">BSTR</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src61" class="srcSentence">A <legacyBold>BSTR</legacyBold> (<legacyBold>B</legacyBold>asic <legacyBold>STR</legacyBold>ing) is a structured data type that contains a character string and the string's length.</caps:sentence>
                <caps:sentence id="src62" class="srcSentence"> COM provides methods to allocate, manipulate, and free a <legacyBold>BSTR</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src63" class="srcSentence">The <legacyBold>_bstr_t</legacyBold> class encapsulates and manages the <legacyBold>BSTR</legacyBold> data type.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src64" class="srcSentence">When the ADO API Reference says a method or property takes a <legacyBold>String</legacyBold> value, it means the value is in the form of a <legacyBold>_bstr_t</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src65" class="srcSentence">Casting _variant_t and _bstr_t Classes</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src66" class="srcSentence">Often it is not necessary to explicitly code a <legacyBold>_variant_t</legacyBold> or <legacyBold>_bstr_t</legacyBold> in an argument to an operation.</caps:sentence>
                <caps:sentence id="src67" class="srcSentence"> If the <legacyBold>_variant_t</legacyBold> or <legacyBold>_bstr_t</legacyBold> class has a constructor that matches the data type of the argument, the compiler will generate the appropriate <legacyBold>_variant_t</legacyBold> or <legacyBold>_bstr_t</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src68" class="srcSentence">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src69" class="srcSentence">For example, the declaration for the <legacyBold>Recordset::Open</legacyBold> method is:</caps:sentence>
              </para>
              <code>    HRESULT Open (
        const _variant_t &amp; Source,
        const _variant_t &amp; ActiveConnection,
        enum CursorTypeEnum CursorType,
        enum LockTypeEnum LockType,
        long Options );</code>
              <para>
                <caps:sentence id="src70" class="srcSentence">The <codeInline>ActiveConnection </codeInline>argument takes a reference to a <legacyBold>_variant_t</legacyBold>, which you may code as a connection string or a pointer to an open <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src71" class="srcSentence">The correct <legacyBold>_variant_t</legacyBold> will be constructed implicitly if you pass a string such as "<codeInline>DSN=pubs;uid=MyUserName;pwd=MyPassword;</codeInline>", or a pointer such as "<codeInline>(IDispatch *) pConn</codeInline>".</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src72" class="srcSentence">If you are connecting to a data source provider that supports Windows authentication, you should specify <system>Trusted_Connection=yes</system> or <system>Integrated Security = SSPI</system> instead of user ID and password information in the connection string.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src73" class="srcSentence">Or you may explicitly code a <legacyBold>_variant_t</legacyBold> containing a pointer such as "<codeInline>_variant_t((IDispatch *) pConn, true)</codeInline>".</caps:sentence>
                <caps:sentence id="src74" class="srcSentence"> The cast, <codeInline>(IDispatch *)</codeInline>, resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src75" class="srcSentence">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface.</caps:sentence>
                <caps:sentence id="src76" class="srcSentence"> Whenever a pointer to an ADO object must be passed as a <legacyBold>Variant</legacyBold>, that pointer must be cast as a pointer to an IDispatch interface.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src77" class="srcSentence">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of <codeInline>true</codeInline>.</caps:sentence>
                <caps:sentence id="src78" class="srcSentence"> This argument causes the <legacyBold>Variant</legacyBold> constructor to call its <legacyBold>AddRef</legacyBold>() method, which compensates for ADO automatically calling the <legacyBold>_variant_t::Release</legacyBold>() method when the ADO method or property call completes.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src79" class="srcSentence">SafeArray</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src80" class="srcSentence">A <legacyBold>SafeArray</legacyBold> is a structured data type that contains an array of other data types.</caps:sentence>
                <caps:sentence id="src81" class="srcSentence"> A <legacyBold>SafeArray</legacyBold> is called <legacyItalic>safe</legacyItalic> because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src82" class="srcSentence">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a <legacyBold>SafeArray</legacyBold>, not a native C/C++ array.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src83" class="srcSentence">For example, the second parameter of the <legacyBold>Connection</legacyBold> object <legacyBold>OpenSchema</legacyBold> method requires an array of <legacyBold>Variant</legacyBold> values.</caps:sentence>
                <caps:sentence id="src84" class="srcSentence"> Those <legacyBold>Variant</legacyBold> values must be passed as elements of a <legacyBold>SafeArray</legacyBold>, and that <legacyBold>SafeArray</legacyBold> must be set as the value of another <legacyBold>Variant</legacyBold>.</caps:sentence>
                <caps:sentence id="src85" class="srcSentence"> It is that other <legacyBold>Variant</legacyBold> that is passed as the second argument of <legacyBold>OpenSchema</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src86" class="srcSentence">As further examples, the first argument of the <legacyBold>Find</legacyBold> method is a <legacyBold>Variant</legacyBold> whose value is a one-dimensional <legacyBold>SafeArray</legacyBold>; each of the optional first and second arguments of <legacyBold>AddNew</legacyBold> is a one-dimensional <legacyBold>SafeArray</legacyBold>; and the return value of the <legacyBold>GetRows</legacyBold> method is a <legacyBold>Variant</legacyBold> whose value is a two-dimensional <legacyBold>SafeArray</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src87" class="srcSentence">Missing and Default Parameters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src88" class="srcSentence">Visual Basic allows missing parameters in methods.</caps:sentence>
            <caps:sentence id="src89" class="srcSentence"> For example, the <legacyBold>Recordset</legacyBold> object <legacyBold>Open</legacyBold> method has five parameters, but you can skip intermediate parameters and leave off trailing parameters.</caps:sentence>
            <caps:sentence id="src90" class="srcSentence"> A default <legacyBold>BSTR</legacyBold> or <legacyBold>Variant</legacyBold> will be substituted depending on the data type of the missing operand.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src91" class="srcSentence">In C/C++, all operands must be specified.</caps:sentence>
            <caps:sentence id="src92" class="srcSentence"> If you want to specify a missing parameter whose data type is a string, specify a <legacyBold>_bstr_t</legacyBold> containing a null string.</caps:sentence>
            <caps:sentence id="src93" class="srcSentence"> If you want to specify a missing parameter whose data type is a <legacyBold>Variant</legacyBold>, specify a <legacyBold>_variant_t</legacyBold> with a value of DISP_E_PARAMNOTFOUND and a type of VT_ERROR.</caps:sentence>
            <caps:sentence id="src94" class="srcSentence"> Alternatively, specify the equivalent <legacyBold>_variant_t</legacyBold> constant, <legacyBold>vtMissing</legacyBold>, which is supplied by the <legacyBold>#import</legacyBold> directive.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src95" class="srcSentence">Three methods are exceptions to the typical use of <legacyBold>vtMissing</legacyBold>.</caps:sentence>
            <caps:sentence id="src96" class="srcSentence"> These are the <legacyBold>Execute</legacyBold> methods of the <legacyBold>Connection</legacyBold> and <legacyBold>Command</legacyBold> objects, and the <legacyBold>NextRecordset</legacyBold> method of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src97" class="srcSentence"> The following are their signatures:</caps:sentence>
          </para>
          <code>_RecordsetPtr &lt;A HREF="mdmthcnnexecute.htm"&gt;Execute&lt;/A&gt;( _bstr_t <legacyItalic xmlns="">CommandText</legacyItalic>, VARIANT * <legacyItalic xmlns="">RecordsAffected</legacyItalic>, 
        long<legacyItalic xmlns=""> Options </legacyItalic>);  // Connection
_RecordsetPtr &lt;A HREF="mdmthcmdexecute.htm"&gt;Execute&lt;/A&gt;( VARIANT * <legacyItalic xmlns="">RecordsAffected</legacyItalic>, VARIANT * <legacyItalic xmlns="">Parameters</legacyItalic>, 
        long<legacyItalic xmlns=""> Options </legacyItalic>);  // Command
_RecordsetPtr &lt;A HREF="mdmthnextrec.htm"&gt;NextRecordset&lt;/A&gt;( VARIANT *<legacyItalic xmlns=""> RecordsAffected </legacyItalic>);  // Recordset</code>
          <para>
            <caps:sentence id="src98" class="srcSentence">The parameters, <legacyItalic>RecordsAffected</legacyItalic> and <legacyItalic>Parameters</legacyItalic>, are pointers to a <legacyBold>Variant</legacyBold>.</caps:sentence>
            <caps:sentence id="src99" class="srcSentence">
              <legacyItalic>Parameters</legacyItalic> is an input parameter which specifies the address of a <legacyBold>Variant</legacyBold> containing a single parameter, or array of parameters, that will modify the command being executed.</caps:sentence>
            <caps:sentence id="src100" class="srcSentence">
              <legacyItalic>RecordsAffected </legacyItalic>is an output parameter that specifies the address of a <legacyBold>Variant</legacyBold>, where the number of rows affected by the method is returned.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src101" class="srcSentence">In the <legacyBold>Command</legacyBold> object <legacyBold>Execute</legacyBold> method, indicate that no parameters are specified by setting <legacyItalic>Parameters</legacyItalic> to either <codeInline>&amp;vtMissing</codeInline> (which is recommended) or to the null pointer (that is, <legacyBold>NULL</legacyBold> or zero (0)).</caps:sentence>
            <caps:sentence id="src102" class="srcSentence"> If <legacyItalic>Parameters</legacyItalic> is set to the null pointer, the method internally substitutes the equivalent of <legacyBold>vtMissing</legacyBold>, and then completes the operation.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src103" class="srcSentence">In all the methods, indicate that the number of records affected should not be returned by setting <legacyItalic>RecordsAffected </legacyItalic>to the null pointer.</caps:sentence>
            <caps:sentence id="src104" class="srcSentence"> In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src105" class="srcSentence">Thus, for these three methods, it is valid to code something such as:</caps:sentence>
          </para>
          <code>pConnection-&gt;Execute("<legacyItalic xmlns="">commandText</legacyItalic>", NULL, adCmdText); 
pCommand-&gt;Execute(NULL, NULL, adCmdText);
pRecordset-&gt;NextRecordset(NULL);</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src106" class="srcSentence">Error Handling</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src107" class="srcSentence">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</caps:sentence>
            <caps:sentence id="src108" class="srcSentence"> The <legacyBold>#import</legacyBold> directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</caps:sentence>
            <caps:sentence id="src109" class="srcSentence"> If the HRESULT indicates failure, the wrapper code throws a COM error by calling _com_issue_errorex() with the HRESULT return code as an argument.</caps:sentence>
            <caps:sentence id="src110" class="srcSentence"> COM error objects can be caught in a <legacyBold>try</legacyBold>-<legacyBold>catch</legacyBold> block.</caps:sentence>
            <caps:sentence id="src111" class="srcSentence"> (For efficiency's sake, catch a reference to a <legacyBold>_com_error</legacyBold> object.)</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src112" class="srcSentence">Remember, these are ADO errors: they result from the ADO operation failing.</caps:sentence>
            <caps:sentence id="src113" class="srcSentence"> Errors returned by the underlying provider appear as <legacyBold>Error</legacyBold> objects in the <legacyBold>Connection</legacyBold> object <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src114" class="srcSentence">The <legacyBold>#import</legacyBold> directive creates only error handling routines for methods and properties declared in the ADO .dll.</caps:sentence>
            <caps:sentence id="src115" class="srcSentence"> However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</caps:sentence>
            <caps:sentence id="src116" class="srcSentence"> See the topic, <legacyLink xlink:href="2952ece0-7217-4448-bb09-f6b64f43b7e2">Visual C++ Extensions</legacyLink>, or the code in the following sections for examples.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src117" class="srcSentence">Visual C++ Equivalents of Visual Basic Conventions</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src118" class="srcSentence">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src119" class="srcSentence">Declaring an ADO Object</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src120" class="srcSentence">In Visual Basic, an ADO object variable (in this case for a <legacyBold>Recordset</legacyBold> object) is declared as follows:</caps:sentence>
              </para>
              <code>Dim rst As ADODB.Recordset</code>
              <para>
                <caps:sentence id="src121" class="srcSentence">The clause, "<codeInline>ADODB.Recordset</codeInline>", is the ProgID of the <legacyBold>Recordset</legacyBold> object as defined in the registry.</caps:sentence>
                <caps:sentence id="src122" class="srcSentence"> A new instance of a <legacyBold>Record</legacyBold> object is declared as follows:</caps:sentence>
              </para>
              <code>Dim rst As New ADODB.Recordset</code>
              <para>
                <caps:sentence id="src123" class="srcSentence">-or-</caps:sentence>
              </para>
              <code>Dim rst As ADODB.Recordset
Set rst = New ADODB.Recordset</code>
              <para>
                <caps:sentence id="src124" class="srcSentence">In Visual C++, the <legacyBold>#import </legacyBold>directive generates smart pointer-type declarations for all the ADO objects.</caps:sentence>
                <caps:sentence id="src125" class="srcSentence"> For example, a variable that points to a <legacyBold>_Recordset</legacyBold> object is of type <legacyBold>_RecordsetPtr</legacyBold>, and is declared as follows:</caps:sentence>
              </para>
              <code>_RecordsetPtr  rs;</code>
              <para>
                <caps:sentence id="src126" class="srcSentence">A variable that points to a new instance of a <legacyBold>_Recordset</legacyBold> object is declared as follows:</caps:sentence>
              </para>
              <code>_RecordsetPtr  rs("ADODB.Recordset");</code>
              <para>
                <caps:sentence id="src127" class="srcSentence">-or-</caps:sentence>
              </para>
              <code>_RecordsetPtr  rs;
rs.CreateInstance("ADODB.Recordset");</code>
              <para>
                <caps:sentence id="src128" class="srcSentence">-or-</caps:sentence>
              </para>
              <code>_RecordsetPtr  rs;
rs.CreateInstance(__uuidof(_Recordset));</code>
              <para>
                <caps:sentence id="src129" class="srcSentence">After the <legacyBold>CreateInstance</legacyBold> method is called, the variable can be used as follows:</caps:sentence>
              </para>
              <code>rs-&gt;Open(...);</code>
              <para>
                <caps:sentence id="src130" class="srcSentence">Notice that in one case, the "<codeInline>.</codeInline>" operator is used as if the variable were an instance of a class (<codeInline>rs.CreateInstance</codeInline>), and in another case, the "<codeInline>-&gt;</codeInline>" operator is used as if the variable were a pointer to an interface (<codeInline>rs-&gt;Open</codeInline>).</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src131" class="srcSentence">One variable can be used in two ways because the "<codeInline>-&gt;</codeInline>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</caps:sentence>
                <caps:sentence id="src132" class="srcSentence"> A private class member of the instance variable contains a pointer to the <legacyBold>_Recordset</legacyBold> interface; the "<codeInline>-&gt;</codeInline>" operator returns that pointer; and the returned pointer accesses the members of the <legacyBold>_Recordset</legacyBold> object.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src133" class="srcSentence">Coding a Missing Parameter — String</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src134" class="srcSentence">When you need to code a missing <legacyBold>String</legacyBold> operand in Visual Basic, you merely omit the operand.</caps:sentence>
                <caps:sentence id="src135" class="srcSentence"> You must specify the operand in Visual C++.</caps:sentence>
                <caps:sentence id="src136" class="srcSentence"> Code a <legacyBold>_bstr_t</legacyBold> that has an empty string as a value.</caps:sentence>
              </para>
              <code>_bstr_t strMissing(L"");</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src137" class="srcSentence">Coding a Missing Parameter — Variant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src138" class="srcSentence">When you need to code a missing <legacyBold>Variant</legacyBold> operand in Visual Basic, you merely omit the operand.</caps:sentence>
                <caps:sentence id="src139" class="srcSentence"> You must specify all operands in Visual C++.</caps:sentence>
                <caps:sentence id="src140" class="srcSentence"> Code a missing <legacyBold>Variant</legacyBold> parameter with a <legacyBold>_variant_t</legacyBold> set to the special value, DISP_E_PARAMNOTFOUND, and type, VT_ERROR.</caps:sentence>
                <caps:sentence id="src141" class="srcSentence"> Alternatively, specify <legacyBold>vtMissing</legacyBold>, which is an equivalent predefined constant supplied by the <legacyBold>#import</legacyBold> directive.</caps:sentence>
              </para>
              <code>_variant_t  vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); </code>
              <para>
                <caps:sentence id="src142" class="srcSentence">-or use -</caps:sentence>
              </para>
              <code>...vtMissing...;</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src143" class="srcSentence">Declaring a Variant</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src144" class="srcSentence">In Visual Basic, a <legacyBold>Variant</legacyBold> is declared with the <legacyBold>Dim</legacyBold> statement as follows:</caps:sentence>
              </para>
              <code>Dim <legacyItalic xmlns="">VariableName</legacyItalic> As Variant</code>
              <para>
                <caps:sentence id="src145" class="srcSentence">In Visual C++, declare a variable as type <legacyBold>_variant_t</legacyBold>.</caps:sentence>
                <caps:sentence id="src146" class="srcSentence"> A few schematic <legacyBold>_variant_t </legacyBold>declarations are shown below.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src147" class="srcSentence">These declarations merely give a rough idea of what you would code in your own program.</caps:sentence>
                  <caps:sentence id="src148" class="srcSentence"> For more information, see the examples below, and the Visual C++documentation.</caps:sentence>
                </para>
              </alert>
              <code>_variant_t  VariableName(<legacyItalic xmlns="">value</legacyItalic>);
_variant_t  VariableName((<legacyItalic xmlns="">data type cast</legacyItalic>) <legacyItalic xmlns="">value</legacyItalic>);
_variant_t  VariableName(<legacyItalic xmlns="">value, </legacyItalic>VT<legacyItalic xmlns="">_DATATYPE</legacyItalic>);
_variant_t  VariableName(interface * <legacyItalic xmlns="">value, </legacyItalic>bool fAddRef = true);</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src149" class="srcSentence">Using Arrays of Variants</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src150" class="srcSentence">In Visual Basic, arrays of <legacyBold>Variants</legacyBold> can be coded with the <legacyBold>Dim</legacyBold> statement, or you may use the <legacyBold>Array</legacyBold> function, as demonstrated in the following example code:</caps:sentence>
              </para>
              <code>Public Sub ArrayOfVariants
Dim cn As ADODB.Connection
Dim rs As ADODB.Recordset
Dim fld As ADODB.Field

    cn.Open "DSN=pubs"
    rs = cn.OpenSchema(adSchemaColumns, _
        Array(Empty, Empty, "authors", Empty))
    For Each fld in rs.Fields
        Debug.Print "Name = "; fld.Name
    Next fld
    rs.Close
    cn.Close
End Sub</code>
              <para>
                <caps:sentence id="src151" class="srcSentence">The following Visual C++ example demonstrates using a <legacyBold>SafeArray</legacyBold> used with a <legacyBold>_variant_t</legacyBold>.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src152" class="srcSentence">Notes</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">The following notes correspond to commented sections in the code example.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src154" class="srcSentence">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src155" class="srcSentence">You only need a one-dimensional array, so you can use <legacyBold>SafeArrayCreateVector</legacyBold>, instead of the general purpose <legacyBold>SAFEARRAYBOUND</legacyBold> declaration and <legacyBold>SafeArrayCreate</legacyBold> function.</caps:sentence>
                        <caps:sentence id="src156" class="srcSentence"> The following is what that code would look like using <legacyBold>SafeArrayCreate</legacyBold>:</caps:sentence>
                      </para>
                      <code>   SAFEARRAYBOUND   sabound[1];
   sabound[0].lLbound = 0;
   sabound[0].cElements = 4;
   pSa = SafeArrayCreate(VT_VARIANT, 1, sabound);</code>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src157" class="srcSentence">The schema identified by the enumerated constant, <legacyBold>adSchemaColumns</legacyBold>, is associated with four constraint columns: TABLE_CATALOG, TABLE_SCHEMA, TABLE_NAME, and COLUMN_NAME.</caps:sentence>
                        <caps:sentence id="src158" class="srcSentence"> Therefore, an array of <legacyBold>Variant</legacyBold> values with four elements is created.</caps:sentence>
                        <caps:sentence id="src159" class="srcSentence"> Then a constraint value that corresponds to the third column, TABLE_NAME, is specified.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src160" class="srcSentence">The <legacyBold>Recordset</legacyBold> that is returned consists of several columns, a subset of which is the constraint columns.</caps:sentence>
                        <caps:sentence id="src161" class="srcSentence"> The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src162" class="srcSentence">Those familiar with <legacyBold>SafeArrays </legacyBold>may be surprised that <legacyBold>SafeArrayDestroy</legacyBold>() is not called before the exit.</caps:sentence>
                        <caps:sentence id="src163" class="srcSentence"> In fact, calling <legacyBold>SafeArrayDestroy</legacyBold>() in this case will cause a run-time exception.</caps:sentence>
                        <caps:sentence id="src164" class="srcSentence"> The reason is that the destructor for <codeInline>vtCriteria</codeInline> will call <legacyBold>VariantClear</legacyBold>() when the <legacyBold>_variant_t </legacyBold>goes out of scope, which will free the <legacyBold>SafeArray</legacyBold>.</caps:sentence>
                        <caps:sentence id="src165" class="srcSentence"> Calling <legacyBold>SafeArrayDestroy</legacyBold>, without manually clearing the <legacyBold>_variant_t</legacyBold>, would cause the destructor to try to clear an invalid <legacyBold>SafeArray</legacyBold> pointer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src166" class="srcSentence">If <legacyBold>SafeArrayDestroy</legacyBold> were called, the code would look like this:</caps:sentence>
                      </para>
                      <code>      TESTHR(SafeArrayDestroy(pSa));
   vtCriteria.vt = VT_EMPTY;
      vtCriteria.parray = NULL;</code>
                      <para>
                        <caps:sentence id="src167" class="srcSentence">However, it is much simpler to let the <legacyBold>_variant_t</legacyBold> manage the <legacyBold>SafeArray</legacyBold>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <code>// Visual_CPP_ADO_Prog_1.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

// Note 1
inline void TESTHR( HRESULT _hr ) { 
   if FAILED(_hr) 
      _com_issue_error(_hr); 
}

int main() {
   CoInitialize(NULL);
   try {
      _RecordsetPtr pRs("ADODB.Recordset");
      _ConnectionPtr pCn("ADODB.Connection");
      _variant_t vtTableName("authors"), vtCriteria;
      long ix[1];
      SAFEARRAY *pSa = NULL;

      pCn-&gt;Provider = "sqloledb";
      pCn-&gt;Open("Data Source='(local)';Initial Catalog='pubs';Integrated Security=SSPI", "", "", adConnectUnspecified);
      // Note 2, Note 3
      pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4);
      if (!pSa) 
         _com_issue_error(E_OUTOFMEMORY);

      // Specify TABLE_NAME in the third array element (index of 2). 
      ix[0] = 2;      
      TESTHR(SafeArrayPutElement(pSa, ix, &amp;vtTableName));

      // There is no Variant constructor for a SafeArray, so manually set the 
      // type (SafeArray of Variant) and value (pointer to a SafeArray).

      vtCriteria.vt = VT_ARRAY | VT_VARIANT;
      vtCriteria.parray = pSa;

      pRs = pCn-&gt;OpenSchema(adSchemaColumns, vtCriteria, vtMissing);

      long limit = pRs-&gt;GetFields()-&gt;Count;
      for ( long x = 0 ; x &lt; limit ; x++ )
         printf( "%d: %s\n", x + 1, ((char*) pRs-&gt;GetFields()-&gt;Item[x]-&gt;Name) );
      // Note 4
      pRs-&gt;Close();
      pCn-&gt;Close();
   }
   catch (_com_error &amp;e) {
      printf("Error:\n");
      printf("Code = %08lx\n", e.Error());
      printf("Code meaning = %s\n", (char*) e.ErrorMessage());
      printf("Source = %s\n", (char*) e.Source());
      printf("Description = %s\n", (char*) e.Description());
   }
   CoUninitialize();
}</code>
                </content>
              </section>
            </sections>
          </section>
          <section>
            <title>
              <caps:sentence id="src168" class="srcSentence">Using Property Get/Put/PutRef</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src169" class="srcSentence">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</caps:sentence>
              </para>
              <code>Public Sub GetPutPutRef
Dim rs As New ADODB.Recordset
Dim cn As New ADODB.Connection
Dim sz as Integer
cn.Open "Provider=sqloledb;Data Source=yourserver;" &amp; _
         "Initial Catalog=pubs;Integrated Security=SSPI;"
rs.PageSize = 10
sz = rs.PageSize
rs.ActiveConnection = cn
rs.Open "authors",,adOpenStatic
' ...
rs.Close
cn.Close
End Sub</code>
              <para>
                <caps:sentence id="src170" class="srcSentence">This Visual C++ example demonstrates the <legacyBold>Get</legacyBold>/<legacyBold>Put</legacyBold>/<legacyBold>PutRef</legacyBold><legacyItalic>Property</legacyItalic>.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src171" class="srcSentence">Notes</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">The following notes correspond to commented sections in the code example.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src173" class="srcSentence">This example uses two forms of a missing string argument: an explicit constant, <legacyBold>strMissing</legacyBold>, and a string that the compiler will use to create a temporary <legacyBold>_bstr_t</legacyBold> that will exist for the scope of the <legacyBold>Open</legacyBold> method.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src174" class="srcSentence">It is not necessary to cast the operand of <codeInline>rs-&gt;PutRefActiveConnection(cn)</codeInline> to <codeInline>(IDispatch *)</codeInline> because the type of the operand is already <codeInline>(IDispatch *)</codeInline>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <code>// Visual_CPP_ado_prog_2.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

int main() {
   CoInitialize(NULL);
   try {
      _ConnectionPtr cn("ADODB.Connection");
      _RecordsetPtr rs("ADODB.Recordset");
      _bstr_t strMissing(L"");
      long oldPgSz = 0, newPgSz = 5;

      // Note 1
      cn-&gt;Provider = "sqloledb";
      cn-&gt;Open("Data Source='(local)';Initial Catalog=pubs;Integrated Security=SSPI;", strMissing, "", adConnectUnspecified);

      oldPgSz = rs-&gt;GetPageSize();
      // -or-
      // oldPgSz = rs-&gt;PageSize;

      rs-&gt;PutPageSize(newPgSz);
      // -or-
      // rs-&gt;PageSize = newPgSz;

      // Note 2
      rs-&gt;PutRefActiveConnection( cn );
      rs-&gt;Open("authors", vtMissing, adOpenStatic, adLockReadOnly, adCmdTable);
      printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, rs-&gt;GetPageSize());
      rs-&gt;Close();
      cn-&gt;Close();
      
   }
   catch (_com_error &amp;e) {
      printf("Description = %s\n", (char*) e.Description());
   }
   ::CoUninitialize();
}</code>
                </content>
              </section>
            </sections>
          </section>
          <section>
            <title>
              <caps:sentence id="src175" class="srcSentence">Using GetItem(x) and Item[x]</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src176" class="srcSentence">This Visual Basic example demonstrates the standard and alternative syntax for <legacyBold>Item</legacyBold>().</caps:sentence>
              </para>
              <code>Public Sub GetItemItem
Dim rs As New ADODB.Recordset
Dim name as String
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _
         adLockBatchOptimistic, adTable
name = rs(0)
' -or-
name = rs.Fields.Item(0)
rs(0) = "Test"
rs.UpdateBatch
' Restore name
rs(0) = name
rs.UpdateBatch
rs.Close
End Sub</code>
              <para>
                <caps:sentence id="src177" class="srcSentence">This Visual C++ example demonstrates <legacyBold>Item</legacyBold>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src178" class="srcSentence">The following note corresponds to commented sections in the code example:  When the collection is accessed with <legacyBold>Item</legacyBold>, the index, <legacyBold>2</legacyBold>, must be cast to <legacyBold>long</legacyBold> so an appropriate constructor will be invoked.</caps:sentence>
                </para>
              </alert>
              <code>// Visual_CPP_ado_prog_3.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

void main() {
   CoInitialize(NULL);
   try {
      _ConnectionPtr cn("ADODB.Connection");
      _RecordsetPtr rs("ADODB.Recordset");
      _variant_t vtFirstName;

      cn-&gt;Provider = "sqloledb";
      cn-&gt;Open("Data Source='(local)';Initial Catalog=pubs;Integrated Security=SSPI;", "", "", adConnectUnspecified);

      rs-&gt;PutRefActiveConnection( cn );
      rs-&gt;Open("authors", vtMissing, adOpenStatic, adLockOptimistic, adCmdTable);
      rs-&gt;MoveFirst();

      // Note 1. Get a field.
      vtFirstName = rs-&gt;Fields-&gt;GetItem((long)2)-&gt;GetValue();
      // -or-
      vtFirstName = rs-&gt;Fields-&gt;Item[(long)2]-&gt;Value;

      printf( "First name = '%s'\n", (char*)( (_bstr_t)vtFirstName) );

      rs-&gt;Fields-&gt;GetItem((long)2)-&gt;Value = L"TEST";
      rs-&gt;Update(vtMissing, vtMissing);

      // Restore name
      rs-&gt;Fields-&gt;GetItem((long)2)-&gt;PutValue(vtFirstName);
      // -or-
      rs-&gt;Fields-&gt;GetItem((long)2)-&gt;Value = vtFirstName;
      rs-&gt;Update(vtMissing, vtMissing);
      rs-&gt;Close();
   }
   catch (_com_error &amp;e) {
      printf("Description = '%s'\n", (char*) e.Description());
   }
   ::CoUninitialize();
}</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src179" class="srcSentence">Casting ADO object pointers with (IDispatch *)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src180" class="srcSentence">The following Visual C++ example demonstrates using (IDispatch *) to cast ADO object pointers.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src181" class="srcSentence">Notes</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">The following notes correspond to commented sections in the code example.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src183" class="srcSentence">Specify an open <legacyBold>Connection</legacyBold> object in an explicitly coded <legacyBold>Variant</legacyBold>.</caps:sentence>
                        <caps:sentence id="src184" class="srcSentence"> Cast it with (IDispatch *) so the correct constructor will be invoked.</caps:sentence>
                        <caps:sentence id="src185" class="srcSentence"> Also, explicitly set the second <legacyBold>_variant_t</legacyBold> parameter to the default value of <legacyBold>true</legacyBold>, so the object reference count will be correct when the <legacyBold>Recordset::Open</legacyBold> operation ends.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src186" class="srcSentence">The expression, <codeInline>(_bstr_t)</codeInline>, is not a cast, but a <legacyBold>_variant_t</legacyBold> operator that extracts a <legacyBold>_bstr_t </legacyBold>string from the <legacyBold>Variant</legacyBold> returned by <legacyBold>Value</legacyBold>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">The expression, <codeInline>(char*)</codeInline>, is not a cast, but a <legacyBold>_bstr_t</legacyBold> operator that extracts a pointer to the encapsulated string in a <legacyBold>_bstr_t</legacyBold> object.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">This section of code demonstrates some of the useful behaviors of <legacyBold>_variant_t</legacyBold> and <legacyBold>_bstr_t</legacyBold> operators.</caps:sentence>
                  </para>
                  <code>// Visual_CPP_ado_prog_4.cpp
// compile with: /EHsc
#import "msado15.dll" no_namespace rename("EOF", "EndOfFile")

int main() {
   CoInitialize(NULL);
   try {
      _ConnectionPtr pConn("ADODB.Connection");
      _RecordsetPtr pRst("ADODB.Recordset");

      pConn-&gt;Provider = "sqloledb";
      pConn-&gt;Open("Data Source='(local)';Initial Catalog='pubs';Integrated Security=SSPI", "", "", adConnectUnspecified);

      // Note 1.
      pRst-&gt;Open("authors", _variant_t((IDispatch *) pConn, true), adOpenStatic, adLockReadOnly, adCmdTable);
      pRst-&gt;MoveLast();

      // Note 2.
      printf("Last name is '%s %s'\n", 
         (char*) ((_bstr_t) pRst-&gt;GetFields()-&gt;GetItem("au_fname")-&gt;GetValue()),
         (char*) ((_bstr_t) pRst-&gt;Fields-&gt;Item["au_lname"]-&gt;Value));

      pRst-&gt;Close();
      pConn-&gt;Close();
   }
   catch (_com_error &amp;e) {
      printf("Description = '%s'\n", (char*) e.Description());
   }   
   ::CoUninitialize();
}</code>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
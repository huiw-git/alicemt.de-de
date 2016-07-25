---
title: "ADO Glossary"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b0478836-4123-4357-969a-c5784fc28be5
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
# ADO Glossary
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c52e9df8bbf3c6497dd6c254bebbfdb6" id="tgt1" class="tgtSentence">This topic defines terms relevant to ADO.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="0cc175b9c0f1b6a831c399e269772661" id="tgt2" class="tgtSentence">A</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="aeaca01b9d18ded27856d3e33244f4ca" id="tgt3" class="tgtSentence">absolute URL</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="fa455fefd328fdb229a081e4a6b2735f" id="tgt4" class="tgtSentence">A fully-qualified URL that specifies the location of a resource that resides on the Internet or an intranet.</caps:sentence>
                <caps:sentence sentenceid="ecf16c207cdb342e2075a145edb46bc6" id="tgt5" class="tgtSentence"> See also <newTerm>URL</newTerm> and <newTerm>relative URL</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="0c3e4bf48f0a577895abf88b2f34e24e" id="tgt6" class="tgtSentence">ActiveX control</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="df02358c2a922372d21134f4bcd1c400" id="tgt7" class="tgtSentence">Self-registering, in-process COM component that often has a visual element either at design time or run time.</caps:sentence>
                <caps:sentence sentenceid="4bb33ce9a3552dbde5300f29bcf58984" id="tgt8" class="tgtSentence"> ActiveX controls also have the ability to communicate with an Active Document container, such as Microsoft Internet Explorer.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8aa6f04f146b3e842d1943957610cb10" id="tgt9" class="tgtSentence">ADISAPI (Advanced Data Internet Server Application Programming Interface)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f7da06766524a796622c2d3f71cbac1b" id="tgt10" class="tgtSentence">An ISAPI DLL that provides parsing, Automation control, Recordset marshaling, and MIME packaging.</caps:sentence>
                <caps:sentence sentenceid="d3baf420f75bf47acfb7e4a04e3a6508" id="tgt11" class="tgtSentence"> The ADISAPI component works through the API provided by Internet Information Services (IIS).</caps:sentence>
                <caps:sentence sentenceid="4572bbe1d4920cccd0454b9de7d429dd" id="tgt12" class="tgtSentence"> See also <newTerm>ISAPI</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="59b2ba42edd99f8912c321efe6427b2a" id="tgt13" class="tgtSentence">aggregate function</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="c6c0e48c53fee4d7bb4111a7c97e0d58" id="tgt14" class="tgtSentence">In a query, a function such as COUNT, AVG, or STDEV that calculates a value using all the rows in a column of a table.</caps:sentence>
                <caps:sentence sentenceid="aea56c7f5edc87f68e28c7fa7f9b3f15" id="tgt15" class="tgtSentence"> In writing expressions and in programming, you can use SQL aggregate functions (including the three listed above) and domain aggregate functions to determine various statistics.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="724874d1be77f450a09b305fc1534afb" id="tgt16" class="tgtSentence">alias</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="effd8a4f347de7e92925b90183b9fa41" id="tgt17" class="tgtSentence">An alternate name you give to a column or expression in an SQL SELECT statement, often shorter or more meaningful.</caps:sentence>
                <caps:sentence sentenceid="27a4dfe5584e6ad86fb798bee9917064" id="tgt18" class="tgtSentence"> For example, BobSales is the alias in the following SELECT statement: "Select wr-Sales as BobSales from SalesDB".</caps:sentence>
                <caps:sentence sentenceid="ccdd00fae259c4944f454a0a1c06cc27" id="tgt19" class="tgtSentence"> An alias can be used to dynamically assign columns to control bindings on the DataControl object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="898db0726efd40f8f674d6d264249ad9" id="tgt20" class="tgtSentence">apartment threading</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="263a902d381ed8a96d67beeb8cec0be8" id="tgt21" class="tgtSentence">A COM threading model where all calls to an object occur on one thread.</caps:sentence>
                <caps:sentence sentenceid="127b3acf3d752c92f5cbacbbdf0d7e39" id="tgt22" class="tgtSentence"> In apartment threading, COM synchronizes and marshals calls.</caps:sentence>
                <caps:sentence sentenceid="219ed2889948d6ad9c22bb153c8779e0" id="tgt23" class="tgtSentence"> See also <newTerm>COMmddefcom</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d62936a880a8a277aabf4870485ae4f9" id="tgt24" class="tgtSentence">asynchronous operation </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b94b6f24a1153282654b8e7b3b0d26bb" id="tgt25" class="tgtSentence">An operation that returns control to the calling program without waiting for the operation to complete.</caps:sentence>
                <caps:sentence sentenceid="998c7b2121b8f7ce4f03c674cbec411a" id="tgt26" class="tgtSentence"> Before the operation is complete, code execution continues.</caps:sentence>
                <caps:sentence sentenceid="4424b85c40fbfd4601d17a7816d0378c" id="tgt27" class="tgtSentence"> See also <newTerm>synchronous operation</newTerm>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="92eb5ffee6ae2fec3ad71c777531578f" id="tgt28" class="tgtSentence">B</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="b8e58d853ed462a1eb69ff13c2b0c753" id="tgt29" class="tgtSentence">binding entry</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="fb9651f96df8f85ba30490d81bdc54dc" id="tgt30" class="tgtSentence">A mapping between a field in a table and a variable.</caps:sentence>
                <caps:sentence sentenceid="3fdacda8593e1eb26cf17d68e8df1a3b" id="tgt31" class="tgtSentence"> In the ADO Visual C++ extensions, <legacyBold>Recordset</legacyBold> fields are mapped to C/C++ variables.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="fae7f4a8304955bc298fa8c210ce08ca" id="tgt32" class="tgtSentence">bitmask</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="dfe6405b7fd3fd7ded42b74c6da29da8" id="tgt33" class="tgtSentence">A numeric value intended for a bit-by-bit value comparison with other numeric values, typically to flag options in parameter or return values.</caps:sentence>
                <caps:sentence sentenceid="3de3851668f932208d03e657dfd9a744" id="tgt34" class="tgtSentence"> Usually this comparison is done with bitwise logical operators, such as <legacyBold>And</legacyBold> and <legacyBold>Or</legacyBold> in Visual Basic, <legacyBold>&amp;</legacyBold> and <legacyBold>|</legacyBold> in C++.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c39fb6d675b9cbfaab79ce6103da5d8b" id="tgt35" class="tgtSentence">For example, the ADO <legacyBold>FieldAttributeEnum</legacyBold> values can be used as bitmasks to determine the attributes of a field.</caps:sentence>
                <caps:sentence sentenceid="3d5446962cd7943809868202c5e9005e" id="tgt36" class="tgtSentence"> Suppose you wanted to determine if a field was updateable.</caps:sentence>
                <caps:sentence sentenceid="0ffc528d20cc3d5481b7fe1b29be62f2" id="tgt37" class="tgtSentence"> You could test for this with the following expression in Visual Basic:<codeInline>Field.Attributes AND adFldUpdatable</codeInline></caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b8c3cb0ca1099659687d3a2e79847c30" id="tgt38" class="tgtSentence">If the result is TRUE, then the field is updateable.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="fad9383ed4698856ed467fd49ecf4820" id="tgt39" class="tgtSentence">bookmark</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="1a9281476657835ee8b49cb651a59cc8" id="tgt40" class="tgtSentence">A marker that uniquely identifies a row within a set of rows so that a user can quickly navigate to it.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f7689f8ca9d9bf4fe9937fbf5af61b3b" id="tgt41" class="tgtSentence">business object</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="207c479355ba5dae2830f1a84c237a90" id="tgt42" class="tgtSentence">An object that performs a defined set of operations, such as data validation or business rule logic.</caps:sentence>
                <caps:sentence sentenceid="cabd60da6d744e8fc49627e1236e8632" id="tgt43" class="tgtSentence"> Business objects usually reside on the middle tier.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="7c46d3d220fbc8ba133402ef35e77187" id="tgt44" class="tgtSentence">business rule</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="9d4850b709ec283f17a30433f0f6ec4d" id="tgt45" class="tgtSentence">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business.</caps:sentence>
                <caps:sentence sentenceid="16840047a0d50639046069506d05fdae" id="tgt46" class="tgtSentence"> Also known as <legacyItalic>business logic</legacyItalic>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4a8a08f09d37b73795649038408b5f33" id="tgt47" class="tgtSentence">C</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="06b3ba65c954b020b9fc31fbb25d162b" id="tgt48" class="tgtSentence">calculated expression</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="deac8c24baf4705c9e5504a5520af6c6" id="tgt49" class="tgtSentence">An expression that is not constant, but whose value depends upon other values.</caps:sentence>
                <caps:sentence sentenceid="427f24c97053c8329dfbda5d417c3a0a" id="tgt50" class="tgtSentence"> To be evaluated, a calculated expression must obtain and compute values from other sources, typically in other fields or rows.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="7a3e56dbf4b75792017d682faf64ac07" id="tgt51" class="tgtSentence">chapter</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0961bc3aebd534f5923590be7cda3152" id="tgt52" class="tgtSentence">A reference to a range of rows from a data source.</caps:sentence>
                <caps:sentence sentenceid="566580a086830c46cf57431129b44266" id="tgt53" class="tgtSentence"> In ADO, a chapter is typically a reference to another <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="0c745e02e4b6f0b7cd541853adb1fa24" id="tgt54" class="tgtSentence">Chapter columns make it possible to define a <legacyItalic>parent-child</legacyItalic> relationship where the <legacyItalic>parent</legacyItalic> is the <legacyBold>Recordset</legacyBold> containing the chapter column and the <legacyItalic>child</legacyItalic> is the <legacyBold>Recordset</legacyBold> represented by the chapter.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="9c0b3d702ffd23877d161e0bf9c601fa" id="tgt55" class="tgtSentence">chapter-alias</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="29f1d7eddb8d4f6c8fb78ded48246fdd" id="tgt56" class="tgtSentence">An alias that refers to the column appended to the parent.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="219995487c9ed80ae3d0ada6a3ce757b" id="tgt57" class="tgtSentence">character set</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b42a614e9c3b8b79e8df2f008c6fbfb3" id="tgt58" class="tgtSentence">A mapping of a set of characters to their numeric values.</caps:sentence>
                <caps:sentence sentenceid="ce37753db2b64c431693e2af56245de0" id="tgt59" class="tgtSentence"> For example, Unicode is a 16-bit character set capable of encoding all known characters and used as a worldwide character-encoding standard.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="1b7d5726533ab525a8760351e9b5e415" id="tgt60" class="tgtSentence">child</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0842b46032cb458885b485cc04898300" id="tgt61" class="tgtSentence">The dependant side of a hierarchical relationship.</caps:sentence>
                <caps:sentence sentenceid="ea4a61a029716eafb9c6a8224b4a478d" id="tgt62" class="tgtSentence"> A child is a node in a hierarchical structure that has another node above it (closer to the root).</caps:sentence>
                <caps:sentence sentenceid="c2b6ac39669318bc535c8980b44df344" id="tgt63" class="tgtSentence"> See also <newTerm>child-alias</newTerm>, <newTerm>parent-child relationship</newTerm>, <newTerm>parent</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e1ee8ada69c51624264503bce817dd0e" id="tgt64" class="tgtSentence">child-alias</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="9f80f289bf29112483feccb8624beae5" id="tgt65" class="tgtSentence">An alias that refers to the child.</caps:sentence>
                <caps:sentence sentenceid="233027ebee97f398211f0b42028a3089" id="tgt66" class="tgtSentence"> See also <newTerm>alias</newTerm>, <newTerm>child</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="14527922cf4f98c3db29ede93c0681f9" id="tgt67" class="tgtSentence">CLSID (class identifier)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="90347bc276a114c0c884972991823e16" id="tgt68" class="tgtSentence">A universally unique identifier (UUID) that identifies a COM component.</caps:sentence>
                <caps:sentence sentenceid="68d629657fa40dc1a2356222ea6631a3" id="tgt69" class="tgtSentence"> Each COM component has its CLSID in the Windows Registry so that it can be loaded by other applications.</caps:sentence>
                <caps:sentence sentenceid="a4cce52bc69334b26018f453a55262a2" id="tgt70" class="tgtSentence"> See also <newTerm>ProgID</newTerm>, <newTerm>COM</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="37cba5cd22b2260b3330d0a3369ac49e" id="tgt71" class="tgtSentence">client tier</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="1be08586c2c2c09a1b11f97eb1d43081" id="tgt72" class="tgtSentence">A logical layer of a distributed system that typically presents data to and processes input from the user, sometimes referred to as the <legacyItalic>front end</legacyItalic>.</caps:sentence>
                <caps:sentence sentenceid="987910c2b976988a8e228293f1656f6d" id="tgt73" class="tgtSentence"> Usually, the client tier requests data from a server based on input, and then formats and displays the result.</caps:sentence>
                <caps:sentence sentenceid="5e714eca205d477df9b4259188e1ab16" id="tgt74" class="tgtSentence"> See also <newTerm>middle tier</newTerm>, <newTerm>data source tier</newTerm>, <newTerm>distributed application</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="68ccab33d1e13a749634ea111d233a00" id="tgt75" class="tgtSentence">COM (Component Object Model)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="758341573b6a43dfda8428b2a7fdbecc" id="tgt76" class="tgtSentence">A binary standard that enables objects to interoperate in a networked environment regardless of the language in which they were developed or on which computers they reside.</caps:sentence>
                <caps:sentence sentenceid="4dbfd382eb616444b627531d5ad62717" id="tgt77" class="tgtSentence"> COM-based technologies include ActiveX Controls, Automation, and object linking and embedding (OLE).</caps:sentence>
                <caps:sentence sentenceid="835fd01e9f5ba60344dbc23546dc68ab" id="tgt78" class="tgtSentence"> COM allows an object to expose its functionality to other components and to host applications.</caps:sentence>
                <caps:sentence sentenceid="bd1fc3a8058980bfbc5f8d7ba11b4ac1" id="tgt79" class="tgtSentence"> It defines both how the object exposes itself and how this exposure works across processes and across networks.</caps:sentence>
                <caps:sentence sentenceid="b9e762295d5a0a3a95a0d2a83b65052f" id="tgt80" class="tgtSentence"> COM also defines the object's life cycle.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f2fa0ffbd5296fb4e8877973761855cf" id="tgt81" class="tgtSentence">COM component</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="52609aa888bfebae9fbc14b9b79aa4c7" id="tgt82" class="tgtSentence">Binary file — such as .dll, .ocx, and some .exe files — that supports the COM standard for providing objects.</caps:sentence>
                <caps:sentence sentenceid="ab52542ebd518c4fe6256b9abd513725" id="tgt83" class="tgtSentence"> Such a file contains code for one or more class factories, COM classes, registry-entry mechanisms, loading code, and so on.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="ef171a8b835c91cc543dd8bd659bb2d4" id="tgt84" class="tgtSentence">comparison operator</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="4b97f4cb5827a6dc5da27ebee3a9d386" id="tgt85" class="tgtSentence">An operator that compares two expressions and returns a Boolean value.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6589c395d63092efaf000da406e37721" id="tgt86" class="tgtSentence">A criteria parameter that may be expressed as "&gt;" (greater than), "&lt;" (less than), "=" (equal), "&gt;=" (greater than or equal), "&lt;=" (less than or equal), "&lt;&gt;" (not equal), or "like" (pattern matching).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="700c216fb376666eaeda0c892e8bdc09" id="tgt87" class="tgtSentence">component</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="812a75dad48a63f87342c88c45b04f9c" id="tgt88" class="tgtSentence">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="732627d078ea8cf769350d54eed6ad51" id="tgt89" class="tgtSentence">compound file</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="62602fce137b0a4b9637ab490389aade" id="tgt90" class="tgtSentence">An implementation of COM structured storage for files.</caps:sentence>
                <caps:sentence sentenceid="a3bde31f32720d11251adc71772f2197" id="tgt91" class="tgtSentence"> A compound file stores separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</caps:sentence>
                <caps:sentence sentenceid="b2085ca99e642fe1c0b47ddfc870504a" id="tgt92" class="tgtSentence"> Together, they function like a file system within a file.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e4dae8c4f9b0e63648348a6f49c29492" id="tgt93" class="tgtSentence">A number of individual files bound together in one physical file.</caps:sentence>
                <caps:sentence sentenceid="a05009e586f5d750a30dd548d3a868ed" id="tgt94" class="tgtSentence"> Each individual file in a compound file can be accessed as if it were a single physical file.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt95" class="tgtSentence">constant</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="bf97d92d59094e4702639ebd5855f589" id="tgt96" class="tgtSentence">A numeric or string value that does not change.</caps:sentence>
                <caps:sentence sentenceid="994071180078e1693f68706ec44db68d" id="tgt97" class="tgtSentence"> Named ADO enumerations (enumerated constants) can be used in your code instead of actual values, for example, <legacyBold>adUseClient</legacyBold> is a constant whose value is 3.</caps:sentence>
                <caps:sentence sentenceid="c1f370d13c17e9ed8704f7aa0b317af4" id="tgt98" class="tgtSentence"> (Const adUseClient = 3).</caps:sentence>
                <caps:sentence sentenceid="371a84655d3c0a0a2a5883fd47d59ba5" id="tgt99" class="tgtSentence"> See also <newTerm>enumeration</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="1791a97a8403730ee0760489a2aeb992" id="tgt100" class="tgtSentence">cursor</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="89109a7d584399415f0e3481602b4f13" id="tgt101" class="tgtSentence">A database element that controls record navigation, updateability of data, and the visibility of changes made to the database by other users.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="8277e0910d750195b448797616e091ad" id="tgt102" class="tgtSentence">D</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="31bcf24e1e7f6114a976a4a369514332" id="tgt103" class="tgtSentence">data binding</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ecddf49a0cd961d9f6a56bf2feb0556b" id="tgt104" class="tgtSentence">The process of associating the objects or controls of an application to a data source.</caps:sentence>
                <caps:sentence sentenceid="cba72f07ebb46be6d5f8e4cb17e1d4f1" id="tgt105" class="tgtSentence"> A control associated with a data source is called a <legacyItalic>data-bound control</legacyItalic>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="019521e747ac404ac0aa3fdd6422587e" id="tgt106" class="tgtSentence">The contents of a data-bound control are associated with values from a database.</caps:sentence>
                <caps:sentence sentenceid="3ac1c5dee24301848a0f356b995aa23e" id="tgt107" class="tgtSentence"> For example, a grid control that is bound to a <legacyBold>Recordset</legacyBold> object can be updated when the rows in the <legacyBold>Recordset</legacyBold> are updated.</caps:sentence>
                <caps:sentence sentenceid="ab351087fba04f8d39e5bbf28f464e36" id="tgt108" class="tgtSentence"> When new values are retrieved by the <legacyBold>Recordset</legacyBold>, new values are displayed in the grid.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="4554a68f24dcbb0859b10f28517ef45f" id="tgt109" class="tgtSentence">data provider</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="3cb7906f553e19ea32d7829b2976580e" id="tgt110" class="tgtSentence">Software that exposes data to an ADO application either directly or via a service provider.</caps:sentence>
                <caps:sentence sentenceid="3cf64379e266967c9b642bdaca9d4403" id="tgt111" class="tgtSentence"> See also service provider.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="585957d02507abe8ad4d8901c1b6a7e0" id="tgt112" class="tgtSentence">data shaping</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e3cca64ca62c8c4af26a49854ff51eee" id="tgt113" class="tgtSentence">A technique which makes use of a formalized syntax (called <legacyBold>Shape language</legacyBold>) to define a specialized <legacyBold>Recordset</legacyBold> object (called a <newTerm>shaped Recordset</newTerm>) that contains not just data, but also references to other <legacyBold>Recordset</legacyBold> objects and/or computed values based on those other <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="7106b70861b6a0ecee8e6b03d03f2cae" id="tgt114" class="tgtSentence">data source tier</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="082447dcd315690d75aa8a7ddcbfbed2" id="tgt115" class="tgtSentence">A logical layer of a distributed system that represents a computer running a DBMS, such as an SQL Server database.</caps:sentence>
                <caps:sentence sentenceid="71ec8e5e2cb85a414aafdc2581ec7576" id="tgt116" class="tgtSentence"> See also <newTerm>client tier</newTerm>, <newTerm>middle tier</newTerm>, <newTerm>distributed application</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c14f7a73c9cca3dec4ca6c9c3e722f2b" id="tgt117" class="tgtSentence">DCOM</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0b44f246a495bae7cd0c53ead5abb2b8" id="tgt118" class="tgtSentence">A wire protocol that enables COM components to communicate directly with each other across a network.</caps:sentence>
                <caps:sentence sentenceid="d4a716c7dba14f4dc556e2481fc6cc26" id="tgt119" class="tgtSentence"> See also <newTerm>COM</newTerm>, <newTerm>component</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f3f5522a1ffb2f3ce9c248bad66c1755" id="tgt120" class="tgtSentence">DDL (Data Definition Language)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ae60a65b64e908fa81288c9c189dbea3" id="tgt121" class="tgtSentence">Those statements in SQL that define, as opposed to manipulate, data.</caps:sentence>
                <caps:sentence sentenceid="5f3dcd258e8b2ce815bfd0b19b1dfa05" id="tgt122" class="tgtSentence"> The schema of a database is created or modified with DDL.</caps:sentence>
                <caps:sentence sentenceid="ef8a9cea53559e3f0c25723dec727e99" id="tgt123" class="tgtSentence"> For example, <legacyBold>CREATE TABLE</legacyBold>, <legacyBold>CREATE INDEX</legacyBold>, <legacyBold>GRANT</legacyBold>, and <legacyBold>REVOKE</legacyBold> are SQL DDL statements.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d8a961df58f718cab1074b46d07cd880" id="tgt124" class="tgtSentence">default stream</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ba0ae8aa334dfed5ccee38940b9167b3" id="tgt125" class="tgtSentence">A text or binary stream (represented by a <legacyBold>Stream</legacyBold> object) that is associated with <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> objects when using certain OLE DB providers, such as the Microsoft OLE DB Provider for Internet Publishing.</caps:sentence>
                <caps:sentence sentenceid="e70ea33a7bc6b98c62699e6ec0831489" id="tgt126" class="tgtSentence"> The default stream typically contains the contents of a file such as the HTML code for the root of a Web site.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="77cc1ce836cedc14028c00678fb3ec21" id="tgt127" class="tgtSentence">distributed application</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e1d491fab8396e86c87b2b4844039d4f" id="tgt128" class="tgtSentence">A program written so that the processing can be divided across multiple computers over a network.</caps:sentence>
                <caps:sentence sentenceid="2c9f536b40e8efc4ca62054210a4ea7b" id="tgt129" class="tgtSentence"> Typically, a distributed application is divided into presentation, business logic, and data store layers, or <legacyItalic>tiers</legacyItalic>.</caps:sentence>
                <caps:sentence sentenceid="b9916024a4a6e33d42d8c4d57076e07e" id="tgt130" class="tgtSentence"> See also client tier, middle tier, data source tier.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a12203cbe784119d3e8d52ad7a2aebe2" id="tgt131" class="tgtSentence">disconnected Recordset</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="86a5ca2b0abdafc6bedd788a756011bb" id="tgt132" class="tgtSentence">A <legacyBold>Recordset</legacyBold> object in a client cache that no longer has a live connection to the server.</caps:sentence>
                <caps:sentence sentenceid="2597f7bb733797a7c1d2caa4a87750fc" id="tgt133" class="tgtSentence"> If the original data source needs to be accessed again for some reason, such as updating data, the connection must be re-established.</caps:sentence>
                <caps:sentence sentenceid="92c2c429d872e7c88b1e0f8beead64fc" id="tgt134" class="tgtSentence"> However, the collections, properties, and methods of a disconnected <legacyBold>Recordset</legacyBold> can still be accessed.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="83ca45919b91bcbbc0319e635a2c4afd" id="tgt135" class="tgtSentence">DML (Data Manipulation Language)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="919e4f185a39c4d0a02205a978b988c9" id="tgt136" class="tgtSentence">Those statements in SQL that manipulate, as opposed to define, data.</caps:sentence>
                <caps:sentence sentenceid="2b6eb54f24154c8128243bce4593d365" id="tgt137" class="tgtSentence"> The values in a database are selected and modified with DML.</caps:sentence>
                <caps:sentence sentenceid="a4b84614c149f01f73b518d9487e0608" id="tgt138" class="tgtSentence"> For example, <legacyBold>INSERT</legacyBold>, <legacyBold>UPDATE</legacyBold>, <legacyBold>DELETE</legacyBold>, and <legacyBold>SELECT</legacyBold> are SQL DML statements.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="4d7e6743965dee50756c2957738131e2" id="tgt139" class="tgtSentence">document source provider</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="676c10fd84ae9cc6db026f159c51fcb2" id="tgt140" class="tgtSentence">A special class of providers that manage folders and documents.</caps:sentence>
                <caps:sentence sentenceid="4749976eb1ba1b02c5d0722676ddee7e" id="tgt141" class="tgtSentence"> When a document is represented by a <legacyBold>Record</legacyBold> object, or a folder of documents is represented by a <legacyBold>Recordset</legacyBold> object, the document source provider populates those objects with a unique set of fields that describe characteristics of the document, instead of the actual document itself.</caps:sentence>
                <caps:sentence sentenceid="1078082a94e3dcb6fb9457c445651a6b" id="tgt142" class="tgtSentence"> See also resource record.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="71fee238d563fd20cb66ec7cc97c9bc4" id="tgt143" class="tgtSentence">DSN (data source name)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="1b7b4247cb78e4fb1cc26583bc983020" id="tgt144" class="tgtSentence">The collection of information used to connect your application to a particular ODBC database.</caps:sentence>
                <caps:sentence sentenceid="ca055cd1d996b9272c81dfb46f8a74d0" id="tgt145" class="tgtSentence"> The ODBC Driver Manager uses this information to create a connection to the database.</caps:sentence>
                <caps:sentence sentenceid="674b706295abe97cd14533c4fbb4eb30" id="tgt146" class="tgtSentence"> A DSN can be stored in a file (a file DSN) or in the Windows Registry (a machine DSN).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="ec6fab0578030164762ad59510e927ca" id="tgt147" class="tgtSentence">dynamic property</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b287e8285c57e1a3c23ef02aaf8a0f11" id="tgt148" class="tgtSentence">A property specific to a data provider or the cursor service.</caps:sentence>
                <caps:sentence sentenceid="86eede812149244410c8d81feaffae5f" id="tgt149" class="tgtSentence"> The <legacyBold>Properties</legacyBold> collection of an object is populated with these automatically ("dynamically").</caps:sentence>
                <caps:sentence sentenceid="56b35ec6d6af19364c3c28e4360f059f" id="tgt150" class="tgtSentence"> An object has no dynamic properties until it is connected to a data source through a particular data provider.</caps:sentence>
                <caps:sentence sentenceid="dc9c77b935db9bb84b2d2023208f07dd" id="tgt151" class="tgtSentence"> See also data provider, cursor.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="e1671797c52e15f763380b45e841ec32" id="tgt152" class="tgtSentence">E</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="3f49fe61d5812612c53377049e3c86d6" id="tgt153" class="tgtSentence">Enumeration</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="636a19bda42a0d60b031099abc0b99fb" id="tgt154" class="tgtSentence">A list of named constants.</caps:sentence>
                <caps:sentence sentenceid="7064fbcf10bed34d35f987812103d8a6" id="tgt155" class="tgtSentence"> Enumerated values need not be unique.</caps:sentence>
                <caps:sentence sentenceid="6a4a5c409e2f45755af2ff410212af79" id="tgt156" class="tgtSentence"> However the name of each value must be unique within the scope where the enumeration is defined.</caps:sentence>
                <caps:sentence sentenceid="6eecbf38653ceda33c720fe878e032e2" id="tgt157" class="tgtSentence"> In ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version).</caps:sentence>
                <caps:sentence sentenceid="0686de8834647139edeca4bff11728d0" id="tgt158" class="tgtSentence"> For example, to open a static <legacyBold>Recordset</legacyBold>, use the <legacyBold>adOpenStatic</legacyBold> enumerated value: <codeInline>Recordset.Open ,,adOpenStatic</codeInline></caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c6571fc5aad14805f3a80f8c64c93116" id="tgt159" class="tgtSentence"> Also referred to as <legacyItalic>enumerated constant</legacyItalic>.</caps:sentence>
                <caps:sentence sentenceid="7bf1a826a55ad86b734132700528c18d" id="tgt160" class="tgtSentence"> See also <newTerm>constant</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="4119639092e62c55ea8be348e4d9260d" id="tgt161" class="tgtSentence">event</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="059b4f96c33cfe1efea9ca5863f0d273" id="tgt162" class="tgtSentence">An action recognized by an object, for which you can write code to respond.</caps:sentence>
                <caps:sentence sentenceid="ad8e0bfd8e71ea39369d435af181860a" id="tgt163" class="tgtSentence"> Events can be generated by command execution, transaction completion, recordset navigation, and data updates, among other actions.</caps:sentence>
                <caps:sentence sentenceid="6cc719857f767a479d3bcfc3c9c28d33" id="tgt164" class="tgtSentence"> See also <newTerm>event handler</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="dfd1c97c3864ec9043d376a0c01353e4" id="tgt165" class="tgtSentence">event handler</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="14588dfca0f1f9ce343398ffa9f706e9" id="tgt166" class="tgtSentence">An event handler is the code that is executed when an event occurs.</caps:sentence>
                <caps:sentence sentenceid="53e6eff871e2183fb0e9fc39b0b8e4e5" id="tgt167" class="tgtSentence"> See also event.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2510c39011c5be704182423e3a695e91" id="tgt168" class="tgtSentence">H</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="c1cbfe271a40788a00e8bf8574d94d4b" id="tgt169" class="tgtSentence">handler</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7d0a5270d9871e2cde6c3002f5fcee1c" id="tgt170" class="tgtSentence">A routine that manages a common and relatively simple condition or operation, such as error recovery or data management.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="41f357023c911cd533417167fd4237e9" id="tgt171" class="tgtSentence">hierarchical Recordset</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f21bafc0707a147f6f766e38ee25e9c9" id="tgt172" class="tgtSentence">A <legacyBold>Recordset</legacyBold> that contains another <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="0637acd384b3e955e38105f5b25d1b1d" id="tgt173" class="tgtSentence"> See also data shaping, chapter.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="abe3cafe49cbc48d3fc7407eb0d12f0e" id="tgt174" class="tgtSentence">For more information, see <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="b81ca7c0ccaa77e7aa91936ab0070695" id="tgt175" class="tgtSentence">hierarchy</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="8258a5b09133cc166079cf4593d1c12a" id="tgt176" class="tgtSentence">In general, a hierarchy is a ranked structure with a top level and subordinate levels.</caps:sentence>
                <caps:sentence sentenceid="b70f32104c189b4a1af004d7a77f6f10" id="tgt177" class="tgtSentence"> In ADO, hierarchical <legacyBold>Recordsets</legacyBold> are used to represent the parent-child relationship between a record and a chapter.</caps:sentence>
                <caps:sentence sentenceid="fb69b36f560ccce925f70a9d8dccee1a" id="tgt178" class="tgtSentence"> Also in ADO, <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects can be used to access hierarchical tree structures such as a folder and documents.</caps:sentence>
                <caps:sentence sentenceid="bb19aded4bf73e8b6cfd197b55eeec0f" id="tgt179" class="tgtSentence"> ADO MD also includes <legacyBold>Hierarchy</legacyBold> objects to represent a relationship between the levels of a dimension in an OLAP cube.</caps:sentence>
                <caps:sentence sentenceid="fb4831a735bbd33459a866e323c7adda" id="tgt180" class="tgtSentence"> See also hierarchical Recordsets, parent-child relationship, chapter, tree.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="55a096a7b4617f0e5cfefbc3eacd84ba" id="tgt181" class="tgtSentence">I-L</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="7aaeb5458a94719e3336b471dfd2b023" id="tgt182" class="tgtSentence">ISAPI (Internet Server Application Programming Interface)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="2aa6223780ab9f5d29da92de09015a31" id="tgt183" class="tgtSentence">A set of functions for Internet servers, such as a Windows NT® Server/Windows 2000 Server running Microsoft® Internet Information Services (IIS).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="3c6e0b8a9c15224a8228b9a98ca1531d" id="tgt184" class="tgtSentence">Key</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="4ad7cfccc8975583abdacd662ceeb90f" id="tgt185" class="tgtSentence">A column or columns in a table that uniquely identify a row; often used to index a table.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="6f8f57715090da2632453988d9a1501b" id="tgt186" class="tgtSentence">M</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="28f604e91eed18929dd4d9227e58e61c" id="tgt187" class="tgtSentence">marshaling</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="9580309fd97e774225d84fe4b6c2fc12" id="tgt188" class="tgtSentence">The process of packaging, sending, and unpackaging interface method parameters across thread or process boundaries.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="06dcdc0c99fca33a7164684f29704aa6" id="tgt189" class="tgtSentence">middle tier</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="4962e48de3af7ed7353f28731702eec9" id="tgt190" class="tgtSentence">The logical layer in a distributed system between a user interface or Web client and the database.</caps:sentence>
                <caps:sentence sentenceid="eeca369a6f936a8b6096506b18bec311" id="tgt191" class="tgtSentence"> This is typically where business objects are instantiated.</caps:sentence>
                <caps:sentence sentenceid="b09bbfe397623216cf79698bc2eb7066" id="tgt192" class="tgtSentence"> The middle tier is a collection of business rules and functions that generate and operate upon receiving information.</caps:sentence>
                <caps:sentence sentenceid="e562db9940ca04da24b2df2067f81ba8" id="tgt193" class="tgtSentence"> They accomplish this through business rules, which can change frequently, and are thus encapsulated into components that are physically separate from the application logic itself.</caps:sentence>
                <caps:sentence sentenceid="f57cef3388867f5e265ab2a1cbc570f0" id="tgt194" class="tgtSentence"> Also known as <legacyItalic>application server tier</legacyItalic>.</caps:sentence>
                <caps:sentence sentenceid="206957fb6bb12ee8b65313c5961ce15f" id="tgt195" class="tgtSentence"> See also distributed application, client tier, data source tier.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="c23a425e62b6c414e4ac87657f22f5b6" id="tgt196" class="tgtSentence">MIME (Multi-purpose Internet Mail Extension)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e5eb99f4908cadba1e4ca97a670dbb95" id="tgt197" class="tgtSentence">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, machine, and e-mail environments.</caps:sentence>
                <caps:sentence sentenceid="c9fd73eb629507a612fcb76557589242" id="tgt198" class="tgtSentence"> In practice, MIME has also been adopted and extended by non-mail applications.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="34d49a49cb8b1ac2b93f8e9f7b185fc8" id="tgt199" class="tgtSentence">MIME is a standard that allows binary data to be published and read on the Internet.</caps:sentence>
                <caps:sentence sentenceid="c8de5b8495aac3a8dc45ee073bb7891a" id="tgt200" class="tgtSentence"> The header of a file with binary data contains the MIME type of the data; this informs client programs (Web browsers and mail packages, for instance) that they will need to handle the data in a different way than they handle straight text.</caps:sentence>
                <caps:sentence sentenceid="f373dc6f608a5fbc98b4ee5d3a267f31" id="tgt201" class="tgtSentence"> For example, the header of a Web document containing a JPEG graphic contains the MIME type specific to the JPEG file format.</caps:sentence>
                <caps:sentence sentenceid="64dc380055917d31fb3c87107107d2b1" id="tgt202" class="tgtSentence"> This allows a browser to display the file with its JPEG viewer, if one is present.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a7d84ce81af140c9cded0d847cafe7d6" id="tgt203" class="tgtSentence">N-O</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="36c4536996ca5615dcf9911f068786dc" id="tgt204" class="tgtSentence">node</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="076666aee9386a584126ab3473b26d1a" id="tgt205" class="tgtSentence">An element in a hierarchical tree structure.</caps:sentence>
                <caps:sentence sentenceid="8636544ad615dc1f4da76baec2ff2387" id="tgt206" class="tgtSentence"> A node may be the root, or the child of another node.</caps:sentence>
                <caps:sentence sentenceid="93071756321412b312097697872bc8ad" id="tgt207" class="tgtSentence"> A node can also be the parent of multiple children.</caps:sentence>
                <caps:sentence sentenceid="f165e2cc857df167ee6343a65482d6dc" id="tgt208" class="tgtSentence"> See also hierarchy, tree, root, child, parent.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="64162d49c9e45af100d4f35ccf36aac5" id="tgt209" class="tgtSentence">object variable</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e0d73a8917d3a44ce926f9fd4a03768a" id="tgt210" class="tgtSentence">A variable that contains a reference to an object.</caps:sentence>
                <caps:sentence sentenceid="2c13fa9ecc7de43b860c882610f9d529" id="tgt211" class="tgtSentence"> For example, <codeInline>objCustomObject</codeInline> is a variable that points to an object of type CustomObject:<codeInline>Set objCustomObject = CreateObject(adodb.Recordset)</codeInline></caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="ea3162428764a75aca45448f412ca348" id="tgt212" class="tgtSentence">ODBC (Open Database Connectivity)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d5810681f12c767dfd17fdc6dbb3bf3a" id="tgt213" class="tgtSentence">A standard programming language interface used to connect to a variety of data sources.</caps:sentence>
                <caps:sentence sentenceid="1722f5207371fe72fd4bb903e9e7920a" id="tgt214" class="tgtSentence"> This is usually accessed through Control Panel, where data source names (DSNs) can be assigned to use specific ODBC drivers.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="6ad3df1954ecac62a4346a8b0f376662" id="tgt215" class="tgtSentence">OLE DB</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a9ef82d02ba6fa1a0c1459b886596664" id="tgt216" class="tgtSentence">A set of interfaces that expose data from a variety of sources using COM.</caps:sentence>
                <caps:sentence sentenceid="30ac29da0591edfc14c6b21ff8490be8" id="tgt217" class="tgtSentence"> OLE DB interfaces provide applications with uniform access to data stored in diverse information sources.</caps:sentence>
                <caps:sentence sentenceid="9a032bfb7c5b8f49c5c404f554b0a3d6" id="tgt218" class="tgtSentence"> These interfaces support the amount of DBMS functionality appropriate to the data source, enabling it to share its data.</caps:sentence>
                <caps:sentence sentenceid="011758f385a4281bedc5e5f899351d53" id="tgt219" class="tgtSentence"> See also COM.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="111eb06991d1b87b6d25fc1fe1b5a6e0" id="tgt220" class="tgtSentence">optimistic locking</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="aa75c453e0ef7c4ed218509420029397" id="tgt221" class="tgtSentence">A type of locking in which the data page containing one or more records, including the record being edited, is unavailable to other users only while the record is being updated by the <legacyBold>Update</legacyBold> method, but is available before and after the call to <legacyBold>Update</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2b56460a8491afb2021f747817a6fb1b" id="tgt222" class="tgtSentence"> Optimistic locking is used when the <legacyBold>Recordset</legacyBold> object is opened with the <legacyBold>LockType</legacyBold> parameter or property set to <legacyBold>adLockOptimistic</legacyBold> or <legacyBold>adLockBatchOptimistic</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="20f63403d713d22a3d47a706d59ecfe4" id="tgt223" class="tgtSentence"> See also pessimistic locking.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="8096d10a660ceec341d94365ce44c8b5" id="tgt224" class="tgtSentence">ordinal value</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="12a708d1b53fc24a2c5c4e1b0be68fc8" id="tgt225" class="tgtSentence">The numeric location of an item within an order.</caps:sentence>
                <caps:sentence sentenceid="a1ab6a876e3e2e8b49ccd6c0db2dfa4c" id="tgt226" class="tgtSentence"> In an ADO collection, the ordinal value of the first item is zero (0).</caps:sentence>
                <caps:sentence sentenceid="eef378e4c56e4c902ca6170cbad98a41" id="tgt227" class="tgtSentence"> The next item is one (1), and so on.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="83878c91171338902e0fe0fb97a8c47a" id="tgt228" class="tgtSentence">P</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="bf99663a8e6a4d238bff755b6b8ecd14" id="tgt229" class="tgtSentence">parameterized command</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="2d9f739426f9a58fbf6e5bf74f303103" id="tgt230" class="tgtSentence">A query or command that allows you to set parameter values before the command is executed.</caps:sentence>
                <caps:sentence sentenceid="d88edf32e93943b6102fbff60ceddbfe" id="tgt231" class="tgtSentence"> For example, a SQL string can be parameterized by embedding parameter markers in the SQL string (designated by the '?' character).</caps:sentence>
                <caps:sentence sentenceid="6f71e7b4cdcf05bfb7a1ac967939f3a8" id="tgt232" class="tgtSentence"> The application then specifies values for each parameter and executes the command.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="d0e45878043844ffc41aac437e86b602" id="tgt233" class="tgtSentence">parent</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="14bc7c75c71882cd9e5b562105d22487" id="tgt234" class="tgtSentence">The controlling side of a hierarchical relationship.</caps:sentence>
                <caps:sentence sentenceid="7e3471189022660d424a61c932772167" id="tgt235" class="tgtSentence"> In a hierarchical structure, a parent has one or more child nodes directly beneath it in the hierarchy.</caps:sentence>
                <caps:sentence sentenceid="461d84ffb72fc8574e65804578ea6bc3" id="tgt236" class="tgtSentence"> See also parent-alias, parent-child relationship, child.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e46b0364d62763ad154a6fffdefc9c90" id="tgt237" class="tgtSentence">parent-alias</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="90cd3fb0d24cc4d10f09e774aed9430a" id="tgt238" class="tgtSentence">An alias that refers to the parent.</caps:sentence>
                <caps:sentence sentenceid="42acd115336fc8f4b4906901d98f312c" id="tgt239" class="tgtSentence"> See also alias, parent.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e11f6d511fe4009cd740881006fe4048" id="tgt240" class="tgtSentence">parent-child relationship</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="6e44463c9254a781f4db30686b991bfb" id="tgt241" class="tgtSentence">A relationship in a hierarchical structure in which the parent is one level higher and directly associated with one or more children.</caps:sentence>
                <caps:sentence sentenceid="33c7ce6a7df19886bcda94987ecd1c51" id="tgt242" class="tgtSentence"> A child is one level lower and must have one parent.</caps:sentence>
                <caps:sentence sentenceid="4238d5b566c6ae98deba85d643dbcecd" id="tgt243" class="tgtSentence"> See also parent, child.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e0473e46202f7c9c7c35668afa1011c9" id="tgt244" class="tgtSentence">pessimistic locking</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="b04d8b9e63f40f9b19ede34516780d2f" id="tgt245" class="tgtSentence">A type of locking in which the page containing one or more records, including the record being edited, is unavailable to other users to ensure that an update will be made.</caps:sentence>
                <caps:sentence sentenceid="d763cfb8c205857ccb901dd52bb6e2de" id="tgt246" class="tgtSentence"> Pessimistic locking behavior is defined by the OLE DB provider.</caps:sentence>
                <caps:sentence sentenceid="956a69fc2432a5f117cf796e922ea9d6" id="tgt247" class="tgtSentence"> Typically, records are locked upon editing and remain unavailable until the <legacyBold>Update</legacyBold> method has completed.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="69631e360fbe3d7ebdb6dc17ed6e5070" id="tgt248" class="tgtSentence"> Pessimistic locking is enabled when the <legacyBold>Recordset</legacyBold> object is opened with the <legacyBold>LockType</legacyBold> parameter or property set to <legacyBold>adLockPessimistic</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="33310bd436d3cb0731557a29cf93a400" id="tgt249" class="tgtSentence"> See also optimistic locking.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="4abcef116566139e94c82bb1bb37583f" id="tgt250" class="tgtSentence">pooling</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="7ec48789c8440f5f0ada136cda93e435" id="tgt251" class="tgtSentence">A performance optimization based on using collections of pre-allocated resources, such as objects or database connections.</caps:sentence>
                <caps:sentence sentenceid="646c053551c0b2f2625cfc850d09e4c4" id="tgt252" class="tgtSentence"> It is more efficient to draw an existing resource from the pool than to create a new resource.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="2578eeb89e09e62d7c1f13c5d73c43e4" id="tgt253" class="tgtSentence">ProgID (programmatic identifier)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="31a0684ef46119ecd36b4d76c2b596fb" id="tgt254" class="tgtSentence">A unique name mapped to the Windows registry by a COM application.</caps:sentence>
                <caps:sentence sentenceid="20cc5a0a5bebbac8747648a96e482a94" id="tgt255" class="tgtSentence"> The ProgID for an ADO Connection is "ADODB.Connection".</caps:sentence>
                <caps:sentence sentenceid="b3d1ce08f01c298af7c2e19a79471164" id="tgt256" class="tgtSentence"> See also CLSID, COM.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="431387eb7262e1cfc79b125eb8a67c60" id="tgt257" class="tgtSentence">proxy</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="cda88681e8d6d281e9b2b6143661c8b1" id="tgt258" class="tgtSentence">An interface-specific object that provides the parameter marshaling and communication required for a client to call an application object that is running in a different execution environment, such as on a different thread or in another process.</caps:sentence>
                <caps:sentence sentenceid="e5e40fcbde92e0e59ce863b9a5d45816" id="tgt259" class="tgtSentence"> The proxy is located with the client and communicates with a corresponding stub that is located with the application object that is being called.</caps:sentence>
                <caps:sentence sentenceid="46220cad507fc503766183039f050209" id="tgt260" class="tgtSentence"> See also stub.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4b43b0aee35624cd95b910189b3dc231" id="tgt261" class="tgtSentence">R</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="432d95a9cf4068e376d2daaeb7f449ef" id="tgt262" class="tgtSentence">relative URL</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f4087a2da659babd46e082b66a289a85" id="tgt263" class="tgtSentence">A partially qualified URL that specifies a resource on the Internet or an intranet whose location is relative to a starting point specified by an absolute URL or equivalent ADO Connection object.</caps:sentence>
                <caps:sentence sentenceid="c3062522e24da446679f38c2e8ca75e2" id="tgt264" class="tgtSentence"> In effect, the concatenated absolute and relative URLs consitute a complete URL.</caps:sentence>
                <caps:sentence sentenceid="ad3fd58f91d9c3dc25d4c7b740dcd40c" id="tgt265" class="tgtSentence"> See also URL and absolute URL.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="fce642c8f1ba36f03cde6becce7215bc" id="tgt266" class="tgtSentence">remote data source</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e80ebdb87719d9e312594e9b63a5efca" id="tgt267" class="tgtSentence">A data source that exists on a another computer, rather than on the local system (where the client application runs).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="5315713b7dd74a2ffcec334dfd9eb82c" id="tgt268" class="tgtSentence">resource record</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="1dfa4f33c5a62541a41dec7a25c06ccc" id="tgt269" class="tgtSentence">A record from a document source provider that contains fields for the definition and description of a folder or document.</caps:sentence>
                <caps:sentence sentenceid="0147b6772d9ee6321b0c382137e057a8" id="tgt270" class="tgtSentence"> The document itself is not contained in the resource record but typically can be accessed by the default stream or a field in the resource record containing a URL.</caps:sentence>
                <caps:sentence sentenceid="865b9b7f704884e25ec5547c9c41f794" id="tgt271" class="tgtSentence"> See also document source provider, default stream, URL.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="2131f033d6f9e7addb358973b976cdd7" id="tgt272" class="tgtSentence">rowset</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d714a777001f06493c987f0a775a964e" id="tgt273" class="tgtSentence">A set of rows from a data source, all having the same field schema.</caps:sentence>
                <caps:sentence sentenceid="8cb08ab959048f20cf18437bc9910cdc" id="tgt274" class="tgtSentence"> A rowset can represent all or some fields from a table.</caps:sentence>
                <caps:sentence sentenceid="e02fe82a1c06f4d011ce83ddfc51cb15" id="tgt275" class="tgtSentence"> A rowset can also represent a virtual table, created by a query or a join of two or more tables.</caps:sentence>
                <caps:sentence sentenceid="0a5d0a40505759c4dcd452840ced3738" id="tgt276" class="tgtSentence"> In ADO, rowsets are represented by <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="03c7c0ace395d80182db07ae2c30f034" id="tgt277" class="tgtSentence">S</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="31a1fd140be4bef2d11e121ec9a18a58" id="tgt278" class="tgtSentence">Scope</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a0ad805ef96200af64509b3d4c730eb0" id="tgt279" class="tgtSentence">The range of reference for an object or variable or a range of records in a view or table.</caps:sentence>
                <caps:sentence sentenceid="5fe1369b3250a01323ab820d3fa7181b" id="tgt280" class="tgtSentence"> For example, local variables can be referenced only within the procedure in which they were defined.</caps:sentence>
                <caps:sentence sentenceid="d13f641c1fb9831e86e1b5c63d50d861" id="tgt281" class="tgtSentence"> Public variables are accessible from anywhere in the application.</caps:sentence>
                <caps:sentence sentenceid="760fb14617f91603268fa79f352f2628" id="tgt282" class="tgtSentence"> Objects, such as the current database, are in scope if they are in the defined search path.</caps:sentence>
                <caps:sentence sentenceid="94144196ea87132048876d168b5f4ec4" id="tgt283" class="tgtSentence"> Record ranges can be specified with a Scope clause in many commands.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f7cc0a3d2d95cdec9b1907b55a59939e" id="tgt284" class="tgtSentence">service provider</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="8ce6da92d2ed6a29b92135b343c2c375" id="tgt285" class="tgtSentence">Software that encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</caps:sentence>
                <caps:sentence sentenceid="6e1622fff7ba0fdfd1a1146de2513f3c" id="tgt286" class="tgtSentence"> It is a provider that does not directly expose data, rather it provides a service, such as query processing.</caps:sentence>
                <caps:sentence sentenceid="4e9bc2fd65d9b2614451634ed5b14834" id="tgt287" class="tgtSentence"> The service provider may process data provided by a data provider.</caps:sentence>
                <caps:sentence sentenceid="d770c4e3f8c765989b1cc7f04ed7ca80" id="tgt288" class="tgtSentence"> See also data provider.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="871052bcdd006465e05f36b6783d0db3" id="tgt289" class="tgtSentence">shaped Recordset</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ff9083418441604eaf4b61b22d7faa95" id="tgt290" class="tgtSentence">A <legacyBold>Recordset</legacyBold> whose columns have been specifically defined to contain not just data, but also references (called chapters) to other <legacyBold>Recordset</legacyBold> objects and/or computed values based on other <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="190dca50d2a46b53a1960d0f993c7e4a" id="tgt291" class="tgtSentence">sibling</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="61b4d13a3d32b427b3785337a74818e7" id="tgt292" class="tgtSentence">Any two or more nodes in a hierarchical structure that are on the same level in the hierarchy.</caps:sentence>
                <caps:sentence sentenceid="81c1ed667ef2bd21df23992fb1845744" id="tgt293" class="tgtSentence"> The root node in a hierarchy has no siblings.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="44235f0a062b5f144020608490dda860" id="tgt294" class="tgtSentence">stored procedure</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ceee9d3b560ecd339e4f6d1378dd93b8" id="tgt295" class="tgtSentence">A precompiled collection of code such as SQL statements and optional control-of-flow statements stored under a name and processed as a unit.</caps:sentence>
                <caps:sentence sentenceid="5222b2b79c0ade52515bdc63e653e9d0" id="tgt296" class="tgtSentence"> Stored procedures are stored within a database; they can be executed with one call from an application and allow user-declared variables, conditional execution, and other powerful programming features.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e8f65fd8d973f9985dc7ea3cf1614ae1" id="tgt297" class="tgtSentence">stub</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0f47d069835df0094d3e211a96b6f250" id="tgt298" class="tgtSentence">An interface-specific object that provides the parameter marshaling and communication required for an application object to receive calls from a client that is running in a different execution environment, such as on a different thread or in another process.</caps:sentence>
                <caps:sentence sentenceid="3701d65bac86feb5f1032817735227cf" id="tgt299" class="tgtSentence"> The stub is located with the application object and communicates with a corresponding proxy that is located with the client that calls it.</caps:sentence>
                <caps:sentence sentenceid="4f445e20ee6b249c83d7b2c7e3bb335a" id="tgt300" class="tgtSentence"> See also proxy.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="703e8e817eeda8efb66f1d952782dc88" id="tgt301" class="tgtSentence">sub-node</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5405bda9f2b39669552c32df2f8f2064" id="tgt302" class="tgtSentence">See child.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f84e01fb95cd60f222f9fe8633e4084f" id="tgt303" class="tgtSentence">synchronous operation</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="dd6979c96ddb22fd4875f99cd113691b" id="tgt304" class="tgtSentence">An operation initiated by code that completes before the next operation may start.</caps:sentence>
                <caps:sentence sentenceid="356cf931edb9c778913a572bafc95e0c" id="tgt305" class="tgtSentence"> See also asynchronous operation.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="35b320fc2e92df31e64a6317ab227eae" id="tgt306" class="tgtSentence">T-Z</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="c0af77cf8294ff93a5cdb2963ca9f038" id="tgt307" class="tgtSentence">Tree</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="35a1b0d08167f2be42c4174722b498ae" id="tgt308" class="tgtSentence">A structure representing a hierarchical relationship between elements (nodes).</caps:sentence>
                <caps:sentence sentenceid="f0750ed690d652098bf55a97b4661870" id="tgt309" class="tgtSentence"> There is one node at the top level of a tree (the root).</caps:sentence>
                <caps:sentence sentenceid="80c9f26f9a10816fd9ac3cd9a2b55d58" id="tgt310" class="tgtSentence"> Underneath the root, there can be multiple children.</caps:sentence>
                <caps:sentence sentenceid="390d6013e54db4675bfb22833a800313" id="tgt311" class="tgtSentence"> Each child may in turn be the parent of other children, thus branching like a tree.</caps:sentence>
                <caps:sentence sentenceid="08e951862a727c37003abe16e30b8b18" id="tgt312" class="tgtSentence"> A folder containing documents and other folders is a typical example of a tree structure.</caps:sentence>
                <caps:sentence sentenceid="a6d27864b1b6aef9223766db03e49bcc" id="tgt313" class="tgtSentence"> See also hierarchy, node, root, child, parent.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="4eaca60f93b9bc00b528a2dfce5334d5" id="tgt314" class="tgtSentence">Web server</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f3014b990534dcf94352c5278a13bb04" id="tgt315" class="tgtSentence">A computer that provides Web services and pages to intranet and Internet users.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This topic defines terms relevant to ADO.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">A</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence">absolute URL</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A fully-qualified URL that specifies the location of a resource that resides on the Internet or an intranet.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> See also <newTerm>URL</newTerm> and <newTerm>relative URL</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence">ActiveX control</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Self-registering, in-process COM component that often has a visual element either at design time or run time.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> ActiveX controls also have the ability to communicate with an Active Document container, such as Microsoft Internet Explorer.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence">ADISAPI (Advanced Data Internet Server Application Programming Interface)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">An ISAPI DLL that provides parsing, Automation control, Recordset marshaling, and MIME packaging.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> The ADISAPI component works through the API provided by Internet Information Services (IIS).</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> See also <newTerm>ISAPI</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src13" class="srcSentence">aggregate function</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src14" class="srcSentence">In a query, a function such as COUNT, AVG, or STDEV that calculates a value using all the rows in a column of a table.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> In writing expressions and in programming, you can use SQL aggregate functions (including the three listed above) and domain aggregate functions to determine various statistics.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src16" class="srcSentence">alias</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src17" class="srcSentence">An alternate name you give to a column or expression in an SQL SELECT statement, often shorter or more meaningful.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> For example, BobSales is the alias in the following SELECT statement: "Select wr-Sales as BobSales from SalesDB".</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> An alias can be used to dynamically assign columns to control bindings on the DataControl object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src20" class="srcSentence">apartment threading</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src21" class="srcSentence">A COM threading model where all calls to an object occur on one thread.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> In apartment threading, COM synchronizes and marshals calls.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> See also <newTerm>COMmddefcom</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src24" class="srcSentence">asynchronous operation </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src25" class="srcSentence">An operation that returns control to the calling program without waiting for the operation to complete.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> Before the operation is complete, code execution continues.</caps:sentence>
                <caps:sentence id="src27" class="srcSentence"> See also <newTerm>synchronous operation</newTerm>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">B</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src29" class="srcSentence">binding entry</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src30" class="srcSentence">A mapping between a field in a table and a variable.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> In the ADO Visual C++ extensions, <legacyBold>Recordset</legacyBold> fields are mapped to C/C++ variables.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src32" class="srcSentence">bitmask</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src33" class="srcSentence">A numeric value intended for a bit-by-bit value comparison with other numeric values, typically to flag options in parameter or return values.</caps:sentence>
                <caps:sentence id="src34" class="srcSentence"> Usually this comparison is done with bitwise logical operators, such as <legacyBold>And</legacyBold> and <legacyBold>Or</legacyBold> in Visual Basic, <legacyBold>&amp;</legacyBold> and <legacyBold>|</legacyBold> in C++.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src35" class="srcSentence">For example, the ADO <legacyBold>FieldAttributeEnum</legacyBold> values can be used as bitmasks to determine the attributes of a field.</caps:sentence>
                <caps:sentence id="src36" class="srcSentence"> Suppose you wanted to determine if a field was updateable.</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> You could test for this with the following expression in Visual Basic:<codeInline>Field.Attributes AND adFldUpdatable</codeInline></caps:sentence>
              </para>
              <para>
                <caps:sentence id="src38" class="srcSentence">If the result is TRUE, then the field is updateable.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src39" class="srcSentence">bookmark</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src40" class="srcSentence">A marker that uniquely identifies a row within a set of rows so that a user can quickly navigate to it.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src41" class="srcSentence">business object</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src42" class="srcSentence">An object that performs a defined set of operations, such as data validation or business rule logic.</caps:sentence>
                <caps:sentence id="src43" class="srcSentence"> Business objects usually reside on the middle tier.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src44" class="srcSentence">business rule</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src45" class="srcSentence">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business.</caps:sentence>
                <caps:sentence id="src46" class="srcSentence"> Also known as <legacyItalic>business logic</legacyItalic>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src47" class="srcSentence">C</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src48" class="srcSentence">calculated expression</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src49" class="srcSentence">An expression that is not constant, but whose value depends upon other values.</caps:sentence>
                <caps:sentence id="src50" class="srcSentence"> To be evaluated, a calculated expression must obtain and compute values from other sources, typically in other fields or rows.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src51" class="srcSentence">chapter</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src52" class="srcSentence">A reference to a range of rows from a data source.</caps:sentence>
                <caps:sentence id="src53" class="srcSentence"> In ADO, a chapter is typically a reference to another <legacyBold>Recordset</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src54" class="srcSentence">Chapter columns make it possible to define a <legacyItalic>parent-child</legacyItalic> relationship where the <legacyItalic>parent</legacyItalic> is the <legacyBold>Recordset</legacyBold> containing the chapter column and the <legacyItalic>child</legacyItalic> is the <legacyBold>Recordset</legacyBold> represented by the chapter.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src55" class="srcSentence">chapter-alias</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src56" class="srcSentence">An alias that refers to the column appended to the parent.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src57" class="srcSentence">character set</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src58" class="srcSentence">A mapping of a set of characters to their numeric values.</caps:sentence>
                <caps:sentence id="src59" class="srcSentence"> For example, Unicode is a 16-bit character set capable of encoding all known characters and used as a worldwide character-encoding standard.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src60" class="srcSentence">child</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src61" class="srcSentence">The dependant side of a hierarchical relationship.</caps:sentence>
                <caps:sentence id="src62" class="srcSentence"> A child is a node in a hierarchical structure that has another node above it (closer to the root).</caps:sentence>
                <caps:sentence id="src63" class="srcSentence"> See also <newTerm>child-alias</newTerm>, <newTerm>parent-child relationship</newTerm>, <newTerm>parent</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src64" class="srcSentence">child-alias</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src65" class="srcSentence">An alias that refers to the child.</caps:sentence>
                <caps:sentence id="src66" class="srcSentence"> See also <newTerm>alias</newTerm>, <newTerm>child</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src67" class="srcSentence">CLSID (class identifier)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src68" class="srcSentence">A universally unique identifier (UUID) that identifies a COM component.</caps:sentence>
                <caps:sentence id="src69" class="srcSentence"> Each COM component has its CLSID in the Windows Registry so that it can be loaded by other applications.</caps:sentence>
                <caps:sentence id="src70" class="srcSentence"> See also <newTerm>ProgID</newTerm>, <newTerm>COM</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src71" class="srcSentence">client tier</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src72" class="srcSentence">A logical layer of a distributed system that typically presents data to and processes input from the user, sometimes referred to as the <legacyItalic>front end</legacyItalic>.</caps:sentence>
                <caps:sentence id="src73" class="srcSentence"> Usually, the client tier requests data from a server based on input, and then formats and displays the result.</caps:sentence>
                <caps:sentence id="src74" class="srcSentence"> See also <newTerm>middle tier</newTerm>, <newTerm>data source tier</newTerm>, <newTerm>distributed application</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src75" class="srcSentence">COM (Component Object Model)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src76" class="srcSentence">A binary standard that enables objects to interoperate in a networked environment regardless of the language in which they were developed or on which computers they reside.</caps:sentence>
                <caps:sentence id="src77" class="srcSentence"> COM-based technologies include ActiveX Controls, Automation, and object linking and embedding (OLE).</caps:sentence>
                <caps:sentence id="src78" class="srcSentence"> COM allows an object to expose its functionality to other components and to host applications.</caps:sentence>
                <caps:sentence id="src79" class="srcSentence"> It defines both how the object exposes itself and how this exposure works across processes and across networks.</caps:sentence>
                <caps:sentence id="src80" class="srcSentence"> COM also defines the object's life cycle.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src81" class="srcSentence">COM component</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src82" class="srcSentence">Binary file — such as .dll, .ocx, and some .exe files — that supports the COM standard for providing objects.</caps:sentence>
                <caps:sentence id="src83" class="srcSentence"> Such a file contains code for one or more class factories, COM classes, registry-entry mechanisms, loading code, and so on.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src84" class="srcSentence">comparison operator</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src85" class="srcSentence">An operator that compares two expressions and returns a Boolean value.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src86" class="srcSentence">A criteria parameter that may be expressed as "&gt;" (greater than), "&lt;" (less than), "=" (equal), "&gt;=" (greater than or equal), "&lt;=" (less than or equal), "&lt;&gt;" (not equal), or "like" (pattern matching).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src87" class="srcSentence">component</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src88" class="srcSentence">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src89" class="srcSentence">compound file</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src90" class="srcSentence">An implementation of COM structured storage for files.</caps:sentence>
                <caps:sentence id="src91" class="srcSentence"> A compound file stores separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</caps:sentence>
                <caps:sentence id="src92" class="srcSentence"> Together, they function like a file system within a file.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src93" class="srcSentence">A number of individual files bound together in one physical file.</caps:sentence>
                <caps:sentence id="src94" class="srcSentence"> Each individual file in a compound file can be accessed as if it were a single physical file.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src95" class="srcSentence">constant</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src96" class="srcSentence">A numeric or string value that does not change.</caps:sentence>
                <caps:sentence id="src97" class="srcSentence"> Named ADO enumerations (enumerated constants) can be used in your code instead of actual values, for example, <legacyBold>adUseClient</legacyBold> is a constant whose value is 3.</caps:sentence>
                <caps:sentence id="src98" class="srcSentence"> (Const adUseClient = 3).</caps:sentence>
                <caps:sentence id="src99" class="srcSentence"> See also <newTerm>enumeration</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src100" class="srcSentence">cursor</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src101" class="srcSentence">A database element that controls record navigation, updateability of data, and the visibility of changes made to the database by other users.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src102" class="srcSentence">D</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src103" class="srcSentence">data binding</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src104" class="srcSentence">The process of associating the objects or controls of an application to a data source.</caps:sentence>
                <caps:sentence id="src105" class="srcSentence"> A control associated with a data source is called a <legacyItalic>data-bound control</legacyItalic>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src106" class="srcSentence">The contents of a data-bound control are associated with values from a database.</caps:sentence>
                <caps:sentence id="src107" class="srcSentence"> For example, a grid control that is bound to a <legacyBold>Recordset</legacyBold> object can be updated when the rows in the <legacyBold>Recordset</legacyBold> are updated.</caps:sentence>
                <caps:sentence id="src108" class="srcSentence"> When new values are retrieved by the <legacyBold>Recordset</legacyBold>, new values are displayed in the grid.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src109" class="srcSentence">data provider</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src110" class="srcSentence">Software that exposes data to an ADO application either directly or via a service provider.</caps:sentence>
                <caps:sentence id="src111" class="srcSentence"> See also service provider.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src112" class="srcSentence">data shaping</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src113" class="srcSentence">A technique which makes use of a formalized syntax (called <legacyBold>Shape language</legacyBold>) to define a specialized <legacyBold>Recordset</legacyBold> object (called a <newTerm>shaped Recordset</newTerm>) that contains not just data, but also references to other <legacyBold>Recordset</legacyBold> objects and/or computed values based on those other <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src114" class="srcSentence">data source tier</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src115" class="srcSentence">A logical layer of a distributed system that represents a computer running a DBMS, such as an SQL Server database.</caps:sentence>
                <caps:sentence id="src116" class="srcSentence"> See also <newTerm>client tier</newTerm>, <newTerm>middle tier</newTerm>, <newTerm>distributed application</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src117" class="srcSentence">DCOM</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src118" class="srcSentence">A wire protocol that enables COM components to communicate directly with each other across a network.</caps:sentence>
                <caps:sentence id="src119" class="srcSentence"> See also <newTerm>COM</newTerm>, <newTerm>component</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src120" class="srcSentence">DDL (Data Definition Language)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src121" class="srcSentence">Those statements in SQL that define, as opposed to manipulate, data.</caps:sentence>
                <caps:sentence id="src122" class="srcSentence"> The schema of a database is created or modified with DDL.</caps:sentence>
                <caps:sentence id="src123" class="srcSentence"> For example, <legacyBold>CREATE TABLE</legacyBold>, <legacyBold>CREATE INDEX</legacyBold>, <legacyBold>GRANT</legacyBold>, and <legacyBold>REVOKE</legacyBold> are SQL DDL statements.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src124" class="srcSentence">default stream</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src125" class="srcSentence">A text or binary stream (represented by a <legacyBold>Stream</legacyBold> object) that is associated with <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> objects when using certain OLE DB providers, such as the Microsoft OLE DB Provider for Internet Publishing.</caps:sentence>
                <caps:sentence id="src126" class="srcSentence"> The default stream typically contains the contents of a file such as the HTML code for the root of a Web site.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src127" class="srcSentence">distributed application</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src128" class="srcSentence">A program written so that the processing can be divided across multiple computers over a network.</caps:sentence>
                <caps:sentence id="src129" class="srcSentence"> Typically, a distributed application is divided into presentation, business logic, and data store layers, or <legacyItalic>tiers</legacyItalic>.</caps:sentence>
                <caps:sentence id="src130" class="srcSentence"> See also client tier, middle tier, data source tier.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src131" class="srcSentence">disconnected Recordset</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src132" class="srcSentence">A <legacyBold>Recordset</legacyBold> object in a client cache that no longer has a live connection to the server.</caps:sentence>
                <caps:sentence id="src133" class="srcSentence"> If the original data source needs to be accessed again for some reason, such as updating data, the connection must be re-established.</caps:sentence>
                <caps:sentence id="src134" class="srcSentence"> However, the collections, properties, and methods of a disconnected <legacyBold>Recordset</legacyBold> can still be accessed.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src135" class="srcSentence">DML (Data Manipulation Language)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src136" class="srcSentence">Those statements in SQL that manipulate, as opposed to define, data.</caps:sentence>
                <caps:sentence id="src137" class="srcSentence"> The values in a database are selected and modified with DML.</caps:sentence>
                <caps:sentence id="src138" class="srcSentence"> For example, <legacyBold>INSERT</legacyBold>, <legacyBold>UPDATE</legacyBold>, <legacyBold>DELETE</legacyBold>, and <legacyBold>SELECT</legacyBold> are SQL DML statements.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src139" class="srcSentence">document source provider</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src140" class="srcSentence">A special class of providers that manage folders and documents.</caps:sentence>
                <caps:sentence id="src141" class="srcSentence"> When a document is represented by a <legacyBold>Record</legacyBold> object, or a folder of documents is represented by a <legacyBold>Recordset</legacyBold> object, the document source provider populates those objects with a unique set of fields that describe characteristics of the document, instead of the actual document itself.</caps:sentence>
                <caps:sentence id="src142" class="srcSentence"> See also resource record.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src143" class="srcSentence">DSN (data source name)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src144" class="srcSentence">The collection of information used to connect your application to a particular ODBC database.</caps:sentence>
                <caps:sentence id="src145" class="srcSentence"> The ODBC Driver Manager uses this information to create a connection to the database.</caps:sentence>
                <caps:sentence id="src146" class="srcSentence"> A DSN can be stored in a file (a file DSN) or in the Windows Registry (a machine DSN).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src147" class="srcSentence">dynamic property</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src148" class="srcSentence">A property specific to a data provider or the cursor service.</caps:sentence>
                <caps:sentence id="src149" class="srcSentence"> The <legacyBold>Properties</legacyBold> collection of an object is populated with these automatically ("dynamically").</caps:sentence>
                <caps:sentence id="src150" class="srcSentence"> An object has no dynamic properties until it is connected to a data source through a particular data provider.</caps:sentence>
                <caps:sentence id="src151" class="srcSentence"> See also data provider, cursor.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src152" class="srcSentence">E</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src153" class="srcSentence">Enumeration</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src154" class="srcSentence">A list of named constants.</caps:sentence>
                <caps:sentence id="src155" class="srcSentence"> Enumerated values need not be unique.</caps:sentence>
                <caps:sentence id="src156" class="srcSentence"> However the name of each value must be unique within the scope where the enumeration is defined.</caps:sentence>
                <caps:sentence id="src157" class="srcSentence"> In ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version).</caps:sentence>
                <caps:sentence id="src158" class="srcSentence"> For example, to open a static <legacyBold>Recordset</legacyBold>, use the <legacyBold>adOpenStatic</legacyBold> enumerated value: <codeInline>Recordset.Open ,,adOpenStatic</codeInline></caps:sentence>
              </para>
              <para>
                <caps:sentence id="src159" class="srcSentence"> Also referred to as <legacyItalic>enumerated constant</legacyItalic>.</caps:sentence>
                <caps:sentence id="src160" class="srcSentence"> See also <newTerm>constant</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src161" class="srcSentence">event</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src162" class="srcSentence">An action recognized by an object, for which you can write code to respond.</caps:sentence>
                <caps:sentence id="src163" class="srcSentence"> Events can be generated by command execution, transaction completion, recordset navigation, and data updates, among other actions.</caps:sentence>
                <caps:sentence id="src164" class="srcSentence"> See also <newTerm>event handler</newTerm>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src165" class="srcSentence">event handler</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src166" class="srcSentence">An event handler is the code that is executed when an event occurs.</caps:sentence>
                <caps:sentence id="src167" class="srcSentence"> See also event.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src168" class="srcSentence">H</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src169" class="srcSentence">handler</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src170" class="srcSentence">A routine that manages a common and relatively simple condition or operation, such as error recovery or data management.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src171" class="srcSentence">hierarchical Recordset</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src172" class="srcSentence">A <legacyBold>Recordset</legacyBold> that contains another <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src173" class="srcSentence"> See also data shaping, chapter.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src174" class="srcSentence">For more information, see <legacyLink xlink:href="25f1d2a1-6d5e-4457-aa07-5db5c75dee18">Accessing Rows in a Hierarchical Recordset</legacyLink>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src175" class="srcSentence">hierarchy</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src176" class="srcSentence">In general, a hierarchy is a ranked structure with a top level and subordinate levels.</caps:sentence>
                <caps:sentence id="src177" class="srcSentence"> In ADO, hierarchical <legacyBold>Recordsets</legacyBold> are used to represent the parent-child relationship between a record and a chapter.</caps:sentence>
                <caps:sentence id="src178" class="srcSentence"> Also in ADO, <legacyBold>Record</legacyBold> and <legacyBold>Stream</legacyBold> objects can be used to access hierarchical tree structures such as a folder and documents.</caps:sentence>
                <caps:sentence id="src179" class="srcSentence"> ADO MD also includes <legacyBold>Hierarchy</legacyBold> objects to represent a relationship between the levels of a dimension in an OLAP cube.</caps:sentence>
                <caps:sentence id="src180" class="srcSentence"> See also hierarchical Recordsets, parent-child relationship, chapter, tree.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src181" class="srcSentence">I-L</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src182" class="srcSentence">ISAPI (Internet Server Application Programming Interface)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src183" class="srcSentence">A set of functions for Internet servers, such as a Windows NT® Server/Windows 2000 Server running Microsoft® Internet Information Services (IIS).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src184" class="srcSentence">Key</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src185" class="srcSentence">A column or columns in a table that uniquely identify a row; often used to index a table.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src186" class="srcSentence">M</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src187" class="srcSentence">marshaling</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src188" class="srcSentence">The process of packaging, sending, and unpackaging interface method parameters across thread or process boundaries.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src189" class="srcSentence">middle tier</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src190" class="srcSentence">The logical layer in a distributed system between a user interface or Web client and the database.</caps:sentence>
                <caps:sentence id="src191" class="srcSentence"> This is typically where business objects are instantiated.</caps:sentence>
                <caps:sentence id="src192" class="srcSentence"> The middle tier is a collection of business rules and functions that generate and operate upon receiving information.</caps:sentence>
                <caps:sentence id="src193" class="srcSentence"> They accomplish this through business rules, which can change frequently, and are thus encapsulated into components that are physically separate from the application logic itself.</caps:sentence>
                <caps:sentence id="src194" class="srcSentence"> Also known as <legacyItalic>application server tier</legacyItalic>.</caps:sentence>
                <caps:sentence id="src195" class="srcSentence"> See also distributed application, client tier, data source tier.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src196" class="srcSentence">MIME (Multi-purpose Internet Mail Extension)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src197" class="srcSentence">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, machine, and e-mail environments.</caps:sentence>
                <caps:sentence id="src198" class="srcSentence"> In practice, MIME has also been adopted and extended by non-mail applications.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src199" class="srcSentence">MIME is a standard that allows binary data to be published and read on the Internet.</caps:sentence>
                <caps:sentence id="src200" class="srcSentence"> The header of a file with binary data contains the MIME type of the data; this informs client programs (Web browsers and mail packages, for instance) that they will need to handle the data in a different way than they handle straight text.</caps:sentence>
                <caps:sentence id="src201" class="srcSentence"> For example, the header of a Web document containing a JPEG graphic contains the MIME type specific to the JPEG file format.</caps:sentence>
                <caps:sentence id="src202" class="srcSentence"> This allows a browser to display the file with its JPEG viewer, if one is present.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src203" class="srcSentence">N-O</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src204" class="srcSentence">node</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src205" class="srcSentence">An element in a hierarchical tree structure.</caps:sentence>
                <caps:sentence id="src206" class="srcSentence"> A node may be the root, or the child of another node.</caps:sentence>
                <caps:sentence id="src207" class="srcSentence"> A node can also be the parent of multiple children.</caps:sentence>
                <caps:sentence id="src208" class="srcSentence"> See also hierarchy, tree, root, child, parent.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src209" class="srcSentence">object variable</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src210" class="srcSentence">A variable that contains a reference to an object.</caps:sentence>
                <caps:sentence id="src211" class="srcSentence"> For example, <codeInline>objCustomObject</codeInline> is a variable that points to an object of type CustomObject:<codeInline>Set objCustomObject = CreateObject(adodb.Recordset)</codeInline></caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src212" class="srcSentence">ODBC (Open Database Connectivity)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src213" class="srcSentence">A standard programming language interface used to connect to a variety of data sources.</caps:sentence>
                <caps:sentence id="src214" class="srcSentence"> This is usually accessed through Control Panel, where data source names (DSNs) can be assigned to use specific ODBC drivers.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src215" class="srcSentence">OLE DB</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src216" class="srcSentence">A set of interfaces that expose data from a variety of sources using COM.</caps:sentence>
                <caps:sentence id="src217" class="srcSentence"> OLE DB interfaces provide applications with uniform access to data stored in diverse information sources.</caps:sentence>
                <caps:sentence id="src218" class="srcSentence"> These interfaces support the amount of DBMS functionality appropriate to the data source, enabling it to share its data.</caps:sentence>
                <caps:sentence id="src219" class="srcSentence"> See also COM.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src220" class="srcSentence">optimistic locking</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src221" class="srcSentence">A type of locking in which the data page containing one or more records, including the record being edited, is unavailable to other users only while the record is being updated by the <legacyBold>Update</legacyBold> method, but is available before and after the call to <legacyBold>Update</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src222" class="srcSentence"> Optimistic locking is used when the <legacyBold>Recordset</legacyBold> object is opened with the <legacyBold>LockType</legacyBold> parameter or property set to <legacyBold>adLockOptimistic</legacyBold> or <legacyBold>adLockBatchOptimistic</legacyBold>.</caps:sentence>
                <caps:sentence id="src223" class="srcSentence"> See also pessimistic locking.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src224" class="srcSentence">ordinal value</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src225" class="srcSentence">The numeric location of an item within an order.</caps:sentence>
                <caps:sentence id="src226" class="srcSentence"> In an ADO collection, the ordinal value of the first item is zero (0).</caps:sentence>
                <caps:sentence id="src227" class="srcSentence"> The next item is one (1), and so on.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src228" class="srcSentence">P</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src229" class="srcSentence">parameterized command</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src230" class="srcSentence">A query or command that allows you to set parameter values before the command is executed.</caps:sentence>
                <caps:sentence id="src231" class="srcSentence"> For example, a SQL string can be parameterized by embedding parameter markers in the SQL string (designated by the '?' character).</caps:sentence>
                <caps:sentence id="src232" class="srcSentence"> The application then specifies values for each parameter and executes the command.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src233" class="srcSentence">parent</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src234" class="srcSentence">The controlling side of a hierarchical relationship.</caps:sentence>
                <caps:sentence id="src235" class="srcSentence"> In a hierarchical structure, a parent has one or more child nodes directly beneath it in the hierarchy.</caps:sentence>
                <caps:sentence id="src236" class="srcSentence"> See also parent-alias, parent-child relationship, child.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src237" class="srcSentence">parent-alias</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src238" class="srcSentence">An alias that refers to the parent.</caps:sentence>
                <caps:sentence id="src239" class="srcSentence"> See also alias, parent.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src240" class="srcSentence">parent-child relationship</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src241" class="srcSentence">A relationship in a hierarchical structure in which the parent is one level higher and directly associated with one or more children.</caps:sentence>
                <caps:sentence id="src242" class="srcSentence"> A child is one level lower and must have one parent.</caps:sentence>
                <caps:sentence id="src243" class="srcSentence"> See also parent, child.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src244" class="srcSentence">pessimistic locking</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src245" class="srcSentence">A type of locking in which the page containing one or more records, including the record being edited, is unavailable to other users to ensure that an update will be made.</caps:sentence>
                <caps:sentence id="src246" class="srcSentence"> Pessimistic locking behavior is defined by the OLE DB provider.</caps:sentence>
                <caps:sentence id="src247" class="srcSentence"> Typically, records are locked upon editing and remain unavailable until the <legacyBold>Update</legacyBold> method has completed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src248" class="srcSentence"> Pessimistic locking is enabled when the <legacyBold>Recordset</legacyBold> object is opened with the <legacyBold>LockType</legacyBold> parameter or property set to <legacyBold>adLockPessimistic</legacyBold>.</caps:sentence>
                <caps:sentence id="src249" class="srcSentence"> See also optimistic locking.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src250" class="srcSentence">pooling</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src251" class="srcSentence">A performance optimization based on using collections of pre-allocated resources, such as objects or database connections.</caps:sentence>
                <caps:sentence id="src252" class="srcSentence"> It is more efficient to draw an existing resource from the pool than to create a new resource.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src253" class="srcSentence">ProgID (programmatic identifier)</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src254" class="srcSentence">A unique name mapped to the Windows registry by a COM application.</caps:sentence>
                <caps:sentence id="src255" class="srcSentence"> The ProgID for an ADO Connection is "ADODB.Connection".</caps:sentence>
                <caps:sentence id="src256" class="srcSentence"> See also CLSID, COM.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src257" class="srcSentence">proxy</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src258" class="srcSentence">An interface-specific object that provides the parameter marshaling and communication required for a client to call an application object that is running in a different execution environment, such as on a different thread or in another process.</caps:sentence>
                <caps:sentence id="src259" class="srcSentence"> The proxy is located with the client and communicates with a corresponding stub that is located with the application object that is being called.</caps:sentence>
                <caps:sentence id="src260" class="srcSentence"> See also stub.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src261" class="srcSentence">R</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src262" class="srcSentence">relative URL</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src263" class="srcSentence">A partially qualified URL that specifies a resource on the Internet or an intranet whose location is relative to a starting point specified by an absolute URL or equivalent ADO Connection object.</caps:sentence>
                <caps:sentence id="src264" class="srcSentence"> In effect, the concatenated absolute and relative URLs consitute a complete URL.</caps:sentence>
                <caps:sentence id="src265" class="srcSentence"> See also URL and absolute URL.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src266" class="srcSentence">remote data source</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src267" class="srcSentence">A data source that exists on a another computer, rather than on the local system (where the client application runs).</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src268" class="srcSentence">resource record</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src269" class="srcSentence">A record from a document source provider that contains fields for the definition and description of a folder or document.</caps:sentence>
                <caps:sentence id="src270" class="srcSentence"> The document itself is not contained in the resource record but typically can be accessed by the default stream or a field in the resource record containing a URL.</caps:sentence>
                <caps:sentence id="src271" class="srcSentence"> See also document source provider, default stream, URL.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src272" class="srcSentence">rowset</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src273" class="srcSentence">A set of rows from a data source, all having the same field schema.</caps:sentence>
                <caps:sentence id="src274" class="srcSentence"> A rowset can represent all or some fields from a table.</caps:sentence>
                <caps:sentence id="src275" class="srcSentence"> A rowset can also represent a virtual table, created by a query or a join of two or more tables.</caps:sentence>
                <caps:sentence id="src276" class="srcSentence"> In ADO, rowsets are represented by <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src277" class="srcSentence">S</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src278" class="srcSentence">Scope</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src279" class="srcSentence">The range of reference for an object or variable or a range of records in a view or table.</caps:sentence>
                <caps:sentence id="src280" class="srcSentence"> For example, local variables can be referenced only within the procedure in which they were defined.</caps:sentence>
                <caps:sentence id="src281" class="srcSentence"> Public variables are accessible from anywhere in the application.</caps:sentence>
                <caps:sentence id="src282" class="srcSentence"> Objects, such as the current database, are in scope if they are in the defined search path.</caps:sentence>
                <caps:sentence id="src283" class="srcSentence"> Record ranges can be specified with a Scope clause in many commands.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src284" class="srcSentence">service provider</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src285" class="srcSentence">Software that encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</caps:sentence>
                <caps:sentence id="src286" class="srcSentence"> It is a provider that does not directly expose data, rather it provides a service, such as query processing.</caps:sentence>
                <caps:sentence id="src287" class="srcSentence"> The service provider may process data provided by a data provider.</caps:sentence>
                <caps:sentence id="src288" class="srcSentence"> See also data provider.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src289" class="srcSentence">shaped Recordset</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src290" class="srcSentence">A <legacyBold>Recordset</legacyBold> whose columns have been specifically defined to contain not just data, but also references (called chapters) to other <legacyBold>Recordset</legacyBold> objects and/or computed values based on other <legacyBold>Recordset</legacyBold> objects.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src291" class="srcSentence">sibling</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src292" class="srcSentence">Any two or more nodes in a hierarchical structure that are on the same level in the hierarchy.</caps:sentence>
                <caps:sentence id="src293" class="srcSentence"> The root node in a hierarchy has no siblings.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src294" class="srcSentence">stored procedure</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src295" class="srcSentence">A precompiled collection of code such as SQL statements and optional control-of-flow statements stored under a name and processed as a unit.</caps:sentence>
                <caps:sentence id="src296" class="srcSentence"> Stored procedures are stored within a database; they can be executed with one call from an application and allow user-declared variables, conditional execution, and other powerful programming features.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src297" class="srcSentence">stub</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src298" class="srcSentence">An interface-specific object that provides the parameter marshaling and communication required for an application object to receive calls from a client that is running in a different execution environment, such as on a different thread or in another process.</caps:sentence>
                <caps:sentence id="src299" class="srcSentence"> The stub is located with the application object and communicates with a corresponding proxy that is located with the client that calls it.</caps:sentence>
                <caps:sentence id="src300" class="srcSentence"> See also proxy.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src301" class="srcSentence">sub-node</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src302" class="srcSentence">See child.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src303" class="srcSentence">synchronous operation</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src304" class="srcSentence">An operation initiated by code that completes before the next operation may start.</caps:sentence>
                <caps:sentence id="src305" class="srcSentence"> See also asynchronous operation.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src306" class="srcSentence">T-Z</caps:sentence>
        </title>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src307" class="srcSentence">Tree</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src308" class="srcSentence">A structure representing a hierarchical relationship between elements (nodes).</caps:sentence>
                <caps:sentence id="src309" class="srcSentence"> There is one node at the top level of a tree (the root).</caps:sentence>
                <caps:sentence id="src310" class="srcSentence"> Underneath the root, there can be multiple children.</caps:sentence>
                <caps:sentence id="src311" class="srcSentence"> Each child may in turn be the parent of other children, thus branching like a tree.</caps:sentence>
                <caps:sentence id="src312" class="srcSentence"> A folder containing documents and other folders is a typical example of a tree structure.</caps:sentence>
                <caps:sentence id="src313" class="srcSentence"> See also hierarchy, node, root, child, parent.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src314" class="srcSentence">Web server</caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src315" class="srcSentence">A computer that provides Web services and pages to intranet and Internet users.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
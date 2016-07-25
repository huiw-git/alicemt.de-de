---
title: "Visual C++ Extensions for ADO"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2952ece0-7217-4448-bb09-f6b64f43b7e2
caps.latest.revision: 9
caps.handback.revision: 9
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
# Visual C++ Extensions for ADO
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="88697a06ee2862269f65afa22c5ca8df" id="tgt1" class="tgtSentence">The preferred method of programming ADO with Visual C++ is using the <legacyBold>#import </legacyBold>directive, as discussed in <legacyLink xlink:href="11233b96-e05c-4221-9aed-5f20944b0f1c">Microsoft Visual C++ ADO Programming</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="c52e09389d182c9fa4b1983f7306874b" id="tgt2" class="tgtSentence"> However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</caps:sentence>
          <caps:sentence sentenceid="8caa73e8197139fe30f63d8326dea727" id="tgt3" class="tgtSentence"> This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using #<legacyBold>import</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ceeeec70fd475bb19ac482bdc2b83cfd" id="tgt4" class="tgtSentence">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure.</caps:sentence>
          <caps:sentence sentenceid="79d56fca9e60c592d9dcca6a56cd6661" id="tgt5" class="tgtSentence"> In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2986363ff4a26b8c8787af09d4ba5423" id="tgt6" class="tgtSentence">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface.</caps:sentence>
          <caps:sentence sentenceid="68b4cb3a98321c776d6bc1d5113c2338" id="tgt7" class="tgtSentence"> The result is a flexible tool that is easier to use and has great performance.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="6700db71f0f0b5aa5aff10241baee405" id="tgt8" class="tgtSentence">A common C/C++ client scenario is to bind a record in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to a C/C++ struct or class containing native C/C++ types.</caps:sentence>
          <caps:sentence sentenceid="9eba75be56520e6dc42644b56572ba2d" id="tgt9" class="tgtSentence"> When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types.</caps:sentence>
          <caps:sentence sentenceid="17810680d0096fa6ab066ede28cade8d" id="tgt10" class="tgtSentence"> The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="797921279a24ff635fb4dee09f66b85f" id="tgt11" class="tgtSentence">See the following topics to learn more about the Visual C++ Extensions for ADO.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="7aa01654cc1722b1f239e6023fc161d5" id="tgt12" class="tgtSentence">             <legacyLink xlink:href="ff759185-df41-4507-8d12-0921894ffbd9">Using Visual C++ Extensions for ADO</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="56a08ccc2651d74d74e91dd0488a2969" id="tgt13" class="tgtSentence">             <legacyLink xlink:href="e492d307-24cb-489c-a5b0-99cdc09b07da">Visual C++ Extensions Header</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a33639434f329dd5eea5fabf65636146" id="tgt14" class="tgtSentence">             <legacyLink xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">ADO with Visual C++ Extensions Example</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="d02b199e-1e52-4cc9-b118-750952ae7f63">ADO for Visual C++ Syntax Index for COM</link>
        <link xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">ADO with Visual C++ Extensions Example</link>
        <link xlink:href="ff759185-df41-4507-8d12-0921894ffbd9">Using Visual C++ Extensions for ADO</link>
        <link xlink:href="e492d307-24cb-489c-a5b0-99cdc09b07da">Visual C++ Extensions Header</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The preferred method of programming ADO with Visual C++ is using the <legacyBold>#import </legacyBold>directive, as discussed in <legacyLink xlink:href="11233b96-e05c-4221-9aed-5f20944b0f1c">Microsoft Visual C++ ADO Programming</legacyLink>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using #<legacyBold>import</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> The result is a flexible tool that is easier to use and has great performance.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">A common C/C++ client scenario is to bind a record in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> to a C/C++ struct or class containing native C/C++ types.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">See the following topics to learn more about the Visual C++ Extensions for ADO.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">             <legacyLink xlink:href="ff759185-df41-4507-8d12-0921894ffbd9">Using Visual C++ Extensions for ADO</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">             <legacyLink xlink:href="e492d307-24cb-489c-a5b0-99cdc09b07da">Visual C++ Extensions Header</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">             <legacyLink xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">ADO with Visual C++ Extensions Example</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="d02b199e-1e52-4cc9-b118-750952ae7f63">ADO for Visual C++ Syntax Index for COM</link>
        <link xlink:href="9739c278-582c-402b-a158-7f68a1b2c293">ADO with Visual C++ Extensions Example</link>
        <link xlink:href="ff759185-df41-4507-8d12-0921894ffbd9">Using Visual C++ Extensions for ADO</link>
        <link xlink:href="e492d307-24cb-489c-a5b0-99cdc09b07da">Visual C++ Extensions Header</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Using ADO with Microsoft Visual J++"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 15542c35-3bf7-4d5f-a3b2-3a5cff286987
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
# Using ADO with Microsoft Visual J++
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="19a1deff125fd09298c4184613fba031" id="tgt1" class="tgtSentence">You can implement ADO using Visual J++ in the following ways:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="bcc486b3aea167922cf7d26f2c922750" id="tgt2" class="tgtSentence">With Visual J++ 6.0 (or later), use ADO for Windows Foundation Classes.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9aa3329b34f331b5338ebf0deddbe659" id="tgt3" class="tgtSentence">With Visual J++ 1.x, use the Java Type Library Wizard.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8256cb4972cf139cb28e6c21ebe6a5e0" id="tgt4" class="tgtSentence">Use the Microsoft SDK for Java utilities.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt5" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="7c9f220b88442212e486828e6afa6fcf" id="tgt6" class="tgtSentence">             <legacyLink xlink:href="1fdfa42e-897e-4770-b320-ab3720adabcc">ADO/WFC Programming</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="172d256908036368f429562273436626" id="tgt7" class="tgtSentence">             <legacyLink xlink:href="f9737a65-4b2f-47fa-b026-1494dca158eb">Using the Java Type Library Wizard</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9c7ecb58133f93c78f3cffd12e58b29b" id="tgt8" class="tgtSentence">             <legacyLink xlink:href="2d7cb5b5-8307-49dd-b07e-c07069bb1626">Using the Microsoft SDK for Java</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c342bb17f1610c2946b3d3953105e47a" id="tgt9" class="tgtSentence">             <legacyLink xlink:href="1fc09dc1-9e32-412e-9f43-b8eb8bb483ca">ADO Java Class Wrappers</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="1fdfa42e-897e-4770-b320-ab3720adabcc">ADO for Windows Foundation Classes</link>
        <link xlink:href="1fc09dc1-9e32-412e-9f43-b8eb8bb483ca">ADO Java Class Wrappers</link>
        <link xlink:href="a14bbc36-87ec-409d-97b3-393b66b1b8e3">ADO/WFC Syntax Index</link>
        <link xlink:href="9dfb6784-037d-4f9d-bb7f-b506b4498573">Using ADO with Microsoft Visual Basic</link>
        <link xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">Using ADO with Microsoft Visual C++</link>
        <link xlink:href="76fc4d00-0c9f-422b-af5c-af6ed8fb29d8">Using ADO with Scripting Languages</link>
        <link xlink:href="f9737a65-4b2f-47fa-b026-1494dca158eb">Using ADO with the Java Type Library Wizard</link>
        <link xlink:href="2d7cb5b5-8307-49dd-b07e-c07069bb1626">Using ADO with the Microsoft SDK for Java</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">You can implement ADO using Visual J++ in the following ways:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">With Visual J++ 6.0 (or later), use ADO for Windows Foundation Classes.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">With Visual J++ 1.x, use the Java Type Library Wizard.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Use the Microsoft SDK for Java utilities.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src5" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">             <legacyLink xlink:href="1fdfa42e-897e-4770-b320-ab3720adabcc">ADO/WFC Programming</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">             <legacyLink xlink:href="f9737a65-4b2f-47fa-b026-1494dca158eb">Using the Java Type Library Wizard</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">             <legacyLink xlink:href="2d7cb5b5-8307-49dd-b07e-c07069bb1626">Using the Microsoft SDK for Java</legacyLink>           </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">             <legacyLink xlink:href="1fc09dc1-9e32-412e-9f43-b8eb8bb483ca">ADO Java Class Wrappers</legacyLink>           </caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="1fdfa42e-897e-4770-b320-ab3720adabcc">ADO for Windows Foundation Classes</link>
        <link xlink:href="1fc09dc1-9e32-412e-9f43-b8eb8bb483ca">ADO Java Class Wrappers</link>
        <link xlink:href="a14bbc36-87ec-409d-97b3-393b66b1b8e3">ADO/WFC Syntax Index</link>
        <link xlink:href="9dfb6784-037d-4f9d-bb7f-b506b4498573">Using ADO with Microsoft Visual Basic</link>
        <link xlink:href="07d25fc0-4958-4e12-b616-36257ead812b">Using ADO with Microsoft Visual C++</link>
        <link xlink:href="76fc4d00-0c9f-422b-af5c-af6ed8fb29d8">Using ADO with Scripting Languages</link>
        <link xlink:href="f9737a65-4b2f-47fa-b026-1494dca158eb">Using ADO with the Java Type Library Wizard</link>
        <link xlink:href="2d7cb5b5-8307-49dd-b07e-c07069bb1626">Using ADO with the Microsoft SDK for Java</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Reshaping"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b1c965b7-3dad-4de6-9e0e-502ca8785be3
caps.latest.revision: 13
caps.handback.revision: 13
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
# Reshaping
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b84e9fc19616efd6788c65e1a8c263af" id="tgt1" class="tgtSentence">A <legacyBold>Recordset</legacyBold> created by a clause of a shape command may be assigned an <legacyItalic>alias</legacyItalic> name (typically with the AS keyword).</caps:sentence>
          <caps:sentence sentenceid="4abfc3169558282447d9192d0bf4557d" id="tgt2" class="tgtSentence"> The alias of a shaped <legacyBold>Recordset</legacyBold> can be referenced in a completely different command.</caps:sentence>
          <caps:sentence sentenceid="df2fbbecbab0ec21f411e543b7ca6169" id="tgt3" class="tgtSentence"> That is, you can reuse, or <legacyItalic>reshape</legacyItalic>, a previously shaped <legacyBold>Recordset</legacyBold> in a new shape command.</caps:sentence>
          <caps:sentence sentenceid="e7d77585977a1c4deb50a1f5a48f7088" id="tgt4" class="tgtSentence"> To support this feature, ADO provides a property, <legacyLink xlink:href="690229d1-46cc-42e6-a57d-4438251fe248">Reshape Name</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ab4a965447e587e7d924131a53aba18a" id="tgt5" class="tgtSentence">Reshaping has two main functions.</caps:sentence>
          <caps:sentence sentenceid="8e180dfb04c748619762812fc78c24c3" id="tgt6" class="tgtSentence"> The first is to associate an existing <legacyBold>Recordset</legacyBold> with a new parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <codeExample>
        <code>rs1.Open "SHAPE {select * from Customers} " &amp; _
         "APPEND ({select * from Orders} AS <codeFeaturedElement xmlns="">chapOrders</codeFeaturedElement> " &amp; _
         "RELATE CustomerID to CustomerID)", cn

rs2.Open "SHAPE {select * from Employees} " &amp; _
         "APPEND (<codeFeaturedElement xmlns="">chapOrders</codeFeaturedElement> RELATE EmployeeID to EmployeeID)", cn</code>
        <comments>
          <content>
            <para>
              <caps:sentence sentenceid="5b52adc10e9de081c3bb59352bd31963" id="tgt7" class="tgtSentence">The second function is to enable non-chaptered access to existing child <legacyBold>Recordset</legacyBold> objects, using the syntax "SHAPE &lt;recordset reshape name&gt;".</caps:sentence>
            </para>
            <alert class="note">
              <para>
                <caps:sentence sentenceid="35d1412d73f4b7c35ba892ad72144659" id="tgt8" class="tgtSentence">You cannot append columns to an existing <legacyBold>Recordset</legacyBold>, reshape a parameterized <legacyBold>Recordset</legacyBold> or the <legacyBold>Recordset</legacyBold> objects in any intervening COMPUTE clause, or perform aggregate operations on any <legacyBold>Recordset</legacyBold> descendant from the <legacyBold>Recordset</legacyBold> being reshaped.</caps:sentence>
                <caps:sentence sentenceid="2e7c1ab9a3d7b52615a1e50a51c3894c" id="tgt9" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> being reshaped and the new shape command must both use the same <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>.</caps:sentence>
              </para>
            </alert>
          </content>
        </comments>
      </codeExample>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">A <legacyBold>Recordset</legacyBold> created by a clause of a shape command may be assigned an <legacyItalic>alias</legacyItalic> name (typically with the AS keyword).</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The alias of a shaped <legacyBold>Recordset</legacyBold> can be referenced in a completely different command.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> That is, you can reuse, or <legacyItalic>reshape</legacyItalic>, a previously shaped <legacyBold>Recordset</legacyBold> in a new shape command.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> To support this feature, ADO provides a property, <legacyLink xlink:href="690229d1-46cc-42e6-a57d-4438251fe248">Reshape Name</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">Reshaping has two main functions.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The first is to associate an existing <legacyBold>Recordset</legacyBold> with a new parent <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <codeExample>
        <code>rs1.Open "SHAPE {select * from Customers} " &amp; _
         "APPEND ({select * from Orders} AS <codeFeaturedElement xmlns="">chapOrders</codeFeaturedElement> " &amp; _
         "RELATE CustomerID to CustomerID)", cn

rs2.Open "SHAPE {select * from Employees} " &amp; _
         "APPEND (<codeFeaturedElement xmlns="">chapOrders</codeFeaturedElement> RELATE EmployeeID to EmployeeID)", cn</code>
        <comments>
          <content>
            <para>
              <caps:sentence id="src7" class="srcSentence">The second function is to enable non-chaptered access to existing child <legacyBold>Recordset</legacyBold> objects, using the syntax "SHAPE &lt;recordset reshape name&gt;".</caps:sentence>
            </para>
            <alert class="note">
              <para>
                <caps:sentence id="src8" class="srcSentence">You cannot append columns to an existing <legacyBold>Recordset</legacyBold>, reshape a parameterized <legacyBold>Recordset</legacyBold> or the <legacyBold>Recordset</legacyBold> objects in any intervening COMPUTE clause, or perform aggregate operations on any <legacyBold>Recordset</legacyBold> descendant from the <legacyBold>Recordset</legacyBold> being reshaped.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> The <legacyBold>Recordset</legacyBold> being reshaped and the new shape command must both use the same <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>.</caps:sentence>
              </para>
            </alert>
          </content>
        </comments>
      </codeExample>
      <relatedTopics>
        <link xlink:href="1bfdcad4-52e1-45bc-ad21-783657ef0a44">Data Shaping</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
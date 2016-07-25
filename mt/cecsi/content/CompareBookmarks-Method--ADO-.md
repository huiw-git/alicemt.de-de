---
title: "CompareBookmarks Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d0b64286-2cc4-4a22-8f1d-9aefeebbcbc6
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
# CompareBookmarks Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a7d8935330860954f167f6cd9ee4d3c3" id="tgt1" class="tgtSentence">Compares two bookmarks and returns an indication of their relative values.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>result = recordset</parameterReference>.<legacyBold>CompareBookmarks(</legacyBold><parameterReference>Bookmark1</parameterReference>, <parameterReference>Bookmark2</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="5a9151e78742700be3e595191733ea45" id="tgt2" class="tgtSentence">Returns a <legacyLink xlink:href="bc8f710d-0621-4673-8d8e-0361e44abed0">CompareEnum</legacyLink> value that indicates the relative row position of two records represented by their bookmarks.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="1c032410c6e330abad092a2b5eaf429c" id="tgt3" class="tgtSentence"> <parameterReference>Bookmark1 </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="14a208fcebd1f39352ab0d01cd471811" id="tgt4" class="tgtSentence">The bookmark of the first row.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="1149ec886f1dce2a6b6405b40feef3ec" id="tgt5" class="tgtSentence"> <parameterReference>Bookmark2 </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="9bfb16b8c009f2b5b3766b6712692992" id="tgt6" class="tgtSentence">The bookmark of the second row.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7d63e89c198bf009602b2fb1d1d0628e" id="tgt7" class="tgtSentence">The bookmarks must apply to the same <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object and its <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">clone</legacyLink>.</caps:sentence>
            <caps:sentence sentenceid="037042ccec3579ad909d4d578ec4a2b7" id="tgt8" class="tgtSentence"> You cannot reliably compare bookmarks from different <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects, even if they were created from the same source or command.</caps:sentence>
            <caps:sentence sentenceid="2b5bf7dfe5cfb4266aecf52fa994e0e2" id="tgt9" class="tgtSentence"> Nor can you compare bookmarks for a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object whose underlying provider does not support comparisons.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="87584758950e2230bcfbb8fde1eea6d0" id="tgt10" class="tgtSentence">A bookmark uniquely identifies a row in a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="c5ad6baccb5e26e3939c4e8bc6b76fb8" id="tgt11" class="tgtSentence"> Use the <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink> property of the current row to obtain its bookmark.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d1ef9f48a3ccf1b0ce22017a593d3f49" id="tgt12" class="tgtSentence">Because the data type of a bookmark is specific to each provider, ADO exposes it as a <languageKeyword>Variant</languageKeyword>.</caps:sentence>
            <caps:sentence sentenceid="28d9e3c80d99a33f375f0dd962140ff5" id="tgt13" class="tgtSentence"> For example, SQL Server bookmarks are of type DBTYPE_R8 (<languageKeyword>Double</languageKeyword>).</caps:sentence>
            <caps:sentence sentenceid="af6e8637d0981ec61f4babcee03116b8" id="tgt14" class="tgtSentence"> ADO would expose this type as a <languageKeyword>Variant</languageKeyword> with a subtype of <languageKeyword>Double</languageKeyword>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="823a01ad84b539aa46f588baa2974207" id="tgt15" class="tgtSentence">When comparing bookmarks, ADO does not attempt any type of coercion.</caps:sentence>
            <caps:sentence sentenceid="0522572030cc8d7b17756a68d14d7bbd" id="tgt16" class="tgtSentence"> The values are simply passed to the provider where the comparison occurs.</caps:sentence>
            <caps:sentence sentenceid="fae8807a57ef60416e746bf5758cdb47" id="tgt17" class="tgtSentence"> If the bookmarks passed to the <unmanagedCodeEntityReference>CompareBookmarks</unmanagedCodeEntityReference> method are stored in variables of differing types, it can generate the following type mismatch error: "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="721e74332ad060a2a6d87503dce57694" id="tgt18" class="tgtSentence">A bookmark that is not valid or incorrectly formed will cause an error.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt19" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f156aa48-bfc2-40d1-962b-7b08855776c6">Visual Basic Example</link>
        <link xlink:href="24ab3f3a-29c5-4ee1-942e-2634c02d0778">Visual C++ Example</link>
        <link xlink:href="3c679a15-e924-49a5-8f3a-38a8266064f8">Visual J++ Example </link>
        <link xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Compares two bookmarks and returns an indication of their relative values.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>result = recordset</parameterReference>.<legacyBold>CompareBookmarks(</legacyBold><parameterReference>Bookmark1</parameterReference>, <parameterReference>Bookmark2</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <legacyLink xlink:href="bc8f710d-0621-4673-8d8e-0361e44abed0">CompareEnum</legacyLink> value that indicates the relative row position of two records represented by their bookmarks.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <parameterReference>Bookmark1 </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">The bookmark of the first row.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <parameterReference>Bookmark2 </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">The bookmark of the second row.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">The bookmarks must apply to the same <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object and its <legacyLink xlink:href="ad49265f-1c05-4271-9bbf-7c00010ac18c">clone</legacyLink>.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> You cannot reliably compare bookmarks from different <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> objects, even if they were created from the same source or command.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Nor can you compare bookmarks for a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object whose underlying provider does not support comparisons.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">A bookmark uniquely identifies a row in a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> Use the <legacyLink xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark</legacyLink> property of the current row to obtain its bookmark.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">Because the data type of a bookmark is specific to each provider, ADO exposes it as a <languageKeyword>Variant</languageKeyword>.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> For example, SQL Server bookmarks are of type DBTYPE_R8 (<languageKeyword>Double</languageKeyword>).</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> ADO would expose this type as a <languageKeyword>Variant</languageKeyword> with a subtype of <languageKeyword>Double</languageKeyword>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">When comparing bookmarks, ADO does not attempt any type of coercion.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> The values are simply passed to the provider where the comparison occurs.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> If the bookmarks passed to the <unmanagedCodeEntityReference>CompareBookmarks</unmanagedCodeEntityReference> method are stored in variables of differing types, it can generate the following type mismatch error: "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">A bookmark that is not valid or incorrectly formed will cause an error.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src19" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="f156aa48-bfc2-40d1-962b-7b08855776c6">Visual Basic Example</link>
        <link xlink:href="24ab3f3a-29c5-4ee1-942e-2634c02d0778">Visual C++ Example</link>
        <link xlink:href="3c679a15-e924-49a5-8f3a-38a8266064f8">Visual J++ Example </link>
        <link xlink:href="481dcc93-487b-490e-ac58-a1e9b2ebfd43">Bookmark Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
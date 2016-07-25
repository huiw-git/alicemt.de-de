---
title: "SetObjectOwner Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e5170a37-9d6e-43db-bfb6-9b6631fa3048
caps.latest.revision: 11
caps.handback.revision: 11
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
# SetObjectOwner Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4310b62a00358c77c69d65d7e982e053" id="tgt1" class="tgtSentence">Specifies the owner of an object in a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Catalog</parameterReference>
          <legacyBold>.SetObjectOwner </legacyBold>
          <parameterReference>ObjectName</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference> ObjectType</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference> OwnerName </parameterReference>[<legacyBold>,</legacyBold><parameterReference>ObjectTypeId</parameterReference>]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="ae6acff36db658f5736cb4196cf31a90" id="tgt2" class="tgtSentence"> <parameterReference>ObjectName </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="f288e39118d48030c1aa0b3eba73f148" id="tgt3" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that specifies the name of the object for which to specify the owner.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a068fbafa8e7b1855906ec04c64f2094" id="tgt4" class="tgtSentence"> <parameterReference>ObjectType </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d755d27c75efe22d516246c26e373e69" id="tgt5" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">ObjectTypeEnum</legacyLink> constants that specifies the owner type.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="2c672e5be89220850e8666a5ceb6b1bd" id="tgt6" class="tgtSentence"> <parameterReference>OwnerName </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="dac9e41ca7a18ed8ab4fa494e391161a" id="tgt7" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that specifies the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> of the <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> or <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> to own the object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e4719a6e71a5f7e279f5954e67b99392" id="tgt8" class="tgtSentence"> <parameterReference>ObjectTypeId </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt9" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="cb52fefc710a547ea2098e6e63a13813" id="tgt10" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> value that specifies the GUID for a provider object type that is not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence sentenceid="21900920cef00f532764b9e5b0bd7c68" id="tgt11" class="tgtSentence"> This parameter is required if <parameterReference>ObjectType</parameterReference> is set to <legacyBold>adPermObjProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="2d5e7933c26a39588a83d13a85395fe3" id="tgt12" class="tgtSentence">An error will occur if the provider does not support specifying object owners.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt13" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e44ec3d4-42ae-447d-aaed-bdea53cb0cca">GetObjectOwner and SetObjectOwner Methods Example (VB)</link>
        <link xlink:href="8965adf0-9075-4125-8142-73eb700029c3">GetObjectOwner Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies the owner of an object in a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Catalog</parameterReference>
          <legacyBold>.SetObjectOwner </legacyBold>
          <parameterReference>ObjectName</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference> ObjectType</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference> OwnerName </parameterReference>[<legacyBold>,</legacyBold><parameterReference>ObjectTypeId</parameterReference>]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <parameterReference>ObjectName </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>String</languageKeyword> value that specifies the name of the object for which to specify the owner.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <parameterReference>ObjectType </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">ObjectTypeEnum</legacyLink> constants that specifies the owner type.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <parameterReference>OwnerName </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">A <languageKeyword>String</languageKeyword> value that specifies the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> of the <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> or <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> to own the object.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <parameterReference>ObjectTypeId </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> value that specifies the GUID for a provider object type that is not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> This parameter is required if <parameterReference>ObjectType</parameterReference> is set to <legacyBold>adPermObjProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">An error will occur if the provider does not support specifying object owners.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e44ec3d4-42ae-447d-aaed-bdea53cb0cca">GetObjectOwner and SetObjectOwner Methods Example (VB)</link>
        <link xlink:href="8965adf0-9075-4125-8142-73eb700029c3">GetObjectOwner Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
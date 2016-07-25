---
title: "GetObjectOwner Method (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8965adf0-9075-4125-8142-73eb700029c3
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
# GetObjectOwner Method (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0eef7800c16fb1e093d00ae8f594273a" id="tgt1" class="tgtSentence">Returns the owner of an object in a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Owner </parameterReference>
          <legacyBold>= </legacyBold>
          <parameterReference>Catalog</parameterReference>
          <legacyBold>.GetObjectOwner(</legacyBold>
          <parameterReference>ObjectName</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>ObjectType </parameterReference>[<legacyBold>,</legacyBold><parameterReference>ObjectTypeId</parameterReference>]<legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="4061387c7383a39e99e834d8722b398c" id="tgt2" class="tgtSentence">Returns a <legacyBold>String</legacyBold> value that specifies the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> of the <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> or <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> that owns the object.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="e6eedf795e5b271037f8285ec57d32dc" id="tgt3" class="tgtSentence"> <legacyItalic>ObjectName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ff092b04a12b003d5855185221576791" id="tgt4" class="tgtSentence">A <legacyBold>String</legacyBold> value that specifies the name of the object for which to return the owner.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="1aa7fc5833ed0d3d844dc29609c26c51" id="tgt5" class="tgtSentence"> <legacyItalic>ObjectType</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="9f734b251da32394f58f13638ac02747" id="tgt6" class="tgtSentence">A <legacyBold>Long</legacyBold> value which can be one of the <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">ObjectTypeEnum</legacyLink> constants, that specifies the type of the object for which to get the owner.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a100c95b6f2fff51fc742a727922e714" id="tgt7" class="tgtSentence"> <legacyItalic>ObjectTypeId</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt8" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="0aed8add3f14987994104b5d25445b52" id="tgt9" class="tgtSentence"> A <legacyBold>Variant</legacyBold> value that specifies the GUID for a provider object type not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence sentenceid="0eb29ae899fa11463c60db8a0c12dbbe" id="tgt10" class="tgtSentence"> This parameter is required if <legacyItalic>ObjectType</legacyItalic> is set to <legacyBold>adPermObjProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="8129b5fbca7f7fef054dc3b96d4a101e" id="tgt11" class="tgtSentence">An error will occur if the provider does not support returning object owners.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e44ec3d4-42ae-447d-aaed-bdea53cb0cca">GetObjectOwner and SetObjectOwner Methods Example (VB)</link>
        <link xlink:href="e5170a37-9d6e-43db-bfb6-9b6631fa3048">SetObjectOwner Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Returns the owner of an object in a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>Owner </parameterReference>
          <legacyBold>= </legacyBold>
          <parameterReference>Catalog</parameterReference>
          <legacyBold>.GetObjectOwner(</legacyBold>
          <parameterReference>ObjectName</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>ObjectType </parameterReference>[<legacyBold>,</legacyBold><parameterReference>ObjectTypeId</parameterReference>]<legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <legacyBold>String</legacyBold> value that specifies the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> of the <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> or <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink> that owns the object.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>ObjectName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A <legacyBold>String</legacyBold> value that specifies the name of the object for which to return the owner.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <legacyItalic>ObjectType</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A <legacyBold>Long</legacyBold> value which can be one of the <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">ObjectTypeEnum</legacyLink> constants, that specifies the type of the object for which to get the owner.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <legacyItalic>ObjectTypeId</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> A <legacyBold>Variant</legacyBold> value that specifies the GUID for a provider object type not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> This parameter is required if <legacyItalic>ObjectType</legacyItalic> is set to <legacyBold>adPermObjProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">An error will occur if the provider does not support returning object owners.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e44ec3d4-42ae-447d-aaed-bdea53cb0cca">GetObjectOwner and SetObjectOwner Methods Example (VB)</link>
        <link xlink:href="e5170a37-9d6e-43db-bfb6-9b6631fa3048">SetObjectOwner Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
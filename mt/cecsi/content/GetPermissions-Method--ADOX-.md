---
title: "GetPermissions Method (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: df201c1f-c76a-465d-98f0-83b7fc36e6e3
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
# GetPermissions Method (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0ae51d035ec5f9621195d8530fbc4669" id="tgt1" class="tgtSentence">Returns the permissions for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">group</legacyLink> or <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">user</legacyLink> on an object or object container.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>ReturnValue</parameterReference>
          <legacyBold>=</legacyBold>
          <parameterReference>GroupOrUser</parameterReference>
          <legacyBold>.GetPermissions(</legacyBold>
          <parameterReference>Name</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference> ObjectType    </parameterReference>[<legacyBold>,</legacyBold><parameterReference>ObjectTypeId</parameterReference>]<legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="dff08017e90d4f113d1e1fde9083c148" id="tgt2" class="tgtSentence">Returns a <languageKeyword>Long</languageKeyword> value that specifies a bitmask containing the permissions that the group or user has on the object.</caps:sentence>
            <caps:sentence sentenceid="3bc82a43cdd6634cbba2a6ba2964c900" id="tgt3" class="tgtSentence"> This value can be one or more of the <legacyLink xlink:href="55ee67c7-a583-42aa-849a-78264b4cb614">RightsEnum</legacyLink> constants.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="22b7f4e9e8916e9f600d9de7d2dbc303" id="tgt4" class="tgtSentence"> <parameterReference>Name </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="41b41d6413e629e61719b3364e20d6ef" id="tgt5" class="tgtSentence">A <languageKeyword>Variant</languageKeyword> value that specifies the name of the object for which to set permissions.</caps:sentence>
                <caps:sentence sentenceid="05a850997b500fc4962eb9d4a6866fdb" id="tgt6" class="tgtSentence"> Set <parameterReference>Name</parameterReference> to a null value if you want to get the permissions for the object container.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a068fbafa8e7b1855906ec04c64f2094" id="tgt7" class="tgtSentence"> <parameterReference>ObjectType </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="88c83fb2e828848c9389cc48f1b344e0" id="tgt8" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">ObjectTypeEnum</legacyLink> constants, that specifies the type of the object for which to get permissions.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e4719a6e71a5f7e279f5954e67b99392" id="tgt9" class="tgtSentence"> <parameterReference>ObjectTypeId </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt10" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="547be508dbe48988dd849aaf77ebaeec" id="tgt11" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> value that specifies the GUID for a provider object type not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence sentenceid="21900920cef00f532764b9e5b0bd7c68" id="tgt12" class="tgtSentence"> This parameter is required if <parameterReference>ObjectType</parameterReference> is set to <legacyBold>adPermObjProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt13" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group Object (ADOX)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object (ADOX)</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="aa366d98-8c7a-4189-bdd8-1d663b243d33">GetPermissions and SetPermissions Methods Example (VB)</link>
        <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property</link>
        <link xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Returns the permissions for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">group</legacyLink> or <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">user</legacyLink> on an object or object container.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>ReturnValue</parameterReference>
          <legacyBold>=</legacyBold>
          <parameterReference>GroupOrUser</parameterReference>
          <legacyBold>.GetPermissions(</legacyBold>
          <parameterReference>Name</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference> ObjectType    </parameterReference>[<legacyBold>,</legacyBold><parameterReference>ObjectTypeId</parameterReference>]<legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Returns a <languageKeyword>Long</languageKeyword> value that specifies a bitmask containing the permissions that the group or user has on the object.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> This value can be one or more of the <legacyLink xlink:href="55ee67c7-a583-42aa-849a-78264b4cb614">RightsEnum</legacyLink> constants.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <parameterReference>Name </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">A <languageKeyword>Variant</languageKeyword> value that specifies the name of the object for which to set permissions.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> Set <parameterReference>Name</parameterReference> to a null value if you want to get the permissions for the object container.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src7" class="srcSentence"> <parameterReference>ObjectType </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src8" class="srcSentence">A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">ObjectTypeEnum</legacyLink> constants, that specifies the type of the object for which to get permissions.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src9" class="srcSentence"> <parameterReference>ObjectTypeId </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src10" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> value that specifies the GUID for a provider object type not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> This parameter is required if <parameterReference>ObjectType</parameterReference> is set to <legacyBold>adPermObjProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group Object (ADOX)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object (ADOX)</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="aa366d98-8c7a-4189-bdd8-1d663b243d33">GetPermissions and SetPermissions Methods Example (VB)</link>
        <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property</link>
        <link xlink:href="b7f925d7-b05c-4376-bb49-f8d2c17b8b24">SetPermissions Method</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
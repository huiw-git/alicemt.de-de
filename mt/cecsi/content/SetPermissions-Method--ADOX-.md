---
title: "SetPermissions Method (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b7f925d7-b05c-4376-bb49-f8d2c17b8b24
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
# SetPermissions Method (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2c66ed24fe414a2de7cb76645e7fbbcd" id="tgt1" class="tgtSentence">Specifies the permissions for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">group</legacyLink> or <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">user</legacyLink> on an object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
GroupOrUser.SetPermissions Name, ObjectType, Action, Rights [, Inherit] [, ObjectTypeId]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="22b7f4e9e8916e9f600d9de7d2dbc303" id="tgt2" class="tgtSentence"> <parameterReference>Name </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="0055d0e3c0ffb7e008abe5a2cd9206a6" id="tgt3" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that specifies the name of the object for which to set permissions.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a068fbafa8e7b1855906ec04c64f2094" id="tgt4" class="tgtSentence"> <parameterReference>ObjectType </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="88c83fb2e828848c9389cc48f1b344e0" id="tgt5" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">ObjectTypeEnum</legacyLink> constants, that specifies the type of the object for which to get permissions.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f449d23b847f366aba7b02fd745b44b6" id="tgt6" class="tgtSentence"> <parameterReference>Action </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="a835044f74cfb977585d1bbc525fc29a" id="tgt7" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="f948febd-c885-4621-823b-421e116fec4e">ActionEnum</legacyLink> constants that specifies the type of action to perform when setting permissions.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e829a59e305e26250b522c8cc2315763" id="tgt8" class="tgtSentence"> <parameterReference>Rights </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5758105a0a3759216dc1e0ef3188722d" id="tgt9" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value which can be a bitmask of one or more of the <legacyLink xlink:href="55ee67c7-a583-42aa-849a-78264b4cb614">RightsEnum</legacyLink> constants, that indicates the rights to set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="fa206625a73161ec49a592cad733c4ef" id="tgt10" class="tgtSentence"> <parameterReference>Inherit </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt11" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="b92fcbf969fb2e473f94d1e70a3357ee" id="tgt12" class="tgtSentence"> A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="c2f6ce79-c4b3-4d40-ac95-21025208f991">InheritTypeEnum</legacyLink> constants, that specifies how objects will inherit these permissions.</caps:sentence>
                <caps:sentence sentenceid="3d5ea7b02c78735582b1011b929643f1" id="tgt13" class="tgtSentence"> The default value is <legacyBold>adInheritNone</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="e4719a6e71a5f7e279f5954e67b99392" id="tgt14" class="tgtSentence"> <parameterReference>ObjectTypeId </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt15" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="cb52fefc710a547ea2098e6e63a13813" id="tgt16" class="tgtSentence"> A <languageKeyword>Variant</languageKeyword> value that specifies the GUID for a provider object type that is not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence sentenceid="21900920cef00f532764b9e5b0bd7c68" id="tgt17" class="tgtSentence"> This parameter is required if <parameterReference>ObjectType</parameterReference> is set to <legacyBold>adPermObjProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="2fb824f52a465548a2beef6881c694a2" id="tgt18" class="tgtSentence">An error will occur if the provider does not support setting access rights for groups or users.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="81d932355eb229c43514231aae62d426" id="tgt19" class="tgtSentence">When calling <legacyBold>SetPermissions</legacyBold>, setting Actions to <legacyBold>adAccessRevoke</legacyBold> overrides any settings of the <parameterReference>Rights</parameterReference> parameter.</caps:sentence>
              <caps:sentence sentenceid="bbfcaf7ab4fd473dc98057e9340a0c69" id="tgt20" class="tgtSentence"> Do not set <parameterReference>Actions</parameterReference> to <legacyBold>adAccessRevoke</legacyBold> if you want the rights specified in the <parameterReference>Rights</parameterReference> parameter to take effect.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt21" class="tgtSentence">Applies To</caps:sentence>
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
        <link xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions Method</link>
        <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies the permissions for a <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">group</legacyLink> or <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">user</legacyLink> on an object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
GroupOrUser.SetPermissions Name, ObjectType, Action, Rights [, Inherit] [, ObjectTypeId]</legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <parameterReference>Name </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>String</languageKeyword> value that specifies the name of the object for which to set permissions.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <parameterReference>ObjectType </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="3fdecfca-aa91-4596-ad98-610f1b7f840b">ObjectTypeEnum</legacyLink> constants, that specifies the type of the object for which to get permissions.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <parameterReference>Action </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="f948febd-c885-4621-823b-421e116fec4e">ActionEnum</legacyLink> constants that specifies the type of action to perform when setting permissions.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <parameterReference>Rights </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">A <languageKeyword>Long</languageKeyword> value which can be a bitmask of one or more of the <legacyLink xlink:href="55ee67c7-a583-42aa-849a-78264b4cb614">RightsEnum</legacyLink> constants, that indicates the rights to set.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src10" class="srcSentence"> <parameterReference>Inherit </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src11" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> A <languageKeyword>Long</languageKeyword> value which can be one of the <legacyLink xlink:href="c2f6ce79-c4b3-4d40-ac95-21025208f991">InheritTypeEnum</legacyLink> constants, that specifies how objects will inherit these permissions.</caps:sentence>
                <caps:sentence id="src13" class="srcSentence"> The default value is <legacyBold>adInheritNone</legacyBold>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src14" class="srcSentence"> <parameterReference>ObjectTypeId </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src15" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> A <languageKeyword>Variant</languageKeyword> value that specifies the GUID for a provider object type that is not defined by the OLE DB specification.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> This parameter is required if <parameterReference>ObjectType</parameterReference> is set to <legacyBold>adPermObjProviderSpecific</legacyBold>; otherwise, it is not used.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src18" class="srcSentence">An error will occur if the provider does not support setting access rights for groups or users.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src19" class="srcSentence">When calling <legacyBold>SetPermissions</legacyBold>, setting Actions to <legacyBold>adAccessRevoke</legacyBold> overrides any settings of the <parameterReference>Rights</parameterReference> parameter.</caps:sentence>
              <caps:sentence id="src20" class="srcSentence"> Do not set <parameterReference>Actions</parameterReference> to <legacyBold>adAccessRevoke</legacyBold> if you want the rights specified in the <parameterReference>Rights</parameterReference> parameter to take effect.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src21" class="srcSentence">Applies To</caps:sentence>
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
        <link xlink:href="df201c1f-c76a-465d-98f0-83b7fc36e6e3">GetPermissions Method</link>
        <link xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name Property</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
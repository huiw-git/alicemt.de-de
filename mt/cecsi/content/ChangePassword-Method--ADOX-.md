---
title: "ChangePassword Method (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d187fbc6-5fac-4abb-803d-bf344dcf0302
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
# ChangePassword Method (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="136c9dfb19c46fd66e76fcb5aca6cd4c" id="tgt1" class="tgtSentence">Changes the password for a <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">user</legacyLink> account.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>User</parameterReference>
          <legacyBold>.ChangePassword </legacyBold>
          <parameterReference>OldPassword</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>NewPassword</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="d8c02888ff63f34eff775f21148fe380" id="tgt2" class="tgtSentence"> <parameterReference>OldPassword </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="774134b6378ac0a63f0ba5f275bf0ccd" id="tgt3" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that specifies the user's existing password.</caps:sentence>
                <caps:sentence sentenceid="af1c221ce2a6eebd4ed6317146576c83" id="tgt4" class="tgtSentence"> If the user doesn't currently have a password, use an empty string ("") for <parameterReference>OldPassword</parameterReference>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="cda361802e0990b73108dd9b492d4cde" id="tgt5" class="tgtSentence"> <parameterReference>NewPassword </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="00830f7ad36118b9e146b91ab089975e" id="tgt6" class="tgtSentence">A <languageKeyword>String</languageKeyword> value that specifies the new password.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="d17c4f96d73f28ba5750a2770cbe2639" id="tgt7" class="tgtSentence">For security reasons, the old password must be specified in addition to the new password.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="c0ad7006d21146e512dd2ce9a72b0637" id="tgt8" class="tgtSentence">An error will occur if the provider does not support the administration of trustee properties.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt9" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c9426757-9cdd-4a95-b506-d3d011569109">Groups and Users Append, ChangePassword Methods Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Changes the password for a <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">user</legacyLink> account.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>User</parameterReference>
          <legacyBold>.ChangePassword </legacyBold>
          <parameterReference>OldPassword</parameterReference>
          <legacyBold>,</legacyBold>
          <parameterReference>NewPassword</parameterReference>
        </legacySyntax>
      </syntaxSection>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src2" class="srcSentence"> <parameterReference>OldPassword </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src3" class="srcSentence">A <languageKeyword>String</languageKeyword> value that specifies the user's existing password.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> If the user doesn't currently have a password, use an empty string ("") for <parameterReference>OldPassword</parameterReference>.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src5" class="srcSentence"> <parameterReference>NewPassword </parameterReference></caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src6" class="srcSentence">A <languageKeyword>String</languageKeyword> value that specifies the new password.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">For security reasons, the old password must be specified in addition to the new password.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">An error will occur if the provider does not support the administration of trustee properties.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object (ADOX)</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="c9426757-9cdd-4a95-b506-d3d011569109">Groups and Users Append, ChangePassword Methods Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
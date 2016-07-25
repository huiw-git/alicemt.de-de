---
title: "Charset Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e42507cb-9b46-4ce4-8191-2948eaf14ca2
caps.latest.revision: 15
caps.handback.revision: 15
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
# Charset Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b382555f6e4935f791702ff3c02889d6" id="tgt1" class="tgtSentence">Indicates the character set into which the contents of a text <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> should be translated for storage in the internal buffer of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ae04bc508f6e493805f86fc160e8082b" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that specifies the character set into which the contents of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> will be translated.</caps:sentence>
            <caps:sentence sentenceid="d43f5e685a01fed59a03ad021ba68955" id="tgt4" class="tgtSentence"> The default value is <legacyBold>Unicode</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="1e6ae33752b892745784dcb1c7b852ec" id="tgt5" class="tgtSentence"> Allowed values are typical strings passed over the interface as Internet character set names (for example, "iso-8859-1", "Windows-1252", and so on).</caps:sentence>
            <caps:sentence sentenceid="a9f74ffff7f3dda93ad032bcfc06456c" id="tgt6" class="tgtSentence"> For a list of the character set names that are known by a system, see the subkeys of HKEY_CLASSES_ROOT\MIME\Database\Charset in the Windows Registry.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="34c5fd4f1ba34a19dbc5270a7b0c2a7b" id="tgt7" class="tgtSentence">In a text <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object, text data is stored in the character set specified by the <unmanagedCodeEntityReference>Charset</unmanagedCodeEntityReference> property.</caps:sentence>
            <caps:sentence sentenceid="05f49f9810346c10b954d773dc9f34b4" id="tgt8" class="tgtSentence"> The default is Unicode.</caps:sentence>
            <caps:sentence sentenceid="f4def6288d14c8de628f3ee75b37141a" id="tgt9" class="tgtSentence"> The <unmanagedCodeEntityReference>Charset</unmanagedCodeEntityReference> property is used for converting data going into the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> or coming out of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence sentenceid="ee13e35a0dc16916c0c9740a7b08af5c" id="tgt10" class="tgtSentence"> For example, if the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> contains ISO-8859-1 data and that data is copied to a BSTR, the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object will convert the data to Unicode.</caps:sentence>
            <caps:sentence sentenceid="f8d8dfe9b202c48fe9bd863cf9d50b42" id="tgt11" class="tgtSentence"> The reverse is also true.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5006eb00d06ed6a5190a09d480c32fc4" id="tgt12" class="tgtSentence">For an open <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>, the current <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> must be at the beginning of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> (0) to be able to set <unmanagedCodeEntityReference>Charset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="609e0a5bc3f98e615d9996a4d2d7d3b0" id="tgt13" class="tgtSentence">
              <unmanagedCodeEntityReference>Charset</unmanagedCodeEntityReference> is used only with text <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> objects (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
            <caps:sentence sentenceid="a59a78d99cf53770ec7f0fc575820095" id="tgt14" class="tgtSentence"> This property is ignored if <unmanagedCodeEntityReference>Type</unmanagedCodeEntityReference> is <legacyBold>adTypeBinary</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a0b0e26a51a4e538a05918e920044966" id="tgt15" class="tgtSentence">For a code sample, see <link xlink:href="cb4273e2-c907-4a86-a621-3bf110088228">Step 4: Populate the Details Text Box</link>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt16" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the character set into which the contents of a text <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> should be translated for storage in the internal buffer of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value that specifies the character set into which the contents of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> will be translated.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>Unicode</legacyBold>.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Allowed values are typical strings passed over the interface as Internet character set names (for example, "iso-8859-1", "Windows-1252", and so on).</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> For a list of the character set names that are known by a system, see the subkeys of HKEY_CLASSES_ROOT\MIME\Database\Charset in the Windows Registry.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">In a text <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object, text data is stored in the character set specified by the <unmanagedCodeEntityReference>Charset</unmanagedCodeEntityReference> property.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> The default is Unicode.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The <unmanagedCodeEntityReference>Charset</unmanagedCodeEntityReference> property is used for converting data going into the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> or coming out of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> For example, if the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> contains ISO-8859-1 data and that data is copied to a BSTR, the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> object will convert the data to Unicode.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> The reverse is also true.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">For an open <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference>, the current <legacyLink xlink:href="daa8319a-49aa-4c1c-9af6-0b01e9ab2f9d">Position</legacyLink> must be at the beginning of the <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> (0) to be able to set <unmanagedCodeEntityReference>Charset</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">
              <unmanagedCodeEntityReference>Charset</unmanagedCodeEntityReference> is used only with text <unmanagedCodeEntityReference>Stream</unmanagedCodeEntityReference> objects (<legacyLink xlink:href="f6a17e8c-7a28-48d0-bded-76b9e0cf7639">Type</legacyLink> is <legacyBold>adTypeText</legacyBold>).</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> This property is ignored if <unmanagedCodeEntityReference>Type</unmanagedCodeEntityReference> is <legacyBold>adTypeBinary</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">For a code sample, see <link xlink:href="cb4273e2-c907-4a86-a621-3bf110088228">Step 4: Populate the Details Text Box</link>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
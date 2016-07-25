---
title: "Name Property (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 81b92baf-b6b9-4f4e-9f33-4503795518cd
caps.latest.revision: 12
caps.handback.revision: 12
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
# Name Property (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="865eccf161347b31e2599e9f5ea8d288" id="tgt1" class="tgtSentence">Indicates the name of the object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="95c701ec7ef8444399749df7594c0234" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>String</languageKeyword> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="69a6d5dac33cbe84468cc46b5d7c3385" id="tgt4" class="tgtSentence">Names do not have to be unique within a collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b6fcc3540e6bab6d0cfbf51359a620f1" id="tgt5" class="tgtSentence">The <legacyBold>Name</legacyBold> property is read/write on <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink>, <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink>, <legacyLink xlink:href="55f116fe-4d56-4892-bffe-0cdd6fc727c9">Key</legacyLink>, <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink>, <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink>, and <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> objects.</caps:sentence>
            <caps:sentence sentenceid="06e19a7415ec358c32bc73c0be8de167" id="tgt6" class="tgtSentence"> The <legacyBold>Name</legacyBold> property is read-only on <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>, <legacyLink xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure</legacyLink>, and <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="85db013f96daa9fab800a63daf5959ec" id="tgt7" class="tgtSentence">For read/write objects (<legacyBold>Column</legacyBold>, <legacyBold>Group</legacyBold>, <legacyBold>Key</legacyBold>, <legacyBold>Index</legacyBold>, <legacyBold>Table</legacyBold> and <legacyBold>User</legacyBold> objects), the default value is an empty string ("").</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="0c7772d194f12b35e6156872cefdccb1" id="tgt8" class="tgtSentence">For keys, this property is read-only on <legacyBold>Key</legacyBold> objects already appended to a collection.</caps:sentence>
              <caps:sentence sentenceid="2d42c0ea8e2a561680c92f918e495741" id="tgt9" class="tgtSentence"> For tables, this property is read-only for <legacyBold>Table</legacyBold> objects already appended to a collection.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt10" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="55f116fe-4d56-4892-bffe-0cdd6fc727c9">Key Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the name of the object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>String</languageKeyword> value.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Names do not have to be unique within a collection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">The <legacyBold>Name</legacyBold> property is read/write on <legacyLink xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column</legacyLink>, <legacyLink xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group</legacyLink>, <legacyLink xlink:href="55f116fe-4d56-4892-bffe-0cdd6fc727c9">Key</legacyLink>, <legacyLink xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index</legacyLink>, <legacyLink xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table</legacyLink>, and <legacyLink xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User</legacyLink> objects.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> The <legacyBold>Name</legacyBold> property is read-only on <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink>, <legacyLink xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure</legacyLink>, and <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">For read/write objects (<legacyBold>Column</legacyBold>, <legacyBold>Group</legacyBold>, <legacyBold>Key</legacyBold>, <legacyBold>Index</legacyBold>, <legacyBold>Table</legacyBold> and <legacyBold>User</legacyBold> objects), the default value is an empty string ("").</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src8" class="srcSentence">For keys, this property is read-only on <legacyBold>Key</legacyBold> objects already appended to a collection.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> For tables, this property is read-only for <legacyBold>Table</legacyBold> objects already appended to a collection.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="6e772783-1bc8-4ea7-94b2-7d7a52ea5c47">Column Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="55ef0ade-68ea-4da5-8aa5-4cd27d1f6d1e">Group Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="6b9578c0-bc94-46b9-b801-c18e14b04b31">Index Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="55f116fe-4d56-4892-bffe-0cdd6fc727c9">Key Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">Property Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
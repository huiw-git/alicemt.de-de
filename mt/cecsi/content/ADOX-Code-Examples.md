---
title: "ADOX Code Examples"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 438e4369-f7e8-4dca-a709-dd501a3ca83f
caps.latest.revision: 8
caps.handback.revision: 8
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
# ADOX Code Examples
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f1cc52c5dd34b463be15cf6a3a35507e" id="tgt1" class="tgtSentence">Use the following code examples to learn how to use the ADOX objects, methods, properties, and events.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="60112f1437485d0ce0860afad2afc9f3" id="tgt2" class="tgtSentence">Paste the entire code example into your code editor.</caps:sentence>
              <caps:sentence sentenceid="d0af02b2a7f5e8d60d6ca45d510c2f3c" id="tgt3" class="tgtSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="ed072a35-e1ae-4cf9-b8d2-0db1e32641fa">
                  <caps:sentence sentenceid="ba8c9b4dccb059eae464098d8236bbdb" id="tgt4" class="tgtSentence">ADOX Code Examples in Microsoft Visual Basic</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="b63ec31e-488c-4677-ab58-01371015e692">
                  <caps:sentence sentenceid="e2f46b5ea43a675c80fe8ddf56e15f36" id="tgt5" class="tgtSentence">ADOX Code Examples in Microsoft Visual C++</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="413263a8-05c0-4404-929d-69f82b987ba3">Command and CommandText Properties Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="aa366d98-8c7a-4189-bdd8-1d663b243d33">GetPermissions and SetPermissions Methods Example (VB)</link>
        <link xlink:href="50f87e27-1bf9-427c-9b1d-704a672434d2">Indexes Append Method Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">Microsoft ADOX Programmer's Reference</link>
        <link xlink:href="7df1089e-69b7-476e-9244-19947c087351">Parameters Collection, Command Property Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="499679bd-287b-487d-bdfb-3803abffec1c">Procedures Refresh Method Example (VB)</link>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
        <link xlink:href="cdad2d66-6ade-40dc-9e74-e40cfa9bc127">Views Refresh Method Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the following code examples to learn how to use the ADOX objects, methods, properties, and events.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <alert class="note">
            <para>
              <caps:sentence id="src2" class="srcSentence">Paste the entire code example into your code editor.</caps:sentence>
              <caps:sentence id="src3" class="srcSentence"> The example may not run correctly if partial examples are used or if paragraph formatting is lost.</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="ed072a35-e1ae-4cf9-b8d2-0db1e32641fa">
                  <caps:sentence id="src4" class="srcSentence">ADOX Code Examples in Microsoft Visual Basic</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="b63ec31e-488c-4677-ab58-01371015e692">
                  <caps:sentence id="src5" class="srcSentence">ADOX Code Examples in Microsoft Visual C++</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bb3274b1-764d-43a7-a49f-ef55680ecd26">Catalog ActiveConnection Property Example (VB)</link>
        <link xlink:href="678e5546-df5d-4cd0-bfe9-6cf13cb385c0">Columns and Tables Append Methods, Name Property Example (VB)</link>
        <link xlink:href="413263a8-05c0-4404-929d-69f82b987ba3">Command and CommandText Properties Example (VB)</link>
        <link xlink:href="f88e7a3b-19ed-46e2-b2ce-3b611d9b8166">Connection Close Method, Table Type Property Example (VB)</link>
        <link xlink:href="aa366d98-8c7a-4189-bdd8-1d663b243d33">GetPermissions and SetPermissions Methods Example (VB)</link>
        <link xlink:href="50f87e27-1bf9-427c-9b1d-704a672434d2">Indexes Append Method Example (VB)</link>
        <link xlink:href="13b5b1c3-6af6-439e-bb65-976578ba6bc2">Keys Append Method, Key Type, RelatedColumn, RelatedTable and UpdateRule Properties Example (VB)</link>
        <link xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">Microsoft ADOX Programmer's Reference</link>
        <link xlink:href="7df1089e-69b7-476e-9244-19947c087351">Parameters Collection, Command Property Example (VB)</link>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="499679bd-287b-487d-bdfb-3803abffec1c">Procedures Refresh Method Example (VB)</link>
        <link xlink:href="d8304849-3f80-4cf3-9425-529d2a8ebedd">Views and Fields Collections Example (VB)</link>
        <link xlink:href="b5b4c082-ac29-4f49-a8b8-e21b554c9b0d">Views Append Method Example (VB)</link>
        <link xlink:href="a05a0190-352d-44ff-9488-0c94e9fb656e">Views Collection, CommandText Property Example (VB)</link>
        <link xlink:href="17df2a83-4166-4df8-8c17-0a33aaac8582">Views Delete Method Example (VB)</link>
        <link xlink:href="cdad2d66-6ade-40dc-9e74-e40cfa9bc127">Views Refresh Method Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ParentCatalog Property (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: a0bb2ed8-d4cb-4f92-8de7-769bbe0e6273
caps.latest.revision: 14
caps.handback.revision: 14
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
# ParentCatalog Property (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c7f716847ac7642f09feebdf78e2c014" id="tgt1" class="tgtSentence">Specifies the parent catalog of a Table, User, or Column object to provide access to provider-specific properties.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="62e296f7fde65ab93feeac1157dc5d16" id="tgt3" class="tgtSentence">Sets and returns a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> object.</caps:sentence>
            <caps:sentence sentenceid="2dac2da61a53d7eb419f1fc9e06284c2" id="tgt4" class="tgtSentence"> Setting <unmanagedCodeEntityReference>ParentCatalog</unmanagedCodeEntityReference> to an open <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> allows access to provider-specific properties prior to appending a table or column to a <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> collection.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="524c2835122eb71533a824f2bcf1cdde" id="tgt5" class="tgtSentence">Some data providers allow provider-specific property values to be written only at creation: that is, when a table or column is appended to its <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> collection.</caps:sentence>
            <caps:sentence sentenceid="56eed899e6b42377925d628fa09d518a" id="tgt6" class="tgtSentence"> To access these properties before appending these objects to a <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference>, specify the <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> in the <unmanagedCodeEntityReference>ParentCatalog</unmanagedCodeEntityReference> property first.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f31d661bd11a4e656aabfbdc399e6741" id="tgt7" class="tgtSentence">An error occurs when the table or column is appended to a different <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> than the <unmanagedCodeEntityReference>ParentCatalog</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt8" class="tgtSentence">Applies To</caps:sentence>
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
                    <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object (ADOX)</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies the parent catalog of a Table, User, or Column object to provide access to provider-specific properties.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets and returns a <legacyLink xlink:href="bb651639-a488-4e38-b6de-0ed99fa4dd92">Catalog</legacyLink> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Setting <unmanagedCodeEntityReference>ParentCatalog</unmanagedCodeEntityReference> to an open <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> allows access to provider-specific properties prior to appending a table or column to a <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> collection.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Some data providers allow provider-specific property values to be written only at creation: that is, when a table or column is appended to its <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> collection.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> To access these properties before appending these objects to a <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference>, specify the <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> in the <unmanagedCodeEntityReference>ParentCatalog</unmanagedCodeEntityReference> property first.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">An error occurs when the table or column is appended to a different <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> than the <unmanagedCodeEntityReference>ParentCatalog</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Applies To</caps:sentence>
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
                    <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="f68e32ce-ef7c-407d-bdb5-d280947ae0e2">User Object (ADOX)</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="448bc850-7584-4c5f-89f3-5f4fee88b259">ParentCatalog Property Example (VB)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
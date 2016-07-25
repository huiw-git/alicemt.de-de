---
title: "DateCreated Property (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 2bf4b00d-045c-444e-8af7-8af6297ed418
caps.latest.revision: 10
caps.handback.revision: 10
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
# DateCreated Property (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a6db6a1be9201ec3f1d3b7e7b46104dc" id="tgt1" class="tgtSentence">Indicates the date the object was created.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4d354fa601a7e22a163f41084b5a0b77" id="tgt2" class="tgtSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d611ca1c625897b420e81a7c115c2884" id="tgt3" class="tgtSentence">Returns a <languageKeyword>Variant</languageKeyword> value specifying the date created.</caps:sentence>
            <caps:sentence sentenceid="dfb254354de76225d89707d3db6d1283" id="tgt4" class="tgtSentence"> The value is null if <unmanagedCodeEntityReference>DateCreated</unmanagedCodeEntityReference> is not supported by the provider.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="384ccb2fd0d89fe528555cf674eeaed8" id="tgt5" class="tgtSentence">The <unmanagedCodeEntityReference>DateCreated</unmanagedCodeEntityReference> property is null for newly appended objects.</caps:sentence>
            <caps:sentence sentenceid="efe86e5ae28c42e8f30018e815c24a35" id="tgt6" class="tgtSentence"> After appending a new <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> or <legacyLink xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure</legacyLink>, you must call the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method of the <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink> or <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink> collection to obtain values for the <unmanagedCodeEntityReference>DateCreated</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
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
        <link xlink:href="d608ea35-6e68-402f-8184-a5041e408678">DateCreated and DateModified Properties Example (VB)</link>
        <link xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the date the object was created.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <languageKeyword>Variant</languageKeyword> value specifying the date created.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The value is null if <unmanagedCodeEntityReference>DateCreated</unmanagedCodeEntityReference> is not supported by the provider.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The <unmanagedCodeEntityReference>DateCreated</unmanagedCodeEntityReference> property is null for newly appended objects.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> After appending a new <legacyLink xlink:href="653421ce-7b94-43d0-9bc6-4900f8f2af45">View</legacyLink> or <legacyLink xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure</legacyLink>, you must call the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method of the <legacyLink xlink:href="a55d380c-2b7b-4b57-af74-8ba0b3de0db9">Views</legacyLink> or <legacyLink xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures</legacyLink> collection to obtain values for the <unmanagedCodeEntityReference>DateCreated</unmanagedCodeEntityReference> property.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="927bcf3e-32f5-4a80-98d3-600779f0732e">Procedure Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="a6d74000-0828-49ba-850a-63da865f8802">Table Object</link>
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
        <link xlink:href="d608ea35-6e68-402f-8184-a5041e408678">DateCreated and DateModified Properties Example (VB)</link>
        <link xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
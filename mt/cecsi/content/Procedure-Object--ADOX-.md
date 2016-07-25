---
title: "Procedure Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 927bcf3e-32f5-4a80-98d3-600779f0732e
caps.latest.revision: 9
caps.handback.revision: 9
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
# Procedure Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ca0f2f4bcebebba752fe70358ddafcc5" id="tgt1" class="tgtSentence">Represents a stored procedure.</caps:sentence>
          <caps:sentence sentenceid="c01e3404dd5b9b8afd59c7b1f7c5cbb5" id="tgt2" class="tgtSentence"> When used in conjunction with the ADO <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object, the <legacyBold>Procedure</legacyBold> object can be used for adding, deleting, or modifying stored procedures.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="30f2f9515ce390b7f939fffc6d73161e" id="tgt3" class="tgtSentence">The <legacyBold>Procedure</legacyBold> object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ddfa0a06d79e79b9ae757beb4fbe6d79" id="tgt4" class="tgtSentence">With the properties of a <legacyBold>Procedure</legacyBold> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="47ff72388116dad2720fdfed6e48e32c" id="tgt5" class="tgtSentence">Identify the procedure with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed2c4ee2552f7a76875bfd07dd0fb690" id="tgt6" class="tgtSentence">Specify the ADO <legacyBold>Command</legacyBold> object that can be used to create or execute the procedure with the <legacyLink xlink:href="bcc9146f-586f-4e69-9c10-863440c9cffa">Command</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1f6ac71f5a656b23e407d68029eef914" id="tgt7" class="tgtSentence">Return date information with the <legacyLink xlink:href="2bf4b00d-045c-444e-8af7-8af6297ed418">DateCreated</legacyLink> and <legacyLink xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt8" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="2ef37ed66bcba3b3442a2f3ef513d24e" id="tgt9" class="tgtSentence">
                  <legacyLink xlink:href="522f6447-ba9e-45f5-a185-37b312e126d4">Procedure Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="413263a8-05c0-4404-929d-69f82b987ba3">Command and CommandText Properties Example (VB)</link>
        <link xlink:href="7df1089e-69b7-476e-9244-19947c087351">Parameters Collection, Command Property Example (VB)</link>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a stored procedure.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When used in conjunction with the ADO <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object, the <legacyBold>Procedure</legacyBold> object can be used for adding, deleting, or modifying stored procedures.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">The <legacyBold>Procedure</legacyBold> object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src4" class="srcSentence">With the properties of a <legacyBold>Procedure</legacyBold> object, you can:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src5" class="srcSentence">Identify the procedure with the <legacyLink xlink:href="81b92baf-b6b9-4f4e-9f33-4503795518cd">Name</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">Specify the ADO <legacyBold>Command</legacyBold> object that can be used to create or execute the procedure with the <legacyLink xlink:href="bcc9146f-586f-4e69-9c10-863440c9cffa">Command</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">Return date information with the <legacyLink xlink:href="2bf4b00d-045c-444e-8af7-8af6297ed418">DateCreated</legacyLink> and <legacyLink xlink:href="fed09266-1547-4bda-9088-c254d81cc738">DateModified</legacyLink> properties.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src8" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">
                  <legacyLink xlink:href="522f6447-ba9e-45f5-a185-37b312e126d4">Procedure Object Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="413263a8-05c0-4404-929d-69f82b987ba3">Command and CommandText Properties Example (VB)</link>
        <link xlink:href="7df1089e-69b7-476e-9244-19947c087351">Parameters Collection, Command Property Example (VB)</link>
        <link xlink:href="ce83b966-474b-4f57-8eb9-370996dfc5c0">Procedures Append Method Example (VB)</link>
        <link xlink:href="94f1ac93-e778-4a40-a85e-94bce5316ac7">Procedures Delete Method Example (VB)</link>
        <link xlink:href="dc7a38e1-93b9-4034-9af2-ff419e8fb2a3">Procedures Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
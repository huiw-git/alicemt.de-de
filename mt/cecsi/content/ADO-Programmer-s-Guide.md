---
title: "ADO Programmer&#39;s Guide"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e3c50eee-964a-4abd-810d-1bd51978e814
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
# ADO Programmer&#39;s Guide
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5fc90346d072a9915e32e1ad698e60d6" id="tgt1" class="tgtSentence">This documentation provides an overview of how to use ADO objects to work with data from various data sources.</caps:sentence>
          <caps:sentence sentenceid="d8037332296685702a47c5961a34c484" id="tgt2" class="tgtSentence"> First, the introduction summarizes the new features and the requirement for installing, using, and redistributing the ADO component.</caps:sentence>
          <caps:sentence sentenceid="922a2f534c5d901ebf7555874d0910ca" id="tgt3" class="tgtSentence"> The next sections discuss the use of the various types of ADO objects.</caps:sentence>
          <caps:sentence sentenceid="ba41465338b3180468b82a09cb3e4700" id="tgt4" class="tgtSentence"> Finally, the appendixes discuss various Microsoft-supplied data and service providers, error messages, and tips about how to use ADO in several programming languages, in addition to samples and a glossary.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt5" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="c5b3a134-de22-4e9c-9489-9a1cc7a5dcfa">
                <caps:sentence sentenceid="8800e1c9b3e22c44ba59a34db3fe4841" id="tgt6" class="tgtSentence">Introduction</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="8e9d52da-342d-46b5-8535-c57f07711db0">
                <caps:sentence sentenceid="d770cfd2e15e26ca8eba174ed0e7c4dc" id="tgt7" class="tgtSentence">ActiveX Data Objects (ADO)</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="63a5f26b-e7ca-47d9-a004-59eaad6052b4">
                <caps:sentence sentenceid="4e79de4fef3e0e14e424410a7b98c487" id="tgt8" class="tgtSentence">Remote Data Services (RDS)</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">
                <caps:sentence sentenceid="79a8924c226eec12a4e4f5759029b642" id="tgt9" class="tgtSentence">ADO (Multidimensional) (ADO MD)</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">
                <caps:sentence sentenceid="4a784aaf0e956196e92c3cf29c7ab139" id="tgt10" class="tgtSentence">ADO Extensions for Data Definition Language and Security (ADOX)</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="2e6417d6-442e-4539-9573-d1322328674a">
                <caps:sentence sentenceid="cd16a0aa211c6d9fc2c5b784fb7cb0d0" id="tgt11" class="tgtSentence">Appendixes</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This documentation provides an overview of how to use ADO objects to work with data from various data sources.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> First, the introduction summarizes the new features and the requirement for installing, using, and redistributing the ADO component.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The next sections discuss the use of the various types of ADO objects.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Finally, the appendixes discuss various Microsoft-supplied data and service providers, error messages, and tips about how to use ADO in several programming languages, in addition to samples and a glossary.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="c5b3a134-de22-4e9c-9489-9a1cc7a5dcfa">
                <caps:sentence id="src6" class="srcSentence">Introduction</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="8e9d52da-342d-46b5-8535-c57f07711db0">
                <caps:sentence id="src7" class="srcSentence">ActiveX Data Objects (ADO)</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="63a5f26b-e7ca-47d9-a004-59eaad6052b4">
                <caps:sentence id="src8" class="srcSentence">Remote Data Services (RDS)</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="75b774a5-fa94-490a-b521-b2b8f7d48919">
                <caps:sentence id="src9" class="srcSentence">ADO (Multidimensional) (ADO MD)</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="c6579b5b-a93e-48c5-8847-743fc4590cd2">
                <caps:sentence id="src10" class="srcSentence">ADO Extensions for Data Definition Language and Security (ADOX)</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
          <listItem>
            <para>
              <legacyLink xlink:href="2e6417d6-442e-4539-9573-d1322328674a">
                <caps:sentence id="src11" class="srcSentence">Appendixes</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "Property Object (ADOX)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6a56def6-dbe6-4ccc-a491-8d076889f019
caps.latest.revision: 5
caps.handback.revision: 5
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
# Property Object (ADOX)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d621722bd3e424a3e830bc02d032826f" id="tgt1" class="tgtSentence">Represents a characteristic of an ADOX object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4e8100275563646026d5d7dedfb9e9c7" id="tgt2" class="tgtSentence">ADOX objects have two types of properties: built-in and dynamic.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="320d0a9db275f9d3aa3ebbef8ad5bf43" id="tgt3" class="tgtSentence">Built-in properties are those properties immediately available to any new object, using the MyObject.Property syntax.</caps:sentence>
            <caps:sentence sentenceid="c7392a7993b42d7a8465aea88b2fc2cf" id="tgt4" class="tgtSentence"> They do not appear as Property objects in an object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties collection</legacyLink>, so although you can change their values, you cannot modify their characteristics.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9def65f203023ccd888ee28786f660b3" id="tgt5" class="tgtSentence">Dynamic properties are defined by the underlying data provider, and appear in the Properties collection for the appropriate ADOX object.</caps:sentence>
            <caps:sentence sentenceid="b034e6fd6b02189899b3b46322739247" id="tgt6" class="tgtSentence">  Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or MyObject.Properties("Name") syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1c08354a2624dc3b87b7587e5140890f" id="tgt7" class="tgtSentence">You cannot delete either kind of property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1c79a7bd2022fe520d6386050d19b212" id="tgt8" class="tgtSentence">A dynamic Property object has four built-in properties of its own: </caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3d54fbf7f193debf84ae3845e76a7524" id="tgt9" class="tgtSentence">The <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property is a string that identifies the property.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0cba58492f9d421691ba1fba46f68fcc" id="tgt10" class="tgtSentence">The <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> property is an integer that specifies the property data type.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="cff778310dbc75c463e56090fd03f09e" id="tgt11" class="tgtSentence">The <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property is a variant that contains the property setting.</caps:sentence>
            <caps:sentence sentenceid="bfe07174d7ebf1583d1133e60a3d9fca" id="tgt12" class="tgtSentence"> Value is the default property for a Property object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a48f251c1d41c3905b0e609c4d3ab04f" id="tgt13" class="tgtSentence">The <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property is a long value that indicates characteristics of the property specific to the provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt14" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="640780dc-5733-4f0c-9c11-6f43c1db5901">ADOX Property Object Properties, Methods, and Events</link>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Represents a characteristic of an ADOX object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">ADOX objects have two types of properties: built-in and dynamic.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">Built-in properties are those properties immediately available to any new object, using the MyObject.Property syntax.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> They do not appear as Property objects in an object's <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties collection</legacyLink>, so although you can change their values, you cannot modify their characteristics.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">Dynamic properties are defined by the underlying data provider, and appear in the Properties collection for the appropriate ADOX object.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence">  Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or MyObject.Properties("Name") syntax.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">You cannot delete either kind of property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">A dynamic Property object has four built-in properties of its own: </caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <legacyLink xlink:href="cfd0e29c-8310-44ab-85c3-5761184b865d">Name</legacyLink> property is a string that identifies the property.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">The <legacyLink xlink:href="8a4c079f-9f4f-4545-801d-85983b8db71e">Type</legacyLink> property is an integer that specifies the property data type.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">The <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property is a variant that contains the property setting.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Value is the default property for a Property object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">The <legacyLink xlink:href="acc15d40-68a6-4ba9-85bd-12d331aecaa6">Attributes</legacyLink> property is a long value that indicates characteristics of the property specific to the provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="640780dc-5733-4f0c-9c11-6f43c1db5901">ADOX Property Object Properties, Methods, and Events</link>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
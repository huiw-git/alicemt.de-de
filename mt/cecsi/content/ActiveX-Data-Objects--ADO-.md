---
title: "ActiveX Data Objects (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8e9d52da-342d-46b5-8535-c57f07711db0
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
# ActiveX Data Objects (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt1" class="tgtSentence">This section contains the following topics.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="d6a66928-e68f-4c38-b87a-838c5de50a28">
                  <caps:sentence sentenceid="822eb9bdef54b3a9f78e4c7cc7fb2a89" id="tgt2" class="tgtSentence">ADO Fundamentals</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="3931e7ec-f66b-4d5d-aad3-c4bf12e8b154">
                  <caps:sentence sentenceid="9eff6ae3d297609018777e196a66fcde" id="tgt3" class="tgtSentence">Getting Data</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="de1d74af-89b6-4f3f-a8c9-07c3e2b3c9a5">
                  <caps:sentence sentenceid="f8edb19297ca671f08928207f9450806" id="tgt4" class="tgtSentence">Examining Data</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="ef514f85-c446-4f05-824e-c9313b2ffae1">
                  <caps:sentence sentenceid="22324e42becabf3b33d445c021318efa" id="tgt5" class="tgtSentence">Editing Data</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">
                  <caps:sentence sentenceid="580ed48e16bfb4354226d58ed9c4cde6" id="tgt6" class="tgtSentence">Updating and Persisting Data</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="4909e413-f3b0-4183-8ad3-67b1434df742">
                  <caps:sentence sentenceid="db0b59b9623daf50a80d69cd1518a7d2" id="tgt7" class="tgtSentence">Error Handling</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="e9003457-0762-48b3-942f-0820266b158f">
                  <caps:sentence sentenceid="0bbf6125791e03ec409c682457a84486" id="tgt8" class="tgtSentence">Handling ADO Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="c1b7d7e6-1707-4ce2-863f-0c6dea967df6">
                  <caps:sentence sentenceid="43524e3b27592ce5306e908928c7d820" id="tgt9" class="tgtSentence">Understanding Cursors and Locks</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="62bd7dc9-45b5-4ca9-8b52-457325e0ce9e">
                  <caps:sentence sentenceid="585957d02507abe8ad4d8901c1b6a7e0" id="tgt10" class="tgtSentence">Data Shaping</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">
                  <caps:sentence sentenceid="df7ba41c46768831ede2a7018622bd04" id="tgt11" class="tgtSentence">Records and Streams</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This section contains the following topics.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="d6a66928-e68f-4c38-b87a-838c5de50a28">
                  <caps:sentence id="src2" class="srcSentence">ADO Fundamentals</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="3931e7ec-f66b-4d5d-aad3-c4bf12e8b154">
                  <caps:sentence id="src3" class="srcSentence">Getting Data</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="de1d74af-89b6-4f3f-a8c9-07c3e2b3c9a5">
                  <caps:sentence id="src4" class="srcSentence">Examining Data</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="ef514f85-c446-4f05-824e-c9313b2ffae1">
                  <caps:sentence id="src5" class="srcSentence">Editing Data</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="8dc27274-4f96-43d1-913c-4ff7d01b9a27">
                  <caps:sentence id="src6" class="srcSentence">Updating and Persisting Data</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="4909e413-f3b0-4183-8ad3-67b1434df742">
                  <caps:sentence id="src7" class="srcSentence">Error Handling</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="e9003457-0762-48b3-942f-0820266b158f">
                  <caps:sentence id="src8" class="srcSentence">Handling ADO Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="c1b7d7e6-1707-4ce2-863f-0c6dea967df6">
                  <caps:sentence id="src9" class="srcSentence">Understanding Cursors and Locks</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="62bd7dc9-45b5-4ca9-8b52-457325e0ce9e">
                  <caps:sentence id="src10" class="srcSentence">Data Shaping</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
            <listItem>
              <para>
                <legacyLink xlink:href="4d68868e-2611-4b5c-9a89-7caa5f753151">
                  <caps:sentence id="src11" class="srcSentence">Records and Streams</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
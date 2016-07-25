---
title: "Members Collection (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3a647cde-efdc-4394-b1b9-8cbb1b9d689f
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
# Members Collection (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="4070b517569207455c1e535a6a968e78" id="tgt1" class="tgtSentence">Contains the <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects from a level or a position along an axis.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="30241c4d86150f222de3795cc2f64572" id="tgt2" class="tgtSentence">A <legacyBold>Members</legacyBold> collection is used to contain the following types of members:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="58fd28cc4a8f56a4aa3fa3fc8affc860" id="tgt3" class="tgtSentence">The members that make up a level in a cube.</caps:sentence>
                <caps:sentence sentenceid="746f4a4d3fe733aadb4270f55c33c077" id="tgt4" class="tgtSentence"> These are contained in the <legacyBold>Members</legacyBold> collection of a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
                <caps:sentence sentenceid="e1f8584c1d5589f47583433e0249726a" id="tgt5" class="tgtSentence"> For example, using the sample from <legacyLink xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</legacyLink>, the four members of the Countries level are Canada, USA, UK, and Germany.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e68f08d57f5896a2e7b0b05a994badc0" id="tgt6" class="tgtSentence">The members that are the children of a specific member within a hierarchy.</caps:sentence>
                <caps:sentence sentenceid="adb9e860aa9150594b305777c045896f" id="tgt7" class="tgtSentence"> These members are returned by the <legacyLink xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children</legacyLink> property of the parent <legacyBold>Member</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="8bb15922c20198525bdef2ed7f2a41e7" id="tgt8" class="tgtSentence"> For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="59817581e085e1233478258862bbb9c0" id="tgt9" class="tgtSentence">The members that define a specific position along an axis of a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">cellset</legacyLink>.</caps:sentence>
                <caps:sentence sentenceid="344d65f32faf8c21bb94da1115309d9c" id="tgt10" class="tgtSentence"> Using the cellset from <legacyLink xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</legacyLink> as an example, the two members of the first position on the x-axis are Valentine and Seattle.</caps:sentence>
                <caps:sentence sentenceid="d521d6ff8547b4e7c18e70021a1c454d" id="tgt11" class="tgtSentence"> These members are contained by the <legacyBold>Members</legacyBold> collection of a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="b940df7c9346cfcf9d6023b64cba156b" id="tgt12" class="tgtSentence">
              <legacyBold>Members</legacyBold> is a standard ADO collection.</caps:sentence>
            <caps:sentence sentenceid="aa7ab60c38131526d7cc907ae21f8cf8" id="tgt13" class="tgtSentence"> With the properties and methods of a collection, you can do the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="119df3e27fc24c7b7e2ba67302fea726" id="tgt14" class="tgtSentence">Obtain the number of objects in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="91b3fcecbf61504098c6ca4a08390a91" id="tgt15" class="tgtSentence">Return an object from the collection with the default <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b855e706ff56cde78c100799a071e811" id="tgt16" class="tgtSentence">Update the objects in the collection from the provider with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt17" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="4e873d782c6ae5c29bf71db71f0b99e8" id="tgt18" class="tgtSentence">
                  <legacyLink xlink:href="da2c0761-fe23-421b-acbf-d97dfa02d2b9">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="87bbd4ad-bb1a-4123-93ef-99ef47fd970b">VBScript Example</link>
        <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains the <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects from a level or a position along an axis.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <legacyBold>Members</legacyBold> collection is used to contain the following types of members:  </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src3" class="srcSentence">The members that make up a level in a cube.</caps:sentence>
                <caps:sentence id="src4" class="srcSentence"> These are contained in the <legacyBold>Members</legacyBold> collection of a <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink> object.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> For example, using the sample from <legacyLink xlink:href="ce37fa06-c581-4d80-9a9b-c3aa66408909">Overview of Multidimensional Schemas and Data</legacyLink>, the four members of the Countries level are Canada, USA, UK, and Germany.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">The members that are the children of a specific member within a hierarchy.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> These members are returned by the <legacyLink xlink:href="61d36468-1ccd-467a-9cb5-17d0bfacc766">Children</legacyLink> property of the parent <legacyBold>Member</legacyBold> object.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">The members that define a specific position along an axis of a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">cellset</legacyLink>.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> Using the cellset from <legacyLink xlink:href="84387746-aa3e-44fd-ad6c-a8214a6966dc">Working with Multidimensional Data</legacyLink> as an example, the two members of the first position on the x-axis are Valentine and Seattle.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> These members are contained by the <legacyBold>Members</legacyBold> collection of a <legacyLink xlink:href="91eab784-3ce9-41d6-a840-9b0939ca0608">Position</legacyLink> object.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src12" class="srcSentence">
              <legacyBold>Members</legacyBold> is a standard ADO collection.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> With the properties and methods of a collection, you can do the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">Obtain the number of objects in the collection with the <legacyLink xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">Return an object from the collection with the default <legacyLink xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item</legacyLink> property.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">Update the objects in the collection from the provider with the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src17" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">
                  <legacyLink xlink:href="da2c0761-fe23-421b-acbf-d97dfa02d2b9">Properties, Methods, and Events</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="87bbd4ad-bb1a-4123-93ef-99ef47fd970b">VBScript Example</link>
        <link xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
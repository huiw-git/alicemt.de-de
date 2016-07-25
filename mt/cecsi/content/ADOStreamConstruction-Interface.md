---
title: "ADOStreamConstruction Interface"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 92f5a939-3e1a-4b14-a9dd-90e6ce2dec74
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
# ADOStreamConstruction Interface
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8adc259fe6451bd2ce439cc3d68f57b8" id="tgt1" class="tgtSentence">The <legacyBold>ADOStreamConstruction</legacyBold> interface is used to construct an ADO <legacyBold>Stream</legacyBold> object from an OLE DB <legacyBold>IStream</legacyBold> object in a C/C++ application.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt2" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="4a44f9f6-0265-4c00-8def-d85b6af923b1">Stream</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2528cae64820cb6ec8186372a5abd076" id="tgt3" class="tgtSentence">Read/Write.</caps:sentence>
                    <caps:sentence sentenceid="9c9d0c73a19ddada6b554fae55ef9674" id="tgt4" class="tgtSentence"> Gets/sets an OLE DB <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt5" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt6" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt7" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt8" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="2c8d750d82c2353e1172842f66e01a9c" id="tgt9" class="tgtSentence">Given an OLE DB <legacyBold>IStream</legacyBold> object (<codeInline>pStream</codeInline>), the construction of an ADO <legacyBold>Stream</legacyBold> object (<codeInline>adoStr</codeInline>) amounts to the following three basic operations:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="3a03410e6ad5299f2283fa0fb412937a" id="tgt10" class="tgtSentence">Create an ADO <legacyBold>Stream</legacyBold> object: </caps:sentence>
              </para>
              <code>Stream20Ptr adoStr;
adoStr.CreateInstance(__uuidof(Stream));</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="98db136dbf63377efc27bc4d0e8340a5" id="tgt11" class="tgtSentence">Query the <legacyBold>IADOStreamConstruction</legacyBold> interface on the <legacyBold>Stream</legacyBold> object: </caps:sentence>
              </para>
              <code>adoStreamConstructionPtr adoStrConstruct=NULL;
adoStr-&gt;QueryInterface(__uuidof(ADOStreamConstruction),
                     (void**)&amp;adoStrConstruct);</code>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="d4962675a641eaaff5deb777cdbf2418" id="tgt12" class="tgtSentence">Call the <codeInline>IADOStreamConstruction::get_Stream</codeInline> property method to set the OLE DB <legacyBold>IStream</legacyBold> object on the ADO <legacyBold>Stream</legacyBold> object: </caps:sentence>
          </para>
          <code>IUnknown *pUnk=NULL;
pRowset-&gt;QueryInterface(IID_IUnknown, (void**)&amp;pUnk);
adoStrConstruct-&gt;put_Stream(pUnk);</code>
          <para>
            <caps:sentence sentenceid="800ba4e9f1eee48df3f30d1cc10e3425" id="tgt13" class="tgtSentence">The resultant <codeInline>adoStr</codeInline> object now represents the ADO <legacyBold>Stream</legacyBold> object constructed from the OLE DB <legacyBold>IStream</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="b4851e92b19af0c5c82447fc0937709d" id="tgt14" class="tgtSentence">Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="674029badbb8130b909d5aae4cbd1b9a" id="tgt15" class="tgtSentence">
              <legacyBold>Version:</legacyBold> ADO 2.0 or a later version</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d273d5404e2059cfd3ade46ba6444451" id="tgt16" class="tgtSentence">
              <legacyBold>Library:</legacyBold> msado15.dll</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="80af8a3307a2abb62e6e71570294640a" id="tgt17" class="tgtSentence">
              <legacyBold>UUID:</legacyBold> 00000283-0000-0010-8000-00AA006D2EA4</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>ADOStreamConstruction</legacyBold> interface is used to construct an ADO <legacyBold>Stream</legacyBold> object from an OLE DB <legacyBold>IStream</legacyBold> object in a C/C++ application.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="4a44f9f6-0265-4c00-8def-d85b6af923b1">Stream</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src3" class="srcSentence">Read/Write.</caps:sentence>
                    <caps:sentence id="src4" class="srcSentence"> Gets/sets an OLE DB <legacyBold>Stream</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">Given an OLE DB <legacyBold>IStream</legacyBold> object (<codeInline>pStream</codeInline>), the construction of an ADO <legacyBold>Stream</legacyBold> object (<codeInline>adoStr</codeInline>) amounts to the following three basic operations:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Create an ADO <legacyBold>Stream</legacyBold> object: </caps:sentence>
              </para>
              <code>Stream20Ptr adoStr;
adoStr.CreateInstance(__uuidof(Stream));</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Query the <legacyBold>IADOStreamConstruction</legacyBold> interface on the <legacyBold>Stream</legacyBold> object: </caps:sentence>
              </para>
              <code>adoStreamConstructionPtr adoStrConstruct=NULL;
adoStr-&gt;QueryInterface(__uuidof(ADOStreamConstruction),
                     (void**)&amp;adoStrConstruct);</code>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src12" class="srcSentence">Call the <codeInline>IADOStreamConstruction::get_Stream</codeInline> property method to set the OLE DB <legacyBold>IStream</legacyBold> object on the ADO <legacyBold>Stream</legacyBold> object: </caps:sentence>
          </para>
          <code>IUnknown *pUnk=NULL;
pRowset-&gt;QueryInterface(IID_IUnknown, (void**)&amp;pUnk);
adoStrConstruct-&gt;put_Stream(pUnk);</code>
          <para>
            <caps:sentence id="src13" class="srcSentence">The resultant <codeInline>adoStr</codeInline> object now represents the ADO <legacyBold>Stream</legacyBold> object constructed from the OLE DB <legacyBold>IStream</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">
              <legacyBold>Version:</legacyBold> ADO 2.0 or a later version</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">
              <legacyBold>Library:</legacyBold> msado15.dll</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">
              <legacyBold>UUID:</legacyBold> 00000283-0000-0010-8000-00AA006D2EA4</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
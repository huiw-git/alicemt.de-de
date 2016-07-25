---
title: "ADORecordConstruction Interface"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 52a5429e-5829-455e-be3b-31f05cbecf2d
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
# ADORecordConstruction Interface
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="85ce345f009c394c2bc5c8d39445a21d" id="tgt1" class="tgtSentence">The <legacyBold>ADORecordConstruction</legacyBold>interface is used to construct an ADO <legacyBold>Record</legacyBold> object from an OLE DB <legacyBold>Row</legacyBold> object in a C/C++ application.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="6595eb9afb5c0dcab73f6d655d486722" id="tgt2" class="tgtSentence">This interface supports the following properties:</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt3" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="5ea8029b-eda4-490b-ae84-2ad036fb582f">
                      <caps:sentence sentenceid="74888bace5aa960d4aad3e660a9bc6cf" id="tgt4" class="tgtSentence">ParentRow</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bbc5f135869218bba11681c163f25f3d" id="tgt5" class="tgtSentence">Write-only.</caps:sentence>
                    <caps:sentence sentenceid="633aede366f0eab42c46ea98b2c4cf41" id="tgt6" class="tgtSentence"> Sets the container of an OLE DB <legacyBold>Row</legacyBold> object on this ADO <legacyBold>Record</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="21019d89-2dd1-4a26-ac6f-384b81d66949">
                      <caps:sentence sentenceid="f1965a857bc285d26fe22023aa5ab50d" id="tgt7" class="tgtSentence">Row</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2528cae64820cb6ec8186372a5abd076" id="tgt8" class="tgtSentence">Read/Write.</caps:sentence>
                    <caps:sentence sentenceid="dc84b7ec7de55508e2458c41c25dcfd3" id="tgt9" class="tgtSentence"> Gets/sets an OLE DB <legacyBold>Row</legacyBold> object from/on this ADO <legacyBold>Record</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt10" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt11" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt12" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt13" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="4123d4f2ed48ae4e6c0b23fecd5aa9c9" id="tgt14" class="tgtSentence">Given an OLE DB <legacyBold>Row</legacyBold> object (<codeInline>pRow</codeInline>), the construction of an ADO <legacyBold>Record</legacyBold> object (<codeInline>adoR</codeInline>), amounts to the following three basic operations:

</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="a32848abff153a08455ead2981acac07" id="tgt15" class="tgtSentence">Create an ADO <legacyBold>Record</legacyBold> object:
</caps:sentence>
              </para>
              <code>_RecordPtr adoR;
adoRs.CreateInstance(__uuidof(_Record));</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="341e80a62ee29e04f35a440b6d3b0630" id="tgt16" class="tgtSentence">Query the <legacyBold>IADORecordConstruction</legacyBold> interface on the <legacyBold>Record</legacyBold> object:
</caps:sentence>
              </para>
              <code>adoRecordConstructionPtr adoRConstruct=NULL;
adoR-&gt;QueryInterface(__uuidof(ADORecordConstruction),
                    (void**)&amp;adoRConstruct);</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a6107d830f8850810c403661931ecb06" id="tgt17" class="tgtSentence">Call the <legacyBold>IADORecordConstruction::put_Row</legacyBold> property method to set the OLE DB <legacyBold>Row</legacyBold> object on the ADO <legacyBold>Record</legacyBold> object:
</caps:sentence>
              </para>
              <code>IUnknown *pUnk=NULL;
pRow-&gt;QueryInterface(IID_IUnknown, (void**)&amp;pUnk);
adoRConstruct-&gt;put_Row(pUnk);</code>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="73beda6be03e75cdf0099b1a79afc7d5" id="tgt18" class="tgtSentence">The resultant <legacyBold>adoR</legacyBold> object now represents the ADO <legacyBold>Record</legacyBold> object constructed from the OLE DB <legacyBold>Row</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a8f4b0c62a3b18e0d21209f569a58a66" id="tgt19" class="tgtSentence">An ADO <legacyBold>Record</legacyBold> object can also be constructed from the container of an OLE DB <legacyBold>Row</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="b4851e92b19af0c5c82447fc0937709d" id="tgt20" class="tgtSentence">Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a6fe5bf718fbaf301c030066e8a6172a" id="tgt21" class="tgtSentence">
              <legacyBold>Version:</legacyBold> ADO 2.0 and later</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d273d5404e2059cfd3ade46ba6444451" id="tgt22" class="tgtSentence">
              <legacyBold>Library:</legacyBold> msado15.dll</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b4de89d5bf80eaf995dd74eeee123b3c" id="tgt23" class="tgtSentence">
              <legacyBold>UUID:</legacyBold> 00000567-0000-0010-8000-00AA006D2EA4</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>ADORecordConstruction</legacyBold>interface is used to construct an ADO <legacyBold>Record</legacyBold> object from an OLE DB <legacyBold>Row</legacyBold> object in a C/C++ application.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">This interface supports the following properties:</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Properties</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="5ea8029b-eda4-490b-ae84-2ad036fb582f">
                      <caps:sentence id="src4" class="srcSentence">ParentRow</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Write-only.</caps:sentence>
                    <caps:sentence id="src6" class="srcSentence"> Sets the container of an OLE DB <legacyBold>Row</legacyBold> object on this ADO <legacyBold>Record</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="21019d89-2dd1-4a26-ac6f-384b81d66949">
                      <caps:sentence id="src7" class="srcSentence">Row</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Read/Write.</caps:sentence>
                    <caps:sentence id="src9" class="srcSentence"> Gets/sets an OLE DB <legacyBold>Row</legacyBold> object from/on this ADO <legacyBold>Record</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">Given an OLE DB <legacyBold>Row</legacyBold> object (<codeInline>pRow</codeInline>), the construction of an ADO <legacyBold>Record</legacyBold> object (<codeInline>adoR</codeInline>), amounts to the following three basic operations:

</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">Create an ADO <legacyBold>Record</legacyBold> object:
</caps:sentence>
              </para>
              <code>_RecordPtr adoR;
adoRs.CreateInstance(__uuidof(_Record));</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">Query the <legacyBold>IADORecordConstruction</legacyBold> interface on the <legacyBold>Record</legacyBold> object:
</caps:sentence>
              </para>
              <code>adoRecordConstructionPtr adoRConstruct=NULL;
adoR-&gt;QueryInterface(__uuidof(ADORecordConstruction),
                    (void**)&amp;adoRConstruct);</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src17" class="srcSentence">Call the <legacyBold>IADORecordConstruction::put_Row</legacyBold> property method to set the OLE DB <legacyBold>Row</legacyBold> object on the ADO <legacyBold>Record</legacyBold> object:
</caps:sentence>
              </para>
              <code>IUnknown *pUnk=NULL;
pRow-&gt;QueryInterface(IID_IUnknown, (void**)&amp;pUnk);
adoRConstruct-&gt;put_Row(pUnk);</code>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src18" class="srcSentence">The resultant <legacyBold>adoR</legacyBold> object now represents the ADO <legacyBold>Record</legacyBold> object constructed from the OLE DB <legacyBold>Row</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">An ADO <legacyBold>Record</legacyBold> object can also be constructed from the container of an OLE DB <legacyBold>Row</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">
              <legacyBold>Version:</legacyBold> ADO 2.0 and later</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">
              <legacyBold>Library:</legacyBold> msado15.dll</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">
              <legacyBold>UUID:</legacyBold> 00000567-0000-0010-8000-00AA006D2EA4</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
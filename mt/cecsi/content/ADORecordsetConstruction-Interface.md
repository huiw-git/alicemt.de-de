---
title: "ADORecordsetConstruction Interface"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 08386eba-f1f7-4879-8ffd-8733930ecb2f
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
# ADORecordsetConstruction Interface
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c7a7d7fa6e1a94a05ac7c8577bcd7b81" id="tgt1" class="tgtSentence">The <legacyBold>ADORecordsetConstruction</legacyBold> interface is used to construct an ADO <legacyBold>Recordset</legacyBold> object from an OLE DB <legacyBold>Rowset</legacyBold> object in a C/C++ application.</caps:sentence>
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
                    <legacyLink xlink:href="8aa90cb0-f588-4141-9dc9-3b22918394ee">
                      <caps:sentence sentenceid="7a3e56dbf4b75792017d682faf64ac07" id="tgt4" class="tgtSentence">Chapter</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2528cae64820cb6ec8186372a5abd076" id="tgt5" class="tgtSentence">Read/Write.</caps:sentence>
                    <caps:sentence sentenceid="842350a7689c658b0a9d65b1518693e2" id="tgt6" class="tgtSentence"> Gets/sets an OLE DB <legacyBold>Chapter</legacyBold> object from/on this ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="9d068fed-39bf-4842-afc3-686a2af2145d">
                      <caps:sentence sentenceid="6c3918c8610eefc745439c1eda77950d" id="tgt7" class="tgtSentence">RowPosition</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2528cae64820cb6ec8186372a5abd076" id="tgt8" class="tgtSentence">Read/Write.</caps:sentence>
                    <caps:sentence sentenceid="53c5f52a9fdcb993f635c0b791a7c38f" id="tgt9" class="tgtSentence"> Gets/sets an OLE DB <legacyBold>RowPosition</legacyBold> object from/on this ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="7d359294-4ff2-47e0-8111-0c221b24d80e">
                      <caps:sentence sentenceid="2131f033d6f9e7addb358973b976cdd7" id="tgt10" class="tgtSentence">Rowset</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2528cae64820cb6ec8186372a5abd076" id="tgt11" class="tgtSentence">Read/Write.</caps:sentence>
                    <caps:sentence sentenceid="7ece6023ff5004ebae632245ab4baf10" id="tgt12" class="tgtSentence"> Gets/sets an OLE DB <legacyBold>Rowset</legacyBold> object from/on this ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt13" class="tgtSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt14" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt15" class="tgtSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db8364551ec38ac92a995fb6398bac21" id="tgt16" class="tgtSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="a0ebd44a8a16877da68e11166d29259d" id="tgt17" class="tgtSentence">Given an OLE DB <legacyBold>Rowset</legacyBold> object (<codeInline>pRowset</codeInline>), the construction of an ADO <legacyBold>Recordset</legacyBold> object (<codeInline>adoRs</codeInline>) amounts to the following three basic operations:

</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="ee657e8025c0c83de68fb6796d4f9daa" id="tgt18" class="tgtSentence">Create an ADO <legacyBold>Recordset</legacyBold> object:
</caps:sentence>
              </para>
              <code>Recordset20Ptr adoRs;
adoRs.CreateInstance(__uuidof(Recordset));</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="54d25a6e28da030ab8517a267d79ed59" id="tgt19" class="tgtSentence">Query the <legacyBold>IADORecordsetConstruction</legacyBold> interface on the <legacyBold>Recordset</legacyBold> object:
</caps:sentence>
              </para>
              <code>adoRecordsetConstructionPtr adoRsConstruct=NULL;
adoRs-&gt;QueryInterface(__uuidof(ADORecordsetConstruction),
                     (void**)&amp;adoRsConstruct);</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="cf56d8ed457a90f6eb83a29a0e988530" id="tgt20" class="tgtSentence">Call the <codeInline>IADORecordsetConstruction::put_Rowset</codeInline> property method to set the OLE DB <codeInline>Rowset</codeInline> object on the ADO <codeInline>Recordset</codeInline> object:
</caps:sentence>
              </para>
              <code>IUnknown *pUnk=NULL;
pRowset-&gt;QueryInterface(IID_IUnknown, (void**)&amp;pUnk);
adoRsConstruct-&gt;put_Rowset(pUnk);</code>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="c42dd95f766915c9f85906db3b94ac60" id="tgt21" class="tgtSentence">The resultant <codeInline>adoRs</codeInline> object now represents the ADO <legacyBold>Recordset</legacyBold> object constructed from the OLE DB <legacyBold>Rowset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e72e35f1f6075df521f7006cb381de11" id="tgt22" class="tgtSentence">You can also construct an ADO <legacyBold>Recordset</legacyBold> object from an OLE DB <legacyBold>Chapter</legacyBold> or <legacyBold>RowPosition</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="b4851e92b19af0c5c82447fc0937709d" id="tgt23" class="tgtSentence">Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a6fe5bf718fbaf301c030066e8a6172a" id="tgt24" class="tgtSentence">
              <legacyBold>Version:</legacyBold> ADO 2.0 and later</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d273d5404e2059cfd3ade46ba6444451" id="tgt25" class="tgtSentence">
              <legacyBold>Library:</legacyBold> msado15.dll</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="80af8a3307a2abb62e6e71570294640a" id="tgt26" class="tgtSentence">
              <legacyBold>UUID:</legacyBold> 00000283-0000-0010-8000-00AA006D2EA4</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="7d359294-4ff2-47e0-8111-0c221b24d80e">Rowset Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>ADORecordsetConstruction</legacyBold> interface is used to construct an ADO <legacyBold>Recordset</legacyBold> object from an OLE DB <legacyBold>Rowset</legacyBold> object in a C/C++ application.</caps:sentence>
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
                    <legacyLink xlink:href="8aa90cb0-f588-4141-9dc9-3b22918394ee">
                      <caps:sentence id="src4" class="srcSentence">Chapter</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Read/Write.</caps:sentence>
                    <caps:sentence id="src6" class="srcSentence"> Gets/sets an OLE DB <legacyBold>Chapter</legacyBold> object from/on this ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="9d068fed-39bf-4842-afc3-686a2af2145d">
                      <caps:sentence id="src7" class="srcSentence">RowPosition</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Read/Write.</caps:sentence>
                    <caps:sentence id="src9" class="srcSentence"> Gets/sets an OLE DB <legacyBold>RowPosition</legacyBold> object from/on this ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyLink xlink:href="7d359294-4ff2-47e0-8111-0c221b24d80e">
                      <caps:sentence id="src10" class="srcSentence">Rowset</caps:sentence>
                    </legacyLink>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Read/Write.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> Gets/sets an OLE DB <legacyBold>Rowset</legacyBold> object from/on this ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src15" class="srcSentence">Events</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src16" class="srcSentence">None.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">Given an OLE DB <legacyBold>Rowset</legacyBold> object (<codeInline>pRowset</codeInline>), the construction of an ADO <legacyBold>Recordset</legacyBold> object (<codeInline>adoRs</codeInline>) amounts to the following three basic operations:

</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src18" class="srcSentence">Create an ADO <legacyBold>Recordset</legacyBold> object:
</caps:sentence>
              </para>
              <code>Recordset20Ptr adoRs;
adoRs.CreateInstance(__uuidof(Recordset));</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">Query the <legacyBold>IADORecordsetConstruction</legacyBold> interface on the <legacyBold>Recordset</legacyBold> object:
</caps:sentence>
              </para>
              <code>adoRecordsetConstructionPtr adoRsConstruct=NULL;
adoRs-&gt;QueryInterface(__uuidof(ADORecordsetConstruction),
                     (void**)&amp;adoRsConstruct);</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">Call the <codeInline>IADORecordsetConstruction::put_Rowset</codeInline> property method to set the OLE DB <codeInline>Rowset</codeInline> object on the ADO <codeInline>Recordset</codeInline> object:
</caps:sentence>
              </para>
              <code>IUnknown *pUnk=NULL;
pRowset-&gt;QueryInterface(IID_IUnknown, (void**)&amp;pUnk);
adoRsConstruct-&gt;put_Rowset(pUnk);</code>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src21" class="srcSentence">The resultant <codeInline>adoRs</codeInline> object now represents the ADO <legacyBold>Recordset</legacyBold> object constructed from the OLE DB <legacyBold>Rowset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">You can also construct an ADO <legacyBold>Recordset</legacyBold> object from an OLE DB <legacyBold>Chapter</legacyBold> or <legacyBold>RowPosition</legacyBold> object.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">Requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src24" class="srcSentence">
              <legacyBold>Version:</legacyBold> ADO 2.0 and later</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src25" class="srcSentence">
              <legacyBold>Library:</legacyBold> msado15.dll</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src26" class="srcSentence">
              <legacyBold>UUID:</legacyBold> 00000283-0000-0010-8000-00AA006D2EA4</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="7d359294-4ff2-47e0-8111-0c221b24d80e">Rowset Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
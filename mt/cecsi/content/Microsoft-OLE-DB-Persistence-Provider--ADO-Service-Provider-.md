---
title: "Microsoft OLE DB Persistence Provider (ADO Service Provider)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e75ef0dc-2016-4fcc-8918-23311c0d4e02
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
# Microsoft OLE DB Persistence Provider (ADO Service Provider)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="79fe1f36f4696cf242a1f6ca00e75861" id="tgt1" class="tgtSentence">The Microsoft OLE DB Persistence Provider enables you to save a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object into a file, and later restore that <legacyBold>Recordset</legacyBold> object from the file.</caps:sentence>
          <caps:sentence sentenceid="5ad413e49aec21bd7d28f841784335f5" id="tgt2" class="tgtSentence"> Schema information, data, and pending changes are preserved.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5004702c5fbd2e05b41a1c97cb49cfa5" id="tgt3" class="tgtSentence">You can save the <legacyBold>Recordset</legacyBold> in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="0975fcf10aa159131d858087aa78f2ce" id="tgt4" class="tgtSentence">Provider Keyword</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="111e8ec0f40dd411986fe96f3360231a" id="tgt5" class="tgtSentence">To invoke this provider, specify the following keyword and value in the connection string.</caps:sentence>
          </para>
          <code>"Provider=<codeFeaturedElement xmlns="">MSPersist</codeFeaturedElement>"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="07213a0161f52846ab198be103b5ab43" id="tgt6" class="tgtSentence">Errors</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="fc595a953da0909792b494808577eb81" id="tgt7" class="tgtSentence">The following errors issued by this provider can be detected in your application.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt8" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt9" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="769f3fc5d448899f95eecbf6cb9e77c4" id="tgt10" class="tgtSentence">E_BADSTREAM</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8d5c2d66d7a2866156e61f1985f6f878" id="tgt11" class="tgtSentence">The file opened does not have a valid format (that is, the format is not ADTG or XML).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="53e96c62b098e391ad21176c89c08b96" id="tgt12" class="tgtSentence">E_CANTPERSISTROWSET</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="701c91eaad1028bd67ba7874624110e0" id="tgt13" class="tgtSentence">The <legacyBold>Recordset</legacyBold> object saved has characteristics that prevent it from being stored.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1d5a008cbf34246c37080a85f36af054" id="tgt14" class="tgtSentence">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3591bd42a2a9eceeb01bd2cf202f0008" id="tgt15" class="tgtSentence">Currently, only parameterized hierarchical <legacyBold>Recordset</legacyBold> objects cannot be saved.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b374f0b7ac1463a00db26106f13a8fe5" id="tgt16" class="tgtSentence">For more information about persistently storing <legacyBold>Recordset</legacyBold> objects, see <legacyLink xlink:href="a9b287f5-04b0-4514-8143-f67879ca9842">Recordset Persistence</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="27a2ab4faba0da27fcf1fb34be7be317" id="tgt17" class="tgtSentence">When a stream is used to open a <legacyBold>Recordset,</legacyBold> there should be no parameters specified other than the <legacyItalic>Source</legacyItalic> parameter of the <legacyBold>Open</legacyBold> method.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider (ADO Service Provider)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The Microsoft OLE DB Persistence Provider enables you to save a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object into a file, and later restore that <legacyBold>Recordset</legacyBold> object from the file.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Schema information, data, and pending changes are preserved.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">You can save the <legacyBold>Recordset</legacyBold> in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Provider Keyword</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">To invoke this provider, specify the following keyword and value in the connection string.</caps:sentence>
          </para>
          <code>"Provider=<codeFeaturedElement xmlns="">MSPersist</codeFeaturedElement>"</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Errors</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">The following errors issued by this provider can be detected in your application.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">E_BADSTREAM</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">The file opened does not have a valid format (that is, the format is not ADTG or XML).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">E_CANTPERSISTROWSET</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">The <legacyBold>Recordset</legacyBold> object saved has characteristics that prevent it from being stored.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src14" class="srcSentence">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src15" class="srcSentence">Currently, only parameterized hierarchical <legacyBold>Recordset</legacyBold> objects cannot be saved.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">For more information about persistently storing <legacyBold>Recordset</legacyBold> objects, see <legacyLink xlink:href="a9b287f5-04b0-4514-8143-f67879ca9842">Recordset Persistence</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">When a stream is used to open a <legacyBold>Recordset,</legacyBold> there should be no parameters specified other than the <legacyItalic>Source</legacyItalic> parameter of the <legacyBold>Open</legacyBold> method.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider (ADO Service Provider)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
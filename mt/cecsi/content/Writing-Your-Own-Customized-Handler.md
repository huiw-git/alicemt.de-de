---
title: "Writing Your Own Customized Handler"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d447712a-e123-47b5-a3a4-5d366cfe8d72
caps.latest.revision: 12
caps.handback.revision: 12
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
# Writing Your Own Customized Handler
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ca59d5764669f0ce7bc018be00d2019b" id="tgt1" class="tgtSentence">You may want to write your own handler if you are an IIS server administrator who wants the default RDS support, but more control over user requests and access rights.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f26c0cabe16813ce32c9b347929cb51b" id="tgt2" class="tgtSentence">The MSDFMAP.Handler implements the <legacyBold>IDataFactoryHandler</legacyBold> interface.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="ece5f2dfd9510d2ce5fd87e13f3b437b" id="tgt3" class="tgtSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence sentenceid="7e5a2625f09b2693631c6f7abcf8ac31" id="tgt4" class="tgtSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence sentenceid="5ee47089982dbcec2c418ba7ac5aad13" id="tgt5" class="tgtSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence sentenceid="e7966be4cfdf511c1cdf461ed10c4409" id="tgt6" class="tgtSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="53a2094ade92003591a08e9f0e43741e" id="tgt7" class="tgtSentence">IDataFactoryHandler Interface</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="cb4032117cef8d77d93a17a6c2f11ea0" id="tgt8" class="tgtSentence">This interface has two methods, <legacyBold>GetRecordset</legacyBold> and <legacyBold>Reconnect</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="7889eea34ce55885e9fcb02b315b5736" id="tgt9" class="tgtSentence"> Both methods require that the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property be set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9ccde386adde416e04ee898f2108e945" id="tgt10" class="tgtSentence">Both methods take arguments that appear after the first comma in the "<legacyBold>Handler=</legacyBold>" keyword.</caps:sentence>
            <caps:sentence sentenceid="9f24e048dbbacbe2688de13c51943b5b" id="tgt11" class="tgtSentence"> For example, <codeInline>"Handler=progid,arg1,arg2;"</codeInline> will pass an argument string of <codeInline>"arg1,arg2"</codeInline>, and <codeInline>"Handler=progid"</codeInline> will pass a null argument.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="cd23c197fd9c9b8dccb06bba7d9aee57" id="tgt12" class="tgtSentence">GetRecordset Method</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9dab25f53e3a142bbb5ea7c295cb8bef" id="tgt13" class="tgtSentence">This method queries the data source and creates a new <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object using the arguments provided.</caps:sentence>
            <caps:sentence sentenceid="aa58629bc6da28f79ad5630f1e988a83" id="tgt14" class="tgtSentence"> The <legacyBold>Recordset</legacyBold> must be opened with <legacyBold>adLockBatchOptimistic</legacyBold> and must not be opened asynchronously.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="dbc11caa5bda99f77e6fb4dabd882e7d" id="tgt15" class="tgtSentence">Arguments</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d3fd9fe8fd4c6c62105a10ce77ba1afc" id="tgt16" class="tgtSentence">         <legacyBold><legacyItalic>conn</legacyItalic></legacyBold>   The connection string.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2f08ebe7cbaada70e889caa4412ec2a8" id="tgt17" class="tgtSentence">         <legacyBold><legacyItalic>args</legacyItalic></legacyBold>   The arguments for the handler.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d4cf8d53961c09a488d843c8ffab1b36" id="tgt18" class="tgtSentence">         <legacyBold><legacyItalic>query</legacyItalic></legacyBold>   The command text for making a query.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b0048767ddb8235dc99fc5b4d6e0b1ad" id="tgt19" class="tgtSentence">         <legacyBold><legacyItalic>ppRS</legacyItalic></legacyBold>   The pointer where the <legacyBold>Recordset</legacyBold> should be returned.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="92fd508c80cb1dc5805e1ffa50cb320a" id="tgt20" class="tgtSentence">Reconnect Method</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1c941d6164ed8e2572e82db1bbff9343" id="tgt21" class="tgtSentence">This method updates the data source.</caps:sentence>
            <caps:sentence sentenceid="3f6bdb806f5284e761b6d6fee3d7f4c3" id="tgt22" class="tgtSentence"> It creates a new <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object and attaches the given <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="dbc11caa5bda99f77e6fb4dabd882e7d" id="tgt23" class="tgtSentence">Arguments</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4780ef042cf7ea27614ea482b691a2ec" id="tgt24" class="tgtSentence">         <legacyBold>           </legacyBold><legacyBold><legacyItalic>conn</legacyItalic></legacyBold><legacyBold>         </legacyBold>   The connection string.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="f4a37f6caab8470d0ec7008bec60bbbb" id="tgt25" class="tgtSentence">         <legacyBold>           </legacyBold><legacyBold><legacyItalic>args</legacyItalic></legacyBold><legacyBold>         </legacyBold>   The arguments for the handler.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1812a4239c0b436a23b814e8b815ba5a" id="tgt26" class="tgtSentence">         <legacyBold>           </legacyBold><legacyBold><legacyItalic>pRS</legacyItalic></legacyBold><legacyBold>         </legacyBold>   A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4e3d13550cb9220649b6ce7622c8abe0" id="tgt27" class="tgtSentence">msdfhdl.idl</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="3547184de52188686ecd1f66dd104e0a" id="tgt28" class="tgtSentence">This is the interface definition for <legacyBold>IDataFactoryHandler</legacyBold> that appears in the <legacyBold>msdfhdl.idl</legacyBold> file.</caps:sentence>
          </para>
          <code>[
  uuid(D80DE8B3-0001-11d1-91E6-00C04FBBBFB3),
  version(1.0)
]
library MSDFHDL
{
    importlib("stdole32.tlb");
    importlib("stdole2.tlb");

    // TLib : Microsoft ActiveX Data Objects 2.0 Library
    // {00000200-0000-0010-8000-00AA006D2EA4}
    #ifdef IMPLIB
    importlib("implib\\x86\\release\\ado\\msado15.dll");
    #else
    importlib("msado20.dll");
    #endif

    [
      odl,
      uuid(D80DE8B5-0001-11d1-91E6-00C04FBBBFB3),
      version(1.0)
    ]
    interface IDataFactoryHandler : IUnknown
    {
HRESULT _stdcall GetRecordset(
      [in] BSTR conn,
      [in] BSTR args,
      [in] BSTR query,
      [out, retval] _Recordset **ppRS);

// DataFactory will use the ActiveConnection property
// on the Recordset after calling Reconnect.
   HRESULT _stdcall Reconnect(
      [in] BSTR conn,
      [in] BSTR args,
      [in] _Recordset *pRS);
    };
};</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">You may want to write your own handler if you are an IIS server administrator who wants the default RDS support, but more control over user requests and access rights.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">The MSDFMAP.Handler implements the <legacyBold>IDataFactoryHandler</legacyBold> interface.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">Beginning with Windows 8 and Windows Server 2012, RDS server components are no longer included in the Windows operating system (see Windows 8 and <externalLink><linkText>Windows Server 2012 Compatibility Cookbook</linkText><linkUri>http://download.microsoft.com/download/2/C/9/2C9C7B01-A1FC-47B6-9166-2151FB6E007C/Windows 8 and Windows Server 2012 Compatibility Cookbook.docx</linkUri></externalLink> for more detail).</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> RDS client components will be removed in a future version of Windows.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Avoid using this feature in new development work, and plan to modify applications that currently use this feature.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> Applications that use RDS should migrate to <externalLink><linkText>WCF Data Service</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=199565</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">IDataFactoryHandler Interface</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">This interface has two methods, <legacyBold>GetRecordset</legacyBold> and <legacyBold>Reconnect</legacyBold>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Both methods require that the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property be set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">Both methods take arguments that appear after the first comma in the "<legacyBold>Handler=</legacyBold>" keyword.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> For example, <codeInline>"Handler=progid,arg1,arg2;"</codeInline> will pass an argument string of <codeInline>"arg1,arg2"</codeInline>, and <codeInline>"Handler=progid"</codeInline> will pass a null argument.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">GetRecordset Method</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">This method queries the data source and creates a new <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object using the arguments provided.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> The <legacyBold>Recordset</legacyBold> must be opened with <legacyBold>adLockBatchOptimistic</legacyBold> and must not be opened asynchronously.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src15" class="srcSentence">Arguments</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src16" class="srcSentence">         <legacyBold><legacyItalic>conn</legacyItalic></legacyBold>   The connection string.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src17" class="srcSentence">         <legacyBold><legacyItalic>args</legacyItalic></legacyBold>   The arguments for the handler.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src18" class="srcSentence">         <legacyBold><legacyItalic>query</legacyItalic></legacyBold>   The command text for making a query.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src19" class="srcSentence">         <legacyBold><legacyItalic>ppRS</legacyItalic></legacyBold>   The pointer where the <legacyBold>Recordset</legacyBold> should be returned.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Reconnect Method</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src21" class="srcSentence">This method updates the data source.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> It creates a new <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object and attaches the given <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src23" class="srcSentence">Arguments</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src24" class="srcSentence">         <legacyBold>           </legacyBold><legacyBold><legacyItalic>conn</legacyItalic></legacyBold><legacyBold>         </legacyBold>   The connection string.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src25" class="srcSentence">         <legacyBold>           </legacyBold><legacyBold><legacyItalic>args</legacyItalic></legacyBold><legacyBold>         </legacyBold>   The arguments for the handler.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src26" class="srcSentence">         <legacyBold>           </legacyBold><legacyBold><legacyItalic>pRS</legacyItalic></legacyBold><legacyBold>         </legacyBold>   A <legacyBold>Recordset</legacyBold> object.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">msdfhdl.idl</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src28" class="srcSentence">This is the interface definition for <legacyBold>IDataFactoryHandler</legacyBold> that appears in the <legacyBold>msdfhdl.idl</legacyBold> file.</caps:sentence>
          </para>
          <code>[
  uuid(D80DE8B3-0001-11d1-91E6-00C04FBBBFB3),
  version(1.0)
]
library MSDFHDL
{
    importlib("stdole32.tlb");
    importlib("stdole2.tlb");

    // TLib : Microsoft ActiveX Data Objects 2.0 Library
    // {00000200-0000-0010-8000-00AA006D2EA4}
    #ifdef IMPLIB
    importlib("implib\\x86\\release\\ado\\msado15.dll");
    #else
    importlib("msado20.dll");
    #endif

    [
      odl,
      uuid(D80DE8B5-0001-11d1-91E6-00C04FBBBFB3),
      version(1.0)
    ]
    interface IDataFactoryHandler : IUnknown
    {
HRESULT _stdcall GetRecordset(
      [in] BSTR conn,
      [in] BSTR args,
      [in] BSTR query,
      [out, retval] _Recordset **ppRS);

// DataFactory will use the ActiveConnection property
// on the Recordset after calling Reconnect.
   HRESULT _stdcall Reconnect(
      [in] BSTR conn,
      [in] BSTR args,
      [in] _Recordset *pRS);
    };
};</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d50eb3cc-a822-486f-b80b-65bb50547ecd">Customization File Connect Section</link>
        <link xlink:href="a368e264-865c-41ee-be00-d9097255c2ea">Customization File Logs Section</link>
        <link xlink:href="e65c2871-9986-44ff-b8b7-7f5eda91b3fa">Customization File SQL Section</link>
        <link xlink:href="42e8ec20-eaac-4a95-8cb8-4bba93a75bcb">Customization File UserList Section</link>
        <link xlink:href="86d77985-a0d0-405a-8587-c85a20540a0e">DataFactory Customization</link>
        <link xlink:href="e776b4e3-fcc4-4bfb-a7e8-5ffae1d83833">Required Client Settings</link>
        <link xlink:href="136f74bf-8d86-4a41-be66-c86cbcf81548">Understanding the Customization File</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
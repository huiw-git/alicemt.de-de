---
title: "ADO Objects and Interfaces"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d0b7e254-c89f-4406-b846-a060ef038c30
caps.latest.revision: 13
caps.handback.revision: 13
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
# ADO Objects and Interfaces
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="31b388298c4d1b266d663890e84e9405" id="tgt1" class="tgtSentence">The relationships between these objects are represented in the <legacyLink xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="db87d9cad199fc228775ff9da16c54b6" id="tgt2" class="tgtSentence">Each object can be contained in its corresponding collection.</caps:sentence>
          <caps:sentence sentenceid="20bdb4c375a0b966ed26312e795cab21" id="tgt3" class="tgtSentence"> For example, an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object can be contained in an <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection.</caps:sentence>
          <caps:sentence sentenceid="317653829ab1ffd079311174ee66d87a" id="tgt4" class="tgtSentence"> For more information, see <legacyLink xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</legacyLink> or a specific collection topic.</caps:sentence>
        </para>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <externalLink>
                    <linkText>
                      <caps:sentence sentenceid="7aba404a06cf69c6f228bd13b8663a17" id="tgt5" class="tgtSentence">IADOCommandConstruction</caps:sentence>
                    </linkText>
                    <linkUri>https://msdn.microsoft.com/library/windows/desktop/aa965677.aspx</linkUri>
                  </externalLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ae0e66849d44780f9b9b52c3cd26bf0f" id="tgt6" class="tgtSentence">Used to retrieve the underlying OLEDB Command from an ADOCommand object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="52a5429e-5829-455e-be3b-31f05cbecf2d">
                    <caps:sentence sentenceid="5b53fca004f5a755587ff62a77466c0d" id="tgt7" class="tgtSentence">ADORecordConstruction</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f9a97d2abe64a0f0f339e2c5928a63b7" id="tgt8" class="tgtSentence">Constructs an ADO <legacyBold>Record</legacyBold> object from an OLE DB <legacyBold>Row</legacyBold> object in a C/C++ application.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">
                    <caps:sentence sentenceid="46259a5522941fbe39dd424e0c2105e5" id="tgt9" class="tgtSentence">ADORecordsetConstruction</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8773f321364926de862e2c4c5a523311" id="tgt10" class="tgtSentence">Constructs an ADO <legacyBold>Recordset</legacyBold> object from an OLE DB <legacyBold>Rowset</legacyBold> object in a C/C++ application.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="92f5a939-3e1a-4b14-a9dd-90e6ce2dec74">ADOStreamConstruction</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7b3906f9f3ceb6af215156467975d323" id="tgt11" class="tgtSentence">Constructs an ADO <legacyBold>Stream</legacyBold> object from an OLE DB <legacyBold>IStream</legacyBold> object in a C/C++ application.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">
                    <caps:sentence sentenceid="1dccadfed7bcbb036c56a4afb97e906f" id="tgt12" class="tgtSentence">Command</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="95a3eebb27707a64fb63822ddf5211ca" id="tgt13" class="tgtSentence">Defines a specific command that you intend to execute against a data source.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="0b16ea45b1b39b44d1b7939a20f7d6aa" id="tgt14" class="tgtSentence">The <legacyBold>Command</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">
                    <caps:sentence sentenceid="4717d53ebfdfea8477f780ec66151dcb" id="tgt15" class="tgtSentence">Connection</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="17dc7d8e216483c723a1979048ea0392" id="tgt16" class="tgtSentence">Represents an open connection to a data source.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="857c40f138d02f65a37171b91e66e504" id="tgt17" class="tgtSentence">The <legacyBold>Connection</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="ad4ba313-1161-4bc7-b8f6-4083305bc81e">IDSOShapeExtensions Interface</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="31bde4adbd1313832ea5b8898a15b221" id="tgt18" class="tgtSentence">Gets the underlying OLEDB Data Source object for the SHAPE provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt19" class="tgtSentence">Error</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f5fafb6469e9e044910d3d57714f0bde" id="tgt20" class="tgtSentence">Contains details about data access errors that pertain to a single operation involving the provider.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="8aefda42a9a3aa31a88cbc4e8787210b" id="tgt21" class="tgtSentence">The <legacyBold>Error</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">
                    <caps:sentence sentenceid="06e3d36fa30cea095545139854ad1fb9" id="tgt22" class="tgtSentence">Field</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d1cda4d581ef6976217bd90991d964f8" id="tgt23" class="tgtSentence">Represents a column of data with a common data type.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">
                    <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt24" class="tgtSentence">Parameter</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2f36405d71b703837f2b1151fab16ae7" id="tgt25" class="tgtSentence">Represents a parameter or argument associated with a <legacyBold>Command</legacyBold> object based on a parameterized query or stored procedure.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="c31392f8c09fab7147617093aa4907cf" id="tgt26" class="tgtSentence">The <legacyBold>Parameter</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">
                    <caps:sentence sentenceid="1a8db4c996d8ed8289da5f957879ab94" id="tgt27" class="tgtSentence">Property</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e13e71f844c46f3e873303d3a5bbc051" id="tgt28" class="tgtSentence">Represents a dynamic characteristic of an ADO object that is defined by the provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">
                    <caps:sentence sentenceid="de17f0f24b49f8364187891f8550ffbb" id="tgt29" class="tgtSentence">Record</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c570f9f69e6ee695bdd929d6840c2579" id="tgt30" class="tgtSentence">Represents a row of a <legacyBold>Recordset</legacyBold>, or a directory or file in a file system.</caps:sentence>
                  <caps:sentence sentenceid="d6f726316f829e9b64c03fc17954d8c8" id="tgt31" class="tgtSentence"> The <legacyBold>Record</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">
                    <caps:sentence sentenceid="c1e71ce69bff36c1582c5f180ea9a4ff" id="tgt32" class="tgtSentence">Recordset</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1ee80b744584c60a3f6db78a7539f3a8" id="tgt33" class="tgtSentence">Represents the set of records from a base table or the results of an executed command.</caps:sentence>
                  <caps:sentence sentenceid="897ca532fd939b8ba420b3045f063105" id="tgt34" class="tgtSentence"> At any time, the <legacyBold>Recordset</legacyBold> object refers to only a single record within the set as the current record.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="c955fbb5152fc75c6a8825ffc712d0a3" id="tgt35" class="tgtSentence">The <legacyBold>Recordset</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">
                    <caps:sentence sentenceid="f7b44cfafd5c52223d5498196c8a2e7b" id="tgt36" class="tgtSentence">Stream</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fc48accf998f0821ec69aae921a9310a" id="tgt37" class="tgtSentence">Represents a binary stream of data.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="8328bff31fc84c52214307bad4e48361" id="tgt38" class="tgtSentence">The <legacyBold>Stream</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</link>
        <link xlink:href="d7b06d72-f792-4328-93a2-5006b9e2c581">ADO Dynamic Properties</link>
        <link xlink:href="c97ed131-1a93-463c-9e61-22f029b0c474">ADO Enumerated Constants</link>
        <link xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">Appendix B: ADO Errors</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The relationships between these objects are represented in the <legacyLink xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Each object can be contained in its corresponding collection.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> For example, an <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">Error</legacyLink> object can be contained in an <legacyLink xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors</legacyLink> collection.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For more information, see <legacyLink xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</legacyLink> or a specific collection topic.</caps:sentence>
        </para>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <externalLink>
                    <linkText>
                      <caps:sentence id="src5" class="srcSentence">IADOCommandConstruction</caps:sentence>
                    </linkText>
                    <linkUri>https://msdn.microsoft.com/library/windows/desktop/aa965677.aspx</linkUri>
                  </externalLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Used to retrieve the underlying OLEDB Command from an ADOCommand object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="52a5429e-5829-455e-be3b-31f05cbecf2d">
                    <caps:sentence id="src7" class="srcSentence">ADORecordConstruction</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Constructs an ADO <legacyBold>Record</legacyBold> object from an OLE DB <legacyBold>Row</legacyBold> object in a C/C++ application.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="08386eba-f1f7-4879-8ffd-8733930ecb2f">
                    <caps:sentence id="src9" class="srcSentence">ADORecordsetConstruction</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Constructs an ADO <legacyBold>Recordset</legacyBold> object from an OLE DB <legacyBold>Rowset</legacyBold> object in a C/C++ application.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="92f5a939-3e1a-4b14-a9dd-90e6ce2dec74">ADOStreamConstruction</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Constructs an ADO <legacyBold>Stream</legacyBold> object from an OLE DB <legacyBold>IStream</legacyBold> object in a C/C++ application.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">
                    <caps:sentence id="src12" class="srcSentence">Command</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Defines a specific command that you intend to execute against a data source.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src14" class="srcSentence">The <legacyBold>Command</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">
                    <caps:sentence id="src15" class="srcSentence">Connection</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Represents an open connection to a data source.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src17" class="srcSentence">The <legacyBold>Connection</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <link xlink:href="ad4ba313-1161-4bc7-b8f6-4083305bc81e">IDSOShapeExtensions Interface</link>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Gets the underlying OLEDB Data Source object for the SHAPE provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="a175d453-fa55-4f49-9ede-a26d83177919">
                    <caps:sentence id="src19" class="srcSentence">Error</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Contains details about data access errors that pertain to a single operation involving the provider.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src21" class="srcSentence">The <legacyBold>Error</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">
                    <caps:sentence id="src22" class="srcSentence">Field</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Represents a column of data with a common data type.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">
                    <caps:sentence id="src24" class="srcSentence">Parameter</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Represents a parameter or argument associated with a <legacyBold>Command</legacyBold> object based on a parameterized query or stored procedure.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src26" class="srcSentence">The <legacyBold>Parameter</legacyBold> object is not safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="b2a4767c-03c7-4935-a3bc-df3e1a38a009">
                    <caps:sentence id="src27" class="srcSentence">Property</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">Represents a dynamic characteristic of an ADO object that is defined by the provider.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">
                    <caps:sentence id="src29" class="srcSentence">Record</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Represents a row of a <legacyBold>Recordset</legacyBold>, or a directory or file in a file system.</caps:sentence>
                  <caps:sentence id="src31" class="srcSentence"> The <legacyBold>Record</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">
                    <caps:sentence id="src32" class="srcSentence">Recordset</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Represents the set of records from a base table or the results of an executed command.</caps:sentence>
                  <caps:sentence id="src34" class="srcSentence"> At any time, the <legacyBold>Recordset</legacyBold> object refers to only a single record within the set as the current record.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src35" class="srcSentence">The <legacyBold>Recordset</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">
                    <caps:sentence id="src36" class="srcSentence">Stream</caps:sentence>
                  </legacyLink>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Represents a binary stream of data.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src38" class="srcSentence">The <legacyBold>Stream</legacyBold> object is safe for scripting.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</link>
        <link xlink:href="d7b06d72-f792-4328-93a2-5006b9e2c581">ADO Dynamic Properties</link>
        <link xlink:href="c97ed131-1a93-463c-9e61-22f029b0c474">ADO Enumerated Constants</link>
        <link xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">Appendix B: ADO Errors</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
---
title: "ConnectModeEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 3792c294-5161-4538-a908-22a5fc50b85f
caps.latest.revision: 10
caps.handback.revision: 10
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
# ConnectModeEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="68bf5132be3772083cddc7b47c1ad9ff" id="tgt1" class="tgtSentence">Specifies the available permissions for modifying data in a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, opening a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, or specifying values for the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property of the <legacyBold>Record</legacyBold> and <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt2" class="tgtSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt3" class="tgtSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt4" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="d651779a61ef5d61d26c6b4d85f24441" id="tgt5" class="tgtSentence">adModeRead</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt6" class="tgtSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="041698cdc102df29fc7c541a1ed75f49" id="tgt7" class="tgtSentence">Indicates read-only permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="f2cadd715d4af41a4ad02a95022b25ea" id="tgt8" class="tgtSentence">adModeReadWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eccbc87e4b5ce2fe28308fd9f2a7baf3" id="tgt9" class="tgtSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3d20d11e7f074b5d2cadcf44f5f55fa8" id="tgt10" class="tgtSentence">Indicates read/write permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="0abfdb76f325a879a1e84fd8ee346c56" id="tgt11" class="tgtSentence">adModeRecursive</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e318f565dbb2a9f98a0402100adf4473" id="tgt12" class="tgtSentence">0x400000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8aed57916a1ff7f1538983ef7fccfadc" id="tgt13" class="tgtSentence">Used in conjunction with the other <legacyItalic>*ShareDeny*</legacyItalic> values (<legacyBold>adModeShareDenyNone</legacyBold>, <legacyBold>adModeShareDenyWrite</legacyBold>, or <legacyBold>adModeShareDenyRead</legacyBold>) to propagate sharing restrictions to all sub-records of the current <legacyBold>Record</legacyBold>.</caps:sentence>
                  <caps:sentence sentenceid="6955ae31f9c93bcc1449338d1fa8e9c7" id="tgt14" class="tgtSentence"> It has no affect if the <legacyBold>Record</legacyBold> does not have any children.</caps:sentence>
                  <caps:sentence sentenceid="cfbf909600dcf4ca960743cf2b59ce19" id="tgt15" class="tgtSentence"> A run-time error is generated if it is used with <legacyBold>adModeShareDenyNone</legacyBold> only.</caps:sentence>
                  <caps:sentence sentenceid="d9adc95e40d8d203bcff6038926a016a" id="tgt16" class="tgtSentence"> However, it can be used with <legacyBold>adModeShareDenyNone</legacyBold> when combined with other values.</caps:sentence>
                  <caps:sentence sentenceid="3004fc8d7720d76d4b321ab163640188" id="tgt17" class="tgtSentence"> For example, you can use "<legacyBold>adModeRead</legacyBold> Or <legacyBold>adModeShareDenyNone</legacyBold> Or <legacyBold>adModeRecursive</legacyBold>".</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8a89f517ea4a94253478b15a570c7bcb" id="tgt18" class="tgtSentence">adModeShareDenyNone</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c74d97b01eae257e44aa9d5bade97baf" id="tgt19" class="tgtSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="02181f4ba2ff4f422112664b421eedda" id="tgt20" class="tgtSentence">Allows others to open a connection with any permissions.</caps:sentence>
                  <caps:sentence sentenceid="f8e74466192844bd07834eddcc1fa028" id="tgt21" class="tgtSentence"> Neither read nor write access can be denied to others.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="9880084138b9339cbe69f657d9624031" id="tgt22" class="tgtSentence">adModeShareDenyRead</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a87ff679a2f3e71d9181a67b7542122c" id="tgt23" class="tgtSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4b5145edbe63631534aefe2e9c5b4dde" id="tgt24" class="tgtSentence">Prevents others from opening a connection with read permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2e363f48e7a087b98d11cc13830970c4" id="tgt25" class="tgtSentence">adModeShareDenyWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c9f0f895fb98ab9159f51fd0297e236d" id="tgt26" class="tgtSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e5de9a66ad8b8cdb68e905ff953ca2c3" id="tgt27" class="tgtSentence">Prevents others from opening a connection with write permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="77a9a630b1b33b5303cae63393e92e2f" id="tgt28" class="tgtSentence">adModeShareExclusive</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c20ad4d76fe97759aa27a0c99bff6710" id="tgt29" class="tgtSentence">12</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5167ea175638f09a022c0fa6caef6cd3" id="tgt30" class="tgtSentence">Prevents others from opening a connection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="7d5b06a7bd07f82dbf9e0b79ccdf80db" id="tgt31" class="tgtSentence">adModeUnknown</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt32" class="tgtSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2519f5b2ce0ab7912c13b0af6ebf9f2" id="tgt33" class="tgtSentence">Default.</caps:sentence>
                  <caps:sentence sentenceid="95b1ee97c13fff3ede78c7ad5585f3b2" id="tgt34" class="tgtSentence"> Indicates that the permissions have not yet been set or cannot be determined.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="a1460d1c6f37ab8b406e22d245c0e868" id="tgt35" class="tgtSentence">adModeWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81e728d9d4c2f636f067f89cc14862c" id="tgt36" class="tgtSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c81c8f5664777f6055d6717c7ac47105" id="tgt37" class="tgtSentence">Indicates write-only permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt38" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt39" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt40" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="41f8bb0ce57a9e4449ef75bde01f5cf8" id="tgt41" class="tgtSentence">AdoEnums.ConnectMode.READ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2cd37f20c6047f7285fd9b06534e140f" id="tgt42" class="tgtSentence">AdoEnums.ConnectMode.READWRITE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ea2484830c88a105f0cbb2486ee9d4dd" id="tgt43" class="tgtSentence">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="51eb0e2275229e5fa0b8f65ed7af2705" id="tgt44" class="tgtSentence">AdoEnums.ConnectMode.SHAREDENYNONE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="742d874b193031b7f08b877af3006d7c" id="tgt45" class="tgtSentence">AdoEnums.ConnectMode.SHAREDENYREAD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03b98682d6afa22000528b85a524fb54" id="tgt46" class="tgtSentence">AdoEnums.ConnectMode.SHAREDENYWRITE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="901a2ca980d707437f5f8d21e8e09284" id="tgt47" class="tgtSentence">AdoEnums.ConnectMode.SHAREEXCLUSIVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0b23e52a7687c4420bcc961036441529" id="tgt48" class="tgtSentence">AdoEnums.ConnectMode.UNKNOWN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ce2342f0b7be55124ccb49fe5521134a" id="tgt49" class="tgtSentence">AdoEnums.ConnectMode.WRITE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt50" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode Property</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies the available permissions for modifying data in a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, opening a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>, or specifying values for the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property of the <legacyBold>Record</legacyBold> and <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> objects.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src5" class="srcSentence">adModeRead</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Indicates read-only permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src8" class="srcSentence">adModeReadWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Indicates read/write permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src11" class="srcSentence">adModeRecursive</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">0x400000</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Used in conjunction with the other <legacyItalic>*ShareDeny*</legacyItalic> values (<legacyBold>adModeShareDenyNone</legacyBold>, <legacyBold>adModeShareDenyWrite</legacyBold>, or <legacyBold>adModeShareDenyRead</legacyBold>) to propagate sharing restrictions to all sub-records of the current <legacyBold>Record</legacyBold>.</caps:sentence>
                  <caps:sentence id="src14" class="srcSentence"> It has no affect if the <legacyBold>Record</legacyBold> does not have any children.</caps:sentence>
                  <caps:sentence id="src15" class="srcSentence"> A run-time error is generated if it is used with <legacyBold>adModeShareDenyNone</legacyBold> only.</caps:sentence>
                  <caps:sentence id="src16" class="srcSentence"> However, it can be used with <legacyBold>adModeShareDenyNone</legacyBold> when combined with other values.</caps:sentence>
                  <caps:sentence id="src17" class="srcSentence"> For example, you can use "<legacyBold>adModeRead</legacyBold> Or <legacyBold>adModeShareDenyNone</legacyBold> Or <legacyBold>adModeRecursive</legacyBold>".</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src18" class="srcSentence">adModeShareDenyNone</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">16</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Allows others to open a connection with any permissions.</caps:sentence>
                  <caps:sentence id="src21" class="srcSentence"> Neither read nor write access can be denied to others.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src22" class="srcSentence">adModeShareDenyRead</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Prevents others from opening a connection with read permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src25" class="srcSentence">adModeShareDenyWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Prevents others from opening a connection with write permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src28" class="srcSentence">adModeShareExclusive</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">12</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Prevents others from opening a connection.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src31" class="srcSentence">adModeUnknown</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">0</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Default.</caps:sentence>
                  <caps:sentence id="src34" class="srcSentence"> Indicates that the permissions have not yet been set or cannot be determined.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src35" class="srcSentence">adModeWrite</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">2</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Indicates write-only permissions.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src38" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src39" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">AdoEnums.ConnectMode.READ</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">AdoEnums.ConnectMode.READWRITE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">AdoEnums.ConnectMode.SHAREDENYNONE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">AdoEnums.ConnectMode.SHAREDENYREAD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">AdoEnums.ConnectMode.SHAREDENYWRITE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">AdoEnums.ConnectMode.SHAREEXCLUSIVE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">AdoEnums.ConnectMode.UNKNOWN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">AdoEnums.ConnectMode.WRITE</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src50" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode Property</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open Method (ADO Record)</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open Method (ADO Stream)</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
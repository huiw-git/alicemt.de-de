---
title: "DataControl Error Codes"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 293df9d5-e1a2-406d-9107-07bf7cdc6f96
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
# DataControl Error Codes
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7e22892c424aae62a64648e31aa14686" id="tgt1" class="tgtSentence">The following table lists the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object error codes.</caps:sentence>
          <caps:sentence sentenceid="afd851230807f8f6d1ebaca904796a53" id="tgt2" class="tgtSentence"> The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="97c5d273230e4b439b4b02c6d80c69ca" id="tgt3" class="tgtSentence">RDS.DataControl error codes</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b1bc248a7ff2b2e95569f56de68615df" id="tgt4" class="tgtSentence">Number</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt5" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="63f7c8aef919ba955c63456b6e127939" id="tgt6" class="tgtSentence">               <legacyBold>IDS_AsyncPending</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d8859fde1347c35138cfe521e5b070d" id="tgt7" class="tgtSentence">4107 -2146824175 0x800A1011</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0799dd6d7475b1223de1ac23ae3d2a43" id="tgt8" class="tgtSentence">Operation cannot be performed while async operation is pending.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a93869475b0354cae04d48ef6ea0cebf" id="tgt9" class="tgtSentence">               <legacyBold>IDS_BadInlineTablegram</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3e1bd0b7ffc499c3c05181235684e7d7" id="tgt10" class="tgtSentence">4105 -2146824183 0x800A1009</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="19cf41a838a452cbd1adb8fc6d2039ea" id="tgt11" class="tgtSentence">Bad inline tablegram.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="58cf44121b5c0a5c87d2ba833ec9a4ea" id="tgt12" class="tgtSentence">               <legacyBold>IDS_CantConnect</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cdd542312dc1f41950f951a117ec5e1e" id="tgt13" class="tgtSentence">4099 -2146824189 0x800A1003</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="65d731a72555d3628c82e423e48f65de" id="tgt14" class="tgtSentence">Cannot connect to server.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3dd8853548130234a41e64d8a3a91644" id="tgt15" class="tgtSentence">               <legacyBold>IDS_CantCreateObject</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ef527876b32993f1958f807740294b89" id="tgt16" class="tgtSentence">4100 -2146824188 0x800A1004</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a7f1ee18c353a5bfde5d15f31d10edab" id="tgt17" class="tgtSentence">Business object cannot be created.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2d6c6934c2b87d03b73370a9bc3d39ab" id="tgt18" class="tgtSentence">               <legacyBold>IDS_CantFindDataspace</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4b05deb2d86c6116930b5b7c881fe989" id="tgt19" class="tgtSentence">4102 -2146824186 0x800A1006</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b7ea0b6b91b0ff0139935293a35b2aba" id="tgt20" class="tgtSentence">Dataspace property is not valid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="dc187b3dd37c4e637a368baad0ff68fb" id="tgt21" class="tgtSentence">               <legacyBold>IDS_CantInvokeMethod</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1c006910391753dd88f21fca79f25dae" id="tgt22" class="tgtSentence">4101 -2146824187 0x800A1005</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="50a76e09f1f2db551c5cb5be84bfc576" id="tgt23" class="tgtSentence">Method cannot be invoked on business object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6159560e73f35d21b418df1a2395a62b" id="tgt24" class="tgtSentence">               <legacyBold>IDS_CrossDomainWarning</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="774e4c7224ee972e9b7fe2350087f5f2" id="tgt25" class="tgtSentence">4112 -2146824170 0x800A1016</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9699f3b33b20d9684b6e74047a652051" id="tgt26" class="tgtSentence">This page accesses data on another domain.</caps:sentence>
                  <caps:sentence sentenceid="6132ea242ff45977ce65a306ec56e478" id="tgt27" class="tgtSentence"> Do you want to allow this?</caps:sentence>
                  <caps:sentence sentenceid="b0612599b828b59ba24d6b914a01571c" id="tgt28" class="tgtSentence"> To avoid this message in Internet Explorer, you can add a secure Web site to your Trusted Sites zone on the <legacyBold>Security</legacyBold> tab of the <legacyBold>Internet Options</legacyBold> dialog box.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6eb728675cadc98f1699db557cb53b2c" id="tgt29" class="tgtSentence">               <legacyBold>IDS_InvalidADCClientVersion</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8f887a705b7486e389cc60c01dfef27e" id="tgt30" class="tgtSentence">4106 -2146824176 0x800A1010</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0671845084670e730745f1f80b4b5433" id="tgt31" class="tgtSentence">Invalid RDS Client Version — Client is newer than server.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="398e029443f48a32b9a3d0dfe561ccf2" id="tgt32" class="tgtSentence">               <legacyBold>IDS_INVALIDARG</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="63f87a4c6383ab351c37fd864c4b29ac" id="tgt33" class="tgtSentence">5376 -2147019520 0x80071500</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="94ee5e86eecbddf1588d0a543188eca3" id="tgt34" class="tgtSentence">One or more arguments are invalid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9338cb9961d42124278fc05d5c76c403" id="tgt35" class="tgtSentence">               <legacyBold>IDS_InvalidBindings</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4db7d4b141c494ef4de5c38be78cc022" id="tgt36" class="tgtSentence">4097 -2146824191 0x800A1001</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9e5aef84cc32d82ef4fa738cb8c3bed1" id="tgt37" class="tgtSentence">Error in bindings property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ffdd3748eaad7a618b011b6c4c64a9a8" id="tgt38" class="tgtSentence">               <legacyBold>IDS_InvalidParam</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="909b93ba69bd3315fe7d290124e71cd8" id="tgt39" class="tgtSentence">4110 -2146824172 0x800A1014</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="94ee5e86eecbddf1588d0a543188eca3" id="tgt40" class="tgtSentence">One or more arguments are invalid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b15933e225b35e9d0e9e8bf563bff0cd" id="tgt41" class="tgtSentence">               <legacyBold>IDS_NOINTERFACE</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2ad738e113c85cf8fb6df0d6e7e5865e" id="tgt42" class="tgtSentence">5377 -2147019519 0x80071501</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9b256236b7be440927c06a104efd8a8e" id="tgt43" class="tgtSentence">No such interface is supported.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="eb6dd0a4abda46e17c96e630dbf702b0" id="tgt44" class="tgtSentence">               <legacyBold>IDS_NotReentrant</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7dd68b086e12b0b5fa9c2487127ab0c7" id="tgt45" class="tgtSentence">4111 -2146824171 0x800A1015</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1ff26128399dcca7849587727bdf6bc1" id="tgt46" class="tgtSentence">Request cannot be executed while the event handler is still processing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="9e5abfe401cfb04da9f6b8d7d8548412" id="tgt47" class="tgtSentence">               <legacyBold>IDS_ObjectNotSafe</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c076b03dc6940a39e9f81b1e1739915f" id="tgt48" class="tgtSentence">4103 -2146824185 0x800A1007</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a4662a34a1b3370a2189c08844119728" id="tgt49" class="tgtSentence">Safety settings on this computer prohibit creation of business object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2f3e4dd2973dd84509e4402aacc0f5bd" id="tgt50" class="tgtSentence">               <legacyBold>IDS_RecordsetNotOpen</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fa14d543aa11bfa8b4652354812842d5" id="tgt51" class="tgtSentence">4109 -2146824173 0x800A1013</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8ac59a6c1241ad5c409268c247dcfc90" id="tgt52" class="tgtSentence">               <legacyBold>Recordset</legacyBold> is not open.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="eca59342dd5db493d5e5109a2f0b1657" id="tgt53" class="tgtSentence">               <legacyBold>IDS_ResetInvalidField</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="99596441c04f46b3a8b0e729eb5e5a2b" id="tgt54" class="tgtSentence">4108 -2146824174 0x800A1012</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0a9d58d2bd8d1f111a24f96fbe561f9b" id="tgt55" class="tgtSentence">Column specified in <legacyBold>SortColumn</legacyBold> or <legacyBold>FilterColumn</legacyBold> does not exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3e611589588541c50866f10679e1a411" id="tgt56" class="tgtSentence">               <legacyBold>IDS_RowsetNotUpdateable</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="53b43ac31c88f7439d5555e8e35a5552" id="tgt57" class="tgtSentence">4104 -2146824184 0x800A1008</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ceb0f9a43b5858905761b7b5511c8434" id="tgt58" class="tgtSentence">Rowset not updateable.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c2b484de3d60fe5e76bee0e1ec560334" id="tgt59" class="tgtSentence">               <legacyBold>IDS_UnexpectedError</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="90ef36118c397ddd812ba54f3056fdd7" id="tgt60" class="tgtSentence">4351 -2146823937 0x800A10FF</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="24f48949498e24c529c7f2a559ca38bf" id="tgt61" class="tgtSentence">Unexpected error.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="85c2412029e8e513860d0c8cf542f2e4" id="tgt62" class="tgtSentence">               <legacyBold>IDS_UpdatesFailed</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e47eb62f6964932284ccd477ce75a0b6" id="tgt63" class="tgtSentence">4098 -2146824190 0x800A1002</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f6cea127c7d5c2240ae27a3e9986083f" id="tgt64" class="tgtSentence">Unable to update database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8b3de2a6312eaaa03bb6af7f015b15a9" id="tgt65" class="tgtSentence">               <legacyBold>IDS_URLMONNotFound</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b92325185f29f4add8692adc2b390843" id="tgt66" class="tgtSentence">4119 -2146824169 0x800A1017</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="18609712e0514f3d0b9bb83190b86b70" id="tgt67" class="tgtSentence">DataControl <legacyBold>URL</legacyBold> property requires the system file Urlmon.dll, which cannot be found.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following table lists the <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">RDS.DataControl</legacyLink> object error codes.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">RDS.DataControl error codes</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Number</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">               <legacyBold>IDS_AsyncPending</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">4107 -2146824175 0x800A1011</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Operation cannot be performed while async operation is pending.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">               <legacyBold>IDS_BadInlineTablegram</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">4105 -2146824183 0x800A1009</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Bad inline tablegram.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">               <legacyBold>IDS_CantConnect</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">4099 -2146824189 0x800A1003</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Cannot connect to server.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">               <legacyBold>IDS_CantCreateObject</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">4100 -2146824188 0x800A1004</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Business object cannot be created.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">               <legacyBold>IDS_CantFindDataspace</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">4102 -2146824186 0x800A1006</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Dataspace property is not valid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">               <legacyBold>IDS_CantInvokeMethod</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">4101 -2146824187 0x800A1005</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Method cannot be invoked on business object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">               <legacyBold>IDS_CrossDomainWarning</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">4112 -2146824170 0x800A1016</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">This page accesses data on another domain.</caps:sentence>
                  <caps:sentence id="src27" class="srcSentence"> Do you want to allow this?</caps:sentence>
                  <caps:sentence id="src28" class="srcSentence"> To avoid this message in Internet Explorer, you can add a secure Web site to your Trusted Sites zone on the <legacyBold>Security</legacyBold> tab of the <legacyBold>Internet Options</legacyBold> dialog box.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">               <legacyBold>IDS_InvalidADCClientVersion</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">4106 -2146824176 0x800A1010</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Invalid RDS Client Version — Client is newer than server.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">               <legacyBold>IDS_INVALIDARG</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">5376 -2147019520 0x80071500</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">One or more arguments are invalid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">               <legacyBold>IDS_InvalidBindings</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">4097 -2146824191 0x800A1001</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Error in bindings property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">               <legacyBold>IDS_InvalidParam</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">4110 -2146824172 0x800A1014</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">One or more arguments are invalid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">               <legacyBold>IDS_NOINTERFACE</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">5377 -2147019519 0x80071501</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src43" class="srcSentence">No such interface is supported.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src44" class="srcSentence">               <legacyBold>IDS_NotReentrant</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">4111 -2146824171 0x800A1015</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src46" class="srcSentence">Request cannot be executed while the event handler is still processing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">               <legacyBold>IDS_ObjectNotSafe</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src48" class="srcSentence">4103 -2146824185 0x800A1007</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src49" class="srcSentence">Safety settings on this computer prohibit creation of business object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src50" class="srcSentence">               <legacyBold>IDS_RecordsetNotOpen</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src51" class="srcSentence">4109 -2146824173 0x800A1013</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src52" class="srcSentence">               <legacyBold>Recordset</legacyBold> is not open.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">               <legacyBold>IDS_ResetInvalidField</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">4108 -2146824174 0x800A1012</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src55" class="srcSentence">Column specified in <legacyBold>SortColumn</legacyBold> or <legacyBold>FilterColumn</legacyBold> does not exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">               <legacyBold>IDS_RowsetNotUpdateable</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">4104 -2146824184 0x800A1008</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src58" class="srcSentence">Rowset not updateable.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">               <legacyBold>IDS_UnexpectedError</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src60" class="srcSentence">4351 -2146823937 0x800A10FF</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src61" class="srcSentence">Unexpected error.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src62" class="srcSentence">               <legacyBold>IDS_UpdatesFailed</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src63" class="srcSentence">4098 -2146824190 0x800A1002</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src64" class="srcSentence">Unable to update database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src65" class="srcSentence">               <legacyBold>IDS_URLMONNotFound</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src66" class="srcSentence">4119 -2146824169 0x800A1017</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src67" class="srcSentence">DataControl <legacyBold>URL</legacyBold> property requires the system file Urlmon.dll, which cannot be found.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl Object (RDS)</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
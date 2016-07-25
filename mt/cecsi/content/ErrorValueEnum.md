---
title: "ErrorValueEnum"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 9469ba3a-5e4f-4a10-bbb8-a51a6c9660ea
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
# ErrorValueEnum
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7e43dc4473ea0423a133a6bbcec6ebf8" id="tgt1" class="tgtSentence">Specifies the type of ADO run-time error.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e6a42db798d9feb299cfdcfa7df04ecf" id="tgt2" class="tgtSentence">Three forms of the error number are listed:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="4b20f3443d56564f84e62e34a84c78ec" id="tgt3" class="tgtSentence">Positive decimal—The low two bytes of the full number in decimal format.</caps:sentence>
              <caps:sentence sentenceid="d2fbe11e3ec46742d06735dd5c0e8aa3" id="tgt4" class="tgtSentence"> This number is displayed in the default Visual Basic error message dialog box.</caps:sentence>
              <caps:sentence sentenceid="d4bef980d2df58f864f2226faa4b1f60" id="tgt5" class="tgtSentence"> For example, Run-time error '3707'.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3dedfb925b5dcaa9e7c5ac32d24d97d0" id="tgt6" class="tgtSentence">Negative decimal—The decimal translation of the full error number.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="aca80113f8d95cff7f2be455ead24e62" id="tgt7" class="tgtSentence">Hexadecimal—The hexadecimal representation of the full error number.</caps:sentence>
              <caps:sentence sentenceid="f20999c64de812db7218b57b4ba9f7d9" id="tgt8" class="tgtSentence"> The Windows facility code is in the fourth digit.</caps:sentence>
              <caps:sentence sentenceid="81982d08b833823129e6308befb92625" id="tgt9" class="tgtSentence"> The facility code for ADO error numbers is <legacyItalic>A</legacyItalic>.</caps:sentence>
              <caps:sentence sentenceid="a7620aa4b0ccc72f69036cc85f58975f" id="tgt10" class="tgtSentence"> For example: 0x800<legacyBold><legacyItalic>A</legacyItalic></legacyBold>0E7B.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="a73f6cf4b1b28581ba54e6c8709fd3de" id="tgt11" class="tgtSentence">OLE DB errors may be passed to your ADO application.</caps:sentence>
            <caps:sentence sentenceid="68bce4fd12062e7c2189b1d649ddc86f" id="tgt12" class="tgtSentence"> Typically, these can be identified by a Windows facility code of <legacyItalic>4</legacyItalic>.</caps:sentence>
            <caps:sentence sentenceid="e614680a96d7c7800379f5d0a5662eb0" id="tgt13" class="tgtSentence"> For example, 0x800<legacyBold><legacyItalic>4</legacyItalic></legacyBold>.</caps:sentence>
          </para>
        </alert>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt14" class="tgtSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt15" class="tgtSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt16" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="d83e20925a0904022e3ea4dbc6c8ba81" id="tgt17" class="tgtSentence">adErrBoundToCommand</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2b06377d46ad6cc52ca09c17f95675a" id="tgt18" class="tgtSentence">3707 -2146824581 0x800A0E7B</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6473c1de2027c2fe8c8420fe3c7416d9" id="tgt19" class="tgtSentence">Cannot change the <legacyBold>ActiveConnection</legacyBold> property of a <legacyBold>Recordset</legacyBold> object that has a <legacyBold>Command</legacyBold> object as its source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="eabe9c9f32b3468f142ed67388a7a8ca" id="tgt20" class="tgtSentence">adErrCannotComplete</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="40c10189624f9ddae0a0b510fd806f10" id="tgt21" class="tgtSentence">3732 -2146824556 0x800A0E94</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="35a5383fc609b5e07e71eac34bfd9549" id="tgt22" class="tgtSentence">Server cannot complete the operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="49ad26c9488e2a8fe65df1983602c7fd" id="tgt23" class="tgtSentence">adErrCantChangeConnection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="03445b6b571d8e610c3f7fcf8eb18c25" id="tgt24" class="tgtSentence">3748 -2146824540 0x800A0EA4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b95be705e17420e2f1e6eeba8c23d6ad" id="tgt25" class="tgtSentence">Connection was denied.</caps:sentence>
                  <caps:sentence sentenceid="c56acbe1f008f6c677afe29f495b95a1" id="tgt26" class="tgtSentence"> New connection you requested has different characteristics than the one already being used.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="59fb23f96ec4e2ce1bbcd65e13f4e89d" id="tgt27" class="tgtSentence">adErrCantChangeProvider</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="630885c3c16ce140aa72f356052adde4" id="tgt28" class="tgtSentence">3220 -2146825068 0X800A0C94</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d8339ec90edbddb37473cef91b4f62ee" id="tgt29" class="tgtSentence">Supplied provider differs from the one already being used.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e785bb2fa6ff45378a737a276783487c" id="tgt30" class="tgtSentence">adErrCantConvertvalue</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="27863a0f6aad48b969da169a9fa9fc80" id="tgt31" class="tgtSentence">3724 -2146824564 0x800A0E8C</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f450dc03cb31f394b26c728d390e08e8" id="tgt32" class="tgtSentence">Data value cannot be converted for reasons other than sign mismatch or data overflow.</caps:sentence>
                  <caps:sentence sentenceid="00920bdd9dc794284dffa4cde31dd310" id="tgt33" class="tgtSentence"> For example, conversion would have truncated data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="2273a44c1021e632121436dbb3089eb6" id="tgt34" class="tgtSentence">adErrCantCreate</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cfb499d28cf8f482ea1d49c7806cc93d" id="tgt35" class="tgtSentence">3725 -2146824563 0x800A0E8D</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e743fa8deecea1165d1a1a5c4aeca2d6" id="tgt36" class="tgtSentence">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="999c389f1ff6329c8ad9c2185acaf17d" id="tgt37" class="tgtSentence">adErrCatalogNotSet</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="21ffb712ffbe27f4fb9380b342f1498a" id="tgt38" class="tgtSentence">3747 -2146824541 0x800A0EA3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3418c0591c545897ff0bf6340e67ca32" id="tgt39" class="tgtSentence">Operation requires a valid <legacyBold>ParentCatalog</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="6eae27104830fd5aacb15b9af863ded5" id="tgt40" class="tgtSentence">adErrColumnNotOnThisRow</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3c280ee9e8b1cd125e6cda9b8f7f8988" id="tgt41" class="tgtSentence">3726 -2146824562 0x800A0E8E</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fcb08b89ebac561cbdfe42ecf91be811" id="tgt42" class="tgtSentence">Record does not contain this field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="27cd03dcf580e86590aab5e95ff8f01c" id="tgt43" class="tgtSentence">adErrDataConversion</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="529dbe7b944709e97978ac15bd26b9ed" id="tgt44" class="tgtSentence">3421 -2146824867 0x800A0D5D</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d4d979068847a806f2f078ee3c1472a6" id="tgt45" class="tgtSentence">Application uses a value of the wrong type for the current operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e2ffad914bb05ba5356837bfa23b40cb" id="tgt46" class="tgtSentence">adErrDataOverflow</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0b849860e839e6acd94135625614f727" id="tgt47" class="tgtSentence">3721 -2146824567 0x800A0E89</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5ceee11ee6f18abd6020a0ddbb8ca861" id="tgt48" class="tgtSentence">Data value is too large to be represented by the field data type.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="0ba06e633c62f187cdd93f4ced95810e" id="tgt49" class="tgtSentence">adErrDelResOutOfScope</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="31b6876dcfaec26131887a998684dd85" id="tgt50" class="tgtSentence">3738 -2146824550 0x800A0E9A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1f891471302c072d618379304026b8f4" id="tgt51" class="tgtSentence">URL of the object to be deleted is outside the scope of the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="20bc93d939b4090eeb4212754699857c" id="tgt52" class="tgtSentence">adErrDenyNotSupported</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="85af8285e25b022258790505c7ad7964" id="tgt53" class="tgtSentence">3750 -2146824538 0x800A0EA6</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1f45ebab218f80b876c92859832841ef" id="tgt54" class="tgtSentence">Provider does not support sharing restrictions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="40dc224be9451444df6595ec761b46a0" id="tgt55" class="tgtSentence">adErrDenyTypeNotSupported</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2c42ae217d628ad29ea04cc3c260197b" id="tgt56" class="tgtSentence">3751 -2146824537 0x800A0EA7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ec2981c2639797308376573b3d4c9db0" id="tgt57" class="tgtSentence">Provider does not support the requested kind of sharing restriction.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e064a9ef087b9e4efa3b9258322f2117" id="tgt58" class="tgtSentence">adErrFeatureNotAvailable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1f8d9c2085cf4417a1e787b3c6a3caed" id="tgt59" class="tgtSentence">3251 -2146825037 0x800A0CB3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5ed6da9009495db306b9094eefb3180c" id="tgt60" class="tgtSentence">Object or provider is not able to perform requested operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="85209059c923d3d59abb5663db2481d0" id="tgt61" class="tgtSentence">adErrFieldsUpdateFailed</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d4dd59f8b073f3675416dc860df15a72" id="tgt62" class="tgtSentence">3749 -2146824539 0x800A0EA5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="712b01818b356ce05a6d49a66296c49a" id="tgt63" class="tgtSentence">Fields update failed.</caps:sentence>
                  <caps:sentence sentenceid="56c7bcb7a8b50c1e23b3fff4bf5baf37" id="tgt64" class="tgtSentence"> For more information, examine the <legacyBold>Status </legacyBold>property of individual field objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3a6cacdb831a10aeddae346e0191e826" id="tgt65" class="tgtSentence">adErrIllegalOperation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="db770b07a75713d64073e9b441050227" id="tgt66" class="tgtSentence">3219 -2146825069 0x800A0C93</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3320f18e2a04f511f9173928e43de3db" id="tgt67" class="tgtSentence">Operation is not allowed in this context.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="54ff6582457be04968adf14e15e37160" id="tgt68" class="tgtSentence">adErrIntegrityViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ff535ac698d1af09946c9fc4a7726689" id="tgt69" class="tgtSentence">3719 -2146824569 0x800A0E87</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4f7bb02613c70cecb68d47cdd4dba315" id="tgt70" class="tgtSentence">Data value conflicts with the integrity constraints of the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e780a0713239569e15d01f090d08d64a" id="tgt71" class="tgtSentence">adErrInTransaction</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7d85f6aa68f9e5aceb0888595c9df8fb" id="tgt72" class="tgtSentence">3246 -2146825042 0x800A0CAE</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="970fb6b0213b972c630d819b3e78aa3a" id="tgt73" class="tgtSentence">
                    <legacyBold>Connection</legacyBold> object cannot be explicitly closed while in a transaction.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="67aacfd2108aa7624a20f5496c65382a" id="tgt74" class="tgtSentence">adErrInvalidArgument</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ecdefa3c38ac68d3178830a16d8a898f" id="tgt75" class="tgtSentence">3001 -2146825287 0x800A0BB9</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fd0b9f7e4126329b27e78050fdf0d765" id="tgt76" class="tgtSentence">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1d76903b04f7989946131cfa03a7f8a0" id="tgt77" class="tgtSentence">adErrInvalidConnection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e6d5d5dc4854a0a518c211d58813cbf0" id="tgt78" class="tgtSentence">3709 -2146824579 0x800A0E7D</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="cbc3bcd76523c0477947e910aa071935" id="tgt79" class="tgtSentence">The connection cannot be used to perform this operation.</caps:sentence>
                  <caps:sentence sentenceid="caac1fb72e23081fe96abab2d88bd3b1" id="tgt80" class="tgtSentence"> It is either closed or invalid in this context.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="b7a21b33027a5e8a12c5b27f5da69d12" id="tgt81" class="tgtSentence">adErrInvalidParamInfo</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2604d4ffaa54262c447da6de09ad83e1" id="tgt82" class="tgtSentence">3708 -2146824580 0x800A0E7C</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="75be0bff06527056a4ff9f2e9308730f" id="tgt83" class="tgtSentence">
                    <legacyBold>Parameter</legacyBold> object is incorrectly defined.</caps:sentence>
                  <caps:sentence sentenceid="7b34ee764aee7f35d550093b3a2f5010" id="tgt84" class="tgtSentence"> Inconsistent or incomplete information was provided.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3909d7df3f096d55bd741ae9e2f6f0bc" id="tgt85" class="tgtSentence">adErrInvalidTransaction</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f744a947d21e9a5b2ce61c74681e6f1a" id="tgt86" class="tgtSentence">3714 -2146824574 0x800A0E82</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3ea05580b30159a801601c9178daec33" id="tgt87" class="tgtSentence">Coordinating transaction is invalid or has not started.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="f413461715943ab2c12697513fd413c7" id="tgt88" class="tgtSentence">adErrInvalidURL</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ac23116ae1778b1016731bcc465aa70a" id="tgt89" class="tgtSentence">3729 -2146824559 0x800A0E91</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5cf210c84c9e237930bf489fd85cf7c2" id="tgt90" class="tgtSentence">URL contains invalid characters.</caps:sentence>
                  <caps:sentence sentenceid="8a3ab5edbda65efb7a654f27c3a5db3d" id="tgt91" class="tgtSentence"> Make sure that the URL is typed correctly.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="0eed1a17f5361e2dd9b60874a7111bc0" id="tgt92" class="tgtSentence">adErrItemNotFound</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4158746bf0dd3832ab3e641fa5aa93fc" id="tgt93" class="tgtSentence">3265 -2146825023 0x800A0CC1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e758e11f2f6deaa77f468891c1e95564" id="tgt94" class="tgtSentence">Item cannot be found in the collection that corresponds to the requested name or ordinal.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="761778e23c21996175184b4df488d782" id="tgt95" class="tgtSentence">adErrNoCurrentRecord</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f6358d9975100763f30ca6d080acf289" id="tgt96" class="tgtSentence">3021 -2146825267 0x800A0BCD</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a7bebc2a5006c65b59816f853a819429" id="tgt97" class="tgtSentence">Either <legacyBold>BOF</legacyBold> or <legacyBold>EOF</legacyBold> is True, or the current record has been deleted.</caps:sentence>
                  <caps:sentence sentenceid="b5e885ea78e1d1e390b106db866684fa" id="tgt98" class="tgtSentence"> Requested operation requires a current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="c9b1bf11dedb1a22470f4be2a85d3e19" id="tgt99" class="tgtSentence">adErrNotExecuting</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d0c60041af8946391556edc020c06e18" id="tgt100" class="tgtSentence">3715 -2146824573 0x800A0E83</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bced4afda1d5c7733e1587608cab638c" id="tgt101" class="tgtSentence">Operation cannot be performed while not executing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="60f2be375c7722d18b08dccc831995b4" id="tgt102" class="tgtSentence">adErrNotReentrant</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="398846bfa8e182c99a0572cfaf501699" id="tgt103" class="tgtSentence">3710 -2146824578 0x800A0E7E</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3854a51bae151a7d4825212cfa1dd1cf" id="tgt104" class="tgtSentence">Operation cannot be performed while processing event.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8b77f5ab31cb2c989e17113b46f75576" id="tgt105" class="tgtSentence">adErrObjectClosed</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fa7401d2fe7ebaf815686d592660b634" id="tgt106" class="tgtSentence">3704 -2146824584 0x800A0E78</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="71c488de73428d38b5e711c77eb8d903" id="tgt107" class="tgtSentence">Operation is not allowed when the object is closed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3535be0f4e22ac975606243a3af38149" id="tgt108" class="tgtSentence">adErrObjectInCollection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8c23055710a390eb09e4ef21b03143d0" id="tgt109" class="tgtSentence">3367 -2146824921 0x800A0D27</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e989275e701d984bc1b20e172866c551" id="tgt110" class="tgtSentence">Object is already in collection.</caps:sentence>
                  <caps:sentence sentenceid="66cbd54be53c06dd795e12c3257d3699" id="tgt111" class="tgtSentence"> Cannot append.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="a414c3fbee1dc96edf5f882d19ffe7b6" id="tgt112" class="tgtSentence">adErrObjectNotSet</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="140b7ff0316cc8c83ecfa7861b3e25dc" id="tgt113" class="tgtSentence">3420 -2146824868 0x800A0D5C</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="944f79da74bfc952823bfc6d2036a0b1" id="tgt114" class="tgtSentence">Object is no longer valid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="0ba10029905b6fb005b14319ecdce080" id="tgt115" class="tgtSentence">adErrObjectOpen</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d2a9a8ec461a0f24866d67c1b8064ead" id="tgt116" class="tgtSentence">3705 -2146824583 0x800A0E79</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a97ff13987f72756164a7cb71c045255" id="tgt117" class="tgtSentence">Operation is not allowed when the object is open.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8591b15cbcfc773b83549e99f51b4a9a" id="tgt118" class="tgtSentence">adErrOpeningFile</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="124c8ac2bacb22b288557b2e1634eb6f" id="tgt119" class="tgtSentence">3002 -2146825286 0x800A0BBA</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8003d8c7181ec5313cd93a4202a5a661" id="tgt120" class="tgtSentence">File could not be opened.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="8d1ed7087c4426e9c4ffbf6f0513b24d" id="tgt121" class="tgtSentence">adErrOperationCancelled</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ba0739c9e1299da5fc3b93e944b99e1a" id="tgt122" class="tgtSentence">3712 -2146824576 0x800A0E80</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="7e5191c87692a08cb12040fec2643746" id="tgt123" class="tgtSentence">Operation has been canceled by the user.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1e9628b77d34f2e1a545f9dc72aeb385" id="tgt124" class="tgtSentence">adErrOutOfSpace</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="242830f6f523b256ef7ffc387fe3d257" id="tgt125" class="tgtSentence">3734 -2146824554 0x800A0E96</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="90ea01da8010bd5d6b8f93b1a97cea52" id="tgt126" class="tgtSentence">Operation cannot be performed.</caps:sentence>
                  <caps:sentence sentenceid="4a9e098bb4c35472495cacb30dcc96b9" id="tgt127" class="tgtSentence"> Provider cannot obtain enough storage space.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="1f70cde482ee9a1ded9036ccf3e9e757" id="tgt128" class="tgtSentence">adErrPermissionDenied</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b8935beb7ad48ecd467bdfcf84355e6a" id="tgt129" class="tgtSentence">3720 -2146824568 0x800A0E88</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8046c352cc2db8155331b20f69e9ba6d" id="tgt130" class="tgtSentence">Insufficient permission prevents writing to the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="d75ad83df371afe1934c93d354025f03" id="tgt131" class="tgtSentence">adErrProviderFailed</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="eafd15dbe8399ba1f9197751600850a5" id="tgt132" class="tgtSentence">3000 -2146825288 0x800A0BB8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b1774743fc74c36a871d459c49f043d8" id="tgt133" class="tgtSentence">Provider did not perform the requested operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3cd3e9e639bdb1e5d0ed4955636278ad" id="tgt134" class="tgtSentence">adErrProviderNotFound</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="22137880c3f646a34e19b3ef3b9dbb28" id="tgt135" class="tgtSentence">3706 -2146824582 0x800A0E7A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="494a7842b31f54c0d62e4053891b680c" id="tgt136" class="tgtSentence">Provider cannot be found.</caps:sentence>
                  <caps:sentence sentenceid="eee61525ae5bae157b6d146d3a113992" id="tgt137" class="tgtSentence"> It may not be correctly installed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="b77e023dc7b95bc5d65bd93ac55cbccb" id="tgt138" class="tgtSentence">adErrReadFile</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d47d2d15831dd93873c4c1210954cdf0" id="tgt139" class="tgtSentence">3003 -2146825285 0x800A0BBB</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c452f28098c0f42979b0b0f49fe8810f" id="tgt140" class="tgtSentence">File could not be read.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="74b55526ce103018ec8c14a40d78a18a" id="tgt141" class="tgtSentence">adErrResourceExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c7ff815c3f5de04139ae57d5cc2db87d" id="tgt142" class="tgtSentence">3731 -2146824557 0x800A0E93</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="044bc9d3d6b3a998156449705513b8fd" id="tgt143" class="tgtSentence">Copy operation cannot be performed.</caps:sentence>
                  <caps:sentence sentenceid="c223ff5a8dd5a041e026cec1a4507c70" id="tgt144" class="tgtSentence"> Object named by destination URL already exists.</caps:sentence>
                  <caps:sentence sentenceid="e8088e2075d6d4b8ddb332493ae57e2e" id="tgt145" class="tgtSentence"> Specify <legacyBold>adCopyOverwrite</legacyBold> to replace the object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="323b38eb44cdee770bc206ce41cd02d1" id="tgt146" class="tgtSentence">adErrResourceLocked</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d085c20e863026ece71dd22e3b52880e" id="tgt147" class="tgtSentence">3730 -2146824558 0x800A0E92</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b0d9568cd4d358547ae2fc184a2a5620" id="tgt148" class="tgtSentence">Object represented by the specified URL is locked by one or more other processes.</caps:sentence>
                  <caps:sentence sentenceid="63f192fc4f92d90a94a3064636267677" id="tgt149" class="tgtSentence"> Wait until the process has finished and try the operation again.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="70f3101b0878148f8f2effa19cd05255" id="tgt150" class="tgtSentence">adErrResourceOutOfScope</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a5046162f7aa2b529b844998557e1895" id="tgt151" class="tgtSentence">3735 -2146824553 0x800A0E97</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="79db6534060533bad96e00b28466eb88" id="tgt152" class="tgtSentence">Source or destination URL is outside the scope of the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="c1cd27c6c0b89e1d9a79b6556b739add" id="tgt153" class="tgtSentence">adErrSchemaViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="53daf584f261e44b958b36f14eb0e98f" id="tgt154" class="tgtSentence">3722 -2146824566 0x800A0E8A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="24f2de2d2ffb5b936cf81654ea490530" id="tgt155" class="tgtSentence">Data value conflicts with the data type or constraints of the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="908aacdf057c6672b0c600bbe5852f5e" id="tgt156" class="tgtSentence">adErrSignMismatch</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="51cf123e348360ca56be22b86805745b" id="tgt157" class="tgtSentence">3723 -2146824565 0x800A0E8B</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="bcd3581be7efca5337e4fa5e2d9de71f" id="tgt158" class="tgtSentence">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="f423bd7deeaee58d6bf0682890adc917" id="tgt159" class="tgtSentence">adErrStillConnecting</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="712dbd5959e46ab6de4925e3d1b71ca4" id="tgt160" class="tgtSentence">3713 -2146824575 0x800A0E81</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0a0a934682cdcc54f368c052dabba12d" id="tgt161" class="tgtSentence">Operation cannot be performed while connecting asynchronously.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="3a259aa4c2b72bee47f9770f5874381e" id="tgt162" class="tgtSentence">adErrStillExecuting</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9a309d7fd0882e74fc4e5629186bdf19" id="tgt163" class="tgtSentence">3711 -2146824577 0x800A0E7F</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f6293da9724c9638e87e1802438ae7b8" id="tgt164" class="tgtSentence">Operation cannot be performed while executing asynchronously.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="e832d77749ab99284a649432cbc86d27" id="tgt165" class="tgtSentence">adErrTreePermissionDenied</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="20bfd9db7f48e46222e132d736f80b1d" id="tgt166" class="tgtSentence">3728 -2146824560 0x800A0E90</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="41b87c5dee1e655921d9908f672380e7" id="tgt167" class="tgtSentence">Permissions are insufficient to access tree or subtree.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="fe2cc8b8aa6b3a83fee7a94e2af5e657" id="tgt168" class="tgtSentence">adErrUnavailable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d2b15144f903e43c776d7cedba1025c0" id="tgt169" class="tgtSentence">3736 -2146824552 0x800A0E98</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b45caf9520f80d3b822e6580ab81c95b" id="tgt170" class="tgtSentence">Operation did not complete and the status is unavailable.</caps:sentence>
                  <caps:sentence sentenceid="3835735f5d7033f0221ef20d578c14bb" id="tgt171" class="tgtSentence"> The field may be unavailable or the operation was not attempted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="f6ef47cd13e2d06b0268b8af04f409bf" id="tgt172" class="tgtSentence">adErrUnsafeOperation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c57dc373f9f5920e7e4823c4fe4c9900" id="tgt173" class="tgtSentence">3716 -2146824572 0x800A0E84</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a0fc8f4a7f16292f706c09eb9d461110" id="tgt174" class="tgtSentence">Safety settings on this computer prevent accessing a data source on another domain.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="fb2730e5ec1cb47c3a8a0f503ba6ab68" id="tgt175" class="tgtSentence">adErrURLDoesNotExist</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ad3a196be96b597d3d4fea54afa6d963" id="tgt176" class="tgtSentence">3727 -2146824561 0x800A0E8F</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b4bdaa76c73e049d0ebd5bf933a7d255" id="tgt177" class="tgtSentence">Either the source URL or the parent of the destination URL does not exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="b5aea24e0e9016d884dae081c7188a52" id="tgt178" class="tgtSentence">adErrURLNamedRowDoesNotExist</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0ba1b716335156a62cba6e633cd41072" id="tgt179" class="tgtSentence">3737 -2146824551 0x800A0E99</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2ff7b013f2b727c293209db2f735c683" id="tgt180" class="tgtSentence">Record named by this URL does not exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="82f1f61c6d3dcab1a2cca858515f226f" id="tgt181" class="tgtSentence">adErrVolumeNotFound</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5822b838583c4b5b2f48a7dcb7e29544" id="tgt182" class="tgtSentence">3733 -2146824555 0x800A0E95</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="12f9b1a7d575a973f5b5378c0cdae762" id="tgt183" class="tgtSentence">Provider cannot locate the storage device indicated by the URL.</caps:sentence>
                  <caps:sentence sentenceid="8a3ab5edbda65efb7a654f27c3a5db3d" id="tgt184" class="tgtSentence"> Make sure that the URL is typed correctly.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="075fd4376d167bcd55be28918240914c" id="tgt185" class="tgtSentence">adErrWriteFile</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="760b9f28c825c60fbe3939af361b3604" id="tgt186" class="tgtSentence">3004 -2146825284 0x800A0BBC</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="390bfc036ec1567e9291f9f08e80655a" id="tgt187" class="tgtSentence">Write to file failed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="def2ed5be5ec2fd3554e3bb111b24748" id="tgt188" class="tgtSentence">adWrnSecurityDialog</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f872a299ee8081f1fcd49b2914a5b490" id="tgt189" class="tgtSentence">3717 -2146824571 0x800A0E85</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b88803d94826b8c1fa07949132d711e5" id="tgt190" class="tgtSentence">For internal use only.</caps:sentence>
                  <caps:sentence sentenceid="96e5fae8aaffcbd7228c5a2af38aea72" id="tgt191" class="tgtSentence"> Do not use.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence sentenceid="23ca00192239b4721d643d5b92a80f6d" id="tgt192" class="tgtSentence">adWrnSecurityDialogHeader</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2a543d3c385267e805e2ebc3ba3038ce" id="tgt193" class="tgtSentence">3718 -2146824570 0x800A0E86</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b88803d94826b8c1fa07949132d711e5" id="tgt194" class="tgtSentence">For internal use only.</caps:sentence>
                  <caps:sentence sentenceid="96e5fae8aaffcbd7228c5a2af38aea72" id="tgt195" class="tgtSentence"> Do not use.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a6dc3038423486f2c8833a3eba25ddab" id="tgt196" class="tgtSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6eab1e0da1f7674de7a4ea00cbba8ea9" id="tgt197" class="tgtSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="24a88804d590812d280d5ac3c0254ec5" id="tgt198" class="tgtSentence">Only the following subsets of ADO/WFC equivalents are defined.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt199" class="tgtSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a303b297092feef0aa30f3a30c495ea3" id="tgt200" class="tgtSentence">AdoEnums.ErrorValue.BOUNDTOCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f832254c32a36882fe8f82be80bde1a" id="tgt201" class="tgtSentence">AdoEnums.ErrorValue.DATACONVERSION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6981320e49fac2bcb2856402a3a79ac8" id="tgt202" class="tgtSentence">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="874f6241e1e0d8f6565ba7e45906e7a5" id="tgt203" class="tgtSentence">AdoEnums.ErrorValue.ILLEGALOPERATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="afd7883d064974b510e576cc745ebb75" id="tgt204" class="tgtSentence">AdoEnums.ErrorValue.INTRANSACTION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="73157c3a0d229638fbd2c03bbc0c8a84" id="tgt205" class="tgtSentence">AdoEnums.ErrorValue.INVALIDARGUMENT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ba07bcce8d0cba9a4e96c765924ebef" id="tgt206" class="tgtSentence">AdoEnums.ErrorValue.INVALIDCONNECTION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1e5d105df87b50929e317a5a94ded27c" id="tgt207" class="tgtSentence">AdoEnums.ErrorValue.INVALIDPARAMINFO</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="15905cf4707d33e707cbb347a746a351" id="tgt208" class="tgtSentence">AdoEnums.ErrorValue.ITEMNOTFOUND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5c0f6a67fec3fbb1d80efa06f1142a40" id="tgt209" class="tgtSentence">AdoEnums.ErrorValue.NOCURRENTRECORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5ff8c7e2b3c0774f3e9251e6defff789" id="tgt210" class="tgtSentence">AdoEnums.ErrorValue.NOTEXECUTING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="286176773d5f571420adfb1296fe768c" id="tgt211" class="tgtSentence">AdoEnums.ErrorValue.NOTREENTRANT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1b55a94c421569176cce8b98e102e7b1" id="tgt212" class="tgtSentence">AdoEnums.ErrorValue.OBJECTCLOSED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98f49cc428fbf1029555f12f0ea32ee8" id="tgt213" class="tgtSentence">AdoEnums.ErrorValue.OBJECTINCOLLECTION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b07f96a0520a694049ef72ca60b88f49" id="tgt214" class="tgtSentence">AdoEnums.ErrorValue.OBJECTNOTSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a68d1f3eb3f3d8ba6f95b97418fe49b9" id="tgt215" class="tgtSentence">AdoEnums.ErrorValue.OBJECTOPEN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3174f148f0931486c0840eae5e33dc13" id="tgt216" class="tgtSentence">AdoEnums.ErrorValue.OPERATIONCANCELLED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="63ae32d6092c7ab34adae3c7f873fcc3" id="tgt217" class="tgtSentence">AdoEnums.ErrorValue.PROVIDERNOTFOUND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="175c29ff97fc670dc975e6433b828f9b" id="tgt218" class="tgtSentence">AdoEnums.ErrorValue.STILLCONNECTING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18c47a62c9cd04e12fd42be55789975b" id="tgt219" class="tgtSentence">AdoEnums.ErrorValue.STILLEXECUTING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fa98c8b28b81c40c9313ed6c1a99df27" id="tgt220" class="tgtSentence">AdoEnums.ErrorValue.UNSAFEOPERATION</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt221" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number Property</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3aee61c7-a9b7-4596-b78e-5828a00d0281">ADO Error Codes</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Specifies the type of ADO run-time error.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Three forms of the error number are listed:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Positive decimal—The low two bytes of the full number in decimal format.</caps:sentence>
              <caps:sentence id="src4" class="srcSentence"> This number is displayed in the default Visual Basic error message dialog box.</caps:sentence>
              <caps:sentence id="src5" class="srcSentence"> For example, Run-time error '3707'.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Negative decimal—The decimal translation of the full error number.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Hexadecimal—The hexadecimal representation of the full error number.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> The Windows facility code is in the fourth digit.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> The facility code for ADO error numbers is <legacyItalic>A</legacyItalic>.</caps:sentence>
              <caps:sentence id="src10" class="srcSentence"> For example: 0x800<legacyBold><legacyItalic>A</legacyItalic></legacyBold>0E7B.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src11" class="srcSentence">OLE DB errors may be passed to your ADO application.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Typically, these can be identified by a Windows facility code of <legacyItalic>4</legacyItalic>.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> For example, 0x800<legacyBold><legacyItalic>4</legacyItalic></legacyBold>.</caps:sentence>
          </para>
        </alert>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Value</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src17" class="srcSentence">adErrBoundToCommand</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">3707 -2146824581 0x800A0E7B</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Cannot change the <legacyBold>ActiveConnection</legacyBold> property of a <legacyBold>Recordset</legacyBold> object that has a <legacyBold>Command</legacyBold> object as its source.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src20" class="srcSentence">adErrCannotComplete</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">3732 -2146824556 0x800A0E94</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Server cannot complete the operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src23" class="srcSentence">adErrCantChangeConnection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">3748 -2146824540 0x800A0EA4</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Connection was denied.</caps:sentence>
                  <caps:sentence id="src26" class="srcSentence"> New connection you requested has different characteristics than the one already being used.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src27" class="srcSentence">adErrCantChangeProvider</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">3220 -2146825068 0X800A0C94</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">Supplied provider differs from the one already being used.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src30" class="srcSentence">adErrCantConvertvalue</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">3724 -2146824564 0x800A0E8C</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Data value cannot be converted for reasons other than sign mismatch or data overflow.</caps:sentence>
                  <caps:sentence id="src33" class="srcSentence"> For example, conversion would have truncated data.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src34" class="srcSentence">adErrCantCreate</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">3725 -2146824563 0x800A0E8D</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src37" class="srcSentence">adErrCatalogNotSet</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">3747 -2146824541 0x800A0EA3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">Operation requires a valid <legacyBold>ParentCatalog</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src40" class="srcSentence">adErrColumnNotOnThisRow</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src41" class="srcSentence">3726 -2146824562 0x800A0E8E</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src42" class="srcSentence">Record does not contain this field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src43" class="srcSentence">adErrDataConversion</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src44" class="srcSentence">3421 -2146824867 0x800A0D5D</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src45" class="srcSentence">Application uses a value of the wrong type for the current operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src46" class="srcSentence">adErrDataOverflow</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src47" class="srcSentence">3721 -2146824567 0x800A0E89</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src48" class="srcSentence">Data value is too large to be represented by the field data type.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src49" class="srcSentence">adErrDelResOutOfScope</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src50" class="srcSentence">3738 -2146824550 0x800A0E9A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src51" class="srcSentence">URL of the object to be deleted is outside the scope of the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src52" class="srcSentence">adErrDenyNotSupported</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src53" class="srcSentence">3750 -2146824538 0x800A0EA6</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src54" class="srcSentence">Provider does not support sharing restrictions.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src55" class="srcSentence">adErrDenyTypeNotSupported</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src56" class="srcSentence">3751 -2146824537 0x800A0EA7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src57" class="srcSentence">Provider does not support the requested kind of sharing restriction.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src58" class="srcSentence">adErrFeatureNotAvailable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src59" class="srcSentence">3251 -2146825037 0x800A0CB3</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src60" class="srcSentence">Object or provider is not able to perform requested operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src61" class="srcSentence">adErrFieldsUpdateFailed</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src62" class="srcSentence">3749 -2146824539 0x800A0EA5</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src63" class="srcSentence">Fields update failed.</caps:sentence>
                  <caps:sentence id="src64" class="srcSentence"> For more information, examine the <legacyBold>Status </legacyBold>property of individual field objects.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src65" class="srcSentence">adErrIllegalOperation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src66" class="srcSentence">3219 -2146825069 0x800A0C93</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src67" class="srcSentence">Operation is not allowed in this context.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src68" class="srcSentence">adErrIntegrityViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src69" class="srcSentence">3719 -2146824569 0x800A0E87</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src70" class="srcSentence">Data value conflicts with the integrity constraints of the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src71" class="srcSentence">adErrInTransaction</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src72" class="srcSentence">3246 -2146825042 0x800A0CAE</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src73" class="srcSentence">
                    <legacyBold>Connection</legacyBold> object cannot be explicitly closed while in a transaction.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src74" class="srcSentence">adErrInvalidArgument</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src75" class="srcSentence">3001 -2146825287 0x800A0BB9</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src76" class="srcSentence">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src77" class="srcSentence">adErrInvalidConnection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src78" class="srcSentence">3709 -2146824579 0x800A0E7D</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src79" class="srcSentence">The connection cannot be used to perform this operation.</caps:sentence>
                  <caps:sentence id="src80" class="srcSentence"> It is either closed or invalid in this context.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src81" class="srcSentence">adErrInvalidParamInfo</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src82" class="srcSentence">3708 -2146824580 0x800A0E7C</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src83" class="srcSentence">
                    <legacyBold>Parameter</legacyBold> object is incorrectly defined.</caps:sentence>
                  <caps:sentence id="src84" class="srcSentence"> Inconsistent or incomplete information was provided.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src85" class="srcSentence">adErrInvalidTransaction</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src86" class="srcSentence">3714 -2146824574 0x800A0E82</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src87" class="srcSentence">Coordinating transaction is invalid or has not started.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src88" class="srcSentence">adErrInvalidURL</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src89" class="srcSentence">3729 -2146824559 0x800A0E91</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src90" class="srcSentence">URL contains invalid characters.</caps:sentence>
                  <caps:sentence id="src91" class="srcSentence"> Make sure that the URL is typed correctly.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src92" class="srcSentence">adErrItemNotFound</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src93" class="srcSentence">3265 -2146825023 0x800A0CC1</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src94" class="srcSentence">Item cannot be found in the collection that corresponds to the requested name or ordinal.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src95" class="srcSentence">adErrNoCurrentRecord</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src96" class="srcSentence">3021 -2146825267 0x800A0BCD</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src97" class="srcSentence">Either <legacyBold>BOF</legacyBold> or <legacyBold>EOF</legacyBold> is True, or the current record has been deleted.</caps:sentence>
                  <caps:sentence id="src98" class="srcSentence"> Requested operation requires a current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src99" class="srcSentence">adErrNotExecuting</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src100" class="srcSentence">3715 -2146824573 0x800A0E83</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src101" class="srcSentence">Operation cannot be performed while not executing.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src102" class="srcSentence">adErrNotReentrant</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src103" class="srcSentence">3710 -2146824578 0x800A0E7E</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src104" class="srcSentence">Operation cannot be performed while processing event.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src105" class="srcSentence">adErrObjectClosed</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src106" class="srcSentence">3704 -2146824584 0x800A0E78</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src107" class="srcSentence">Operation is not allowed when the object is closed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src108" class="srcSentence">adErrObjectInCollection</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src109" class="srcSentence">3367 -2146824921 0x800A0D27</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src110" class="srcSentence">Object is already in collection.</caps:sentence>
                  <caps:sentence id="src111" class="srcSentence"> Cannot append.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src112" class="srcSentence">adErrObjectNotSet</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src113" class="srcSentence">3420 -2146824868 0x800A0D5C</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src114" class="srcSentence">Object is no longer valid.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src115" class="srcSentence">adErrObjectOpen</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src116" class="srcSentence">3705 -2146824583 0x800A0E79</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src117" class="srcSentence">Operation is not allowed when the object is open.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src118" class="srcSentence">adErrOpeningFile</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src119" class="srcSentence">3002 -2146825286 0x800A0BBA</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src120" class="srcSentence">File could not be opened.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src121" class="srcSentence">adErrOperationCancelled</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src122" class="srcSentence">3712 -2146824576 0x800A0E80</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src123" class="srcSentence">Operation has been canceled by the user.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src124" class="srcSentence">adErrOutOfSpace</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src125" class="srcSentence">3734 -2146824554 0x800A0E96</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src126" class="srcSentence">Operation cannot be performed.</caps:sentence>
                  <caps:sentence id="src127" class="srcSentence"> Provider cannot obtain enough storage space.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src128" class="srcSentence">adErrPermissionDenied</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src129" class="srcSentence">3720 -2146824568 0x800A0E88</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src130" class="srcSentence">Insufficient permission prevents writing to the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src131" class="srcSentence">adErrProviderFailed</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src132" class="srcSentence">3000 -2146825288 0x800A0BB8</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src133" class="srcSentence">Provider did not perform the requested operation.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src134" class="srcSentence">adErrProviderNotFound</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src135" class="srcSentence">3706 -2146824582 0x800A0E7A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src136" class="srcSentence">Provider cannot be found.</caps:sentence>
                  <caps:sentence id="src137" class="srcSentence"> It may not be correctly installed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src138" class="srcSentence">adErrReadFile</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src139" class="srcSentence">3003 -2146825285 0x800A0BBB</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src140" class="srcSentence">File could not be read.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src141" class="srcSentence">adErrResourceExists</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src142" class="srcSentence">3731 -2146824557 0x800A0E93</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src143" class="srcSentence">Copy operation cannot be performed.</caps:sentence>
                  <caps:sentence id="src144" class="srcSentence"> Object named by destination URL already exists.</caps:sentence>
                  <caps:sentence id="src145" class="srcSentence"> Specify <legacyBold>adCopyOverwrite</legacyBold> to replace the object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src146" class="srcSentence">adErrResourceLocked</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src147" class="srcSentence">3730 -2146824558 0x800A0E92</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src148" class="srcSentence">Object represented by the specified URL is locked by one or more other processes.</caps:sentence>
                  <caps:sentence id="src149" class="srcSentence"> Wait until the process has finished and try the operation again.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src150" class="srcSentence">adErrResourceOutOfScope</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src151" class="srcSentence">3735 -2146824553 0x800A0E97</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src152" class="srcSentence">Source or destination URL is outside the scope of the current record.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src153" class="srcSentence">adErrSchemaViolation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src154" class="srcSentence">3722 -2146824566 0x800A0E8A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src155" class="srcSentence">Data value conflicts with the data type or constraints of the field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src156" class="srcSentence">adErrSignMismatch</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src157" class="srcSentence">3723 -2146824565 0x800A0E8B</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src158" class="srcSentence">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src159" class="srcSentence">adErrStillConnecting</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src160" class="srcSentence">3713 -2146824575 0x800A0E81</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src161" class="srcSentence">Operation cannot be performed while connecting asynchronously.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src162" class="srcSentence">adErrStillExecuting</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src163" class="srcSentence">3711 -2146824577 0x800A0E7F</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src164" class="srcSentence">Operation cannot be performed while executing asynchronously.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src165" class="srcSentence">adErrTreePermissionDenied</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src166" class="srcSentence">3728 -2146824560 0x800A0E90</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src167" class="srcSentence">Permissions are insufficient to access tree or subtree.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src168" class="srcSentence">adErrUnavailable</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src169" class="srcSentence">3736 -2146824552 0x800A0E98</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src170" class="srcSentence">Operation did not complete and the status is unavailable.</caps:sentence>
                  <caps:sentence id="src171" class="srcSentence"> The field may be unavailable or the operation was not attempted.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src172" class="srcSentence">adErrUnsafeOperation</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src173" class="srcSentence">3716 -2146824572 0x800A0E84</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src174" class="srcSentence">Safety settings on this computer prevent accessing a data source on another domain.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src175" class="srcSentence">adErrURLDoesNotExist</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src176" class="srcSentence">3727 -2146824561 0x800A0E8F</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src177" class="srcSentence">Either the source URL or the parent of the destination URL does not exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src178" class="srcSentence">adErrURLNamedRowDoesNotExist</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src179" class="srcSentence">3737 -2146824551 0x800A0E99</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src180" class="srcSentence">Record named by this URL does not exist.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src181" class="srcSentence">adErrVolumeNotFound</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src182" class="srcSentence">3733 -2146824555 0x800A0E95</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src183" class="srcSentence">Provider cannot locate the storage device indicated by the URL.</caps:sentence>
                  <caps:sentence id="src184" class="srcSentence"> Make sure that the URL is typed correctly.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src185" class="srcSentence">adErrWriteFile</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src186" class="srcSentence">3004 -2146825284 0x800A0BBC</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src187" class="srcSentence">Write to file failed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src188" class="srcSentence">adWrnSecurityDialog</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src189" class="srcSentence">3717 -2146824571 0x800A0E85</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src190" class="srcSentence">For internal use only.</caps:sentence>
                  <caps:sentence id="src191" class="srcSentence"> Do not use.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <legacyBold>
                    <caps:sentence id="src192" class="srcSentence">adWrnSecurityDialogHeader</caps:sentence>
                  </legacyBold>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src193" class="srcSentence">3718 -2146824570 0x800A0E86</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src194" class="srcSentence">For internal use only.</caps:sentence>
                  <caps:sentence id="src195" class="srcSentence"> Do not use.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src196" class="srcSentence">ADO/WFC Equivalent</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src197" class="srcSentence">Package: <legacyBold>com.ms.wfc.data</legacyBold></caps:sentence>
          </para>
          <para>
            <caps:sentence id="src198" class="srcSentence">Only the following subsets of ADO/WFC equivalents are defined.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">Constant</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">AdoEnums.ErrorValue.BOUNDTOCOMMAND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">AdoEnums.ErrorValue.DATACONVERSION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">AdoEnums.ErrorValue.ILLEGALOPERATION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">AdoEnums.ErrorValue.INTRANSACTION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">AdoEnums.ErrorValue.INVALIDARGUMENT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src206" class="srcSentence">AdoEnums.ErrorValue.INVALIDCONNECTION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">AdoEnums.ErrorValue.INVALIDPARAMINFO</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src208" class="srcSentence">AdoEnums.ErrorValue.ITEMNOTFOUND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">AdoEnums.ErrorValue.NOCURRENTRECORD</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src210" class="srcSentence">AdoEnums.ErrorValue.NOTEXECUTING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src211" class="srcSentence">AdoEnums.ErrorValue.NOTREENTRANT</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">AdoEnums.ErrorValue.OBJECTCLOSED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">AdoEnums.ErrorValue.OBJECTINCOLLECTION</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">AdoEnums.ErrorValue.OBJECTNOTSET</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src215" class="srcSentence">AdoEnums.ErrorValue.OBJECTOPEN</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src216" class="srcSentence">AdoEnums.ErrorValue.OPERATIONCANCELLED</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src217" class="srcSentence">AdoEnums.ErrorValue.PROVIDERNOTFOUND</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src218" class="srcSentence">AdoEnums.ErrorValue.STILLCONNECTING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src219" class="srcSentence">AdoEnums.ErrorValue.STILLEXECUTING</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src220" class="srcSentence">AdoEnums.ErrorValue.UNSAFEOPERATION</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src221" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="f92323c5-dd11-4a63-a505-d9014a0f067f">Number Property</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3aee61c7-a9b7-4596-b78e-5828a00d0281">ADO Error Codes</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
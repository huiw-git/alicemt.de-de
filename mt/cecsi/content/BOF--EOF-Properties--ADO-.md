---
title: "BOF, EOF Properties (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 36c31ab2-f3b6-4281-89b6-db7e04e38fd2
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
# BOF, EOF Properties (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="02a5e5af5ee6de1dd50e8b094ea30de8" id="tgt1" class="tgtSentence">
                <legacyBold>BOF</legacyBold>     Indicates that the current record position is before the first record in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="15138d9c46897f68fac7d0f21948fa8f" id="tgt2" class="tgtSentence">
                <legacyBold>EOF</legacyBold>     Indicates that the current record position is after the last record in a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt3" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="816347951f67d24ba94c43f45ae07376" id="tgt4" class="tgtSentence">The <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties return <languageKeyword>Boolean</languageKeyword> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="8d6c14da18f528211f8c524a771f2003" id="tgt5" class="tgtSentence">Use the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties to determine whether a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object contains records or whether you have gone beyond the limits of a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object when you move from record to record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0daf8f5bb66af8124224e48c2fe5a961" id="tgt6" class="tgtSentence">The <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> property returns <languageKeyword>True</languageKeyword> (-1) if the current record position is before the first record and <languageKeyword>False</languageKeyword> (0) if the current record position is on or after the first record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1af3adbbf7db1faa27fcb5edb2670e7d" id="tgt7" class="tgtSentence">The <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> property returns <languageKeyword>True</languageKeyword> if the current record position is after the last record and <languageKeyword>False</languageKeyword> if the current record position is on or before the last record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="35d1f75411ec7da7646d63026c6b7509" id="tgt8" class="tgtSentence">If either the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> property is <languageKeyword>True</languageKeyword>, there is no current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0b44b32ce1f028d4bc909db934c01344" id="tgt9" class="tgtSentence">If you open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object containing no records, the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties are set to <languageKeyword>True</languageKeyword> (see the <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink> property for more information about this state of a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>).</caps:sentence>
            <caps:sentence sentenceid="60e1430e9a6e85577931c3f4c654ade7" id="tgt10" class="tgtSentence"> When you open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object that contains at least one record, the first record is the current record and the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties are <languageKeyword>False</languageKeyword>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="30f6f3c06e1277711e90343a421aa8b3" id="tgt11" class="tgtSentence">If you delete the last remaining record in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties may remain <languageKeyword>False</languageKeyword> until you attempt to reposition the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fa9cebacb4a0a1f7be14a5d2a189171e" id="tgt12" class="tgtSentence">This table shows which <legacyBold>Move</legacyBold> methods are allowed with different combinations of the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17ccb3c4610a519d1ff8a72a35375b6c" id="tgt13" class="tgtSentence">
                      <legacyBold> </legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8c0e4042bf92a624a930e1eabffc1d33" id="tgt14" class="tgtSentence">MoveFirst,</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="aa4486cbb251418b54bf37a38e07877d" id="tgt15" class="tgtSentence">MoveLast</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0026203374d8ea84d4a013fa08d3fcff" id="tgt16" class="tgtSentence">MovePrevious,</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1c499b86b2e4d22445360f91198d62be" id="tgt17" class="tgtSentence">Move &lt; 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d985b49bef3a49fd9e4f65751bc1210a" id="tgt18" class="tgtSentence">Move 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b4cbb1696921e55d58b38393901c9f2c" id="tgt19" class="tgtSentence">MoveNext,</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d13578c31f385a8123887d115e322bd6" id="tgt20" class="tgtSentence">Move &gt; 0</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7b413a9f121c74dc867133afc4074809" id="tgt21" class="tgtSentence">
                      <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference>=<languageKeyword>True</languageKeyword>, <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference>=<languageKeyword>False</languageKeyword> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22ee71e9dcc9ca12fc313c6e1ce3f806" id="tgt22" class="tgtSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt23" class="tgtSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt24" class="tgtSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22ee71e9dcc9ca12fc313c6e1ce3f806" id="tgt25" class="tgtSentence">Allowed</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="69a0ea9d5ae2f378bec59812bace8926" id="tgt26" class="tgtSentence">
                      <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference>=<languageKeyword>False</languageKeyword>, <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference>=<languageKeyword>True</languageKeyword> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22ee71e9dcc9ca12fc313c6e1ce3f806" id="tgt27" class="tgtSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22ee71e9dcc9ca12fc313c6e1ce3f806" id="tgt28" class="tgtSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt29" class="tgtSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt30" class="tgtSentence">Error</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4cc57633c089ec52158fff60059f7372" id="tgt31" class="tgtSentence">Both <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt32" class="tgtSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt33" class="tgtSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt34" class="tgtSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb5e100e5a9a3e7f6d1fd97512215282" id="tgt35" class="tgtSentence">Error</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="237abe5bbfdeb376c061582e72b5aa27" id="tgt36" class="tgtSentence">Both <languageKeyword>False</languageKeyword></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22ee71e9dcc9ca12fc313c6e1ce3f806" id="tgt37" class="tgtSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22ee71e9dcc9ca12fc313c6e1ce3f806" id="tgt38" class="tgtSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22ee71e9dcc9ca12fc313c6e1ce3f806" id="tgt39" class="tgtSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22ee71e9dcc9ca12fc313c6e1ce3f806" id="tgt40" class="tgtSentence">Allowed</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="e343a9894a059dfc91bf9c166db1b9fe" id="tgt41" class="tgtSentence">Allowing a <legacyBold>Move</legacyBold> method does not guarantee that the method will successfully locate a record; it only means that calling the specified <legacyBold>Move</legacyBold> method will not generate an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b61e989716f28c95bb8987f1cd3e8185" id="tgt42" class="tgtSentence">The following table shows what happens to the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> property settings when you call various <legacyBold>Move</legacyBold> methods but are unable to successfully locate a record.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17ccb3c4610a519d1ff8a72a35375b6c" id="tgt43" class="tgtSentence">
                      <legacyBold> </legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c9a3639b57c741dcd0334c28032e4280" id="tgt44" class="tgtSentence">BOF</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2e51b1ab42e8a4a67f3445174be5191b" id="tgt45" class="tgtSentence">EOF</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e337f992a9ddcb2aafeb021bd51ddf2f" id="tgt46" class="tgtSentence">
                      <legacyBold>MoveFirst</legacyBold>, <legacyBold>MoveLast</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26c671bb351c73504f878f0437ef0557" id="tgt47" class="tgtSentence">Set to <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26c671bb351c73504f878f0437ef0557" id="tgt48" class="tgtSentence">Set to <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1b89cb6b548ebcf7546808cde830807d" id="tgt49" class="tgtSentence">
                      <legacyBold>Move</legacyBold> 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="66d22a5d2567b9fe66598b724f1e1ace" id="tgt50" class="tgtSentence">No change</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="66d22a5d2567b9fe66598b724f1e1ace" id="tgt51" class="tgtSentence">No change</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1fef78424bf0352491c2a5c802bb2135" id="tgt52" class="tgtSentence">
                      <legacyBold>MovePrevious</legacyBold>, <legacyBold>Move</legacyBold> &lt; 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26c671bb351c73504f878f0437ef0557" id="tgt53" class="tgtSentence">Set to <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="66d22a5d2567b9fe66598b724f1e1ace" id="tgt54" class="tgtSentence">No change</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="00a3afbdec8b39787f263dca5fa1d0d8" id="tgt55" class="tgtSentence">
                      <legacyBold>MoveNext</legacyBold>, <legacyBold>Move</legacyBold> &gt; 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="66d22a5d2567b9fe66598b724f1e1ace" id="tgt56" class="tgtSentence">No change</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="26c671bb351c73504f878f0437ef0557" id="tgt57" class="tgtSentence">Set to <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt58" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b6573c6e-fee8-4267-a722-fadaec6eafe6">Visual Basic Example</link>
        <link xlink:href="bd2b9d85-e75e-4fc8-a392-076582019caa">Visual C++ Example</link>
        <link xlink:href="eecd75a8-3e4f-4a18-b1c1-4c053dd7833f">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src1" class="srcSentence">
                <legacyBold>BOF</legacyBold>     Indicates that the current record position is before the first record in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">
                <legacyBold>EOF</legacyBold>     Indicates that the current record position is after the last record in a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties return <languageKeyword>Boolean</languageKeyword> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties to determine whether a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object contains records or whether you have gone beyond the limits of a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object when you move from record to record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">The <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> property returns <languageKeyword>True</languageKeyword> (-1) if the current record position is before the first record and <languageKeyword>False</languageKeyword> (0) if the current record position is on or after the first record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">The <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> property returns <languageKeyword>True</languageKeyword> if the current record position is after the last record and <languageKeyword>False</languageKeyword> if the current record position is on or before the last record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">If either the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> or <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> property is <languageKeyword>True</languageKeyword>, there is no current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">If you open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object containing no records, the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties are set to <languageKeyword>True</languageKeyword> (see the <legacyLink xlink:href="834f0121-394a-44d4-ad7d-999b43a6fe63">RecordCount</legacyLink> property for more information about this state of a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference>).</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> When you open a <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object that contains at least one record, the first record is the current record and the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties are <languageKeyword>False</languageKeyword>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If you delete the last remaining record in the <unmanagedCodeEntityReference>Recordset</unmanagedCodeEntityReference> object, the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties may remain <languageKeyword>False</languageKeyword> until you attempt to reposition the current record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">This table shows which <legacyBold>Move</legacyBold> methods are allowed with different combinations of the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> properties.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">
                      <legacyBold> </legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">MoveFirst,</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">MoveLast</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">MovePrevious,</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Move &lt; 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Move 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">MoveNext,</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Move &gt; 0</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">
                      <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference>=<languageKeyword>True</languageKeyword>, <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference>=<languageKeyword>False</languageKeyword> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Allowed</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">
                      <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference>=<languageKeyword>False</languageKeyword>, <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference>=<languageKeyword>True</languageKeyword> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Error</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Both <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Error</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Error</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Both <languageKeyword>False</languageKeyword></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Allowed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Allowed</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src41" class="srcSentence">Allowing a <legacyBold>Move</legacyBold> method does not guarantee that the method will successfully locate a record; it only means that calling the specified <legacyBold>Move</legacyBold> method will not generate an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src42" class="srcSentence">The following table shows what happens to the <unmanagedCodeEntityReference>BOF</unmanagedCodeEntityReference> and <unmanagedCodeEntityReference>EOF</unmanagedCodeEntityReference> property settings when you call various <legacyBold>Move</legacyBold> methods but are unable to successfully locate a record.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">
                      <legacyBold> </legacyBold> </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">BOF</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">EOF</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">
                      <legacyBold>MoveFirst</legacyBold>, <legacyBold>MoveLast</legacyBold></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Set to <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Set to <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">
                      <legacyBold>Move</legacyBold> 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">No change</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">No change</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">
                      <legacyBold>MovePrevious</legacyBold>, <legacyBold>Move</legacyBold> &lt; 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Set to <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">No change</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">
                      <legacyBold>MoveNext</legacyBold>, <legacyBold>Move</legacyBold> &gt; 0</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">No change</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Set to <languageKeyword>True</languageKeyword></caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src58" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b6573c6e-fee8-4267-a722-fadaec6eafe6">Visual Basic Example</link>
        <link xlink:href="bd2b9d85-e75e-4fc8-a392-076582019caa">Visual C++ Example</link>
        <link xlink:href="eecd75a8-3e4f-4a18-b1c1-4c053dd7833f">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
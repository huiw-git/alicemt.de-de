---
title: "Clone Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: ad49265f-1c05-4271-9bbf-7c00010ac18c
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
# Clone Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7f3e36ea17caa95e77aed30e56f6efac" id="tgt1" class="tgtSentence">Creates a duplicate <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object from an existing <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="e05a271f17e9dbf9e8a3efed4c3cf96c" id="tgt2" class="tgtSentence"> Optionally, specifies that the clone be read-only.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>rstDuplicate</parameterReference> = <parameterReference>rstOriginal</parameterReference>.<legacyBold>Clone (</legacyBold><parameterReference>LockType</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="28dbccfdd55ef79c2c10a9ae31454a3f" id="tgt3" class="tgtSentence">Returns a <legacyBold>Recordset</legacyBold> object reference.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="88534b38763821f3d2775fecccc14366" id="tgt4" class="tgtSentence"> <legacyItalic>rstDuplicate</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="d1c9216d0d18c65a881eaa14946727d6" id="tgt5" class="tgtSentence">An object variable that identifies the duplicate <legacyBold>Recordset</legacyBold> object to be created.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="b546b7611118dd21c73049b10bbb75a5" id="tgt6" class="tgtSentence"> <legacyItalic>rstOriginal</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="6d0582921dce2df8ff3e2a7302707d37" id="tgt7" class="tgtSentence">An object variable that identifies the <legacyBold>Recordset</legacyBold> object to be duplicated.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="00e63dd1871d614041a829c759866a4b" id="tgt8" class="tgtSentence"> <legacyItalic>LockType</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="16c952cba827b0f636670d0a0b4b6619" id="tgt9" class="tgtSentence">Optional.</caps:sentence>
                <caps:sentence sentenceid="ebb517a8a6b07dd65a07e642167ff2ef" id="tgt10" class="tgtSentence"> A <legacyLink xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</legacyLink> value that specifies either the lock type of the original <legacyBold>Recordset</legacyBold>, or a read-only <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="e24f700c1f7b07b50eee41fbb780f5f9" id="tgt11" class="tgtSentence"> Valid values are <legacyBold>adLockUnspecified</legacyBold> or <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="55806e3581713e1e5f8c53306e79d20e" id="tgt12" class="tgtSentence">Use the <legacyBold>Clone</legacyBold> method to create multiple, duplicate <legacyBold>Recordset</legacyBold> objects, especially if you want to maintain more than one current record in a given set of records.</caps:sentence>
            <caps:sentence sentenceid="7405ac9913d838dba14f7a68191aff17" id="tgt13" class="tgtSentence"> Using the <legacyBold>Clone</legacyBold> method is more efficient than creating and opening a new <legacyBold>Recordset</legacyBold> object that uses the same definition as the original.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="330847d85c805dbf197f65bbee1fa19d" id="tgt14" class="tgtSentence">The <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property of the original <legacyBold>Recordset</legacyBold>, if any, will not be applied to the clone.</caps:sentence>
            <caps:sentence sentenceid="b9e0b7ce3459ae9de63edc5eccdcd573" id="tgt15" class="tgtSentence"> Set the <legacyBold>Filter</legacyBold> property of the new <legacyBold>Recordset</legacyBold> to filter the results.</caps:sentence>
            <caps:sentence sentenceid="1480032809ea79dfeb6f5d4ef925bbab" id="tgt16" class="tgtSentence"> The simplest way to copy any existing <legacyBold>Filter</legacyBold> value is to assign it directly, as follows.</caps:sentence>
          </para>
          <code>rsNew.Filter = rsOriginal.Filter</code>
          <para>
            <caps:sentence sentenceid="239b141cba1240ea1785a9dff7fe7bd8" id="tgt17" class="tgtSentence">The current record of a newly created clone is set to the first record.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2d043c07712a0ebc40313ab9daf051db" id="tgt18" class="tgtSentence">Changes you make to one <legacyBold>Recordset</legacyBold> object are visible in all of its clones regardless of cursor type.</caps:sentence>
            <caps:sentence sentenceid="ebdff9f9c2970e70a975021aed19d0ba" id="tgt19" class="tgtSentence"> However, after you execute <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> on the original <legacyBold>Recordset</legacyBold>, the clones will no longer be synchronized to the original.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="27401fb381692f47fbb70743909c05b6" id="tgt20" class="tgtSentence">Closing the original <legacyBold>Recordset</legacyBold> does not close its copies, nor does closing a copy close the original or any of the other copies.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9276247dbfc60bcb2d2c321ee91d64d6" id="tgt21" class="tgtSentence">You can only clone a <legacyBold>Recordset</legacyBold> object that supports bookmarks.</caps:sentence>
            <caps:sentence sentenceid="49bc06483929df883e64b4208205ab13" id="tgt22" class="tgtSentence"> Bookmark values are interchangeable; that is, a bookmark reference from one <legacyBold>Recordset</legacyBold> object refers to the same record in any of its clones.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="60fb56dcde00abfeda8443bd58139ced" id="tgt23" class="tgtSentence">Some <legacyBold>Recordset</legacyBold> events that are triggered will also occur in all <legacyBold>Recordset</legacyBold> clones.</caps:sentence>
            <caps:sentence sentenceid="0fe111307fc70c9193d6f5b814e3e849" id="tgt24" class="tgtSentence"> However, because the current record can differ between cloned <legacyBold>Recordsets</legacyBold>, the events may not be valid for the clone.</caps:sentence>
            <caps:sentence sentenceid="31c67a72e22a368e4a55a956269b5a56" id="tgt25" class="tgtSentence"> For example, if you change a value of a field, a <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField</legacyLink> event will occur in the changed <legacyBold>Recordset</legacyBold> and in all clones.</caps:sentence>
            <caps:sentence sentenceid="9bff79b5d0aa029146076ad14b859f49" id="tgt26" class="tgtSentence"> The <legacyItalic>Fields</legacyItalic> parameter of the <legacyBold>WillChangeField</legacyBold> event of a cloned <legacyBold>Recordset</legacyBold> (where the change was not made) will refer to the fields of the current record of the clone, which may be a different record than the current record of the original <legacyBold>Recordset</legacyBold> where the change occurred.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="53fc25c7a64add24046b2fafb18a05f4" id="tgt27" class="tgtSentence">The following table provides a full listing of all <legacyBold>Recordset</legacyBold> events.</caps:sentence>
            <caps:sentence sentenceid="8825d236a46107d4a4ddc57a29c1619e" id="tgt28" class="tgtSentence"> It indicates whether they are valid and triggered for any recordset clones generated by using the <legacyBold>Clone</legacyBold> method.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4119639092e62c55ea8be348e4d9260d" id="tgt29" class="tgtSentence">Event</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a286e9544099d058fe099f25c28be01b" id="tgt30" class="tgtSentence">Triggered in clones?</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="45dc39bf305686b15d24c24dcb1c8cf5" id="tgt31" class="tgtSentence">
                      <legacyLink xlink:href="475de5e2-f634-4954-9edf-0027a6ba38d6">EndOfRecordset</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt32" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c5d7522e8d9627918984b3ced15448f9" id="tgt33" class="tgtSentence">
                      <legacyLink xlink:href="a28d3858-566c-468d-b070-d1de4339fbea">FetchComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt34" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6b6fcbee0ce47814622ddb772b5c902" id="tgt35" class="tgtSentence">
                      <legacyLink xlink:href="301716fd-81fc-40eb-8a04-221ef7ab410e">FetchProgress</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt36" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b92fd832c20ba91ca693ed0282914623" id="tgt37" class="tgtSentence">
                      <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">FieldChangeComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt38" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d114508c9500ed9d572e29005206fc60" id="tgt39" class="tgtSentence">
                      <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">MoveComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt40" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="03a5c7e97a29fa61b8ca4ba5601a4022" id="tgt41" class="tgtSentence">
                      <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">RecordChangeComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt42" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c289ddf135e2c7ca86fd53a435e55e9f" id="tgt43" class="tgtSentence">
                      <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">RecordsetChangeComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt44" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6bb04e1c77b04c6a9ec5dbd53b657ded" id="tgt45" class="tgtSentence">
                      <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt46" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b33d8ea6c5e0c5db4c0aa20e4caff272" id="tgt47" class="tgtSentence">
                      <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">WillChangeRecord</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt48" class="tgtSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e24c8215ac26e28a89c13bbc5563c329" id="tgt49" class="tgtSentence">
                      <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt50" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6fdfbf3ff4d434976ecc14dcbe50df8a" id="tgt51" class="tgtSentence">
                      <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt52" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt53" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="64cb1753-e074-4a2d-8b74-7c35f3f6f64d">Visual Basic Example</link>
        <link xlink:href="36b96e3d-8cb0-4b79-bd93-ea5e0eb5679f">VBScript Example</link>
        <link xlink:href="7ac96c1d-d0d8-4bf8-b165-533818d0f590">Visual C++ Example</link>
        <link xlink:href="6b699f2b-e5c7-4584-ab25-663a9243d30e">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Creates a duplicate <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object from an existing <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Optionally, specifies that the clone be read-only.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <legacyBold>Set</legacyBold>
          <parameterReference>rstDuplicate</parameterReference> = <parameterReference>rstOriginal</parameterReference>.<legacyBold>Clone (</legacyBold><parameterReference>LockType</parameterReference><legacyBold>)</legacyBold></legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a <legacyBold>Recordset</legacyBold> object reference.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src4" class="srcSentence"> <legacyItalic>rstDuplicate</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src5" class="srcSentence">An object variable that identifies the duplicate <legacyBold>Recordset</legacyBold> object to be created.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>rstOriginal</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">An object variable that identifies the <legacyBold>Recordset</legacyBold> object to be duplicated.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src8" class="srcSentence"> <legacyItalic>LockType</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src9" class="srcSentence">Optional.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> A <legacyLink xlink:href="d2894eaf-4450-4ace-aa51-c8b875fd3010">LockTypeEnum</legacyLink> value that specifies either the lock type of the original <legacyBold>Recordset</legacyBold>, or a read-only <legacyBold>Recordset</legacyBold>.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> Valid values are <legacyBold>adLockUnspecified</legacyBold> or <legacyBold>adLockReadOnly</legacyBold>.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Use the <legacyBold>Clone</legacyBold> method to create multiple, duplicate <legacyBold>Recordset</legacyBold> objects, especially if you want to maintain more than one current record in a given set of records.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> Using the <legacyBold>Clone</legacyBold> method is more efficient than creating and opening a new <legacyBold>Recordset</legacyBold> object that uses the same definition as the original.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src14" class="srcSentence">The <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property of the original <legacyBold>Recordset</legacyBold>, if any, will not be applied to the clone.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> Set the <legacyBold>Filter</legacyBold> property of the new <legacyBold>Recordset</legacyBold> to filter the results.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> The simplest way to copy any existing <legacyBold>Filter</legacyBold> value is to assign it directly, as follows.</caps:sentence>
          </para>
          <code>rsNew.Filter = rsOriginal.Filter</code>
          <para>
            <caps:sentence id="src17" class="srcSentence">The current record of a newly created clone is set to the first record.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">Changes you make to one <legacyBold>Recordset</legacyBold> object are visible in all of its clones regardless of cursor type.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> However, after you execute <legacyLink xlink:href="d81ab76f-1aa8-4ccf-92ec-b65254dc3ea1">Requery</legacyLink> on the original <legacyBold>Recordset</legacyBold>, the clones will no longer be synchronized to the original.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">Closing the original <legacyBold>Recordset</legacyBold> does not close its copies, nor does closing a copy close the original or any of the other copies.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">You can only clone a <legacyBold>Recordset</legacyBold> object that supports bookmarks.</caps:sentence>
            <caps:sentence id="src22" class="srcSentence"> Bookmark values are interchangeable; that is, a bookmark reference from one <legacyBold>Recordset</legacyBold> object refers to the same record in any of its clones.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src23" class="srcSentence">Some <legacyBold>Recordset</legacyBold> events that are triggered will also occur in all <legacyBold>Recordset</legacyBold> clones.</caps:sentence>
            <caps:sentence id="src24" class="srcSentence"> However, because the current record can differ between cloned <legacyBold>Recordsets</legacyBold>, the events may not be valid for the clone.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> For example, if you change a value of a field, a <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField</legacyLink> event will occur in the changed <legacyBold>Recordset</legacyBold> and in all clones.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> The <legacyItalic>Fields</legacyItalic> parameter of the <legacyBold>WillChangeField</legacyBold> event of a cloned <legacyBold>Recordset</legacyBold> (where the change was not made) will refer to the fields of the current record of the clone, which may be a different record than the current record of the original <legacyBold>Recordset</legacyBold> where the change occurred.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">The following table provides a full listing of all <legacyBold>Recordset</legacyBold> events.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> It indicates whether they are valid and triggered for any recordset clones generated by using the <legacyBold>Clone</legacyBold> method.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Event</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Triggered in clones?</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">
                      <legacyLink xlink:href="475de5e2-f634-4954-9edf-0027a6ba38d6">EndOfRecordset</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">
                      <legacyLink xlink:href="a28d3858-566c-468d-b070-d1de4339fbea">FetchComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">
                      <legacyLink xlink:href="301716fd-81fc-40eb-8a04-221ef7ab410e">FetchProgress</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">
                      <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">FieldChangeComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">
                      <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">MoveComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">
                      <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">RecordChangeComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">
                      <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">RecordsetChangeComplete</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">
                      <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">
                      <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">WillChangeRecord</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">
                      <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">
                      <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src53" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="64cb1753-e074-4a2d-8b74-7c35f3f6f64d">Visual Basic Example</link>
        <link xlink:href="36b96e3d-8cb0-4b79-bd93-ea5e0eb5679f">VBScript Example</link>
        <link xlink:href="7ac96c1d-d0d8-4bf8-b165-533818d0f590">Visual C++ Example</link>
        <link xlink:href="6b699f2b-e5c7-4584-ab25-663a9243d30e">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>
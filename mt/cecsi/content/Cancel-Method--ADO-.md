---
title: "Cancel Method (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: e0db4e15-6787-41e2-8f13-9e9b524d620a
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
# Cancel Method (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="cdba83d7670a587305bacacee482194a" id="tgt1" class="tgtSentence">Cancels execution of a pending asynchronous method call.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>object</parameterReference>
          <legacyBold>.Cancel</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="1f3b3c11bbd9c0642696efb1a7167578" id="tgt2" class="tgtSentence">Use the <legacyBold>Cancel</legacyBold> method to terminate execution of an asynchronous method call: that is, a method invoked with the <legacyBold>adAsyncConnect</legacyBold>, <legacyBold>adAsyncExecute</legacyBold>, or <legacyBold>adAsyncFetch </legacyBold>option.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="290feeeefdf193aee340f2b575704be1" id="tgt3" class="tgtSentence">The following table shows what task is terminated when you use the <unmanagedCodeEntityReference>Cancel</unmanagedCodeEntityReference> method on a particular type of object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c79bf6b78f88b625b9789dbd133095da" id="tgt4" class="tgtSentence">If <legacyItalic>object</legacyItalic> is a</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c1dc3fc50d2ac43448338ac6829b465a" id="tgt5" class="tgtSentence">The last asynchronous call to this method is terminated</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="555f9a06d38c9a7f1e0ed6e8c26a7c6d" id="tgt6" class="tgtSentence">
                      <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="355e6ce6705dd124cd2aba662895a99c" id="tgt7" class="tgtSentence">
                      <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="229994e8f1e8bb43ef4e490f160fdd57" id="tgt8" class="tgtSentence">
                      <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5a0f482bf3089b345bff63e5a456c168" id="tgt9" class="tgtSentence">
                      <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> or <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b1ccf905a960737c5efc1fe367730619" id="tgt10" class="tgtSentence">
                      <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="719c37a387b14a8cd65fac25f6cb0729" id="tgt11" class="tgtSentence">
                      <legacyLink xlink:href="b9bcf272-3c74-479f-95dd-0229a32e98fc">CopyRecord</legacyLink>, <legacyLink xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord</legacyLink>, <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord</legacyLink>, or <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d74900fa26cfe1b94abd1519b4f578cd" id="tgt12" class="tgtSentence">
                      <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="79f1d4e12b864d00d708b5caf7ee6da2" id="tgt13" class="tgtSentence">
                      <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="de0565f6045c90f4e8a342841fd36088" id="tgt14" class="tgtSentence">
                      <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ce13356234dd8a50e856275376adaf84" id="tgt15" class="tgtSentence">
                      <legacyLink xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt16" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5c0530ad-68d0-4cba-b1af-9386d566c7c5">Visual Basic Example</link>
        <link xlink:href="4ade106d-063d-486e-bc4d-a1a6b6e0bea9">VBScript Example</link>
        <link xlink:href="7e0eaa39-0c24-4d8c-87e8-f9c4fd3455e7">Visual C++ Example</link>
        <link xlink:href="3e41ee6f-5138-4d32-98ac-05e30a2a6fd2">Visual J++ Example</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
        <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Cancels execution of a pending asynchronous method call.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
          <parameterReference>object</parameterReference>
          <legacyBold>.Cancel</legacyBold>
        </legacySyntax>
      </syntaxSection>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Use the <legacyBold>Cancel</legacyBold> method to terminate execution of an asynchronous method call: that is, a method invoked with the <legacyBold>adAsyncConnect</legacyBold>, <legacyBold>adAsyncExecute</legacyBold>, or <legacyBold>adAsyncFetch </legacyBold>option.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">The following table shows what task is terminated when you use the <unmanagedCodeEntityReference>Cancel</unmanagedCodeEntityReference> method on a particular type of object.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">If <legacyItalic>object</legacyItalic> is a</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">The last asynchronous call to this method is terminated</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">
                      <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">
                      <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">
                      <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">
                      <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> or <legacyLink xlink:href="663defab-5545-4973-9036-24d5882c9737">Open</legacyLink></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">
                      <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">
                      <legacyLink xlink:href="b9bcf272-3c74-479f-95dd-0229a32e98fc">CopyRecord</legacyLink>, <legacyLink xlink:href="2726498c-dbd8-4266-983b-ae7d62c39142">DeleteRecord</legacyLink>, <legacyLink xlink:href="6d2807b0-b861-4583-bcaf-fb0b82e0f2d0">MoveRecord</legacyLink>, or <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">
                      <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">
                      <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">
                      <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">
                      <legacyLink xlink:href="d26f48fb-904e-4932-a245-3b4332ca1600">Open</legacyLink>             </caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
                  </para>
                </TD>
                <TD>
                  <para> </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5c0530ad-68d0-4cba-b1af-9386d566c7c5">Visual Basic Example</link>
        <link xlink:href="4ade106d-063d-486e-bc4d-a1a6b6e0bea9">VBScript Example</link>
        <link xlink:href="7e0eaa39-0c24-4d8c-87e8-f9c4fd3455e7">Visual C++ Example</link>
        <link xlink:href="3e41ee6f-5138-4d32-98ac-05e30a2a6fd2">Visual J++ Example</link>
        <link xlink:href="560b5b3d-fba9-4275-8920-9c3e186134f7">Cancel Method (RDS)</link>
        <link xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch Method</link>
        <link xlink:href="eaa856cc-c786-462e-890c-c896261b1741">CancelUpdate Method</link>
        <link xlink:href="76d8a6e9-bc6c-4ea0-8e7a-2bae5ed06650">CancelUpdate Method (RDS)</link>
        <link xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute Method (ADO Command)</link>
        <link xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute Method (ADO Connection)</link>
        <link xlink:href="663defab-5545-4973-9036-24d5882c9737">Open Method (ADO Connection)</link>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
      </relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>